# Card Harvest

> **Core-edition note.** This reference describes a durable-note harvest for a learner
> who keeps an external note store. No note store, harvest script or canonical-state
> adapter ships with this core. Without one, the draft/preview discipline still
> applies, but drafts stay local Markdown, nothing is committed, and no canonical
> state changes. Say so plainly rather than simulating a commit.

Card Harvest 的目的不是由 Agent 重新总结原著，而是把用户已经在 primary-text reading、open reconstruction、hinge repair、explain-back 与 Exit Reconstruction 中**生成并经校准的理解**整理为可复用的、来源绑定的卡片候选，避免学习结束后重复手工总结。

## 默认范围与时机

- Mode 0 默认只产生 `L` 文献卡候选；不得自动生成 `E` 永久笔记，也不得自动生成 `P` 问题卡。
- `E` / `P` 只能在后续阶段作为候选：`E` 需要用户确认其为稳定的独立判断；`P` 可由真正未决的文本或论证问题触发，但不得自动 draft、commit 或升级为研究问题。
- 不按每轮问答或每个 micro-check 生成卡。默认候选单位是：完成的 Passage Package、完成的 argument node、或完成的局部 argumentative chain。
- Harvest 在后台排队，不打断 micro-check。只在以下节点集中报告：完成一个 Passage Package、完成 Coherent Argument Pathway 的一个局部单元、或 Mode 0 session 正常结束 / 暂停时。
- 每到上述节点，必须执行一次静默的 Harvest-disposition check，即使结论是不制卡。把候选单位、结论（`CANDIDATE` / `DEFER` / `NONCARD`）、理由，以及 `DEFER` 的明确重访触发条件记录到 `learning-state.md`。不得让一个已完成局部链仅因后续阅读继续推进而无记录地悬置；否则 Harvest 会依赖 Agent 记忆而可无限推迟。

## Harvest source order

候选内容必须按以下优先序保留，而非由 Agent 的流畅概括覆盖：

1. user-generated open reconstruction；
2. repaired / confirmed explain-back；
3. user-confirmed correction；
4. primary-text evidence；
5. agent calibration。

Agent calibration 只有在用户明确确认、亲自重述，或在后续开放重构中成功运用时，才可进入候选；否则只留在 `learning-state.md`，不得写进卡片为用户理解。

## 双产物输出架构：Internal Draft 与 Rendering Preview

Card Harvest 必须生成两个**内容层级不同**的 project-local 产物；不得把内部审计 schema 直接当成未来卡片正文。

1. **Harvest Internal Draft**：权威审计与确认包。它保留：
   - candidate status、deduplication result、proposed filename；
   - passage / pathway metadata、source / page range、local question、textual / argumentative context；
   - provenance-separated `user-generated understanding`、`primary-text evidence`、`agent calibration`、`unresolved`；
   - textual / interpretive boundary 与真实未决项。
   它只保存于项目 `card-drafts/card-harvest/`，不得写入笔记库。
2. **Rendering Preview**：拟提交正文的纯 outliner block 呈现。它不复制 candidate status、去重过程、provenance 标签、workflow metadata、boundary / unresolved 栏目或 Agent 身份标签。它只保存于 project-local preview 路径，等待用户确认后才可能成为提交内容。

Internal Draft 中每项仍须显式标明 provenance，且不得混写：

```text
user-generated understanding
primary-text evidence
agent calibration
unresolved
```

只收集已经在项目记录中存在的用户重构、用户确认的校准与实际文本证据；不要为填满 schema 而补写用户没有形成的理解。`unresolved` 只记录真实保留的问题、文本压缩处或用户提出的困惑，不自动扩展为 P 卡。

## Rendering Preview 规则

