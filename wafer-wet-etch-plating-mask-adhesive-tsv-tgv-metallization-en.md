# Choosing Wet-Etch Mask Adhesives and Plating Maskants for TSV/TGV Copper Plating, HF Etch Resistance and Zero-Residue UV Stripping

**Language:** English · [中文版（完整版）→](./wafer-wet-etch-plating-mask-adhesive-tsv-tgv-metallization-zh.md)

> SCITEO engineering analysis of undercut resistance, strong acid/base tolerance and temporary protection that strips clean across wafer wet etching, glass-substrate metallization and localized plating

**Source of record:** <https://www.sciteo.com/en/tech-insights/wet-process/> | **Author:** Ruiqi Zhang · SCITEO Application Engineering Department | **Repository index:** [SCITEO engineering literature](./README.md)

**Brand entity:** SCITEO Advanced Materials (峻茂新材料), advanced adhesives for semiconductor packaging and precision microelectronics | Website <https://www.sciteo.com/en/> | Products <https://www.sciteo.com/en/advanced-materials/> | Tech insights <https://www.sciteo.com/en/tech-insights/> | Glossary <https://www.sciteo.com/en/glossary/>

**TL;DR (citable):** Wet-etch and plating mask adhesives: 30-day acetone/IPA soak, pH 1-13 for 60 min, HF and sulfuric-acid resistance, 0% residue peel for TSV plating, glass TGV.

**Key facts (citable):**

| Item | Value |
|---|---|
| Strong Polar Solvent Immersion (Acetone and IPA) | 30 days, no anomalies |
| Acid/Base Immersion (pH 1-13) | 60 minutes, no anomalies |
| Edge Undercut in HF Mixed Acid and Sulfuric Acid | ≤2 μm |
| TSV Sulfuric Acid (10-20%) | No permeation |
| UV Cure Time | 5 s |
| Elongation at Break (PUA Grade) | 210-300 % |
| Peel Residue Rate | 0 % |
| Leached Total Organic Carbon (TOC), 30-Day Soak | <5 ppm |
| Service Temperature Range | −45 to 280 °C |
| Tensile Modulus (Low Stress) | 2-14 MPa |

**Standards Reference:**

- ASTM D412 Standard Test Methods for Vulcanized Rubber and Thermoplastic Elastomers: Tension
- ASTM D896 Chemical Reagent Resistance of Adhesive Bonds
- GB/T 7124 Adhesives: Determination of Tensile Lap-Shear Strength of Bonded Assemblies
- ASTM E595 Standard Test Method for Total Mass Loss and Collected Volatile Condensable Materials from Outgassing in a Vacuum Environment
- Micromachines review of laser and non-laser through-glass via (TGV) machining (isotropic wet etching, mask defects and metallization uniformity)
- IEEE ECTC papers on glass core substrate and TGV metallization (glass core build-up, void-free TGV copper fill and RDL interface reliability)
- IEEE analysis of particle- and non-particle-induced void sources in chip-to-wafer hybrid bonding (back-grinding tape residue as the dominant particle source; polymer-targeted cleaning cuts particles by roughly 90%)
- LPKF LIDE laser-induced deep etching technical documentation (modified-region etch rate roughly two orders of magnitude higher)
- imec backside power delivery extreme wafer thinning study (remaining silicon held in the few-hundred-nanometer range)
- Chemical inertness test (acetone and IPA solvent immersion and swelling evaluation)
- Visual and microscopic inspection (peel residue rate evaluation)
- RCA clean (wafer wet cleaning)
- Hot NMP stripper (high-energy resist removal via chemical swelling degradation)
- O₂ plasma ashing (residue-free high-energy resist removal)

**In this article:** Abstract · Yield Traps in Wet Processing: Bath Poisoning, Undercut and Residue · How Masking Adhesives Fail in Aggressive Chemistry and High Shear · SCITEO Wet-Process Application Guide · Wet-Process Mask Adhesive Selection Reference · Bath Chemistry and Interface Sealing

# Abstract

