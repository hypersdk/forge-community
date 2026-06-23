# Forge — Community

> **GPU & AI infrastructure fabric for Kubernetes — autonomous placement, FinOps, Zeus AI ops engineer**

Public issue tracker and community feedback space for **Forge** by [Zyvor AI Labs](https://zyvor.dev).

The source code is maintained in a private repository. This repo is for:
- Bug reports
- Feature requests
- UX feedback
- Documentation gaps
- Questions and discussion

---

## Key features

- 7 Kubernetes operators — GPU, AI, storage, network, quota, network-intelligence, virtualization
- 60+ CRDs for GPU fleet, AI workloads, and cost management
- Zeus AI embedded ops engineer — grounded answers, approval-gated actions
- FinOps — chargebacks, budget guardian, cost attribution per team/workload
- Model catalog, RAG studio, inference gateway, training factory
- 24 eBPF programs for GPU and network telemetry
- 94-page React UI, 25-module Rust CLI, Python & Go SDKs
- Multi-cluster federation and Velero DR

---

## Installation

Forge runs on any Kubernetes cluster — EKS, GKE, AKS, k3s, kubeadm.

**Standalone install:**
```bash
git clone https://github.com/hypersdk/forge && cd forge
./scripts/install-standalone.sh
```

**Helm:**
```bash
helm repo add hypersdk https://charts.hypersdk.dev
helm upgrade --install forge hypersdk/forge-core \
  --namespace forge-system --create-namespace
```

**Requirements:** Kubernetes 1.28+, NVIDIA GPU nodes with DCGM (for GPU features), 8 GB RAM for control plane

---

## Report a bug

[Open a Bug Report →](../../issues/new?template=bug_report.yml)

Include: what you did, what happened, what you expected, your environment, and screenshots/logs (redact secrets).

## Request a feature

[Open a Feature Request →](../../issues/new?template=feature_request.yml)

## UX feedback

[Open a UX Feedback →](../../issues/new?template=ux_feedback.yml)

## Ask a question

Use [GitHub Discussions](../../discussions) for open-ended questions, ideas, and roadmap conversations.

---

## Security

**Do not report security vulnerabilities publicly.**

Email **security@zyvor.dev** — see [SECURITY.md](SECURITY.md).

---

## Do not post

- Source code or internal configuration
- API tokens, license keys, or credentials  
- Private logs with sensitive data
- Security vulnerabilities (email security@zyvor.dev)

---

Maintained by [Zyvor AI Labs](https://zyvor.dev)
