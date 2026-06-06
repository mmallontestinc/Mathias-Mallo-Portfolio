# Mathias Mallo -- Technical Portfolio

**IT Operations | Security & Compliance Operations | AI-Augmented Engineering**

This repository summarizes selected internal and proprietary projects in a sanitized format. The original codebases are private because they support real operational, compliance, and product-adjacent workflows.

**Public-safe summary:** This portfolio contains public-safe summaries, architecture descriptions, and case studies. It does not include proprietary source code, customer data, credentials, internal infrastructure details, confidential audit evidence, private screenshots, or confidential NTest information.

## Ownership

The projects documented in this portfolio were conceived, architected, and developed by me in support of real operational, compliance, and engineering challenges.

Where AI-assisted engineering methodologies were used, all architectural decisions, validation, governance decisions, and production outcomes remained under human ownership and review.

## Impact Highlights

- Developed governance and evidence-management tooling utilized during successful SOC 2 Type 2 certification activities.
- Established the validation framework that enabled migration from legacy Linux 14 virtualization environments toward native Linux 24 operation.
- Validated specialized trace-processing workflows through millions of trace-processing operations.
- Built multi-system evidence correlation across Microsoft Graph research, Teams context, GitLab activity, support records, SLA versions, release history, and affected customer environments.
- Supported global operational contexts spanning North America, Europe, LATAM, Africa, and Asia.

## Featured Projects

| Project | Problem | Solution | Technologies | Impact |
| --- | --- | --- | --- | --- |
| [EverForge Governance & Operations Platform](docs/everforge-governance-platform.md) | Compliance and operational workflows were spread across tools, documents, and manual follow-up. | Built a governed operations platform with a Rust core API, worker-backed execution, evidence promotion, scheduled reporting, and an operator console. | Rust, Python, React, Tauri, SQLite/PostgreSQL concepts, background services | Developed governance and evidence-management tooling utilized during successful SOC 2 Type 2 certification activities. |
| [Compliance Intelligence & Evidence Correlation Engine](docs/compliance-intelligence-engine.md) | Audit evidence was fragmented across support records, communications, releases, access records, and customer-impact timelines. | Designed a correlation workflow that reconstructs event history and prepares audit-ready evidence packages from multiple systems. | Python, Microsoft Graph concepts, Teams, GitLab, ticketing/support records, reporting workflows | Reduced manual evidence reconstruction effort and improved confidence in audit narratives. |
| [NTest Kernel Compatibility Engine](docs/kernel-compatibility-engine.md) | Legacy Linux virtualization remained a dependency for specialized OTDR hardware and trace workflows. | Built a validation framework comparing legacy oracle behavior against Linux 24 native candidates and compatibility mappings. | Python, Shell, C, Java, Linux, kernel modules, hardware validation workflows | Solved a decade-old operational constraint by creating a repeatable compatibility-validation framework for Linux 24 migration. |
| [NTest SBOM Scanner](docs/sbom-scanner.md) | Vulnerability visibility and SBOM review required manual command-line workflows. | Built desktop tools that wrap SBOM scanning, vulnerability review, and report export workflows. | JavaFX, Maven, Rust, Tauri, TypeScript, Syft, Grype | Improved software inventory and vulnerability reporting for support, QA, and compliance workflows. |
| [FiberWatch macOS Compatibility Validation](docs/macos-compatibility-validation.md) | Apple ecosystem compatibility needed practical validation and troubleshooting support. | Participated in AI-assisted testing and troubleshooting workflows while applying hands-on Apple device experience. | macOS, iOS, iPadOS, watchOS, troubleshooting, AI-assisted validation | Added structured compatibility feedback without overstating enterprise MDM administration experience. |

## Skills

| Operations & Support | Security & Compliance | Platforms & Tooling | Engineering |
| --- | --- | --- | --- |
| IT Operations | SOC 2 Type 2 | Windows/Linux/macOS | Python |
| Remote support | Compliance automation | Azure VMs | Java |
| VPN onboarding | Evidence management | Hyper-V | Rust |
| Device support | Audit reporting | VirtualBox | React/Tauri |
| Documentation | Secure access workflows | GitHub/GitLab | AI-assisted engineering |

## Portfolio Structure

- [Docs index](docs/index.md)
- [About me](docs/about-me.md)
- [Privacy and redaction policy](docs/privacy-and-redaction.md)
- [Architecture diagrams](assets/diagrams/)
- [Case studies](case-studies/)
- [Documentation templates](templates/)

## Contact

- Email: [mathias.mallo@icloud.com](mailto:mathias.mallo@icloud.com)
- GitHub: [github.com/mmallontestinc](https://github.com/mmallontestinc)
- Website: [mmalloitconsultant.com](https://mmalloitconsultant.com)
- Location: Spain / Remote

## Public Review Boundary

Private/proprietary source code is not included. Architecture is generalized for public review, and all sensitive operational details have been removed or abstracted.
