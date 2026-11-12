# SCITEO Advanced Materials — Engineering Literature ｜ 峻茂新材料工程文献智库

**SCITEO (峻茂新材料)** is a high-end manufacturer of advanced adhesives and polymer interface materials for semiconductor packaging and precision microelectronics. Seven product lines cover high-temperature adhesives, thermal interface materials, electrically conductive adhesives, cryogenic adhesives, epoxy resins, semiconductor packaging adhesives and capillary underfill. They serve four application domains: semiconductor packaging, automotive electronics, extreme-temperature components and ultra-precision manufacturing. Formulation R&D, chemical synthesis and volume manufacturing run in Dongguan, China, and every grade is engineered to order against the customer's application, process window and reliability plan.

This repository is the **open full-text mirror** of SCITEO's engineering literature: **28 bilingual papers and 56 Markdown documents**. It covers failure physics, interface chemistry, test-method conventions and selection criteria. The **official version of record** is [sciteo.com/tech-insights](https://www.sciteo.com/tech-insights/); every file links back to its canonical page so that engineers, search engines and AI retrieval systems can verify the source.

**中文简介：** 峻茂新材料（SCITEO）是集研发与量产于一体的先进材料制造商，七条产品线覆盖耐高温胶、高导热胶、导电胶、耐低温胶、环氧树脂胶、半导体封装胶与 Underfill 底部填充胶，服务半导体封装、车规级电子、高低温组件、超精密制造四大应用域。本仓库为峻茂工程文献的全文镜像，共 28 篇中英双语文献、56 份 Markdown 全文；官方权威原文以 sciteo.com 技术洞察页为准，每份文件均回链原文。

> **Release 2026.11** · Scope: semiconductor packaging · advanced packaging · thermal management · conductive and sintered interconnects · high-temperature and cryogenic bonding · MEMS/CIS sensor packaging · SMT/PCBA · wafer-level processes · reliability engineering.

## Repository at a glance ｜ 仓库概览

