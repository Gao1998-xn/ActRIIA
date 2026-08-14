# GLP-1 + Bimagrumab 双抗立项报告
## 配体选择性阻断策略与筛选模型设计

---

**项目名称**：GLP-1R 激动 + ActRII 配体选择性中和双功能分子  
**分子概念**：将 Semaglutide（GLP-1R 激动）与 Bimagrumab（增肌减脂）的功能整合为单一双抗分子，以**配体选择性中和**替代 Bima 的受体全面阻断策略  
**日期**：2026-08-14  

---

## 一、项目概述

### 1.1 背景与问题

Bimagrumab（BYM338）通过直接结合 ActRIIA/IIB 受体实现增肌减脂，在临床试验中已证实可显著减少体脂并增加瘦体重 [65, 67]。然而，受体阻断策略会**无差别拦截所有 ActRII 配体**，包括 GDF11、BMP9、BMP10 等具有重要生理功能的配体，导致骨量减少、血管/出血风险、铁代谢紊乱等脱靶毒性。ACE-031（ActRIIB-Fc 配体陷阱）即因 BMP9/BMP10 被清除后出现出血不良事件而终止开发。

### 1.2 解决方案

将分子设计从"受体阻断"转变为"**配体选择性中和**"：

| 阻断目标 | 不阻断目标 |
|----------|------------|
| Activin A | GDF11 |
| Activin B | BMP9 |
| pro/latent GDF8 | BMP10 |

**核心逻辑**：在保留 Bima 增肌减脂药效的同时，通过配体层面的选择性中和规避 GDF11/BMP9/BMP10 阻断带来的脱靶毒性，并融合 GLP-1R 激动功能实现代谢获益的协同增强。

### 1.3 临床联合用药证据

Nunn 等（2024, Mol Metab）在 DIO 小鼠中证明 bimagrumab + semaglutide 联合用药的协同效应 [35]：

| 治疗组 | 脂肪减少 | 瘦体重变化 |
|--------|----------|------------|
| Bimagrumab 单药 | ~30% | +10% |
| Semaglutide 单药 | ~50% | -10% |
| **联合治疗** | **~70%** | **保留** |

BELIEVE Phase 2 试验（Heymsfield 等, 2026, Nat Med）在 507 例肥胖成人中证实 [67]：

| 治疗组 | 体重变化（48 周） |
|--------|-------------------|
| 安慰剂 | -3.3 kg |
| Bima 30 mg/kg | -9.3 kg |
| Sema 2.4 mg | -14.2 kg |
| **Bima + Sema 联合** | **-17.8 kg** |

均 P<0.001 vs 安慰剂。这些数据为双功能分子设计提供了直接的药效学依据。

---

## 二、分子格式建议

### 2.1 推荐方案：双臂双特异性抗体 + GLP-1 肽段融合（三功能分子）

```
                    ┌── Arm 1: 抗 Activin A/B（中和 inhibin βA/βB 共享表位）
                    │
  Fc ───────────────┤
                    │
                    └── Arm 2: 抗 pro/latent GDF8（结合 GDF8 prodomain 表位）
                    
  Fc C 端 ─── GLP-1 肽段（基于 semaglutide 序列，GLP-1R 激动）
```

| 组分 | 功能 | 靶点 | 筛选策略 |
|------|------|------|----------|
| **Arm 1** | 中和 Activin A/B | inhibin βA/βB 共享表位 | CAGA12-Luc 报告基因筛选 |
| **Arm 2** | 中和 pro/latent GDF8 | GDF8 prodomain 表位 | 结合筛选 + 激活抑制功能筛选 |
| **GLP-1 肽段** | GLP-1R 激动 | GLP-1R | 基于 semaglutide 序列设计，融合至 Fc |

### 2.2 推荐理由

1. **结构可行性**：Activin A（βA 同源二聚体）和 Activin B（βB 同源二聚体）成熟域共享约 50-65% 序列同源性，存在可被单一抗体识别的保守表位。GDF8 prodomain 与 inhibin β 亚基结构完全不同，无法用同一抗体结合，需独立臂。

2. **独立优化**：两臂可分别筛选和亲和力成熟，互不干扰；GLP-1 肽段可独立设计并验证 GLP-1R 激动活性。

3. **肽-Fc 融合格式成熟**：peptibody 格式在药物开发中已有先例（如 romiplostim），semaglutide 肽段序列可经修饰后融合至 Fc C 端或 N 端。

4. **筛选可分阶段进行**：先分别筛选两个抗体臂，再组装为双特异性格式，最后融合 GLP-1 肽段，降低筛选复杂度并允许并行推进。

### 2.3 筛选分两轮

- **Campaign 1**：筛选抗 Activin A/B 抗体（以 Activin A 为抗原正向筛选，以 Activin B 交叉反应为二次筛选）
- **Campaign 2**：筛选抗 pro/latent GDF8 抗体（以 pro/latent GDF8 为抗原结合筛选 + 功能筛选）
- **两轮均包含反向筛选**：确保不结合/不阻断 GDF11、BMP9、BMP10

### 2.4 CMC 注意事项

双臂双特异性 + 肽段融合的三功能分子在 CMC 层面具有挑战性（正确组装率、肽段融合稳定性、异质性）。建议采用成熟的双特异性平台（如 Knob-in-Hole、CrossMab、COMMON light chain 等）。

