# Contributing to ArthaOps Open Source Ecosystem

Thank you for your interest in contributing to ArthaOps open-source modules and developer tools!

ArthaOps is dedicated to autonomous multi-cloud infrastructure intelligence with provable safety and zero customer disruption.

---

## 🔒 Security & Architectural Invariants

Before contributing, please note the fundamental design invariants governing all ArthaOps public modules:

1. **100% Read-Only Safety**: Distribution modules (such as IAM roles and telemetry connectors) must **never** request mutating, creating, or deleting permissions. All grants must adhere strictly to the principle of least privilege.
2. **Confused Deputy Defense**: Cloud onboarding templates must enforce strict external identifiers (`ExternalId` in AWS, Tenant/App validation in Azure, Workload Identity Audience in GCP) to prevent cross-tenant impersonation.
3. **Zero Production Data Access**: Connectors may only query infrastructure metadata, resource topologies, and cost/telemetry APIs. They must never request access to production database records, object store payloads, or customer PII.
4. **Clean HCL & OpenTofu Standards**: All Terraform modules must pass `tofu fmt -check` and `tofu validate` with zero warnings.

---

## 🛠️ Development & Submission Process

1. **Fork the Repository**: Create a branch off `main` (e.g. `feat/add-govcloud-partition` or `fix/iam-path-normalization`).
2. **Format and Validate**:
   ```bash
   tofu fmt -check
   tofu validate
   ```
3. **Commit Messages**: Follow [Conventional Commits](https://www.conventionalcommits.org/) (`feat: ...`, `fix: ...`, `docs: ...`, `ci: ...`).
4. **Open a Pull Request**: Provide a clear description of the change, why it is needed, and evidence of local verification.

---

## 🛡️ Responsible Vulnerability Disclosure

If you discover a security vulnerability, please **DO NOT** open a public issue. Review our [SECURITY.md](SECURITY.md) and report it directly to:
[`security@arthaops.com`](mailto:security@arthaops.com).
