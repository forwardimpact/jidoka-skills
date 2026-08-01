# Jidoka Skills

Skills that maintain the [Jidoka](https://github.com/forwardimpact/monorepo/blob/main/JIDOKA.md) instruction architecture with the `jidoka` CLI (install it with `npx @forwardimpact/jidoka` or the platform bootstrap). This pack was renamed from `coaligned-skills`. To migrate, run `git mv .coaligned .jidoka`. Reinstall this pack. Swap the CLI name.

## Install

With [APM](https://microsoft.github.io/apm/):

```bash
apm install forwardimpact/jidoka-skills
```

## Available Skills

| Skill | Description |
| --- | --- |
| **jidoka-audit** | Run the full Jidoka check suite and act on what it finds. Use for a periodic instruction-quality health check, when CI reports a `jidoka` failure, or before a release. Triage every finding and route it to the fix that owns it. |
| **jidoka-invariant** | Author a declarative invariant rule module for `jidoka invariants`. Use when a repository needs to enforce its own architectural rule. Examples are a forbidden import, a value that must agree across files, and a directory shape. Write it as a `.jidoka/invariants/*.rules.mjs` module the CLI discovers and runs. |
| **jidoka-jtbd** | Author and maintain Jobs To Be Done entries for the Jidoka standard. Use when you write a Big Hire or Little Hire, when you add a `<job>` tag, when `package.json .jobs` blocks are stale, or when `jidoka jtbd` reports a schema or freshness failure. |
| **jidoka-layer** | Author or repair an instruction layer to the Jidoka standard. A layer is an agent profile, agent reference, SKILL.md, skill reference, or checklist. Use when you add an agent or skill, when `jidoka instructions` flags a length breach, or when one layer restates another. |
| **jidoka-setup** | Bootstrap the Jidoka instruction architecture in a repository. Use when a repo has no layered agent instructions yet. Use when you adopt the Jidoka standard. Use when you wire the `jidoka` checks into the repository. The line then stops the moment a layer drifts, a job goes stale, or an invariant breaks. |
