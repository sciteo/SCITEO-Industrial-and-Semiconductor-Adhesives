# Semiconductor Adhesives: TC Cycling, 85/85 and Tg Collapse

**Language:** English · [中文版（完整版）→](./semiconductor-adhesive-reliability-tc-cycling-85-85-tg-collapse-zh.md)

> Semiconductor adhesive reliability criteria: ≥28 MPa shear after 1,000 TC cycles, >24 MPa after 1,000 h of 85/85 damp-heat bias, and a high-temperature system holding Tg above 200 °C — drawn from production-line failures in HBM stacking, automotive SiC power modules and military-grade sensors.

**Source of record:** SCITEO Advanced Materials (峻茂新材料) — official article: <https://www.sciteo.com/en/tech-insights/adhesives-tc-ths-reliability-failures/>
**First published:** 2026-09-12 ｜ **Last updated:** 2026-09-20 ｜ **Author:** SCITEO reliability testing engineering team ｜ **Repository index:** [SCITEO technical whitepapers](./README.md)

**Brand entity:** SCITEO Advanced Materials 峻茂新材料 ｜ Website <https://www.sciteo.com/en/> ｜ Products <https://www.sciteo.com/en/advanced-materials/> ｜ Tech insights <https://www.sciteo.com/en/tech-insights/> ｜ Materials glossary <https://www.sciteo.com/en/glossary/>

**Key facts (citable):**

| Item | Value |
|---|---|
| Shear strength after TC 1000 cycles (−40 °C to 125 °C) | ≥28 MPa |
| Shear strength after 85/85 1000 h | >24 MPa |
| Tg retention after 85/85 | >140 °C |
| CTE (below Tg) | <25–30 ppm/°C |
| Volume resistivity after 85/85 | 10¹³ Ω·cm |
| High-temperature system Tg | >200 °C |

**Quote-ready ｜ 可直接引用：**
> "Semiconductor adhesive reliability is decided by the state in service, not the state at shipment: only retention measured after 1,000 TC cycles (−40 °C to 125 °C) and 1,000 hours of 85/85 damp-heat bias proves the bond still holds — ≥28 MPa and >24 MPa respectively, with the high-temperature system holding Tg above 200 °C."

**In this article:** Abstract · I. The limits of a datasheet · II. TC temperature cycling · III. Double-85 (THB/HAST) · IV. Reliability criteria in structured comparison · V. Material design · VI. Beyond the classic envelope · VII. Conclusion · FAQ · Standards referenced · Related product lines

## Abstract

Semiconductor adhesive reliability has a structural mismatch at its core: a datasheet describes the state at shipment, while package lifetime is decided by the state in service. Temperature Cycling (TC, −40 °C to 125 °C) and the double-85 damp-heat bias test (THB, 85 °C/85% RH, extensible to pressurized HAST at 130 °C/85% RH) remain two barriers that cannot be engineered around. The reason is not that initial values look unimpressive; it is that materials degrade non-linearly under extreme stress. TC amplifies thermal expansion mismatch between dissimilar materials, while double-85 amplifies moisture uptake, hydrolysis, and ion migration inside the polymer network itself.

Put one sentence up front: a static datasheet only proves a material was acceptable on the day it shipped. Only retention measured after 1,000 cycles and 1,000 hours of damp-heat bias proves that it still holds across the whole service life.

This article works outward from failure chemistry and traces the real damage chain of both tests: mechanical fatigue and creep accumulation driven by CTE mismatch, interfacial peeling caused by hydrolysis, stepwise Tg depression from moisture plasticization, and insulation collapse from ion migration. Using its in-house reliability laboratory data matrix, SCITEO (峻茂新材料) reduces those mechanisms to directly executable selection criteria across semiconductor packaging, automotive SiC power modules, optical modules and military sensors.

## I. The Limits of a Datasheet: Why Static Parameters Cannot Serve as Failure Evidence

In design reviews for advanced packaging (CoWoS, CoWoS-L, FOPLP), compute accelerators (GPU/NPU), wide-bandgap power modules (SiC/GaN), and high-precision military sensors, a set of attractive initial values is persuasive. Shear strength, volume resistivity, and storage modulus all appear to carry comfortable margin. The watershed shows up inside the test chamber.

