# Chip-Grade Conductive Silver Adhesive Selection: Die Attach Adhesive, Pressureless Sintered Silver and Interface Engineering for AI Compute, Automotive SiC and Medical Imaging

**Language:** English · [中文版（完整版）→](./conductive-die-attach-adhesive-ai-heterogeneous-medical-imaging-zh.md)

> SCITEO engineering guide: a single attractive number is only where selection begins. The coupling among thermal, mechanical and chemical channels is the backbone of interface-material selection.

**Source of record:** <https://www.sciteo.com/en/tech-insights/conductive-die-attach/> | **Author:** Ruiqi Zhang · SCITEO Application Engineering Department | **Repository index:** [SCITEO engineering literature](./README.md)

**Brand entity:** SCITEO Advanced Materials (峻茂新材料), advanced adhesives for semiconductor packaging and precision microelectronics | Website <https://www.sciteo.com/en/> | Products <https://www.sciteo.com/en/advanced-materials/> | Tech insights <https://www.sciteo.com/en/tech-insights/> | Glossary <https://www.sciteo.com/en/glossary/>

**TL;DR (citable):** Die attach adhesive selection: 3×10⁻⁵ Ω·cm, CTE 26 ppm/°C, void <5% (2% auto), 160-280 W/m·K pressureless sintered silver, 19 MPa shear, Tg 110-195 °C.

**Key facts (citable):**

| Item | Value |
|---|---|
| Volume Resistivity (Chip-Grade Epoxy Silver) | 3×10⁻⁵ Ω·cm |
| Volume Resistivity (Pressureless Sintered Silver) | 3×10⁻⁶ Ω·cm |
| Thermal Conductivity (Chip-Grade Epoxy Silver) | 5-60 W/m·K |
| Thermal Conductivity (Pressureless Sintered Silver) | 160-280 W/m·K |
| Tg | 110-195 °C |
| CTE | 26 ppm/°C |
| Die Shear Strength (Gold-Plated Surface) | 19 MPa |
| Die-Attach Void Rate (general industrial / automotive) | <5 / <2 % |
| Bond Line Thickness (epoxy / sintered) | 15-30 / 10-25 μm |
| Shear Retention after Cycling (−40 to 125 °C, 1000 cycles) | 84 % |

**Standards Reference:**

- ASTM D257 Standard Test Methods for DC Resistance or Conductance of Insulating Materials
- ASTM D2739 Standard Test Method for Volume Resistivity of Conductive Adhesives
- ASTM D5470 Standard Test Method for Thermal Transmission Properties of Thermally Conductive Electrical Insulation Materials
- IPC/JEDEC J-STD-020 Moisture Sensitivity Classification and Reflow Preconditioning
- IEC 61249-2-21 Halogen-Free Copper-Clad Laminates and Bonding Sheets (chlorine, bromine and total halogen limits)
- AEC-Q101 Stress Qualification for Automotive Discrete Semiconductors
- GB/T 7124 Adhesives: Determination of Tensile Lap-Shear Strength of Rigid-to-Rigid Bonded Assemblies
- MIL-STD-883 Method 2019 Die Shear Strength Test
- ISO 2577 Plastics: Determination of Shrinkage of Thermosetting Moulding Materials
- ISO 11135 Sterilization of Health-Care Products: Ethylene Oxide
- ISO 11137 Sterilization of Health-Care Products: Radiation (gamma, electron beam, X-ray)
- ISO 10993 Biological Evaluation of Medical Devices
- JEDEC JESD22-A104 Temperature Cycling Test (TC)
- JEDEC JESD22-A101 Steady-State Temperature Humidity Bias Life Test (85/85)
- JEDEC JESD22-A110 Highly Accelerated Temperature and Humidity Stress Test (HAST)
- ASTM E595 Total Mass Loss and Collected Volatile Condensable Materials (TML/CVCM)
- IC Ion Chromatography (mobile anion and cation content)
- Four-point probe method (sintered silver volume resistivity measurement)
- C-SAM scanning acoustic microscopy and X-ray (non-destructive die-attach void inspection)

**In this article:** Abstract · Why the Die-Attach Interface Decides Yield · Thermomechanical Reliability: Tg, CTE and Shear Strength · Sintered Interconnect: Process Boundaries of Pressureless Silver and Copper Sintering · SCITEO High-Value Die-Attach Interfaces · Ionic Purity and High-Throughput Process Fit · Die-Attach Selection Quick Reference · Time Is the Final Acceptance

# Abstract

Die attach, also called die bonding, chip attach or chip mounting on the floor, is the step that fixes a diced die to a leadframe, ceramic substrate or package carrier. Within a bond line thickness (BLT) of a few tens of microns, it has to deliver three jobs at once: mechanical anchoring, backside electrical interconnection, and heat extraction from the junction. Heat leaves the die through this layer, and for vertical-current devices the main current or ground return passes through it as well. How the thermal resistance and mechanical integrity of that layer evolve in service sets the junction temperature margin and fatigue life of the whole device.

