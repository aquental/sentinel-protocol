<p align="center">
  <img src="assets/sentinel-logo.svg" alt="Sentinel Protocol" width="120" />
</p>

# Contributing to Sentinel Protocol

Thanks for your interest in contributing. Sentinel is an open protocol, and outside contributions make it better. This document explains how to get involved.

## Where to start

If you're new to the project, these are good first steps:

1. Read the [README](README.md) to understand what Sentinel does
2. Browse open [issues](https://github.com/sentinel-protocol/sentinel-protocol/issues) — look for ones labeled `good first issue` or `help wanted`
3. Set up your local environment (instructions below)
4. Pick something small for your first PR

If you're unsure where to help, open an issue or reach out at [sol-sentinel-protocol@proton.me](mailto:sol-sentinel-protocol@proton.me). We're happy to point you in the right direction.

## What we're looking for

**High priority:**

- Bug fixes in the Anchor programs
- Test coverage (unit tests, integration tests, edge cases, fuzzing)
- New framework plugins beyond ElizaOS/GOAT/ZerePy
- Policy templates (pre-built Governor configs for common agent use cases)
- Security review and responsible disclosure

**Always welcome:**

- Documentation improvements and typo fixes
- Code examples and tutorials
- Performance optimizations
- CI/CD improvements
- Translations of docs

**Out of scope (for now):**

- Token-related features (tokenomics design is not finalized)
- Frontend redesigns without prior discussion
- Changes to the core account structures without an RFC

## Development setup

### Prerequisites

- [Rust](https://rustup.rs/) — latest stable
- [Solana CLI](https://docs.solanalabs.com/cli/install) — v1.18+
- [Anchor](https://www.anchor-lang.com/docs/installation) — v0.30+
- [Node.js](https://nodejs.org/) — v18+
- [Yarn](https://yarnpkg.com/) — v1.22+
- [Python](https://python.org/) — 3.10+ (only needed for python-sdk work)

### Getting running

```bash
# Fork the repo on GitHub, then:
git clone https://github.com/your-username/sentinel-protocol.git
cd sentinel-protocol

# Install JS dependencies
yarn install

# Build all Anchor programs
anchor build

# Start a local Solana validator
solana-test-validator

# Run the full test suite
anchor test

# Run a specific test file
anchor test -- --grep "governor-registry"
```

If the build fails, make sure your Solana CLI and Anchor versions match the ones listed in `Anchor.toml`.

### Project layout

```
programs/           Anchor programs (Rust) — the on-chain logic
sdk/                TypeScript SDK and framework plugins
python-sdk/         Python SDK (ZerePy integration)
app/                Governance dashboard (Next.js)
cli/                CLI tool for managing governors
tests/              Integration and stress tests
docs/               Architecture docs and integration guides
examples/           Working code examples
```

## Making changes

### Branch naming

Use a descriptive branch name with a prefix:

- `fix/` — bug fixes (`fix/circuit-breaker-cooldown-overflow`)
- `feat/` — new features (`feat/goat-plugin`)
- `docs/` — documentation (`docs/elizaos-integration-guide`)
- `test/` — test additions (`test/permission-engine-edge-cases`)
- `refactor/` — code cleanup (`refactor/governor-state-layout`)

### Commit messages

Write clear commit messages. We don't enforce a strict format, but please:

- Start with a verb in present tense ("Add spending policy validation", not "Added" or "Adds")
- Keep the first line under 72 characters
- Reference issue numbers when relevant ("Fix cooldown overflow (#42)")

Bad: `update stuff` / `wip` / `fix bug`
Good: `Fix circuit breaker not resetting after cooldown period` / `Add batch validation to Permission Engine`

### Code style

**Rust (Anchor programs):**

- Run `cargo fmt` before committing
- Run `cargo clippy` and address warnings
- Use descriptive variable names — `spending_limit_per_day` over `sl`
- Add doc comments (`///`) on all public functions and structs
- Custom errors should have clear messages

**TypeScript (SDK):**

- Run `yarn lint` before committing
- Use TypeScript strict mode
- Export types for everything public
- Add JSDoc comments on exported functions

**Python (SDK):**

- Follow PEP 8
- Use type hints
- Run `ruff check` before committing

### Testing

Every PR that touches program logic needs tests. No exceptions.

- **Unit tests** — in the same file as the program logic, under `#[cfg(test)]`
- **Integration tests** — in `tests/`, using Anchor's test framework
- **Edge cases matter** — test boundary values, overflow conditions, unauthorized callers, invalid states

```bash
# Run all tests
anchor test

# Run with verbose output
anchor test -- --nocapture

# Run a specific suite
anchor test -- --grep "circuit-breaker"
```

If you're adding a new feature, write at least:

1. A happy-path test (it works as expected)
2. An unauthorized-caller test (someone without permission tries it)
3. A boundary test (max values, zero values, edge conditions)

## Pull requests

### Before submitting

- [ ] Your branch is up to date with `main`
- [ ] All tests pass locally (`anchor test`)
- [ ] `cargo fmt` and `cargo clippy` are clean
- [ ] `yarn lint` passes (if you touched TypeScript)
- [ ] You've added or updated tests for your changes
- [ ] You've updated docs if your change affects the public API

### PR description

Explain what your PR does and why. Include:

- What problem it solves (link the issue if there is one)
- What approach you took and why
- Anything the reviewer should pay attention to
- Screenshots or test output if relevant

### Review process

1. A maintainer will review your PR within a few days
2. We may ask for changes — this is normal and not a rejection
3. Once approved, a maintainer will merge it
4. If your PR sits without review for more than a week, feel free to ping us

### Small PRs are better

A 50-line PR that does one thing gets reviewed in a day. A 500-line PR that does five things sits in the queue. When possible, break large changes into smaller, reviewable pieces.

## Reporting bugs

Open an issue with:

- What you expected to happen
- What actually happened
- Steps to reproduce
- Your environment (OS, Solana CLI version, Anchor version, Node version)
- Relevant logs or error output

## Security vulnerabilities

**Do not open a public issue for security vulnerabilities.**

Email [sol-sentinel-protocol@proton.me](mailto:sol-sentinel-protocol@proton.me) with:

- Description of the vulnerability
- Steps to reproduce or proof of concept
- Your assessment of severity

We will acknowledge receipt within 48 hours and work on a fix. Critical issues get patched within 7 days. You'll be credited in the release notes unless you prefer to stay anonymous.

## RFCs for significant changes

If you want to propose a change to the core protocol (account structures, instruction interfaces, program architecture), please open an RFC issue first. Tag it with `rfc` and describe:

- The problem you're solving
- Your proposed solution
- Alternatives you considered
- Impact on existing users

This lets us discuss the design before you write code, so nobody wastes time on an approach that won't be merged.

## Code of conduct

Be respectful. We're building infrastructure that agents and developers depend on — the bar is high for both code quality and how we treat each other. Harassment, trolling, and bad-faith arguments will get you blocked.

## License

By contributing to Sentinel Protocol, you agree that your contributions will be licensed under the [Apache 2.0 License](LICENSE).

## Questions?

- **Email:** [sol-sentinel-protocol@proton.me](mailto:sol-sentinel-protocol@proton.me)
- **X/Twitter:** [@sln_sentinel_ai](https://x.com/sln_sentinel_ai)
- **Issues:** [GitHub Issues](https://github.com/sentinel-protocol/sentinel-protocol/issues)
