# Alchemy Hive SEO Skill

A Claude skill system for SEO strategy that's simultaneously policy-governed and psychologically literate. Three source frameworks fused into one: Sutherland's *Alchemy* model, the Bee Colony page-role model, and Outlier SEO practice. A living search ecology with persistent memory across sessions.

Not a checklist. Not a content calendar. Not another plugin that tells you your title tag is too long.

---

## What it actually does

Most SEO tooling is built on the assumption that search is a logical system — optimise the right variables, get the right output. Sutherland's core argument, and the premise this skill is built on, is that search isn't logical. Users aren't logical. The systems that win are the ones that understand what people *actually* want, which is often quite different from what they type.

Alchemy Hive structures that insight into a working practice:

**Colony roles** assign every page a strategic function. A Scout page tests an unknown before the site commits to it. A Follower page exploits validated demand with maximum reliability. A Memory asset preserves accumulated trust and link equity that would be expensive to rebuild. An Outlier page does something the rest of the SERP is too rational to try. Pages don't just exist — they have jobs.

**Seven Alchemy Protocols** handle the situations where doing the logical thing has already failed: Expectation Architecture (snippet-to-page gap), Hidden Intent (anxiety-first framing), Costly Signal (trust through investment), Trivia Amplifier (small high-leverage interventions), Logic-Proof Detector (non-logical escalation for stuck pages), Adaptive Preference (reframing a second-best position), and Anti-Waggle-Dance (demand signals outside the keyword tools).

**Waggle-dance research** surfaces signals that the standard keyword tools miss entirely — Reddit anxiety patterns, Amazon review language, PAA clusters, SERP volatility, YouTube autocomplete — and feeds them into the scout briefing system.

**TABARC-Code** is the technical programmer persona built into the skill. Audit findings don't just produce recommendations; they produce working code. Structured data schemas, Core Web Vitals fixes, canonical implementation, robots.txt, redirect chain resolution — the implementation queue is part of the output. A bit of conceit but yup.

**Persistent memory** tracks every experiment, page role assignment, protocol application, and review deadline across sessions. Nothing gets lost between conversations. Scout 90-day reviews and Outlier 120-day reviews are logged at deployment and flagged when they come due.

---

## Repo structure

```
alchemy-hive-seo/
├── SKILL.md                          master router — entry point for all requests
├── DESCRIPTION.md
├── README.md
├── CHANGELOG.md
├── memory/
│   └── memory.md                     persistent state — every skill reads and writes here
├── core/
│   ├── colony-core.md                C1–C10 determinate invariants
│   └── measurement-architecture.md   five-dimension measurement model
├── roles/
│   ├── scout-bee.md                  discovery page role
│   ├── follower-bee.md               exploitation page role
│   ├── memory-bee.md                 legacy asset role
│   └── outlier-bee.md                controlled deviation role
├── alchemy/
│   ├── alchemy-router.md             protocol selector
│   ├── expectation-architecture.md   pre-click to on-page gap management
│   ├── hidden-intent.md              anxiety-first content framing
│   ├── costly-signal.md              trust through investment signals
│   ├── trivia-amplifier.md           high-leverage small interventions
│   ├── logic-proof-detector.md       non-logical escalation for stuck pages
│   ├── anti-waggle-dance.md          demand signals outside the keyword tools
│   └── adaptive-preference.md        second-best position reframing
├── intelligence/
│   ├── waggle-dance.md               structured research and signal gathering
│   └── counterfactual-test.md        publishing gate — four-question test
├── audit/
│   ├── site-audit.md                 full site audit procedure
│   └── feedback-loops.md             propagation rules, role transitions, graduation
├── agents/
│   └── tabarc-code.md                technical programmer persona
└── templates/
    ├── page-role.yaml                page role assignment schema
    ├── scout-brief.md                brief template for new scout pages
    ├── audit-report.md               site audit output format
    └── trivia-log.md                 trivia amplifier experiment log
```

---

## Quick start

**Audit a site:** Send `audit [domain]` — the master router handles the chain from page inventory through role assignment to pending review calendar.

**Brief a scout page:** Send `scout [topic]` — the system runs waggle-dance research, anti-waggle extension, counterfactual gate, and produces a full brief with hypothesis and success signals.

**Apply an alchemy protocol directly:** Send `alchemy [protocol name or context]` — the alchemy router selects the appropriate protocol or accepts a named one.

**Generate technical implementation:** Send `implement [fix type]` or `structured data [page]` — TABARC-Code takes over and produces working code against your stack.

**Check system state:** Read `memory/memory.md` — it holds every active experiment, role assignment, and pending review date.

---

## Entrypoints

| Task | File |
|---|---|
| Full site audit | `audit/site-audit.md` |
| Brief a scout page | `roles/scout-bee.md` |
| Research demand signals | `intelligence/waggle-dance.md` |
| Apply an alchemy protocol | `alchemy/alchemy-router.md` |
| Publishing gate | `intelligence/counterfactual-test.md` |
| Trivial intervention testing | `alchemy/trivia-amplifier.md` |
| Diagnose a stuck page | `alchemy/logic-proof-detector.md` |
| Technical implementation | `agents/tabarc-code.md` |
| System state | `memory/memory.md` |

---

## Design principles

Every skill file declares its relationships explicitly in YAML front matter: what it calls, what calls it, what chains downstream, what flows upstream, what its lateral peers are. When A links to B, B holds an explicit reciprocal contract referencing A. This isn't casual documentation — it's a structured contract system that makes the information flow auditable and the skill boundaries clear.

Feedback travels in both directions. A Trivia Amplifier win propagates forward as site-wide policy. A Scout retirement with a named failure reason propagates back to modify waggle-dance heuristics. Outlier `protocol-wrong` failures write back to the relevant alchemy protocol file. The system learns from what doesn't work, not just what does.

Skill versions increment when a procedure changes. The cause is logged. Nothing updates silently.

---

*Alchemy Hive SEO Skill v1.0 — built for Claude (claude-sonnet-4-20250514)*
