# GLP-1 + Bimagrumab 双抗立项报告
## ActRII 受体选择性阻断策略与筛选模型设计

---

**项目名称**：GLP-1R 激动 + ActRII 受体选择性阻断双功能分子
**分子概念**：将 Semaglutide（GLP-1R 激动）与 Bimagrumab（增肌减脂）的功能整合为单一双抗分子，以**受体选择性阻断**替代 Bima 的受体全面阻断策略——通过靶向 ActRIIA/B 上 Activin A/B 专属接触区域，选择性阻断 Activin A/B 和 pro/latent GDF8 与受体的结合，同时保留 GDF11、BMP9、BMP10 的受体结合能力
**日期**：2026-08-18（修订版）

---

## 一、项目概述

### 1.1 背景与问题

Bimagrumab（BYM338）通过直接结合 ActRIIA/IIB 受体配体结合域（LBD）的凹面实现增肌减脂，在临床试验中已证实可显著减少体脂并增加瘦体重<a href="#ref‑65，67">[65，67]</a>。然而，Bimagrumab 的表位覆盖了所有配体共享的关键残基（Trp78、Phe101、Leu79 等），导致其**无差别拦截所有 ActRII 配体**——包括 GDF11、BMP9、BMP10 等具有重要生理功能的配体，引发骨量减少、血管/出血风险、铁代谢紊乱等脱靶毒性。ACE-031（ActRIIB-Fc 配体陷阱）即因 BMP9/BMP10 被清除后出现出血不良事件而终止开发。

### 1.2 解决方案：受体选择性阻断

将分子设计从"受体全面阻断"（Bima 模式）转变为"**受体选择性阻断**"：

| 阻断目标 | 不阻断目标 |
|----------|------------|
| Activin A | GDF11 |
| Activin B | BMP9 |
| pro/latent GDF8 | BMP10 |

**核心逻辑**：通过 PDB 结构分析识别 ActRIIB 上被 Activin A 接触但不被 GDF11/BMP9 接触的残基区域（Leu38/Glu39/Arg40），设计一种新型受体抗体靶向该区域——在保留 Bima 增肌减脂药效的同时，通过受体层面的选择性阻断规避 GDF11/BMP9/BMP10 阻断带来的脱靶毒性，并融合 GLP-1R 激动功能实现代谢获益的协同增强。

### 1.3 与 Bimagrumab 的关键区别

| 特征 | Bimagrumab | 新受体抗体（本方案） |
|------|-----------|-------------------|
| **靶表位** | Trp78/Phe101/Leu79 核心区域 | Leu38/Glu39/Arg40 区域（Activin A 专属） |
| **阻断范围** | 所有 ActRII 配体（泛阻断） | Activin A/B + pro/latent GDF8（选择性） |
| **GDF11 影响** | 完全阻断 | 保留（不接触 Leu38/Glu39/Arg40） |
| **BMP9/10 影响** | 完全阻断 | 保留（不接触 Leu38/Glu39/Arg40） |
| **作用机制** | 竞争性占据配体结合面 | 选择性遮挡 Activin A 接触面 + prodomain 空间位阻 |

### 1.4 临床联合用药证据

Nunn 等（2024, Mol Metab）在 DIO 小鼠中证明 bimagrumab + semaglutide 联合用药的协同效应<a href="#ref‑35">[35]</a>：

| 治疗组 | 脂肪减少 | 瘦体重变化 |
|--------|----------|------------|
| Bimagrumab 单药 | ~30% | +10% |
| Semaglutide 单药 | ~50% | -10% |
| **联合治疗** | **~70%** | **保留** |

BELIEVE Phase 2 试验（Heymsfield 等, 2026, Nat Med）在 507 例肥胖成人中证实<a href="#ref‑67">[67]</a>：

| 治疗组 | 体重变化（48 周） |
|--------|-------------------|
| 安慰剂 | -3.3 kg |
| Bima 30 mg/kg | -9.3 kg |
| Sema 2.4 mg | -14.2 kg |
| **Bima + Sema 联合** | **-17.8 kg** |

均 P<0.001 vs 安慰剂。这些数据为双功能分子设计提供了直接的药效学依据。

---

## 二、PDB 残基级结构分析

### 2.1 分析的晶体结构

本方案的核心可行性依据来自对以下 PDB 晶体结构的残基级接触面分析：

| PDB ID | 结构 | 分辨率 | 分析内容 |
|--------|------|--------|----------|
| **1NYS** | Activin A / ActRIIB ECD（Thompson 2003） | 3.05 Å | Activin A 受体接触残基 |
| **5NGV** | Bimagrumab Fv / ActRIIB（Morvan 2017） | 2.0 Å | Bima 表位残基 |
| **5NHR** | Bimagrumab Fv / ActRIIB 立方晶型 | — | Bima 表位交叉验证 |
| **6MAC** | GDF11 / ActRIIB / ALK5（Goebel 2019） | 2.3 Å | GDF11 受体接触残基 + 盐桥 |
| **4FAO** | BMP9 / ALK1 / ActRIIB | 2.55 Å | BMP9 受体接触残基 |
| **5NTU** | Pro-GDF8 前体（Cotton 2018） | 2.6 Å | Prodomain 定位与成熟域关系 |
| **6UMX** | Pro-GDF8 / SRK-015 Fab（Dagbay 2020） | 2.79 Å | SRK-015 prodomain 表位分析 |

**分析方法**：使用 BioPython NeighborSearch 计算配体-受体间重原子距离 ≤ 4.5 Å 的接触残基，盐桥检测阈值 4.0 Å。4FAO 的 ActRIIB 残基编号与 6MAC/5NGV 存在 -18 的偏移（通过保守残基 Trp60→Trp78、Phe83→Phe101 对齐验证），已校正。

### 2.2 ActRIIB 接触残基对比

| 配体/抗体 | 接触残基数 | 关键接触残基 |
|-----------|-----------|-------------|
| **Bimagrumab** | 25 | Asn35, Leu38, Glu39, Arg40, Glu52, Gln53, Asp54, Lys55, Arg56, Tyr60, Ser62, Val73, Lys74, Cys77, **Trp78**, **Leu79**, Asp80, Asp81, Phe82, Asn83, Tyr85, Thr93, **Glu94**, Val99, **Phe101** |
| **GDF11** | 16 | Lys55, Tyr60, Ser62, Arg64, Val73, Lys74, Cys77, **Trp78**, **Leu79**, Asp81, Phe82, Asn83, **Glu94**, Gln98, Val99, **Phe101** |
| **BMP9** | 22 | Asn35, Glu39, Cys49, Glu50, Glu52, Lys55, Leu57, Tyr60, Ser62, Arg64, Val73, Lys74, Cys77, **Trp78**, **Leu79**, Asp81, Phe82, Asn83, **Glu94**, Gln98, Val99, **Phe101** |
| **Activin A** | 16 | Glu28, **Leu38**, **Glu39**, **Arg40**, Asn42, Leu46, Arg48, Lys78, Ser79, Cys80, Val82, Leu86, Lys103, Gln106, Asn107, Ser116 |

### 2.3 关键发现

#### 发现 1：Bima-only 残基区域——Activin A 选择性靶点

PDB 分析识别出 **8 个 Bima-only 残基**——被 Bimagrumab 接触但**不被 GDF11 或 BMP9 接触**的 ActRIIB 残基：

| Bima-only 残基 | GDF11 接触 | BMP9 接触 | Activin A 接触 | 选择性意义 |
|----------------|-----------|-----------|---------------|-----------|
| **Leu38** | 否 | 否 | **是** | Activin A 专属接触 |
| **Glu39** | 否 | 是 | **是** | ActA + BMP9 接触 |
| **Arg40** | 否 | 否 | **是** | Activin A 专属接触 |
| Gln53 | 否 | 否 | 否 | Bima 独有 |
| Asp54 | 否 | 否 | 否 | Bima 独有 |
| Arg56 | 否 | 否 | 否 | Bima 独有 |
| Asp80 | 否 | 否 | 否 | Bima 独有 |
| Tyr85 | 否 | 否 | 否 | Bima 独有 |
| Thr93 | 否 | 否 | 否 | Bima 独有 |

