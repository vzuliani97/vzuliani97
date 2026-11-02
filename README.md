<a href="https://vzuliani97.github.io"><img src="assets/banner.jpg" width="100%" alt="Valter Zuliani, Software Engineer: Full Stack, Cloud and DevOps. A terminal shows 54, 54 and 15 passing tests in three repositories and a Lighthouse score of 100."></a>

<p align="center">
  <a href="https://vzuliani97.github.io"><img alt="Portfolio" src="https://img.shields.io/badge/Portfolio-vzuliani97.github.io-0f766e?style=for-the-badge"></a>
  <a href="https://www.linkedin.com/in/valter-zuliani-70152a97"><img alt="LinkedIn" src="https://img.shields.io/badge/LinkedIn-Valter_Zuliani-0a66c2?style=for-the-badge&logo=linkedin&logoColor=white"></a>
  <img alt="Open to remote work and relocation" src="https://img.shields.io/badge/Open_to-remote_work_and_relocation-b7791f?style=for-the-badge">
</p>

# Hi, I'm Valter

**Software Engineer: Full Stack, Cloud & DevOps.** I build, deploy and operate full-stack applications, APIs and cloud infrastructure with TypeScript, Node.js, React and AWS.

Medellín, Colombia · Authorized to work in Europe · Open to remote work and relocation · Spanish and Italian native, English C1

| 123 | Since 2020 | 100 | C1 |
|:---:|:---:|:---:|:---:|
| automated tests across 3 portfolio systems (54 + 54 + 15) | professional software experience | mobile Lighthouse on 3 routes of my portfolio, measured 1 Nov 2026 | English, with native Spanish and Italian |

## Selected work

### Yamesi Core · Business Operations & Traceability System

<a href="https://vzuliani97.github.io/work/yamesi/"><img src="assets/yamesi-sell.jpg" width="100%" alt="Yamesi Core point of sale: catalog photos with reference, weight and size, and the sale summary with each piece's photo"></a>

**What it is for:** the counter of an 18k gold jewelry store. Find a piece by photo, reference or size; sell it with a Colombian-style invoice; keep the catalog and its photos current; record petty cash with receipts; and balance the drawer every night.

**What I built:**
- Data model in plain SQL: gold lots in milligrams, gap-free invoice numbers, VAT per line, closings and an audit log.
- NestJS API with roles, Zod validation, idempotent invoices, row and advisory locks, and a login lockout.
- React point of sale, an inventory portal with drag-and-drop photos, petty cash with receipts, closing and reports.
- Invoice PDF with each piece's photo, a CUFE calculation that matches the DIAN example and a QR. For demonstration only: not transmitted to or validated by the DIAN.
- Docker Compose, CI with CodeQL, Gitleaks and an image-metadata check, and a simulated business day (`make demo`).

`54 tests` · `44 real catalog pieces` · `CUFE = DIAN example` · `NestJS` · `React` · `PostgreSQL` · `S3` · `PDFKit` · `Docker`

<table>
  <tr>
    <td width="33%"><a href="https://github.com/vzuliani97/yamesi#processes-step-by-step"><img src="assets/yamesi-inventory.jpg" alt="Inventory portal: the catalog with photos, stock value and filters"></a><br><sub>Inventory portal</sub></td>
    <td width="33%"><a href="https://github.com/vzuliani97/yamesi#colombian-sales-invoice"><img src="assets/yamesi-invoice.jpg" alt="Invoice PDF: each line with the piece's photo, reference, serial and gold weight; CUFE and QR"></a><br><sub>Invoice PDF with each piece's photo</sub></td>
    <td width="33%"><a href="https://github.com/vzuliani97/yamesi#3-petty-cash-with-receipts"><img src="assets/yamesi-petty-cash.jpg" alt="Petty cash with the receipt photos of the day"></a><br><sub>Petty cash with receipts</sub></td>
  </tr>
</table>

Built for a real store: the demo runs on 44 pieces from the public catalog of Joyería Yamesi, with their real reference, gold weight, size, price and photo.

<p>
  <img src="assets/catalog/ani-sol-59.jpg" width="15%" alt="Solitaire ring">
  <img src="assets/catalog/can-mel-55.jpg" width="15%" alt="Hoop earrings">
  <img src="assets/catalog/dij-var-141.jpg" width="15%" alt="Heart pendant">
  <img src="assets/catalog/an-dam-172.jpg" width="15%" alt="Ring">
  <img src="assets/catalog/pul-63.jpg" width="15%" alt="Bracelet">
  <img src="assets/catalog/top-ani-36.jpg" width="15%" alt="Butterfly studs">
</p>

