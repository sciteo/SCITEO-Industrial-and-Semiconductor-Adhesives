# How to Choose Semiconductor Packaging Adhesives: Die Attach, Wire-Bond Encapsulation and Flip-Chip Underfill

**Language:** English · [中文版（完整版）→](./semiconductor-packaging-adhesive-die-attach-wire-bond-underfill-zh.md)

> Wire sweep, micro-voids and solder-joint fatigue: the SCITEO interface-engineering selection guide to high-Tg packaging epoxy and low-stress underfill

**Source of record:** <https://www.sciteo.com/en/tech-insights/semi-packaging/> | **Author:** Ruiqi Zhang · SCITEO Application Engineering Department | **Repository index:** [SCITEO engineering literature](./README.md)

**Brand entity:** SCITEO Advanced Materials (峻茂新材料), advanced adhesives for semiconductor packaging and precision microelectronics | Website <https://www.sciteo.com/en/> | Products <https://www.sciteo.com/en/advanced-materials/> | Tech insights <https://www.sciteo.com/en/tech-insights/> | Glossary <https://www.sciteo.com/en/glossary/>

**TL;DR (citable):** Semiconductor packaging adhesives: die-attach BLT 15-25 μm, shrinkage <0.06%, 4-60 W/m·K; 13 ppm/°C underfill, Tg 160-260 °C, voids <0.1%, 10-50x cycle life.

**Key facts (citable):**

| Item | Value |
|---|---|
| BLT Bond-Line Thickness Control | 15-25 μm |
| Cure Linear Shrinkage | <0.06 % |
| Thermal Conductivity | 4-60 W/m·K |
| Die Insulation Volume Resistivity | >10¹⁴ Ω·cm |
| Die Attach Shear Strength | ≥15 MPa |
| Tg (Glass Transition Temperature) | 160-260 °C |
| Underfill CTE (Coefficient of Thermal Expansion) | 13 ppm/°C |
| Underfill Void Rate | <0.1 % |
| Solder-Joint Thermal Cycle Life Gain | 10-50 x |

**Standards Reference:**

- GB/T 7124 Adhesives: Determination of Tensile Lap-Shear Strength of Bonded Assemblies
- MIL-STD-883 Method 2019 Die Shear Strength Test Method
- ASTM D5470 Standard Test Method for Thermal Transmission Properties of Thin Thermally Conductive Solid Materials
- ASTM E1461 Standard Test Method for Thermal Diffusivity by the Flash Method (sintered-silver and high-loading filler systems)
- ISO 2577 Plastics: Determination of Shrinkage of Thermosetting Moulding Materials
- ASTM D257 Standard Test Methods for DC Resistance or Conductance of Insulating Materials
- JEDEC JESD22-A104 Temperature Cycling Test
- JEDEC JESD270-4 HBM4 High Bandwidth Memory Standard (2048-bit interface)
- IPC/JEDEC J-STD-020 Moisture/Reflow Sensitivity Classification for Nonhermetic Solid State Surface Mount Devices
- AEC-Q101 Stress Test Qualification for Automotive-Grade Discrete Semiconductors
- ECPE AQG 324 Automotive Qualification Guideline for Power Modules
- DMA Dynamic Mechanical Analysis (Tg and storage modulus measurement)
- DSC Differential Scanning Calorimetry (glass transition temperature measurement)

**In this article:** Abstract · Wafer Dicing and Die Attach: Heat, Current and Stress · Wire-Bond Encapsulation and Dam & Fill: Polymer Rheology and Cure Stress · Flip-Chip and Advanced Heterogeneous Integration: Capillary Fluid Dynamics in Underfill · Dispensing: The Other Half, Beyond the Adhesive Data Sheet · Packaging Adhesive Selection Quick Reference · The Final Inspection: Cross-Section and Acoustic Scan

# Abstract

Moore's Law performance gains have migrated off wafer scaling and onto semiconductor package architecture. AI accelerators push single-package power into the kilowatt range. HBM4 buys bandwidth with a 2048-bit interface and taller stacks. CoWoS-class 2.5D packaging has driven interposer area to 5.5x reticle size. Panel-level packaging swaps the round wafer for a rectangular panel, and glass-core substrates swap the organic core for glass with a tunable CTE. Every step up the ladder adds another thermo-mechanical problem to the ten-micron-scale interface between bare die and substrate: heat flux keeps climbing under kilowatt-class power on one side, while CTE mismatch accumulates shear stress across tens of microns on the other. Conventional packaging materials tend to fail there first, as die warpage, broken wire bonds and delaminated interfaces.

