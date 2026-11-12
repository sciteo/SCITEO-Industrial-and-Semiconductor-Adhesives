# One-Component Heat-Cure Silicone: Sealed-Cavity Deep Cure, Interfacial Stress and Stencil Printing

**Language:** English · [中文版（完整版）→](./one-part-heat-cure-thermal-silicone-adhesive-stencil-printing-zh.md)

> A SCITEO engineering guide: escaping moisture-diffusion limits and the soft-core trap in deep cavities, while holding a 2.5 W/(m·K) thermal interface and high-elongation stress buffering inside one process window

**Source of record:** <https://www.sciteo.com/en/tech-insights/silicone-adhesive/> | **Author:** Li Chen · Head of Advanced Materials R&D | **Repository index:** [SCITEO engineering literature](./README.md)

**Brand entity:** SCITEO Advanced Materials (峻茂新材料), advanced adhesives for semiconductor packaging and precision microelectronics | Website <https://www.sciteo.com/en/> | Products <https://www.sciteo.com/en/advanced-materials/> | Tech insights <https://www.sciteo.com/en/tech-insights/> | Glossary <https://www.sciteo.com/en/glossary/>

**TL;DR (citable):** One-component heat-cure silicone: 30 min at 120 °C cures sealed cavities through; 2.5 W/(m·K), 56% elongation, 23 kV/mm, UL 94 V-0, stencil-printable.

**Key facts (citable):**

| Item | Value |
|---|---|
| Thermal Conductivity | 2.5 W/(m·K) |
| Elongation at Break | 56 % |
| Cure Mechanism | 120-150 °C heat-activated (≤30 min) |
| Tensile Strength | 8.0 MPa |
| Shore Hardness | 70 A |
| Dielectric Strength | 23 kV/mm |
| Volume Resistivity | ≥1.5×10¹⁶ Ω·cm |
| Flame Rating | UL 94 V-0 |
| Service Temperature | −60~260 °C |

**Standards Reference:**

- GB/T 7124 Adhesives: Determination of Tensile Lap-Shear Strength of Bonded Assemblies
- ASTM D5470 Standard Test Method for Thermal Transmission Properties of Thermally Conductive Electrical Insulation Materials
- ASTM D412 Standard Test Methods for Vulcanized Rubber and Thermoplastic Elastomers: Tension
- GB/T 1408 Insulating Materials: Test Methods for Electric Strength
- ASTM D257 Standard Test Methods for DC Resistance or Conductance of Insulating Materials
- UL 94 Standard for Safety of Flammability of Plastic Materials for Parts in Devices and Appliances
- IPC-7525 Stencil Design Guidelines
- IPC/JEDEC J-STD-020 Moisture Sensitivity Classification for Nonhermetic Solid State Surface-Mount Devices
- JEDEC JESD22-A104 Temperature Cycling Test
- IEC 60068-2-14 Environmental Testing: Change of Temperature
- IEC 62477-2 Safety Requirements for Power Electronic Converter Systems and Equipment, Part 2: Power Electronic Converters from 1,000 V AC or 1,500 V DC up to 36 kV AC or 54 kV DC
- IEC 60664-1 Insulation Coordination for Equipment Within Low-Voltage Supply Systems: Principles, Requirements and Tests
- IEC 60112 Method for the Determination of the Proof and the Comparative Tracking Indices of Solid Insulating Materials
- IEC 60270 High-Voltage Test Techniques: Partial Discharge Measurements
- ISO 16750-4 Road Vehicles: Environmental Conditions and Testing for Electrical and Electronic Equipment
- AEC-Q100 Stress Test Qualification for Automotive-Grade Integrated Circuits
- ASTM E595 Total Mass Loss and Collected Volatile Condensable Materials from Outgassing in a Vacuum Environment
- DSC Differential Scanning Calorimetry (cure reaction enthalpy and degree of cure)
- DMA Dynamic Mechanical Analysis (modulus and glass transition)

**In this article:** Abstract · Why Room-Temperature Silicone Never Cures Deep Inside a Sealed Cavity · Latent Cure and Anti-Poisoning: Two Boundaries of a One-Component Silicone · Where It Lands: Five High-Density Thermal Interfaces · Stress Distribution at a Macroscopic Interface: Modulus, Elongation and CTE · Heat and Insulation: Two Boundaries No Single Value Can Replace · Line Integration: Stencil Printing and Dispensing on One Material · Selection Quick Reference: Work Backward from the Failure Mode · What the Cure Mechanism Delivers

# Abstract

Silicone failures in sealed cavities and large-area metal bonds rarely start with weak initial adhesion. In client failure analysis (FA), we have opened a long list of returned automotive control units, high-density servo stators and fully sealed sensors: the outer material had long since cured, the bond face was intact, yet the core near the cavity floor was still as soft as wet toothpaste and, under vibration, flowed like slurry. Conventional one-component room-temperature-vulcanizing (RTV) silicone crosslinks on ambient moisture diffusing from the surface inward. Once a thick aluminum housing, a flange seal or a dense skin closes the cavity, the water path is cut and the deep section can sit for weeks without completing cure.

