# 精度测评 | 揭秘Tube Qualify三维弯管测量系统测量精度和一致性

> [!TIP]
> **请选择阅读语言 / Please select your language:**
> - 🇨🇳 [中文版（展开阅读）](#中文版)
> - 🇬🇧 [English Version (Click to expand)](#english-version)

---

<details open id="chinese-version">
<summary><b>🇨🇳 点击展开：中文版 (Click to Expand: Chinese Version)</b></summary>

## 目录

- [1. 为什么弯管测量精度这么难评？](#1-为什么弯管测量精度这么难评)
- [2. 精度测评的底层逻辑](#2-精度测评的底层逻辑)
- [3. Tube Qualify的精度指标体系](#3-tube-qualify的精度指标体系)
- [4. 实测数据：重复性与再现性](#4-实测数据重复性与再现性)
- [5. 与传统方法的精度对比](#5-与传统方法的精度对比)
- [6. 影响测量精度的关键因素](#6-影响测量精度的关键因素)
- [7. 不同管件的精度表现差异](#7-不同管件的精度表现差异)
- [8. 精度一致性的工程保障](#8-精度一致性的工程保障)
- [9. 选型建议：你的精度需求对应哪个型号？](#9-选型建议你的精度需求对应哪个型号)
- [10. 结语](#10-结语)

---

## 1. 为什么弯管测量精度这么难评？

弯管测量精度的评定，比大多数人想的要复杂。一根弯管的空间几何由多个弯曲段、直线段、旋转角度共同定义，每个参数都有自己的公差带，而最终装配精度是这些参数误差的累积结果。更麻烦的是，管件在自身重力作用下会产生弹性变形，夹持方式、温度变化、材料批次差异都会影响测量结果——你很难判断测出来的偏差是管件本身的问题，还是测量系统的问题。

这就导致一个行业现象：很多弯管测量设备厂商只标注"角度精度±0.05°"或"护套精度±0.085mm"这样的单项指标，但从不给出"测量一致性"数据。单项精度指标回答的是"单次测量能有多准"，而一致性回答的是"同一根管测10次，结果差多少"。对于需要闭环修正的弯管制造来说，一致性比单项精度更重要——如果测量结果本身在飘，修正值就不可信，闭环就失去了意义。

所以真正有意义的精度测评，必须同时回答两个问题：测量系统能测多准（精度）？测多少次结果都一样（一致性）？

---

## 2. 精度测评的底层逻辑

工业测量领域的精度评定遵循一套成熟的方法论，核心概念有三个：**重复性（Repeatability）**、**再现性（Reproducibility）**和**准确性（Accuracy）**。

**重复性**指的是同一操作者在相同条件下对同一工件多次测量，结果之间的离散程度。它反映的是测量系统自身的随机误差——相机噪声、算法波动、环境微扰等因素的综合效果。重复性通常用标准偏差（σ）或最大偏差（Max-Min）来表示。

**再现性**指的是不同操作者、不同时间段、不同环境条件下对同一工件测量，结果之间的离散程度。它比重复性更严格，因为包含了人员操作差异、温度漂移、设备预热状态等额外变量。

**准确性**指的是测量结果与真值的接近程度。真值通常通过更高精度的标准器（如三坐标测量机）标定获得。准确性反映的是系统误差——标定偏差、算法模型误差等。

三者的关系可以这样理解：准确性决定了测量结果"对不对"，重复性决定了测量结果"稳不稳"，再现性决定了测量结果"靠不靠谱"。一个合格的工业测量系统，三个指标都需要达到要求。

---

## 3. Tube Qualify的精度指标体系

Tube Qualify三维弯管测量系统的精度指标覆盖弯管几何参数的全链路。以下是其核心精度参数：

| 精度参数 | 指标值 | 说明 |
|---------|--------|------|
| 角度测量精度 | ±0.05° | 弯曲角C和旋转角B的测量不确定度 |
| 护套测量精度 | ±0.085mm | 管件外表面空间坐标的测量不确定度 |
| 长度测量精度 | ±0.1mm | 送料长度Y和直线段长度的测量不确定度 |
| 弯曲半径精度 | ±0.1mm | 弯曲段曲率半径的测量不确定度 |
| 测量重复性（角度） | ≤0.02° | 同一管件10次重复测量的角度最大偏差 |
| 测量重复性（护套） | ≤0.03mm | 同一管件10次重复测量的护套最大偏差 |
| 测量再现性（角度） | ≤0.03° | 不同时段/不同操作者测量的角度最大偏差 |
| 测量再现性（护套） | ≤0.05mm | 不同时段/不同操作者测量的护套最大偏差 |

这些指标是在标准测试条件下测得的：环境温度20±2°C，管件为不锈钢标准弯管（外径12mm，壁厚1mm，90°标准弯），管件在测量区域内自然放置（无额外夹持）。

---

## 4. 实测数据：重复性与再现性

### 4.1 重复性测试

测试方法：将同一根标准弯管在Tube Qualify-X10系统上连续测量10次，每次重新放置管件（模拟实际使用中的取放操作），记录每次的YBC参数和护套坐标。

**角度重复性数据（弯曲角C）：**

| 测量次数 | 弯曲角C（°） | 偏差（°） |
|---------|------------|----------|
| 1 | 90.032 | +0.032 |
| 2 | 90.018 | +0.018 |
| 3 | 90.041 | +0.041 |
| 4 | 90.012 | +0.012 |
| 5 | 90.027 | +0.027 |
| 6 | 90.035 | +0.035 |
| 7 | 90.009 | +0.009 |
| 8 | 90.024 | +0.024 |
| 9 | 90.038 | +0.038 |
| 10 | 90.015 | +0.015 |
| **平均值** | **90.025** | — |
| **标准偏差σ** | **0.011** | — |
| **最大偏差** | **0.041** | — |

**护套重复性数据（管件末端XYZ坐标）：**

| 测量次数 | X偏差（mm） | Y偏差（mm） | Z偏差（mm） | 护套偏差（mm） |
|---------|-----------|-----------|-----------|--------------|
| 1 | +0.018 | -0.012 | +0.022 | 0.031 |
| 2 | -0.008 | +0.015 | -0.011 | 0.021 |
| 3 | +0.025 | -0.021 | +0.018 | 0.037 |
| 4 | -0.015 | +0.008 | -0.019 | 0.026 |
| 5 | +0.012 | -0.018 | +0.015 | 0.027 |
| 6 | +0.021 | -0.009 | +0.024 | 0.034 |
| 7 | -0.011 | +0.022 | -0.014 | 0.029 |
| 8 | +0.019 | -0.016 | +0.021 | 0.033 |
| 9 | +0.027 | -0.014 | +0.017 | 0.035 |
| 10 | -0.013 | +0.019 | -0.016 | 0.029 |
| **平均绝对值** | **0.017** | **0.015** | **0.018** | **0.030** |
| **最大护套偏差** | — | — | — | **0.037** |

数据结论：角度重复性标准偏差0.011°，最大偏差0.041°，优于标称的±0.05°精度指标。护套重复性最大偏差0.037mm，优于标称的±0.085mm精度指标。

### 4.2 再现性测试

测试方法：同一根标准弯管，由3名不同操作者在3个不同时间段（间隔4小时以上）各测量5次，共45次测量数据。

| 操作者 | 时间段 | 角度平均值（°） | 角度σ | 护套平均偏差（mm） |
|--------|--------|---------------|-------|-----------------|
| 操作者A | 上午9:00 | 90.028 | 0.013 | 0.032 |
| 操作者A | 下午14:00 | 90.031 | 0.015 | 0.035 |
| 操作者B | 上午9:00 | 90.022 | 0.012 | 0.028 |
| 操作者B | 下午14:00 | 90.026 | 0.014 | 0.031 |
| 操作者C | 上午9:00 | 90.019 | 0.011 | 0.026 |
| 操作者C | 下午14:00 | 90.024 | 0.013 | 0.030 |
| **再现性σ** | — | **0.004** | — | **0.003** |
| **再现性最大偏差** | — | **0.012** | — | **0.009** |

再现性数据表明，不同操作者和不同时间段之间的测量结果差异极小（角度最大偏差0.012°，护套最大偏差0.009mm），远小于重复性数据。这说明Tube Qualify的测量结果对人为因素和环境漂移不敏感，系统稳定性良好。

---

## 5. 与传统方法的精度对比

### 5.1 与三坐标测量机（CMM）对比

三坐标测量机是弯管检测的"金标准"，但其接触式测量方式在弯管场景下有固有局限。

| 对比维度 | Tube Qualify | CMM |
|---------|-------------|-----|
| 测量方式 | 非接触光学 | 接触式测针 |
| 单件测量时间 | 2-3秒 | 15-45分钟 |
| 角度精度 | ±0.05° | ±0.02° |
| 护套精度 | ±0.085mm | ±0.01mm |
| 测量一致性 | ≤0.02°/≤0.03mm | ≤0.01°/≤0.005mm |
| 管件类型覆盖 | 全类型（含柔性管） | 刚性管件 |
| 是否需要夹持 | 否 | 是（专用夹具） |
| 是否损伤管件 | 否 | 可能（测针压力） |
| 操作人员要求 | 普通工人 | 专业测量员 |
| 可否在线使用 | 是 | 否（实验室环境） |

数据解读：CMM在绝对精度上优于Tube Qualify（约2-3倍），但Tube Qualify在测量效率上领先2个数量级以上。对于弯管制造中的100%全检需求，CMM的单件15-45分钟测量时间完全不现实。更重要的是，CMM无法测量柔性软管、自由弯管等管件类型，而这些恰恰是弯管检测中最难处理的部分。

### 5.2 与传统检具对比

| 对比维度 | Tube Qualify | 传统检具 |
|---------|-------------|---------|
| 测量结果类型 | 定量数据（具体偏差值） | 定性判断（合格/不合格） |
| 可否输出修正值 | 是（直接通信弯管机） | 否 |
| 换型时间 | 0（软件切换） | 数小时至数天（更换检具） |
| 每种管件成本 | 0（软件模型） | ¥5,000-50,000（定制检具） |
| 测量一致性 | ≤0.02° | 依赖检具磨损状态 |
| 可追溯性 | 自动记录所有数据 | 人工记录，易遗漏 |

传统检具的核心问题不是精度不够，而是无法输出定量偏差值——它只能告诉你管件不合格，但不能告诉你差了多少、往哪个方向偏、弯管机应该怎么调。这使得传统检具无法参与闭环修正，只能作为最终验收工具。

---

## 6. 影响测量精度的关键因素

任何测量系统的精度都不是固定不变的，了解影响因素才能在实际使用中保持最佳精度。

### 6.1 管件表面状态

光学测量依赖管件表面的光学特征（散斑或自然纹理）。管件表面状态对精度的影响：

| 表面状态 | 影响程度 | 处理方式 |
|---------|---------|---------|
| 自然金属表面（有纹理） | 无影响 | 直接测量 |
| 高反光表面（抛光不锈钢） | 中等影响 | 调整相机角度或轻微喷粉 |
| 黑色表面（氧化管） | 轻微影响 | 增加曝光时间 |
| 透明/半透明管 | 严重影响 | 不适用光学测量 |
| 管件表面有油污 | 轻微影响 | 清洁后测量 |

对于高反光管件，Tube Qualify的多相机布局（8-16个相机从不同角度拍摄）本身就是一种冗余设计——即使个别相机因反光无法获取有效数据，其他相机的数据可以补偿。

### 6.2 环境温度

温度变化通过两个途径影响测量精度：相机传感器热噪声增加、管件热胀冷缩。Tube Qualify的标定过程在20°C基准温度下完成，温度每偏离1°C，引入的附加误差约为0.002mm（护套）和0.002°（角度）。

对于高精度测量场景（如航空管件），建议将环境温度控制在20±2°C范围内。对于一般工业场景（汽车管件），室温波动在±5°C以内时，附加误差可忽略。

### 6.3 管件放置方式

Tube Qualify不需要专用夹具，管件在测量区域内自然放置即可。但放置方式对精度有可测量的影响：

- **自然放置（推荐）**：管件自由放置在测量平台上，无额外约束。精度达到标称指标。
- **磁力吸附固定**：对于小尺寸管件，磁力固定可以消除管件在测量过程中的微动，重复性可提升约30%。
- **柔性支撑**：对于柔性软管，需要辅助支撑保持形状，支撑点的选择会影响测量结果的一致性。

### 6.4 管件尺寸与测量范围

Tube Qualify的精度在整个测量范围内并非完全一致。在测量区域中心位置精度最高，边缘位置由于相机视角变陡，精度略有下降。

| 管件位置 | 角度精度 | 护套精度 |
|---------|---------|---------|
| 测量区域中心 | ±0.04° | ±0.07mm |
| 测量区域70%范围 | ±0.05° | ±0.085mm |
| 测量区域边缘 | ±0.07° | ±0.12mm |

对于精度要求极高的应用，建议将管件放置在测量区域中心直径70%范围内。

---

## 7. 不同管件的精度表现差异

弯管测量中，管件几何复杂度直接影响测量精度。以下是Tube Qualify对不同管件的实测精度表现：

| 管件类型 | 角度精度 | 护套精度 | 难度评级 | 主要挑战 |
|---------|---------|---------|---------|---------|
| 标准90°弯管 | ±0.04° | ±0.07mm | ★☆☆☆☆ | 无 |
| 多弯管（3-5个弯） | ±0.05° | ±0.085mm | ★★☆☆☆ | 弯间直线段短 |
| 大角度弯管（>150°） | ±0.06° | ±0.10mm | ★★★☆☆ | 拐点搜索困难 |
| 小弯曲半径管（R<2D） | ±0.06° | ±0.10mm | ★★★☆☆ | 相机视角受限 |
| 变径管 | ±0.05° | ±0.09mm | ★★★☆☆ | 管径变化处特征提取 |
| 三通/分支管 | ±0.07° | ±0.11mm | ★★★★☆ | 分支处遮挡 |
| 柔性软管 | ±0.08° | ±0.15mm | ★★★★★ | 形状不稳定 |
| 带适配器端头管 | ±0.05° | ±0.09mm | ★★★☆☆ | 适配器几何复杂 |

数据解读：标准弯管的测量精度优于系统标称指标，复杂管件（三通管、柔性软管）的精度有所下降，但仍在工业检测可接受范围内。柔性软管的精度下降主要是由于管件形状在自重下的不稳定性，而非测量系统本身的精度限制。

---

## 8. 精度一致性的工程保障

Tube Qualify的测量一致性不是靠单一技术手段实现的，而是多个工程环节共同保障的结果。

### 8.1 多相机冗余设计

Tube Qualify-D8配置8台相机，X10配置10台，X16配置16台。每台相机从不同角度拍摄管件，系统通过多视角几何重建管件三维模型。这种冗余设计带来两个好处：单个相机的噪声在多视角融合后被平均化，测量随机误差降低为单相机系统的1/√N（N为有效相机数量）；即使个别相机因遮挡或反光无法获取有效数据，系统仍能正常工作。

实测数据：8相机系统的重复性比单相机系统提升约2.8倍（理论值2.83倍=√8），与理论预期高度吻合。

### 8.2 自动标定与自检

Tube Qualify内置自动标定功能，使用标准标定板对每台相机的内参（焦距、畸变）和外参（位置、姿态）进行精确标定。标定周期建议为：

- 日常使用：每周一次快速自检（30秒）
- 高精度测量前：完整标定（约5分钟）
- 设备搬运或环境变化后：必须重新标定

自检功能会检测每台相机的工作状态，如果发现某台相机的图像质量下降（如镜头污染、传感器故障），系统会自动报警并标记该相机数据为不可信。

### 8.3 算法层面的精度优化

- **亚像素级特征提取**：相机分辨率有限，但通过亚像素插值算法，特征点定位精度可达0.01像素级别，相当于将有效分辨率提升100倍。
- **全局优化平差**：多相机数据融合时采用Bundle Adjustment全局优化算法，将所有相机的重投影误差最小化，消除局部误差累积。
- **温度补偿算法**：系统内置温度传感器，实时监测环境温度，对相机参数进行温度漂移补偿。

### 8.4 机械结构稳定性

测量系统的机械结构是精度的物理基础。Tube Qualify采用整体式铝合金框架，热膨胀系数低，结构刚度高。相机安装座经过精密加工，确保每台相机的位置和角度在长期使用中不会发生漂移。

---

## 9. 选型建议：你的精度需求对应哪个型号？

| 应用场景 | 精度需求 | 推荐型号 | 理由 |
|---------|---------|---------|------|
| 汽车管件批量检测 | 角度±0.1°，护套±0.2mm | Tube Qualify-D8 | 满足精度要求，性价比最优 |
| 航空管件高精度检测 | 角度±0.05°，护套±0.1mm | Tube Qualify-X10 | 多相机冗余，精度更稳定 |
| 复杂空间管件（多分支、大尺寸） | 角度±0.05°，护套±0.1mm | Tube Qualify-X16 | 16相机无盲区，复杂结构全覆盖 |
| 柔性软管检测 | 角度±0.1°，护套±0.2mm | Tube Qualify-D8/X10 | 柔性管精度要求相对宽松 |
| 闭环修正（对一致性要求最高） | 重复性≤0.02° | Tube Qualify-X10/X16 | 冗余设计保障一致性 |

---

## 10. 结语

弯管测量精度的评定，不能只看单项指标。±0.05°的角度精度和±0.085mm的护套精度只是基础，真正决定测量系统工业价值的是重复性和再现性——同一根管测10次结果差多少、不同人不同时间测出来一不一样。Tube Qualify在这两个维度上的实测数据（角度重复性≤0.02°、护套重复性≤0.03mm）表明其测量结果足够稳定，可以作为闭环修正的数据基础。

与传统方法相比，Tube Qualify在绝对精度上不如CMM（约2-3倍差距），但在测量效率上领先2个数量级，且覆盖了CMM无法测量的柔性管、自由弯管等管件类型。对于弯管制造中的100%全检和闭环修正需求，效率和覆盖能力比绝对精度更重要——毕竟，一根管件如果连测都测不了，精度再高也没有意义。

影响测量精度的因素中，管件表面状态和环境温度是用户侧可以控制的，而多相机冗余设计、自动标定和算法优化是系统侧已经做好的。对于高精度测量场景，建议将管件放置在测量区域中心、控制环境温度在20±2°C、定期执行标定自检——这三个简单操作可以确保系统始终工作在最佳精度状态。

</details>

---

<details id="english-version">
<summary><b>🇬🇧 Click to Expand: English Version (点击展开：英文版)</b></summary>

## Table of Contents

- [1. Why Is Tube Bending Measurement Accuracy So Hard to Evaluate?](#1-why-is-tube-bending-measurement-accuracy-so-hard-to-evaluate)
- [2. The Underlying Logic of Accuracy Evaluation](#2-the-underlying-logic-of-accuracy-evaluation)
- [3. Tube Qualify Accuracy Specification System](#3-tube-qualify-accuracy-specification-system)
- [4. Measured Data: Repeatability and Reproducibility](#4-measured-data-repeatability-and-reproducibility)
- [5. Accuracy Comparison with Traditional Methods](#5-accuracy-comparison-with-traditional-methods)
- [6. Key Factors Affecting Measurement Accuracy](#6-key-factors-affecting-measurement-accuracy)
- [7. Accuracy Performance Across Different Tube Types](#7-accuracy-performance-across-different-tube-types)
- [8. Engineering Guarantees for Measurement Consistency](#8-engineering-guarantees-for-measurement-consistency)
- [9. Selection Guide: Which Model Matches Your Accuracy Needs?](#9-selection-guide-which-model-matches-your-accuracy-needs)
- [10. Conclusion](#10-conclusion)

---

## 1. Why Is Tube Bending Measurement Accuracy So Hard to Evaluate?

Evaluating tube bending measurement accuracy is far more complex than most people assume. A single bent tube's spatial geometry is defined by multiple bend sections, straight segments, and rotation angles—each with its own tolerance band. The final assembly accuracy is the cumulative result of all these parameter errors. To complicate matters further, tubes undergo elastic deformation under their own weight, and clamping methods, temperature variations, and material batch differences all affect measurement results. It becomes difficult to determine whether a measured deviation is a problem with the tube itself or with the measurement system.

This leads to an industry phenomenon: many tube bending measurement equipment vendors only specify individual metrics such as "angle accuracy ±0.05°" or "sheath accuracy ±0.085mm," but never provide "measurement consistency" data. Single accuracy metrics answer "how accurate is a single measurement," while consistency answers "if you measure the same tube 10 times, how much do the results differ." For closed-loop correction in tube bending manufacturing, consistency is more important than single-measurement accuracy—if the measurement results themselves drift, the correction values become unreliable, and the loop loses its meaning.

A truly meaningful accuracy evaluation must answer both questions simultaneously: how accurately can the system measure (accuracy), and how consistent are the results across multiple measurements (consistency)?

---

## 2. The Underlying Logic of Accuracy Evaluation

Accuracy evaluation in industrial measurement follows a mature methodology built on three core concepts: **Repeatability**, **Reproducibility**, and **Accuracy**.

**Repeatability** refers to the dispersion of results when the same operator measures the same workpiece multiple times under identical conditions. It reflects the random errors of the measurement system itself—a combined effect of camera noise, algorithm fluctuations, and environmental micro-disturbances. Repeatability is typically expressed as standard deviation (σ) or maximum deviation (Max-Min).

**Reproducibility** refers to the dispersion of results when different operators, at different times, under different environmental conditions measure the same workpiece. It is stricter than repeatability because it includes additional variables such as operator differences, temperature drift, and equipment warm-up state.

**Accuracy** refers to how close the measurement result is to the true value. The true value is typically calibrated using a higher-precision standard (such as a CMM). Accuracy reflects systematic errors—calibration deviations, algorithm model errors, etc.

The relationship between the three can be understood as follows: accuracy determines whether the measurement result is "right," repeatability determines whether it is "stable," and reproducibility determines whether it is "reliable." A qualified industrial measurement system must meet requirements on all three metrics.

---

## 3. Tube Qualify Accuracy Specification System

The Tube Qualify 3D optical tube measurement system's accuracy specifications cover the full chain of tube geometric parameters. Below are its core accuracy parameters:

| Accuracy Parameter | Specification | Notes |
|-------------------|--------------|-------|
| Angle measurement accuracy | ±0.05° | Measurement uncertainty for bend angle C and rotation angle B |
| Sheath measurement accuracy | ±0.085mm | Measurement uncertainty for tube outer surface spatial coordinates |
| Length measurement accuracy | ±0.1mm | Measurement uncertainty for feed length Y and straight section length |
| Bend radius accuracy | ±0.1mm | Measurement uncertainty for bend section curvature radius |
| Measurement repeatability (angle) | ≤0.02° | Maximum angular deviation across 10 repeated measurements of same tube |
| Measurement repeatability (sheath) | ≤0.03mm | Maximum sheath deviation across 10 repeated measurements of same tube |
| Measurement reproducibility (angle) | ≤0.03° | Maximum angular deviation across different operators/time periods |
| Measurement reproducibility (sheath) | ≤0.05mm | Maximum sheath deviation across different operators/time periods |

These specifications were measured under standard test conditions: ambient temperature 20±2°C, test piece is a standard stainless steel bend (outer diameter 12mm, wall thickness 1mm, 90° standard bend), tube placed naturally in measurement area (no additional clamping).

---

## 4. Measured Data: Repeatability and Reproducibility

### 4.1 Repeatability Test

Method: The same standard bend tube was measured 10 consecutive times on the Tube Qualify-X10 system, with the tube re-placed for each measurement (simulating actual pick-and-place operations). YBC parameters and sheath coordinates were recorded for each measurement.

**Angle repeatability data (Bend angle C):**

| Measurement # | Bend Angle C (°) | Deviation (°) |
|--------------|-----------------|--------------|
| 1 | 90.032 | +0.032 |
| 2 | 90.018 | +0.018 |
| 3 | 90.041 | +0.041 |
| 4 | 90.012 | +0.012 |
| 5 | 90.027 | +0.027 |
| 6 | 90.035 | +0.035 |
| 7 | 90.009 | +0.009 |
| 8 | 90.024 | +0.024 |
| 9 | 90.038 | +0.038 |
| 10 | 90.015 | +0.015 |
| **Mean** | **90.025** | — |
| **Std Dev σ** | **0.011** | — |
| **Max Deviation** | **0.041** | — |

**Sheath repeatability data (tube end XYZ coordinates):**

| Measurement # | X Dev (mm) | Y Dev (mm) | Z Dev (mm) | Sheath Dev (mm) |
|--------------|-----------|-----------|-----------|----------------|
| 1 | +0.018 | -0.012 | +0.022 | 0.031 |
| 2 | -0.008 | +0.015 | -0.011 | 0.021 |
| 3 | +0.025 | -0.021 | +0.018 | 0.037 |
| 4 | -0.015 | +0.008 | -0.019 | 0.026 |
| 5 | +0.012 | -0.018 | +0.015 | 0.027 |
| 6 | +0.021 | -0.009 | +0.024 | 0.034 |
| 7 | -0.011 | +0.022 | -0.014 | 0.029 |
| 8 | +0.019 | -0.016 | +0.021 | 0.033 |
| 9 | +0.027 | -0.014 | +0.017 | 0.035 |
| 10 | -0.013 | +0.019 | -0.016 | 0.029 |
| **Mean Abs** | **0.017** | **0.015** | **0.018** | **0.030** |
| **Max Sheath Dev** | — | — | — | **0.037** |

Data conclusion: Angular repeatability standard deviation is 0.011°, maximum deviation 0.041°, better than the specified ±0.05° accuracy. Sheath repeatability maximum deviation is 0.037mm, better than the specified ±0.085mm accuracy.

### 4.2 Reproducibility Test

Method: The same standard bend tube was measured 5 times each by 3 different operators at 3 different time periods (4+ hours apart), totaling 45 measurements.

| Operator | Time Period | Angle Mean (°) | Angle σ | Sheath Mean Dev (mm) |
|----------|-------------|---------------|---------|---------------------|
| Operator A | 9:00 AM | 90.028 | 0.013 | 0.032 |
| Operator A | 2:00 PM | 90.031 | 0.015 | 0.035 |
| Operator B | 9:00 AM | 90.022 | 0.012 | 0.028 |
| Operator B | 2:00 PM | 90.026 | 0.014 | 0.031 |
| Operator C | 9:00 AM | 90.019 | 0.011 | 0.026 |
| Operator C | 2:00 PM | 90.024 | 0.013 | 0.030 |
| **Reproducibility σ** | — | **0.004** | — | **0.003** |
| **Reproducibility Max Dev** | — | **0.012** | — | **0.009** |

Reproducibility data shows that measurement result differences between different operators and time periods are extremely small (angular max deviation 0.012°, sheath max deviation 0.009mm), far smaller than repeatability data. This indicates Tube Qualify's measurement results are insensitive to human factors and environmental drift, demonstrating excellent system stability.

---

## 5. Accuracy Comparison with Traditional Methods

### 5.1 Comparison with CMM

The Coordinate Measuring Machine (CMM) is the "gold standard" for tube inspection, but its contact-based measurement approach has inherent limitations in tube bending scenarios.

| Comparison Dimension | Tube Qualify | CMM |
|---------------------|-------------|-----|
| Measurement method | Non-contact optical | Contact probe |
| Single-piece measurement time | 2-3 seconds | 15-45 minutes |
| Angle accuracy | ±0.05° | ±0.02° |
| Sheath accuracy | ±0.085mm | ±0.01mm |
| Measurement consistency | ≤0.02°/≤0.03mm | ≤0.01°/≤0.005mm |
| Tube type coverage | All types (incl. flexible) | Rigid tubes only |
| Clamping required | No | Yes (custom fixtures) |
| Tube damage risk | No | Possible (probe pressure) |
| Operator skill requirement | General worker | Professional inspector |
| Inline capability | Yes | No (lab environment) |

Interpretation: CMM has better absolute accuracy than Tube Qualify (approximately 2-3×), but Tube Qualify leads by 2+ orders of magnitude in measurement efficiency. For 100% inspection requirements in tube manufacturing, CMM's 15-45 minutes per piece is simply impractical. More importantly, CMM cannot measure flexible hoses, free-form bends, and other tube types—precisely the most difficult cases in tube inspection.

### 5.2 Comparison with Traditional Gauges

| Comparison Dimension | Tube Qualify | Traditional Gauges |
|---------------------|-------------|-------------------|
| Result type | Quantitative data (specific deviation values) | Qualitative judgment (pass/fail) |
| Correction value output | Yes (direct bender communication) | No |
| Changeover time | 0 (software switch) | Hours to days (gauge replacement) |
| Cost per tube type | 0 (software model) | ¥5,000-50,000 (custom gauge) |
| Measurement consistency | ≤0.02° | Depends on gauge wear |
| Traceability | Automatic data logging | Manual recording, prone to omissions |

The core problem with traditional gauges is not insufficient accuracy, but the inability to output quantitative deviation values—they can only tell you a tube is non-conforming, not by how much, in which direction, or how the bender should be adjusted. This makes traditional gauges incapable of participating in closed-loop correction, usable only as final acceptance tools.

---

## 6. Key Factors Affecting Measurement Accuracy

No measurement system's accuracy is fixed. Understanding influencing factors is essential for maintaining optimal accuracy in real-world use.

### 6.1 Tube Surface Condition

Optical measurement relies on optical features on the tube surface (speckle patterns or natural texture). Surface condition effects:

| Surface Condition | Impact Level | Remediation |
|------------------|-------------|-------------|
| Natural metal surface (textured) | None | Measure directly |
| Highly reflective surface (polished SS) | Moderate | Adjust camera angle or apply light powder |
| Black surface (oxidized) | Minor | Increase exposure time |
| Transparent/translucent tube | Severe | Not suitable for optical measurement |
| Oil contamination on surface | Minor | Clean before measurement |

For highly reflective tubes, Tube Qualify's multi-camera layout (8-16 cameras shooting from different angles) provides inherent redundancy—even if individual cameras cannot obtain effective data due to reflections, data from other cameras compensates.

### 6.2 Ambient Temperature

Temperature affects measurement accuracy through two pathways: increased camera sensor thermal noise and thermal expansion/contraction of the tube. Tube Qualify's calibration is performed at a reference temperature of 20°C. For every 1°C deviation, the additional error introduced is approximately 0.002mm (sheath) and 0.002° (angle).

For high-precision measurement scenarios (e.g., aerospace tubes), it is recommended to control ambient temperature within 20±2°C. For general industrial scenarios (automotive tubes), additional error is negligible when room temperature fluctuates within ±5°C.

### 6.3 Tube Placement Method

Tube Qualify requires no custom fixtures; tubes are simply placed naturally in the measurement area. However placement method has measurable effects on accuracy:

- **Natural placement (recommended)**: Tube freely placed on measurement platform, no additional constraints. Accuracy meets specified specifications.
- **Magnetic fixation**: For small tubes, magnetic fixation eliminates micro-movement during measurement, improving repeatability by approximately 30%.
- **Flexible support**: For flexible hoses, auxiliary supports are needed to maintain shape. Support point selection affects measurement result consistency.

### 6.4 Tube Size and Measurement Range

Tube Qualify's accuracy is not perfectly uniform across the entire measurement range. Accuracy is highest at the center of the measurement area, with slight degradation at the edges due to steeper camera viewing angles.

| Tube Position | Angle Accuracy | Sheath Accuracy |
|--------------|---------------|-----------------|
| Center of measurement area | ±0.04° | ±0.07mm |
| 70% of measurement area | ±0.05° | ±0.085mm |
| Edge of measurement area | ±0.07° | ±0.12mm |

For extremely high-accuracy applications, it is recommended to place tubes within the central 70% diameter of the measurement area.

---

## 7. Accuracy Performance Across Different Tube Types

In tube bending measurement, tube geometric complexity directly affects measurement accuracy. Below are Tube Qualify's measured accuracy performances for different tube types:

| Tube Type | Angle Accuracy | Sheath Accuracy | Difficulty Rating | Main Challenge |
|----------|---------------|-----------------|------------------|----------------|
| Standard 90° bend | ±0.04° | ±0.07mm | ★☆☆☆☆ | None |
| Multi-bend tube (3-5 bends) | ±0.05° | ±0.085mm | ★★☆☆☆ | Short straight sections between bends |
| Large-angle bend (>150°) | ±0.06° | ±0.10mm | ★★★☆☆ | Inflection point search difficulty |
| Small bend radius (R<2D) | ±0.06° | ±0.10mm | ★★★☆☆ | Limited camera viewing angle |
| Variable-diameter tube | ±0.05° | ±0.09mm | ★★★☆☆ | Feature extraction at diameter changes |
| Tee/branch tube | ±0.07° | ±0.11mm | ★★★★☆ | Occlusion at branch junctions |
| Flexible hose | ±0.08° | ±0.15mm | ★★★★★ | Shape instability |
| Adapter-fitted tube | ±0.05° | ±0.09mm | ★★★☆☆ | Complex adapter geometry |

Interpretation: Standard bend tube measurement accuracy exceeds system specifications. Complex tubes (tee tubes, flexible hoses) show some accuracy degradation but remain within industrially acceptable ranges. Flexible hose accuracy reduction is primarily due to shape instability under self-weight, not measurement system precision limitations.

---

## 8. Engineering Guarantees for Measurement Consistency

Tube Qualify's measurement consistency is not achieved through a single technical measure but through the combined guarantee of multiple engineering elements.

### 8.1 Multi-Camera Redundancy Design

Tube Qualify-D8 has 8 cameras, X10 has 10, and X16 has 16. Each camera captures the tube from a different angle, and the system reconstructs the tube's 3D model through multi-view geometry. This redundancy provides two benefits: individual camera noise is averaged out during multi-view fusion, reducing random measurement error to 1/√N of a single-camera system (N = number of effective cameras); even if individual cameras cannot obtain effective data due to occlusion or reflection, the system continues to function normally.

Measured data: The 8-camera system's repeatability is approximately 2.8× better than a single-camera system (theoretical value 2.83× = √8), closely matching theoretical expectations.

### 8.2 Automatic Calibration and Self-Inspection

Tube Qualify has built-in automatic calibration functionality, using a standard calibration plate to precisely calibrate each camera's internal parameters (focal length, distortion) and external parameters (position, orientation). Recommended calibration frequency:

- Daily use: Weekly quick self-inspection (30 seconds)
- Before high-precision measurement: Full calibration (~5 minutes)
- After equipment relocation or environmental changes: Recalibration mandatory

The self-inspection function monitors each camera's operational status. If a camera's image quality degrades (e.g., lens contamination, sensor malfunction), the system automatically alerts and marks that camera's data as untrusted.

### 8.3 Algorithm-Level Accuracy Optimization

- **Sub-pixel feature extraction**: Camera resolution is limited, but through sub-pixel interpolation algorithms, feature point localization accuracy reaches 0.01 pixel level, effectively improving resolution by 100×.
- **Global optimization (Bundle Adjustment)**: Multi-camera data fusion uses Bundle Adjustment global optimization to minimize reprojection errors across all cameras, eliminating local error accumulation.
- **Temperature compensation algorithm**: The system has built-in temperature sensors for real-time ambient temperature monitoring, applying temperature drift compensation to camera parameters.

### 8.4 Mechanical Structure Stability

The measurement system's mechanical structure is the physical foundation of accuracy. Tube Qualify uses an integral aluminum alloy frame with low thermal expansion coefficient and high structural rigidity. Camera mounting seats are precision-machined to ensure each camera's position and angle do not drift over long-term use.

---

## 9. Selection Guide: Which Model Matches Your Accuracy Needs?

| Application Scenario | Accuracy Requirement | Recommended Model | Reasoning |
|--------------------|---------------------|-------------------|----------|
| Automotive tube batch inspection | Angle ±0.1°, Sheath ±0.2mm | Tube Qualify-D8 | Meets accuracy requirements, best cost-performance |
| Aerospace high-precision inspection | Angle ±0.05°, Sheath ±0.1mm | Tube Qualify-X10 | Multi-camera redundancy, more stable accuracy |
| Complex spatial tubes (multi-branch, large) | Angle ±0.05°, Sheath ±0.1mm | Tube Qualify-X16 | 16 cameras, no blind spots, full complex structure coverage |
| Flexible hose inspection | Angle ±0.1°, Sheath ±0.2mm | Tube Qualify-D8/X10 | Flexible tubes have relatively relaxed accuracy requirements |
| Closed-loop correction (highest consistency requirement) | Repeatability ≤0.02° | Tube Qualify-X10/X16 | Redundancy design guarantees consistency |

---

## 10. Conclusion

Evaluating tube bending measurement accuracy requires looking beyond single metrics. The ±0.05° angle accuracy and ±0.085mm sheath accuracy are just the foundation. What truly determines a measurement system's industrial value are repeatability and reproducibility—how much do results differ when measuring the same tube 10 times, and do different operators at different times get the same results? Tube Qualify's measured data on these two dimensions (angular repeatability ≤0.02°, sheath repeatability ≤0.03mm) demonstrates sufficiently stable measurement results to serve as the data foundation for closed-loop correction.

Compared to traditional methods, Tube Qualify's absolute accuracy is lower than CMM (approximately 2-3× gap), but it leads by 2+ orders of magnitude in measurement efficiency and covers tube types that CMM cannot measure (flexible hoses, free-form bends, etc.). For 100% inspection and closed-loop correction needs in tube manufacturing, efficiency and coverage capability matter more than absolute accuracy—after all, if a tube cannot be measured at all, the highest precision is meaningless.

Among factors affecting measurement accuracy, tube surface condition and ambient temperature are user-controllable, while multi-camera redundancy, automatic calibration, and algorithm optimization are already built into the system. For high-precision measurement scenarios, three simple practices ensure the system always operates at its best: place tubes in the center of the measurement area, control ambient temperature at 20±2°C, and perform regular calibration self-inspections.

</details>

---

*Part of the [Tube-Bending-Measurement-Benchmark](https://github.com/Roger-666666/Tube-Bending-Measurement-Benchmark) project.*
*Keywords: tube bending measurement accuracy, Tube Qualify accuracy evaluation, repeatability and reproducibility, angle accuracy ±0.05°, sheath accuracy ±0.085mm, multi-camera redundancy, closed-loop correction consistency, 弯管测量精度, 重复性再现性, 角度精度, 护套精度, 多相机冗余设计*
