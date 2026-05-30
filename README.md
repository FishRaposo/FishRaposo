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

## The Five

These five repos form a complete AI infrastructure portfolio. Each one reinforces the same thesis from a different angle:

> I build production AI infrastructure — from compliance-grade systems to internal knowledge platforms, reliable RAG, evaluation harnesses, and agent observability.

---

### 1. WCP Compliance Agent V5

**Compliance-Grade AI System**

Five-service monorepo for WH-347 federal payroll compliance. Every compliance decision cites the statute.

**React 19 · Vercel AI SDK · FastAPI ×2 · 271 tests · 0 failures**

This is the flagship. It proves I can build serious AI systems where correctness, traceability, and reliability matter. Multi-service architecture, deterministic validation, LLM verdict synthesis, trust scoring, auditable persistence, distributed tracing.

> Compliance AI where the LLM explains, but deterministic validation decides.

[`📂 View Repo`](https://github.com/FishRaposo/WCP-Compliance-Agent-V5)

---

### 2. KnowledgeOps Starter Kit

**Internal AI Knowledge Platform**

Reference architecture for internal AI knowledge tools: ingestion, hybrid retrieval with citations, LLM gateway, evaluation service, tracing, cost controls, RBAC, and deployable operations stack.

This turns my portfolio from "a set of projects" into a methodology. Organizational knowledge is infrastructure.

> From scattered company knowledge to operational AI infrastructure.

[`📂 View Repo`](https://github.com/FishRaposo/10-knowledgeops)

---

### 3. GroundTruth

**Production RAG Assistant Template**

Internal assistant template that answers only from uploaded documents, cites sources, refuses when evidence is insufficient, and exposes retrieval traces for debugging.

The clearest client-facing repo. Directly maps to the market problem: "Can we ask questions over our documents and trust the answers?"

> RAG that retrieves, cites, refuses, and can be debugged.

[`📂 View Repo`](https://github.com/FishRaposo/01-groundtruth)

---

### 4. EvalForge

**Regression Testing for RAG and Agents**

Practical evaluation harness for RAG and agentic AI systems. Tests retrieval correctness, citation quality, refusal behavior, semantic similarity, and regression drift through versioned YAML suites and CI-friendly reports.

Most people build LLM workflows. Far fewer can test whether those workflows keep working.

> I do not just ship AI systems. I measure whether they work.

[`📂 View Repo`](https://github.com/FishRaposo/02-evalforge)

---

### 5. AgentTrace

**Observability and Replay for AI Agents**

Lightweight observability layer for agentic AI workflows. Records tool calls, model invocations, intermediate decisions, inputs, outputs, latency, cost, and final results, with replay and dashboard visualization.

Most AI profiles stop at "I can build agents." This goes deeper: "I can trace, replay, debug, and monitor agents in production."

> If an agent fails, you should be able to see why.

[`📂 View Repo`](https://github.com/FishRaposo/03-agenttrace)

---

## The Infrastructure Stack

| Pillar | Repo | What It Shows |
|--------|------|---------------|
| Production Architecture | WCP V5 | Multi-service AI system with compliance, tracing, tests, trust scoring |
| Knowledge Infrastructure | KnowledgeOps | Full internal AI knowledge platform architecture |
| Grounded Retrieval | GroundTruth | RAG with citations, refusal, retrieval traces |
| AI Evaluation | EvalForge | Regression testing, citation checks, CI-friendly evals |
| AI Observability | AgentTrace | Tool-call tracing, replay, latency, cost monitoring |

---

## Supporting Toolkit

| Repo | What It Does |
|------|-------------|
| [04-llm-gateway](https://github.com/FishRaposo/04-llm-gateway) | LLM gateway with routing, fallbacks, provider abstraction, cost controls |
| [05-docflow](https://github.com/FishRaposo/05-docflow) | Document ingestion and processing pipeline for RAG systems |
| [06-semantic-router](https://github.com/FishRaposo/06-semantic-router) | Semantic routing layer for multi-agent and operational AI systems |
| [07-costpilot](https://github.com/FishRaposo/07-costpilot) | Cost, latency, and token observability dashboard for LLM operations |
| [08-compliancelens](https://github.com/FishRaposo/08-compliancelens) | Compliance automation toolkit for audits, records, operational review |
| [09-inboxops-ai](https://github.com/FishRaposo/09-inboxops-ai) | Human-in-the-loop workflow automation for operational pipelines |

---

## Archived

| Repo | Notes |
|------|-------|
| [WCP-Compliance-Agent-V3](https://github.com/FishRaposo/WCP-Compliance-Agent-V3) | Predecessor to V5 · three-service architecture |
| [WCP-Compliance-Agent-V2](https://github.com/FishRaposo/WCP-Compliance-Agent-V2) | TypeScript predecessor · early monolithic implementation |

---

## Contact

Send me your broken AI workflow. I'll tell you what's breaking, why it's breaking, and the fastest path to a system your team can actually depend on.
