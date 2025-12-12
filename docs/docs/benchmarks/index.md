---
title: Performance Benchmarks
description: Real-world performance comparisons between TUnit and other .NET testing frameworks
sidebar_position: 1
---

# Performance Benchmarks

:::info Last Updated
These benchmarks were automatically generated on **2025-12-12** from the latest CI run.

**Environment:** Ubuntu Latest • .NET SDK 10.0.101
:::

## 🎯 Executive Summary

TUnit demonstrates significant performance advantages across all testing scenarios:

<div className="benchmark-summary">

### Average Performance vs Other Frameworks

- **1.2x faster** than xUnit v3
- **1.1x faster** than NUnit
- **1.0x faster** than MSTest

</div>

---

## 🚀 Runtime Performance


### results

:::tip Native AOT Performance
TUnit with Native AOT compilation is **19.31x faster** than regular JIT!
:::

**Performance:** **1.21x faster** than xUnit • **1.11x faster** than NUnit • **1.01x faster** than MSTest

| Framework | Version | Mean | Median | StdDev |
|-----------|---------|------|--------|--------|
| 🏆 **TUnit** | 1.0.30 | 476.16 ms | 477.00 ms | 3.834 ms |
| NUnit | 4.4.0 | 528.53 ms | 528.27 ms | 6.243 ms |
| MSTest | 4.0.1 | 483.06 ms | 481.48 ms | 9.443 ms |
| xUnit3 | 3.2.0 | 575.60 ms | 575.63 ms | 5.530 ms |
| 🏆 **TUnit (AOT)** | 1.0.30 | 24.66 ms | 24.64 ms | 0.164 ms |


---

## 🔨 Build Performance

Compilation time comparison across frameworks:

| Framework | Version | Mean | Median | StdDev |
|-----------|---------|------|--------|--------|
| 🏆 **TUnit** | 1.0.30 | 1.713 s | 1.696 s | 0.0346 s |
| Build_NUnit | 4.4.0 | 1.502 s | 1.505 s | 0.0172 s |
| Build_MSTest | 4.0.1 | 1.566 s | 1.567 s | 0.0099 s |
| Build_xUnit3 | 3.2.0 | 1.455 s | 1.455 s | 0.0160 s |


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
- **Runtime**: .NET 10.0.1 (10.0.1, 10.0.125.57005), X64 RyuJIT x86-64-v3
- **SDK**: .NET SDK 10.0.101
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

*Last generated: 2025-12-12T00:24:08.420Z*
