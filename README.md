# Richman Chea · DnA Arkitecs

*"Defense & Attack — Attack Problems, Defend Peace"* · [dnaarkitecs.com](https://dnaarkitecs.com)

I'm an **AI Systems Architect and Forward-Deployed Builder**: I go into a business, find the bottleneck, and ship the system that removes it.
My work covers autonomous multi-agent harnesses, deterministic AI security, real-time GPU computer vision, and outcome-verified go-to-market infrastructure.
Everything below is open source, tested, and built so a stranger can run it in minutes.

**571 passing tests across 9 repos** (run 2026-11-20: agent-guard 175, gearbox 63, tripwire 33, rollcall-tally 44, person-key 41, landed 104, paytally 24, keysight 9, foundry 78).

## Flagship open source

| Repo | What it does | Domain |
|---|---|---|
| [**agent-guard**](https://github.com/DnA-Arkitecs/agent-guard) | Deterministic checks that sit between an AI agent and its tools: prompt-injection, path, secret and SQL guards that decide the same way every time. v1.1 folds zero-width, look-alike and Base64 tricks before judging | AI security |
| [**foundry**](https://github.com/DnA-Arkitecs/foundry) | A 7-station deterministic AI software factory: every station is a code gate, blind holdout scenarios are sealed by SHA-256, and every decision lands in a SQLite ledger. Agents propose files; only a gate says done | AI software delivery |
| [**gearbox**](https://github.com/DnA-Arkitecs/gearbox) | A multi-model harness that shifts work between models and agents, with every step recorded | Agent orchestration |
| [**tripwire**](https://github.com/DnA-Arkitecs/tripwire) | Pre-registered A/B experiments with circuit breakers: rules sealed with a SHA-256 fingerprint before the first send, tests halted the moment bounces or complaints say stop | Experiment integrity |
| [**rollcall-tally**](https://github.com/DnA-Arkitecs/rollcall-tally) | Attendance proof from video-call rosters: a meeting counts only if host and guest were in the room together, with name matching that survives messy display names | Outcome verification |
| [**person-key**](https://github.com/DnA-Arkitecs/person-key) | Stable keys for matching people across messy records, so one person is one entity | Entity resolution |
| [**keysight**](https://github.com/DnA-Arkitecs/keysight) | Phone camera in, GPU hand-skeleton HUD out, with a typing-form check. Trusted HTTPS to any phone through a Cloudflare tunnel, no certificate warning | Real-time computer vision |
| [**landed**](https://github.com/DnA-Arkitecs/landed) | Finds out why a cold email lands in spam and hands back the exact fix, using live DNS and blocklist lookups | Deliverability |

## agent-guard v1.1 red-team benchmark

> `python -m agent_guard --benchmark`: 50 hostile calls across 6 attack vectors, 40 realistic engineering calls, 18,000 timed decisions.
>
> | | |
> |---|---|
> | **50 / 50** | hostile calls blocked by the rule meant to catch them (injection exfiltration, destructive SQL, shell, credential theft, encoding evasion, scope escape) |
> | **0 / 40** | false positives on ordinary work (0.0%) |
> | **161 / 311 / 424 µs** | p50 / p95 / p99 decision latency, no model, no network |
>
> The README carries a threat-model boundary table: what a pre-execution guard catches in under half a millisecond, and what only tool scoping and isolation can stop.

## Production systems metrics

> Numbers from systems I run in production, anonymized.
>
> | | |
> |---|---|
> | **398** | production modules orchestrated across multi-model pipelines |
> | **21,370+** | tool executions guarded by deterministic checks |
> | **1.1M+** | entity records resolved at **91.6%** domain accuracy |

## How I build

- **Deterministic where it counts.** Models propose; code checks. Guards, verification and kill rules are plain code with tests.
- **Outcome over activity.** A job counts when its result is verified, not when it ran.
- **Never twice.** Every mistake an agent makes becomes a test or a gate, so the same failure cannot ship again.
- **Ship, measure, refine.** A working average version beats a perfect plan.

[dnaarkitecs.com](https://dnaarkitecs.com)