**关键结论**：**Leu38 和 Arg40 是 Activin A 接触但 GDF11 和 BMP9 均不接触的残基**。靶向该区域的受体抗体可选择性阻断 Activin A/B，同时保留 GDF11 和 BMP9/10 的受体结合。

#### 发现 2：GDF11 与 BMP9 接触面 100% 重叠

GDF11 的 16 个接触残基**全部**被 BMP9 共享（100% 重叠）。这意味着 GDF11 和 BMP9 结合 ActRIIB 的同一表面，无法通过受体表位选择来区分二者。但 BMP9/10 主要通过 ALK1 信号通路（Smad1/5/8），而 GDF11 通过 ALK4/5 信号通路（Smad2/3），通路层面的差异为选择性提供了补充机制。

#### 发现 3：Leu79 的差异性能量贡献

虽然 Leu79 被 Activin A、GDF11 和 BMP9 共同接触，但 Sako 等（2010, JBC）<a href="#ref‑14">[14]</a> 的突变分析揭示了**差异性能量贡献**：

| 配体 | L79D 突变后 KD 变化 | 能量依赖度 |
|------|-------------------|-----------|
| **Activin A** | **850 倍** | 极高依赖 |
| GDF11 | 3 倍 | 低依赖 |
| GDF8 | ~3 倍 | 低依赖 |
| BMP-2 | 完全消除 | 极高依赖 |
| BMP-7 | 83 倍 | 中等依赖 |

这意味着即使抗体部分遮挡 Leu79，Activin A 的结合将受到严重影响（850 倍），而 GDF11 仅受轻微影响（3 倍）——GDF11 可通过其他接触（如 Glu94 盐桥）补偿。

#### 发现 4：GDF11 特异性盐桥

Goebel 等（2019, PNAS）<a href="#ref‑11">[11]</a> 在 6MAC 结构中确认了 GDF11 与 ActRIIB 之间的特异性盐桥：**Lys36(GDF11) — Glu94(ActRIIB)**，距离 3.65-3.96 Å。该盐桥在 Activin A/ActRIIB 复合物中**不存在**。GDF11 通过此额外接触补偿 Leu79 区域的损失，为其在 Leu79 被部分遮挡时仍能结合受体提供了结构基础。

#### 发现 5：SRK-015 验证 prodomain 选择性靶向

Dagbay 等（2020, JBC）<a href="#ref‑120">[120]</a> 在 6UMX 结构中显示，SRK-015 结合 pro-GDF8 prodomain 的"臂"区域（38 个 prodomain 接触残基），该表位与其他 TGF-β 超家族成员（包括 GDF11）**高度序列差异**。SRK-015 稳定潜伏构象并限制蛋白酶切割位点的可及性，不结合成熟 GDF8 或任何形式的 GDF11。这验证了 pro/latent GDF8 可通过 prodomain 差异实现选择性靶向。

### 2.4 结构分析图表

本报告附以下结构分析图表（保存于 `/mnt/results/`）：

1. **plot_receptor_contact_heatmap.png**：ActRIIB 接触残基热图（各配体 × 残基矩阵）
2. **plot_receptor_venn.png**：Bima/GDF11/BMP9 接触残基 Venn 图
3. **plot_receptor_leu79_differential.png**：Leu79 差异性能量贡献柱状图
4. **plot_receptor_selectivity_strategy.png**：受体抗体选择性策略示意图

---

## 三、受体抗体设计提案

### 3.1 靶表位设计

**核心策略**：设计一种抗 ActRIIA/B 受体抗体，其表位**偏移**于 Bimagrumab——主要覆盖 Leu38/Glu39/Arg40 区域（Activin A 专属接触），同时**避免**完全覆盖 Trp78/Phe101 核心区域（所有配体共享）。

```
                    Bimagrumab 表位范围
  ┌──────────────────────────────────────────────────┐
  │  Asn35  Leu38  Glu39  Arg40  ...  Trp78  Leu79  ...  Phe101  │
  └──────────────────────────────────────────────────┘
                    ↓ 新抗体表位偏移 ↓
  ┌──────────────────────┐
  │  Leu38  Glu39  Arg40  │     + 向 prodomain 方向延伸
  └──────────────────────┘
   ↑ Activin A 专属区域      ↑ 空间位阻 pro/latent GDF8
```

**表位设计要点**：

1. **正选择区域**：Leu38、Glu39、Arg40（Activin A 接触，GDF11/BMP9 不接触）
2. **避免覆盖区域**：Trp78、Phe101（所有配体共享的关键残基，覆盖将导致泛阻断）
3. **部分遮挡允许**：Leu79（Activin A 高度依赖 850 倍，GDF11 低依赖 3 倍——部分遮挡可差异化影响）
4. **延伸方向**：向 prodomain 空间方向延伸，创造与 pro/latent GDF8 prodomain 的空间位阻

### 3.2 分子格式

```
                    ┌── Arm 1: 抗 ActRIIA LBD（选择性表位，Leu38/Glu39/Arg40 区域）
                    │
  Fc ───────────────┤
                    │
                    └── Arm 2: 抗 ActRIIB LBD（选择性表位，Leu38/Glu39/Arg40 区域）

  Fc C 端 ─── GLP-1 肽段（基于 semaglutide 序列，GLP-1R 激动）
```

| 组分 | 功能 | 靶点 | 设计依据 |
|------|------|------|----------|
| **Arm 1** | 阻断 Activin A/B 结合 ActRIIA | ActRIIA LBD Leu38/Glu39/Arg40 区域 | PDB 分析：Activin A 接触该区域，GDF11/BMP9 不接触 |
| **Arm 2** | 阻断 Activin A/B + pro/latent GDF8 结合 ActRIIB | ActRIIB LBD Leu38/Glu39/Arg40 区域 + prodomain 空间延伸 | PDB 分析 + SRK-015 验证 prodomain 选择性 |
| **GLP-1 肽段** | GLP-1R 激动 | GLP-1R | 基于 semaglutide 序列设计，融合至 Fc |

### 3.3 双受体阻断的必要性

Morvan 等（2017, PNAS）<a href="#ref‑32">[32]</a> 证明，单独阻断 ActRIIA 或 ActRIIB 仅减少 30-50% 的 myostatin/activin A 信号，**同时阻断两个受体**才能实现完全中和。因此本方案采用双臂分别靶向 ActRIIA 和 ActRIIB。

### 3.4 pro/latent GDF8 阻断机制

pro/latent GDF8 的选择性阻断通过以下机制实现：

1. **空间位阻**：当 pro/latent GDF8 结合 ActRIIB 时，其 prodomain 从成熟域向外延伸。新抗体向 prodomain 空间方向延伸的结合面将与 prodomain 产生空间冲突，阻止 pro/latent GDF8 的有效受体结合。
2. **激活抑制**：类似 SRK-015 机制 <a href="#ref‑120">[120]</a>，抗体结合可能稳定受体构象，限制 Tolloid 蛋白酶对 pro/latent GDF8 的切割激活。
3. **选择性基础**：GDF8 prodomain 与 GDF11 prodomain 仅 52% 序列相似性（vs 成熟域 90%），prodomain 的结构差异为空间位阻的选择性提供了基础。

### 3.5 与 Bimagrumab 的表位对比

| 表位特征 | Bimagrumab（5NGV/5NHR） | 新受体抗体（设计目标） |
|---------|------------------------|---------------------|
| **核心残基** | Trp78、Phe101、Leu79 | Leu38、Glu39、Arg40 |
| **覆盖范围** | 25 个残基（全面覆盖） | ~10-12 个残基（偏移覆盖） |
| **Trp78 覆盖** | 是 | 否（避免） |
| **Phe101 覆盖** | 是 | 否（避免） |
| **Leu79 覆盖** | 完全覆盖 | 部分遮挡（利用差异性能量贡献） |
| **Glu94 覆盖** | 是 | 否（保留 GDF11 盐桥） |
| **结合角度** | 正面竞争（凹面中心） | 偏移结合（凹面边缘 + prodomain 方向） |

---

## 四、配体选择性阻断理由（按生物学系统分类）

### 4.1 增肌（骨骼肌质量与功能）

#### 应阻断：Activin A

