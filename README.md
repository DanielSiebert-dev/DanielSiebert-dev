# Greetings, DevSecOps Overlords! 👾 I'm Daniel

### Cloud Warlock | DevSecOps Sentinel | Finance-to-Code Transmuter | Squad C & E Warlord

🔗 [LinkedIn](https://www.linkedin.com/in/daniel-siebert/) | [GitHub](https://github.com/DanielSiebert-dev)

![me_coding](https://github.com/DanielSiebert-dev/DanielSiebert-dev/blob/main/Cloud%20Engineering.webp?raw=true)

## 🛠️ Core Arsenal
![Python](https://img.shields.io/badge/Python-3776AB?style=for-the-badge&logo=python&logoColor=white) (PyCharm Overlord) ![AWS](https://img.shields.io/badge/AWS-FF9900?style=for-the-badge&logo=amazon-aws&logoColor=white) (Cloud Practitioner & Solutions Architect) ![Terraform](https://img.shields.io/badge/Terraform-7B42BC?style=for-the-badge&logo=terraform&logoColor=white) ![Docker](https://img.shields.io/badge/Docker-2496ED?style=for-the-badge&logo=docker&logoColor=white) ![GitHub Actions](https://img.shields.io/badge/GitHub_Actions-2088FF?style=for-the-badge&logo=github-actions&logoColor=white) ![SAP](https://img.shields.io/badge/SAP-0FAAFF?style=for-the-badge&logo=sap&logoColor=white) ![Linux](https://img.shields.io/badge/Linux-FCC624?style=for-the-badge&logo=linux&logoColor=black) ![JIRA](https://img.shields.io/badge/JIRA-0052CC?style=for-the-badge&logo=jira-software&logoColor=white) ![PostgreSQL](https://img.shields.io/badge/PostgreSQL-336791?style=for-the-badge&logo=postgresql&logoColor=white) ![Node.js](https://img.shields.io/badge/Node.js-339933?style=for-the-badge&logo=node.js&logoColor=white)

## 🌌 About the Warlock
With 12+ years wielding finance, controlling, and IT magic (7 years mastering SAP), I’ve conjured strategic programs, ERP rituals, and software integrations to optimize financial realms. As the warlord leading Squad C and E—commanding a legion of four fellow warriors, making us five strong—my grimoire blends DevSecOps spells—AWS, Terraform, Docker, and CI/CD pipelines—with potent new runes: PostgreSQL tuning with PgBouncer and Node.js wizardry for scalable apps.  

I lead daily standups, unveil the lore of each task with clear explanations, and split grand quests into manageable parts for my team. Our code flows through a Teambranch, where I review every line, before merging into the Development branch after epic council approvals. I channel JIRA, Confluence, and testing runes to fuse finance and tech, crafting lean workflows and cost-saving artifacts. A veteran of leadership crusades and technical quests, I’ve driven transformations and sparked innovations.  

My quest evolves: from financial lore to cloud mastery, merging ERP expertise with automation and security. As part of the African Trading Club, I apply tech to boost trade operations in Tanzania, weaving DevSecOps and financial alchemy into epic, scalable solutions—all while ruling with PyCharm!  

## 🕒 My Epic Quest
- 🌐 Mastered financial control, global IT budgeting, and ERP deployments.
- 💻 Earned AWS Certified Cloud Practitioner and Solutions Architect Associate via a Cloud Engineering odyssey.
- 🔒 Thriving as a DevSecOps intern at webeet.io, leading Squad C & E, hacking automation, security, and infra with PyCharm as my wand.
- 📊 Optimized PostgreSQL with PgBouncer, stabilized Node.js apps with Healthchecks and Smoke Tests.

## 🚀 Recent Conquests
### Observability Stack
**Timestamp: 2025-08-26 22:23 CEST**  
This cycle warped by—peak sprint mode where you blink and behold a citadel! With my tribe, we forged an observability stack from the void in 7 legendary steps.  

#### Treasures Gained:
- ✅ Ansible playbooks + templates sealed in S3’s vault
- ✅ IAM + Security Groups enchanted with least-privilege, zero-trust runes
- ✅ AWS SSM Run Command casting playbooks (no SSH, no exposed IPs!)
- ✅ Filebeat shipping logs to Logstash → Elasticsearch → Kibana
- ✅ JSON logging + rotation etched at the app layer  

Each move iterated, validated with `terraform validate`, and stacked with precision. Fast, secure, testable—pure DevSecOps glory!  

### PgBouncer + Node.js: Eliminating Prepared Statement Pitfalls
**Timestamp: 2025-09-08 11:52 CEST**  
A subtle foe emerged: PgBouncer’s transaction pooling clashed with PostgreSQL’s prepared statements!  

#### The Challenge:
- Server-side prepared statements (e.g., 'get-user') bind to a single backend. Switching connections in transaction mode caused "prepared statement does not exist" errors and re-prepare overhead.  

#### Our Victory:
- ⚙️ Adjusted Node.js Postgres driver to avoid named prepares in pooled mode.
- ⚙️ Extended healthchecks to validate the App → PgBouncer → Postgres chain.
- ⚙️ Added smoke tests (200 → 503 → 200) to simulate outages.
- ⚙️ Cleaned up repo structure (.gitignore, configs) for lean infra.  

#### Why It Matters:
For finance or high-load systems, these errors mean downtime and lost trust. Our fix reduces risk and preps for scaling.  

#### Next Spell:
TLS, secrets management, and load tests for a cloud-native leap!  

### Optimizing PostgreSQL Performance with PgBouncer
**Timestamp: 2025-09-08 11:52 CEST**  
Scaling database connections unveiled PostgreSQL’s hidden curse: expensive backend processes!  

#### The Curse:
- 10 connections: Smooth sailing.
- 100 connections: Scheduling slows the ship.
- 1000 connections: CPU grinds to a halt with context-switching.  

#### The Remedy:
- PgBouncer, a lightweight pooler, shields Postgres by limiting client sockets and controlling active processes—not guessing by RAM.  
- Key Takeaway: The bottleneck is PostgreSQL’s resource hunger, not PgBouncer’s memory.  

### FinOps Epic: Automated Cost Control for QA Environment
**Timestamp: 2025-09-08 11:52 CEST**  
As the FinOps team lead for Squad C and E—commanding four fierce warriors, making us five strong—I’m conjuring automated cost controls to keep our QA layer-infra repo within budget. (MVP for learning; future migration to central user-creation infra repo for best practices alignment.)  

#### The Grand Goal:
Implement automated cost control and optimization measures to ensure we operate within budget, focusing on the layer-qa environment.  

#### Acceptance Criteria Conquered:
- ✅ Automated controls in place to prevent runaway costs in QA (tags for spend visibility and attribution to teams/projects—coordinated with other teams for correct tags).
- ✅ Automated process for cleaning up orphaned resources implemented.  

#### Sub-Quests (All Greenlit):
- ✅ C1 - Implement "Auto-Stop" for QA Instances #62 (Prevents idle resource drain).
- ✅ C2 - Configure Proactive Budget Alerts #63 (Spend visibility and early warnings).
- ✅ C3 - Automated Cleanup of Orphaned Resources #64 (Sweep unused artifacts).
- ✅ C4 - Implement "Office Hours" for Non-Production Environments #65 (Schedule shutdowns outside business hours).
- ✅ C5 - Create a Cost Visibility Dashboard #66 (Layer-infra repo MVP; migrate later).  

**Status vs. AC**: Stack up (app, postgres:16.10, pgbouncer); App connects via PgBouncer; Health checks behave (200 → 503 → 200); Failure drill passes; Resource limits effective; .env used; PgBouncer transaction pooling enabled; Dedicated Postgres volume.  

**Overdeliveries**: App exposes /healthz and /readyz; Tunable pool settings; Reduced PgBouncer logging noise.  

**What's Next**: Run backup-restore.sh (snapshot, smoke-restore, full); Load tests; Adjust pool/timeout based on traffic.  

### server.js & Infra Alignment with PgBouncer-Safe Solution
**Timestamp: 2025-09-08 11:52 CEST**  
Aligned app and infra with PgBouncer-safe patterns to banish incorrect habits.  

#### Changes Forged:
- server.js: Single Pool with modest max size; Removed prepared statements; Added /health, /ready, /readyz; Parameterized queries for /user/:id.
- Docker & PgBouncer: Compose aligned with infra; pgbouncer.ini for transaction mode and health checks.
- Docs: Updated README.md, FILE_STRUCTURE.md, BRANCHING.md, WORKFLOW_COMPOSE.md.  

#### Verification:
- ✅ backup-restore.sh snapshot/smoke-restore/full (dumps created, restored, app health 200).
- ✅ Containers start cleanly; Health checks via PgBouncer 200.
- Why: Replaces oversized pools and DB_PORT mismatches for efficient, compatible pooling.  

#### Next: Load tests; Metrics under traffic; Tune pool/timeout.

## 🛡️ Skill Vault
- **Languages & Frameworks:** Python (PyCharm), Flask, JavaScript, Node.js
- **Databases:** SQL, PostgreSQL, SQLite
- **Web:** HTML5, CSS3
- **Cloud & DevSecOps:** AWS, Terraform, Docker, GitHub Actions
- **Tools:** Git, SAP, Linux, JIRA, Confluence, Ansible, Filebeat, Logstash, Elasticsearch, Kibana, PgBouncer
- **Expertise:** IaC, CI/CD, Containerization, Security (IAM, VPC), Database Optimization

## 💪 Warlord Traits
- **Leadership:** Commanded legions of 12, forged cross-functional alliances as Squad C & E Teamlead, leading daily standups and task breakdowns.
- **Problem-Solving:** Debugged processes, slashed costs with analysis hacks.
- **Communication:** Delivered epic scrolls, negotiated with elders.
- **Adaptability:** Thrived across diverse realms.
- **Resilience:** Survived turnarounds, conquered global campaigns.

## 🌐 Tongues of Power
- German (Native)
- English (C1)
- French (A1)

## 📡 Join the Quest
Explore my [portfolio](https://github.com/DanielSiebert-dev?tab=repositories).  
Let’s code, secure, and conquer the multiverse! 🚀  

## 📊 Codex of Glory
<p align="center">
  <img src="https://github-readme-stats.vercel.app/api?username=DanielSiebert-dev&theme=github_dark_dimmed&show_icons=true&hide_border=true&layout=compact" alt="GitHub Stats" />
  <img src="https://github-readme-stats.vercel.app/api/top-langs/?username=DanielSiebert-dev&theme=github_dark_dimmed&layout=compact&langs_count=8&hide_border=true" alt="Top Languages" />
  <img src="https://github-profile-trophy.vercel.app/?username=DanielSiebert-dev&theme=onedark&no-frame=true&column=4&margin-w=15&margin-h=15" alt="Trophies" />
</p>

## 😂 Nerd Meme of the Cycle
Why did the DevSecOps wizard fail at stand-up? Because he kept encrypting the punchline! 😂  

## ⏳ Last Update
Monday, September 08, 2025, 12:07 PM CEST  
![Visitor Badge](https://visitor-badge.laobi.icu/badge?page_id=DanielSiebert-dev.DanielSiebert-dev)
