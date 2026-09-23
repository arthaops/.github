## Description
<!-- Provide a clear, concise summary of the change and the motivation behind it. -->

## Type of Change
- [ ] 🐛 Bug fix (non-breaking change fixing an issue)
- [ ] ✨ New feature / enhancement (non-breaking change adding functionality)
- [ ] 🔒 Security hardening
- [ ] 📚 Documentation update
- [ ] 🧪 CI/CD or test harness improvement

## Security Invariants Checklist
- [ ] **100% Read-Only**: This change does NOT introduce mutating or destructive cloud permissions.
- [ ] **Zero Data Ingestion**: This change does NOT request access to database contents, object storage payloads, or customer PII.
- [ ] **Confused Deputy Immunity**: Any IAM trust policies maintain strict external identity validation.
- [ ] **Code Quality**: Formatted with `tofu fmt` and passes `tofu validate`.
