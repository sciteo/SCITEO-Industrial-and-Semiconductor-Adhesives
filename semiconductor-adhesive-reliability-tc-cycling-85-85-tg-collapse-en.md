# Why Packaging Adhesives Fail Temperature Cycling and 85/85: Cracking, Damp-Heat Bias and Tg Collapse

**Language:** English · [中文版（完整版）→](./semiconductor-adhesive-reliability-tc-cycling-85-85-tg-collapse-zh.md)

> SCITEO reliability-lab engineering notes: advanced packaging for compute chips, automotive SiC power modules and military sensors — the physical-chemical failure chain of packaging adhesives in service

**Source of record:** <https://www.sciteo.com/en/tech-insights/adhesives-tc-ths-reliability-failures/> | **Author:** Wang Peixin · Head of Reliability Testing Engineering | **Repository index:** [SCITEO engineering literature](./README.md)

**Brand entity:** SCITEO Advanced Materials (峻茂新材料), advanced adhesives for semiconductor packaging and precision microelectronics | Website <https://www.sciteo.com/en/> | Products <https://www.sciteo.com/en/advanced-materials/> | Tech insights <https://www.sciteo.com/en/tech-insights/> | Glossary <https://www.sciteo.com/en/glossary/>

**TL;DR (citable):** Packaging adhesive reliability: ≥28 MPa shear after 1,000 TC cycles, >24 MPa after 85/85 with Tg above 140 °C, plus AEC-Q100 and JEDEC selection criteria.

**Key facts (citable):**

| Item | Value |
|---|---|
| Shear Strength after 1,000 TC Cycles | ≥28 MPa |
| Shear Retention after 85/85 | >24 MPa |
| Tg Retention after 85/85 | >140 °C |
| CTE (Below Tg) | 13-30 ppm/°C |
| Volume Resistivity after 85/85 | 10¹³ Ω·cm |
| High-Temp System Tg | >200 °C |

**Standards Reference:**

- JEDEC JESD22-A104F.01 Temperature Cycling Test (TC, −40 °C to 125 °C, 1000 cycles)
- JEDEC JESD22-A101D Steady-State Temperature-Humidity Bias Life Test (THB / 85/85, 85 °C/85% RH, 1000 hours)
- JEDEC JESD22-A110 Highly Accelerated Temperature and Humidity Stress Test (bHAST, 130 °C/85% RH, 96 hours)
- JEDEC JESD22-A118 Unbiased Highly Accelerated Temperature and Humidity Stress Test (uHAST)
- JEDEC JESD22-A103 High Temperature Storage Life Test (HTSL, 150 °C, 1000 hours)
- JEDEC JESD22-A106B.01 Thermal Shock Test (TS, liquid-to-liquid rapid temperature change)
- JEDEC JESD47K Stress-Test-Driven Qualification of Integrated Circuits (basis for accepting HAST as a THB equivalent)
- AEC-Q100 Rev-J/J1 Failure Mechanism Based Stress Test Qualification for Integrated Circuits (Grade 0: −40 °C to +150 °C; temperature cycling at −55 °C to +150 °C)
- AEC-Q104 Failure Mechanism Based Stress Test Qualification for Multichip Modules (MCM)
- ECPE AQG 324 Qualification Guideline for Power Modules (power cycling and thermal cycling)
- IPC/JEDEC J-STD-020F Moisture Sensitivity Classification and 260 °C reflow preconditioning
- IPC/JEDEC J-STD-035A Acoustic Microscopy for Nonhermetic Encapsulated Electronic Components (C-SAM delamination assessment)
- IEC 60068-2-78:2012 / GB/T 2423.3-2016 Damp Heat, Steady State (the national-standard basis for 85/85)
- ASTM E595-15(2021) Total Mass Loss and Collected Volatile Condensable Materials (CVCM) for space applications
- ISO 2577 Plastics, thermosetting moulding materials: determination of shrinkage (cure shrinkage)
- DMA Dynamic Mechanical Analysis (Tg, tanδ peak position and storage modulus)
- TMA Thermomechanical Analysis (CTE measurement)
- TGA Thermogravimetric Analysis to ASTM E1131 (thermal weight loss and Td5)
- GB/T 7124 Adhesives: Determination of Tensile Lap-Shear Strength of Rigid-to-Rigid Bonded Assemblies
- MIL-STD-883 Method 2019 Die Shear Strength Test Method

**In this article:** Abstract · Why Static Parameters Cannot Carry a Failure Call · Temperature Cycling: From CTE Mismatch to Creep Accumulation · 85/85 Damp-Heat Bias (THB/HAST): Electrochemical Migration and Tg Collapse · Structured Comparison of Reliability Criteria · Material Design: Working from the Formulation Up · The Evolving Test Envelope for Advanced Package Interfaces · Reliability at the Scale of Microns and Years

# Abstract

Temperature cycling and 85/85 damp heat are two of the hardest gates in semiconductor packaging qualification. The datasheet can show generous margin at shipment; after a full chamber run, however, die shear strength drops, C-SAM lights up with delamination, popcorn cracks appear after reflow, or leakage current climbs under bias. The failures are rarely caused by insufficient initial adhesion. They come from non-linear degradation of the crosslinked polymer under coupled thermomechanical and hygrothermal-electrochemical stress: TC keeps amplifying CTE mismatch and viscoelastic creep between dissimilar materials, while 85/85 and HAST accelerate moisture ingress, hydrolysis of the coupling interface, wet-Tg collapse from moisture plasticization, and bias-driven electrochemical migration (ECM/CAF).