---

## 三、配体选择性阻断理由（按生物学系统分类）

### 3.1 增肌（骨骼肌质量与功能）

#### 应阻断：Activin A

- **Activin A 是比 GDF8 更重要的肌肉负调节因子（在灵长类中）**：Latres 等（2017, Nat Commun）证明在灵长类中 Activin A 对肌肉质量的负向调节作用比 GDF8 更显著；同时抑制 Activin A 和 GDF8 产生的肌肉肥大和力量增强显著优于单独抑制任一配体 [64]。
- **Activin A 通过 p38β MAPK 诱导肌肉分解**：Ding 等（2016, J Cachexia Sarcopenia Muscle）证明 Activin A 通过 p38β MAPK 激活肌肉蛋白水解，阻断 p38β MAPK 可防止 ActRIIB 介导的分解代谢 [41]。
- **联合阻断 Activin A + GDF8 可增加肌肉量高达 150%**：Chen 等（2017, PNAS）证明联合抑制 activins 和 myostatin 可使肌肉量增加约 150%，在肌营养不良和癌症恶病质模型中具有治疗潜力 [29]。
- **受体层面的双重重要性**：Morvan 等（2017, PNAS）证明同时阻断 ActRIIA 和 ActRIIB（bimagrumab）才能完全中和 myostatin/activin A 的 Smad2/3 信号，单独阻断任一受体仅减少 30-50% 信号 [32]。配体层面同理——需同时中和 Activin A 和 GDF8。

#### 应阻断：Activin B

- **Activin B 通过 ActRII → Smad2/3 信号诱导肌肉萎缩**：与 Activin A 共享下游信号通路，在肌肉中具有冗余的负调节功能 [39, 41]。
- **Activin B 促进肝纤维化**：Wang 等（2022, Hepatol Commun）证明 Activin B 水平与肝损伤程度相关，中和 Activin B 在 CCl4 诱导的纤维化模型中可显著预防和改善纤维化，通过抑制 JNK/iNOS/PARP1 信号和减少肝星状细胞活化 [63]。

#### 应阻断：pro/latent GDF8

- **GDF8 是骨骼肌量的首要负调节因子**：GDF8 KO 小鼠肌肉量翻倍；GDF8 抑制在多种疾病模型中增加肌肉量 [37, 42]。
- **pro/latent 靶向实现 GDF11 选择性**：GDF8 与 GDF11 成熟域 90% 同源，但 prodomain 仅 52% 相似——靶向 prodomain 可避免 GDF11 交叉反应。
- **Apitegromab（SRK-015）验证了 pro/latent 靶向的可行性**：结合 pro/latent myostatin 的 prodomain"臂"区域，稳定潜伏构象并限制蛋白酶切割，不结合成熟 myostatin 或任何形式的 GDF11 [120, 125]。

#### 不应阻断：GDF11

- **GDF11 KO 致死**：围产期致死，伴轴向骨骼同源转化、腭裂、肾脏发育不全。
- **人类 GDF11 LOF 致多系统疾病**：颅面、脊椎、神经系统、心脏、视觉、听觉异常。
- **GDF11 对肌肉力量有益**：GYM329 研究中，抗 GDF11 抗体联合给药显著抑制了 GYM329 诱导的肌肉力量增强；rGDF11 逆转了肌肉力量下降。
- **肌肉特异性 GDF11 KO 对肌肉量无影响**：GDF11 在出生后不调节肌肉量，阻断它不会带来肌肉增益。
- **GDF11 促进成骨**（与 GDF8 抑制成骨相反）：阻断 GDF11 导致骨量减少。

#### 不应阻断：BMP9/BMP10

- **BMP9 是循环血管静息因子**：David 等（2008, Circ Res）证明 BMP9 在循环中以 2-12 ng/mL 浓度存在，通过 ALK1 信号维持内皮静息，抑制内皮细胞迁移和增殖 [130]。
- **BMP9/10 双重阻断导致 HHT 样表型**：通过 ActRIIB-Fc 或 ALK1-Fc 联合阻断 BMP9/BMP10 在易感小鼠中强烈模拟遗传性出血性毛细血管扩张症（HHT）表型，包括动静脉畸形。
- **ACE-031（ActRIIB-Fc）因出血终止**：ActRIIB-Fc 作为配体陷阱同时清除 BMP9/BMP10，导致出血不良事件而终止开发。
- **BMP10 敲除胚胎致死**：BMP10 对心脏发育至关重要，KO 小鼠在妊娠中期死亡。

---

### 3.2 减脂（脂肪组织质量与功能）

#### 应阻断：Activin A + GDF8

