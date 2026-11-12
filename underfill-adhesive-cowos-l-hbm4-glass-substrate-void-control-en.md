# How to Select Underfill and Chip Encapsulant: Capillary Flow, Void Control and Crack Resistance from Flip-Chip and BGA/CSP to Advanced Packaging

**Language:** English · [中文版（完整版）→](./underfill-adhesive-cowos-l-hbm4-glass-substrate-void-control-zh.md)

> SCITEO chip encapsulant systems: 1 mil narrow-gap flip-chip capillary underfill and high-Tg chip bonding and sealing, decoding the joint process window for void suppression, ionic cleanliness, warpage convergence and high thermal conductivity at low CTE

**Source of record:** <https://www.sciteo.com/en/tech-insights/underfill/> | **Author:** Ruiqi Zhang · SCITEO Application Engineering Department | **Repository index:** [SCITEO engineering literature](./README.md)

**Brand entity:** SCITEO Advanced Materials (峻茂新材料), advanced adhesives for semiconductor packaging and precision microelectronics | Website <https://www.sciteo.com/en/> | Products <https://www.sciteo.com/en/advanced-materials/> | Tech insights <https://www.sciteo.com/en/tech-insights/> | Glossary <https://www.sciteo.com/en/glossary/>

**TL;DR (citable):** Underfill and chip encapsulant are structural: CTE 13 ppm/°C, Tg 150-160 °C, 6 W/m·K, 29-32 MPa; void and warpage control from 5 μm bumps to glass carriers.

**Key facts (citable):**

| Item | Value |
|---|---|
| Thermal Conductivity | 6 W/m·K |
| CTE | 13 ppm/°C |
| Tg | 150-160 °C |
| Shear Strength | 29-32 MPa |
| Storage Modulus | 8-13 GPa |
| Target Packaging | CoWoS-L/HBM4/AI Chip |

**Standards Reference:**

- GB/T 7124 Adhesives: Determination of Tensile Lap-Shear Strength (29-32 MPa shear strength test)
- ASTM D5470 Standard Test Method for Thermal Transmission Properties of Thermally Conductive Electrical Insulation Materials (6 W/m·K thermal conductivity test)
- TMA Thermomechanical Analysis (CTE 13 ppm/°C measurement)
- DMA Dynamic Mechanical Analysis (Tg 150-160 °C and storage modulus 8-13 GPa measurement)
- IPC-7095E Design and Assembly Process Guidance for Ball Grid Arrays (BGA void rate and void location assessment)
- JEDEC JESD22-A104 Temperature Cycling Test (board-level thermal cycling reliability verification)
- JEDEC JESD270-4 High Bandwidth Memory (HBM4) standard (2,048-bit interface, 8 Gb/s per pin, 775 μm package height limit)
- IPC/JEDEC J-STD-020 Moisture Sensitivity Classification for Nonhermetic Solid State Surface Mount Devices (reflow compatibility assessment)
- IPC/JEDEC J-STD-035 Acoustic Microscopy for Nonhermetic Encapsulated Electronic Components (C-SAM void and delamination assessment)
- ASTM D2196 Standard Test Methods for Rheological Properties of Non-Newtonian Materials by Rotational Viscometer (capillary flow window assessment)

**In this article:** Abstract · Advanced Packaging Turns an Auxiliary into a Structural Material · Failure Mechanisms: Holding Stress, Voids, Ions, and Heat Paths in Unified Balance · Parameter Boundaries of SCITEO Chip Encapsulant and Underfill Formulations · SCITEO Engineering Methodology: Progressing Across Packaging Scales · Underfill Selection Matrix at a Glance · Lower Defect Density

# Abstract

The production yield threshold of a high-Tg chip encapsulant never hinges on whether a single metric can be pushed to its theoretical limit. It demands that low coefficient of thermal expansion (CTE), high glass transition temperature (Tg), narrow-gap capillary flowability and interfacial adhesion hold simultaneously inside one epoxy formulation. Compromising inorganic filler volume fraction merely to lower viscosity lets solder joint fatigue during reflow and thermal cycling breach the reliability floor almost immediately. Conversely, overloading filler to depress CTE induces particle bridging, filler filtration and severe flow stagnation at micron-scale clearances.

Generative AI training and inference workloads have shifted the compute bottleneck from transistor density to in-package interconnect density and thermomechanical boundaries. CoWoS-family 2.5D platforms co-package logic dies with multiple High Bandwidth Memory (HBM) stacks, micro-bump pitch contracts from tens of microns toward 5 μm, and accelerator thermal design power crosses the kilowatt threshold. Underfill is no longer an auxiliary dispensing consumable that merely cushions drop shock at the end of the line. It is a core structural layer that governs package warpage, resists solder extrusion and completes the vertical heat path. In CSP packages, power modules and precision sensors, high-performance chip encapsulants that combine narrow-gap capillary penetration with perimeter sealing move the acceptance criterion from "the gap is filled" to the joint optimum of void rate, interfacial stress, low outgassing and long-term thermal-cycle life. SCITEO Advanced Materials organizes its formulation matrix around this scale axis: CTE down to 13 ppm/°C, Tg 150 to 160 °C, thermal conductivity 0.8 to 6 W/m·K and lap shear 29 to 32 MPa, spanning 1 mil chip-level gaps through panel-level glass-core carriers.

