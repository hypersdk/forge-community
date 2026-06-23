> 🚀 **Trial v0.30.0 is live!** The latest release is available for trial today — [get started in 5 minutes →](#try-v030-in-5-minutes)

# Forge — Community

> **GPU & AI infrastructure fabric for Kubernetes — autonomous placement, FinOps, Zeus AI ops engineer.**

![Version](https://img.shields.io/badge/version-v0.30.0-blue) ![Discussions](https://img.shields.io/github/discussions/hypersdk/forge-community) ![Issues](https://img.shields.io/github/issues/hypersdk/forge-community) ![License](https://img.shields.io/badge/license-Proprietary-red)

Public issue tracker and community feedback space for **Forge** by [Zyvor AI Labs](https://zyvor.dev).
The source code is maintained in a private repository. This repo is for bug reports, feature requests, UX feedback, and community discussion.

---

## What's new in v0.30

- Zeus AI approval gate GA — Zeus proposes remediation actions, operators approve with one click
- FinOps chargeback export — export per-team GPU cost reports to CSV, Slack, or S3
- RAG studio v2 — visual pipeline builder for retrieval-augmented generation workflows
- GPU scheduler preemption — high-priority training jobs can preempt lower-priority inference
- Multi-cluster federation v0.30 — unified placement and cost view across up to 20 clusters

---

## Why Forge

| Problem | Forge answer |
|---------|-------------|
| GPU clusters are opaque — no visibility without DCGM expertise | Live inventory, DCGM telemetry, MIG lifecycle, scheduling pools — out of the box |
| kubectl is too slow for GPU fleet ops | K8s console with SSE logs, WebSocket exec, drain progress, fleet health in one UI |
| AI infra spans too many disconnected tools | Model catalog, RAG studio, inference gateway, training factory — one control plane |
| Incidents need context across 6 tabs | Zeus AI embedded everywhere — grounded answers, approval-gated remediation |
| GPU cost and security are afterthoughts | FinOps chargebacks, budget guardian, SIEM export, threat hunting built in |

---

## Architecture

```
┌─────────────────────────────────────────────────────────────────────┐
│  Clients          Web UI · Rust CLI · Python/Go SDK                  │
├─────────────────────────────────────────────────────────────────────┤
│  AI Layer         Zeus · Model Router · Embedding · RAG Ingest       │
├─────────────────────────────────────────────────────────────────────┤
│  Intelligence     Placement · FinOps · RCA · Orchestrator · Topology │
├─────────────────────────────────────────────────────────────────────┤
│  Control Plane    7 Operators · 60+ CRDs · GPU scheduler · eBPF      │
└─────────────────────────────────────────────────────────────────────┘
```

---

## Try v0.30 in 5 minutes

```bash
# Standalone install (any Kubernetes cluster — EKS, GKE, AKS, k3s, kubeadm)
curl -fsSL https://releases.hypersdk.dev/forge/install.sh | FORGE_VERSION=0.30.0 bash

# Helm
helm repo add hypersdk https://charts.hypersdk.dev
helm upgrade --install forge hypersdk/forge-core --version 0.30.0 \
  --namespace forge-system --create-namespace
```

**Requirements:** Kubernetes 1.28+, NVIDIA GPU nodes with DCGM (for GPU features), 8 GB RAM for control plane

---

## Report a bug

[Open a Bug Report →](../../issues/new?template=bug_report.yml)

Include: what you did, what happened, what you expected, your environment, screenshots or logs (redact secrets).

## Request a feature

[Open a Feature Request →](../../issues/new?template=feature_request.yml)

## UX feedback

[Open a UX Report →](../../issues/new?template=ux_feedback.yml)

## Ask a question

Use [GitHub Discussions](../../discussions) for open-ended questions, ideas, and roadmap conversations.

---

## Security

**Do not report security vulnerabilities publicly.**
Email **security@zyvor.dev** — see [SECURITY.md](SECURITY.md).

---

## Do not post

- Source code, internal configs, or architecture details
- API tokens, license keys, or credentials
- Private logs with sensitive data
- Security vulnerabilities — email security@zyvor.dev instead

---

## Join the community

⭐ [Star this repo](https://github.com/hypersdk/forge-community) · 💬 [Open a Discussion](https://github.com/hypersdk/forge-community/discussions) · 🐛 [Report a Bug](../../issues/new?template=bug_report.yml) · 📧 [hello@zyvor.dev](mailto:hello@zyvor.dev)

Maintained by [Zyvor AI Labs](https://zyvor.dev)