- **Bima 临床试验证明 ActRII 阻断显著减脂**：Heymsfield 等（2021, JAMA Netw Open）在 T2D+肥胖患者中，bimagrumab 48 周治疗使体脂减少 21%（vs 安慰剂 0.5%），同时瘦体重增加 3.6% [65, 70]。
- **GDF8 抑制改善脂肪组织和胰岛素敏感性**：Dong 等（2015, Int J Obes）证明抑制小鼠 myostatin 可通过 irisin 介导的肌肉-脂肪串扰改善胰岛素敏感性并促进白色脂肪棕色化 [44]。
- **Myostatin 与肥胖和代谢综合征相关**：Myostatin 水平升高与脂肪量增加、葡萄糖耐量受损和胰岛素抵抗相关；抑制 myostatin 可减少脂肪量并改善胰岛素敏感性 [51, 52, 53, 54]。
- **ActRII 阻断 + GLP-1 联合显著增强减脂**：Nunn 等（2024, Mol Metab）在 DIO 小鼠中证明 bimagrumab 单独使脂肪减少约 30%，semaglutide 单独约 50%，联合治疗达 70% 脂肪减少——优于任一单药 [35]。

#### 不应阻断：GDF11

- **GDF11 抑制脂肪生成并改善脂肪细胞代谢**：Frohlich 等（2022, Cell Prolif）证明 GDF11 通过 WNT/β-catenin 和 ALK5/SMAD2/3 通路抑制脂肪生成并改善成熟脂肪细胞的葡萄糖代谢 [98]。Lin 等（2023, Heliyon）证明 GDF11 通过 ALK5/KLF15/β-catenin/PPARγ 级联抑制人脂肪基质细胞的脂肪分化 [100]。
- **GDF11 基因转移防止高脂饮食诱导的肥胖**：Lu 等（2019, J Transl Med）证明 GDF11 基因转移可防止高脂饮食诱导的肥胖并改善代谢稳态 [96]。
- **外源 GDF11 减少体重并改善葡萄糖稳态**：Walker 等（2020, Sci Rep）证明外源 rGDF11（而非 rGDF8）减少体重并改善葡萄糖耐量 [99]。
- **GDF11 促进脂肪棕色化**：Sagliocchi 等（2026, J Basic Clin Physiol Pharmacol）证明 GDF11 通过 Smad2/3 信号促进冷诱导的脂肪棕色化和代谢激活 [101]。
- **GDF11 刺激脂联素分泌**：Katsimpardi 等（2019, Aging Cell）证明全身性 GDF11 刺激脂联素分泌并在老年小鼠中诱导类似热量限制的表型 [97]。

#### 不应阻断：BMP9/BMP10

- **BMP9 影响脂肪生成和胰岛素信号**：Chen 等（2021, J Diabetes Res）综述指出 BMP9 与胰岛素抵抗、脂肪量和肝脏葡萄糖处理相关 [83]。
- **BMP9/10 协调肝脏细胞间通讯**：Zhao 等（2024, eLife）证明肝星状细胞通过产生 GDF2（BMP9）和 BMP10 维持肝脏健康和器官身份 [79]。

---

### 3.3 糖代谢（葡萄糖稳态与胰岛素敏感性）

#### 应阻断：GDF8

- **GDF8 抑制改善胰岛素敏感性**：Dong 等（2015）证明 myostatin 抑制通过 irisin 介导的肌肉-脂肪串扰改善胰岛素敏感性 [44]。Myostatin 水平与胰岛素抵抗正相关 [52]。
- **Bima 改善 HbA1c**：在 T2D 患者中，bimagrumab 48 周治疗使 HbA1c 额外降低约 0.76 个百分点 [65, 70]。

#### 应阻断：Activin A

- **Activin A 与代谢功能障碍相关**：Activin A 水平在 MASLD 患者中升高并与纤维化程度相关 [92]。
- **联合阻断 Activin A + GDF8 对葡萄糖稳态的改善**：Nunn 等（2024）证明 bimagrumab + semaglutide 联合治疗显著降低血糖和胰岛素水平，增加脂联素，降低瘦素 [35]。

#### 应阻断：Activin B（含重要注意事项）

- **理由**：Activin B 通过 ActRII → Smad2/3 信号在肌肉中与 Activin A 冗余；Activin B 促进肝纤维化 [63]。
- **重要注意事项**：Kobayashi 等（2025, Nat Commun）发现 Activin B 在葡萄糖代谢中具有**有益作用**——通过诱导 FGF21 改善胰岛素敏感性，通过上调 PDE4B 抑制肝脏胰高血糖素作用（肝脏胰高血糖素抵抗），并通过高胰高血糖素血症增强葡萄糖刺激的胰岛素分泌（GSIS）[60]。
- **GLP-1 组分的补偿作用**：双抗中的 GLP-1R 激动组分可补偿 Activin B 阻断后丧失的降糖效应——GLP-1 本身即改善胰岛素敏感性、抑制肝糖输出、增强 GSIS。此外，肥胖状态下 FSTL3（Activin B 内源性抑制剂）在脂肪组织中已升高 [60]，Activin B 的有益代谢效应在肥胖中本已被部分抑制。
- **需监测的指标**：FGF21 水平、胰高血糖素水平、GSIS 反应。

#### 不应阻断：GDF11

- **GDF11 改善葡萄糖稳态**：外源 rGDF11 改善葡萄糖耐量 [99]；GDF11 基因转移改善代谢稳态 [96]；GDF11 改善脂肪细胞葡萄糖摄取和胰岛素信号 [98]。
- **GDF11 刺激脂联素分泌**：脂联素是改善胰岛素敏感性的关键脂肪因子 [97]。

#### 不应阻断：BMP9/BMP10

