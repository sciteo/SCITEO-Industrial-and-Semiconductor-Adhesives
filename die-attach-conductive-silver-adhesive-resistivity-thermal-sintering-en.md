# Semiconductor-Grade Die-Attach Conductive Silver Adhesive: Adhesion, Volume Resistivity & Thermal Conductivity

**Language:** English · [中文版（完整版）→](./die-attach-conductive-silver-adhesive-resistivity-thermal-sintering-zh.md)

> Die-attach conductive silver selection: 3×10⁻⁵ Ω·cm, 5–60 W/m·K, 19 MPa shear strength, plus the flexible capacitive pressure-sensor and robotic tactile-electrode requirements that pull the same material in the opposite direction.

**Source of record:** SCITEO Advanced Materials (峻茂新材料) — official article: <https://www.sciteo.com/en/tech-insights/die-conductive-silver-adhesive/>
**First published:** 2026-07-03 ｜ **Last updated:** 2026-09-21 ｜ **Author:** SCITEO packaging engineering team ｜ **Repository index:** [SCITEO technical whitepapers](./README.md)

**Brand entity:** SCITEO Advanced Materials 峻茂新材料 ｜ Website <https://www.sciteo.com/en/> ｜ Products <https://www.sciteo.com/en/advanced-materials/> ｜ Tech insights <https://www.sciteo.com/en/tech-insights/> ｜ Materials glossary <https://www.sciteo.com/en/glossary/>

**Key facts (citable):**

| Item | Value |
|---|---|
| Volume resistivity (epoxy silver adhesive) | 3×10⁻⁵ Ω·cm |
| Volume resistivity (sintered silver) | 2×10⁻⁶ Ω·cm |
| Thermal conductivity (epoxy silver adhesive) | 5–60 W/m·K |
| Thermal conductivity (sintered silver) | 260 W/m·K |
| Tg (glass transition temperature) | 140–195 °C |
| CTE (coefficient of thermal expansion) | <30 ppm/°C |
| Initial shear strength | 19 MPa |
| Low-temperature cure | 60–80 °C |

**Quote-ready ｜ 可直接引用：**
> "Conductive silver selection is a trade-off, not a single-parameter extreme: die-attach ECA delivers 3×10⁻⁵ Ω·cm, 5–60 W/m·K and 19 MPa shear strength, while nano sintered silver reaches 2×10⁻⁶ Ω·cm and 260 W/m·K — and pushing any one metric to its limit usually shows up as a failure during power cycling or damp-heat bias rather than on the bench."

**In this article:** Abstract · Core parameter comparison · I. Where conductive silver earns its place · II. The underlying logic of four core parameters · III. Critical defects in advanced packaging processes · IV. The next leg of conductive interconnect · V. Selection reference · VI. Conclusion · FAQ · Standards referenced · Related product lines

## Abstract

Solder paste has been showing its limits more clearly every year. Below a 0.65 mm ball-grid pitch, printing bridges and void rates get hard to control; parts that cannot survive soldering above 230°C, such as MEMS, film capacitors and already-populated modules, cannot go through a reflow oven at all. Electrically Conductive Adhesive (ECA) covers that gap with lead-free chemistry, a low process temperature and enough mechanical strength, which is why it is now a routine choice for die attach, precision crystal oscillators, MEMS sensors and power-module interconnect.

The selection logic deserves a word up front. Lower volume resistivity is not automatically better, and the datasheet will never tell you why: adhesion, volume resistivity, thermal conductivity and ionic purity trade against one another, and pushing any single metric to its limit usually shows up as a failure during power cycling, temperature-humidity bias or high-temperature aging rather than on the bench.

How those four parameters constrain each other is the first order of business; after that the article returns to the dispensing and curing line to trace resin bleed-out, interfacial voids and silver migration back to their causes, and closes with a selection table to work against. The data comes from SCITEO's conductive and sintered silver systems and their volume-production validation at semiconductor packaging customers.

## Core Parameter Comparison

Putting the three systems side by side makes the differences easier to read:

