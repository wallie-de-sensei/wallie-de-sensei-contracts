# Documentation Index

Welcome to the Wallie de Sensei Contracts documentation! This directory contains comprehensive technical documentation for developers, auditors, and contributors.

## 📖 Getting Started

New to the project? Start with these:

1. **[streaming.md](streaming.md)** - Core streaming protocol concepts and lifecycle
2. **[DEPLOYMENT.md](DEPLOYMENT.md)** - Step-by-step deployment guide
3. **[security.md](security.md)** - Security model and best practices

## 🏗️ Architecture & Design

- **[streaming.md](streaming.md)** - Stream lifecycle, accrual formula, access control
- **[storage.md](storage.md)** - Contract storage architecture and TTL policies
- **[factory.md](factory.md)** - Factory contract design and stream instantiation
- **[governance.md](governance.md)** - Governance mechanisms and proposals
- **[stream-templates.md](stream-templates.md)** - Reusable stream templates
- **[token-assumptions.md](token-assumptions.md)** - Token trust model and assumptions

## 🔒 Security

- **[security.md](security.md)** - CEI ordering, authorization, overflow protection
- **[audit.md](audit.md)** - Entry points and invariants for auditors
- **[maintainer-security-checklist.md](maintainer-security-checklist.md)** - Security checklist for maintainers
- **[ABI_STABILITY.md](ABI_STABILITY.md)** - ABI stability guarantees
- **[formal-verification.md](formal-verification.md)** - Formal verification notes

## 🚀 Deployment

- **[DEPLOYMENT.md](DEPLOYMENT.md)** - Testnet deployment checklist
- **[mainnet.md](mainnet.md)** - Mainnet deployment guide
- **[mainnet-deployment-checklist-alignment.md](mainnet-deployment-checklist-alignment.md)** - Mainnet checklist alignment
- **[upgrade.md](upgrade.md)** - Contract upgrade strategy and migration

## 🧪 Testing

- **[test-coverage.md](test-coverage.md)** - Test coverage standards and reports
- **[snapshot-tests.md](snapshot-tests.md)** - Snapshot testing methodology
- **[snapshot-test-coverage-matrix.md](snapshot-test-coverage-matrix.md)** - Coverage matrix
- **[snapshot-test-authoring-guide.md](snapshot-test-authoring-guide.md)** - How to write snapshot tests
- **[snapshot-workflow-quick-reference.md](snapshot-workflow-quick-reference.md)** - Quick reference guide
- **[pr-accrual-property-tests.md](pr-accrual-property-tests.md)** - Property-based test documentation

## 📚 API Reference

- **[error.md](error.md)** - Complete error code reference
- **[events.md](events.md)** - Event schemas and topics
- **[dust-threshold.md](dust-threshold.md)** - Dust threshold calculations
- **[recipient-stream-index.md](recipient-stream-index.md)** - Recipient indexing design

## 🔧 Implementation Details

- **[cancel-stream-semantics.md](cancel-stream-semantics.md)** - Stream cancellation behavior
- **[global-resume.md](global-resume.md)** - Global resume functionality
- **[extend-underfunding-fix.md](extend-underfunding-fix.md)** - Stream extension edge cases
- **[stream-id-monotonicity-uniqueness.md](stream-id-monotonicity-uniqueness.md)** - Stream ID design
- **[gas.md](gas.md)** - Gas optimization and budget notes
- **[indexer-derivation.md](indexer-derivation.md)** - Off-chain indexer design

## 📋 Alignment & Validation

- **[PROTOCOL_NARRATIVE_VS_CODE_ALIGNMENT.md](PROTOCOL_NARRATIVE_VS_CODE_ALIGNMENT.md)** - Protocol alignment validation
- **[protocol-narrative-code-alignment.md](protocol-narrative-code-alignment.md)** - Additional alignment docs

## 🌊 For Wave Program Contributors

If you're contributing through the Wave Program:

1. **Read**: [streaming.md](streaming.md) for core concepts
2. **Review**: [security.md](security.md) for security patterns
3. **Understand**: [test-coverage.md](test-coverage.md) for testing standards
4. **Reference**: [error.md](error.md) and [events.md](events.md) during development

## 📖 Document Conventions

- **`.md`** - All documentation is in Markdown format
- **Code blocks** - Include syntax highlighting for code examples
- **Links** - Use relative links between documents
- **Updates** - Keep docs in sync with code changes

## 🤝 Contributing to Documentation

When updating documentation:

1. Follow existing format and style
2. Include code examples where helpful
3. Update this README if adding new documents
4. Verify all links work correctly
5. Keep language clear and concise

---

For general contribution guidelines, see [../CONTRIBUTING.md](../CONTRIBUTING.md)
