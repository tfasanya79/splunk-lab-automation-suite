# 🤝 Contributing to Splunk Lab Automation Suite

Welcome to the Splunk Lab Automation Suite! We're excited you're here to help automate and modernize Splunk administration. Follow the guide below to contribute effectively.

---

## 📋 Table of Contents

* [Code of Conduct](#code-of-conduct)
* [How to Contribute](#how-to-contribute)
* [Branching Strategy](#branching-strategy)
* [Coding Guidelines](#coding-guidelines)
* [Commit Convention](#commit-convention)
* [Pull Request Checklist](#pull-request-checklist)

---

## 📜 Code of Conduct

Please follow our [Code of Conduct](./CODE_OF_CONDUCT.md) to foster a healthy and inclusive environment.

---

## 🚀 How to Contribute

1. **Fork** the repository.
2. **Clone** your fork:

   ```bash
   git clone https://github.com/your-username/splunk-lab-automation-suite.git
   ```
3. **Create a branch** for your feature:

   ```bash
   git checkout -b feature/your-feature-name
   ```
4. **Write your code** inside the appropriate module folder.
5. **Test locally** (unit tests or CLI scripts).
6. **Commit** and **push** your changes.
7. **Submit a Pull Request** to `dev` branch.

---

## 🌿 Branching Strategy

* `main`: Stable, production-ready automation suite.
* `dev`: Active development and integration branch.
* `feature/*`: New features (e.g., `feature/alert-api`)
* `bugfix/*`: Bug fixes (e.g., `bugfix/index-create`)

---

## 🧹 Coding Guidelines

### Python

* Use `black` formatter and `flake8` for linting.
* Log using the `logging` module (not `print`).
* Structure REST API calls using `requests` or `splunk-sdk`.

### Bash Scripts

* Include `#!/bin/bash` and set `-euo pipefail` flags.
* Comment each major block.
* Use readable variable names.

### Conf Files

* Validate syntax using CI before PR approval.
* Use GitOps structure for version-controlled `.conf`.

---

## ✍️ Commit Convention

Format:

```
type(scope): message
```

Examples:

* `feat(api): add index creation endpoint`
* `fix(config): resolve typo in outputs.conf`
* `docs(readme): update project overview`

Types: `feat`, `fix`, `chore`, `docs`, `refactor`, `test`

---

## ✅ Pull Request Checklist

* [ ] PR targets `dev`
* [ ] Folder and file names are correct
* [ ] Code is linted and tested
* [ ] Function and variable names are meaningful
* [ ] Documentation (if applicable) is included
* [ ] At least one reviewer assigned

---

## 🙌 Need Help?

Open an issue or tag a maintainer in the Pull Request. We're here to support you.

Happy automating! 💥

