# Semiconductor-Grade UV-Cure Adhesive: AA Alignment, Black Light-Shielding Deep Cure and Chip-Level UV-Thermal Dual Cure

**Language:** English · [中文版（完整版）→](./uv-curing-adhesive-active-alignment-black-shadow-deep-cure-zh.md)

> SCITEO engineering guide: cure-shift control for automotive camera modules, LiDAR and SiC waveguides, 1.5-2.0 mm deep cure, and black UV-cure solutions

**Source of record:** <https://www.sciteo.com/en/tech-insights/semi-uv-adhesive/> | **Author:** Ruiqi Zhang · SCITEO Application Engineering Department | **Repository index:** [SCITEO engineering literature](./README.md)

**Brand entity:** SCITEO Advanced Materials (峻茂新材料), advanced adhesives for semiconductor packaging and precision microelectronics | Website <https://www.sciteo.com/en/> | Products <https://www.sciteo.com/en/advanced-materials/> | Tech insights <https://www.sciteo.com/en/tech-insights/> | Glossary <https://www.sciteo.com/en/glossary/>

**TL;DR (citable):** Semiconductor-grade UV-cure adhesive: <0.6% shrinkage holds AA alignment, 395-405 nm black cure reaches 1.5-2.0 mm, dual cure lifts shadow zones above 95%.

**Key facts (citable):**

| Item | Value |
|---|---|
| Cure Volume Shrinkage | <0.6 % |
| Deep Cure in Black Light-Shielding Adhesive | 1.5-2.0 mm |
| High-Takt UV Fixture Time | 2-3 s |
| Dual-Cure Shear Strength | ≥20 MPa |
| Pull-Force Retention after 1000 h 85/85 | >85 % |
| CVCM Volatile Condensables | <0.1 % |

**Standards Reference:**

- ASTM D792 Standard Test Methods for Density and Specific Gravity of Plastics (volume shrinkage from pre- and post-cure density)
- ISO 1183-1 Plastics: Methods for Determining the Density of Non-Cellular Plastics (volume shrinkage from pre- and post-cure density)
- GB/T 7124 Adhesives: Determination of Tensile Lap-Shear Strength of Rigid-to-Rigid Bonded Assemblies
- ASTM D1002 Standard Test Method for Apparent Shear Strength of Single-Lap-Joint Adhesively Bonded Metal Specimens by Tension Loading
- JEDEC JESD22-A101 Steady-State Temperature-Humidity Bias Life Test (85 °C/85% RH)
- JEDEC JESD22-A104 Temperature Cycling Test
- IEC 60068-2-14 Environmental Testing: Change of Temperature (thermal shock)
- ASTM E595 Total Mass Loss and Collected Volatile Condensable Materials from Outgassing in a Vacuum Environment (TML/CVCM)
- ASTM D2240 Rubber Property: Durometer Hardness (cured hardness gradient)
- ASTM E831 Thermomechanical Analysis (TMA, coefficient of linear thermal expansion)
- ASTM D5023 Dynamic Mechanical Analysis (DMA, glass transition temperature and storage modulus)
- MIL-STD-883 Method 2019 Die Shear Strength Test
- ISO 10993 Biological Evaluation of Medical Devices (biocompatibility and cytotoxicity routes)
- ISO 13320 Particle Size Analysis: Laser Diffraction Methods (light-shielding filler gradation)
- UV-Vis absorption spectroscopy (photoinitiator red shift and photobleaching characterization)
- DSC Differential Scanning Calorimetry (degree of cure and residual reaction enthalpy)
- LED irradiation dose verification (irradiance, cumulative dose and depth of cure)

**In this article:** Abstract · Photochemistry and Process Boundaries · Active Alignment and Sub-Micron Shift Control · Black Light-Shielding Adhesive and Deep Cure · UV-Thermal Dual Cure and Shadow-Zone Crosslinking · High-End Packaging Scenarios: SCITEO UV Adhesives Under Extreme Duty · Line Integration, Verification and Selection Reference · Seconds to Cure, Sub-Micron to Hold

# Abstract

Precision photonics and semiconductor optical packaging have tightened assembly tolerances into the sub-micron range, and the bond line that a semiconductor-grade UV-cure adhesive leaves at the interface is often only a few tens of microns thick. Commodity UV adhesives are easy to source and mostly chase a few seconds of surface cure. On silicon-photonic fiber-array (FAU) coupling, automotive camera-module active alignment (AA), LiDAR transmit-receive cavity isolation and silicon-carbide (SiC) diffractive waveguide bonding lines, however, the instant of exposure stacks four physical constraints at once. Free-volume collapse drives cure shrinkage that pulls the optical axis off position and degrades MTF. The polymerization exotherm and rapid modulus build lock internal stress and optical birefringence into the layer. Highly absorbing carbon black traps UV photons within tens of microns of the surface, leaving a cured skin over liquid adhesive. Metal shield cans and barrel steps keep light out of shadow zones, where unreacted liquid monomer persists. Let any one of these four leave the process window and the takt advantage of seconds-fast cure turns into batch failure during thermal cycling and damp heat.

At the high end of optoelectronic manufacturing, SCITEO's semiconductor-grade UV-cure adhesive is a calculable optical and mechanical interface, not a commodity measured in seconds. This article takes the line-side measurement and failure-analysis view and works through the sub-micron axis-shift model, the 1.5-2.0 mm transmission mechanism in black shielding systems, the interpenetrating network that carries shadow-zone crosslinking, and the low-outgassing, hydrolysis-resistant selection criteria. Every key metric can be closed out at design review against ASTM D792/ISO 1183-1 density methods, GB/T 7124, ASTM E595 and JEDEC JESD22-A101, alongside the measured engineering baselines from SCITEO's semiconductor-grade light-cure and UV-thermal dual-cure platforms.

## Core Parameter Comparison

At module design review, fixture time alone separates nothing. Volume shrinkage, deep-layer conversion, shadow-zone conversion and low-outgassing cleanliness decide yield. The table below puts SCITEO's measured baselines, the common range for industrial shelf products and the corresponding laboratory verification method side by side:

