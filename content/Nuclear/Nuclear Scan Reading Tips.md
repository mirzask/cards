---
tags:
  - nuclear
---

# Reporting Flows

- Post-CABG you divide circulation between native and graft circulation. In the native circulation, physiology rapidly deteriorates (→ low flow). So we will typically see greater amounts of calcification in native circulation and low flow. This is not a reflection of graft closure, rather it is progression of native disease post-CABG.
	- ⚠️ Be careful about reporting flows post-CABG so that referring doctor is not concerned about low flows and inadvertently sending patient to cath lab. If normal, Bateman will report them. If not normal (especially globally), it is probably best to not report them.
		- 'Not reported because not clinically relevant.'
- Other conditions where reporting flows may not be clinically relevant would be liver failure, renal failure.
- In patients with cirrhosis/ESLD, our protocol is to have them do [[Dobutamine]] (instead of [[Pharmacologic Stressors#Vasodilators|vasodilators]] like [[Pharmacologic Stressors#Regadenoson (Lexiscan)|regadenoson]])

## `Snapshot`

![[Nuclear Scan Reading Tips-20241104100237310.webp|611]]

- Steps:
	- At $t_0$, tracer has has not entered the heart
	- At the peak it has entered the heart
	- At the plateau, it has now entered the myocardium
- Initially, counts higher in blood pool than myocardium → then flips
	- So at the peak, the green curve will be highest
- In the **plateau phase**, the signal-to-noise reflects the counts in <font color="#245bdb">myocardium</font> (blue) and <font color="#c00000">blood pool</font> (red)
- Resting flows can be documented as high if the graph starts at $t_0$ is above 0.
- Blood pool is in red.
- Generally rest blood pool is 30% higher than peak stress.
	- If < 30%, then potentially problematic for flow calculation
- Compartment models are more sensitive if the QC is problematic.

# Quality Control
## `Slice`

- On the left and right side of the screen, you can shift the cyan colored lines to intersect your short axis views to make sure you are looking at appropriate cuts to represent apical, mid- and basal views.
## Misregistration

- Let's say that the LV is not correctly drawn, you can manually adjust the registration:
	- In the `Slice` tab, select the `Manual` button in the top row
	- Edit things to your liking
	- Click `Mask` and `Constrain`
	- Lastly, click the `Process` button at the top row

## `QGS`

- Sanity check for EF estimation
	- Look at the curve on the right
		- ![[Nuclear Scan Reading Tips-20241106114346810.webp|491]]
	- The <font color="#c00000">red line</font> should be 'V-shaped' (makes sense as you go between diastole-systole-diastole).
		- In reality, I've mostly seen it more U- than V-, but the point is that there should be a distinct trough/inflection point.
		- As you can imagine, [[Atrial Fibrillation|AFib]] can sometimes be finnicky.
	- ⚠️ Data support that EF can be reported a little higher when using 16 vs 8 frames/second.

## `Fusion`

- Look for splenic shutoff

# [[Single-photon emission computed tomography (SPECT)|SPECT]]

- In Cedars, scans that end with `_AC` are [[Attenuation Correction (AC)|attenuation corrected]] and scans that end with `_SC` are **scatter corrected**.
- In the `QPS` tab, selecting `Prompt+` will overlay the supine and upright images
	- 🤔 Does the defect go away when the images are overlaid?

## QC for [[Single-photon emission computed tomography (SPECT)|SPECT]]

- Click the `Raw` tab at the top
	- Appreciate the appearance of the heart
		- You may also notice pleural/pericardial effusion and uptake elsewhere, e.g. infection/pneumonia, tumor, etc.
	- Perfusion pattern
	- Artifacts
		- Bouncing heart
		- Lateral wall motion/Lateral wall hot spot
		- Diaphragmatic attenuation
		- Breast attenuation
		- Upward creep - may be seen if a patient hops onto the scanner shortly after exercise. Due to the diaphragm going up and down as the patient is huffing and puffing following exercise.
			- This is why some protocols will have patient wait ~15 mins post-exercise
- Inspect the **sinogram**, **linogram**
	- ![[Nuclear Scan Reading Tips-20241106115329022.webp]]
- "Hurricane sign" is suggestive of motion artifact on [[Single-photon emission computed tomography (SPECT)|SPECT]]
	- ![[Nuclear Scan Reading Tips-20241106115153990.webp|260]]

# CT scans

- Look at the scout film (`Tomogram` or `Scout`)
- If IDA, then HU can be <25-30 HU
- [[Mitral Annular Calcification (MAC)]]
- Look for anomalous coronaries
- Look for enlargement of heart structures, e.g. atrium, ventricles, coronary sinus
- Can also try to get a sense of dominance, e.g. large LCx feeding or RCA
- Switching to MIP (instead of MPR) will allow you to see lung nodules better
- Reporting
	- If lung nodule is < 6 mm, then probably don't need to report (unless there are a bunch, etc.)
	- If nodule(s), then "Recommend standard acquisition full lung CT"
- Lymphadenopathy
- Hernias: hiatal, Morgagni, Bochdalek, etc.
- Dilation, e.g. atrial, aortic root, etc.
- Lipomatous hypertrophy of interatrial septum