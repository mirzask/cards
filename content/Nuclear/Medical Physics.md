---
tags:
  - nuclear
---

- Radioactivity occurs when we have an instability in the nuclear structure of an atom. There's several different ways in which this can happen:
	- ![[Medical Physics-20240816210957822.webp]]
	- Change in the number of **protons** at the center (i.e. change in $Z$)
		- Not only would we add protons or lose protons, but we're also *changing the chemical nature*.
		- 3 major processes that this can occur:
			- **Alpha decay**
				- Where a cluster of protons and neutrons (e.g. ${}^4_2 \text{He}$) are expelled from the nucleus.
					- ![[Medical Physics-20240816211024316.webp|425]]
				- Common in very large atoms, such as uranium and plutonium.
			- **Beta decay**
				- Where either a proton sheds a positron (or a neutron sheds an electron), i.e. shed a little bit of charge either in the positive sense or in the negative sense → Z increases or decreases by 1, respectively, but A remains unchanged.
				- Does NOT change the number of nucleons, but it does change the amount of charge in the center of the nucleus.
			- **Electron Capture**
				- Electron cloud passes close by a large nucleus → grabs an electron from the electron cloud + a proton is changed to a neutron
	- Isomeric transitions: No change in the number of protons, i.e. no change in $Z$
		- **Gamma Decay**
			- We have an atom that maybe starts to raise its energy state → goes to a low energy state with no change in the number of nucleons or the number of protons at the center of it, but gives off energy and conserves energy → produces a <u>gamma ray</u> that then detected by the system
- Calculating the number of radioactive atoms in a sample
	- Is proportional to the number of atoms present
	- The change in the number is proportional to a constant ($k$, sometimes written as $\lambda$) times the number that's present. When we integrate that we end up with the familiar exponential decay.
	- $\frac{dN}{dt} = -kN$ → Integration of this is $\int \frac{dN}{N} = -k \int dt$
	- $N = N_0 \cdot \exp({-kt})$
	- Example: We have a five millicary (mCi) dose of technitium that spilled on the floor carpet in the in a laboratory. And with a half life of 72 hours, how long must we wait to reach 1/1,000th of the activity remaining?
		- $\text{Dose} = \text{Dose}_0 \cdot \exp(\frac{-t \cdot \ln(2)}{t_{1/2}})$
		- $t = \frac{t_{1/2}}{\ln(2)} \cdot \ln(1,000)$ = 717 hours

# Compton Scattering

- The way that Compton scattering takes place is an **incident photon** scatters off an electron in the electron cloud and the photon heads off in a new direction and kicks out an electron into the media.
	- ![[Medical Physics-20240816211105568.webp|482]]
- The amount of energy change is determined by the **Compton formula**.
	- The new energy is largely determined by the <u>incident energy</u> and the <u>angle</u>.
	- Higher incident energy → bigger energy change energy change
	- Higher unit angle → bigger energy change
- Example: A technologist opens the 140 keV photon window to +/-14 keV (20%). What is the minimum single scattering angle that the energy window can reject (assume perfect energy resolution and $mc^2$ = 511 keV?
	- See 18 minutes mark in lecture 1

