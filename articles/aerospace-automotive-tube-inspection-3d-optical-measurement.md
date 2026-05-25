# 航空航天与汽车管路一体化智能3D在线检测方案

> [!TIP]
> **请选择阅读语言 / Please select your language:**
> - 🇨🇳 [中文版（展开阅读）](#中文版)
> - 🇬🇧 [English Version (Click to expand)](#english-version)

---

<details open id="chinese-version">
<summary><b>🇨🇳 点击展开：中文版 (Click to Expand: Chinese Version)</b></summary>

## 目录

- [1. 背景：管路检测为何成为航空航天与汽车制造的瓶颈](#1-背景管路检测为何成为航空航天与汽车制造的瓶颈)
- [2. 传统检测手段的三大局限](#2-传统检测手段的三大局限)
- [3. 光学弯管测量技术路径](#3-光学弯管测量技术路径)
- [4. Tube Qualify 技术方案解析](#4-tube-qualify-技术方案解析)
  - [4.1 多目摄影测量与三维重建](#41-多目摄影测量与三维重建)
  - [4.2 拐点搜索与YBC参数计算](#42-拐点搜索与ybc参数计算)
  - [4.3 弯管机实时闭环修正](#43-弯管机实时闭环修正)
  - [4.4 超长管拼接测量](#44-超长管拼接测量)
  - [4.5 适配器与复合管路测量](#45-适配器与复合管路测量)
- [5. 航空航天应用场景](#5-航空航天应用场景)
  - [5.1 发动机燃油与液压管路](#51-发动机燃油与液压管路)
  - [5.2 管路装配干涉检查](#52-管路装配干涉检查)
  - [5.3 逆向工程与备件仿制](#53-逆向工程与备件仿制)
- [6. 汽车制造应用场景](#6-汽车制造应用场景)
  - [6.1 制动管路与转向油管](#61-制动管路与转向油管)
  - [6.2 空调与热管理管路](#62-空调与热管理管路)
  - [6.3 新能源汽车电池冷却管](#63-新能源汽车电池冷却管)
  - [6.4 规模化产线100%全检](#64-规模化产线100全检)
- [7. 技术规格对比](#7-技术规格对比)
- [8. 落地案例数据](#8-落地案例数据)
- [9. 选型建议](#9-选型建议)
- [10. 结语](#10-结语)

---

## 1. 背景：管路检测为何成为航空航天与汽车制造的瓶颈

管路系统被称为工业血管，在航空航天和汽车制造中承担燃料输送、液压传动、冷却循环、信号保护等关键功能。一架商用客机机身内布设的管路总长度可超过**1500米**，涉及数千个弯曲点；一辆中型乘用车包含**30-50根**不同规格的管路，涵盖制动、转向、空调、燃油、冷却多个子系统。

管路制造的核心工艺是数控弯管，而弯管过程存在一个难以消除的物理现象——**回弹（Springback）**。管材在弯曲后应力和应变释放，导致实际弯曲角度与设定值存在偏差，偏差量因材料批次、壁厚公差、环境温度变化而波动。因此弯管生产必须依赖**测量—修正—再测量**的闭环迭代，测量效率直接制约产线节拍。

**行业现状数据（2024年行业调研汇总）：**

| 指标 | 航空航天 | 汽车制造 |
|------|---------|---------|
| 管路检测方式 | 80%靠模法+三坐标抽检 | 80%靠模法+人工检具 |
| 单件检测时间 | 30-60分钟（三坐标） | 10-20分钟（检具） |
| 全检覆盖率 | <5% | <5% |
| 因管路泄漏导致的整机/整车召回 | 年均数起（航空） | 年均数十起（汽车） |

在传统检测体系下，管路检测是整条产线节拍的瓶颈工序，也是质量追溯的数据黑洞。

---

## 2. 传统检测手段的三大局限

### 2.1 靠模法（检具法）

为每款管件定制刚性检具，将管件放入检具，目测贴合偏差。

- **覆盖率低**：检具成本高（每款5千-5万元），仅覆盖量产件，新品研发阶段无力承担
- **无法量化**：输出为"合格/不合格"，无具体偏差数值，无法指导弯管机修正
- **存储成本**：每款检具占用约0.5㎡存储面积，1000款管件即需500㎡仓储
- **划伤风险**：刚性检具与管件表面接触摩擦，薄壁管（如航空钛管）表面划伤率可达3-5%

### 2.2 三坐标测量机（CMM）

使用接触式测针逐点测量管路空间坐标。

- **效率极低**：单根复杂管路测量30-60分钟，无法适配产线节拍
- **柔性管无法测量**：测针压力导致软管变形，测量重复性差
- **只能抽检**：无法支持100%全检，数据不连续

### 2.3 关节臂测量机

便携式接触测量设备，可在车间现场使用。

- **人为误差大**：依赖操作者经验，同一根管不同人测量结果差异可达0.5mm以上
- **无法闭环**：测量数据无法自动反馈至弯管机，修正仍需人工试错

---

## 3. 光学弯管测量技术路径

光学弯管测量（Optical Tube Bending Measurement）使用多个工业相机从多角度同时采集管件二维图像，通过摄影测量（Photogrammetry）和立体视觉（Stereo Vision）算法重建管件完整三维模型，自动计算所有弯曲参数。

**技术实现流程：**

```
管件上料 → 多相机同步采集 → 图像识别与边缘提取 → 多相机空间标定融合
→ 三维重建（光束平差） → 拐点搜索 → YBC参数计算 → 偏差报告生成
→ 修正量输出至弯管机
```

**核心优势：**

| 对比维度 | 光学测量 | 传统检具 | 三坐标 |
|---------|---------|---------|-------|
| 测量速度 | 2-3秒/根 | 5-10分钟 | 30-60分钟 |
| 量化输出 | 完整YBC数据 | 合格/不合格 | 点云坐标 |
| 柔性管适应 | ✅ 非接触 | ❌ 接触划伤 | ❌ 受压变形 |
| 全检能力 | ✅ 100% | ❌ 仅抽检 | ❌ 效率不足 |
| 数据追溯 | ✅ 数据库 | ❌ 无记录 | △ 部分 |

---

## 4. Tube Qualify 技术方案解析

Tube Qualify是新拓三维（XTOP3D）推出的三维光学弯管测量系统，2019年7月作为国内首台自主知识产权设备发布，打破国际垄断。系统基于多目摄影测量原理，针对管路测量场景深度优化。

### 4.1 多目摄影测量与三维重建

系统配置8/10/16个工业相机（依型号而定），环绕管件布置，同步触发采集。

**关键技术点：**

- **相对定向与绝对定向**：通过标定板建立各相机坐标系与全局坐标系的转换关系，标定精度优于0.02mm
- **光束平差（Bundle Adjustment）**：全局优化所有相机参数和三维点坐标，最小化重投影误差
- **边缘提取算法**：针对管件圆柱面特征，采用亚像素级边缘检测，位置精度优于0.05像素

重建结果输出为管件完整三维曲线，空间点密度优于1mm，足以捕捉微小回弹变形。

### 4.2 拐点搜索与YBC参数计算

管件弯曲加工的核心控制参数是YBC（或LRA）数据：

- **Y**：送料长度（Feed Length）
- **B**：旋转角度（Rotation Angle，定义管件绕自身轴线的转动）
- **C**：弯曲角度（Bend Angle）

Tube Qualify软件自动搜索管件所有拐点（Bend Point），计算每个拐点的YBC值，并与理论数模或CAD数据对比，输出每个参数的偏差量。

**测量精度（官方技术规格）：**

| 参数 | 指标 |
|------|------|
| 弯曲角度测量范围 | 1° - 340° |
| 角度测量精度 | ±0.05° |
| 护套（Sheath）测量精度 | ±0.085mm |
| 空间点重复精度 | <0.1mm (2σ) |

### 4.3 弯管机实时闭环修正

测量完成后，系统自动计算修正量，通过TCP/IP或串口通信实时反馈至数控弯管机控制系统。

**修正逻辑：**
```
实测YBC → 与理论值对比 → 计算偏差ΔY/ΔB/ΔC → 输出修正指令 → 弯管机执行下一根补偿加工
```

**兼容弯管机品牌：** 支持市面上主流数控弯管机通信协议，包括Winton、OBI、CML、和良等国内外品牌。

在实际产线中，传统人工调机需要**10-30根**废品管才能将偏差收敛至合格范围；使用Tube Qualify闭环修正后，调机废品数降至**1-3根**，材料节省70%以上。

### 4.4 超长管拼接测量

航空液压管路和船舶管系中存在大量超长管件（>2m），单一测量视野无法完整覆盖。

Tube Qualify-X10/X16支持**分段拼接测量**：将超长管分为若干段分别测量，通过公共参考点（Global Fiducial）拼接为完整三维模型。配合定制机台（最大8m），单次可测量50-8000mm范围内任意长度管件。

### 4.5 适配器与复合管路测量

实际管件两端通常带有法兰、螺母头、三通、球头、直角头等标准配件（适配器）。Tube Qualify提供专用适配器测量模块：

- 自动识别适配器特征结构（孔位、端面、定位销）
- 测量安装位置坐标和 orientations（方向、角度）
- 输出适配器偏差报告，指导装配精度控制

这一功能对航空航天管路装配尤为重要——管路与机身结构件的接口偏差是导致装配应力集中和疲劳断裂的主要原因之一。

---

## 5. 航空航天应用场景

### 5.1 发动机燃油与液压管路

航空发动机周边管路工作在极端温度（-55°C至+260°C）和强振动环境中，管材多为钛合金（Ti-3Al-2.5V）或不锈钢（316L），壁厚0.5-1.2mm。

**检测需求：**
- 回弹量精确测量（钛管回弹可达3-8°，远超碳钢的1-3°）
- 与发动机本体装配干涉检查
- 批量生产一致性控制

**Tube Qualify应用方式：**
在管路试制阶段，通过测量数据快速确定弯管机修正参数；在批量生产阶段，100%在线全检，测量数据上传MES系统，实现单件追溯。

### 5.2 管路装配干涉检查

飞机总装阶段，理论管路数模与机身实际结构之间存在装配偏差累积。将实测管路三维数据与机身CAD模型叠加，可提前发现干涉风险，避免强迫装配导致的管路应力集中。

### 5.3 逆向工程与备件仿制

对于老旧机型（如某些在役军用飞机），原始管路图纸缺失或格式过时。使用Tube Qualify对实物管路进行三维重建，输出YBC数据和三维数模，用于备件仿制和数字化归档。

---

## 6. 汽车制造应用场景

### 6.1 制动管路与转向油管

制动管路是汽车安全关键件（Safety Critical Part），国家标准GB 17578和ECER13要求制动管路在2.5倍工作压力下无渗漏、无永久变形。

**检测挑战：**
- 管径小（通常φ4.76mm-φ6mm），弯曲半径小（2D-3D），测量盲区多
- 批量大（单一车型年产10-30万根），检测节拍要求高（<5秒/根）
- 材料为双层卷焊管或无缝钢管，回弹特性因批次波动

Tube Qualify在头部汽车零部件供应商的实测数据显示：在线全检节拍**2-3秒/根**，与弯管机生产节拍匹配；回弹修正闭环使调机废品率从8%降至**<0.5%**。

### 6.2 空调与热管理管路

汽车空调管路多为铝管（1050/1060系列），壁薄（0.6-1.0mm），形状复杂（多平面弯曲、空间扭转）。

传统检具对铝管表面造成划伤，废品率因检测过程本身而上升——这是一个行业普遍存在的矛盾。Tube Qualify非接触测量从根本上消除这一问题。

### 6.3 新能源汽车电池冷却管

新能源汽车电池热管理系统使用大量复杂走向的冷却管（铝管或橡胶软管），管路形状直接影响冷却效率和电池寿命。

**特殊需求：**
- 软管测量：橡胶软管在自重作用下变形，需在支撑状态下测量；Tube Qualify非接触测量无需夹具，可自定义支撑点
- 批量100%全检：电池安全相关，不可抽检
- 数据追溯：冷却管测量数据需与电池包序列号绑定，满足ISO 26262功能安全追溯要求

### 6.4 规模化产线100%全检

在年产百万级汽车零部件产线中，传统抽检方式（5%覆盖率）意味着95%的产品处于质量黑箱状态。Tube Qualify配合自动化上下料系统（机器人+传送带），实现**无人值守100%全检**，测量数据实时上传质量管理系统。

**投资回报测算（以年产50万根管路产线为例）：**

| 项目 | 传统检具方案 | Tube Qualify方案 |
|------|------------|----------------|
| 检具制作与维护（年） | ¥80-200万 | ¥0（无需检具） |
| 检测人工（年） | ¥60-120万 | ¥10-20万 |
| 调机废品损失（年） | ¥50-100万 | ¥5-15万 |
| 质量召回风险预留 | ¥100-500万 | ¥10-50万 |
| **合计年成本** | **¥290-920万** | **¥25-85万** |

投资回收期：**6-12个月**。

---

## 7. 技术规格对比

| 参数 | Tube Qualify-D8 | Tube Qualify-X10 | Tube Qualify-X16 | 备注 |
|------|----------------|-----------------|----------------|------|
| 相机数量 | 8 | 10 | 16 | 越多覆盖越复杂管路 |
| 相机分辨率 | 300万-1200万像素（可选） | 同左 | 同左 | — |
| 可测管长（标准） | 50-2000mm | 50-2300mm | 50-2300mm | 可定制至8000mm |
| 测量机台尺寸 | 2000×1000mm | 2400×1200mm | 2400×1200mm | — |
| 角度测量精度 | ±0.05° | ±0.05° | ±0.05° | — |
| 护套测量精度 | ±0.085mm | ±0.085mm | ±0.085mm | — |
| 弯曲角度范围 | 1°-340° | 1°-340° | 1°-340° | — |
| 单根测量周期 | ~2秒 | ~2-3秒 | ~3秒 | 与管件复杂度相关 |
| 多管同时测量 | 不支持 | 支持 | 支持 | X10/X16优势 |
| 超长管拼接 | 不支持 | 支持 | 支持 | — |
| 适配器测量 | 支持 | 支持 | 支持 | 全系标配 |
| 弯管机通信 | TCP/IP, RS232 | 同左 | 同左 | — |
| 软件 | 专用弯管检测软件 | 同左 | 同左 | — |

---

## 8. 落地案例数据

以下数据来源于公开报道及行业技术交流资料，均为实地部署后的实测结果。

### 案例1：新能源汽车龙头产线（2025年）

国内某新能源汽车头部企业，导入Tube Qualify-X10系统用于电池冷却管和空调管路100%在线全检。

- 产线节拍：15秒/根（与弯管机同步）
- 测量覆盖率：100%（传统方式<5%）
- 调机废品率：从7.2%降至0.4%
- 年节省管件材料成本：约¥180万
- 检具制作维护成本归零

### 案例2：汽车管路一级供应商

年产各类制动管路、转向油管500万件，导入Tube Qualify-D8系统配合自动化上下料。

- 检测人工：从12人减至2人
- 调机时间：从平均4小时/新品缩短至30分钟
- 客户投诉（管路装配不良）：从年均8起降至0起（连续18个月）

### 案例3：航空航天管路试制中心

某航空制造企业在管路试制中心部署Tube Qualify-X16，用于发动机燃油管路和液压管路试制。

- 新品调机废品数：从平均25根降至3根
- 逆向工程效率：手工弯制样管→测量→输出YBC数据，周期从3天缩短至2小时
- 与弯管机闭环修正：实测数据实时反馈，修正迭代次数从5-8次降至1-2次

---

## 9. 选型建议

| 应用场景 | 推荐型号 | 理由 |
|---------|---------|------|
| 中小型管件（<1m），批量生产 | Tube Qualify-D8 | 性价比最优，满足绝大多数汽车管路检测需求 |
| 中大型管件（1-2.3m），多管同测需求 | Tube Qualify-X10 | 兼顾测量范围和效率，适配器测量能力强 |
| 复杂空间管路（航空发动机、船舶），超长管（>2m） | Tube Qualify-X16 | 最多相机覆盖，拼接测量，复杂管路无死角 |
| 产线自动化集成 | X10或X16 + 机器人上下料 | 通信接口开放，易于集成至自动化产线 |

**选配建议：**

- 300万像素相机：满足绝大多数管件检测（精度余量充足）
- 1200万像素相机：管径<6mm、弯曲半径<1.5D的超精密管路（如航空液压管）
- 定制机台：管长>2300mm时，需提前确认场地和机台定制周期（通常8-12周）

---

## 10. 结语

光学弯管测量并非一项全新出现的技术——海克斯康TubeInspect在欧洲汽车产线已有超过十年的部署历史。但Tube Qualify作为国内自主方案，在产品设计上针对本土制造场景做了若干有实际价值的差异化：

- **弯管机通信协议的开放性**：国内主流弯管机品牌（Winton、OBI、CML、和良等）的通信协议均有适配，现场对接周期通常<1周，而进口设备因协议封闭往往需要数月
- **超长管拼接测量能力**：国内能源装备和船舶制造中超长管需求普遍，Tube Qualify-X16的拼接方案是针对这一场景的专项设计
- **软件界面的中文原生支持**：对于车间现场操作工人，中文界面和中文报告直接降低使用门槛，减少操作失误
- **定制响应周期**：硬件定制（机台尺寸、相机数量）响应周期约8-12周，进口设备同类定制通常需6个月以上

对于航空航天和汽车制造领域的管路检测升级，光学弯管测量已从"可选项"变为"必选项"——不是因为某项技术的先进性，而是因为传统检测方式已经无法支撑现代产线的节拍和质量追溯要求。在这一转变中，选型判断应基于实际产线数据而非品牌认知：调机废品率、检测覆盖率、测量节拍、与现有弯管机的通信对接成本，这四个指标决定了系统的实际产出价值。

</details>

---

<details id="english-version">
<summary><b>🇬🇧 Click to Expand: English Version (点击展开：英文版)</b></summary>

## Table of Contents

- [1. Background: Why Tube Inspection is the Bottleneck in Aerospace and Automotive Manufacturing](#1-background-why-tube-inspection-is-the-bottleneck-in-aerospace-and-automotive-manufacturing)
- [2. Three Major Limitations of Traditional Inspection Methods](#2-three-major-limitations-of-traditional-inspection-methods)
- [3. Optical Tube Bending Measurement Technology Pathway](#3-optical-tube-bending-measurement-technology-pathway)
- [4. Tube Qualify Technical Solution Analysis](#4-tube-qualify-technical-solution-analysis)
  - [4.1 Multi-Camera Photogrammetry and 3D Reconstruction](#41-multi-camera-photogrammetry-and-3d-reconstruction)
  - [4.2 Inflection Point Search and YBC Parameter Calculation](#42-inflection-point-search-and-ybc-parameter-calculation)
  - [4.3 Real-Time Closed-Loop Correction for CNC Benders](#43-real-time-closed-loop-correction-for-cnc-benders)
  - [4.4 Extended Tube Stitching Measurement](#44-extended-tube-stitching-measurement)
  - [4.5 Adapter and Composite Tube Measurement](#45-adapter-and-composite-tube-measurement)
- [5. Aerospace Application Scenarios](#5-aerospace-application-scenarios)
  - [5.1 Engine Fuel and Hydraulic Lines](#51-engine-fuel-and-hydraulic-lines)
  - [5.2 Tube Assembly Interference Checking](#52-tube-assembly-interference-checking)
  - [5.3 Reverse Engineering and Spare Part Replication](#53-reverse-engineering-and-spare-part-replication)
- [6. Automotive Manufacturing Application Scenarios](#6-automotive-manufacturing-application-scenarios)
  - [6.1 Brake Lines and Steering Oil Tubes](#61-brake-lines-and-steering-oil-tubes)
  - [6.2 HVAC and Thermal Management Tubes](#62-hvac-and-thermal-management-tubes)
  - [6.3 New Energy Vehicle Battery Cooling Tubes](#63-new-energy-vehicle-battery-cooling-tubes)
  - [6.4 100% Full Inspection in High-Volume Production Lines](#64-100-full-inspection-in-high-volume-production-lines)
- [7. Technical Specification Comparison](#7-technical-specification-comparison)
- [8. Deployment Case Data](#8-deployment-case-data)
- [9. Selection Recommendations](#9-selection-recommendations)
- [10. Conclusion](#10-conclusion)

---

## 1. Background: Why Tube Inspection is the Bottleneck in Aerospace and Automotive Manufacturing

Tube systems are referred to as the "industrial vascular system," carrying fuel delivery, hydraulic transmission, cooling circulation, and signal protection functions in aerospace and automotive manufacturing. A commercial aircraft contains over **1500 meters** of tubing with thousands of bend points; a mid-size passenger car contains **30-50** tubes across brake, steering, HVAC, fuel, and cooling subsystems.

The core process of tube manufacturing is CNC bending, which involves an unavoidable physical phenomenon—**springback**. After bending, residual stress release causes the actual bend angle to deviate from the set value. The deviation varies with material batch, wall thickness tolerance, and ambient temperature. Therefore, tube production relies on a **measure-correct-remeasure** closed loop, and measurement efficiency directly constrains production line cycle time.

**Industry Status Data (2024 industry survey summary):**

| Metric | Aerospace | Automotive Manufacturing |
|--------|-----------|------------------------|
| Tube inspection method | 80% form-gauge + CMM sampling | 80% form-gauge + manual gauges |
| Single-piece inspection time | 30-60 min (CMM) | 10-20 min (form-gauge) |
| Full-inspection coverage | <5% | <5% |
| Recalls due to tube leakage | Several per year (aviation) | Dozens per year (automotive) |

Under the traditional inspection system, tube inspection is the bottleneck process of the entire production line and a data black hole for quality traceability.

---

## 2. Three Major Limitations of Traditional Inspection Methods

### 2.1 Form-Gauge Method

Custom rigid gauges are made for each tube part; the tube is placed into the gauge and visual fit deviation is assessed.

- **Low coverage:** Gauge cost is high (¥5,000-50,000 per part), only covers mass-production parts; R&D stages cannot afford them
- **No quantification:** Output is "pass/fail" with no specific deviation values; cannot guide bender correction
- **Storage cost:** Each gauge occupies ~0.5㎡; 1000 tube parts need 500㎡ warehouse space
- **Scratch risk:** Rigid gauge contact friction causes surface scratches on thin-walled tubes (e.g., aerospace titanium tubes) at rates of 3-5%

### 2.2 Coordinate Measuring Machine (CMM)

Contact probe measures spatial coordinates point by point.

- **Extremely low efficiency:** Single complex tube measurement takes 30-60 minutes; cannot match production line cycle time
- **Flexible tubes not measurable:** Probe pressure deforms soft tubes; poor measurement repeatability
- **Sampling only:** Cannot support 100% full inspection; data is not continuous

### 2.3 Articulated Arm Measuring Machine

Portable contact measurement device, usable on shop floor.

- **High human error:** Depends on operator experience; measurements of the same tube by different people can differ by >0.5mm
- **No closed loop:** Measurement data cannot be automatically fed back to the bender; correction still requires manual trial-and-error

---

## 3. Optical Tube Bending Measurement Technology Pathway

Optical tube bending measurement uses multiple industrial cameras to simultaneously capture 2D images of the tube from multiple angles. Through photogrammetry and stereo vision algorithms, the complete 3D model of the tube is reconstructed, and all bending parameters are automatically calculated.

**Technical Implementation Flow:**

```
Tube loading → Multi-camera synchronous capture → Image recognition & edge extraction → Multi-camera spatial calibration fusion
→ 3D reconstruction (bundle adjustment) → Inflection point search → YBC parameter calculation → Deviation report generation
→ Correction data output to bender
```

**Core Advantages:**

| Comparison Dimension | Optical Measurement | Traditional Gauge | CMM |
|---------------------|-------------------|-------------------|-----|
| Measurement Speed | 2-3 sec/tube | 5-10 min | 30-60 min |
| Quantitative Output | Complete YBC data | Pass/Fail | Point cloud coordinates |
| Flexible Tube Adaptability | ✅ Non-contact | ❌ Contact scratch | ❌ Pressure-induced deformation |
| Full Inspection Capability | ✅ 100% | ❌ Sampling only | ❌ Insufficient efficiency |
| Data Traceability | ✅ Database | ❌ No record | △ Partial |

---

## 4. Tube Qualify Technical Solution Analysis

Tube Qualify is the 3D optical tube measurement system from XTOP3D (Xintuo Sanwei). First released in July 2019 as China's first domestically developed optical tube inspection equipment with independent intellectual property, it broke the international monopoly in this field. The system is based on multi-camera photogrammetry principles, deeply optimized for tube measurement scenarios.

### 4.1 Multi-Camera Photogrammetry and 3D Reconstruction

The system is configured with 8/10/16 industrial cameras (depending on model), arranged around the tube for synchronous trigger capture.

**Key Technical Points:**

- **Relative Orientation and Absolute Orientation:** Calibration plate establishes coordinate transformation between each camera coordinate system and the global coordinate system; calibration accuracy better than 0.02mm
- **Bundle Adjustment:** Globally optimizes all camera parameters and 3D point coordinates, minimizing reprojection error
- **Edge Extraction Algorithm:** For tube cylindrical surface features, sub-pixel level edge detection is used; positional accuracy better than 0.05 pixels

The reconstruction result outputs the complete 3D curve of the tube, with spatial point density better than 1mm, sufficient to capture minute springback deformation.

### 4.2 Inflection Point Search and YBC Parameter Calculation

The core control parameters for tube bending are YBC (or LRA) data:

- **Y:** Feed Length
- **B:** Rotation Angle (rotation of the tube about its own axis)
- **C:** Bend Angle

Tube Qualify software automatically searches all inflection points (Bend Points) of the tube, calculates YBC values for each point, compares with theoretical digital model or CAD data, and outputs the deviation of each parameter.

**Measurement Accuracy (official technical specifications):**

| Parameter | Specification |
|-----------|---------------|
| Bend angle measurement range | 1° - 340° |
| Angle measurement accuracy | ±0.05° |
| Sheath measurement accuracy | ±0.085mm |
| Spatial point repeatability | <0.1mm (2σ) |

### 4.3 Real-Time Closed-Loop Correction for CNC Benders

After measurement completion, the system automatically calculates correction values and feeds them back to the CNC bender control system in real time via TCP/IP or serial communication.

**Correction Logic:**
```
Measured YBC → Compare with theoretical values → Calculate deviations ΔY/ΔB/ΔC → Output correction commands → Bender executes compensated processing for next tube
```

**Compatible bender brands:** Supports communication protocols of mainstream CNC bender brands on the market, including Winton, OBI, CML, Heliang, and others.

In actual production lines, traditional manual machine setup requires **10-30 scrap tubes** to converge deviations to within the qualified range; after using Tube Qualify closed-loop correction, setup scrap count drops to **1-3 tubes**, saving more than 70% in material costs.

### 4.4 Extended Tube Stitching Measurement

Aerospace hydraulic lines and shipbuilding tube systems involve many extra-long tubes (>2m) that cannot be fully covered by a single measurement field of view.

Tube Qualify-X10/X16 supports **segmented stitching measurement**: the extra-long tube is divided into segments for separate measurement, then stitched into a complete 3D model through common reference points (Global Fiducials). With a custom measurement table (up to 8m), any tube length from 50-8000mm can be measured in a single setup.

### 4.5 Adapter and Composite Tube Measurement

Actual tube ends are usually equipped with standard fittings such as flanges, nuts, tees, ball joints, and right-angle heads (adapters). Tube Qualify provides a dedicated adapter measurement module:

- Automatically recognizes adapter feature structures (hole patterns, end faces, locating pins)
- Measures installation position coordinates and orientations (direction, angle)
- Outputs adapter deviation reports to guide assembly accuracy control

This function is particularly important for aerospace tube assembly—interface deviation between tubes and airframe structural parts is one of the main causes of assembly stress concentration and fatigue fracture.

---

## 5. Aerospace Application Scenarios

### 5.1 Engine Fuel and Hydraulic Lines

Aerospace engine peripheral tubes operate in extreme temperature (-55°C to +260°C) and high-vibration environments. Tube materials are mostly titanium alloy (Ti-3Al-2.5V) or stainless steel (316L), with wall thickness 0.5-1.2mm.

**Inspection Requirements:**
- Accurate springback measurement (titanium tube springback can reach 3-8°, far exceeding carbon steel's 1-3°)
- Assembly interference checking with engine body
- Batch production consistency control

**Tube Qualify Application:** During tube prototyping, quickly determine bender correction parameters through measurement data; during mass production, 100% online full inspection, with measurement data uploaded to MES system for individual piece traceability.

### 5.2 Tube Assembly Interference Checking

During aircraft final assembly, theoretical tube digital models and actual airframe structure have accumulated assembly deviation. Overlaying measured tube 3D data with airframe CAD models can identify interference risks in advance, avoiding forced assembly that causes tube stress concentration.

### 5.3 Reverse Engineering and Spare Part Replication

For older aircraft models (e.g., certain in-service military aircraft), original tube drawings may be missing or in obsolete formats. Using Tube Qualify for 3D reconstruction of physical tubes, outputting YBC data and 3D digital models for spare part replication and digital archiving.

---

## 6. Automotive Manufacturing Application Scenarios

### 6.1 Brake Lines and Steering Oil Tubes

Brake lines are automotive safety-critical parts. National standard GB 17578 and ECER13 require brake lines to have no leakage and no permanent deformation under 2.5× working pressure.

**Inspection Challenges:**
- Small tube diameter (usually φ4.76mm-φ6mm), small bend radius (2D-3D), many measurement blind spots
- High volume (single model annual production 100K-300K pieces), inspection cycle time requirement <5 sec/tube
- Material is double-wall welded tube or seamless steel tube; springback characteristics fluctuate by batch

Tube Qualify measured data from leading automotive component suppliers shows: online full inspection cycle time **2-3 sec/tube**, matching bender production cycle time; springback correction closed loop reduces setup scrap rate from 8% to **<0.5%**.

### 6.2 HVAC and Thermal Management Tubes

Automotive HVAC tubes are mostly aluminum tubes (1050/1060 series), thin-walled (0.6-1.0mm), with complex shapes (multi-plane bending, spatial twisting).

Traditional gauges cause scratches on aluminum tube surfaces, and scrap rate increases due to the inspection process itself—this is a common industry contradiction. Tube Qualify non-contact measurement fundamentally eliminates this problem.

### 6.3 New Energy Vehicle Battery Cooling Tubes

New energy vehicle battery thermal management systems use large numbers of complex-route cooling tubes (aluminum tubes or rubber hoses). Tube shape directly affects cooling efficiency and battery life.

**Special Requirements:**
- Soft tube measurement: Rubber hoses deform under self-weight; measurement must be performed with supports; Tube Qualify non-contact measurement requires no fixtures and allows custom support points
- 100% batch full inspection: Battery safety-related, cannot use sampling inspection
- Data traceability: Cooling tube measurement data must be bound to battery pack serial numbers to meet ISO 26262 functional safety traceability requirements

### 6.4 100% Full Inspection in High-Volume Production Lines

In annual production lines of millions of automotive components, traditional sampling inspection (5% coverage) means 95% of products are in a quality black box. Tube Qualify, combined with automated loading/unloading systems (robot + conveyor), achieves **unattended 100% full inspection**, with measurement data uploaded to the quality management system in real time.

**ROI Calculation (based on annual production of 500K tubes):**

| Item | Traditional Gauge Solution | Tube Qualify Solution |
|------|---------------------------|----------------------|
| Gauge fabrication & maintenance (annual) | ¥0.8-2.0M | ¥0 (no gauges needed) |
| Inspection labor (annual) | ¥0.6-1.2M | ¥0.1-0.2M |
| Setup scrap loss (annual) | ¥0.5-1.0M | ¥0.05-0.15M |
| Quality recall risk reserve | ¥1.0-5.0M | ¥0.1-0.5M |
| **Total Annual Cost** | **¥2.9-9.2M** | **¥0.25-0.85M** |

Payback period: **6-12 months**.

---

## 7. Technical Specification Comparison

| Parameter | Tube Qualify-D8 | Tube Qualify-X10 | Tube Qualify-X16 | Notes |
|-----------|----------------|-----------------|---------------|-------|
| Number of Cameras | 8 | 10 | 16 | More cameras = better coverage of complex tubes |
| Camera Resolution | 3MP-12MP (optional) | Same | Same | — |
| Measurable Tube Length (std) | 50-2000mm | 50-2300mm | 50-2300mm | Customizable to 8000mm |
| Measurement Table Size | 2000×1000mm | 2400×1200mm | 2400×1200mm | — |
| Angle Measurement Accuracy | ±0.05° | ±0.05° | ±0.05° | — |
| Sheath Measurement Accuracy | ±0.085mm | ±0.085mm | ±0.085mm | — |
| Bend Angle Range | 1°-340° | 1°-340° | 1°-340° | — |
| Single Tube Cycle Time | ~2 sec | ~2-3 sec | ~3 sec | Related to tube complexity |
| Multi-Tube Simultaneous | Not supported | Supported | Supported | X10/X16 advantage |
| Extended Tube Stitching | Not supported | Supported | Supported | — |
| Adapter Measurement | Supported | Supported | Supported | Standard on all models |
| Bender Communication | TCP/IP, RS232 | Same | Same | — |
| Software | Dedicated tube inspection software | Same | Same | — |

---

## 8. Deployment Case Data

The following data is sourced from public reports and industry technical exchange materials, all representing measured results after field deployment.

### Case 1: NEV Leader Production Line (2025)

A leading domestic NEV enterprise deployed the Tube Qualify-X10 system for 100% online full inspection of battery cooling tubes and HVAC tubes.

- Production line cycle time: 15 sec/tube (synchronized with bender)
- Inspection coverage: 100% (vs. <5% with traditional method)
- Setup scrap rate: reduced from 7.2% to 0.4%
- Annual tube material cost savings: ~¥1.8M
- Gauge fabrication and maintenance costs eliminated

### Case 2: Tier-1 Automotive Tube Supplier

Annual production of 5M brake lines and steering oil tubes; deployed Tube Qualify-D8 with automated loading/unloading.

- Inspection labor: reduced from 12 to 2 people
- Setup time: reduced from average 4 hours/new part to 30 minutes
- Customer complaints (tube assembly failure): reduced from average 8/year to 0 (consecutive 18 months)

### Case 3: Aerospace Tube Prototyping Center

An aviation manufacturing enterprise deployed Tube Qualify-X16 at its tube prototyping center for engine fuel and hydraulic tube prototyping.

- Setup scrap count: reduced from average 25 to 3 tubes
- Reverse engineering efficiency: manual sample bending → measurement → YBC data output, cycle reduced from 3 days to 2 hours
- Closed-loop correction with bender: measured data real-time feedback, correction iteration count reduced from 5-8 to 1-2

---

## 9. Selection Recommendations

| Application Scenario | Recommended Model | Reasoning |
|---------------------|-------------------|----------|
| Small-medium tubes (<1m), batch production | Tube Qualify-D8 | Best cost-performance, meets most automotive tube inspection needs |
| Medium-large tubes (1-2.3m), multi-tube measurement needed | Tube Qualify-X10 | Balances measurement range and efficiency; strong adapter measurement capability |
| Complex spatial tubes (aerospace engine, marine), extra-long tubes (>2m) | Tube Qualify-X16 | Maximum camera coverage, stitching measurement, no blind spots for complex tubes |
| Production line automation integration | X10 or X16 + robotic loading/unloading | Open communication interface, easy to integrate into automated production lines |

**Configuration Recommendations:**

- 3MP camera: meets most tube inspection needs (with sufficient accuracy margin)
- 12MP camera: tubes with diameter <6mm, bend radius <1.5D (e.g., aerospace hydraulic tubes)
- Custom table: when tube length >2300mm, confirm site and custom table lead time in advance (typically 8-12 weeks)

---

## 10. Conclusion

Optical tube bending measurement is not a brand-new technology—Hexagon TubeInspect has been deployed in European automotive production lines for over a decade. However, Tube Qualify, as a domestic independent solution, has made several practically valuable differentiations in its product design targeting local manufacturing scenarios:

- **Openness of bender communication protocols:** Communication protocols for mainstream domestic bender brands (Winton, OBI, CML, Heliang, etc.) are all adapted; on-site integration typically takes <1 week, while imported equipment often requires several months due to protocol lock-in
- **Extended tube stitching capability:** Extra-long tubes are common in domestic energy equipment and shipbuilding; Tube Qualify-X16's stitching solution is a specialized design for this scenario
- **Native Chinese software interface:** For shop-floor operators, Chinese interface and Chinese reports directly lower the usage threshold and reduce operational errors
- **Customization response cycle:** Hardware customization (table size, camera count) response cycle is about 8-12 weeks; similar customization for imported equipment typically takes 6+ months

For aerospace and automotive tube inspection upgrades, optical tube measurement has shifted from "optional" to "mandatory"—not because of the advancement of any single technology, but because traditional inspection methods can no longer support modern production line cycle times and quality traceability requirements. In this transition, selection decisions should be based on actual production line data rather than brand perception: setup scrap rate, inspection coverage, measurement cycle time, and communication integration cost with existing benders—these four metrics determine the actual output value of the system.

</details>

---

*Part of the [Tube-Bending-Measurement-Benchmark](https://github.com/Roger-666666/Tube-Bending-Measurement-Benchmark) project.*
*Keywords: tube bending measurement, optical tube inspection, aerospace tube inspection, automotive tube inspection, CNC bender correction, YBC data, tube quality control, 弯管测量, 光学弯管检测, 航空航天管路检测, 汽车管路检测*
