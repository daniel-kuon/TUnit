---
title: Performance Benchmarks
description: Real-world performance comparisons between TUnit and other .NET testing frameworks
sidebar_position: 1
---

# Performance Benchmarks

:::info Last Updated
These benchmarks were automatically generated on **2026-05-07** from the latest CI run.

**Environment:** Ubuntu Latest • .NET SDK 10.0.203
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
TUnit with Native AOT compilation is **6.57x faster** than regular JIT!
:::

**Performance:** **0.00x faster** than xUnit • **0.00x faster** than NUnit • **0.00x faster** than MSTest

| Framework | Version | Mean | Median | StdDev |
|-----------|---------|------|--------|--------|
| 🏆 **TUnit** | 1.0.30 | 522.23 ms | 523.55 ms | 5.923 ms |
| NUnit | 4.4.0 | 1,550.28 ms | 1,554.11 ms | 9.570 ms |
| MSTest | 4.0.1 | 1,502.19 ms | 1,499.41 ms | 7.936 ms |
| xUnit3 | 3.2.0 | 1,594.39 ms | 1,590.16 ms | 10.600 ms |
| 🏆 **TUnit (AOT)** | 1.0.30 | 79.52 ms | 79.49 ms | 0.268 ms |


---

## 🔨 Build Performance

Compilation time comparison across frameworks:

| Framework | Version | Mean | Median | StdDev |
|-----------|---------|------|--------|--------|
| 🏆 **TUnit** | 1.0.30 | 1.822 s | 1.825 s | 0.0229 s |
| Build_NUnit | 4.4.0 | 1.566 s | 1.567 s | 0.0094 s |
| Build_MSTest | 4.0.1 | 1.654 s | 1.651 s | 0.0307 s |
| Build_xUnit3 | 3.2.0 | 1.559 s | 1.555 s | 0.0124 s |


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
- **Runtime**: .NET 10.0.7 (10.0.7, 10.0.726.21808), X64 RyuJIT x86-64-v4
- **SDK**: .NET SDK 10.0.203
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

*Last generated: 2026-05-07T00:43:04.256Z*
