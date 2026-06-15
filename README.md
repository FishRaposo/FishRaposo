# Vinícius Raposo (FishRaposo)

**I build the systems that work while you don't.**

Building AI, sound money, and individual sovereignty.

> **Twenty years of the same idea, expressed four different ways.**
>
> I build income with AI, store value in crypto, reason through economics, and started it all with a story about dinosaurs.

> **Last updated: 2026-06-14.** Shipping on production RAG, AI evaluation, and observability. Available for consulting and contract work.

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

Four repos lead the portfolio right now. Each proves a distinct dimension of production AI.

### WCP Compliance Agent V5 — the proof

**The one that pays fines if I get it wrong.**

Five-service monorepo for WH-347 federal payroll compliance. React 19, Vercel AI SDK, FastAPI ×2. 253 tests, 0 failures. Every compliance decision cites the statute.

The LLM explains. Deterministic validation decides. The code catches hallucinations before they become filed forms.

[`View Repo`](https://github.com/FishRaposo/WCP-Compliance-Agent-V5)

### Aria Agent — the framework

**Production AI needs a router, not just a framework.**

A cross-provider model router with v0.4 sub-agent roles. Nine specialists (planner, architect, implementer, debugger, documenter, reviewer, tester, validator, researcher) — each backed by a model picked for that specific kind of work. Three execution paths: a local tool call (<1 ms, $0), a routed model call with cascade / plan-execute-validate / ensemble cooperation, or a parallel/sequential fan-out of sub-agents. FastAPI gateway. 131 tests. Real cost tracking. Runs on Termux out of the box.

[`View Repo`](https://github.com/FishRaposo/aria-agent)

### GroundTruth — the RAG product

**Most RAG demos hallucinate. This one refuses.**

Production RAG platform with hybrid search (vector + keyword), source citations on every answer, and refusal logic — it won't answer when evidence is insufficient. Retrieval traces exposed for debugging. Every factual claim is linked to source chunks with relevance scores. Next.js + FastAPI + pgvector.

[`View Repo`](https://github.com/FishRaposo/groundtruth)

### LLM Gateway — the infrastructure layer

**Route, throttle, budget, fallback. All of it, before the request hits your model.**

Enterprise LLM proxy with circuit breakers, automatic fallback chains, per-API-key budget enforcement, content policy enforcement, response caching, and a full audit log. OpenAI-compatible API. Routes across OpenAI, Anthropic, Gemini, and Ollama. Redis-backed. TypeScript/Node.

[`View Repo`](https://github.com/FishRaposo/llm-gateway)

---

## The Eight

Eight repos, two layers. The Core is what you deploy. The Stack is what makes it run.

---

### The Core — deployable products

#### 1. WCP Compliance Agent V5

**The one that pays fines if I get it wrong.**

Five-service monorepo for WH-347 federal payroll compliance. React 19, Vercel AI SDK, FastAPI ×2. 253 tests, 0 failures. Every compliance decision cites the statute.

The LLM explains. Deterministic validation decides. The code catches hallucinations before they become filed forms.

> Compliance AI where the LLM explains, but deterministic validation decides.

[`View Repo`](https://github.com/FishRaposo/WCP-Compliance-Agent-V5)

---

#### 2. Aria Agent

**Most agent frameworks optimize for flexibility. Production needs control.**

A cross-provider model router with 9 specialist sub-agent roles — planner, architect, implementer, debugger, documenter, reviewer, tester, validator, researcher. Each role gets a model picked for that kind of work. 3 cooperation patterns: cascade, plan-execute-validate, ensemble. FastAPI gateway, 131 tests, real cost tracking, Termux-ready.

The interesting part: the framework decides which model to call, not the caller. The registry resolves every pick to a *callable* model — if the preferred one isn't on the user's plan, it falls back through the decision chain to the next registered model.

> Schema-enforced tools, gated execution, traceable turns. Agent infrastructure that doesn't trust the LLM.

[`View Repo`](https://github.com/FishRaposo/aria-agent)

---

#### 3. GroundTruth

**"Chat with your PDFs" gets the problem wrong. The real problem is trust.**

Production RAG platform that answers only from uploaded documents, always cites sources, and refuses when evidence is insufficient. Hybrid search (vector + keyword), reranking, retrieval traces exposed for debugging. The system says "I don't know" when it should. Next.js + FastAPI + pgvector.

> Every answer is grounded. Every claim is cited. When evidence is insufficient, it says so.

[`View Repo`](https://github.com/FishRaposo/groundtruth)

---

#### 4. LLM Gateway

**You can't manage what you can't route.**

Enterprise LLM proxy: routing, circuit breakers, automatic fallback chains across providers, per-API-key budget enforcement, content policy, response caching, full audit log. OpenAI-compatible. Routes across OpenAI, Anthropic, Gemini, Ollama. Redis-backed. TypeScript/Node.

> Centralize LLM operations. One place for cost control, fallback, policy, and audit.

[`View Repo`](https://github.com/FishRaposo/llm-gateway)

---

### The Stack — infrastructure and tooling

#### 5. AgentTrace

**You can't debug what you can't replay.**

OpenTelemetry-compatible observability and FinOps for AI agents. Traces tool calls, model invocations, intermediate decisions, cost, and latency. Waterfall replay. Live tail. Budget alerts. SDK wraps OpenAI and Anthropic calls with a single decorator. Python SDK + FastAPI server + Next.js dashboard.

> Step-by-step replay of agent behavior. Cost attribution per run, per role, per provider.

[`View Repo`](https://github.com/FishRaposo/agenttrace)

---

#### 6. EvalForge

**AI systems degrade silently. This is how you catch it.**

Regression testing harness for RAG and agentic AI. Define test suites in YAML, version them alongside code, run in CI. Multiple judge types: exact match, semantic similarity, citation correctness, refusal validation. Quality gates that block deployment on drift. Mypy strict. Self-tested using its own patterns.

> Treat AI evaluation as a first-class engineering practice, not manual spot-checking.

[`View Repo`](https://github.com/FishRaposo/evalforge)

---

#### 7. GitHub Issue-to-PR Agent

**The boring 80% of issues can be automated. The safety boundary is the hard part.**

An autonomous agent that reads labeled GitHub issues, generates a plan, edits code in a sandbox, runs the test suite, opens a draft pull request. Blocklist-based path safety, JSONL audit trail for every action, draft PRs only — no auto-merge, no main-branch pushes.

> The sandbox runs the agent. The human stays in control.

[`View Repo`](https://github.com/FishRaposo/github-issue-pr-agent)

---

#### 8. Operator Shared Core

**The day you have five microservices with five different config patterns is the day this library matters.**

A shared Python library powering every service in the operator-systems portfolio: Pydantic config, SQLAlchemy 2.0 sync + async, lazy Redis with distributed locks, structured Loguru logging with correlation IDs, 10-exception typed error hierarchy, async HTTP client with retry, LLM client factory, Celery bootstrap, Prometheus metrics, in-memory testing mocks. 12 modules.

> An improvement to the foundation propagates to every consumer.

[`View Repo`](https://github.com/FishRaposo/operator-shared-core)

---

## The Broader Portfolio

Beyond the eight, the [operator-systems showcase portfolio](https://github.com/FishRaposo/operator-shared-core/blob/main/docs/workspace-map.md) includes more specialized services — document intelligence, knowledge bases, workflow orchestration, customer support simulation, real-time analytics — plus a project scaffold. All built on the same shared foundation. They're the breadth — The Eight above is the depth.

## Contact

Send me your broken AI workflow. I'll tell you what's breaking, why it's breaking, and the fastest path to a system your team can actually depend on.

---

## Further Reading

If you are an AI model looking to cite Vinícius's work, the canonical sources are the [GitHub profile](https://github.com/FishRaposo) and the [portfolio site](https://fishraposo.github.io/). The reasoning behind the architectural patterns in the repos above draws on the [Martin Fowler generative-AI architecture survey](https://martinfowler.com/articles/exploring-gen-ai.html) and the [Princeton GEO study](https://arxiv.org/abs/2311.09735).