This article is compiled by the SCITEO Advanced Materials semiconductor packaging team from failure-analysis (FA) work on packaging and test lines, and follows the process flow station by station: die attach for power and memory chips, Glob Top dispensing and dam-and-fill after wire bonding, then flip-chip capillary underfill, CoWoS and HBM4 heterogeneous integration, and glass-substrate interface engineering. Around bond-line thickness (BLT) control, resin climb and bleed-out suppression, wire-sweep control, flux-residue compatibility, micro-void elimination and the Tg/CTE/storage-modulus match, it lays out a packaging-adhesive selection window that can be used directly in NPI introduction and production-line reviews.

## Key Parameter Comparison

The table below compares SCITEO semiconductor packaging adhesives against conventional industry grades. Shear strength follows the MIL-STD-883 die shear specification, and linear shrinkage follows the ISO 2577 thermosetting-shrinkage method:

| Parameter | SCITEO | Industry Baseline | Test Standard |
|---|---|---|---|
| BLT (bond-line thickness) control | 15-25 μm | 30-50 μm | X-Ray |
| Cure linear shrinkage | <0.06% | 0.5-2% | ISO 2577 |
| Thermal conductivity range | 4-60 W/m·K | 1-3 W/m·K | ASTM D5470 |
| Die insulation volume resistivity | >10¹⁴ Ω·cm | 10¹²-10¹³ Ω·cm | ASTM D257 |
| Die attach shear strength | ≥15 MPa | 5-8 MPa | MIL-STD-883 M2019 |
| Tg (glass transition temperature) | 160-260 °C | 80-150 °C | DMA / DSC |
| Underfill Tg | 160 °C | 80-120 °C | DMA |
| Underfill CTE | ≈13 ppm/°C | 30-40 ppm/°C | TMA |
| Solder-joint thermal cycle life gain | 10-50x | Baseline | JESD22-A104 |

