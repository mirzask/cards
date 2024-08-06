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

# Continuity Equation for Aortic Valve Area

- Echo Measurements (ASE guidelines)
	- View: PLAX, zoomed up view
	- Inner-edge to inner-edge in **mid-systole**
	- Make measaurements parallel and adjacent to the aortic valve *or* at the site of velocity measurement within 5 mm of the aortic annulus (where you'll likely be assessing LVOT VTI)

**Continuity Equation** is based on the preservation of flow. In other words, the flow through the aortic valve will be equal to the flow through the LVOT. This translates into $\text{AV stroke volume = LVOT stroke volume}$.

Consider fluid moving through a tube: the flow at point $x$ is the same as point $y$ if the size at each of the two points is the *same*. But, if the diameter of the tube at $x$ is 1/2 that of $y$, then the flow at $x$ will be double that at $y$.
$$
\text{Aortic Valve Area (AVA)} = \frac{\text{LVOT area} \times \text{LVOT VTI}}{\text{AV VTI}}
$$
From the Mayo Board Review course, which highlights the importance of assessing for the AV VTI from *multiple windows*‼️
![[Echo Math-20240731135211518.webp|552]]

# Systemic Vascular Resistance (SVR)

$$
\text{SVR} = \frac{\text{MAP - CVP}}{\text{CO}}
$$
# Pulmonary Vascular Resistance (PVR)

$$
\text{PVR} = \frac{\text{mean PAP - PCWP}}{\text{CO}}
$$
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

## RV Systolic Pressure (RVSP)

$$
\text{RVSP} = \text{RAP} + (4 \cdot {V_{\text{TR}}}^2)
$$
$$
\text{RVSP} = \text{SBP} - (4 \cdot {V_{\text{Systolic VSD}}}^2)
$$

## LV End-Diastolic Pressure (LVEDP)

$$
\text{LVEDP} = \text{DBP} - (4 \cdot {V_{\text{End Aortic Regurg}}}^2)
$$
## PA End-Diastolic Pressure (PAEDP)

$$
\text{PAEDP} = \text{RAP} + (4 \cdot {V_{\text{End Pulm Regurg}}}^2)
$$

## Left Atrial Pressure (LAP)

$$
\text{LAP} = \text{SBP} - (4 \cdot {V_{\text{MR}}}^2)
$$
$$
\text{LAP} = \text{RAP} + (4 \cdot {V_{\text{PFO}}}^2)
$$
# Proximal Isovelocity Surface Area (PISA)

## PISA for Regurgitation

$$
\text{ERO} = \frac{2 \pi \cdot {r_{\text{PISA}}}^2 \cdot \text{Aliasing velocity}}{V_{\text{max}}}
$$
$$
\text{Regurgitant Volume} = \text{ERO} \times \text{VTI}_{\text{Regurg}}
$$
## PISA for Stenosis

$$
\text{MVA} = \bigg( \frac{2 \pi \cdot {r_{\text{PISA}}}^2 \cdot \text{Aliasing velocity}}{V_{\text{max}}} \bigg) \times \frac{\alpha}{180}
$$



