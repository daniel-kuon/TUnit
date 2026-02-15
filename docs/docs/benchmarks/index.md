---
title: Performance Benchmarks
description: Real-world performance comparisons between TUnit and other .NET testing frameworks
sidebar_position: 1
---

# Performance Benchmarks

:::info Last Updated
These benchmarks were automatically generated on **2026-02-15** from the latest CI run.

**Environment:** Ubuntu Latest • .NET SDK 10.0.103
:::

## 🎯 Executive Summary

TUnit demonstrates significant performance advantages across all testing scenarios:

<div className="benchmark-summary">

### Average Performance vs Other Frameworks

- **1.4x faster** than xUnit v3
- **1.4x faster** than NUnit
- **1.4x faster** than MSTest

</div>

---

## 🚀 Runtime Performance


### results

:::tip Native AOT Performance
TUnit with Native AOT compilation is **10.34x faster** than regular JIT!
:::

**Performance:** **1.40x faster** than xUnit • **1.38x faster** than NUnit • **1.39x faster** than MSTest

| Framework | Version | Mean | Median | StdDev |
|-----------|---------|------|--------|--------|
| 🏆 **TUnit** | 1.0.30 | 465.28 ms | 464.50 ms | 7.501 ms |
| NUnit | 4.4.0 | 643.96 ms | 641.96 ms | 7.805 ms |
| MSTest | 4.0.1 | 645.19 ms | 642.31 ms | 9.476 ms |
| xUnit3 | 3.2.0 | 650.03 ms | 649.31 ms | 7.253 ms |
| 🏆 **TUnit (AOT)** | 1.0.30 | 45.00 ms | 45.18 ms | 3.810 ms |


---

## 🔨 Build Performance

Compilation time comparison across frameworks:

| Framework | Version | Mean | Median | StdDev |
|-----------|---------|------|--------|--------|
| 🏆 **TUnit** | 1.0.30 | 1.736 s | 1.741 s | 0.0254 s |
| Build_NUnit | 4.4.0 | 1.531 s | 1.529 s | 0.0091 s |
| Build_MSTest | 4.0.1 | 1.613 s | 1.606 s | 0.0136 s |
| Build_xUnit3 | 3.2.0 | 1.532 s | 1.534 s | 0.0098 s |


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
- **Runtime**: .NET 10.0.3 (10.0.3, 10.0.326.7603), X64 RyuJIT x86-64-v4
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

*Last generated: 2026-02-15T00:30:24.991Z*