- `L` 文件名继续使用现有笔记库的形式：`L：` + 概念、命题或可独立引用的论证结论；不得使用 Passage Package 名、Bridge 编号、学习阶段或 workflow 标签。
- preview 正文必须使用笔记库真实使用的 outliner blocks，不能使用 Markdown heading / 表单字段，也不在正文重复一级标题。
- 默认骨架是：可选的现有 `#tag` → 核心命题／概念界定（优先保留用户重构）→ 必要的嵌套论证、限定或反驳 → `- ---` → 已核验的来源行；它不是每张卡都必须有 tag、引文或嵌套层级的强制模板。
- preview 的内容优先序不变：用户开放 reconstruction → repaired / confirmed explain-back → user-confirmed calibration → primary-text evidence → Agent calibration。Agent 不得为了更学术或更流畅而改写用户已经形成的论证结构。
- 生成 preview 前再次以只读方式检查现有笔记库：只加入已存在、语义明确且真正承担概念或论证关系的链接；保留目标的原始全角／半角拼写；不得为链接密度创建新页或加入远距离关联。
- tag 不是必填项；仅使用笔记库中已有且稳定、准确的 tag。不得创建 `tags::`、`source::`、`type::` 或其他新 properties。
- source section 只在来源与页码已经核验时采用现有卡片习惯：`- ---` 后给书名、作者／译者、页码。若中心命题依赖一条高度浓缩、已核验的原文措辞，可在其下保留**一条最关键的短引文**作为 `>` blockquote；否则省略。不得为形式完整而生成、改写或伪造引文。
- textual / interpretive boundary 与 unresolved 默认仅留在 Internal Draft。只有某个疑难对该卡哲学意义不可省略时，才可转化为现有笔记库习惯中的 `疑难：`、`批判：`、`==问题==` 或普通嵌套 block；不得保留 workflow 标签。

## Card Harvest procedure

1. 先完成并记录 Passage Package / node 的学习状态；单次正确答案、recognition-only 回答或未完成的 repair 不触发 Harvest。到 Package Exit、局部链闭合或正常暂停时，先记录 Harvest disposition；后续章节尚未读完不构成自动 `DEFER` 理由。
2. 在决定卡片数量、标题或类型之前，从 `learning-state.md` 中逐项提取该单位的已确认材料，并建立 coverage map：核心 claim、必要论证转换、决定性例子、用户原话式重构、已确认校准、文本限度与未决 warrant，必须逐项映射为某一候选卡、明确 deferred destination 或 justified non-card destination。卡片数由这个映射决定，不得用一个醒目的结论代替完整重构。
3. 再按该 map 建立 provenance-separated **Harvest Internal Draft**；学习过程、错误类型、提示层级和未获确认的 Agent 解释仍留在 `learning-state.md`。若 handoff 或摘要压缩了关键桥梁，先从 prior session reconstruction 恢复，不得据摘要补写。
4. 以只读方式检查笔记库中是否已有相关 `L` 卡。检索必须以 source、page range、author/text、局部问题和现有链接为线索，并阅读候选卡正文；文件名前缀或单一关键词不能单独证明重复。
5. 已有相关 L 卡时，Internal Draft 记录 `append / merge candidate`；没有重复时，才记录 new candidate。两种情形均不得修改笔记库。
6. 对每个 Internal Draft 生成独立的 **Rendering Preview**，并再做一次最小只读 links / tags 检查。Internal Draft 与 preview 不得共用同一正文格式。
7. 在集中报告节点汇报候选数量、关联现有卡、拟新建 / merge 状态、preview 与未决项。严格遵守：`READ → Internal Draft → Rendering Preview → editable local draft → user edits → diff / mechanical validation → explicit user confirmation → commit`。机械草稿只能生成可编辑 `.md`、baseline、hash、metadata、diff 和机械 validation；Agent 仍负责卡片内容、颗粒度、用户修改的语义解释与写作偏好学习。没有笔记库或提交工具时，流程在 `explicit user confirmation` 后停止：把稿件交给用户，不执行 commit。

   若 candidate 已经创建，随后却改变了中心概念、拟定文件名或 source / page span，这不是普通文字修订：保留旧 candidate 的 Internal Draft 作为 superseded audit trace，并从新的 preview 创建新的 candidate。不要把 scope-rescoping 写进旧文件后继续沿用旧 metadata；baseline/hash 只能跟踪字节变化，不能证明 source anchor、范围与正文仍一致。提交后的身份登记、手工编辑识别与后续修订必须遵循笔记库自己的卡片身份规则；这些记录只存在 project-local metadata，不得写入卡片正文。

## Learning-state boundary

`learning-state.md` 保存学习轨迹：失败、提示、repair、support fading 与当前掌握状态。Harvest Internal Draft 保存可再利用、来源绑定的审计材料；Rendering Preview 仅模拟用户现有的卡片呈现。三者不得简单复制全文；Harvest 不修改 Horizon、Claim Status、Active Research Question、Thesis 或笔记库。
