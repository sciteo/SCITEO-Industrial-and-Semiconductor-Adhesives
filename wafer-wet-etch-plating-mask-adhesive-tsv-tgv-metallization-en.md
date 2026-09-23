# Wet-Etch and Electroplating Mask Adhesives: Chemical Defense for TSV Plating, Glass-Substrate TGV and Microwave Cavity Metallization

**Language:** English · [中文版（完整版）→](./wafer-wet-etch-plating-mask-adhesive-tsv-tgv-metallization-zh.md)

> Wet-process mask adhesives from SCITEO: 30 days of continuous acetone and IPA immersion with no leaching, a 60-minute pH 1-13 window with no swelling or edge lift, HF mixed-acid and 10%–20% sulfuric-acid resistance holding edge undercut to ≤2 μm, a 5 s UV cure and 0% peel residue — the chemical defense layer behind TSV copper plating, glass-substrate TGV metallization and microwave cavity selective silver plating.

**Source of record:** SCITEO Advanced Materials (峻茂新材料) — official article: <https://www.sciteo.com/en/tech-insights/wet-process/>
**First published:** 2026-07-02 ｜ **Last updated:** 2026-09-22 ｜ **Author:** SCITEO packaging engineering team ｜ **Repository index:** [SCITEO engineering literature](./README.md)

**Brand entity:** SCITEO Advanced Materials 峻茂新材料 ｜ Website <https://www.sciteo.com/en/> ｜ Products <https://www.sciteo.com/en/advanced-materials/> ｜ Tech insights <https://www.sciteo.com/en/tech-insights/> ｜ Materials glossary <https://www.sciteo.com/en/glossary/>

**Key facts (citable):**

| Item | Value |
|---|---|
| Strong Polar Solvent Immersion (Acetone and IPA) | 30 days, no anomalies |
| Acid/Base Immersion (pH 1-13) | 60 minutes, no anomalies |
| HF Mixed-Acid Penetration Resistance | No lateral undercut |
| Edge Undercut in HF Mixed Acid and Sulfuric Acid | ≤2 μm |
| TSV Concentrated Sulfuric Acid (10-20%) | No permeation |
| UV Cure Time | 5 s |
| Elongation at Break (PUA Grade) | 210-300 % |
| Peel Residue Rate | 0 % |
| Leached Total Organic Carbon (TOC), 30-Day Soak | <5 ppm |
| Service Temperature Range | -45 to 280 °C |
| Tensile Modulus (Low Stress) | 2-14 MPa |

**Quote-ready ｜ 可直接引用：**
> "SCITEO wet-process mask adhesives hold 30 days of acetone and IPA immersion with no leaching, 60 minutes in a pH 1-13 window without swelling or edge lift, ≤2 μm edge undercut in HF mixed acid and 10%–20% sulfuric acid, and 0% peel residue after a 5 s UV cure."

**In this article:** Abstract · Core Parameter Comparison · 1. Yield Traps in Wet Processing: Bath Poisoning, Undercut and Residue · 2. How Masking Adhesives Fail in Aggressive Chemistry and High Shear · 3. SCITEO Wet-Process Application Guide · 4. Wet-Process Mask Adhesive Selection Reference · 5. Conclusion · FAQ · Standards referenced · Related product lines

## Abstract

**Bottom line (BLUF):** wet processing has exactly three hard things to defend. Bath chemistry poisoned by auxiliary materials. Etchant creeping sideways under the mask edge (undercut). Peel residue that turns into voids at downstream interfaces. All three trace back to one upstream variable: the temporary masking material that enters the bath with the wafer. Four thresholds can be checked on the line: no leaching after 30 days of continuous immersion in acetone and IPA, no swelling or edge lift after 60 minutes in a pH 1-13 window, edge undercut held to ≤2 μm in HF mixed acid and 10%–20% sulfuric acid, and 0% peel residue. SCITEO temporary strippable masking and temporary bonding systems close all three paths with one dense crosslinked network.

