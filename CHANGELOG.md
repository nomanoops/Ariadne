# Changelog / 版本更新

## v1.0.0

Compared with the earlier **v0.1.0-beta**, v1.0.0 reorganizes and condenses the Skill around its teaching functions while retaining its focus on primary texts, learner understanding, and open-ended exploration. These are changes to the instructions, not a claim that model behavior or learning outcomes have been proven equivalent or improved.

相较于此前的 **v0.1.0-beta**，v1.0.0 围绕教学功能重新组织并收缩了 Skill，同时保留原著阅读、学习者理解与开放性探索的核心方向。以下是规则设计的变化，不代表模型行为或学习效果已被证明等效或提升。

### Changed / 调整

- **A smaller, function-oriented structure.** The main Skill handles ordinary teaching and core evidence boundaries; four references cover entry and horizon, text pathways and evidence, difficulty and reintegration, and optional workflows. The compared beta snapshot had twelve references. / **更精简的功能结构。** 主文件承担日常教学和核心证据边界；四份 references 分别处理学习入口与视域、原著路径与证据、困难与整合，以及可选工作流。对照的 beta 快照包含十二份 references。
- **Ordinary teaching and adaptive support.** The main file brings direct explanation, difficulty diagnosis, and flexible support together without making a fixed question ladder or a specialist reference the default response to an initial difficulty. / **日常教学与动态支架。** 主文件集中处理直接解释、困难诊断和灵活支持，不把固定提问阶梯或首次困难时加载专项 reference 设为默认。
- **Explicit continuation after reconstruction.** Following the learner’s reconstruction and necessary calibration, the agent is instructed to assess the local Package Exit and choose an appropriate next action, rather than wait for a generic instruction to continue. An unresolved broader question does not automatically block a completed local goal. / **重构后的明确推进。** 学习者重构并完成必要校准后，Agent 应判断当前阅读单元是否达到退出条件，并选择适当的后续行动，而不是默认等待用户说“继续”。更宽泛的问题尚未解决，并不自动阻止已达成的局部目标。
- **Reading-contact default.** When a specific primary window was assigned and the learner subsequently reconstructs that text, the agent ordinarily assumes the reading was done for teaching and local Exit. This is not independent verification; explicit non-reading, reliance on other material, or substantial contrary evidence calls for reconsideration. / **阅读接触默认规则。** 明确布置指定原文后，若学习者提交相应文本重构，教学与局部退出通常默认其已阅读；这不等于独立核验。如明确未读、依赖其他材料或存在实质相反证据，则需要重新处理。
- **Independent host boundary.** Host-specific project state, private tools, and engineering maintenance are not bundled or assumed. Optional retrieval, notes and continuity depend on the host and permission. The earlier beta was also designed as an independent core; independence is not presented here as a newly introduced feature. / **独立宿主边界。** 不打包或假定宿主专属的项目状态、私人工具和工程维护机制；可选检索、笔记与持续学习取决于实际宿主和权限。此前 beta 也已采用独立 Core 定位，独立性本身并非本版新功能。

### Scope and limitations / 范围与限制

- The former beta included author-specific diagnostic material that is not retained as dedicated references in this version; general conceptual, comparative and difficulty-diagnosis guidance remains. / 旧版 beta 的部分特定作者诊断材料不再作为独立 references 保留；一般性的概念、比较与困难诊断指导仍在。
- The v1.0.0 package uses the MIT License. / v1.0.0 采用 MIT 许可证。
- AI can misread learners or texts and produce inaccurate quotations or interpretations. Verify important claims against sources; the structural refactor does not establish that prior model errors are fixed. / AI 仍可能误读学习者或原著、给出不准确引文或解释；重要判断应回到来源核查。本次结构重构不证明此前的模型错误已被修复。

## v0.1.0-beta / 此前测试版

An earlier Ariadne Core review candidate organized exploratory philosophical learning around primary texts, learner autonomy, coherent reading paths and explicit interpretive boundaries, without bundling the private research system. Its own documentation described it as an **unreleased candidate**. / 此前的 Ariadne Core 审阅候选以原著校准、学习者自主、连贯阅读路径与解释边界组织探索性哲学学习，不打包私人研究系统。