[Case study](https://vzuliani97.github.io/work/yamesi/) · [Source](https://github.com/vzuliani97/yamesi) · [Every process, step by step](https://github.com/vzuliani97/yamesi#processes-step-by-step) · [Design walkthrough](https://github.com/vzuliani97/yamesi/blob/main/DESIGN_WALKTHROUGH.md)

### OpsCircuit · Cloud Delivery & Incident Automation Lab

<a href="https://vzuliani97.github.io/work/opscircuit/"><img src="assets/opscircuit-n8n.jpg" width="100%" alt="n8n incident intake: a real execution with every step green, from the Alertmanager webhook to the page to on-call"></a>

**What it is for:** shows how a small team ships to Kubernetes, watches what is running, and turns a storm of alerts into one incident and one page, with drills that prove the recovery works.

**What I built:**
- A 3-node kind cluster with Kustomize overlays, Argo CD (GitOps), and Prometheus and Grafana provisioned as code.
- Hardened workloads: non-root containers, NetworkPolicies, Pod Security Admission; Checkov with zero failed checks.
- Outage and bad-release drills; found an alert that could never fire, fixed it and wrote the postmortem.
- n8n incident workflow: authenticated webhook, validation, deduplication in PostgreSQL, enrichment, bounded retries, dead letters and replay.
- Terraform for an AWS design (VPC, EKS, RDS, ECR), validated in CI and never applied.

`15 integration tests` · `self-heal in 2 s` · `5 deliveries → 1 page` · `Kubernetes` · `Argo CD` · `Prometheus` · `Grafana` · `Terraform` · `n8n`

<table>
  <tr>
    <td width="33%"><a href="https://github.com/vzuliani97/opscircuit#2-observe"><img src="assets/opscircuit-grafana.jpg" alt="Grafana dashboard provisioned as code"></a><br><sub>Grafana, provisioned as code</sub></td>
    <td width="33%"><a href="https://github.com/vzuliani97/opscircuit#3-turn-alerts-into-one-incident-n8n"><img src="assets/opscircuit-n8n-notify.jpg" alt="n8n: service catalog, incident upsert and the page to on-call"></a><br><sub>n8n: enrich, deduplicate and page</sub></td>
    <td width="33%"><a href="https://github.com/vzuliani97/opscircuit#5-practice-the-bad-day"><img src="assets/opscircuit-alerts.jpg" alt="Prometheus alert rules"></a><br><sub>Prometheus alert rules</sub></td>
  </tr>
</table>

[Case study](https://vzuliani97.github.io/work/opscircuit/) · [Source](https://github.com/vzuliani97/opscircuit) · [Every process, step by step](https://github.com/vzuliani97/opscircuit#processes-step-by-step) · [Incident lab verification](https://github.com/vzuliani97/opscircuit/blob/main/docs/INCIDENT_AUTOMATION_VERIFICATION.md) · [Postmortem](https://github.com/vzuliani97/opscircuit/blob/main/docs/incidents/2026-10-30-postmortem.md)

### NekoBet · Live Sportsbook, Casino & Wallet Platform

<a href="https://vzuliani97.github.io/work/nekobet/"><img src="assets/nekobet-betting.jpg" width="100%" alt="NekoBet live sportsbook: football, basketball, baseball and hockey with each sport's clock, moving odds, the bet slip and my bets"></a>

**What it is for:** a point-of-sale network where every store sells live sports bets, casino games and prepaid top-ups from one balance, from a portal or a partner API. Everything runs in real time; the production betting platforms I worked on and their data are confidential, so this public version runs on a simulated feed. The engineering goal is a balance that never goes wrong.

**What I built:**
- A real-time sportsbook for football, basketball, baseball and ice hockey, each with its own clock and scoring model (Poisson goals and runs, a normal model of points, overtime and extra innings), results, double chance, totals and both teams to score, `ODDS_CHANGED` refusals and every market settled once.
- An event page with a live tracker drawn for each sport (pitch, court, diamond or rink) that flashes on every score.
- Casino: a seamless wallet with idempotent, HMAC-signed provider callbacks and rollback tombstones; a lobby of five games with an animated slot machine.
- Balance and ledger: one conditional `UPDATE`, `CHECK` constraints and append-only movements; idempotent sales; an HMAC-signed B2B API; a login lockout; CI images that Argo CD deploys in OpsCircuit.

`54 tests` · `4 sports live` · `70 retries → 1 sale` · `NestJS` · `PostgreSQL` · `React` · `SSE` · `HMAC` · `Docker`

<table>
  <tr>
    <td width="33%"><a href="https://github.com/vzuliani97/nekobet#2-place-a-live-bet"><img src="assets/nekobet-event.jpg" alt="Football event: live tracker on the pitch, scoreboard and every market"></a><br><sub>Football: live tracker and markets</sub></td>
    <td width="33%"><a href="https://github.com/vzuliani97/nekobet#2-place-a-live-bet"><img src="assets/nekobet-basketball.jpg" alt="Basketball event: court tracker by quarter, winner and total points"></a><br><sub>Basketball: court tracker by quarter</sub></td>
    <td width="33%"><a href="https://github.com/vzuliani97/nekobet#3-play-the-casino-seamless-wallet"><img src="assets/nekobet-casino.jpg" alt="Casino lobby and a slot machine paying x20 through the wallet"></a><br><sub>Casino: slot machine paying ×20</sub></td>
  </tr>
</table>

[Case study](https://vzuliani97.github.io/work/nekobet/) · [Source](https://github.com/vzuliani97/nekobet) · [Every process, step by step](https://github.com/vzuliani97/nekobet#processes-step-by-step) · [Concurrency experiment](https://github.com/vzuliani97/nekobet/blob/main/docs/concurrency-experiment.md) (local and reproducible, not a production benchmark) · [Design walkthrough](https://github.com/vzuliani97/nekobet/blob/main/DESIGN_WALKTHROUGH.md)

## What I have worked on

**Full Stack Developer · Inversiones Zuliani S.A.S. (Yamesi)** · Medellín · May 2020 – Present
- Proposed and built the store's accounting and invoicing system, replacing spreadsheets and paper receipts; the business uses it for around 15 invoices a day.
- Deployed it with Docker on AWS EC2, with documents and images in S3, HTTPS, and network access controlled through security groups, SSH and VPN. Since 2023, as a contractor, I support, fix, test and update it.

**Junior DevOps Engineer · The Big Group** · Sydney · Oct 2024 – Mar 2026 · part-time
- Supported deployment and maintenance of AWS services for payments, digital operations and hospitality in an English-speaking international team, with CI/CD pipelines, Docker and Kubernetes.
- Investigated production incidents through logs and monitoring, and applied access controls to cloud resources.

**Software Developer (Full Stack / Cloud) · Código Digital Codi S.A.S.** · Medellín · Oct 2021 – Feb 2023
- Developed full-stack modules and Node.js APIs for transactional platforms, white-label iGaming platforms for several countries and healthcare applications with Angular, React, TypeScript, PHP and MySQL; built a B2B API secured with key pairs and IP allowlisting; and managed AWS infrastructure and deployments from staging to production with EC2, VPC, VPN, EKS, Terraform, Docker and GitLab CI/CD.
- Worked on the real-time sports betting and casino integration of the point-of-sale portal: the live-odds frontend, the provider integration, the betting backend (bet validation, balance and settlement) and its infrastructure.

**Software Developer · LaCompay Colombia** · Medellín · Nov 2020 – Apr 2021
- Contributed to the development of features for a C++ payment gateway, focused on transaction processing.

## Stack

**Software**
![TypeScript](https://img.shields.io/badge/TypeScript-3178C6?style=flat-square&logo=typescript&logoColor=white)
![Node.js](https://img.shields.io/badge/Node.js-5FA04E?style=flat-square&logo=nodedotjs&logoColor=white)
![NestJS](https://img.shields.io/badge/NestJS-E0234E?style=flat-square&logo=nestjs&logoColor=white)
![React](https://img.shields.io/badge/React-20232A?style=flat-square&logo=react&logoColor=61DAFB)
![Angular](https://img.shields.io/badge/Angular-DD0031?style=flat-square&logo=angular&logoColor=white)
![PostgreSQL](https://img.shields.io/badge/PostgreSQL-4169E1?style=flat-square&logo=postgresql&logoColor=white)
![MySQL](https://img.shields.io/badge/MySQL-4479A1?style=flat-square&logo=mysql&logoColor=white)
![PHP](https://img.shields.io/badge/PHP-777BB4?style=flat-square&logo=php&logoColor=white)

**Cloud & delivery**
![AWS](https://img.shields.io/badge/AWS-232F3E?style=flat-square&logo=amazonwebservices&logoColor=white)
![Docker](https://img.shields.io/badge/Docker-2496ED?style=flat-square&logo=docker&logoColor=white)
![Kubernetes](https://img.shields.io/badge/Kubernetes-326CE5?style=flat-square&logo=kubernetes&logoColor=white)
![Terraform](https://img.shields.io/badge/Terraform-844FBA?style=flat-square&logo=terraform&logoColor=white)
![GitHub Actions](https://img.shields.io/badge/GitHub_Actions-2088FF?style=flat-square&logo=githubactions&logoColor=white)
![GitLab CI/CD](https://img.shields.io/badge/GitLab_CI%2FCD-FC6D26?style=flat-square&logo=gitlab&logoColor=white)
![Linux](https://img.shields.io/badge/Linux-FCC624?style=flat-square&logo=linux&logoColor=black)

**Working knowledge from the portfolio**
![Argo CD](https://img.shields.io/badge/Argo_CD-EF7B4D?style=flat-square&logo=argo&logoColor=white)
![Prometheus](https://img.shields.io/badge/Prometheus-E6522C?style=flat-square&logo=prometheus&logoColor=white)
![Grafana](https://img.shields.io/badge/Grafana-F46800?style=flat-square&logo=grafana&logoColor=white)
![n8n](https://img.shields.io/badge/n8n-EA4B71?style=flat-square&logo=n8n&logoColor=white)

## Education

Systems Engineer, Universidad de Medellín · Advanced Diploma of IT (Cyber Security), Sydney

<sub>Portfolio projects are independent reconstructions with no employer code. Their data is synthetic (production systems are confidential), except the Yamesi Core demo catalog (© Inversiones Zuliani S.A.S., used with permission). AI-assisted; verified through tests and CI.</sub>