- **BMP9 调节铁调素和铁代谢**：BMP9 是肝脏铁调素表达的关键调节因子，阻断 BMP9 可导致铁过载 [85, 82]。铁过载与糖尿病发病机制相关。
- **BMP9 影响葡萄糖代谢**：BMP9 与胰岛素抵抗和葡萄糖处理相关 [83]。

---

### 3.4 肝脏功能

#### 应阻断：Activin A

- **Activin A 促进肝纤维化**：Hamang 等（2023, Biochem Pharmacol）综述指出 Activin A 信号与肝纤维化和肝细胞损伤相关，促进细胞外基质产生和肝细胞凋亡；抑制 activins 在小鼠模型中可减轻肝纤维化并支持再生 [93]。
- **Activin A 拮抗剂减轻肝纤维化**：Mekala 等（2024, Cells）证明 Activin A 拮抗剂 NUCC-555 可抑制 Activin A 诱导的基因表达和肝星状细胞活化标志物 [94]。
- **情境依赖性注意**：Liu 等（2023, Diabetes）报告在 MASLD 模型中过表达 Activin A 反而减轻了肝脏脂肪变性和炎症 [91]，提示 Activin A 在肝脏中的角色可能具有情境依赖性。但该研究使用的是过表达而非中和，且在疾病模型中 Activin A 的净效应可能不同于生理水平。临床数据（Activin A 水平与肝纤维化正相关 [92]）支持阻断策略。

#### 应阻断：Activin B

- **Activin B 促进肝纤维化启动和进展**：Wang 等（2022, Hepatol Commun）证明 Activin B 水平与肝损伤相关，中和 Activin B 在 CCl4 模型中可显著预防和改善纤维化 [63]。
- **Activin B 诱导铁调素**：Canali 等（2016, Endocrinology）证明 Activin B（而非 Activin A）在肝细胞中通过非经典 Smad1/5/8 信号（经 BMP I 型受体 ALK2/ALK3）诱导铁调素表达，参与炎症性贫血 [61]。Kanamori 等（2016, Sci Rep）证实 Activin B 通过 ALK2/ActRIIA 信号和 BR-Smad 激活直接增加铁调素转录 [62]。
- **阻断 Activin B 对铁代谢的影响需评估**：阻断 Activin B 可能降低铁调素水平，理论上可改善炎症性贫血，但也需监测铁稳态。

#### 不应阻断：BMP9/BMP10

- **BMP9 是肝脏铁调素的核心调节因子**：BMP9 信号通过 SMAD 通路调节肝铁调素表达，控制系统铁代谢 [85, 82]。阻断 BMP9 可导致铁过载。
- **BMP9/10 维持肝脏健康**：Zhao 等（2024, eLife）证明肝星状细胞通过产生 GDF2（BMP9）和 BMP10 促进分化和维持器官身份 [79]。Chen 等（2024, Biomolecules）综述了 BMP9 在肝脏疾病中的作用 [85]。
- **Sotatercept 耗竭循环 BMP9/BMP10 的教训**：sotatercept 作为 ActRIIA-Fc 配体陷阱可能通过耗竭循环 BMP9 和 BMP10 导致 BMP 信号减少。

#### 不应阻断：GDF11

- **GDF11 对肝脏具有保护功能**：GDF11 通过抑制 p21 延缓细胞衰老；GDF11 缺陷加速肝脏衰老（通过 mTORC1/TFEB 信号抑制自噬）。
- **GDF11 减少肝脏氧化损伤**：Zhou 等（2019）证明 rGDF11 减少老年小鼠的 AGEs、蛋白质氧化和脂质过氧化。

---

### 3.5 选择性阻断理由汇总表

| 配体 | 增肌 | 减脂 | 糖代谢 | 肝脏 | **决策** |
|------|------|------|--------|------|----------|
| **Activin A** | 灵长类首要负调因子 [64]；联合阻断增肌 150% [29] | ActRII 阻断减脂 21% [65] | 与纤维化正相关 [92] | 促进纤维化 [93, 94] | **阻断** |
| **Activin B** | 与 ActA 冗余 [39, 41] | — | 有益（FGF21/GSIS）[60]；GLP-1 补偿 | 促进纤维化 [63]；诱导铁调素 [61, 62] | **阻断**（监测糖代谢） |
| **pro/latent GDF8** | 首要负调因子 [37, 42]；prodomain 靶向避 GDF11 [120] | 改善胰岛素敏感性 [44, 51] | 改善胰岛素敏感性 [44, 52] | — | **阻断** |
| **GDF11** | 对力量有益；肌肉 KO 无影响 | 抑制脂肪生成 [98, 100]；防肥胖 [96] | 改善葡萄糖稳态 [99] | 抗衰老/抗氧化 | **不阻断** |
| **BMP9** | — | 影响胰岛素信号 [83] | 调节铁调素/铁代谢 [85] | 铁调素核心调节 [85]；维持肝脏健康 [79] | **不阻断** |
| **BMP10** | — | — | — | 心脏发育必需；KO 致死 | **不阻断** |

---

## 四、筛选模型设计

### 4.1 体外筛选模型

#### 4.1.1 正向筛选 1：CAGA12-Luc 报告基因系统（阻断 Activin A/B → Smad2/3 信号）

