# Evidence-Led Paper Writing Techniques

Reusable techniques for turning research material into scientific prose whose claims are proportional to its evidence.

本仓库提供一套可复用的、以证据为中心的科研论文写作方法，以及一个可在 Codex 中使用的技能包。它帮助作者把“已有结果”组织成可检验、可追溯、边界清晰的论证，而不是把写作变成对结论的修辞放大。

## What this repository is for | 适用场景

Use these techniques when you need to:

- turn observations, analyses, experiments, and figures into a coherent paper argument;
- distinguish what was observed from what is hypothesized or explained;
- test competing explanations before committing to a narrative;
- calibrate a claim to the evidence actually available;
- preserve reported numbers, citations, qualifiers, and uncertainty during revision; and
- choose the smallest useful writing output, from a figure caption to a section plan.

适合用于论文构思、结果段改写、图表叙事、审稿回复前自检，以及团队内部的论证一致性检查。

## Repository layout | 仓库结构

```text
.
├── README.md                         # Project overview and usage
├── WRITING_TECHNIQUES.md             # Standalone guide for people and teams
├── LICENSE                           # CC BY 4.0 for prose and templates
└── skills/
    └── evidence-led-paper-writing/   # Codex skill package
```

## Install the Codex skill | 安装 Codex 技能

1. Clone or download this repository.
2. Copy `skills/evidence-led-paper-writing` into the `skills` directory configured for your Codex environment.
3. Restart or reload Codex if your environment does not detect new skills automatically.
4. Invoke it by name in a request, for example: “Use `$evidence-led-paper-writing` to audit this Results section.”

For a shell-based installation, set `CODEX_HOME` to your Codex home directory, then run one of the following from the repository root:

```powershell
New-Item -ItemType Directory -Force "$env:CODEX_HOME\skills\evidence-led-paper-writing" | Out-Null
Copy-Item -Recurse -Force .\skills\evidence-led-paper-writing\* "$env:CODEX_HOME\skills\evidence-led-paper-writing\"
```

```bash
mkdir -p "$CODEX_HOME/skills/evidence-led-paper-writing"
cp -R skills/evidence-led-paper-writing/. "$CODEX_HOME/skills/evidence-led-paper-writing/"
```

If your Codex setup uses a different managed skill location, use that location instead. The destination folder should retain the package name `evidence-led-paper-writing`.

## Example prompts | 示例提示词

```text
Use $evidence-led-paper-writing to convert these experiment notes into a
problem → testable claim → method → evidence → scope map. Flag every missing link.
```

```text
请使用 $evidence-led-paper-writing 审查这段 Results：分别标出观察事实、
假设和被证据支持的解释；不要补造实验、数值或引用。
```

```text
For this figure and caption, state the proof responsibility of each panel,
the alternative explanation it addresses, and one residual limitation.
```

```text
Rewrite this paragraph conservatively. Preserve all numbers, citations,
conditions, comparisons, and uncertainty; weaken any claim not directly supported.
```

```text
基于现有结果，给出最小但有信息量的下一步验证：说明它区分哪些竞争解释，
以及阳性和阴性结果各意味着什么。
```

## Core practices | 核心原则

The central chain is:

> problem → testable claim → method → evidence → scope

At every link, ask whether the next statement follows from the preceding evidence. Keep three kinds of statements distinct:

- **Observation:** what was measured or directly seen.
- **Hypothesis:** a proposed account that remains open to testing.
- **Supported explanation:** an interpretation favored by specified evidence, with alternatives and limits stated.

The companion guide, [WRITING_TECHNIQUES.md](WRITING_TECHNIQUES.md), expands these practices into checklists, templates, and examples.

## Boundaries | 使用边界

These materials support reasoning and revision; they do not validate scientific truth. They should not be used to:

- invent results, sample sizes, citations, methods, or statistical support;
- conceal uncertainty, negative results, protocol deviations, or conflicting evidence;
- turn correlation into causation without a warranted design and analysis;
- replace domain expertise, ethics review, data governance, or coauthor review; or
- reproduce copyrighted text or pass generated prose off as unreviewed evidence.

Authors remain responsible for source checking, analytical validity, authorship, and compliance with their venue and institution.

## Contributing | 贡献方式

Contributions are welcome when they make the techniques clearer, more testable, or easier to apply across fields.

Before opening a pull request:

1. Keep examples synthetic, anonymized, or explicitly reusable.
2. State which part of the evidence-to-claim chain the change improves.
3. Preserve uncertainty and do not introduce unsupported methodological advice.
4. Prefer a small, reviewable change with a concrete before/after example when useful.
5. Ensure prose and templates can be shared under this repository's license.

For substantial proposals, open an issue first with the writing problem, the intended user outcome, and a minimal example.
