# Hi, I'm Valter

## Software Engineer | Full Stack, Cloud & DevOps

I build, deploy and operate full-stack applications, APIs and cloud infrastructure using TypeScript, Node.js, React and AWS.

Based in Medellín, Colombia · Authorized to work in Europe · Open to remote work and relocation.

**Portfolio:** [vzuliani97.github.io](https://vzuliani97.github.io): case studies with architecture, verification and real screenshots.

### Selected work

**[Yamesi Core](https://github.com/vzuliani97/yamesi): Business Operations & Traceability System**
[![Yamesi Core: point of sale with the store's catalog photos and the invoice panel](https://raw.githubusercontent.com/vzuliani97/yamesi/main/docs/screenshots/01-sell-invoices.png)](https://github.com/vzuliani97/yamesi)
For a real jewelry store: the demo runs on 44 pieces from its public catalog (reference, gold weight, size, price and photo). NestJS, React, PostgreSQL and S3-compatible storage. A Colombian-style invoice PDF for demonstration (19% VAT per line, CUFE and QR; not transmitted to the DIAN), an inventory portal with photo upload, gold traceability by lot, gap-free numbering under concurrency, a daily closing that locks the day, and an audit trail. 54 tests.
[Case study](https://vzuliani97.github.io/work/yamesi/) · [Source](https://github.com/vzuliani97/yamesi) · [Design walkthrough](https://github.com/vzuliani97/yamesi/blob/main/DESIGN_WALKTHROUGH.md)

**[OpsCircuit](https://github.com/vzuliani97/opscircuit): Cloud Delivery & Incident Automation Lab**
[![OpsCircuit: n8n incident workflow between Alertmanager and on-call](https://raw.githubusercontent.com/vzuliani97/opscircuit/main/docs/screenshots/n8n-incident-intake.png)](https://github.com/vzuliani97/opscircuit/tree/main/ops-automation)
- **Platform:** Kubernetes with GitOps (Argo CD), Prometheus/Grafana and security checks in CI.
- **Drills:** outage drills with a postmortem.
- **Incident workflow:** a self-hosted n8n workflow that validates, deduplicates, enriches and pages, with replayable dead letters and 15 integration tests in CI.
- **Terraform for AWS:** validated in CI, never applied.

[Case study](https://vzuliani97.github.io/work/opscircuit/) · [Source](https://github.com/vzuliani97/opscircuit) · [Incident lab verification](https://github.com/vzuliani97/opscircuit/blob/main/docs/INCIDENT_AUTOMATION_VERIFICATION.md) · [Postmortem](https://github.com/vzuliani97/opscircuit/blob/main/docs/incidents/2026-10-30-postmortem.md)

**[AtomicTrail](https://github.com/vzuliani97/atomictrail): Transaction Reliability Lab**
[![AtomicTrail: cashier with the store balance, top-up sales and a refunded rejection](https://raw.githubusercontent.com/vzuliani97/atomictrail/main/docs/screenshots/02-cashier-sale.png)](https://github.com/vzuliani97/atomictrail)
A TypeScript and PostgreSQL system that keeps balances correct under concurrent requests, retries, provider timeouts and reversals: idempotency, an append-only ledger, HMAC-signed integrations and real-time events. Live betting and a casino wallet are simulated scenarios. The concurrency evidence is a local, reproducible experiment, not a production benchmark.
[Case study](https://vzuliani97.github.io/work/atomictrail/) · [Source](https://github.com/vzuliani97/atomictrail) · [Concurrency experiment](https://github.com/vzuliani97/atomictrail/blob/main/docs/concurrency-experiment.md) · [Design walkthrough](https://github.com/vzuliani97/atomictrail/blob/main/DESIGN_WALKTHROUGH.md)

### Core stack

**Software:** TypeScript, Node.js, NestJS, React, Angular, SQL, PostgreSQL, REST APIs

**Cloud & delivery:** AWS, Docker, Kubernetes, Terraform, GitHub Actions, GitLab CI/CD, Linux

**Working knowledge (portfolio):** n8n, demonstrated in a self-hosted incident lab with authenticated webhooks, validation, deduplication, enrichment, retries and failure handling

### Contact

[Portfolio](https://vzuliani97.github.io) · [LinkedIn](https://www.linkedin.com/in/valter-zuliani-70152a97) · Systems Engineer (Universidad de Medellín) · Advanced Diploma in Cyber Security (Australia) · Spanish and Italian native, English C1

<sub>Portfolio projects are independent reconstructions with synthetic data and no employer code, AI-assisted and verified through tests and CI.</sub>