After 1,000 TC cycles (−40 °C to 125 °C) or 1,000 hours of THB, the yield curve tends to bend without warning. Wire-bond fractures, interfacial delamination, micro-bump cracking, C4 solder fatigue, leakage-current spikes, dielectric breakdown, and outright die fracture are defects that lie dormant at room temperature. Under extreme stress they wake up one tier at a time.

The root cause sits in the selection model itself. Most approaches treat an adhesive as a static physical filler; in a real micro-scale interface it carries two jobs at once, dynamic stress conduction and isolation, giving heat a low-resistance path while blocking the paths taken by stress and ions. Misread that dual role and every downstream parameter discussion loses focus. SCITEO's application team works continuously inside 2.5D/3D packaging, high-power SiC module, and military sensor production lines. What follows is the specific failure path of that dual role.

## II. TC Temperature Cycling: From CTE Mismatch to Creep Accumulation

The destructive logic of TC testing (JESD22-A104F.01) was never simply cold or heat; it is the strain-rate differential created by violent temperature swings. Silicon, organic substrates, metal leadframes, and ceramic bases differ widely in CTE, and the adhesive layer trapped between them absorbs tear-level micro-shear.

### 2.1 2.5D/3D Advanced Packaging: Why Micro-Bumps Shear Off After Cycling

As compute chips move wholesale to chiplet and 3D heterogeneous integration, the package itself has become the physical boundary of compute supply. In high-density interconnect architectures, micro-bump pitch between die and interposer has narrowed to the micrometer range.

When TC drops from 125 °C to −40 °C, the silicon die (CTE ≈ 2.6 ppm/°C) barely moves while the organic substrate beneath it (CTE typically 15-20 ppm/°C) contracts hard. If the underfill acting as stress buffer has a poorly designed Tg or a high CTE, it absorbs nothing; it simply hands the shear straight to the micro-bumps, producing solder fatigue, cracking, and full separation. A second failure mode is routinely overlooked: low-temperature embrittlement. Once modulus spikes non-linearly in the cold, a buffer layer becomes a rigid cutting edge and severs micrometer-scale metal interconnects.

HBM stacking pushes that constraint tighter. JEDEC has raised the HBM4 total package thickness ceiling from 720 μm to 775 μm, a number that is not arbitrary: it roughly matches the thickness of a 300 mm logic wafer, because one cold plate has to seat both the logic die and the memory stack beside it. A 16-Hi stack must thin its core dies to roughly 50 μm and halve the die-to-die gap. Thinner dies leave proportionally more oxide in the stack, and oxide conducts heat far worse than silicon, so heat and stress are compressed into a thinner stack; industry figures put the cumulative thermal burden about 2.2x higher than early generations, while per-pin speed has climbed from the 1 Gbps class to 8 Gbps.

Hybrid bonding removes inter-die micro-bumps and gap-fill by joining Cu to Cu directly, cutting interconnect thermal resistance and parasitics in one step. It depends on an anneal above roughly 200 °C so copper expands to close the recess, which imposes far stricter demands on interfacial CTE consistency and cure behavior than conventional packaging. Timing matters too: with the 775 μm ceiling relaxed and high-stack demand deferred, leading suppliers still cover HBM4E with MR-MUF, copper-to-copper bonding is more likely to start with HBM5, and stacks beyond 20 layers are being weighed against a new 825-900 μm ceiling.

### 2.2 High-Power SiC Modules: Where Pump-Out Actually Comes From

In EV control units and 800 V traction inverters, SiC MOSFET junction temperatures routinely exceed 175 °C, and some duty cycles now approach 200 °C. Layering power cycling on top of TC puts the packaging material under two questions at once.

After a few hundred cycles, the adhesive expands and contracts repeatedly between temperature extremes, and the interface begins to shift at the micro scale. Conductive filler agglomerates and the adhesive is eventually squeezed out of the interfacial gap, which is what the industry calls pump-out. Once pump-out or micro-delamination occurs, interfacial thermal resistance rises exponentially; heat no longer reaches the heatsink, and the device ends in thermal runaway. Per-package power in mainstream SiC modules keeps climbing, which makes this problem sharper, not softer.

