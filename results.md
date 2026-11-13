# Understanding Results

This page explains how to interpret eUNC benchmark results.

## Test Statuses

### ✅ PASS

The test observed the expected behavior.

A passing result indicates that the tested behavior worked under the conditions of that test.

It does not guarantee that every possible use of the function is correct.

### ❌ NOT PASSED

The test did not observe the expected behavior.

Possible reasons include:

- The function is unavailable.
- The function behaves differently than expected.
- The executor implements only part of the tested behavior.
- The test encountered an environment-specific limitation.
- The test contains an incorrect assumption or assertion.

A failed test should not automatically be interpreted as proof that an executor is malicious.

### ⏺️ UNKNOWN

The test could not produce a conclusive PASS or NOT PASSED result.

Unknown results may occur when:

- The test returns an unsupported result.
- The test cannot determine whether the expected behavior occurred.
- The execution environment prevents a reliable conclusion.

UNKNOWN is not equivalent to PASS.

## Overall Score

The current runner calculates its overall score using:

```
Score = Passed Tests / Total Tests
```

Unknown tests remain included in the total test count.

This means that an unknown result does not count as a successful test.

## Category Scores

Category scores represent the proportion of tests passed within a category.

They should be interpreted alongside the number of tests in that category.

## Executor Identification

Executor identification is separate from benchmark results.

An identified executor name or version is informational and should not be treated as proof of authenticity.

## eID

The report may include an eID field.

An eID should not automatically be interpreted as a cryptographic signature, proof of report integrity, or verification of executor identity.

## Important Disclaimer

A benchmark score is not a security rating.

A high score does not prove:

- The executor is safe.
- The executor is malware-free.
- The executor cannot steal information.
- The executor cannot manipulate results.
- The executor implements every UNC function correctly.

A benchmark can only provide evidence about the behaviors it actually tests.