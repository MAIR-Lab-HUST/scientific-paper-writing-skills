[English](README.md) | [简体中文](README.zh-CN.md)

# Evidence-Led Paper Writing Techniques

Reusable techniques for turning research material into scientific prose whose claims are proportional to the available evidence.

This repository provides an evidence-centered scientific writing methodology and a reusable Codex skill. It helps researchers organize existing results into testable, traceable, and properly scoped arguments without rhetorically overstating the conclusions.

## What this repository is for

Use these techniques when you need to:

- turn observations, analyses, experiments, and figures into a coherent paper argument;
- distinguish observations from hypotheses and supported explanations;
- test competing explanations before committing to a narrative;
- calibrate each claim to the evidence actually available;
- preserve numbers, citations, conditions, comparisons, and uncertainty during revision; and
- choose the smallest useful writing output, from a figure caption to a section plan.

Typical uses include paper planning, Results-section revision, figure-led storytelling, pre-rebuttal checks, and argument-consistency reviews within a research team.

## Repository layout

```text
.
├── README.md                         # English documentation
├── README.zh-CN.md                   # Simplified Chinese documentation
├── WRITING_TECHNIQUES.md             # Standalone guide for people and teams
├── LICENSE                           # CC BY 4.0 for prose and templates
└── skills/
    └── evidence-led-paper-writing/   # Codex skill package
```

## Install the Codex skill

1. Clone or download this repository.
2. Copy `skills/evidence-led-paper-writing` into the `skills` directory configured for your Codex environment.
3. Restart or reload Codex if your environment does not detect new skills automatically.
4. Invoke the skill by name, for example: “Use `$evidence-led-paper-writing` to audit this Results section.”

For a shell-based installation, set `CODEX_HOME` to your Codex home directory, then run one of the following commands from the repository root.

PowerShell:

```powershell
New-Item -ItemType Directory -Force "$env:CODEX_HOME\skills\evidence-led-paper-writing" | Out-Null
Copy-Item -Recurse -Force .\skills\evidence-led-paper-writing\* "$env:CODEX_HOME\skills\evidence-led-paper-writing\"
```

Bash:

```bash
mkdir -p "$CODEX_HOME/skills/evidence-led-paper-writing"
cp -R skills/evidence-led-paper-writing/. "$CODEX_HOME/skills/evidence-led-paper-writing/"
```

If your Codex setup uses a different managed skill location, use that location instead. Keep the destination folder name `evidence-led-paper-writing`.

## Example prompts

```text
Use $evidence-led-paper-writing to convert these experiment notes into a
problem → testable claim → method → evidence → scope map. Flag every missing link.
```

```text
Use $evidence-led-paper-writing to audit this Results section. Mark observations,
hypotheses, and evidence-supported explanations separately. Do not invent results,
numbers, experiments, or citations.
```

```text
For this figure and caption, state the proof responsibility of each panel,
the alternative explanation it addresses, and one residual limitation.
```

```text
Rewrite this paragraph conservatively. Preserve all numbers, citations,
conditions, comparisons, and uncertainty; weaken any unsupported claim.
```

```text
Given the current results, propose the smallest informative next test.
Explain which competing explanations it distinguishes and what positive
and negative outcomes would each mean.
```

## Core practices

The central chain is:

> problem → testable claim → method → evidence → scope

At every link, ask whether the next statement follows from the preceding evidence. Keep three kinds of statements distinct:

- **Observation:** what was measured or directly seen.
- **Hypothesis:** a proposed account that remains open to testing.
- **Supported explanation:** an interpretation favored by specified evidence, with alternatives and limits stated.

The companion guide, [WRITING_TECHNIQUES.md](WRITING_TECHNIQUES.md), expands these practices into checklists, templates, and examples.

## Boundaries

These materials support reasoning and revision; they do not validate scientific truth. Do not use them to:

- invent results, sample sizes, citations, methods, or statistical support;
- conceal uncertainty, negative results, protocol deviations, or conflicting evidence;
- turn correlation into causation without a warranted design and analysis;
- replace domain expertise, ethics review, data governance, or coauthor review; or
- reproduce copyrighted text or present generated prose as unreviewed evidence.

Authors remain responsible for source checking, analytical validity, authorship, and compliance with their venue and institution.

## Contributing

Contributions are welcome when they make the techniques clearer, more testable, or easier to apply across fields.

Before opening a pull request:

1. Keep examples synthetic, anonymized, or explicitly reusable.
2. State which part of the evidence-to-claim chain the change improves.
3. Preserve uncertainty and do not introduce unsupported methodological advice.
4. Prefer a small, reviewable change with a concrete before/after example when useful.
5. Ensure prose and templates can be shared under this repository's license.

For substantial proposals, open an issue first with the writing problem, the intended user outcome, and a minimal example.

## License

The prose and reusable templates in this repository are licensed under [CC BY 4.0](LICENSE).
