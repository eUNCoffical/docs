# Running eUNC

This page explains how eUNC runs its benchmark and produces results.

## Execution Overview

The benchmark follows a general execution process:

1. Initialize the benchmark configuration.
2. Load the required modules.
3. Identify the executor when possible.
4. Load the test manifest.
5. Execute the registered tests.
6. Classify each result.
7. Generate the final report.
8. Optionally save the report to a file.

## Loading eUNC

A typical loader looks like this:

\`\`\`lua
loadstring(game:HttpGet(
    "https://raw.githubusercontent.com/EnhancedUNC/eUNC/main/src/main.lua"
))()
\`\`\`

This retrieves and executes the benchmark's main entry point.

The loader requires the execution environment to support the functions used by the loading process.

## Test Execution

Tests are loaded through the benchmark's manifest.

Each test is expected to expose a callable Run function.

The runner executes individual tests and classifies their outcomes.

Tests should evaluate actual behavior rather than simply checking whether a function exists.

## Result Classification

Each test receives one of three statuses:

- PASS
- NOT PASSED
- UNKNOWN

See [Understanding Results](results.md).

## Individual Results

Individual results can be displayed as the benchmark executes or after the test runner completes.

The debug configuration controls certain output and timing options.

See [Debug Configuration](debug-configuration.md).

## Final Report

The final report contains information such as:

- Total tests
- Passed tests
- Tests that did not pass
- Unknown tests
- Overall score
- Test duration
- Category results

The exact information available depends on the benchmark version.

## Saving Results

eUNC can optionally export its report to a JSON file.

The export requires the executor environment to provide the necessary file-writing functionality.

See [Debug Configuration](debug-configuration.md).