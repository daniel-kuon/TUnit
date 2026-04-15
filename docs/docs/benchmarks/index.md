---
title: Performance Benchmarks
description: Real-world performance comparisons between TUnit and other .NET testing frameworks
sidebar_position: 1
---

# Performance Benchmarks

:::info Last Updated
These benchmarks were automatically generated on **2026-04-15** from the latest CI run.

**Environment:** Ubuntu Latest • .NET SDK 10.0.202
:::

## 🎯 Executive Summary

TUnit demonstrates significant performance advantages across all testing scenarios:

<div className="benchmark-summary">

### Average Performance vs Other Frameworks

- **1.3x faster** than xUnit v3
- **1.3x faster** than NUnit
- **1.2x faster** than MSTest

</div>

---

## 🚀 Runtime Performance


### results

:::tip Native AOT Performance
TUnit with Native AOT compilation is **4.42x faster** than regular JIT!
:::

**Performance:** **1.33x faster** than xUnit • **1.25x faster** than NUnit • **1.18x faster** than MSTest

| Framework | Version | Mean | Median | StdDev |
|-----------|---------|------|--------|--------|
| 🏆 **TUnit** | 1.0.30 | 542.2 ms | 542.2 ms | 3.47 ms |
| NUnit | 4.4.0 | 679.1 ms | 681.0 ms | 7.44 ms |
| MSTest | 4.0.1 | 642.4 ms | 641.4 ms | 10.11 ms |
| xUnit3 | 3.2.0 | 723.7 ms | 720.8 ms | 8.19 ms |
| 🏆 **TUnit (AOT)** | 1.0.30 | 122.8 ms | 122.9 ms | 0.27 ms |


---

## 🔨 Build Performance

Compilation time comparison across frameworks:

| Framework | Version | Mean | Median | StdDev |
|-----------|---------|------|--------|--------|
| 🏆 **TUnit** | 1.0.30 | 1.799 s | 1.809 s | 0.0288 s |
| Build_NUnit | 4.4.0 | 1.611 s | 1.611 s | 0.0271 s |
| Build_MSTest | 4.0.1 | 1.708 s | 1.708 s | 0.0141 s |
| Build_xUnit3 | 3.2.0 | 1.615 s | 1.615 s | 0.0154 s |


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
- **Runtime**: .NET 10.0.6 (10.0.6, 10.0.626.17701), X64 RyuJIT x86-64-v3
- **SDK**: .NET SDK 10.0.202
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

*Last generated: 2026-04-15T00:39:11.451Z*
