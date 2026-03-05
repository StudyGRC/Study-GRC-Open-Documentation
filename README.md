# Study GRC Open Documentation

![Markdown](https://img.shields.io/badge/Made%20with-Markdown-1f425f.svg)
[![License: CC BY-SA 4.0](https://img.shields.io/badge/License-CC%20BY--SA%204.0-lightgrey.svg)](https://creativecommons.org/licenses/by-sa/4.0/)
[![GitHub contributors](https://img.shields.io/github/contributors/StudyGRC/Study-GRC-Open-Documentation.svg?style=flat-square)](https://github.com/StudyGRC/Study-GRC-Open-Documentation/graphs/contributors)
[![GitHub last commit](https://img.shields.io/github/last-commit/StudyGRC/Study-GRC-Open-Documentation.svg?style=flat-square)](https://github.com/StudyGRC/Study-GRC-Open-Documentation/commits/main)
[![PRs Welcome](https://img.shields.io/badge/PRs-welcome-brightgreen.svg?style=flat-square)](http://makeapullrequest.com)
[![Discord](https://img.shields.io/discord/1211424757279494176?style=plastic&label=Discord)](https://discord.com/invite/X5EK5sU7he)

Welcome to the official repository for **Study GRC** documentation. This project houses our community built, community-driven Governance, Risk, and Compliance (GRC) policies, procedures, and guidelines. And it’s officially what Study GRC itself uses; free for others to tailor while adhering to the license.

## 📖 Our Philosophy: Markdown First

We believe that security and compliance documentation should be treated like code. By utilizing a "Markdown First" approach, we ensure our documentation is:
* **Version Controlled:** Every change is tracked, audited, and reversible.
* **Collaborative:** Anyone in the community can suggest improvements via Pull Requests. (or opening an issue)
* **Platform Agnostic:** Markdown is universally readable. 

> **Note:** While Markdown is our primary source of truth, we are interested in providing beautifully formatted Word Documents as an option in the future.

## 📂 Repository Structure

To ensure permanent links and easy discovery, our repository is organized by document **category** rather than status. 

* `/Policies` — High-level rules, mandates, and executive directives.
* `/Procedures` — Step-by-step instructions for executing policies.
* `/Standards` — Specific, mandatory technical baselines (e.g., encryption requirements).
* `/Guidelines` — Best practices and recommendations.
* `/Templates` — Standardized forms and starting points for new documents.

## 🏷️ Document Lifecycle & Status

The `main` branch of this repository is our active source of truth. To track where a document is in its lifecycle, we use **YAML Frontmatter** (metadata at the very top of each `.md` file). 

Every document will display one of the following statuses in its header:

| Status | Description |
| :--- | :--- |
| 📝 **Draft** | Work-in-progress documents. Found in active Pull Requests, not yet merged into `main`. |
| 🔎 **Reviewing** | Documents actively awaiting community or leadership review in an open Pull Request. |
| ✅ **Approved** | The current, active, and official Study GRC documentation. |
| ⏳ **Requires Review** | Previously approved documents that have reached their expiration date or require updates. |

## 🤝 Contributing

We are a community-built and community-driven project! We welcome contributions from GRC professionals, students, and enthusiasts. 

Whether you are fixing a typo, updating a standard, or drafting a brand new policy, please review our [Contributing Guidelines](CONTRIBUTING.md) to understand our Git-native workflow.

## 📄 License

This work is licensed under a [Creative Commons Attribution-ShareAlike 4.0 International License][cc-by-sa]. 

You are free to:
* **Share** — copy and redistribute the material in any medium or format.
* **Adapt** — remix, transform, and build upon the material for any purpose, even commercially.

Under the following terms:
* **Attribution** — You must give appropriate credit, provide a link to the license, and indicate if changes were made. You may do so in any reasonable manner, but not in any way that suggests the licensor endorses you or your use.
* **ShareAlike** — If you remix, transform, or build upon the material, you must distribute your contributions under the same license as the original.

[cc-by-sa-shield]: https://img.shields.io/badge/License-CC%20BY--SA%204.0-lightgrey.svg
[cc-by-sa]: http://creativecommons.org/licenses/by-sa/4.0/
