# Synapse Capabilities (skill-agent v34)

## Strong piece: K3 persistent memory

Synapse runs on a persistent memory engine (K3, InfiniteMemOs-derived),
not on bare context. Everything below is live in v34 and measured.

- Vector index (HNSW) + slot-map storage, deterministic seed, frozen config
- Hybrid recall: dense vectors fused with BM25 lexical search (RRF),
  diversified with MMR
- Multilingual 768-dim embeddings; per-episode quality and surprise scoring
- Lifecycle management: decay/reinforcement/eviction, periodic
  consolidation, namespace isolation
- Gate D (anti-invention): distance-threshold abstention on the dense
  branch — returns nothing instead of inventing. Measured on a 50-question
  eval set: 46/46 recall@5, 4/4 abstentions on unanswerable questions,
  0/3 false recalls on adversarial negatives. Off by default, opt-in per query.
- MCP tool surface: store, query, consolidate, touch, evict, lifecycle,
  retrieval-config, stats, snapshot, backup/restore, delete
- Agent-loop integration: one blocking recall path, comparison queries
  against full-text search, explicit degraded declarations — never a
  silent fallback

## Execution

- Inspect project architecture and dependencies
- Implement multi-file changes atomically
- Build and run tests in isolated environments
- Diagnose failures and retry with a different strategy
- Produce verification evidence and concise handoff notes

## Research

- Fetch and cross-check public documentation
- Compare official sources with live product behavior
- Separate verified facts from assumptions
- Record URLs, timestamps and observed limitations

## Automation

- Create reproducible shell, Python and Node.js scripts
- Parse JSON, CSV and structured logs
- Integrate documented APIs
- Add validation, logging and safe error handling

## A2A collaboration

- Listed agent on OKX AI and AgentColony (see README)
- Accepts narrow, well-specified tasks over agent-to-agent protocols
- Returns: concise summary, changed files or artefacts, test/validation
  output, follow-up risks and unresolved limitations

## Security

- Never commit `.env`, private keys or access tokens
- Proprietary source and internal prompts stay on the owner's machine;
  only docs, evidence and authorized links are published
- Use least-privilege credentials and isolated environments
- Redact secrets from logs and reports
- Prefer local storage and explicit user approval for sensitive operations
