# Hi, I'm Rodrigo Pimenta 👋

I write software that keeps distributed systems alive.

**Systems Engineer @ Hughes Network Systems.** Second-highest committer of ~15 engineers on the automation platform behind our satellite ground segment — 400+ commits across 53 delivered tickets. Most of what I build is self-healing automation: systems that detect a fault, remediate it in bounded scope, record the action, and alert. The goal is that an outage becomes a non-event instead of a 2am page.

I also build **AI-native** — Kiro, Cursor, and Claude Code are in my daily workflow. Deep systems debugging and AI leverage aren't in tension: the first tells me what's worth building, the second gets it shipped.

---

### 🛰️ Live projects

**[Orbital Watch](https://orbital.rodrigopimenta.com)** · [`source`](https://github.com/rodrigopimenta10/orbital-watch)

Which satellites are over a ground station, when they next pass, and what geomagnetic activity is doing to orbital drag and link margin.

The interesting part isn't the dashboard — it's that **the page reports its own data freshness instead of assuming it.** Every upstream source is isolated and degrades independently: live fetch → cache → committed snapshot, each classified `fresh` / `stale` / `failed` on the page with the reasoning shown. A build cannot fail, and it cannot quietly publish stale numbers as if they were current. 150 tests, offline-deterministic builds, scheduled rebuilds on a Cloudflare Worker cron with a dead-man check that notices if the scheduler itself dies.

`Python` · `Cloudflare Workers` · `CI/CD` · `pytest`

**[rodrigopimenta.com](https://rodrigopimenta.com)** · [`source`](https://github.com/rodrigopimenta10/portfolio-website)

Portfolio and background. React + Vite, dual-hosted so links already in circulation never break.

---

### 🔧 What I've built at work

**Ceph storage self-healing monitor** — sole author, 6,586 lines, 77 of 79 commits. Watches 24 nodes across 8 clusters every 3 minutes. Performs automated metadata-server failover, but only after assessing whether a standby can actually sustain the load — so it never fails over into a worse node. Outcomes are verified against the cluster log to distinguish a real failover from a same-node reclaim. Append-only event history across 7 PostgreSQL tables, 19-panel Grafana dashboard, pytest suite in CI.

**Config integrity self-heal** — sole author, 3,594 lines. Detects configuration drift and corruption across the gateway fleet over SFTP and restarts the affected service. Modernized a blocking-I/O workload onto `asyncio` with semaphore-bounded fan-out rather than process pools.

**Platform-wide logging redesign** — root-caused a defect that silently discarded log records. Cut the footprint from 19.68 GB to 58 MB and reclaimed ~25 GB in production, then built audit tooling that swept all 146 scheduled jobs for the same pattern instead of fixing them one at a time.

**Production root cause analysis** — a 738 MB core dump traced with `gdb` to an unguarded deserialization path in a vendor component, and a 177-process leak traced to a library deadlock at interpreter teardown. Both delivered as actionable defect reports rather than "it crashed again."

---

### Tech I work with

**Languages** Python · SQL · Bash · PowerShell
**Automation & CI/CD** Ansible · Jenkins · pytest · uv · ruff · Fabric
**Data & observability** PostgreSQL · BigQuery · Grafana · pandas
**Infrastructure** Linux/RHEL · Ceph · asyncio · gdb / core-dump analysis
**AI-native tooling** Kiro · Cursor · Claude Code

---

### 📫 Reach me

[LinkedIn](https://linkedin.com/in/rodrigoppimenta) · [rodrigopimenta.com](https://rodrigopimenta.com) · [Résumé](https://rodrigopimenta.com/rodrigo_pimenta_resume.pdf) · RodrigoPimenta102@gmail.com

Open to platform, infrastructure, backend, and SRE software engineering roles — remote, or the NYC, DC–Baltimore, and SF Bay Area metros.
