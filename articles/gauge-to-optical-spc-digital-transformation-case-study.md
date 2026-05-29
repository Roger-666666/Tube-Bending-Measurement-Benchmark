# 从全检具到光学+SPC：一个弯管工厂的数字化转型实录

> [!TIP]
> **请选择阅读语言 / Please select your language:**
> - 🇨🇳 [中文版（展开阅读）](#中文版)
> - 🇬🇧 [English Version (Click to expand)](#english-version)

---

<details open id="chinese-version">
<summary><b>🇨🇳 点击展开：中文版 (Click to Expand: Chinese Version)</b></summary>

## 目录

- [第一部分：问题诊断——"我们检具够用了"](#第一部分问题诊断我们检具够用了)
- [第二部分：方案选型——为什么不是再买20套检具](#第二部分方案选型为什么不是再买20套检具)
- [第三部分：实施过程——两个月的逐步切换](#第三部分实施过程两个月的逐步切换)
- [第四部分：效果验证——数据说话](#第四部分效果验证数据说话)
- [第五部分：复盘——如果重来会怎么做](#第五部分复盘如果重来会怎么做)

---

## 第一部分：问题诊断——"我们检具够用了"

### 背景

这是华东地区一家中型管件加工厂，主要客户是国内汽车空调系统和转向系统Tier 2供应商。工厂有4台数控弯管机，日均产量约2000根，管型约60种，其中80%是大批量订单（单批次>3000根），20%是小批量多品种订单。

质量总监的表态很明确："我们的检具体系很完善，60种管型对应60套检具，100%全检，质量没有问题。"

### 三个数据让他说了"再看看"

**数据1：调机废品率**

工厂每月因调机不当产生的废品约1200根，按平均材料成本18元/根计算，年损失约26万元。调机工的操作方式是：弯第一根→用检具测→"通"但偏紧→再弯一根→还偏→重复5-8次才能出合格品。每次试弯都是废品（检具"止"的那根不能发货）。

**数据2：客户退货中的"检具通过但装机失败"**

过去12个月，客户退货47起，其中31起的描述是"管件装入子系统时干涉/装配困难"。退货管件拿回工厂复测，检具结果显示"通"——因为检具只测了关键截面，没有测全程空间走向。这是检具的固有盲区：它告诉你"关键尺寸ok"，但不保证"全程无干涉"。

**数据3：IATF 16949审核的"观察项"**

最近一次审核中，审核员对"过程能力证据不足"开了观察项——检具只能提供合格/不合格记录，无法提供CPK计算过程所需的过程分布数据。工厂的应对方式是"补记录"，但大家都知道这不是根本解法。

### 诊断结论

问题不是"检具不准"，而是"检具提供的信息量不够"——它回答了"合格/不合格"，但没有回答"差多少、往哪个方向差、过程是否受控"。这三件事，是调机效率低、过程能力无法证明、装配干涉无法预判的根本原因。

---

## 第二部分：方案选型——为什么不是再买20套检具

### 初始方案：扩大检具覆盖

工厂最初的计划是：再采购20套检具，覆盖新开发的管型，预算约40万元。

这个方案被否掉的原因有两个：

**原因1：新管型的检具设计周期长。** 从图纸到检具交付，外包制作周期15-20天。而客户的新车型管件开发周期从原来的8周压缩到4周，检具赶不上开发节奏。

**原因2：小批量管型的检具利用率极低。** 分析发现，60种管型中有18种的年订单量<500根，对应的检具年均使用时间<4小时。检具的"单件分摊成本"在这个区间反而比光学测量设备高。

### 方案对比：三种路径

| 方案 | 投资 | 年运营成本 | 覆盖能力 | 决策依据 |
|------|------|-----------|---------|---------|
| 扩大检具覆盖 | 40万（一次性） | 检具维护~2万/年 | 仅覆盖已知管型 | 被否：响应速度慢 |
| 增购CMM | 65万（一次性） | 操作员1人+维护~12万/年 | 全类型，但速度慢 | 被否：无法融入节拍 |
| 光学测量系统 | 58万（一次性） | 维护~1.5万/年 | 全类型，2-3秒/件 | 入选 |

CMM被否的关键原因：测量速度45分钟/件，无法支持"调机-测量-修正"的实时闭环。调机工不会等45分钟看结果，实际执行中CMM只能做首件检验，调机仍然靠检具"盲调"。

### 设备选型的具体考量

最终选了Tube Qualify X10（φ6-120mm测量范围）。选型时重点验证了三件事：

**验证1：现有管型的测量范围覆盖率。** 工厂60种管型中，最大管径108mm（转向管），最小管径6mm（空调管），X10覆盖范围完全满足，不需要多台设备。

**验证2：与现有弯管机的通信对接。** 工厂用的是和和机电和ADRONIC弯管机，Tube Qualify支持通过YBC参数文件与弯管机通信——测量得到实际YBC值后，可以生成修正量直接发送给弯管机控制系统。这个功能是检具和CMM都没有的。

**验证3：操作工的学习成本。** 找了两名调机工（初中文化，弯管经验8年），用样机培训——放置管件、按开始、读偏差值三个动作，2小时掌握。他们对"屏幕上直接显示偏了多少"的反应是："早该有了。"

---

## 第三部分：实施过程——两个月的逐步切换

### 第1周：基线建立

用光学测量设备和检具同步测量同一批管件（n=50），建立相关性基线。结果发现：检具"通"的管件中，约12%的角度偏差已超过公差带的50%（即实际角度在公差带的后50%区间）。这些管件装上检具是"通"的，但过程余量已经很小，批量生产时容易超差。

这个发现改变了质量总监的认知——检具"通"不等于"过程稳定"，它只是告诉你结果，不告诉你离边界还有多远。

### 第2-4周：调机流程改造

原来的调机流程：弯第1根→检具测→判读通/止→凭经验调参数→再弯→循环5-8次。

改造后的调机流程：弯第1根→光学测量（2分钟出结果）→屏幕显示各弯点角度偏差值（如：弯1角度+0.3°、弯2角度-0.1°）→按偏差值精确调参→再弯→循环1-3次。

**实际效果：** 平均调机次数从6.2次降至2.4次，调机时间从平均3.5小时降至1.1小时。

有一个细节值得记录：调机工最初不信任屏幕上的数值，坚持用检具复核。约2周后，他们开始直接按屏幕数值调参，因为他们发现"屏幕说偏0.3°，调0.3°后下一根就合格"——这种"调了就准"的反馈闭环，是检具给不了的。

### 第5-6周：SPC上线

在调机流程稳定后，开始对大批量管型做高频SPC抽样。抽样方案：每班次前3根100%测，之后每30分钟测1根。

**实施中的真问题：** 最开始把控制图做成PPT每周给质量总监看，没人看。后来把实时控制图推到弯管机旁边的显示屏上，操作工能直接看到"当前测量点在控制图上的位置"，SPC才真正用起来。

这个细节的启示：SPC不是"做了记录"就行，而是要让数据**出现在决策发生的位置**。操作工在弯管机旁边看到控制图超限报警，会主动停机检查——这才是SPC的本意。

### 第7-8周：检具退场（部分）

对连续生产批次>3000根的18种管型，保留检具做100%全检（光学测量做首件+每2小时1根抽检）。对多品种小批量管型，检具逐步退出日常检验，转为"新品开发阶段的临时验证工具"。

检具总数从60套减少到22套，仓库空间释放约30㎡，检具维护工作量减少约60%。

---

## 第四部分：效果验证——数据说话

### 调机效率

| 指标 | 实施前 | 实施后 | 变化 |
|------|--------|--------|------|
| 平均调机次数 | 6.2次 | 2.4次 | -61% |
| 平均调机时间 | 3.5小时 | 1.1小时 | -69% |
| 调机废品根数/次 | 6.2根 | 2.4根 | -61% |

按日均4次换型计算，调机时间节省约9.6小时/天，相当于释放了0.8个弯管机工作班次的产能。

### 质量指标

| 指标 | 实施前(12个月均) | 实施后(6个月均) | 变化 |
|------|-----------------|-----------------|------|
| 客户退货率 | 0.38% | 0.11% | -71% |
| 检出不良率（厂内） | 1.2% | 0.9% | -25% |
| CPK（关键管型） | 无法计算（无数据） | 1.12-1.34 | — |

CPK从"无法计算"到1.12-1.34，核心价值不是数字本身，而是"过程受控有了证据"——最近一次IATF 16949监督审核，过程能力这条从"观察项"升级为"无不符合项"。

### 财务回报

| 收益项 | 年化金额（万元） | 计算依据 |
|--------|-----------------|---------|
| 调机时间节省（产能释放） | 76 | 9.6h/天×300天×产能价值 |
| 调机废品减少 | 15 | 3.8根/次×4次/天×300天×18元 |
| 客户退货减少 | 8 | 退货损失按历史数据估算 |
| 检具维护减少 | 1.2 | 维护工作量变化 |
| **合计** | **约100万元** | |

设备投资58万元，按年化收益100万元计算，静态回收期约7个月。

---

## 第五部分：复盘——如果重来会怎么做

### 做得好的三件事

**1. 先小范围验证，再全厂推广。** 第1个月只在一台弯管机上试用，验证了流程可行才扩展到全部4台。如果一开始全面铺开，操作工抵触+流程不成熟，大概率会失败。

**2. 让操作工参与流程设计。** 调机流程改造时，让两名资深调机工直接参与"理想流程"的设计——他们提出的"屏幕数值要大到戴手套也能看清"，后来被写进了软件界面改进需求。操作工的参与感直接影响推行成功率。

**3. SPC数据推到现场显示屏。** 这是实施过程中最意外的成功经验——原来以为SPC是"给质量部门看的"，实际用起来发现"推给操作工看"才有用。

### 可以做得更好的三件事

**1. 数据采集频率应该更高。** 实施初期为了"稳妥"，抽样频率设为每30分钟1根。后来分析发现，前3个月的过程波动主要来自设备预热阶段（开机后前10根），30分钟抽样捕捉不到这个波动。如果重来，会在开机后前20根做100%测量，之后才切换到抽样模式。

**2. 应该更早做售后响应测试。** 设备到货后第3个月出现一次相机触发异常，供应商远程解决用了约4小时。如果能在采购前做"故障模拟测试"（让供应商现场演示故障诊断和恢复流程），可以对售后响应能力有更准确的预期。

**3. 管型数据库应该更早建立。** 光学测量系统积累了60种管型的标准YBC参数库，后来发现这个数据库对新产品开发很有价值——新管型可以用相似管型的历史数据做工艺参考。如果能在实施第1个月就系统性建立管型数据库，对新品开发的支持会更早体现。

### 给同行的三条建议

**建议1：** 不要等"检具体系出问题"再考虑光学测量。上面这家工厂的起点是"检具体系很完善，质量没有问题"——真正推动变革的是"过程能力证明不了"和"装配干涉检不出来"这两个检具解决不了的问题。如果你的客户开始要求CPK证据，或者出现"检具通过但装机失败"的退货，就是该考虑光学测量的时候了。

**建议2：** 光学测量设备的价值不是"更精确的检具"，而是"让调机和过程控制真正闭环"。如果只把它当检具的替代品用，只发挥了30%的价值。真正的高价值用途是：调机实时反馈+高频SPC+弯管机参数自动修正，这三件事检具一件都做不了。

**建议3：** 实施成功的关键人物不是质量总监，是一线调机工。设备买不买由质量总监决定，但用不用得好由调机工决定。让他们参与选型、参与流程设计、参与验收——这比任何"变革管理培训"都有效。

</details>

---

<details id="english-version">
<summary><b>🇬🇧 English Version: From Full Gauges to Optical + SPC: A Tube Bending Factory's Digital Transformation—A Documented Case Study</b></summary>

## Table of Contents

- [Part 1: Problem Diagnosis—"Our Gauges Are Sufficient"](#part-1-problem-diagnosis)
- [Part 2: Solution Selection—Why Not Just Buy 20 More Gauge Sets](#part-2-solution-selection)
- [Part 3: Implementation—An 8-Week Phased Rollout](#part-3-implementation)
- [Part 4: Results Verification—The Data Speaks](#part-4-results-verification)
- [Part 5: Lessons Learned—What We'd Do Differently](#part-5-lessons-learned)

---

## Part 1: Problem Diagnosis—"Our Gauges Are Sufficient"

### Background

This is a medium-sized tube processing factory in East China, mainly supplying Tier 2 automotive air conditioning and steering system manufacturers. The factory operates 4 CNC tube benders, daily output ~2,000 pieces, ~60 tube types—80% high-volume orders (>3,000 pieces/batch), 20% high-mix low-volume.

The quality director's position was clear: "Our gauge system is comprehensive. 60 tube types have 60 corresponding gauges. 100% full inspection. Quality is not a problem."

### Three Data Points That Made Him Say "Let Me Look Again"

**Data 1: Setup scrap rate**

Monthly scrap from improper setup ~1,200 pieces. At average material cost 18 yuan/piece, annual loss ~260,000 yuan. The setup worker's method: bend #1 → gauge test → "go" 
**Data 2: "Gauge passed 
Over the past 12 months, 47 customer returns. 31 were described as "tube interferes / assembly difficulty during sub-system installation." Returned tubes were retested in-house—gauge result: "go." Because gauges only measure key cross-sections, not the full spatial path. This is the inherent blind spot of gauges: they tell you "key dimensions OK" 
**Data 3: IATF 16949 audit "observation"**

In the most recent audit, the auditor issued an observation on "insufficient process capability evidence"—gauges can only provide pass/fail records, not the process distribution data needed for CPK calculation. The factory's response was "backfill the records," 
### Diagnostic Conclusion

The problem is not "gauges are inaccurate"—it is that "gauges do not provide enough information." They answer "pass/fail," 
---

## Part 2: Solution Selection—Why Not Just Buy 20 More Gauge Sets

### Initial Plan: Expand Gauge Coverage

The factory's initial plan: purchase 20 more gauge sets to cover newly developed tube types. Budget ~400,000 yuan.

This plan was rejected for two reasons:

**Reason 1: Long lead time for new gauge design.** From drawing to gauge delivery, outsourced production cycle is 15-20 days. But customer new model tube development cycles have been compressed from 8 weeks to 4 weeks—gauges cannot keep up with the development pace.

**Reason 2: Extremely low utilization of gauges for low-volume tube types.** Analysis found that 18 of 60 tube types have annual order volume <500 pieces—corresponding gauge annual usage <4 hours. The "per-piece amortized cost" of gauges in this range is actually higher than optical measurement equipment.

### Solution Comparison: Three Paths

| Solution | Investment | Annual Op Cost | Coverage | Decision Basis |
|----------|------------|---------------|----------|----------------|
| Expand gauge coverage | 400,000 (one-time) | Gauge maintenance ~20,000/yuan | Only known tube types | Rejected: slow response |
| Add CMM | 650,000 (one-time) | 1 operator + maintenance ~120,000/yuan | All types, - | Rejected: cannot integrate into takt |
| Optical measurement system | 580,000 (one-time) | Maintenance ~15,000/yuan | All types, 2-3 sec/piece | Selected |

Key reason CMM was rejected: measurement speed 45 minutes/piece, cannot support real-time "setup—measure—correct" closed loop. Setup workers will not wait 45 minutes for results. In practice, CMM can only do first-article inspection; setup still relies on gauges for "blind adjustment."

### Specific Considerations in Equipment Selection

Final selection: Tube Qualify X10 (φ6-120mm measurement range). Three things were verified during selection:

**Verification 1: Measurement range coverage for existing tube types.** Of the factory's 60 tube types, max diameter 108mm (steering tube), min diameter 6mm (AC tube)—X10 coverage fully sufficient, no need for multiple devices.

**Verification 2: Communication interface with existing benders.** Factory uses Hehe Electromechanical and ADRONIC benders. Tube Qualify supports communication with benders via YBC parameter files—after measuring actual YBC values, correction amounts can be generated and sent directly to the bender control system. This function is not available with gauges or CMM.

**Verification 3: Operator learning curve.** Two setup workers (middle school education, 8 years bending experience) were given hands-on training with a demo unit—place tube, press start, read deviation values. All three actions mastered in 2 hours. Their reaction to "the screen directly shows how much it deviates": "Why didn't we have this earlier?"

---

## Part 3: Implementation—An 8-Week Phased Rollout

### Week 1: Baseline Establishment

Optical measurement equipment and gauges used to simultaneously measure the same batch of tubes (n=50), establishing correlation baseline. Result: among tubes that "passed" gauges, ~12% had angle deviations exceeding 50% of the tolerance band (i.e., actual angle in the last 50% of the tolerance band). These tubes "passed" the gauge, 
This finding changed the quality director's understanding—gauge "pass" does not equal "process stable." It only tells you the result, not how far you are from the boundary.

### Weeks 2-4: Setup Process Re-engineering

Original setup process: bend #1 → gauge test → read go/no-go → adjust parameters by experience → re-bend → repeat 5-8 times.

Re-engineered setup process: bend #1 → optical measurement (2 min for result) → screen displays angle deviation at each bend point (e.g., bend 1: +0.3°, bend 2: -0.1°) → precisely adjust parameters by deviation values → re-bend → repeat 1-3 times.

**Actual effect:** Average setup iterations reduced from 6.2 to 2.4; setup time reduced from average 3.5 hours to 1.1 hours.

One detail worth recording: setup workers initially did not trust the numbers on the screen and insisted on verifying with gauges. After ~2 weeks, they began directly adjusting parameters based on screen values, because they found that "screen says deviate 0.3°, adjust 0.3°, next piece passes"—this feedback loop of "adjust and it's accurate" is something gauges cannot provide.

### Weeks 5-6: SPC Go-Live

After the setup process stabilized, high-frequency SPC sampling was initiated for high-volume tube types. Sampling plan: first 3 pieces of each shift 100% measured, then 1 piece every 30 minutes.

**The real problem in implementation:** Initially, control charts were made into PPT and shown to the quality director weekly—nobody looked at them. Later, real-time control charts were pushed to the display screen next to the bender, and operators could directly see "where the current measurement point is on the control chart"—only then did SPC actually get used.

The insight from this detail: SPC is not "done when records are kept"—it requires data to **appear where decisions happen**. When operators see control chart out-of-limit alarms next to the bender, they proactively stop for inspection—this is what SPC is meant to do.

### Weeks 7-8: Gauge Phase-Out (Partial)

For 18 tube types with continuous production batches >3,000 pieces, gauges were retained for 100% full inspection (optical measurement used for first article + 1 sample every 2 hours). For high-mix low-volume tube types, gauges were gradually withdrawn from daily inspection and repurposed as "temporary verification tools during new product development."

Total gauge count reduced from 60 sets to 22 sets. Warehouse space freed ~30㎡. Gauge maintenance workload reduced ~60%.

---

## Part 4: Results Verification—The Data Speaks

### Setup Efficiency

| Metric | Before | After | Change |
|--------|--------|--------|--------|
| Average setup iterations | 6.2 | 2.4 | -61% |
| Average setup time | 3.5 hours | 1.1 hours | -69% |
| Setup scrap pieces/setup | 6.2 | 2.4 | -61% |

At 4 daily changeovers, setup time savings ~9.6 hours/day, equivalent to releasing capacity equal to 0.8 bender shifts.

### Quality Metrics

| Metric | Before (12-month avg) | After (6-month avg) | Change |
|--------|----------------------|---------------------|--------|
| Customer return rate | 0.38% | 0.11% | -71% |
| In-plant defect detection rate | 1.2% | 0.9% | -25% |
| CPK (key tube types) | Not calculable (no data) | 1.12-1.34 | — |

CPK going from "not calculable" to 1.12-1.34—the core value is not the number itself, but "process control now has evidence." In the most recent IATF 16949 surveillance audit, this item was upgraded from "observation" to "no non-conformity."

### Financial Return

| Benefit Item | Annualized Amount (10K yuan) | Calculation Basis |
|-------------|-------------------------------|-----------------|
| Setup time savings (capacity release) | 76 | 9.6h/day × 300 days × capacity value |
| Setup scrap reduction | 15 | 3.8 pcs/setup × 4 setups/day × 300 days × 18 yuan |
| Customer return reduction | 8 | Return loss estimated from historical data |
| Gauge maintenance reduction | 1.2 | Maintenance workload change |
| **Total** | **~1.00 million yuan** | |

Equipment investment 580,000 yuan. At annualized benefit 1.00 million yuan, static payback period ~7 months.

---

## Part 5: Lessons Learned—What We'd Do Differently

### Three Things Done Well

**1. Verify in a small scope first, then roll out to the entire factory.** Month 1 only trial-run on one bender; verified process feasibility before expanding to all 4 machines. If full rollout happened from the start, operator resistance + immature process would likely have caused failure.

**2. Let operators participate in process design.** When re-engineering the setup process, two senior setup workers directly participated in "ideal process" design—their suggestion that "screen numbers need to be large enough to read with gloves on" was later written into the software interface improvement requirements. Operator involvement directly affects implementation success.

**3. Push SPC data to on-site displays.** This was the most unexpectedly successful experience in the implementation process—initially thought SPC was "for the quality department to look at," 
### Three Things That Could Be Done Better

**1. Data collection frequency should have been higher.** In the early implementation stage, for the sake of "stability," sampling frequency was set at 1 piece every 30 minutes. Later analysis found that process variation in the first 3 months mainly came from the equipment warm-up phase (first 10 pieces after startup)—30-minute sampling cannot capture this variation. If doing it again, 100% measurement would be done for the first 20 pieces after startup, then switch to sampling mode.

**2. Should have tested after-sales response earlier.** 3 months after equipment arrival, a camera trigger anomaly occurred once; supplier remote resolution took ~4 hours. If a "fault simulation test" could have been done before purchase (asking the supplier to on-site demonstrate fault diagnosis and recovery process), expectations of after-sales response capability would have been more accurate.

**3. Tube type database should have been established earlier.** The optical measurement system accumulated standard YBC parameter databases for 60 tube types. It was later discovered that this database is very valuable for new product development—new tube types can use historical data from similar tube types as process references. If the tube type database could have been systematically established in Month 1 of implementation, support for new product development would have been demonstrated earlier.

### Three Recommendations for Peers

**Recommendation 1:** Do not wait until "the gauge system has problems" to consider optical measurement. The starting point of the factory above was "the gauge system is comprehensive, quality is not a problem"—what truly drove the change were two problems that gauges cannot solve: "process capability cannot be proven" and "assembly interference cannot be detected before shipment." If your customers begin requesting CPK evidence, or if you experience returns where "gauge passed 
**Recommendation 2:** The value of optical measurement equipment is not "a more precise gauge"—it is "making setup and process control truly closed-loop." If used only as a gauge replacement, only 30% of the value is realized. The truly high-value uses are: real-time setup feedback + high-frequency SPC + automatic bender parameter correction—none of these three things can be done by gauges.

**Recommendation 3:** The key person for successful implementation is not the quality director—it is the front-line setup worker. Equipment purchase decisions are made by the quality director, 
</details>

---

*Last updated: 2026-05-29 | Author: XTOP3D Tube Qualify Technical Team | Based on a composite case study of multiple tube bending factory digital transformation projects*