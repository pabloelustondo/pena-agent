# Constraints

## Technical Constraints

- **API Rate Limits:** Feed aggregation services (RSS, news APIs) have rate limits
- **Latency:** Summary generation via LLM can take 5-30 seconds per article
- **Storage:** Need to store articles, summaries, metadata, user feedback
- **Token Budget:** LLM calls are expensive; must optimize context/token usage

## Scope Constraints

- **MVP Scope:** RSS feeds + web articles only (no social media, paywalled content, video)
- **Initial Content:** AI/tech news sources only (not general news)
- **User Base:** Single user or small cohort (not multi-tenant SaaS initially)
- **Deployment:** Local or simple cloud deployment (not enterprise infrastructure)

## Time/Resource Constraints

- **Solo Development:** Primarily one person
- **Iterative Learning:** Product emerges from experimentation, not upfront design
- **Budget:** Minimal—mostly API costs and open-source tools

## Methodological Constraints

- **Spec-Driven:** All features must start with a spec, not ad-hoc coding
- **Observable:** All code must include logging, metrics, tracing
- **Testable:** Every feature must have acceptance criteria tied to benchmarks
- **Documented:** Decisions, learnings, and evaluations are first-class artifacts

## Tool Constraints

- **LLM Availability:** Dependent on OpenAI API, Anthropic API, or similar
- **Feed Sources:** Limited to publicly available feeds and APIs
- **No Real-Time:** Will not support live event tracking or breaking news
- **No Guaranteed Accuracy:** LLM outputs require human judgment; not suitable for safety-critical decisions

## Organizational Constraints

- **Knowledge Base:** Project knowledge lives in this repo; no separate wiki or external documentation
- **Community:** Not an open-source project initially; focus on internal learning
- **Release Cadence:** Ad-hoc, iterative—not calendar-based releases
