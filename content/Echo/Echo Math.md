---
tags:
  - echo
---

# Hydraulic Orifice Formula
![[Echo Math-20240731133827802.webp|416]]


$$
\text{Flow rate} = \text{Area} \times \text{Velocity}
$$
$$
\text{Volume} = \text{Area} \times \text{Velocity Time Integral (VTI)}
$$

# Stroke Volume

$$
\text{SV} = \text{Area}_{\text{LVOT}} \times \text{VTI}_{\text{LVOT}}
$$
$$
\text{Area}_{\text{LVOT}} = \pi \cdot \frac{(\text{LVOT diameter})^2}{2} = 0.785 \times (\text{LVOT diameter})^2
$$
Thus,
$$
\text{SV} = 0.785 \times (\text{LVOT diameter})^2 \times \text{VTI}_{\text{LVOT}}
$$

# Echo-Based Qp/Qs ([[Intracardiac Shunts]])

$$
\frac{Q_p}{Q_s} = \frac{\text{SV}_{\text{RVOT}}}{\text{SV}_{\text{LVOT}}} = \frac{(\text{Area}_{\text{RVOT}} \times \text{VTI}_{\text{RVOT}})}{(\text{Area}_{\text{LVOT}} \times \text{VTI}_{\text{LVOT}})}
$$

# Cardiac Output

$$
\text{CO} = \text{HR} \times \text{SV}
$$

# Cardiac Index

$$
\text{CI} = (\text{SV} \times \text{HR})/\text{BSA}
$$

```python
def calculate_hemodynamics(vti_lvot, lvot_diameter, heart_rate, bsa, 
                           sbp, dbp, est_rap):
    stroke_volume = 0.785 * (lvot_diameter ** 2) * vti_lvot
    svi = (stroke_volume / bsa) if bsa != 0 else 0
    cardiac_output = stroke_volume * heart_rate
    cardiac_index = cardiac_output / bsa
    map = (sbp + (2 * dbp)) / 3
    svr = (map - est_rap) / cardiac_output
    return stroke_volume, svi, cardiac_output, cardiac_index, svr
```

# Continuity Equation for Aortic Valve Area

