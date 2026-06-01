# Tools & Dependencies Under Evaluation

## LLM Platforms

| Tool | Status | Notes |
|------|--------|-------|
| **GitHub Copilot** | Evaluating | VS Code integration; code generation focus |
| **Claude (Anthropic)** | Evaluating | Long context window; strong reasoning |
| **GPT-4 (OpenAI)** | Evaluating | Broad capabilities; most mature |
| **Codex (OpenAI)** | Evaluating | Code-focused variant of GPT-3 |

**Goal:** Determine which tool(s) are best for each phase (prototyping, coding, documentation, test generation).

## Data & Knowledge Storage

| Tool | Status | Notes |
|------|--------|-------|
| **PostgreSQL** | Candidate | Structured data, JSONB for flexibility |
| **Vector DB (Pinecone, Weaviate)** | Candidate | Semantic search, embeddings |
| **LLM Memory (LangChain, LLamaIndex)** | Candidate | Long-term memory, RAG |

## Feed & Content APIs

| Tool | Status | Notes |
|------|--------|-------|
| **RSS Parser** | Standard library | Basic feed aggregation |
| **NewsAPI** | Candidate | Structured news aggregation |
| **Hacker News API** | Standard | Technical news source |
| **Twitter API** | Optional | Social signal for prioritization |

## Framework & Runtime

| Tool | Status | Notes |
|------|--------|-------|
| **Python** | Primary | LLM ecosystem, data science libs |
| **FastAPI** | Candidate | Modern async web framework |
| **Celery / Airflow** | Candidate | Task scheduling, DAGs |
| **Docker** | Standard | Containerization, deployment |

## Observability & Monitoring

| Tool | Status | Notes |
|------|--------|-------|
| **Structlog / Python logging** | Standard | Structured logs |
| **Prometheus** | Candidate | Metrics collection |
| **Grafana** | Candidate | Visualization |
| **Jaeger** | Candidate | Distributed tracing |

---

## Tool Evaluation Criteria

Every tool should be evaluated against:

1. **Fit for PENA:** Does it solve the problem better than alternatives?
2. **Learnability:** Can a solo dev adopt it quickly?
3. **Sustainability:** Is it maintained? Will it be around in 2 years?
4. **Cost:** Does it fit within budget constraints?
5. **Observability:** Can we instrument it for feedback?
6. **SDLC Integration:** Does it support spec-driven, knowledge-centric development?

---

## Known Unknowns

- Will LLM API costs be prohibitive at scale?
- Which vector DB is best for semantic search of news?
- How to balance local dev vs. cloud deployment?
- Can we achieve real-time aggregation, or is batch processing sufficient?
