# Getting Started

Welcome to Enhanced UNC Benchmark (eUNC).

This guide explains how to get started with eUNC and understand its basic operation.

## Requirements

eUNC requires a Roblox execution environment capable of running its Lua source code.

Depending on the tests being executed, individual executor capabilities may be required.

Some tests may not be applicable to every executor.

## Getting eUNC

The official source repository is:

https://github.com/EnhancedUNC/eUNC

Always obtain eUNC from the official repository.

## Running the Benchmark

The general process is:

1. Load eUNC using your executor.
2. Allow the benchmark to execute its tests.
3. Review the individual test results.
4. Review the final report.
5. Investigate failures or unknown results when necessary.

See [Running eUNC](running-eunc.md) for more information.

## Understanding Results

eUNC uses three result classifications:

| Symbol | Meaning |
|---|---|
| ✅ | PASS |
| ❌ | NOT PASSED |
| ⏺️ | UNKNOWN |

These classifications represent the observed outcome of individual tests.

See [Understanding Results](results.md).

## Important

eUNC does not certify executor safety.

Passing tests indicates that specific expected behavior was observed. It does not establish that an executor is secure or trustworthy.