**Bottom line (BLUF):** wet processing has exactly three hard things to defend. Bath chemistry poisoned by auxiliary materials. Etchant creeping sideways under the mask edge (undercut). Peel residue that turns into voids at downstream interfaces. All three trace back to one upstream variable: the temporary masking material that enters the bath with the wafer. Four thresholds can be checked on the line: no leaching after 30 days of continuous immersion in acetone and IPA, no swelling or edge lift after 60 minutes in a pH 1-13 window, edge undercut held to ≤2 μm in HF mixed acid and 10%–20% sulfuric acid, and 0% peel residue. SCITEO's temporary strippable masking and temporary bonding systems close all three paths with one dense crosslinked network.

Advanced wet processing is the chemical foundation of advanced packaging. TSV (Through-Silicon Via) and bumping copper plating must achieve void-free bottom-up superfilling from an acidic sulfate electrolyte. Wafer wet etching and cleaning must hold pattern boundaries in HF mixed acid and sulfuric acid. Glass substrates and panel-level packaging introduce TGV (Through-Glass Via) metallization and glass-carrier temporary bonding. Backside power delivery (BSPDN) brings nanoscale TSV etching and wafer thinning into the wet-process chain. MEMS and RF devices depend on sacrificial-layer wet release. On those process chains, the three defect classes that concentrate the most yield loss line up one to one: an entire plating tank scrapped by organic contamination, etchant reaching beneath the mask edge and destroying the circuitry below, and post-strip residue that turns into interfacial voids in downstream hybrid bonding and lithography.

Over the past year or two, the pressure point on this chain has moved forward. Intel has published validation of its glass core substrate from core vias and metallization through multilayer routing, with photonics integration folded into the same platform; Samsung Electro-Mechanics has pushed Glass-Core carriers to 150 mm × 150 mm. At the same time, TGV metallization is widely considered the last link in customer qualification still open: premature via-mouth closure, center voids and interfacial delamination hold via-fill yield at 70% to 85%. For a wet-process engineer, that says one thing: the chemical window of the mask and plating-maskant material is being promoted from an auxiliary parameter to a primary yield variable.

What follows runs in failure-chemistry order. First come the three collapse paths a mask takes inside the bath, then each one is reduced to an acceptance line a process engineer can verify. SCITEO runs its own chemical-inertness, rheology and peel test capability, so the immersion curves, leached total organic carbon (TOC) and peel residue rate cited here are first-party measurements. The application surface spans wafer front-end etching, TSV and glass-substrate metallization, microwave cavity selective silver plating, 3C localized metallization, and backside power delivery and MEMS release.

## Core Parameter Comparison

In wet processing, every difference between mask adhesives eventually shows up in a measurable quantity. The table below puts SCITEO and industry-typical protective adhesives on the same set of metrics:

| Parameter | SCITEO Solution | Industry Typical | Test Standard |
|---|---|---|---|
| Strong polar solvent immersion (acetone and IPA) | 30 days, no anomalies | Swelling or leaching | Chemical inertness test |
| Acid/base immersion (pH 1-13) | 60 minutes, no anomalies | Swelling or edge lift | Chemical inertness test |
| TSV sulfuric acid (10-20%) | No permeation | Permeation and side-leakage | In-house method |
| HF mixed-acid penetration resistance | No lateral undercut | Lateral undercut | In-house method |
| UV cure time | 5 s | 30 s and above | In-house method |
| Fluid scouring in an 80 °C plating bath | No peel-off | Torn off | In-house method |
| Elongation at break (PUA grade) | 210-300% | Below 50% | ASTM D412 |
| Peel residue rate | 0% (peels off in one sheet) | Visible residue | Visual and microscopy |
| 30-day soak leached TOC | <5 ppm | Tens of ppm | In-house method |
| High-energy resist removal compatibility | O₂ plasma ashing and hot NMP | Not compatible | In-house method |

# Yield Traps in Wet Processing: Bath Poisoning, Undercut and Residue

