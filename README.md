<p align="center">
  <img src="./assets/agentappflow-hero.png" alt="AgentAppFlow hero banner" width="100%" />
</p>

<h1 align="center">AgentAppFlow</h1>

<p align="center">
  Local-first infrastructure for project-aware AI development workflows.
</p>

<p align="center">
  <a href="https://github.com/RINNECODER/agentappflow-app"><img src="https://img.shields.io/badge/product-agentappflow--app-0f172a?style=for-the-badge" alt="Product Repo"></a>
  <img src="https://img.shields.io/badge/platform-macOS--first-2563eb?style=for-the-badge" alt="macOS First">
  <img src="https://img.shields.io/badge/runtime-local--only-0f766e?style=for-the-badge" alt="Local Only">
  <img src="https://img.shields.io/badge/ui-swift-f97316?style=for-the-badge" alt="Swift">
  <img src="https://img.shields.io/badge/core-python-1d4ed8?style=for-the-badge" alt="Python">
  <img src="https://img.shields.io/badge/executor-rust-b45309?style=for-the-badge" alt="Rust">
  <a href="./LICENSE"><img src="https://img.shields.io/badge/license-MIT-111827?style=for-the-badge" alt="MIT License"></a>
</p>

## What Is AgentAppFlow?

AgentAppFlow is an open-source system for turning AI coding tools into project-aware, guardrailed collaborators.

The product direction is simple:
- a Mac-first app handles onboarding, controls, approvals, and project visibility
- a Python orchestration core manages AI workflows, memory, and retrospectives
- a Rust execution layer enforces guarded local actions and policy boundaries
- every managed project keeps its framework state inside `.agentappflow/` so the setup stays visible, portable, and local

The result is a local development workflow where AI agents can operate with project memory, repeatable rules, and controlled self-improvement without depending on a backend.

## Why This Exists

Most AI coding tools are powerful but stateless, inconsistent, and weak at preserving project-specific working patterns over time.

AgentAppFlow is designed to close that gap by combining:
- local project memory inspired by tools like Claude-Mem
- specialized internal agent roles inspired by systems like HyperAgent
- explicit repo-level framework state that can evolve with the project
- approval-aware guardrails so automation stays useful without going rogue

## Architecture At A Glance

```text
Swift macOS app
  -> onboarding, project registration, approvals, history, framework health

Python core
  -> planning, memory, retrieval, retrospectives, framework proposals

Rust executor
  -> guarded execution, filesystem policy, diff validation, audit trail

Managed repo
  -> .agentappflow/
```

Core principles:
- local-first, no backend required
- Mac-first UX today, OS-neutral product direction long term
- Python owns AI cognition
- Rust owns risky local execution boundaries
- project memory stays visible instead of disappearing into a black box

## Repository Map

This repository is the ecosystem index. The main product repo is `agentappflow-app`.

- [agentappflow-app](https://github.com/RINNECODER/agentappflow-app): primary product repo and Mac-first local control center
- [agentappflow-docs](https://github.com/RINNECODER/agentappflow-docs): deeper architecture, memory design, and adapter conventions
- [agentappflow-cli](https://github.com/RINNECODER/agentappflow-cli): command-line automation and scaffolding tools
- [agentappflow-plugins](https://github.com/RINNECODER/agentappflow-plugins): plugin architecture and integrations
- [agentappflow-skills](https://github.com/RINNECODER/agentappflow-skills): reusable developer skills and workflows

## Project Contract

Every managed user repo is expected to contain:

```text
.agentappflow/
  project.yaml
  rules/
  templates/
  sessions/
  retros/
  proposals/
  cache/
```

This is the shared contract that lets tools like Codex and Claude Code discover project context, follow rules, reuse memory, and participate in controlled framework evolution.

## Current Status

AgentAppFlow is in the architecture and product-foundation phase.

Current focus:
- defining the app-first product direction
- locking the Swift/Python/Rust runtime split
- designing the `.agentappflow/` project framework layout
- preparing the first implementation slice for onboarding and project bootstrap

## Branching

- `main`: stable baseline
- `dev`: active development

## License

MIT. See [LICENSE](./LICENSE).

## Star History

[![Star History Chart](https://api.star-history.com/svg?repos=RINNECODER/agentappflow&type=Date)](https://www.star-history.com/#RINNECODER/agentappflow&Date)
