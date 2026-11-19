# Literature Acquisition and Intake

This reference owns the acquisition procedure for secondary literature: what to obtain,
in what order, how to record it, and where the agent must stop and ask the learner. No
acquisition script, index or PDF checker ships with the core. "Record" means a Markdown
entry in the project's literature record.

## 1. 文献重要性分级

对检索到的文献区分：

- **Core**：直接决定当前 competing interpretation / major horizon revision / active argument；
- **Important**：显著补充核心解释或提供重要反例；
- **Background**：综述、背景、一般性说明。

Core 文献优先保证全文获取。

## 2. 默认获取顺序

```text
current project literature/sources
→ configured local literature roots
→ lawful web acquisition
→ User Acquisition Request
```

即先查当前项目已下载文献，再查项目配置的本地文献根目录，再联网获取（下面的「获取优先级」是 web acquisition 这一步的内部顺序），最后若仍无法取得 Core 全文才发起 User Acquisition Request。

## 3. 广泛网络发现与获取优先级（仅适用于 Agent 新获取）

对 Core / Important 文献，Agent 可以进行广泛网络检索，用于确认版本、完整书目信息、DOI、可用性、馆藏 / 借阅状态与潜在全文位置；不得把检索范围不必要地限于出版社首页或少数数据库。检索发现的候选位置必须区分为：已验证可访问、availability lead、或未验证线索。

当且仅当 Agent 要**主动获取一份新的外部副本**时，按以下顺序尝试：

1. publisher / official OA；
2. institutional repository；
3. author manuscript / accepted manuscript / preprint；
4. legal digital lending / public-domain copy；
5. other clearly authorized full-text source。

如果仍无法取得全文，可记录其他索引或镜像生态中存在该文献这一事实，标为 `availability lead`，并注明未验证授权 / 未下载；不得自动下载明显未经授权分发的受版权保护全文。若该文献为 Core，发出 User Acquisition Request。

不得从明显未授权来源主动下载新的受版权保护文献。该限制只约束 Agent 的新获取动作，不适用于已经存在于用户本地、当前项目或用户提供渠道中的材料。

## 4. 获取程序（无脚本路线）

每一份新来源按同一顺序手工执行，并逐步记录：

```text
read-only availability check
→ choose one verified lawful route
→ obtain the file (or ask the learner)
→ verify identity from the title page or an authoritative record
→ record local path, access type, access date and reading boundary
```

- 先只做只读检查并列出候选合法路径，再获取，再登记。
- 每一项来源事实标明为「Agent 手工核验」，不得冒称文件级脚本事实。
- 遇到 paywall、登录、CAPTCHA、anti-bot challenge、unauthorized mirror 或授权不明，停在 `HUMAN_ACTION_REQUIRED`，不得绕过。
- 不得覆盖、替换或删除来源文件。若同名文件已存在，先确认是否为同一文献。
- 若合法下载的 PDF 保存为无扩展名或不透明响应名，先核验内容，再将项目副本改为可识别的 `Author_Year_ShortTitle.pdf` 名称，并同步 acquisition record、Literature Matrix 与文献索引。
- 解析器能读取不等于用户可在系统文件管理器中直接识别和打开。

The acquisition record establishes file-level facts, not a complete citation. Before assigning a newly acquired source a corpus role or using it in a Passage Package, verify its bibliographic identity from the title page, first-page header, or authoritative source record, then record the confirmed citation, version, local path, access type, and reading boundary in the Literature Matrix. Do not promote a null or filename-derived title into a citation.

`OCR_REQUIRED` 只表示文件已安全保存为本地副本；是否进行 OCR 由学习者决定，并遵循 Manual OCR Rule。不得自动 OCR。

## 5. 自动下载规则

如果 Agent 能合法取得 Core / Important 文献全文：

- 下载到当前项目 `literature/sources/`；
- 推荐文件名 `Author_Year_ShortTitle.pdf`（按实际书目替换，不使用示例年份）；
- 如果是 HTML / text full text，可保存为 `.html` 或 `.md`，但优先保留原始 PDF；
- 不覆盖同名文件，除非确认是同一文献且用户允许；
- 下载后校验文件可打开，并记录来源 URL 与访问日期。

## 6. literature-map 记录

每个已获取来源记录：

- full citation
- local path
- source URL
- access type
- access date
- acquisition status：downloaded full text / local user-provided copy / local copy already existed / abstract only / preview only / user needed
- access status：text layer usable / OCR required / waiting for user-provided OCR copy
- availability leads：index / mirror ecosystem existence, location or identifier, verification status, and `not downloaded` where authorization is unverified
- relevance：Core / Important / Background
- reading status：not read / skimmed / relevant section read / full read / paused for OCR