At SCITEO's reliability laboratory, no packaging adhesive enters a customer's qualification sequence until both the temperature-cycling and damp-heat bias decay curves have been completed. Drawing on first-hand teardown and FA cross-section experience, this article examines the failure physics (PoF) and interface chemistry behind CTE-driven micro-bump shear fatigue, low-temperature brittle fracture and creep relaxation, passivation-interface hydrolysis, stepwise wet-Tg depression from water uptake, and dendritic shorts from mobile ions. It then converts those mechanisms into selection criteria and process windows that can be checked directly, covering 2.5D/3D advanced packaging, automotive SiC power modules, 800G/1.6T optical modules, and high-reliability industrial and deep-sea sensors.

# Why Static Parameters Cannot Carry a Failure Call

In a design review for advanced packaging (CoWoS, CoWoS-L, FOPLP), compute accelerators (GPU/NPU), wide-bandgap power modules (SiC/GaN), or high-precision military sensors, a clean set of initial values tends to carry the room: shear strength, volume resistivity, storage modulus, all with what looks like comfortable margin. The disagreement usually starts the day the chamber door opens.

After 500 to 1,000 TC cycles, 1,000 hours of 85/85 damp-heat bias (THB), or 96 hours of pressurized HAST, the electrical yield and die-shear curves often fall off a cliff at some unexpected point. Under an acoustic scanning microscope (C-SAM/SAT, judged to IPC/JEDEC J-STD-035A), the die corners or the area above the bump array are often already covered by a bright red delamination patch. Dye-and-pry or a cross-section under SEM then shows a familiar set of structural and electrical collapses: wire-bond neck fracture, passivation-interface debonding, coalescing micro-voids in the bond line, die cracking from dynamic warpage, fatigue shear at the root of micro-bumps or C4 balls, and leakage-current spikes or dielectric breakdown under high bias.

Initial strength was sufficient, so why does delamination still occur? The answer is that a room-temperature datasheet test and an in-service aging qualification do not measure the same physical dimension. Many selection exercises treat the packaging adhesive as a static mechanical bond or filler, yet at a real micron-scale heterogeneous interface the adhesive has to perform three dynamic functions: lock the expansion difference between die and substrate through violent temperature swings, hold a low-thermal-resistance path under power pulses, and block moisture and mobile ions under a humid electric field. More importantly, post-aging teardown often reveals a harsh fact: most failures are not cohesive fractures (CF) inside the adhesive, but adhesive failures (AF) where the crack runs along the polyimide (PI), polybenzoxazole (PBO), or silicon nitride (SiNx) passivation on the die, or lifts the solder mask or gold/ENEPIG interface in one sheet. If the evaluation only watches the bulk tensile strength and ignores viscoelastic creep during the soak and chemical bond hydrolysis at the interface, the selection direction is wrong from the start.

At SCITEO, a packaging adhesive is never judged on a single static number. The decision rests on the convergence of three dynamic data sets measured on the same aged lot: mechanical retention of die shear/shear strength after TC and damp heat (per GB/T 7124 or MIL-STD-883 Method 2019), thermomechanical dry and wet Tg, storage-modulus spectrum and CTE curves (by DMA and TMA), and electrochemical trends in volume resistivity and surface insulation resistance (SIR) after 85/85 bias. Only when all three curves have run on the same batch do the selection conclusions carry production weight.

# Temperature Cycling: From CTE Mismatch to Creep Accumulation

TC testing (JESD22-A104F.01) does not damage the adhesive simply through high-temperature degradation or low-temperature freezing. What does the work is the differential thermal expansion strain generated across a wide temperature range, plus viscoelastic creep and stress relaxation that accumulate during the soak at each extreme. The silicon die, organic substrate, copper leadframe and ceramic base each expand and contract at very different rates, and the adhesive layer trapped in a gap of tens of microns must absorb repeated high-level shear stress. The first few dozen cycles often show nothing; once interface microcracks and plastic deformation reach a critical level, they link up into macroscopic delamination after a few hundred cycles.

Many engineers assume that a part passing thermal shock (TS, e.g., JESD22-A106B.01 or a two-chamber/liquid-bath rapid transition) will also pass TC. The failure physics is completely different. Thermal shock drives an extremely high ramp rate, with transfer times usually in seconds to tens of seconds, and tests resistance to transient thermal gradients and brittle fracture. Temperature cycling (JESD22-A104F.01 explicitly excludes the fast ramps of liquid-bath thermal shock) controls the ramp rate and also requires a soak selected to the failure mechanism: solder creep and fatigue evaluations typically use a 10 to 15 minute soak (Soak Mode 3/4). That soak window is exactly what gives the viscoelastic chain segments time to respond. An adhesive with insufficient crosslink density or low modulus keeps relaxing and creeping through the high-temperature soak, then cannot return along the same path when the chamber drops to the cold extreme. Each cycle leaves a small irreversible residual strain, and the part eventually ends in fatigue debonding or solder-joint shear.

## Advanced Packaging and Flip-Chip: Why Micro-Bumps Shear Off

In chiplet heterogeneous integration, 2.5D silicon interposer packaging and high-density flip-chip, the bump pitch between die and substrate has approached the micrometer scale, and the load-bearing cross-section of each solder joint has shrunk sharply.