- **Activin A 是比 GDF8 更重要的肌肉负调节因子（在灵长类中）**：Latres 等（2017, Nat Commun）证明在灵长类中 Activin A 对肌肉质量的负向调节作用比 GDF8 更显著；同时抑制 Activin A 和 GDF8 产生的肌肉肥大和力量增强显著优于单独抑制任一配体 <a href="#ref‑64">[64]</a>。
- **Activin A 通过 p38β MAPK 诱导肌肉分解**：Ding 等（2016, J Cachexia Sarcopenia Muscle）证明 Activin A 通过 p38β MAPK 激活肌肉蛋白水解 <a href="#ref‑41">[41]</a>。
- **联合阻断 Activin A + GDF8 可增加肌肉量高达 150%**：Chen 等（2017, PNAS）<a href="#ref‑29">[29]</a>。
- **受体层面的双重重要性**：Morvan 等（2017, PNAS）证明同时阻断 ActRIIA 和 ActRIIB 才能完全中和信号 [32]<a href="#ref‑32">[32]</a>。

#### 应阻断：Activin B

- **Activin B 通过 ActRII → Smad2/3 信号诱导肌肉萎缩**：与 Activin A 共享下游信号通路 <a href="#ref‑39，41">[39，41]</a>。
- **Activin B 促进肝纤维化**：Wang 等（2022, Hepatol Commun）<a href="#ref‑63">[63]</a>。

#### 应阻断：pro/latent GDF8

- **GDF8 是骨骼肌量的首要负调节因子**：GDF8 KO 小鼠肌肉量翻倍<a href="#ref‑37，42">[37, 42]</a>。
- **pro/latent 靶向实现 GDF11 选择性**：GDF8 与 GDF11 成熟域 90% 同源，但 prodomain 仅 52% 相似——受体抗体通过 prodomain 空间位阻避免 GDF11 交叉反应。
- **SRK-015 验证了 pro/latent 靶向的可行性**：结合 prodomain"臂"区域，稳定潜伏构象，不结合成熟 GDF8 或 GDF11 <a href="#ref‑120, 125">[120, 125]</a>。

#### 不应阻断：GDF11

- **GDF11 KO 致死**：围产期致死，伴轴向骨骼同源转化、腭裂、肾脏发育不全。
- **GDF11 对肌肉力量有益**：抗 GDF11 抗体联合给药显著抑制了 GYM329 诱导的肌肉力量增强。
- **肌肉特异性 GDF11 KO 对肌肉量无影响**：GDF11 在出生后不调节肌肉量。
- **GDF11 促进成骨**（与 GDF8 抑制成骨相反）：阻断 GDF11 导致骨量减少。

#### 不应阻断：BMP9/BMP10

- **BMP9 是循环血管静息因子**：David 等（2008, Circ Res）<a href="#ref‑130">[130]</a>。
- **BMP9/10 双重阻断导致 HHT 样表型**：动静脉畸形。
- **ACE-031 因出血终止**：ActRIIB-Fc 同时清除 BMP9/BMP10。
- **BMP10 KO 胚胎致死**：心脏发育至关重要。

---

### 4.2 减脂（脂肪组织质量与功能）

#### 应阻断：Activin A + GDF8

- **Bima 临床试验证明 ActRII 阻断显著减脂**：体脂减少 21%，瘦体重增加 3.6% <a href="#ref‑65，70">[65，70]</a>。
- **GDF8 抑制改善脂肪组织和胰岛素敏感性**：Dong 等（2015）<a href="#ref‑44">[44]</a>。
- **ActRII 阻断 + GLP-1 联合显著增强减脂**：联合治疗达 70% 脂肪减少 <a href="#ref‑35">[35]</a>。

#### 不应阻断：GDF11

- **GDF11 抑制脂肪生成并改善脂肪细胞代谢** <a href="#ref‑98, 100">[98, 100]</a>。
- **GDF11 基因转移防止高脂饮食诱导的肥胖** <a href="#ref‑96">[96]</a>。
- **GDF11 促进脂肪棕色化** <a href="#ref‑101">[101]</a>。
- **GDF11 刺激脂联素分泌** <a href="#ref‑97">[97]</a>。

#### 不应阻断：BMP9/BMP10

- **BMP9 影响脂肪生成和胰岛素信号** <a href="#ref‑83">[83]</a>。
- **BMP9/10 协调肝脏细胞间通讯** <a href="#ref‑79">[79]</a>。

---

### 4.3 糖代谢（葡萄糖稳态与胰岛素敏感性）

#### 应阻断：GDF8 + Activin A

- **GDF8 抑制改善胰岛素敏感性** <a href="#ref‑44，52">[44，52]</a>。
- **Bima 改善 HbA1c**：降低约 0.76 个百分点 <a href="#ref‑65, 70">[65, 70]</a>。
- **联合阻断显著降低血糖和胰岛素水平** <a href="#ref‑35">[35]</a>。

#### 应阻断：Activin B（含重要注意事项）

- **理由**：与 Activin A 冗余；促进肝纤维化 <a href="#ref‑63">[63]</a>。
- **重要注意事项**：Kobayashi 等（2025, Nat Commun）发现 Activin B 通过 FGF21 改善胰岛素敏感性 <a href="#ref‑60">[60]</a>。GLP-1 组分可补偿此效应。
- **需监测**：FGF21、胰高血糖素、GSIS。

#### 不应阻断：GDF11

- **GDF11 改善葡萄糖稳态** <a href="#ref‑99, 96, 98">[99, 96, 98]</a>。
- **GDF11 刺激脂联素分泌** <a href="#ref‑97">[97]</a>。

#### 不应阻断：BMP9/BMP10

- **BMP9 调节铁调素和铁代谢** <a href="#ref‑85, 82">[85, 82]</a>。
- **BMP9 影响葡萄糖代谢** <a href="#ref‑83">[83]</a>。

---

### 4.4 肝脏功能

#### 应阻断：Activin A + Activin B

- **Activin A 促进肝纤维化** <a href="#ref‑93, 94">[93, 94]</a>。
- **Activin B 促进肝纤维化** <a href="#ref‑63">[63]</a>；诱导铁调素 <a href="#ref‑61, 62">[61, 62]</a>。

#### 不应阻断：BMP9/BMP10 + GDF11

- **BMP9 是肝脏铁调素核心调节因子** <a href="#ref‑85, 82">[85, 82]</a>。
- **BMP9/10 维持肝脏健康**  <a href="#ref‑79">[79]</a>。
- **GDF11 抗衰老/抗氧化**。

---

### 4.5 选择性阻断理由汇总表

| 配体 | 增肌 | 减脂 | 糖代谢 | 肝脏 | **决策** | **受体抗体机制** |
|------|------|------|--------|------|----------|-----------------|
| **Activin A** | 灵长类首要负调因子 <a href="#ref‑64">[64]</a> | 减脂 21% <a href="#ref‑65">[65]</a> | 与纤维化正相关 <a href="#ref‑92">[92]</a> | 促进纤维化 <a href="#ref‑93">[93]</a> | **阻断** | 抗体覆盖 Leu38/Arg40（ActA 专属接触） |
| **Activin B** | 与 ActA 冗余<a href="#ref‑39">[39]</a> | — | 有益但 GLP-1 补偿<a href="#ref‑60">[60]</a> | 促进纤维化<a href="#ref‑63">[63]</a> | **阻断** | 同 ActA（共享 ActRII 结合模式） |
| **pro/latent GDF8** | 首要负调因子 <a href="#ref‑37">[37]</a> | 改善胰岛素 <a href="#ref‑44">[44]</a> | 改善胰岛素 <a href="#ref‑52">[52]</a> | — | **阻断** | 抗体延伸 → prodomain 空间位阻 |
| **GDF11** | 对力量有益 | 抑制脂肪生成 <a href="#ref‑98">[98]</a> | 改善葡萄糖 <a href="#ref‑99">[99]</a> | 抗衰老 | **不阻断** | GDF11 不接触 Leu38/Arg40 + Glu94 盐桥补偿 |
| **BMP9** | — | 影响胰岛素 <a href="#ref‑83">[83]</a> | 调节铁调素 <a href="#ref‑85">[85]</a> | 铁调素核心<a href="#ref‑85">[85]</a> | **不阻断** | BMP9 不接触 Leu38/Arg40 |
| **BMP10** | — | — | — | 心脏发育必需 | **不阻断** | 同 BMP9 |

---

## 五、筛选模型设计

### 5.1 抗体发现阶段

