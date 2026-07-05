# Investigation Playbook

> Engineering standards, development methodology and reusable practices for computational intelligence projects.

![Status](https://img.shields.io/badge/status-stable-brightgreen)
![Version](https://img.shields.io/badge/version-v1.0.0-blue)
![License](https://img.shields.io/badge/license-MIT-green)

---

# Overview

The **Investigation Playbook** is the engineering foundation for every project developed within this laboratory.

Rather than being a collection of templates or documentation files, this repository defines the principles, standards and development practices shared across all projects.

Its purpose is to ensure that every repository follows the same engineering philosophy, architectural standards, documentation quality and development workflow.

The playbook is a living reference that evolves together with the laboratory.

---

# Philosophy

This repository is built around a simple idea:

> **Good software is designed before it is implemented.**

Engineering decisions should be understandable, documented, reproducible and justifiable.

Every project should be developed with the same level of rigor regardless of its size or complexity.

The goal is not simply to build software that works, but software that is maintainable, reproducible and educational.

---

# What You'll Find

The playbook currently defines standards for:

- Engineering methodology
- Software architecture
- Git workflow
- Documentation
- Architecture Decision Records (ADRs)
- Development practices

These standards are intended to be reused by every project in the laboratory.

---

# Repository Structure

```text
.
├── architecture/
├── documentation/
├── engineering/
├── git/
├── adr/
├── README.md
├── VISION.md
└── CHANGELOG.md
```

---

# Engineering Workflow

Every project developed in this laboratory follows the same engineering lifecycle.

```text
Idea
    ↓
Research
    ↓
Requirements
    ↓
Architecture
    ↓
Architecture Decision Records
    ↓
Implementation
    ↓
Testing
    ↓
Benchmarking
    ↓
Documentation
    ↓
Review
    ↓
Release
```

This workflow emphasizes understanding, reproducibility and long-term maintainability over rapid implementation.

---

# Repository Contents

| Directory        | Description                                             |
| ---------------- | ------------------------------------------------------- |
| `engineering/`   | Engineering principles and development methodology      |
| `architecture/`  | Architectural guidelines and design standards           |
| `documentation/` | Documentation conventions and structure                 |
| `git/`           | Git workflow, branching strategy and commit conventions |
| `adr/`           | Architecture Decision Record standards                  |
<!-- | `testing/`       | Testing philosophy and quality standards                | -->
<!-- | `benchmarking/`  | Benchmarking methodology and evaluation practices       | -->
<!-- | `templates/`     | Reusable project templates                              | -->

---

# Versioning

This repository follows Semantic Versioning.

Major versions introduce significant changes to the engineering methodology.

Minor versions extend or improve existing standards.

Patch versions correct documentation errors or clarify existing guidelines.

---

# Contributing

Engineering standards evolve continuously.

Contributions should improve clarity, consistency or engineering quality while preserving the overall philosophy of the laboratory.

Before proposing major changes, review the existing documentation and, when appropriate, create an Architecture Decision Record explaining the motivation behind the proposal.

---

# Roadmap

Current status:

- ✅ Vision established
- ✅ Engineering standards defined
- ✅ Documentation standards completed
- ✅ Architecture guidelines completed
- ✅ Git workflow established
- ✅ ADR methodology defined

Future iterations will introduce:

- Additional project templates
- Coding standards
- Deployment guidelines
- Security standards
- Data engineering standards
- Machine Learning standards

---

# License

This project is released under the MIT License.

See the `LICENSE` file for additional information.

---

## Final Note

This repository is not intended to document a single project.

It documents the engineering philosophy behind an entire ecosystem of computational intelligence projects.

Every future repository builds upon the foundations established here.