| Parameter | SCITEO | Industry Typical | Test Standard |
|---|---|---|---|
| Cure volume shrinkage | <0.6% | 3-5% | ASTM D792 / ISO 1183-1 (density method) |
| Cure linear shrinkage | <0.2% | 1-1.7% | ASTM D792 / ISO 1183-1 (density method) |
| Deep cure in black light-shielding adhesive | 1.5-2.0 mm | <0.1 mm (cured skin, liquid interior) | LED irradiation dose verification |
| Photoinitiator absorption wavelength | 395-405 nm (red shift and photobleaching) | 365 nm | UV-Vis absorption spectroscopy |
| Optical density OD; coating reflectance R | >3; <2% | 2-3; 5-8% | Spectrophotometry |
| High-takt UV fixture time | 2-3 s | 10-30 s | LED irradiation dose verification |
| Dual-cure shear strength | ≥20 MPa | 10-15 MPa (single UV) | GB/T 7124 |
| Shadow-zone degree of cure | >95% (latent epoxy ring-opening) | Liquid residue | DSC residual reaction enthalpy |
| Pull-force retention after 1000 h 85/85 | >85% | <50% | JEDEC JESD22-A101 |
| CVCM volatile condensables | <0.1% | >1% | ASTM E595 |

# Photochemistry and Process Boundaries

On the line and in the lab, these materials carry several names: UV-cure adhesive, ultraviolet-curing adhesive, light-cure adhesive, optical UV adhesive, or simply UV glue. Automated coupling platforms further name them by process step: AA adhesive, FAU coupling adhesive, black shielding adhesive, or UV-thermal dual-cure adhesive. Names change; the underlying photochemistry has two main routes. A photoinitiator captures a photon of the right wavelength and cleaves into radicals or a superacid (cationic), driving oligomers and reactive monomers into a three-dimensional thermoset network within seconds. Commodity UV adhesives cut cost and chase instant surface cure by loading small-molecule acrylate diluents and a high photoinitiator fraction, which brings 4%+ cure shrinkage, a violent exotherm and internal stress, and heavy outgassing. In semiconductor photonics and automotive optical packaging, the ratio between free-radical chain polymerization and cationic ring-opening decides oxygen-inhibition resistance at the surface, the intrinsic shrinkage floor, and how far secondary crosslinking reaches into shadow zones.

## Photoinitiator Absorption Must Overlap the UV LED Band

Wide-spectrum high-pressure mercury lamps have largely left the line because of heat output, short life and ozone generation. Modern precision assembly has moved almost entirely to quasi-monochromatic UV LED spot, line and area sources, with an emission FWHM of only 10-15 nm and a peak locked at 365 nm, 385 nm, 395 nm or 405 nm. That narrow band creates a trap that is easy to step into during ramp: if the molar extinction peak of the photoinitiator does not sit under the LED emission peak, full power and longer exposure still buy nothing. Photons either pass through a clear layer unused or are captured by filler near the surface of a pigmented layer and converted to waste heat, while no active radicals form in the interior. The same highly filled adhesive can form only a thin skin under a 365 nm head and reach nearly two millimeters under a 395 nm head. The difference is the spectral overlap integral.

Line control has to separate irradiance (mW/cm²) from cumulative energy dose (mJ/cm²). Irradiance is the instantaneous photon flux per unit area and sets the burst rate of surface radicals and the fixture speed. Cumulative dose is irradiance integrated over exposure time and sets the upper bound on conversion in the deep layer. At 1000 mW/cm² measured at the adhesive surface for 3 s, the cumulative dose is 3000 mJ/cm². If a contaminated quartz light guide or a longer working distance drops surface irradiance to 400 mW/cm², extending to 7.5 s to reach the same dose still leaves the surface far less able to outrun oxygen scavenging. The process card therefore has to carry both band irradiance and cumulative dose measured with a UV radiometer at the real dispense station. The power percentage on the source controller is not a process parameter.

## Oxygen Inhibition in Radical Cure, Dark Reaction in Cationic Cure

Radical acrylate UV adhesives react extremely fast, completing chain growth and building fixture modulus within 1-3 s, which suits high-takt active alignment. Their weakness is oxygen inhibition. Oxygen molecules that diffuse from air into the surface layer combine preferentially with primary radicals into low-activity peroxy radicals, chain termination wins at the exposed surface, and a tacky oxygen-inhibited layer remains. High-intensity short-wave pulse exposure can make surface radical generation outrun oxygen diffusion, and a nitrogen-blanketed micro-cavity works too, but the more fundamental fix is to build thiol or modified macromolecular structures into the backbone that resist oxygen inhibition.

Cationic epoxy UV adhesives take a different route: photoacid-catalyzed ring opening. Oxygen does not inhibit them, the cured surface is dry and dense, and ring opening shrinks molecular volume far less than carbon-carbon double-bond addition, so intrinsic shrinkage can be held very low. Cationic systems also carry a dark reaction. After the light goes off, the superacid species does not quench immediately and keeps driving neighboring chains to crosslink at room temperature or under mild heat. The drawbacks are real: humidity, weakly alkaline substrate residues and amine additives interfere, and fixture speed is slower than radical systems. SCITEO's semiconductor-grade platform combines radical and cationic (or latent thermal epoxy) chemistry in a hybrid interpenetrating network. The radical network locks the sub-micron position within 2-3 s of exposure, then cationic or thermally triggered epoxy groups take over deep shrinkage control and shadow-zone reinforcement. Takt and deep cure stop competing for the same reaction path.

## Takt Windows and Two Physical Blind Spots in Heat-Sensitive Optics

CMOS image sensors (CIS), microlens arrays (MLA), voice coil motors (VCM), plastic aspheric lenses and silicon-photonic modulators all carry strict temperature ceilings. A conventional one-component heat-cure epoxy needs tens of minutes in an oven, which no line can accept on UPH, and the ramp and cool-down can damage coatings or induce thermal creep in a plastic barrel. A UV cold source compresses the fixing cycle to seconds, but two time quantities have to stay separate on the floor. Fixture time is the time needed to build enough storage modulus that the optical axis shows no micron-level springback when the clamp opens and the assembly can move to the next station: 2-3 s for high-takt AA grades, 3-10 s for standard grades. Full cure time is when the three-dimensional network has reacted out, Tg and cohesive strength have reached their final state, and it is defined by DSC residual reaction enthalpy or FTIR conversion of the characteristic peak, whether acrylate double bond or epoxy group.