## 7. 无法取得全文时的规则

如果 Core 文献无法由 Agent 合法获取全文：

- 不得悄悄用 abstract 替代全文，也不得跳过；
- Agent 必须告诉用户：
  - 文献完整 citation；
  - 为什么它是 Core；
  - 已尝试过哪些获取路径；
  - 当前能看到的 access level；
  - 希望用户帮助寻找什么版本：publisher PDF / accepted manuscript / scanned chapter / library copy。

然后进入 User Acquisition Request（Manual Acquisition Handoff）。该 handoff 必须最小化为：作者、完整题名、年份、所需范围（整本 / 指定章 / 完整文章）、已知优先章节或页码、为何需要、以及 `literature/sources/` 目标目录；不得要求用户重命名文件或重复提供已经记录的书目信息。用户在该请求后自行提供或上传文件后：

- 不再追查、推断或裁决其历史获取来源；
- 按 user-provided research material 处理；
- 依照 Existing Local / User-Provided Material 规则继续正常研究；
- 如用户请求整理，可复制 / 整理到当前项目 `literature/sources/`，但不覆盖原文件；
- 更新 literature-map。

## 8. 比较性研究的对称性

当 FIDD 比较两个竞争解释时：

- 如果 A 方已有全文 Core 文献，而 B 方只有 overview / abstract，不得据此做最终比较或宣布某一边更强；
- 应优先尝试补齐 B 方至少一篇 Core specialist source；
- 若获取失败，应请求用户协助。

## 9. 不要把「能访问网页」误当成「已纳入项目」

对 Core / Important 文献：

- 在线阅读只算 temporary access；
- 如果合法可下载，应保存本地副本；
- project literature files 应成为后续跨-thread 研究的持久资料。

## 10. 本地目录结构

仅当项目实际获取、接收或需要持久保存本地文献副本时，才建立以下目录；若学习者只提供一段文本作局部阅读，则不为满足目录结构而创建项目文献库：

- `literature/sources/`
- 可选：`literature/notes/`

不要把下载的二手文献放进学习者笔记库。

## 11. Existing Local / User-Provided Material

下列材料一律视为 **user-provided research material**：

- 配置的 Local literature roots 中已经存在的文件；
- 当前项目中已经存在的文件；
- 用户主动上传的文件；
- 用户在 User Acquisition Request 后自行提供的文件。

Agent 可以对这类材料执行：

- 打开与读取；
- 文本检索或 text extraction；如 PDF 被判定为 `OCR required`，严格遵循 Manual OCR Rule：不得自动 OCR，改发出 Manual OCR Request；
- summarize；
- Guided Text Entry 或 Secondary Text Entry；
- quotation verification；
- argument reconstruction；
- citation、页码与文本位置分析。

文件名、metadata 或历史命名出现 `z_library`、`1lib`、`libgen` 或其他来源标签，不得单独成为拒绝读取本地已有文件的依据。Agent 不得仅凭此类标签推断、追查或裁决用户的历史获取是否合法。

如 provenance 对研究记录有必要，只记录 `local user-provided copy`；不得将文件名中的来源标签转换为法律判断。

## 12. 本地文献根目录（只读）

对项目配置的本地文献根目录（configured local literature roots）：

- 递归、只读搜索；
- 不自动移动原文件；
- 不自动重命名；
- 不自动删除；
- 不修改原始 PDF/EPUB/DOCX；
- 若某篇文献是当前项目 Core source，只有在用户请求或项目工作确有持久副本需要时，才复制一份到项目 `literature/sources/`，并保留原文件不变。

本地检索支持按 DOI、author、year、title、filename 匹配目标文献。若找到多个疑似版本，不要自动选择，先报告各版本差异（年份、版本、语言、页数 / PDF 元数据等），由用户决定。

## 13. 用户控制

自动下载只适用于：

- 合法公开可访问；
- 明确属于当前项目；
- Core / Important research literature。

不要批量下载大量「可能有用」的文献。默认每轮最多自动下载 3–5 篇新文献，除非用户另有要求。

## 14. Safety boundary

本规则不授权 Agent 主动寻找盗版下载链接、指导绕过付费墙，或从明确未授权来源替用户下载新的受版权保护材料。对新获取动作始终适用 lawful acquisition rule；对 Existing Local / User-Provided Material 则按上述阅读与分析规则处理。

## 15. FIDD 特别规则

在 Focused Interpretive Deep Dive 中：

- 每个主要 competing interpretation 尽量至少确保 1 篇本地可读 Core specialist source；
- handbook / SEP 不算替代 specialist source；
- 如果某一路线的代表文献无法取得，主动请求用户帮助，而不是直接用 overview 代表该立场。
