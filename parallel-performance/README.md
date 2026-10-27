# Parallel Computing & Performance (CPU to GPU) — Full Track Record

**vrboddhula** · [← Back to profile](../README.md) · Updated 2026-10-27

## Progress

[░░░░░░░░░░░░░░░░░░░░] 0%   (0 of 48 projects completed)

## Foundations of Parallelism

| Project | Score | Understanding | Reviewed | Feedback |
|---|---|---|---|---|
| Build a professional scaling study: measure parallel dot product and Mandelbrot speedup from 1 to N threads, compute parallel efficiency at each point, isolate four overhead sources with micro-benchmarks, and diagnose bottleneck type from the efficiency curve shape. | ⬜ Not started | — | — | — |
| Build five targeted overhead micro-experiments — thread creation, uncontended vs contended mutex, false sharing, and memory bandwidth saturation — then combine all overhead sources into a deliberately bad parallel design that is measurably slower than serial with every thread count. | ⬜ Not started | — | — | — |
| Implement data parallelism (image blur split across rows) and task parallelism (3-stage producer-consumer pipeline) for the same processing workload, measure their performance profiles, demonstrate Monte Carlo as an embarrassingly parallel benchmark, and build a decision framework for choosing the right decomposition. | ⬜ Not started | — | — | — |
| Complete a professional parallel scaling study: parallelize a 2D Gaussian convolution with correct decomposition, false-sharing avoidance, and median timing; run from 1 to N threads; compute speedup and efficiency; fit Amdahl's Law to the data; and write a structured performance report with bottleneck identification in journal/. | ⬜ Not started | — | — | — |
| Apply block, cyclic, and dynamic partitioning strategies to an irregular workload, measure load imbalance for each, then run a 2D domain decomposition experiment demonstrating how row-major vs column-major partition alignment affects cache performance by more than 3×. | ⬜ Not started | — | — | — |
| Build and time programs that demonstrate the concrete difference between concurrency (interleaving on one thread) and parallelism (simultaneous execution on multiple cores), then survey the three hardware parallelism levels — multi-core, SIMD, and GPU. | ⬜ Not started | ⚠️ Unverified | 2026-10-27 | [→](https://github.com/techmonster-dev-org/tm-student-vrboddhula-parallel-performance/issues/1) |
| Implement Gustafson's Law formula alongside Amdahl's, run a weak scaling experiment where problem size grows proportionally with thread count, measure weak scaling efficiency, and decide which scaling model applies to real-world system designs. | ⬜ Not started | ⚠️ Unverified | 2026-10-27 | [→](https://github.com/techmonster-dev-org/tm-student-vrboddhula-parallel-performance/issues/3) |
| Implement Amdahl's Law formula, tabulate predicted speedup curves for serial fractions 1–50%, parallelize a prefix-sum workload, measure its scaling from 1–8 threads, and fit the formula to recover the program's empirical serial fraction. | ⬜ Not started | ❌ Failed | 2026-10-27 | [→](https://github.com/techmonster-dev-org/tm-student-vrboddhula-parallel-performance/issues/2) |

## CPU Parallelism at Scale

| Project | Score | Understanding | Reviewed | Feedback |
|---|---|---|---|---|
| Contrast static vs dynamic scheduling on imbalanced tasks using an atomic counter, measure the speedup from dynamic dispatch, and study the per-thread-deque work-stealing design used by TBB and Rayon. | ⬜ Not started | — | — | — |
| Implement a ThreadPool class with a mutex-protected task queue, std::packaged_task for future-returning submit(), and graceful shutdown — then benchmark it against per-task thread creation. | ⬜ Not started | — | — | — |
| Measure false sharing on parallel histogram counters, fix it with alignas(64) padding, then implement per-thread aggregation to achieve 40x speedup over shared atomics — the universal high-throughput parallel counting pattern. | ⬜ Not started | — | — | — |
| Implement and benchmark the five core parallel skeletons — map, reduce, map-reduce (word count), pipeline (bounded queue), and fork-join (recursive async) — and learn to match each pattern to the right problem. | ⬜ Not started | — | — | — |
| Split a 500 M-element reduction loop across std::thread workers, combine partial results, and measure speedup vs thread count — the manual baseline before higher-level abstractions. | ⬜ Not started | — | — | — |
| Apply std::execution::par and par_unseq to for_each, transform, reduce, and sort; measure par vs seq speedup across data sizes; understand the TBB backend requirement and floating-point non-determinism of parallel reduce. | ⬜ Not started | — | — | — |
| Implement tree reduction with per-thread partial sums, demonstrate why shared-atomic accumulation serializes cores, use std::reduce with its associativity caveat, and implement parallel prefix-sum scan. | ⬜ Not started | — | — | — |
| Apply thread pool dispatch, per-thread unordered_map aggregation, and parallel-STL sort to a 64-document word-count corpus; run a full scaling study from 1 to 8 threads reporting speedup and parallel efficiency. | ⬜ Not started | — | — | — |

## SIMD & Data Parallelism

| Project | Score | Understanding | Reviewed | Feedback |
|---|---|---|---|---|
| Explore the SIMD execution model by probing CPU vector ISA support, measuring scalar vs AVX2 array-add throughput, and understanding register widths across the SSE/AVX/AVX-512 family. | ⬜ Not started | — | — | — |
| Vectorize a batched L2 normalization kernel using the full SIMD toolkit — auto-vectorization, manual AVX2+FMA with 4-accumulator reduction, and OpenMP multithreading — then produce a speedup breakdown table and efficiency analysis vs theoretical peak. | ⬜ Not started | — | — | — |
| Write loops the compiler can auto-vectorize, read -fopt-info-vec reports, and systematically remove vectorization blockers including aliasing, loop-carried dependencies, and non-unit stride access. | ⬜ Not started | — | — | — |
| Benchmark a particle physics update in Array-of-Structs vs Struct-of-Arrays layout, measure the SIMD throughput difference, and learn to use alignas(32) and std::aligned_alloc correctly. | ⬜ Not started | — | — | — |
| Implement vectorized array sum and dot product using multi-lane FMA accumulators and a hadd/extractf128 horizontal reduction, measuring throughput and examining the floating-point associativity implications. | ⬜ Not started | — | — | — |
| Implement a complete RGB-to-grayscale + threshold image processing pipeline in scalar and AVX2, measure end-to-end speedup, and evaluate the portability tradeoff between raw intrinsics and cross-platform SIMD libraries. | ⬜ Not started | — | — | — |
| Replace per-lane conditional branches with compare-and-blendv patterns to implement threshold filtering and ReLU activation using AVX2, measuring throughput and understanding the GPU warp divergence analogy. | ⬜ Not started | — | — | — |
| Hand-write a SAXPY kernel using __m256, _mm256_loadu_ps, and _mm256_fmadd_ps, then compare its throughput against scalar and auto-vectorized versions to understand when intrinsics add value. | ⬜ Not started | — | — | — |

## GPU Programming I — CUDA Fundamentals

| Project | Score | Understanding | Reviewed | Feedback |
|---|---|---|---|---|
| Benchmark and compare pageable host memory, pinned (page-locked) host memory, and Unified Memory for GPU data transfer, quantifying bandwidth differences and learning when each approach is appropriate. | ⬜ Not started | — | — | — |
| Set up a CUDA environment and write your first device kernel, learning the CPU-vs-GPU design tradeoff, the SIMT execution model, warps, and the Streaming Multiprocessor hierarchy. | ⬜ Not started | — | — | — |
| Map 2D problems (images, matrices) to 2D CUDA grids using dim3, apply boundary checks for non-multiple dimensions, study how block size affects occupancy, and use a 2D grid-stride loop for arbitrary-size problems. | ⬜ Not started | — | — | — |
| Implement GPU vector addition end-to-end: cudaMalloc, H2D copy, a __global__ kernel using the global index formula, D2H copy, verification, and a grid-stride loop for arbitrary array sizes. | ⬜ Not started | — | — | — |
| Write a complete 2D box-blur image filter and a matrix transpose kernel, applying dim3 2D launches, clamped boundary handling, CUDA_CHECK error checking, and cudaEvent timing — and observe why naive transpose is bandwidth-limited by strided writes. | ⬜ Not started | — | — | — |
| Measure the cost of intra-warp branch divergence, write branchless alternatives using CUDA math intrinsics, and restructure a reduction kernel to be warp-uniform — learning the pattern that prevents the most common GPU performance pitfall. | ⬜ Not started | — | — | — |
| Write a CUDA_CHECK macro for robust error handling, demonstrate why CPU-side timing is wrong for asynchronous kernels, and build a correct cudaEvent_t timing harness — the professional foundation for all future kernel benchmarking. | ⬜ Not started | — | — | — |
| Build a complete GPU image processing pipeline (5x5 Gaussian blur + Sobel edge detection) integrating pinned memory, __constant__ memory, CUDA_CHECK error handling, GPU event timing, and a CPU-vs-GPU speedup comparison — the phase capstone. | ⬜ Not started | — | — | — |

## GPU Programming II — Performance

| Project | Score | Understanding | Reviewed | Feedback |
|---|---|---|---|---|
| Use Nsight Compute to profile naive and tiled GEMM kernels, read the key metrics (SM throughput, stall reasons, memory bandwidth %, occupancy), and follow the optimize-measure loop to connect profiler output to code fixes. | ⬜ Not started | — | — | — |
| Apply the complete Phase 5 optimization stack (coalescing, shared memory staging, bank conflict padding, occupancy tuning) to a matrix transpose kernel, measuring bandwidth and profiling with Nsight at each step from 8% to 83%+ of peak. | ⬜ Not started | — | — | — |
| Measure the performance penalty of 32-way shared memory bank conflicts in a matrix transpose, then eliminate them with +1 padding and verify the speedup and bank assignment analytically. | ⬜ Not started | — | — | — |
| Implement the canonical tiled GEMM kernel using shared memory to reduce global memory traffic by a factor of TILE and measure the resulting GFLOP/s speedup over the naive kernel. | ⬜ Not started | — | — | — |
| Benchmark coalesced vs strided global memory access patterns to quantify the bandwidth penalty of uncoalesced loads and writes on a real GPU. | ⬜ Not started | — | — | — |
| Implement the staging pattern using __shared__ memory to build a latency microbenchmark and a 1D stencil kernel that reduces global memory traffic by exploiting data reuse. | ⬜ Not started | — | — | — |
| Measure how block size, register count, and shared memory allocation affect SM occupancy, then observe the relationship between occupancy and throughput for both memory-bound and compute-bound kernels. | ⬜ Not started | — | — | — |
| Implement the 5-step reduction optimization progression — from naive interleaved to warp-shuffle __shfl_down_sync — measuring the effective bandwidth at each step and explaining each bottleneck fixed. | ⬜ Not started | — | — | — |

## HPC, Heterogeneous Computing & the Capstone

| Project | Score | Understanding | Reviewed | Feedback |
|---|---|---|---|---|
| Use cudaMemcpyAsync and multiple CUDA streams to overlap PCIe data transfers with GPU kernel execution, measure the speedup from 2-stream and 4-stream pipelines, and understand multi-GPU dispatch with cudaSetDevice. | ⬜ Not started | — | — | — |
| Use OpenMP tasks for recursive parallelism, collapse(2) for nested loops, atomic/critical/reduction for shared state, and diagnose and fix false sharing between OpenMP threads. | ⬜ Not started | — | — | — |
| Measure local vs remote NUMA memory access bandwidth, fix NUMA-unaware allocation using first-touch initialization, and control thread/memory placement with numactl and OMP_PROC_BIND. | ⬜ Not started | — | — | — |
| Optimize dense matrix multiply through the full stack: naive → cache-blocked → OpenMP → AVX2 → OpenBLAS on CPU, and naive CUDA → shared-memory tiled → cuBLAS on GPU. Report GFLOP/s and % of peak at every stage; package with CMake + GoogleTest; explain every speedup with roofline reasoning and document two tradeoffs. | ⬜ Not started | — | — | — |
| Call cuBLAS sgemm to perform GEMM and compare GFLOP/s against a naive kernel and the theoretical peak; use Thrust device algorithms without writing kernels; and build a decision framework for library vs custom kernel. | ⬜ Not started | — | — | — |
| Apply the measure → roofline → bottleneck → fix → repeat optimization loop to a 2D convolution: use perf stat to identify cache bottlenecks, apply tiling and OpenMP, and report results honestly with GFLOP/s, % of peak, speedup, and machine context. | ⬜ Not started | — | — | — |
| Parallelize loops with #pragma omp parallel for, write correct parallel reductions, compare scheduling strategies, and benchmark OpenMP against parallel STL on a shared-memory machine. | ⬜ Not started | — | — | — |
| Measure PCIe transfer bandwidth, find the CPU vs GPU break-even problem size for elementwise ops, apply the roofline model to classify operations as bandwidth or compute bound, and build a decision framework. | ⬜ Not started | — | — | — |

---
*Machine-readable proof with commit SHA anchors: [verified-record.json](./verified-record.json)*