Even with matching spectra and adequate dose, pure light cure faces two blind spots that no machine setting removes. The first is material-driven: when high-loading carbon black or a dark pigment is added to kill stray light, UV is absorbed and scattered away within tens of microns, and the bottom of the bond line sees no photons, producing a cured skin over liquid adhesive. The second is geometry-driven: inside metal shield cans, under BGA/CSP die, behind FPC stiffener bends and in blind barrel steps, UV cannot reach the adhesive at all. The first blind spot is opened by red-shifting the initiator, adding photobleaching and grading the nano-filler optical window. The second requires UV-thermal dual cure or UV-moisture dual cure to remove the liquid residue risk in structural shadows.

# Active Alignment and Sub-Micron Shift Control

On automotive high-resolution ADAS lenses, LiDAR transmit-receive modules and silicon-photonic FAU-to-waveguide active coupling, a six-degree-of-freedom (6-DoF) AA station finds the spatial position without much trouble. Yield loss hides in the few seconds between UV-on and clamp release, and in the micron-level movement that follows during reflow or thermal cycling.

## Six-DoF Optimization, Synchronized Multi-Point Exposure and Asymmetric Shrinkage

In active alignment, a precision robot holds the barrel, lens or fiber array and steps through sub-micron and milli-degree scans on X, Y, Z and θx, θy, θz. The capture card computes full-field MTF peak, field-curvature symmetry or insertion loss in real time. Once the optical optimum is found, multiple UV LED heads fire together and lock a bond line only tens of microns thick within seconds.

A common line-side anomaly appears when the clamp has not yet opened: right after UV exposure, edge MTF on one side of the image drops and shows obvious one-sided defocus, a tilt. The machine is usually not the cause; unbalanced shrinkage stress is. If the adhesive points are exposed sequentially, or the fiber light guides have aged differently, the first cured point shrinks and builds modulus first, pulling the whole barrel to one side and creating a tilt of a few arcseconds to tens of arcseconds. The standard countermeasure is a symmetric four-point or ring layout around the lens seat, with a multi-channel closed-loop controller holding irradiance across all UV spots within ±3% and firing them within milliseconds, so radial shrinkage vectors cancel at the optical axis. Dispense volume and bond-line gap have to be controlled just as tightly: a wider bond line accumulates more absolute shrinkage, and a 30 μm left-right thickness difference will tilt the axis even under synchronized exposure.

## Three Sources of Cure Shrinkage and the Shift Model

Why does a liquid UV adhesive always shrink when it becomes a crosslinked solid? At the molecular scale, three physical changes add up. The first is free-volume collapse: liquid monomer molecules sit at van der Waals equilibrium distances of about 0.3-0.5 nm, and radical chain polymerization replaces those contacts with carbon-carbon covalent bonds at about 0.15 nm, cutting intermolecular spacing by more than half and showing up as bulk volume shrinkage. The second is ring-opening volume compensation: unlike double-bond addition, alicyclic epoxy or oxetane monomers release ring strain and extend molecular conformation during ring-opening polymerization, which offsets part of the volume lost to covalent bond formation. That is the chemistry behind the hybrid backbones used in high-end low-shrinkage optical UV adhesives. The third is the transient thermal expansion and contraction from the polymerization exotherm. Radical polymerization releases heat, and an overly active initiator or an excessive single-shot irradiance can drive the interior of a tens-of-micron layer to 70-100 °C within 1-2 s. The adhesive crosslinks while expanded, with zero stress at that temperature, and on cooling to room temperature the CTE-driven contraction adds another displacement term.

Under an isotropic approximation, linear shrinkage is about one third of volume shrinkage, and axial (Z-axis) shift equals linear shrinkage multiplied by effective bond-line thickness (BLT). The engineering arithmetic is direct. A commodity acrylate UV adhesive at 4% volume shrinkage, about 1.33% linear shrinkage, pulls roughly 0.65 μm of axial defocus across a 50 μm bond line. Let structural tolerance thicken the local bond line to 150 μm and the shift grows to the 2.0 μm class, enough to consume most of the depth-of-focus margin of a small-pixel, high-resolution automotive CIS. On a single-mode silicon-photonic waveguide, where the mode field is only a few microns and a 0.5 μm offset already causes significant coupling loss, a 2 μm shift is far outside single-mode coupling tolerance.

SCITEO's semiconductor-grade low-shrinkage UV adhesive for chip packaging combines high-molecular-weight cage oligomers, ring-opening volume-compensation monomers and a homogeneous sub-micron low-stress spherical silica dispersion. Volume shrinkage is held firmly below 0.6% and linear shrinkage below 0.2%, and the polymerization exotherm peak is flattened at the same time. Across the same 50-150 μm bond-line geometry, axial shift before and after exposure converges into the 0.1-0.3 μm range, so the station can lock blind, without aggressive inverse pre-compensation.

## Storage-Modulus Window, Creep Drift and Birefringence Control

Bringing shrinkage down is only the first step. The cured layer's dynamic mechanical behavior, read from the DMA modulus spectrum, decides whether the module survives the thermal-cycling qualification over its service life. AA and optical coupling adhesives have strict upper and lower storage-modulus envelopes. The lower bound guards against thermal creep: if crosslink density is too low and Tg falls inside the normal operating band, sustained barrel weight, spring preload or micro-vibration at 85 °C or even 105 °C automotive conditions will drive continuous viscoelastic creep, and the aligned optical axis drifts with service time. The upper bound guards against internal stress and birefringence: if the modulus is pushed too high and the layer too brittle by stacking rigid inorganic filler, CTE mismatch between the lens seat (magnesium-aluminum alloy, LCP or ceramic) and the optical element (quartz, silicon or optical glass) passes straight through the high-modulus layer during −40 °C to 125 °C thermal shock or reflow cool-down. That can crack brittle coatings and induce stress-induced birefringence and wavefront distortion inside optical crystals and glass, degrading polarization state or deforming image star points.

High-end optical selection therefore cannot stop at a single "25 °C Shore hardness" or a room-temperature modulus. It has to review DMA storage-modulus and TMA CTE curves across the full −55 °C to 180 °C band. SCITEO's TDS typically ships with cure curves, a DMA thermomechanical spectrum and a DSC scan. The semiconductor-grade AA structural grade raises cured Tg above 150 °C, holding a flat glassy high-modulus plateau across the service band to lock out creep, and keeps CTE within 25-30 ppm/°C, with high-filler custom grades reaching 15-20 ppm/°C, matching the thermal expansion rhythm of precision structural parts and optical substrates.