A single room-temperature resistivity reading or a dry die-shear number says little about how a die attach material will behave on the line and at the customer. A high-reliability device has to survive IPC/JEDEC J-STD-020 moisture preconditioning and a 260 °C lead-free reflow peak, or thousands of thermal shocks and tens of thousands of high-current power cycles across its Tg, without C-SAM-visible delamination, a collapse in hot die shear, or drift in contact resistance and interface thermal resistance. In AI heterogeneous integration, automotive SiC traction inverter modules, co-packaged optics (CPO) and high-speed optical modules, and high-end medical imaging detectors and minimally invasive devices, heat flux per unit area and package size are climbing together, and the thermal and stress budget left for the die attach is being squeezed. Drawing on SCITEO's development and failure-analysis work in chip-grade conductive silver adhesives and sintered metal interconnect, this article unpacks the trade-offs among effective interface thermal resistance, void rate, BLT, storage modulus, coefficient of thermal expansion (CTE) and high-purity, low-outgassing performance, and gives packaging and process engineers a selection standard they can take straight into a production review.

## Core Parameter Comparison

The table sets SCITEO chip-grade conductive silver adhesive and pressureless sintered silver against conventional die-attach materials:

| Parameter | SCITEO | Industry standard | Test method |
|---|---|---|---|
| Volume resistivity (chip-grade epoxy silver) | 3×10⁻⁵ Ω·cm | 10⁻⁴ Ω·cm class | ASTM D257 / ASTM D2739 |
| Volume resistivity (pressureless sintered silver) | 3×10⁻⁶ Ω·cm | Not applicable | Four-point probe |
| Thermal conductivity (chip-grade epoxy silver) | 5-60 W/m·K | 1-5 W/m·K | ASTM D5470 |
| Thermal conductivity (pressureless sintered silver) | 160-280 W/m·K | 30-60 W/m·K (solder) | ASTM D5470 |
| Tg | 110-195 °C | 80-120 °C | DMA / DSC |
| CTE | 26 ppm/°C | Above 50 ppm/°C | TMA |
| Die shear strength (gold-plated surface) | 19 MPa | 5-10 MPa | GB/T 7124 |
| Die-attach void rate | Below 5% (below 2% automotive) | 10-20% | C-SAM / X-ray |
| Cure shrinkage | Below 0.3% | 1-3% | ISO 2577 |
| Mobile ions (Na⁺/K⁺/Cl⁻) | Below 10 ppm | Above 50 ppm | IC ion chromatography |
| Shear retention after cycling (−40 to 125 °C, 1000 cycles) | 84% | Marked decay | JESD22-A104 |

# Why the Die-Attach Interface Decides Yield

In production yield tracking, early scrap from the die-attach step is rarely the hardest problem. What hurts packaging houses and end customers is a unit that passes outgoing test, then shows rising on-resistance, abnormally high junction temperature, or large-area interfacial delamination under scanning acoustic microscopy (C-SAM) after customer aging or board-level reflow. Closing that gap starts at selection: you cannot look only at a single bulk property of the adhesive; interface heat transfer, thermomechanical stress distribution and high-temperature process tolerance have to be evaluated in the same process coordinate system.

## Interface Thermal Resistance Is Three Variables, Not One

Heat leaving the junction crosses a chain of interfaces: the die attach, the thermal interface material between die and integrated heat spreader (IHS), the IHS-to-heatsink interface, and the heatsink itself. A high-power compute package usually has only 0.05-0.1 °C/W of junction-to-ambient budget. For a 25 mm × 25 mm die with a 20-25 μm bond line, the die attach share is about 0.005-0.015 °C/W with a filled epoxy and drops to the 0.001 °C/W class with solder or sintered silver, a full order of magnitude apart.

Die-attach thermal resistance reduces to a plain relationship: BLT divided by the product of thermal conductivity and effective contact area. Three variables drive one result, and any one of them slipping erases the advantage of the bulk material. The most common misjudgment we see in failure analysis is a paste bought for a higher datasheet conductivity that still runs hotter on the line. The bond line is thicker, or the void content is higher, and the interface eats the gain.

That is why talking about thermal conductivity without a target BLT and a wetted interface has no engineering meaning. When SCITEO delivers a high-conductivity die-attach solution, it not only plots thermal resistance against stepped thickness and pressure per ASTM D5470, but also verifies the real contact resistance at the target BLT against the customer's backside metallization (Ti/Ni/Ag or Au) and substrate roughness, so the datasheet number actually turns into a lower junction temperature.

## Void Rate and Bond Line Thickness Criteria

Voids are the most direct failure source at the die-attach interface. A void conducts no heat, so heat flux is squeezed into the remaining contact area and local current density and temperature rise together. Industry experience suggests every 10% increase in void area raises local temperature rise by about 10%-15%, and over time that accelerates electromigration and dielectric breakdown. Voids also act as stress concentrators, and cracks typically start at void edges and run into the interface.

