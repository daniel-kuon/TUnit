---
title: Performance Benchmarks
description: Real-world performance comparisons between TUnit and other .NET testing frameworks
sidebar_position: 1
---

# Performance Benchmarks

:::info Last Updated
These benchmarks were automatically generated on **2026-07-31** from the latest CI run.

**Environment:** Ubuntu Latest • .NET SDK 10.0.302
:::

## 🎯 Executive Summary

TUnit demonstrates significant performance advantages across all testing scenarios:

<div className="benchmark-summary">

### Average Performance vs Other Frameworks

- **1.6x faster** than xUnit v3
- **1.5x faster** than NUnit
- **1.5x faster** than MSTest

</div>

---

## 🚀 Runtime Performance


### results

:::tip Native AOT Performance
TUnit with Native AOT compilation is **14.31x faster** than regular JIT!
:::

**Performance:** **1.55x faster** than xUnit • **1.51x faster** than NUnit • **1.52x faster** than MSTest

| Framework | Version | Mean | Median | StdDev |
|-----------|---------|------|--------|--------|
| 🏆 **TUnit** | 1.0.30 | 379.90 ms | 380.55 ms | 2.824 ms |
| NUnit | 4.4.0 | 574.49 ms | 574.31 ms | 7.958 ms |
| MSTest | 4.0.1 | 578.25 ms | 571.00 ms | 21.361 ms |
| xUnit3 | 3.2.0 | 587.11 ms | 583.47 ms | 15.137 ms |
| 🏆 **TUnit (AOT)** | 1.0.30 | 26.54 ms | 26.43 ms | 1.394 ms |


---

## 🔨 Build Performance

Compilation time comparison across frameworks:

| Framework | Version | Mean | Median | StdDev |
|-----------|---------|------|--------|--------|
| 🏆 **TUnit** | 1.0.30 | 1.754 s | 1.743 s | 0.0656 s |
| Build_NUnit | 4.4.0 | 1.590 s | 1.593 s | 0.0260 s |
| Build_MSTest | 4.0.1 | 1.652 s | 1.655 s | 0.0165 s |
| Build_xUnit3 | 3.2.0 | 1.578 s | 1.578 s | 0.0190 s |


---

## 📊 Methodology

These benchmarks compare TUnit against the most popular .NET testing frameworks:

| Framework | Version Tested |
|-----------|----------------|
| **TUnit** | 1.0.30 |
| **xUnit v3** | 3.2.0 |
| **NUnit** | 4.4.0 |
| **MSTest** | 4.0.1 |

### Test Scenarios

The benchmarks measure real-world testing patterns:

- **DataDrivenTests**: Parameterized tests with multiple data sources
- **AsyncTests**: Realistic async/await patterns with I/O simulation
- **ScaleTests**: Large test suites (1000+ tests) measuring scalability
- **MatrixTests**: Combinatorial test generation and execution
- **MassiveParallelTests**: Parallel execution stress tests

### Environment

- **OS**: Ubuntu Latest (GitHub Actions)
- **Runtime**: .NET 10.0.10 (10.0.10, 10.0.1026.32716), X64 RyuJIT x86-64-v4
- **SDK**: .NET SDK 10.0.302
- **Hardware**: GitHub Actions Standard Runner (Ubuntu)
- **Tool**: BenchmarkDotNet v0.15.6, Linux Ubuntu 24.04.4 LTS (Noble Numbat)

### Why These Numbers Matter

- **No Mocking**: All tests use realistic patterns, not artificial micro-benchmarks
- **Equivalent Logic**: Each framework implements identical test scenarios
- **Warm-Up Excluded**: Measurements exclude JIT warm-up overhead
- **Statistical Rigor**: Multiple iterations with outlier detection

### Source Code

All benchmark source code is available in the [`tools/speed-comparison`](https://github.com/thomhurst/TUnit/tree/main/tools/speed-comparison) directory.

### Interactive Comparison

Want to estimate performance for your test suite? Try the [Benchmark Calculator](/docs/benchmarks/calculator) to see potential time savings.

---

:::note Continuous Benchmarking
These benchmarks run automatically daily via [GitHub Actions](https://github.com/thomhurst/TUnit/actions/workflows/speed-comparison.yml).

Each benchmark runs multiple iterations with statistical analysis to ensure accuracy. Results may vary based on hardware and test characteristics.
:::

*Last generated: 2026-07-31T02:33:46.876Z*