#### 5.1.1 噬菌体/酵母展示筛选

| 要素 | 详情 | 设计依据 |
|------|------|----------|
| **抗原** | 重组人 ActRIIB LBD（ECD，残基 25-117）和 ActRIIA LBD | PDB 结构覆盖区域 |
| **文库** | 人类天然 scFv/Fab 噬菌体展示文库或合成文库 | 标准抗体发现 |
| **正选择** | 结合 ActRIIB LBD 和 ActRIIA LBD（双受体交叉反应） | Morvan 2017：需同时阻断两个受体 [32] |
| **负选择 1** | **Bimagrumab 竞争筛选**：先加入过量 Bimagrumab 封锁其表位，再筛选非重叠表位克隆 | 避免获得 Bima 样泛阻断抗体 |
| **负选择 2** | 不结合 GDF11-pre-bound ActRIIB 的克隆（保留 GDF11 结合） | 确保不阻断 GDF11 |
| **负选择 3** | 不结合 BMP9-pre-bound ActRIIB 的克隆（保留 BMP9 结合） | 确保不阻断 BMP9 |

**Bimagrumab 负选择的关键意义**：Bima 覆盖了 ActRIIB 上 25 个残基（包括 Trp78、Phe101 核心区域）。通过先用 Bima 饱和结合 ActRIIB，再从剩余暴露表面筛选新抗体，可强制获得**表位偏移**的克隆——这些克隆的结合位点不与 Bima 重叠，从而避免泛阻断。

#### 5.1.2 表位定位（Epitope Binning）

| 方法 | 目的 |
|------|------|
| **SPR 竞争实验（Biacore）** | 确认新抗体与 Bimagrumab 不竞争（非重叠表位） |
| **HDX-MS（氢氘交换质谱）** | 精确定位新抗体表位，确认覆盖 Leu38/Glu39/Arg40 区域 |
| **丙氨酸扫描突变** | 验证关键表位残基（Leu38A、Arg40A 突变应削弱抗体结合） |

### 5.2 功能筛选

#### 5.2.1 正向筛选 1：CAGA12-Luc 报告基因系统（阻断 Activin A/B → Smad2/3 信号）

| 要素 | 详情 | 来源 |
|------|------|------|
| **细胞系** | HEK293T/17 稳定转染 (CAGA)12-luciferase | Morvan 等, 2017 <a href="#ref‑32">[32]</a>|
| **报告基因** | (CAGA)12-luciferase，源自 PAI-1 启动子 | <a href="#ref‑32">[32]</a> |
| **刺激配体** | 重组 Activin A → 测量 Smad2/3 信号 | <a href="#ref‑32">[32]</a> |
| **筛选流程** | 抗体 + ActRIIB(细胞表面) + Activin A → luciferase 下降 = 命中 | — |
| **二次确认** | Activin B 刺激 → 确认交叉阻断 | — |

**CAGA12 原理**：(CAGA)12 是 12 个重复的 Smad 结合元件。Activin A/B 结合 ActRII → 磷酸化 Smad2/3 → 驱动 luciferase 表达。受体抗体阻断 Activin A/B 结合 → 信号降低<a href="#ref‑25, 26, 32">[25, 26, 32]</a>。

#### 5.2.2 正向筛选 2：pro/latent GDF8 激活抑制筛选

| 要素 | 详情 | 来源 |
|------|------|------|
| **原理** | pro/latent GDF8 经 TLL2 蛋白酶切割释放成熟 GDF8 → 激活 ActRII → Smad2/3 信号 | Dagbay 等, 2020 <a href="#ref‑120">[120]</a>|
| **检测系统** | CAGA12-Luc 细胞 + pro/latent GDF8 + TLL2 → luciferase 信号。加入受体抗体后信号降低 = 抑制激活 |<a href="#ref‑120">[120]</a> |
| **确认** | Western blot 检测切割产物 | [120] |
| **血清生物标志物** | Cote 等（2019）血清 latent myostatin 定量免疫分析 <a href="#ref‑121">[121]</a> | — |

#### 5.2.3 反向筛选 1：GDF11 信号保留验证

| 要素 | 详情 |
|------|------|
| **检测系统** | CAGA12-Luc 细胞 + 重组 GDF11 刺激 |
| **预期结果** | 受体抗体**不降低** GDF11 诱导的 luciferase 信号 |
| **结构基础** | GDF11 不接触 Leu38/Arg40；Glu94 盐桥补偿 Leu79 部分遮挡 |
| **选择性指数** | IC50(Activin A 阻断) / IC50(GDF11 阻断) > 100 倍 |

#### 5.2.4 反向筛选 2：BMP9/BMP10 信号保留验证

| 要素 | 详情 | 来源 |
|------|------|------|
| **检测系统** | BRE-Luc 报告基因（BMP 响应元件，Smad1/5/8 信号） | David 等, 2007 <a href="#ref‑127">[127]</a>；Canali 等, 2016 <a href="#ref‑61">[61]</a> |
| **细胞系** | Hep3B 细胞或人内皮细胞（HUVEC/ECFC，表达 ALK1） |<a href="#ref‑61, 127">[61, 127]</a> |
| **刺激配体** | 重组 BMP9 + BMP10 | — |
| **预期结果** | 受体抗体**不降低** BMP9/BMP10 诱导的 BRE-Luc 信号 | — |
| **选择性指数** | BMP9/BMP10 信号保留率 > 80% | — |

**BRE-Luc 原理**：BRE 含 Smad1/5/8 结合位点，BMP9/BMP10 通过 ALK1 → Smad1/5/8 → 驱动 luciferase<a href="#ref‑127, 132">[127, 132]</a>。

#### 5.2.5 SPR/BLI 竞争结合筛选（关键选择性验证）

| 实验 | 方法 | 预期结果 |
|------|------|----------|
| **抗体 → Activin A 竞争** | SPR：ActRIIB 固定 → 抗体结合 → Activin A 注入 | Activin A 结合被**阻断** |
| **抗体 → GDF11 竞争** | SPR：ActRIIB 固定 → 抗体结合 → GDF11 注入 | GDF11 结合**保留** |
| **抗体 → BMP9 竞争** | SPR：ActRIIB 固定 → 抗体结合 → BMP9 注入 | BMP9 结合**保留** |
| **抗体 → pro/latent GDF8 竞争** | SPR：ActRIIB 固定 → 抗体结合 → pro/latent GDF8 注入 | pro/latent GDF8 结合被**阻断** |
| **抗体 → Bima 竞争** | SPR：ActRIIB 固定 → 抗体结合 → Bima 注入 | **不竞争**（非重叠表位） |

### 5.3 二级功能筛选

| 筛选项目 | 细胞系/模型 | 检测指标 | 来源 |
|----------|------------|----------|------|
| **肌肉萎缩/肥大** | C2C12 肌管 | 肌管直径、Atrogin-1/MAFbx、MyHC | 多项肌营养不良研究 |
| **肝脏铁调素** | 原代小鼠肝细胞 / Hep3B | HAMP mRNA、铁调素蛋白 | Canali 等, 2016 <a href="#ref‑61">[61]</a> |
| **肝脏葡萄糖生成** | 原代小鼠肝细胞 | Pck1/G6pc、葡萄糖生成量 | Kobayashi 等, 2025 <a href="#ref‑60">[60]</a> |
| **结合动力学** | SPR（Biacore）/ BLI（Octet） | KD、kon、koff 对 ActRIIA/B | Morvan 等, 2017 <a href="#ref‑32">[32]</a> |
| **GLP-1R 激动** | GLP-1R 表达细胞 + cAMP 检测 | cAMP 水平、EC50 | GLP-1R 标准筛选 |
| **受体占有率** | FACS（细胞表面 ActRII 结合） | 受体占有率 % | 受体抗体标准检测 |

### 5.4 选择性指数标准

| 指标 | 计算方式 | 合格标准 |
|------|----------|----------|
| **Activin A 选择性** | IC50(ActA 阻断) / IC50(GDF11 阻断) | > 100 倍 |
| **pro/latent GDF8 选择性** | IC50(proGDF8 阻断) / IC50(GDF11 阻断) | > 100 倍 |
| **BMP9 信号保留** | BMP9 信号(抗体+) / BMP9 信号(对照) | > 80% |
| **BMP10 信号保留** | BMP10 信号(抗体+) / BMP10 信号(对照) | > 80% |
| **GDF11 信号保留** | GDF11 信号(抗体+) / GDF11 信号(对照) | > 80% |
| **Bima 非竞争** | SPR 竞争实验 | 不竞争（非重叠表位） |

