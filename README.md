# Vinícius Raposo (FishRaposo)

**I build the systems that work while you don't.**

Applied AI reliability — production RAG, agents, evaluation, deterministic scaffolding.

&gt; **Last updated: 2026-08-23.** The shipped/high-signal repos below are the current proof; the full catalog lives on the portfolio site.

Most AI demos look great until they meet real users, messy data, or production constraints. I build the opposite.

This isn't cost arbitrage. It's engineering arbitrage.

**Now:** Founding Engineer at Zap Viagens — privacy-first, self-hosted AI products (CRM automation, campaign generation) on open-source models for service businesses.

---

## What I Build

Systems that work in production. Not demos that break on real data.

Production AI is the execution surface: RAG pipelines with grounded retrieval, evaluation flows that catch regressions, agent infrastructure that does not trust the LLM, and observability so you know what is failing and why. The recurring move: discover the method with expensive intelligence, encode it as deterministic software and policy, let cheap models execute it reliably. The nondeterminism doesn't disappear — it stops mattering.

**The proof, quantified:** my personal benchmark reverse-engineers NDS ROMs with byte-level verification. Frontier models score 6–8/10 bare, with high variance. Under my spec/skill scaffolding: 10/10, variance zero.

---

## The Anchor: Expat Money

Jun 2022 – Nov 2025 creating and leading the AI function inside a real business — not side projects. Internal assistants, content-generation pipelines, scraping workflows, RAG systems, business automation. The result: content costs down 90%, production time halved.

The interesting part: Expat Money helps people structure their lives across jurisdictions — flag theory, expat planning, financial sovereignty. The AI wasn't decoration. It was how a business built around individual autonomy automated the labor of producing expert knowledge at scale. That's what grounded retrieval looks like in a domain where wrong answers have real consequences.

---

## Start Here: Current Public Proof

These are the repos I would inspect first.

- **[WCP-Compliance-Agent-V5](https://github.com/FishRaposo/WCP-Compliance-Agent-V5)** — Production-grade WH-347 compliance platform: deterministic validation decides, the LLM explains, every decision traceable. The CV summarizes it as 270 unit tests; the full receipt records 367 public tests across five service bins plus four tooling checks, with an offline-verifiable evidence bundle.
- **[aria-agent](https://github.com/FishRaposo/aria-agent)** — Canonical clean-break agent harness: approval gates, execution tracing, progressive-disclosure Agent Skills.
- **[groundtruth](https://github.com/FishRaposo/groundtruth)** — Production RAG platform: hybrid search, citations, refusal logic.
- **[llm-gateway](https://github.com/FishRaposo/llm-gateway)** — LLM proxy with routing, guardrails, cost control, and fallback.
- **[agenttrace](https://github.com/FishRaposo/agenttrace)** — Agent observability and replay SDK with cost attribution, prompt-cost reporting, and an absorbed safety-bounded issue→draft-PR workflow (lineage: llm-cost-latency-monitor, github-issue-pr-agent; source archived).
- **[evalforge](https://github.com/FishRaposo/evalforge)** — Regression testing for RAG and agentic AI: retrieval and conversational evaluations (lineage: rag-evaluation-lab, ai-support-simulator).

Writing: *[Taste Is All You Need](https://x.com/FishRaposo/status/2080404528692924696)* — a long-form analysis of agent-harness economics and why scaffolding beats model spend.

---

## Full Public Repo Catalog

The full public repo catalog lives on the portfolio, each project with its own page:

**[fishraposo.github.io/projects.html](https://fishraposo.github.io/projects.html)**

The catalog separates highlighted shipped systems, supporting infrastructure, meta/profile repos, and archive/study repos.

---

## Contact

Freelance engagements via **[Upwork](https://www.upwork.com/freelancers/~01ca94c53d0d0101f3)** — everything above is the due diligence.

Send me your broken AI workflow. I'll tell you what's breaking, why it's breaking, and the fastest path to a system your team can actually depend on.