SCITEO moves the driving force from ambient moisture to a controlled thermal field. A latent platinum-catalyzed, one-component addition-cure thermal silicone holds a long working life at room temperature, then cures uniformly through any depth of a sealed cavity within 30 min in a 120 °C tunnel oven (10 min at 150 °C). A multi-size spherical filler network builds a 2.5 W/(m·K) low-resistance heat path; an elastomer network of 56% elongation at break, 8.0 MPa tensile strength and Shore A 70 absorbs the CTE mismatch strain between aluminum, PCB and ceramic substrate; and 23 kV/mm dielectric strength, volume resistivity of at least 1.5×10¹⁶ Ω·cm and low-molecular cyclic siloxane (D3-D10) residue below 50 ppm meet the insulation and fog-free requirements of 800 V traction and precision optical sensors. The rheology is balanced for shear thinning and thixotropic recovery, so one material runs on both SMT stencil printing and automated precision dispensing without forcing the line to re-establish its process parameters.

## Parameter Comparison: One-Component Heat-Cure Silicone and Conventional RTV

| Parameter | SCITEO | Conventional RTV | Test Standard |
|---|---|---|---|
| Cure mechanism | 120-150 °C heat-activated (≤30 min) | Room-temperature moisture (7 days) | DSC |
| Cure in sealed cavity | Full, homogeneous cure | Deep section stays uncured | Degree-of-cure profile |
| Thermal conductivity | 2.5 W/(m·K) | 0.5-1.5 W/(m·K) | ASTM D5470 |
| Elongation at break | 56% | 20-30% | ASTM D412 |
| Tensile strength | 8.0 MPa | 2-4 MPa | ASTM D412 |
| Lap-shear after thermal shock | 5 MPa | 1-2 MPa | GB/T 7124 |
| Dielectric strength | 23 kV/mm | 15-20 kV/mm | GB/T 1408 |
| Volume resistivity | ≥1.5×10¹⁶ Ω·cm | 10¹⁴-10¹⁵ Ω·cm | ASTM D257 |
| Service temperature | −60~260 °C | −60~220 °C | IEC 60068-2-14 |

# Why Room-Temperature Silicone Never Cures Deep Inside a Sealed Cavity

One-component de-alcohol or de-oxime RTV silicone needs no oven: open the package, dispense, and ambient humidity forms the skin. Consumer electronics, white goods and open power boards have relied on this chemistry for years. SCITEO puts its R&D focus on a different class of structures. Once the product shifts to semiconductor packaging, fully sealed metal cavities, liquid-cooling plate bonding, high-power-density e-drive control units, RF communication modules, or automotive and industrial modules that must serve for years under tens of G of vibration and wide-temperature thermal shock, the physical limits of moisture cure surface all at once.

## Moisture Diffusion Stalls, and Condensation Byproducts Revert Inside the Cavity

Condensation RTV has two preconditions: water molecules in air must reach the reactive sites through the adhesive, and the methanol, ethanol or butanone-oxime released by the reaction must escape outward. In open conformal coating, the layer is only a few hundred microns thick: a skin forms in about 15 min, and moisture completes the journey within 48 h to 7 days. In a narrow deep-section pot or a large metal-flange bond, only a very narrow edge is exposed to air. The surface skins over first, and that dense polysiloxane elastomer film is itself a water barrier; diffusion into the depth falls away sharply.

Fick's law puts the advance of moisture cure against the square root of time: double the diffusion path and the core needs more than four times as long to reach the same crosslink density. Past 8-10 mm of potting depth, or when a metal lid is locked down immediately after dispensing, the interior is effectively cut off from ambient moisture. Worse, the alcohol or oxime byproducts released slowly in the depth cannot escape and stay locked inside the cavity. Once the unit runs at full load and local temperature climbs above 150 °C, residual moisture and alcohol species drive hydrolytic depolymerization of the polysiloxane backbone — the "reversion" the industry sees as silicone turning soft again — and a body that had barely formed softens and flows inside the hot sealed cavity, sometimes corroding copper busbars and solder joints.

We once cut open a reworked unit. The outer layer was a proper elastomer; the core still flowed. The root cause sits here, not in bond strength.

## Seven Days of Cure Is a Real Cost on a Lean Line

On modern automotive and industrial lines, cure time converts directly into work-in-process (WIP) inventory cost and floor space. A 48 h to 7-day RTV cure cycle forces the plant to run a large, humidity-controlled curing room stacked with semi-finished parts. Push the line to ship on takt and move a part into the next torquing, flipping or vibration-test step before the core has fully crosslinked, and the semi-fluid core creeps under gravity and assembly stress. We helped a customer trace a batch of automotive controller heat-sink fins that ran above thermal resistance: the thermal paste was not short on conductivity. The assembly had been stood upright and moved to the line after only 4 h of settling, the uncured silicone sagged by microns, the bond-line thickness (BLT) over the hot die drifted off datum, and a local void raised the thermal resistance.

