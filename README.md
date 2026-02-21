# RotorERP

![License: MIT](https://img.shields.io/badge/License-MIT-green.svg)
![Build: SFDX](https://img.shields.io/badge/build-SFDX-blue.svg)
![Compliance: DORA | GDPR](https://img.shields.io/badge/compliance-DORA%20%7C%20GDPR-orange.svg)

> A beautiful, modular aviation leasing ERP built natively on Salesforce. Designed for the user; engineered for the enterprise.

## Philosophy

> "You've got to start with the customer experience and work backwards to the technology." — Steve Jobs

RotorERP is purpose-built for helicopter and aviation leasing operations. We believe enterprise software shouldn't require a training manual. Every screen, every workflow, and every automation is designed with one goal: **it just works.**

### Core Principles

- **Zero-Training UI** — If a leasing operator can't complete a billing run without reading a manual, we've failed
- **3-Click Rule** — No routine task should require more than 3 clicks
- **Aviation-Native Vocabulary** — MSN, Lease Identifier, Airframe, Flight Hours, Cycles, MRO, AOG
- **Modular by Default** — Install only what you need via Salesforce Unlocked Packages
- **Configuration over Customization** — Sensible, industry-standard defaults pre-loaded

## Quick Start

```bash
# 1. Clone the repository
git clone https://github.com/Clutch2View/RotorERP-Salesforce-Aviation-Leasing-Modules.git
cd RotorERP-Salesforce-Aviation-Leasing-Modules

# 2. Authenticate with your Salesforce DevHub
sf org login web --set-default-dev-hub --alias DevHub

# 3. Create a scratch org
sf org create scratch --definition-file config/project-scratch-def.json --alias RotorERP --duration-days 30 --set-default

# 4. Open the org
sf org open --target-org RotorERP
```

## Architecture

- **Selector Layer** — SOQL queries and data retrieval
- **Domain Layer** — Trigger handlers and record validation
- **UI Layer** — Lightning Web Components (LWC) only

All modules are packaged as **Salesforce Unlocked Packages (2GP)** under the `rotorerp` namespace.

## Enterprise Integrations

RotorERP natively supports the **Microsoft 365 E5** technology stack:

- **Entra ID (Azure AD)** — SSO and JIT provisioning via permission set mapping
- **SharePoint Online** — Heavy document storage via Salesforce Files Connect
- **Microsoft Teams** — Adaptive Cards for Stage 1 & Stage 2 approval workflows
- **Power BI Premium** — Structured OData/REST APIs for analytics
- **Microsoft Purview** — Data classification mapping for enterprise DLP

## Security & Compliance

This system is architected to meet strict European financial standards:

- **DORA** — Immutable audit trails, strict access controls, incident logging
- **GDPR** — Data classification metadata, Shield encryption readiness, Right to be Forgotten flows
- **SAF-T / GoBD** — Multi-book accounting with localized compliance format support

See [SECURITY.md](SECURITY.md) for full details.

## License

Distributed under the **MIT License**. See `LICENSE` for more information.

---

*Built with precision for aviation. Powered by Salesforce.*
