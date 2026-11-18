## Rodrigo Pimenta

Backend and platform engineer, six-plus years in Python. I build systems that keep themselves running: self-healing automation, asyncio services, PostgreSQL and CI/CD.

I'm a Systems Engineer III at Hughes Network Systems, on the automation platform for its satellite gateways, with 24/7 on-call against a 99.9% availability SLA. Outside work I build on Google Cloud and AWS with Terraform.

Open to backend and platform engineering roles in New York.

### Now

- Leading [Sightline](https://lunarsightline.com), a lunar landing-site planner that runs on Google Cloud.
- Building [aws-platform-terraform](https://github.com/rodrigopimenta10/aws-platform-terraform) one module at a time. The network is done and identity is nearly done; containers and EKS come next.

### Projects

**Sightline** · [live site](https://lunarsightline.com) · [code](https://github.com/shackleton-station/sightline)

Shows when the Sun and Earth are in view from a landing site at the Moon's south pole, every hour from 2026 to 2049, and whether a landing date fits a mission's limits.

- **My part:** I led the six-person team behind it (NASA Space Apps 2026) and owned the architecture decisions. AI coding agents wrote most of the code, under my direction and review.
- **Stack:** Python pipeline on NASA SPICE and LOLA data. React and TypeScript front end. Four Cloud Run services on Google Cloud behind a load balancer, CDN and Cloud Armor, with Firestore, Redis and Pub/Sub into BigQuery. All of it is in Terraform, applied from GitHub Actions with no stored keys.
- **Result:** Sun and Earth positions match JPL Horizons within 0.0071° over 5,469,984 hourly checks. Deploys go out as a canary and roll back automatically. 2,020 tests run in CI.

**aws-platform-terraform** · [code](https://github.com/rodrigopimenta10/aws-platform-terraform) · [live drill reports](https://github.com/rodrigopimenta10/aws-platform-terraform/tree/main/docs/live)

A production-style AWS platform in Terraform, built as reusable modules with tests. It is a learning portfolio: a daily Claude Code run builds the next roadmap item, and I review it and study the note it writes.

- **Stack:** Terraform, `terraform test` with mock providers, Moto, tflint, checkov, GitHub Actions with OIDC.
- **Done so far:** remote state, VPC, VPC endpoints, flow logs, KMS, GitHub OIDC and IAM permissions boundaries. EKS, serverless and observability are on the roadmap.
- **Result:** every module is tested offline, with no AWS account. GitHub Actions then applies the live stacks to a real account through OIDC, with no stored keys, and destroys them again. More than 20 drill reports with redacted console screenshots are in the repo.

**Orbital Watch** · [live site](https://orbital.rodrigopimenta.com) · [code](https://github.com/rodrigopimenta10/orbital-watch)

Satellite passes over a ground station next to live space weather, on a static site that reports how fresh its own data is.

- **Stack:** Python build, Cloudflare Pages, a Cloudflare Worker on a schedule, GitHub Actions, pytest. Built with Claude Code.
- **Result:** each of the seven upstream sources is marked fresh, stale or failed on the page, with the reason. A build with every source unreachable still finishes and says so, and CI checks that on every push.

### At Hughes

This code belongs to my employer and is not public. From my [resume](https://rodrigopimenta.com/rodrigo_pimenta_resume.pdf):

- Second of 21 contributors over the last year on the satellite gateway automation platform: 491 commits across 67 delivered tickets.
- Sole author of a Ceph storage monitor that watches 24 nodes across 8 clusters and averages about 130 verified metadata-server failovers a month with no human involvement.
- Sole author of a configuration self-heal for 18 gateways at 8 sites, averaging about 295 remediations a month.
- Root-caused a logging defect that silently discarded records, and cut the log footprint from 19.68 GB to 58 MB.

### Reach me

[rodrigopimenta.com](https://rodrigopimenta.com) · [LinkedIn](https://linkedin.com/in/rodrigoppimenta) · [Resume (PDF)](https://rodrigopimenta.com/rodrigo_pimenta_resume.pdf) · [RodrigoPimenta102@gmail.com](mailto:RodrigoPimenta102@gmail.com)