## Replacing the Moisture Path: Addition-Cure Silicone

To root out deep-section undercure and sealed-cavity reversion, condensation chemistry has to go. SCITEO's one-component heat-cure thermal silicone takes the addition-cure route — platinum-catalyzed hydrosilylation — building an exceptionally stable Si-CH₂-CH₂-Si three-dimensional elastomer network.

No byproducts. The entire reaction does not depend on external water. Addition cure releases no alcohol or oxime species, so the body does not trap voids left by volatilized byproducts, and a sealed cavity never develops a locally acidic or alcoholic atmosphere.

Low cure shrinkage. Condensation systems typically shrink 1%-3%; addition systems stay under 0.5%. Alignment stability in thin-wall sensors and precision optics depends on exactly this difference.

No depth limit. Once conduction brings the whole part to target temperature, the network forms throughout the adhesive at once, and cure depth is no longer tied to a diffusion length.

# Latent Cure and Anti-Poisoning: Two Boundaries of a One-Component Silicone

Two-component addition-cure silicone can also cure through a deep section, but it needs an expensive two-component metering and mixing valve, and it carries static-mixer losses, A/B ratio drift and a pot life of tens of minutes that constrains scheduling. Turning an addition system into a one-component (1K) product is the real barrier: the same tube must hold "long, stable working life at room temperature" and "fast, complete crosslinking at temperature".

## Latent Catalyst: Balancing Working Life and Cure Speed

SCITEO builds in a composite latent inhibitor with a precise thermal dissociation threshold, locking the platinum active centers behind coordination bonds. Through cold-chain storage and 25 °C workshop dispensing, the complex stays stable, vinyl and Si-H groups do not react, and the adhesive holds a working life (pot life) of several days in an open stencil or dispense syringe; day and night shifts can hand over without repeated line flushing. When a coated or potted assembly enters a tunnel oven, a curing tunnel or a contact heater and the measured adhesive temperature crosses 110-120 °C, the inhibitor ligand releases, the platinum sites open within seconds, and crosslinking starts exponentially: at 120 °C the reaction completes within 30 min. To avoid a high-temperature cure tail from too much inhibitor, or room-temperature viscosity climb from too little, SCITEO narrows the molecular-weight distribution (MWD) of the base vinyl silicone, removing the very-low-molecular tail that drives volatilization loss and holding rheology and thermal response inside a tight tolerance band.

The balance point is set by inhibitor concentration and catalyst ratio; the base-resin molecular-weight distribution brings it inside a window acceptable to both stencil printing and precision dispensing. Narrow that band and the line has to accommodate the material: longer warm-up, slower dispensing, auxiliary heating on the stencil. Storage needs a cold chain, and the package should return to room temperature before opening to avoid condensation.

## Tack-Free Is Not Cured: Read Residual Enthalpy

The two concepts must be kept apart. A tack-free RTV surface says nothing about the interior, which can still be fluid. Degree of cure in a heat-cure system is quantified from residual reaction enthalpy by DSC, and first-article inspection (FAI) should release on residual enthalpy and a degree-of-cure profile rather than a thumb pressed into the surface. Hardness readings produce misjudgment, especially on parts with real thermal mass: the surface has hardened while the core is still below temperature.

A 120-150 °C hold of up to 30 min takes the material from liquid to a three-dimensionally crosslinked network, so parts cool and move directly into thermal-shock testing or assembly. Set against a 48 h to 7-day room-temperature cycle, WIP inventory and flow time compress to their physical limit.

## Line-Side Platinum Poisoning: Diagnose and Block It

Process engineers working with addition-cure silicone keep running into one stubborn problem: why does a local patch stay tacky after the oven, especially at the edge of a pad or a rubber seal? This is the "platinum catalyst poisoning" unique to addition-cure silicone. The vacant coordination sites of the platinum complex are readily occupied by nitrogen (N), phosphorus (P) or sulfur (S) compounds carrying lone pairs, or by heavy-metal ions such as tin (Sn) and lead (Pb), forming irreversible strong coordination bonds; a trace of contamination can permanently deactivate the catalyst.

On the electronics floor, the sources hide in three corners. First, amine or organic-acid activators in no-clean flux or rosin residue on the PCBA. Second, sulfide accelerators leaching from EPDM or NBR seals, or from latex finger cots used in cavity assembly. Third, organotin-catalyzed condensation RTV or polyurethane adhesive used in the same shop. SCITEO raises the contamination tolerance of the platinum system through bulky chelating modification, and pushes a clear line-side rule set to customers: use low-residue flux or pair plasma cleaning with deionized-water rinse around solder joints; specify peroxide-cured FKM or silicone for housing seals; and dedicate valves, stencil wipes and fixtures to addition-cure material to cut cross-contamination at the source.

# Where It Lands: Five High-Density Thermal Interfaces

Different hardware architectures place different mechanical and electrical demands on a one-component silicone; the picture only becomes clear once it lands on a real structure. The five families below are where engineering inquiries have concentrated.

## Humanoid Robot Joint Modules: Stator Potting and Winding Heat

