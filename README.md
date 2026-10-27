# Vinícius Raposo — Fish

**AI systems you can leave on without babysitting.** Built for work where wrong answers are expensive.

Applied AI Reliability Engineer. You can stop watching a system when it checks itself: deterministic code decides before the model speaks, retrieval answers from your own data or refuses, risky actions wait for an approval bound to that exact action, and evals catch what quietly broke before it ships. Each piece ships with tests you can re-run, so "it still works" is something you check, not something you hope.

## What leaving it on looks like

Sample-data demos from the public repos. Click a screen for its walkthrough.

<table>
<tr>
<td width="50%" valign="top"><a href="https://fishraposo.github.io/projects/wcp-compliance-agent-v5.html"><img src="https://fishraposo.github.io/images/portfolio/wcp-decision.png" alt="WCP V5 audit station: a payroll rejected on three deterministic violations"></a><br><sub><b>Checks decide.</b> A WH-347 payroll rejected on three deterministic violations. The LLM explains; it can't approve what the checks didn't verify.</sub></td>
<td width="50%" valign="top"><a href="https://fishraposo.github.io/projects/groundtruth.html"><img src="https://fishraposo.github.io/images/portfolio/gt-refusal.png" alt="groundtruth refusing a question the corpus cannot support"></a><br><sub><b>It refuses.</b> A question the sources can't support gets an explicit refusal and a retrieval trace, not a guess.</sub></td>
</tr>
<tr>
<td width="50%" valign="top"><a href="https://fishraposo.github.io/projects/aria-agent.html"><img src="https://fishraposo.github.io/images/portfolio/aria-blocked.png" alt="ARIA blocking a prompt-injection attempt before any model call"></a><br><sub><b>It stops itself.</b> A prompt-injection attempt blocked before a single model call.</sub></td>
<td width="50%" valign="top"><a href="https://fishraposo.github.io/projects/evalforge.html"><img src="https://fishraposo.github.io/images/portfolio/eval-case.png" alt="evalforge failed retrieval case with judge scores"></a><br><sub><b>It tells you what broke.</b> An answer that looks right but cites the wrong evidence, failed before it ships.</sub></td>
</tr>
</table>

## What I help with

- **Coding agents you can let run.** Claude Code set up for your repo: project instructions, permissions, hooks that block what shouldn't happen and run your checks, MCP connections and guardrails.
- **AI-built apps that keep breaking in production.** A written audit of what breaks and what to fix first, then fixes, each with a test so it stays fixed.
- **RAG and agent systems that cite, refuse and hand off** instead of guessing, with evaluations that catch regressions.

Fixed prices and written scope, through [Upwork](https://www.upwork.com/freelancers/~01ca94c53d0d0101f3). Open to remote applied-AI roles (full-time or contract).

## Proof

Public, MIT-licensed, with tests you can run yourself. Each repo has a verification record that says what it proves and what it doesn't.

| Repo | What it does when nobody's watching | Evidence |
|---|---|---|
| **[WCP-Compliance-Agent-V5](https://github.com/FishRaposo/WCP-Compliance-Agent-V5)** | Five-service WH-347 payroll compliance platform: deterministic validation decides, the LLM explains, and unverified wage coverage goes to human review instead of approval. | 377 tests, including evals over 100 golden examples; checksum-verified evidence |
| **[groundtruth](https://github.com/FishRaposo/groundtruth)** | RAG application that cites every answer and refuses what its sources can't support: hybrid retrieval, versioned documents, human review. | 331 API + 62 web tests; real-HTTP workflow and restart checks |
| **[evalforge](https://github.com/FishRaposo/evalforge)** | Regression gate for RAG and agents that catches answers which look right but cite the wrong evidence, with pass / fail / indeterminate release exits. | 358 Python + 36 frontend tests |
| **[aria-agent](https://github.com/FishRaposo/aria-agent)** | Agent harness whose approvals bind the exact action, with execution tracing and a Claude Code setup fixture (permissions, blocking hooks, independent verifier). | 360 Python + 64 frontend tests |
| **[agenttrace](https://github.com/FishRaposo/agenttrace)** | Tracing SDK, collector and dashboard that find the failing step across concurrent AI workflows, with cost attribution. | 171 SDK + 124 collector + 41 dashboard tests |
| **[llm-gateway](https://github.com/FishRaposo/llm-gateway)** | LLM proxy with routing, guardrails, atomic per-key budgets, and failover across OpenAI, Anthropic, Gemini, and Ollama. | 177 backend + 41 dashboard tests |

These are portfolio systems with sample data, not hosted deployments. Each project page has its walkthrough and verified results. Full catalog: [fishraposo.github.io/projects.html](https://fishraposo.github.io/projects.html).

## Games

Games and game tools, built with the same habit: each one ships a way to check it.

<a href="https://fishraposo.github.io/projects/recall.html"><img src="https://fishraposo.github.io/images/portfolio/recall-demo.gif" alt="Recall: the blade flies out, cuts through enemies and curves back to the player" width="480"></a>

| Repo | What it is | Evidence |
|---|---|---|
| **[recall](https://github.com/FishRaposo/recall)** | Browser arcade game in plain JavaScript, no engine and no asset files: one throwing blade that comes back, five enemy types, synthesized sound. Ships a [task pack](https://github.com/FishRaposo/recall/tree/main/tasks): four planted gameplay bugs and two feature requests, each with a brief, acceptance criteria (input sequence, expected visual outcome, verifiable game state), a reference solution and a headless check. | 18 unit tests; every task check fails on its starting state and passes on its reference solution |
| **[material-progression](https://github.com/FishRaposo/material-progression)** | NeoForge Minecraft mod in Java rebuilding progression around geology, metallurgy and workshops, with the full design written alongside the code. | Local 0.2.0 release candidate; not yet a public release |
| **[game-systems-sandbox](https://github.com/FishRaposo/game-systems-sandbox)** | Seeded Monte Carlo simulators for combat, loot, XP and economy balance, with a dashboard that runs offline on demo data. | 173 Python tests; 56 root + 39 dashboard Vitest tests |

All three: [fishraposo.github.io/#games](https://fishraposo.github.io/#games).

## Before

**Founding Engineer, Zap Viagens** (Jun – Oct 2026). Built privacy-first AI products for service businesses on self-hosted open-source models, designed so customer data stays on owned infrastructure.

**AI Lead, Expat Money** (Jun 2022 – Nov 2025). Created and led the AI function from zero. Cut AI-for-content costs 90% — replaced a $200/month tool with a $20/month one — and halved content production time. Built grounded retrieval for cross-jurisdiction expat planning — a domain where wrong answers have real consequences.

## Writing

**[Taste Is All You Need](https://x.com/FishRaposo/status/2080404528692924696)** — long-form analysis of agent-harness economics: why scaffolding beats model spend. Backed by a personal agent-scaffolding benchmark reverse-engineering NDS ROMs with byte-level verification: frontier models score 6–8/10 unaided with high variance; under my spec/skill scaffolding, 10/10 with zero variance.

## Links

[Portfolio](https://fishraposo.github.io) · [X](https://x.com/FishRaposo) · [Upwork](https://www.upwork.com/freelancers/~01ca94c53d0d0101f3) · fishraposo@gmail.com

Send me what you're tired of babysitting. I'll tell you specifically what's wrong before you spend a dollar.

<sub>Last updated: 2026-10-27</sub>
