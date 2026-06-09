# Vinícius Raposo (FishRaposo)

**AI Infrastructure Engineer** — I build the systems that work while you don't.

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

Five-service monorepo for WH-347 federal payroll compliance. React 19, Vercel AI SDK, FastAPI x2. 271 tests. 0 failures. Every compliance decision cites the statute.

This is the flagship because it proves the hardest thing in AI: building systems where correctness is non-negotiable. The LLM explains. Deterministic validation decides. If the model hallucinates a wage interpretation, the code catches it before anyone files the wrong form.

Trust scoring. Auditable persistence. Distributed tracing. The boring parts that make the system actually run.

> Compliance AI where the LLM explains, but deterministic validation decides.

[`View Repo`](https://github.com/FishRaposo/WCP-Compliance-Agent-V5)

---

### 2. Aria Agent

**Most agent frameworks optimize for flexibility. Production needs control.**

A lightweight framework for controlled AI agents: Pydantic-validated tool calls (every argument checked before execution, not after), human-in-the-loop approval gates for high-risk actions, bounded conversation memory, and per-turn audit trails. Built on shared infrastructure, designed to fail safe.

The interesting engineering here is what's *not* allowed: arbitrary tool calls, unbounded context growth, silent auto-execution of side effects. Aria shows how a real agent system enforces constraints — the kind of engineering production AI needs but demo frameworks skip.

> Schema-enforced tools, gated execution, traceable turns. Agent infrastructure that doesn't trust the LLM.

[`View Repo`](https://github.com/FishRaposo/aria-agent)

---

### 3. RAG Evaluation Lab

**"Is our RAG actually working?" is the question nobody can answer.**

A testing harness that measures RAG pipelines quantitatively: retrieval hit-rate (are the right chunks coming back?), MRR (how high do they rank?), answer faithfulness (is the answer supported by retrieved context?), citation coverage (do the citations reference real sources?), latency, and cost. Versioned golden question sets, automated scoring, markdown reports. CI-friendly.

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

An autonomous agent that reads labeled GitHub issues, plans the change, edits code in a sandboxed repo, runs the test suite, and opens a draft pull request. Every action is allowlisted — no secret access, no main-branch pushes, no auto-merges. Drafts only. Humans review, humans merge.

The interesting engineering is the safety surface: what the agent *cannot* do. Allowlisted repositories, allowlisted file paths, audit trails for every tool call, gated PR creation on test results. The agent bridges "issue filed" to "draft PR ready for review" without ever crossing the trust boundary.

> The tool I wish I had for the other 80% of the work.

[`View Repo`](https://github.com/FishRaposo/github-issue-pr-agent)

---

### 6. Operator Shared Core

**Twelve Python services, one foundation library. Consistency by construction.**

The shared library that powers every Python service in the operator-systems portfolio: Pydantic-based configuration loading, SQLAlchemy 2.0 sync + async database managers, lazy Redis with distributed locks, structured Loguru logging with correlation IDs, a 10-exception typed error hierarchy, async HTTP client with retry, LLM client factory, Celery bootstrap, Prometheus metrics, and in-memory testing mocks.

Any improvement to the foundation automatically propagates to every consumer. Every project starts with the same config patterns, the same error structures, the same logging output. Inconsistency across a portfolio of services is the fastest way to make it look like an accident instead of a system.

> The infrastructure underneath the infrastructure.

[`View Repo`](https://github.com/FishRaposo/operator-shared-core)

---

## The Infrastructure Stack

- **Production Case Study** — WCP V5 — Multi-service compliance AI with deterministic validation, trust scoring, 271 tests, every decision cites the statute
- **Agent Framework** — Aria Agent — Controlled agents with Pydantic tools, approval gates, bounded memory, audit trails
- **RAG Evaluation** — RAG Evaluation Lab — Quantitative RAG scoring: hit-rate, MRR, faithfulness, citation coverage, CI-friendly reports
- **LLM Observability** — LLM Cost & Latency Monitor — Token costs, latency, per-request telemetry, self-hosted
- **Agent in Production** — GitHub Issue-to-PR Agent — Autonomous issue-to-draft-PR with allowlisted safety boundaries
- **Shared Foundation** — Operator Shared Core — The library every Python service in the portfolio imports

## The Broader Portfolio

Beyond the six anchors, the [operator-systems showcase portfolio](https://github.com/FishRaposo/operator-shared-core/blob/main/docs/workspace-map.md) includes 6 more specialized services (document intelligence, knowledge bases, workflow orchestration, customer support simulation, real-time analytics) all built on the same shared foundation. They're the breadth — The Six above is the depth.

## Archived

- [WCP-Compliance-Agent-V3](https://github.com/FishRaposo/WCP-Compliance-Agent-V3) — Predecessor to V5, three-service architecture
- [WCP-Compliance-Agent-V2](https://github.com/FishRaposo/WCP-Compliance-Agent-V2) — TypeScript predecessor, early monolithic implementation

---

## Contact

Send me your broken AI workflow. I'll tell you what's breaking, why it's breaking, and the fastest path to a system your team can actually depend on.