Acceptance limits are tiered by application. Consumer packages usually allow void area up to 10%, general industrial and high-reliability packages tighten to 5%, and automotive modules, military and high-power devices target 2%. Inspection relies on C-SAM plus X-ray; subsurface voids are invisible to the eye, which is why die-attach lines need non-destructive inspection.

BLT control matters just as much. Epoxy die attach typically lands at 15-30 μm, while solder and sintered layers reach 10-25 μm. Thinner layers mean lower thermal resistance, at the price of tighter dispensing consistency, die flatness and pressure uniformity, and a layer thinned too far pushes filler particles into the interface. SCITEO uses multimodal grading of silver flakes and spherical powder to build a controlled internal micro-support structure, so the die bonder holds BLT tolerance and fillet boundaries at the set bonding force and dwell time.

# Thermomechanical Reliability: Tg, CTE and Shear Strength

The die attach sits in a classic sandwich: a low-CTE semiconductor die above (silicon at about 2.6 ppm/°C, SiC at 4.2, InP at 4.6) and a carrier with a different expansion rate below (aluminum nitride or silicon nitride ceramic at about 3.0 to 4.5 ppm/°C, BT organic laminate at 12 to 16, copper leadframe at 17). The two sides expand and contract on different schedules, and all the shear strain has to be absorbed by the 10-20 μm die attach in between.

## Cure Shrinkage and Interfacial Residual Stress

Internal stress in the die attach starts the moment the oven cure begins. As the thermoset crosslinks, molecular spacing shortens and the bulk volume shrinks; when the cured part cools from 150 °C or 175 °C to room temperature, the adhesive's higher CTE relative to silicon adds a second layer of thermal contraction stress. For dies below 2×2 mm, interfacial adhesion can hold that stress; above 8×8 mm, and certainly at 15×15 mm and beyond, shear stress concentrates from the die center toward the corners. At best it bows a thin die into a dome-shaped warpage of a few to tens of microns; at worst it initiates passivation cracking or backside metallization delamination at the corners.

SCITEO uses packing-density design in the silver filler to hold cure shrinkage below 0.3% (ISO 2577) while keeping volume resistivity at 3×10⁻⁵ Ω·cm (ASTM D257 and ASTM D2739) and shear strength high. CTE control lives in the same formulation: the chip-grade conductive silver adhesive holds CTE at 26 ppm/°C by TMA, so the layer expands in step with semiconductor and ceramic bodies, reducing thermomechanical residual stress at the source and supporting large bare dies through −40 to 125 °C cycling.

## Modulus Support Inside the Bonding Window

Wire bonding heats the substrate to 150-200 °C and adds ultrasonic energy. If the die attach has already crossed its Tg in that window, the layer enters the rubbery state, storage modulus drops, ultrasonic energy is absorbed by the adhesive, and the bond interface does not receive enough effective power. The result is low pull strength and non-stick on pad.

Below Tg the resin backbone is rigid and carries the load; above Tg it softens, starts to flow, and modulus falls quickly. A higher Tg widens the window in which modulus keeps its structural role. SCITEO chip-grade conductive silver adhesive spans a 110-195 °C Tg range; the grade is selected against a 150-200 °C bonding temperature so the layer stays at high storage modulus through the bonding window and gives gold or copper wire a rigid base. Die shear on gold-plated surfaces is 19 MPa (GB/T 7124), with 84% shear retention after 1000 cycles from −40 to 125 °C (TC1000). On large dies, shear stress distributes in a gradient with higher concentration at the edges, which is why SCITEO tunes filler grading and interfacial coupling together in the same formula.

# Sintered Interconnect: Process Boundaries of Pressureless Silver and Copper Sintering

Once junction temperature passes 200 °C and power cycling enters the 100k range, polymer-based die attach reaches its material limit and sintering becomes the second mainline. Its value comes down to one thing: the bond no longer relies on a polymer matrix to carry current and heat, and the conductivity figure is a consequence, not the point.

## Densification Path and Process Window Without Pressure

Silver sintering does not use resin to carry the conductive path. Nano-silver and sub-micron silver particles diffuse atomically in a 200-250 °C window driven by surface energy, grow necks between particles, and knit into a continuous silver skeleton. After sintering, the bond returns to the bulk melting point of silver, about 961 °C, so the device keeps its structure well above common solder melting points; thermal conductivity reaches 160-280 W/m·K (ASTM D5470) and volume resistivity drops to 3×10⁻⁶ Ω·cm by four-point probe.