## Core Parameter Comparison

The table below places the critical metrics of the SCITEO underfill and chip encapsulant series alongside conventional underfill formulations, enabling rapid gap analysis during packaging design reviews:

| Parameter | SCITEO Solution | Conventional Industry | Test Standard |
|---|---|---|---|
| CTE (Below Tg) | 13 ppm/°C | 30 to 50 ppm/°C | TMA |
| Tg | 150 to 160 °C | 80 to 120 °C | DMA |
| Thermal Conductivity | 6 W/m·K | 0.2 to 1.0 W/m·K | ASTM D5470 |
| Lap Shear Strength | 29 to 32 MPa | 10 to 15 MPa | GB/T 7124 |
| Mobile Ion Content | < 10 ppm | 30 to 100 ppm | Ion Chromatography |
| Cure Shrinkage | < 0.2% | 1.0% to 1.5% | Density Method |

# Advanced Packaging Turns an Auxiliary into a Structural Material

The semiconductor industry's performance narrative has pivoted from scaling down individual transistors to densely aggregating multiple dies. The single-exposure lithographic reticle limit remains fixed near 26 mm × 33 mm (approximately 850 mm²); scaling monolithic dies beyond this ceiling incurs a nonlinear yield penalty. Consequently, the industry has embraced chiplet disaggregation and advanced packaging, recombining compute, memory, and I/O dies across heterogeneous process nodes within a unified package envelope. In packaging failure analysis and SMT laboratories, underfill is brought back to the review table typically triggered by two telltale signatures: C-SAM acoustic micrographs revealing red acoustic delamination halos fanning outward from die corners following Moisture Sensitivity Level (MSL) preconditioning and 260 °C lead-free reflow; and cross-sectional SEM analysis after thermal cycling (TC) exposing fatigue micro-cracks at micro-bump roots or diagonal shear cracks cleaving from the fillet into the die passivation layer.

Historically in consumer electronic board assembly, underfilling BGAs and CSPs was primarily tasked with shoring up solder joints against drop impact and random vibration. However, with high-density flip-chip and multi-die heterogeneous integration becoming the architectural standard, a single package now aggregates logic compute dies, high-bandwidth memory stacks, and high-speed I/O interfaces, driving interconnect joint counts into thousands or tens of thousands. While package footprints expand to multiple reticle sizes, standoff heights and pitches are undergoing aggressive micron-scale compression. A localized wetting void or modulus mismatch within the underfill layer instantly concentrates accumulated thermal shear strains onto adjacent micro-bumps, precipitating early-life open-circuit failures.

## Large-Format 2.5D: Local Silicon Bridges Become the Dominant Architecture

The architectural backbone of CoWoS-family 2.5D integration has transitioned from full-span silicon interposers (CoWoS-S) and redistribution-layer interposers (CoWoS-R) toward CoWoS-L, which embeds localized silicon interconnect (LSI) bridges into an RDL interposer. By substituting full silicon interposers with local high-density bridges, CoWoS-L mitigates macro-warpage over large form factors, establishing itself as the high-volume vehicle for flagship AI accelerators. Packages scaling to 5.5× reticle sizes have entered high-volume manufacturing with yields holding stably above 98%, and roadmaps target even larger multiples. As package surface area steps up, interfacial area multiplies and cumulative CTE mismatches scale linearly, leaving virtually zero margin for individual interfaces: an expansion delta across a single layer is sufficient to manifest as catastrophic macroscopic warpage or delamination.

This marks the watershed in the structural role of underfill. In conventional flip-chip packaging, underfill merely filled inter-bump cavities and redistributed mechanical loads. In large-scale 2.5D packages, it actively governs warpage deflection and establishes primary vertical heat-flow conduits, graduating from a process consumable into a co-equal third structural layer alongside the silicon die and organic substrate.

## Narrow-Gap Capillary Infiltration

For packaging process engineers, the initial hurdle in underfill selection stems from the fundamental conflict between fluid rheodynamics and high-loading filler systems. As micro-bump pitch contracts from conventional flip-chip standoffs (>100 μm) down to sub-40 μm, and onward to the ultra-fine 10 μm down to 5 μm regimes targeted by next-generation packaging, the hydraulic radius between die and substrate shrinks drastically.

Governed by capillary flow dynamics, halving the standoff gap sharply raises capillary resistance. While reducing resin viscosity is the intuitive response to facilitate rapid filling, matching the cured epoxy's CTE to silicon and organic substrates demands exceptionally high volume loadings of spherical inorganic silica. If particle size distribution—specifically the upper cutoff diameter D99—and surface organosilane functionalization are improperly engineered, dense micro-bump arrays act as a micron-scale sieve. Large filler particles bridge at the dispensing entry, triggering severe filler filtration and flow-front stagnation. Consequently, filler concentrates heavily along the dispensing edge while the fluid that reaches the die center or egress boundary degrades into a resin-rich, filler-depleted zone. Upon thermal cure, this localized zone exhibits an uncontrolled CTE surge, creating an insidious nucleation site for thermal-fatigue cracking.