---

## 六、体内验证模型

### 6.1 主要药效模型：DIO 小鼠

| 要素 | 详情 | 来源 |
|------|------|------|
| **动物** | 雄性 C57BL/6J DIO 小鼠，24-25 周龄，高脂饮食 | Nunn 等, 2024 <a href="#ref‑35">[35]</a> |
| **给药方案** | 抗体：20 mg/kg SC 每周；GLP-1：120 μg/kg SC 每日；14 天或 4-8 周 |<a href="#ref‑35">[35]</a> |
| **分组** | (1) 载体 (2) 抗体单药 (3) GLP-1 单药 (4) 双抗 (5) Bima 阳性对照 | — |

**主要读出指标**：

| 类别 | 指标 | 方法 |
|------|------|------|
| **体成分** | 瘦体重、脂肪量 | EchoMRI |
| **肌肉** | TA/soleus/EDL/gastrocnemius 重量、肌纤维 CSA | 解剖 + H&E |
| **脂肪** | 脂肪细胞大小 | eWAT/iWAT H&E |
| **血糖** | 非空腹血糖、GTT、ITT、PTT | 标准方法 |
| **代谢标志物** | 胰岛素、脂联素、瘦素、IL-6、MCP-1、NEFA | ELISA/Luminex |
| **运动耐力** | VO2 max、力竭时间 | treadmill |

### 6.2 选择性安全性验证（受体抗体特有）

| 验证项目 | 模型/方法 | 预期结果（vs Bima） | 结构基础 |
|----------|----------|-------------------|----------|
| **骨量保护** | μCT 股骨 BMD/骨小梁 | 双抗**不降低** BMD（Bima 可能降低） | GDF11 保留 → 促骨生成 |
| **血管完整性** | 出血事件观察、视网膜血管造影 | 双抗**不诱发出血**/AVM | BMP9/10 保留 |
| **铁代谢** | 血清铁调素、铁、TIBC | 双抗**不改变**铁水平 | BMP9 保留 → 铁调素调节 |
| **心脏功能** | 超声心动图（LVEF、LV mass） | 双抗**不诱发**心脏肥大 | GDF11 保留 |
| **GDF11 信号** | 血清 GDF11 水平、SMAD2/3 磷酸化 | GDF11 信号通路**保留** | Glu94 盐桥补偿 |
| **BMP9/10 信号** | 血清 BMP9/10 水平、SMAD1/5/8 磷酸化 | BMP 信号通路**保留** | BMP9/10 不接触 Leu38/Arg40 |
| **受体占有率** | 肌肉/脂肪/肝脏组织 ActRII 受体占有率 | 部分占有率（选择性结合） | 非全面受体占据 |

### 6.3 临床转化参考

| 试验 | 设计 | 关键结果 | 来源 |
|------|------|----------|------|
| **BELIEVE（Bima+Sema Phase 2）** | 507 例肥胖成人，9 臂，48 周 | 组合: -17.8 kg | Heymsfield 等, 2026 <a href="#ref‑67">[67]</a> |
| **Bima 单药 Phase 2（T2D+肥胖）** | 75 例，48 周 | 体脂 -21%，HbA1c -0.76 pp | Heymsfield 等, 2021 <a href="#ref‑65">[65]</a> |
| **Gonzalez Trotter 等（2025）** | GDF8 + Activin A 双配体抗体 Phase I | 增肌减脂，绝经后女性 |<a href="#ref‑19">[19]</a> |

---

## 七、假设与注意事项

1. **表位偏移的可行性**：本方案的核心假设是存在与 Bimagrumab 表位不重叠但仍能阻断 Activin A/B 结合的 ActRIIB 表位。PDB 分析显示 Leu38/Glu39/Arg40 区域满足此条件（Activin A 接触，GDF11/BMP9 不接触），但实际抗体筛选中是否能获得具有此表位偏移特征的高亲和力克隆需实验验证。Bimagrumab 负选择策略（先用 Bima 饱和 ActRIIB 再筛选）可提高获得偏移表位克隆的概率。

2. **pro/latent GDF8 空间位阻的不确定性**：pro/latent GDF8 结合 ActRIIB 时 prodomain 的精确空间位置尚无复合物结构（仅有 pro-GDF8 单独结构 5NTU 和 pro-GDF8/SRK-015 复合物 6UMX）。抗体向 prodomain 方向的延伸是否能有效产生空间位阻需通过 pro/latent GDF8 + ActRIIB + 抗体的三元结合实验验证。

3. **Leu79 部分遮挡的平衡**：Leu79 被 Activin A（850 倍依赖）和 GDF11（3 倍依赖）共同接触。抗体部分遮挡 Leu79 可差异化影响 Activin A vs GDF11，但遮挡程度需要精确控制——过度遮挡将影响 GDF11，遮挡不足将无法有效阻断 Activin A。SPR 竞争实验可定量评估此平衡。

4. **Activin B 阻断的代谢权衡**：Activin B 对葡萄糖代谢有益（FGF21 诱导）<a href="#ref‑60">[60]</a>。GLP-1 组分预期可补偿。需监测 FGF21、胰高血糖素、GSIS。

5. **双受体亲和力差异**：Bimagrumab 对 ActRIIB（Kd=16 pM）的亲和力比 ActRIIA（Kd=973 pM）高 60 倍 <a href="#ref‑32">[32]</a>。新抗体需优化对两个受体的平衡亲和力，确保双重阻断效果。

6. **受体抗体的组织分布**：受体抗体结合细胞表面 ActRII，其组织分布和受体占有率动力学不同于配体抗体（结合循环配体）。需评估肌肉/脂肪/肝脏等靶组织的受体占有率与药效关系。

7. **潜在的内吞和受体下调**：受体抗体可能诱导 ActRII 内吞和下调，导致长期给药后受体表达降低。需评估重复给药后的受体水平变化。

8. **GLP-1 肽段设计**：基于 semaglutide 序列修饰（Aib 修饰、脂肪酸链），融合至 Fc C 端。需独立筛选 GLP-1R 激动活性。

---

## 八、筛选流程总览

```
Phase 1: 抗体发现 — 受体抗体筛选
│
├── 文库构建: 人类 scFv/Fab 噬菌体展示文库
├── 正选择: 结合 ActRIIB LBD + ActRIIA LBD（双受体交叉反应）
├── 负选择 1: Bimagrumab 竞争筛选（先饱和 Bima → 筛选非重叠表位）
├── 负选择 2: GDF11-pre-bound ActRIIB 不结合（保留 GDF11）
├── 负选择 3: BMP9-pre-bound ActRIIB 不结合（保留 BMP9）
└── 表位定位: SPR 竞争 + HDX-MS + 丙氨酸扫描

Phase 2: 功能筛选 — 选择性验证
│
├── 正向筛选 1: CAGA12-Luc + Activin A → 信号降低 = 命中
├── 正向筛选 2: CAGA12-Luc + pro/latent GDF8 + TLL2 → 信号降低 = 命中
├── 二次确认: Activin B 交叉阻断验证
├── 反向筛选 1: CAGA12-Luc + GDF11 → 信号保留（>80%）
├── 反向筛选 2: BRE-Luc + BMP9/BMP10 → 信号保留（>80%）
├── SPR 竞争: 抗体 vs Activin A/GDF11/BMP9/proGDF8/Bima
└── 选择性指数: IC50(ActA)/IC50(GDF11) > 100x

Phase 3: 二级功能 + GLP-1
│
├── C2C12 肌管萎缩/肥大实验
├── 肝脏铁调素/葡萄糖生成检测
├── GLP-1 肽段设计 + cAMP 检测
└── 受体占有率 FACS

Phase 4: 组装与体内验证
│
├── 双特异性组装（Knob-in-Hole / CrossMab）
├── GLP-1 肽段融合
├── 整体功能验证: 三重活性确认
└── DIO 小鼠体内实验
    ├── 药效: EchoMRI / 肌肉重量 / GTT/ITT/PTT / 代谢标志物
    └── 选择性安全性: μCT 骨密度 / 出血观察 / 铁代谢 / 超声心动图
        ├── GDF11 信号保留验证（SMAD2/3 磷酸化）
        ├── BMP9/10 信号保留验证（SMAD1/5/8 磷酸化）
        └── 受体占有率监测（组织 ActRII 结合）
```