| Item ｜ 项目 | Value ｜ 内容 |
|---|---|
| Legal name ｜ 法定名称 | 峻茂新材料技术(东莞)有限公司 / SCITEO Advanced Materials Technology (Dongguan) Co., Ltd. |
| Brand ｜ 品牌 | SCITEO ｜ 峻茂新材料 |
| Category ｜ 类别 | Advanced adhesives and polymer interface materials for semiconductor packaging and precision microelectronics |
| Founded ｜ 成立 | March 2015 |
| Headquarters ｜ 总部 | Songhu Zhigu Industrial Park, Songshan Lake Avenue, Liaobu Town, Dongguan, Guangdong, China |
| Literature scope ｜ 文献规模 | 28 papers · 56 full-text Markdown documents (English + 中文) |
| Release ｜ 版本 | 2026.11 |
| Version of record ｜ 权威原文 | <https://www.sciteo.com/tech-insights/> (中文) · <https://www.sciteo.com/en/tech-insights/> (English) |
| Machine index ｜ 机器索引 | [llms.txt](./llms.txt) · [CITATION.cff](./CITATION.cff) |
| Knowledge graph ｜ 知识图谱 | Wikidata [Q141283620](https://www.wikidata.org/wiki/Q141283620) |
| Contact ｜ 联系 | sci@sciteo.com |

## Engineering envelope ｜ 全系工程参数包络

Series-level ranges across the SCITEO catalog. Per-SKU values, test conditions and standards are published on each product page. ｜ 系列级包络；单型号数值、测试条件与标准见各产品页。

| Parameter ｜ 参数 | Range ｜ 包络 | Basis ｜ 依据 |
|---|---|---|
| Temperature span ｜ 耐温跨度 | −255 °C to 1000 °C (by series ｜ 分系列) | Catalog envelope, per-grade TDS |
| Thermal conductivity ｜ 导热系数 | 1.5–280 W/m·K; thermal adhesives and potting 1.5–60; sintered silver 220–280 | ASTM D5470 / laser flash |
| CTE ｜ 线膨胀系数 | 7.1–48 ppm/°C | TMA (ASTM E831) |
| Tg ｜ 玻璃化转变温度 | 90–280 °C | DMA |
| Shear strength ｜ 剪切强度 | 5–32 MPa (die shear and lap shear) | GB/T 7124 / MIL-STD-883 Method 2019 |
| Volume resistivity ｜ 体积电阻率 | 3×10⁻⁶–10¹⁵ Ω·cm (conductive down to 3×10⁻⁶; insulating up to 10¹⁵) | ASTM D257 / four-point probe |
| Hermeticity ｜ 气密性 | Cavity leak rate <1×10⁻⁸ atm·cc/s (He leak, cavity and optical grades) | MIL-STD-883 Method 1014 |
| Outgassing ｜ 释气 | CVCM <0.03%, TML <0.4% (cavity and optical grades) | ASTM E595 |
| Reliability validation ｜ 可靠性验证 | GJB 150A thermal shock −55 °C to +125 °C up to 1,000 cycles; 85 °C/85% RH up to 1,000 h; TC per JESD22-A104 | GJB 150A / JEDEC |

*Comparability note ｜ 可比性说明:* reliability ranges span different chemistries and different test conditions. Grade-level conditions, values and standards are published on each product page and in each paper's Standards Reference block. ｜ 可靠性区间跨不同体系与不同测试条件，单档条件、数值与标准见产品页与各文献的标准出处块。

## Articles ｜ 文献总览 (28 papers · 56 documents)

| # | Domain ｜ 领域 | English full text | 中文全文 | Version of record ｜ 权威原文 |
|---|---|---|---|---|
| 1 | High-temperature | [How to Select a High-Temperature Adhesive: 200–1000 °C Ultra-High-Temp Grades, Sensor Packaging and Semiconductor Process Bonding](./high-temperature-adhesive-selection-200-1000c-sensor-semiconductor-en.md) | [耐高温胶水怎么选？200–1000 °C 耐超高温胶、传感器芯片封装与半导体高温制程粘接](./high-temperature-adhesive-selection-200-1000c-sensor-semiconductor-zh.md) | <https://www.sciteo.com/tech-insights/extreme-high-temp-adhesive/> |
| 2 | Thermal interface | [High-Temp Thermal Adhesive Selection: 20-60 W/m·K TIMs for 400 °C Service, IGBT/SiC Modules and Compute Chips](./high-temperature-thermal-adhesive-20-60w-igbt-power-module-en.md) | [耐高温导热胶怎么选？20-60 W/m·K 高导热、400 °C 耐温与 IGBT 功率模块、算力芯片界面热管理解析](./high-temperature-thermal-adhesive-20-60w-igbt-power-module-zh.md) | <https://www.sciteo.com/tech-insights/high-temp-thermal-adhesive/> |
| 3 | Conductive | [How to Select a High-Temp Conductive Adhesive: From 300 °C SiC Die Attach to 1000 °C Sensor Interconnect](./high-temperature-conductive-adhesive-300c-sic-1000c-aviation-sensor-en.md) | [耐高温导电胶怎么选？从 300 °C SiC 芯片封装到 1000 °C 传感器的导电互连方案](./high-temperature-conductive-adhesive-300c-sic-1000c-aviation-sensor-zh.md) | <https://www.sciteo.com/tech-insights/high-temp-conductive-adhesive/> |
| 4 | Reliability | [Why Packaging Adhesives Fail Temperature Cycling and 85/85: Cracking, Damp-Heat Bias and Tg Collapse](./semiconductor-adhesive-reliability-tc-cycling-85-85-tg-collapse-en.md) | [为什么冷热循环和双85 很难通过？胶粘剂温度循环开裂、双85 湿热偏压与 Tg 塌陷失效机理](./semiconductor-adhesive-reliability-tc-cycling-85-85-tg-collapse-zh.md) | <https://www.sciteo.com/tech-insights/adhesives-tc-ths-reliability-failures/> |
| 5 | Semiconductor packaging | [How to Choose Semiconductor Packaging Adhesives: Die Attach, Wire-Bond Encapsulation and Flip-Chip Underfill](./semiconductor-packaging-adhesive-die-attach-wire-bond-underfill-en.md) | [半导体封装胶怎么选？从芯片固晶贴装(Die Attach)、引线键合包封到 Flip-Chip 底部填充的全链用胶方案](./semiconductor-packaging-adhesive-die-attach-wire-bond-underfill-zh.md) | <https://www.sciteo.com/tech-insights/semi-packaging/> |
| 6 | Wide-temperature | [How to Select a Wide-Temperature Adhesive: −70 °C to 300 °C Bonding, CTE Matching and Crack-Free Sealing](./wide-temperature-adhesive-70c-300c-cte-matching-thermal-shock-en.md) | [耐高低温胶水怎么选？-70 °C 到 300 °C 宽温域粘接的 CTE 匹配、粘接密封防开裂](./wide-temperature-adhesive-70c-300c-cte-matching-thermal-shock-zh.md) | <https://www.sciteo.com/tech-insights/wide-temp-adhesive/> |
| 7 | Advanced packaging | [From 3nm GAAFET to CoWoS-L Heterogeneous Integration: Wafer-Bond Cleanliness, Thermal Stress and Interface Adhesive Failure Modes](./advanced-packaging-interface-materials-gaafet-cowos-l-en.md) | [从 3nm GAAFET 到 CoWoS-L 异构集成：晶圆键合洁净度、热应力与封装用胶失效解析](./advanced-packaging-interface-materials-gaafet-cowos-l-zh.md) | <https://www.sciteo.com/tech-insights/semiconductor-process/> |
| 8 | High-temperature | [Why High-Temperature Adhesives Fail: Softening, Debonding, Cracking and Carbonization at 300-500 °C](./high-temperature-adhesive-failure-mechanisms-300-500c-quantum-sensor-en.md) | [耐高温胶水为什么会失效？300-500 °C 高温胶粘剂软化、脱胶、开裂与碳化的技术解析](./high-temperature-adhesive-failure-mechanisms-300-500c-quantum-sensor-zh.md) | <https://www.sciteo.com/tech-insights/high-temp-adhesive/> |
| 9 | Conductive | [Chip-Grade Conductive Silver Adhesive Selection: Die Attach Adhesive, Pressureless Sintered Silver and Interface Engineering for AI Compute, Automotive SiC and Medical Imaging](./conductive-die-attach-adhesive-ai-heterogeneous-medical-imaging-en.md) | [芯片级导电银胶怎么选？固晶胶、无压烧结银与 AI 算力、车规 SiC、医疗影像的粘接界面工程](./conductive-die-attach-adhesive-ai-heterogeneous-medical-imaging-zh.md) | <https://www.sciteo.com/tech-insights/conductive-die-attach/> |
| 10 | Thermal interface | [High-Thermal-Conductivity Adhesive Selection: Test-Method Conventions, Bond Line Thickness and 100 W/cm²-Class Thermal Interface Design](./high-thermal-conductivity-adhesive-thermal-resistance-100w-cm2-en.md) | [高导热胶怎么选？从导热系数测试口径、BLT 胶层厚度到 100 W/cm² 级散热界面设计](./high-thermal-conductivity-adhesive-thermal-resistance-100w-cm2-zh.md) | <https://www.sciteo.com/tech-insights/high-thermal-conductivity/> |
| 11 | Reliability | [Anti-Aging Epoxy Life-Cycle Reliability: Damp Heat, Thermal Cycling, Salt Spray, and Accelerated Life Models](./anti-aging-epoxy-adhesive-damp-heat-thermal-cycling-life-prediction-en.md) | [耐老化胶全寿命可靠性：湿热老化、冷热循环、盐雾油蚀与加速寿命预测模型](./anti-aging-epoxy-adhesive-damp-heat-thermal-cycling-life-prediction-zh.md) | <https://www.sciteo.com/tech-insights/anti-aging-epoxy/> |
| 12 | MEMS & sensors | [MEMS Sensor Packaging Adhesive Selection: Die Attach to Cavity Sealing](./mems-sensor-packaging-adhesive-die-attach-cavity-sealing-en.md) | [MEMS 传感器封装胶怎么选？从固晶贴装到腔体密封的界面工程](./mems-sensor-packaging-adhesive-die-attach-cavity-sealing-zh.md) | <https://www.sciteo.com/tech-insights/mems-packaging/> |
| 13 | High-temperature | [How to Select High-Temperature Potting Compounds: Insulation and Hermetic Sealing for 400 °C Sensors, Semiconductor Chambers, and High-Voltage Drives](./high-temperature-potting-400c-sensor-high-voltage-motor-en.md) | [耐高温灌封胶怎么选？400 °C 高温传感器、半导体设备与高压电驱的灌封密封解析](./high-temperature-potting-400c-sensor-high-voltage-motor-zh.md) | <https://www.sciteo.com/tech-insights/high-temp-potting/> |
| 14 | Semiconductor packaging | [How to Select Underfill and Chip Encapsulant: Capillary Flow, Void Control and Crack Resistance from Flip-Chip and BGA/CSP to Advanced Packaging](./underfill-adhesive-cowos-l-hbm4-glass-substrate-void-control-en.md) | [底部填充胶 (Underfill) 怎么选？从倒装芯片、BGA/CSP 到先进封装的毛细流动、空洞控制与抗开裂选型](./underfill-adhesive-cowos-l-hbm4-glass-substrate-void-control-zh.md) | <https://www.sciteo.com/tech-insights/underfill/> |
| 15 | Conductive | [Semiconductor-Grade Die-Attach Conductive Silver Adhesive: Adhesion, Volume Resistivity and Thermal Conduction Trade-Offs, Plus Resin Bleed-Out, Void and Silver-Migration Control](./die-attach-conductive-silver-adhesive-resistivity-thermal-sintering-en.md) | [半导体级导电银胶选型：粘接力、体积电阻率与导热协同，及树脂渗出、空洞与银迁移防控](./die-attach-conductive-silver-adhesive-resistivity-thermal-sintering-zh.md) | <https://www.sciteo.com/tech-insights/die-conductive-silver-adhesive/> |
| 16 | Modules | [Module Packaging Adhesives for Humanoid Joints, 1.6T Optics and Power](./module-packaging-adhesive-ai-compute-humanoid-robot-joint-rf-en.md) | [模组封装胶怎么选？人形机器人关节、1.6T 光模块与算力电源的导热灌封及光学粘接解析](./module-packaging-adhesive-ai-compute-humanoid-robot-joint-rf-zh.md) | <https://www.sciteo.com/tech-insights/module-packaging/> |
| 17 | PCBA | [How to Select High-Density PCBA Encapsulants: Board-Level Sealing, Underfill and Piezo-Jet Dispensing Interface Failure Mechanisms](./high-density-pcba-packaging-adhesive-sip-underfill-jet-dispensing-en.md) | [高密度 PCBA 封装胶怎么选？板级密封、底部填充与压电喷射点胶的界面失效机理](./high-density-pcba-packaging-adhesive-sip-underfill-jet-dispensing-zh.md) | <https://www.sciteo.com/tech-insights/pcba-packaging/> |
| 18 | High-temperature | [How to Select 300 °C High-Temp Epoxy: Tg, CTE, and Interface Reliability](./high-temperature-epoxy-adhesive-300c-sensor-motor-insulation-en.md) | [耐 300 °C 高温环氧树脂胶怎么选？精密传感器、半导体设备与高端电机绝缘的耐热粘接密封解析](./high-temperature-epoxy-adhesive-300c-sensor-motor-insulation-zh.md) | <https://www.sciteo.com/tech-insights/high-temp-epoxy/> |
| 19 | Cryogenic | [Cryogenic Adhesive Selection: −55 °C to −255 °C Bonding Failure Physics and Interface Materials for LNG, Liquid Hydrogen, Superconducting Magnets and Quantum Computing](./cryogenic-adhesive-minus-55-to-255c-liquid-nitrogen-helium-bonding-en.md) | [耐低温胶水怎么选？-55 °C 至 −255 °C 超低温与液氮液氦工况的深冷粘接失效机理](./cryogenic-adhesive-minus-55-to-255c-liquid-nitrogen-helium-bonding-zh.md) | <https://www.sciteo.com/tech-insights/low-temperature-resistant-adhesive/> |
| 20 | Low-temperature | [Low-Temperature Cure Conductive Silver Adhesive: 80 °C Cure, Silver Network and Contact Resistance](./low-temperature-cure-conductive-silver-adhesive-60-80c-thermal-budget-en.md) | [低温固化导电银胶怎么选？80 °C 低温导电胶剪切强度、接触电阻控制与热敏器件互连](./low-temperature-cure-conductive-silver-adhesive-60-80c-thermal-budget-zh.md) | <https://www.sciteo.com/tech-insights/low-temp-cure-conductive/> |
| 21 | SMT | [SMT Cold Solder Joints, Solder Voids and Head-in-Pillow: 008004 and SiP Vacuum Reflow](./smt-solder-void-head-in-pillow-008004-vacuum-reflow-en.md) | [SMT 虚焊、焊点空洞与枕头效应怎么解决？008004 微元件与 SiP 真空回流焊工艺解析](./smt-solder-void-head-in-pillow-008004-vacuum-reflow-zh.md) | <https://www.sciteo.com/tech-insights/smt-adhesive/> |
| 22 | Low-temperature | [Low-Temp Cure Adhesive Selection: 60-80 °C Epoxy for Thermal-Sensitive Packaging and Optical Bonding](./low-temperature-curing-adhesive-60-80c-thermal-sensitive-packaging-en.md) | [低温固化胶怎么选？60-80 °C 环氧树脂胶、热敏元器件封装与光学粘接选型](./low-temperature-curing-adhesive-60-80c-thermal-sensitive-packaging-zh.md) | <https://www.sciteo.com/tech-insights/low-temp-curing/> |
| 23 | Wafer process | [Choosing Wet-Etch Mask Adhesives and Plating Maskants for TSV/TGV Copper Plating, HF Etch Resistance and Zero-Residue UV Stripping](./wafer-wet-etch-plating-mask-adhesive-tsv-tgv-metallization-en.md) | [湿法刻蚀掩膜胶与电镀遮蔽胶怎么选？从 TSV/TGV 镀铜、耐 HF 蚀刻到 UV 可剥胶防渗镀与无残胶方案](./wafer-wet-etch-plating-mask-adhesive-tsv-tgv-metallization-zh.md) | <https://www.sciteo.com/tech-insights/wet-process/> |
| 24 | Wafer process | [Vacuum Coating Adhesives: PVD/CVD 400 °C, Low Outgassing and Dry-Process Masking with a Clean Peel](./pvd-cvd-process-adhesive-wafer-metallization-glass-substrate-en.md) | [真空镀膜用胶怎么选？PVD/CVD 耐 400 °C 高温、低释气与干法工艺无残胶遮蔽可去胶](./pvd-cvd-process-adhesive-wafer-metallization-glass-substrate-zh.md) | <https://www.sciteo.com/tech-insights/semi-pvd/> |
| 25 | MEMS & sensors | [CIS Image Sensor Packaging Adhesive: Automotive CMOS, Optical Chip WLCSP/TSV and Glass-Lid Cavity Bonding](./cis-image-sensor-packaging-adhesive-automotive-tsv-active-alignment-en.md) | [CIS 图像传感器封装胶怎么选：车规 CMOS、光学芯片晶圆级封装(WLCSP/TSV)与玻璃盖板空腔键合](./cis-image-sensor-packaging-adhesive-automotive-tsv-active-alignment-zh.md) | <https://www.sciteo.com/tech-insights/cis-packaging/> |
| 26 | Materials | [One-Component Heat-Cure Silicone: Sealed-Cavity Deep Cure, Interfacial Stress and Stencil Printing](./one-part-heat-cure-thermal-silicone-adhesive-stencil-printing-en.md) | [单组份加温固化硅胶怎么选？封闭腔体深层固化、界面应力与钢网印刷](./one-part-heat-cure-thermal-silicone-adhesive-stencil-printing-zh.md) | <https://www.sciteo.com/tech-insights/silicone-adhesive/> |
| 27 | Connectors | [Connector and Harness Potting Compound Selection: Mil-Spec Thermal Shock, AI Data Center Module Connectors and Medical Harness Sealing Solutions](./connector-harness-potting-adhesive-military-thermal-shock-automotive-medical-en.md) | [连接器与线束灌封胶怎么选？军标冷热冲击、AI数据中心模块接头与医用线束的密封方案](./connector-harness-potting-adhesive-military-thermal-shock-automotive-medical-zh.md) | <https://www.sciteo.com/tech-insights/connector-adhesives/> |
| 28 | UV curing | [Semiconductor-Grade UV-Cure Adhesive: AA Alignment, Black Light-Shielding Deep Cure and Chip-Level UV-Thermal Dual Cure](./uv-curing-adhesive-active-alignment-black-shadow-deep-cure-en.md) | [半导体级 UV 光固化胶怎么选？AA 主动对准、黑色遮光胶的深层固化与芯片 UV 热双重固化技术解析](./uv-curing-adhesive-active-alignment-black-shadow-deep-cure-zh.md) | <https://www.sciteo.com/tech-insights/semi-uv-adhesive/> |

## Start here by engineering question ｜ 按工程问题检索

| Engineering question ｜ 工程问题 | English paper | 中文文献 |
|---|---|---|
| Why do high-temperature adhesives fail inside the rated window at 300–500 °C? | [Why High-Temperature Adhesives Fail: Softening, Debonding, Cracking and Carbonization at 300-500 °C](./high-temperature-adhesive-failure-mechanisms-300-500c-quantum-sensor-en.md) | [中文](./high-temperature-adhesive-failure-mechanisms-300-500c-quantum-sensor-zh.md) |
| How do I select an adhesive that survives 200–1000 °C in sensor packaging and semiconductor process? | [How to Select a High-Temperature Adhesive: 200–1000 °C Ultra-High-Temp Grades, Sensor Packaging and Semiconductor Process Bonding](./high-temperature-adhesive-selection-200-1000c-sensor-semiconductor-en.md) | [中文](./high-temperature-adhesive-selection-200-1000c-sensor-semiconductor-zh.md) |
| Why do packaging adhesives fail temperature cycling and 85/85 damp heat, and which parameters should I check first? | [Why Packaging Adhesives Fail Temperature Cycling and 85/85: Cracking, Damp-Heat Bias and Tg Collapse](./semiconductor-adhesive-reliability-tc-cycling-85-85-tg-collapse-en.md) | [中文](./semiconductor-adhesive-reliability-tc-cycling-85-85-tg-collapse-zh.md) |
| How do I select underfill for flip-chip, CoWoS-L, HBM4 and glass substrates? | [How to Select Underfill and Chip Encapsulant: Capillary Flow, Void Control and Crack Resistance from Flip-Chip and BGA/CSP to Advanced Packaging](./underfill-adhesive-cowos-l-hbm4-glass-substrate-void-control-en.md) | [中文](./underfill-adhesive-cowos-l-hbm4-glass-substrate-void-control-zh.md) |
| Chip-grade conductive silver or pressureless sintered silver for AI compute, automotive SiC and medical imaging? | [Chip-Grade Conductive Silver Adhesive Selection: Die Attach Adhesive, Pressureless Sintered Silver and Interface Engineering for AI Compute, Automotive SiC and Medical Imaging](./conductive-die-attach-adhesive-ai-heterogeneous-medical-imaging-en.md) | [中文](./conductive-die-attach-adhesive-ai-heterogeneous-medical-imaging-zh.md) |
| How do I reach ≤0.05 °C·cm²/W at a 20–25 μm bond line for 100 W/cm²-class interfaces? | [High-Thermal-Conductivity Adhesive Selection: Test-Method Conventions, Bond Line Thickness and 100 W/cm²-Class Thermal Interface Design](./high-thermal-conductivity-adhesive-thermal-resistance-100w-cm2-en.md) | [中文](./high-thermal-conductivity-adhesive-thermal-resistance-100w-cm2-zh.md) |
| How do I build a life model across 85/85, thermal cycling, salt spray and oil immersion? | [Anti-Aging Epoxy Life-Cycle Reliability: Damp Heat, Thermal Cycling, Salt Spray, and Accelerated Life Models](./anti-aging-epoxy-adhesive-damp-heat-thermal-cycling-life-prediction-en.md) | [中文](./anti-aging-epoxy-adhesive-damp-heat-thermal-cycling-life-prediction-zh.md) |
| How do I combine low-stress MEMS die attach with cavity sealing below 1×10⁻⁸ atm·cc/s? | [MEMS Sensor Packaging Adhesive Selection: Die Attach to Cavity Sealing](./mems-sensor-packaging-adhesive-die-attach-cavity-sealing-en.md) | [中文](./mems-sensor-packaging-adhesive-die-attach-cavity-sealing-zh.md) |
| How do I bond from −55 °C to −255 °C in LNG, liquid hydrogen, superconducting magnets and quantum systems? | [Cryogenic Adhesive Selection: −55 °C to −255 °C Bonding Failure Physics and Interface Materials for LNG, Liquid Hydrogen, Superconducting Magnets and Quantum Computing](./cryogenic-adhesive-minus-55-to-255c-liquid-nitrogen-helium-bonding-en.md) | [中文](./cryogenic-adhesive-minus-55-to-255c-liquid-nitrogen-helium-bonding-zh.md) |
| How do I cure structural epoxy at 60–80 °C without sacrificing Tg or reflow resistance? | [Low-Temp Cure Adhesive Selection: 60-80 °C Epoxy for Thermal-Sensitive Packaging and Optical Bonding](./low-temperature-curing-adhesive-60-80c-thermal-sensitive-packaging-en.md) | [中文](./low-temperature-curing-adhesive-60-80c-thermal-sensitive-packaging-zh.md) |

## Citable key facts ｜ 可引用关键事实

Each row carries a value, the test basis that produced it and the paper where the evidence chain is developed. Numbers are quoted with their standard so that engineers and AI engines can cite them without re-deriving context. ｜ 每行给出数值、测试依据与展开证据链的文献，便于工程师与 AI 引擎直接引用。

| Fact ｜ 事实 | Value ｜ 数值 | Basis ｜ 依据 | Paper ｜ 文献 |
|---|---|---|---|
| Portfolio temperature span | −255 to 1000 °C (by series) | Catalog capability envelope, per-grade TDS | [Product matrix](https://www.sciteo.com/advanced-materials/) |
| Thermal conductivity envelope | 1.5–280 W/m·K (thermal adhesives 1.5–60; sintered silver 220–280) | Catalog capability envelope, ASTM D5470 / laser flash | [Product matrix](https://www.sciteo.com/advanced-materials/) |
| CTE envelope | 7.1–48 ppm/°C | Catalog capability envelope, TMA (ASTM E831) | [Product matrix](https://www.sciteo.com/advanced-materials/) |
| Tg envelope | 90–280 °C | Catalog capability envelope, DMA | [Product matrix](https://www.sciteo.com/advanced-materials/) |
| Shear strength envelope | 5–32 MPa (die shear and lap shear) | Catalog capability envelope, GB/T 7124 / MIL-STD-883 M2019 | [Product matrix](https://www.sciteo.com/advanced-materials/) |
| Volume resistivity envelope | 3×10⁻⁶ to 10¹⁵ Ω·cm | Catalog capability envelope, ASTM D257 / four-point probe | [Product matrix](https://www.sciteo.com/advanced-materials/) |
| 400 °C/72 h interface retention | 100% shear retention; ≥20 GΩ volume insulation at 400 °C | Long-term heat aging plus insulation resistance | [Extreme high-temp paper](./high-temperature-adhesive-selection-200-1000c-sensor-semiconductor-en.md) |
| 300–500 °C failure window | Tg 190–240 °C; modulus plateau 10–25 GPa; CTE 7.5–25 ppm/°C; ≥80% shear after 250 °C/500 h | DMA, TMA, GB/T 7124, JESD22-A103 | [High-temp failure paper](./high-temperature-adhesive-failure-mechanisms-300-500c-quantum-sensor-en.md) |
| TC1000 and 85/85 retention | ≥28 MPa after 1,000 TC cycles; >24 MPa after 1,000 h at 85/85; Tg >140 °C | JESD22-A104F.01, JESD22-A101D | [Reliability paper](./semiconductor-adhesive-reliability-tc-cycling-85-85-tg-collapse-en.md) |
| Underfill thermal and void anchors | CTE 13 ppm/°C; Tg 150–160 °C; 6 W/m·K; voids <0.1%; shear 29–32 MPa | TMA, DMA, ASTM D5470, C-SAM | [Underfill paper](./underfill-adhesive-cowos-l-hbm4-glass-substrate-void-control-en.md) |
| Chip-grade conductive silver | 3×10⁻⁵ Ω·cm; 19 MPa on gold; mobile ions <10 ppm | ASTM D257, GB/T 7124, ion chromatography | [Die-attach silver paper](./die-attach-conductive-silver-adhesive-resistivity-thermal-sintering-en.md) |
| Pressureless sintered silver | 3×10⁻⁶ Ω·cm; 160–280 W/m·K; bond line 10–25 μm | Four-point probe, laser flash / ASTM E1461 | [Conductive die-attach paper](./conductive-die-attach-adhesive-ai-heterogeneous-medical-imaging-en.md) |
| Hermetic cavity and outgassing | Leak rate <1×10⁻⁸ atm·cc/s; CVCM <0.03%; TML <0.4% | MIL-STD-883 Method 1014, ASTM E595 | [CIS packaging paper](./cis-image-sensor-packaging-adhesive-automotive-tsv-active-alignment-en.md) |
| Cryogenic bonding | Service to −255 °C; KIC ≥5.3 MPa√m at 77 K; 50 LN₂ cycles without cracking | Cryogenic mechanical testing and LN₂ shock cycling | [Cryogenic paper](./cryogenic-adhesive-minus-55-to-255c-liquid-nitrogen-helium-bonding-en.md) |
| Low-temperature cure conductive | 80 °C/60 min; 4×10⁻⁵ Ω·cm; Tg 120 °C; 18 MPa die shear | DSC/DMA, ASTM D257, die shear | [Low-temp conductive paper](./low-temperature-cure-conductive-silver-adhesive-60-80c-thermal-budget-en.md) |
| 400 °C potting | 1.3×10¹⁰ Ω at 300 °C/48 h; 2.5 W/(m·K); 96% shear after 400 °C/360 h | GB/T 31838.2, ASTM D5470, GB/T 7124 | [High-temp potting paper](./high-temperature-potting-400c-sensor-high-voltage-motor-en.md) |
| 300 °C epoxy | Tg 280 °C; CTE 7.5–48 ppm/°C; ≥92% shear after 300 °C × 72 h | DMA, TMA, GB/T 7124 | [High-temp epoxy paper](./high-temperature-epoxy-adhesive-300c-sensor-motor-insulation-en.md) |
| High-temp thermal interface | 2.5–60 W/m·K; Td5 425 °C; 26 MPa shear; CTE 10 ppm/°C | ASTM D5470, TGA, GB/T 7124, TMA | [High-temp TIM paper](./high-temperature-thermal-adhesive-20-60w-igbt-power-module-en.md) |
| Wide-temperature service | −70 to 300 °C; TC1500 ≥95%; THS1500 ≥90%; cure shrinkage <0.06% | GJB 150.5A, JESD22-A104/A101, ISO 2577 | [Wide-temp paper](./wide-temperature-adhesive-70c-300c-cte-matching-thermal-shock-en.md) |
| 008004 SMT process window | Area ratio ≥0.66 (0.75 for micro-components); transfer ≥95%; void rate <2%; warpage ≤0.05 mm/inch | IPC J-STD-001, IPC-7095E, 3D SPI/AOI/AXI | [SMT paper](./smt-solder-void-head-in-pillow-008004-vacuum-reflow-en.md) |
| UV-cure optical locking | Volume shrinkage <0.6%; black-adhesive deep cure 1.5–2.0 mm; >85% pull-force after 85/85 1000 h | ISO 2577, JESD22-A101, pull testing | [UV-cure paper](./uv-curing-adhesive-active-alignment-black-shadow-deep-cure-en.md) |
| Connector and harness potting | −55 to +150 °C; 1,000 thermal shocks; 26 MPa on copper; >10¹⁴ Ω·cm | GJB 150.5A, ASTM D257, lap shear | [Connector paper](./connector-harness-potting-adhesive-military-thermal-shock-automotive-medical-en.md) |
| Anti-aging life anchors | ≥90% shear after 1,000 h at 85/85; ≥95% after 1,000 TC; 28 MPa after 30 days salt spray | JESD22-A101/A104, ISO 9227:2022 | [Anti-aging paper](./anti-aging-epoxy-adhesive-damp-heat-thermal-cycling-life-prediction-en.md) |

## Standards and test frameworks ｜ 标准与试验体系

- **JEDEC:** JESD22-A101D (85/85 THB), JESD22-A103 (HTSL), JESD22-A104F.01 (TC), JESD22-A106B.01 (TS), JESD22-A110E (bHAST), JESD22-A118 (uHAST), JESD22-A102 (PCT), JESD47K, J-STD-020F, J-STD-035A.
- **Automotive:** AEC-Q100 Rev-J1 (Grade 0/1), AEC-Q104 (multichip modules), ECPE AQG 324 (power modules).
- **Military and aerospace:** GJB 150.3A/150.4A/150.5A/150.9A/150.11A, GJB 548B, MIL-STD-883 Method 2019/1014.
- **ASTM:** D5470 (thermal conductivity), E595 (outgassing), D257 (volume resistivity), E831 (TMA), E1131 (TGA), D896 (chemical resistance), D3045 (heat aging), D2739 (contact resistance), D2557 (cryogenic tensile), D412 (tensile), D792 (density).
- **ISO / IEC:** ISO 2577 (shrinkage), ISO 9227:2022 (neutral salt spray), IEC 60112 (CTI), IEC 60034-18-41, IEC 61215.
- **IPC:** IPC-7095E (BGA design and assembly), IPC J-STD-001, IPC/JEDEC J-STD-020/035.
- **GB/T:** GB/T 7124 (lap shear), GB/T 2791 (T-peel), GB/T 1034 (water absorption), GB/T 2423.3 (damp heat), GB/T 31838.2 (volume resistance).

## How to cite ｜ 引用方式

**Plain text ｜ 纯文本**

> SCITEO Advanced Materials (峻茂新材料). "SCITEO Advanced Materials — Engineering Literature", 2026.11. Official version of record: <https://www.sciteo.com/tech-insights/>. Full-text mirror: <https://github.com/sciteo/SCITEO-Industrial-and-Semiconductor-Adhesives>.

**BibTeX**

```bibtex
@techreport{sciteo_engineering_literature_2026,
  author      = {{SCITEO Advanced Materials (峻茂新材料)}},
  title       = {SCITEO Advanced Materials --- Engineering Literature},
  institution = {SCITEO Advanced Materials Technology (Dongguan) Co., Ltd.},
  year        = {2026},
  month       = {11},
  url         = {https://www.sciteo.com/tech-insights/},
  note        = {Full-text mirror: https://github.com/sciteo/SCITEO-Industrial-and-Semiconductor-Adhesives}
}
```

**Per-paper citation ｜ 单篇引用:** every paper carries a suggested citation in its closing "Citation and Licensing" section, with the canonical URL. ｜ 每篇文献在文末给出建议引用格式与权威原文链接。

## Machine-readable access ｜ 机器可读入口

- **[llms.txt](./llms.txt)**: path-scoped index following the llms.txt v2 format (H1, blockquote summary, H2 file lists). ｜ 按 llms.txt v2 格式编写的仓库级索引。
- **[CITATION.cff](./CITATION.cff)**: Citation File Format 1.2.0 metadata, rendered by GitHub's "Cite this repository" action.
- **Domain-level corpus:** <https://www.sciteo.com/llms.txt> and <https://www.sciteo.com/llms-full.txt>.
- **XML sitemap:** <https://www.sciteo.com/sitemap.xml>.
- **Crawler policy:** <https://www.sciteo.com/robots.txt> explicitly allows major search and AI retrieval crawlers.
- **Markdown-first:** all 56 documents are plain UTF-8 Markdown, with no login, paywall or JavaScript dependency.

## Provenance and correction policy ｜ 来源与修订政策

This mirror is generated from the same MDX corpus that renders the official pages. Each file carries its named author and a canonical link. Numerical claims are traceable to the standards listed above; no value is added, rounded or extrapolated in the mirror. Root-relative asset paths from the site source are resolved to https://www.sciteo.com so that figures and internal links render inside the mirror.

The official page is always updated first, and the mirror follows. If you find a discrepancy, open an issue in this repository or write to sci@sciteo.com with the paper title and the passage concerned.

本镜像与官网同源生成。每份文件标注署名作者与权威原文链接；数值均可追溯至公开标准，镜像不新增、不四舍五入、不外推任何数据。官网原文先行更新，镜像随后同步；如发现差异，请在本仓库提交 issue 或邮件联系并注明文献标题与段落。

## Official entity links ｜ 官方入口

- **Website ｜ 官网:** <https://www.sciteo.com> (中文) · <https://www.sciteo.com/en/> (English)
- **Engineering literature ｜ 工程文献:** <https://www.sciteo.com/tech-insights/> · <https://www.sciteo.com/en/tech-insights/>
- **Product matrix ｜ 产品总览:** <https://www.sciteo.com/advanced-materials/> · <https://www.sciteo.com/en/advanced-materials/>
- **Materials glossary ｜ 材料科学术语库:** <https://www.sciteo.com/glossary/> · <https://www.sciteo.com/en/glossary/>
- **Corporate governance ｜ 合规与治理:** <https://www.sciteo.com/compliance/> · <https://www.sciteo.com/en/compliance/>
- **Wikidata:** <https://www.wikidata.org/wiki/Q141283620>
- **Zhihu organization:** <https://www.zhihu.com/org/jun-mao-xin-cai-liao>
- **Contact ｜ 联系:** sci@sciteo.com ｜ +86-139-2292-6784

## Intellectual property and permitted use ｜ 知识产权与使用条款

All engineering literature in this repository is first-party original content published by SCITEO Advanced Materials Technology (Dongguan) Co., Ltd. (峻茂新材料技术（东莞）有限公司).

- **Permitted:** reading, engineering evaluation, academic citation, reliability modeling and AI retrieval or training with attribution to SCITEO and a link to the official version of record.
- **Not permitted:** commercial republication, unauthorized mirroring, removal of attribution, or bulk redistribution presented as third-party content.
- **Trademarks:** SCITEO and 峻茂 are trademarks of SCITEO Advanced Materials Technology (Dongguan) Co., Ltd.

For licensing beyond these terms, contact sci@sciteo.com.