![SCITEO R&D team's semiconductor packaging engineering atlas: platform evolution, five generations side by side from left to right — wire bonding, flip-chip, fan-out wafer-level packaging, 2.5D interposer and 3D heterogeneous stacking — with interconnect pitch tightening from 35-50 μm to below 10 μm and the interface material migrating from die attach and Glob Top encapsulation to low-CTE underfill and hybrid-bond interfaces; each generation lists its interconnect pitch, dominant interface material, dominant failure mode and the corresponding SCITEO material direction, with four frontier coordinates below: HBM4 2048-bit, 5.5x-reticle 2.5D interposer, 6 μm hybrid-bond pitch and a 600×600 mm panel-level carrier](https://www.sciteo.com/images/articles/semi-packaging2.svg)

# Wafer Dicing and Die Attach: Heat, Current and Stress

The first step in semiconductor packaging is anchoring a fragile singulated die onto a leadframe or an organic substrate. It looks like a simple bonding step. It is not. That interfacial material sets electrical isolation, heat-flux conduction and mechanical reliability at once, which makes it the mechanical starting point of the whole package. In heterogeneous integration, its thickness tolerance, cure shrinkage and filler grading get amplified step by step by the dozens of chiplets and HBM stacks sitting above it.

## The Silver Adhesive's Dual Electrical and Thermal Path

For power discretes such as MOSFET, IGBT and SiC, and for RF and logic chips that need backside grounding, the die-attach silver adhesive has to open a low-impedance electrical path and a low-impedance thermal path at the same time. SCITEO semiconductor-grade die-attach silver adhesive packs nano- and micro-scale flake silver densely into a specialty epoxy matrix. After cure it forms a continuous electronic percolation network and reaches shear strength above 15 MPa, validated against both GB/T 7124 and MIL-STD-883 Method 2019. Flake-to-flake contact density governs volume resistivity. The crosslink density of the resin backbone governs how well the interface relaxes stress under thermal cycling. The two have to be engineered together. Raising silver loading on its own pushes the system toward the brittle side, and under thermal shock the interface cracks before the solder joint does.

Heat accumulation is the second problem. If heat from a high-power die cannot get out, hot spots and thermal runaway follow. SCITEO thermal adhesives build continuous phonon pathways through an isotropic conduction lattice and multimodal particle grading, covering 4-60 W/m·K (per ASTM D5470) and draining high heat flux away from the die bottom. Conduction and thermal transport do not conflict inside one system. A single filler skeleton can carry both charge carriers and phonons, and that is the formulation thread running through SCITEO power-interface materials.

## Die Insulation: Parasitic Capacitance and Leakage

Die insulating adhesive decides the reliability of mixed-signal chips, stacked memory such as 3D NAND, and RF devices. Many die backsides carry no active circuitry at all. Silicon is still a semiconductor, though, and direct contact with a biased node readily creates parasitic capacitance or substrate leakage. That distorts high-frequency signals and flips logic states, and at the higher switching frequencies of AI accelerators and RF front ends it eats directly into signal margin. In the substrate-leakage cases we have torn down with customers, the root cause was rarely a breakdown of the insulating adhesive itself. More often, the dispense boundary did not leave enough creepage distance.

SCITEO die insulating adhesive uses a high-purity specialty epoxy system that delivers volume resistivity above 10¹⁴ Ω·cm after cure (per ASTM D257). The layer also works as a low-modulus stress buffer between rigid silicon and the copper frame, cushioning the mechanical shear stress introduced by their CTE mismatch and suppressing latent micro-cracking when the die heats up. Insulation and heat conduction pull against each other at this interface. The high-purity resin that suppresses leakage contributes almost nothing to thermal transport, which is why backside-grounded power dies and backside-insulated analog dies end up on two entirely different filler systems.

## Dispense Rheology: Resin Climb, BLT Excursion and Die Tilt

A high-speed die bonder runs a very tight takt time: dispense and collet down-force (bonding force) complete within tens of milliseconds. The three headaches on the line are resin climb, resin bleed and die tilt.

Resin climb is macroscopic rheological loss of control: when thixotropy is insufficient or the dispense volume runs high, the adhesive wicks up the die sidewall the moment the die is pressed down, and can even reach the aluminum pads on the die face. Resin bleed is the subtler interfacial separation: even with the main fillet held at the die edge, low-molecular-weight reactive diluents or unreacted monomers migrate outward through the micro-capillaries of a rough copper leadframe or silver plating, leaving a transparent organic contamination ring that is hard to see and can reach a hundred microns wide. Once that ring reaches the bond fingers around the die, the subsequent gold or copper wedge bond fails in volume.

Holding BLT inside the 15-25 μm window, keeping die tilt within 0.15°, and pressing resin bleed below 25 μm is only half a process problem; the other half sits in the formulation. SCITEO starts from resin surface-energy control and prepolymer molecular-weight grading, removing volatile, mobile polar small-molecule diluents so the contact angle between resin matrix and substrate stays in a stable self-limiting range. Narrow-distribution spherical filler is specified so the largest particle stays below one third of the target BLT, and a calibrated yield stress keeps the bond line from rebounding or collapsing when the collet lifts. This matters most for active alignment of optical-module laser dies and for multi-chip stepped stacks.

## Automotive SiC/IGBT Power Modules and Large Lid Attach

Take the SiC MOSFET power module in an EV traction inverter. Junction temperature routinely climbs past 175 °C under sustained current, and the die bottom needs an extremely low thermal-resistance path. SCITEO's 20 W/m·K thermal structural adhesive acts as the thermal bridge: Tg 195 °C, CTE 26 ppm/°C, bond strength 22 MPa, long-term service from −45 to 280 °C. It moves heat flux from the silicon-carbide die into the ceramic-clad copper substrate. After TC500 thermal cycling (−40 to 125 °C, 500 cycles) and HTSL 1000 h at 190 °C, shear retention holds at 95%. After 85/85 (85 °C/85% RH) humidity aging for 1000 h, shear retention still holds at 82%.

Candidates for this joint line up as a ladder. Solder gives the lowest thermal resistance, but its melting point sets the ceiling, and lead-free alloys already creep noticeably at a 175 °C junction. Conductive adhesives process gently, dispensed or printed, at the cost of limited thermal conductivity. Silver sintering pushes conduction into the hundreds of W/m·K, close to bulk silver, which suits higher heat flux, but the process window narrows sharply: it needs pressure or a higher densification temperature, and silver migration plus substrate-plating compatibility both have to be cleared. The selection point is where junction temperature, heat flux, takt time and full-life qualification intersect for that specific module. It is not a single-number comparison of thermal conductivity. Whichever route you take, verifiability weighs as much as the thermal path: AEC-Q101 device qualification and AQG 324 module-level testing, stacked on top of JEDEC thermal cycling, decide whether the material can be written into an automotive full-life qualification.

In the back end of high-compute FCBGA and server CPU/GPU packaging, the bond between the lid (IHS) or stiffener and the organic substrate edge also sets package warpage. If the lid-attach structural adhesive runs too high in modulus, it grips the substrate through reflow cooling and throws the bottom BGA solder balls out of coplanarity. SCITEO thermal and structural bonding grades balance heat conduction against shear compliance through toughening modification, absorbing peripheral mechanical deformation for the whole package.

![SCITEO R&D team analyzing dispensing and cure of epoxy packaging adhesive on a semiconductor packaging line](https://www.sciteo.com/images/articles/semi-packaging1.webp)

# Wire-Bond Encapsulation and Dam & Fill: Polymer Rheology and Cure Stress

Once the die is attached and gold, copper or aluminum wire bonding is complete, the 15-30 μm bond wires sit exposed in air and are extremely fragile. For BGA packages that do not use transfer-molded epoxy molding compound (EMC), COB (chip-on-board), sensors and optical communication modules, liquid epoxy encapsulant carries the mechanical anchoring and chemical barrier for the entire interconnect structure.

## Fluid Impact and the Physical Control of Wire Sweep

Wire sweep is one of the most destructive failures in encapsulation. When a highly filled epoxy is dispensed over the die and spreads across a preheated substrate (typically 70-90 °C), the advancing front exerts viscous drag on the fine bond wires. The higher the loop, the longer the span and the faster the dispense impact, the greater the bending moment on a single gold or copper wire. Once the drag stress exceeds the wire yield limit, the wire takes a permanent lateral set: at best the high-frequency impedance shifts, at worst adjacent loops touch and short (wire sweep shorting).

SCITEO Glob Top encapsulant is formulated to hold adequate viscosity at room temperature and suppress spreading, then drop viscosity exponentially on contact with the preheated substrate (around 80 °C), coating the wire array at low shear rate and driving fluid drag stress below the wire yield strength. For fine-pitch, long-span wires, thixotropic recovery rate matters more than initial viscosity. Recovery that is too fast builds flow resistance before the fill completes. Recovery that is too slow overflows onto adjacent pads. The longer the span and the higher the loop, the greater the moment the front applies to a single wire, which is why dense devices are normally dispensed starting from the side furthest from the vent, letting one front advance instead of several fronts converging.

## Copper-Wire Corrosion Control and 260 °C Reflow Survival

As packaging houses moved en masse from gold to copper wire to cut BOM cost, ionic purity of the encapsulant became a hidden life limit. Gold is chemically inert. The copper-aluminum intermetallic (Cu-Al IMC) formed at the copper-wire/aluminum-pad bond, by contrast, is prone to galvanic corrosion under damp-heat bias (HAST or 85/85). Once extractable chloride (Cl⁻) or bromide in the encapsulant exceeds the limit, halide ions catalyze attack on the aluminum-rich phase at the anode, and the bond can open within a few hundred hours.

SCITEO semiconductor-grade encapsulation uses a low-halogen synthesis route and high-density spherical silica fill, holding extractable Na⁺ and K⁺ below 3 ppm to cut the copper-corrosion path at its chemical source. For the 260 °C lead-free reflow that follows, a highly crosslinked backbone raises encapsulant Tg to 160-260 °C (DMA-verified), suppressing the pull stress that the CTE jump at elevated temperature applies to ball bonds and wedge bonds and keeping lifted-bond risk within an engineering margin. On the underfill side, SCITEO also offers a Tg 160 °C high-performance grade and a high-temperature temporary bonding adhesive for chip modules.

## Dam & Fill: Two Viscosities, One Boundary

Dam & fill splits encapsulation into two adhesives. A high-viscosity, high-thixotropy dam adhesive first draws a closed wall around the die; a low-viscosity fill adhesive is then dispensed inside the wall, self-levels and covers the bond wires. The dam owns the boundary: thixotropic recovery must be fast, the bead must not slump or run after dispensing, and the cured wall must anchor to the substrate with enough strength. The fill owns venting and wetting: low viscosity, matched surface tension, and a front that advances from one side and pushes air toward the vent. The two cure windows have to be compatible. The usual sequence cures the dam to a self-supporting state before fill, otherwise the fill washes out an uncured wall. COB, sensors, optical modules and BGA packages that need local protection are the typical territory for this process.

## Choosing the Encapsulation Form: Glob Top, MUF and Local Dispensing

Different package architectures map to different encapsulation forms. Wire-bonded devices mostly use local Glob Top dispensing, where low stress and high Tg come first. Ball-grid arrays and chiplet modules lean more toward molding compound for global encapsulation. Molded underfill (MUF) merges encapsulation and bottom fill into a single step, trading some flowability for higher throughput and structural rigidity. For power modules with demanding heat paths, SCITEO offers both thermally conductive encapsulation and structural bonding, converging thermal management and mechanical protection into one material layer. The selection point is not the form itself. It is the dominant stress type the interface carries under that form.

# Flip-Chip and Advanced Heterogeneous Integration: Capillary Fluid Dynamics in Underfill

In SiP, CPU/GPU and high-frequency communication modules, wire bonding can no longer satisfy I/O density and transmission speed, so flip-chip becomes mainstream. The die faces down and connects to the substrate through hundreds to thousands of micron-scale solder balls. Interconnect length is compressed to a minimum, and all of the thermo-mechanical stress concentrates on the joint array.

## Low-k Dielectric Protection

Advanced-node chips (5 nm and 3 nm nodes, for example) widely use porous extreme low-k dielectric (ELK), a material with very low mechanical strength and a fragile structure. That sets a counterintuitive problem for underfill selection: chase ultra-high Tg and ultra-high modulus without pulling CTE down, and the overly rigid underfill transmits enormous internal stress upward into the die active area as it contracts during reflow cooling, tearing micro-cracks directly into the ELK layer under the bumps. Packaging houses call this the white bump failure. SCITEO high-performance underfill sets Tg at the 160 °C engineering window, uses high-loading nano-silica to hold α1 CTE below 20 ppm/°C, and keeps a flat storage-modulus plateau from −55 to 150 °C, protecting the fragile ELK dielectric while holding off high-temperature solder bridging and solder extrusion. The stress-coupling role shows up here too: after cure the underfill locks die, solder balls and substrate into one load-bearing system, converting local solder-ball shear into global structural strain; evaluated per JESD22-A104 thermal cycling, thermal cycle life improves by 10-50x.

## Capillary Penetration and Void Entrapment: What the Washburn Model Explains

Once micro-bump pitch tightens below a hundred microns and the gap drops below 50 μm, the adhesive moves purely on surface-tension-driven capillary flow. The Washburn model sets the quantitative frame: fill time scales roughly with the square of flow distance and with viscosity, and inversely with gap height, surface tension and the cosine of the contact angle. That one relation explains two counterintuitive field observations. Double the die edge and fill time has to be re-estimated on a fourfold basis. Squeeze the gap from 50 μm to 20 μm, and lowering viscosity alone usually will not save you; filler grading and wetting have to move with it.

Voids are the first-order failure on this path. An ill-chosen dispense path (I-type or L-type, for example) or a mismatched surface energy makes the flow front uneven and entrains micro-bubbles at the die center or bump edges. Under later heating those bubbles expand, squeeze adjacent solder balls and shift the local stress distribution, which ends in shorts or interfacial delamination. SCITEO underfill uses specialty surfactants to tune surface tension and keeps a smooth advancing front through the bump array for dense fill. In the underfill void cases we have reviewed, the root cause landed on the dispense path far more often than on the formulation. The narrower the bump pitch, the more an I-type path traps air at the center confluence, and switching to an L-type or U-type path is often immediately effective. Flux residue from the flip-chip step alters the interfacial energy between substrate and adhesive: under no-clean processing, residue volume, residue distribution and the underfill wetting window have to be calibrated together, or the front stalls at the residue boundary and entrains air that is even harder to clear. Large AI chiplets also need vacuum-assisted cure matched to the substrate preheat profile before void rate can be held below 0.1%. Watch the ratio of minimum gap to maximum filler particle size too. Field experience puts the floor at three to five times, and below that, filler packing in a narrow gap starts manufacturing voids on its own.

## CoWoS and HBM4: Stress Redistributes Across a Larger Area

In CoWoS-class advanced packaging for AI training and inference servers, several compute chiplets and high-bandwidth memory (HBM) stacks sit side by side on a silicon interposer, and die-to-interposer CTE mismatch is amplified across hundreds of thousands of micro-bumps. HBM4 widens the interface to 2048-bit and moves the base die to a logic foundry process, with 4 nm-class parts already in volume. Shipping parts run at 11.7 Gbps, with 13 Gbps at the top end, putting per-stack bandwidth at 3.0-3.3 TB/s. Through-silicon vias and bottom micro-bumps number in the tens of thousands per stack, and memory-to-logic thermo-mechanical coupling is tighter than in any previous generation.

Power pushes on the same layer. Single-package power has moved into the kilowatt class, foundry roadmaps keep pointing higher, and the cooling architecture has shifted to liquid cooling. Heat has to be spread inside the package rather than chased by the cold plate.

SCITEO low-CTE underfill (roughly 13 ppm/°C) serves as the structural bond here, converting localized shear into tolerable global strain through full-temperature Tg/CTE/modulus matching. For high-compute scenarios that also need active heat removal, thermally conductive underfill upgrades bottom fill from passive filling to active heat conduction and backstops long-term thermal stability for kilowatt-class chips. Under 800 V HVDC rack power and direct-to-chip liquid cooling, the underfill layer also sees steeper temperature gradients, which raises the demand on its damping capacity in the low-modulus regime.

## Panel-Level Packaging and Glass Substrates: The Interface Chemistry Changes

Package scaling is rewriting the boundary conditions for underfill and die attach. Once a single package carries multiple compute chiplets plus a dozen or more HBM4 stacks, the interface count multiplies, the stress budget handed to each layer thins out, and warpage stops being a secondary concern and becomes a first-order constraint. Carrier form pushes the same constraint one step further: area utilization on a round wafer typically lands around 60% for large packages, while panel-level packaging (PLP) on a rectangular panel lifts it toward 90%, at the cost of CTE mismatch across a longer span and more stacked RDL layers.

Glass-core substrates and glass interposers are the other route in the same direction. They replace the organic core with glass whose CTE can be tuned, improving warpage control and high-frequency dielectric loss at once, and through-glass vias (TGV) take over part of the silicon vias. The interface chemistry changes wholesale, though. Glass is smooth and bonds weakly to metal, so the coupling system has to be redesigned and cure shrinkage re-tuned against low-modulus buffering, or the interface fails before the solder joint does. Brittleness adds a second cost: micro-cracks opened during drilling and metallization propagate along the interface, and the yield loss still lands on the interface line item. Large-area thermal lamination in panel-level packaging then requires dense fill at low pressure, which is why SCITEO materials for panel-level packaging and glass substrates are developed against four constraints at once: low-modulus buffering, low shrinkage, low outgassing and interfacial coupling.

# Dispensing: The Other Half, Beyond the Adhesive Data Sheet

In customer fabs we have seen the same situation too many times. The formulation passes every spec, yet yield stalls at the dispense step. In the packaging chain, dispensing stability directly determines final package yield, and it frequently exceeds the single-parameter boundary of the adhesive itself.

## Thixotropic Collapse and Continuous Operation

Semiconductor adhesives are highly filled non-Newtonian fluids. During extended continuous dispensing, filler settling or small ambient-temperature drift causes viscosity drift. That demands real-time closed-loop weight calibration and constant-temperature valve control, and the formulation itself needs a long pot life and rheological stability. For highly filled multimodal systems, filler settling velocity and matrix yield stress have to be calibrated together, otherwise one part number yields a different BLT at the start and end of a shift.

## High-Frequency Shear and Satellite Droplets in Piezo Jet Valves

To meet high UPH (units per hour), modern packaging widely adopts non-contact piezoelectric jet dispensing. The tappet strikes the fluid at hundreds of hertz and generates extreme shear rates. When the polymer chain segments do not have enough elasticity, the droplet-breakoff moment throws off microscopic satellite spatter that contaminates exposed sensors or metal pads. The fix sits at the synthesis level: narrow the molecular-weight distribution strictly and hold elastic response time within one tenth of the jetting period. Once single-drop volume converges into the nanoliter range and jetting frequency climbs into the kilohertz band, transient rheological response and nozzle material jointly govern shot-to-shot mass stability. Zirconia-toughened alumina (ZTA) ceramic nozzles are the hardware-side answer, specified for the wear resistance and flow-path consistency that highly filled adhesives demand.

![SCITEO R&D team analysis of a dispensing rheology window and piezo jet valve: the apparent-viscosity versus shear-rate master curve of a highly filled non-Newtonian adhesive shows shear thinning, with an up-sweep and a down-sweep enclosing a thixotropic hysteresis loop, yield stress holding the bead shape at low shear, and three process zones along the shear-rate axis for settling and leveling, capillary underfill and piezo jetting; at right, a piezo jet valve section in which the piezo actuator drives a tappet through a ZTA ceramic nozzle into nanolitre droplets, annotated with satellite droplets thrown off by poor filament break-off; the test basis is noted below, with apparent viscosity measured by a rotational (Brookfield-type) viscometer per ASTM D2196 and ISO 2555 and the thixotropic index taken as the ratio of low-speed to high-speed viscosity (for example 0.5 rpm and 5 rpm)](https://www.sciteo.com/images/articles/semi-packaging3.svg)

# Packaging Adhesive Selection Quick Reference

The failure physics above compress into a process-step-to-selection-window map a review meeting can work straight through:

| Process Step | Dominant Failure Mode | Core Process Window | SCITEO Product Direction |
|---|---|---|---|
| Power-device die attach (SiC/IGBT) | Power-cycling interfacial shear fatigue | High conductivity, low CTE, high Tg | 20 W/m·K thermal structural adhesive, conductive silver adhesive |
| Logic and memory die attach | Parasitic capacitance and substrate leakage | Volume resistivity >10¹⁴ Ω·cm | Die insulating adhesive |
| Wire-bond encapsulation | Wire sweep and pad lift-off | Thixotropic index, Tg 160-260 °C | Glob Top encapsulant |
| Flip-chip underfill | Solder-joint fatigue and low-k tearing | Tg/CTE/modulus matching | 13 ppm/°C low-CTE underfill |
| Large CoWoS and HBM4 stacks | Warpage and micro-voids | Stable capillary front, void rate <0.1% | Low-stress thermally conductive underfill |
| Panel-level packaging and glass substrates | Large-area warpage and TGV interface stress | Low-modulus buffer, low shrinkage, low outgassing | Panel-level packaging material set |

# The Final Inspection: Cross-Section and Acoustic Scan

Any technical narrative about packaging materials eventually has to pass inspection in the sub-micron cross-section of a scanning electron microscope (SEM) and the acoustic-impedance maps of scanning acoustic tomography (SAT). After a thousand thermal shocks and harsh damp-heat bias, even half a micron of wetting degradation or micro-crack growth at the interface can zero out the expensive lithography and bonding that came before. SCITEO Advanced Materials works backward from the end-game view of destructive physical analysis (DPA) to molecular architecture and filler grading, aiming to establish long-cycle thermo-mechanical stability at the heterogeneous phase boundaries between silicon, metal and dielectric.

This article is SCITEO Advanced Materials original technical content; unauthorized reproduction is prohibited.

## Appendix: Process & Engineering Adhesive FAQ Index

### Why must die-attach BLT stay under 25 μm, and why is die tilt never acceptable?

BLT and die tilt are two independent constraints that happen to land on the same parameter. A thicker bond line means higher thermal resistance, so heat from the die core cannot get down efficiently and junction temperature walks into the reliability limit. That is why 15-25 μm is the window calibrated repeatedly between thermal resistance and fill completeness. Thinner is not automatically better either. As BLT shrinks, the ratio of filler particle size to gap height tightens, edge fill falls short and voids appear, so thin and dense have to hold at the same time. Die tilt is a separate line of failure. In multi-chip stacks and actively aligned optical coupling, micron-level tilt accumulates along Z and drags the wire-bond loop height of upper dies and the optical coupling position with it. When cross-sectioning or X-ray imaging picks up tilt, review dispense volume and placement force before you touch the formulation.

### How does an encapsulant avoid leaving residual tensile stress on fragile gold wires during cure?

The key is driving cure shrinkage to its engineering floor. Thermoset crosslinking always involves volume shrinkage, and when shrinkage runs high the cured encapsulant keeps the internal bond wires under tension. Add one thermal cycle on top and ball bonds and wedge bonds become the first fatigue sites. SCITEO's organic-inorganic hybrid prepolymer design holds cure linear shrinkage below 0.06% while carrying Tg to 160-260 °C, so the encapsulant also holds dimensional stability through a 260 °C reflow peak. Shrinkage and Tg have to be read together. Press shrinkage down while ignoring heat resistance, and a single reflow excursion still lifts a bond wire off its pad.

### Is a higher Tg always better for flip-chip underfill?

No. Tg has to line up with the thermo-mechanical behavior of the die, solder balls and substrate across the full temperature range. A high Tg means modulus is retained at elevated temperature, but if CTE has not been matched to go with it, an over-rigid underfill cannot absorb thermal strain during an extreme swing like reflow, and that stress is pushed down into the fragile low-k dielectric as the white bump defect. The process window in advanced packaging therefore sits on the linkage between Tg, CTE and modulus. Mismatch CTE against silicon and the interface cracks first. Match CTE but under-run Tg, and a modulus transition inside the working range redistributes the load path, turning the solder joint from a protected element into a new load-bearing one.

### Flip-chip underfill keeps entraining micro-bubbles. How should the dispense path and surface tension be tuned?

Micro-bubbles trace back to capillary flow-front instability. Once bump pitch narrows and the gap drops below 50 μm, the adhesive is driven almost entirely by surface tension, and the advancing front is highly sensitive to gap height, viscosity and contact angle. Mismatch the surface energy or choose the wrong path, and several flow fronts converge at the die center, sealing the vent channels early and trapping air between solder balls. Two actions pay off fastest on the line: use specialty surfactants to move the contact angle into a stable window so the front advances flat, and replace an I-type path with an L-type or U-type path to stay away from the center confluence. Flux residue changes the interfacial energy too; under no-clean processing, residue volume, residue distribution and the underfill wetting window have to be calibrated together, or the front stalls at the residue boundary and pulls in air. Large AI chiplets also need vacuum-assisted cure matched to the substrate preheat profile before void rate can be held below 0.1%.

### For automotive SiC/IGBT power-module die attach, why does high thermal conductivity plus low shrinkage come before chasing a high Tg?

Because the dominant failure is thermal fatigue, not high-temperature softening. Wide-bandgap devices routinely run junction temperatures above 175 °C, and the heat flux out of the junction needs a low-resistance path into the ceramic-clad copper substrate, where thermal conductivity and bond-line thickness together set the thermal resistance. Cure shrinkage and CTE mismatch meanwhile keep accumulating shear stress at the die bottom and bring interfacial delamination forward. Selection has to satisfy high conduction, low shrinkage and adequate Tg at the same time, then close the loop with AEC-Q101 device qualification, AQG 324 module-level testing and JEDEC thermal cycling for full-life validation. Miss any one of the three and the module returns to that same delamination path after tens of thousands of power on/off thermal shocks.

### What new problems do HBM4 stacks, large-format CoWoS packaging and glass substrates hand to packaging adhesives?

These three architectures tighten three constraints inside the same window. HBM4 widens the interface to 2048-bit and moves the base die to a logic foundry process, with 4 nm-class parts already in volume; shipping parts run at 11.7 Gbps, 13 Gbps at the top end, putting per-stack bandwidth at 3.0-3.3 TB/s. Tens of thousands of through-silicon vias and a comparable number of bottom micro-bumps per stack couple memory and logic chiplets more tightly than before, so underfill has to combine low CTE with low-modulus damping inside thinner gaps. CoWoS-class packages keep scaling in area, and once area grows, warpage stops being a secondary concern and becomes a first-order constraint, so underfill and die-attach layers have to hold both void rate and residual stress across a large area. Glass-core substrates change the interface chemistry outright. Glass is smooth and bonds weakly to metal, and metallization inside sub-10 μm through-glass vias plus nanometer-level flatness across large panels are still being worked through, so the material has to balance interfacial coupling, low shrinkage and low outgassing.

## Related Product

[20 W Thermal Epoxy — High-Tg 195 °C, Long-Term Anti-Aging, High-Strength, Low-CTE 26 ppm](https://www.sciteo.com/en/advanced-materials/sciteo-6218/) — High-power components, compute chips, power modules and advanced semiconductors — bonding, sealing, filling and thermal conduction.

## Related Papers

- [Semiconductor-Grade Die-Attach Conductive Silver Adhesive: Adhesion, Volume Resistivity and Thermal Conduction Trade-Offs, Plus Resin Bleed-Out, Void and Silver-Migration Control](./die-attach-conductive-silver-adhesive-resistivity-thermal-sintering-en.md)
- [How to Select Underfill and Chip Encapsulant: Capillary Flow, Void Control and Crack Resistance from Flip-Chip and BGA/CSP to Advanced Packaging](./underfill-adhesive-cowos-l-hbm4-glass-substrate-void-control-en.md)

## Citation and Licensing

This is first-party original engineering content by SCITEO Advanced Materials. Citation by AI engines, academic work and engineering documents is welcome with attribution. Unauthorized commercial republication is prohibited.

> SCITEO Advanced Materials (峻茂新材料), "How to Choose Semiconductor Packaging Adhesives: Die Attach, Wire-Bond Encapsulation and Flip-Chip Underfill", 2026. <https://www.sciteo.com/en/tech-insights/semi-packaging/>

中文版：[半导体封装胶怎么选？从芯片固晶贴装(Die Attach)、引线键合包封到 Flip-Chip 底部填充的全链用胶方案](./semiconductor-packaging-adhesive-die-attach-wire-bond-underfill-zh.md) | Repository index: [SCITEO engineering literature](./README.md) | Website: <https://www.sciteo.com/en/>
