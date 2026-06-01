# Assumptions

## Product Assumptions

- [ ] Users prefer quality + relevance over volume
- [ ] Source quality can be evaluated algorithmically (even imperfectly)
- [ ] LLM-generated summaries are useful for news curation
- [ ] Users will provide feedback to improve relevance over time
- [ ] Epistemic assistance (confidence, contradiction detection) adds measurable value

## Technical Assumptions

- [ ] Modern LLMs (Claude, GPT-4) are sufficient for news summarization and evaluation
- [ ] Feed aggregation APIs (RSS, etc.) are reliable enough for MVP
- [ ] User context can be captured and stored efficiently
- [ ] Lightweight fact-checking is possible without external APIs
- [ ] Local or cloud-hosted deployment is sufficient (no need for edge computing)

## Methodological Assumptions

- [ ] Spec-driven development reduces rework and technical debt
- [ ] Observable systems are easier to debug and improve than black boxes
- [ ] Explicit benchmarks clarify success better than vague goals
- [ ] AI-assisted development can be systematic, not just exploratory
- [ ] This methodology will produce sustainable, maintainable code

## Market Assumptions

- [ ] There is unmet demand for epistemic news assistance (beyond engagement optimization)
- [ ] Target users will adopt a tool that reduces information overload
- [ ] Word-of-mouth growth is possible if the tool is genuinely useful
- [ ] The project can stay small and focused (resist feature bloat)

## Learning Assumptions

- [ ] Building this project will reveal gaps in AI-assisted SDLC methodology
- [ ] Tool evaluation (Copilot vs. Claude vs. ChatGPT) will be actionable
- [ ] Published learnings will be valuable to others experimenting with AI + SDLC

---

## Validation Plan

Each assumption should have an associated test or benchmark:

| Assumption | Test | Success Criteria |
|-----------|------|------------------|
| LLMs are sufficient for summarization | Build POC; evaluate summaries manually | 80%+ of summaries rated "useful" |
| Source quality can be evaluated | Build source scorer; compare to manual evaluation | 70%+ agreement with human judgment |
| Users prefer quality over volume | Survey/interview target users | 70%+ prioritize relevance over breadth |
| Observable systems are easier to maintain | Measure debug time on observed vs. unobserved features | 50%+ faster debugging with observability |

---

## Assumptions to Challenge

- Is "epistemic assistance" actually what users want, or is it marketing?
- Can we avoid feature creep and stay focused on the core MVP?
- Is solo development sustainable, or will bottlenecks emerge?
- Will the knowledge-centric repo structure actually improve development, or add overhead?
