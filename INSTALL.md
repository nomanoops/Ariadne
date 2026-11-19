# 安装与启动（macOS）

## 验证范围

当前候选在 macOS 14.1.2、Hermes Agent v0.21.7+6274.gbf0203a 上，使用全新隔离 `HERMES_HOME` 手工复制；文件逐项一致，`hermes skills list` 发现 `ariadne`。同机已有 gateway 时，为避免碰触生产 gateway，测试额外指定了独立 gateway 锁目录；通过真实模型 `deepseek-v4-pro` 运行一次 `hermes chat` 单轮对话，记录显示实际调用 `skill_view`，且返回的正文与本候选逐字一致。

**这是特殊隔离测试，不是对默认 gateway 启动、其他版本或其他平台的验证。** 模型实际表现的限制见 [KNOWN-LIMITATIONS.md](KNOWN-LIMITATIONS.md)。

## 先决条件

1. 已安装 Hermes Agent，终端中 `hermes --version` 可运行。
2. 可访问经你授权的模型；在所选 Hermes 环境中按照 Hermes 官方文档完成提供方配置。测试使用已有授权，没有把凭据复制到发行包中。不要在聊天或公开反馈中粘贴密钥。
3. 已取得本候选文件，终端位于包含 `skill/ariadne/SKILL.md` 的发行目录根部。需要 `rsync` 和 `diff`。

## 安装与发现

以下命令新建一个隔离目录，不覆盖已有 Skill；不要指向已有的 Hermes 数据目录。

```bash
TEST_HOME="$HOME/.ariadne-review-home"
if [ -e "$TEST_HOME" ]; then
  printf '%s\n' '测试目录已存在；停止并选择一个尚不存在的目录。' >&2
else
  mkdir -p "$TEST_HOME/skills/research/ariadne"
  rsync -a skill/ariadne/ "$TEST_HOME/skills/research/ariadne/"
  diff -qr skill/ariadne/ "$TEST_HOME/skills/research/ariadne/"
  HERMES_HOME="$TEST_HOME" hermes skills list
fi
```

如果复制成功，列表应包含一条 `ariadne`、`local`、`enabled`。`diff` 无输出表示比较的内容一致。首次启动 Hermes 可能自动添加其自带技能，因此之后列表不一定只有一条记录。

## 启动一次对话

在配置了可用模型的环境中，可以尝试：

```bash
HERMES_HOME="$TEST_HOME" hermes chat -q '请加载 ariadne，陪我从一段原著开始讨论；先让我提供文本和困惑。' --oneshot
```

这是基于 Hermes CLI 的使用方式；**本次真实模型测试使用的是隔离锁目录与显式模型配置，不是这条默认配置命令的完整验证。** 如果同机已有 gateway，默认启动可能发生冲突。不要用 `--force`、`--replace` 或迁移命令来接管现有 gateway；请在没有冲突的独立环境测试，或参阅 Hermes 官方文档。

本次实验使用隔离 home 下另设 `HERMES_GATEWAY_LOCK_DIR`，并通过进程环境提供模型授权、显式指定提供方与模型；这是为本机并行测试采取的特殊安排，不是对所有部署安全性的保证，也不是安装必需步骤。未经理解其影响，不应在生产环境随意覆盖锁目录。

## 退出与限制

隔离目录可能包含配置和对话；不提供递归删除命令。需要清理时请自行确认准确路径与内容，再决定如何处理。不要删除日常 `~/.hermes`。

未验证：Linux、Windows、其他 Hermes 版本、多轮教学、所有 references 的运行时路由及新用户首次配置模型的完整过程。安装成功或技能加载成功，不代表哲学解释正确。
