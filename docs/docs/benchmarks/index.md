---
title: Performance Benchmarks
description: Real-world performance comparisons between TUnit and other .NET testing frameworks
sidebar_position: 1
---

# Performance Benchmarks

:::info Last Updated
These benchmarks were automatically generated on **2026-02-10** from the latest CI run.

**Environment:** Ubuntu Latest • .NET SDK 10.0.102
:::

## 🎯 Executive Summary

TUnit demonstrates significant performance advantages across all testing scenarios:

<div className="benchmark-summary">

### Average Performance vs Other Frameworks

- **0.0x faster** than xUnit v3
- **0.0x faster** than NUnit
- **0.0x faster** than MSTest

</div>

---

## 🚀 Runtime Performance


### results

:::tip Native AOT Performance
TUnit with Native AOT compilation is **6.50x faster** than regular JIT!
:::

**Performance:** **0.00x faster** than xUnit • **0.00x faster** than NUnit • **0.00x faster** than MSTest

| Framework | Version | Mean | Median | StdDev |
|-----------|---------|------|--------|--------|
| 🏆 **TUnit** | 1.0.30 | 513.53 ms | 513.66 ms | 2.445 ms |
| NUnit | 4.4.0 | 1,557.51 ms | 1,557.61 ms | 11.158 ms |
| MSTest | 4.0.1 | 1,506.47 ms | 1,505.43 ms | 8.327 ms |
| xUnit3 | 3.2.0 | 1,605.46 ms | 1,602.74 ms | 10.863 ms |
| 🏆 **TUnit (AOT)** | 1.0.30 | 78.95 ms | 78.91 ms | 0.438 ms |


---

## 🔨 Build Performance

Compilation time comparison across frameworks:

| Framework | Version | Mean | Median | StdDev |
|-----------|---------|------|--------|--------|
| 🏆 **TUnit** | 1.0.30 | 1.747 s | 1.747 s | 0.0290 s |
| Build_NUnit | 4.4.0 | 1.516 s | 1.517 s | 0.0121 s |
| Build_MSTest | 4.0.1 | 1.593 s | 1.587 s | 0.0180 s |
| Build_xUnit3 | 3.2.0 | 1.530 s | 1.531 s | 0.0212 s |


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
- **Runtime**: .NET 10.0.2 (10.0.2, 10.0.225.61305), X64 RyuJIT x86-64-v3
- **SDK**: .NET SDK 10.0.102
- **Hardware**: GitHub Actions Standard Runner (Ubuntu)
- **Tool**: BenchmarkDotNet v0.15.6, Linux Ubuntu 24.04.3 LTS (Noble Numbat)

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

*Last generated: 2026-02-10T00:35:00.134Z*