Advanced wet processing is the chemical foundation of advanced packaging. TSV (Through-Silicon Via) and bumping copper plating must achieve void-free bottom-up superfilling from an acidic sulfate electrolyte. Wafer wet etching must hold pattern boundaries in HF mixed acid and concentrated sulfuric acid. Glass substrates and panel-level packaging introduce TGV (Through-Glass Via) metallization and glass-carrier temporary bonding. Backside power delivery (BSPDN) brings nanoscale TSV etching and wafer thinning into the wet-process chain. MEMS and RF devices depend on sacrificial-layer wet release. On those process chains, the three defect classes that concentrate the most yield loss map onto them one to one: an entire plating tank scrapped by organic contamination, etchant reaching beneath the mask edge and destroying the circuitry below, and post-strip residue that turns into interfacial voids in downstream hybrid bonding and lithography.

What follows runs in failure-chemistry order. First the three collapse paths a mask takes inside the bath, then each one reduced to an acceptance line a process engineer can verify. SCITEO runs its own chemical-inertness, rheology and peel test capability, so the immersion curves, leached total organic carbon (TOC) and peel residue rate cited here are first-party measurements. The application surface spans wafer front-end etching, TSV and glass-substrate metallization, microwave cavity selective silver plating, 3C localized metallization, and backside power delivery and MEMS release.

## Core Parameter Comparison

In wet processing, every difference between mask adhesives eventually shows up in a measurable quantity. The table below puts SCITEO and industry-typical protective adhesives on the same set of metrics:

| Parameter | SCITEO Solution | Industry Typical | Test Standard |
|---|---|---|---|
| Strong polar solvent immersion (acetone and IPA) | 30 days, no anomalies | Swelling or leaching | Chemical inertness test |
| Acid/base immersion (pH 1-13) | 60 minutes, no anomalies | Swelling or edge lift | Chemical inertness test |
| TSV concentrated sulfuric acid (10-20%) | No permeation | Permeation and side-leakage | In-house method |
| HF mixed-acid penetration resistance | No lateral undercut | Lateral undercut | In-house method |
| UV cure time | 5 s | 30 s and above | In-house method |
| Fluid scouring in an 80 °C plating bath | No peel-off | Torn off | In-house method |
| Elongation at break (PUA grade) | 210-300% | Below 50% | ASTM D412 |
| Peel residue rate | 0% (peels off in one sheet) | Visible residue | Visual and microscopy |
| High-energy resist removal compatibility | O₂ plasma ashing and hot NMP | Not compatible | In-house method |