| 要素 | 详情 | 来源 |
|------|------|------|
| **细胞系** | HEK293T/17（ATCC），稳定转染 (CAGA)12-luciferase 报告基因 | Morvan 等, 2017, PNAS [32] |
| **报告基因构建** | (CAGA)12-luciferase，源自 PAI-1 启动子，克隆至 pGL3 载体（Promega） | Morvan 等, 2017 [32] |
| **检测系统** | Britelite Plus（Perkin-Elmer），Spectramax M5 读数 | Morvan 等, 2017 [32] |
| **刺激配体** | 重组 Activin A（R&D Systems）→ 测量 Smad2/3 信号激活 | Morvan 等, 2017 [32] |
| **筛选流程** | 抗体库 + Activin A → CAGA12-Luc 活性下降 = 阳性命中 | — |
| **二次确认** | 阳性命中再用 Activin B 刺激 → 确认交叉反应性 | — |

**CAGA12 报告基因原理**：(CAGA)12 是 12 个重复的 Smad 结合元件（CAGAC 序列），来自 PAI-1 启动子。当 Activin A/B 或 GDF8/GDF11 结合 ActRII → 磷酸化 Smad2/3 → Smad2/3-Smad4 复合物入核结合 CAGA 元件 → 驱动 luciferase 表达。抗体中和配体后 → Smad2/3 信号降低 → luciferase 信号降低 [25, 26, 32]。

**备选/补充报告系统**：
- **Ad-CAGA12-Luc 腺病毒报告系统**：Chen 等（2018, JoVE）开发的腺病毒载体（Ad-CAGA12-Luc），可在多种靶细胞中实现 >90-100% 感染效率，支持活细胞实时成像和体内 IVIS 成像 [25]。
- **CAGA12-Td-Tomato 荧光报告**：用于活细胞单细胞水平 Smad3 信号动态可视化 [26]。

#### 4.1.2 正向筛选 2：pro/latent GDF8 结合与激活抑制筛选

pro/latent GDF8 不直接信号传导（无活性前体），因此筛选策略不同于 Activin A/B：

**步骤 1：结合筛选**

| 要素 | 详情 | 来源 |
|------|------|------|
| **抗原** | 重组 pro/latent GDF8（含 prodomain + 成熟域，未切割形式） | Scholar Rock 方法学 [120, 121] |
| **筛选方法** | 噬菌体展示/酵母展示库 → 固相 ELISA（pro/latent GDF8 包被）→ 结合阳性克隆 | — |
| **反筛** | 同时用成熟 GDF8、GDF11 pro/latent 形式进行反筛 → 去除交叉反应克隆 | — |

**步骤 2：功能筛选（激活抑制）**

| 要素 | 详情 | 来源 |
|------|------|------|
| **原理** | pro/latent GDF8 经 TLL2（tolloid-like 2）蛋白酶切割释放成熟 GDF8 → 成熟 GDF8 激活 ActRII → Smad2/3 信号 | Dagbay 等, 2020, JBC [120] |
| **检测系统** | CAGA12-Luc HEK293T/17 细胞 + pro/latent GDF8 + TLL2 蛋白酶 → 测量 luciferase 信号。加入候选抗体后信号降低 = 抑制激活 | SRK-015 方法学 [120, 121] |
| **确认** | Western blot 检测 pro/latent GDF8 切割产物（成熟 GDF8 条带减少） | Dagbay 等, 2020 [120] |
| **血清生物标志物** | Cote 等（2019, SLAS Discovery）开发了血清 latent myostatin 定量免疫分析方法，可用于体内靶点结合验证 [121] | — |

**SRK-015 结构参考**：Dagbay 等（2020, JBC）解析了 SRK-015 Fab 与 pro/latent myostatin 的复合物结构（PDB 6UMX, 2.79 A），显示 SRK-015 结合 prodomain 的"臂"区域，稳定潜伏构象并限制 TLL2 切割位点的可及性 [120]。

#### 4.1.3 反向筛选（Counter-screen）：确保不阻断 GDF11、BMP9、BMP10

**Counter-screen 1：GDF11 不阻断验证**

| 要素 | 详情 |
|------|------|
| **检测系统** | CAGA12-Luc HEK293T/17 细胞 + 重组 GDF11 刺激 |
| **预期结果** | 候选抗体不降低 GDF11 诱导的 luciferase 信号 |
| **原理** | GDF11 与 GDF8 共享 ActRII → Smad2/3 通路，若抗体交叉反应则会阻断 GDF11 信号 |

**Counter-screen 2：BMP9/BMP10 不阻断验证**

| 要素 | 详情 | 来源 |
|------|------|------|
| **检测系统** | BRE-Luc 报告基因（BMP 响应元件，检测 Smad1/5/8 信号） | David 等, 2007, Blood [127]；Canali 等, 2016 [61] |
| **细胞系** | Hep3B 细胞（人肝癌细胞系，表达内源性 RGM/HJV，支持 BMP 信号）或人内皮细胞（如 HUVEC/ECFC，表达 ALK1） | Canali 等, 2016 [61]；David 等, 2007 [127] |
| **刺激配体** | 重组 BMP9 + BMP10（R&D Systems） | — |
| **预期结果** | 候选抗体不降低 BMP9/BMP10 诱导的 BRE-Luc 信号 | — |
| **BRE-Luc 原理** | BRE（BMP Responsive Element）含 Smad1/5/8 结合位点，BMP9/BMP10 通过 ALK1/ALK2/ALK3 → Smad1/5/8 → 驱动 luciferase 表达 [127, 132] | — |

