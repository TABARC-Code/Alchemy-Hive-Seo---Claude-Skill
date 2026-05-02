# Description — Alchemy Hive SEO Skill

**Version:** 1.0  
**Author:** TABARC-Code
**Written** for Blackwood Studio
**Compatible with:** Claude (claude-sonnet-4-20250514 and later)  
**Language:** UK English

---

## What this is

A Claude skill system for organic search strategy. Thirty-one files. Four conceptual layers. One persistent memory file that survives across sessions.

The core argument is that most SEO practice fails not because people don't know about title tags and backlinks, but because they're trying to be rational in a system where the winning moves are frequently irrational. Sutherland's *Alchemy* makes this case at length. This skill operationalises it.

Three frameworks are fused into a single working system:

**Sutherland's Alchemy model** — Ok I am  fan  the idea that psychological value and logical value are different things, and that small, apparently trivial interventions can have disproportionate effects. Relevant protocols: Costly Signal, Trivia Amplifier, Hidden Intent, Adaptive Preference.

**The Bee Colony model** — a page role aof Rory Sunderland: Assignment framework. Every page on a site has a job. Scout pages test unknowns. Follower pages exploit proven demand. Memory assets hold accumulated trust. Outlier pages do things the rest of the SERP won't. Pages without roles are passengers.

**Outlier SEO practice** — information architecture, hidden intent analysis, entity-first thinking, anti-fragility design. The counterfactual content test (would the information landscape be meaningfully different without this page?) is the publishing gate. Everything goes through it before it goes live.

---

## What's included

### Core infrastructure

`SKILL.md` is the master router. It classifies every incoming request and dispatches it to the right skill or skill chain. It also enforces session start and close protocols — memory is read at the start of every session, written at the end. Nothing falls through the gaps.

`memory/memory.md` is the persistent state file. It holds every active experiment, page role assignment, protocol application, and pending review date. It's the single source of truth for what the system knows about a site. Updated by every skill on every write operation.

`core/colony-core.md` defines ten determinate invariants — C1 through C10 — that every page must pass regardless of its role. Reachability, canonical declaration, indexability, mobile parity, structured data integrity, page experience, user problem statement, information gain, trust signals, internal link purpose. Not negotiable, not subject to experimentation.

`core/measurement-architecture.md` provides a five-dimension measurement model: visibility, cognitive friction, trust, adaptive gain, anti-fragility.

### Page roles

Four role files govern the full lifecycle of a page — from initial assignment through optimisation cycles to reclassification or retirement. Each role file includes full setup procedures, refresh triggers, success metrics, demotion and graduation criteria, and explicit bidirectional link contracts with every skill it touches.

### Intelligence

`intelligence/waggle-dance.md` handles structured demand signal research: standard keyword tool scan, SERP landscape analysis, gap identification, and anti-waggle extension. It chains directly into `alchemy/anti-waggle-dance.md` for non-tool signal sourcing — Reddit, Amazon reviews, competitor Q&A, PAA clusters, YouTube autocomplete, SERP volatility patterns.

`intelligence/counterfactual-test.md` is the four-question publishing gate. A page must pass all four questions — or it doesn't go live.

### Alchemy protocols

Seven protocols, each covering a specific problem type. The alchemy router selects the appropriate one based on context, or accepts a named protocol directly.

| Protocol | Problem it addresses |
|---|---|
| Expectation Architecture | Snippet promise doesn't match the page's opening experience |
| Hidden Intent | The query is about anxiety, not information |
| Costly Signal | The page looks untrustworthy compared to competitors |
| Trivia Amplifier | Small framing or structural change with disproportionate expected effect |
| Logic-Proof Detector | The page has been technically correct for months and still doesn't move |
| Anti-Waggle-Dance | Demand that isn't in any keyword tool yet |
| Adaptive Preference | The site is second, new, or free-tier — and people resent it |

### Audit system

`audit/site-audit.md` is a six-phase full site audit: page inventory, colony-core validation, SERP landscape scan, anti-waggle research, role assignment, and measurement baseline. Output goes to the audit report template and memory.

`audit/feedback-loops.md` handles all role transitions — Scout 90-day reviews, Outlier 120-day reviews, Memory 6-month audits, Follower SERP drift detection. It also manages the propagation rules: what happens when an experiment wins or fails, and how that result changes the system's behaviour going forward.

### TABARC-Code

`agents/tabarc-code.md` is the technical programmer persona. When an audit produces a technical fail or a protocol produces an implementation requirement, TABARC-Code handles the code. It covers the full C1–C6 technical stack: redirect chains, canonical implementation, robots.txt, XML sitemaps, structured data (JSON-LD only — Article, FAQPage, HowTo, BreadcrumbList), Core Web Vitals (LCP, CLS, INP), and internal link anchor text auditing.

It asks one question if the CMS or tech stack is unknown before producing code. Stack-agnostic output is usually wrong output.

### Templates

Four output templates: `page-role.yaml` (role assignment schema), `scout-brief.md`, `audit-report.md`, `trivia-log.md`.

---

## Design decisions worth noting

**Bidirectional link contracts** are declared in YAML front matter on every skill file. When A calls B, B explicitly acknowledges A. When a chain runs A → B → C → D, all four files declare the chain. Reverse flows — failure feedback, negative learning signals — are named and documented. The system cannot develop silent dependencies.

**Named failure reasons** exist for every retirement and demotion path. A Scout doesn't just fail — it fails for a specific, categorised reason that feeds back into the skill that generated it. `no-demand` failures modify waggle-dance heuristics. `protocol-wrong` failures write back to the alchemy protocol file. The system builds a failure vocabulary rather than burying the evidence.

**Skill versioning** is procedure-level, not cosmetic. A version number increments when a procedure actually changes. The reason is logged in memory. This is partly discipline and partly useful — when something starts working differently than expected, there's a record of what changed and when.

**The counterfactual test is mandatory.** Even for Outlier pages, which exist specifically to be unconventional. An unusual page that adds nothing is just an unusual page that adds nothing. The gate applies regardless of how creative the strategy.

---

## What this is not

What it does not do: autonomous spidering — it doesn't follow links across a site, build a URL graph, or discover pages by itself. It requires you to bring the page list from a sitemap, GSC export, or a dedicated crawler like Screaming Frog.
What it does do: once it has that list, it processes every page through the colony-core checklist, can make live HTTP requests to individual URLs (canonical headers, status codes, anchor text), and runs the waggle-dance signal scan across the site's topic space.
The DESCRIPTION.md line "It doesn't crawl your site" is technically accurate in the spidering sense, but it's misleading — it implies more passivity than is real. Something like:

**You need to provide a
a sitemap Url to maximse the seo effects. Its not a bug but  awork aroud with Claude Skills.

"It doesn't spider your site autonomously — bring it a sitemap or GSC export and it will work through every page. TABARC-Code makes live HTTP requests to individual URLs for canonical, status code, and anchor text checks."
Most SEO documents stop at the recommendation layer. That's where most of the value gets lost.

---

*Alchemy Hive SEO Skill — Designed for Blackwood Studio*
