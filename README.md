# skills

Agent skills, installable with [`npx skills`](https://skills.sh).

## deslop

Detect or rewrite text that reads as AI-generated, without overcorrecting it into flat, voiceless prose.

Synthesized from the top anti-slop/humanizer skills on skills.sh (stop-slop, no-ai-slop, humanizer, unslop, slopbeth, deslop, anti-slop, humanize, anti-ai-slop-writing) plus current research on AI writing tells. Covers prose/writing — not a code-quality tool.

```bash
npx skills add yawbtng/skills --skill deslop
```

See [`skills/deslop/SKILL.md`](skills/deslop/SKILL.md) for the full instructions and [`skills/deslop/references/`](skills/deslop/references/) for the pattern catalog, current word-tell list, structural checks, and scoring rubric it draws on.

## eng

Unified engineering workflow orchestrator. Auto-detects your current phase (discover, plan, build, verify, ship, learn) from git state, todos, and recent docs, and routes to the right sub-skill — no need to remember which one to call.

**Requires two other plugins to actually run:** [gstack](https://github.com/search?q=gstack+cli) (`/gstack:plan-ceo-review`, `/gstack:plan-eng-review`, `/gstack:review`, `/gstack:ship`, `/gstack:retro`) and Compound Engineering (`/workflows:brainstorm`, `/workflows:plan`, `/workflows:work`, `/workflows:review`, `/workflows:compound`). Without both, phases that invoke their sub-skills will fail. If you don't have them, the phase-detection logic and decision tree are still a useful reference for building your own orchestrator around different workflow skills.

```bash
npx skills add yawbtng/skills --skill eng
```

See [`skills/eng/SKILL.md`](skills/eng/SKILL.md) for the full phase-detection logic and decision tree.

## for-yourname-doc

Writes (or updates) a `FOR_[NAME].md` — a single, plain-language project doc aimed at one specific person, not a README or API reference. Covers what the project does, a "big picture" analogy for how it fits together, technical architecture, tech choices and why, and — the distinctive part — real bugs, pitfalls, and lessons from the project, so it doubles as onboarding and a post-mortem.

```bash
npx skills add yawbtng/skills --skill for-yourname-doc
```

See [`skills/for-yourname-doc/SKILL.md`](skills/for-yourname-doc/SKILL.md) for the required sections and tone guide, and [`skills/for-yourname-doc/reference.md`](skills/for-yourname-doc/reference.md) for a fill-in-the-blank section outline.
