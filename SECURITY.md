# Security Policy — ArthaOps

ArthaOps takes the security of our platform, our customer data, and our open-source tools with the utmost seriousness.

---

## 🔒 Supported Versions

We provide security updates and critical patches for the following versions of ArthaOps client tools and integrations:

| Tool / Integration | Supported Versions |
|---|---|
| `cost-sentinel-action` | `>= 1.0.0` |
| `terraform-aws-arthaops-role` | `>= 1.0.0` |
| `arthaops-python-client` | `>= 1.0.0` |
| ArthaOps Core Platform (SaaS) | Current Live (Continuous) |

---

## 🛡️ Reporting a Vulnerability

If you discover a security vulnerability in ArthaOps or any associated repository, please report it responsibly:

- **Email**: [`security@arthaops.com`](mailto:security@arthaops.com)
- **PGP Key**: Available upon request for encrypted communication.
- **Expected Response Time**: Within **24 hours** for initial acknowledgment and triage.
- **Remediation SLA**: Critical vulnerabilities are remediated within **48 hours** under our fail-closed incident response protocol.

> [!IMPORTANT]
> **Please do NOT open public GitHub issues or discussions for security vulnerabilities.**

---

## 🏛️ Security & Privacy Guarantees

1. **Zero Data Ingestion**: ArthaOps analyzes cloud metadata and billing exports only. We never access, copy, or persist production databases, application payloads, or customer PII.
2. **Read-Only Least Privilege**: Our AWS integrations operate strictly via scoped AWS STS AssumeRole with external IDs.
3. **Provably-Constrained Safety**: All autonomous actions are validated against an 8-law mathematical Safety Kernel with automatic fail-closed rollback mechanisms.
4. **End-to-End Encryption**: All customer credentials and external IDs are encrypted at rest using AWS KMS and Fernet symmetric ciphers.

---

## 🤝 Responsible Disclosure & Bounty

We deeply appreciate the efforts of security researchers in keeping the cloud ecosystem safe. We adhere to responsible disclosure principles and provide recognition for verified, non-duplicate vulnerability reports.