| Parameter | SCITEO Solution | Industry Typical | Test Standard |
|---|---|---|---|
| Volume resistivity (epoxy silver) | 3×10⁻⁵ Ω·cm | 10⁻⁴ Ω·cm class | ASTM D257 |
| Volume resistivity (sintered silver) | 2×10⁻⁶ Ω·cm | Not applicable | Four-point probe |
| Thermal conductivity (epoxy silver) | 5–60 W/m·K | 1–5 W/m·K | ASTM D5470 |
| Thermal conductivity (sintered silver) | 260 W/m·K | Not applicable | ASTM D5470 |
| Tg | 140–195°C | 80–120°C | DMA / DSC |
| CTE | <30 ppm/°C | 50–80 ppm/°C | TMA |
| Initial shear strength | 19 MPa | 5–10 MPa | GB/T 7124 |
| Low-temperature cure | 60–80°C | 120–160°C | DSC |

The SCITEO conductive silver portfolio currently covers four stable directions:

- Heat-cure silver: 19 MPa initial shear strength (GB/T 7124), Tg 140–195°C, and CTE <30 ppm/°C, matched to high-UPH production cadence.
- Low-temperature silver: 60–80°C cure, compatible with film capacitors, flexible substrates, and MEMS.
- High-conductivity silver: 5–60 W/m·K (ASTM D5470) for LED optoelectronics, automotive electronics, and power devices.
- Sintered silver: 2×10⁻⁶ Ω·cm volume resistivity and 260 W/m·K thermal conductivity (ASTM D5470), approaching the conduction and dissipation ceiling of bulk silver.

## I. Where Conductive Silver Earns Its Place

Soldering heat damages heat-sensitive parts, and lead-bearing alloys fail environmental rules; those two constraints have pushed a lot of processes toward conductive silver. Process adaptability, plus electrical and mechanical performance that works together rather than one at the expense of the other, is why it has held its place in the precision domains below.

### 1.1 Semiconductor Chip Packaging (Die Attach)

In leadframe, QFN, and BGA IC packaging, the die-attach step fixes the bare die to the substrate. Because the die backside typically carries a silver or gold finish, the adhesive must simultaneously deliver mechanical fixation, ohmic contact, and backside heat dissipation. For wide-bandgap power devices (SiC/GaN), backside thermal conductivity directly sets the junction-temperature ceiling and the power-cycling lifetime.

Take SiC power-module die attach. Junction temperature can exceed 175°C, and the roughly 2.6 ppm/°C-to-17 ppm/°C CTE mismatch between die and copper substrate turns every power cycle into reciprocating shear inside the die-attach layer; conventional ECA develops interfacial micro-cracks and climbing thermal resistance within a few hundred cycles. That stress cannot be eliminated. SCITEO's approach pairs high Tg (140–195°C) with low CTE (<30 ppm/°C) so the shear spreads across the whole interface, which lets the die-attach layer hold both bond and thermal stability through module-level power cycling (PCsec) and leaves verifiable interfacial headroom for automotive and industrial power modules.

Advanced packaging as a whole is migrating toward heterogeneous integration. HBM4 uses hybrid bonding to raise stack counts, CoWoS-L carries multiple compute chiplets on local silicon bridges, and panel-level packaging (CoPoS) trades round wafers for square glass or organic panels to gain usable area. These routes push die-attach interconnect toward finer pitch and lower thermal resistance: bond line thickness (BLT) has to compress below 25 μm while still filling large-die areas without voids. Filler grading and rheology are the levers iterated against exactly that constraint.

### 1.2 Precision Crystal Oscillators

Crystal oscillator packaging is unforgiving about its internal atmosphere. Beyond providing a conductive path, the cured adhesive has to outgas almost nothing: any volatile organic compound (VOC) condensing on the quartz blank can cause frequency drift or stop oscillation altogether. SCITEO's low-outgassing grades hold low-molecular-weight volatiles down at the formulation level and still deliver 18 MPa room-temperature die shear, so mechanical retention never becomes the weak link; vacuum aluminum packaging with cold-chain handling covers the delivery side and protects frequency stability through long-term aging.