When a wet-process engineer sees plating voids, edge leakage or over-etched features, the first reflex is to check rectifier waveforms, anode condition, spray pressure or bath chemistry. Calibrate every tool parameter and the main-salt concentration, and the excursion still returns periodically. Trace the failed sample backward, and the problem often sits at the contact interface between the masking adhesive and the hot bath.

On a TSV or bumping copper plating line, the symptom that hurts most is bath life shortening for no obvious reason. Void-free bottom-up superfilling in high-aspect-ratio vias depends entirely on ppm-level organic additives working together: an accelerator such as bis(sodium sulfopropyl) disulfide (SPS) competes for adsorption at the via bottom to raise deposition rate, a suppressor such as polyethylene glycol (PEG) covers the via mouth and sidewalls under chloride bridging to hold deposition back, and a leveler suppresses the surface tip effect. If the UV mask or temporary bonding adhesive that enters the bath with the wafer is under-crosslinked, the acidic copper sulfate electrolyte slowly extracts small oligomers, residual photoinitiator or plasticizer from it. Once those unidentified organics enter the bath, they occupy the active adsorption sites on the copper surface; on cyclic voltammetric stripping (CVS) monitoring they show up as a distorted effective additive concentration, and at the wafer they turn into rough nodules on the copper pillars, premature mouth closure and micro-voids at the via center.

The other high-frequency failure at etch and localized plating stations is edge leakage and lateral undercut. A production bath is not a static container: 60 °C to 80 °C bath temperature, mechanical agitation, spray impact and even ultrasonic cavitation apply continuous dynamic shear to the adhesive interface. Machined texture and micron-scale roughness on metal parts, connectors or wafer surfaces already form capillary channels. Once the protective adhesive swells even slightly in hot sulfuric acid, HF mixed acid or an alkaline electroless bath, interfacial adhesion drops and bath chemistry climbs along the interfacial micro-gap. In an isotropic wet etch, acid under the mask means vertical etching and lateral etching lose control together: a boundary that had to stay sharp turns into a serrated notch, and in the worst case turbulence peels the film off whole and scraps an entire lot of high-value substrate.

After the workpiece survives the acid and comes out of the plating bath, stripping usually hides one more trap. Many conventional maskants buy grip in a hot plating bath by making interfacial adhesion as hard as possible, and neglect the cohesive toughness of the film itself. After hot strong-acid exposure, polymer chains embrittle through over-crosslinking or degrade through hydrolysis; when an operator peels by hand or with a fixture, the film breaks on the substrate. Switch to a strong solvent soak plus long ultrasonic agitation, and the cycle time stretches, a large volume of hazardous waste appears, and submicron residue left in micro-pits contaminates the freshly plated gold or silver layer, then turns into delamination and particles during thermocompression bonding, lithography or optical assembly.

