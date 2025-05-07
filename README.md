# 🚀 Splunk Lab Automation Suite

Automate Splunk administration end-to-end using Python, REST API, and DevOps tools. This repository simulates a real-world Splunk engineering project with clearly scoped automation tasks, CI/CD, and deployment best practices.

---

## 📌 Project Goals

* Build a modular framework for Splunk administration automation.
* Simulate a production-like lab with Splunk Enterprise, Forwarders, and app deployment.
* Assign individual components to team members for agile collaboration.

---

## 📁 Repo Structure

```
splunk-lab-automation-suite/
├── api_wrappers/        # REST API tools for users, indexes, alerts
├── backup_restore/      # Configs, lookups, and KO backups
├── ci_cd/               # GitHub Actions and validation pipelines
├── configs/             # Template .conf files (inputs, outputs, props, etc.)
├── dashboards/          # JSON/XML-based dashboard templates
├── docs/                # Project wiki, arch diagrams, onboarding guides
├── install/             # Splunk/UF installers and playbooks
├── ko_management/       # Saved search, lookup, macro, field update scripts
├── monitoring/          # Health checks, Slack/email alerts, metrics
├── tests/               # Unit/integration tests
├── LICENSE
├── README.md
└── CONTRIBUTING.md
```

---

## 🗂️ Work Areas & Assignees

| Module                           | Description                                         | Owner (Sample)    |
| -------------------------------- | --------------------------------------------------- | ----------------- |
| `install/`                       | Install Splunk/UF using Python or Ansible           | @splunkInstaller  |
| `api_wrappers/index_mgmt.py`     | Automate index creation, retention policies         | @dataOpsAdmin     |
| `api_wrappers/user_role_mgmt.py` | Create/update/delete users and roles                | @ldapSpecialist   |
| `monitoring/`                    | Health checks (disk, queue, forwarders)             | @splunkWatcher    |
| `ko_management/`                 | Automate saved searches, lookups, field extractions | @koEngineer       |
| `dashboards/`                    | Auto-deploy dashboards from templates               | @dashboardBuilder |
| `backup_restore/`                | Scheduled backup of configs, apps, KOs              | @infraBackupAdmin |
| `ci_cd/`                         | Validate + deploy changes via GitHub Actions        | @cicdEngineer     |

---

## 🛠 Key Automation Domains

### 1. Deployment & Config

* Install/upgrade Splunk Enterprise/UF
* Update and push configuration files (conf)
* Version control all configs

### 2. Index & Storage

* Create/delete indexes via REST API
* Manage SmartStore settings, retention

### 3. Users & Roles

* CRUD operations on users/roles
* Role-based access control enforcement

### 4. Knowledge Objects (KOs)

* Automate upload of savedsearches, macros, tags
* Lookup CSV updates

### 5. Health & Monitoring

* Check disk, license, indexing queues, forwarders
* Send alerts via email/Slack

### 6. Dashboards & Alerts

* Manage alerts via REST API
* Template and deploy dashboards

### 7. Backup & Recovery

* Snapshot KOs, apps, configs
* Disaster restore script

### 8. CI/CD & GitOps

* Validate and lint confs
* Auto-promote changes to TEST/PROD

---

## 🔧 Setup

```bash
# Clone
$ git clone https://github.com/your-org/splunk-lab-automation-suite.git
$ cd splunk-lab-automation-suite

# Create virtualenv
$ python3 -m venv venv
$ source venv/bin/activate

# Install deps
$ pip install -r requirements.txt
```

---

## ✅ Getting Started for Team Members

1. Fork the repo
2. Create a branch: `git checkout -b feature/my-task`
3. Add your module inside the right folder
4. Submit a pull request
5. CI/CD will validate `.conf` syntax and API contracts

---

## 🤝 Contributing

See [CONTRIBUTING.md](./CONTRIBUTING.md) for team process, style guide, and Git flow

---

## 📜 License

MIT License © 2025 Splunk Admin Lab Team
