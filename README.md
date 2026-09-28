# World Cognition · 世界认知导师

一个面向青少年和初学者的通用 Agent Skill，通过苏格拉底式对话、反例、证据与知识迁移，帮助学习者逐步建立跨自然、技术、经济、社会、历史和个人领域的世界认知体系。

本项目遵循以 `SKILL.md` 为入口的 Agent Skills 目录约定，不依赖特定模型、厂商或专有 API。任何支持加载 Skills 的 Agent，都可以按其平台要求安装和使用。

它不会只给出结论，而会引导学习者理解：

- 为什么事情会发生；
- 哪些变量真正重要，它们如何相互作用；
- 一个规律在什么条件下成立或失效；
- 结论有什么证据、反例和不确定性；
- 同一套思维能迁移到哪些新问题。

## 安装

### 方法一：使用 Git 克隆

```bash
git clone https://github.com/Mdboer18/world-cognition.git <AGENT_SKILLS_DIR>/world-cognition
```

将 `<AGENT_SKILLS_DIR>` 替换为你的 Agent 所使用的 Skills 目录。具体目录位置和刷新方式请参考对应 Agent 的说明；部分 Agent 需要重新启动或开启新会话后才会加载新 Skill。

### 方法二：下载 ZIP

在 GitHub 或 Gitee 仓库页面点击“下载 ZIP”，解压后将整个 `world-cognition` 文件夹放入 Agent 的 Skills 目录：

```text
<AGENT_SKILLS_DIR>/world-cognition
```

安装后的目录应满足：

```text
<AGENT_SKILLS_DIR>/world-cognition/SKILL.md
```

不要在 `world-cognition` 外再多嵌套一层同名目录。

## 使用

如果 Agent 支持显式 Skill 调用，可以使用：

```text
使用 $world-cognition 和我讨论：为什么城市会形成？
```

如果 Agent 支持自动发现 Skills，也可以直接提出适合探究的问题，例如：

- 为什么货币会有价值？
- 为什么不同文明会发展出不同制度？
- 人工智能为什么会产生“幻觉”？
- 为什么人容易拖延？

当一次讨论形成较完整的理解后，可以让它生成“认知卡片”；积累多张卡片后，还可以进行阶段或月度复盘。

## 目录结构

```text
world-cognition/
├── SKILL.md
├── agents/
├── prompts/
├── rules/
└── templates/
```

- `SKILL.md`：Skill 入口与工作模式
- `agents/openai.yaml`：部分 Agent 可识别的可选界面元数据；不影响其他平台加载 `SKILL.md`
- `prompts/`：导师对话、认知卡片和月度复盘提示
- `rules/`：苏格拉底式教学、年龄适配和知识关联规则
- `templates/`：认知卡片与世界认知地图模板

## 兼容性

- 入口文件采用通用的 `SKILL.md` 与 YAML Front Matter。
- Skill 内容由 Markdown 文件组成，不依赖特定模型或工具调用。
- 不同 Agent 对 Skills 的目录位置、显式调用语法和自动发现机制可能不同，请以所用平台的文档为准。
- 平台无法识别的可选元数据文件可以被安全忽略。

## 适用边界

这个 Skill 适合值得推理和讨论的问题。普通寒暄、操作指令、紧急问题，或用户明确只需要简短事实答案时，不会强行启动完整教学流程。

## 许可证

本项目采用 [MIT License](LICENSE)。
