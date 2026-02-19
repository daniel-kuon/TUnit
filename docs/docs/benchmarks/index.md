---
title: Performance Benchmarks
description: Real-world performance comparisons between TUnit and other .NET testing frameworks
sidebar_position: 1
---

# Performance Benchmarks

:::info Last Updated
These benchmarks were automatically generated on **2026-02-19** from the latest CI run.

**Environment:** Ubuntu Latest • .NET SDK 10.0.103
:::

## 🎯 Executive Summary

TUnit demonstrates significant performance advantages across all testing scenarios:

<div className="benchmark-summary">

### Average Performance vs Other Frameworks

- **1.3x faster** than xUnit v3
- **1.3x faster** than NUnit
- **1.3x faster** than MSTest

</div>

---

## 🚀 Runtime Performance


### results

:::tip Native AOT Performance
TUnit with Native AOT compilation is **12.39x faster** than regular JIT!
:::

**Performance:** **1.34x faster** than xUnit • **1.34x faster** than NUnit • **1.34x faster** than MSTest

| Framework | Version | Mean | Median | StdDev |
|-----------|---------|------|--------|--------|
| 🏆 **TUnit** | 1.0.30 | 490.24 ms | 489.66 ms | 5.627 ms |
| NUnit | 4.4.0 | 656.19 ms | 651.48 ms | 13.915 ms |
| MSTest | 4.0.1 | 655.15 ms | 655.28 ms | 6.523 ms |
| xUnit3 | 3.2.0 | 657.28 ms | 657.43 ms | 7.674 ms |
| 🏆 **TUnit (AOT)** | 1.0.30 | 39.57 ms | 39.20 ms | 1.905 ms |


---

## 🔨 Build Performance

Compilation time comparison across frameworks:

| Framework | Version | Mean | Median | StdDev |
|-----------|---------|------|--------|--------|
| 🏆 **TUnit** | 1.0.30 | 1.783 s | 1.784 s | 0.0287 s |
| Build_NUnit | 4.4.0 | 1.548 s | 1.544 s | 0.0150 s |
| Build_MSTest | 4.0.1 | 1.634 s | 1.639 s | 0.0131 s |
| Build_xUnit3 | 3.2.0 | 1.545 s | 1.543 s | 0.0161 s |


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
- **Runtime**: .NET 10.0.3 (10.0.3, 10.0.326.7603), X64 RyuJIT x86-64-v3
- **SDK**: .NET SDK 10.0.103
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

*Last generated: 2026-02-19T00:30:40.173Z*