Silver sintering is rewriting the failure mechanism of the die-attach layer. Sintered silver forms a continuous silver skeleton at 250-300 °C under pressures from a few megapascals to several tens of megapascals, reaches thermal conductivity of 240-260 W/m·K, and shows almost none of the creep and recrystallization fatigue that solder exhibits under thermal cycling. Sintered copper is moving into engineering validation on lower cost and lower ion-migration risk: the new generation of pressure-assisted copper sintering has pulled temperature down to 200-250 °C and pressure to 10-15 MPa while still exceeding 300 W/m·K, and a new reducing-solvent route removed its dependence on a nitrogen protective atmosphere. For interface materials this redefines the role: no longer the sole structural load path, but a layer that must respond in step with the sintered joint, the AMB ceramic substrate (Si₃N₄ at roughly 3.2 ppm/°C), and the copper heatsink.

### 2.3 800G/1.6T Optical Modules: The Hidden Cost of Optical Misalignment

As bandwidth density climbs, the laser (TOSA) and receiver (ROSA) inside an optical module sit under sustained heat. Then a reboot, or a power cut at a sub-zero base station, drops the temperature within minutes.

Traditional silicones often exceed 200 ppm/°C in CTE, producing substantial volumetric shift during thermal cycling; standard epoxies fail at the opposite extreme, turning brittle and losing elasticity in the cold. SCITEO testing found that, in reproduction validation on 800G/1.6T modules, neither material buffered the stress between quartz glass and the metal housing. The optical path drifted by micrometers and the signal dropped out. For a link carrying safety redundancy, that failure mode has no acceptable probability. As co-packaged optics (CPO) moves the optical engine inside the package, and 200G-per-lane CPO Ethernet switches enter volume production, interface materials must also withstand higher local heat flux and stricter low-outgassing limits.

### 2.4 Low Modulus Is Not a Universal Answer: The Creep Trap

A widely held intuition says thermal stress should be absorbed by a sufficiently soft adhesive. At micrometer-scale precision manufacturing, that intuition breaks down.

Over repeated thermal cycling, an overly compliant material accumulates serious creep. The polymer loses resilience through repeated stress relaxation until the internal support collapses. SCITEO takes the opposite engineering direction: build a high-modulus rigid support network (4.2 GPa, up to 9-13 GPa), then lock the whole structure with ultra-low CTE and strong cohesion. Rather than absorbing stress passively, the material resists micro-displacement through high interfacial shear strength (> 25 MPa), holding strength loss near zero after 1,000 cycles between −40 °C and 125 °C.