Embodied-AI and humanoid robots drive their axes with frameless torque motors, integrating stator windings, reducers, encoders and driver boards into a very small joint volume. Newer platforms route liquid cooling into the joint and visibly suppress housing temperature, yet the path from copper in the slot to the laminate stack, and from the end winding to the housing, still depends on potting compound filling the gaps. When the thermal path is restricted, winding temperature rises, torque output sags, encoders and torque sensors drift, and whole-body motion accuracy follows.

From the material side, this is a classic motor-potting duty: little space, high heat flux, and long-term vibration.

Joint modules place three demands on a potting material. Copper-to-housing needs a continuous thermal path, and the 2.5 W/(m·K) filler network displaces the air in those gaps. Stator and magnets must be locked without applied pressure, and a low-modulus, high-elongation network lets the stress of frequent starts, stops and reversals land on the adhesive rather than the insulation system. The joint also lives in high-frequency vibration and drop impact, so the adhesive has to absorb impact energy through deformation; rigidity is not a viable answer.

## Automotive ECU, ADAS Domain Controller and Aluminum Cold-Plate Bonding and Sealing

Smart-driving domain controllers, chassis control units (ECUs) and industrial PLC modules mostly use a sandwich of "heat-generating chip/PCB + thermal interface + die-cast aluminum housing/liquid cold plate". Here the one-component heat-cure silicone often carries two jobs at once: high-conductivity gap filling on the die backside or the PCB heat-spreading copper, and structural bonding plus IP67/IP68 sealing in the aluminum flange groove.

Die-cast aluminum runs a CTE of about 23 ppm/°C, FR-4 in-plane 14-17 ppm/°C, and ceramic substrate (Al₂O₃/Si₃N₄) only 3-7 ppm/°C. Across the −40 °C cold-soak to 125 °C full-load swing, a 300 mm-class domain-controller housing moves several hundred microns relative to the board inside it. A high-modulus rigid adhesive converts that into enormous thermal shear, and the result is either a torn bond line or a cracked BGA ball or ceramic substrate. SCITEO's heat-cure silicone needs no primer: a built-in reactive silane adhesion system forms covalent bonds with anodized aluminum, etched aluminum, electrophoretic coating and FR-4. An initial 6 MPa lap-shear, measured to GB/T 7124, still holds above 5.0 MPa after 1,000 thermal-shock cycles, and the fracture is 100% cohesive rather than interfacial — the elastomer absorbs housing warpage and thermal expansion through its own deformation.

## Automotive High Voltage: BMS, On-Board Chargers and Storage PCS

As EV platforms move fully to 800 V and even 1,000 V architectures, SiC MOSFETs push switching frequency and heat flux in on-board chargers (OBC), DC-DC converters, battery management systems (BMS) and energy-storage power conversion systems (PCS) to a new level. Conventional silicone gel is soft but mechanically weak: under high vibration and high current it can tear or pump out at the interface, and ordinary silicone accelerates thermo-oxidative degradation above 200 °C in long-term service.

SCITEO lifts the long-term service ceiling of this system to 260 °C, covering the radiant heat zone around SiC power devices. On the electrical boundary, 23 kV/mm dielectric strength (GB/T 1408) and volume resistivity of at least 1.5×10¹⁶ Ω·cm (ASTM D257) hold insulation resistance and breakdown margin after 85/85 damp-heat aging. More critical is resistance to electrochemical migration (ECM) under DC high voltage: the formulation holds mobile sodium, potassium and chloride ions below 5 ppm, blocking the slow short-circuit path in which copper or silver ions grow conductive dendrites along the adhesive interface under humid DC bias. The elastomer body reaches UL 94 V-0 through a halogen-free flame-retardant package, and the qualification frame for this class is built on ISO 16750-4 at the vehicle level and AEC-Q100 at the device level, giving the high-voltage cavity a long-term flame and insulation barrier.

## MV Solid-State Transformers and High-Frequency Magnetic Components: Suppressing Partial Discharge

A solid-state transformer (SST) converts 10-13.8 kV medium-voltage AC to 800 V DC in one stage, relying on silicon carbide to push switching into the tens of kilohertz. The architecture is moving fast in DC power for AI data centers, fast-charging sites and rail traction; the core difficulty is the composite insulation and partial discharge (PD) control of a tens-of-kilohertz high-frequency transformer.

High-frequency transformer insulation is usually built by wrapping the winding in polyimide (PI) film and casting epoxy into the gaps, forming a PI-EP composite. The two materials differ in physical and chemical behavior, so the interface retains micro-voids; partial discharge (PD) initiates there, and thermal cycling opens the voids further. Engineering analyses record this path more often than power devices failing first. Raise frequency and temperature together and the path only advances faster.

Heat is the second unavoidable front. Losses in the high-frequency transformer and MV power modules concentrate in windings and core, and heat can leave only through the potting layer toward the housing; hot-spot temperature directly sets how much insulation life remains. Zoned potting is already established practice: potting the high-voltage coil assembly as a separate unit instead of casting compound and core together, so CTE mismatch does not crack the core.