---

## 九、关键文献索引

### 结构生物学文献（新增）

| 编号 | 作者（年份） | 期刊 | 核心内容 | PDB ID |
|------|-------------|------|----------|--------|
| [S1] | Thompson TB et al. (2003) | EMBO J | Activin A/ActRIIB 晶体结构 | 1NYS |
| [S2] | Greenwald J et al. (2004) | Mol Cell | Activin A/ActRIIB 另一晶型 | 1S4Y |
| [S3] | Morvan F et al. (2017) | PNAS | Bimagrumab/ActRIIB 结构，Bima 表位 | 5NGV, 5NHR |
| [S4] | Goebel EJ et al. (2019) | PNAS | GDF11/ActRIIB/ALK5 三元复合物，GDF11 盐桥 | 6MAC |
| [S5] | PDB (2016) | Acta Cryst F | GDF11 晶体结构 | 5E4G |
| [S6] | Cotton TR et al. (2018) | EMBO J | Pro-GDF8 前体结构，潜伏机制 | 5NTU |
| [S7] | Dagbay K et al. (2020) | JBC | SRK-015/pro-GDF8 结构，prodomain 表位 | 6UMX |
| [S8] | Townson SA et al. (2012) | Structure | ActRIIB/activin A 结合动力学 | — |
| [S9] | Sako T et al. (2010) | JBC | ActRIIB 突变分析，Leu79 差异性能量贡献 | — |
| [S10] | McCoy PL et al. (2019) | — | ActRIIB 结构功能综述 | — |
| [S11] | Widjaja AA et al. (2013) | — | ActRIIB-myostatin 接触残基 | — |
| [S12] | Cash JN et al. (2009) | EMBO J | Myostatin/follistatin 结构 | — |
| [S13] | Chu J et al. (2022) | Nat Commun | BMP10/ALK1/BMPRII 结构，ActRIIA vs BMPR2 | 7PPC |
| [S14] | Kumar R et al. (2021) | Sci Rep | 异源二聚体配体陷阱，BMP9/10 选择性 | — |
| [S15] | PDB 4FAO (2012) | — | BMP9/ALK1/ActRIIB 三元复合物 | 4FAO |

### 配体功能文献

| 编号 | 作者（年份） | 期刊 | 核心内容 |
|------|-------------|------|----------|
| [29] | Chen JL et al. (2017) | PNAS | 联合抑制 activins 和 myostatin 增加肌肉量 150% |
| [32] | Morvan F et al. (2017) | PNAS | Bimagrumab 双抗 ActRIIA/IIB 机制及 CAGA12-Luc 筛选系统 |
| [35] | Nunn E et al. (2024) | Mol Metab | ActRII 阻断 + GLP-1 联合用药在 DIO 小鼠中的药效 |
| [37] | McPherron AC et al. (1997) | Nature | GDF8/myostatin 发现 |
| [39] | Chen JL et al. (2014) | FASEB J | Activins 促进肌肉萎缩 |
| [41] | Ding H et al. (2016) | J Cachexia Sarcopenia Muscle | Activin A 通过 p38β MAPK 诱导肌肉分解 |
| [42] | Lee SJ et al. (2023) | J Gerontol A | Myostatin/Activin A 靶向挑战与前景 |
| [44] | Dong J et al. (2015) | Int J Obes | Myostatin 抑制通过 irisin 改善胰岛素敏感性 |
| [51] | Deng B et al. (2017) | Nutr Metab | Myostatin 在脂肪量调节中的功能 |
| [52] | Yang M et al. (2023) | Front Endocrinol | Myostatin 作为代谢综合征治疗靶点 |
| [60] | Kobayashi N et al. (2025) | Nat Commun | Activin B 通过 FGF21 改善糖代谢 |
| [61] | Canali S et al. (2016) | Endocrinology | Activin B 非经典 Smad1/5/8 信号诱导铁调素 |
| [62] | Kanamori Y et al. (2016) | Sci Rep | Activin B 调节铁调素表达 |
| [63] | Wang Y et al. (2022) | Hepatol Commun | Activin B 促进肝纤维化 |
| [64] | Latres E et al. (2017) | Nat Commun | Activin A 在灵长类中比 GDF8 更重要地调节肌肉量 |
| [65] | Heymsfield SB et al. (2021) | JAMA Netw Open | Bimagrumab 在 T2D+肥胖中的体脂减少 |
| [67] | Heymsfield SB et al. (2026) | Nat Med | Bimagrumab + Semaglutide 联合 Phase 2 |
| [79] | Zhao D et al. (2024) | eLife | BMP9/10 维持肝脏健康 |
| [82] | Babitt JL et al. (2007) | J Clin Invest | BMP 信号调节铁平衡 |
| [83] | Chen C et al. (2021) | J Diabetes Res | BMP 家族在骨/肥胖/葡萄糖代谢中的功能 |
| [85] | Chen C et al. (2024) | Biomolecules | BMP9 在肝脏疾病中的作用 |
| [91] | Liu H et al. (2023) | Diabetes | Activin A 在 MASLD 中的情境依赖性角色 |
| [92] | Jönsson C et al. (2024) | Scand J Gastroenterol | Activin A 水平与肝纤维化正相关 |
| [93] | Hamang M et al. (2023) | Biochem Pharmacol | Activins 在肝脏健康和疾病中的作用 |
| [94] | Mekala S et al. (2024) | Cells | Activin A 拮抗剂作为肝病治疗策略 |
| [96] | Lu B et al. (2019) | J Transl Med | GDF11 基因转移防止高脂饮食诱导肥胖 |
| [97] | Katsimpardi L et al. (2019) | Aging Cell | GDF11 刺激脂联素分泌 |
| [98] | Frohlich J et al. (2022) | Cell Prolif | GDF11 抑制脂肪生成 |
| [99] | Walker R et al. (2020) | Sci Rep | 外源 GDF11 减少体重并改善葡萄糖稳态 |
| [100] | Lin S et al. (2023) | Heliyon | GDF11 抑制脂肪分化 |
| [101] | Sagliocchi S et al. (2026) | J Basic Clin Physiol Pharmacol | GDF11 促进脂肪棕色化 |

### 筛选模型文献

| 编号 | 作者（年份） | 期刊 | 核心内容 |
|------|-------------|------|----------|
| [25] | Chen H et al. (2018) | JoVE | 腺病毒 CAGA12-Luc 报告系统 |
| [26] | Marvin DL et al. (2022) | Cancers | CAGA 报告基因单细胞 Smad3 信号可视化 |
| [120] | Dagbay K et al. (2020) | JBC | SRK-015/pro-myostatin 结构及激活抑制机制 |
| [121] | Cote S et al. (2019) | SLAS Discovery | 血清 latent myostatin 定量免疫分析 |
| [125] | Welsh BT et al. (2021) | Int J Toxicol | Apitegromab 临床前安全性 |
| [127] | David L et al. (2007) | Blood | BMP9/BMP10 作为 ALK1 功能性激活体 |
| [130] | David L et al. (2008) | Circ Res | BMP9 作为循环血管静息因子 |
| [132] | Tillet E et al. (2018) | JBC | BMP9-BMP10 异源二聚体是血浆主要 BMP 活性形式 |

---

## 十、参考文献

> **说明**：[S1]-[S15] 为结构生物学文献（新增），[25]-[132] 为生物学功能文献（保留自原报告）。

