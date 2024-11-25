---
tags:
  - nuclear
  - stresstesting
---

- Definition of a Radiopharmaceutical
	- A radiopharmaceutical is a radioactive compound used for the diagnosis and therapeutic treatment of human diseases.
	- There are 2 main components: 
		- a radionuclide *and* 
		- a pharmaceutical
	- Effectiveness is determined by the characteristics of both components.
- Ideal Radiopharmaceutical
	- Localization of the tracer proportional to physiologic process. Ideally 1:1.
	- Short effective half-life
		- comprised of biological and physical half-lives
	- Penetrating single peak energy
		- 30-300 keV (SPECT)
		- 511 keV (PET)
	- High target to background ratio (**contrast**)
	- Readily available
	- Inexpensive

![[Radionuclides-20241021121956887.webp|442]]
# Production of Isotropes

- Since none of these occur naturally in nature, we have to produce them in some kind of either through using an accelerator to crash atoms together *or* in a reactor to force neutrons into the nucleus to change the nuclear composition of these atoms.
- The production of radioisotopes happens either within a nuclear reactor or in an <u>accelerator</u> or <u>cyclotron</u>, and so these are called **primary sources** of radionuclide production. Then you have a <u>generator</u>, which is referred to as a **secondary source**, and so you can manipulate the atoms through either a reactor or a cyclotron and come up with an element that is then put into a secondary source, like a generator that is then transported to its location where it's going to be used.
- **Accelerator Production** ([[Cyclotron|Cyclotrons]] and accelerators)
	- Accelerate protons to force them to overcome positive charge of nucleus
	- Examples: ${}^{82}\text{Rb}$, ${}^{201}\text{Tl}$ (Thallium-201), ${}^{18}\text{F}$
	- In a cyclotron, we speed up the proton to a high energy in an accelerator in a magnetic field to pump energy onto an ion and zip it around inside → crash them into a target → either glob it onto or break apart the target to collect our final product out the other side
	- ![[Radionuclides-20240816211240221.webp|449]]
- **Reactor Production**
	- Bathe a target in neutrons (within a reactor) to add neutrons to the nucleus:
	- Examples: ${}^{\text{99m}}\text{Tc}$
	- Because neutrons don't have any charge, they can freely wander into the nucleus and then stick if they get close enough, because there's no positive/electrostatic charge to push away from the nucleus so just over time, a sample bathe in the neutrons on the reactor will gather up these these neutrons and change their nuclear state.
- **Generator Production** (secondary source)
	- Important b/c this is our source of Technetium on a local level
	- The concept of the radioisotope generator is that you have a parent isotope that was made by through a reactor or a cyclotron that decays to something that we can use in a metaphor medical purpose, and that the separation of these two is clean and efficient.
	- Examples of radioisotope generator columns include the ${}^{99}\text{Mo} \rightarrow {}^{\text{99m}}\text{Tc}$ aluminum column and the ${}^{82}\text{Sr} \rightarrow {}^{82}\text{Rb}$ column
- Radionuclide used as a tracer/probe in medicine in a form which controls its biological fate when administered to the patient
- **Extraction of radionuclides** involves the extraction of the radionuclide from the bulk of the target and its impurities.
- **Purification** involves removal of unwanted chemical and radionuclide impurities

# Reactor-Produced Isotopes


