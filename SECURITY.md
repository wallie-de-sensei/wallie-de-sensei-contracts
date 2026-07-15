# Security Policy

## Reporting Security Vulnerabilities

**Please do not report security vulnerabilities through public GitHub issues.**

If you discover a security vulnerability in Wallie de Sensei Contracts, please report it privately to help us address it before public disclosure.

### How to Report

1. **Email**: Send details to security@wallie-de-sensei.io (or create a private security advisory on GitHub)
2. **Include**:
   - Description of the vulnerability
   - Steps to reproduce
   - Potential impact assessment
   - Suggested fix (if available)
3. **Response Time**: We aim to acknowledge reports within 48 hours

### What to Expect

- **Acknowledgment**: We'll confirm receipt of your report
- **Assessment**: We'll evaluate the severity and impact
- **Fix Development**: We'll work on a patch
- **Disclosure**: We'll coordinate disclosure timing with you
- **Credit**: We'll credit you in release notes (unless you prefer to remain anonymous)

## Security Best Practices

### For Users

When deploying or interacting with these contracts:

- **Verify contract addresses** before interacting
- **Test on testnet first** before mainnet deployment
- **Use hardware wallets** for admin operations
- **Review all transaction details** before signing
- **Monitor contract events** for unexpected activity

### For Developers

When contributing to this codebase:

- **Follow CEI pattern** (Checks-Effects-Interactions) for all state changes
- **Validate all inputs** before processing
- **Test overflow scenarios** in arithmetic operations
- **Require authorization** on state-changing functions
- **Write security tests** for edge cases and adversarial scenarios
- **Review [docs/security.md](docs/security.md)** for detailed guidelines

## Security Features

### Access Control
- Admin-only functions for critical operations
- Sender/recipient authorization on stream operations
- Global emergency pause capability

### Economic Safety
- Overflow protection in accrual calculations
- Deposit validation before stream creation
- Withdrawal limits based on accrued amounts

### Audit Trail
- Comprehensive event emission for all state changes
- Immutable audit log via blockchain events
- Transparent contract version tracking

## Known Limitations

See [contracts/stream/SECURITY.md](contracts/stream/SECURITY.md) for detailed security analysis and known considerations.

## Security Audits

| Version | Audit Firm | Date | Report |
|---------|-----------|------|--------|
| TBD     | TBD       | TBD  | TBD    |

_(No external audits completed yet. This is alpha software.)_

## Responsible Disclosure

We believe in responsible disclosure and will:

- Work with security researchers to validate and fix issues
- Provide appropriate credit for discoveries
- Coordinate disclosure timing
- Publish security advisories for confirmed vulnerabilities

## Bug Bounty Program

_(Coming soon)_

## Security Resources

- **Documentation**: [docs/security.md](docs/security.md)
- **CEI Analysis**: [contracts/stream/CEI_ANALYSIS.md](contracts/stream/CEI_ANALYSIS.md)
- **Error Codes**: [docs/error.md](docs/error.md)
- **Audit Prep**: [docs/audit.md](docs/audit.md)

---

Thank you for helping keep Wallie de Sensei secure! 🔒
