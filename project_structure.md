
## 🧩 Project Structure Overview

**Repository Name:** `splunk-lab-automation-suite`
**Goal:** Automate every core Splunk admin domain using Python, REST API, and GitOps practices inside a realistic VM-based lab.

---

## 📁 Project Folder Structure

```bash
splunk-lab-automation-suite/
│
├── docs/                    # 📚 Documentation, architecture diagrams
├── install/                 # �� Scripts to install Splunk/UF on VMs
│   ├── install_splunk.py
│   ├── install_forwarder.py
│   └── ansible/
│       └── splunk-playbook.yml
│
├── configs/                 # ⚙️ App + conf templates (inputs.conf etc)
│   ├── inputs.conf
│   └── outputs.conf
│
├── api_wrappers/            # 🔌 Python wrappers for Splunk REST API
│   ├── index_mgmt.py
│   ├── user_role_mgmt.py
│   ├── alert_mgmt.py
│   └── dashboard_mgmt.py
│
├── monitoring/              # 📈 Scripts for MC checks, health, Slack alerts
│   ├── check_disk.py
│   ├── forwarder_status.py
│   └── alert_to_slack.py
│
├── dashboards/              # 📊 Dashboard JSON/XML templates
│
├── ko_management/           # 📂 Saved searches, lookups, field extractions
│   └── update_saved_search.py
│
├── backup_restore/          # 💾 Scheduled backup/restore of configs & KOs
│
├── ci_cd/                   # 🔁 GitHub Actions or Jenkins pipelines
│   └── validate_conf.yml
│
├── tests/                   # ✅ Unit and integration tests
│
├── LICENSE
├── README.md
└── CONTRIBUTING.md
```

---

## 🧑‍💻 Roles and Task Areas

| Role                | Responsibility                                                             |
| ------------------- | -------------------------------------------------------------------------- |
| **Project Lead**    | Oversees architecture, CI/CD, task coordination                            |
| **Installer Dev**   | Creates installation scripts for Splunk, UF, and handles Ansible playbooks |
| **API Engineer**    | Builds REST API wrappers for admin tasks like user/index mgmt              |
| **Monitoring Lead** | Develops health checks, license/disk alerts, and Slack notifications       |
| **KO Manager**      | Automates dashboards, saved searches, and lookup updates                   |
| **Backup Engineer** | Implements configuration and knowledge object backup/restore workflows     |
| **CI/CD Engineer**  | Sets up GitHub Actions for config validation, push to TEST/PROD            |
| **Integrator**      | Builds integrations with ServiceNow, AWS, or other external tools          |

---

## 🛠️ Step-by-Step Phase Plan (Agile Sprints)

### 🥇 Phase 1: Core Setup

* [ ] Set up GitHub repo
* [ ] Create baseline VM lab (Ubuntu + Splunk + UF)
* [ ] Build initial installer script (`install_splunk.py`)
* [ ] Create `README.md` with project charter
* [ ] Setup `dev`, `test`, and `prod` branches

---

### 🥈 Phase 2: REST API Automation

* [ ] Index management automation (`api_wrappers/index_mgmt.py`)
* [ ] User and role automation (`user_role_mgmt.py`)
* [ ] Alert CRUD APIs (`alert_mgmt.py`)

---

### 🥉 Phase 3: Monitoring & Forwarders

* [ ] Disk/license/queue check scripts
* [ ] Forwarder health tracker
* [ ] Slack or Teams integration

---

### 🏅 Phase 4: Knowledge Objects & Dashboards

* [ ] Automate creation of saved searches, lookups, tags
* [ ] Upload/update dashboard JSONs via script

---

### 🧪 Phase 5: CI/CD + GitOps

* [ ] Add GitHub Actions for conf file linting
* [ ] Pipeline for `conf` promotion from dev → test → prod

---

### 🎯 Phase 6: Backup & Audit

* [ ] Implement scheduled config backup scripts
* [ ] Auto-generate Markdown doc of users/indexes/KOs

---

## 🧠 Best Practices Embedded

* **Idempotency:** Scripts should be rerunnable without side-effects
* **Environment Isolation:** ENV vars or config files for lab separation
* **Logging:** Standard logging across all Python scripts
* **Security:** Avoid hardcoded creds — use vaults or .env files
* **Testing:** Every module in `api_wrappers/` must have unit tests


