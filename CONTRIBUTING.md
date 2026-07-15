# Contributing to Wallie de Sensei Contracts

Thank you for your interest in contributing to Wallie de Sensei! This guide will help you get started with contributing through the Wave Program.

## 🌊 Wave Program

The Wave Program is our structured contribution system where maintainers create scoped issues for contributors to pick up during sprint cycles. See [plan.md](plan.md) for the types of work available.

## Getting Started

### 1. Set Up Your Development Environment

```bash
# Clone the repository
git clone https://github.com/wallie-de-sensei/wallie-de-sensei-contracts.git
cd wallie-de-sensei-contracts

# Install Rust (version 1.94.1 is automatically enforced)
rustup toolchain install

# Add WebAssembly target
rustup target add wasm32-unknown-unknown

# Build the project
cargo build --workspace

# Run tests
cargo test --workspace
```

### 2. Find an Issue

Browse open issues labeled with:
- `wave-program` - Issues available for Wave Program contributors
- `good-first-issue` - Great for newcomers
- `bug`, `feature`, `documentation`, `testing` - Different work types

### 3. Claim an Issue

Comment on the issue to let maintainers know you're working on it. We'll assign it to you and provide any additional context needed.

## Development Workflow

### Branch Naming

Create a descriptive branch name:
- `fix/issue-number-short-description` for bug fixes
- `feat/issue-number-short-description` for features
- `docs/issue-number-short-description` for documentation
- `test/issue-number-short-description` for tests

Example: `fix/42-stream-calculation-overflow`

### Making Changes

1. **Write clear, documented code** - Add comments for complex logic
2. **Follow Rust conventions** - Use `cargo fmt` and `cargo clippy`
3. **Maintain test coverage** - Aim for 95%+ coverage on new code
4. **Update documentation** - Keep docs in sync with code changes

### Testing Requirements

Run the full test suite before submitting:

```bash
# Run all tests
cargo test --workspace

# Run specific contract tests
cargo test -p fluxora_stream
cargo test -p factory
cargo test -p governance

# Run with verbose output
cargo test -- --nocapture

# Run property-based tests with more cases
PROPTEST_CASES=10000 cargo test -p fluxora_stream --test balance_conservation
```

### Code Quality Checks

```bash
# Format code
cargo fmt --all

# Run linter
cargo clippy --all-targets --all-features -- -D warnings

# Build for WebAssembly
cargo build --target wasm32-unknown-unknown --workspace
```

## Submitting Your Work

### Pull Request Process

1. **Commit your changes** with clear messages:
   ```bash
   git add .
   git commit -m "fix: resolve stream calculation overflow in edge case"
   ```

2. **Push to your branch**:
   ```bash
   git push origin fix/42-stream-calculation-overflow
   ```

3. **Open a Pull Request** with:
   - Clear title describing the change
   - Reference to the issue number (e.g., "Fixes #42")
   - Description of what changed and why
   - Test results and coverage information
   - Screenshots or examples if applicable

### Pull Request Template

```markdown
## Description
Brief description of changes

## Related Issue
Fixes #issue-number

## Changes Made
- Bullet list of key changes
- Include file paths if helpful

## Testing
- [ ] All existing tests pass
- [ ] Added new tests for changes
- [ ] Manually tested functionality
- [ ] Property-based tests pass (if applicable)

## Checklist
- [ ] Code follows project style guidelines
- [ ] Documentation updated
- [ ] No compiler warnings
- [ ] Commit messages are clear
```

## Code Review

Maintainers will review your PR and may:
- Request changes or clarifications
- Suggest improvements
- Ask for additional tests
- Approve and merge

Please be responsive to feedback and iterate on your submission.

## Testing Standards

### Unit Tests
- Test each function's happy path and edge cases
- Use descriptive test names: `test_withdraw_after_cliff_period`
- Include boundary value tests

### Integration Tests
- Test complete workflows end-to-end
- Verify contract interactions
- Test authorization and access control

### Property-Based Tests
- Use `proptest` for randomized testing
- Define invariants that must always hold
- Add regression test cases

### Example Test Structure

```rust
#[test]
fn test_stream_accrual_respects_cliff() {
    let env = Env::default();
    // Setup
    let contract = create_contract(&env);
    
    // Test before cliff
    assert_eq!(contract.calculate_accrued(stream_id), 0);
    
    // Test after cliff
    advance_time(&env, cliff_time + 1);
    assert!(contract.calculate_accrued(stream_id) > 0);
}
```

## Documentation Standards

- Add inline comments for complex logic
- Update relevant markdown files in `docs/`
- Include examples in documentation
- Document all public functions and types
- Explain _why_, not just _what_

## Security Considerations

When working on this codebase:

1. **Never compromise CEI (Checks-Effects-Interactions) ordering**
2. **Always validate input parameters**
3. **Test overflow scenarios for arithmetic operations**
4. **Verify authorization on all state-changing functions**
5. **Consider reentrancy implications**
6. **Test with malicious inputs**

See [docs/security.md](docs/security.md) for detailed security guidelines.

## Getting Help

- **Questions?** Ask in the issue you're working on
- **Stuck?** Request guidance from maintainers
- **Found a problem?** Open a new issue with details

## Recognition

Contributors will be recognized in:
- Release notes and changelogs
- GitHub contributor list
- Wave Program leaderboards (coming soon)

## License

By contributing, you agree that your contributions will be licensed under the same license as the project.

---

Happy coding! 🚀
