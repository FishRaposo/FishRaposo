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

---

### 1. WCP Compliance Agent V5

**The one that pays fines if I get it wrong.**

Five-service monorepo for WH-347 federal payroll compliance. React 19, Vercel AI SDK, FastAPI x2. 271 tests. 0 failures. Every compliance decision cites the statute.

This is the flagship because it proves the hardest thing in AI: building systems where correctness is non-negotiable. The LLM explains. Deterministic validation decides. If the model hallucinates a wage interpretation, the code catches it before anyone files the wrong form.

Trust scoring. Auditable persistence. Distributed tracing. The boring parts that make the system actually run.

> Compliance AI where the LLM explains, but deterministic validation decides.

[`View Repo`](https://github.com/FishRaposo/WCP-Compliance-Agent-V5)

---

### 2. KnowledgeOps

**Your company knows things. Your systems don't.**

Reference architecture for internal AI knowledge tools. Ingestion, hybrid retrieval with citations, LLM gateway, evaluation service, tracing, cost controls, RBAC. Deployable as-is.

This is the playbook. Every other repo in this portfolio plugs into the patterns defined here. Organizational knowledge is infrastructure. Treat it that way.

> From scattered company knowledge to operational AI infrastructure.

[`View Repo`](https://github.com/FishRaposo/knowledgeops)

---

### 3. GroundTruth

**"Can we ask questions over our documents and trust the answers?"**

Yes. But only if your RAG actually cites sources, refuses when evidence is insufficient, and lets you trace retrieval. GroundTruth does all three. Upload documents. Get answers with citations. When the system can't find enough evidence, it says so instead of guessing.

Internal assistant template. Production-ready. No vibes-based retrieval.

> RAG that retrieves, cites, refuses, and can be debugged.

[`View Repo`](https://github.com/FishRaposo/groundtruth)

---

### 4. EvalForge

**Most people build LLM workflows. Far fewer can test whether those workflows keep working.**

Regression testing for RAG and agents. Tests retrieval correctness, citation quality, refusal behavior, semantic similarity, and regression drift through versioned YAML suites and CI-friendly reports.

Your LLM app changes every time you update a prompt, swap a model, or touch your retrieval pipeline. Without evals, you have no idea what broke. EvalForge makes the breakage visible before your users do.

> I do not just ship AI systems. I measure whether they work.

[`View Repo`](https://github.com/FishRaposo/evalforge)

---

### 5. AgentTrace

**If an agent fails in production, you should be able to see why.**

Observability layer for agentic workflows. Records tool calls, model invocations, intermediate decisions, inputs, outputs, latency, cost, and final results. Replay and dashboard.

Most AI profiles stop at "I can build agents." This goes deeper: "I can trace, replay, debug, and monitor agents in production." The difference between a demo and a system is observability.

> If an agent fails, you should be able to see why.

[`View Repo`](https://github.com/FishRaposo/agenttrace)

---

### 6. LLM Gateway

**Your LLM calls need a bouncer. This is it.**

Enterprise proxy with routing, guardrails, cost control, fallback, and provider abstraction. Route to the right model for the right task. Block calls that exceed budget. Fall back when a provider goes down. Swap providers without touching application code.

Every production system with multiple LLM calls eventually needs this. Better to build it once, centrally, than to scatter provider logic across five services.

> Your LLM calls need a bouncer. This is it.

[`View Repo`](https://github.com/FishRaposo/llm-gateway)

---

## The Infrastructure Stack

- **Production Architecture** — WCP V5 — Multi-service compliance AI with deterministic validation, trust scoring, 271 tests
- **Knowledge Infrastructure** — KnowledgeOps — Full internal AI knowledge platform: ingestion, retrieval, gateway, eval, RBAC
- **Grounded Retrieval** — GroundTruth — RAG with source citations, refusal on insufficient evidence, retrieval traces
- **AI Evaluation** — EvalForge — Regression testing, citation checks, semantic similarity, CI-friendly eval suites
- **AI Observability** — AgentTrace — Tool-call tracing, replay, latency, cost monitoring for agentic workflows
- **LLM Routing & Control** — LLM Gateway — Provider abstraction, fallback, guardrails, cost controls

## Archived

- [WCP-Compliance-Agent-V3](https://github.com/FishRaposo/WCP-Compliance-Agent-V3) — Predecessor to V5, three-service architecture
- [WCP-Compliance-Agent-V2](https://github.com/FishRaposo/WCP-Compliance-Agent-V2) — TypeScript predecessor, early monolithic implementation

---

## Contact

Send me your broken AI workflow. I'll tell you what's breaking, why it's breaking, and the fastest path to a system your team can actually depend on.