**BMP9/10 检测灵敏度参考**：David 等（2007, Blood）报告 BMP9 在 BRE-Luc 系统中 EC50 约 45-27 pg/mL，BMP9 在循环中以 2-12 ng/mL 浓度存在 [127, 130]。Tillet 等（2018, JBC）证明循环中 BMP9-BMP10 异源二聚体是血浆中 BMP 生物活性的主要形式 [132]。

#### 4.1.4 二级功能筛选

| 筛选项目 | 细胞系/模型 | 检测指标 | 来源 |
|----------|------------|----------|------|
| **肌肉萎缩/肥大** | C2C12 小鼠肌母细胞分化为肌管 | 肌管直径、Atrogin-1/MAFbx 表达、MyHC 表达 | 多项肌营养不良研究 |
| **肝脏铁调素** | 原代小鼠肝细胞 / Hep3B | HAMP mRNA（qPCR）、铁调素蛋白（ELISA） | Canali 等, 2016 [61] |
| **肝脏葡萄糖生成** | 原代小鼠肝细胞 | Pck1/G6pc 表达、葡萄糖生成量（加 pyruvate/glucagon 刺激） | Kobayashi 等, 2025 [60] |
| **结合动力学** | SPR（Biacore）或 BLI（Octet） | KD、kon、koff 对各配体 | Morvan 等, 2017 [32] |
| **GLP-1R 激动** | GLP-1R 表达细胞 + cAMP 检测 | cAMP 水平、EC50 | GLP-1R 激动剂标准筛选 |

### 4.2 体内验证模型

#### 4.2.1 主要药效模型：DIO 小鼠（饮食诱导肥胖）

| 要素 | 详情 | 来源 |
|------|------|------|
| **动物** | 雄性 C57BL/6J DIO 小鼠（Jackson #380050），24-25 周龄，高脂饮食（60% kcal fat, Research Diets D12492） | Nunn 等, 2024 [35] |
| **给药方案** | 抗体：20 mg/kg SC 每周；Semaglutide（或融合分子的 GLP-1 部分）：120 ug/kg SC 每日；疗程 14 天（急性）或 4-8 周（慢性） | Nunn 等, 2024 [35] |
| **分组** | (1) 载体对照 (2) 抗体单药 (3) GLP-1 单药 (4) 联合/双抗 (5) Bima 阳性对照 | — |

**主要读出指标**：

| 类别 | 指标 | 方法 | 来源 |
|------|------|------|------|
| **体成分** | 瘦体重、脂肪量 | EchoMRI 体成分分析仪 | Nunn 等, 2024 [35] |
| **肌肉重量** | TA、soleus、EDL、gastrocnemius | 解剖称重 | Morvan 等, 2017 [32]；Nunn 等, 2024 [35] |
| **肌纤维横截面积** | CSA | H&E 染色 + ImageJ 定量 | Nunn 等, 2024 [35] |
| **脂肪组织形态** | 脂肪细胞大小 | eWAT/iWAT H&E + Adiposoft (ImageJ) | Nunn 等, 2024 [35] |
| **血糖** | 非空腹血糖 | 血糖仪 | Nunn 等, 2024 [35] |
| **胰岛素** | 血浆胰岛素 | 超敏小鼠胰岛素 ELISA（Crystal Chem 90080） | Nunn 等, 2024 [35] |
| **葡萄糖耐量** | GTT | 腹腔注射葡萄糖后血糖曲线 | Kobayashi 等, 2025 [60] |
| **胰岛素敏感性** | ITT | 腹腔注射胰岛素后血糖曲线 | Kobayashi 等, 2025 [60] |
| **肝糖生成** | PTT | 腹腔注射丙酮酸钠后血糖曲线 | Kobayashi 等, 2025 [60] |
| **脂联素** | 血浆脂联素 | 夹心 ELISA（EMD Millipore） | Nunn 等, 2024 [35] |
| **瘦素/IL-6/MCP-1** | 血浆细胞因子 | Luminex 多重检测（MAGPIX） | Nunn 等, 2024 [35] |
| **游离脂肪酸/甘油** | 血浆 NEFA、甘油 | Wako HR Series NEFA-HR(2)；Sigma Free Glycerol Reagent | Nunn 等, 2024 [35] |
| **运动耐力** | VO2 max、力竭时间 | treadmill VO2 max 协议 | Nunn 等, 2024 [35] |
| **肌肉力量** | 原位收缩功能 | gastrocnemius 电刺激收缩力测定 | Morvan 等, 2017 [32] |

#### 4.2.2 选择性验证模型（确保不阻断 GDF11/BMP9/BMP10）

