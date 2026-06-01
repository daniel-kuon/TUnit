---
title: Performance Benchmarks
description: Real-world performance comparisons between TUnit and other .NET testing frameworks
sidebar_position: 1
---

# Performance Benchmarks

:::info Last Updated
These benchmarks were automatically generated on **2026-06-01** from the latest CI run.

**Environment:** Ubuntu Latest • .NET SDK 10.0.300
:::

## 🎯 Executive Summary

TUnit demonstrates significant performance advantages across all testing scenarios:

<div className="benchmark-summary">

### Average Performance vs Other Frameworks

- **1.2x faster** than xUnit v3
- **1.1x faster** than NUnit
- **1.1x faster** than MSTest

</div>

---

## 🚀 Runtime Performance


### results

:::tip Native AOT Performance
TUnit with Native AOT compilation is **12.04x faster** than regular JIT!
:::

**Performance:** **1.16x faster** than xUnit • **1.15x faster** than NUnit • **1.07x faster** than MSTest

| Framework | Version | Mean | Median | StdDev |
|-----------|---------|------|--------|--------|
| 🏆 **TUnit** | 1.0.30 | 513.78 ms | 514.02 ms | 3.922 ms |
| NUnit | 4.4.0 | 592.76 ms | 592.86 ms | 10.967 ms |
| MSTest | 4.0.1 | 548.09 ms | 548.88 ms | 15.941 ms |
| xUnit3 | 3.2.0 | 598.08 ms | 595.68 ms | 9.750 ms |
| 🏆 **TUnit (AOT)** | 1.0.30 | 42.66 ms | 42.76 ms | 2.763 ms |


---

## 🔨 Build Performance

Compilation time comparison across frameworks:

| Framework | Version | Mean | Median | StdDev |
|-----------|---------|------|--------|--------|
| 🏆 **TUnit** | 1.0.30 | 1.653 s | 1.639 s | 0.0611 s |
| Build_NUnit | 4.4.0 | 1.525 s | 1.522 s | 0.0133 s |
| Build_MSTest | 4.0.1 | 1.578 s | 1.579 s | 0.0176 s |
| Build_xUnit3 | 3.2.0 | 1.521 s | 1.523 s | 0.0113 s |


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
- **Runtime**: .NET 10.0.8 (10.0.8, 10.0.826.23019), X64 RyuJIT x86-64-v3
- **SDK**: .NET SDK 10.0.300
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

*Last generated: 2026-06-01T00:54:23.827Z*
