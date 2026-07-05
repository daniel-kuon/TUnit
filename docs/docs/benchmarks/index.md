---
title: Performance Benchmarks
description: Real-world performance comparisons between TUnit and other .NET testing frameworks
sidebar_position: 1
---

# Performance Benchmarks

:::info Last Updated
These benchmarks were automatically generated on **2026-07-05** from the latest CI run.

**Environment:** Ubuntu Latest • .NET SDK 10.0.301
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
TUnit with Native AOT compilation is **4.27x faster** than regular JIT!
:::

**Performance:** **0.01x faster** than xUnit • **0.00x faster** than NUnit • **0.00x faster** than MSTest

| Framework | Version | Mean | Median | StdDev |
|-----------|---------|------|--------|--------|
| 🏆 **TUnit** | 1.0.30 | 586.6 ms | 585.6 ms | 5.70 ms |
| NUnit | 4.4.0 | 1,193.4 ms | 1,191.6 ms | 6.05 ms |
| MSTest | 4.0.1 | 2,976.9 ms | 2,976.1 ms | 5.97 ms |
| xUnit3 | 3.2.0 | 3,070.4 ms | 3,070.0 ms | 9.05 ms |
| 🏆 **TUnit (AOT)** | 1.0.30 | 137.5 ms | 137.4 ms | 1.45 ms |


---

## 🔨 Build Performance

Compilation time comparison across frameworks:

| Framework | Version | Mean | Median | StdDev |
|-----------|---------|------|--------|--------|
| 🏆 **TUnit** | 1.0.30 | 1.764 s | 1.750 s | 0.0571 s |
| Build_NUnit | 4.4.0 | 1.631 s | 1.633 s | 0.0125 s |
| Build_MSTest | 4.0.1 | 1.689 s | 1.690 s | 0.0131 s |
| Build_xUnit3 | 3.2.0 | 1.623 s | 1.623 s | 0.0169 s |


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
- **Runtime**: .NET 10.0.9 (10.0.9, 10.0.926.27113), X64 RyuJIT x86-64-v3
- **SDK**: .NET SDK 10.0.301
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

*Last generated: 2026-07-05T02:50:13.752Z*