| 验证项目 | 模型/方法 | 预期结果 | 来源 |
|----------|----------|----------|------|
| **骨量保护** | uCT 分析股骨骨密度（BMD）/骨小梁微结构 | 双抗不应降低 BMD（vs Bima 可能降低） | GDF11/BMP 促骨生成文献 |
| **血管完整性** | 观察出血事件、视网膜血管造影 | 双抗不应诱发出血或 AVM | ACE-031 教训；BMP9/10 血管文献 |
| **铁代谢** | 血清铁调素（ELISA）、血清铁、TIBC | 双抗不应显著改变铁调素/铁水平 | BMP9 铁代谢文献 [85] |
| **心脏功能** | 超声心动图（LVEF、LV mass） | 双抗不应诱发心脏肥大 | GDF11 心脏保护文献 |
| **循环配体水平** | Activin A ELISA（血清）、latent myostatin 免疫分析 | 验证靶点结合（配体蓄积） | Morvan 等, 2017 [32]；Cote 等, 2019 [121] |

#### 4.2.3 临床转化参考

| 试验 | 设计 | 关键结果 | 来源 |
|------|------|----------|------|
| **BELIEVE（Bima+Sema Phase 2）** | 507 例肥胖成人，9 臂（安慰剂/Bima 10或30 mg/kg/Sema 1.0或2.4 mg/组合），48 周 | Bima 30: -9.3 kg；Sema 2.4: -14.2 kg；组合: -17.8 kg（均 P<0.001 vs 安慰剂 -3.3 kg） | Heymsfield 等, 2026, Nat Med [67] |
| **Bima 单药 Phase 2（T2D+肥胖）** | 75 例 T2D+超重/肥胖，48 周 | 体脂 -21%，瘦体重 +3.6%，HbA1c 额外降 0.76 pp，体重 -6.5% | Heymsfield 等, 2021, JAMA Netw Open [65, 70] |

---

## 五、关键文献索引

### 配体功能文献

| 编号 | 作者（年份） | 期刊 | 核心内容 |
|------|-------------|------|----------|
| [29] | Chen JL et al. (2017) | PNAS | 联合抑制 activins 和 myostatin 增加肌肉量 150% |
| [32] | Morvan F et al. (2017) | PNAS | Bimagrumab 双抗 ActRIIA/IIB 机制及 CAGA12-Luc 筛选系统 |
| [35] | Nunn E et al. (2024) | Mol Metab | ActRII 阻断 + GLP-1 联合用药在 DIO 小鼠中的药效 |
| [41] | Ding H et al. (2016) | J Cachexia Sarcopenia Muscle | Activin A 通过 p38β MAPK 诱导肌肉分解 |
| [44] | Dong J et al. (2015) | Int J Obes | Myostatin 抑制通过 irisin 改善胰岛素敏感性 |
| [51] | Deng B et al. (2017) | Nutr Metab | Myostatin 在脂肪量调节中的功能 |
| [52] | Yang M et al. (2023) | Front Endocrinol | Myostatin 作为代谢综合征治疗靶点 |
| [60] | Kobayashi N et al. (2025) | Nat Commun | Activin B 通过 FGF21 和肝脏胰高血糖素抵抗改善糖代谢 |
| [61] | Canali S et al. (2016) | Endocrinology | Activin B 非经典 Smad1/5/8 信号诱导铁调素 |
| [62] | Kanamori Y et al. (2016) | Sci Rep | 炎症诱导的 Activin B 调节铁调素表达 |
| [63] | Wang Y et al. (2022) | Hepatol Commun | Activin B 促进肝纤维化 |
| [64] | Latres E et al. (2017) | Nat Commun | Activin A 在灵长类中比 GDF8 更重要地调节肌肉量 |
| [65] | Heymsfield SB et al. (2021) | JAMA Netw Open | Bimagrumab 在 T2D+肥胖中的体脂减少 |
| [67] | Heymsfield SB et al. (2026) | Nat Med | Bimagrumab + Semaglutide 联合 Phase 2 试验 |
| [91] | Liu H et al. (2023) | Diabetes | Activin A 在 MASLD 模型中的保护作用 |
| [93] | Hamang M et al. (2023) | Biochem Pharmacol | Activins 在肝脏健康和疾病中的作用 |
| [94] | Mekala S et al. (2024) | Cells | Activin A 拮抗剂作为肝病治疗策略 |
| [96] | Lu B et al. (2019) | J Transl Med | GDF11 基因转移防止高脂饮食诱导肥胖 |
| [97] | Katsimpardi L et al. (2019) | Aging Cell | GDF11 刺激脂联素分泌和热量限制样表型 |
| [98] | Frohlich J et al. (2022) | Cell Prolif | GDF11 抑制脂肪生成并改善脂肪细胞代谢 |
| [99] | Walker R et al. (2020) | Sci Rep | 外源 GDF11 减少体重并改善葡萄糖稳态 |
| [100] | Lin S et al. (2023) | Heliyon | GDF11 通过 ALK5/KLF15/beta-catenin/PPARgamma 抑制脂肪分化 |
| [101] | Sagliocchi S et al. (2026) | J Basic Clin Physiol Pharmacol | GDF11 促进脂肪棕色化 |

### 筛选模型文献