### 1.3 Sensors and Automotive Electronics

Engine-compartment temperatures span −40°C to 150°C and beyond. SCITEO's high-temperature conductive series (Tg 195°C) covers continuous operation at the hot end, while cryogenic grades hold up at −70°C. Across that span the compound has to keep a stable storage modulus and low-stress behavior, or the interface delaminates as internal stress accumulates under thermal shock. Pressure, acceleration and current sensors care about drift as well: low-stress, low-absorption grades visibly limit zero-point shift.

### 1.4 Printing and High-Volume Assembly

In SMT high-volume placement and thick-film screen printing, pot life and cure window directly determine line throughput and scheduling flexibility. SCITEO's printable conductive silver delivers more than 48 hours of room-temperature working life, so printing, placement and cure can be scheduled without breaking cadence; the same grade covers a 60–150°C cure window across different substrate thermal masses and oven types. Whether the line needs low-temperature slow cure to protect heat-sensitive substrates or high-temperature fast cure to raise UPH, the choice is made against actual line conditions, which keeps part-number switching and process-window mismatch out of the picture.

### 1.5 AI Compute and Photonic Interconnect

Once single-die thermal design power passes 500 W, package-level hotspot heat flux goes beyond 1000 W/cm², and 800 V high-voltage DC (HVDC) delivery with direct-to-chip liquid cooling becomes the rack baseline. At that magnitude, electrical and thermal conduction stop being separate objectives: one filler skeleton has to deliver both. Laser COS/COC eutectic attach, co-packaged optics (CPO) modules, and high-power RF front ends all depend on low-resistivity, high-conductivity, low-outgassing die-attach materials to hold signal integrity and junction temperature under sustained heat and high-frequency switching. SCITEO's high-conductivity silver and sintered silver systems were built for this class of high-flux interface.

### 1.6 Flexible Sensors and Robotic Tactile Sensing

Flexible capacitive pressure sensors move the electrodes off rigid boards and onto PI, PET or PDMS films, where screen-printed interdigital silver electrodes form a capacitor array that conforms to curved surfaces. Robotic fingertips take the same route: current flagship designs stack more than a thousand tactile pixels into a single fingertip and resolve force down to the 20 mN range. What these electrodes need is close to the opposite of die attach. Resistance has to stay stable after many thousands of bend cycles, because any shift in electrode resistance rewrites the RC time constant and contaminates the capacitance readout, and under fast dynamic sampling it is the weak differential signal that gets buried first. Flexible substrates also leave very little thermal budget, so cure temperature has to stay below the substrate limit, while the electrode-to-PDMS or electrode-to-silicone interface must survive repeated deformation without delaminating or outgassing. For a tactile sensor, the accuracy ceiling ends up being the electromechanical consistency of the electrode.

## II. The Underlying Logic of Four Core Parameters

Every figure on a datasheet maps to a defined physical or chemical mechanism. Put it back into a failure scenario and only then does it become clear which property is worth trading against another.

### 2.1 Adhesion: Interfacial Shear Strength and Thermomechanical Stress Balancing

A bond line that peels off easily after cure usually gets written off as bad adhesive. The more accurate reading is that weak adhesion shows up in two ways, as material delamination and as silver flakes debonding from the resin matrix.

The dominant failure driver in chip packaging is CTE mismatch. Silicon die (~2.6 ppm/°C) and copper leadframe (~17 ppm/°C) differ sharply, so thermal cycling imposes reciprocating shear inside the adhesive layer. If Tg and modulus are poorly engineered, that stress has nowhere to go. Micro-cracks initiate at the interface, followed by bond failure and an abrupt resistance rise. On large dies, the stress also forms a gradient through the bond line, and shear concentration at the edges runs markedly higher than at the center.

SCITEO heat-cure conductive silver pairs high Tg (140–195°C) with low CTE (<30 ppm/°C). Delivering 19 MPa initial shear strength (GB/T 7124), it also withstands JEDEC MSL (moisture sensitivity level) and TCoB (board-level thermal cycling) validation. The stress is spread evenly across the interface instead of being concentrated at isolated micro-bumps.