When the chamber falls from 125 °C to −40 °C or even −55 °C, the silicon die (CTE ≈ 2.6 ppm/°C) barely changes dimension, while the organic substrate underneath (ABF or BT, 14-20 ppm/°C in plane) contracts hard. The underfill and the encapsulant are supposed to spread that global shear mismatch across the whole die area through a rigid post-cure envelope. But if the adhesive's glass transition temperature (Tg) is below the high-temperature soak, or its sub-Tg CTE (α1) is high (for example above 35 ppm/°C), the adhesive layer becomes an amplifier of thermal stress, pushing the bump root back and forth through every thermal swing until low-cycle solder fatigue cracks appear and entire rows of micro-bumps shear off.

At the same time, dynamic warpage and low-temperature embrittlement worsen the stress state at the corners. In large dies or multi-layer stacks, the bond-line thickness (BLT) and principal stress are highly non-uniform between the center and the four corners, and the corners carry the largest peel stress and shear strain (the distance-to-neutral-point, DNP, effect). If the adhesive undergoes a brittle transition between −40 °C and −65 °C, with storage modulus rising sharply and fracture toughness collapsing, the corner bond line initiates a crack first, or pulls the die passivation (PI/SiN) out in one piece, after which the crack propagates around the bump array toward the center. In ultra-thin die stacks and molded underfill (MUF) processes, the thinned die loses bending stiffness, and the tolerance window for cure shrinkage and full-temperature CTE matching is compressed to the limit. SCITEO's flip-chip underfill platform holds sub-Tg CTE at 13-25 ppm/°C and room-temperature storage modulus in the 4.2 GPa class, so the shear displacement at the bump root stays inside the elastic range rather than being absorbed passively by a low-modulus layer.

## Automotive SiC Power Modules and Multichip Modules: Interfacial Debonding and Thermal-Paste Pump-Out

In 800 V traction inverters, onboard chargers (OBC) and solid-state power controllers for electric vehicles, SiC MOSFETs run at extreme current density and transient thermal shock; normal junction temperature exceeds 175 °C, and a new generation of modules qualified to ECPE AQG 324 now lists 200 °C short-duration junction capability. Under the severe AEC-Q100 Rev-J/J1 and AEC-Q104 multichip-module requirements, structural adhesives, potting compounds and thermal interface materials face combined thermomechanical fatigue and thermo-oxidative aging.

After hundreds of TC and power cycles, conventional low-crosslink thermal adhesives or soft silicone gels micro-slip under the repeated expansion and contraction breathing of the stack. Low-molecular-weight silicone oil or incompletely cured resin separates from the dense thermal filler (oil bleed and exudation), filler particles agglomerate into local voids, and the adhesive is gradually squeezed out of the thermal interface at the edge — the classic pump-out effect. Once pump-out occurs, or a micron-scale edge debond appears between the adhesive and the active-metal-brazed silicon nitride ceramic (Si₃N₄ AMB, CTE about 3.2 ppm/°C), the direct-bonded copper (DBC) or the nickel/silver plating, interfacial thermal resistance (Rth) rises by a multiple. The kilowatt-class heat generated by the die cannot leave in time, and local overheating, breakdown and thermal runaway follow. To protect module cycle life, the adhesive and interface material must not only hold a low CTE that tracks the ceramic and metal below Tg, but also keep thermal weight loss at 200 °C in the 0.01%-0.04% range, eliminating high-temperature volatilization, pulverization and interfacial creep displacement. SCITEO addresses pump-out by designing filler surface coupling and matrix crosslink density in one formulation window, holding thermal weight loss at 0.01%-0.04% after long-term aging at 200 °C and keeping interfacial thermal resistance from drifting with cycle count.

## 800G/1.6T Optical Modules and Precision Optical Packaging

In 800G/1.6T high-speed optical modules and co-packaged optics (CPO) for AI data-center compute clusters, the laser assembly (TOSA), receiver assembly (ROSA), fiber array (FAU) and micro-lens array run hot at full load; a cold start in the data hall, a LiDAR cold-soak condition or a power-cycle restart at an outdoor base station can drop the local temperature by tens of degrees within minutes.

Optical-grade bonding imposes a much tighter TC criterion than ordinary electronic packaging: the adhesive must not crack, and the permanent dimensional deformation after hundreds of −40 °C to 85 °C cycles must stay within sub-micron or even hundred-nanometer limits. Conventional silicone adhesives typically exceed 200 ppm/°C CTE and breathe heavily through thermal swings; a conventional unmodified rigid epoxy can hold position at room temperature but readily initiates microcracks in quartz glass lenses or micro-peeling at a metal housing interface when internal stress concentrates at the cold end. When SCITEO's laboratory reproduced TC failures in high-speed optical modules, it found that even when no macroscopic crack was visible under the eye or a low-power microscope, an irreversible creep offset of 0.3-0.5 μm in the polymer network was enough to drop fiber-coupling efficiency, showing up as insertion-loss (IL) failure and bit-error-rate degradation.

## Low Modulus Is Not a Universal Answer: The Long-Term Creep Trap

Faced with thermal stress from CTE mismatch, the industry has long relied on an intuitive selection rule: if hard-against-hard cracks, choose a low-modulus, high-elasticity soft adhesive to absorb the strain. That approach may work in millimeter-thick bond lines on large structural parts, but when copied directly into micron-scale gaps (BLT 10-50 μm) in chip packaging and precision interconnect, it often produces catastrophic late-life failure.

The cause is ratcheting and viscoelastic creep accumulation inside a micron-scale constraint. A compliant adhesive with too low a modulus undergoes irreversible conformational slip of its molecular chains under repeated hot-cold pulling, and each temperature soak consumes more of its elastic recovery potential. After a few hundred cycles, the soft adhesive neither protects the fragile micro-bumps and wire bonds nor holds itself together; fatigue relaxation opens micro-voids at the interface.

