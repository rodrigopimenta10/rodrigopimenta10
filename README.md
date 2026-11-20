## Rodrigo Pimenta

Backend and platform software engineer, six-plus years in Python. I build systems that keep themselves running, and I set the engineering standards for the team that builds around them.

At Hughes I am a Systems Engineer III (software engineering): the escalation point and code-review gate for a ~12-engineer department automating HughesNet's satellite gateways, on call 24/7 against a 99.9% SLA. That code belongs to my employer and is not public. Two systems I wrote there:

- A self-healing monitor for Ceph storage. It replaced a manual recovery of about 1.5 hours, an outage for 40,000–60,000 subscribers, with automated failover inside one 3-minute cycle.
- A configuration self-heal that closed an outage path cutting off 20,000–30,000 subscribers about once a month.

### What is public

- **[Sightline](https://lunarsightline.com)** ([code](https://github.com/shackleton-station/sightline)): a lunar landing-site planner built for NASA Space Apps 2026. I led the team of six, owned the architecture and built all of the Google Cloud infrastructure in Terraform. AI coding agents wrote most of the code under my direction and review. Sun and Earth positions match JPL Horizons within 0.0071° over 5,469,984 hourly checks.
- **[aws-platform-terraform](https://github.com/rodrigopimenta10/aws-platform-terraform)**: a production-style AWS platform built as tested Terraform modules. GitHub Actions applies it to a real account with no stored keys and destroys it again; the [drill reports](https://github.com/rodrigopimenta10/aws-platform-terraform/tree/main/docs/live) are in the repo.
- **[orbital-watch](https://github.com/rodrigopimenta10/orbital-watch)** ([live](https://orbital.rodrigopimenta.com)): satellite passes and space weather on a static site that says how fresh each of its seven data sources is.
- **[portfolio-website](https://github.com/rodrigopimenta10/portfolio-website)**: [rodrigopimenta.com](https://rodrigopimenta.com), with a live status panel for the systems above and the Terraform that runs it in `infra/`.

Strongest in Python, SQL and PostgreSQL, Bash and PowerShell. The cloud work is Terraform on Google Cloud and AWS.

Relocating to New York. Open to senior backend, platform and infrastructure engineering roles, as an individual contributor or tech lead.

[rodrigopimenta.com](https://rodrigopimenta.com) · [LinkedIn](https://linkedin.com/in/rodrigopimenta10) · [Resume (PDF)](https://rodrigopimenta.com/rodrigo_pimenta_resume.pdf) · [RodrigoPimenta102@gmail.com](mailto:RodrigoPimenta102@gmail.com)