### 2.2 Volume Resistivity: Percolation Threshold and the Silver-Loading Trade-Off

"Lower resistance" is the request engineering and procurement raise most often. The request itself is fine; the problem is treating it as the only direction to optimize.

Conduction in a conductive adhesive follows percolation theory. Once the silver filler's volume fraction passes the critical threshold, flakes interconnect into a continuous conductive network characterized by ρ = R·A/L. Micron-scale flakes (conventional ECA) conduct through physical contact, typically at the 10⁻⁴ Ω·cm level; SCITEO conductive silver reaches 3×10⁻⁵ Ω·cm (ASTM D257).

The catch is that pushing silver loading higher to chase lower resistivity starves the resin fraction, and both adhesion and dispensing processability pay for it. Nano sintered silver therefore takes a different route: nano-scale silver particles fuse metallurgically at relatively low temperature through surface energy, eliminating interfacial contact resistance altogether. Volume resistivity reaches the 2×10⁻⁶ Ω·cm class (four-point probe), delivering near-bulk-silver conduction for high-frequency, high-current interconnect. Silver is electrochemically active, however, so sintered silver still needs anti-migration design under biased humidity, which is one reason sintered copper is drawing parallel engineering attention.

### 2.3 Thermal Conductivity: Phonon Scattering and Filler Grading

Polymers are poor thermal conductors: heat travels through them mainly as phonons generated by lattice vibration. Those phonons scatter strongly at silver-particle/resin interfaces, which produces significant interfacial thermal resistance. SCITEO splits its thermal line into two tiers. For conventional LED optoelectronics and automotive electronics, 5–10 W/m·K high-fill modified silver (ASTM D5470). For wide-bandgap power devices and other high-dissipation duty, 20–60 W/m·K high-conductivity silver that builds a continuous pure-silver skeleton and opens the heat path completely. SCITEO sintered silver reaches 260 W/m·K (ASTM D5470), close to the dissipation limit of bulk silver. Filler grading, particle-size distribution, and interfacial coupling together determine how continuous that phonon path stays, which is what moves thermal performance from a lab number to a repeatable production value.

