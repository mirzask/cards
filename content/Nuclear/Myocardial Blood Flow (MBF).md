---
tags:
  - stresstesting
  - nuclear
aliases:
  - MBF
  - MBFR
---
- [[Positron Emission Tomography (PET)|PET]] measurement of MBF assesses the entire coronary circulation, including focal obstruction and diffuse disease of the epicardial coronary arteries, the functioning of the microvasculature(‼️), and the ability of the cell membrane to transport the radionuclide into the cell.
	- Yes, MBF can be useful for detection of [[Microvascular Dysfunction|coronary microvascular disease]]
- Interpretation of myocardial perfusion imaging (MPI) studies has been primarily qualitative or semi-quantitative in nature, assessing regional perfusion defects in relative terms. Quantitative positron emission tomography (PET) measurements of myocardial blood flow (MBF) in absolute terms (milliliters per gram per minute) offer a paradigm shift in the evaluation and management of patients with CAD.[^asnc]
	- Coincides with shift from anatomical gold standard (i.e., coronary angiogram) to a functional one
- Non-invasive quantification of MBF extends the scope of conventional MPI from detection of end-stage, advanced, and flow-limiting epicardial CAD to early stages of atherosclerosis or microvascular dysfunction and assessment of balanced reduction of MBF in all three major coronary arteries.[^asnc]
- Useful to couple MPI with [[Cardiac PET Imaging#Quantification of Myocardial Blood Flow|quantification of myocardial blood flow (MBF)]] as MBF adds usefulness in 6 distinctive areas: [^bateman]
	- Improved diagnosis of epicardial CAD
	- Improved assessment of extent and severity of epicardial CAD
		- Traditional [[Single-photon emission computed tomography (SPECT)|SPECT]] or [[Positron Emission Tomography (PET)|PET MPI]] detects obstructive CAD but potentially under-assesses CAD extent and severity.
	- Improved risk stratification
	- Improves selection of patients for coronary interventions and/ or medical therapy
	- Can identify [[Microvascular Dysfunction|Coronary Microvascular Dysfunction]]
		- Diagnosis of **[[Microvascular Dysfunction|coronary microvascular disease]]**, with or without epicardial CAD, has prognostic and quality of life significance in both women and men, and is addressable by targeted therapies.
	- Provides assurance that vasodilator stress has been effective
		- Confirmation of adequate pharmacologic stress in patients who may not respond to pharmacologic stressors and go totally unrecognized with traditional MPI, with the risk of an apparently normal scan in the presence of severe coronary disease. The only way to be certain that vasodilation and hence augmentation of blood flow has occurred is by measuring MBF.


# Coronary Flow Reserve (CFR)

Myocardial Blood Flow Reserve (MBFR) is the ratio of peak hyperemia to resting myocardial blood flow. MBFR adds diagnostic and prognostic information over MPI data.
$$
\text{CFR} = \frac{\text{stress MBF}}{\text{rest MBF}}
$$
- Coronary flow reserve (CFR), the ratio of maximal myocardial blood flow (MBF) during pharmacologically-induced coronary vasodilation to resting MBF, is an integrated measure of flow through both the large epicardial coronary arteries and the microcirculation.
	- The calculation of CFR assumes that maximal vasodilatation is achieved, which is done by abolishing coronary vasomotor tone, often with vasodilators like Regadenoson. For invasive CFR determination in the cath lab, this is often obtained following intravenous [[Adenosine|adenosine]] administration.
- Indirect parameter to evaluate the function of the coronary circulation
- Impairment is a strong predictor of CV mortality
- ⚠️ High resting flows, e.g. d/t ↑ BP, may *falsely* lower your CFR measurement
	- Resting MBF has a linear relationship with cardiac work, and CFR is influenced by metabolic demand, diastolic time, and driving blood pressure. ∴, when comparing different patients, resting MBF values must be corrected to take into account the main determinants of external cardiac workload, namely SBP and HR (rate-pressure product)

$$
\begin{align}
\text{Rate-pressure Product (RPP)} = \text{HR} \times \text{SBP} \\
\text{Corrected CFR} = \frac{\text{stress MBF}}{\text{rest MBF} \times \frac{10,000}{\text{RPP}}}
\end{align}
$$
```python
def calculate_mbfr(MBF_stress, MBF_rest, hr=None, sbp=None):
  """Calculates myocardial blood flow reserve (MBFR).

  Args:
    MBF_stress: Blood flow during hyperemic conditions (mL/min/g).
    MBF_rest: Blood flow at rest (mL/min/g).
    HR: heart rate (bpm), optional
    SBP: systolic blood pressure (mmHg), optional

  Returns:
    MBFR as a float.
  """

  if MBF_rest <= 0:
    return "Error: Resting blood flow cannot be zero."
  elif hr is not None and sbp is not None:
      rpp = hr * sbp
      mbfr = MBF_stress / ( MBF_rest * (9000/rpp) )
      return mbfr
  else:
      mbfr = MBF_stress / MBF_rest
      return mbfr

# Example
MBF_stress = 1.7
MBF_rest = 1.1
HR = 95
SBP = 160

calculate_mbfr(MBF_stress, MBF_rest)
calculate_mbfr(MBF_stress, MBF_rest, HR, SBP)
```

> [!NOTE] MBF is _dynamic_ and responds to ∆ in myocardial work
> The two main determinants of myocardial work are **heart rate** and **systolic blood pressure**.


- In the absence of obstructive stenosis of the epicardial arteries, reduced CFR is a marker of [[Microvascular Dysfunction|Coronary Microvascular Dysfunction]], but because obstructive disease of the epicardial arteries and [[Microvascular Dysfunction|CMD]] often coexist, discrimination between the effects of these two conditions on myocardial perfusion is challenging. [^cmd-natrev]


# Quality Control of Myocardial Blood Flow

- ⚠️ Interpreting physicians should never accept a MBF value without review of simple quality control metrics. The quality control evaluation is an essential first step in the decision whether to report the MBF measurement.[^bateman]
- Quality Control [^bateman]
	- review the co-registration of emission and transmission scans, 
		- assess the transaxial, coronal, and sagittal views
		- Any required correction of misalignment must be performed on the PET scanner console with repeat reconstruction after proper alignment
	- review the placement of the blood pool and myocardial ROIs
		- ![[Myocardial Blood Flow (MBF)-20240815224421512.webp]]
		- blood pool ROIs should be in the same location for rest and stress and should not touch the walls of either the left atrium or the left ventricle to avoid spillover
		- myocardial ROIs also must accurately encompass the myocardium during all frames that will be used for determining the tracer uptake. This ROI needs to be inspected to ensure that it is accurately tracing the myocardium and excludes adjacent non-cardiac structures that may contain tracer.
	- review both rest and stress blood pool and myocardial time-activity curves
		- The blood pool and myocardial activity curves should start at zero (at least one background frame prior to radiotracer infusion) and have single peaks (multiple peaks suggest patient motion, radiotracer infusion issues, or detector saturation).
	- ⚠️ If the quality review fails, an attempt at correction can be considered; if correction is not feasible, then the values should not be reported.


# Quantification of Myocardial Blood Flow Reserve

> [!warning] Be careful about interpretation in Low EF and CABG
> the accuracy and utility of quantitative assessment of myocardial blood flow have not been adequately tested in patients with low ejection fraction (EF) or prior coronary artery bypass graft surgery (CABG).


$$
\text{Flow Reserve} = \frac{\text{Peak stress flow}}{\text{Rest flow}}
$$

Myocardial Blood Flow Reserve (MBFR) > 2 is normal

**General interpretation and classification of risk in relation to global MBFR** [^bateman]

| MBFR                            |        Interpretation         | Relative risk |
| ------------------------------- |:-----------------------------:|:-------------:|
| >2                              |            Normal             |      Low      |
| 1.7-2                           |        Mildly abnormal        | Intermediate  |
| 1.2—< 1.7                       |           Abnormal            |     High      |
| <1.2 with a perfusion defect    |        Highly abnormal        |   Very high   |
| <1.2 without a perfusion defect | Consider non-diagnostic study | Indeterminate |

- Resting flows
	- ranges from 0.4 to 1.2 mL/min/g
	- In general, varies with myocardial workload with higher MBF in patients with ↑ HR or BP
	- Regions of infarction often have low resting flows.
	- MBF in regions of predominant infarction may increase proportionally with vasodilation, such that MBFR appears normal. Usually, peak MBF remains low.
	- **Tip**: MBFR in regions of predominant infarction may be normal or possibly high which can be misleading and affect global MBFR values. In such cases, the focus of MBFR reporting should be more on non-infarct territories.
- $\text{MBFR} = \frac{\text{stress MBF}}{\text{rest MBF}}$
	- Considerations:
		- abnormally low MBFR if HR/BP significantly ↑ (e.g. held meds for study) b/c resting MBF is unusually elevated
- By combining the interpretation of stress MBF with MBFR, i.e., normal *stress* MBF and low MBFR due to high *rest* MBF may still be interpreted as normal. 
	- Very high resting MBFs out of proportion to the RPP should raise suspicion of detector saturation.


## Clinical value of myocardial blood flow reserve

| CAD          | Clinical Value                                                                                                                                                                                                                                                                                                                                                                                                         |
| ------------ | ---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------- |
| No known CAD | - High negative predictive value in combination with normal perfusion<br>- Confirm an abnormality is CAD<br>- Predict more severe disease: e.g., 1-vessel abnormal perfusion, 2-3-vessel abnormal MBFR<br>- Confirm single vessel disease: 1 vessel abnormal perfusion, 1 vessel abnormal MBFR Normal perfusion, abnormal MBFR: identify balanced CAD, microvascular disease<br>- Identify non-responder: all patients |
| Known CAD    | - Often abnormal after CABG, CAD history, myocardial infarction<br>- Cardiomyopathy less useful but if normal, helps exclude CAD<br>- Renal failure patients generally abnormal<br>- Post PCI may be abnormal, but most useful if pre-PCI data available<br>- Identify non-responder: all patients                                                                                                                     |

# Interpreting Myocardial Blood Flow Reserve

- An important value of MBFR measurement involves the reclassification of a normal MPI from low risk to high-risk study.[^bateman]
- **Global MBFR >2** has been shown in numerous studies to correlate with an excellent prognosis.[^bateman]
- *Normal* MBFR establishes <u>physiologic</u> normality of the epicardial coronaries and the microvasculature.[^bateman]
- *Low* MBFR in the setting of no known CAD will usually require further testing such as invasive coronary angiography or [[Coronary Computed Tomography Angiography (CCTA)|CCTA]] to rule out epicardial CAD. However, there will not be a 1:1 correlation of low MBFR and epicardial CAD, as some patients will have microvascular disease alone or in combination with mild-moderate epicardial CAD.[^bateman]
- The lower the MBFR the greater the likelihood of multi-vessel obstructive CAD, the worse the prognosis and the greater the likelihood of benefit from revascularization.[^bateman]

> [!NOTE] Making sense of **Normal perfusion** but **low MBFR**
> Normal perfusion with low or very low MBFR is commonly encountered. Explanations can include severe balanced flow reduction due to multivessel disease, severe microvascular disease, a combination of moderate severity epicardial disease and microvascular disease, and non-responsiveness to the vasodilator. Further testing is needed. An important first step is establishing whether inhibitors such as caffeine might have affected test results. If this seems unlikely, a CACS would be very useful in deciding whether invasive coronary angiography or CTA should be next steps.

- Making sense of discordant findings where images appear visually and semi-quantitatively normal but MBFR is low or very low. 
	- This result can be reflective of any of 4 pathophysiologies: 
		- multivessel CAD,
		- coronary microvascular disease, (See Case 4 from [^bateman])
			- more likely if low [[Coronary Artery Calcium (CAC)|CAC]]
		- a combination of moderate diffuse epicardial CAD and coronary microvascular disease, or
		- a circulating pharmacologic stress inhibitor (most commonly caffeine-containing substances) (See Case 3 from [^bateman])
	- [[Coronary Artery Calcium (CAC)]]
		- high CAC → invasive coronary angiography to differentiate epicardial CAD from microvascular disease
		- low CAC → [[Coronary Computed Tomography Angiography (CCTA)|CCTA]] or no further testing may be recommended


# Reporting [[Myocardial Blood Flow (MBF)]]

- Because MBF measurements may be unfamiliar to referring physicians, the way in which they are reported needs to be sufficiently instructive that the measurement has clinical meaning.[^bateman] (See [[Myocardial Blood Flow (MBF)#Examples of useful sentences for reporting PET MBFR|Examples of useful sentences for reporting PET MBFR]])
- ⚠️ The interpreting physician should recognize that MBFR calculations maybe less helpful in patients with prior CABG, prior large infractions, and ESRD. In addition, the calculation will be invalid in the presence of severe [[Mitral Regurgitation|mitral]] or [[Aortic Regurgitation|aortic regurgitation]].

## Examples of useful sentences for reporting PET MBFR

Source: [^bateman]
- Description
	- There was a rise in MBF between rest and stress
	- There was no rise in MBF between rest and stress
	- Global MBFR was ## (fill in number, e.g. 2.06)
- Conclusion
	- Normal MBFR confirms study normalcy, which indicates lower risk of CAD beyond normal perfusion and predicts a low risk for major coronary-related events
	- Despite normal myocardial perfusion, MBFR is abnormal, placing the patient in a higher risk category for CAD and cardiac-related events in patients with no known CAD
	- There is a perfusion defect in a single coronary territory along with corresponding regional reduction in MBFR. Normal MBFR within the remainder of the myocardium makes more extensive CAD unlikely.
	- While the perfusion indicates single vessel disease, MBFR is globally reduced, raising concern for more extensive CAD.
	- The absence of a rise in MBF with normal perfusion does not exclude CAD.
	- MBFR is not reported in this patient due to technical or patient-specific concerns that can affect accuracy and inappropriate clinical decisions.

# Lung Uptake

- **Increased lung uptake** on the perfusion images, particularly when severe, may reflect severe LV dysfunction with increased LV end-diastolic and capillary wedge pressures. 
	- It can also reflect infiltrative diseases of the lungs, and can be seen in smokers. 
	- Increased lung uptake can adversely affect image quality, and in particular may interfere with interpretation of the **lateral wall**. 
	- Solution: It may be necessary to increase the time between injection and image acquisition from 4-5 minutes to 7-8 minutes.


[^asnc]: Dilsizian V, Bacharach SL, Beanlands RS, et al. ASNC imaging guidelines/SNMMI procedure standard for positron emission tomography (PET) nuclear cardiology procedures. Journal of Nuclear Cardiology. 2016;23(5):1187-1226. doi:10.1007/s12350-016-0522-3
[^bateman]: Bateman TM, Heller GV, Beanlands R, et al. Practical Guide for Interpreting and Reporting Cardiac PET Measurements of Myocardial Blood Flow: An Information Statement from the American Society of Nuclear Cardiology, and the Society of Nuclear Medicine and Molecular Imaging. Journal of Nuclear Medicine. 2021;62(11):1599-1615. doi:10.2967/jnumed.121.261989
[^cmd-natrev]: Camici, P. G., d’Amati, G., & Rimoldi, O. (2014). Coronary microvascular dysfunction: mechanisms and functional assessment. Nature Reviews Cardiology, 12(1), 48–62. https://doi.org/10.1038/nrcardio.2014.160