## Secondary Reflow Shock

In System-in-Package (SiP) modules and 2.5D heterogeneous assemblies, components with fully cured underfill must frequently endure secondary board-level lead-free reflow, where peak temperatures reach 260 °C. This thermal envelope imposes extreme demands on the high-temperature structural integrity of the underfill matrix.

As furnace temperatures surpass the solder melting range (approximately 217 °C to 220 °C), micro-bumps transition into a molten liquid accompanied by volumetric thermal expansion. If the underfill possesses an inadequate glass transition temperature (Tg), suffers rapid modulus decay at elevated temperatures, or harbors micro-voids and flux residue weak interfaces at bump collars from initial capillary filling, molten solder is driven by internal hydrostatic pressure along interfacial micro-fissures. This leads to catastrophic solder extrusion and inter-bump bridging shorts. Consequently, high-reliability underfill selection cannot rely solely on ambient die-shear strength; it requires rigorous verification of high-temperature storage modulus retention and reflow-shock resilience.

## Thermal Dissipation Pathways

As localized heat flux keeps climbing in high-compute chips and power-dense modules, heat extraction from the active die face toward the substrate becomes as critical as the primary backside path through thermal interface materials (TIM) to the cold plate. In an unfilled bump array, or one filled with conventional low-conductivity epoxy (~0.2 W/m·K), the resin-rich gaps act as thermal barriers and breed hot spots beneath high-speed SerDes interfaces or core logic. SCITEO raises the thermal conductivity of its underfill and chip encapsulant grades to 0.8 to 6 W/m·K while holding dielectric constant near 3.1 from 1 MHz to 1 GHz and volume resistivity at 10¹⁵ to 10¹⁶ Ω·cm, so junction temperature comes down without sacrificing micron-gap capillary wetting or high-frequency signal integrity.

# Failure Mechanisms: Holding Stress, Voids, Ions, and Heat Paths in Unified Balance

Silicon dies possess a nominal CTE of approximately 2.6 ppm/°C, whereas common BT or ABF organic packaging substrates exhibit planar CTE values ranging from 14 to 20 ppm/°C, with silicon interposers and glass carriers sitting closer to the silicon side, around 3 ppm/°C. As the assembled package cools from cure or 260 °C reflow down to room temperature—or endures harsh thermal cycling chambers from −55 °C to 125 °C—differential contraction rates between adjacent layers generate severe interfacial shear strains.

## Stress Redistribution and the Modulus Window

Governed by the Distance-to-Neutral-Point (DNP) formulation, corner micro-bumps furthest from the die's neutral geometric center bear the highest shear strain. Because micro-bump solder volumes are orders of magnitude smaller than traditional BGA spheres, their plastic strain absorption capacity is minimal; unencapsulated bumps rapidly succumb to low-cycle fatigue rupture within early thermal cycles. Once dispensed and drawn into the bump matrix via capillary suction, underfill polymerizes into a dense three-dimensional thermoset network that rigidly couples the die to the substrate. This mechanism redistributes concentrated shear loads uniformly across the entire adhesive interface, reverting solder joints to their core function as electrical and power conduits.

In engineering qualification, higher storage modulus is not inherently advantageous. An excessively rigid underfill becomes brittle at cryogenic and low temperatures. It not only initiates stress cracks along the outer edge of the dispensing fillet that tear into the substrate solder mask, but also transfers excessive thermomechanical shear stress directly into the mechanically fragile low-k and extreme low-k (ELK) dielectric stacks of the active die, cleaving fine copper interconnects. Conversely, an underfill with insufficient modulus fails to constrain solder deformation at elevated temperatures. Extensive packaging line validation confirms that an ambient storage modulus of 8 to 11 GPa represents the golden window, balancing fatigue protection for micro-bumps against fracture prevention for low-k layers. For ultra-thin stacked dies or MEMS assemblies, toughened low-modulus formulations are required to dissipate interlaminar peeling stresses. SCITEO provides a tiered modulus and fracture-toughness formulation platform, allowing direct mechanical impedance matching to customer package architectures.

