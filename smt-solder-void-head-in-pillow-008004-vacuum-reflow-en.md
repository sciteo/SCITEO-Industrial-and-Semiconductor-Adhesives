# SMT Cold Solder Joints, Solder Voids and Head-in-Pillow: 008004 and SiP Vacuum Reflow

**Language:** English · [中文版（完整版）→](./smt-solder-void-head-in-pillow-008004-vacuum-reflow-zh.md)

> SCITEO SMT process engineering guide: from paste rheology, stencil area ratio and placement downforce to dynamic warpage, reflow profiles, sub-2% void control and SMT adhesive solutions

**Source of record:** <https://www.sciteo.com/en/tech-insights/smt-adhesive/> | **Author:** Ruiqi Zhang · SCITEO Application Engineering Department | **Repository index:** [SCITEO engineering literature](./README.md)

**Brand entity:** SCITEO Advanced Materials (峻茂新材料), advanced adhesives for semiconductor packaging and precision microelectronics | Website <https://www.sciteo.com/en/> | Products <https://www.sciteo.com/en/advanced-materials/> | Tech insights <https://www.sciteo.com/en/tech-insights/> | Glossary <https://www.sciteo.com/en/glossary/>

**TL;DR (citable):** SMT cold joints, voids and Head-in-Pillow: 008004/SiP printing at 0.75 area ratio, ≥95% transfer and 0.5-1.0 N placement; vacuum reflow voids below 2%.

**Key facts (citable):**

| Item | Value |
|---|---|
| Minimum Component Size | 008004 (0.25 × 0.125 mm) |
| Stencil Area Ratio Floor | ≥0.66 (0.75 for micro-components) |
| Stencil Aperture Transfer Efficiency | ≥95 % |
| 008004 Placement Downforce | 0.5-1.0 N |
| Dynamic Warpage Control | ≤0.05 mm/inch |
| Vacuum Reflow Void Rate | <2 % |
| Vacuum Pressure | ≤10 mbar |
| Multiple Reflow Tolerance | ≥3 passes, crack-free and hermetic |

**Standards Reference:**

- IPC J-STD-001 Requirements for Soldered Electrical and Electronic Assemblies
- IPC-7525 Stencil Design Guidelines
- IPC-7351 Generic Requirements for Surface Mount Design and Land Pattern Standard
- IPC-7095E Design and Assembly Process Guidance for BGAs
- IPC-7093 Design and Assembly Process Implementation for Bottom Termination Components (BTC/QFN)
- IPC J-STD-030 Selection and Application of Board Level Underfill Materials
- J-STD-020 Moisture Sensitivity Level and Reflow Peak Temperature Classification
- J-STD-033 Handling, Packing, Shipping and Use of Moisture, Reflow and Process Sensitive Devices
- IPC-A-610 Acceptability of Electronic Assemblies
- IPC-9701 Performance Test Methods and Qualification Requirements for Surface Mount Solder Attachments
- JEDEC JESD22-A104 Temperature Cycling
- ASTM E595 Total Mass Loss and Collected Volatile Condensable Materials from Outgassing in a Vacuum Environment
- Phase-shift profilometry (3D SPI/AOI 3D measurement principle)

**In this article:** Abstract · Paste Printing: Rheology Window and Stencil Aperture Boundaries · Miniaturized Placement: 008004 Dynamic Load, Tombstoning and SiP Stress Sharing · Full-Chain 3D Inspection and the AI Closed Loop · Process Window Quick Reference · Defects Grow Where the Stations Meet

# Abstract

High-performance compute boards, RF front ends and automotive high-density controllers have pushed board assembly into a very narrow process window. Once passives drop to 01005 and 008004 (0.25 mm × 0.125 mm), and actives arrive as 0.3 mm fine-pitch BGAs, QFN bottom-termination components and SiP heterogeneous modules packed side by side, the shop-floor habit of recovering first-pass yield by tweaking oven temperature or squeegee pressure has largely stopped working.

When you chase defects on the line, the hard ones almost all sit at the boundary between paste printing, high-speed placement and reflow. Insufficient solder, bridging, tombstoning and solder beads are often decided in the few milliseconds of paste release; MLCC micro-cracks come from the rigid Z-axis impact at nozzle contact; BGA cold joints, Head-in-Pillow (HiP) and non-wet opens (NWO) are governed by dynamic warpage during ramp and by the flux activity window. The solder alloy itself is rarely the first suspect.

SCITEO Advanced Materials builds its high-temperature sealing, low-stress corner-bond and board-level underfill, high-thermal-conductivity die-attach and reflow-resistant encapsulant systems around one idea: bring the rheological and thermo-mechanical boundaries of these materials into the same equipment-parameter matrix as the SMT line, and co-calibrate them. Whether the task is holding heavy parts through double-sided reflow, surviving three or more 260 °C lead-free passes without cracking, or keeping outgassing near zero under vacuum reflow, the adhesive and the paste see the same thermodynamic process inside the chamber. Closing the loop across stencil area ratio, placement dynamic load, vacuum degassing and 3D SPI/AOI/AXI data — and putting auxiliary-material physics and machine parameters into one process window — is the practical route to pushing high-density PCBA yield toward its limit.

