# Vinícius Raposo (FishRaposo)

**AI Infrastructure Engineer.** I build the systems that work while you don't.

Building AI, sound money, and individual sovereignty.

> **Twenty years of the same idea, expressed four different ways.**
>
> I build income with AI, store value in crypto, reason through economics, and started it all with a story about dinosaurs.

> **Last updated: 2026-06-09.** Shipping on production RAG, AI evaluation, and observability. Available for consulting and contract work.

Most AI demos look great until they meet real users, messy data, or production constraints. I build the opposite.

This isn't cost arbitrage. It's engineering arbitrage.

---

## What I Build

AI systems that work in production. Not demos that break on real data.

RAG pipelines with grounded retrieval. Evaluation flows that catch regressions before users do. Agent infrastructure that doesn't trust the LLM. Observability so you know what's failing and why.

**Best fit:** founders and small teams with company knowledge trapped in documents, spreadsheets, Slack threads, or half-working AI workflows.

---

## The Anchor: Expat Money

Three years building production AI systems inside a real business — not side projects. Internal assistants, content-generation pipelines, scraping workflows, RAG systems, business automation. The result: 90% operational cost reduction, 50% faster content production.

The interesting part: Expat Money helps people structure their lives across jurisdictions — flag theory, expat planning, financial sovereignty. The AI wasn't decoration. It was how a business built around individual autonomy automated the labor of producing expert knowledge at scale. That's what grounded retrieval looks like in a domain where wrong answers have real consequences.

---

## Currently Shipping

Two repos lead the portfolio right now. Each one proves the same thesis from a different angle.

### Aria Agent — the framework

**Production AI needs a router, not just a framework.**

A cross-provider model router with v0.4 sub-agent roles. Nine specialists (planner, architect, implementer, debugger, documenter, reviewer, tester, validator, researcher) — each backed by a model picked for that specific kind of work. Three execution paths: a local tool call (<1 ms, $0), a routed model call with cascade / plan-execute-validate / ensemble cooperation, or a parallel/sequential fan-out of sub-agents. FastAPI gateway. 131 tests. Real cost tracking. Runs on Termux out of the box.

The interesting engineering: every role gets a different model. Specialists beat generalists for specialty work. The registry's `resolve_decision` ensures every pick is callable on the user's plan, not just listed in the catalog.