![SCITEO engineering analysis of Distance-to-Neutral-Point versus solder shear strain in an isometric cutaway: the cross section displays silicon die, micro-bump array, underfill matrix, and organic substrate, where corner bumps with maximum DNP experience peak shear strain and fail first under γ = Δα × ΔT × DNP ÷ h, with red and blue strain curves showing the pronounced strain mitigation delivered by underfill](https://www.sciteo.com/images/articles/underfill3.svg)

## Void Control

Voids represent the primary catalyst for underfill failure; however, in production quality screening, spatial location carries far greater weight than aggregate void counts. Isolated micro-voids drifting along the outer edge of the fillet merely reflect minor exhaust pressure fluctuations during dispense termination. Conversely, voids anchored against micro-bump roots or dense interconnect traces serve as extrusion escape paths during reflow and trigger localized stress concentrations and thermal impedance spikes during service. In alignment with IPC-7095E assessment methodology, quality acceptance must jointly bind void area percentage with high-risk spatial zoning. SCITEO underfill systems reliably constrain overall void area fractions below 1% in volume production while guaranteeing zero voids at solder collars and critical interconnect zones. Following 1,000 thermal cycles from −45 °C to 125 °C, acoustic C-SAM reassessment demonstrates void growth below 0.5%, with zero newly formed delamination or collar micro-cracks.

Root-cause troubleshooting requires quantification prior to attribution: verify void fraction and coordinates before diagnosing dominant mechanisms. Voids dispersed along substrate margins point to entrapped gas caused by insufficient substrate preheating; voids aligned along converging fluid fronts indicate dispense trajectories that prematurely sealed vent paths; and voids clustered around pads signify no-clean flux residues that altered local surface energy and inhibited wetting. Interfacial compatibility with no-clean flux residues presents a persistent challenge: following flip-chip reflow, bump collars and substrate pads remain coated with ultra-thin films of rosin or synthetic resin residues. If the underfill's surface tension and polar functional groups fail to wet this chemistry, the advancing fluid front dewets like water on a lotus leaf, permanently locking air pockets around the bump neck. As bump pitch contracts to 15 μm and 5 μm, cavity cleaning becomes virtually impossible; the underfill's intrinsic surface activity and wetting tolerance toward trace residues dictate whether high-volume yield can be achieved.

Secondary contributors include moisture outgassing from organic laminates. BT and ABF substrates, along with solder mask layers, are inherently hygroscopic. Without rigorous pre-bake dehydration, trapped moisture vaporizes when heated on the dispensing chuck (60 °C to 100 °C) or inside the cure oven, boiling upward into the uncured resin to form scattered pinhole voids. Finally, dispense path and venting geometry remain critical. Flawed multi-pass dispense patterns cause rapid lateral edge flows to merge prematurely at the egress boundary, converting unfilled central cavities into dead zones that trap massive central air pockets.

## Hermetic Sealing and Mobile Ion Barriers

Micro-gaps inside the package are the pathways for moisture and ionic migration. The cured chip encapsulant must form a continuous sealing interface that cuts the moisture path and prevents electrochemical migration from causing insulation failure under high bias. Measured against MIL-STD-883 Method 5011 and ion chromatography, SCITEO's low-volatility, high-purity encapsulant grade holds Cl⁻ below 8 ppm and Na⁺ and K⁺ below 5 ppm each. Combined with ASTM E595 (125 °C / 24 h) total mass loss of 0.42% and condensable volatiles below 0.02%, shear strength retention stays in the 90% to 98% band after 1,000 h at 155 °C HTSL, 1,000 h of 85/85 damp heat and 1,000 cycles from −40 °C to 125 °C. For automotive and industrial power modules that serve in hot, humid environments, ionic cleanliness and damp-heat endurance decide device life more than initial room-temperature strength.

## Auxiliary Thermal Conduction

In high-power-density packages, the inter-bump void volume represents an inefficient thermal conduit. In conventional underfill formulations, the baseline epoxy matrix exhibits a bulk thermal conductivity of roughly 0.2 W/m·K, which rises to only 0.5 to 1.0 W/m·K when loaded with standard fused silica. In high-power processors or 3D stacked architectures, bottom logic dies or base dies remain sandwiched between the substrate and upper chips, obstructing upward heat escape. Thermally conductive underfill modified with engineered ceramic fillers converts this micro-gap into a low-thermal-resistance bridge. This not only accelerates lateral heat spreading into substrate thermal vias, but also homogenizes localized hot spots across the die plane, preventing high-current micro-bumps from succumbing to accelerated electromigration (EM) failure induced by thermal crowding.

# Parameter Boundaries of SCITEO Chip Encapsulant and Underfill Formulations

Within the SCITEO Advanced Materials laboratory, we engineer backward from specific packaging failure sites rather than optimizing isolated datasheet metrics. To serve diverse process requirements, SCITEO has developed multiple epoxy-based chip encapsulation and underfill families covering electrical insulation, high thermal conductivity and high-temperature endurance. Four core metrics define the selection boundary for large accelerator packaging and frame the trade-offs inside our formulation platform.

## CTE: Converging on Silicon-to-Substrate Composite Expansion

Warpage poses the ultimate risk in large-format packaging, originating from the cumulative mismatch of component CTEs across thermal swings. SCITEO leverages micro- and nano-scale silica filler loading to depress the cured underfill CTE to 13 ppm/°C, converging tightly toward the composite expansion profile of silicon dies and organic carriers. The reliability dividend for solder fatigue life is measured in orders of magnitude: the closer the underfill matches adjacent structural layers, the lower the cyclic interfacial shear stress, deferring fatigue crack initiation.

Depressing CTE inevitably drives an exponential rise in resin viscosity. To overcome the classic trade-off between ultra-low CTE and capillary fluidity, SCITEO filler engineering deploys multimodal particle size grading spanning sub-micron to micron regimes. This approach preserves high solids loading while drastically reducing inter-particle friction and shear packing resistance. Furthermore, rigorous top-cut filtering (D99 truncation) tailored to specific standoff heights, combined with organosilane surface grafting, ensures low interfacial surface tension and uniform resin wetting, eliminating filler settlement and particle bridging in narrow gaps.

## Tg and Storage Modulus: Preserving Rigidity Across Load Regimes

The glass transition temperature sets the ceiling above which the material loses rigidity. The SCITEO high-Tg underfill series reaches 160 °C, well above the full-load junction temperature band of a compute die. Under sustained load the matrix stays in the glassy state, supports the solder joints without softening or collapse, and keeps solder fatigue life inside its design envelope.

Tg and CTE must be evaluated in tandem; analyzing either metric in isolation obscures the actual failure sequence. If CTE is mismatched against silicon, cyclic shear strain accumulates continuously, cleaving the interface prior to mechanical yield. Conversely, if CTE is matched but Tg is insufficient, the modulus drop within the operating thermal window shifts the stress distribution, converting solder joints from protected nodes into the primary load-bearing path and exhausting fatigue margins.

## Thermal Conduction: Balancing Capillary Fluidity and Heat Transfer

Elevating bulk thermal conductivity typically requires increasing ceramic filler loading, which concurrently inflates viscosity, CTE, and matrix brittleness. SCITEO thermally conductive underfill achieves 6 W/m·K—nearly an order of magnitude higher than conventional formulations (0.2 to 1.0 W/m·K)—while maintaining low capillary viscosity to enhance heat dissipation without compromising narrow-gap wicking. Calibrating this balance demands exhaustive laboratory profiling: minor deviations in filler morphology or size distribution trade flowability against thermal transport, altering line-level fill times. Formulation selection must therefore rest on empirical rheological and thermal data.

When qualifying thermally conductive underfill, engineering teams should target interfacial thermal resistance measured under operational pressure and target Bond Line Thickness (BLT), rather than generic bulk conductivity values on a datasheet. Underfill thermal impedance is acutely sensitive to BLT and clamping pressure: thinner bond lines compress filler networks into continuous phonon pathways, yielding higher apparent conductivity where sample-to-sample variance often exceeds formulation differences. Standardizing clamping pressure and BLT establishes the true baseline for cross-material comparison. Only when void-free, dense filling is achieved within target micro-scale gaps can high bulk conductivity translate directly into suppressed die junction temperatures.

## Interfacial Adhesion and Low Ionic Contamination

During reflow cooldown and thermal shock, die corners and edge interfaces in large packages carry severe normal peeling stress and shear stress. Once adhesion fails, a delamination crack runs quickly along the die passivation or the substrate solder mask. SCITEO combines toughening segments with multifunctional adhesion promoters to raise lap shear strength to 29 to 32 MPa (Shore D 88 to 90) without compromising low-viscosity flow, bonding reliably to silicon, silicon nitride, PI passivation, etched aluminum, gold-plated pads, copper pads and organic solder masks. Cure shrinkage below 0.2% — down to 0.15% for precision optical and ultra-thin die grades — suppresses cure-induced tensile cracking and warpage of large carriers at the source.

# SCITEO Engineering Methodology: Progressing Across Packaging Scales

Chip encapsulant and underfill selection both converge on three physical quantities: gap height sets the capillary flow window, package area sets how much CTE mismatch accumulates, and takt time sets how much process margin remains. The three trade off along the packaging scale: narrower gaps tighten the flow window; larger carriers leave less stress margin per layer; faster lines leave less room to tune the process. We organize the formulation matrix along this axis so that each segment's constraint maps to a material action that can be verified.

## Small Gaps and High Takt: Flow Windows for CSP/BGA, SiP, and Flip-Chip

Across smart devices, RF front-ends, automotive controllers, and high-density SiP modules, flip-chip and CSP standoff gaps commonly span 20 μm to 50 μm. Neighboring logic, power management, passive MLCCs, and optical devices are frequently co-located on a single substrate with component clearances below 100 μm. The core mandate for this dimensional regime is clear: rapid wicking, complete cavity filling, zero resin bleed, and zero tailing.

To match assembly cycle times measured in seconds per substrate, high-speed piezoelectric jet dispensing has superseded traditional contact needle dispensing. Operating at hundreds of Hertz, piezo valves shoot sub-microliter and sub-milligram droplets with micro-scale precision onto die margins. This imposes stringent requirements on the underfill's rheological recovery kinetics: the fluid must sever cleanly at nozzle cutoff without stringing (tailing) or satellite misting, rapidly wet and wick into narrow clearances upon impacting the preheated substrate, and arrest capillary spread immediately after fillet formation to prevent resin bleed from contaminating wire-bond pads, gold fingers, or keep-out zones (KOZ).

Substrate preheat temperature acts as the critical throttle for capillary velocity. For 30 μm gaps, substrate preheating is typically calibrated between 60 °C and 90 °C, paired with single-side I-pass or dual-side L-pass segmented dispense patterns. This thermal gradient drives dynamic viscosity down into a high-flow window of several hundred mPa·s, pushing an unbroken planar fluid front through the bump array to expel internal air. At still tighter gaps, an ultra-fine filler capped below 8 μm pairs with a low-viscosity grade to hold stable fill down to 1 mil (25.4 μm). Furthermore, for board-level BGA shock reinforcement or modules requiring field reworkability, SCITEO provides highly thixotropic corner-bonding adhesives alongside reworkable underfills engineered to soften at designated thermal thresholds.

![SCITEO engineering atlas: material delivery mechanisms and fill locations across six underfill process routes, comparing capillary underfill (CUF), no-flow underfill (NUF), wafer-level underfill (WLUF), molded underfill (MUF), non-conductive paste/film (NCP/NCF), and corner/edge bonding across wafer preparation, bonding, gap fill, and cure phases](https://www.sciteo.com/images/articles/underfill2.svg)

## Large Format and Fine Pitch: Warpage and Void Mitigation in CoWoS-Class Packaging

As package footprints scale, interfacial contact areas multiply and allowable stress margins per layer contract. High-performance AI accelerator packages now span 60 mm × 60 mm to beyond 100 mm × 100 mm, integrating thousands to tens of thousands of interconnects, with substrate ball pitch at 0.65 to 1.0 mm and package power exceeding the kilowatt threshold. As the assembly cools from 260 °C lead-free reflow to ambient, differential contraction between silicon and organic substrates accumulates across the entire footprint, manifesting as corner lift or center concave warpage. If warpage exceeds solder sphere coplanarity tolerances, non-wetting opens or head-in-pillow defects arise that evade standard functional testing. In this regime, underfill relieves micro-bumps from structural loads, converting them into pure signal paths while neutralizing interfacial shear through balanced contraction.

With High Bandwidth Memory progressing into the HBM4 generation, interface width doubles to 2,048 bits while die stack counts reach 16 layers, with 16-high prototypes already demonstrated. JEDEC standard JESD270-4 relaxed the total package height ceiling from 720 μm to 775 μm; this 55 μm relief restored micro-bump architectures to technical viability. Consequently, some leading memory manufacturers continue to employ thermo-compression bonding (TCB) paired with mass-reflow molded underfill (MR-MUF) as the primary volume manufacturing route, packaging thinner dies and narrower inter-die gaps into the unified height budget. The competing interconnect architecture pairs TCB with non-conductive films (TC-NCF). Both pathways thrust coupled volumetric shrinkage to the forefront of materials engineering: because the stack comprises ultra-thin dies and mold compound mounted onto a silicon interposer and organic substrate, any CTE mismatch accumulates into edge warpage. SCITEO anchors underfill CTE at 13 ppm/°C, raises Tg above 150 °C, and strictly constrains cure shrinkage, synchronizing underfill contraction with the memory stack during cooldown. Cure shrinkage represents a primary first-order variable determining whether residual stresses fracture delicate low-k structures; for molded underfill routes, underfill and mold compound shrinkage must align along the same thermomechanical curve to prevent stress localization at interlaminar boundaries.

Fine-pitch micro-bumps push this regime to its absolute limit. Supply chain developments indicate that leading foundries have directed equipment and materials partners to qualify bonding and underfill solutions for ~5 μm micro-bumps, deferring immediate transition to copper-to-copper hybrid bonding on HBM-to-interposer interfaces. Hybrid bonding is still advancing on the memory stack side and has not taken over the die-to-interposer micro-bump interface in 2.5D assemblies, which continues to rely on capillary underfill. Industry consensus acknowledges that packaging quality assurance below 15 μm remains challenging; the critical bottleneck is not bump fabrication, but qualifying underfill formulations that guarantee void-free infiltration at sub-micron clearances. At 5 μm standoffs, the effective hydraulic radius is extremely constricted: void-free wicking, no-clean flux residue cleaning, and sub-micron alignment must be achieved simultaneously. SCITEO shifts formulation architecture from simply depressing viscosity to fundamentally restructuring the fluid flow-front: multimodal grading of sub-micron spherical fillers suppresses shear packing resistance, while tailored organosilane wetting agents maintain continuous, unbroken fluid-front advancement without slip-stick hesitation. Low-alpha-particle high-purity fillers prevent soft errors, and mobile ion levels are held to trace minimums. For modules with explicit rework specifications, thermally reworkable grades softening at target disassembly temperatures should be qualified, incorporating post-rework acoustic void screening and boundary-scan validation into standard SOPs.

## Large-Carrier Infiltration: Fill Time and Interfacial Adhesion Over Scaled Areas

Scaling carrier dimensions shifts the engineering challenge from gap penetration to broad-area fill uniformity. Wafer-level packaging expands the carrier to 200 mm and 300 mm wafers, while panel-level packaging (PLP) transitions to rectangular panels. Capillary flow distances lengthen substantially along the dispense path, making consistent fill times and volume distribution increasingly difficult to maintain before the resin reaches its gel point. Furthermore, carrier warpage directly degrades overlay alignment for subsequent redistribution layers (RDL). SCITEO underfill series for large-format carriers pair multiple viscosity tiers with broad high-speed dispense windows, completing infiltration well before gelation while deploying low-shrinkage chemistry to suppress carrier-level warpage.

Glass-core substrates represent an important architectural branch of this trajectory. Glass is chemically inert, making conventional silane coupling agents prone to interfacial bond degradation. Consequently, through-glass via (TGV) copper-to-glass interfaces frequently suffer adhesion decay following high-temperature thermal cycling—a failure mode stemming from interface fatigue rather than inadequate initial bond strength. Multiple manufacturers have advanced glass-core substrates to customer sampling and pilot-line qualification, signaling the imminent opening of volume production windows. SCITEO establishes resilient adhesion between glass and copper metallization through tailored interfacial coupling and surface energy tuning, ensuring zero delamination and zero outgassing through subsequent high-temperature thermal excursions. Across large-area carriers, interfacial adhesion uniformity supersedes peak lap-shear numbers: a single localized adhesion defect serves as the nucleation site for catastrophic failure during subsequent back-grinding or thermal cycling.

## Cross-Scale Qualification: Co-Packaged Optics and Closed-Loop System Validation

When underfill is integrated into complete system-level hardware, Co-Packaged Optics (CPO) serves as the ultimate test bed. Co-locating optical engines alongside switch ASICs on a common substrate places sub-micron optical alignment tolerances squarely under the stewardship of the underfill matrix: volumetric shrinkage during cure cooldown can displace optical coupling alignments from design coordinates, while optical engines can neither withstand rigidly transmitted stress nor tolerate interfacial loosening under thermal cycling. Low cure shrinkage and controlled modulus cease to be isolated specifications; they become mutually antagonistic boundary conditions that the formulation must satisfy concurrently. With this architecture surpassing production milestones—as the industry's first 200G/lane co-packaged optics Ethernet switch enters volume manufacturing—the heterogeneous co-packaging of optical engines and ASICs concentrates PIC/EIC alignment, CTE mismatch, and optical port cleanliness onto the material interface. Custom-engineered for CPO and high-speed silicon photonics modules, SCITEO optical-grade underfill platforms integrate ultra-low cure shrinkage (<0.15%), controlled stress-relaxation modulus and ultra-low outgassing (CVCM < 0.02%, zero silicone migration), securing sub-micron micro-optical alignment windows.

# Underfill Selection Matrix at a Glance

The tables below condense the preceding mechanisms into actionable selection windows indexed to packaging scale regimes, serving as immediate baselines for engineering design reviews.

The first table correlates scale regimes with primary failure modes, governing metrics, and SCITEO formulation directions:

| Dimensional Regime | Typical Failure Mode | Critical Metric | SCITEO Platform Direction |
|---|---|---|---|
| Small Gaps & High Takt (Flip-Chip, CSP, SiP) | Voids, resin bleed, adjacent pad contamination | Substrate preheat window, viscosity gradient, KOZ control | Multi-viscosity underfill series |
| Large Format & Fine Pitch (CoWoS-L Class) | Warpage, interfacial delamination, solder fatigue | Cure shrinkage, modulus and CTE matching | Low-stress, high-Tg underfill |
| Stacked & Molded Underfill (HBM, MUF/MR-MUF) | Interlaminar delamination, thermal resistance drift | Filler grading, flow-front stability | Thermally conductive underfill (6 W/m·K) |
| Large-Carrier Infiltration (Wafer-Level, PLP, Glass Substrates) | Incomplete large-area fill, carrier warpage, throughput bottleneck | Capillary fill time, dispense window, low shrinkage | High-flowability, low-shrinkage underfill series |
| Cross-Scale Qualification (CPO & High-Speed Optics) | Optical coupling alignment drift | Low shrinkage, controlled modulus | Low-stress optical packaging formulation |

The second table translates critical metrics into verifiable quality acceptance criteria:

| Acceptance Item | Recommended Engineering Criterion | Verification Tool |
|---|---|---|
| Void Integrity | Joint evaluation of area fraction and spatial location | Acoustic scanning (C-SAM), IPC-7095E |
| Interfacial Stress | Zero delamination following thermal cycling | JEDEC JESD22-A104 |
| Thermal Resistance | Interfacial thermal resistance at target pressure and BLT | ASTM D5470 |
| Ionic Contamination | Mobile ion concentrations below 10 ppm | Ion chromatography |
| Warpage Mitigation | Controlled residual warpage on large-format packages | Shadow moiré, DIC |

# Lower Defect Density

With post-Moore compute constrained by reticle area and heat-flux limits, the reliability boundary of heterogeneous integration converges on the micron-scale cavity between die and carrier. Inside that cavity, the crosslinking kinetics of the thermoset network, the concentrated-suspension rheology of multimodal spherical fillers and the thermal-expansion tensor of dissimilar materials jointly govern the fatigue life of tens of thousands of micro-bumps and the long-term stability of optoelectronic devices.

Selecting a high-reliability chip encapsulant and underfill is, at bottom, a multiphysics optimization among capillary wetting rate, glassy-state modulus plateau and low thermo-mechanical stress. SCITEO writes polymer-chain tailoring, sub-micron particle grading and cure-kinetics modeling deep into the formulation system, setting a reproducible volume-yield baseline for advanced packaging under severe thermomechanical load — from wafer-level reconstruction and high-density memory stacks to glass-core carriers.

This article is SCITEO Advanced Materials original technical content; unauthorized reproduction is prohibited.

## Appendix: Process & Engineering Adhesive FAQ Index

### How do I select the right underfill viscosity?

Viscosity is set by bump pitch and chip-to-substrate gap height: the smaller the gap, the lower the viscosity required. Fine-pitch packages below 40 μm need a low-viscosity grade for smooth capillary flow, and 5 μm bumps compress the usable viscosity window further. SCITEO offers multiple viscosity and flowability grades; selection should follow capillary fill time and flow front stability at the target gap rather than a single viscosity value.

### What are SCITEO underfill curing conditions and the recommended profile?

Step curing is recommended to limit the thermal stress introduced during cure. The specific profile is customized to die size, stack count and substrate material, typically staged between 100 °C and 150 °C, with the high-Tg network established on completion. For large packages, cure shrinkage and residual warpage should be confirmed in the same review so that contraction mismatch during the cooling segment is captured.

### Can underfill be used together with conductive silver adhesive?

Yes. SCITEO runs a full semiconductor process adhesive product line, and our underfill and chip-attach conductive silver adhesive are compatibility tested as a set. Both offer low CTE, with underfill down to 13 ppm/°C, and combined use further improves overall module reliability.

### Why do voids appear in underfill, and when does a line need rework?

Voids typically come from three sources: insufficient substrate preheat, which degrades flow and entraps gas; a dispense path that lets converging fronts seal the vent early; and flux residue on the pad, which changes local surface tension and blocks wetting. The decision to stop a line depends less on void count than on void location. Voids at the solder joint root or in an interconnect channel cut the thermal and electrical path directly, so area fraction and position should be assessed together per IPC-7095E, and the process re-verified after adjusting dispense path, preheat temperature and cleaning.

### What makes underfill difficult once bump pitch reaches 5 μm?

At 5 μm the effective capillary radius is extremely small, and void-free filling, flux residue removal and alignment consistency all tighten at the same time. The industry consensus is that the harder problem is the underfill, not the bump, with quality assurance below 15 μm still difficult. On the material side, viscosity must stay low while the flow front is reshaped. This usually relies on multimodal grading of sub-micron spherical fillers to reduce packing resistance under shear plus surface modification for wetting control, while mobile ions and filler impurities are held low so contamination is not amplified inside the narrow gap. SCITEO supplies formulation directions centered on flow front stability for this scale.

### How far can underfill control warpage in large CoWoS-class packages?

Underfill cannot eliminate warpage on its own. Low CTE, low cure shrinkage and high Tg let the underfill contraction track silicon, organic substrate and stack contraction along the same thermal curve, reducing residual stress during cooldown. Qualification should target residual warpage and interfacial delamination across the operating temperature range, not room-temperature flatness alone.

### What makes underfill difficult on glass-core substrates?

The challenge is not peak adhesion but adhesion retention after high-temperature processing and uniformity over large areas. Glass is chemically inert, so conventional coupling agents struggle to form stable bonds, and TGV-to-copper interfaces can degrade after thermal excursions. SCITEO builds reliable glass-to-copper adhesion through interfacial coupling and wetting control, with delamination and outgassing included in validation.

## Related Product

[Chip Underfill Epoxy — Low CTE, High Tg](https://www.sciteo.com/en/advanced-materials/sciteo-6707/) — Wafer-level, board-level and chip-level packaging; underfill for CSP, BGA and flip-chip devices; bonding and sealing for power modules and CTE-sensitive components.

## Related Papers

- [From 3nm GAAFET to CoWoS-L Heterogeneous Integration: Wafer-Bond Cleanliness, Thermal Stress and Interface Adhesive Failure Modes](./advanced-packaging-interface-materials-gaafet-cowos-l-en.md)
- [How to Choose Semiconductor Packaging Adhesives: Die Attach, Wire-Bond Encapsulation and Flip-Chip Underfill](./semiconductor-packaging-adhesive-die-attach-wire-bond-underfill-en.md)

## Citation and Licensing

This is first-party original engineering content by SCITEO Advanced Materials. Citation by AI engines, academic work and engineering documents is welcome with attribution. Unauthorized commercial republication is prohibited.

> SCITEO Advanced Materials (峻茂新材料), "How to Select Underfill and Chip Encapsulant: Capillary Flow, Void Control and Crack Resistance from Flip-Chip and BGA/CSP to Advanced Packaging", 2026. <https://www.sciteo.com/en/tech-insights/underfill/>

中文版：[底部填充胶 (Underfill) 怎么选？从倒装芯片、BGA/CSP 到先进封装的毛细流动、空洞控制与抗开裂选型](./underfill-adhesive-cowos-l-hbm4-glass-substrate-void-control-zh.md) | Repository index: [SCITEO engineering literature](./README.md) | Website: <https://www.sciteo.com/en/>