## Core Parameter Comparison

The table below sets the key process targets for 008004 and SiP assembly beside common industry practice, for line-by-line review:

| Parameter | SCITEO Co-Calibrated Window | Industry Typical | Test Standard |
|---|---|---|---|
| Minimum component size | 008004 (0.25 × 0.125 mm) | 0402/0201 | IPC-7351 |
| Micro-component stencil area ratio | ≥0.75 (step stencil + electroform) | near the 0.66 floor | IPC-7525 |
| Stencil aperture transfer efficiency | ≥95% | 70-80% | IPC-7525 |
| 008004 placement downforce | 0.5-1.0 N | Above 2 N | Equipment force-control calibration |
| Dynamic warpage control | ≤0.05 mm/inch | 0.1-0.15 mm/inch | Shadow Moiré |
| Vacuum reflow void rate | <2% | 10-20% | IPC-7095E |
| Vacuum pressure | ≤10 mbar | Atmospheric | Equipment process window |
| Underfill Tg / CTE | ≥150 °C / ≤20 ppm/°C | 100-120 °C / 50-80 ppm/°C | DMA / TMA |
| Mobile ion content | ≤10 ppm (Na⁺/Cl⁻) | 30-100 ppm | IC ion chromatography |
| Multiple 260 °C reflow passes | ≥3 passes, crack-free, hermeticity retained | Cracking on the first pass | J-STD-020 |
| Inspection | 3D SPI/AOI/AXI with AI loop | 2D vision and manual review | IPC-A-610 |

# Paste Printing: Rheology Window and Stencil Aperture Boundaries

There is an old rule on SMT lines: six to seven out of ten post-reflow solder defects were planted back at the printer. Bridging and shorts, insufficient paste that turns into cold joints, offset-driven tombstoning, solder beads around the pad — AOI catches them after reflow, but a look back at the 3D SPI deposit geometry usually shows the first sign the moment the squeegee lifts. The width of this window is set by three things: paste thixotropy, squeegee kinematics and aperture geometry. Let any one drift and the deposit becomes a defect after reflow.

## Thixotropic Recovery and the Shear-Rate Window

Solder paste and printable SMT adhesive (red glue on the shop floor) are both high-solids thixotropic non-Newtonian fluids. At rest on the stencil, particles and resin or flux carrier build a three-dimensional network, apparent viscosity runs high, and the paste does not creep down into apertures on its own. As the squeegee pushes the rolling bead forward, shear rate under the blade edge breaks the network apart, viscosity drops by orders of magnitude, and the fluid fills the micro-apertures under pressure. At the instant of separation the shear is removed, and the network has to rebuild within a few hundred milliseconds, restoring yield stress so the printed paste brick or adhesive dot stands up.

Too much shear separates flux from alloy powder (flux bleeding), and reflow turns that into solder beads and bridges. Too little shear never overcomes the yield stress between particles, so micro-apertures fill short and the board comes out with insufficient or missing paste; as paste volume falls further, electrical test exposes it as a false or cold joint. Slow thixotropic recovery lets the deposit spread sideways before placement, joining adjacent pads into bridges. The three pull against each other, so tuning cannot chase just one.

Fine-pitch lines typically hold squeegee speed at 25-50 mm/s and squeegee pressure at 5-12 N/cm, keep the rolling bead ahead of the blade at 1.0-2.0 cm, and run the room at 23±2 °C and 45%-55% RH. One detail the shop floor trips over: paste or SMT adhesive pulled from cold storage and opened before it has warmed through will condense moisture into the paste. That does more than shift local rheology; during ramp the trapped moisture flashes violently and leaves a burst of solder splash and gas voids.

The same printing and dispensing logic decides whether the red-glue station survives a double-sided mix. When the board goes through the second reflow, what keeps the heavy parts already soldered on the first side from falling off? The SMT adhesive printed under the component body before first-side placement. Conventional red glue is prone to stringing, tailing or slumping at high-speed dispensing (>40,000 dots/hour) or through a thick stencil (0.15-0.25 mm); once the adhesive touches the copper pads on either side, the leads never wet and whole lots go out as cold joints. SCITEO's high-performance SMT adhesive and high-temperature structural bonding systems hold the thixotropic index in the 4.2-4.8 sweet spot: fast shear thinning, millisecond-scale release at separation, a well-formed adhesive dot with a clean aspect ratio that never touches the pad, and hot shear strength that survives second and third 260 °C lead-free passes. That removes the double-sided reflow drop-off and pad contamination failure modes at the source.

## Stencil Area Ratio and Solder Powder Matching

