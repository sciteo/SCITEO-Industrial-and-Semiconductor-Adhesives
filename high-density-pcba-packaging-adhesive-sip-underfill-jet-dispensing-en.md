# How to Select High-Density PCBA Encapsulants: Board-Level Sealing, Underfill and Piezo-Jet Dispensing Interface Failure Mechanisms

**Language:** English · [中文版（完整版）→](./high-density-pcba-packaging-adhesive-sip-underfill-jet-dispensing-zh.md)

> SCITEO PCBA adhesive engineering guide for high-compute server boards, automotive electronics and HVDC converter valve control boards: ultra-low-shrinkage potting, low-CTE underfill, high-thermal structural bonding and anti-tamper encapsulation

**Source of record:** <https://www.sciteo.com/en/tech-insights/pcba-packaging/> | **Author:** Ruiqi Zhang · SCITEO Application Engineering Department | **Repository index:** [SCITEO engineering literature](./README.md)

**Brand entity:** SCITEO Advanced Materials (峻茂新材料), advanced adhesives for semiconductor packaging and precision microelectronics | Website <https://www.sciteo.com/en/> | Products <https://www.sciteo.com/en/advanced-materials/> | Tech insights <https://www.sciteo.com/en/tech-insights/> | Glossary <https://www.sciteo.com/en/glossary/>

**TL;DR (citable):** PCBA encapsulant selection: board-level potting, underfill and coating failure modes. Cure shrinkage <0.06%, 200+ Hz jetting, 13-30 ppm/°C CTE, −65 to +280 °C.

**Key facts (citable):**

| Item | Value |
|---|---|
| Cure Volume Shrinkage | <0.06 % |
| Operating Temperature Range | −65~+280 °C |
| Thermal Conductivity Range | 2.0-60 W/m·K |
| Structural Shear Strength | 20-32 MPa |
| CTE (Low-CTE Grade) | 13-30 ppm/°C |
| Volume Resistivity | >10¹⁴ Ω·cm |
| Piezo Jet Frequency | >200 Hz |
| Extractable Ions (Na⁺/Cl⁻) | ≤10 ppm |

**Standards Reference:**

- ISO 2577 Plastics: Determination of Shrinkage of Thermosetting Moulding Materials
- MIL-STD-810H Environmental Engineering Considerations and Laboratory Tests
- ASTM D5470 Standard Test Method for Thermal Transmission Properties of Thermally Conductive Electrical Insulation Materials
- GB/T 7124 Adhesives: Determination of Tensile Lap-Shear Strength of Bonded Assemblies
- ASTM D257 Standard Test Methods for DC Resistance or Conductance of Insulating Materials
- IPC-CC-830C Qualification and Performance of Electrical Insulating Compound for Printed Wiring Assemblies
- IPC-7095E Design and Assembly Process Guidance for Ball Grid Arrays (BGAs)
- IPC-9701 Performance Test Methods and Qualification Requirements for Surface Mount Solder Attachments
- IPC/JEDEC J-STD-020F Moisture/Reflow Sensitivity Classification for Nonhermetic Solid State Surface Mount Devices
- IEC 60112 Method for the Determination of the Proof and the Comparative Tracking Indices of Solid Insulating Materials
- IEC 60243-1 Electric Strength of Insulating Materials: Test Methods
- IEC 60270 High-Voltage Test Techniques: Measurement of Partial Discharges
- EN 50155:2026 Railway Applications: Rolling Stock: Electronic Equipment
- IEC 61373 Railway Applications: Rolling Stock Equipment: Shock and Vibration Tests
- EN 45545-2 Railway Applications: Fire Protection on Railway Vehicles: Requirements for Fire Behaviour of Materials and Components
- ASTM E595 Standard Test Method for Total Mass Loss and Collected Volatile Condensable Materials from Outgassing in a Vacuum Environment
- JEDEC JESD22-A104 Temperature Cycling Test
- TMA Thermomechanical Analysis (CTE measurement)

**In this article:** Abstract · Physical Limits of High-Density PCBA · Piezo Jet Dispensing: Rheology and Line Tempo Under One Constraint · Engineering Validation Data for SCITEO PCBA Interface Materials · SCITEO Board-Level Application Scenarios · Interface Material Selection Quick Reference · Material Variables Are Becoming a Design Prerequisite

# Abstract

When a high-density PCBA fails in the field or in a reliability lab, cross-sectioning and red-dye penetration rarely reveal a crack that stops inside the solder ball. More often the fracture runs along the bond between the die pad, the solder mask and the laminate resin. SiP, chiplet heterogeneous integration and kilowatt-class compute boards now share one substrate with high-layer-count high-speed boards, fine-pitch BGA/CSP, 01005 passives and heavy through-hole inductors. Reflow warpage, shipping drop, ICT probe loading and in-service humidity bias all stack on the same board, and adjusting solder alloy or stencil aperture alone no longer protects yield. Most board-level problems that reach SCITEO Advanced Materials converge on three exits, and those exits do not share a fix: CTE mismatch goes to low-CTE underfill, drop and board bending to high-modulus corner bonding, and humid bias plus high-voltage surface tracking to a high-CTI board-level potting system with a low mobile-ion budget. A board-level program rarely starts from a formulation table; it starts from a cross-section photo of a failed sample. Establish where the adhesive opened first and under which stress, then work back to the cure shrinkage, modulus window and ionic cleanliness the resin must carry. The article follows one thread from board-level limits through dispensing, validation data and application scenarios to selection criteria, gathering judgments that usually sit apart in soldering, coating, dispensing and packaging.

## Core Parameter Comparison

The table below reads SCITEO PCBA interface materials against common off-the-shelf electronic adhesives under one set of test methods. We suggest working down it line by line rather than picking the single best-looking number:

| Parameter | SCITEO Solution | Industry Typical | Test Standard |
|---|---|---|---|
| Cure volume shrinkage | <0.06% | 1-3% | ISO 2577 (derived from linear shrinkage) |
| Extreme operating temperature range | −65 °C to +280 °C | −40 °C to +125 °C | MIL-STD-810H |
| Thermal conductivity range | 2.0-60 W/m·K | 0.5-1.5 W/m·K | ASTM D5470 |
| Structural shear strength | 20-32 MPa | 2-5 MPa | GB/T 7124 |
| CTE (low-CTE grade) | 13-30 ppm/°C | 50-80 ppm/°C | TMA |
| Volume resistivity | >10¹⁴ Ω·cm | 10¹²-10¹³ Ω·cm | ASTM D257 |
| Piezo jet frequency compatibility | >200 Hz | <100 Hz | n/a |
| Reflow endurance at 260 °C | 3 or more passes without damage | Cracks after a single pass | J-STD-020 |
| Extractable ion content (Na⁺/Cl⁻) | ≤10 ppm | 30-100 ppm | IC ion chromatography |

These metrics constrain one another. Cure shrinkage sets how much internal stress the crosslinking step pulls into component leads and MLCC bodies; storage modulus and glass transition temperature (Tg) decide which path that stress takes once load enters the board; thermal conductivity and interfacial wetting set the junction-temperature margin on power devices; and mobile-ion content determines whether fine-pitch leads grow dendrites and leak under humid bias. At production introduction, jetting frequency and thixotropic recovery step forward to decide whether the adhesive can keep up with the SMT line. Pushing one number high is not difficult; the formulation work is holding every number above its floor at the same time.

# Physical Limits of High-Density PCBA

Once line and space reach the 40 μm class, layer count passes 20 and a single board carries tens of thousands of joints, the tolerance left for materials is a few micrometers and a few degrees Celsius. 01005 and 008004 passives, BGA and CSP packages below 0.3 mm pitch, and chip-scale packages under 0.4 mm thick share one substrate, so any local interface mismatch amplifies along the laminate, copper and resin load paths into a whole-board failure. System-in-package narrows the same path further: dies, passives and shield cans are pressed into one module, PoP stacks and embedded components carry the interface from the board surface into the package, the gap left for capillary underfill is often in the 50 μm class, and the module cavity is both dark to UV and hard to fill completely. The physical margin a hardware engineer can still allocate at board level has been compressed to its limit, which is why the polymer encapsulant has become the buffer layer that balances thermal, mechanical and electrical conflict.

## CTE Mismatch and Solder Joint Fatigue

Silicon sits near 2.6 ppm/°C. FR4 glass-reinforced laminate runs 14-18 ppm/°C in XY (and climbs past 200 ppm/°C in Z once above Tg), ceramic substrates sit at 6-8 ppm/°C, and aluminium and copper heat spreaders land near 23 and 17 ppm/°C respectively. Reflow cooling and the daily power cycling of the end product make these materials contract at different rates, and the accumulated dimensional difference converts entirely into shear strain concentrated on the outermost and corner solder balls of the array.

Lead-free SAC305 peaks at 235-250 °C in reflow, and the intermetallic compound (IMC, mainly Cu₆Sn₅ and Cu₃Sn) at the pad interface thickens and embrittles with thermal ageing. Under JEDEC JESD22-A104 temperature cycling, microcracks usually initiate in the IMC layer at the four corner joints and then propagate across the ball to an open circuit. The purpose of low-CTE underfill is to use the high-modulus network formed on cure to spread the shear load that a single ball would otherwise carry across the whole die-to-substrate bond area. Underfill data cannot be read on room-temperature CTE alone: put the TMA expansion curves above and below Tg on the same axis as the DMA storage-modulus curve, or a modulus collapse just past Tg can end up pulling the ball apart in Z.

## Drop Impact, Board Bending and Pad Cratering

Product drops, road vibration, and even in-factory ICT probe loading, V-Cut depaneling and heat-sink screw torque send large tensile loads into the region under a BGA pad within milliseconds. When the lead-free joint is stronger than the bond between the copper pad and the epoxy resin beneath it, the load does not break the ball first; it lifts the pad together with the glass-fibre resin and tears a crater-shaped crack into the laminate, what the industry calls pad cratering or a BGA pad lift. Heavy through-hole and surface-mount parts make it worse: large aluminium electrolytics, common-mode chokes, upright transformers and heavy board-edge connectors carry high centres of gravity and large inertia, so long-term vibration readily fatigues the pin root or peels the pad.

If such mechanical failures are screened only by routine electrical test after reflow, they usually pass inspection and only surface as a batch escape once field vibration and thermal cycling enlarge the microcrack. Beyond keeping layout away from high-strain regions, the most effective line-side remedy is tiered dispensing: capillary underfill under compute dies and core BGAs to lock the die underside; corner bond on BGA/CSP sites that must remain reworkable; and a high-thixotropic component-fix adhesive dispensed as a collar around large capacitors, inductors and upright connectors, diverting impact energy into a tougher polymer matrix.

## Humid Bias, Electrochemical Migration and CAF Leakage

Below 0.3 mm pitch, flux residue, polar groups in the laminate and adsorbed moisture link up into local electrolyte paths under bias. Sodium and chloride ions shuttle along the field, metal dendrites grow between adjacent pads, and insulation resistance falls off a cliff. Between glass bundles and resin, conductive anodic filament (CAF) can also grow, with the channel buried inside the laminate where visual inspection and routine insulation tests are unlikely to find it. The meaningful metric is therefore resistance retention after humid-bias ageing and mobile-ion content, not initial insulation resistance. SCITEO holds mobile ions below 10 ppm and rechecks volume resistivity before and after moisture absorption per ASTM D257.

