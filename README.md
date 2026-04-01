# AgentAppFlow

Open-source ecosystem for local, project-aware AI development workflows.

## Repositories
- [agentappflow-app](https://github.com/RINNECODER/agentappflow-app): primary product repo and Mac-first local control center.
- [agentappflow-plugins](https://github.com/RINNECODER/agentappflow-plugins): plugin architecture and integrations.
- [agentappflow-skills](https://github.com/RINNECODER/agentappflow-skills): reusable developer skills and workflows.
- [agentappflow-cli](https://github.com/RINNECODER/agentappflow-cli): command-line automation and scaffolding tools.
- [agentappflow-docs](https://github.com/RINNECODER/agentappflow-docs): docs, architecture, and onboarding.

## Product Direction
- `agentappflow-app` is the canonical product hub.
- The app is Mac-first in UX today, but the product name stays OS-neutral for future expansion.
- Runtime architecture is local-only: Swift UI, Python orchestration, Rust execution guardrails.
- Managed projects store their framework state inside `.agentappflow/` within each user repo.

## Branching Strategy
- `main`: stable baseline
- `dev`: active development

## License
MIT (see [LICENSE](./LICENSE)).