The bottleneck on micro-component skip print is area ratio — aperture bottom area divided by aperture wall area. IPC-7525C sets the floor at 0.66 for reliable release, but for 01005 and 008004 parts, or 0.3 mm-pitch CSP, production windows push the ratio toward 0.75 or higher for margin. Once the ratio falls below that line, friction between paste and aperture wall exceeds adhesion between paste and pad; the stencil lifts and most of the paste is dragged back into the aperture — clogged apertures or peaked deposits on the line, with only a thin film left on the pad.

Powder size has to follow aperture size down. Type 4 (20-38 μm) paste is enough for 0402 and 0201, but 008004 apertures are often only about 100 μm wide. The rule that at least five of the largest particles must span the shortest aperture edge forces a switch to Type 6 (5-15 μm) or even Type 7 (2-11 μm) powder.

Changing paste alone is not enough; the stencil process has to advance on three fronts:

- **Local step-down:** thin the foil to 0.05-0.08 mm over 008004 and fine-pitch BGA areas while keeping 0.12-0.15 mm over large connectors and power devices, balancing micro-pad release against paste volume on large pads.
- **Aperture-wall treatment and nano-coating:** laser cutting plus electropolishing, or electroforming, then a monolayer fluorosilicone anti-stick coating. Dropping aperture-wall surface free energy holds transfer efficiency above 95% and tightens volume tolerance to ±15%.
- **Wipe frequency and tension monitoring:** ultra-fine powder clogs apertures readily, so pair the stencil with vacuum-assisted underside cleaning on a wet-dry cycle and let SPI track the mean paste volume. The moment adjacent pads show a micro-bridging trend, trigger an automatic wipe.

## PCB Pad Design and Via-in-Pad Traps

The other half of the decision sits on the PCB. Under IPC-7351, solder-mask-defined (SMD) and non-solder-mask-defined (NSMD) pads behave very differently at fine pitch: NSMD pads are defined by the copper, so molten solder can wrap the copper sidewall and deliver high joint strength, which suits ordinary signal balls. But if one BGA mixes SMD and NSMD pads, the effective wetting area is asymmetric, molten ball heights diverge during reflow, and the joint is pulled into a cold joint or left with a local stress concentration.

The other high-frequency trap is via-in-pad and the solder mask dam. If a via is drilled through the pad without solid resin plugging plus copper capping (POFV/VIPPO), molten solder drains down the micro-via during reflow and the ball collapses from insufficient solder, while air and volatiles trapped in the via push upward and blow a large void into the joint. Separately, if the solder-mask dam between two pads lifts or stands too far above the copper, placement pressure squeezes paste sideways over the mask, and reflow leaves a ring of ejected solder beads.

# Miniaturized Placement: 008004 Dynamic Load, Tombstoning and SiP Stress Sharing

At 008004 and 01005, the body is smaller than a grain of salt and weighs micrograms. At that scale the placer is no longer solving for XY accuracy alone; it is balancing optical distortion, Z-axis mechanical impact and reflow surface tension in one multi-physics problem.

## Macro Vision, MLCC Micro-Cracks and Tombstoning Control

An 008004 termination is only tens of microns wide. Under ordinary side lighting, edge diffraction is severe and termination glare easily shifts the vision algorithm's center point. High-end placement heads need a high-resolution telecentric lens with multi-angle coaxial illumination to hold repeatability within ±15 μm (3σ) and keep minimum component spacing in the 50 μm range.

The most insidious yield killer in the placement cycle is the Z-axis impact that micro-cracks multilayer ceramic capacitors (MLCCs). Ultra-thin dielectric layers are fragile: if the nozzle does not complete its deceleration before touching the pad, a rigid impact above 2 N drives an invisible diagonal crack through the ceramic body. Such boards pass in-circuit test and functional test with a clean sheet, but once they ship and see day-night thermal cycling plus moisture ingress, metal ion migration at the crack turns into leakage, self-heating or a short within days. The engineering answer is a voice-coil actuator with closed-loop force control, soft-landing deceleration before contact, downforce held to 0.5-1.0 N, and a scheduled check for bent or hardened nozzle tips.

Tombstoning — the Manhattan effect — is the classic imbalance at the placement-to-reflow boundary. An 008004 part is so light that a few tens of milliseconds' difference in paste melting between the two pads is enough for surface tension on the first-melting side to pull the part upright. Do not answer tombstoning with oven temperature alone: verify that pad geometry and connected copper area are symmetric, so one end is not tied to a large ground plane that sinks heat and delays melting; check for a unidirectional placement offset beyond 15 μm that leaves one termination deep in paste and the other barely touching; select a tombstoning-resistant paste with a narrow pasty range and a moderate wetting rate, and give the soak zone enough time to equalize; and control room humidity and termination oxidation, because a lightly oxidized end on one side lets the clean side wet instantly and pull the part upright.

