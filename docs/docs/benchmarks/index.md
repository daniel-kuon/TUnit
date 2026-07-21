---
title: Performance Benchmarks
description: Real-world performance comparisons between TUnit and other .NET testing frameworks
sidebar_position: 1
---

# Performance Benchmarks

:::info Last Updated
These benchmarks were automatically generated on **2026-07-21** from the latest CI run.

**Environment:** Ubuntu Latest • .NET SDK 10.0.302
:::

## 🎯 Executive Summary

TUnit demonstrates significant performance advantages across all testing scenarios:

<div className="benchmark-summary">

### Average Performance vs Other Frameworks

- **1.2x faster** than xUnit v3
- **1.2x faster** than NUnit
- **1.0x faster** than MSTest

</div>

---

## 🚀 Runtime Performance


### results

:::tip Native AOT Performance
TUnit with Native AOT compilation is **10.23x faster** than regular JIT!
:::

**Performance:** **1.16x faster** than xUnit • **1.16x faster** than NUnit • **1.00x faster** than MSTest

| Framework | Version | Mean | Median | StdDev |
|-----------|---------|------|--------|--------|
| 🏆 **TUnit** | 1.0.30 | 511.31 ms | 511.46 ms | 5.977 ms |
| NUnit | 4.4.0 | 595.66 ms | 593.81 ms | 11.346 ms |
| MSTest | 4.0.1 | 509.17 ms | 505.46 ms | 8.893 ms |
| xUnit3 | 3.2.0 | 594.25 ms | 591.71 ms | 7.850 ms |
| 🏆 **TUnit (AOT)** | 1.0.30 | 49.99 ms | 49.62 ms | 3.763 ms |


---

## 🔨 Build Performance

Compilation time comparison across frameworks:

| Framework | Version | Mean | Median | StdDev |
|-----------|---------|------|--------|--------|
| 🏆 **TUnit** | 1.0.30 | 1.814 s | 1.803 s | 0.0599 s |
| Build_NUnit | 4.4.0 | 1.673 s | 1.667 s | 0.0231 s |
| Build_MSTest | 4.0.1 | 1.703 s | 1.708 s | 0.0264 s |
| Build_xUnit3 | 3.2.0 | 1.644 s | 1.641 s | 0.0189 s |


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
- **Runtime**: .NET 10.0.10 (10.0.10, 10.0.1026.32716), X64 RyuJIT x86-64-v3
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

*Last generated: 2026-07-21T02:27:44.072Z*
