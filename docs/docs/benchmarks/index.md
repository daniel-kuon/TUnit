---
title: Performance Benchmarks
description: Real-world performance comparisons between TUnit and other .NET testing frameworks
sidebar_position: 1
---

# Performance Benchmarks

:::info Last Updated
These benchmarks were automatically generated on **2026-05-01** from the latest CI run.

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
TUnit with Native AOT compilation is **7.05x faster** than regular JIT!
:::

**Performance:** **0.00x faster** than xUnit • **0.00x faster** than NUnit • **0.00x faster** than MSTest

| Framework | Version | Mean | Median | StdDev |
|-----------|---------|------|--------|--------|
| 🏆 **TUnit** | 1.0.30 | 561.07 ms | 560.84 ms | 6.688 ms |
| NUnit | 4.4.0 | 1,576.97 ms | 1,577.65 ms | 5.175 ms |
| MSTest | 4.0.1 | 1,533.09 ms | 1,531.03 ms | 8.690 ms |
| xUnit3 | 3.2.0 | 1,630.91 ms | 1,630.89 ms | 5.108 ms |
| 🏆 **TUnit (AOT)** | 1.0.30 | 79.63 ms | 79.72 ms | 0.359 ms |


---

## 🔨 Build Performance

Compilation time comparison across frameworks:

| Framework | Version | Mean | Median | StdDev |
|-----------|---------|------|--------|--------|
| 🏆 **TUnit** | 1.0.30 | 1.861 s | 1.865 s | 0.0283 s |
| Build_NUnit | 4.4.0 | 1.668 s | 1.668 s | 0.0167 s |
| Build_MSTest | 4.0.1 | 1.730 s | 1.729 s | 0.0211 s |
| Build_xUnit3 | 3.2.0 | 1.652 s | 1.648 s | 0.0221 s |


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
- **Runtime**: .NET 10.0.7 (10.0.7, 10.0.726.21808), X64 RyuJIT x86-64-v3
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

*Last generated: 2026-05-01T00:45:38.109Z*
