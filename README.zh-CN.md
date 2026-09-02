[English](README.md) | [简体中文](README.zh-CN.md)

# 证据驱动的科研论文写作方法

一套可复用的科研写作方法，用于把研究材料转化为与现有证据强度相匹配的科学论述。

本仓库提供以证据为中心的科研写作方法，以及一个可复用的 Codex Skill。它帮助研究者将已有结果组织成可检验、可追溯且边界清晰的论证，避免用修辞夸大结论。

## 适用场景

当你需要完成以下任务时，可以使用这些方法：

- 将观察、分析、实验和图表组织为连贯的论文论证；
- 区分观察事实、研究假设和已有证据支持的解释；
- 在确定论文叙事前检验相互竞争的解释；
- 让每项主张的强度与实际证据相匹配；
- 在修改过程中保留数值、引用、条件、比较关系和不确定性；
- 根据任务选择最小但有用的输出，从图注到章节规划均可。

典型用途包括论文构思、Results 章节修改、图表驱动的叙事、审稿回复前自检，以及研究团队内部的论证一致性检查。

## 仓库结构

```text
.
├── README.md                         # 英文文档
├── README.zh-CN.md                   # 简体中文文档
├── WRITING_TECHNIQUES.md             # 面向个人和团队的独立写作指南
├── LICENSE                           # 文字与模板采用 CC BY 4.0 许可
└── skills/
    └── evidence-led-paper-writing/   # Codex Skill 软件包
```

## 安装 Codex Skill

1. 克隆或下载本仓库。
2. 将 `skills/evidence-led-paper-writing` 复制到 Codex 环境配置的 `skills` 目录。
3. 如果 Codex 没有自动识别新 Skill，请重新启动或重新加载 Codex。
4. 在请求中使用 Skill 名称调用，例如：“使用 `$evidence-led-paper-writing` 审查这个 Results 章节。”

如果通过命令行安装，请先将 `CODEX_HOME` 设置为 Codex 主目录，然后在仓库根目录执行以下任一命令。

PowerShell：

```powershell
New-Item -ItemType Directory -Force "$env:CODEX_HOME\skills\evidence-led-paper-writing" | Out-Null
Copy-Item -Recurse -Force .\skills\evidence-led-paper-writing\* "$env:CODEX_HOME\skills\evidence-led-paper-writing\"
```

Bash：

```bash
mkdir -p "$CODEX_HOME/skills/evidence-led-paper-writing"
cp -R skills/evidence-led-paper-writing/. "$CODEX_HOME/skills/evidence-led-paper-writing/"
```

如果你的 Codex 使用其他托管 Skill 路径，请改用相应路径。目标文件夹名称应保持为 `evidence-led-paper-writing`。

## 示例提示词

```text
使用 $evidence-led-paper-writing 将这些实验记录转换为
“问题 → 可检验主张 → 方法 → 证据 → 适用范围”映射，并标出所有缺失环节。
```

```text
使用 $evidence-led-paper-writing 审查这个 Results 章节。分别标出观察事实、
研究假设和证据支持的解释；不要虚构结果、数值、实验或引用。
```

```text
针对这张图和图注，说明每个面板承担的证明责任、它排除的替代解释，
以及仍然存在的一项局限。
```

```text
保守地改写这个段落。保留所有数值、引用、条件、比较关系和不确定性；
弱化任何缺少直接证据支持的主张。
```

```text
基于现有结果，提出信息量足够但成本最小的下一项验证。
说明它能够区分哪些竞争解释，以及阳性和阴性结果分别意味着什么。
```

## 核心方法

核心论证链条是：

> 问题 → 可检验主张 → 方法 → 证据 → 适用范围

在每个环节都应检查后一项陈述是否能够从前面的证据中推出，并明确区分三类陈述：

- **观察事实：** 实际测量到或直接看到的内容。
- **研究假设：** 尚待检验的一种可能解释。
- **证据支持的解释：** 由特定证据支持的解释，同时说明替代解释和适用边界。

配套指南 [WRITING_TECHNIQUES.md](WRITING_TECHNIQUES.md) 提供了进一步的检查清单、模板和示例。

## 使用边界

这些材料用于辅助推理和修改，但不能替代科学真实性验证。请勿使用它们：

- 虚构结果、样本量、引用、研究方法或统计证据；
- 隐瞒不确定性、阴性结果、方案偏差或相互冲突的证据；
- 在研究设计和分析不足以支持因果结论时，将相关性表述为因果关系；
- 替代领域专家判断、伦理审查、数据治理或合作者审阅；
- 复制受版权保护的文本，或把未经审核的生成内容当作科学证据。

作者仍须对来源核验、分析有效性、作者署名以及对期刊、会议和所在机构要求的遵守承担责任。

## 参与贡献

欢迎提交能够让这些方法更清晰、更可检验或更容易跨学科使用的贡献。

提交 Pull Request 前，请确保：

1. 示例为合成内容、已匿名化内容或明确允许复用的内容。
2. 说明修改改善了“证据—主张”链条中的哪个环节。
3. 保留不确定性，不引入缺少证据支持的方法建议。
4. 优先提交规模小、便于审阅的修改；适用时提供明确的修改前后对比。
5. 确保新增文字和模板可以按照本仓库的许可证共享。

对于较大的修改建议，请先创建 Issue，说明写作问题、预期用户结果和最小示例。

## 许可证

本仓库的文字与可复用模板采用 [CC BY 4.0](LICENSE) 许可。