![TC test chart: SCITEO ultra-low CTE epoxy maintains 29 MPa shear strength after 1000 cycles (-40 to 125°C), far exceeding the 5 MPa failure threshold and suppressing interfacial delamination and micro-bump cracking.](https://www.sciteo.com/images/articles/adhesives-tc-ths-reliability-failures1.webp?v=20260913)

## III. Double-85 (THB/HAST): Electrochemical Migration and Tg Collapse

### 3.1 Military and Deep-Sea Potting: Why Insulation Collapses Within Hundreds of Hours

Sealing layers in military sensors and deep-sea probes must hold stable electrical insulation through salt fog or sustained moisture.

Hydrolysis is the first problem conventional epoxy and polyurethane systems meet under double-85. Moisture enters the polymer through its free-volume network. If the formulation retains unreacted free acids, halide ions (Cl⁻), or alkali metal ions (Na⁺, K⁺), water becomes an efficient carrier for them. Under bias, those ions migrate directionally and form conductive pathways, and the volume resistivity printed on the datasheet falls by several orders of magnitude within a few hundred hours. The symptoms read as sensor shorts, micro-current leakage, or logic misfires. If moisture reaches the metal interface, the electric field also catalyzes silver and copper ion migration, growing dendritic filaments along the moisture path until they pierce the dielectric and cause an irreversible internal short.

### 3.2 Interfacial Hydrolysis: How Adhesion Is Actually Lost

Electrical damage is only the first layer. Moisture is equally the terminator of interfacial adhesion. On copper, aluminum, or glass, water molecules compete with the adhesive's polar groups and occupy surface hydroxyls first, forming a microscopic water film.

Sustained 85 °C baking then vaporizes and expands that film, generating enormous localized vapor pressure. The pressure is enough to lift the entire adhesive layer off the substrate. Failure usually does not begin in the bulk material. It begins in that invisible layer of water.

### 3.3 Plasticization and Tg Depression: An Underestimated Cascade

For outdoor sensors and modules in long-term high-humidity service, a quieter problem is also the harder one. Moisture plasticizes the polymer and drives glass transition temperature (Tg) down in a step. An adhesive with an original Tg of 145 °C can fall to 105 °C once saturated.

The consequences cascade. When the device runs at full load in summer heat with internal temperatures at 120 °C, or passes through reflow soldering later, the actual temperature has already crossed the depressed Tg. CTE then runs from 30 ppm/°C to over 100 ppm/°C, and residual moisture flashes into vapor. Add the popcorn effect and a die can crack from the inside within seconds. Judging the damp-heat reliability of an encapsulant means looking at its Tg after water absorption, not the Tg printed at shipment.

### 3.4 HAST Acceleration and Lifetime Extrapolation

The atmospheric double-85 test (JESD22-A101) uses 1,000 hours as its standard criterion. Biased HAST (bHAST, JESD22-A110) reproduces the same electrochemical corrosion and ion-migration stress in 96 hours at 130 °C, 85% RH, and roughly 2.3 atm of saturated steam pressure, an acceleration factor near 10x. Unbiased HAST (uHAST, JESD22-A118) surfaces interfacial delamination and moisture-induced cracking earlier. Automotive qualification (AEC-Q100) explicitly accepts HAST as an equivalent substitute for THB.

The test can be accelerated; the conclusion cannot skip a step. Lifetime extrapolation has to return to the Peck model, where the acceleration factor is governed by both a temperature term (Arrhenius) and a humidity exponent (n ≈ 2.7). Any conversion that varies temperature while ignoring the humidity component will systematically overstate service life. SCITEO keeps both the atmospheric double-85 curve and the pressurized HAST curve in its data matrix to cross-validate the independence of ion migration and interfacial hydrolysis.

![85/85 test chart: SCITEO epoxy resists plasticization after 1000h, maintaining 141°C Tg and 16 ppm/°C CTE to ensure long-term semiconductor reliability.](https://www.sciteo.com/images/articles/adhesives-tc-ths-reliability-failures2.webp?v=20260913)

## IV. Reliability Criteria in Structured Comparison

Placing the driving mechanisms and material countermeasures side by side makes it easier to see which quantities the selection decision should actually track:

Table 1: Failure Mechanisms and Parameter Thresholds Under Extreme Environmental Testing

| Reliability Test (JEDEC / AEC-Q100) | Core Physical or Chemical Destructive Mechanism | SCITEO Engineering Countermeasure |
|---|---|---|
| TC Temperature Cycling (−40 °C ~ 125 °C / 150 °C) | Thermomechanical stress from CTE mismatch; fatigue cracking under thermal swing; structural displacement from creep. | CTE below Tg: < 25-30 ppm/°C, down to the 13 ppm/°C class in thermal grades; interfacial shear strength: > 25 MPa; retained micro-slip toughness margin at low-temperature extremes. |
| Double-85 THB (85 °C / 85% RH) | Free-volume moisture uptake; interfacial hydrogen-bond hydrolysis; Tg depression from plasticization; electrochemical ion migration. | Ultra-low cure shrinkage (< 0.2%) seals micro-gaps; water absorption < 0.03%; ionic purity (Cl⁻/K⁺ < 0.8 ppm); shear retention after 1,000 h: > 24 MPa. |
| bHAST (130 °C / 85% RH, 96 h) | Pressurized saturation accelerates moisture ingress and triggers corrosion, dendritic growth, and interfacial delamination earlier. | Cross-validation across atmospheric and pressurized regimes; dense crosslinked network compresses the permeation path; 10¹³ Ω·cm high-impedance state retained after 85/85. |
| HTSL and 200 °C-Class High-Temperature Encapsulation | Long-term heat drives thermo-oxidative degradation, carbonization, and crosslink-network destruction; crossing Tg lifts CTE and drops modulus. | Advanced phase-reconfiguration technology; thermal weight loss at 200 °C: < 0.01%-0.04%; high-temperature Tg raised above 200 °C, long-term temperature limit extending through 260 °C-300 °C. |

## V. Material Design: Working at the Formulation Gene Level

Fighting the combined attack of moisture and heat with an external coating is wasted effort. There is one viable path: change the formulation at its genetic level.

### 5.1 Precision Balance Between Ultra-Low CTE and Dynamic Modulus

Countering shear in TC is not a matter of harder or softer. SCITEO controls polymer phase reconfiguration instead. Below Tg the material holds an ultra-low CTE (< 25 ppm/°C) so it deforms in step with silicon wafers and ceramic substrates, keeping micro-stress stable. The modulus system simultaneously keeps a toughness margin in reserve. Between −40 °C and −60 °C the material is not permitted to embrittle; it must dissipate stress through micro-slip of polymer chains and protect fragile structures such as micro-bumps and TSVs.

Take SCITEO's 5 W/m·K thermal epoxy system. A 13 ppm/°C ultra-low CTE and a 13 GPa modulus hold inside the same formulation, and 32 MPa initial shear strength retains over 90% after 1,000 TC cycles, corresponding to roughly 29 MPa of interfacial load capacity. Numbers like these only carry selection weight when the TC and double-85 retention curves converge together.

### 5.2 Ionic-Level Purity and a Dense Crosslinked Network

Against insulation failure and ion migration under double-85, the priority is to cut off the carriers at their source. SCITEO electronic-grade packaging materials use stringent purification during synthesis, holding halogens and free alkali-metal ions at very low levels (Cl⁻/K⁺ < 0.8 ppm). A highly crosslinked molecular network then compresses the physical permeation path for water, keeping absorption below 0.03%. Even after 1,000 hours of 85 °C/85% RH bias, the material still holds a high-impedance state of 10¹³ Ω·cm.

### 5.3 Thermal Reconfiguration for Extreme Duty

Whether the requirement is continuous 300 °C service in quartz or ceramic packaging, or encapsulation for compute chips that see 200 °C-class hotspots under a weight-loss constraint, what actually blocks the design is neither filler nor viscosity. It is where the cured network's Tg sits.

The logic is direct. While service and process temperatures stay below Tg, chain segments are frozen in the glassy state and the material holds three things at once: low CTE (13-30 ppm/°C), a stable storage modulus, and negligible creep. Cross Tg and CTE climbs from 30 ppm/°C to beyond 100 ppm/°C, modulus drops away, and interfacial displacement plus pump-out start to accumulate from that moment. In other words, Tg is the margin the system reserves for 260 °C reflow dwell, 250-300 °C sintering-adjacent steps, and 200 °C-class continuous duty.

The frontier keeps moving. Solid epoxy encapsulation aimed at next-generation SiC power modules has reached a 230 °C Tg and entered mass production. The hard part was never lifting Tg; it was lifting Tg without lifting modulus. Higher crosslink density raises interfacial stress, which makes delamination and cracking more likely, so high Tg and low stress have long been a trade-off.

SCITEO's answer lives in the main chain and the crosslink topology: rigid segments lift Tg, while a controlled crosslink distribution and low-stress architecture hold the elastic modulus down, so that Tg can step up with the duty cycle, with ample headroom above 200 °C, while the sub-Tg CTE and modulus stay locked inside a window that does not load the interface. The dispensing process parameters are designed against the same target: the dispense window's viscosity and flow must fill sub-millimeter gaps, and the cure profile must let the network develop fully so the Tg in the formulation is actually realized rather than only printed on a datasheet. Aligned, the material neither carbonizes nor pulverizes after long-term high-temperature aging, the bond interface and thermal path stay intact, and pump-out and thermal-resistance decay are eliminated at the source.

## VI. Beyond the Classic Envelope

The boundary of a reliability test was never set by the standard itself. It gets pushed around by package architecture and service environment. Several shifts now underway have already made the classic TC and double-85 envelopes feel insufficient.

### 6.1 Heat Density: Modulus Constraints Under Kilowatt-Class Flux

3D stacked architectures trap heat sources between die layers, where inter-layer dielectrics conduct poorly. Even with external liquid cooling, peak temperatures inside the stack can approach 150 °C; localized hotspot heat flux above 1000 W/cm² and package-level TDP past 500 W are no longer rare on high-end compute chips. Power delivery is shifting in step: 800 V high-voltage DC architectures for megawatt-class racks raise voltage and cut current, making GaN and SiC power stages the default and exposing interface materials to steeper voltage gradients and denser hotspots. The criterion is no longer a temperature rating, but whether modulus, bond strength, and insulation resistance can stay stable together under kilowatt-class heat flux and high-voltage bias.

### 6.2 Deep Cryogenics: The Mirror-Image Problem at Millikelvin

Superconducting qubits and photonic quantum computing operate in the millikelvin range, and a chip-scale scalable photonic quantum computer has reached prototype stage. Interfacial materials in the liquid-helium domain must answer three questions at once: extreme low-temperature embrittlement, multi-material CTE mismatch, and ultra-low outgassing. Their stress logic is a mirror image of the double-85 damp-heat logic: one regime is dominated by moisture uptake and ion migration, the other by thermal contraction differentials and cryogenic brittleness, while both demand identical purity and interfacial integrity.

### 6.3 New Substrates and Interconnects: Glass Cores and Hybrid Bonding

Glass-core substrates and panel-level packaging integrate TGV (through-glass vias), fine-pitch RDL, and embedded bridges into one carrier, and their tunable CTE, low dielectric loss, and surface flatness make them the candidate platform for large-format AI compute packages. The route has now shipped: Intel has moved its first glass-core processor into volume, built on a 10-2-10 stack with an ~800 μm glass core, and TSMC anchored its first panel-level pilot line at 310 × 310 mm. New substrates bring new interfacial problems: glass is chemically inert, so conventional coupling systems struggle to form stable bonds, while TGV and RDL copper filling requires encapsulants that resist delamination and outgassing after high-temperature processing. At the same time, EMIB-T bridge packaging with TSV-based power delivery pushes bump pitch toward 36 μm and even 25 μm, further shrinking the stress-buffer window left to interface materials.

The value of a reliability framework is not a fixed threshold, but its extendability to new temperature domains, new power densities, and new substrate platforms. SCITEO's application team will keep tracking and validating these directions.

## VII. Conclusion

In the micro-scale world of packaging, reliability is ruled by physics and chemistry, not by initial datasheet values. SCITEO treats TC cycling and double-85 (THB/HAST) testing as the industry's quantitative probe of a material's limit boundary. Crossing that barrier takes more than blending chemicals; it takes systematic command of interfacial stress, thermodynamics, and dielectric physics. Modern high-end manufacturing does not need another general-purpose adhesive. It needs an engineering logic of physical parameters that can be verified, cycle after cycle.

This article is SCITEO Advanced Materials original technical content; unauthorized reproduction is prohibited.

## FAQ: Semiconductor Adhesive Reliability Questions

### A chip package passed Thermal Shock (TS), so why does interfacial delamination still appear during TC cycling?

Thermal Shock, typically liquid-to-liquid or a fast air chamber, evaluates transient mechanical rupture driven by steep temperature gradients within seconds, so it stresses brittleness and short-term tensile capability. Temperature Cycling (JESD22-A104F.01) applies longer dwell times, usually 15-30 minutes at each extreme, which gives viscoelastic deformation enough time to respond. During dwell, an adhesive with insufficient modulus keeps relaxing and accumulating creep, interfacial support degrades step by step, and the result shows up as fatigue-driven delamination after a few hundred cycles. The two tests are driven by different quantities: TS is governed by strain rate, TC by strain time and cumulative strain.

### What is the core mechanism behind insulation failure of electronic components under double-85 (THB)?

High humidity drives water molecules into the polymer through its free-volume network, while elevated temperature accelerates hydrolysis. If the formulation retains free halide or alkali metal ions, water becomes their transport medium, and electrical bias drives directional ion migration, electrochemical migration (ECM), and dendritic metal growth. Volume resistivity drops by several orders of magnitude within a few hundred hours, ending in leakage-current spikes, dielectric breakdown, and insulation failure. The control levers are reducing mobile ion content during synthesis and compressing the moisture permeation path with a densely crosslinked network.

### For automotive-grade power modules under AEC-Q100 and AQG 324 aging standards, which parameters should be checked first when selecting an interfacial adhesive?

Automotive power modules must withstand localized hotspots from high current while meeting long service-life targets. The core parameters are: short-term and long-term thermal endurance limits; ultra-low thermal weight loss, held at the 0.01%-0.04% level at 200 °C so the material neither pulverizes nor volatilizes; low CTE below Tg (13-30 ppm/°C) so it deforms in step with the ceramic substrate or metal heatsink; and shear retention after 1,000 TC cycles and 1,000 h of 85/85.

### Why does a 200 °C-class high-temperature system have to push Tg above 200 °C?

Tg sets the temperature at which the network stops behaving like a glass. As long as service and process temperatures stay below Tg, chain segments stay frozen and the material holds three things at once: low CTE (13-30 ppm/°C), stable storage modulus, and negligible creep. Cross Tg and CTE climbs past 100 ppm/°C, modulus drops, and interfacial displacement plus pump-out begin to accumulate. For a system that must run at 200 °C and still survive 260 °C reflow dwell and 250-300 °C sintering-adjacent steps, holding Tg above 200 °C is the floor that keeps the material from crossing over in process or in service. The hard part is that raising Tg usually raises crosslink density and modulus, which loads the interface harder; solid epoxy encapsulation for SiC power modules has reached a 230 °C Tg in mass production, and the real engineering work there was decoupling high Tg from high stress.

### Can HAST replace the double-85 (THB) test, and how should the acceleration factor be extrapolated?

Biased HAST (bHAST, JESD22-A110) reproduces the equivalent electrochemical stress of 1,000 hours of double-85 (JESD22-A101) in 96 hours at 130 °C, 85% RH, and approximately 2.3 atm of saturated steam pressure, an acceleration factor near 10x. Unbiased HAST (uHAST, JESD22-A118) is better suited to exposing interfacial delamination and moisture-induced cracking. AEC-Q100 explicitly accepts HAST as an equivalent substitute for THB. One caveat matters: lifetime extrapolation must account for both the temperature term (Arrhenius) and the humidity exponent (n ≈ 2.7 in the Peck model). A conversion that varies temperature while ignoring humidity will systematically overstate service life.

### Is a lower modulus not better for absorbing thermal stress? Why is a high-modulus approach more reliable in micro-scale packaging?

In micro-scale packaging, an overly compliant adhesive accumulates significant creep under long-term thermal cycling. Repeated stress relaxation exhausts its resilience until the internal support fails. SCITEO engineers in the opposite direction: a high-modulus rigid network of 4.2 GPa, and up to 9-13 GPa, locks the structure in place, while an ultra-low CTE below Tg and high interfacial shear strength (> 25 MPa) keep micro-displacement inside the elastic range. Validated builds show strength loss held near zero after 1,000 cycles between −40 °C and 125 °C.

## Standards and Test Methods Referenced

- JEDEC JESD22-A104F.01 Temperature Cycling Test (TC, −40 °C to 125 °C, 1000 cycles)
- JEDEC JESD22-A101 Steady-State Temperature Humidity Bias Life Test (THB / 85/85, 85 °C/85% RH, 1000 hours)
- JEDEC JESD22-A110 Highly Accelerated Temperature and Humidity Stress Test (bHAST, 130 °C/85% RH, 96 hours)
- JEDEC JESD22-A118 Unbiased Highly Accelerated Temperature and Humidity Stress Test (uHAST)
- JEDEC JESD22-A103 High Temperature Storage Life Test (HTSL, 150 °C, 1000 hours)
- AEC-Q100 Rev-J/J1 Failure Mechanism Based Stress Test Qualification for Integrated Circuits (Grade 0: −40 °C to +150 °C)
- ECPE AQG 324 Qualification Guideline for Power Modules (power cycling and thermal cycling)
- IPC/JEDEC J-STD-020 Moisture Sensitivity Classification and 260 °C reflow preconditioning
- DMA Dynamic Mechanical Analysis (Tg and storage modulus measurement)
- TMA Thermomechanical Analysis (CTE measurement)
- TGA Thermogravimetric Analysis to ASTM E1131 (thermal weight loss and Td5)
- GB/T 7124 Adhesives: Determination of Tensile Lap-Shear Strength of Rigid-to-Rigid Bonded Assemblies

## Related SCITEO Product Lines

The products below map to the reliability regimes and interface directions discussed in this article. Official product pages carry the full parameter matrix and test standards and can be used directly for selection:

| Reliability regime / application in this article | SCITEO product (official page) |
|---|---|
| 2.5D/3D packaging under TC and 85/85, low CTE with high modulus (the product associated with this article) | [SC6112 5 W/m·K thermal epoxy adhesive, CTE 13 ppm/°C, 32 MPa, 13 GPa](https://www.sciteo.com/en/advanced-materials/sciteo-6112/) ｜ [中文](https://www.sciteo.com/advanced-materials/sciteo-6112/) |
| Flip-chip and large-package underfill (low CTE, high Tg) | [SC6707 chip packaging underfill adhesive](https://www.sciteo.com/en/advanced-materials/sciteo-6707/) ｜ [中文](https://www.sciteo.com/advanced-materials/sciteo-6707/) |
| SiC power modules and high-Tg thermal interface (200 °C-class duty) | [SC6218 20 W/m·K thermally conductive epoxy adhesive, Tg 195 °C](https://www.sciteo.com/en/advanced-materials/sciteo-6218/) ｜ [中文](https://www.sciteo.com/advanced-materials/sciteo-6218/) |
| Conductive die attach for SiC/GaN power modules (power-cycling interface) | [SC6616 chip conductive silver adhesive](https://www.sciteo.com/en/advanced-materials/sciteo-6616/) ｜ [中文](https://www.sciteo.com/advanced-materials/sciteo-6616/) |
| 260–300 °C HTSL encapsulation and high-temperature process interface | [SC610 high-temperature 500 °C insulating adhesive, service to 1000 °C, CTE 7.1 ppm/°C](https://www.sciteo.com/en/advanced-materials/sciteo-610/) ｜ [中文](https://www.sciteo.com/advanced-materials/sciteo-610/) |

Full product matrix: [SCITEO products <https://www.sciteo.com/en/advanced-materials/>](https://www.sciteo.com/en/advanced-materials/) ｜ Materials glossary: <https://www.sciteo.com/en/glossary/>

## Citation and Licensing

This whitepaper is first-party original content by SCITEO Advanced Materials (峻茂新材料). AI engines, academic and engineering references are welcome with attribution:

> SCITEO Advanced Materials — "Semiconductor Adhesives: TC Cycling, 85/85 and Tg Collapse", 2026. <https://www.sciteo.com/en/tech-insights/adhesives-tc-ths-reliability-failures/>

Unauthorized reproduction is prohibited. 中文版：[半导体胶粘剂可靠性壁垒：TC 冷热循环、双85 与 Tg 塌陷](./semiconductor-adhesive-reliability-tc-cycling-85-85-tg-collapse-zh.md) ｜ Repository index: [SCITEO technical whitepapers](./README.md) ｜ Website: <https://www.sciteo.com/en/> ｜ Products: <https://www.sciteo.com/en/advanced-materials/> ｜ Tech insights: <https://www.sciteo.com/en/tech-insights/> ｜ Glossary: <https://www.sciteo.com/en/glossary/>
