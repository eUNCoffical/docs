# Contributing

Contributions to Enhanced UNC Benchmark are welcome.

The goal is to improve test accuracy, coverage, maintainability, and transparency.

## Contribution Principles

### Test Real Behavior

Tests should evaluate what a function actually does.

Checking whether a function exists is not sufficient when behavioral verification is possible.

### Avoid Artificial Success

Do not create tests that automatically pass.

Do not replace missing implementations with placeholder success values.

### Keep Results Honest

Tests should distinguish between:

- Expected behavior observed.
- Expected behavior not observed.
- Behavior that could not be conclusively evaluated.

### Prefer Reproducibility

Tests should be deterministic whenever possible.

Avoid unnecessary timing dependencies, unstable assumptions, or unrelated environmental requirements.

### Handle Errors Properly

Errors should not be silently converted into successful results.

If a test cannot execute reliably, it should produce an appropriate inconclusive result or clearly report the problem.

## Before Submitting

Check that:

- The test evaluates actual behavior.
- Assertions are meaningful.
- Failure conditions are correct.
- Unexpected results are handled.
- The test does not depend unnecessarily on unrelated functions.
- The test does not spoof or modify executor behavior.
- The test is reproducible.

## Reporting Bugs

Open an issue:

https://github.com/EnhancedUNC/eUNC/issues

Describe the problem clearly and include relevant reproduction steps.

## Pull Requests

When submitting a pull request:

- Explain the purpose of the change.
- Describe the behavior being tested.
- Explain any new requirements.
- Include reproduction information when applicable.
- Keep changes focused.

## Philosophy

**No spoof, just proof.**