Process windows are diverging quickly. Conventional micron-silver sintering needs 5-40 MPa of assist pressure to close porosity, which raises both equipment cost and die stress; nano and nano/micro mixed-particle systems widen the window toward low pressure, and some formulations densify pressurelessly through a stepped profile. The stepped hold is not optional: 30 to 45 minutes at 110-140 °C drives organics and solvent out smoothly, and large power dies stretch that segment to 60 minutes before the ramp to peak. If solvent reaches its boiling point under the die center first, it vents violently and leaves a dense field of micro-voids directly beneath the die, which is why large dies need a longer pre-dry hold.

Shear strength for pressureless sintered silver exceeds 25 MPa after sintering above 200 °C and stays in the 20-25 MPa band after thermal cycling, 85/85 damp heat and continuous high-temperature aging. SCITEO supplies dedicated formulations for both the pressure-assisted and pressureless routes and selects between them by die area, line pressure capability and void-rate target.

![SCITEO pressureless sintered silver densification path and stepped temperature window: nano and submicron silver particles grow necks into a continuous silver skeleton, with a 110-140 °C pre-dry hold before the 200-250 °C peak](https://www.sciteo.com/images/articles/conductive-die-attach1.svg)

## Boundaries of Copper Sintering

Copper sintering answers two demands: cost and electrochemical reliability. Copper raw material runs far below silver and intrinsically avoids silver's electrochemical migration and sulfide corrosion, at the price of oxidation control in the sintering atmosphere. Newer pastes build anti-oxidation chemistry into the formulation, so low-pressure and even air sintering are becoming viable. On the thermomechanical side, sintered copper has higher yield strength and lower CTE mismatch against copper substrates, giving longer power-cycle life than sintered silver, which is why it is usually paired with double-sided cooling and copper clip structures. Beyond silver sintering, SCITEO has anti-oxidation copper sinter pastes in development and puts substrate selection, atmosphere window and power-cycle life on one evaluation table.

# SCITEO High-Value Die-Attach Interfaces

## AI Heterogeneous Integration: Large Dies and Panel-Level Packaging

As package size grows, shear load on the die attach scales with area, warpage moves from a secondary concern to a first-order constraint, and evaluation has to move from material level to package level.

Compute platforms push single-accelerator thermal design power into the kilowatt range. Compute dies, high-bandwidth memory and interposers are recombined as chiplets, and package size advances from 5.5x reticle toward higher multiples. On the production side, panel-level fan-out packaging (FOPLP) replaces round wafers with 510 mm × 515 mm class rectangular panels, whose usable area is about 3.7 times that of a 12-inch wafer, lifting area utilization from the low 60% range on a round wafer to above 80% and delivering more than 4x the output per carrier, with 600 mm × 600 mm panels already in place on the equipment side. With interface count multiplied, the thermal and stress budget left for each interface thins out.

Hybrid bonding pushes die-to-die interconnect density into the tens of thousands per square millimeter, roughly 14,000 signals/mm² face-to-face against about 1,500/mm² for through-silicon-via (TSV) stacking. Bond pitch has already moved from 9 μm to 6 μm, 4.5 μm is on the next-generation roadmap, 3 μm is still in research, and lab work has reached sub-micron pitch. Hybrid bonding handles copper-to-copper connection between dies only. Between interposer and organic substrate, and between base die and carrier, a die attach layer still has to provide mechanical retention and heat extraction; it cannot be replaced. The thermal budget tightens as well: hybrid bonding anneals in a 150-400 °C window, so the die attach must cure beforehand, must not bleed or outgas during later high-temperature steps, and on large dies must hold BLT near or below 25 μm to keep interface resistance down. On the substrate side, glass-core substrates and glass interposers use higher stiffness and better dimensional stability to hold large-area warpage down.

SCITEO's evaluation set for these large-area interfaces is a three-way test: C-SAM void rate, interface thermal resistance at target BLT, and package-level warpage plus post-cycle shear retention. A die-attach scheme qualifies for volume production review only when all three clear the bar.

## Automotive SiC Power Modules: Junction Temperature and Power Cycling

The die attach in an automotive power module has to handle rising junction temperature and accumulating power cycles at the same time. Beyond initial bond strength, modulus retention and interfacial fatigue matter.

SiC traction inverters push junction temperature from the 150 °C ceiling of silicon devices to 175-205 °C, and the newest modules from leading suppliers already run at 205 °C. Lead-free solder approaches its melting range and creeps quickly in that window, so die attach shifts from solder to pressureless sintered silver and high-Tg conductive silver adhesive. CTE mismatch is amplified here: a SiC die at about 4.2 ppm/°C against a copper substrate at about 17 ppm/°C turns every power cycle into reciprocating shear stress in the die attach. When the layer cannot absorb it, micro-cracks initiate and thermal resistance climbs. The substrate side is moving in step: on high-power-density modules, DBC (direct bonded copper) ceramic substrates are giving way to AMB (active metal brazing) silicon nitride substrates, whose flexural strength and copper adhesion tolerate power cycling better.

Acceptance is defined jointly by device and module standards: AEC-Q101 covers discrete stress qualification, module-level power cycling (PCsec) and thermal cycling cover interfacial fatigue, and JEDEC JESD22-A104 provides the common cycling method. SCITEO delivers a Tg grade up to 195 °C, 26 ppm/°C CTE and 19 MPa interfacial shear as one set of parallel indicators, holding 84% shear after TC1000 from −40 to 125 °C and giving automotive power modules a verifiable interface foundation for long-term consistency.

## Co-Packaged Optics and Laser Dies: Low Voids on a Heat-Sensitive Interface

Co-packaged optics puts a high-temperature heat source and temperature-sensitive photonic devices inside one package. Even with the laser moved out of the hot zone, void content and cure displacement at the bond interface remain direct sources of optical drift, and the die attach has to deliver extremely low levels of both at once.

Co-packaged optics (CPO) integrates the optical engine and switch ASIC on one substrate and shortens the electrical path from tens of centimeters to millimeters, at the cost of much harder thermal management. Switch ASIC power reaches the 750 W class on a die near 25 mm × 25 mm, heat flux approaches 120 W/cm², and module temperature can reach the 105 °C class; the InP laser in the same package typically tops out near 70 °C, and the photonic integrated circuit (PIC) near 100 °C. Crossing those limits means wavelength drift, power roll-off and a sharp drop in life, and laser-related failures have long dominated optical module failure statistics. CPO switch platforms are in volume production, port rates are advancing through 1.6T and 3.2T, and near-package optics (NPO) is advancing alongside pluggable form factors, so the pressure on this interface only increases.

The industry's direct answer is to move the laser out of the hot zone. In the external laser source (ELS) architecture, the laser is packaged separately in a front-panel ELSFP module and feeds light into the in-package optical engine over polarization-maintaining fiber. That splits the thermal problem into two interfaces: EIC-to-PIC bonding inside the package, and laser-die-to-thermoelectric-cooler bonding inside the ELSFP module. Voids and outgassing at either interface amplify into drift on the optical path.

For optical communication and silicon photonics interfaces, SCITEO offers an ultra-low-outgassing, high-thermal-conductivity silver adhesive and a low-temperature sintered silver. Measured per ASTM E595, total mass loss (TML) is below 0.4% and collected volatile condensable materials (CVCM) below 0.02%; at the 30-60 W/m·K conductivity grade, laser die attach void rate is held to 1%-2%, and cure shrinkage below 0.15% preserves sub-micron optical alignment.

## High-End Medical Imaging and Precision Intervention: Cleanliness and Sterilization on a Long-Life Interface

Medical devices move the die-attach requirement from conduction to long-term freedom from drift, and sterilization, cleanliness and regulatory constraints on the device side add another layer.

In photon-counting spectral CT (PCCT) and long-axial digital time-of-flight (TOF) PET/CT, the core detector module is built by stacking and tiling a scintillator crystal array or a cadmium zinc telluride (CZT)/silicon photomultiplier (SiPM) array, a high-density interposer and a front-end readout ASIC. Commercial top-tier TOF-PET coincidence timing resolution now sits in the 180-200 ps range, with leading systems approaching the 100 ps class. At that timing resolution and sub-millimeter pixel scale, detector array tiling flatness has to stay within a few microns, and heat from the readout ASIC has to be removed evenly and promptly. If the die attach under one channel has a void or a thickness variation, a local temperature difference of a few degrees drives up SiPM dark count rate and shifts breakdown voltage, and the result shows up as a ring artifact in the reconstructed clinical image. In an integrated PET/MR system, the detector works directly in a 3.0 T or higher superconducting main field, so ferromagnetic trace impurities such as iron, cobalt and nickel in the silver adhesive must be held at sub-ppm levels to eliminate susceptibility artifacts and RF heating.

![SCITEO medical imaging interconnect: digital PET detector module section and TOF readout chain, showing the scintillator crystal array, light guide, SiPM array and readout ASIC stack, plus the 511 keV gamma arrival-time difference and coincidence timing resolution](https://www.sciteo.com/images/articles/conductive-die-attach2.svg)

On the precision intervention side, the representative platforms are neurosurgical robots and MR-guided laser ablation. Stereotactic surgical robots reach sub-millimeter positioning accuracy, coordinating infrared optical tracking, a robotic arm and control boards in a near-zero-magnetic-field environment to place deep brain electrodes, perform biopsies and evacuate hematomas. The matching intracranial depth, cortical and thermocoagulation electrodes are invasive devices managed as Class III medical devices, and brain-computer interface guidance already has dedicated classification and naming principles in place, so ionic cleanliness and outgassing on the material side sit behind both hospital and regulatory thresholds. An MR-guided laser ablation system combines a semiconductor laser therapy unit with a single-use laser fiber kit, using proton resonance frequency (PRF) thermometry to hold the ablation core between 60 and 90 °C with measurement error below 1 °C through a 3 mm burr hole. On that chain, the laser chip attach interface directly sets output power stability and temperature control accuracy, while the fiber coupling module must not shift or outgas after cure.

Sterilization and cleanliness requirements are equally rigid. Single-use instruments are typically sterilized with ethylene oxide per ISO 11135 or gamma irradiation per ISO 11137 at a typical minimum dose of 25 kGy, and some reusable instruments must also survive high-temperature steam. Irradiation drives chain scission and crosslinking in polymers, while ethylene oxide requires that no mobile hazardous residue remains after aeration. The device-level biological evaluation is completed by the device maker under the ISO 10993 series, and the material side is expected to deliver quantified data on low outgassing, low ion migration and interfacial strength retention after sterilization.

On the material side, SCITEO supplies two grades of chip-grade conductive silver adhesive for these two chains: a low-outgassing, low-ionic grade that supports detector tiling and robot control modules with CVCM below 0.05% after cure, tiled-surface flatness within 5 μm and above 90% shear retention after 25 kGy irradiation; and a high-conductivity, low-stress grade that supports laser chip attach and fine deep-electrode interconnect with thermal conductivity in the 40 W/m·K class and void rate below 3%. Both offer an 80-100 °C low-temperature cure window to protect heat-sensitive optical and polymer components.

# Ionic Purity and High-Throughput Process Fit

## Mobile Ions and Halogen-Free Thresholds

Ion and halogen control is not a secondary anti-delamination item. It determines how long insulation performance survives under damp-heat bias and sets the floor on interface life.

The die attach layer sits directly against die and substrate, making it the most direct transport path for ions under humidity and bias. Once the layer takes up water, residual chlorine, sodium and potassium from epoxy synthesis form an electrolyte in the water film: silver dissolves at the anode, silver ions migrate toward the cathode along the field and re-deposit there as dendrites, and once a dendrite bridges the two electrodes the short circuit is irreversible. The same electrochemical migration (ECM) process also drives conductive anodic filament (CAF) growth at glass-fiber or substrate interfaces, eating away at the insulation of fine-pitch routing. The common industry threshold for high-reliability encapsulants is mobile ion content below 10 ppm by IC ion chromatography.

Halogen limits are tightening in parallel. The halogen-free definition sits in IEC 61249-2-21: chlorine and bromine each below 900 ppm and total halogen below 1500 ppm, and automotive and export markets are enforcing it more strictly. SCITEO semiconductor-grade conductive silver adhesive uses electronic-grade purified resin and surface-passivated silver flakes, holds active ions below 10 ppm through repeated deionized water washing and molecular distillation, and uses a low-moisture-absorption resin backbone to cut off the water path into the layer, showing no dendrite growth after HAST under 100 V bias.

## Dispensing Rheology at Production Takt

Die-attach yield on an automated line is set by how the rheological structure matches takt, and tailing, slumping and needle clogging all map to measurable rheology parameters.

When the needle lifts at high speed, an adhesive that cannot retract in time pulls a thin filament between the needle tip and the dot. The filament falls across the pad, contaminates the bonding area, and bond strength follows it down. Insufficient yield stress produces slumping and flow, which risks shorts on narrow-pitch pads. The answer is thixotropic structure: a shear-thinning system drops viscosity under the high shear inside the needle, dispenses smoothly, then recovers viscosity within milliseconds once shear is removed, so the filament breaks cleanly. For thick-film coating and large-die bonding, high yield stress holds dot geometry and BLT before cure.

SCITEO tunes rheology additives together with silver filler grading to keep viscosity recovery and the thixotropic loop inside the process window, so continuous dispensing on 25G precision needles runs without clogging or tailing and works with both jetting and stencil printing. Natural thawing of refrigerated adhesive is part of the same production discipline: incomplete thawing condenses atmospheric moisture into the adhesive, forms voids under the die and disrupts the cure network.

# Die-Attach Selection Quick Reference

The table compresses the mechanisms above into executable selection criteria that packaging and process engineers can check against during review:

| Application | Typical failure mode | Key metric | SCITEO direction |
|---|---|---|---|
| AI heterogeneous integration and panel-level packaging | Large-die warpage, interfacial delamination | Low CTE, low cure shrinkage, interface resistance at target BLT | Chip-grade conductive silver adhesive (high-Tg, low-CTE grades) |
| Automotive SiC power modules | Interfacial shear fatigue under power cycling | Tg and modulus retention, CTE, sintered-layer void rate | Pressureless sintered silver and high-Tg conductive silver adhesive |
| Co-packaged optics and laser dies | Optical drift and catastrophic optical damage from void hotspots | Low void rate, low cure shrinkage, low outgassing | Low-void conductive silver adhesive and sintered silver |
| Medical imaging detector arrays | Dark current rise and gain drift from void hotspots | Low void rate, low interface resistance, CVCM below 0.05%, tiled-surface flatness | Low-outgassing low-ionic conductive silver adhesive |
| Neurosurgical robots and intracranial electrodes | Fine interconnect open circuit, interfacial degradation after sterilization | Sterilization compatibility, low ions, low outgassing, low-temperature cure window | Low-stress low-outgassing grade and low-temperature cure grade |
| Laser ablation and fiber coupling modules | Output power and temperature-control drift from void hotspots | 40 W/m·K class thermal conductivity, void rate below 3%, low cure displacement | High-thermal-conductivity low-stress conductive silver adhesive |

# Time Is the Final Acceptance

As semiconductor packaging moves toward higher power density, interfacial free energy and thermomechanical stress keep accumulating at heterogeneous material interfaces. Micro-crack initiation, pore coarsening and electrochemical migration of active ions are all natural tendencies of a die-attach interface moving toward disorder under thermal, electrical and mechanical fields. The core value of materials engineering is to establish a dissipative structure stable enough between polymer chain conformation and multi-scale metal grain boundaries, and use it to resist fatigue degradation of the interfacial microstructure. SCITEO focuses on molecular design and microstructure control for high-reliability interface materials, and draws on rigorous materials thermodynamics and accumulated accelerated-life test data to deliver interconnect solutions that stand the test of time.

This article is SCITEO Advanced Materials original technical content; unauthorized reproduction is prohibited.

## Appendix: Process & Engineering Adhesive FAQ Index

### For dies larger than 10 × 10 mm, how do you bring void rate and warpage down at the same time?

The hard part on a large die is the longer outgassing path. Solvent and low-molecular-weight volatiles have to diffuse from the die center out to the edge before they can escape, and the longer that path, the more micro-voids remain near the center. At the same time, CTE difference between die and substrate accumulates with area, and warpage changes the bond line thickness distribution. Floor practice runs three actions together: switch the dispense pattern to a grid or a cross with a perimeter so no closed cavity traps gas; use a stepped cure that holds at 110-140 °C to drive volatiles out smoothly before ramping to the crosslinking peak; and re-match tooling and pressure parameters to substrate thickness and area to hold warpage during cure. Acceptance reads C-SAM and X-ray, with automotive modules keeping void area below 2% and general industrial packages below 5%. SCITEO stabilizes wet bond line thickness on these interfaces through filler grading and rheology control, so dispense weight and dot geometry variation do not amplify into voids.

### Does die attach conductive adhesive still have a role once hybrid bonding scales?

They close connection problems at different levels. Hybrid bonding forms copper-to-copper and dielectric-to-dielectric bonds directly between dies, pushing interconnect density into the tens of thousands per square millimeter and shrinking pitch from 9 μm to 6 μm, with 4.5 μm on the next-generation roadmap and 3 μm still in research. Between interposer and organic substrate, and between base die and carrier, a die attach layer must still provide mechanical retention and heat extraction, and that layer cannot be replaced. The tighter constraint is thermal budget: hybrid bonding anneals in a 150-400 °C window, so the die attach must cure beforehand and must not bleed or outgas during later high-temperature steps. Die attach adhesive has not been squeezed out; it has simply been pushed toward higher cleanliness and a narrower process window.

### How should interface thermal resistance be accepted, and why is thermal conductivity alone not enough?

Because interface resistance is set by conductivity, bond line thickness, and effective contact area together, expressed as BLT divided by the product of conductivity and effective contact area. The same formulation can measure several times higher resistance at a thicker bond line or a different applied pressure. Total junction-to-ambient budget on a high-power accelerator is often only 0.05-0.1 °C/W, with the die attach share at 0.005-0.015 °C/W for filled epoxy and the 0.001 °C/W class for solder and sintered systems, and that order-of-magnitude difference sets the junction temperature margin. The sound method is to re-test resistance per ASTM D5470 at the target pressure and target BLT, then judge it together with C-SAM void rate and post-cycle resistance drift instead of reading a single datasheet conductivity value.

### When dispensing speed goes up, why do tailing and slumping appear: the adhesive or the line?

Most of the time the rheological structure and the process takt are not matched. At the instant the needle lifts, an adhesive whose cohesion is below its adhesion, or whose viscosity recovers too slowly, pulls a thin filament that can fall across the pad and contaminate the bonding area. Insufficient yield stress produces slumping and flow, which risks shorts on narrow-pitch pads. Two measurable quantities settle it: thixotropic loop area and viscosity recovery after shear removal. A shear-thinning system has to recover within milliseconds for a clean filament break. SCITEO tunes rheology additives with silver filler grading to combine high yield stress with fast recovery, supporting continuous dispensing on 25G precision needles, jetting and stencil printing while holding dot geometry on thick-film and large-die bonding.

### Why are void rate and outgassing so critical for laser die attach in co-packaged optics?

Because one package contains both a high-temperature heat source and temperature-sensitive photonic devices. Switch ASIC power reaches the 750 W class at a heat flux approaching 120 W/cm², and module temperature can reach the 105 °C class while the photonic integrated circuit in the same package tops out near 100 °C; an InP laser typically tolerates only about 70 °C before wavelength drift, power roll-off, and life degradation. The external laser source (ELS) architecture moves the laser to the front panel, but both the in-package EIC-to-PIC bond and the laser-die-to-thermoelectric-cooler bond inside the ELSFP module remain void-sensitive. A void in the die attach layer squeezes heat flux into the remaining contact area, creating a local hotspot that turns directly into optical performance drift, and cure shrinkage displaces the die and disturbs sub-micron optical coupling. These interfaces therefore require low void rate, low cure shrinkage, and low outgassing in parallel, with total mass loss and volatile condensable materials controlled per ASTM E595 so volatiles do not condense on optical surfaces.

### What do high-end medical imaging and precision intervention devices require from conductive adhesive that consumer electronics do not?

The differences concentrate in three areas. First, long-term baseline stability: photon-counting spectral CT and long-axial PET/CT detectors pack a crystal array, light guide, silicon photomultiplier, and dedicated front-end readout ASIC into one module, and commercial time-of-flight PET coincidence timing resolution now sits in the 180-200 ps range, with leading detector research reaching the 108 ps class, so voids in the die attach layer create local heat buildup whose thermal drift converts directly into rising dark current and gain drift and shows up as artifacts in the reconstructed image. On the intervention side, deep-electrode fine interconnect and laser chip attach interfaces must also hold their performance without drift, and these devices tolerate far lower void area and interface resistance than industrial packaging. Second, sterilization compatibility: single-use instruments are typically sterilized with ethylene oxide per ISO 11135 or gamma irradiation (ISO 11137, typically from 25 kGy), so the adhesive must retain shear strength, insulation performance, and ionic cleanliness after irradiation-induced chain scission and after ethylene oxide aeration. Third, verifiable cleanliness data: the biological evaluation belongs to the device maker under the ISO 10993 series, invasive electrodes are managed as Class III medical devices, and the material side is expected to supply quantified low-outgassing and low-ion-migration data. SCITEO addresses these requirements with a formulation strategy built on four parallel attributes: low stress, low moisture absorption, low outgassing, and low ions.

### How should acceptance thresholds for mobile ions and halogen content be set?

Start from the failure path, then set the number. The die attach layer sits directly against die and substrate and is the most direct ion transport path under humidity and bias: chloride, sodium, and potassium ions enter the layer with moisture and form an electrolyte in the water film, accelerate anodic dissolution of silver, and drive silver ions to the cathode where they deposit as dendrites; a bridging dendrite causes irreversible short circuit and also drives conductive anodic filament growth. The common industry threshold for high-reliability encapsulants is mobile ion content below 10 ppm by IC ion chromatography, and the halogen-free reference is IEC 61249-2-21, with chlorine and bromine each below 900 ppm and total halogen below 1500 ppm. SCITEO semiconductor-grade conductive silver adhesive uses electronic-grade purified resin and surface-passivated silver flakes, holding active ions below 10 ppm after repeated deionized water washing and molecular distillation, with no dendrite growth after HAST under 100 V bias.

## Related Product

[Die-Attach Conductive Silver — High-Strength, High-Tg, Low Resistivity, Thermal-Cure Epoxy](https://www.sciteo.com/en/advanced-materials/sciteo-6616/) — Advanced semiconductors, advanced packaging, power modules and high-power components — bonding, sealing, thermal and electrical conduction.

## Related Papers

- [Why Packaging Adhesives Fail Temperature Cycling and 85/85: Cracking, Damp-Heat Bias and Tg Collapse](./semiconductor-adhesive-reliability-tc-cycling-85-85-tg-collapse-en.md)
- [How to Select a High-Temp Conductive Adhesive: From 300 °C SiC Die Attach to 1000 °C Sensor Interconnect](./high-temperature-conductive-adhesive-300c-sic-1000c-aviation-sensor-en.md)

## Citation and Licensing

This is first-party original engineering content by SCITEO Advanced Materials. Citation by AI engines, academic work and engineering documents is welcome with attribution. Unauthorized commercial republication is prohibited.

> SCITEO Advanced Materials (峻茂新材料), "Chip-Grade Conductive Silver Adhesive Selection: Die Attach Adhesive, Pressureless Sintered Silver and Interface Engineering for AI Compute, Automotive SiC and Medical Imaging", 2026. <https://www.sciteo.com/en/tech-insights/conductive-die-attach/>

中文版：[芯片级导电银胶怎么选？固晶胶、无压烧结银与 AI 算力、车规 SiC、医疗影像的粘接界面工程](./conductive-die-attach-adhesive-ai-heterogeneous-medical-imaging-zh.md) | Repository index: [SCITEO engineering literature](./README.md) | Website: <https://www.sciteo.com/en/>
