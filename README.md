# Apigee X on a GCP Enterprise Landing Zone — Setup Blueprint & Checklist

A consultant-grade, self-contained HTML presentation for walking a (semi-technical) client
through what it takes to stand up **Apigee X** on top of an enterprise GCP landing zone.
It explains the concepts simply and, crucially, spells out **everything we need from the client** to provision.

## What's inside
- **22 slides** — concept → object model → reference architecture → per-zone checklist → provisioning sequence → ask → timeline → next steps.
- **Apigee object model** — Organization / Environment Groups / Environments / Instances explained as an inline diagram.
- **Reference architecture** — the "Landing Zone Blueprint", an inline SVG split into 7 named build zones (Z1–Z7), with real GCP resources and the LB health-check ranges.
- **Per-zone checklists** — each zone has two columns: *what we configure* (with the actual resources, roles & constraints) and *what we need from you*.
- **Provisioning sequence** — the ordered build (keys → peering → runtime → ingress → southbound).
- **Consolidated pre-requisites slide** — the single takeaway the client keeps.
- **Speaker notes** — hidden on screen (press `N` or the *Notes* button), printed in the PDF export.
- **Design system** — Poppins/Inter/JetBrains Mono, inline icon set, slide chrome (section + page no.), top progress rail, gradient + drop-shadow diagrams.

## The 7 build zones
| Zone | Focus |
| ---- | ----- |
| **Z1** | Foundation & Identity — projects, IAM, billing, API enablement |
| **Z2** | Networking & VPC — Shared VPC, PSA `/22`, Cloud Router + NAT |
| **Z3** | Apigee X Runtime — org, regional instances, env groups, CMEK |
| **Z4** | Northbound Ingress — PSC NEG, Global External ALB, Cloud Armor, certs, DNS |
| **Z5** | Southbound Connectivity — GKE/Cloud Run/Compute, PSC, on-prem via Interconnect/VPN |
| **Z6** | Security & Governance — Cloud KMS/CMEK, VPC-SC, Org Policy, Secret Manager |
| **Z7** | Observability & Operations — Cloud Monitoring, Logging, API Analytics, alerting |

## Using the deck
- **Navigate:** `→` / `Space` next · `←` previous · click right/left half · `Home`/`End` jump · `N` toggle notes.
- **Export PDF:** `Ctrl/Cmd+P` → A4 Landscape, background graphics on. Colors and speaker notes are preserved.
- **Tech:** single `index.html`, no build step. Tailwind + anime.js via CDN, inline SVG, Google Fonts (Poppins/Inter).

## Deployment
Hosted on **GitHub Pages** via the `Enterprise Deployment` GitHub Actions workflow (`.github/workflows/deploy.yml`).
Pushing to `main` builds and publishes `index.html` automatically.

---
*Enterprise API platform walkthrough material.*