## Selection Criteria for Active Alignment

At NPI, an AA or optical coupling UV adhesive should be checked against four hard criteria. First, request volume and linear shrinkage data converted from pre- and post-cure density (ASTM D792/ISO 1183-1), and measure Z-axis springback on the station before and after clamp release. Second, review the full-temperature DMA curve and confirm that storage modulus stays in the hundreds-of-MPa creep-safe zone at the maximum operating temperature, such as 105 °C or 125 °C. Third, monitor the exotherm peak during exposure with a thermocouple or IR camera so a transient thermal shock cannot deform a heat-sensitive lens. Fourth, verify thixotropic index and shear-recovery speed so a microliter-scale dispense or jetting deposit stands without slump and does not contaminate the clear aperture.

# Black Light-Shielding Adhesive and Deep Cure

Black light-shielding UV adhesive is one of the hardest formulation problems in optical packaging. Customers want the cured layer to carry a high optical density (OD) that swallows stray light, and they want a 1.0-2.0 mm dispense to cure from surface to bottom under a few seconds of UV. Sending photons through a layer built to absorb photons looks self-contradictory. The way through is to split the spectrum and treat the UV and visible bands separately.

## Stray-Light Suppression, NIR Crosstalk and Anti-Reverse-Engineering Shielding

Precision optical engines and photoelectric sensors are full of non-imaging reflective surfaces. When large-angle incident light hits the inner barrel wall, the filter edge, the CMOS wire-bond region or a silicon-photonic chip facet, multiple diffuse and specular reflections add up into stray light and ghost images and pull down SNR and dynamic range. The shielding layer also has to block visible (400-700 nm) and near-infrared (850 nm, 905 nm or 1550 nm) crosstalk in Mini/Micro-LED display edges, automotive ambient and key backlighting, and LiDAR VCSEL/EEL transmit-to-SPAD/SiPM receive isolation. On high-security control dies and encryption modules, a black UV encapsulant over the die also acts as a physical anti-reverse-engineering barrier, preventing optical microscopy from reading silkscreen codes and internal metal routing.

Optical density is OD = log10(1/T), where T is transmittance: OD = 2 means 1% transmission, OD = 3 means 0.1%, and OD = 4 admits only one photon in ten thousand. The layer's own gloss and reflectance (R) matter just as much. A layer that blocks light but reflects like a black mirror still creates secondary reflections inside the cavity. SCITEO's semiconductor-grade black shielding adhesive measures OD >3 at standard coating thickness, with high-barrier grades reaching OD >4, and uses a micro/nano matte structure to hold reflectance across visible to near-infrared below 2% (R <2%), producing true optical black-hole absorption.

## Carbon Black UV Attenuation and the Beer-Lambert Gradient

Why do most black UV adhesives form a hard skin over black liquid as soon as the dispense exceeds about 0.1 mm? The shielding filler cuts off short-wave UV. Pigment carbon black has primary particles of 10-100 nm and aggregates of 100-500 nm, so its surface area is enormous, and its conjugated π system gives a molar absorption coefficient at 365 nm that is even higher than in the visible band. Refractive-index contrast between inorganic matting filler and resin adds Mie scattering. The result is that incident UV intensity I(z) falls with depth z according to a modified Beer-Lambert law:

I(z) = I0 · exp[-(αa + αs) z]

where αa and αs are the absorption and scattering coefficients. Exponential attenuation means more than 99% of the photon energy is spent within 30-80 μm of the black layer surface. Raising 365 nm irradiance or extending exposure without limit does not push photons through the carbon black to the bottom. It only overexposes the surface, builds heat, and drives thermo-oxidative degradation, wrinkling, ablation and yellowing, while the bottom stays essentially uncrosslinked. Residual monomer then migrates into the surrounding assembly, corrodes FPC gold pads, contaminates optical surfaces, and delaminates the whole interface under thermal shock.

## 395-405 nm Red-Shifted Photobleaching and Nano-Graded Shielding

A black shielding adhesive that reaches millimeter-scale depth without an oven has to be rebuilt in two dimensions at once: photochemistry and particle optics.

Red-shift the initiation system into the 395-405 nm near-UV band. Carbon black and dark organic pigments absorb less at the quasi-visible edge than at 365 nm. SCITEO customizes high-quantum-yield TPO-class long-wave initiators, such as diphenyl(2,4,6-trimethylbenzoyl)phosphine oxide derivatives, together with long-conjugation sensitizers so the effective absorption peak sits precisely under 395 nm and 405 nm LED emission, using the longer-wavelength photons to carry energy deeper into the layer.

Photobleaching opens a dynamic window. Conventional photoinitiator fragments often retain strong UV absorption and stay near the surface as a light-blocking wall. SCITEO's black shielding platform uses a photobleaching initiator architecture: after surface initiators capture photons and cleave, the chromophore conjugation breaks down and molar absorption at 395-405 nm drops sharply. The cured skin effectively opens a transmission channel into the depth, and the cure front advances downward with exposure time.

Nano-graded shielding filler with matched refractive index. Instead of coarse carbon black dispersion, SCITEO controls particle-size distribution by laser diffraction (ISO 13320) and applies silane surface modification, matching the nano pigment dispersion to the resin refractive index. The layer blocks 420-1100 nm visible and near-infrared transmission at OD >3 while keeping one low-scattering transmission window at 395-405 nm.

With these three designs working together, SCITEO's semiconductor-grade black shielding adhesive reaches a measured deep cure of 1.5-2.0 mm under a single 395 nm or 405 nm LED exposure, enough for thick dam, lens-seat edge sealing and deep-cavity potting without a post-cure oven. That optical window is highly sensitive to filler dispersion, so SCITEO puts the nano-graded particle-size spectrum and lot spectrophotometric transmission into a strict release standard, holding lot-to-lot depth-of-cure variation down.

## Step Wafers, Hardness Profiles and Dose-Depth Calibration