On the material side, there are only three levers. First, lower the modulus so thermal cycling displacement is absorbed by the adhesive layer rather than the insulation interface. Second, keep the thermal network continuous so winding and core hot spots come down, because higher temperature lowers partial-discharge inception voltage (PDIV); heat and insulation are coupled at high voltage and high frequency. Third, control purity and mobile ions, because on the DC side the field is unidirectional and continuous, making ion migration and dendrites a more direct risk than on AC.

The quantitative gates must align as well. On the 800 V DC side, creepage and clearance follow IEC 60664-1; on the MV side, insulation coordination and safety verification follow IEC 62477-2. Housings and insulating parts commonly run a comparative tracking index (CTI) of at least 600 V, and PD-free designs target discharge below 5 pC. The potting step must also reduce residual void density in the adhesive layer. Voids are both where PD starts and a break in the thermal path, which is why vacuum deaeration and vacuum potting are not optional here.

On a fully cast high-frequency transformer, the main insulation is normally still carried by a cast epoxy system. Low-modulus silicone earns its place in power-unit, driver and auxiliary-electronics potting and in interface buffering. Vacuum casting and vacuum-assisted axial injection potting close residual voids in the epoxy layer; the silicone on the adjacent power unit handles thermal cycling displacement. Keeping those roles distinct is what prevents a program from placing its expectations in the wrong location. Insulation and safety verification for this equipment class can be framed around IEC 62477-2.

## Fully Sealed Sensors and MEMS

Sensor potting asks something different of a material than power modules do, and the conflict sits elsewhere. The sensing structures in pressure sensors, accelerometers and gyroscopes are extremely sensitive to package stress; once the modulus rises, package stress travels into the sensing beam, and zero-point drift and sensitivity loss follow. A 56% elongation paired with an elastomer network two to three orders of magnitude softer than epoxy provides stress buffering here, holding cure shrinkage and thermal expansion stress within what the sensing structure can bear. The formulation must also control low-molecular-weight siloxane volatiles and mobile ions so nothing condenses on the cold surfaces of a sealed cavity.

# Stress Distribution at a Macroscopic Interface: Modulus, Elongation and CTE

Die-level packaging follows rigid matching: high-modulus, ultra-low-CTE epoxy against micron-scale thermal strain. At that scale, the logic holds.

Expand the view to board-level assembly or system-level thermal design, and the logic changes. Displacement rises from microns to millimeters, and the material no longer needs to resist movement; it needs to accommodate it.

## Stress Equals Modulus Times Strain

Interfacial shear magnitude is set by that relation. Under thermal shock, aluminum expands by a non-negligible absolute distance; with high modulus and low elongation, that displacement converts instantly into enormous interfacial shear, and the result is either cohesive fracture or removal of the oxide layer from the substrate.

The 56% elongation of SCITEO's heat-cure elastic thermal silicone corresponds to an elastic modulus two to three orders of magnitude lower than rigid epoxy; as the aluminum moves, the adhesive absorbs the destructive strain energy through deformation, preserving both structural integrity and substrate. High elongation with 8.0 MPa tensile strength: toughness and strength are both indispensable.

## Combined Thermal Shock and Vibration

In robot servo joints, heavy-duty automotive ECUs and outdoor base stations, thermal stress and mechanical load coexist. Tens of G of high-frequency vibration plus occasional drop impact is punishing for a high-modulus adhesive: under sudden peel load it cannot yield elastically and often fractures brittlely, or tears the metal substrate before it releases.

At 56% elongation the interface has sufficient compliant travel to absorb high-frequency impact energy, while 8.0 MPa tensile strength keeps the adhesive body from failing under extreme pull. Tensile properties are measured to ASTM D412, modulus and glass transition (Tg) to DMA, and thermal cycling conditions are set from JEDEC JESD22-A104 or IEC 60068-2-14. In combined thermal-vibration testing, higher-modulus samples tend to show interfacial whitening first; the low-modulus system that absorbs displacement through its own deformation keeps a more intact interface.

# Heat and Insulation: Two Boundaries No Single Value Can Replace

In an electromechanical assembly, thermal potting compound has to carry three functions at once: adhesion, heat transfer, insulation. Of the three, heat transfer is the one most easily misled by a single number.

## Interfacial Thermal Resistance Is Not Set by Conductivity Alone

In high-power devices such as high-current drone ESC modules, 5G-A base-station power amplifiers and photovoltaic inverter power stages, accumulated heat causes throttling and eventual thermal failure. SCITEO's system uses micro- and nano-scale spherical alumina and platelet boron nitride in a densely packed hybrid filler, forming a continuous 2.5 W/(m·K) phonon path after cure (per ASTM D5470).

Conductivity, however, is only one term in thermal interface material (TIM) performance. Microscopic roughness between the heat source and the heat sink retains an air layer, and air conducts at only about 0.024 W/(m·K). If that air is not displaced, no filler network, however dense, can deliver. The adhesive fills those micro-gaps under assembly pressure, converting point contact into areal contact, and only then does conduction become real.

