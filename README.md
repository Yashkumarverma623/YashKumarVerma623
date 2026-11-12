<div align="center">

# Yash Kumar Verma
### AI Engineer • Agentic Systems • Production RAG • Inference Optimization

[![Typing SVG](https://readme-typing-svg.demolab.com?font=Fira+Code&weight=600&size=21&pause=1000&color=38BDF8&center=true&vCenter=true&width=750&lines=AI+Engineer+%7C+Agentic+Systems+%26+Production+RAG;Autonomous+Code+Repair+%26+Deterministic+CI+Evals;vLLM+PagedAttention+%26+Dynamic+Inference+Routing;Turning+Probabilistic+Models+into+Reliable+Software)](https://github.com/Yashkumarverma623)

<p align="center">
  <a href="https://linkedin.com/in/yash-kumar-verma623"><img src="https://img.shields.io/badge/LinkedIn-0A66C2?style=for-the-badge&logo=linkedin&logoColor=white" alt="LinkedIn" /></a>
  <a href="mailto:yashkumarverma623@gmail.com"><img src="https://img.shields.io/badge/Email-yashkumarverma623%40gmail.com-EA4335?style=for-the-badge&logo=gmail&logoColor=white" alt="Email" /></a>
  <a href="https://github.com/Yashkumarverma623"><img src="https://img.shields.io/badge/GitHub-181717?style=for-the-badge&logo=github&logoColor=white" alt="GitHub" /></a>
  
  <img src="https://img.shields.io/badge/Status-Available%20Immediately%20for%20Full--Time-10B981?style=for-the-badge&logo=statuspage&logoColor=white" alt="Status" />
 
</p>

---

<p align="center">
  <a href="#core-tenets"><b>Core Tenets</b></a> •
  <a href="#impact-metrics"><b>Impact Metrics</b></a> •
  <a href="#production-experience"><b>Experience</b></a> •
  <a href="#flagship-architectures"><b>Flagship Architectures</b></a> •
  <a href="#research-publications"><b>Research</b></a> •
  <a href="#technical-arsenal"><b>Tech Stack</b></a> •
  <a href="#github-analytics"><b>GitHub Analytics</b></a>
</p>

</div>

---

<a id="core-tenets"></a>
## 🎯 Core Engineering Tenets

I design, benchmark, and deploy **agentic AI systems**, **high-precision retrieval pipelines**, and **distributed inference infrastructure**. My engineering approach focuses on converting non-deterministic model capabilities into bounded, deterministic, and verifiable production services:

* 📐 **Statistical Rigor over Vibe Checks:** LLM evaluations and PR regression gates must be governed by statistical hypothesis testing—leveraging paired bootstrap resampling, McNemar's exact test on discordant pairs, and Holm–Bonferroni corrections rather than arbitrary score thresholds.
* ⚡ **Inference Economics & Throughput:** Maximizing performance per dollar through hybrid query routing—dispatching complex multi-step reasoning to frontier models (GPT-4o) while serving 65%+ structured extraction via self-hosted open weights (Llama-3.1-8B) optimized with vLLM PagedAttention and chunked prefill.
* 🛡️ **Defensive Agent Architecture:** Enforcing strict runtime safety via Tree-sitter AST-aware semantic chunking, cyclic LangGraph workflows with state rollbacks, real-time Presidio PII redaction, heuristic prompt-injection guardrails, and Pydantic schema validation with automatic repair loops.

---

<a id="impact-metrics"></a>
## 📊 Engineering Impact at a Glance

| Metric | Impact Delivered | Architecture / Methodology |
| :---: | :--- | :--- |
| **`-68%`** | **LLM Inference Cost Reduction** | Dynamic query routing (GPT-4o ↔ self-hosted Llama-3.1-8B on vLLM with PagedAttention) |
| **`0.72 → 0.91`** | **Ragas Faithfulness Lift** | Hybrid retrieval (BM25 + BGE-large via RRF) + Cross-Encoder reranking (`bge-reranker-large`) |
| **`+28%`** | **Context Precision Improvement** | Distractor context filtering & reciprocal rank fusion across enterprise knowledge corpora |
| **`93.33%`** | **Baseline Agent pass@1** | Sierra `tau-bench` retail domain evaluation with paired bootstrap CIs (83.33%–100%) in `AgentGate` |
| **`+13.8%`** | **SciFact nDCG@10 Gain** | Min-max score fusion over dense/BM25 baseline (*p* = 0.021 Holm-adjusted) in `rag-bench` |
| **`+17.1%`** | **NFCorpus nDCG@10 Gain** | Tuned hybrid RRF fusion with zero latency penalty compared to raw dense retrieval |
| **`24%`** | **SWE-bench-lite pass@1** | Autonomous multi-agent LangGraph code repair harness in isolated Docker containers |
| **`-35%`** | **Scope Hallucination Drop** | AST-aware code repository chunking using Tree-sitter semantic boundaries + Gemini embeddings |
| **`-38.2%`** | **PostgreSQL p95 Latency Reduction** | PgBouncer pooling, N+1 query elimination & composite indexing (340ms → 210ms at 1,500 req/s) |
| **`-42%`** | **Tool-Call Schema Failures** | Pydantic schema validation with self-healing retry loops & Presidio PII filtering (&lt;45ms overhead) |

---

<a id="production-experience"></a>
## 💼 Production Engineering Experience

### 🏢 **Stealth AI Startup (Series-A)**
**AI Engineer Intern** • *Remote* • `Feb 2026 – Jun 2026`  
*Focus: Production RAG & Multi-Agent Inference Platform*

* **Hybrid Retrieval & Reranking Optimization:** Optimized end-to-end retrieval for a multi-tenant enterprise RAG platform. Upgraded naive dense search to a hybrid retrieval pipeline (`BM25` + `BGE-large`) using Reciprocal Rank Fusion (RRF) coupled with cross-encoder reranking (`bge-reranker-large`), improving **Context Precision by 28%** and downstream **Ragas Faithfulness from 0.72 to 0.91** by suppressing distractor context chunks.
* **Cost-Optimized Dynamic Query Routing:** Engineered an intent-based dynamic query router across frontier and open-weight models. Dispatched complex multi-step reasoning to GPT-4o while routing **65%+ of high-volume structured extraction queries** to a self-hosted `Llama-3.1-8B` instance served via **vLLM with PagedAttention and chunked prefill**, slashing **inference costs by 68%** with zero degradation in task accuracy.
* **Production Agent Hardening & Guardrails:** Hardened multi-agent execution pipelines against adversarial inputs and tool failures. Integrated real-time **Microsoft Presidio PII redaction**, heuristic prompt-injection guardrails, and **Pydantic schema validation with automatic repair loops**, reducing downstream **tool-call schema failures by 42%** while sustaining `<45ms` guardrail latency overhead.

```
[Inbound Query] ──► [Presidio PII + Prompt Guardrail (<45ms)] ──► [Intent Classifier Router]
                                                                        │
                   ┌────────────────────────────────────────────────────┴──────────────────────────┐
                   ▼                                                                               ▼
     [High-Complexity Multi-Step Reasoning]                                     [Structured Extraction / High Volume (65%+)]
                   │                                                                               │
             [GPT-4o Engine]                                                         [Self-Hosted vLLM: Llama-3.1-8B]
                   │                                                                    (PagedAttention + Chunked Prefill)
                   │                                                                               │
                   └───────────────────────────────────┬───────────────────────────────────────────┘
                                                       ▼
                               [Pydantic Schema Validation & Repair Loop] ──► [-42% Tool-Call Schema Failures]
```

---

### 🏢 **Tellis Technologies Pvt Ltd**
**Software Engineer Intern** • *Remote* • `Sept 2025 – Jan 2026`  
*Focus: Autonomous Code Generation & Agentic Systems*

* **Autonomous Code Repair in LangGraph:** Developed an autonomous multi-agent code repair system in **LangGraph**. Designed a stateful cyclic workflow (`Planner` → `Editor` → `Test Runner` → `Verifier`) with checkpointed state rollbacks that localizes GitHub issues, synthesizes targeted unified-diff patches, and iteratively self-corrects syntax and test regressions across up to 3 repair loops.
* **Tree-sitter AST Repository Indexing:** Built an AST-aware repository indexing and retrieval pipeline using **Tree-sitter** and **ChromaDB**. Chunked codebases along semantic boundaries (classes, methods, docstrings) embedded via Gemini code embeddings, ensuring agent context windows received syntactically complete code structures and reducing agent **scope hallucinations by 35%** compared to naive character-split chunking.
* **SWE-bench Docker Evaluation Harness:** Engineered an automated Docker evaluation harness to benchmark agentic code generation against **SWE-bench-lite (50-task split)**. Executed generated patches in isolated ephemeral containers with strict cgroup timeouts, achieving a **24% pass@1 resolution rate** while instrumenting diff validity, test execution traces, and repair iteration counts.

```
[GitHub Issue / Bug] ──► [AST-Aware Retrieval (Tree-sitter + ChromaDB)]
                                    │
                                    ▼
       ┌────────────────► [LangGraph Stateful Cycle] ◄─────────────────┐
       │                            │                                  │
       │                            ▼                                  │
       │                  [1. Planner Agent]                           │
       │                            │                                  │ (Up to 3 Iterative
       │                            ▼                                  │  Self-Correction Loops)
       │                  [2. Editor Agent] ──► [Unified Diff Patch]   │
       │                            │                                  │
       │                            ▼                                  │
       │                  [3. Test Runner (Docker Ephemeral Sandbox)]  │
       │                            │                                  │
       │                            ▼                                  │
       │                  [4. Verifier Agent] ─────────────────────────┘
       │                            │
       └─ (Syntax / Test Regress) ──┤ (Pass Tests & Clean Invariants)
                                    ▼
                      [24% pass@1 SWE-bench-lite Verified PR]
```

---

### 🏢 **Luminary**
**Software Developer Intern** • *Remote* • `Apr 2025 – Sept 2025`  
*Focus: Event-Driven Microservices & Distributed Systems*

* **Distributed Kafka Saga Orchestration:** Engineered asynchronous event consumers and distributed transaction workflows using **Apache Kafka** and **FastAPI**. Implemented orchestrator-based Saga patterns with idempotent event handling and dead-letter queues (DLQ), guaranteeing strict data consistency across distributed billing, inventory, and fulfillment states.
* **PostgreSQL Throughput & Latency Optimization:** Optimized high-traffic relational database queries and connection handling in PostgreSQL. Configured **PgBouncer connection pooling**, eliminated N+1 query patterns using eager prefetching, and added composite indices on high-cardinality access paths, driving a **38.2% reduction in p95 read latency (340ms → 210ms)** under simulated 1,500 req/s loads.
* **Full-Stack Observability & CI/CD Pipelines:** Developed real-time administrative dashboards and deployment automation using **React, Next.js, and Docker**. Implemented WebSocket channels backed by **Redis pub/sub** for live event streaming, and authored GitHub Actions CI/CD pipelines incorporating **Vitest** unit tests, **Playwright** E2E test suites, and **OpenTelemetry** distributed tracing.

---

<a id="flagship-architectures"></a>
## 🚀 Flagship Open Source & Eval Architectures

### 1. [AgentGate](https://github.com/Yashkumarverma623/AgentGate) — Statistical CI Regression Gate for Tool-Using LLM Agents
> **Deterministic statistical gate preventing silent capability regressions in multi-turn tool-calling agents.**

[![Python](https://img.shields.io/badge/Python-3.10%2B-3776AB?style=flat-square&logo=python&logoColor=white)](https://github.com/Yashkumarverma623/AgentGate)
[![tau-bench](https://img.shields.io/badge/Benchmark-tau--bench%20Retail-blueviolet?style=flat-square)](https://github.com/sierra-research/tau-bench)
[![State](https://img.shields.io/badge/Storage-SQLite%20(WAL)-003B57?style=flat-square&logo=sqlite&logoColor=white)](https://github.com/Yashkumarverma623/AgentGate)
[![CI](https://img.shields.io/badge/CI%2FCD-GitHub%20Actions-2088FF?style=flat-square&logo=githubactions&logoColor=white)](https://github.com/Yashkumarverma623/AgentGate)
[![Tests](https://img.shields.io/badge/Tests-33%20Passing-10B981?style=flat-square&logo=pytest&logoColor=white)](https://github.com/Yashkumarverma623/AgentGate)

* **Statistical Hypothesis Testing:** Replaced fragile percentage-threshold heuristics with rigorous paired statistical tests. Implemented **paired bootstrap resampling (10,000 iterations)** and **McNemar's exact test** on discordant pairs ($b$ vs $c$). Correctly classifies noisy small-sample drops as inconclusive ($p = 0.25$) while decisively blocking real regressions (e.g., 0/10 passing, $p = 0.002$) with non-zero CI exit codes.
* **Sierra `tau-bench` Retail Evaluation:** Established an empirical 30-trial baseline achieving **93.33% pass@1** (95% bootstrap CI: `[83.33%, 100%]`) on Sierra's multi-turn retail domain benchmark.
* **ACID State Engine & Leaky-Bucket Rate Pacing:** Engineered an ACID **SQLite WAL state engine** for idempotent, crash-resilient run resumption alongside a token/request leaky-bucket quota pacer that prevents rate exhaustion on free-tier APIs. Includes two-stage failure triage (deterministic checks → LLM judge) for zero-cost benchmark runs backed by 33 unit tests.

```
       [Pull Request Code Change] ──► [GitHub Actions CI Gate]
                                              │
                                              ▼
                             [tau-bench Multi-Turn Simulation]
                                              │
                      ┌───────────────────────┴───────────────────────┐
                      ▼                                               ▼
         [Deterministic State Checker]                    [LLM Judge Secondary Check]
                      │                                               │
                      └───────────────────────┬───────────────────────┘
                                              ▼
                                 [SQLite WAL State Storage]
                                              │
                                              ▼
                      [Paired Bootstrap (10k iters) & McNemar's Test]
                                              │
                      ┌───────────────────────┴───────────────────────┐
                      ▼                                               ▼
         [Inconclusive Variance (p=0.25)]                [Statistically Proven Regression (p=0.002)]
               (Soft PR Warning)                                   (Hard PR Block ❌)
```

---

### 2. [rag-bench](https://github.com/Yashkumarverma623/rag-bench) — Reproducible Retrieval & RAG Benchmark with FWER Corrections
> **Empirical benchmark of 16 retrieval configurations across BEIR benchmarks with honest reporting of null results.**

[![Python](https://img.shields.io/badge/Python-3.10%2B-3776AB?style=flat-square&logo=python&logoColor=white)](https://github.com/Yashkumarverma623/rag-bench)
[![BEIR](https://img.shields.io/badge/Dataset-BEIR%20(SciFact%20%2B%20NFCorpus)-FF6F00?style=flat-square)](https://github.com/beir-cellar/beir)
[![Vector](https://img.shields.io/badge/Vector%20Index-Faiss%20HNSW-00599C?style=flat-square)](https://github.com/Yashkumarverma623/rag-bench)
[![Reranking](https://img.shields.io/badge/Reranker-Cross--Encoder-green?style=flat-square)](https://github.com/Yashkumarverma623/rag-bench)
[![Stats](https://img.shields.io/badge/Correction-Holm--Bonferroni-8A2BE2?style=flat-square)](https://github.com/Yashkumarverma623/rag-bench)

* **16 Retrieval Pipelines Profiled:** Systematic evaluation across sparse (`BM25`), dense (`BGE-small` exact & Faiss HNSW), four hybrid score fusions (RRF, min-max normalization, CombSUM), and cross-encoder reranking on **BEIR SciFact** and **NFCorpus**.
* **Statistically Validated Gains:** Achieved **+13.8% nDCG@10 gain** on SciFact (0.6539 → 0.7444 over BM25; Holm-adjusted $p = 0.021$ vs pure dense) via min-max score fusion. Tuned hybrid RRF delivered **+17.1% nDCG@10 gain** on NFCorpus over baseline BM25.
* **Empirical Null Results & Production Trade-Offs:** Published critical negative findings: CPU cross-encoder reranking introduced a prohibitive **~7.7s p95 latency penalty** (vs `81ms` for hybrid fusion) with no statistically significant accuracy lift on SciFact; meanwhile, **Faiss HNSW matched exact flat search within 0.0033 nDCG@10** while delivering a 10× throughput increase.

```
                    [Query Input]
                          │
          ┌───────────────┴───────────────┐
          ▼                               ▼
    [BM25 Lexical]              [BGE-small Dense (Faiss HNSW)]
    (SciFact: 0.6539)           (Matched Exact within 0.0033 nDCG)
          │                               │
          └───────────────┬───────────────┘
                          ▼
            [Min-Max Hybrid Score Fusion]
                          │
          ┌───────────────┴───────────────┐
          ▼                               ▼
 [Production Hybrid Path]        [CPU Cross-Encoder Reranker]
  • nDCG@10: 0.7444 (+13.8%)      • nDCG@10: No stat-sig gain
  • Latency p95: 81ms             • Latency p95: ~7,700ms (95x slower)
  • Status: RECOMMENDED ✅         • Status: NULL RESULT DOCUMENTED ⚠️
```

---

### 3. [Autonomous-SWE-Agent](https://github.com/Yashkumarverma623/Autonomous-SWE-Agent) — Multi-Agent Issue-to-PR Engine with Tree-Sitter & Sandbox Verification
> **LangGraph cyclic multi-agent workflow for autonomous codebase navigation, patch synthesis, and regression verification.**

[![LangGraph](https://img.shields.io/badge/Orchestrator-LangGraph-blue?style=flat-square)](https://github.com/Yashkumarverma623/Autonomous-SWE-Agent)
[![Tree-sitter](https://img.shields.io/badge/Parser-Tree--sitter%20AST-orange?style=flat-square)](https://github.com/tree-sitter/tree-sitter)
[![Docker](https://img.shields.io/badge/Sandbox-Docker%20Containers-2496ED?style=flat-square&logo=docker&logoColor=white)](https://github.com/Yashkumarverma623/Autonomous-SWE-Agent)
[![Benchmark](https://img.shields.io/badge/Benchmark-SWE--bench--lite%20(24%25%20pass%401)-red?style=flat-square)](https://github.com/princeton-nlp/SWE-bench)

* **Multi-Agent Cyclic Architecture:** Built an issue-to-PR repair engine organizing specialized agents: `Planner` (deconstructs issue & formulates search strategy), `Localizer` (maps fault locations to exact AST spans), `Editor` (synthesizes minimal unified-diff patches), and `Verifier` (executes test suites in containerized sandboxes).
* **AST-Aware Repository Parsing:** Utilizes Tree-sitter grammars to chunk source code along concrete syntax boundaries (classes, methods, control blocks), preventing truncation of closing braces or context windows and reducing scope hallucinations by 35%.
* **Containerized Execution & Self-Healing:** Dispatches synthesized patches into ephemeral Docker sandboxes with strict cgroup limits. Automatically feeds compiler errors, test tracebacks, and assertion failures back to the Editor agent across up to 3 repair iterations, achieving **24% pass@1 resolution rate on SWE-bench-lite (50-task split)**.

---

### 4. [tweakcn-mcp](https://github.com/Yashkumarverma623/tweakcn-mcp) — Model Context Protocol (MCP) Server for UI Generation & Theme Customization
> **Model Context Protocol server connecting LLM agents to shadcn/ui design tokens and deterministic theme transformations.**

[![Protocol](https://img.shields.io/badge/Protocol-Model%20Context%20Protocol%20(MCP)-blueviolet?style=flat-square)](https://modelcontextprotocol.io/)
[![TypeScript](https://img.shields.io/badge/Language-TypeScript-3178C6?style=flat-square&logo=typescript&logoColor=white)](https://github.com/Yashkumarverma623/tweakcn-mcp)
[![shadcn/ui](https://img.shields.io/badge/Components-shadcn%2Fui-000000?style=flat-square&logo=shadcnui&logoColor=white)](https://ui.shadcn.com/)
[![Validation](https://img.shields.io/badge/Schema-Zod%20Validation-3E67B1?style=flat-square&logo=zod&logoColor=white)](https://github.com/Yashkumarverma623/tweakcn-mcp)

* **Full MCP Server Implementation:** Exposes MCP tool, prompt, and resource primitives conforming to the official Model Context Protocol specification, allowing coding agents (Claude Desktop, Antigravity, Cursor) to interactively inspect, theme, and scaffold components.
* **Deterministic AST Theme Manipulation:** Modifies Tailwind configuration files and CSS variable palettes using TypeScript AST parsers, avoiding messy string replacement errors and guaranteeing syntactically valid theme configurations.
* **Zod Schema Verification & WCAG Contrast Checks:** Every generated color palette and component variant undergoes runtime Zod schema validation and automated WCAG 2.1 AA color contrast ratio calculations before being written to disk.

---

<a id="research-publications"></a>
## 📜 Research & Publications

### 📄 **Agentic RAG for Domain-Specific Knowledge Retrieval**
* **Authors:** Yash Kumar Verma et al.  
* **Accepted At:** **ICCTDN-2026** (*International Conference on Communication, Technological Advancements and Digital Network*)  
* **Proceedings Indexing:** Springer Lecture Notes in Networks and Systems (**Springer LNNS**)  
* **Core Contribution:** Formulates an adaptive multi-agent retrieval architecture that overcomes multi-hop reasoning failures and knowledge degradation in domain-specific technical corpora through cyclic verification and reciprocal rank score fusion.

---

<a id="technical-arsenal"></a>
## 🛠️ Technical Arsenal

<div align="center">

### 🧠 Agentic AI, LLMs & Evaluation
![LangGraph](https://img.shields.io/badge/LangGraph-1C3C3C?style=for-the-badge&logo=langchain&logoColor=white)
![MCP](https://img.shields.io/badge/Model%20Context%20Protocol-4B0082?style=for-the-badge&logo=code&logoColor=white)
![vLLM](https://img.shields.io/badge/vLLM%20(PagedAttention)-3B82F6?style=for-the-badge&logo=nvidia&logoColor=white)
![tau-bench](https://img.shields.io/badge/tau--bench-6B21A8?style=for-the-badge&logo=target&logoColor=white)
![Ragas](https://img.shields.io/badge/Ragas%20Evals-10B981?style=for-the-badge&logo=checkmarx&logoColor=white)
![OpenAI](https://img.shields.io/badge/OpenAI%20API-412991?style=for-the-badge&logo=openai&logoColor=white)
![Google Gemini](https://img.shields.io/badge/Google%20Gemini-886CE4?style=for-the-badge&logo=google&logoColor=white)
![Hugging Face](https://img.shields.io/badge/Hugging%20Face-FFD21E?style=for-the-badge&logo=huggingface&logoColor=black)
![QLoRA](https://img.shields.io/badge/QLoRA%20Fine--Tuning-EC4899?style=for-the-badge&logo=pytorch&logoColor=white)
![Llama 3.1](https://img.shields.io/badge/Meta%20Llama%203.1-0668E1?style=for-the-badge&logo=meta&logoColor=white)

### 🔍 RAG, Search & Guardrails
![Hybrid Search](https://img.shields.io/badge/BM25%20%2B%20Dense%20Hybrid-0284C7?style=for-the-badge&logo=searxng&logoColor=white)
![Faiss](https://img.shields.io/badge/Faiss%20HNSW-00599C?style=for-the-badge&logo=facebook&logoColor=white)
![ChromaDB](https://img.shields.io/badge/ChromaDB-FF6600?style=for-the-badge&logo=databricks&logoColor=white)
![Reranking](https://img.shields.io/badge/Cross--Encoder%20Reranking-059669?style=for-the-badge&logo=fastapi&logoColor=white)
![RRF](https://img.shields.io/badge/Reciprocal%20Rank%20Fusion-7C3AED?style=for-the-badge&logo=scipy&logoColor=white)
![Presidio](https://img.shields.io/badge/Microsoft%20Presidio%20PII-0078D4?style=for-the-badge&logo=microsoft&logoColor=white)
![Tree-sitter](https://img.shields.io/badge/Tree--sitter%20AST-1F2937?style=for-the-badge&logo=git&logoColor=white)

### ⚡ Backend, Systems & Databases
![Python](https://img.shields.io/badge/Python%203.10%2B-3776AB?style=for-the-badge&logo=python&logoColor=white)
![FastAPI](https://img.shields.io/badge/FastAPI-009688?style=for-the-badge&logo=fastapi&logoColor=white)
![Node.js](https://img.shields.io/badge/Node.js-339933?style=for-the-badge&logo=node.js&logoColor=white)
![Express](https://img.shields.io/badge/Express-000000?style=for-the-badge&logo=express&logoColor=white)
![Apache Kafka](https://img.shields.io/badge/Apache%20Kafka%20(Saga)-231F20?style=for-the-badge&logo=apachekafka&logoColor=white)
![Redis](https://img.shields.io/badge/Redis%20Pub%2FSub-DC382D?style=for-the-badge&logo=redis&logoColor=white)
![PostgreSQL](https://img.shields.io/badge/PostgreSQL%20%2B%20PgBouncer-4169E1?style=for-the-badge&logo=postgresql&logoColor=white)
![SQLite](https://img.shields.io/badge/SQLite%20WAL-003B57?style=for-the-badge&logo=sqlite&logoColor=white)

### 🎨 Frontend & Design Engineering
![TypeScript](https://img.shields.io/badge/TypeScript-3178C6?style=for-the-badge&logo=typescript&logoColor=white)
![JavaScript](https://img.shields.io/badge/JavaScript%20(ES2022%2B)-F7DF1E?style=for-the-badge&logo=javascript&logoColor=black)
![React](https://img.shields.io/badge/React%2018%2F19-61DAFB?style=for-the-badge&logo=react&logoColor=black)
![Next.js](https://img.shields.io/badge/Next.js-000000?style=for-the-badge&logo=next.js&logoColor=white)
![Tailwind CSS](https://img.shields.io/badge/Tailwind%20CSS-06B6D4?style=for-the-badge&logo=tailwindcss&logoColor=white)
![shadcn/ui](https://img.shields.io/badge/shadcn%2Fui-000000?style=for-the-badge&logo=shadcnui&logoColor=white)

### 🛠️ Infrastructure, DevOps & Testing
![Docker](https://img.shields.io/badge/Docker-2496ED?style=for-the-badge&logo=docker&logoColor=white)
![GitHub Actions](https://img.shields.io/badge/GitHub%20Actions%20CI%2FCD-2088FF?style=for-the-badge&logo=githubactions&logoColor=white)
![AWS](https://img.shields.io/badge/AWS%20(EC2%20%7C%20Lambda)-232F3E?style=for-the-badge&logo=amazonwebservices&logoColor=white)
![Playwright](https://img.shields.io/badge/Playwright%20E2E-2EAD33?style=for-the-badge&logo=playwright&logoColor=white)
![Vitest](https://img.shields.io/badge/Vitest-6E9F18?style=for-the-badge&logo=vitest&logoColor=white)
![pytest](https://img.shields.io/badge/pytest-0A9EDC?style=for-the-badge&logo=pytest&logoColor=white)
![mypy](https://img.shields.io/badge/mypy%20Strict-2A6DB0?style=for-the-badge&logo=python&logoColor=white)
![Linux](https://img.shields.io/badge/Linux%20Ubuntu-FCC624?style=for-the-badge&logo=linux&logoColor=black)

</div>

---

<a id="github-analytics"></a>
## 📈 GitHub Activity & Analytics

<div align="center">

### 🐍 Contribution Activity Stream
<picture>
  <source media="(prefers-color-scheme: dark)" srcset="https://raw.githubusercontent.com/Yashkumarverma623/YashKumarVerma623/output/github-snake-dark.svg">
  <source media="(prefers-color-scheme: light)" srcset="https://raw.githubusercontent.com/Yashkumarverma623/YashKumarVerma623/output/github-snake.svg">
  <img alt="Yash's GitHub contribution snake animation" src="https://raw.githubusercontent.com/Yashkumarverma623/YashKumarVerma623/output/github-snake.svg" width="100%" />
</picture>

<br/><br/>

### 📊 Repository & Coding Metrics
<p align="center">
  <img src="https://github-readme-stats.vercel.app/api?username=Yashkumarverma623&show_icons=true&theme=tokyonight&hide_border=true" width="49%" alt="Yash's GitHub Stats" />
  <img src="https://streak-stats.demolab.com?user=Yashkumarverma623&theme=tokyonight&hide_border=true&border_radius=8" width="49%" alt="Yash's GitHub Streak" />
</p>

<p align="center">
  <img src="https://github-readme-stats.vercel.app/api/top-langs/?username=Yashkumarverma623&layout=compact&theme=tokyonight&hide_border=true" width="55%" alt="Top Languages" />
</p>

</div>

---

## 🏆 Honors & Hackathons

* 🥇 **Winner, 10+ Hackathons:** Secured First Place in 10+ collegiate, inter-college, and regional hackathons across Delhi NCR spanning Agentic AI systems, automated developer tooling, and distributed full-stack tracks.
* 🎓 **Academic Foundation:** Bachelor of Technology in Computer Science & Engineering (Vishveshwarya Group of Institutions, Greater Noida, UP • GPA: 7.87 / 10.0 • Sep 2022 – Jun 2026).

---

<a id="connect-collaborate"></a>
## 📬 Connect & Collaborate

I am actively engaging with **AI research teams, high-growth AI startups, and systems engineering groups** building production-grade agentic frameworks, high-throughput RAG infrastructure, and deterministic evaluation gates.

* 💼 **LinkedIn:** [linkedin.com/in/yash-kumar-verma623](https://www.linkedin.com/in/yash-kumar-verma623)
* 📧 **Email:** [yashkumarverma623@gmail.com](mailto:yashkumarverma623@gmail.com)
* 🐙 **GitHub:** [github.com/Yashkumarverma623](https://github.com/Yashkumarverma623)
* 📍 **Location:** Jamshedpur, Jharkhand, India *(Available immediately for full-time roles • Open to relocation across India & remote global teams)*

<div align="center">
  <sub>Engineered with precision for determinism, scale, and statistical integrity. © 2026 Yash Kumar Verma.</sub>
</div>