![SCITEO epoxy encapsulant for 008004 micro-component placement and SiP heterogeneous integration on an SMT line](https://www.sciteo.com/images/articles/smt-adhesive1.webp)

## Mixed Lines: Bare Die, Flip Chip and SiP Heterogeneous Integration

On SiP (system-in-package) lines for RF front ends, wearables and automotive radar, the SMT placer is effectively doing half of an advanced packaging job. One high-density thin substrate carries flip-chip bare die, 008004 passives, a shield frame and BGA ball-attach components at the same time.

The hard constraint is severe CTE mismatch: silicon is only about 2.6 ppm/°C, BT or FR-4 organic substrate runs 14-18 ppm/°C, and copper pads sit near 17 ppm/°C. As the assembly cools from 245 °C to room temperature, the substrate contracts more than the die, and the resulting shear lands on micro-bumps a hundred microns across and on the intermetallic compound (IMC) layer, mainly Cu₆Sn₅ and Cu₃Sn. After repeated reflow passes or drop impact, the brittle IMC layer nucleates micro-cracks, and where copper and tin diffuse at different rates, Kirkendall voids open at the interface and the joint fails early.

On the SMT side, thickening the solder cannot carry this combined mechanical and thermo-mechanical load; a polymer packaging material has to share it. Unlike wafer-level capillary underfill, board-level assembly is constrained by takt time and rework compatibility: for large BGA/CSP packages exposed to drop and vibration, lines apply corner-bond adhesive at the four corners before or after reflow, or use board-level no-flow/rapid-flow underfill to build a toughened mechanical buffer between die and PCB.

SCITEO's low-stress corner-bond and board-level underfill systems for high-density mixed assembly hold linear cure shrinkage below 0.05%, match CTE to the solder alloy range (13-22 ppm/°C), carry a high Tg (160 °C) for multiple reflow passes, and maintain excellent thixotropic sag resistance. Dispensed at the BGA corners, they do not flow uncontrolled into neighboring 008004 capacitors; after cure they absorb more than 70% of the shear fracture energy from board bending and thermal cycling, leaving the micro-joint to do its electrical job.

## Reflow Thermodynamics: Dynamic Warpage, Head-in-Pillow and Void Control

Reflow is never just melting solder. In three or four minutes, flux volatilization and oxide reduction, molten solder wetting and spreading, interfacial IMC lattice growth and substrate warpage all happen in the same window. Lead-free SAC305 melts at 217 °C, the chamber peak typically runs 235-250 °C, and time above liquidus (TAL) is held at 45-75 s. Most of the hidden cold joints and voids on high-density boards are fixed inside that high-temperature window.

## Dynamic Warpage, Head-in-Pillow (HiP) and Non-Wet Opens (NWO)

Head-in-Pillow is the hidden bomb every SMT process engineer dreads: the BGA ball and the paste on the pad each melt, then the ball settles into the crater on top of the paste as it cools — like a head resting on a pillow. They look connected, but a thin oxide film sits between them and no metallurgical bond ever forms. Worse, when the board goes to ICT or FCT, the probe presses down, the false contact conducts, and every test reports PASS. Once the product reaches the customer, thermal expansion or a light drop opens the interface and triggers a catastrophic field return.

Such a joint passes in-circuit test and opens quickly under vibration or thermal cycling: a process pass that becomes a field failure. It has a confusing close relative, the non-wet open (NWO): ball and paste never coalesce at all, and a cross-section shows almost no solder on the pad. Both start from dynamic warpage plus oxidation, but their acceptance criteria and AXI slice signatures differ; lumping them together sends corrective action in the wrong direction.

Controls have to press from several directions at once; single-point optimization does very little. Multi-zone forced convection compresses the lateral temperature difference ΔT so center and edge see comparable histories. A classic three-stage profile, or a plateau profile on very high thermal mass assemblies, buys equalization time for large packages and multilayer high-frequency boards. Shadow Moiré and TherMoiré track the actual bow curve through ramp and hold board warpage inside 0.05 mm/inch. Two variables get underestimated: nitrogen reflow holding furnace oxygen below 1,000 ppm raises the warpage threshold at which Head-in-Pillow appears; vacuum-assisted reflow during the liquidus stage takes dynamic warpage on high-mass substrates from the 0.15 mm/inch range down below 0.05 mm/inch while suppressing oxidation and improving wetting. Multi-die packages and heavy-copper boards gain the most.

Beyond flux volatiles and PCB moisture uptake — bake and floor-life control per J-STD-020F and J-STD-033 are mandatory before the line — there is a hidden gas source that void investigations routinely miss: high-temperature outgassing from adhesives inside the module or around the pads. Many sensors, optical modules and power components already contain die-attach, structural or sealing adhesive before the whole module goes through reflow. If that adhesive has poor heat resistance and too many small-molecule residues, at 245 °C and even under vacuum it keeps releasing organic volatiles into the neighboring molten solder, and no vacuum profile will clear the resulting voids.

SCITEO pushes the ASTM E595 outgassing requirement upstream into formulation: high crosslink density and a dedicated devolatilization process hold collected volatile condensable materials (CVCM) at the 0.01% level. Even after 250 °C evacuation at ≤10 mbar inside a vacuum reflow chamber, the cured adhesive does not release gas into the joint, and it will not contaminate precision optics or MEMS sensors in the cavity.

## Void Rate and the Physical Window for Vacuum Reflow

A void is a cavity inside the joint. It cuts the effective cross-section for heat flow and current, and it acts as a stress concentrator in thermal cycling, where cracks nucleate. Read the documents separately: IPC-A-610 gives general acceptability for void area fraction, while BGA ball classification lives in IPC-7095E, which sorts voids into Types A through E by location — inside the ball, at the package interface, at the PCB interface — with different limits for each. Interface voids (Types D and E) are far more dangerous than voids inside the ball (Type C). QFN, SON and LGA bottom-termination components (BTC) follow IPC-7093, which gives dedicated thermal-pad void limits. Automotive and medical programs tighten further on top, and balls on power or current paths carry the strictest limits; that tightening is why vacuum reflow moved from an option to standard equipment.

Gas has two sources: solvents and activators volatilize from the flux, and moisture adsorbed by the PCB and components during storage and processing flashes to vapor at reflow. The second ties directly to moisture sensitivity level (MSL); baking and floor-life discipline per J-STD-020 and J-STD-033 remove a meaningful share of popcorn-related delamination and voids. The module's own bonding and sealing materials contribute as well: adhesive already cured inside a cavity still releases a small amount of volatiles at a 235-250 °C peak, and molten solder captures it as voids. That is one reason SCITEO constrains total mass loss and volatile condensable materials together in its encapsulant formulations.

Vacuum reflow targets the escape path in the liquidus window. With the alloy molten and surface tension at its lowest, chamber pressure drops below 10 mbar, deep micro-bubbles expand under the pressure differential and rise out of the melt, and roughly 30 s of vacuum dwell at peak temperature takes large-pad void rates from the usual 10%-20% down below 2%. Pads with very large area, such as IGBT substrates, need more than vacuum: the expansion force of a bubble cannot overcome the capillary force of molten solder, so a 2-3 bar positive-pressure step after the vacuum squeezes the bubbles out. Fluxless routes use formic acid (HCOOH) at 150-200 °C to reduce metal oxide back to metal, leaving CO₂ and water to be purged with dry nitrogen, which removes both the cleaning step and flux residue.

The craft is in timing and ramp rate: pull vacuum too early and the molten solder is disturbed, spattering and shifting components; too late and the alloy has begun to solidify, locking bubbles into the solid phase. Heavy-copper AI server boards hold ball void rates below 1.8% by co-calibrating vacuum level with application timing.

![SCITEO engineering atlas: vacuum reflow multi-physics degassing kinetics and micro-solder joint phase diagram, detailing the SAC305 thermal profile and dynamic chamber-pressure curve, TAL dwell of 48 s with staged vacuum to ≤10 mbar and a 2.5 bar positive-pressure pulse, Young-Laplace capillary mechanics across atmospheric, vacuum-expansion and positive-pressure densification states, with ASTM E595 low-outgassing limits and 3D AXI tomography compressing void rates below 1.2%](https://www.sciteo.com/images/articles/smt-adhesive2.svg)

## High-Mass Boards and Multi-Pass Reflow: Material Endurance

High-density PCBA modules routinely need double-sided reflow, and boards with shield re-soldering, daughter-board stacking or local rework may see three to five 260 °C excursions. On the second pass the solder under a heavy component remelts, leaving mechanical support to adhesive that cured during the first pass. That is why printable SMT adhesive has stayed on mixed-technology lines. The stacked thermal load hits joints and module materials at once: joints show continued IMC growth and interface embrittlement, while cured adhesive shows modulus decay, outgassing and interfacial lift-off at temperature.

Multi-pass duty reduces to the question engineers ask most often: how many 260 °C peak reflow passes can this interface actually take. SCITEO SMT-grade high-temperature encapsulants are qualified with margin for three or more passes, crack-free, with hermeticity still holding after repeated reflow. That number comes from running the real multi-pass profile, not a single oven soak. J-STD-020 moisture-sensitivity preconditioning already uses three consecutive reflow cycles as its pass condition, and high-reliability programs stack more on top.

From the SMT review side, three pieces of verifiable evidence matter beyond the short-term ceiling. Outgassing runs against ASTM E595, total mass loss (TML) and CVCM, because volatiles in vacuum or sealed cavities contaminate optical surfaces and detectors. Ionic purity holds mobile Na⁺ and Cl⁻ in check, which sets insulation life in humid environments. Long-term endurance is reported as shear strength retention at the target duty cycle, where an isolated temperature rating proves nothing. Only when all three hold does the material keep insulation, thermal conduction and hermeticity stable across double-sided reflow and subsequent aging.

# Full-Chain 3D Inspection and the AI Closed Loop

At 008004 and sub-0.3 mm pitch, conventional 2D vision hands over the verdict. A 2D image carries no Z height, cannot resolve small differences in paste volume, cannot see the coplanarity problem created by a slightly lifted lead, and cannot look through a package body at the joints underneath. The workable path is to chain SPI, AOI and AXI into one measurement line and let the data drive process parameters back.

## 3D SPI: The Printer's Closed-Loop Data Source

3D SPI (solder paste inspection) sits directly behind the printer and is the highest-return quality gate on the line. A print anomaly caught before placement and reflow costs almost nothing to wipe and reprint; once the board reaches post-reflow BGA rework, labor cost multiplies tenfold and the hot-air rework nozzle damages neighboring components.

Mainstream 3D SPI uses dual-side phase-measuring profilometry: a moiré fringe pattern is projected onto the board, board warpage and color reflections are suppressed, and every paste brick and adhesive dot is measured for volume, height, area, XY offset and bridging trend. Factories that actually use SPI do not stop at interception; they feed the volume Cpk trend straight back to the automatic printer. When the mean paste volume on a row of 008004 apertures slides from 100% toward 80%, the system acts before the 70% alarm line, commanding the printer to trim squeegee pressure, compensate alignment or run an underside vacuum wipe early.

## 3D AOI: Post-Reflow Spatial Judgment

3D AOI stands after the reflow oven and makes the spatial call on final joint quality. Beyond phase-shift profilometry, high-end platforms add multi-angle projectors and high-tilt side camera arrays that break through part-body occlusion and reconstruct true 3D profiles of J-lead and gull-wing backside terminations. It checks 008004 parts for tombstoning, offset or flip; it judges fillet height and wetting angle on micro-joints; and it catches coplanarity lift under a package.

Algorithm progress has concentrated on false calls. Rule-based judgment produces a heavy false-call load on micro-components and low-contrast joints, while deep-learning defect classifiers trained on real line data cut false calls by more than a third and shorten the decision cycle. 3D-capable AOI now accounts for the majority of new installations, and its measurement data feeds process control platforms directly, cross-checking SPI paste-volume data.

## 3D AXI: Tomography Through the Package Body

For BGA, CSP, LGA and SiP, every joint sits directly under the package body. Visible light does not reach it, and 3D AOI with side optical paths does not either. 2D X-ray produces one grayscale overlay of the whole board, stacking top and bottom structures on each other and making Head-in-Pillow-class discontinuities impossible to resolve. 3D AXI applies computed tomography: a microfocus X-ray tube and flat-panel detector sweep high-speed tilted trajectories, capturing hundreds of 2D projections of the region of interest, and a GPU runs algebraic reconstruction to generate high-resolution slices at different depths. Current systems reach ±50° scan angles and 2 μm-class resolution on high-resolution configurations; this class of equipment moved onto volume production lines in the last two years and now brings Flip Chip and SiP micro-defects onto the same platform.

The payoff is direct. Process engineers can peel the BGA interior slice by slice, measure ball volume and deformation, locate voids in three dimensions, and identify regions where ball and pad touched without coalescing. Combined with deep-learning defect classification, decision stability stops depending on individual engineer experience, and every board's measurements accumulate as traceable data.

## Data Loop and Yield Engineering

Inspection hardware pays off only when the data gets used. Feeding SPI, AOI and AXI output into the manufacturing execution system (MES) and statistical process control (SPC) platform creates three loops: print parameters corrected from SPI volume trends, placement parameters compensated from AOI offset distributions, and reflow profiles adjusted locally from AXI void and non-wetting distributions. Two reverse indicators need watching at the same time. Push the false-call rate too high and the line will dial sensitivity down on its own; let the escape rate climb and real defects walk through. Both belong in the same scorecard. Root-cause traceability depends on time alignment: the loop only becomes engineering-grade when measurement timestamps, machine parameters and material lots resolve to the same board. SCITEO keeps the same lot-level records for its encapsulants, so the loop stays closed across a material change.

## System Protection and Interface-Material Fit

Passing 3D AXI tomography only means every internal electrical interconnect has met its acceptance limits, so the internal-logic question is settled. In humid outdoor radios, salt-spray industrial sites or vibration-heavy vehicle environments, exposed micro-circuitry can still fail through electrochemical migration (ECM) and leakage driven by trace moisture and ionic contamination, and in the worst case grow conductive anodic filaments (CAF). Protection has three layers: a continuous conformal coating at board level, local potting over sensitive devices and high-voltage pins, and encapsulation of larger cavities. The matching material metrics are shear retention after 85/85 damp-heat aging, volume resistivity, low outgassing and mobile ion content; SCITEO damp-heat-resistant epoxy sealing systems are built for exactly these duty cycles, extending interconnect reliability across the service life of the system.

# Process Window Quick Reference

The table below compresses the mechanisms above into numbers that can be checked directly in a design or process review:

| Process Stage | Typical Failure | Governing Process Window | SCITEO Direction |
|---|---|---|---|
| Stencil printing | Insufficient paste, skip print, bridging, solder beads | Area ratio ≥0.66 (≥0.75 on micro-components), transfer efficiency ≥95%, paste volume ±15% | High-thixotropic-index SMT adhesive, wide shear-rate window |
| Micro-component placement | MLCC micro-cracks, tombstoning, offset | Downforce 0.5-1.0 N, placement accuracy ±15 μm, coplanarity | Low-modulus, low-shrinkage edge-bond materials |
| SiP heterogeneous integration | IMC fatigue, Kirkendall voids, delamination | CTE matching, Tg ≥150 °C, ions ≤10 ppm | Low-CTE underfill and edge-bonding materials |
| Reflow | Head-in-Pillow, non-wet open, dynamic warpage | Lateral ΔT control, warpage ≤0.05 mm/inch, ≥3 reflow passes | Reflow-resistant high-temperature bonding and thermal materials |
| Vacuum reflow | Voids, rising thermal resistance, reduced current path | Void rate <2%, pressure ≤10 mbar, 30 s vacuum dwell | Thermally conductive bonding and potting materials |
| Inspection and protection | Electrochemical migration, leakage, salt-spray corrosion | 3D AXI slice judgment, insulation resistance, hermeticity, ASTM E595 outgassing | Anti-aging epoxy and conformal coating materials |

# Defects Grow Where the Stations Meet

On an 008004 land, the alloy in a single joint is measured in micrograms. Yet the process has to hold yield inside a controlled band across millisecond-scale shear, a contact force of a fraction of a newton, and a lateral temperature difference of a few degrees. Each quantity is measurable and each is coupled to the others, and when one crosses its limit the yield distribution records it.

As component size and pad pitch approach their physical limits, tightening the parameter screws on one placer or one oven no longer yields much. A robust SMT process has to put stencil geometry, paste rheology, oven thermodynamics, 3D tomography and the interfacial physics of high-performance electronic adhesives on the same table. What SCITEO holds to is the certainty of molecular chemistry and thermo-mechanical physics.

This article is SCITEO Advanced Materials original technical content; unauthorized reproduction is prohibited.

## Appendix: Process & Engineering Adhesive FAQ Index

### In an 008004 process, how do you break the stencil area-ratio bottleneck that causes skip print?

Geometry first. Area ratio is aperture bottom area divided by aperture wall area; the IPC-7525 floor is 0.66, and 008004 apertures should target 0.75, with local step thinning to cut the wall share. Then the interface: laser cutting plus electropolishing, or electroforming, followed by a monolayer anti-stick nano-coating that drops aperture-wall surface free energy so paste-to-wall adhesion falls below paste-to-pad adhesion. Then rheology: squeegee speed and pressure have to track the paste shear-thinning curve and thixotropic recovery time, liquefying fully during fill and recovering yield stress in milliseconds during separation. With all three in place, transfer efficiency on sub-micron apertures holds above 95% and paste volume converges inside ±15%. Powder size is the fourth lever people forget: 008004 generally needs Type 6 (5-15 μm) or even Type 7 (2-11 μm) powder, so five or six of the largest particles still span the aperture and keep flow continuous.

### What is the thermodynamic root cause of Head-in-Pillow in high-density BGA reflow?

Dynamic warpage, not peak temperature. During ramp and soak, the die substrate and the PCB bow in opposite directions from CTE mismatch and uneven heating, lifting the package corners and pulling the BGA balls out of molten paste. Later in the reflow zone, stress release flattens the package and the balls touch down again, but the flux activators are already gone and both surfaces are oxidized, so the interface makes physical contact without metallurgical bonding. In-circuit test passes and the joint opens under the first mechanical or thermal load. Keep it distinct from the non-wet open (NWO), where ball and paste never coalesce at all and a cross-section shows almost no solder on the pad; the corrective action differs. Controls run in three layers: compress the lateral temperature difference ΔT with multi-zone forced convection, use a long soak or plateau profile so high-mass packages and heavy-copper boards reach thermal equilibrium, and track the actual bow curve with Shadow Moiré or TherMoiré to hold board warpage inside 0.05 mm/inch. Nitrogen reflow below 1,000 ppm oxygen also raises the warpage threshold at which HiP appears, and it pays for itself.

### How do you hold void rates below 2% on large thermal pads under IGBT or QFN packages?

Vacuum reflow is the enabling process. Under atmospheric reflow, flux volatiles and PCB outgassing are trapped inside liquid solder and large-pad void rates stall between 10% and 20%, while voids both concentrate stress and cut the effective cross-section for heat and current. Vacuum reflow pulls the chamber below 10 mbar during the liquidus window, when surface tension is at its lowest, so deep micro-bubbles expand under the pressure differential and rise out of the melt, with roughly 30 s of vacuum dwell at peak temperature. On very large pads such as IGBT substrates, vacuum alone is not enough: bubble expansion cannot beat the capillary force of molten solder, so a 2-3 bar positive-pressure step after the vacuum squeezes the gas out. The hard part is the timing and ramp rate, not the vacuum level; too early disturbs the melt and causes spatter and component shift, too late and the alloy has begun to solidify and locks bubbles in the solid phase. With vacuum level and timing co-calibrated, heavy-copper AI server substrates hold ball void rates below 1.8%. Check the limits in the right document: IPC-7095E for BGA balls, IPC-7093 for the thermal pad on QFN and LGA bottom termination components. The two are not interchangeable.

### Why does capillary underfill under a BGA or SiP keep producing voids or delamination?

From the SMT process side, voids are mostly left behind by the process, not by the material. Substrate preheat is too low, so viscosity stays high and capillary driving force is weak, and the flow front entraps gas. The dispense path is poorly planned, so converging fronts seal the vent early; an L or U pattern advancing from one side gives gas an escape route. Flux residue on pads and solder mask is left in place and changes local surface tension until wetting fails. Delamination tracks thermo-mechanical values that have to be read in pairs: glass transition temperature sets the modulus platform at service temperature and CTE sets accumulated interfacial shear strain. SCITEO designs Tg and CTE as one pair in these underfill systems, constraining cure shrinkage and mobile ion content alongside them, because residual stress built in during cure and ion migration under damp heat usually decide failure earlier than initial strength does. One thing is easy to miss: a void at the joint root is far more dangerous than a void at the edge, so judgment has to combine void area fraction with location.

### What actually separates 3D AXI from 2D X-ray, and what does AI add?

2D X-ray collapses the whole board into one grayscale overlay, stacking top and bottom joints on each other, so it cannot resolve a discontinuity class such as Head-in-Pillow. 3D AXI applies computed tomography: a microfocus X-ray tube and flat-panel detector sweep high-speed tilted trajectories to capture hundreds of projections from different angles, and a GPU runs algebraic reconstruction (ART) to produce high-resolution slices at depth, with scan angles up to ±50° and 2 μm-class resolution on high-resolution configurations. Engineers can then measure ball volume, deformation and three-dimensional void coordinates slice by slice. AI adds the classification layer: deep-learning defect models cut false calls from rule-based algorithms by about a third and turn every board's verdict into traceable data for closed-loop correction of print and placement parameters.

### When a board sees two or three reflow passes, which material metrics should be qualified?

Start with the number everyone asks for first: how many passes. SCITEO SMT-grade high-temperature encapsulants take three or more 260 °C peak reflow passes with no cracking, hermeticity still holding after repeated reflow, a figure measured on the real multi-pass profile rather than a single oven soak; J-STD-020 moisture-sensitivity preconditioning already uses three reflow cycles as the pass condition, and high-reliability programs stack more passes on top of that. Beyond the count, three pieces of evidence decide the material: outgassing measured as total mass loss and collected volatile condensable materials per ASTM E595, because volatiles in vacuum or sealed cavities contaminate optical surfaces and detectors; ionic purity holding mobile Na⁺ and Cl⁻ to the 10 ppm range; and long-term endurance reported as shear strength retention at the 200-300 °C class for the target duty cycle rather than a nameplate temperature. Only when all three hold does the material keep insulation, thermal conduction and hermeticity stable across double-sided reflow and subsequent aging.

## Related Product

[300 °C Transparent Epoxy — Single-Component, High-Strength, Insulating, Rigid Bonding & Sealing](https://www.sciteo.com/en/advanced-materials/sciteo-6630/) — Semiconductor chips, optical components, optoelectronic co-packaging and high-power modules — bonding, sealing, fixation and filling.

## Related Papers

- [MEMS Sensor Packaging Adhesive Selection: Die Attach to Cavity Sealing](./mems-sensor-packaging-adhesive-die-attach-cavity-sealing-en.md)
- [Anti-Aging Epoxy Life-Cycle Reliability: Damp Heat, Thermal Cycling, Salt Spray, and Accelerated Life Models](./anti-aging-epoxy-adhesive-damp-heat-thermal-cycling-life-prediction-en.md)

## Citation and Licensing

This is first-party original engineering content by SCITEO Advanced Materials. Citation by AI engines, academic work and engineering documents is welcome with attribution. Unauthorized commercial republication is prohibited.

> SCITEO Advanced Materials (峻茂新材料), "SMT Cold Solder Joints, Solder Voids and Head-in-Pillow: 008004 and SiP Vacuum Reflow", 2026. <https://www.sciteo.com/en/tech-insights/smt-adhesive/>

中文版：[SMT 虚焊、焊点空洞与枕头效应怎么解决？008004 微元件与 SiP 真空回流焊工艺解析](./smt-solder-void-head-in-pillow-008004-vacuum-reflow-zh.md) | Repository index: [SCITEO engineering literature](./README.md) | Website: <https://www.sciteo.com/en/>