One phenomenon is easily overlooked: customers report that a unit runs hotter after potting. Most of the time the cause is not insufficient conductivity but entrained air, lost control of bond-line thickness, or incomplete cure. A gas bubble is close to an infinite thermal resistance, and a few large voids can sever the filler network; a bond line that rises from 100 μm to 200 μm doubles bulk resistance. Vacuum deaeration, volumetric dispensing and degree-of-cure verification carry no less weight here than material selection.

![SCITEO R&D team analysis of sealed-cavity potting process windows: bottom-point filling and a last-fill vent create a bottom-up air path, 5-20 mbar vacuum expands a 0.2 mm bubble by roughly 3.7-5.9x in diameter and lifts its effective rise speed about 20x at 10 mbar, while R≥1.5 mm internal corners, 2 mm insert overmolding and 2 mm component-to-wall clearance suppress voids](https://www.sciteo.com/images/articles/silicone-adhesive2.svg)

## Breakdown and Migration Are Different Problems

In high-voltage relay encapsulation, automotive BMS and MV-DC structures, breakdown resistance is a non-negotiable floor. Dielectric strength of 23 kV/mm with volume resistivity of at least 1.5×10¹⁶ Ω·cm maintains high-impedance insulation after long-term damp heat, and preserves breakdown margin near the 260 °C ceiling.

Another path is easily missed: mobile ions migrate along the field under humid bias and grow dendrites between closely spaced conductors. On DC there is no periodic reversal, so migration accumulates in one direction and ion purity requirements tighten. Mobile-ion control and crosslink-density design at formulation level target exactly this slow failure path.

## Tear and Impact

A cured elastic network has to strike a balance between two failure modes: no fatigue-crack growth under high-frequency vibration, no brittle fracture under accidental impact. The combination of 56% elongation and 8.0 MPa tensile strength, together with good substrate wetting and interfacial adhesion, supports structures such as large heat sinks bonded to dies and heavy-duty power modules.

## Outgassing

Outgassing is the other invisible line in sealed potting. In vacuum or at elevated temperature, volatiles released by the material condense on optical surfaces, sensing surfaces and probes; cleaning carries a high cost, and in optics or space hardware the surface is written off as a failure. The industry quantifies the risk with total mass loss (TML) and collected volatile condensable materials (CVCM) per ASTM E595, and the conventional line is TML at or below 1.0% and CVCM at or below 0.10%. For optical surfaces and vacuum cavities, SCITEO pushes its low-outgassing grades to TML below 0.3% and CVCM below 0.02%. An addition-cure system does not rely on moisture diffusion and releases no alcohol byproduct, so the real variables are residual low-molecular-weight siloxanes and degree of cure, closed out jointly by high-purity raw materials and adequate conversion control.

# Line Integration: Stencil Printing and Dispensing on One Material

However good the material, it does not reach volume if the line cannot take it. Large thermal backplanes need coating, single-dot dispensing is slow, and bond-line thickness (BLT) consistency is difficult to control.

SCITEO's one-component heat-cure system consumes almost no working time at room temperature, which widens the front-end process window, and SMT stencil printing can be used directly.

## Thixotropy and Shear Thinning

As the metal squeegee advances at a defined pressure and speed, the adhesive forms a smooth rolling bead at the leading edge. Viscosity collapses at high shear and the material fills the fine apertures; once the squeegee passes and shear disappears, viscosity recovers quickly and the printed edge holds its shape. Printable thermal interface materials usually sit in the tens of thousands to hundreds of thousands of mPa·s range, with highly filled precision-dispense grades reaching the 6×10⁵ mPa·s class; shear thinning and thixotropic recovery must match the print cycle for deposit volume to remain stable at speed. SCITEO pushes down the shear-thinning onset through filler grading, so a 6×10⁵ mPa·s material still fills the apertures under squeegee shear.

## Area Ratio and BLT

Release quality is set jointly by aperture area ratio and aperture-wall surface energy. Per the IPC-7525 stencil design guidelines, area ratio (aperture opening area to wall area) should be at least 0.66 and aspect ratio at least 1.5; below that threshold, adhesive tends to remain on the aperture walls, presenting as skip printing and low deposit volume.

BLT requires its own calculation. At 2.5 W/(m·K), a bond line increasing from 100 μm to 200 μm doubles bulk thermal resistance, and junction temperature rises with it. Thickness on a printed thermal silicone must therefore be managed to microns, not released to ordinary stencil tolerance.

SCITEO's work on base-resin molecular-weight distribution widens the printing window, so a single print can lay down hundreds of thermal pads across an industrial backplane with micron-level thickness control. After printing, place the devices and run the 120-150 °C cure oven; if the same assembly also goes through SMT reflow, confirm device moisture sensitivity per IPC/JEDEC J-STD-020 before the reflow oven.

## One Material for Printing and Dispensing

The two processes are not mutually exclusive; most lines combine them: precision dispensing for narrow gaps, blind holes and local reinforcement, stencil printing for large thermal pads and heat-spreading surfaces. One material serving both requires viscosity and thixotropy that remain stable across shear-rate regimes. Filler gradation and rheology additives are designed for exactly this, giving predictable behavior in the high-shear printing regime and the low-shear dispensing regime, and reducing re-qualification work at changeover.

# Selection Quick Reference: Work Backward from the Failure Mode

The table below compresses the mechanisms above into a checklist for design and process review:

| Application | Typical Failure Mode | Key Metrics | SCITEO Direction |
|---|---|---|---|
| Humanoid robot joint-module stator potting | Winding temperature rise, insulation aging, vibration abrasion | Thermal conductivity, elongation at break, low modulus, temperature rating | Heat-cure elastic thermal silicone |
| Industrial ECU and domain controller | Interfacial delamination, shear decay after thermal shock | Post-shock shear strength, CTE match | Heat-cure elastic thermal silicone |
| High-voltage BMS, OBC and storage PCS | Breakdown, electrochemical migration, damp-heat aging | Dielectric strength, volume resistivity, mobile ions | High-voltage insulating thermal potting system |
| Solid-state transformer and MV-DC power unit | Partial discharge in the potting layer, interface micro-gaps, hot spot | Low modulus with high elongation, dielectric strength, low outgassing | Heat-cure low-stress insulating potting system |
| Fully sealed sensor | Deep-section undercure, stress cracking, outgassing contamination | Full cure, low modulus, TML/CVCM | Heat-cure low-stress potting system |
| Large-area thermal backplane coating | Skip printing, stringing, uneven BLT | Thixotropy, area ratio, BLT consistency | Stencil-printable thermal silicone |

# What the Cure Mechanism Delivers

The choice of cure mechanism is fundamentally a choice of controllability. Room-temperature cure hands control to ambient humidity and structural geometry; heat cure takes it back onto a temperature profile, and the deep-section problem inside a sealed structure disappears with it. SCITEO builds a modulus lower than epoxy and high elongation into the formulation as baseline characteristics, so macroscopic CTE mismatch is absorbed by the adhesive layer; the thermal network stays continuous, and hot spots remain under control. The material is compatible with stencil printing, so the line does not have to re-qualify at changeover.

This article is SCITEO Advanced Materials original technical content; unauthorized reproduction is prohibited.

## Appendix: Process & Engineering Adhesive FAQ Index

### Why does room-temperature-vulcanizing (RTV) silicone stay uncured deep inside a sealed cavity or a large metal sandwich?

Condensation-cure RTV relies on moisture diffusion to crosslink. In an open environment the edge skins over first and forms a dense polymer barrier, after which inward diffusion is restricted; cure depth scales roughly with the square root of time, so a bond line twice as thick needs several times longer for the core to reach the same degree of cure. Once the potting volume is enclosed by a metal housing, the moisture supply itself is interrupted, and a soft core after several weeks is no surprise. This problem cannot be settled by surface hardness; open the part and inspect the degree-of-cure profile, or measure residual reaction enthalpy by DSC.

### How does the latent catalyst in a one-component heat-cure silicone trigger at 120 °C without reacting during cold storage?

The system uses platinum-catalyzed hydrosilylation, with an inhibitor added to occupy the platinum active sites temporarily. At room temperature the inhibitor is stable and the chains do not react, which establishes both working life and storage stability. As the adhesive temperature crosses 110-120 °C the inhibitor releases, the catalyst starts working, and crosslinking completes within 30 min at 120 °C. The formulation difficulty lies in the balance point between working life and cure speed; SCITEO adjusts inhibitor concentration, catalyst ratio and base-resin molecular-weight distribution together so that point falls inside a window acceptable to both stencil printing and precision dispensing.

### For stator potting in a humanoid robot joint module, why look at elongation and modulus rather than bond strength alone?

Joint modules rarely fail by static pull-off; they fail through winding temperature rise, high-frequency vibration and the stress cycling produced by frequent starts and stops. Stress equals modulus times strain, so a high-modulus adhesive converts displacement directly into interfacial shear during thermal cycling and impact, and the load ultimately lands on the insulation system and magnet positioning. A low-modulus, high-elongation network absorbs strain energy through its own deformation, and the stress peak falls accordingly. Review thermal conductivity, elongation at break, modulus, temperature range and post-shock shear retention as a set; that comes closer to real service conditions than any single strength value.

### How does a 2.5 W/(m·K) thermal silicone lower interfacial thermal resistance, and why must the air layer be displaced first?

Interfacial thermal resistance has two components: bulk resistance through the adhesive, and resistance at the two contact interfaces. Microscopic roughness always remains between the device and the heat sink, and the air trapped in those recesses conducts at only about 0.024 W/(m·K), forming an efficient thermal insulator. The adhesive fills those micro-gaps under assembly pressure, converting point contact into areal contact, and only then does the 2.5 W/(m·K) filler network have a continuous phonon path. When verifying to ASTM D5470, lock the pressure and bond-line thickness; change either variable and the measured conductivity drifts with it.

### A unit runs hotter after potting. Which part of the adhesive system is actually responsible?

Do not rush to a higher-conductivity grade. Check three things in order: whether the layer contains entrained air, whether bond-line thickness is out of tolerance, and whether the degree of cure is sufficient. A gas bubble is close to an infinite thermal resistance, and a few large voids can sever a 2.5 W/(m·K) filler network; a bond line rising from 100 μm to 200 μm doubles the bulk thermal resistance; and incomplete cure means contact pressure between filler particles never develops, leaving the phonon path broken. Vacuum deaeration, volumetric dispensing and first-article DSC release come before any discussion of material selection.

### In large-area stencil printing of thermal silicone, how do you suppress skip printing, stringing and uneven bond-line thickness?

Skip printing usually originates in one of two mismatches. The first is squeegee speed against the adhesive's shear-thinning rate: run too fast and the material has not thinned sufficiently to fill the aperture. The second is insufficient area ratio at release, or excessive aperture-wall surface energy, which leaves adhesive on the walls. In practice, hold squeegee speed at 15-30 mm/s, maintain a uniform rolling bead 1-2 cm in diameter ahead of the blade, clean the stencil underside with lint-free cloth on a schedule, and design apertures to an area ratio of at least 0.66 per IPC-7525. SCITEO's work on base-resin molecular-weight distribution mainly widens the adjustable range of these parameters, so the line does not have to run against the process boundary.

### For medium-voltage equipment such as solid-state transformers, what is the most overlooked potting risk?

Partial discharge (PD). High-frequency transformers commonly wrap the winding in polyimide film and cast epoxy into the gaps, forming a PI-EP composite whose interface tends to retain micro-voids, and PD initiates there. Thermal cycling then opens the voids further, and engineering analyses record this path more often than power devices failing first. The material response is to lower modulus so thermal cycling displacement is absorbed by the adhesive layer rather than the insulation interface, while a continuous thermal network lowers hot-spot temperature and restores partial-discharge inception voltage (PDIV). On the 800 V DC side, creepage and clearance follow IEC 60664-1; on the MV side, insulation coordination and safety verification follow IEC 62477-2; PD-free designs target discharge below 5 pC.

### A local patch of addition-cure silicone stays tacky after the oven. Is it platinum poisoning or undercure?

Start with location and a cross-section. Poisoning concentrates at edges touching a pad, a rubber seal or cleaning residue and stays local, while areas away from the contamination cure normally; undercure follows thermal mass, loading or the tunnel profile and shows up as a broad or core-side shortfall. Cut the part and measure DSC residual reaction enthalpy: a high residual with an uncrosslinked edge points to poisoning, while a uniformly high residual points to an under-temperature core. Work the contamination list first (amine flux, sulfur-bearing cleaners and gloves, organotin materials), then rule out surface contamination with plasma cleaning and a deionized-water rinse; adjust catalyst or extend cure only after those are closed.

### How do heat-cure silicone, thermal epoxy, thermal gel, grease and pads divide the work at selection?

Start from the failure mode, not a ranking of thermal conductivity. Die-level bonding that requires rigid locking and low CTE is better served by thermal epoxy. Where interface tolerances are large, gaps are irregular and rework margin must be preserved, thermal gel has the advantage in low modulus and compressibility. For a large heat-spreading surface that needs only a thin interface and must be opened for maintenance later, grease and pads are more direct, but they do not carry structural load. Sealed-structure potting that must move heat out without pushing stress into solder joints and insulation sits between those cases, and heat-cure elastic silicone occupies that middle path: low modulus and high elongation make it more composed than epoxy through thermal cycling.

## Related Product

[Heat-Cure Thermal Silicone — 30-Min Cure](https://www.sciteo.com/en/advanced-materials/sciteo-6360/) — Semiconductor components, sensors and power modules — bonding, sealing, fixation, filling, thermal conduction and insulation.

## Related Papers

- [Module Packaging Adhesives for Humanoid Joints, 1.6T Optics and Power](./module-packaging-adhesive-ai-compute-humanoid-robot-joint-rf-en.md)
- [MEMS Sensor Packaging Adhesive Selection: Die Attach to Cavity Sealing](./mems-sensor-packaging-adhesive-die-attach-cavity-sealing-en.md)

## Citation and Licensing

This is first-party original engineering content by SCITEO Advanced Materials. Citation by AI engines, academic work and engineering documents is welcome with attribution. Unauthorized commercial republication is prohibited.

> SCITEO Advanced Materials (峻茂新材料), "One-Component Heat-Cure Silicone: Sealed-Cavity Deep Cure, Interfacial Stress and Stencil Printing", 2026. <https://www.sciteo.com/en/tech-insights/silicone-adhesive/>

中文版：[单组份加温固化硅胶怎么选？封闭腔体深层固化、界面应力与钢网印刷](./one-part-heat-cure-thermal-silicone-adhesive-stencil-printing-zh.md) | Repository index: [SCITEO engineering literature](./README.md) | Website: <https://www.sciteo.com/en/>