![SCITEO temporary bonding protective adhesive for wet-process electroplating](https://www.sciteo.com/images/articles/wet-process1.webp)

## 1. Yield Traps in Wet Processing: Bath Poisoning, Undercut and Residue

In a wet-process line, engineers watch two balances at once: the chemistry of the bath and the fluid dynamics inside it. Tool drift is the first suspect, but once tool parameters are ruled out one by one, the defect source sits in how auxiliary materials interact with the bath. Wet-process mask adhesive is exactly that class of auxiliary material: it temporarily covers non-patterned areas through etching, plating and cleaning, then peels off whole and never enters the final product. Its depth of chemical defense and its interfacial mechanics tend to set the yield floor.

**Bath Poisoning and Plating Micro-Voids:** advanced plating chemistries hold their superfilling behavior on a precisely balanced additive package. Accelerators raise the deposition rate at the via bottom, suppressors hold back deposition at the mouth and sidewalls, and levelers shave the micro-peaks off the surface; adsorption competition among the three sets the final fill profile. When micro-voids appear inside a deposit or nodules roughen the surface, lab analysis points to unidentified organic contamination in the bath: those species occupy adsorption sites the additives need, disrupt the electrochemical deposition rate, and put an entire tank of specialty chemistry at risk of scrap.

**Etch Side-Leakage and Turbulent Mask Peel-Off:** a production bath is not a static soak. Aggressive mechanical agitation stacks on top of ultrasonic energy, bath temperature typically sits between 60 °C and 80 °C, and acid concentrations run well above bench-test levels. The sulfuric acid system used in TSV processing and the HF mixed acid used in etching both swell and lift the mask edge over non-patterned areas first; once fluid shear opens the interfacial bond, the film detaches over a large area and acid enters from beneath the protected region. Wet etching is isotropic, so once lateral undercut starts it cannot be pulled back by retuning process parameters, and the fine circuitry below is gone.

**Residue Contamination and Secondary Corrosion:** after plating, the temporary protective layer has to come off completely. Removing a hardened resist forces lines into aggressive strippers or extended ultrasonic cleaning. The price is micro-residue that becomes the source of particles and voids in downstream lithography and wire bonding, plus possible corrosion of the freshly formed metal layer.

## 2. How Masking Adhesives Fail in Aggressive Chemistry and High Shear

When the tool side has been checked and rechecked, only one explanation usually survives: the temporary protective layer that goes into the bath with the workpiece failed first. Conventional resins fail in three places, and the three feed each other. Once leaching opens a path into the bath, interfacial adhesion and cohesion start degrading together.

**Extraction and Bath Poisoning:** ordinary UV adhesives and low-crosslink epoxy systems lack crosslink density. Give them enough time in an acidic or alkaline plating bath and unreacted monomers and plasticizers are extracted into the bath, disturbing surface tension and the electrochemical balance and triggering bubbles or full-tank scrap. The root cause is insufficient solvent barrier capability in the crosslinked network, and an acid or alkali rating alone will not reveal it.

**Interfacial Adhesion Collapse:** some masking adhesives optimize chemical resistance and leave mechanical strength behind. Hot chemistry softens the layer first, then bath agitation applies continuous fluid shear, and the interfacial shear strength between adhesive and substrate drops to zero; the film washes away whole and leaves large areas unplated. Low surface energy on glass, ceramics and polished metals amplifies the problem.

**Cohesive Failure and Residue:** after hot strong-acid exposure, polymer chains in ordinary masks embrittle, and the film breaks at its cohesive strength rather than at the interface. It cannot be pulled off in one sheet, so mottled residue stays behind on rough substrates. That residue later becomes particle contamination and interfacial voids in hybrid bonding, lithography and wire bonding. One step saved upstream, three steps paid for downstream.

## 3. SCITEO Wet-Process Application Guide

For the two failure classes (auxiliary-material poisoning of the main process and mechanical detachment), SCITEO designs the crosslinked network and the interfacial anchoring separately and takes each one to its limit: the network side uses specialty polymer hybridization and dense three-dimensional crosslinking to shut down solvent pathways, while the interface side matches polar groups and rheology so the film stays put in the bath.

### 3.1 Semiconductor: Wafer Wet-Etch Masking and TSV/Bumping Copper Plating Protection

**A Dense Network, Verified by Measured Immersion Windows:** at semiconductor grade, RCA cleaning and the 10% to 20% sulfuric acid used in TSV processing sit outside what a routine acid/alkali soak test can describe, so the criteria have to come from measured curves. SCITEO corrosion-resistant grades show no leaching after 30 days of continuous immersion in industrial acetone and isopropyl alcohol (IPA), and stay free of swelling, leaching and edge lift after 60 minutes of continuous immersion in a pH 1-13 acid/base window. Both data points point to the same conclusion: the crosslinked network itself is a dense permeation barrier. Our selection workflow runs that immersion curve to completion first, then validates against the customer's actual bath chemistry in a small-sample review, and recommends the material for production only after swelling and leaching are ruled out. A stable chemical backbone keeps etchants and sulfate ions out of the film, which suppresses HF lateral undercut at the mechanism level. After immersion in HF mixed acid and 10%–20% sulfuric acid at 60–80 °C, edge undercut stays within 2 μm, and leached total organic carbon (TOC) after a 30-day soak stays below 5 ppm, so the plating bath does not have to be dumped because of auxiliary-material leaching.

Undercut scatter usually comes from defects in the mask itself, not from bath chemistry: pinholes in the film, thin edge coverage and microcracks left by incomplete cure all become preferential entry paths for etchant, and each one turns local attack into via-position offset and pattern destruction. Edge-seal acceptance therefore has to be judged on minimum thickness and defect density, not on average film thickness.

**High-Energy Resist Removal Compatibility:** a densely crosslinked film is not suited to conventional mechanical stripping. The system is compatible with back-end high-energy resist removal, supporting hot NMP stripper for chemical swelling and degradation, or O₂ plasma ashing for residue-free carbon removal, so the wafer meets cleanliness requirements before the next step. For wafers entering hybrid bonding, organic residue left after stripping expands into interfacial voids during anneal, so cleanliness at this step sets the yield of the entire stacking chain.

### 3.2 Glass Substrates and Panel-Level Packaging: TGV Wet Metallization and Glass-Carrier Temporary Bonding

Advanced packaging is moving from round wafers to rectangular panels, and glass substrates and glass carriers are the key platforms for this generation, carrying both mechanical support and interconnection on two routes at once: glass core substrates and panel-level fan-out packaging (FOPLP). The intrinsic advantages are quantifiable: a tunable CTE of 3-9 ppm/°C that aligns with silicon's thermal expansion (roughly 2.6-3.2 ppm/°C), surface roughness controllable at the nanometer scale for fine-pitch routing, and a dissipation factor of roughly 0.002 to 0.003 at 10 GHz that is lower than most organic carriers. Alkali-free glass formulations also hold mobile ions (Na⁺, K⁺) down to CMOS-compatible levels, keeping front-end devices free of contamination. The trade-off is equally clear: low surface energy, weak bonding to metallization layers and high brittleness, and wet processes converge exactly on that weakness.

The mainstream TGV route is laser-induced deep etching (LIDE): an ultrafast laser direct-writes a modified track inside the glass without removing any material and without lithography, then the whole glass sheet goes through an isotropic wet etch in which the modified regions dissolve far faster than the untouched ones, leaving the through-via behind. Isotropy cuts both ways on this route. It delivers low-roughness sidewalls and controllable taper, and it also means the etch advances sideways at the same time. Any local defect in the mask (pinhole, thin edge, cure microcrack) gets amplified into via-position offset and pattern destruction.

Via formation is followed by deep-hole plating: bottom-up superfilling from an acidic sulfate electrolyte depends on the difference in additive adsorption between via bottom and via mouth. Deposition that closes the mouth too early traps a void at the center; small leakage at the mask edge shifts the local current-density distribution and amplifies both void and seam risk. The seed layer is mostly a PVD Ti/Cu stack (tens of nanometers of adhesion/barrier under a copper seed in the hundred-nanometer range), and above an aspect ratio of 10:1 the shadowing effect thins or even breaks the copper seed at the via bottom. A 5°–15° sidewall taper helps sputtered atoms reach the bottom, which is why taper is managed as a process window, not eliminated as a defect.

In this chain, masking and temporary protection become first-order variables. A glass carrier must provide rigid support through thinning, backside alignment and redistribution layer (RDL) processing; the temporary bonding layer has to fix ultra-thin glass to a silicon or glass carrier so it survives handling and high-speed scanning vibration, and hold uniform thickness across a large panel to avoid edge stress concentration. Carriers cycle repeatedly between thinning and backside alignment, so stress builds between glass and adhesive and the layer has to combine temperature resistance with stress buffering. That performance is judged on glass transition temperature (Tg) and the storage-modulus curve, not on a single temperature rating. SCITEO temporary strippable masking and temporary bonding systems adapt polar groups and rheology to the glass-to-metallization interface, delivering sharp masking boundaries in TGV plating and RDL patterning, and combining chemical resistance with low-stress debonding for glass carriers. For emerging architectures such as co-packaged optics (CPO) and glass optical waveguides, alignment tolerance has entered the sub-micron range, and cure shrinkage plus debond residue now belong on the interface material checklist.

### 3.3 Defense and Aerospace: Selective Silver/Gold Plating on Microwave Cavities and RF Filters

**Interfacial Anchoring Against Fluid Scouring:** microwave cavities and filters are usually aluminum, which grows a dense native oxide in air and gives conventional resins no stable interface to hold. SCITEO corrosion-resistant grades use specialty polar groups to form physical anchoring on aluminum, and keep a complete boundary under intense mechanical convection in an 80 °C plating bath with a sharp plating-stop edge and no flash. Phased-array radar and microwave filters are acutely sensitive to boundary burrs, a burr changes cavity RF behavior, so edge quality and chemical resistance are the same specification here.

### 3.4 Precision 3C Structural Parts and Irregular Substrates

The 3C masking problem is geometric: high-temperature tape cannot hold a 3D curved surface or a narrow fillet, liquid masking adhesive detaches under hot high-velocity flow, and neither strips cleanly afterward. All three problems tend to land on the same part at the same time.

**Curved-Surface Conformality and Shear-Resistant Adhesion:** SCITEO polyurethane acrylate (PUA) UV strippable adhesive is dispensed across complex curved surfaces and narrow fillets, so conformality no longer depends on manual application, and cures in 5 s under UV. After cure the initial interfacial adhesion is high enough to resist edge-lift and detachment in high-convection baths with ultrasonic agitation, for ambient and mid-temperature wet processes.

**High Cohesion and 0% Residue Peel:** the UV formulation reaches 210% to 300% elongation at break (ASTM D412), so it stretches as one piece instead of fracturing at the tear line. An operator lifts an edge and peels the film off whole, leaving the substrate free of residue and removing the solvent-based second strip entirely. That also removes the secondary corrosion aggressive strippers cause on the metal layer, along with the VOC and waste-stream handling behind it. Peel validation passes only when the film comes off in one piece with no cohesive failure at the tear line, which is the precondition for reproducing a 0% residue rate.

### 3.5 Leading-Edge Extensions: Backside Power Delivery Thinning and MEMS Wet Release

Backside power delivery (BSPDN) moves the power network to the wafer backside and adds wafer-to-wafer bonding, extreme thinning, backside alignment, nanoscale silicon via (nTSV) etching and backside metallization to the flow. Once a wafer is thinned to very low thickness, rigidity drops sharply and mechanical support can only come from the temporary bonding layer. Wet cleaning and resist removal between thinning and backside alignment then raise the bar on chemical resistance and edge sealing. If the bonding layer allows edge ingress during wet processing, warpage and overlay error grow together and eventually show up as higher contact resistance or an open circuit. SCITEO temporary bonding and masking systems carry formulation margin for this temperature and chemistry window, treating low outgassing as the entry condition and debond residue as the closing metric.

Wet release of MEMS and RF devices is another hard class. Sacrificial layer removal relies on HF or buffered oxide etchant (BOE), and released movable structures are prone to capillary-driven stiction, so any residue from the release liquid or the protective layer raises the odds. Protective materials must hold dimensional stability in aggressive chemistry, be selectively removable within the release window, and avoid introducing organic residue into the cavity. SCITEO targets controllable swelling and high-cohesion peeling for these conditions, balancing release selectivity with downstream cleanliness.

## 4. Wet-Process Mask Adhesive Selection Reference

The failure paths above condense into a table that can be checked row by row: process step on the left, failure mode in the middle, criteria and technical direction on the right.

| Process Step | Dominant Failure Mode | Selection Criterion | SCITEO Technical Direction |
|---|---|---|---|
| TSV/bumping copper plating | Bath poisoning, plating voids | No leaching after 30-day solvent immersion, pH 1-13 tolerance, cure rate, edge sealing | UV strippable mask adhesive |
| Wafer wet etching | Lateral undercut, edge lift | HF and sulfuric acid permeation resistance, interfacial adhesion | HF-resistant etch protection adhesive |
| Glass-substrate TGV metallization | Low adhesion on glass, plating leakage | Polar-group anchoring, boundary sharpness, low-stress debonding | Temporary bonding and masking systems |
| Panel-level packaging and glass carriers | Edge stress concentration, amplified warpage | Large-area thickness uniformity, bath resistance, low-residue debonding | Temporary bonding adhesive |
| Microwave cavity selective silver plating | Fluid-scour detachment, boundary flash | Shear-resistant adhesion at 80 °C, plating-stop boundary accuracy | High-adhesion corrosion-resistant mask adhesive |
| 3C irregular-part localized plating | Poor curved-surface conformity, residue | Elongation at break, cohesion, 0% residue | PUA UV strippable adhesive |
| MEMS wet release | Structure stiction, organic residue | Controllable swelling, selective removal, low outgassing | Wet-process compatible protection systems |

## 5. Conclusion

Bath chemistry is the core asset of a wet-process line, and the temporary masking material decides how long that asset holds. Put the four hard thresholds on paper: 30 days of solvent immersion with no leaching, 60 minutes in a pH 1-13 window with no swelling or edge lift, ≤2 μm undercut in HF mixed acid and sulfuric acid, and 0% peel residue. Hold those four and bath poisoning, etch side-leakage and residue contamination all become measurable and trackable. SCITEO pairs high-adhesion, high-cohesion, residue-free UV strippable systems with formulation margin for glass core substrates, panel-level packaging and backside power delivery, handing that acceptance chain to the specific process window.

This article is SCITEO Advanced Materials original technical content; unauthorized reproduction is prohibited.

## FAQ: Wet-Process Mask Adhesive Questions

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

## Standards and Test Methods Referenced

- ASTM D412 Standard Test Methods for Vulcanized Rubber and Thermoplastic Elastomers: Tension
- ASTM D896 Chemical Reagent Resistance of Adhesive Bonds
- GB/T 7124 Adhesives: Determination of Tensile Lap-Shear Strength of Bonded Assemblies
- ASTM E595 Standard Test Method for Total Mass Loss and Collected Volatile Condensable Materials from Outgassing in a Vacuum Environment
- Micromachines review of laser and non-laser through-glass via (TGV) machining (isotropic wet etching, mask defects and metallization uniformity)
- Chemical inertness test (acetone and IPA solvent immersion and swelling evaluation)
- Visual and microscopic inspection (peel residue rate evaluation)
- RCA clean (wafer wet cleaning)
- Hot NMP stripper (high-energy resist removal via chemical swelling degradation)
- O₂ plasma ashing (residue-free high-energy resist removal)

## Related SCITEO Product Lines

The products below map to the wet-process chemistry, masking and temporary-bonding directions discussed in this article. Official product pages carry the full parameter matrix and test standards and can be used directly for selection:

| Wet-process scenario in this article | SCITEO product (official page) |
|---|---|
| Temporary bonding and masking for TSV/bumping plating, glass-substrate TGV metallization and glass carriers (the product associated with this article) | [SC6301 semiconductor-grade temporary bonding adhesive, PVD/CVD compatible](https://www.sciteo.com/en/advanced-materials/sciteo-6301/) ｜ [中文](https://www.sciteo.com/advanced-materials/sciteo-6301/) |
| Rapid UV-cured masking and device-level protection in wafer and packaging flows | [SC6020 UV-curing chip packaging adhesive](https://www.sciteo.com/en/advanced-materials/sciteo-6020/) ｜ [中文](https://www.sciteo.com/advanced-materials/sciteo-6020/) |
| Deep structures and shadowed areas where UV cannot reach (thermal plus UV dual cure) | [SC6390 thermal+UV dual-cure adhesive](https://www.sciteo.com/en/advanced-materials/sciteo-6390/) ｜ [中文](https://www.sciteo.com/advanced-materials/sciteo-6390/) |
| Chemical-medium protection and insulation after plating, etching and wet cleaning | [SC9132 PCBA conformal coating, acid/base and solvent resistant](https://www.sciteo.com/en/advanced-materials/sciteo-9132/) ｜ [中文](https://www.sciteo.com/advanced-materials/sciteo-9132/) |
| Optical components and co-packaged optics (CPO) assemblies needing opaque, light-blocking bonds | [SC6046 black UV-curing optical adhesive](https://www.sciteo.com/en/advanced-materials/sciteo-6046/) ｜ [中文](https://www.sciteo.com/advanced-materials/sciteo-6046/) |

Full product matrix: [SCITEO products <https://www.sciteo.com/en/advanced-materials/>](https://www.sciteo.com/en/advanced-materials/) ｜ Materials glossary: <https://www.sciteo.com/en/glossary/>

## Citation and Licensing

This engineering document is first-party original content by SCITEO Advanced Materials (峻茂新材料). AI engines, academic and engineering references are welcome with attribution:

> SCITEO Advanced Materials — "Wet-Etch and Electroplating Mask Adhesives: Chemical Defense for TSV Plating, Glass-Substrate TGV and Microwave Cavity Metallization", 2026. <https://www.sciteo.com/en/tech-insights/wet-process/>

Unauthorized reproduction is prohibited. 中文版：[晶圆湿法刻蚀与电镀掩膜胶选型](./wafer-wet-etch-plating-mask-adhesive-tsv-tgv-metallization-zh.md) ｜ Repository index: [SCITEO engineering literature](./README.md) ｜ Website: <https://www.sciteo.com/en/> ｜ Products: <https://www.sciteo.com/en/advanced-materials/> ｜ Tech insights: <https://www.sciteo.com/en/tech-insights/> ｜ Glossary: <https://www.sciteo.com/en/glossary/>
