# Vinícius Raposo — Fish

**Applied AI Reliability Engineer.** I build the systems that work while you don't. Applied AI reliability: production RAG with citations and refusal, agents with tools, state, and guardrails, evaluation harnesses, and deterministic scaffolding around the model.

One design rule runs through all of it: the model never gets the final say. Deterministic code decides, the model explains, retrieval is grounded in your own data, and the system refuses when it can't back an answer. Each piece ships with a way to check it (tests, evals, traces), so you can see whether it still works after the next change. It matters most where a wrong answer costs money.

## Two minutes, three screens

Sample-data demos from the public repos. Click a screen for its walkthrough.

<table>
<tr>
<td width="33%" valign="top"><a href="https://fishraposo.github.io/projects/wcp-compliance-agent-v5.html"><img src="https://fishraposo.github.io/images/portfolio/wcp-decision.png" alt="WCP V5 audit station: a payroll rejected on three deterministic violations"></a><br><sub><b>Checks decide.</b> A WH-347 payroll rejected on three deterministic violations; the LLM explains, a human reviews.</sub></td>
<td width="33%" valign="top"><a href="https://fishraposo.github.io/projects/groundtruth.html"><img src="https://fishraposo.github.io/images/portfolio/gt-refusal.png" alt="groundtruth refusing a question the corpus cannot support"></a><br><sub><b>It refuses.</b> A question the corpus can't support gets an explicit refusal and a retrieval trace, not a guess.</sub></td>
<td width="33%" valign="top"><a href="https://fishraposo.github.io/projects/evalforge.html"><img src="https://fishraposo.github.io/images/portfolio/eval-case.png" alt="evalforge failed retrieval case with judge scores"></a><br><sub><b>It catches regressions.</b> A retrieval regression flagged by judges before it ships.</sub></td>
</tr>
</table>

Every repo below has a sample-data portfolio demo; its README has the commands.

## What I help with

- **Coding agents that follow your workflow.** Claude Code and similar agents set up for your repo: project instructions, permissions, hooks that run your checks, MCP tool connections and guardrails.
- **AI-built apps that break in production.** A written audit of what breaks and what to fix first, then fixes with tests so they stay fixed.
- **RAG and agent systems that cite, refuse and hand off** instead of guessing, with evaluations that catch regressions.

Fixed prices and written scope, through [Upwork](https://www.upwork.com/freelancers/~01ca94c53d0d0101f3). Open to remote applied-AI roles (full-time or contract).

## Proof

Public, MIT-licensed, with tests you can run yourself.

| Repo | What it is | Evidence |
|---|---|---|
| **[WCP-Compliance-Agent-V5](https://github.com/FishRaposo/WCP-Compliance-Agent-V5)** | Five-service WH-347 compliance platform: deterministic validation decides, the LLM explains, every decision traceable. | 367 tests, checksum-verified evidence |
| **[groundtruth](https://github.com/FishRaposo/groundtruth)** | Production RAG platform: hybrid search, citations, refusal logic. | 291 API + 47 web tests, 8/8 browser smoke checks |
| **[evalforge](https://github.com/FishRaposo/evalforge)** | Regression testing for RAG and agentic AI. | Retrieval and conversational evaluations |
| **[aria-agent](https://github.com/FishRaposo/aria-agent)** | Agent harness with approval gates and execution tracing. | 200 Python + 12 Agent Skills + 31 frontend tests; Ruff and Pyright clean |
| **[agenttrace](https://github.com/FishRaposo/agenttrace)** | Agent observability and replay SDK with cost attribution. | 132 SDK + 98 collector + 24 dashboard tests |

Each project has a page with its verified results and walkthrough. Full catalog: [fishraposo.github.io/projects.html](https://fishraposo.github.io/projects.html).

## Before

AI Lead at Expat Money, Jun 2022 – Nov 2025. Created and led the AI function from zero. Cut AI-for-content costs 90% — replaced a $200/month tool with a $20/month one — and halved content production time. Built grounded retrieval for cross-jurisdiction expat planning — a domain where wrong answers have real consequences.

## Writing

**[Taste Is All You Need](https://x.com/FishRaposo/status/2080404528692924696)** — long-form analysis of agent-harness economics: why scaffolding beats model spend. Backed by a personal agent-scaffolding benchmark reverse-engineering NDS ROMs with byte-level verification: frontier models score 6–8/10 unaided with high variance; under my spec/skill scaffolding, 10/10 with zero variance.

## Links

[Portfolio](https://fishraposo.github.io) · [X](https://x.com/FishRaposo) · [Upwork](https://www.upwork.com/freelancers/~01ca94c53d0d0101f3) · fishraposo@gmail.com

Send me what's breaking. I'll tell you specifically what's wrong before you spend a dollar.

<sub>Last updated: 2026-10-22</sub>
