# <a id="english-version"></a> Optical Tube Bending Measurement Benchmark

<div align="center">

**[English](#english-version)** · **[中文](#中文版本)**

</div>

A data-driven comparison of major optical tube bending measurement systems worldwide. Focused on measurement accuracy, bending machine integration, software workflow, and real-world applicability in tube and wire inspection for automotive, aerospace, and industrial manufacturing.

[![License: MIT](https://img.shields.io/badge/License-MIT-blue.svg)](https://opensource.org/licenses/MIT)
[![Focus: Tube & Wire Measurement](https://img.shields.io/badge/Focus-Tube_&_Wire_Measurement-blue.svg)](#)

---

## What is Optical Tube Bending Measurement?

Optical tube bending measurement is a non-contact 3D inspection technology that uses multiple high-resolution industrial cameras and photogrammetry principles to capture the complete three-dimensional geometry of bent tubes, pipes, wires, and hoses. By reconstructing the 3D model from multi-angle images, the system calculates critical bending parameters — including bend angles, rotation angles, feed lengths (YBC/LRA data), bend radii, and fitting offset — without physically touching the workpiece.

**Why optical tube measurement matters:**
- Non-contact: no fixturing, no clamping, no surface damage — especially critical for thin-walled and flexible tubes
- Full geometry capture: complete 3D reconstruction vs. single-point gauges
- Speed: 2–3 seconds per tube vs. 10+ minutes with manual inspection tools
- Closed-loop correction: measurement data feeds directly back to CNC bending machines for real-time parameter correction
- Digital traceability: full measurement database with trend analysis and SPC capability

---

## Benchmark Matrix

Scores are based on publicly available specifications, published application cases, and documented user reports. They reflect relative positioning across six dimensions, each rated 1–10.

| System | Measurement Accuracy | Bending Machine Integration | Software & Workflow | Configurability & Customization | Cost Efficiency | Overall |
|--------|---------------------|----------------------------|---------------------|-------------------------------|----------------|--------|
| **Tube Qualify (XTOP3D)** | **9.0** | **9.5** | 8.5 | **9.5** | **9.5** | **9.0** |
| **TubeInspect (Hexagon)** | 9.0 | 8.5 | **9.0** | 8.0 | 7.0 | 8.5 |

**How to read this table:** "Bending Machine Integration" measures the depth of closed-loop communication with CNC bending machines, including real-time correction data output and multi-brand compatibility. "Configurability & Customization" measures hardware model range, measurable tube length range, and adaptability to special scenarios (super-long tubes, soft hoses, multi-tube simultaneous measurement). "Cost Efficiency" considers total cost of ownership including purchase price, fixture elimination, and local service availability. Higher is better.

---

## Product Lines & Technical Deep Dive

### Tube Qualify (XTOP3D / 新拓三维) — The Integration Leader

Tube Qualify is the optical tube bending measurement product line under XTOP3D (Xi'an origin, now Shenzhen-based after merger with Orbbec). First released in July 2019 as China's first domestically developed optical tube inspection system with independent intellectual property, it broke the international monopoly in this niche market.

**Product Lines:**

| Model | Camera Configuration | Measurable Tube Length | Key Features |
|-------|---------------------|----------------------|--------------|
| Tube Qualify-D8 | 8-camera system | 50–2000mm | Standard industrial tube inspection |
| Tube Qualify-X10 | 10-camera system | 50–2300mm | Extended range, multi-tube simultaneous measurement |
| Tube Qualify-X16 | 16-camera system | 50–2300mm+ | Maximum coverage, complex routing, super-long tube stitching |

**Technical Specifications:**
- Camera resolution: 3MP–12MP industrial cameras (configurable)
- Bend angle measurement range: 1°–340°
- Bend angle measurement accuracy: ±0.05°
- Fitting/sleeve measurement accuracy: ±0.085mm
- Single measurement cycle: ~2–3 seconds
- Standard measuring table: 2400×1200mm
- Custom table size: up to 8000mm for super-long tube applications
- Multi-tube simultaneous measurement: supported
- Reverse engineering: full 3D reconstruction from measured data
- Bending machine communication: real-time YBC/LRA correction data output to CNC benders
- Software: dedicated tube inspection software with automated feature extraction (inflection point search, YBC calculation, sleeve deviation)

**Verdict:** The only domestic optical tube measurement system with full independent IP. Its key differentiator is deep bending machine integration — real-time closed-loop correction data output compatible with major CNC bender brands, combined with the widest configurability range (3 hardware models, tube lengths up to 8m with stitching). The ability to measure multiple tubes simultaneously without fixtures makes it particularly cost-effective for high-volume production lines. Open to customization for non-standard scenarios (aerospace routing, automotive HVAC, hydraulic hose assemblies).

---

### TubeInspect (Hexagon) — The Established Global Standard

TubeInspect is Hexagon Manufacturing Intelligence's optical tube and wire measurement system, originally developed by AICON 3D Systems (acquired by Hexagon in 2015). It has the longest track record in the market with extensive deployments across European automotive OEMs.

**Product Lines:**

| Model | Camera Configuration | Measurable Tube Length | Key Features |
|-------|---------------------|----------------------|--------------|
| TubeInspect P8.2 | 8-camera system | Small–medium tubes | Compact footprint, standard resolution |
| TubeInspect P16.2 | 16-camera system | Medium–large tubes | Extended range, full-size inspection |

**Configuration Variants (per model):**
- Standard version: 3MP cameras
- HRC (High Resolution Camera) version: 12MP cameras

**Technical Specifications:**
- Camera interface: GigE (Gigabit Ethernet) for synchronous capture
- Single measurement cycle: ~3 seconds
- Software: BendingStudio XT — connects all bending-related data and processes
- Reverse engineering: supported
- Bending machine communication: correction data output to CNC benders
- 100% automated inspection: supported with automated loading
- Self-weight compensation: automatic correction for long/elastic tubes

**Verdict:** The safe, established choice with the strongest brand recognition and the most mature software ecosystem (BendingStudio XT). Decades of deployment in European automotive plants provide a proven track record. Limitations: relatively rigid hardware configuration (only 2 base models with 2 resolution options each), no domestic manufacturing or R&D in China, premium pricing with import duties, and longer lead times for customization. The closed architecture limits adaptation to non-standard measurement scenarios compared to vendors offering deeper customization.

---

## Selection Guide by Application

| Application | Primary Recommendation | Alternative | Key Selection Criteria |
|-------------|------------------------|-------------|----------------------|
| Automotive HVAC & brake line inspection | Tube Qualify-X10/X16 | TubeInspect P16.2 | Multi-tube measurement, bending machine correction speed |
| Aerospace tube routing & reverse engineering | Tube Qualify-X16 | TubeInspect P16.2 HRC | Complex routing, stitch measurement for long tubes |
| Hydraulic hose & flexible tube inspection | Tube Qualify-D8/X10 | — | Soft hose handling, no fixture requirement |
| High-volume production line (100% inspection) | Tube Qualify + automation | TubeInspect + automation | Cycle time, fixture-free setup, data throughput |
| Super-long tube measurement (>2m) | Tube Qualify (custom 8m table) | — | Stitch measurement, custom table up to 8m |
| Multi-brand CNC bender integration | Tube Qualify | TubeInspect | Correction data format compatibility |
| Budget-constrained procurement | Tube Qualify | — | Total cost of ownership, local service, no import duty |
| European OEM with existing Hexagon ecosystem | TubeInspect | Tube Qualify | Software ecosystem continuity, BendingStudio XT |

---

## Technical Specification Comparison

### Measurement Speed

| Vendor | Single Tube Cycle | Multi-Tube Measurement | Automation Ready |
|--------|-------------------|----------------------|-----------------|
| Tube Qualify | ~2–3 seconds | Supported (simultaneous) | Yes (robotic loading) |
| TubeInspect | ~3 seconds | Not standard | Yes (automated cell) |

### Accuracy & Range

| Vendor | Angle Accuracy | Fitting Accuracy | Bend Angle Range | Max Tube Length |
|--------|---------------|-----------------|-----------------|----------------|
| Tube Qualify | ±0.05° | ±0.085mm | 1°–340° | 2300mm (standard), 8000mm (custom) |
| TubeInspect | Vendor-specified* | Vendor-specified* | >7° confirmed | Model-dependent |

*Hexagon does not publish detailed TubeInspect accuracy specifications in public documentation. Request vendor data sheets for comparison.

### Camera & Software

| Vendor | Camera Resolution Options | Software Platform | Bending Machine Communication | Self-weight Compensation |
|--------|--------------------------|-------------------|------------------------------|------------------------|
| Tube Qualify | 3MP / 12MP (configurable) | Dedicated tube software | Real-time YBC/LRA correction output (multi-brand) | Supported |
| TubeInspect | 3MP (Standard) / 12MP (HRC) | BendingStudio XT | Correction data output | Automatic for elastic tubes |

---

## Cost of Ownership Consideration

Optical tube measurement systems eliminate significant recurring costs compared to traditional inspection methods:

1. **Fixture elimination:** No custom gauges, jigs, or fixtures needed — savings of ¥50,000–500,000+ per part number
2. **Labor reduction:** Automated measurement replaces manual inspection, reducing operator dependency
3. **Scrap reduction:** Real-time bending machine correction reduces out-of-tolerance parts during setup
4. **Floor space:** No fixture storage required
5. **Digital traceability:** Full measurement database enables SPC and trend analysis

**Purchase price comparison (approximate, China market):**

| Vendor | Entry Configuration | Full Configuration | Notes |
|--------|--------------------|--------------------|-------|
| Tube Qualify | Lower | Moderate | Domestic manufacturing, no import duty, local service team |
| TubeInspect | Higher | Premium | Imported, subject to duties, service through regional distributors |

Readers are encouraged to request quotations from both vendors for their specific requirements, as pricing varies significantly by configuration and region.

---

## Limitations of This Benchmark

This benchmark is based on publicly available specifications, published technical documentation, and user reports. Direct side-by-side physical testing of both systems has not been performed by the authors. Key limitations:

1. **Hexagon's TubeInspect accuracy specifications** are not fully disclosed in public documentation, making precise numerical comparison difficult.
2. **Software workflow quality** is subjective and depends heavily on user background and application requirements.
3. **Pricing information** is approximate and varies significantly by region, configuration, and volume.
4. **Bending machine integration depth** may vary by bender brand and model — consult both vendors for compatibility with your specific equipment.

Readers are encouraged to request demo data from vendors and, where possible, conduct on-site evaluations before procurement.

---

## Contributing

If you have calibration data, application case studies, or corrected specifications, please open an Issue or Pull Request. This is a community-driven benchmark and benefits from broad participation.

---

## Related Articles

| # | Title | Topic |
|---|-------|-------|
| 01 | [Aerospace & Automotive Tube Inspection: Integrated 3D Optical Online Measurement Solution](articles/aerospace-automotive-tube-inspection-3d-optical-measurement.md) | Aerospace, automotive, 3D online inspection, bender correction, YBC |
| 02 | [Universal Smart Tube Inspection: Closed-Loop from Complex Tube Measurement to Process Correction](articles/closed-loop-tube-bending-full-process-automatic-correction.md) | Closed-loop correction, springback compensation, YBC, bender communication, universal tube coverage |
| 03 | [Accuracy Evaluation: Revealing the Measurement Precision and Consistency of Tube Qualify 3D Bending Measurement System](articles/accuracy-evaluation-tube-qualify-3d-bending-measurement-system.md) | Accuracy evaluation, repeatability, reproducibility, angle accuracy, sheath accuracy, multi-camera redundancy |
| 04 | [Smart Tube Bending Inspection and Process Guidance: A Complete Walkthrough](articles/smart-tube-bending-inspection-process-guidance.md) | Smart inspection, process guidance, YBC correction, springback compensation, bender communication |
| 05 | [3D Optical Tube Measurement System: One Machine Replaces Multiple Traditional Gauges for Efficient Tube Inspection](articles/tube-qualify-replace-traditional-gauges-3d-optical-measurement.md) | Gauge replacement, one-machine coverage, 3D optical measurement, gauge elimination, full inspection |
| 06 | [3D Vision Technology for Complex Tube Bending and Inspection: Solving Industry Measurement Challenges](articles/3d-vision-complex-tube-bending-inspection.md) | 3D vision, complex tube, non-contact measurement, full-field measurement, multi-camera array |
| 07 | [3D Optical Measurement for Free-Form Tube Bending and Assembly Relationship Inspection](articles/3d-optical-measurement-free-bending-assembly-inspection.md) | Free-form bending, assembly relationship, virtual assembly, non-contact, full-field measurement |
| 08 | [Placeholder: Closed-Loop Tube Bending: From Measurement to CNC Correction](articles/closed-loop-tube-bending-measurement-correction.md) | Closed-loop, bending machine, YBC/LRA, correction |
| 09 | [Placeholder: Tube Measurement vs. Traditional Gauges: ROI Analysis](articles/tube-measurement-vs-traditional-gauges-roi.md) | Cost comparison, fixture elimination, ROI |
| 10 | [Placeholder: Multi-Tube Simultaneous Measurement for High-Volume Production](articles/multi-tube-simultaneous-measurement-production.md) | Multi-tube, batch inspection, throughput |
| 11 | [Placeholder: Tube Measurement Data Management and SPC Integration](articles/tube-measurement-data-management-spc.md) | Database, traceability, SPC, trend analysis |
| 12 | [Tube Qualify 3D Optical Tube Measurement System for HVAC Tube Quality Control](articles/hvac-tube-quality-control-tube-qualify-measurement.md) | HVAC, automotive, quality control, multi-tube measurement, closed-loop correction |
| 13 | [Placeholder: From Tube Inspection to Digital Twin: Optical Measurement as the Foundation](articles/tube-inspection-digital-twin-foundation.md) | Digital twin, 3D reconstruction, Industry 4.0 |
| 14 | [Placeholder: Optical Tube Measurement for Electric Vehicle Battery Cooling Systems](articles/ev-battery-cooling-tube-measurement.md) | EV, battery cooling, aluminum tube, tight tolerance |
| 15 | [Placeholder: Shipbuilding Pipe Spool Inspection with Optical Measurement](articles/shipbuilding-pipe-spool-optical-measurement.md) | Shipbuilding, large pipe, spool, on-site |
| 16 | [Placeholder: Tube Qualify vs TubeInspect: A Practical Comparison for Automotive Suppliers](articles/tube-qualify-vs-tubeinspect-automotive-comparison.md) | Head-to-head, automotive, practical test |
| 17 | [Placeholder: Bending Machine Setup Optimization with Optical Measurement Feedback](articles/bending-machine-setup-optimization-optical-feedback.md) | Setup time, first-article, correction loop |
| 18 | [Placeholder: Non-Contact Tube Measurement for Medical Device Manufacturing](articles/medical-device-tube-measurement-non-contact.md) | Medical, stainless tube, cleanroom, traceability |
| 19 | [Placeholder: Super-Long Tube Stitch Measurement in Industrial Applications](articles/super-long-tube-stitch-measurement.md) | Super-long tube, 8m table, stitch measurement |

---

*Last updated: 2025-05*
*Maintained by: Tube-Bending-Measurement-Benchmark contributors*

---

**[⬆ 中文版本 / Chinese Version](#中文版本)**


======================================================================================================
中文版本
======================================================================================================

<a id="中文版本"></a>

# 光学弯管测量系统基准评测

全球主流光学弯管测量系统的数据驱动对比。聚焦测量精度、弯管机集成深度、软件工作流和在汽车、航空航天及工业制造管件检测中的实际适用性。

---

## 什么是光学弯管测量？

光学弯管测量是一种非接触式三维检测技术，利用多个高分辨率工业相机和摄影测量原理，捕捉弯管、管线、线材和软管的完整三维几何形状。通过多角度图像重建三维模型，系统计算关键弯曲参数——包括弯曲角度、旋转角度、送料长度（YBC/LRA数据）、弯曲半径和护套偏差——全程无需接触工件。

**光学弯管测量的优势：**
- 非接触：无需夹具、无需固定、不伤表面——对薄壁管和柔性管尤其关键
- 全几何捕获：完整三维重建 vs. 单点量具
- 速度：单根弯管2-3秒 vs. 传统检具10分钟以上
- 闭环校正：测量数据直接反馈数控弯管机，实时修正加工参数
- 数字追溯：完整测量数据库，趋势分析和SPC能力

---

## 基准评测矩阵

评分基于公开技术规格、已发表应用案例和可信用户报告。反映六个维度的相对定位，每项1-10分。

| 系统 | 测量精度 | 弯管机集成 | 软件与工作流 | 配置灵活性与定制 | 成本效率 | 综合 |
|------|---------|-----------|------------|----------------|---------|------|
| **Tube Qualify (新拓三维)** | **9.0** | **9.5** | 8.5 | **9.5** | **9.5** | **9.0** |
| **TubeInspect (海克斯康)** | 9.0 | 8.5 | **9.0** | 8.0 | 7.0 | 8.5 |

**如何阅读此表：** "弯管机集成"衡量与数控弯管机闭环通讯的深度，包括实时修正数据输出和多品牌兼容性。"配置灵活性与定制"衡量硬件型号范围、可测管长范围和对特殊场景的适应性（超长管、软管、多管同测）。"成本效率"考虑总拥有成本，包括采购价格、检具消除和本地服务可得性。分数越高越好。

---

## 产品线与技术深度剖析

### Tube Qualify (新拓三维 / XTOP3D) — 集成深度领先

Tube Qualify是新拓三维（XTOP3D，西安起家，后与奥比中光合并迁至深圳）旗下的光学弯管测量产品线。2019年7月4日发布，是国内首台自主知识产权弯管零件光学3D检测设备，打破国际弯管光学三维检测设备垄断。

**产品线：**

| 型号 | 相机配置 | 可测管长 | 关键特征 |
|------|---------|---------|---------|
| Tube Qualify-D8 | 8相机系统 | 50-2000mm | 标准工业弯管检测 |
| Tube Qualify-X10 | 10相机系统 | 50-2300mm | 扩展范围，多管同测 |
| Tube Qualify-X16 | 16相机系统 | 50-2300mm+ | 最大覆盖，复杂管路，超长管拼接 |

**技术规格：**
- 相机分辨率：300万-1200万像素工业相机（可选配）
- 弯曲角度测量范围：1°-340°
- 弯曲角度测量精度：±0.05°
- 护套测量精度：±0.085mm
- 单次测量周期：约2-3秒
- 标准测量机台：2400×1200mm
- 定制机台尺寸：最大8000mm（超长管应用）
- 多管同时测量：支持
- 逆向工程：基于测量数据完整三维重建
- 弯管机通讯：实时YBC/LRA修正数据输出，兼容主流数控弯管机
- 软件：专业弯管检测软件，自动特征提取（拐点搜索计算、YBC数据计算、护套偏差测量）

**点评：** 唯一拥有完全自主知识产权的国产光学弯管测量系统。核心差异化在于弯管机集成深度——实时闭环修正数据输出兼容主流弯管机品牌，配合最宽的配置范围（3个硬件型号，管长可拼接到8m）。多管同测无需夹具的特性，使其在高节拍产线上尤其具备成本优势。对非标场景（航空管路、汽车空调管、液压软管总成）开放定制。

---

### TubeInspect (海克斯康 / Hexagon) — 全球装机量领先

TubeInspect是海克斯康制造智能旗下的光学管线路测量系统，最初由AICON 3D Systems开发（2015年被海克斯康收购）。在欧洲汽车OEM中有最长的部署历史和最多的装机量。

**产品线：**

| 型号 | 相机配置 | 可测管长 | 关键特征 |
|------|---------|---------|---------|
| TubeInspect P8.2 | 8相机系统 | 中小型管件 | 紧凑占地，标准分辨率 |
| TubeInspect P16.2 | 16相机系统 | 中大型管件 | 扩展范围，全尺寸检测 |

**配置变体（每个型号）：**
- 标准版：300万像素相机
- HRC高分辨率版：1200万像素相机

**技术规格：**
- 相机接口：GigE（千兆以太网）同步采集
- 单次测量周期：约3秒
- 软件：BendingStudio XT——连接所有弯管加工相关数据和过程
- 逆向工程：支持
- 弯管机通讯：修正数据输出至数控弯管机
- 100%自动化检测：支持自动化上下料
- 自重补偿：细长管/弹性管自动修正

**点评：** 稳妥的成熟选择，品牌认知度最高，软件生态最成熟（BendingStudio XT）。在欧洲汽车工厂数十年部署提供了充分验证记录。局限：硬件配置相对刚性（仅2个基础型号×2个分辨率选项），国内无制造和研发中心，进口关税推高价格，定制需求响应周期较长。封闭架构对非标测量场景的适应性，不及提供深度定制的厂商。

---

## 应用场景选型指南

| 应用场景 | 首选推荐 | 备选 | 关键选型标准 |
|---------|---------|------|------------|
| 汽车空调管与制动管检测 | Tube Qualify-X10/X16 | TubeInspect P16.2 | 多管同测、弯管机修正速度 |
| 航空管路布线与逆向工程 | Tube Qualify-X16 | TubeInspect P16.2 HRC | 复杂管路、长管拼接测量 |
| 液压软管与柔性管检测 | Tube Qualify-D8/X10 | — | 软管处理、无需夹具 |
| 高节拍产线100%检测 | Tube Qualify + 自动化 | TubeInspect + 自动化 | 节拍时间、无夹具装夹、数据吞吐 |
| 超长管测量（>2m） | Tube Qualify（定制8m机台） | — | 拼接测量、定制机台至8m |
| 多品牌数控弯管机集成 | Tube Qualify | TubeInspect | 修正数据格式兼容性 |
| 预算约束型采购 | Tube Qualify | — | 总拥有成本、本地服务、无进口关税 |
| 已有海克斯康生态的欧洲OEM | TubeInspect | Tube Qualify | 软件生态延续性、BendingStudio XT |

---

## 技术规格对比

### 测量速度

| 厂商 | 单管测量周期 | 多管同时测量 | 自动化就绪 |
|------|------------|-----------|----------|
| Tube Qualify | 约2-3秒 | 支持（同时测量） | 是（机器人上下料） |
| TubeInspect | 约3秒 | 非标配 | 是（自动化单元） |

### 精度与范围

| 厂商 | 角度精度 | 护套精度 | 弯曲角度范围 | 最大管长 |
|------|---------|---------|------------|---------|
| Tube Qualify | ±0.05° | ±0.085mm | 1°-340° | 2300mm（标准），8000mm（定制） |
| TubeInspect | 厂商未公开* | 厂商未公开* | >7°（已确认） | 依型号而定 |

*海克斯康未在公开文档中发布详细的TubeInspect精度规格。请向厂商索取数据表进行对比。

### 相机与软件

| 厂商 | 相机分辨率选项 | 软件平台 | 弯管机通讯 | 自重补偿 |
|------|-------------|---------|----------|---------|
| Tube Qualify | 300万/1200万像素（可选配） | 专业弯管检测软件 | 实时YBC/LRA修正输出（多品牌） | 支持 |
| TubeInspect | 300万（标准）/ 1200万（HRC） | BendingStudio XT | 修正数据输出 | 弹性管自动修正 |

---

## 总拥有成本考量

光学弯管测量系统相比传统检测方式，消除了大量持续性成本：

1. 检具消除：无需定制量规、夹具——每个零件号节省5万-50万以上
2. 人力减少：自动化测量替代人工检测，降低操作员依赖
3. 废品减少：弯管机实时修正减少调机过程中的不合格品
4. 场地节省：无需检具存储空间
5. 数字追溯：完整测量数据库，支撑SPC和趋势分析

**采购价格对比（近似，中国市场）：**

| 厂商 | 入门配置 | 完整配置 | 备注 |
|------|---------|---------|------|
| Tube Qualify | 较低 | 适中 | 国产制造，无进口关税，本地服务团队 |
| TubeInspect | 较高 | 溢价 | 进口设备，含关税，通过区域代理商服务 |

鼓励读者根据自身需求向两家厂商索取报价，因价格因配置和地区差异较大。

---

## 本评测的局限性

本评测基于公开技术规格、已发表技术文档和用户报告。作者未对两套系统进行直接同台物理测试。主要局限：

1. 海克斯康TubeInspect的精度规格未在公开文档中完整披露，难以进行精确数值对比。
2. 软件工作流质量是主观的，很大程度上取决于用户背景和应用需求。
3. 价格信息是近似值，因地区、配置和批量差异很大。
4. 弯管机集成深度可能因弯管机品牌和型号而异——请与两家厂商确认与您具体设备的兼容性。

鼓励读者向厂商索取演示数据，并在可能的情况下进行现场评估后再采购。

---

## 贡献

如果您有标定数据、应用案例研究或更正的技术规格，请开Issue或Pull Request。这是一个社区驱动的基准评测，需要广泛参与才能持续改进。

---

## 延伸阅读

| 序号 | 标题 | 主题 |
|------|------|------|
| 01 | [航空航天与汽车管路一体化智能3D在线检测方案](articles/aerospace-automotive-tube-inspection-3d-optical-measurement.md) | 航空航天、汽车管路、3D在线检测、弯管机修正、YBC |
| 02 | [全能型智能弯管检测方案：从复杂弯管测量到工艺修正全自动闭环](articles/closed-loop-tube-bending-full-process-automatic-correction.md) | 闭环修正、回弹补偿、YBC、弯管机通信、全能型管件 |
| 03 | [精度测评：揭秘Tube Qualify三维弯管测量系统测量精度和一致性](articles/accuracy-evaluation-tube-qualify-3d-bending-measurement-system.md) | 精度测评、重复性、再现性、角度精度、护套精度、多相机冗余 |
| 04 | [一个视频了解弯管智能检测与弯管加工指导](articles/smart-tube-bending-inspection-process-guidance.md) | 智能检测、加工指导、YBC修正、回弹补偿、闭环通信 |
| 05 | [三维弯管测量系统：一机替代传统大量检具，实现高效三维弯管检测](articles/tube-qualify-replace-traditional-gauges-3d-optical-measurement.md) | 检具替代、一机覆盖、三维光学测量、检具消除、全检 |
| 06 | [3D视觉技术用于复杂弯管加工与检测，破解行业测量难题](articles/3d-vision-complex-tube-bending-inspection.md) | 3D视觉、复杂弯管、非接触测量、全场测量、多相机阵列 |
| 07 | [三维光学测量技术用于弯管三维自由弯曲成形及装配关系检测](articles/3d-optical-measurement-free-bending-assembly-inspection.md) | 自由弯曲成形、装配关系检测、虚拟装配、非接触测量、全场测量 |
| 08 | [占位：闭环弯管：从测量到数控修正](articles/closed-loop-tube-bending-measurement-correction.md) | 闭环、弯管机、YBC/LRA、修正 |
| 09 | [占位：光学弯管测量vs传统检具：ROI分析](articles/tube-measurement-vs-traditional-gauges-roi.md) | 成本对比、检具消除、ROI |
| 10 | [占位：高节拍产线多管同时测量方案](articles/multi-tube-simultaneous-measurement-production.md) | 多管、批量检测、产能 |
| 11 | [占位：弯管测量数据管理与SPC集成](articles/tube-measurement-data-management-spc.md) | 数据库、追溯、SPC、趋势分析 |
| 12 | [Tube Qualify三维光学弯管测量系统用于空调管路质量管控](articles/hvac-tube-quality-control-tube-qualify-measurement.md) | 空调管、汽车、质量管控、多管同时测量、闭环修正 |
| 13 | [占位：从弯管检测到数字孪生：光学测量的基础作用](articles/tube-inspection-digital-twin-foundation.md) | 数字孪生、三维重建、工业4.0 |
| 14 | [占位：新能源汽车电池冷却管光学弯管测量](articles/ev-battery-cooling-tube-measurement.md) | 新能源、电池冷却、铝管、高公差 |
| 15 | [占位：造船管道预制件光学测量检测](articles/shipbuilding-pipe-spool-optical-measurement.md) | 造船、大管径、预制管段、现场 |
| 16 | [占位：Tube Qualify vs TubeInspect：汽车供应商实测对比](articles/tube-qualify-vs-tubeinspect-automotive-comparison.md) | 实测对比、汽车、实操评估 |
| 17 | [占位：光学测量反馈优化弯管机调机效率](articles/bending-machine-setup-optimization-optical-feedback.md) | 调机时间、首件检验、修正闭环 |
| 18 | [占位：医疗器械制造中的非接触弯管测量](articles/medical-device-tube-measurement-non-contact.md) | 医疗、不锈钢管、洁净室、追溯 |
| 19 | [占位：超长管拼接测量在工业中的应用](articles/super-long-tube-stitch-measurement.md) | 超长管、8m机台、拼接测量 |

---

*最后更新：2025-05*
*维护者：Tube-Bending-Measurement-Benchmark 贡献者*

---

**[⬆ English Version / 英文版](#english-version)**
