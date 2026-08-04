# TGF-β 超家族配体研究报告：GDF8、GDF11、BMP9、BMP10

> **项目背景**：设计一种类似 bimagrumab（Bima）的抗体，但减少心脏副作用。
> **报告日期**：2026-08-04
> **模板**：每份报告包含 (1) 生理功能，(2) 阻断后的作用与影响，(3) 动物模型与给药方案，(4) 针对该通路的药物及临床结果。

---

## 目录

- [一、GDF8（Myostatin / 生长分化因子 8）](#一gdf8myostatin--生长分化因子-8)
- [二、GDF11（生长分化因子 11）](#二gdf11生长分化因子-11)
- [三、BMP9（GDF2 / 骨形态发生蛋白 9）](#三bmp9gdf2--骨形态发生蛋白-9)
- [四、BMP10（骨形态发生蛋白 10）](#四bmp10骨形态发生蛋白-10)
- [五、综合对比与对 Bimagrumab 改良项目的启示](#五综合对比与对-bimagrumab-改良项目的启示)

---

# 一、GDF8（Myostatin / 生长分化因子 8）

## 1. 生理功能

GDF8（又称肌肉抑制素，Myostatin）是 TGF-β 超家族成员，主要由骨骼肌分泌，是骨骼肌质量的**核心负调控因子**。其成熟结构域与 GDF11 有约 90% 的序列同源性，但生理功能截然不同。

| 系统/组织 | 生理功能 |
|---|---|
| **骨骼肌** | 持续抑制肌细胞增殖与分化，负调控肌肉质量。GDF8 基因突变（如比利时蓝牛、皮尔曼牛）导致"双肌"表型，肌肉量增加 20-40% |
| **脂肪代谢** | 调节脂肪蓄积——GDF8 缺失动物脂肪量显著减少，提示其参与能量代谢平衡 |
| **骨代谢** | 通过 ActRIIB 信号抑制骨形成；GDF8 阻断可增加骨密度和骨皮质强度 |
| **心脏** | 在心肌中低表达，对心脏发育非必需；但病理性心肌重构中可能参与 ActRII 介导的信号 |
| **生殖/内分泌** | 表达水平较低，非主要生殖调控因子（与 Activin A/B 不同） |
| **血清浓度** | 人类血清 GDF8 约 5-10 ng/mL，比小鼠（>100 ng/mL）低约 20 倍——这是临床转化失败的关键原因之一 |

**信号通路**：GDF8 → ActRIIA/ActRIIB → ALK4/ALK5 → Smad2/3 → 肌肉萎缩基因转录（MuRF1、Atrogin-1）。GDF8 以前体形式（pro-myostatin）分泌，经蛋白酶切割后释放成熟形式，但成熟 GDF8 与前肽（propeptide）结合形成潜伏复合体，在生理条件下大多无活性。

## 2. 阻断后的作用与影响

### 正面效应

| 效应 | 说明 |
|---|---|
| 骨骼肌显著增生 | 肌纤维横截面积增大、肌细胞数量增加，肌肉量提升 20-40% |
| 改善肌少症 | 老年小鼠肌肉质量与握力恢复 |
| 改善 DMD 模型 | mdx 小鼠肌纤维增大、纤维化减轻、握力改善 |
| 减少脂肪蓄积 | GDF8 缺失动物体脂率下降，代谢改善 |
| 增加骨密度 | 皮质骨厚度与骨强度增加 |
| 改善胰岛素敏感性 | 肌肉量增加伴随代谢改善 |
| 化疗/癌症恶病质保护 | 减少肌肉丢失，延长生存 |

### 负面效应与风险

| 风险 | 说明 |
|---|---|
| **心脏安全性** | GDF8 与 GDF11 高度同源，抗 GDF8 抗体可能交叉阻断 GDF11，而 GDF11 具有逆转年龄性心肌肥大的潜在保护作用 |
| 肌腱/韧带脆弱 | GDF8 缺失动物肌腱胶原减少、力学强度下降 |
| 人类血清浓度低 | 人类 GDF8 仅为小鼠的 1/20，且 DMD 患者已降低约 65%，治疗窗口窄 |
| 功能改善有限 | 单纯增加肌肉体积未必转化为肌力/运动功能改善，需神经输入配合 |
| 再生干扰争议 | GDF11（与 GDF8 高度同源）在高浓度下抑制肌肉卫星细胞再生 |

## 3. 动物模型与给药方案

| 模型 | 物种/品系 | 给药方案 | 主要结果 |
|---|---|---|---|
| **mdx 小鼠**（DMD 模型） | C57BL/10ScSn-Dmdmdx | 抗 GDF8 抗体 10 mg/kg IP，每周 2 次 × 4-12 周 | 肌纤维增大、纤维化减轻、握力改善 |
| **C26 结肠癌恶病质** | BALB/c 小鼠 | sActRIIB-Fc 10 mg/kg IP q3d | 肌肉丢失减少 50%+，生存延长 |
| **年龄性肌少症** | C57BL/6 老年鼠（24 月龄） | 抗 GDF8 抗体 5-10 mg/kg | 肌肉质量恢复，握力改善 |
| **高脂饮食肥胖** | C57BL/6 DIO 小鼠 | 抗 GDF8 抗体 / ActRIIB-Fc | 脂肪量减少，胰岛素敏感性改善 |
| **食蟹猴**（毒理/药效） | Macaca fascicularis | Bimagrumab 10-30 mg/kg IV | 股四头肌横截面积增加，安全窗评估 |
| **卵巢切除骨丢失** | C57BL/6 OVX 小鼠 | ActRIIB-Fc 10 mg/kg | 骨密度增加，皮质骨强度改善 |
| **GLP-1 诱导肌丢失** | DIO 小鼠 + 司美格鲁肽 | 抗 GDF8/Activin A 双重阻断 | 肌肉保留 + 脂肪减少协同 |

## 4. 针对该通路的药物及临床结果

| 药物 | 公司 | 机制 | 适应症 | 给药方案 | 临床结果 | 状态 |
|---|---|---|---|---|---|---|
| **MYO-029**（Stamulumab） | Wyeth/Pfizer | 抗成熟 GDF8 抗体 | 肌少症/DMD/LGMD | 1-10 mg/kg IV q2w × 6 月 | **失败**：肌肉体积/力量无改善 | 终止 |
| **Landogrozumab**（LY-2495655） | Eli Lilly | 抗 GDF8 抗体 | 肌少症/髋关节置换/胰腺癌恶病质 | 315 mg IV × 5 剂 / 20 周 | 肌少症：+0.44 kg 四肢瘦体重，爬楼梯改善；髋置换与胰腺癌：**失败** | 终止 |
| **Domagrozumab**（PF-06252616） | Pfizer | 抗 GDF8/GDF11 抗体 | DMD / LGMD | 3-30 mg/kg IV q2w | **失败**：无功能改善 | 2018 终止 |
| **Bimagrumab**（BYM338） | Novartis/Lilly | 抗 ActRIIA/ActRIIB 双受体阻断 | sIBM / 肌少症 / 肥胖+T2D | 30 mg/kg IV q4w | sIBM：**失败**（6MWD 无改善）；肌少症：大腿肌体积 +6.5%，仅慢步速者功能改善；肥胖+T2D：脂肪 -20%，肌肉 +4%，HbA1c -0.8% | 肥胖适应症推进中 |
| **Apitegromab**（SRK-015） | Scholar Rock | 抗**潜伏型** GDF8 抗体 | SMA / 肥胖（联合替尔泊肽） | 5-15 mg/kg IV q4w | SMA：运动功能改善；肥胖+替尔泊肽：瘦体重保留 1.9 kg（相对保留 54.9%） | Phase 3 进行中 |
| **GYM329** | Roche | 抗潜伏型 GDF8 抗体 | FSHD | 临床剂量待定 | 临床前优于 landogrozumab/domagrozumab/bimagrumab | Phase 2 进行中 |
| **Trevogrumab**（REGN-1033） | Regeneron | 抗成熟/潜伏/pro-GDF8，**不交叉 GDF11** | 肌少症 / IBM | SC 给药 | 临床前肌肉增加，无 GDF11 交叉反应 | Phase 2 进行中 |
| **Ramatercept**（ACE-031/RAP-031） | Acceleron | ActRIIB-Fc 配体陷阱 | DMD | 3-10 mg/kg SC q2w | 肌肉增加但**因鼻衄、牙龈出血、毛细血管扩张终止**（BMP9/BMP10 交叉抑制） | 终止 |
| **KER-065** | Keros | 改良 ActRIIA/IIB 陷阱（降低 BMP 结合） | DMD / 肌少症 | 1.25-2 mg/kg SC q28d | Phase 1 耐受良好，骨密度改善；Phase 2 DMD 计划 2026 Q1 | Phase 2 准备中 |

**关键教训**：第一代抗 GDF8 药物几乎全部失败，核心原因包括：(1) 与 GDF11 交叉反应导致心脏风险；(2) 人类血清 GDF8 浓度远低于小鼠，治疗窗口窄；(3) 靶向成熟 GDF8 而非潜伏形式，生物利用度低；(4) 单纯增肌不等于功能改善。新一代策略（apitegromab、GYM329、trevogrumab）靶向潜伏型 GDF8 并避免 GDF11 交叉反应，展现出更好的前景。

---

# 二、GDF11（生长分化因子 11）

## 1. 生理功能

GDF11（又称 BMP-11）是 TGF-β 超家族成员，成熟结构域与 GDF8 有约 90% 序列同源性，但表达模式与生物学功能显著不同。GDF11 是近年来衰老研究中最具争议的分子之一。

| 系统/组织 | 生理功能 |
|---|---|
| **胚胎发育** | 中轴骨骼后部模式形成所必需；GDF11 敲除小鼠出现颈椎/胸椎/肋骨异常及腭裂，围产期致死 |
| **心脏** | **争议核心**：Loffredo 2013 报告 GDF11 随年龄下降，外源补充可逆转年龄性心肌肥大；但 Egerman 2015 报告 GDF11 随年龄**上升**；后续研究显示 GDF11 在心肌中磷酸化 Smad2 的能力比 GDF8 更强 |
| **骨骼肌** | Sinha 2014 报告 GDF11 恢复老年小鼠肌肉卫星细胞功能与握力；但 Egerman 2015 报告 GDF11 **抑制**肌肉再生，与 GDF8 功能相似 |
| **骨代谢** | GDF11 通过刺激破骨细胞生成、抑制成骨细胞分化而**减少骨量** |
| **血管** | 促血管生成，改善年龄性内皮功能障碍 |
| **肝脏** | 抗纤维化——GDF11 通过抑制 NLRP3 炎症小体保护肝细胞 |
| **炎症** | 拮抗 TNF-α 诱导的炎症反应 |
| **血清浓度** | 随年龄变化趋势**高度争议**：部分研究显示下降，部分显示上升，可能与检测方法（抗体特异性、与 GDF8 交叉反应）有关 |

**信号通路**：GDF11 → ActRIIA/ActRIIB → ALK4/ALK5 → Smad2/3（与 GDF8 共享通路）；但在心肌中，GDF11 激活 Smad2 的效力显著强于 GDF8。

## 2. 阻断后的作用与影响

### 正面效应

| 效应 | 说明 |
|---|---|
| 肌肉增加 | 阻断 GDF11（与 GDF8 共享 ActRII 通路）可增加肌肉质量 |
| 改善 β-地中海贫血？ | 理论上阻断 GDF11 可促进红细胞生成——但**单独抗 GDF11 在 β-地中海贫血小鼠中未改善红细胞生成** |
| 骨量增加 | GDF11 促进破骨细胞生成，阻断后理论上可增加骨量 |

### 负面效应与风险

| 风险 | 说明 |
|---|---|
| **消除心脏保护** | GDF11 可能逆转年龄性心肌肥大——阻断后可能**消除这一保护效应**，增加心脏风险 |
| **严重恶病质** | GDF11 在高剂量下导致严重恶病质和死亡——Harper 2018 报告 GDF11 减轻压力超负荷心肌肥大但引起致命性恶病质 |
| **抑制肌肉再生** | GDF11 可能抑制（而非促进）肌肉卫星细胞再生——阻断理论上有利于肌肉，但与心脏保护矛盾 |
| **抗炎作用丧失** | GDF11 拮抗 TNF-α 炎症——阻断后可能加重炎症 |
| **抗纤维化作用丧失** | GDF11 保护肝脏免受纤维化——阻断后可能加重肝纤维化 |
| **检测困难** | GDF11 与 GDF8 高度同源，难以区分——药物交叉反应风险高 |

## 3. 动物模型与给药方案

| 模型 | 物种/品系 | 给药方案 | 主要结果 |
|---|---|---|---|
| **异种共生**（parabiosis） | C57BL/6 老年鼠 ↔ 年轻鼠 | 血液共享（天然 GDF11 交换） | 老年鼠心肌肥大逆转、肌肉卫星细胞恢复 |
| **压力超负荷心肌肥大**（TAC） | C57BL/6 小鼠 | GDF11 重组蛋白 0.1 mg/kg IP qd | 心肌肥大减轻，但高剂量致恶病质与死亡 |
| **年龄性肌肉退化** | C57BL/6 老年鼠 | GDF11 重组蛋白 1 μg/kg/d × 4 周 | 肌肉卫星细胞功能恢复、握力改善（Sinha 报告） |
| **肌肉损伤修复** | 老年大鼠 | GDF11 重组蛋白 | **延迟**肌肉功能恢复（Egerman 报告，与 Sinha 矛盾） |
| **卵巢切除骨丢失** | C57BL/6 OVX 小鼠 | GDF11 propeptide-Fc | 骨量减少——GDF11 促进破骨细胞生成 |
| **β-地中海贫血** | Hbbth3/+ 小鼠 | 抗 GDF11 抗体 | **未改善**红细胞生成（需同时阻断 GDF8） |
| **炎症性肠病** | DSS 结肠炎小鼠 | GDF11 重组蛋白 | 炎症减轻，结肠保护 |
| **肝纤维化** | CCl4 小鼠 | GDF11 重组蛋白 | 肝纤维化减轻，NLRP3 抑制 |

## 4. 针对该通路的药物及临床结果

| 药物 | 公司 | 机制 | 对 GDF11 的作用 | 临床状态 |
|---|---|---|---|---|
| **Bimagrumab** | Novartis/Lilly | 抗 ActRIIA/ActRIIB | **共阻断** GDF11（与 GDF8、Activin A/B 共享 ActRII） | 肥胖适应症推进中 |
| **Sotatercept**（Winrevair） | Merck/Acceleron | ActRIIA-Fc | **共捕获** GDF11（高亲和力） | FDA 批准 PAH |
| **Luspatercept**（Reblozol） | BMS/Acceleron | 改良 ActRIIB-Fc | **共捕获** GDF11（高亲和力，与 GDF8 共享） | FDA 批准 β-地中海贫血/MDS |
| **Domagrozumab** | Pfizer | 抗 GDF8/**GDF11** | 直接靶向 GDF11（交叉反应） | **已终止**（DMD 失败） |
| **GDF11 propeptide-Fc** | 学术 | GDF11 前肽陷阱 | 特异性阻断 GDF11 | 临床前 |
| **抗 GDF11 单抗** | 学术 | 抗 GDF11 抗体 | 特异性阻断 | β-地中海贫血小鼠模型中**单独无效** |

**关键要点**：目前**尚无 GDF11 特异性药物进入临床试验**。GDF11 在临床中被"附带"阻断——bimagrumab、sotatercept、luspatercept 均通过 ActRII 共捕获 GDF11。这带来一个核心矛盾：GDF11 可能具有心脏保护作用（逆转年龄性心肌肥大），而 bimagrumab 阻断 GDF11 可能**消除这一保护**——这正是本项目（减少 bimagrumab 心脏副作用）需要重点考虑的问题。

---

# 三、BMP9（GDF2 / 骨形态发生蛋白 9）

## 1. 生理功能

BMP9（又称 GDF2）是 TGF-β 超家族中**唯一在循环中以较高浓度持续存在的 BMP 家族成员**，主要由肝脏星状细胞分泌，是血管稳态的关键维持因子。

| 系统/组织 | 生理功能 |
|---|---|
| **血管内皮** | 通过 ALK1-Endoglin-BMPRII → Smad1/5/8 通路维持内皮**静息状态**，抑制病理性血管新生 |
| **血管发育** | 与 BMP10 共同维持动静脉分化与血管完整性；BMP9/10 是**仅知的 ALK1 生理配体** |
| **肝脏** | 旁分泌因子，控制肝窦内皮细胞窗孔，维持肝脏稳态，抗纤维化 |
| **肺循环** | 维持肺动脉内皮静息；BMP9 信号缺失导致肺动脉高压（PAH）；但 BMP9 亦通过非经典 ALK1-Smad3 通路驱动血管活性基因表达 |
| **淋巴管** | 调节淋巴管发育与功能 |
| **神经** | 胆碱能神经元分化因子（在非血管组织中通过 ALK1/ALK2 信号） |
| **血清浓度** | 循环浓度约 2-12 ng/mL，是血浆中 BMP 活性的主要贡献者（与 BMP10 形成异源二聚体） |

**信号通路**：BMP9 → ALK1 + Endoglin + BMPRII/ActRII → Smad1/5/8（经典通路）；亦可经 ALK1 → Smad3（非经典通路，驱动血管活性基因）。BMP9 对 ALK1 的亲和力高于 BMP10，但 BMP10 在心脏发育中不可替代。

## 2. 阻断后的作用与影响

### 正面效应

| 效应 | 说明 |
|---|---|
| **部分保护 PAH** | 选择性 BMP9 抑制在野百合碱/苏拉明 PAH 模型中部分改善肺血流动力学 |
| 抗血管新生（肿瘤） | BMP9 维持内皮静息——阻断后可能促进血管新生（对某些肿瘤治疗有利？但证据有限） |
| 再生医学应用 | BMP9 在骨修复与软骨修复中有成骨活性 |

### 负面效应与风险

| 风险 | 说明 |
|---|---|
| **HHT 样表型** | BMP9 阻断导致遗传性出血性毛细血管扩张症（HHT）样表现——动静脉畸形（AVM）、鼻衄、牙龈出血、毛细血管扩张 |
| **出血并发症** | STM 434（Activin A 抑制剂，BMP9 脱靶）临床试验中鼻衄 34%、牙龈出血 22% |
| **Ramatercept 终止** | ActRIIB-Fc 交叉抑制 BMP9/BMP10 → 鼻衄、牙龈出血、毛细血管扩张 → **临床试验终止** |
| **肝纤维化加重** | BMP9 维持肝窦内皮稳态——阻断后可能加重肝纤维化 |
| **血管失稳** | BMP9 缺失导致内皮增殖失控、血管渗漏 |
| **与 BMP10 协同毒性** | BMP9 + BMP10 联合阻断产生**最强 HHT 样表型**——这是 ActRII 陷阱类药物的核心安全风险 |

## 3. 动物模型与给药方案

| 模型 | 物种/品系 | 给药方案 | 主要结果 |
|---|---|---|---|
| **Bmp9 基因敲除** | C57BL/6 Bmp9-/- | 基因缺失 | 出生后存活但出现血管异常、肝窦内皮窗孔改变 |
| **新生鼠视网膜 AVM 模型** | C57BL/6 新生鼠 | 抗 BMP9 抗体 + 抗 BMP10 抗体 IP | 视网膜动静脉畸形——联合阻断最强 |
| **ALK1 条件性敲除** | Acvrl1fl/fl; Cdh5-Cre | 基因缺失 | 内皮 ALK1 丢失 → AVM、血管发育异常 |
| **Endoglin 条件性敲除** | Engfl/fl; Cdh5-Cre | 基因缺失 | HHT 样表型 |
| **CCl4 肝纤维化** | C57BL/6 小鼠 | CCl4 + BMP9 补充/阻断 | BMP9 维持肝窦稳态，阻断加重纤维化 |
| **野百合碱 PAH** | Sprague-Dawley 大鼠 | MCT 诱导 + 抗 BMP9 抗体 | 选择性 BMP9 抑制部分改善 PAH |
| **Su5416/缺氧 PAH** | C57BL/6 大鼠 | Su5416 + 缺氧 + BMP9 调控 | BMP9 信号缺失促进 PAH |
| **经乳汁 BMP9/10 免疫阻断** | C57BL/6 哺乳期 | 母鼠注射抗 BMP9/BMP10 抗体 | 仔鼠出现 HHT 样血管畸形 |

## 4. 针对该通路的药物及临床结果

| 药物 | 公司 | 机制 | 对 BMP9 的作用 | 临床结果 | 状态 |
|---|---|---|---|---|---|
| **Sotatercept**（Winrevair） | Merck/Acceleron | ActRIIA-Fc | **脱靶捕获 BMP9**——新发现：sotatercept 降低循环 BMP9/BMP10 水平，减少 BMP 信号 | PULSAR：PVR -145.8 至 -239.5 dyn·s·cm⁻⁵；STELLAR：6MWD +40.8m；ZENITH：复合终点风险降低 76% | FDA 批准 PAH（2024） |
| **Luspatercept**（Reblozol） | BMS/Acceleron | 改良 ActRIIB-Fc | **低 BMP9 亲和力**（关键差异化设计） | MEDALIST：输血独立率 37.9% vs 13.2%；BELIEVE：输血负担降低 21.4% vs 4.5% | FDA 批准 |
| **Ramatercept**（ACE-031） | Acceleron | ActRIIB-Fc | **高 BMP9/BMP10 亲和力** → 交叉抑制 | 肌肉增加但**因鼻衄、牙龈出血、毛细血管扩张终止** | 终止 |
| **STM 434** | Summit | 抗 Activin A 抗体 | **BMP9 脱靶抑制** | Phase 1：鼻衄 34%、牙龈出血 22% | 终止/暂停 |
| **KER-065** | Keros | 改良 ActRIIA/IIB 陷阱 | **设计降低 BMP9/BMP10 结合** | Phase 1 耐受良好，无出血事件报告 | Phase 2 准备中 |
| **TRC105**（Carotuximab） | TRACON | 抗 Endoglin 抗体 | 间接阻断 BMP9-Endoglin 信号 | 肾癌 Phase Ib：与阿昔替尼联用，出血风险 | 多适应症探索中 |
| **HS135** | 学术 | Activin/GDF 陷阱 | BMP9 亲和力待确认 | 临床前 PAH 模型有效 | 临床前 |

**关键安全教训**：BMP9 阻断是 ActRII 陷阱类药物**出血并发症的主要来源**。Ramatercept 和 STM 434 均因 BMP9 交叉抑制导致的 HHT 样出血而终止。Luspatercept 通过工程化改造**降低 BMP9 亲和力**成功规避了这一风险。Sotatercept 虽然脱靶降低 BMP9/BMP10，但在 PAH 患者中获益大于风险（PAH 本身存在 BMP 信号不足），但最新研究提示这一脱靶效应可能是**减少 BMP 信号而非再平衡**——长期安全性仍需关注。

---

# 四、BMP10（骨形态发生蛋白 10）

## 1. 生理功能

BMP10 是 TGF-β 超家族成员，在**心脏发育**中具有不可替代的作用，出生后转为循环因子，与 BMP9 共同维持血管稳态。

| 系统/组织 | 生理功能 |
|---|---|
| **心脏发育（核心功能）** | BMP10 敲除小鼠**胚胎致死**——心室肌细胞增殖严重减少、心脏发育停滞；BMP9 无法代偿 BMP10 在心脏发育中的功能 |
| **心内膜发育** | BMP10 促进人多能干细胞向心内膜细胞分化 |
| **出生后血管稳态** | 循环 BMP10 通过内皮 ALK1 维持**血流依赖性动脉静息**——与 BMP9 功能重叠但非完全冗余 |
| **血管发育** | 与 BMP9 共同为**仅知的 ALK1 生理配体**；BMP10 介导的 ALK1 信号在血管发育与维持中持续需要 |
| **心脏病理** | 心衰患者中 BMP10/ALK1/Endoglin 表达升高，与不良预后相关（EMPEROR 项目，Packer 2025） |
| **血浆活性** | BMP9/BMP10 异源二聚体提供血浆中**最主要的 BMP 生物活性**（Tillet 2018） |
| **血清浓度** | 循环浓度低于 BMP9，但与 BMP9 协同维持血管完整性 |

**信号通路**：BMP10 → ALK1 + Endoglin + BMPRII → Smad1/5/8（与 BMP9 共享）；在心脏发育中通过 ALK1/ALK3/ALK6 → Smad1/5/8 → 心肌细胞增殖基因。

## 2. 阻断后的作用与影响

### 正面效应

| 效应 | 说明 |
|---|---|
| **PAH 治疗潜力** | BMP10 与 BMP9 共同维持肺血管稳态——在 PAH（BMP 信号不足）中，适度调控可能有益（但 sotatercept 机制更复杂） |
| 肌肉增加（间接） | ActRIIB-Fc 阻断 BMP10 + GDF8 + Activin → 肌肉增加（但出血风险抵消获益） |

### 负面效应与风险

| 风险 | 说明 |
|---|---|
| **胚胎致死** | BMP10 完全缺失 = 胚胎死亡（心脏发育失败）——孕妇用药绝对禁忌 |
| **HHT 样表型** | BMP10 阻断诱导尾部 AVM；BMP9 + BMP10 联合阻断产生**最强 HHT 样表型** |
| **心脏发育毒性** | BMP10 在心脏发育中不可替代——任何影响发育期 BMP10 信号的药物均有致畸风险 |
| **心衰恶化风险** | 心衰患者 BMP10/ALK1 通路升高可能是代偿反应——阻断可能恶化心衰 |
| **Sotatercept 新发现** | Sotatercept **脱靶降低循环 BMP9 和 BMP10**，减少 BMP 信号——这是新发现的安全隐患 |
| **出血并发症** | 与 BMP9 协同——联合阻断导致鼻衄、牙龈出血、毛细血管扩张（Ramatercept 终止原因） |

## 3. 动物模型与给药方案

| 模型 | 物种/品系 | 给药方案 | 主要结果 |
|---|---|---|---|
| **Bmp10 基因敲除** | C57BL/6 Bmp10-/- | 基因缺失 | **胚胎致死**——心室肌细胞增殖严重减少 |
| **Bmp10 条件性敲除（心脏）** | Nkx2.5-Cre; Bmp10fl/fl | 心脏特异性缺失 | 心脏发育停滞，BMP9 无法代偿 |
| **Bmp10 条件性敲除（内皮）** | Cdh5-Cre; Acvrl1fl/fl | 内皮 ALK1 缺失 | 血管发育异常、AVM |
| **新生鼠视网膜 AVM 模型** | C57BL/6 新生鼠 | 抗 BMP9 + 抗 BMP10 抗体 IP | 联合阻断 → 最强 AVM 表型 |
| **经乳汁免疫阻断** | C57BL/6 哺乳期 | 母鼠抗 BMP10 抗体 | 仔鼠血管畸形 |
| **心衰模型** | 小鼠 TAC / 心梗模型 | BMP10 通路检测 | BMP10/ALK1 升高与不良重构相关 |
| **ALK1-Fc 陷阱** | C57BL/6 小鼠 | ALK1-Fc 融合蛋白 | 捕获 BMP9 + BMP10 → HHT 样表型 |

## 4. 针对该通路的药物及临床结果

| 药物 | 公司 | 机制 | 对 BMP10 的作用 | 临床结果 | 状态 |
|---|---|---|---|---|---|
| **Sotatercept**（Winrevair） | Merck/Acceleron | ActRIIA-Fc | **脱靶降低循环 BMP10**——Jones 2026 新发现 | PAH 有效但 BMP10 耗竭是新的安全隐患 | FDA 批准 PAH |
| **Luspatercept**（Reblozol） | BMS/Acceleron | 改良 ActRIIB-Fc | **低 BMP10 亲和力**（工程化改造） | 地中海贫血/MDS 有效，出血风险低 | FDA 批准 |
| **Ramatercept**（ACE-031） | Acceleron | ActRIIB-Fc | **高 BMP10 亲和力** → 交叉抑制 | 肌肉增加但**因 BMP9/BMP10 交叉抑制导致出血终止** | 终止 |
| **ALK1-Fc** | 学术 | ALK1-Fc 融合蛋白 | **特异性捕获 BMP9 + BMP10** | 临床前：最强 HHT 样表型 | 临床前 |
| **KER-065** | Keros | 改良 ActRIIA/IIB 陷阱 | **设计降低 BMP10 结合** | Phase 1 耐受良好 | Phase 2 准备中 |

**关键安全教训**：BMP10 阻断的风险与 BMP9 类似但更严重——BMP10 在心脏发育中不可替代，且与 BMP9 联合阻断产生最强 HHT 样表型。Sotatercept 脱靶降低 BMP10 的新发现提示，即使是"选择性" ActRIIA-Fc 也可能影响 BMP10 水平，这对孕妇和心衰患者构成潜在风险。

---

# 五、综合对比与对 Bimagrumab 改良项目的启示

## 跨配体药物选择性对比表

| 药物 | Activin A | Activin B | GDF8 | GDF11 | BMP9 | BMP10 | 心脏风险来源 | 出血风险来源 |
|---|---|---|---|---|---|---|---|---|
| **Bimagrumab** | 高（受体阻断） | 高 | 高 | **高** | 低 | 低 | 阻断 GDF11 → 消除心肌肥大逆转保护 | 低 |
| **Sotatercept** | 高 | 高 | 高 | 高 | **脱靶高** | **脱靶高** | — | **高**（BMP9/10 耗竭） |
| **Luspatercept** | **低** | 高 | 高 | 高 | **低** | **低** | — | 低 |
| **Ramatercept** | 高 | 高 | 高 | 高 | **高** | **高** | — | **高**（已终止） |
| **KER-065** | 高 | 中 | 高 | 中 | **低** | **低** | — | 低 |
| **STM 434** | 高 | 中 | 中 | 中 | **脱靶高** | 低 | — | **高**（已终止） |
| **Trevogrumab** | 低 | 低 | 高 | **无** | 无 | 无 | 低 | 低 |

## 对 Bima 改良的核心启示

1. **GDF11 是心脏风险的关键**：Bimagrumab 通过 ActRII 阻断 GDF11，可能消除 GDF11 逆转年龄性心肌肥大的保护作用。Trevogrumab 的设计思路——**避免 GDF11 交叉反应**——是减少心脏副作用的最直接策略。

2. **BMP9/BMP10 是出血风险的来源**：Bimagrumab 对 BMP9/BMP10 亲和力低，这是其相对 ramatercept 的优势。改良抗体应**保持或进一步降低** BMP9/BMP10 亲和力，参考 luspatercept/KER-065 的工程化策略。

3. **靶向潜伏型 GDF8 优于成熟 GDF8**：Apitegromab 和 GYM329 靶向潜伏型 GDF8，生物利用度更高且可避免 GDF11 交叉反应——这为 Bima 改良提供了新方向。

4. **Activin A 阻断可能有益于心脏**：ActRII 信号在心衰中是病理性的（降解 SERCA2a），阻断 Activin A 可能具有心脏保护作用。因此，**保留 Activin A 阻断 + 去除 GDF11 阻断**可能是最优策略。

5. **理想改良方向**：设计一种抗体，**保留**对 Activin A/B 和 GDF8 的阻断（肌肉/代谢获益），**去除**对 GDF11 的阻断（心脏保护），**维持低** BMP9/BMP10 亲和力（出血安全）——即向 trevogrumab + KER-065 的混合特征靠拢。

---

## 参考文献（关键来源）

1. Loffredo FS et al. Growth differentiation factor 11 is a circulating factor that reverses age-related cardiac hypertrophy. *Cell*. 2013;153(4):828-839. doi:10.1016/j.cell.2013.04.015
2. Egerman MA et al. GDF11 Increases with Age and Inhibits Skeletal Muscle Regeneration. *Cell Metab*. 2015;22(1):164-174. doi:10.1016/j.cmet.2015.05.010
3. Sinha M et al. Restoring systemic GDF11 levels reverses age-related dysfunction in mouse skeletal muscle. *Science*. 2014;344(6184):649-652. doi:10.1126/science.1251152
4. Harper SC et al. GDF11 Decreases Pressure Overload Induced Hypertrophy, but Can Cause Severe Cachexia and Premature Death. *Circ Res*. 2018;123(1):73-85. doi:10.1161/CIRCRESAHA.118.312955
5. Morvan F et al. Blockade of activin type II receptors with a dual anti-ActRIIA/IIB antibody is critical to promote muscle growth. *PNAS*. 2017;114(47):12633-12638. doi:10.1073/pnas.1707925114
6. Wetzlich BWA et al. Therapeutic applications and challenges in myostatin inhibition for enhanced skeletal muscle. *Mol Cell Biochem*. 2024. doi:10.1007/s11010-024-05120-y
7. Jones E et al. Sotatercept reduces bone morphogenetic protein signaling in patients with pulmonary arterial hypertension. *Sci Transl Med*. 2026. doi:10.1126/scitranslmed.ads5175
8. Desroches-Castan A et al. BMP9 and BMP10: Two close vascular quiescence partners that stand out. *Dev Dyn*. 2021. doi:10.1002/dvdy.395
9. Packer M et al. Coordinated expression of BMP10/ALK1/endoglin—proteins that drive embryonic cardiac and vascular development. *Eur J Heart Fail*. 2025. doi:10.1002/ejhf.3764
10. Chen W et al. BMP10 is essential for maintaining cardiac growth during murine cardiogenesis. *Development*. 2004. doi:10.1242/dev.01094
11. Tu L et al. Selective BMP9 inhibition partially protects against experimental pulmonary arterial hypertension. *Pulm Circ*. 2019.
12. Tillet E et al. Molecular basis of ALK1-mediated signalling by BMP9/BMP10 and their prodomain-bound forms. *Nat Commun*. 2020. doi:10.1038/s41467-020-15425-3
13. David L et al. BMP-9 signals via ALK1 and inhibits bFGF-induced endothelial cell proliferation. *J Cell Sci*. 2007. doi:10.1242/jcs.002949
14. Scharpfenecker M et al. BMP9 regulates endoglin-dependent chemokine responses in endothelial cells. *Blood*. 2012. doi:10.1182/blood-2012-07-440784
15. Packer M et al. Effect of sotatercept on circulating proteomics in pulmonary arterial hypertension. *Eur Respir J*. 2024. doi:10.1183/13993003.01483-2024
16. Ho JD et al. Similar sequences but dissimilar biological functions of GDF11 and myostatin. *Exp Mol Med*. 2020. doi:10.1038/s12276-020-00516-4
17. Walker RG et al. Biochemistry and Biology of GDF11 and Myostatin: similarities, differences and questions for the future. *Circ Res*. 2016. doi:10.1161/CIRCRESAHA.116.308391
18. Loffredo FS et al. Questions and answers about myostatin, GDF11, and the aging heart. *Circ Res*. 2016. doi:10.1161/CIRCRESAHA.115.307861

---

*报告生成日期：2026-08-04 | 项目：Bimagrumab 改良抗体设计*