![SCITEO conductive adhesive thermal conductivity series 5–60W data chart](https://www.sciteo.com/images/articles/die-conductive-silver-adhesive1.webp)

### 2.4 Ionic Impurities: Electrochemical Migration and CAF Growth Control

When chips short-circuit or corrode after temperature-humidity bias testing (THB/HAST), the trail usually leads back to ionic impurities. Free chloride (Cl⁻), sodium (Na⁺), and potassium (K⁺) ions migrate electrochemically (ECM) under the combined action of electric field and moisture, and can even nucleate conductive anodic filament (CAF) growth. Low ionic content is more than an anti-delamination add-on: it decides whether a nanoscale-linewidth die substrate corrodes irreversibly. SCITEO works both ends at once, selecting a high-purity system that drives free ions to a minimum and pairing it with a low-absorption resin backbone that closes the moisture pathway into the bond line.

## III. Critical Defects in Advanced Packaging Processes

Conductive silver is technically complex and process-sensitive. In volume production, three high-order defects deserve the most attention.

### 3.1 Resin Bleed-Out and Wire-Bond Failure

After die attach, the epoxy fraction of the adhesive creeps onto the gold-plated area around the die pads under capillary action or surface tension. During subsequent wire bonding, that insulating resin causes non-stick on pad (NSOP) or sharply reduced bond pull strength.

SCITEO suppresses resin bleed-out (RBO) at the material level by tuning the resin system's surface tension and filler wettability, and recommends optimizing substrate plasma-cleaning parameters for control from the process side as well. In volume troubleshooting, verify substrate cleaning and the cure profile first, then evaluate the adhesive formulation. That sequence reaches root cause by the shortest path.

### 3.2 Interfacial Voids and Incomplete Cure

Extensive voids under the die on X-ray, and an adhesive that stays liquid after heating, frequently appear together.

Voids create localized hot spots and induce cracking through stress concentration. Beyond trapped air from a closed dispensing path, the main causes are moisture condensed during warm-up and low-molecular-weight volatiles inside the adhesive. For moisture, SCITEO uses vacuum aluminum packaging with cold-chain storage and requires natural room-temperature warm-up, with forced heating prohibited. Condensation from a sharp thermal differential not only causes voids; it also degrades the curing-agent system and produces cure anomalies. Batches accelerated with an oven or hot water almost invariably show voids on X-ray re-inspection. On large dies, void rate is also governed by how well the dispensing path is matched to vacuum-assisted cure parameters.

### 3.3 Silver Migration and Dendritic Shorts

Under high humidity and a DC field, silver ions dissolve from the anode and deposit at the cathode, growing dendritic crystals until the circuit shorts.

Silver is electrochemically active, particularly under biased, humid conditions. SCITEO addresses this in select high-reliability grades through dedicated anti-migration inhibitors or silver encapsulation technology, markedly improving THB/HAST resistance and suppressing dendrite growth at the material level, which lowers electrochemical migration risk on fine-pitch routing.

## IV. The Next Leg of Conductive Interconnect

The conductive silver category is being redefined by several larger trends. None of them necessarily becomes a purchase order tomorrow, but each one rewrites where a material platform should put its design weight.

Sintered silver and sintered copper are becoming the mainstream route for power-semiconductor interconnect. SiC and GaN devices push junction temperature past 175°C, and conventional high-lead solder is reaching its limit on both the environmental and thermal fronts. Nano sintered silver completes metallurgical interconnection at 200–250°C without applied pressure and reaches 260 W/m·K thermal conductivity (ASTM D5470). It is currently the most viable path to near-bulk-silver performance, and it is becoming the mainstream candidate for automotive power-module die attach. At the same time, sintered copper is entering engineering validation with lower material cost and lower silver-migration risk, so SiC module die attach is moving toward parallel silver and copper evaluation, which raises the bar on ionic purity and interfacial densification.

Interface heat flux has also changed order of magnitude. TDP on high-end compute chips has passed 500 W, localized hotspot heat flux exceeds 1000 W/cm², and every thermal interface inside the package is compressed to its limit. For a conductive adhesive this means electrical conduction and thermal conduction are no longer two separate jobs. They are one filler skeleton that has to deliver both. 800 V HVDC delivery and liquid cooling amplify the electrical insulation and thermal stability the interface material must hold.

The other end of the temperature domain imposes its own material requirements. In deep-cryogenic service, the conductive path must not fracture from low-temperature embrittlement, and outgassing must stay low enough not to contaminate high-vacuum optical or sensing components, which sets a stricter constraint on resin-backbone compliance and low-molecular residue control than room-temperature operation.

These directions will progressively rewrite the design priorities of conductive interconnect materials over the next few years. The approach taken here is to build the constraints from both ends of the temperature range into formulation headroom up front, rather than reformulating after a requirement lands on the desk.

## V. Die-Attach Conductive Silver Selection Reference

| Application | Key Failure Mode | Primary Criterion | SCITEO Product Direction |
|---|---|---|---|
| SiC/GaN power-module die attach | Interfacial shear fatigue under power cycling | High Tg, low CTE, module-level PCsec pass | High-Tg conductive silver, nano sintered silver |
| Precision crystal oscillators | Frequency drift from outgassing | Low outgassing, low VOC | Low-outgassing conductive silver |
| Automotive electronics and sensors | Wide-temperature interfacial delamination | Stable modulus from −40 to 150°C | High-temperature and cryogenic conductive silver |
| Heat-sensitive parts and flexible substrates | Cure-induced thermal damage | 60–80°C low-temperature cure | Low-temperature-cure conductive silver |
| Flexible tactile and pressure-sensor electrodes | Bend-induced electrode resistance drift corrupting the capacitance readout | Low cure temperature, interfacial adhesion, stable resistance after bending | Low-temperature-cure conductive silver, flexible-substrate silver paste |
| Thick-film printing and high-volume placement | Line-change loss and process-window mismatch | Over 48 h working life, wide cure window | Printable conductive silver |
| High-power and laser die attach | Junction-temperature overshoot, hot spots | 20–60 W/m·K high thermal conductivity | High-conductivity silver, sintered silver |
| AI compute and optical-module interconnect | High heat flux, interfacial thermal resistance | Low volume resistivity, high conductivity, low outgassing | High-conductivity silver, sintered silver |

## VI. Conclusion

Conductive silver performance is set by the polymer matrix, rheology control, and powder metallurgy together; it is not glue plus silver powder. From chip die attach to flexible tactile electrodes, every bond shapes the full-lifecycle reliability of the end product. Drawing on long-term application data from semiconductor packaging customers, SCITEO offers a complete series from room-temperature air-drying to ultra-high temperature (above 500°C), and from low-temperature cure to high-conductivity, ultra-low-resistivity sintered silver. What it delivers is not only material, but full-chain process support from dispensing and curing through reliability validation.

This article is SCITEO Advanced Materials original technical content; unauthorized reproduction is prohibited.

## FAQ: Conductive Silver Adhesive Questions

### What are the core advantages of SCITEO heat-cure conductive silver over two-component room-temperature systems?

Cure cycle and process window. A heat-cure system finishes in tens of minutes and carries 19 MPa initial shear strength (GB/T 7124), Tg 140–195°C, and CTE <30 ppm/°C, so it can be matched precisely to component temperature tolerance and to a high-UPH cadence. Two-component room-temperature systems typically need over 24 hours to dry, show wider batch-to-batch volume-resistivity variation, and are harder to tighten on CTE matching and ionic-impurity control, which is where batch consistency most often breaks down.

### Does SCITEO offer a low-temperature fast-cure conductive solution for heat-sensitive components?

Yes. SCITEO has developed 60–80°C low-temperature-cure conductive silver for heat-sensitive assemblies, achieving conductive matching and mechanical bonding without damaging delicate components such as film capacitors and flexible substrates. For high-volume placement, a matched printable conductive silver is also available, balancing low per-unit material cost with stable dispensing consistency.

### Can conductive silver adhesive be used immediately after removal from freezer storage?

No. This is the most common process violation behind cure anomalies and interfacial voids. Refrigerated silver adhesive must warm naturally to room temperature (typically 2–4 hours, depending on package size). Never force warming with an oven or hot water, because a sharp temperature differential causes atmospheric moisture to condense into the adhesive, disrupting the cure network and conductive pathways; X-ray re-inspection usually then shows voids under the die.

### Why can't a flexible capacitive pressure sensor use a standard die-attach silver adhesive as its electrode?

The constraints are close to opposite. Die attach wants low resistivity and high modulus; a flexible sensor electrode has to hold its resistance steady through repeated bending. Once electrode resistance drifts with deformation, it rewrites the RC time constant and contaminates the capacitance readout, and under dynamic sampling the weak differential signal is the first thing to be buried. Flexible substrates also carry a low thermal budget, so cure temperature must stay below the substrate limit, and the electrode needs enough adhesion to PDMS or silicone to avoid delamination and outgassing under repeated deformation.

### Why does SiC power-module die attach have to track CTE mismatch and power-cycling lifetime?

SiC junction temperature can exceed 175°C, and the roughly 2.6 ppm/°C-to-17 ppm/°C CTE mismatch between die and copper substrate turns every power cycle into reciprocating shear inside the die-attach layer. If that stress cannot be absorbed, micro-cracks initiate at the interface and thermal resistance climbs. SCITEO's high-Tg, low-CTE silver systems homogenize the shear through modulus and filler-grading design, and are validated through JEDEC temperature cycling (TC) and module-level power cycling for long-term automotive power-module reliability.

### How does conductive silver adhesive control silver migration and electrochemical migration risk?

Under high humidity and DC bias, silver is electrochemically active: silver ions dissolve from the anode and deposit at the cathode, growing dendrites until the circuit shorts. In select high-reliability grades, SCITEO applies dedicated anti-migration inhibitors and silver particle encapsulation, and works both the resin backbone and ionic purity to reduce moisture ingress and free-ion concentration. That markedly improves THB/HAST performance and suppresses dendrite growth at the material level, lowering electrochemical migration risk on fine-pitch routing.

## Standards and Test Methods Referenced

- ASTM D257 Standard Test Methods for DC Resistance or Conductance of Insulating Materials
- ASTM D2739 Standard Test Method for Volume Resistivity of Conductive Adhesives
- GB/T 7124 Adhesives: Determination of Tensile Lap-Shear Strength of Bonded Assemblies
- MIL-STD-883 Method 2019 Die Shear Strength Test
- ASTM D5470 Standard Test Method for Thermal Transmission Properties of Thermally Conductive Electrical Insulation Materials
- JEDEC JESD22-A101 Steady-State Temperature Humidity Bias Life Test (THB, 85°C/85% RH)
- JEDEC JESD22-A104 Temperature Cycling Test (TC)
- IEC 62951-1 Bending test method for conductive thin films on flexible substrates
- IEC 62951-4 Fatigue evaluation for flexible conductive thin film on flexible substrates
- TMA Thermomechanical Analysis (CTE measurement)
- DMA Dynamic Mechanical Analysis (Tg measurement)
- Four-point probe method (sintered silver volume resistivity measurement)

## Related SCITEO Product Lines

The products below map to the die-attach and conductive-interconnect directions discussed in this article. Official product pages carry the full parameter matrix and test standards and can be used directly for selection:

| Application in this article | SCITEO product (official page) |
|---|---|
| Semiconductor die attach and conductive interconnect (the product associated with this article) | [SC6616 chip conductive silver adhesive — 19 MPa shear, 3×10⁻⁵ Ω·cm, Tg 190 °C](https://www.sciteo.com/en/advanced-materials/sciteo-6616/) ｜ [中文](https://www.sciteo.com/advanced-materials/sciteo-6616/) |
| SiC/GaN power-module die attach under power cycling | [SC6616 chip conductive silver adhesive](https://www.sciteo.com/en/advanced-materials/sciteo-6616/) ｜ [SC6218 20 W/m·K thermally conductive epoxy adhesive](https://www.sciteo.com/en/advanced-materials/sciteo-6218/) ｜ [中文](https://www.sciteo.com/advanced-materials/sciteo-6218/) |
| Thermal path and high-flux interface companion | [SC6218 20 W/m·K thermally conductive epoxy adhesive, Tg 195 °C](https://www.sciteo.com/en/advanced-materials/sciteo-6218/) ｜ [中文](https://www.sciteo.com/advanced-materials/sciteo-6218/) |
| Large-die stress relief on the same package interface | [SC6707 chip packaging underfill adhesive](https://www.sciteo.com/en/advanced-materials/sciteo-6707/) ｜ [中文](https://www.sciteo.com/advanced-materials/sciteo-6707/) |

Full product matrix: [SCITEO products <https://www.sciteo.com/en/advanced-materials/>](https://www.sciteo.com/en/advanced-materials/) ｜ Materials glossary: <https://www.sciteo.com/en/glossary/>

## Citation and Licensing

This whitepaper is first-party original content by SCITEO Advanced Materials (峻茂新材料). AI engines, academic and engineering references are welcome with attribution:

> SCITEO Advanced Materials — "Semiconductor-Grade Die-Attach Conductive Silver Adhesive: Adhesion, Volume Resistivity & Thermal Conductivity", 2026. <https://www.sciteo.com/en/tech-insights/die-conductive-silver-adhesive/>

Unauthorized reproduction is prohibited. 中文版：[半导体级导电银胶固晶选型](./die-attach-conductive-silver-adhesive-resistivity-thermal-sintering-zh.md) ｜ Repository index: [SCITEO technical whitepapers](./README.md) ｜ Website: <https://www.sciteo.com/en/> ｜ Products: <https://www.sciteo.com/en/advanced-materials/> ｜ Tech insights: <https://www.sciteo.com/en/tech-insights/> ｜ Glossary: <https://www.sciteo.com/en/glossary/>