| 编号 | 作者（年份） | 期刊 | 核心内容 |
|------|-------------|------|----------|
| [25] | Chen H et al. (2018) | JoVE | 腺病毒 CAGA12-Luc 报告系统用于 TGF-beta/Smad3 信号活细胞成像 |
| [26] | Marvin DL et al. (2022) | Cancers | CAGA 报告基因用于单细胞 Smad3 信号动态可视化 |
| [32] | Morvan F et al. (2017) | PNAS | HEK293T/17 稳定转染 CAGA12-Luc，Bimagrumab 筛选和功能验证 |
| [61] | Canali S et al. (2016) | Endocrinology | BRE-Luc 和 CAGA-Luc 在 Hep3B 细胞中用于 Activin/BMP 信号区分 |
| [120] | Dagbay K et al. (2020) | JBC | SRK-015 与 pro/latent myostatin 复合物结构及激活抑制机制 |
| [121] | Cote S et al. (2019) | SLAS Discovery | 血清 latent myostatin 定量免疫分析方法 |
| [125] | Welsh BT et al. (2021) | Int J Toxicol | Apitegromab 临床前安全性评估 |
| [127] | David L et al. (2007) | Blood | BMP9/BMP10 作为 ALK1 功能性激活体的鉴定 |
| [130] | David L et al. (2008) | Circ Res | BMP9 作为循环血管静息因子 |
| [132] | Tillet E et al. (2018) | JBC | BMP9-BMP10 异源二聚体是血浆中主要 BMP 活性形式 |

---

## 六、假设与注意事项

1. **Activin B 阻断的代谢权衡**：Activin B 对葡萄糖代谢有益（FGF21 诱导、肝脏胰高血糖素抵抗、增强 GSIS）[60]。GLP-1 组分预期可补偿这些效应，但需在体内模型中监测 FGF21、胰高血糖素、GSIS 等指标。肥胖状态下 FSTL3（Activin B 内源性抑制剂）已升高，Activin B 的有益代谢效应在肥胖中本已被部分抑制。

2. **Activin A 在肝脏中的情境依赖性**：Liu 等（2023）报告在 MASLD 模型中过表达 Activin A 反而减轻了肝脏脂肪变性 [91]，提示 Activin A 在肝脏中的角色可能具有复杂性。但该研究使用过表达而非中和，且疾病模型中的净效应可能不同于生理状态。临床数据（Activin A 水平与肝纤维化正相关 [92]）支持阻断策略。

3. **双特异性格式的 CMC 挑战**：双臂双特异性 + 肽段融合的三功能分子在 CMC 层面具有挑战性（正确组装率、肽段融合稳定性、异质性）。建议采用成熟的双特异性平台（如 Knob-in-Hole、CrossMab、COMMON light chain 等）。

4. **GLP-1 肽段设计**：建议基于 semaglutide 序列进行修饰（如 Aib 修饰、脂肪酸链修饰以延长半衰期），融合至 Fc C 端或通过 linker 连接。需独立筛选 GLP-1R 激动活性（cAMP 检测）。

5. **筛选顺序建议**：先完成两个抗体臂的独立筛选和优化 → 组装为双特异性 → 融合 GLP-1 肽段 → 整体分子功能验证。这降低了筛选复杂度并允许并行推进。

6. **Bima 单药血糖升高的安全性提示**：Nunn 等（2024）报告 bimagrumab 单药在 DIO 小鼠中轻度升高血糖 [35]。双抗中 GLP-1 组分预期可补偿这一效应，但需在体内实验中重点监测血糖动态。

---

## 七、筛选流程总览

```
Campaign 1: 抗 Activin A/B 抗体筛选
│
├── 正向筛选: CAGA12-Luc (HEK293T/17) + Activin A → 信号降低 = 命中
├── 二次确认: Activin B 交叉反应性验证
├── 反向筛选 1: GDF11 不阻断 (CAGA12-Luc + GDF11)
├── 反向筛选 2: BMP9/BMP10 不阻断 (BRE-Luc + BMP9/10)
├── 动力学验证: SPR/BLI (KD, kon, koff)
└── 二级功能: C2C12 肌管萎缩实验

Campaign 2: 抗 pro/latent GDF8 抗体筛选
│
├── 结合筛选: ELISA (pro/latent GDF8 抗原)
├── 反筛: 成熟 GDF8、GDF11 pro/latent 去除交叉反应
├── 功能筛选: CAGA12-Luc + pro/latent GDF8 + TLL2 → 信号降低 = 命中
├── 确认: Western blot (切割产物检测)
├── 反向筛选 1: GDF11 不阻断 (CAGA12-Luc + GDF11)
├── 反向筛选 2: BMP9/BMP10 不阻断 (BRE-Luc + BMP9/10)
└── 动力学验证: SPR/BLI

GLP-1 肽段设计
│
├── 序列设计: 基于 semaglutide，Aib/脂肪酸链修饰
├── 功能验证: GLP-1R 表达细胞 + cAMP 检测 (EC50)
└── 融合验证: Fc 融合后 GLP-1R 激动活性保持

组装与整体验证
│
├── 双特异性组装 (Knob-in-Hole / CrossMab 等)
├── GLP-1 肽段融合
├── 整体功能验证: 三重活性确认
└── 体内验证: DIO 小鼠药效 + 选择性安全性
    ├── 药效: EchoMRI / 肌肉重量 / GTT/ITT/PTT / 代谢标志物
    └── 安全性: uCT 骨密度 / 出血观察 / 铁代谢 / 超声心动图
```

---

*报告生成日期：2026-08-14*  
*基于系统文献检索（LiteratureSearch + WebFetch）整理，所有引用均来自同行评审文献*
