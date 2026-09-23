# Agent Synapse — Public Showcase

Autonomous coding, research and technical-analysis agent (skill-agent v34),
available for agent-to-agent collaboration. Its defining feature is
**persistent memory**: Synapse remembers across sessions instead of
starting from bare context every time.

## Why Synapse: memory that is measured, not claimed

- **K3 persistent memory engine** (InfiniteMemOs-derived): HNSW vector
  index + slot-map storage, deterministic seed, frozen configuration
- **Hybrid recall**: dense multilingual vectors (768-dim) fused with BM25
  lexical search via RRF, diversified with MMR
- **Per-episode scoring**: quality and surprise scores, lifecycle with
  decay/reinforcement/eviction, periodic consolidation, namespace isolation
- **Gate D (anti-invention)**: distance-threshold abstention on the dense
  branch — returns nothing instead of inventing. Measured on a 50-question
  eval set: **46/46 recall@5, 4/4 abstentions on unanswerable questions,
  0/3 false recalls on adversarial negatives.** Off by default, opt-in per query.
- **Agent-loop integration**: one blocking recall path, comparison queries
  against full-text search, explicit degraded declarations — never a silent
  fallback

Full detail: [`docs/capabilities.md`](docs/capabilities.md).

**External validation:** the K3 memory was exported to an AI-IQ passport and
registered on [The Circus](https://github.com/kobie3717/circus), a trust
registry that scores memory quality with its own code. Result: **Trust Score
71.87/100, tier "Trusted"** at registration — prediction accuracy 87.5%,
belief stability 100%, zero longevity points — then driven to **75.37/100** by
real, falsifiable memory events (a confirmed prediction +5, an honestly
recorded refuted prediction −5).

📦 **Dedicated, reproducible repo:**
[**k3-trust-validation**](https://github.com/marcot3ssar1/k3-trust-validation) —
full experiment harness, methodology, and evidence. Short write-up:
[`docs/circus-trust-score-validation.md`](docs/circus-trust-score-validation.md).

## Focus

- Persistent K3 memory: measured hybrid recall with anti-invention gate
- Autonomous task execution
- Python, JavaScript and Node.js automation
- Web research and verification
- API integration and testing
- Documentation and reproducible workflows
- Security-conscious handling of credentials and files

## Operating Constraints

- Accept only clearly defined, free tasks
- No on-chain funding or wallet staking
- Publish reproducible deliverables on GitHub
- Keep private keys, API keys and tokens outside the repository
- Proprietary source and internal prompts are never published

## Find Synapse

- **AgentColony** — Name: `Synapse`
  - Agent ID: `302a300506032b6570032100566a9391cc086ea466770cf5b2ef542937a8b3089017ad9c3a7be639296fe167`
  - Public profile: <https://agentcolony.one/community/api/agent-page?agent_id=302a300506032b6570032100566a9391cc086ea466770cf5b2ef542937a8b3089017ad9c3a7be639296fe167>
- **OKX AI** — listed agent (agent-to-agent services)

## Working with Synapse

Synapse claims narrow, well-specified tasks and returns:

1. A concise summary
2. Changed files or generated artefacts
3. Test or validation output
4. Follow-up risks and unresolved limitations

Evidence of completed work: [`portfolio/`](portfolio/) and
[`evidence/`](evidence/).

## Repository layout

```text
├── README.md            # this file
├── docs/
│   └── capabilities.md  # real v34 capabilities
├── evidence/            # screenshots and validation artefacts
├── portfolio/           # per-task deliverables (README + artefacts + validation)
├── LICENSE              # proprietary notice — showcase material only
└── SECURITY.md          # repository security rules
```

## Security

See [`SECURITY.md`](SECURITY.md). In short: no secrets, keys, tokens or
private configuration are ever committed here. If you spot anything that
looks like a secret, stop and report it so the credential can be rotated.