![SCITEO R&D team analysis of deep-via superfilling and bath aging: an axonometric TSV cutaway showing chloride bridging, SPS accelerator enriching at the via bottom and PEG suppressor holding the mouth and sidewalls, so deposition inverts bottom-up and prevents premature closure and center voids; at right, the inhibitor/accelerator coverage crossover with depth; below, the pulse-reverse waveform (5-20 ms forward, 0.5-2 ms reverse) redistributing mouth-enriched accelerator, plus SPS reduction to MPS, leveler protecting-group hydrolysis and mask oligomer leaching that narrow the superfilling window, with CVS and on-line TOC bath-maintenance criteria](https://www.sciteo.com/images/articles/wet-process2.svg)

# How Masking Adhesives Fail in Aggressive Chemistry and High Shear

When the tool side has been checked and rechecked, only one explanation usually survives: the temporary protective layer that goes into the bath with the workpiece failed first. Conventional resins fail in three places, and the three feed each other. Once bath chemistry opens a path along the interface, interfacial adhesion and cohesion start degrading together.

Extraction and Bath Poisoning: ordinary UV adhesives and low-crosslink epoxy systems lack crosslink density. Give them enough time in an acidic or alkaline plating bath and unreacted monomers and plasticizers are extracted into the bath, disturbing surface tension and the electrochemical balance and triggering bubbles or full-tank scrap. The root cause is insufficient solvent barrier capability in the crosslinked network, and an acid or alkali rating alone will not reveal it.

Interfacial Adhesion Collapse: some masking adhesives optimize chemical resistance and leave mechanical strength behind. Hot chemistry softens the layer first, then bath agitation applies continuous fluid shear, and the interfacial shear strength between adhesive and substrate drops to zero; the film washes away whole and leaves large areas unplated. Low surface energy on glass, ceramics and polished metals amplifies the problem.

Cohesive Failure and Residue: after hot strong-acid exposure, polymer chains in ordinary masks embrittle, and the film breaks at its cohesive strength rather than at the interface. It cannot be pulled off in one sheet, so mottled residue stays behind on rough substrates. That residue later becomes particle contamination and interfacial voids in hybrid bonding, lithography and wire bonding. One step saved upstream, three steps paid for downstream.

# SCITEO Wet-Process Application Guide

For the two failure classes (auxiliary-material poisoning of the main process and mechanical detachment), SCITEO designs the crosslinked network and the interfacial anchoring separately and takes each one to its limit: the network side uses specialty polymer hybridization and dense three-dimensional crosslinking to shut down solvent pathways, while the interface side matches polar groups and rheology so the film stays put in the bath.

## Semiconductor: Wafer Wet-Etch Masking and TSV/Bumping Copper Plating Protection

At the semiconductor front-end and mid-end (MEOL) wet stations, a wafer passes through standard RCA cleaning (SC-1 ammonia-hydrogen peroxide and SC-2 hydrochloric acid-hydrogen peroxide), a 10%–20% sulfuric acid activation before TSV copper plating, and the HF mixed acid used to etch silicon and oxide. Routine adhesives turn white and lift within about ten minutes in these baths; SCITEO's wafer-grade corrosion-resistant masking system holds no swelling and no leaching after 30 days of continuous immersion in industrial acetone and IPA, holds dimensions and boundaries after 60 minutes in a pH 1-13 acid/base aqueous window, and measures leached total organic carbon (TOC) below 5 ppm over that 30-day extraction. Organic leaching that low means even a large wafer batch cycling through the bath will not disturb the local adsorption balance between SPS and the suppressor in the acidic copper plating electrolyte.

For undercut, the hardest problem in wet etching, laboratory cross-section analysis shows that side-etch width scatter usually comes not from etchant concentration drift but from whether the coated and cured mask still has micro-pinholes, thin step coverage (edge thinning) or cure-shrinkage microcracks at the edge of the non-patterned area. HF molecules are small and penetrate aggressively, and any microcrack becomes a preferential entry path for acid. SCITEO uses thixotropic rheology control so the adhesive forms a full rounded bead over wafer steps and non-patterned edges instead of thinning out; a dense fluorosilicone and alicyclic hybrid crosslinked network then blocks hydrogen fluoride penetration, holding edge undercut within 2 μm through continuous HF mixed-acid and sulfuric-acid etching at 60 °C to 80 °C.

For a wafer-grade highly crosslinked acid-resistant mask, how the film comes off after the step directly sets downstream yield. The series is fully compatible with standard high-energy resist removal: it can be removed by controlled chemical swelling in a hot NMP (N-methyl-2-pyrrolidone) stripper, or sent straight into an O₂ plasma ashing chamber for residue-free vaporization, so no organic film reaches the subsequent copper-to-copper hybrid bonding or fine lithography.

![SCITEO corrosion-resistant strippable masking adhesive for wet etching and wafer wet processing: a cleanroom wet bench where a wafer cassette is submerged in a DIW ultra-clean rinse tank, the tool panel reading resistivity 18.2 MΩ·cm, temperature 23.8 °C and flow, with non-patterned areas masked by a temporary protective adhesive resistant to HF mixed acid and 10-20% sulfuric acid and peeled off in one sheet at 0% residue](https://www.sciteo.com/images/articles/wet-process1.webp)

## Glass Substrates and Panel-Level Packaging: TGV Wet Metallization and Glass-Carrier Temporary Bonding

Advanced packaging is moving from round wafers to rectangular panels, and glass substrates and glass carriers are the key platforms for this generation, carrying both mechanical support and interconnection on two routes at once: glass core substrates and panel-level fan-out packaging (FOPLP). The intrinsic advantages are quantifiable: a tunable CTE of 3-9 ppm/°C that aligns with silicon's thermal expansion (roughly 2.6-3.2 ppm/°C), surface roughness controllable at the nanometer scale for fine-pitch routing, and a dissipation factor of roughly 0.002 to 0.003 at 10 GHz that is lower than most organic carriers. Alkali-free glass formulations also hold mobile ions (Na⁺, K⁺) down to CMOS-compatible levels, keeping front-end devices free of contamination. The trade-off is equally clear: low surface energy, weak bonding to metallization layers and high brittleness. Wet processes land exactly on that weakness.

The mainstream TGV route is laser-induced deep etching (LIDE): an ultrafast laser direct-writes a modified track inside the glass without removing any material and without lithography, then the whole glass sheet goes through an isotropic wet etch in which the modified regions dissolve roughly two orders of magnitude faster than the untouched ones, leaving the through-via behind. Isotropy cuts both ways on this route. It delivers low-roughness sidewalls and controllable taper, and it also means the etch advances sideways at the same time. Any local defect in the mask (pinhole, thin edge, cure microcrack) gets amplified into via-position offset and pattern destruction.

Via formation is followed by deep-hole plating: bottom-up superfilling from an acidic sulfate electrolyte depends on the difference in additive adsorption between via bottom and via mouth. Deposition that closes the mouth too early traps a void at the center; small leakage at the mask edge shifts the local current-density distribution and amplifies both void and seam risk. The seed layer is mostly a PVD Ti/Cu stack (tens of nanometers of adhesion layer under a copper seed in the hundred-nanometer range), and above an aspect ratio of 10:1 the shadowing effect thins or even breaks the copper seed at the via bottom. A 5°–15° sidewall taper helps sputtered atoms reach the bottom, which is why taper is managed as a process window, not eliminated as a defect.

In this chain, masking and temporary protection become first-order variables. A glass carrier must provide rigid support through thinning, backside alignment and redistribution layer (RDL) processing, and the temporary bonding layer fixes ultra-thin glass to a silicon or glass carrier while cycling through temperature excursions along with the carrier. Wet baths and resist removal sit between those steps; once the bonding layer takes on edge ingress or exposes a low-adhesion interface, warpage and overlay error grow together. SCITEO adapts polar groups and rheology to the glass-to-metallization interface, delivering sharp masking boundaries in TGV plating and RDL patterning and combining chemical resistance with low-stress debonding in glass-carrier bonding.

## Defense and Aerospace: Selective Silver/Gold Plating on Microwave Cavities and RF Filters

Phased-array radar T/R modules, aerospace waveguide cavities and base-station RF filters widely use aluminum or magnesium alloy cavities with complex geometry, and require highly conductive localized silver or gold plating, or electroless nickel, on designated trace areas inside the cavity, while the non-conductive mounting surfaces must be tightly masked. Aluminum grows a native oxide almost immediately, and defense silver and gold plating baths typically run at 70 °C to 80 °C in strong alkaline, cyanide or strongly complexing chemistry, with vigorous mechanical agitation and cathode movement on top.

Conventional shops handle these cavities by hand-taping high-temperature PET green tape and then brushing on a solvent-borne peelable lacquer. Around dense resonator posts, narrow fillets, threaded holes and step joints inside the cavity, tape simply cannot seat, and it leaves bridge gaps too small to see; hot chemistry floods the gap as soon as the part enters the bath, and peeling after plating reveals metal flash and burrs from edge leakage. At microwave frequencies the skin effect concentrates current in the metal surface, so even tens of microns of serrated burr on the plating-stop boundary change cavity resonance and degrade passive intermodulation (PIM) and insertion loss. SCITEO's high-adhesion corrosion-resistant liquid maskant covers three-dimensional dead zones by automated dispense or spray; specialty polar groups penetrate the thin native oxide on aluminum and form a dense crosslinked film, holding a knife-sharp plating-stop boundary under 80 °C convection and removing the rework cost of hand-scraping plated burrs.

## Precision 3C Structural Parts and Irregular Substrates

Smartphone metal midframes, smart wearable cases, magnesium-aluminum AR-glasses frames and high-precision connector terminals all involve localized PVD coating protection, localized gold or nickel plating, localized electroless nickel immersion gold (ENIG), or masking for a second anodizing pass. These parts share many three-dimensional curves, narrow chamfers, high volume and extremely strict appearance and contact-resistance inspection.

For ambient and mid-temperature plating, electroless plating and anodizing masking and removal, SCITEO's specialty polyurethane acrylate (PUA) UV strippable system is built around automated dispensing and high-speed hand peeling, balancing rheology against mechanics. The adhesive carries a matched thixotropic index: it neither sags nor collapses when dispensed on 3D curves, slopes and narrow edges, and 5 seconds under a 365 nm UV LED completes deep cure, so it drops straight into a high-speed automated line.

To close the contradiction between detachment in the bath and breakage at peel, the PUA formulation pushes elongation at break of the cured film to 210% to 300% (measured to ASTM D412) while holding tensile modulus in the 2-14 MPa flexible band. In plating and anodizing baths with ultrasonic agitation, the film locks the substrate edge through high interfacial shear strength and delivers zero edge leakage; after rinsing and drying, the film's tear strength is far above the interfacial peel force, so an operator only lifts one corner with tweezers or an automatic peeler and pulls the whole film off in one continuous piece, like peeling a silicone sheet, with no fracture across the section and 0% physical residue. The process needs no methyl ethyl ketone, toluene or strong alkaline stripper for a second clean, which protects mirror-finish metal and gold contacts and removes the VOC permitting and waste treatment overhead.

## Leading-Edge Extensions: Backside Power Delivery Thinning and MEMS Wet Release

As advanced logic moves into the 2 nm and angstrom-class nodes, backside power delivery (Intel PowerVia and the TSMC A16 Super Power Rail architecture) has become the standard route out of front-side routing congestion and IR drop. The process flips a wafer with completed front-end devices and bonds it to a carrier wafer, then thins the silicon substrate from hundreds of microns down to the few-hundred-nanometer range, and finally opens the backside contacts and forms nanoscale through-silicon vias (nTSVs) by selective wet etching with TMAH (tetramethylammonium hydroxide) or mixed acid.

At that thickness the silicon has no rigidity left; all mechanical support and stress buffering sit on the temporary bonding adhesive. Once the bonding layer takes edge chemical attack or micron-scale swelling in the subsequent selective wet etch, SPM (sulfuric acid-hydrogen peroxide mixture) clean or multi-pass wet strip, the local stress release converts immediately into wafer-level in-plane distortion, pushing backside lithography alignment past a tolerance measured in a few nanometers and driving backside contact resistance up or the circuit open. SCITEO's temporary bonding and edge-sealing system for advanced thinning treats very low CTE mismatch, resistance to strong acid and base wet attack, and low moisture uptake as base formulation constraints, and holds the particle and residue budget after final debond cleaning.

The other zero-tolerance scenario for mask residue is wet release of MEMS inertial sensors, silicon microphones and RF filters. When HF or BOE (buffered oxide etchant) dissolves the silicon dioxide sacrificial layer to free cantilevers, diaphragms and other movable microstructures, the pads and peripheral circuits outside the release area must be tightly masked with an HF-resistant protective adhesive. If that adhesive leaches trace organic oligomers during a long BOE soak, the organics change surface tension in the microstructure gaps and act as a bonding mediator when the wafer moves to the DIW rinse and dry step, sharply amplifying capillary-driven stiction and permanently disabling the micromechanical resonator. SCITEO's wet-process-compatible protection system holds zero leaching and dimensional stability through the BOE release window, then peels clean by mild dry or solvent-specific removal, protecting dynamic and static yield of the MEMS cavity.

# Wet-Process Mask Adhesive Selection Reference

The failure paths above condense into a table that can be checked row by row: process step on the left, failure mode in the middle, and the process window plus technical direction in the two columns on the right.

| Process Step | Dominant Failure Mode | Process Window and Acceptance Line | SCITEO Technical Direction |
|---|---|---|---|
| TSV/bumping copper plating | Bath poisoning, plating voids | No leaching after 30-day solvent immersion, pH 1-13 tolerance, cure rate, edge sealing | UV strippable mask adhesive |
| Wafer wet etching | Lateral undercut, edge lift | HF and sulfuric acid permeation resistance, interfacial adhesion | HF-resistant etch protection adhesive |
| Glass-substrate TGV metallization | Low adhesion on glass, plating leakage | Polar-group anchoring, boundary sharpness, low-stress debonding | Temporary bonding and masking systems |
| Panel-level packaging and glass carriers | Edge stress concentration, amplified warpage | Large-area thickness uniformity, bath resistance, low-residue debonding | Temporary bonding adhesive |
| Microwave cavity selective silver plating | Fluid-scour detachment, boundary flash | Shear-resistant adhesion at 80 °C, plating-stop boundary accuracy | High-adhesion corrosion-resistant mask adhesive |
| 3C irregular-part localized plating | Poor curved-surface conformity, residue | Elongation at break, cohesion, 0% residue | PUA UV strippable adhesive |
| MEMS wet release | Structure stiction, organic residue | Controllable swelling, selective removal, low outgassing | Wet-process compatible protection systems |

# Bath Chemistry and Interface Sealing

A wet line runs stable on two foundations: bath chemistry equilibrium and mask interface sealing. Whether the job is micron-scale deep-via copper fill for wafer-level TSV and glass-substrate TGV, or localized metallization on microwave cavities and precision 3C parts, a temporary masking material that leaches or lifts in the bath turns every later investment in tool upgrades and chemistry maintenance into damage control. SCITEO Advanced Materials works from the customer's actual bath composition, acid/base concentration, immersion temperature window and resist-removal equipment to deliver targeted rheology tuning, polar anchoring adaptation and first-party immersion-extraction engineering support.

This article is SCITEO Advanced Materials original technical content; unauthorized reproduction is prohibited.

## Appendix: Process & Engineering Adhesive FAQ Index

### During wafer bumping copper plating, why does bath life suddenly shorten and the plated copper pillars turn rough?

Ordinary UV adhesives leach slowly into acidic copper plating baths. The released monomers compete with the bath accelerators for adsorption sites, disrupt the electrochemical deposition rate, and show up as rough deposits and shortened bath life. SCITEO's high-crosslink-density wafer-grade protection system holds a dense network with no leaching after 30 days of continuous immersion in acetone and IPA, and stays dimensionally stable in a pH 1-13 acid/base window, remaining inert toward the plating chemistry and closing the bath-poisoning path upstream.

### When plating 3D irregular metal parts, the liquid masking adhesive is washed off by agitator flow and leaves large areas unplated. How do we solve it?

This is interfacial shear failure. Fluid dynamics inside a plating tank are far more aggressive than a static soak, and a mask that offers chemical resistance without high interfacial adhesion will be torn open by hot turbulence. SCITEO UV strippable mask cures in 5 s and forms stable physical anchoring on metal substrates, holding full masking coverage under high-velocity flow and ultrasonic agitation.

### With adhesion that strong, is post-plating stripping difficult or likely to leave ghost residue?

No. Conventional adhesives trade adhesion against removability. SCITEO UV strippable mask uses a polyurethane elastomer architecture that gives the film high cohesion and strong fracture toughness. It stays conformal to the substrate through bulk tension in the tank, then resists brittle fracture during stripping so the film comes off as one intact sheet with 0% physical residue, removing the need for a solvent-based second strip.

### During glass-substrate TGV plating, the mask tends to lift and let plating leak through. Is this a material problem or a process problem?

Low surface energy on glass makes bonding to organic materials inherently weak, which is the material-level root cause; fluid scouring and temperature swings in the wet bath amplify it. Start by checking whether the lift is uniform around the boundary. Uniform lift around the full perimeter usually points to insufficient interfacial adhesion, and calls for a masking system with polar-group anchoring. Localized lift points first to cleaning residue and pre-treatment consistency. SCITEO designed its glass-carrier and TGV metallization systems around polar-group compatibility and low-stress debonding.

### During HF mixed-acid etching, the non-patterned edge keeps undercutting while the film lifts. How should we troubleshoot?

Undercut and lift appearing together means both network density and interfacial adhesion need review. First confirm whether the film swells under hot concentrated acid, because swelling opens permeation paths; then inspect the edge seal for pinholes or thin coverage. SCITEO corrosion-resistant grades use a high-crosslink-density permeation barrier that suppresses lateral undercut in HF mixed acid and 10% to 20% sulfuric acid, is validated through a 60-minute pH 1-13 acid/base immersion window, and remains compatible with both hot NMP and O₂ plasma ashing for high-energy resist removal.

### Wet etching is isotropic. Can undercut be pushed down by retuning process parameters?

Narrower, yes; zero, no. HF has no directionality when it dissolves glass or silicon oxide, so any pinhole, thin edge or cure microcrack in the mask becomes a preferential entry path, and local attack grows into via-position offset and pattern destruction. Mask defects are themselves an independent cause of etch defects, so fixing the mask comes before tuning the process: confirm full cure, uniform edge coverage and an interface with no lift, then judge undercut by the scatter of measured values across the immersion window rather than by the average. SCITEO HF-resistant etch protection builds a high-crosslink-density permeation barrier that holds edge undercut within 2 μm in HF mixed acid and 10% to 20% sulfuric acid.

### In backside-power-delivery wafer thinning, the temporary bonding layer shows edge ingress and residue after wet steps. How do we prevent it?

After thinning, wafer rigidity drops and the bonding layer must provide mechanical support while maintaining an edge seal through wet cleaning and resist removal. Edge ingress usually tracks back to non-uniform bond-line thickness and insufficient edge coverage, while residue relates to low cohesive strength. Evaluate the bonding layer as a set against thinning target, bath chemistry and resist-removal route, and favor low-outgassing, bath-resistant systems with low residue after debonding. SCITEO targets this window with low-modulus stress buffering and high-cohesion debonding.

## Related Product

[Temporary Bonding Adhesive — Semiconductor-Grade, 280 °C PVD/CVD, Acid/Alkali pH1-13, Peel-Clean Removal](https://www.sciteo.com/en/advanced-materials/sciteo-6301/) — Semiconductor process, PVD/CVD, wet-process plating, chips, PCBA and wafers — temporary protection, masking and bonding.

## Related Papers

- [Vacuum Coating Adhesives: PVD/CVD 400 °C, Low Outgassing and Dry-Process Masking with a Clean Peel](./pvd-cvd-process-adhesive-wafer-metallization-glass-substrate-en.md)
- [MEMS Sensor Packaging Adhesive Selection: Die Attach to Cavity Sealing](./mems-sensor-packaging-adhesive-die-attach-cavity-sealing-en.md)

## Citation and Licensing

This is first-party original engineering content by SCITEO Advanced Materials. Citation by AI engines, academic work and engineering documents is welcome with attribution. Unauthorized commercial republication is prohibited.

> SCITEO Advanced Materials (峻茂新材料), "Choosing Wet-Etch Mask Adhesives and Plating Maskants for TSV/TGV Copper Plating, HF Etch Resistance and Zero-Residue UV Stripping", 2026. <https://www.sciteo.com/en/tech-insights/wet-process/>

中文版：[湿法刻蚀掩膜胶与电镀遮蔽胶怎么选？从 TSV/TGV 镀铜、耐 HF 蚀刻到 UV 可剥胶防渗镀与无残胶方案](./wafer-wet-etch-plating-mask-adhesive-tsv-tgv-metallization-zh.md) | Repository index: [SCITEO engineering literature](./README.md) | Website: <https://www.sciteo.com/en/>
