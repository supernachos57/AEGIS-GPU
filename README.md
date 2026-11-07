# AEGIS — AI Execution & GPU Investigation Simulator

AEGIS is an independent GPU performance engineering and architecture research project that connects real machine-learning workload measurements with simplified GPU architecture modeling.

## Components

**A — Real GPU Performance Lab:** Implement, validate, benchmark, and optimize ML-oriented kernels using C++ and AMD HIP, starting with general matrix multiplication (GEMM) on an AMD Radeon RX 7800 XT. Study throughput, memory traffic, and execution bottlenecks.

**B — GPU Architecture Simulator:** Build a simplified C++ model of GPU execution, including compute units, wavefront scheduling, occupancy, registers, memory latency, and bandwidth. Compare simulated trends against real measurements and explore hypothetical architectures. This is not intended as a cycle-accurate model of proprietary hardware.

## Roadmap

The nine-phase plan is a starting estimate, not a fixed deadline.

| Phase | Scope | Hours |
| --- | --- | ---: |
| 0 | Repository, tooling, and documentation | 8–12 |
| 1 | GEMM baseline and correctness | 15–25 |
| 2 | Benchmark infrastructure and measurements | 20–30 |
| 3 | GEMM optimization and bottleneck analysis | 30–45 |
| 4 | Additional ML workloads | 35–55 |
| 5 | Simulator foundations | 35–55 |
| 6 | Scheduling, occupancy, and memory models | 45–70 |
| 7 | Simulator validation against measurements | 30–50 |
| 8 | Architectural experiments and final report | 20–35 |
| **Total** | | **238–377** |

For phase objectives, deliverables, dependencies, acceptance criteria, scheduling estimates, and Mermaid diagrams, see the **[detailed development roadmap](docs/roadmap.md)**.

## Engineering methodology

- Validate correctness against reference results and edge cases before optimizing.
- Record hardware, software versions, workloads, timing methodology, and repeated benchmark measurements.
- Distinguish measurements from hypotheses and simulator assumptions.
- Document design choices, alternatives, tradeoffs, and limitations.
- Close phases based on verified deliverables rather than hours elapsed.

## First GEMM design direction

The initial HIP GEMM baseline will use one thread per output element, a 2D thread layout, 16×16 threads per workgroup, and row-major indexing. This is a correctness-first baseline, not an optimized kernel.

## Current status

**Phase 0 — Project initialization.** Kernels, benchmarks, and simulator code have not yet been implemented.

AEGIS is independently directed; engineering decisions and conclusions will be recorded as the project develops.
