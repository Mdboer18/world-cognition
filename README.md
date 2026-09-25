# World Cognition · 世界认知导师

一个面向青少年和初学者的 Codex Skill，通过苏格拉底式对话、反例、证据与知识迁移，帮助学习者逐步建立跨自然、技术、经济、社会、历史和个人领域的世界认知体系。

它不会只给出结论，而会引导学习者理解：

- 为什么事情会发生；
- 哪些变量真正重要，它们如何相互作用；
- 一个规律在什么条件下成立或失效；
- 结论有什么证据、反例和不确定性；
- 同一套思维能迁移到哪些新问题。

## 安装

### 方法一：使用 Git 克隆

```bash
git clone https://github.com/Mdboer18/world-cognition.git ~/.codex/skills/world-cognition
```

安装后重新启动 Codex，或开启一个新会话。

### 方法二：下载 ZIP

在 GitHub 或 Gitee 仓库页面点击“下载 ZIP”，解压后将整个 `world-cognition` 文件夹放到：

```text
~/.codex/skills/world-cognition
```

确保目录内直接包含 `SKILL.md`，不要多嵌套一层同名目录。

## 使用

在 Codex 中可以直接说：

```text
使用 $world-cognition 和我讨论：为什么城市会形成？
```

也可以提出适合探究的问题，例如：

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
- `agents/openai.yaml`：Codex 展示与默认提示配置
- `prompts/`：导师对话、认知卡片和月度复盘提示
- `rules/`：苏格拉底式教学、年龄适配和知识关联规则
- `templates/`：认知卡片与世界认知地图模板

## 适用边界

这个 Skill 适合值得推理和讨论的问题。普通寒暄、操作指令、紧急问题，或用户明确只需要简短事实答案时，不会强行启动完整教学流程。

## 许可证

本项目采用 [MIT License](LICENSE)。