SCITEO takes the opposite physical design route for advanced packaging and high-reliability structural bonding: instead of softening the adhesive to yield passively, it builds a dense crosslinked skeleton with high storage modulus (4.2 GPa at room temperature, 9-13 GPa in high-rigidity thermal and underfill systems), presses the glassy-state CTE into the 13-25 ppm/°C band that tracks silicon and ceramics, and pairs it with 32 MPa-class interfacial shear strength. This coordinated high-modulus, ultra-low-CTE, strong-chemical-bonding mechanism locks the micro-strain from thermal cycling inside the purely elastic range and cuts off viscoelastic creep and solder fatigue at the source. Measured data show that, at etched aluminum and silicon/ceramic interfaces, die shear strength remains at 28.5 MPa or above after 1,000 cycles from −40 °C to 125 °C.

![SCITEO R&D's analysis of the thermal-cycling (TC) interfacial shear-strength evolution model at −40 °C to 125 °C on etched aluminum: the SCITEO ultra-low-CTE epoxy retains 28.5 MPa after 1,000 cycles (above the 28 MPa acceptance line), while a conventional epoxy follows a steep decay, crossing below the 5 MPa industrial structural failure threshold within tens of cycles and reaching zero around 60 cycles, suppressing interfacial delamination and micro-bump cracking.](https://www.sciteo.com/images/articles/adhesives-tc-ths-reliability-failures1.svg)

# 85/85 Damp-Heat Bias (THB/HAST): Electrochemical Migration and Tg Collapse

If temperature cycling is a pure thermomechanical fatigue campaign, 85/85 steady-state damp-heat bias (THB, 85 °C/85% RH, 1,000 h, JESD22-A101) and highly accelerated temperature-humidity stress testing (bHAST/uHAST, JESD22-A110/A118) are a combined chemical and electrical attack by water, heat and electric field. A failed 85/85 result is rarely a single path; three degradation chains advance in parallel inside the chamber: hydrolysis and peeling of the coupling chemistry at the interface, wet-Tg collapse from moisture plasticization, and electrochemical migration of mobile ions under bias. The national-standard steady-state damp-heat condition, GB/T 2423.3 / IEC 60068-2-78, specifies temperature and humidity without bias and is not interchangeable with THB.

SCITEO's failure-analysis team has repeatedly found a deceptive pattern in 85/85 and HAST samples: many adhesives that claim high insulation and high adhesion show no electrical or shear anomaly in the first 200 hours. The real turning point arrives when moisture reaches saturation inside the adhesive and pulls the wet Tg across a critical temperature; the interfacial debonding and leakage breakdown that follow are simply the cascade triggered by that physical phase change.

## High-End Sensor Packaging: Insulation Collapse After Aging

The sealing layers in military sensors, deep-sea probes and automotive radar control boards must hold electrical insulation through long-term moisture and salt-fog exposure, keeping leakage current at the picoampere (pA) to nanoampere (nA) level.

Under the high vapor pressure of 85 °C/85% RH, water enters the free volume of the crosslinked network and diffuses in a Fickian or non-Fickian manner into the depth of the adhesive. If the resin retains hydrolyzable halide ions, free organic acids or sodium/potassium ions (Na⁺/K⁺) from synthesis, the water inside the adhesive acts as a high-permittivity ionizing solvent, activating those frozen impurities into mobile carriers. Once a DC bias is applied across pins or pads, anions and cations migrate in opposite directions, and the nominal 10¹⁴ Ω·cm volume resistivity can fall by three to four orders of magnitude within two or three hundred hours, directly causing high-impedance sensor signal drift, transimpedance-amplifier offset or logic-control false triggering.

When moisture reaches the copper traces, silver-filled solder joints or SnPb/SnAgCu solder surfaces underneath, the applied field drives anodic dissolution (M → Mⁿ⁺ + ne⁻). The resulting silver, copper or tin ions migrate along the interfacial water film toward the cathode, deposit there and grow back toward the anode as dendrites. Once a dendrite bridges a micron-scale line gap, it creates a permanent low-resistance short or a burn-out. In glass-reinforced organic substrates (FR-4, BT or ABF) and at the underfill boundary, the same humid-bias combination catalyzes hydrolysis of the silane coupling layer on the glass fibers and grows conductive anodic filaments (CAF) along the glass-resin separation path. These defects sit deep inside the multilayer interface and cannot be found by visual inspection; only 85/85 bias and bHAST with in-situ surface insulation resistance (SIR) monitoring can intercept them early. SCITEO holds mobile ions at the ppm level in sensor potting systems and compresses the free-volume path with a dense crosslinked network, so volume resistivity remains at 10¹³ Ω·cm after 1,000 h of 85/85.

## Interfacial Bond Hydrolysis and Micro-Void Vapor Pressure: C-SAM Delamination and Adhesion Failure

Electrical damage is only the first layer. Moisture is equally the terminator of interfacial adhesion. On die passivation (PI, SiNx), alumina/nitride ceramics, copper leadframes or optical glass, an adhesive builds a bond above 20 MPa mainly through the covalent Si–O–M bonds formed by dehydration-condensation between functionalized silane coupling agents and surface hydroxyl groups (–OH), together with a dense hydrogen-bond network between polar groups.

Water, however, is a strongly polar small molecule. When moisture from 85/85 or HAST reaches the adhesive-substrate interface, water molecules preferentially occupy the hydrophilic sites on the substrate, not only breaking the existing interfacial hydrogen bonds but also, under sustained high temperature, reverse-hydrolyzing the Si–O–Si or Si–O–M covalent bonds built by the silane coupling agent. As the chemical bonds are dismantled one by one, the interface degrades to weak van der Waals adsorption and accumulates a continuous nanoscale-to-micron water film at the boundary.

At that point, voids trapped during dispensing or pulled open by cure shrinkage become powerful pressure multipliers. A micro-void saturates with water vapor first during 85/85; under the 85 °C soak or a 130 °C HAST, the vapor inside expands violently and generates a local saturated vapor pressure far above that of the surrounding dense adhesive, jacking the weakened interface open like a miniature hydraulic ram (mixed Mode I opening and Mode II sliding fracture). That is why, after 85/85 and a die-shear test, the fracture surface often stops cleanly at the die passivation or the metal plating, with no residual adhesive on the die side.

## Moisture Plasticization and Wet-Tg Collapse

In 85/85 and moisture sensitivity level (MSL) qualification, an even more insidious and destructive cascade is the plasticizing effect of water on the crosslinked network.

A cured adhesive network contains many secondary hydroxyl, ether or amine groups. When water molecules enter the spaces between polymer chains, they form intermolecular hydrogen bonds with those polar groups, effectively injecting a small-molecule lubricant into a tightly locked network, expanding the free volume and intensifying segmental motion. The direct result is a large step-down in glass transition temperature (Tg). A conventional epoxy encapsulant with a dry DSC or DMA Tg of 145 °C often collapses to a wet Tg of 100 °C or even below 85 °C after saturation at 85/85.

Once the wet Tg collapses, the entire production and service chain loses control. On one hand, when the device runs inside the 85/85 chamber (85 °C) or at a full-load hotspot (110-125 °C), the ambient temperature has already crossed the depressed wet Tg; the adhesive silently falls from the high-modulus glassy state into the rubbery state, storage modulus drops by more than an order of magnitude, CTE jumps from 30 ppm/°C to 100-150 ppm/°C (the α2 high-expansion region), and free volume expands sharply, multiplying the diffusion rate of moisture and ions. On the other hand, when the part is preconditioned to IPC/JEDEC J-STD-020F moisture sensitivity (for example MSL 1 or MSL 3, including 85/85 or 85 °C/60% RH absorption) and then pushed through a 260 °C lead-free reflow oven, the adhesive layer, already weakened in high-temperature modulus and cohesive strength by wet-Tg collapse, cannot suppress the multi-megapascal vapor pressure generated by residual moisture flashing at 260 °C. Popcorn cracking follows within seconds and can blow the underfill, the encapsulant and even the die apart from the inside. A dry Tg quoted without water absorption, coefficient of hygroscopic expansion (CHE) and wet Tg therefore has no meaning in a damp-heat reliability review.

## bHAST/uHAST Acceleration: Where the Equivalence Breaks Down

To shorten the 1,000-hour 85/85 cycle, semiconductor and automotive production lines commonly use highly accelerated temperature-humidity stress testing under JEDEC JESD47K and AEC-Q100: biased HAST (bHAST, JESD22-A110, typically 130 °C, 85% RH, about 2.3 atm absolute, 96 hours) to accelerate the electrochemical corrosion and ion migration of 1,000 hours of 85/85, and unbiased HAST (uHAST, JESD22-A118, 130 °C/85% RH, 96 hours) to screen interfacial delamination and moisture-induced mechanical degradation.

But when HAST is used as a 10x time-compression substitute for 85/85, two engineering boundaries must be enforced, or the acceleration factor will be badly distorted. First, the life extrapolation model must include both the temperature activation energy and the relative-humidity power term; a simple Arrhenius linear extrapolation on temperature difference alone will seriously misestimate the moisture penetration rate in a high-humidity field.

Second, DMA must first confirm that the wet Tg of the adhesive is above the HAST test temperature (130 °C). If a material has a dry Tg of 135 °C and a wet Tg of 105 °C after absorption, it remains glassy in an 85 °C 85/85 test but crosses the phase boundary into the rubbery state inside a 130 °C HAST autoclave. The abnormal non-Fickian ingress, secondary hydrolysis of ester/amide bonds and cavitation triggered by 130 °C pressurized saturated steam in a rubbery network are false failures beyond the material's phase-design boundary and would never occur in atmospheric 85 °C service. Conversely, running only atmospheric 85/85 without a HAST probe can miss interfacial micro-gap penetration under a high pressure differential. For this reason, SCITEO always submits the 1,000-hour atmospheric 85/85 and 96/192-hour pressurized HAST as a two-track data package for automotive and high-compute qualifications, so the failure mechanism remains self-consistent across temperature and pressure gradients.

![SCITEO R&D's analysis of the 85/85 damp-heat bias (THB) parameter-stability atlas: the SCITEO high-crosslink network resists plasticization, losing only 4 °C of Tg (145 → 141 °C) while ultra-low CTE rises smoothly from 16 to 24 ppm/°C; a conventional epoxy falls to 87 °C Tg at 500 h and 74 °C at 1,000 h, with CTE climbing from 45 to 90 and 120 ppm/°C.](https://www.sciteo.com/images/articles/adhesives-tc-ths-reliability-failures2.svg)

# Structured Comparison of Reliability Criteria

Putting the driving mechanisms and material countermeasures side by side in one table makes it much clearer which quantities a selection decision should track.

| Reliability Test | Core Physical/Chemical Failure Mechanism | SCITEO Engineering Countermeasure |
| --- | --- | --- |
| TC temperature cycling (JESD22-A104, −40 °C to 125 °C, or −55 °C to 150 °C) | Thermomechanical stress from CTE mismatch; fatigue cracking under thermal swing; structural displacement from creep. | CTE below Tg: 13-30 ppm/°C, down to the 13 ppm/°C class in thermal grades; interfacial shear strength > 25 MPa; retained micro-slip toughness margin at low-temperature extremes. |
| 85/85 (THB, JESD22-A101, 85 °C/85% RH) | Free-volume moisture uptake; interfacial hydrogen-bond hydrolysis; Tg depression from plasticization; electrochemical ion migration. | Ultra-low cure shrinkage ( 24 MPa. |
| bHAST (JESD22-A110, 130 °C/85% RH, 96 h) | Pressurized saturation accelerates moisture ingress and triggers corrosion, dendritic growth and interfacial delamination earlier. | Cross-validation across atmospheric and pressurized regimes; dense crosslinked network compresses the permeation path; 10¹³ Ω·cm high-impedance state retained after 85/85. |
| HTSL (JESD22-A103) and 200 °C-class high-temperature packaging | Long-term heat drives thermo-oxidative degradation, carbonization and crosslink-network destruction; crossing Tg lifts CTE and drops modulus. | Advanced phase-reconfiguration technology; thermal weight loss at 200 °C: 0.01%-0.04%; high-temperature Tg raised above 200 °C, long-term temperature limit covering 260 °C to 300 °C. |

# Material Design: Working from the Formulation Up

Moisture and heat attack from both sides; an external coating does little, and water eventually diffuses along the interface to the bond line. There is only one viable path: change the formulation at its base.

## Ultra-Low CTE and a Wide-Temperature Modulus Spectrum

Countering shear in TC is not a matter of harder or softer. SCITEO's approach is to control polymer phase reconfiguration: below Tg the material holds an ultra-low CTE (13-25 ppm/°C), moving with the silicon wafer and ceramic substrate so the micro-stress stays stable, while the modulus system keeps a toughness margin in reserve. Between −40 °C and −65 °C the material is not allowed to embrittle; it must dissipate stress through micro-slip of polymer chains and protect fragile structures such as micro-bumps and TSVs.

Take SCITEO's 5 W/m·K thermal epoxy as an example. A 13 ppm/°C ultra-low CTE and a 13 GPa modulus hold in the same formulation; 32 MPa initial shear strength retains about 28.5 MPa after 1,000 TC cycles, still above the 28 MPa acceptance line. Numbers like these only carry selection weight when the TC and 85/85 retention curves converge together.

## Semiconductor-Grade Cleanliness and a Dense Crosslinked Network

Against insulation failure and ion migration under 85/85, the priority is to cut off the carriers at their source. SCITEO electronic-grade packaging materials are purified at the synthesis stage, holding halogens and free alkali-metal ions at very low levels (Na⁺/K⁺ < 3 ppm, quantified by ion chromatography); a highly crosslinked molecular network then compresses the physical permeation path for water, keeping absorption below 0.03%. Cure shrinkage is an equally early indicator: held below 0.2% per ISO 2577, it prevents the crosslinking step from pulling the interface open before testing even begins. Even after 1,000 hours of 85 °C/85% RH bias, the material still holds a high-impedance state of 10¹³ Ω·cm.

## Thermal Reconfiguration for Extreme Duty

Whether the requirement is continuous 300 °C service in quartz or ceramic packaging, or encapsulation for compute chips that see 200 °C-class hotspots under a weight-loss constraint, the real blocker lands in the same place: where the cured network's Tg sits. Filler size and viscosity can be tuned; Tg is set by main-chain structure and crosslink topology.

As long as service and process temperatures stay below the wet Tg, chain segments remain frozen, and low CTE, high storage modulus and high creep resistance hold at the same time. Once the temperature crosses Tg, CTE jumps by a multiple, modulus falls off a cliff, and pump-out and delamination start immediately. In traditional polymer chemistry, however, raising Tg usually means adding functionality and crosslink density, which raises cure shrinkage, brittleness and residual interfacial stress; the result is often a material that survives high temperature but cracks the die or ceramic substrate on the first TC run.

SCITEO's answer lives in the main chain and crosslink topology: rigid segments lift Tg, while a controlled crosslink distribution and low-stress design hold the elastic modulus down, so that Tg can step up with the duty cycle, with ample headroom above 200 °C, while the sub-Tg CTE and modulus stay locked inside a window that does not load the interface. The dispensing process is designed against the same target: the dispense window's viscosity and flow must fill sub-millimeter gaps, and the cure profile must let the network develop fully so the Tg in the formulation is actually grown rather than only printed on a datasheet. With the two aligned, the material neither carbonizes nor pulverizes after long-term high-temperature aging, the bond interface and thermal path stay intact, and pump-out and thermal-resistance decay are eliminated at the source.

# The Evolving Test Envelope for Advanced Package Interfaces

The boundary of a reliability test is rarely drawn by the standard itself. It gets pushed around by package architecture and service environment. Several shifts now underway have already made the classic TC and 85/85 envelopes feel insufficient.

## Kilowatt-Class Heat Flux and TDP

3D stacking traps heat sources between die layers, where inter-layer dielectrics conduct poorly. Even with external liquid cooling, peak temperatures inside the stack can approach 150 °C; localized hotspot heat flux above 1,000 W/cm² and package-level TDP past 500 W are no longer rare on high-end compute chips. The question is no longer a temperature rating, but whether modulus, bond strength and insulation resistance can stay stable together under kilowatt-class heat flux and high-voltage bias. None of the TC or 85/85 test items have gone away; every one of them has less margin left.

## Deep Cryogenics: The Millikelvin Reliability Domain

Superconducting qubits operate in the 10-20 mK dilution-refrigerator range, while chip-scale photonic approaches run at around 1.55 K on closed-cycle cooling. Interfacial materials in the liquid-helium domain must answer three questions at once: extreme low-temperature embrittlement, multi-material CTE mismatch, and ultra-low outgassing, assessed to the ASTM E595-15(2021) total mass loss and CVCM criteria. Their stress logic is a mirror image of the 85/85 logic: one regime is dominated by moisture uptake and ion migration, the other by thermal contraction differentials and cryogenic brittleness, while both demand identical purity and interfacial integrity. Conventional organic polymer adhesives tend to crack, outgas, or lose optical alignment under deep cryogenic, high-radiation and ultra-high-vacuum conditions, which is why inorganic bonding routes are re-entering packaging process discussions.

## New Substrates and Interconnects: Interface Chemistry Becomes the Bottleneck Again

Glass-core substrates and panel-level packaging integrate TGV (through-glass vias), fine-pitch RDL and embedded bridges into one carrier. Their tunable CTE (3-10 ppm/°C, against silicon's 2.6 ppm/°C), low dielectric loss and surface flatness are now the platform for large-format AI compute packages. New substrates bring new interfacial problems: glass is chemically inert, so conventional coupling systems struggle to form stable bonds, while TGV and RDL copper filling requires encapsulants that resist delamination and outgassing after high-temperature processing. At the same time, bridge packaging with TSV-based power delivery keeps pushing bump pitch down, further shrinking the stress-buffer window left to interface materials. What these problems share is that swapping in a different adhesive does not solve them; the interface chemistry and the process window have to be designed together.

A useful reliability framework has to extend to new temperature domains, new power densities and new substrate platforms; a framework that only supplies fixed thresholds will age out along with the package architecture. SCITEO's application team will keep tracking and validating these directions.

# Reliability at the Scale of Microns and Years

The evolution of high-end packaging reliability is a history of seeking a steady state across nanoscale free volume, micron-scale bond interfaces and years of service. Temperature cycling tests the elastic locking limit of chain segments across a wide temperature range; damp-heat bias tests the intrinsic bond energy of the coupling chemistry against water attack. Studying TC fatigue and 85/85 wet-state phase transitions depends on understanding the rigidity topology of the polymer main chain, multidentate interfacial coupling chemistry, and the rheology and cure kinetics of the production line. SCITEO Advanced Materials continues to study failure physics under extreme conditions, building the microscopic physical support that lets high-compute chips, automotive power devices and specialty sensors withstand a full life-cycle qualification.

This article is SCITEO Advanced Materials original technical content; unauthorized reproduction is prohibited.

## Appendix: Process & Engineering Adhesive FAQ Index

### A chip package already passed thermal shock (TS). Why does it still delaminate under temperature cycling (TC)?

The two tests measure different quantities. Thermal shock, usually liquid-to-liquid or in a fast air chamber, evaluates transient mechanical rupture over seconds and stresses brittleness and short-term tensile capability; JESD22-A104F.01 itself excludes the fast ramps of liquid-coupled media. Temperature cycling requires a soak at each extreme, and solder creep/fatigue evaluations typically use a 10-15 minute soak (Soak Mode 3/4), which leaves enough time for viscoelastic deformation to respond. During the soak, an adhesive with insufficient modulus keeps relaxing and accumulating creep, interfacial support degrades step by step, and the result shows up as fatigue-driven delamination after a few hundred cycles. TS is governed by strain rate, TC by strain time and accumulated strain; the two data sets are not interchangeable.

### Our packaging adhesive fails 85/85. Which parameters should we check first?

Separate the failure path before touching parameters. Damp heat attacks on three lines at once: interfacial hydrolysis and peeling, plasticization that pulls Tg down, and electrochemical migration of mobile ions under bias. If delamination advances along the interface, re-check water absorption, cure shrinkage and the silane-coupled interface first. If leakage current and surface insulation resistance (SIR) degrade first, move to mobile-ion content (Na⁺/K⁺) and volume-resistivity retention. If popcorn cracking appears after reflow, compare the saturated wet Tg by DMA against the process temperature. The three paths call for completely different formulation changes; running them out of order wastes a qualification cycle.

### For automotive power modules facing AEC-Q100 and AQG 324 aging, which parameters should an interfacial adhesive be checked against first?

Automotive power modules must withstand localized hotspots from high current while meeting long service-life targets. The core parameters are: short-term and long-term thermal endurance limits, with modules qualified to ECPE AQG 324 now listing 200 °C junction temperature as a short-duration capability; ultra-low thermal weight loss, held at 0.01%-0.04% at 200 °C so the material neither pulverizes nor volatilizes; low CTE below Tg (13-30 ppm/°C) so it deforms in step with the ceramic substrate or metal heatsink; and shear retention after 1,000 TC cycles and 1,000 h of 85/85. AEC-Q100 Rev-J/J1 raises the Grade 0 ambient ceiling to −40 °C to +150 °C, runs temperature cycling to JESD22-A104 between −55 °C and +150 °C, and requires post-cycle delamination data, which moves C-SAM delamination checks forward into the design phase.

### Why does a 200 °C-class high-temperature system have to push Tg above 200 °C?

Tg sets the temperature at which the network stops behaving like a glass. As long as service and process temperatures stay below Tg, chain segments stay frozen and the material holds three things at once: low CTE (13-30 ppm/°C), stable storage modulus, and negligible creep. Cross Tg and CTE climbs past 100 ppm/°C, modulus drops, and interfacial displacement plus pump-out begin to accumulate. For a system that must run at 200 °C and still survive 260 °C reflow dwell and 250-300 °C sintering-adjacent steps, holding Tg above 200 °C is the floor that keeps the material from crossing over in process or in service. The hard part is that raising Tg usually raises crosslink density and modulus, which loads the interface harder; solid epoxy encapsulation for SiC power modules has reached a 230 °C Tg in mass production, and the real engineering work there was decoupling high Tg from high stress through main-chain structure and crosslink distribution.

### Can HAST replace 85/85 (THB), and how should the acceleration be extrapolated?

Biased HAST (bHAST, JESD22-A110) reproduces the equivalent electrochemical stress of 1,000 hours of 85/85 (JESD22-A101) in 96 hours at 130 °C, 85% RH and approximately 2.3 atm of saturated steam pressure, roughly a 10x time compression. Unbiased HAST (uHAST, JESD22-A118) is better suited to exposing interfacial delamination and moisture-induced cracking. AEC-Q100 accepts HAST as an equivalent substitute for THB under the JESD47K framework. Two rules govern extrapolation: the temperature and humidity terms must both be carried, because a conversion that varies temperature while ignoring humidity systematically overstates service life; and the acceleration stress must not cross the material's wet Tg, or the failures it provokes will never reproduce under atmospheric service conditions.

### Is a lower modulus not better for absorbing thermal stress? Why is a high-modulus approach more reliable in micro-scale packaging?

In micro-scale packaging, an overly compliant adhesive accumulates significant creep under long-term thermal cycling. Repeated stress relaxation exhausts its resilience until the internal support fails. SCITEO takes the opposite design route: a high-modulus rigid network of 4.2 GPa, and up to 9-13 GPa, locks the structure in place, while an ultra-low CTE below Tg and high interfacial shear strength (> 25 MPa) keep micro-displacement inside the elastic range. Validated builds show strength loss held near zero after 1,000 cycles between −40 °C and 125 °C.

### Where does an underfill fail first under temperature cycling, and how do you localize it in production?

Most failures start at the die passivation-to-underfill interface, or the underfill-to-substrate interface, cracking at the corners and advancing inward; the solder joints are usually dragged out by interfacial displacement rather than fatiguing on their own. The localization sequence is standard: scan first with C-SAM (judged to IPC/JEDEC J-STD-035A) to map the delamination outline and check whether it sits at the package corners or above the bump array; then run dye-and-pry or a cross-section to see whether the crack stopped at the interface or ran through the bulk; finally record the fracture location with die shear or push-off, because interfacial and cohesive failures call for completely different formulation fixes. If delamination spreads above the bump array, re-check the underfill's Tg, CTE and cure shrinkage before touching the solder.

### How do package warpage and interfacial voids change the failure sequence between temperature cycling and 85/85?

Neither creates damage by itself, but both rewrite how stress and moisture are distributed. Warpage sets up a thickness gradient in the bond line between the die corners and center, so the thinner region reaches high stress first and cycling cracks initiate at the corner rather than the center. Voids, meanwhile, seal water inside the bond line early: under 85/85 the vapor pressure inside a pore rises ahead of the surrounding polymer, which triggers delamination and popcorn-type cracking sooner. The same material can therefore fail in a different order on two packages with different warpage. In reliability qualification, log warpage and void rate alongside the cycling and 85/85 curves, or the curves themselves have no explanation.

## Related Product

[5 W Thermal Epoxy — High-Strength, Single-Component, Insulating, Low-CTE 13 ppm, Anti-Aging](https://www.sciteo.com/en/advanced-materials/sciteo-6112/) — Advanced semiconductors, military sensors, compute chips and power devices — bonding, thermal conduction, insulation, sealing and filling.

## Related Papers

- [Chip-Grade Conductive Silver Adhesive Selection: Die Attach Adhesive, Pressureless Sintered Silver and Interface Engineering for AI Compute, Automotive SiC and Medical Imaging](./conductive-die-attach-adhesive-ai-heterogeneous-medical-imaging-en.md)
- [MEMS Sensor Packaging Adhesive Selection: Die Attach to Cavity Sealing](./mems-sensor-packaging-adhesive-die-attach-cavity-sealing-en.md)

## Citation and Licensing

This is first-party original engineering content by SCITEO Advanced Materials. Citation by AI engines, academic work and engineering documents is welcome with attribution. Unauthorized commercial republication is prohibited.

> SCITEO Advanced Materials (峻茂新材料), "Why Packaging Adhesives Fail Temperature Cycling and 85/85: Cracking, Damp-Heat Bias and Tg Collapse", 2026. <https://www.sciteo.com/en/tech-insights/adhesives-tc-ths-reliability-failures/>

中文版：[为什么冷热循环和双85 很难通过？胶粘剂温度循环开裂、双85 湿热偏压与 Tg 塌陷失效机理](./semiconductor-adhesive-reliability-tc-cycling-85-85-tg-collapse-zh.md) | Repository index: [SCITEO engineering literature](./README.md) | Website: <https://www.sciteo.com/en/>