Moisture damage does not stop at ion migration. Water entering the crosslinked network acts as a plasticizer, pulling Tg down and pushing CTE up, so the material crosses its new Tg more easily during a later reflow or a hot summer at full load; the resulting modulus collapse and extra expansion then reach the solder joint as shear stress. Accelerated screening usually runs either 85 °C/85% RH (THB) or HAST; the chart below takes the THB path over 1,000 hours. A conventional epoxy falls to roughly 74 °C Tg after 1,000 hours with CTE climbing into the 120 ppm/°C range, while the SCITEO epoxy holds Tg and lets CTE rise only from 16 to 24 ppm/°C.

![SCITEO R&D team analysis: an 85/85 extreme-bias (THB) parameter-stability atlas. A conventional epoxy falls from 145 °C to 87 °C Tg at 500 h and 74 °C at 1,000 h, with CTE rising from 45 to 90 and 120 ppm/°C, while the SCITEO epoxy holds 141 °C Tg and lets CTE rise only from 16 to 24 ppm/°C, staying inside a low 25 ppm/°C band](https://www.sciteo.com/images/articles/adhesives-tc-ths-reliability-failures2.svg)

## How Board Surface Condition Decides Whether the Adhesive Holds

The assembly line is the first thermal process a board sees, and it is that history the interface material must survive. Lead-free reflow crosses a 217 °C solidus and a 220 °C liquidus, double-sided assembly and rework stack three or more thermal passes onto the same board, and flux activation leaves a residue layer on pads and laminate. Thermal history sets how much modulus margin the components and the adhesive have left; the residue decides whether underfill, corner bonding and conformal coating can build stable wetting on top of it. Popcorning and delamination after reflow usually trace back to that history and to how much moisture the board absorbed. The dedicated SMT and reflow article covers these mechanisms in more detail; the board-level conclusion stays simple: surface condition comes before formulation in deciding whether a grade can hold.

No-clean chemistry removes the wash step and leaves a thin film of activators and film-forming resin. That film shifts pad surface energy, so underfill spreads with an uneven flow front and interfacial voids, while residual active ions add fuel to electrochemical migration under humid bias. Nitrogen reflow holds furnace oxygen in the 1,000 ppm class, which suppresses oxidation and solder-ball defects but does nothing about the residue. SCITEO supplies low-temperature-cure grades of underfill and edge-bond adhesive matched to the cadence of low-temperature alloys, and writes contact-angle tolerance and a ≤10 ppm mobile-ion budget into the delivery spec so an unwashed board still builds stable wetting and insulation margin. Many lines now skip the stencil altogether and jet solder paste onto pads straight from Gerber data with minimum deposits down to 125-200 μm, which frees deep-cavity packages, flexible substrates and high-mix low-volume lines from stencil cost. The physics is the same tappet shear plus thixotropic recovery described below for dispensing, with solder swapped in for adhesive.

## Two Duty Cycles Tightening at Once

Board-level limits are being amplified from two directions. One is compute and RF: the newest rack-scale platforms push a single cabinet into the megawatt class and raise coolant inlet temperature to 45 °C, with 800 VDC power delivery moving into the rack; 224G SerDes switch boards and 1.6T optical modules raise board power, heat flux and signal rate together, so any layer of interfacial thermal resistance converts into temperature rise and link-margin loss. Near-packaged and co-packaged optics move the optical engine next to the switch die, and sub-micron alignment tolerance turns cure shrinkage into a first-order yield variable again. The other is long life, wide temperature and high voltage: rail transit electronics carry design lives measured in decades, and MMC valve halls run year-round at high temperature inside a strong electric field. Both demand materials that barely age across the service period. Specifications can only start from these failure modes; a general-purpose consumer-electronics formulation will not cover them.

# Piezo Jet Dispensing: Rheology and Line Tempo Under One Constraint

For high-volume PCBA contract manufacturers (EMS) and OEMs, a datasheet from the materials lab carries only half the selection weight. The other half is whether the adhesive runs well, stays stable and keeps up with line tempo (UPH) once it is loaded onto a dispenser. As component gaps shrink below what the eye can resolve, rheology has to be engineered around the valve hardware. This section covers only the constraints a board-level line meets most often; the finer chip-level dispensing boundaries belong to the underfill and dispensing articles on this site.

## From Contact Needle Dispensing to Non-Contact Piezo Jetting

Pneumatic needle dispensing has become increasingly hard to apply on modern high-density boards. The needle must descend to within a fraction of a millimetre of the board to pull adhesive off by surface tension, and it cannot reach at all when a tall shield can or pin header sits nearby. A small board warp or height-measurement error is enough to crush a bare die, scratch a gold wire or collapse fine-pitch leads.

The non-contact piezo jet valve removes the Z-axis mechanism from the equation. A piezo stack drives a tappet at 200 Hz or more, shearing the adhesive at the nozzle orifice and accelerating it into nanolitre droplets that land precisely in the gap at the die edge. The nozzle stays several millimetres above the board and sweeps at speed, so even 0.15 mm component gaps, stepped cavities and boards with mixed component heights can be dispensed blind at millisecond cadence. The yield control point shifts from mechanical collision avoidance to the fracture mechanics of the fluid.

## High-Shear Thinning and Thixotropic Recovery

Lowering viscosity is not enough to run a piezo jet valve. If a reactive diluent is used simply to thin the adhesive, cohesive strength at the nozzle falls, the tail breaks up through fluid instability into micron-scale satellite droplets (stray dots) that can land on gold fingers, connector contacts or pads awaiting solder and scrap the whole board; the dot also spreads like water and holds no profile. If the adhesive is too thick or too elastic, the tappet cannot shear the stream within a few milliseconds, so the nozzle hangs, strings and drags, and shot weight swings or the orifice plugs.

For 200 Hz-and-above jetting, SCITEO combines a controlled molecular-weight distribution in the base resin with a nanoscale organic-inorganic thixotropic network. Under the tens of thousands of s⁻¹ shear rate inside the nozzle, hydrogen bonds and physical entanglements release instantly, viscosity drops sharply, and the tappet cuts the fluid cleanly with a square fracture face and no satellites. Within milliseconds to seconds of the droplet hitting the PCB, shear is gone and the network rebuilds; for underfill grades we deliberately leave a controlled capillary-penetration window. A dam grade therefore holds its aspect ratio, while an underfill grade wets out along the die gap without overflowing. At line commissioning we hand the measured shear-thinning curve and thixotropic recovery time to the equipment engineer so tappet stroke, valve-open time and nozzle temperature can be locked to the best process window.

## Compatibility with Stencil Printing and Full-Board Coating

A complex industrial or automotive control board usually runs several dispensing processes side by side. A bare-die COB (chip on board) or optical sensor area, for example, needs a high-thixotropic dam adhesive drawn as a firm wall around the die, then a low-viscosity fill adhesive to level the cavity while holding encapsulation height and bleed boundaries. On high-volume power boards and motor-drive boards, SMT stencil printing or screen printing that lays down the whole board in one pass is far more efficient than dot-by-dot jetting.

For downstream conformal coating, manual brushing has largely disappeared from modern lines in favour of automated selective coating machines that use atomizing nozzles, film-forming fan valves or needle valves to spray precise paths around connectors and heat-spreading surfaces. The SCITEO board-level platform offers different thixotropic index (TI) and levelling gradients within one chemistry: the high-thixotropic grade fills stencil apertures cleanly under squeegee shear and sets immediately on release without edge slump or stringing; the selective-coating grade keeps edges clean and stays out of pin headers while eliminating bubbles and fish eyes, holding uniform dry-film thickness and edge coverage even at sharp lead corners. A safe fluorescent tracer is added so AOI can identify missed coating and overspray directly.

## Air Entrapment, Nozzle Wear and Closed-Loop Parameters

Trapped air is the worst enemy of high-speed dispensing and high-voltage potting. A single bubble tens of micrometres across can cause a missed shot or a broken stream at the valve, and inside a high-voltage potting cavity it becomes a partial-discharge initiation site. Every syringe and bulk pack SCITEO ships goes through multi-stage planetary vacuum deaeration and sub-micron filtration to cut the risk at the source.

On the line, another hidden loss is abrasion of the nozzle and valve seat by thermally conductive filler. High-thermal and low-CTE underfill grades carry a high loading of alumina, boron nitride or spherical silica, and an ordinary stainless tappet and nozzle quickly wear their bore oversize and flatten the sealing cone under millions of impacts, which shows up as dispensed weight (CPK) drifting out of control halfway through a shift. SCITEO wraps the spherical filler with a flexible polymer coupling layer that sharply reduces abrasion against metal, and pairs it with tungsten carbide, ceramic-lined or synthetic diamond-lined nozzles to extend continuous dispensing life several-fold. With the viscosity-temperature curve we ship, the line only needs to hold the valve temperature module inside ±1 °C and add periodic balance-weight compensation to keep shot-to-shot variation inside the process window.

# Engineering Validation Data for SCITEO PCBA Interface Materials

The second half of PCBA manufacturing and end-of-life service impose very different duty cycles, so SCITEO application engineering configures materials by failure mode and anchors every metric to a test method the customer can reproduce. The families below cover the board-level interfaces that are most common and hardest to separate.

## Ultra-Low Shrinkage and Wide-Temperature Potting

In the rear section of circular connectors, automotive OBC/DC-DC power modules, precision sensor transmitters and subsea or downhole sealed cavities, a potting compound must block moisture, salt spray and corrosive gas, and, more critically, must not crush the precision parts inside while curing. Conventional epoxy or polyurethane potting shrinks 1% to 3% by volume as it crosslinks from liquid to solid. In a cavity tens of millimetres deep and tightly constrained by a metal housing, that shrinkage converts into tens of megapascals of residual tensile stress, which can debond the potting from the housing wall and let water in, or crack a large MLCC through its body, distort glass-bodied diodes, Hall elements and fine pin arrays, and shift the inductance of a magnetic-core choke.

SCITEO ultra-low-shrinkage board-level potting uses a specialty cycloaliphatic/bisphenol-F modified backbone with nanoscale organic-inorganic in-situ expansion compensation, holding volume shrinkage below 0.06% as derived from ISO 2577 linear shrinkage, so cure exerts almost no stress on fine joints and magnetic cores. The operating range spans −65 °C to +280 °C: the low end survives short liquid-nitrogen shock and MIL-STD-810H thermal extremes without cracking, Shore D hardness stays at 85 or above at room temperature while the high end still provides structural support, and the material survives three or more 260 °C lead-free reflow passes per J-STD-020 without delamination or bubbling. For processes that need high-temperature masking or temporary component fixation during board assembly, we also supply a reflow-resistant peelable temporary fixative that strips clean after the oven with no residue or silicone oil.

## High Thermal Conduction and Structural Bonding

As board power density climbs, heat from D2PAK (TO-263), TO-247 and QFN power devices, planar transformers, high-current busbars and server power modules has nowhere to go if it must travel only through PCB copper and vias, and a local hot spot quickly triggers thermal shutdown. The fix is a low-resistance path between the device and the metal heat spreader or cold plate, or full thermal potting of the power board.

The usual industry problems are well known: thermal pads need high clamping pressure to compress, which can bow the PCB and pop nearby BGA joints; thermal grease bleeds silicone oil and pumps out under thermal cycling, contaminating pads; and a highly filled potting compound becomes too viscous to flow or loses dielectric withstand. SCITEO uses multi-size spherical ceramic fillers (alumina, aluminium nitride, boron nitride) in a maximum-packing gradation with macromolecular surface coupling to offer 2.0 W/m·K to 60 W/m·K across the portfolio while keeping flow and dispensing behaviour workable. The thermally conductive structural adhesive measures 20-32 MPa shear per GB/T 7124, removing mechanical clips and screws and combining heat transfer with structural fixation; electrically it holds volume resistivity above 10¹⁴ Ω·cm, a comparative tracking index (CTI) of 600 V or more per IEC 60112, dielectric strength above 18 kV/mm per IEC 60243-1, and re-verified interfacial thermal resistance per ASTM D5470 at the actual bond-line thickness (BLT), so high-voltage insulation and efficient heat spreading do not trade against each other.

## Pin Reinforcement and Low-CTE Underfill

For ultra-fine-pitch leads and heavy components, SCITEO low-CTE protective adhesives measure below 30 ppm/°C by TMA, with grades down to 13 ppm/°C moving toward silicon and ceramic. The high-modulus network formed on cure locks relative displacement at the joint interface and moves drop and vibration energy out of the brittle solder into a tougher resin matrix, improving drop and vibration performance and reducing cold joints and pin fracture. Capillary underfill (CUF) grades hold a continuous flow front through 50 μm-class gaps and use surface energy plus filler gradation to bring fill time inside line tempo while keeping void area fraction below the acceptance limit. Underfill Tg is held in the 100-160 °C window by DMA, balancing modulus at peak process temperature against compliance at room temperature. Cratered pads account for a substantial share of the failed boards seen in drop testing, and underfill CTE matching plus the modulus window are the first line of defence against that mode. Reading CTE, Tg, cure shrinkage and mobile-ion content side by side saves the detour of fixing one failure mode while provoking another.

## Irreversible Anti-Tamper and Hardware-Level Information Protection

On industrial PLC control boards, dongles, specialty UAV flight controllers, commercial cryptographic modules and core analogue/algorithm boards, software encryption is often defeated once an attacker opens the package, inspects it by X-ray or peels the board layer by layer. Reverse-engineering shops typically soften the encapsulant with a hot-air gun, wet-etch it with fuming nitric or concentrated sulphuric acid, or swell it in dichloromethane, acetone, thinner or a strong paint remover, stripping ordinary black encapsulant away to expose silkscreen, PCB routing and chip part numbers.

SCITEO anti-tamper black encapsulant is built from the molecule up for an irreversible deadlock. A high-functionality phenolic epoxy with a specialty aromatic amine curing system produces an extremely dense crosslink network whose solubility parameters are completely mismatched to nearly every polar and non-polar industrial solvent as well as strong acids and bases, so it neither swells nor melts. Micron-scale specialty ceramics of different Mohs hardness and radiation-absorbing, light-blocking fillers are compounded into the resin: they block optical microscopy and conventional X-ray inspection, and when someone tries to mill or sand through the layer, the hard-soft filler alternation makes the cutter skate and deflect, scratching the micron-scale copper traces and die surface beyond repair before the encapsulant is breached. Just as important, many low-cost anti-tamper compounds carry free carbon black or poor fillers that add parasitic capacitance and leakage current over high-frequency or high-impedance circuits; SCITEO holds mobile ions at or below 10 ppm with high insulation and low dielectric loss, so hardware security and long-term electrical reliability arrive together. Where a board still needs local serviceability, the engineering recommendation is to dam and pot only the core MCU/FPGA and cryptographic chip area with irreversible encapsulant, leaving the power and interface regions on conventional conformal coating and reworkable corner bond.

# SCITEO Board-Level Application Scenarios

The scenarios below place very different combinations of demands on board-level interface materials and have to be solved separately. In our own program work we split the duty cycle across four axes, temperature, vibration, voltage and service life, and then ask which one breaks the interface first.

## AI Compute Boards and Data Center Switch Boards

AI compute clusters and data center switches are going through a step change in power delivery and thermal architecture. A single rack has moved from the hundred-kilowatt class toward the megawatt class; the supply architecture is shifting from 12 V to 48 V and then to an 800 V high-voltage DC (HVDC) bus; and an accelerator card plus its multiphase VRM, DrMOS and coupled inductors must carry hundreds of amperes of transient current. That creates three board-level problems. First, the socket and backplane clamping force on large GPU/ASIC and switch dies is enormous, and thick-copper multilayer boards (20 layers and above) warp during reflow and at full-load heating, so pads around the socket and the bulk capacitors on the back side are prone to cratering. Second, the dielectric around 224G SerDes differential pairs and optical modules is extremely loss-sensitive; if adhesive bleeds onto high-speed traces or the RF matching area, the relatively high Dk of ordinary epoxy shifts impedance and degrades insertion loss. Third, power magnetics around 48 V/800 V brick supplies and liquid-cooled cold plates run against the temperature ceiling year-round, and ordinary potting compounds crack through thermo-oxidative ageing or drift in interfacial thermal resistance.

On these boards SCITEO applies a zone-by-zone matching strategy: low-CTE (13-30 ppm/°C), three-pass-reflow-capable underfill and corner bond around the core die and the dense passives on its back side to offset thick-copper warpage and heat-sink clamping stress; a low-loss, low-shrinkage reinforcing adhesive with Dk held at 3.2-3.8 and Df below 0.01 at 1 MHz near high-speed pairs, RF front ends and optical couplers; and a high-thermal, high-CTI (≥600 V), thermo-oxidation-resistant potting and structural adhesive in the PSU/BBU and planar-inductor potting zones, so high heat flux and high-voltage clearance stay stable over the long term.

## Rail Traction and Onboard Electronics

Traction converter control boards in high-speed and metro trains, train control and management (TCMS) boards, and the powertrain control boards in electric vehicles (BMS/OBC/motor controller) face 15 to 30 years of mechanical vibration and extreme thermal cycling. In rail applications, EN 50155:2026 sets demanding requirements for temperature class and supply interruption, IEC 61373 defines severe random vibration and mechanical shock spectra by mounting location (body, bogie, axle), and the whole assembly must also clear the fire and smoke-toxicity thresholds of EN 45545-2.

At PCBA level, two duty cycles matter most. One is condensation: as a train runs through tunnels or across climate zones, the steep temperature difference between the cabinet interior and exterior can flash-condense water onto the board, and a water film bridging fine-pitch leads under the permanently energised battery bias quickly starts electrochemical migration and corrosion. The other is vibration: large inductors, relays and filter capacitors inside the converter cabinet sit in a mix of high-frequency mechanical resonance and electromagnetic-force vibration, and through-hole joints fatigue and crack. The established industry answer is a three-layer defence of underfill, component collars and conformal coating: wide-temperature underfill or corner bond on BGA/QFP control devices, a high-strength, high-toughness component-fix adhesive bonding large capacitors, heavy inductors and board-edge connectors firmly to the board, and a full-board coating of high-durability conformal coating qualified to IPC-CC-830C and UL 94 V-0 (or a UV/moisture dual-cure coating in shadowed areas). The corresponding SCITEO system retains more than 95% shear strength after 1,000 thermal shocks from −40 °C to +125 °C, with no blistering, cracking or whitening, keeping condensation and vibration damage away from the joint.

## HVDC Flexible Transmission and Valve Control Boards

In UHVDC transmission and offshore-wind flexible DC converter stations, a gigawatt-class link is built from thousands of modular multilevel converter (MMC) submodules stacked in series and parallel into a valve tower tens of metres high. Each submodule carries a core control board (valve control and gate-drive boards) handling IGBT/IGCT gate drive, fibre-optic communication, energy harvesting and fault bypass protection. These boards sit on a high-potential platform and operate energised, with very short maintenance windows; a single false trigger or insulation breakdown can trip the link and cause an outage.

The electromagnetic and climatic environment inside the valve hall and power cubicle is severe. Microsecond switching of power devices produces common-mode voltage steps with dv/dt in the tens of kV/μs range, and the energy-harvesting transformer, isolation optocouplers and high-voltage sensing circuits on the control board must withstand demanding power-frequency and impulse withstand tests. If the encapsulant contains a micron-scale void, or if thermal cycling opens a microcrack and debonds it from a component lead, the high field initiates partial discharge (PD) in the gap first, bombarding and carbonising the surrounding resin until a tree-like track forms and breakdown follows. Under IEC 60270, high-voltage project acceptance often holds PD at 1.1 times rated voltage to 10 pC, sometimes 5 pC. Offshore wind converter platforms add high salt spray, high humidity and marine fungal growth. SCITEO's high-insulation deep-cavity potting and coating system combines very low viscosity and high penetration with extremely low cure shrinkage (<0.06%) and low volatile content (low outgassing), wetting the root of high-voltage devices completely without leaving microvoids, and pairs a CTI of 600 V or more with a 30-year thermal-ageing model to extinguish PD initiation at the source.

## High-End Medical Electronics and Surgical Robotics Control Boards

Surgical robotics, medical imaging and in-vitro diagnostics ask no less of board-level reliability than any industrial duty cycle; the pressure simply arrives from a different direction. Joint control boards in multi-arm surgical robots must survive repeated high-temperature steam sterilisation after every procedure, and 134 °C saturated steam attacks the adhesive with heat, moisture and chemistry at once. CT and DR detector front-end boards and ultrasound front ends need very low dielectric loss and dimensional stability across a wide temperature range, because alignment drift from cure shrinkage lands directly in image quality. Control boards in clinical chemistry and immunoassay analysers sit permanently among reagent vapour and wash-solution splash, and once ionic cleanliness fails, metrological drift becomes a misread test result. Wearable and implantable monitoring stretches the same line further: continuous glucose monitoring and similar products must stay unaged for years at body temperature in contact with body fluid.

Few formulations clear all four gates of sterilisation cycling, low ions, low outgassing and low shrinkage at once. For high-reliability medical electronics SCITEO combines low-shrinkage potting, low-ion underfill and photo-thermal dual-cure adhesives: the potted body retains more than 90% shear strength after 500 autoclave cycles at 134 °C, mobile ions stay at or below 10 ppm, total mass loss and collected volatile condensable materials are held to an optical-grade low per ASTM E595, and low-CTE underfill at 13-30 ppm/°C keeps detector and sensor front ends aligned across the temperature range. For contact devices that need an ISO 10993 biocompatibility assessment, the material platform can support the customer's registration path with cytotoxicity and extractable data.

## Flexible Circuits (FPC) and Rigid-Flex Boards

In foldable devices, wearables, automotive LiDAR and the CCS (cell contacting system) busbar sensing assemblies of EV battery packs, FPCs and rigid-flex boards have largely replaced conventional wiring harnesses. The most common mistake in flex bonding is to carry a high-modulus adhesive from rigid boards straight onto flex. FPC substrates are thin polyimide (PI) or liquid crystal polymer (LCP), and a conventional rigid epoxy applied at the rigid-flex transition creates an extremely sharp stress-concentration step; a small bend or vibration then snaps the copper trace flush with the adhesive edge.

At the other end, on CCS FPC-to-nickel laser welds, NTC thermistor probes and connector pin roots, the adhesive must survive −40 °C to +125 °C automotive temperature, continuous road vibration and potential battery condensation. SCITEO grades the flex system explicitly by modulus: low-modulus, high-elongation stress-buffering adhesives and UV/moisture dual-cure coatings in dynamic bend zones and at the rigid-flex boundary, so the material does not embrittle at low temperature or creep and delaminate under damp heat; and a high-adhesion, ≤10 ppm mobile-ion, electrochemical-migration-resistant encapsulant for static steel/FR4 stiffener bonding and sensor-joint encapsulation, combining seconds-level UV surface cure with moisture/heat deep cure in shadowed areas to match the takt of automated EV production lines.

## Reflow Thermal History and the Three-Pass Window for High-Temperature Adhesives

Whether the material is SMT red glue for double-sided reflow, a special module adhesive dispensed before the oven, or underfill and potting compound that must survive repeated passes during board rework, BGA reballing and pin-in-paste through-hole reflow, the lead-free reflow profile is a hard gate for every polymer. SAC305 paste has a solidus at 217 °C and a liquidus near 220 °C; to wet large copper planes and high-thermal-mass parts, the furnace peak is usually pushed to 235-250 °C (260 °C on some thick boards or halogen-free processes), with time above liquidus (TAL) of 45 to 90 seconds.

A double-sided board with front reflow, back reflow and one local hot-air rework pass forces the adhesive layer through three or more reflow shocks peaking at 250-260 °C. The thermal weaknesses of ordinary electronic adhesives show up across that history: too-fast ramp in preheat and soak flashes residual solvent or adsorbed moisture into vapour, causing popcorning that cracks the adhesive or the die; at the 250 °C peak, an insufficient decomposition temperature (Td) lets the backbone crack and outgas, blowing interconnected voids around the joint or pushing molten solder off the pad (solder-ball spatter or bridging); and in the subsequent cooling zone, where the ramp can reach 3-4 °C/s, excessive CTE can pull the just-solidified joint apart.

Holding the three-pass window requires margin at two anchor points. The first is hot modulus and the Tg ladder: SCITEO's reflow-resistant high-temperature system covers multiple Tg platforms from 190 °C to 280 °C, so the compound does not collapse or flow at the peak. The second is the decomposition backbone: we lift the 5% weight-loss temperature (Td5, by TGA) to 465 °C, a full 200 °C above the highest lead-free reflow peak, and pair it with 13-30 ppm/°C low expansion and very low moisture uptake, so three 260 °C passes leave no delamination, cracking or blistering at the interface. The engineering figure below breaks down the four-zone lead-free profile, the physical stress at each zone and the material defence line SCITEO builds against it.

![SCITEO R&D team analysis: a four-zone lead-free reflow profile and the three-pass process window for SCITEO high-temperature adhesives. SAC305 solidus 217 °C and liquidus near 220 °C, reflow peak 235-250 °C, TAL 45-90 s and cooling at or below 4 °C/s, with the warpage, flux-residue, IMC-growth and residual-stress pain points of each zone, plus the four material gates of Tg across 190-280 °C (multi-grade portfolio), Td5 of 465 °C, CTE 13-30 ppm/°C and no damage after three 260 °C reflow passes, and the thermal-margin ladder](https://www.sciteo.com/images/articles/pcba-packaging2.svg)

# Interface Material Selection Quick Reference

The failure chains above compress into one table for a process engineer to work down during review:

| Process Segment | Typical Failure Mode | Key Metrics | SCITEO Direction |
|---|---|---|---|
| SMT assembly and reflow | Underfill voids from flux residue, brittle fracture in low-temperature alloys | Surface-energy tolerance, ≤10 ppm mobile ions, low-temperature cure window | Low-temperature-cure underfill and edge-bond adhesives |
| Pin reinforcement and corner bonding | Pad cratering and pin fracture under drop impact | CTE 13-30 ppm/°C, high modulus, Tg 100-160 °C | Low-CTE underfill and edge-bond adhesives |
| Chip underfill | Voids from insufficient capillary flow, interfacial delamination under thermal cycling | Capillary flow, void area fraction, mobile ions ≤10 ppm | Underfill encapsulants |
| SiP modules and die stacks | Underfill voids inside the module cavity, delamination at PoP interfaces | Capillary flow through 50 μm-class gaps, low shrinkage, low outgassing | Module underfill and dam-and-fill encapsulants |
| Power device to heat spreader bonding | Interfacial thermal resistance drift, thermal-layer pump-out | 2.0-60 W/m·K, 20-32 MPa shear, re-verified interfacial resistance | High-thermal structural bonding adhesives |
| Aerospace connector and power module potting | Cure shrinkage stress cracking MLCCs and glass-bodied devices | Volume shrinkage <0.06%, −65~+280 °C | Ultra-low-shrinkage wide-temperature potting |
| FPC and rigid-flex boards | Dynamic bend fatigue, adhesive creep and interfacial delamination under low temperature and damp heat | Low modulus and high elongation, ≤10 ppm ions, −40~+125 °C range | Flexible stiffening and stress-buffering structural adhesives |
| Classified boards and algorithm modules | Optical microscopy and chemical-etch reverse engineering | Chemical inertness, no non-destructive stripping, ≤10 ppm ions | Anti-tamper encapsulants |
| Rail transit onboard boards | Long-term vibration fatigue, electrochemical migration under condensation and salt spray | EN 50155:2026 temperature class, IEC 61373 vibration, EN 45545-2 fire performance | Wide-temperature underfill and conformal coating |
| Converter valve hall and offshore platform boards | Partial discharge inception, wide-temperature ageing, fungal attack | CTI ≥600 V, partial discharge ≤10 pC, low-outgassing potting | High-insulation wide-temperature potting |

# Material Variables Are Becoming a Design Prerequisite

In many hardware teams, electronic adhesives used to be treated as a firefighter called in after the first prototype hit a wall: a board drops out in testing or fails dual-85 and thermal shock, and a process engineer is sent to the market for a tube of adhesive to patch the problem. That reactive approach could survive in the low-density era. It does not survive a high-density PCBA with micron-scale gaps, kilowatt-class heat flux and high voltage combined with high frequency. If no keep-out zone was reserved for dispensing, no one checked the surface-energy match between solder mask and flux, and no one reviewed the shrinkage-stress path through the potting cavity, swapping adhesives afterwards usually moves the failure rather than removing it.

Once PCB stack-up, lead-free alloy and component package dimensions are fixed by industry standards, most of the freedom left to hardware and process teams for tuning board-level thermo-mechanical margin now sits with polymer material suppliers such as SCITEO Advanced Materials. Bringing cure shrinkage, storage-modulus-versus-temperature, interfacial thermal resistance, ionic cleanliness and the dispensing rheology window into schematic and layout review, and starting that work alongside chip selection and thermal simulation, is how line yield and a thirty-year field life become defined values on the drawing.

This article is SCITEO Advanced Materials original technical content; unauthorized reproduction is prohibited.

## Appendix: Process & Engineering Adhesive FAQ Index

### Why do some adhesives throw satellite droplets during piezo jet dispensing and contaminate adjacent fine-pitch pads?

The root cause is rheology matching, not the machine. The adhesive sees an extremely short extensional event at the nozzle, and if cohesive strength is insufficient, or if structural recovery after shear thinning is too slow, the fluid tail breaks up through Rayleigh-Plateau instability and throws off micron-scale satellites. Only two quantities can actually be pinned on the line: filament break length and thixotropic recovery time. Too short a break length strings, and too slow a recovery lets the dot creep across the board. SCITEO jetting grades use molecular-weight distribution control and a purpose-built thixotropic network to keep a clean fracture face at 200 Hz and above, then rebuild viscosity quickly once the droplet contacts the substrate, without giving up the capillary penetration that underfill needs. Stray-droplet complaints that look like an equipment fault usually end up back at this layer of rheology matching.

### For large-volume potting and power device encapsulation, what makes sub-0.06% shrinkage physically necessary?

The driver is residual cure stress. Crosslinking a liquid resin into a three-dimensional network always involves volume shrinkage, and above roughly 1% shrinkage a large cavity accumulates tens of megapascals of constraint stress, which is enough to crack a multilayer ceramic capacitor through its body or displace glass-bodied diodes and exposed pins. SCITEO uses an organic-inorganic hybrid prepolymer for in-situ expansion compensation, holding volume shrinkage below 0.06% as derived from ISO 2577 linear shrinkage. Cure then exerts negligible physical drag on internal precision parts, while the material still survives repeated 260 °C reflow. That check happens earliest on the rear section of aerospace connectors and specialty power modules, because shrinkage overrun usually does not surface until thermal cycling starts.

### Why can anti-tamper encapsulants not be dissolved by standard solvents, and how should rework be handled?

The cured network is built from a high-density crosslinked phenolic epoxy and aromatic amine system whose crosslink density and solubility parameters are completely mismatched against thinners, dichloromethane, acetone and other standard industrial solvents, so solvent molecules cannot penetrate and swell the network. We designed it for irreversible physical protection: any attempt to melt or chemically strip the layer destroys the underlying traces and dies first, which removes the information value of reverse engineering. Encapsulation of this type is a one-way process with no non-destructive rework path. Where a rework window must be preserved, the right move is to switch to locally removable underfill and corner-bond reinforcement at the design stage and to assess confidentiality and serviceability separately, rather than looking for a fix after ramp.

### Why is it difficult for a thermally conductive PCBA encapsulant to combine high thermal conductivity with high volume resistivity?

The conflict comes from the filler itself. Metal and graphite fillers conduct heat through electrons, which is efficient but drops insulation resistance by several orders of magnitude; ceramic fillers such as boron nitride, aluminium nitride and alumina conduct through phonons and insulate well, but interfacial thermal resistance is highly sensitive to filler grading and surface coupling. SCITEO combines multimodal ceramic filler grading with polymer interfacial coupling so that phonon pathways connect across the particles, reaching thermal conductivity across the 2.0 to 60 W/m·K range while holding volume resistivity above 10¹⁴ Ω·cm, and then re-verifies interfacial thermal resistance per ASTM D5470 at the target pressure and bond-line thickness so that a single test condition cannot distort the picture. In review we remind customers that thermal conductivity is a material value while interfacial resistance is what actually sets junction temperature, so the two have to be read together.

### What do conformal coating, underfill and full potting each solve, and can one replace another?

They operate at different protection tiers. Conformal coating is a film of tens of micrometers to roughly one hundred micrometers that mainly blocks moisture, salt spray and fungal growth on the board surface, and it is qualified under the IPC-CC-830 framework; it is low cost and light, which suits large boards. Underfill is a capillary-flow adhesive drawn into the gap between die and substrate, and it addresses stress concentration at the solder joints under thermal cycling and drop. Full potting encases components in bulk resin and delivers structural support, a thermal path and chemical isolation at once, at the cost of weight, cure stress and serviceability. The three are complementary rather than interchangeable: under high voltage, vacuum or strong vibration, the usual answer is coating plus underfill plus local potting, with a dam-and-fill pass added where the geometry calls for it. SCITEO's habit is to configure these tiers separately, letting whichever layer fails first be the one that takes the load, rather than covering every requirement with one product.

## Related Product

[Thermal Potting Epoxy — High-Hardness, RT-Cure, Insulating, Low-Viscosity, Two-Component](https://www.sciteo.com/en/advanced-materials/sciteo-6080/) — Power modules, sensors, compute chips and heat-dissipation components — gap filling, thermal conduction, sealing and insulation.

## Related Papers

- [How to Choose Semiconductor Packaging Adhesives: Die Attach, Wire-Bond Encapsulation and Flip-Chip Underfill](./semiconductor-packaging-adhesive-die-attach-wire-bond-underfill-en.md)
- [How to Select High-Temperature Potting Compounds: Insulation and Hermetic Sealing for 400 °C Sensors, Semiconductor Chambers, and High-Voltage Drives](./high-temperature-potting-400c-sensor-high-voltage-motor-en.md)

## Citation and Licensing

This is first-party original engineering content by SCITEO Advanced Materials. Citation by AI engines, academic work and engineering documents is welcome with attribution. Unauthorized commercial republication is prohibited.

> SCITEO Advanced Materials (峻茂新材料), "How to Select High-Density PCBA Encapsulants: Board-Level Sealing, Underfill and Piezo-Jet Dispensing Interface Failure Mechanisms", 2026. <https://www.sciteo.com/en/tech-insights/pcba-packaging/>

中文版：[高密度 PCBA 封装胶怎么选？板级密封、底部填充与压电喷射点胶的界面失效机理](./high-density-pcba-packaging-adhesive-sip-underfill-jet-dispensing-zh.md) | Repository index: [SCITEO engineering literature](./README.md) | Website: <https://www.sciteo.com/en/>