- Echo Measurements (ASE guidelines)
	- View: PLAX, zoomed up view
	- Inner-edge to inner-edge in **mid-systole**
	- Make measurements parallel and adjacent to the aortic valve *or* at the site of velocity measurement within 5 mm of the aortic annulus (where you'll likely be assessing LVOT VTI)

**Continuity Equation** is based on the preservation of flow. In other words, the flow through the aortic valve will be equal to the flow through the LVOT. This translates into $\text{AV stroke volume = LVOT stroke volume}$.

Consider fluid moving through a tube: the flow at point $x$ is the same as point $y$ if the size at each of the two points is the *same*. But, if the diameter of the tube at $x$ is 1/2 that of $y$, then the flow at $x$ will be double that at $y$.
$$
\text{Aortic Valve Area (AVA)} = \frac{\text{LVOT area} \times \text{LVOT VTI}}{\text{AV VTI}}
$$
From the Mayo Board Review course, which highlights the importance of assessing for the AV VTI from *multiple windows*‼️

![[Echo Math-20240731135211518.webp|552]]

```python
def calculate_aortic_stenosis(vmax, vti_lvot, vti_ao, lvot_diameter):
    mean_gradient = 4 * (vmax ** 2)
    stroke_volume = 0.785 * (lvot_diameter ** 2) * vti_lvot
    ava = (stroke_volume / vti_ao) if vti_ao != 0 else 0
    return mean_gradient, stroke_volume, ava
```

# Systemic Vascular Resistance (SVR)

$$
\text{SVR} = \frac{\text{MAP - CVP}}{\text{CO}}
$$

Using IVC collapsibility indices to estimate RAP, and arm blood pressure measurements to calculate mean arterial pressure, SVR (in Wood units) can be calculated as

$$
\text{SVR} = \frac{\text{MAP} - \text{RAP}}{\text{CO}}
$$


# Pulmonary Vascular Resistance (PVR)

$$
\text{PVR} = \frac{\text{mean PAP - PCWP}}{\text{CO}}
$$
Using Echo hemodynamics, you may also be able to calculate PVR with the following equation:
$$
\text{PVR} = \bigg( \frac{V_{\text{TR}}}{\text{VTI}_{\text{RVOT}}} \bigg) \cdot 10 + 0.16
$$


# [[Pressure Half Time (PHT)]]

$$
\text{PHT} = 0.29 \times \text{Deceleration Time (DT)}
$$
## [[Pressure Half Time (PHT)#Mitral Valve Area (MVA) from PHT|Mitral Valve Area (MVA) from PHT]]

$$
\text{Mitral Valve Area (MVA)} = \frac{220}{\text{PHT}}
$$

# Modified Bernoulli Equation for Pressure Gradients

These often involve measuring a pressure gradient across a "leaky" structure (e.g. [[Tricuspid Regurgitation|TR]], [[Ventricular Septal Defect (VSD)|VSD]], [[Patent Foramen Ovale|PFO]], [[Patent Ductus Arteriosus|PDA]], etc.), where we are measuring the maximal gradient between two different pressures of the heart that are separated by the "leaky" structure. For example, in the case of [[Tricuspid Regurgitation|TR]], we are measuring the gradient between the RA and RV. Importantly, maximal regurgitation gradient isn't all that helpful WITHOUT a reference point, and in Echo these often will be RAP, SBP, DBP.

| Structure       | Gradient Between |
| --------------- | ---------------- |
| Tricuspid Valve | RA + RV          |
| Pulmonic Valve  | RV + PA          |
| Mitral Valve    | LA + LV          |
| Aortic Valve    | LV + Aorta       |
| VSD             | LV + RV          |
| PFO             | LA + RA          |

## RV Systolic Pressure (RVSP)

$$
\text{RVSP} = \text{RAP} + (4 \cdot {V_{\text{TR}}}^2)
$$

![[Echo Math-20240807155941577.webp]]

In the case of [[Ventricular Septal Defect (VSD)]], the RVSP can be calculated using the following formula:
$$
\text{RVSP} = \text{SBP} - (4 \cdot {V_{\text{Systolic VSD}}}^2)
$$
For example, patient with late-presenting STEMI and found to have [[Ventricular Septal Defect (VSD)|VSR]]. BP was 114/74 mmHg and VSD Doppler tracing below. What is their RVSP? $\text{RVSP} = 114 - (4 \cdot 4^2) = 114 - 64 = 50$.
![[Echo Math-20240807165057788.webp]]
## LV End-Diastolic Pressure (LVEDP)


$$
\begin{align}
\text{LVEDP} &= \text{Aorta DP} - (4 \cdot {V_{\text{End Aortic Regurg}}}^2) \\
&= \text{DBP} - (4 \cdot {V_{\text{End Aortic Regurg}}}^2)
\end{align}
$$
📝 We use DBP as a proxy for aorta diastolic pressure.

![[Echo Math-20240807164119404.webp|544]]
In the above Doppler tracing, $V_{\text{End Aortic Regurg}}$ is 2 m/s. This example also illustrates the 'a-dip' that can sometimes be seen with [[Aortic Regurgitation]].

## PA End-Diastolic Pressure (PAEDP)

$$
\text{PAEDP} = \text{RAP} + (4 \cdot {V_{\text{End Pulm Regurg}}}^2)
$$
📝 Technically, you'll want to use RVEDP in place of RAP. However, physiologically RAP = RVEDP, so it should work to use RAP instead.

## Left Atrial Pressure (LAP)

$$
\begin{align}
\text{LAP} &= \text{LV}_{\text{systolic}} - (4 \cdot {V_{\text{MR}}}^2) \\
&= \text{SBP} - (4 \cdot {V_{\text{MR}}}^2)
\end{align}
$$
📝 We can't easily measure $\text{LV}_{\text{systolic}}$, so we use SBP as a surrogate 👆as the two values should be similar.

For example, a patient with peak mitral valve gradient of 3 m/s and BP of 100/54. The LAP would be $100 - 4 \cdot 3^2 = 64$ mmHg!

In the setting of a [[Patent Foramen Ovale|PFO]], the LAP can be estimated using the following formula:
$$
\text{LAP} = \text{RAP} + (4 \cdot {V_{\text{PFO}}}^2)
$$
# Proximal Isovelocity Surface Area (PISA)

- Exploits Doppler color flow aliasing.
- As fluid in a container goes through a *narrow* orifice, the velocity ↑. With PISA, we take advantage of this phenomenon by shifting our Doppler baseline in the direction of flow. This exposes these "hemispheres" that correspond to different velocities that we can use to calculate regurgitant/stenotic flow.
- The flow at the PISA should be equal to the flow at the narrowest portion, which is termed the **effective regurgitant orifice (ERO)**; the area of which is referred to as the ERO area (or EROA)

$$
\begin{align}
\text{Flow at PISA} &= \text{Flow at ERO} \\
\text{Area} \times \text{Velocity of PISA} &= \text{EROA} \times \text{Velocity of Regurgitant Jet}
\end{align}
$$

## PISA for Regurgitation


> [!tip]- Direction of PISA radius measurement
> You will draw the line for PISA radius calculation towards **the direction of the ultrasound beam**
> ![[Echo Math-20240807171015934.webp]]

$$
\text{EROA} = \frac{2 \pi \cdot {r_{\text{PISA}}}^2 \cdot \text{Aliasing velocity}}{V_{\text{max}}}
$$
$$
\text{Regurgitant Volume} = \text{EROA} \times \text{VTI}_{\text{Regurg}}
$$
## PISA for Stenosis

$$
\text{MVA} = \bigg( \frac{2 \pi \cdot {r_{\text{PISA}}}^2 \cdot \text{Aliasing velocity}}{V_{\text{max}}} \bigg) \times \frac{\alpha}{180}
$$