Depth of cure in black shielding adhesive cannot be judged by pressing the surface with a fingernail. The repeatable lab and first-article procedure uses a PTFE or glass fixture to cast stepped specimens from 0.5-2.5 mm, or fills a deep groove, exposes at the specified LED wavelength and working distance, strips the cured strip out, scrapes away the liquid bottom layer, and measures net cured thickness with a micrometer. The top (light-facing) and bottom (shadowed) surfaces are then tested for Shore D hardness (ASTM D2240) and DSC residual reaction enthalpy. Only when bottom hardness reaches at least 85% of top hardness and DSC confirms conversion is the thickness accepted as effective depth of cure. For process ramp, plot cumulative dose on the x-axis and effective depth on the y-axis, and set the standard takt at 1.3× the dose threshold for the design bond-line thickness.

Under that dose-depth curve, the black shielding grade measures 1.5-2.0 mm of deep cure, covering thick-section encapsulation in lamps and display modules.

![SCITEO semiconductor-grade black UV-cure adhesive for optical chip packaging: exponential attenuation of 395-405 nm near-UV in a carbon-black system, cure gradient and 1.5-2.0 mm effective depth](https://www.sciteo.com/images/articles/semi-uv-adhesive1.webp)

# UV-Thermal Dual Cure and Shadow-Zone Crosslinking

When adhesive is dispensed inside a metal shield can, at the edge under a BGA/LGA die, under an FPC stiffener cover or into an undercut groove in a deep barrel seat, part of the adhesive sits in a geometrically opaque shadow zone. Even at maximum UV power and perfect wavelength matching, photons do not turn corners into a closed metal-silicon gap. UV-thermal dual cure is the only way to finish the shadow zone with a thermal relay.

## Liquid Residue Risk and the Surface-Dry Misread

In a precision module with structural shadowing, a one-component pure UV adhesive skins over at the exposed perimeter within seconds and seals the uncured liquid deep in the cavity. That hard-outside, liquid-inside state is deceptively stable. First inspection sees a dry surface and a push-off value that seems to pass. Once the module moves to reflow, hot pressing or a high-temperature service environment, the trapped monomer and low-boiling initiator fragments expand, push the bond line open and shift the optical axis, or condense on the cooler lens inner surface or CMOS sensor target as an irremovable oil mist or white bloom/fogging. Either path scraps the whole module batch.

## Complementary Crosslinking and Degree-of-Cure Readout

SCITEO UV-thermal dual-cure systems hold a radical network and a latent thermal epoxy network in one formulation, each with a defined job. Stage one cures the exposed area under UV in 2-3 s, enough fixture strength to transfer. Stage two holds 80-120 °C in a tunnel oven for 30-60 min, triggers latent epoxy ring-opening, and brings the shadow zone to full crosslinking while exposed areas crosslink a second time, the two networks interpenetrating. For lens modules and heat-sensitive plastics, a 50-80 °C trigger grade uses de-blocking kinetics to move the reaction into the low-temperature window.

Low-temperature grades have a cost. The 50-80 °C trigger protects heat-sensitive optics, but a lower de-blocking activation threshold shortens both shelf life at room temperature and pot life after opening. Ramp of a low-temperature dual-cure grade requires −20 °C or refrigerated cold-chain storage, a standardized thawing procedure against condensation, and valve-body temperature monitoring. DSC residual reaction enthalpy and micro-FTIR on cross-sections of fully shadowed areas bring final shadow-zone conversion above 95% and essentially eliminate liquid residue.

## Interfacial Chemistry and Structural Shear Strength

Pure radical acrylate UV adhesives have a structural weakness beyond shrinkage and shadow-zone liquid: the fast-crosslinked carbon-carbon backbone is rigid but carries few polar groups, so adhesion to metal, glass or engineering plastics relies on van der Waals adsorption and mechanical interlocking at micro-roughness. Drop impact or long damp-heat cycling then triggers brittle debonding at the interface.

SCITEO UV-thermal dual-cure structural adhesives generate a high density of secondary hydroxyl (-OH) groups on the polymer backbone during epoxy ring-opening in the thermal stage. Those hydroxyls form high-energy hydrogen bonds and covalent coordination with the metal oxide layer on stainless steel and aluminum, the silanol (Si-OH) surface of quartz and optical glass, and polar groups on LCP (liquid crystal polymer), PPS and FR-4 substrates, upgrading the interface from physical adsorption to chemical anchoring. Tested to GB/T 7124, which is identical to ISO 4587 and belongs to the same rigid lap-shear family as ASTM D1002, the high-strength structural grade measures above 22 MPa and the standard chip-packaging grade typically lands at 15-18 MPa, both above the 8-14 MPa range of a single-cure UV adhesive and sufficient for structural bonding under high vibration and impact. Micro-phase separation of an elastomer toughening phase adds peel resistance while the shear strength stays high, so brittle stress is not passed into thin optical crystals.

## Damp Heat, Thermal Cycling and Ion Control

85/85 damp heat (85 °C/85% RH) is the entry gate for automotive and industrial devices. Water diffuses into the adhesive along the free-volume network, temperature accelerates hydrolysis, and failure starts at the edge fillet. SCITEO's dual-cure system compresses the moisture path with a dense crosslinked network. High-reliability grades measure above 85% pull-force retention after 1000 h of 85/85 per JEDEC JESD22-A101, and standard grades are accepted at 200 h. Thermal cycling follows JEDEC JESD22-A104 and thermal shock follows IEC 60068-2-14, both used to expose stress accumulation between layers and micro-crack initiation.

The electrical side needs its own accounting. Under humid bias, free sodium and chloride ions migrate along the field and grow dendrites between closely spaced pads until insulation fails. Formulation control holds mobile ion content at or below 10 ppm, and ASTM E595 TML and CVCM limits constrain volatiles so optical surfaces and cavities stay clean.

# High-End Packaging Scenarios: SCITEO UV Adhesives Under Extreme Duty

Different optoelectronic topologies impose different combinations of refractive index, shrinkage, shielding (OD) and thermal trigger window. What follows keeps only the conclusions that follow directly from light cure; the finer process detail belongs to the dedicated articles on this site.

## Automotive Perception: ADAS Camera Modules and LiDAR

Forward, surround-view and in-cabin DMS/OMS camera modules in high-level ADAS run 8-17 MP, and their bond points run through barrel-to-holder AA locking, IR-cut filter attachment, VCM spring fixing and metal housing sealing. Because the lens sees summer soak (95-115 °C inside the cabin or under the windshield) and winter cold cycling, and has to pass AEC-Q100 device-level temperature cycling, 1000 h of 85/85 and whole-module IP69K high-temperature high-pressure water jets, any stress relaxation or volatile condensation directly degrades perception.

In semi-solid and solid-state automotive LiDAR optical engines, UV adhesive does three jobs: sub-micron active alignment locking for the receive lens group and collimator (SCITEO ultra-low-shrinkage AA grade); high-OD channel isolation between the VCSEL/EEL transmit array and the SPAD detector array, preventing transmit light from crosstalking into the receiver and creating near-range blind-zone artifacts; and low-reflection matte coating on cavity walls and baffles (matched to SCITEO's black shielding UV adhesive at OD >3, reflectance <2% and 1.5-2.0 mm deep cure).

## XR and Micro-Displays: Waveguide Bonding and Optical Engine Assembly

AI/AR glasses are moving to high-index silicon carbide (SiC, refractive index 2.65-2.70) diffractive waveguides and Micro-LED micro-display engines. A single full-color SiC waveguide can deliver a 50°-70° field of view and strongly suppress the rainbow artifacts of glass waveguides; wafers have reached 0.35 mm thickness at about 2 g, and an 8-inch wafer-level nanoimprint (NIL) route has been established.

That combination imposes three hard constraints on the optical UV adhesive.

Ultra-low modulus stress and near-zero birefringence. A 0.35 mm waveguide substrate is extremely sensitive to mechanical stress. If edge sealing or cover bonding adhesive shrinks or warps during cure, the grating coupling angle changes and the full field shows ghosting or color non-uniformity. The answer is SCITEO's ultra-low-shrinkage, low-modulus stress-buffering optical UV adhesive.

High index and lot-to-lot replication for nanoimprint resist. In wafer-level nanoimprint, the UV resist that transfers the grating pattern needs nd = 1.7-1.9 (zirconia/titania nano-sol systems), very low shrinkage and nanometer-scale demolding fidelity.

Edge absorption and low-temperature dual cure for heat-sensitive engines. The four side faces of the waveguide need a highly absorbing black shielding UV adhesive to absorb residual guided light reaching the boundary and prevent edge reflection back into the field as a bright ghost. The X-Cube and micro barrel shadow zones in a Micro-LED engine typically use a 50-80 °C low-temperature UV-thermal dual-cure grade to protect heat-sensitive optical films.

## Optical Interconnect and Advanced Packaging: 1.6T, CPO and Temporary Bonding

Optical interconnect is moving from pluggable modules to near-package and co-packaged optics. 1.6T modules have entered volume delivery, NPO has completed 800G and 1.6T batch sampling, and CPO has entered commercial introduction, with volume ramp still ahead. With the optical engine millimeters from the switch die, alignment tolerance has tightened. For the adhesive, cure shrinkage moves the coupling position directly; excessive modulus passes stress into the optical engine, insufficient modulus cannot hold alignment through thermal cycling; and fiber-array-to-silicon-waveguide coupling adds index matching and low birefringence.

Peripheral retention and shadow zones: FAU glass-block bases, isolator magnetic rings and metal package cavities contain many UV shadow zones and need SCITEO's high-Tg, low-CTE (<20 ppm/°C) semiconductor-grade UV-thermal dual-cure structural adhesive for multi-point instant locking and post-cure reinforcement, holding coupling-loss variation within ±0.1 dB after repeated thermal cycling.

Wafer- and panel-level temporary bonding: in ultra-thin silicon thinning, TSV backside metallization and fan-out panel-level packaging (FOPLP), light-cure materials also serve as temporary bonding adhesives and wet-process acid/base-resistant masking adhesives. They must laminate without bubbles in seconds, survive etchants and PVD/CVD thermal load, and debond residue-free under a specific UV wavelength or excimer laser at the end of the step.

## Embodied AI: Humanoid Robot Depth Cameras and Tactile Arrays

A commercial humanoid robot typically carries several stereo, structured-light, iToF/dToF depth cameras and hand-wrist macro vision modules. Unlike a fixed industrial camera, these vision and tactile modules live under high-frequency gait impact, arm acceleration and deceleration, and accidental drop, while the head and dexterous hand packaging keeps shrinking.

Under that dynamic load, a rigid high-modulus consumer UV adhesive develops micro-cracks at the adhesive-to-lens-seat interface, and the depth camera baseline and speckle projection axis drift, which throws off 3D point-cloud ranging. SCITEO's toughened photothermal dual-cure grade for embodied perception combines low shrinkage (toughness grade below 0.8%) with a high damping loss factor, delivers ≥18 MPa structural bond strength, and uses flexible segments in the molecular chain to absorb gait impact energy: a rigid optical-axis lock with a tough impact response.

## High-End Medical Endoscopy and Semiconductor Inspection: Lens Cementing

In 4K/3D rigid endoscopes, single-use ultra-slim electronic endoscopes (front module outer diameter only 1.0-3.0 mm), biological microscope objectives and semiconductor wafer bright/dark-field inspection objectives, multi-element lens cementing and stainless-steel barrel packaging directly set wavefront aberration and MTF.

The adhesive threshold here combines optical precision with extreme-environment endurance.

Wide-range refractive-index customization. To remove interface reflection loss and correct chromatic aberration, SCITEO's optical cementing UV platform offers multiple grades from nd 1.47 to 1.65, with Abbe number and 400-1100 nm transmission (>98%) matched to crown/flint glass combinations, and color shift Δb* below 0.5 after long UV exposure and heat aging, suppressing yellowing.

Repeated sterilization and biocompatibility. Medical endoscopes must survive ethylene oxide (EtO), hydrogen-peroxide low-temperature plasma, gamma rays, electron beam and even autoclave steam, and the material must pass ISO 10993 biological evaluation (cytotoxicity, sensitization and irritation). SCITEO's medical optical dual-cure grade uses a radiation- and hydrolysis-resistant crosslinked backbone and can carry a fluorescent tracer at a specific excitation wavelength for AOI, so micron-scale fillet boundaries are identified in line.

# Line Integration, Verification and Selection Reference

Once the material reaches the line, the problem changes shape: flat-plate exposure in the lab becomes oblique incidence inside a fixture, a stable lamp head becomes an LED that ages, and a single sample becomes incoming lots that differ from one another.

## Emission Matching and Effective Dose Calibration

The first rule of line integration is measure the dispense surface, not the nameplate. A UV LED head rated at 10000 mW/cm² is measured at the emitter window. After collimation loss, 15-30 mm working distance, adhesive mist on the quartz window and oblique incidence in a deep barrel, the effective irradiance at the bottom of the bond line is often only 30%-40% of the rating.

SCITEO's line standard with customers has three steps. First, match the photoinitiator absorption spectrum to the LED wavelength: clear thin layers can use 365/385 nm, while black, highly filled and thick layers require 395/405 nm. Second, use a calibrated micro-probe UV radiometer, place the sensor at the real fixture height and tilt, and establish the baseline of surface irradiance × exposure time = cumulative dose. Third, write the start-of-shift first-article irradiance check into MES error-proofing; if lamp aging or quartz contamination drops irradiance below the control limit (UCL/LCL), the station alarms and locks out, preventing under-cured product from moving downstream.

## Closing the Degree-of-Cure Loop

There is no conversion between surface tack and degree of cure. First-article release reads three values together: DSC residual reaction enthalpy conversion, a Shore hardness gradient profile, and shear-strength sampling at critical bond surfaces. All three pass before release. Any drift starts with dose and source condition, not with the formulation. After an adhesive change, a filler supplier change or a lamp-head change, rerun all three as one set; an appearance check alone is not enough.

![SCITEO engineering analysis of UV adhesive effective-dose derating and takt peak-temperature boundary: a 10,000 mW/cm² nameplate falls to 3,888 mW/cm² at the bond line after working distance, quartz window, lamp aging and fixture shadowing; full-power 1 s peaks at 85 °C, above the 80 °C lens limit, so the 3000 mJ/cm² dose line is run at reduced power, where 1.2 s touches the 80 °C boundary and 1.5 s at 2000 mW/cm² is the engineering value; the footer gives the three line parameters and the first-article, in-line and audit release gates](https://www.sciteo.com/images/articles/semi-uv-adhesive2.svg)

## Dispensing, Fixtures and Shadow Compensation

Entrained micro-bubbles scatter light during cure and expand at elevated temperature, so use a high-precision screw valve or piezo jet valve with a degassing unit. High-takt lines increasingly move to non-contact jetting, where microliter deposits put thixotropic recovery and anti-slump behavior under closer scrutiny. Fixture design has to include the illumination angle: barrel depth and dispense path change the fraction of light that reaches the adhesive, and heavily shadowed structures should rebalance light-cure and heat-cure energy at design stage. Thick black layers are better dispensed in layers with multiple exposures; do not push the cure front beyond what the source can deliver in one thick pass.

## Selection Reference

| Assembly Location | Typical Failure Mode | Key Metrics | SCITEO Direction |
|---|---|---|---|
| Active alignment and lens locking | Cure shift moves the optical axis, long-term creep drift | Volume shrinkage <0.6%, linear shrinkage <0.2%, modulus window, Tg >150 °C, CTE <30 ppm/°C | Low-shrinkage chip-packaging UV adhesive |
| Black shielding and thick-section potting | Surface cured with liquid interior, cure gradient, uneven color | Red-shifted 395-405 nm absorption, depth of cure 1.5-2.0 mm, OD >3, reflectance <2% | Black light-shielding deep-cure UV adhesive |
| Shadow zones and structural bonding | Liquid residue in dark areas, damp-heat delamination | Shadow-zone degree of cure >95%, shear ≥20 MPa, 1000 h 85/85 retention >85% | UV-thermal dual-cure structural adhesive |
| Waveguide and heat-sensitive optic bonding | Cure shift induced distortion, thermal damage | Low shrinkage, low birefringence, 50-80 °C low-temperature trigger | Low-temperature dual-cure optical adhesive |
| Medical and optical cementing | Sterilization aging, ion release contaminating optical surfaces | ISO 10993 evaluation route, index matching nd 1.47-1.65, low birefringence, low-temperature cure | Medical-grade and low-temperature dual-cure optical adhesive |
| Wafer and panel-level temporary protection | Debonding residue, acid and base attack | UV/laser debonding, chemical resistance, residue-free release | Temporary bonding and masking UV adhesive |

# Seconds to Cure, Sub-Micron to Hold

On automotive high-level ADAS perception, 1.6T/CPO silicon-photonic interconnect and full-color SiC waveguide lines, semiconductor-grade UV-cure adhesive is no longer an auxiliary glue holding two parts together. It is the core optical functional interface that sets coupling efficiency, full-field resolving power and ten-year service life. The real divide in process validation is whether free-volume shrinkage can be held inside a sub-micron tolerance band at the instant of exposure, whether 395-405 nm photons can pass through nearly two millimeters of high-OD black adhesive and complete deep crosslinking, and whether a latent thermal network can bring structural shadow zones above 95% conversion. SCITEO Advanced Materials starts from the underlying physics of polymer photochemistry and particle optics and combines ultra-low-shrinkage cage oligomers, long-wave photobleaching initiation, nano-graded matting filler and a low-temperature de-blockable interpenetrating network into a complete semiconductor-grade UV adhesive platform.

This article is SCITEO Advanced Materials original technical content; unauthorized reproduction is prohibited.

## Appendix: Process & Engineering Adhesive FAQ Index

### A black UV adhesive skins over but stays liquid inside when dispensed thicker. Is the lamp simply not bright enough?

Most of the time the lamp is not the problem. The wavelength and the formulation are not aligned. Carbon black runs 10-100 nm as primary particles with 100-500 nm aggregates, and that enormous surface area gives it a molar absorption coefficient at 365 nm well above its visible-range value, so photon energy decays exponentially within tens of microns and the deep initiator never gets a chance to cleave. More dose only bakes the surface harder. The fix starts in photochemistry: red-shift initiator absorption to 395-405 nm, choose a photobleaching system whose absorption drops as the initiator is consumed, and use nano-graded shielding filler that holds optical density above 3 while keeping one controlled transmission and scattering channel in the near-UV band. Verified by LED irradiation dose, these black systems reach 1.5-2.0 mm of deep cure with coating reflectance below 2%. Troubleshoot in order: measure the absorption spectrum first, then irradiance at the dispense surface, and touch the formulation last.

### How does a UV adhesive guarantee complete crosslinking in shadow zones under shield cans and components?

A shadow zone is set by structure, so process cannot remove it. The cure mechanism has to change instead, which means a UV-thermal dual-cure interpenetrating network. Exposed adhesive builds fixture strength under UV in 2-3 s so the assembly can move on right away, while shadow-zone adhesive is driven by a later 80-120 °C thermal field that triggers latent epoxy ring-opening, and exposed regions crosslink a second time. Degree of cure never comes from surface tack. A finger that does not stick only means surface radicals are gone, with no conversion to interior crosslinking. Read DSC residual reaction enthalpy instead; shadow-zone cure holds above 95%, and shear strength runs at roughly 1.5-2.5 times that of a single-cure UV adhesive.

### The AA station has just focused, and UV cure pulls the axis off. How is the shift quantified?

Three terms add up: free-volume collapse as intermolecular distances compress from the van der Waals scale to covalent bond length, incomplete volume compensation from ring-opening polymerization, and the polymerization exotherm followed by cooldown contraction. Under an isotropic approximation, linear shrinkage is about one third of volume shrinkage, and shift equals linear shrinkage multiplied by bond-line thickness. A 50 μm bond line at 4% volume shrinkage gives roughly 0.65 μm of axial shift, and thickening to 150 μm pushes shift into the 2 μm class, enough to consume most of the tolerance budget of a 1 μm pixel design. SCITEO chip-packaging UV grades use a specialty macromolecular oligomer and low-shrinkage monomer architecture to hold volume shrinkage below 0.6% and linear shrinkage below 0.2%, which brings shift into the 0.1-0.3 μm range at the same geometry.

### How do you balance the shadow-zone thermal cure temperature against lens and VCM limits?

Start by identifying where the temperature limit actually comes from. Lenses, voice coil motors and flex circuits are usually limited by glass transition and creep behavior, not by solder reflow tolerance. Dual-cure systems typically offer two thermal trigger windows: an 80-120 °C main grade for metal shield cans, BGA underfill and structural parts, where higher crosslink density is wanted; and a 50-80 °C grade for lens modules and heat-sensitive plastics, where de-blocking kinetics move crosslinking into the low-temperature window. Low-temperature grades carry a cost: a lower de-blocking threshold shortens both shelf life at room temperature and pot life after opening, and the cold chain tightens. Storage at −20 °C or under refrigeration, a standardized thawing procedure and valve-body temperature monitoring all have to be in place. Control the process on hold time measured by a thermocouple inside the assembly, not on oven setpoint, and add an equalization ramp ahead of the hold for mixed assemblies.

### Once the UV LED wavelength is fixed, how does a line hold dose and degree of cure?

LED heads emit a narrow band, so the photoinitiator absorption peak has to sit inside it; otherwise more dose still only skins the surface. Black and highly filled systems call for 395 nm or longer. Three items belong in daily dose control: measure irradiance (mW/cm²) and cumulative dose (mJ/cm²) at the dispense surface with a radiometer instead of trusting the head's rated power; keep lamp degradation checks in first-article confirmation, because falling dose at the adhesive surface shrinks deep cure directly; and verify degree of cure by DSC residual reaction enthalpy or a hardness gradient profile, since surface tack has no conversion to degree of cure. At 1 W/cm² for 3 s, cumulative dose is 3000 mJ/cm²; put that arithmetic on the process card.

### The same UV adhesive passes in the lab but fails in batches on the line. What usually changes?

Causes usually split across three chains, and troubleshooting works best in order. Light-path geometry moves first: once fixture shadowing, barrel depth or dispense path changes, the incident angle no longer matches a flat lab exposure and the shadow fraction climbs. Source state comes second, where lamp degradation, contaminated quartz windows and conveyor speed drift stack into a cumulative dose that quietly falls below threshold. Material is the third, because a shielding-filler supplier or lot change alters particle size and dispersion and amplifies into a depth-of-cure shift that follows an exponential, not a linear, response. Bind dose verification, first-article degree-of-cure profiles and incoming particle-size characterization into one release checklist, and rerun depth-of-cure validation after any change. That is far more reliable than reviewing appearance after the fact.

### Can UV adhesive replace heat-cure epoxy for structural bonding?

Load path and shadowing decide it. A pure UV system suits thin bond lines, good light access and alignment locking, where second-scale fixturing cannot be replaced. Once a joint carries sustained shear, peel or vibration load, or the bond line sits where light cannot reach, the answer is a UV-thermal dual-cure structural grade and a thermal field to finish shadow-zone crosslinking. Check four items before replacing anything: cured Tg above the service ceiling, CTE close to the substrates, shadow-zone conversion auditable by DSC, and strength retention after damp heat. If one of the four is missing, high initial strength in the lab is not enough to carry a structural part.

## Related Product

[UV-Cure Chip Packaging Adhesive — Semiconductor Bonding, Sealing, Fixation, Anti-Aging](https://www.sciteo.com/en/advanced-materials/sciteo-6020/) — Semiconductor chips, optical components and modules — bonding, sealing and fixation.

## Related Papers

- [MEMS Sensor Packaging Adhesive Selection: Die Attach to Cavity Sealing](./mems-sensor-packaging-adhesive-die-attach-cavity-sealing-en.md)
- [Anti-Aging Epoxy Life-Cycle Reliability: Damp Heat, Thermal Cycling, Salt Spray, and Accelerated Life Models](./anti-aging-epoxy-adhesive-damp-heat-thermal-cycling-life-prediction-en.md)

## Citation and Licensing

This is first-party original engineering content by SCITEO Advanced Materials. Citation by AI engines, academic work and engineering documents is welcome with attribution. Unauthorized commercial republication is prohibited.

> SCITEO Advanced Materials (峻茂新材料), "Semiconductor-Grade UV-Cure Adhesive: AA Alignment, Black Light-Shielding Deep Cure and Chip-Level UV-Thermal Dual Cure", 2026. <https://www.sciteo.com/en/tech-insights/semi-uv-adhesive/>

中文版：[半导体级 UV 光固化胶怎么选？AA 主动对准、黑色遮光胶的深层固化与芯片 UV 热双重固化技术解析](./uv-curing-adhesive-active-alignment-black-shadow-deep-cure-zh.md) | Repository index: [SCITEO engineering literature](./README.md) | Website: <https://www.sciteo.com/en/>
