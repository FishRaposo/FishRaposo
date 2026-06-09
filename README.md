# Vinícius Raposo (FishRaposo)

**AI Infrastructure Engineer** — I build the systems that work while you don't.

> **Last updated: 2026-06-09.** Currently focused on production RAG, AI evaluation, and observability. Open to consulting and contract work.

Most AI demos look great until they meet real users, messy data, or production constraints. I build the opposite.

This isn't cost arbitrage. It's engineering arbitrage.

---

## What I Build

- Internal AI assistants that survive real usage
- RAG pipelines with source citations and grounded retrieval
- Workflow automation that reduces operational drag
- AI copilots your team can actually trust
- Evaluation flows, observability, and failure handling
- Production-grade AI infrastructure

I don't sell chatbot wrappers. I build the infrastructure underneath: retrieval logic, data pipelines, system prompts, evaluation flows, failure handling, and deployment structure.

**Best fit:** founders and small teams with company knowledge trapped in documents, spreadsheets, Slack threads, or half-working AI workflows.

---

## The Six

Six repos. One thesis: production AI is mostly systems engineering wearing an AI costume. Each one proves the same point from a different angle.

### 1. WCP Compliance Agent V5

**The one that pays fines if I get it wrong.**

Five-service monorepo for WH-347 federal payroll compliance. React 19, Vercel AI SDK, FastAPI x2. 253 tests, 0 failures. Every compliance decision cites the statute.

The LLM explains. Deterministic validation decides. If the model hallucinates a wage interpretation, the code catches it before anyone files the wrong form.

> Compliance AI where the LLM explains, but deterministic validation decides.

[`View Repo`](https://github.com/FishRaposo/WCP-Compliance-Agent-V5)

---

### 2. Aria Agent

**Most agent frameworks optimize for flexibility. Production needs control.**

A lightweight framework for controlled AI agents: Pydantic-validated tool calls (every argument checked before execution, not after), human-in-the-loop approval gates for high-risk actions, bounded conversation memory, and per-turn audit trails. Built on a shared Python foundation, designed to fail safe.

The interesting engineering is what's *not* allowed: arbitrary tool calls, unbounded context growth, silent auto-execution of side effects. Aria shows how a real agent system enforces constraints — the kind of engineering production AI needs but demo frameworks skip.

> Schema-enforced tools, gated execution, traceable turns. Agent infrastructure that doesn't trust the LLM.

[`View Repo`](https://github.com/FishRaposo/aria-agent)

---

### 3. RAG Evaluation Lab

**"Is our RAG actually working?" is the question nobody can answer.**

A testing harness for measuring RAG pipeline quality: retrieval hit-rate (do the right chunks come back?), answer groundedness (is the answer supported by retrieved context?), versioned golden question sets, automated scoring, and markdown reports. CI-friendly.

Every prompt change, model swap, or chunking tweak can silently break retrieval. Without evals, you discover the breakage from users. With them, you see it in the CI report before deploy.

> I do not just ship RAG systems. I measure whether they work.

[`View Repo`](https://github.com/FishRaposo/rag-evaluation-lab)

---

### 4. LLM Cost & Latency Monitor

**You should know what a prompt costs before the invoice arrives.**

A self-hosted observability SDK that wraps LLM calls to track token usage, estimate cost from a local pricing table, measure latency, and surface aggregate metrics. Plug it in as middleware, embed it as a client wrapper, or ingest external telemetry via API. No external SaaS dependency, no data leaving your infrastructure.

A single prompt experiment can cost dollars. Latency varies wildly across models and prompt lengths. Without instrumentation, you're discovering your spend at the end of the billing cycle and your latency when users complain.

> Production LLM apps are expensive to run. Measure the cost while you can still decide whether it was worth it.

[`View Repo`](https://github.com/FishRaposo/llm-cost-latency-monitor)

---

### 5. GitHub Issue-to-PR Agent

**The boring 80% of issues can be automated. The safety boundary is the hard part.**

An autonomous agent that reads labeled GitHub issues, generates a plan, edits code in a sandbox, runs the test suite, and opens a draft pull request. Blocklist-based path safety (extensions + critical files), a JSONL audit trail for every action, draft PRs only — no auto-merge, no main-branch pushes, no merge. The sandbox runs the agent; the human stays in control.

The interesting engineering is what the agent *cannot* do. It's the difference between an automation that helps your team and one that ships surprises.

> The tool I wish I had for the other 80% of the work.

[`View Repo`](https://github.com/FishRaposo/github-issue-pr-agent)

---

### 6. Operator Shared Core

**The day you have five microservices with five different config patterns, five different error structures, and five different logging formats is the day this library matters.**

A shared Python library powering every service in the operator-systems portfolio: Pydantic-based configuration loading, SQLAlchemy 2.0 sync + async database managers, lazy Redis with distributed locks, structured Loguru logging with correlation IDs, a 10-exception typed error hierarchy, async HTTP client with retry, LLM client factory, Celery bootstrap, Prometheus metrics, and in-memory testing mocks. 12 modules. 39 unit tests.

Any improvement to the foundation automatically propagates to every consumer. Inconsistency across a portfolio of services is the fastest way to make it look like an accident instead of a system.

> The infrastructure underneath the infrastructure.

[`View Repo`](https://github.com/FishRaposo/operator-shared-core)

---

## The Broader Portfolio

Beyond the six anchors, the [operator-systems showcase portfolio](https://github.com/FishRaposo/operator-shared-core/blob/main/docs/workspace-map.md) includes 5 more specialized Python services — document intelligence, knowledge bases, workflow orchestration, customer support simulation, and real-time analytics — plus a project scaffold and one experimental TypeScript sandbox. All built on the same shared foundation. They're the breadth — The Six above is the depth.

## Contact

Send me your broken AI workflow. I'll tell you what's breaking, why it's breaking, and the fastest path to a system your team can actually depend on.