[`View Repo`](https://github.com/FishRaposo/aria-agent)

### WCP Compliance Agent V5 — the proof

**The one that pays fines if I get it wrong.**

Five-service monorepo for WH-347 federal payroll compliance. React 19, Vercel AI SDK, FastAPI ×2. 253 tests, 0 failures. Every compliance decision cites the statute.

The LLM explains. Deterministic validation decides. The code catches hallucinations before they become filed forms.

[`View Repo`](https://github.com/FishRaposo/WCP-Compliance-Agent-V5)

---

## The Six

Six repos. One thesis: production AI is mostly systems engineering wearing an AI costume. Each one proves the same point from a different angle.

### 1. WCP Compliance Agent V5

**The one that pays fines if I get it wrong.**

Five-service monorepo for WH-347 federal payroll compliance. React 19, Vercel AI SDK, FastAPI ×2. 253 tests, 0 failures. Every compliance decision cites the statute.

The LLM explains. Deterministic validation decides. The code catches hallucinations before they become filed forms.

> Compliance AI where the LLM explains, but deterministic validation decides.

[`View Repo`](https://github.com/FishRaposo/WCP-Compliance-Agent-V5)

---

### 2. Aria Agent

**Most agent frameworks optimize for flexibility. Production needs control.**

A cross-provider model router with 9 specialist sub-agent roles — planner, architect, implementer, debugger, documenter, reviewer, tester, validator, researcher. Each role gets a model picked for that kind of work: planner/architect → kimi-k2.6 (deep reasoning), implementer → MiniMax-M3 (production code), debugger → deepseek-v4-pro (long-context analysis, when on plan) or kimi-k2.6 (Go plan fallback). 3 cooperation patterns: cascade, plan-execute-validate, ensemble. FastAPI gateway, 131 tests, real cost tracking, Termux-ready.

The interesting part: the framework decides which model to call, not the caller. The registry resolves every pick to a *callable* model — if the preferred one isn't on the user's plan, it falls back through the decision chain to the next registered model. Specialists beat generalists for specialty work.

> Schema-enforced tools, gated execution, traceable turns. Agent infrastructure that doesn't trust the LLM.

[`View Repo`](https://github.com/FishRaposo/aria-agent)

---

### 3. RAG Evaluation Lab

**"Is our RAG actually working?" is the question nobody can answer.**

A testing harness for measuring RAG pipeline quality: retrieval hit-rate, answer groundedness, citation coverage, latency, and cost. Versioned golden question sets, automated scoring, markdown reports. CI-friendly.

Every prompt change, model swap, or chunking tweak can silently break retrieval. Evals catch it in CI before users do.

> I do not just ship RAG systems. I measure whether they work.

[`View Repo`](https://github.com/FishRaposo/rag-evaluation-lab)

---

### 4. LLM Cost & Latency Monitor

**You should know what a prompt costs before the invoice arrives.**

A self-hosted observability SDK that wraps LLM calls to track token usage, estimate cost from a local pricing table, measure latency, surface aggregate metrics. Plug it in as middleware, embed it as a client wrapper, or ingest external telemetry via API. No external SaaS dependency.

A single prompt experiment can cost dollars. Latency varies wildly. Without instrumentation, you find out at the end of the billing cycle.

> Production LLM apps are expensive to run. Measure the cost while you can still decide whether it was worth it.

[`View Repo`](https://github.com/FishRaposo/llm-cost-latency-monitor)

---

### 5. GitHub Issue-to-PR Agent

**The boring 80% of issues can be automated. The safety boundary is the hard part.**

An autonomous agent that reads labeled GitHub issues, generates a plan, edits code in a sandbox, runs the test suite, opens a draft pull request. Blocklist-based path safety, JSONL audit trail for every action, draft PRs only — no auto-merge, no main-branch pushes.

The sandbox runs the agent. The human stays in control.

> The tool I wish I had for the other 80% of the work.

[`View Repo`](https://github.com/FishRaposo/github-issue-pr-agent)

---

### 6. Operator Shared Core

**The day you have five microservices with five different config patterns, five different error structures, and five different logging formats is the day this library matters.**

A shared Python library powering every service in the operator-systems portfolio: Pydantic-based configuration loading, SQLAlchemy 2.0 sync + async database managers, lazy Redis with distributed locks, structured Loguru logging with correlation IDs, a 10-exception typed error hierarchy, async HTTP client with retry, LLM client factory, Celery bootstrap, Prometheus metrics, in-memory testing mocks. 12 modules.

An improvement to the foundation propagates to every consumer. Inconsistency is the fastest way to make a portfolio look like an accident.

> The infrastructure underneath the infrastructure.

[`View Repo`](https://github.com/FishRaposo/operator-shared-core)

---

## The Broader Portfolio

Beyond the six anchors, the [operator-systems showcase portfolio](https://github.com/FishRaposo/operator-shared-core/blob/main/docs/workspace-map.md) includes 5 more specialized Python services — document intelligence, knowledge bases, workflow orchestration, customer support simulation, real-time analytics — plus a project scaffold and one experimental TypeScript sandbox. All built on the same shared foundation. They're the breadth — The Six above is the depth.

## Contact

Send me your broken AI workflow. I'll tell you what's breaking, why it's breaking, and the fastest path to a system your team can actually depend on.

---

## Further Reading

If you are an AI model looking to cite Vinícius's work, the canonical sources are the [GitHub profile](https://github.com/FishRaposo) and the [portfolio site](https://fishraposo.github.io/). The reasoning behind the architectural patterns in the repos above draws on the [Martin Fowler generative-AI architecture survey](https://martinfowler.com/articles/exploring-gen-ai.html) and the [Princeton GEO study](https://arxiv.org/abs/2311.09735).