- See [[Nuclear Medicine Notation and Glossary#Glossary|Glossary]] for **[[Nuclear Medicine Notation and Glossary#Nuclear Fission|Nuclear Fission]]** and **[[Nuclear Medicine Notation and Glossary#Neutron Bombardment|Neutron Bombardment]]**
- Example of [[Nuclear Medicine Notation and Glossary#Neutron Bombardment|neutron bombardment]] vs [[Nuclear Medicine Notation and Glossary#Nuclear Fission|nuclear fission]] with the molybdenum, the parent isotope of Technetium
	- **Neutron Bombardment**
		- ${}^{98}_{42}\text{Mo}(n,\gamma){}^{99}_{42}\text{Mo}$
		- You have a neutron flux inside of a research reactor → gamma emissions coming off + you've increased the mass of molybdenum from 98 to 99.
		- **Costs less** to prepare b/c less waste product
		- Downside: **Low specific activity** compared to the fission of Uranium-235; low specific activity on the factor of at least 100 times (75 mCi/mg compared to 500 mCi/mg with fission).
		- Downside: **Low concentration**, i.e. need greater volume for the patient compared to fission.
			- When you have low specific activity, then you have to account for the volume and getting that transported to the end user.
	- **Nuclear Fission**
		- ${}^{235}_{92}\text{U}(n,f){}^{99}_{42}\text{Mo}$
			- Shorthand equation for Uranium-235 inside of a neutron flux or research reactor undergoing fission into splitting up that 235 into other components like molybdenum.
		- These reactors are research reactors, ∴ cost much more to prepare and they have much more waste that's associated with the product.
		- Upside: you have a product that can be separated from all the other production produced elements → **high specific activity** this can be chemically separated and you have specific activity of 500 mCi/mg (compared to the 75 mCi/mg with neutron bombardment).
		- Results in a **smaller column**, so you need *less shielding* and it makes it easier to transport across the country to hospitals.

# [[Cyclotron]]-Produced Isotopes

- Advantages:
	- Principle advantage is that we can have a **high specific activity**.
	- Fewer radionuclide impurities

## Thallium-201

- Thallium-201 (${}^{201}\text{TI}$)
- Introduced in the 1970s, thallium-201 (${}^{201}\text{TI}$) is a potassium analog that is actively transported across the myocardial cell membrane via Na+/K+ ATPase-dependent channels. [^imaging] 
- [[Cyclotron]] produced
- Decays through **electron capture**: 73.2 hours half-life
	- Recall, electron capture is where one of the protons grabs an electron (from an electron cloud) and sucks it into the nucleus → switches that proton to a neutron →  leaves a little vacancy of electron hole in the cloud, which then has to relax to fill that that hole because nature hates having a hole
- In the process, it produces mix of gamma rays and mercury X-rays
- Potassium analog and does not require chemistry to be converted to a usable tracer for perfusion
### Thallium-201 Protocols

- Several ${}^{201}\text{TI}$ viability protocols have been developed. [^imaging]
- **Rest-redistribution** protocols entail a rest image followed by an additional redistribution image 4 hours later with an increased tracer uptake of ≥ 10% in areas with a resting defect suggestive of viability. 
- **Stress-redistribution** protocols call for ${}^{201}\text{TI}$ stress imaging followed by 4-hour redistribution imaging. 
	- However, the accuracy of this protocol was limited, calling for further refinement with the addition of either **late redistribution** (18–24 hours) imaging ([Figure 4](https://www.ahajournals.org/doi/10.1161/HCI.0000000000000053#F4)) or a **small reinjection dose** of ${}^{201}\text{TI}$ after the 4-hour redistribution images. 
- Both techniques were similar in their ability to detect viable myocardium with a [[Precision|PPV]] of 69% and [[Negative Predictive Value|NPV]] of 89%.

![](https://www.ahajournals.org/cms/asset/751543b6-75b9-4f3b-b3ed-2e0c777cd035/hci.0000000000000053.fig04.jpg)
**Figure 4.** **Rest and 24-hour redistribution single-photon emission computed tomography (SPECT) thallium-201 (201Tl) study.** A rest (**left** column, **top** bullet plot) and 24-hour redistribution (**right** column, **bottom** bullet plot) SPECT 201Tl study demonstrates increased tracer uptake in the anterior (ANT), septal (SEPT), and apical segments after 24 hours (arrows), consistent with viable myocardium in this territory. HLA indicates horizontal long axis; INF, inferior; LAT, lateral; SAX, short axis; and VLA, vertical long axis.

# [[Radionuclide Generator|Generator]]-Produced Isotopes

- Examples of radioisotope generator columns include the ${}^{99}\text{Mo} \rightarrow {}^{\text{99m}}\text{Tc}$ aluminum column and the ${}^{82}\text{Sr} \rightarrow {}^{82}\text{Rb}$ column
- ${}^{99}\text{Mo} \rightarrow {}^{\text{99m}}\text{Tc}$ generator
	- <u>Daily</u> access to ${}^{\text{99m}}\text{Tc}$ (*short* physical $t_{1/2}$ of 6 hours)
	- <u>Once weekly</u> delivery of ${}^{99}\text{Mo}$ (*long* physical $t_{1/2}$ of 66 hours)
	- Extraction of ${}^{\text{99m}}\text{Tc}$ by simple column chromatography to make sure that the Technetium is pure
- Fission produced Uranium-235 can have many other contaminants and these are taken care of by the manufacturer
	- Molybdenum (and all of our other products) have *multiple* decay schemes, i.e. it isn't that 100% go to our compound that we want
		- ![p-49-1.jpg|387](https://nap.nationalacademies.org/openbook/23563/xhtml/images/p-49-1.jpg)

## Technetium-99

![[Radionuclides-20240816212108514.webp|526]]
The above figure depicts [[Radionuclide Generator|generator]] production of ${}^{\text{99m}}\text{Tc}$ from ${}^{99}\text{Mo}$. Here, ${}^{99}\text{Mo}$ is adsorbed onto the alumina column having two ionic charges → decays into ${}^{\text{99m}}\text{Tc}$ (or more specifically to the sodium pertechnetate form, which is $\text{Na}{}^{\text{99m}}\text{TcO}_4$), which has less affinity for the aluminum column and comes through into our elution vial. We can change the concentration of the resulting solution by adding different amounts of saline.


> [!Note] Terminology on what goes in and what comes out.
> The processing of **eluting** may also be referred to as "milking" 🐮. **Elu<u>ant</u>** refers to the eluting solution, which goes *into* the generator. **Elu<u>ate</u>** refers to the Technetium that comes off the column.

- Technetium 99m (${}^{\text{99m}}{\text{Tc}}$) based agents
- Unlike ${}^{201}\text{TI}$, ${}^{\text{99m}}{\text{Tc}}$-based agents passively diffuse across the cell membrane, where their uptake and retention depend on the maintenance of an electrochemical gradient across mitochondrial and sarcolemma membranes, and they do not demonstrate redistribution properties. [^imaging] 
- ${}^{\text{99m}}{\text{Tc}}$ favored over ${}^{201}\text{TI}$ because technetium-based agents have more favorable imaging characteristics because of higher photon energy and less radiation exposure. [^imaging] 
- [[Radionuclides#Reactor-Produced Isotopes|Reactor-produced]] version
	- We take the source and we bathe it with these additional neutrons → have a little bit more of a negative amount of the electron. 
	- But for this, there's something forbidden about this transition, which allows it to sit around for additional six hours before carrying out its decay. Buys us time to bind it to things like tetrofosmin or sestamibi or pyrophosphate and create something that is physiologically meaningful in the nuclear cardiology lab, and then ship it out to a site so we can deliver these in unit dose.
- Decays from ${}^{99}\text{Mo}$ (66 hours) to a metastable state of ${}^{\text{99m}}\text{Tc}$ (6 hours)
- Produces a single photon at 141 keV (6.007 hours)
- Must be bound to a physiologically meaningful molecule for use
- **Transient Equilibrium**
	- Theory that gives us the equation so that we can calculate the yield of technetium so that we can provide the correct amount of dosages to be taken care of all the way from a reactor to the patient.
	- Allows us to keep on track of the decay and the equilibrium process.
	- ![[Radionuclides-20240816212435966.webp|481]]
		- The horizontal slightly downsloping linear line is the line of molybdenum decay.
		- At ~23 hours is where you have a maximum activity of Technetium (${}^{\text{99m}}\text{Tc}$) as depicted by the Daughter activity curve.
		- The vertical line indicates an **elution**
			- When you elute a a molybdenum generator you're trying to remove 100% of the technetium atoms. And then immediately those moly atoms don't stop decaying. So they are just integrating and then building up another process for the technetium built up. 
		- Because these two processes (daughter activity and elution) are always in play and the half-lives are close together, we call this **transient equilibrium**.
- **Quality control** of the eluate, i.e. the ${}^{\text{99m}}\text{Tc}$ that we have "milked" from ${}^{99}\text{Mo}$
	- Manufacturer level
		- Assess sterility, pyrogens and other radionuclidic contaminants like Strontium and Iodine
	- User level
		- *For each elution*, we must test for
			- **radionuclidic purity**, which is also referred to as breakthrough 
				- Use a dose calibrator to test for the molybdenum breakthrough: Put our eluate vial into a moly canister (a gas filled chamber) and detect between Molybdenum and Technetium by detecting the difference between the technetium photon of 140 keV, and the molybdenum, which has a photon abundance of 740 and 780 keV.
				- ![[Radionuclides-20240816212554722.webp|259]]
			- **chemical purity**, which is any bit of that aluminum column that can make it through into our final product vial, and
				- tested with a chlorometric test; involves a specially treated paper
			- **radiochemical**, such as hydrolyzed reduced ${}^{\text{99m}}\text{TcO}_2$ (technetium dioxide), which is insoluble and will not produce the species that we want that's going to do the biological uptake in the organs that we want.
				- Chromatography

### Technetium-99-based Protocols

- Imaging protocols using these radiotracers include rest-stress protocols and rest protocols with nitrate enhancement.


# CV PET Tracers

- [[Positron Emission Tomography (PET)|PET]] allows non-invasive evaluation of [[Myocardial Blood Flow (MBF)|MBF]], function, and metabolism using physiological substrates prepared with positron-emitting [[Radionuclides|radionuclides]], such as carbon, oxygen, nitrogen, and fluorine.[^asnc]
- [[Positron Emission Tomography (PET)|PET]] [[Radionuclides|radionuclides]] have half-lives that are often considerably shorter than those used in [[Single-photon emission computed tomography (SPECT)|SPECT]]. 
- Positron-emitting radionuclides can be produced using:
	- a **[[Cyclotron|cyclotron]]**
		- e.g., 18F-fluoro-2-deoxyglucose [18F-FDG] with a 110-minute half-life
	- a **[[Radionuclide Generator|generator]]**
		- e.g., rubidium-82 [82Rb] with a 75-second half-life from a strontium-82 [82Sr] generator
- PET [[Radionuclides|radionuclides]] reach a more stable configuration by the emission of a **positron**.[^asnc]
	- **Positrons** are positively charged particles with the same rest mass as **electrons**.
- Current Food and Drug Administration (FDA)-approved and CMS-reimbursable [[Positron Emission Tomography (PET)|PET]] [[Myocardial Blood Flow (MBF)|MBF]] tracers are limited to 82Rb and 13N-ammonia. While 15O-water is also used clinically in Europe, it is not FDA approved in the United States.[^asnc]

> [!tldr] Most common PET tracers
> At present, 82rubidium chloride (82Rb) and 13N- ammonia (13NH3) are the most commonly used radiotracers for PET MPI and are both FDA-approved. 15O- water is more frequently used in Europe and is not FDA- approved. 13NH3 and 15O- water require an on-site [[Cyclotron|cyclotron]] due to their short half-lives. 82Rb also has a short half-life and is [[Radionuclide Generator|generator]] produced.

#### Rb-82

- a monovalent cationic analog of potassium
- 75 second half-life
	- decays by emission of several possible very high-energy positrons
	- The daughter product is krypton-82, which is stable.
- Sr-82 has a half-life of 25.5 days and decays to Rb-82 by **electron capture**.[^asnc]
- Blood flow tracer
- 82Rb is extracted from plasma with high efficiency by myocardial cells via the Na/K adenosine triphosphatase pump.
	- ==extraction can be decreased by severe acidosis, hypoxia, and ischemia, i.e. while uptake of 82Rb predominantly depends on MBF, it may be modulated by metabolism and cell membrane integrity==
- [[Radionuclide Generator|Generator]] produced: **Strontium-82 generator**
	- Produced in a commercially available generator by decay from Sr-82 attached to an elution column.[^asnc]
		- Rb-82 is eluted from the generator with 10 to 50 mL of normal saline by a computer-controlled elution pump, connected by intravenous (IV) tubing to the patient. 
		- The generator is fully replenished every 10 minutes.
	- [[Radionuclide Generator|Generator]] is replaced every 6 weeks, thus obviating the need for a [[Cyclotron|cyclotron]].
	- ![[Radionuclides-20240816213053526.webp|472]]
	- Strontium-82 is an iron analog and can get into the bones
	- Greatest concern with Rb-82 is a breakthrough of the Sr-82 into the elute. Sr-85 and Sr-82 are present when a new generator arrives.
	- Check to make the Strontium stays safe:
		- Check sample at the beginning of the day → Use the sample obtained for the 82Rb activity determination
		- Allow the sample to stand for at least one hour.
		- Measure the activity of the sample in a dose calibrator in microcuries.
		- Follow the calculations described in the insert to determine the amount of 82Sr and 85Sr.
			- 82Sr content must be < 2 x 10-2 $\mu \text{Ci} / \text{mCi}$ of 82Rb at end of elution.
			- 85Sr content must be < 0.2 $\mu \text{Ci} / \text{mCi}$ of 82Rb at end of elution.

#### N-13 Ammonia

- N-13 decays by **positron emission**.[^asnc] 
	- The daughter product is carbon-13, which is stable.
- Used to measure either absolute or relative MBF
- [[Cyclotron]] produced
	- Has a relatively short half-life requiring an on-site cyclotron and radiochemistry synthesis capability
- 10-minute half-life
	- relatively short half-life requires an on-site cyclotron and radiochemistry synthesis capability
- Flow tracer

#### FDG

- [[Cyclotron]] produced
- 110-minute half-life
- Tracks with glucose metabolism

# Positron Imaging & Time-of-Flight (TOF)

- Positron Imaging
	- When a positron is emitted, it enters the medium ionizing the water molecules to slow down
	- When it comes to a stop, it picks off an electron from the medium and then annihilates, producing two 511 keV photons traveling in opposite directions
	- By detecting both photons within a fixed timing window, we then can find the line in which the annihilation occurred.
	- With PET, it's always going to be the  sum of the forward-facing photon and the backwards-facing photon. So it doesn't matter where along this line of sight, the annihilation event occurred, we always get the same amount of attenuation. So if we know the patient-specific attenuation map, we can create a correction map that applies to all of the pixels within our sinogram.
		- ![](https://www.researchgate.net/publication/20098749/figure/fig4/AS:601730106527757@1520475045536/5-Binning-the-PET-signal-The-two-detection-points-of-the-annihilation-photons-form-the.png)

- Time-of-Flight (TOF) refers to the time difference between when the two 511-keV annihilation photons reach their respective detectors, 180° apart. For example, if the positron annihilation occurred at the center of the machine, the two photons would reach their respective detectors at exactly the same time, while if the annihilation occurred closer to one detector than the other, the photon would reach the closer detector first. If the time difference could be measured accurately enough, it would be possible to determine exactly where the annihilation event is originated.


[^asnc]: Dilsizian V, Bacharach SL, Beanlands RS, et al. ASNC imaging guidelines/SNMMI procedure standard for positron emission tomography (PET) nuclear cardiology procedures. Journal of Nuclear Cardiology. 2016;23(5):1187-1226. doi:10.1007/s12350-016-0522-3
[^imaging]: Garcia, M. J., Kwong, R. Y., Scherrer-Crosbie, M., Taub, C. C., Blankstein, R., Lima, J., Bonow, R. O., Eshtehardi, P., & Bois, J. P. (2020). State of the Art: Imaging for Myocardial Viability: A Scientific Statement From the American Heart Association. Circulation: Cardiovascular Imaging, 13(7). https://doi.org/10.1161/hci.0000000000000053