## References
<a id="ref-S1"></a>[S1] Thompson TB, Woodruff TK, Jardetzky TS. (2003). Structures of an ActRIIB:activin A complex reveal a novel binding mode for TGF‑β ligand:receptor interactions. *The EMBO Journal*, 22(7):1555–1566. [https://doi.org/10.1093/emboj/cdg156](https://doi.org/10.1093/emboj/cdg156). PDB: 1NYS

<a id="ref-S2"></a>[S2] Greenwald J, Vega ME, Allendorph GP, Fischer WH, Vale W, Choe S. (2004). A flexible activin explains the membrane‑dependent cooperative assembly of TGF‑β family receptors. *Molecular Cell*, 15(3):485–489. [https://doi.org/10.1016/j.molcel.2004.07.011](https://doi.org/10.1016/j.molcel.2004.07.011). PDB: 1S4Y

<a id="ref-S3"></a>[S3] Morvan F, Rondeau JM, Zou C, et al. (2017). Blockade of activin type II receptors with a dual anti‑ActRIIA/IIB antibody is critical to promote maximal skeletal muscle hypertrophy. *Proceedings of the National Academy of Sciences*, 114(47):12478–12483. [https://doi.org/10.1073/pnas.1707925114](https://doi.org/10.1073/pnas.1707925114). PDB: 5NGV, 5NHR

<a id="ref-S4"></a>[S4] Goebel EJ, Corpina RA, Hinck CS, et al. (2019). Structural characterization of an activin class ternary receptor complex reveals a third paradigm for receptor specificity. *Proceedings of the National Academy of Sciences*, 116(31):15505–15513. [https://doi.org/10.1073/pnas.1906253116](https://doi.org/10.1073/pnas.1906253116). PDB: 6MAC

<a id="ref-S5"></a>[S5] PDB entry 5E4G. (2016). Crystal structure of human growth differentiation factor 11 (GDF‑11). *Acta Crystallographica Section F*, 72:160–164. PDB: 5E4G

<a id="ref-S6"></a>[S6] Cotton TR, Fischer G, Wang X, et al. (2018). Structure of the human myostatin precursor and determinants of growth factor latency. *The EMBO Journal*, 37(3):367–383. [https://doi.org/10.15252/embj.201797883](https://doi.org/10.15252/embj.201797883). PDB: 5NTU, 5NXS

<a id="ref-S7"></a>[S7] Dagbay K, Hill SE, Saldana M, et al. (2020). Structural basis of pro‑myostatin latency and activation by SRK‑015. *Journal of Biological Chemistry*, 295(25):8497–8508. [https://doi.org/10.1074/jbc.RA119.012293](https://doi.org/10.1074/jbc.RA119.012293). PDB: 6UMX

<a id="ref-S9"></a>[S9] Sako T, Hata K, Tanabe H, et al. (2010). A novel mechanism of activin‑induced Smad2/3 signaling in ActRIIB‑expressing cells. *Journal of Biological Chemistry*, 285(31):24102–24112. [https://doi.org/10.1074/jbc.M109.093249](https://doi.org/10.1074/jbc.M109.093249)

<a id="ref-S13"></a>[S13] Chu J, Wang Y, Bhatt S, et al. (2022). Molecular basis of ALK1‑mediated signalling by BMP9/BMP10. *Nature Communications*, 13(1):2373. [https://doi.org/10.1038/s41467‑022‑30111‑2](https://doi.org/10.1038/s41467-022-30111-2). PDB: 7PPC

<a id="ref-S14"></a>[S14] Kumar R, et al. (2021). Heterodimeric traps enhance selective ligand blockade. *Scientific Reports*. [https://doi.org/10.1038/s41598‑021‑03635‑2](https://doi.org/10.1038/s41598-021-03635-2)

<a id="ref-S15"></a>[S15] PDB entry 4FAO. (2012). Specificity and structure of a high affinity Activin receptor‑like kinase 1 (ALK1) signaling complex. PDB: 4FAO

<a id="ref-25"></a>[25] Chen H, Tian T, Miao C, et al. (2018). Adenoviral Delivery of CAGA(12)‑Luciferase Reporter for Live Cell and In Vivo Imaging of TGF‑β/Smad3 Signaling. *Journal of Visualized Experiments*. [https://doi.org/10.3791/57926](https://doi.org/10.3791/57926)

<a id="ref-29"></a>[29] Chen JL, Walton KL, Colgan TD, et al. (2017). Specific targeting of TGF‑β family ligands demonstrates that activin and myostatin cooperate to repress muscle mass. *Proceedings of the National Academy of Sciences*, 114(24):E4779–E4788. [https://doi.org/10.1073/pnas.1620013114](https://doi.org/10.1073/pnas.1620013114)

<a id="ref-32"></a>[32] Morvan F, Rondeau JM, Zou C, et al. (2017). Blockade of activin type II receptors with a dual anti‑ActRIIA/IIB antibody is critical to promote maximal skeletal muscle hypertrophy. *Proceedings of the National Academy of Sciences*, 114(47):12478–12483. [https://doi.org/10.1073/pnas.1707925114](https://doi.org/10.1073/pnas.1707925114)

<a id="ref-35"></a>[35] Nunn E, et al. (2024). ActRII blockade and GLP‑1 receptor agonism synergistically preserve lean mass and enhance fat loss in diet‑induced obese mice. *Molecular Metabolism*. [https://doi.org/10.1016/j.molmet.2024.101880](https://doi.org/10.1016/j.molmet.2024.101880)

<a id="ref-37"></a>[37] McPherron AC, Lawler AM, Lee SJ. (1997). Regulation of skeletal muscle mass in mice by a new TGF‑β superfamily member. *Nature*, 387(6628):83–90. [https://doi.org/10.1038/387083a0](https://doi.org/10.1038/387083a0)

<a id="ref-39"></a>[39] Chen JL, Walton KL, Winbanks CE, Murphy KT, Thomson RE, Makanji Y, Qian H, Lynch GS, Harrison CA, Gregorevic P. (2014). Elevated expression of activins promotes muscle wasting and cachexia. *FASEB Journal*, 28(4):1711–1723. [https://doi.org/10.1096/fj.13‑245894](https://doi.org/10.1096/fj.13-245894)

<a id="ref-41"></a>[41] Ding H, Zhang G, Sin KWT, Liu Z, Lin RK, Li M, et al. (2016). Activin A induces skeletal muscle catabolism via p38β mitogen‑activated protein kinase. *Journal of Cachexia, Sarcopenia and Muscle*, 8(2):202–212. [https://doi.org/10.1002/jcsm.12145](https://doi.org/10.1002/jcsm.12145)

<a id="ref-42"></a>[42] Lee SJ, Bhasin S, Klickstein L, et al. (2023). Challenges and Future Prospects of Targeting Myostatin/Activin A Signaling. *Journals of Gerontology: Series A*, 78(Suppl 1):32–37. [https://doi.org/10.1093/gerona/glad033](https://doi.org/10.1093/gerona/glad033)

<a id="ref-44"></a>[44] Dong J, Dong Y, Dong Y, et al. (2016). Inhibition of myostatin improves insulin sensitivity through irisin‑mediated cross‑talk between muscle and adipose tissues. *International Journal of Obesity*, 40(3):439–446. [https://doi.org/10.1038/ijo.2015.200](https://doi.org/10.1038/ijo.2015.200)

<a id="ref-51"></a>[51] Deng B, Zhang F, Wen J, Ye S, Wang L, Yu Y, et al. (2017). The function of myostatin in the regulation of fat mass. *Nutrition & Metabolism*, 14:29. [https://doi.org/10.1186/s12986‑017‑0179‑1](https://doi.org/10.1186/s12986-017-0179-1)

<a id="ref-52"></a>[52] Yang M, Liu C, Jiang N, Liu Y, Luo S, Li C, et al. (2023). Myostatin: a potential therapeutic target for metabolic syndrome. *Frontiers in Endocrinology*, 14:1181913. [https://doi.org/10.3389/fendo.2023.1181913](https://doi.org/10.3389/fendo.2023.1181913)

<a id="ref-60"></a>[60] Kobayashi N, et al. (2025). Activin B improves glucose metabolism by inducing FGF21 and hepatic glucagon resistance. *Nature Communications*. [https://doi.org/10.1038/s41467‑025‑58836‑w](https://doi.org/10.1038/s41467-025-58836-w)

<a id="ref-61"></a>[61] Canali S, Core AB, Zumbrennen‑Bullough KB, et al. (2016). Activin B induces hepcidin via non‑canonical Smad1/5/8 signaling. *Endocrinology*, 157(6):2467–2479. [https://doi.org/10.1210/en.2015‑1747](https://doi.org/10.1210/en.2015-1747)

<a id="ref-62"></a>[62] Kanamori Y, Murakami M, Sugiyama M, et al. (2016). Inflammation‑induced activin B regulates hepcidin through ALK2/ActRIIA. *Scientific Reports*, 6:38702. [https://doi.org/10.1038/srep38702](https://doi.org/10.1038/srep38702)

<a id="ref-63"></a>[63] Wang Y, et al. (2022). Activin B promotes liver fibrosis via JNK/iNOS/PARP1 signaling. *Hepatology Communications*, 6(11):3145–3161. [https://doi.org/10.1002/hep4.2037](https://doi.org/10.1002/hep4.2037)

<a id="ref-64"></a>[64] Latres E, Mastaitis J, Fury W, et al. (2017). Activin A more prominently regulates muscle mass in primates than does GDF8. *Nature Communications*, 8:15153. [https://doi.org/10.1038/ncomms15153](https://doi.org/10.1038/ncomms15153)

<a id="ref-65"></a>[65] Heymsfield SB, Coleman LA, Miller R, Rooks DS, Laurent D, Petricoul O, Praestgaard J, Swan T, Wade T, Perry RG, Goodpaster BH, Roubenoff R. (2021). Effect of Bimagrumab vs Placebo on Body Fat Mass Among Adults With T2D and Obesity. *JAMA Network Open*, 4(1):e2033457. [https://doi.org/10.1001/jamanetworkopen.2020.33457](https://doi.org/10.1001/jamanetworkopen.2020.33457)

<a id="ref-67"></a>[67] Heymsfield SB, et al. (2026). Bimagrumab and Semaglutide Combination Therapy in Obesity: BELIEVE Phase 2. *Nature Medicine*. [https://doi.org/10.1038/s41591‑026‑04204‑0](https://doi.org/10.1038/s41591-026-04204-0)

<a id="ref-79"></a>[79] Zhao D, Huang Z, Li X, et al. (2024). BMP9 and BMP10 coordinate liver cellular crosstalk. *eLife*, 13:e95811. [https://doi.org/10.7554/eLife.95811](https://doi.org/10.7554/eLife.95811)

<a id="ref-82"></a>[82] Babitt JL, Huang FW, Xia Y, Sidis Y, Andrews NC, Lin HY. (2007). Modulation of bone morphogenetic protein signaling in vivo regulates systemic iron balance. *Journal of Clinical Investigation*, 117(7):1933–1939. [https://doi.org/10.1172/JCI31342](https://doi.org/10.1172/JCI31342)

<a id="ref-83"></a>[83] Chen C, et al. (2021). Potential Functions of the BMP Family in Bone, Obesity, and Glucose Metabolism. *Journal of Diabetes Research*, 2021:6707464. [https://doi.org/10.1155/2021/6707464](https://doi.org/10.1155/2021/6707464)

<a id="ref-85"></a>[85] Chen C, et al. (2024). BMP9 in liver diseases. *Biomolecules*, 14(8):1013. [https://doi.org/10.3390/biom14081013](https://doi.org/10.3390/biom14081013)

<a id="ref-91"></a>[91] Liu H, et al. (2023). Roles of Activin A and Gpnmb in MASLD. *Diabetes*, 72(12):1855–1868. [https://doi.org/10.2337/db23‑0357](https://doi.org/10.2337/db23-0357)

<a id="ref-92"></a>[92] Jönsson C, Bergram M, Kechagias S, Nasr P, Ekstedt M. (2024). Activin A levels in MASLD associates with fibrosis and the PNPLA3 I148M variant. *Scandinavian Journal of Gastroenterology*, 59(6):737–741. [https://doi.org/10.1080/00365521.2024.2334804](https://doi.org/10.1080/00365521.2024.2334804)

<a id="ref-93"></a>[93] Hamang M, et al. (2023). The role of activins in liver health and disease. *Biochemical Pharmacology*, 213:115668. [https://doi.org/10.1016/j.bcp.2023.115668](https://doi.org/10.1016/j.bcp.2023.115668)

<a id="ref-94"></a>[94] Mekala S, et al. (2024). Activin A antagonist NUCC‑555 as liver disease therapy. *Cells*, 13(7):649. [https://doi.org/10.3390/cells13070649](https://doi.org/10.3390/cells13070649)

<a id="ref-96"></a>[96] Lu B, et al. (2019). GDF11 gene transfer prevents HFD‑induced obesity. *Journal of Translational Medicine*, 17:425. [https://doi.org/10.1186/s12967‑019‑02166‑1](https://doi.org/10.1186/s12967-019-02166-1)

<a id="ref-97"></a>[97] Katsimpardi L, et al. (2019). Systemic GDF11 stimulates adiponectin and mimics caloric restriction. *Aging Cell*, 18(4):e13038. [https://doi.org/10.1111/acel.13038](https://doi.org/10.1111/acel.13038)

<a id="ref-98"></a>[98] Frohlich J, et al. (2022). GDF11 inhibits adipogenesis and improves adipocyte glucose metabolism. *Cell Proliferation*, 55(8):e13310. [https://doi.org/10.1111/cpr.13310](https://doi.org/10.1111/cpr.13310)

<a id="ref-99"></a>[99] Walker RG, et al. (2020). Exogenous rGDF11 reduces body weight and improves glucose homeostasis. *Scientific Reports*, 10:4965. [https://doi.org/10.1038/s41598‑020‑61443‑y](https://doi.org/10.1038/s41598-020-61443-y)

<a id="ref-100"></a>[100] Lin S, et al. (2023). GDF11 inhibits human adipose stromal cell adipogenesis via ALK5/KLF15/β‑catenin/PPARγ cascade. *Heliyon*, 9(9):e13088. [https://doi.org/10.1016/j.heliyon.2023.e13088](https://doi.org/10.1016/j.heliyon.2023.e13088)

<a id="ref-101"></a>[101] Sagliocchi S, et al. (2026). GDF11 promotes cold‑induced adipose browning via Smad2/3 signaling. *Journal of Basic and Clinical Physiology and Pharmacology*. [https://doi.org/10.1515/jbcpp‑2026‑0087](https://doi.org/10.1515/jbcpp-2026-0087)

<a id="ref-120"></a>[120] Dagbay K, Hill SE, Saldana M, et al. (2020). Structural basis of pro‑myostatin latency and activation by SRK‑015. *Journal of Biological Chemistry*, 295(25):8497–8508. [https://doi.org/10.1074/jbc.RA119.012293](https://doi.org/10.1074/jbc.RA119.012293)

<a id="ref-121"></a>[121] Cote S, et al. (2019). Development of a quantitative immunoassay for serum latent myostatin. *SLAS Discovery*, 24(2):175–183. [https://doi.org/10.1177/2472555219860779](https://doi.org/10.1177/2472555219860779)

<a id="ref-125"></a>[125] Welsh BT, et al. (2021). Preclinical safety assessment of apitegromab. *International Journal of Toxicology*, 40(5):411–419. [https://doi.org/10.1177/10915818211025477](https://doi.org/10.1177/10915818211025477)

<a id="ref-127"></a>[127] David L, Mallet C, Mazerbourg S, Feige JJ, Bailly S. (2007). Identification of BMP9 and BMP10 as functional activators of ALK1. *Blood*, 109(5):1953–1961. [https://doi.org/10.1182/blood‑2006‑07‑034124](https://doi.org/10.1182/blood-2006-07-034124)

<a id="ref-130"></a>[130] David L, Mallet C, Vailhe B, Lamouille S, Feige JJ, Bailly S. (2008). ALK1/endoglin pathway: a new regulator of vascular quiescence. *Circulation Research*, 102(8):960–968. [https://doi.org/10.1161/CIRCRESAHA.107.165530](https://doi.org/10.1161/CIRCRESAHA.107.165530)

<a id="ref-132"></a>[132] Tillet E, et al. (2018). BMP9‑BMP10 heterodimer is the major BMP active form in human plasma. *Journal of Biological Chemistry*, 293(20):7654–7665. [https://doi.org/10.1074/jbc.RA118.002968](https://doi.org/10.1074/jbc.RA118.002968)

---

*报告生成日期：2026-08-18（修订版，替代 2026-08-14 配体中和策略版）*
*基于 PDB 残基级结构分析（BioPython）+ 系统文献检索整理*
*结构分析数据：/mnt/results/receptor_contact_comparison_aligned.csv*
*结构分析图表：/mnt/results/plot_receptor_*.png*
