# Veridexa
# VERIDEXA

**Audit-readiness infrastructure for AML decision governance.**

Most AML systems record what was decided. VERIDEXA preserves why it was defensible.

---

## The Problem

When the FCA knocks, regulated firms need to show not just what decisions were made — but why each one was defensible under the exact policy in force at that moment. Most AML platforms capture the outcome. None of them freeze the governance context.

The result: when an auditor asks a firm to reconstruct a decision from 18 months ago — including the policy version, risk appetite, evidence, and approval chain in force at the time — the answer requires days of manual investigation across multiple disconnected systems. Sometimes it is impossible.

This is not a tool failure. It is a structural gap that every regulated firm carries, quietly, until the moment it matters.

---

## What VERIDEXA Does

VERIDEXA sits above existing AML platforms as a lightweight governance layer. Every AML decision is captured as a permanent, tamper-evident record — linked to the exact policy version, risk appetite statement, evidence, and approval chain active at the moment the decision was made.

When a regulator or auditor requests reconstruction of any decision, the answer is retrievable in under 30 minutes.

> **"The challenge is rarely the absence of a decision. The challenge is preserving the decision rationale, the applicable policy framework, and the governance context in a way that remains accessible and defensible long after the original decision was made."**
>
> — Daniel Grant, AML & Compliance Professional, Wise

---

## Core Capabilities

| Capability | What It Does |
|---|---|
| **Decision capture** | Records every AML decision via REST API with RFC 3161 trusted timestamp and SHA-256 chain hash |
| **Policy version binding** | Links each decision to the exact frozen policy snapshot in force at capture time — not today's version |
| **Risk appetite linkage** | Freezes the applicable risk appetite statement at decision time alongside the decision record |
| **Evidence chain** | Attaches and hashes supporting documents permanently to each decision record |
| **Approval workflow** | Captures the full approval chain with timestamps, reasons, and information request history |
| **Audit replay** | Reconstructs any decision with full governance context — policy, evidence, approval chain — exactly as it existed at decision time |
| **Examination pack generator** | Generates a complete, signed, timestamped evidence pack for FCA supervisory visits in under 30 minutes |
| **Tamper-evident architecture** | Every record sealed with RFC 3161 timestamp and SHA-256 hash chain — no record can be altered without detection |

---

## Who It Is Built For

VERIDEXA is designed for FCA-regulated firms carrying personal MLRO liability and regulatory audit exposure:

- **Electronic Money Institutions (EMIs)**
- **Cryptoasset firms**
- **Payment institutions**
- **AML-supervised professional services firms** (law, accountancy, trust and company service providers)

---

## How It Works

VERIDEXA integrates with existing AML tooling via a REST API and webhook layer. Firms continue using their existing CDD and transaction monitoring systems. VERIDEXA captures the governance layer above them — the policy context, approval chain, and evidence record that existing tools do not preserve.

No replacement of existing infrastructure is required.

```
Existing AML tools          VERIDEXA governance layer
(CDD, TM, case mgmt)   →   Decision record + policy snapshot +
                            risk appetite + evidence + approval chain
                            → Tamper-evident, permanently sealed,
                              instantly retrievable
```

---

## Security and Infrastructure

- Hosted on **Azure UK South** (primary) with **Azure UK West** (disaster recovery)
- **AES-256 encryption** at rest, **TLS 1.3** in transit
- **RFC 3161** trusted timestamping on every record
- **SHA-256** hash chain linking all records
- **Azure Key Vault** for secrets management
- **RBAC** with role-based access across Analyst, Senior Officer, MLRO, Compliance Manager, IT Admin, and Auditor roles
- **SCIM 2.0** provisioning for enterprise identity management
- **WCAG 2.1 AA** accessibility compliance

---

## Technology Stack

| Layer | Technology |
|---|---|
| Backend | .NET 8 / ASP.NET Core Web API / C# |
| Frontend | React 18 + TypeScript + Vite |
| Database | Azure SQL Server + Entity Framework Core 8 |
| Queue | Azure Service Bus |
| Cache | Redis |
| Search | Azure Cognitive Search |
| Real-time | SignalR |
| Auth | ASP.NET Core Identity + JWT + TOTP/FIDO2 |
| CI/CD | GitHub Actions + SAST + Dependabot |

---

## Status

Platform development complete. Currently running structured practitioner validation conversations with senior compliance leaders across UK-regulated EMIs, payment institutions, and cryptoasset firms ahead of Q4 2026 pilot launch.

A 3-minute product demo is available on request.

---

## Contact

**Yogesh Dhungel**
Founder and Product Architect, VERIDEXA REGTECH LTD (prelaunch)

[LinkedIn](https://www.linkedin.com/company/veridexa) 
---

*VERIDEXA REGTECH LTD is incorporated in England and Wales. Source code is proprietary and not publicly available.*
