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
| **[policydesk](https://github.com/FishRaposo/policydesk)** | Policy sandbox with deterministic refund rules, synthetic replay, simulated approvals, and opt-in local OpenAI testing. | [Synthetic reports](https://github.com/FishRaposo/policydesk/tree/main/reports) · [offline sandbox](https://fishraposo.github.io/policydesk/) · [local OpenAI setup](https://github.com/FishRaposo/policydesk#try-openai-locally-with-your-own-key) |
| **[llm-gateway](https://github.com/FishRaposo/llm-gateway)** | LLM proxy with routing, guardrails, atomic per-key budgets, and failover across OpenAI, Anthropic, Gemini, and Ollama. | 177 backend + 41 dashboard tests |

Also: **[agenttrace](https://github.com/FishRaposo/agenttrace)**, the tracing SDK, collector and dashboard, remains in the [catalog](https://fishraposo.github.io/projects/agenttrace.html).

These are portfolio systems with sample data. PolicyDesk supports local OpenAI testing with your own key; its public sandbox remains offline with synthetic data. OpenAI integration implemented; live verification and empirical results not yet performed. No model or financial backend is hosted. Each project page has its walkthrough and verified results. Full catalog: [fishraposo.github.io/projects.html](https://fishraposo.github.io/projects.html).

## Games

The first code I ever wrote was a game mod, at 11. Gaming led to modding, modding led to ROM hacking and reverse engineering, and that led to game development proper. Thousands of hours across design theory and building, none of it professional yet. This section is the bridge.

**How I got here**
- **Modding first.** Tweaking other people's games is how I learned to program, and I still build mods: [material-progression](https://github.com/FishRaposo/material-progression) rebuilds Minecraft's progression around geology, metallurgy and workshops, because that's the game I wanted to play (NeoForge, Java; local 0.2.0 release candidate).
- **ROM hacking and reverse engineering.** My own ROM hacks and the tooling to make them. The same skill set sits under my agent-scaffolding benchmark, which reverse-engineers NDS ROMs with byte-level verification (see Writing below).
- **Engines.** Unity, Godot and Unreal, mostly prototyping and learning each one's way of doing things.
- **Theory.** *Level Up!* and other design books, courses, and a lot of developer channels. Portal is the game I've studied most closely, front to back.

**What I believe**
- A game is a business from the first day. Monetization and marketing get designed in from the start; bolted on at the end, they don't work.
- Use every tool available, AI above all. The games below were built with AI assistance to my brief, and each one is tested like production software.
- Genre is not a wall. I can talk design from MMORPGs to life sims to puzzle games, and the systems underneath (progression, economies, combat, procedural generation) carry across.

**What I bring:** game design and systems, the code that implements them, and the test design that proves they work. I'm not a visual artist: my games use code-drawn and AI-generated art and asset packs, and I've worked with human artists before.

**Built for game-dev roles**

Three small games, each built to be broken on purpose. Every one ships a task pack: planted gameplay bugs and feature requests, each with a brief, acceptance criteria (input sequence, expected visual outcome, verifiable game state), a reference solution and an automated check that fails on the starting state and passes on the solution.

<table>
<tr>
<td width="33%" valign="top"><a href="https://fishraposo.github.io/projects/recall.html"><img src="https://fishraposo.github.io/images/portfolio/recall-demo.gif" alt="Recall: the blade flies out, cuts through enemies and curves back"></a></td>
<td width="33%" valign="top"><a href="https://fishraposo.github.io/projects/wick.html"><img src="https://fishraposo.github.io/images/portfolio/wick-demo.gif" alt="Wick: lantern light on a procedurally generated floor"></a></td>
<td width="33%" valign="top"><a href="https://fishraposo.github.io/projects/thaw.html"><img src="https://fishraposo.github.io/images/portfolio/thaw-demo.gif" alt="Thaw: a crate kicked into water becomes a bridge to the hut"></a></td>
</tr>
<tr>
<td align="center"><a href="https://fishraposo.itch.io/recall"><b>▶ Play Recall on itch.io</b></a></td>
<td align="center"><a href="https://fishraposo.itch.io/wick"><b>▶ Play Wick on itch.io</b></a></td>
<td align="center"><a href="https://fishraposo.itch.io/thaw"><b>▶ Play Thaw on itch.io</b></a></td>
</tr>
</table>

| Repo | What it is | Evidence |
|---|---|---|
| **[recall](https://github.com/FishRaposo/recall)** | Arcade action: one throwing blade that always comes back; catching it after a hit raises your multiplier. Hitstop, screen shake, input buffering, synthesized sound. | 18 unit tests; [task pack](https://github.com/FishRaposo/recall/tree/main/tasks) of 4 bugs + 2 features, each verified fail → pass in headless Chromium |
| **[wick](https://github.com/FishRaposo/wick)** | Turn-based roguelike where lantern oil is your field of view: procedural floors, shadowcasting, Dijkstra-map AI (moths chase the light, shades flee it, hounds hunt by sound). | 18 unit tests incl. connectivity over 1,800 generated floors; [task pack](https://github.com/FishRaposo/wick/tree/main/tasks) of 2 bugs + 1 feature |
| **[thaw](https://github.com/FishRaposo/thaw)** | Ice-sliding puzzle game in twelve rooms, with a breadth-first solver that proves every one. | 19 unit tests, all 12 levels re-solved at par each run; [task pack](https://github.com/FishRaposo/thaw/tree/main/tasks) of 2 bugs + 1 feature |

Also: [game-systems-sandbox](https://github.com/FishRaposo/game-systems-sandbox), a portfolio piece of seeded Monte Carlo balance simulators. All three play in the browser on [itch.io](https://fishraposo.itch.io); everything else: [fishraposo.github.io/#games](https://fishraposo.github.io/#games).

I'm open to game-dev evaluation and task-design work (training and testing AI on game development), game design roles, and building my own games.

## Before

**Founding Engineer, Zap Viagens** (Jun – Oct 2026). Built privacy-first AI products for service businesses on self-hosted open-source models, designed so customer data stays on owned infrastructure.

**AI Lead, Expat Money** (Jun 2022 – Nov 2025). Created and led the AI function from zero. Cut AI-for-content costs 90% — replaced a $200/month tool with a $20/month one — and halved content production time. Built grounded retrieval for cross-jurisdiction expat planning — a domain where wrong answers have real consequences.

## Writing

**[Taste Is All You Need](https://x.com/FishRaposo/status/2080404528692924696)** — long-form analysis of agent-harness economics: why scaffolding beats model spend. Backed by a personal agent-scaffolding benchmark reverse-engineering NDS ROMs with byte-level verification: frontier models score 6–8/10 unaided with high variance; under my spec/skill scaffolding, 10/10 with zero variance.

## Links

[Portfolio](https://fishraposo.github.io) · [X](https://x.com/FishRaposo) · [Upwork](https://www.upwork.com/freelancers/~01ca94c53d0d0101f3) · fishraposo@gmail.com

Send me what you're tired of babysitting. I'll tell you specifically what's wrong before you spend a dollar.

<sub>Last updated: 2026-10-28</sub>
