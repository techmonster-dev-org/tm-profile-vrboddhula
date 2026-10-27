# AI-Chip & ML-Systems Engineering (GPU Kernels to Compilers) — Full Track Record

**vrboddhula** · [← Back to profile](../README.md) · Updated 2026-10-27

## Progress

[░░░░░░░░░░░░░░░░░░░░] 0%   (0 of 48 projects completed)

## Deep Learning for Systems Engineers

| Project | Score | Understanding | Reviewed | Feedback |
|---|---|---|---|---|
| Implement scaled dot-product and multi-head attention from scratch in NumPy and PyTorch, apply causal masking, quantify the O(S²) memory cost, and compare standard attention to F.scaled_dot_product_attention. | ⬜ Not started | — | — | — |
| Build a decoder-only mini transformer, profile its forward pass with the PyTorch profiler, compute MFU, classify the top bottlenecks using the roofline model, and produce a written optimization agenda for Phase 2. | ⬜ Not started | — | — | — |
| Explore fp32/fp16/bf16/int8 numeric formats, implement symmetric int8 quantization, benchmark GEMM throughput across dtypes on GPU, and implement a mixed-precision forward pass with torch.autocast. | ⬜ Not started | — | — | — |
| Implement matrix multiply from scratch, count FLOPs using the 2×M×N×K formula, measure GPU GEMM throughput, and identify which transformer layers dominate the FLOPs budget. | ⬜ Not started | ⚠️ Unverified | 2026-10-27 | [→](https://github.com/techmonster-dev-org/tm-student-vrboddhula-ai-chip-ml-systems/issues/2) |
| Build a roofline calculator, compute arithmetic intensity for every major ML op, classify each as compute-bound or memory-bound, and produce a per-op optimization agenda for a full transformer layer. | ⬜ Not started | — | — | — |
| Explore tensors as N-dimensional arrays with shape, strides, and dtype; understand row-major layout, contiguity, and broadcasting, and connect each concept to its GPU memory-access implication. | ⬜ Not started | ❌ Failed | 2026-10-27 | [→](https://github.com/techmonster-dev-org/tm-student-vrboddhula-ai-chip-ml-systems/issues/1) |
| Implement a full transformer encoder layer from scratch in PyTorch, produce a per-component FLOPs breakdown, compute weight and activation memory, and map every sub-block to its kernel type (GEMM vs elementwise). | ⬜ Not started | — | — | — |
| Implement a 3-layer MLP forward pass in NumPy, instrument it with FLOPs and bytes-per-layer counts, classify each op as compute-bound or memory-bound, and verify against PyTorch's nn.Sequential. | ⬜ Not started | ⚠️ Unverified | 2026-10-27 | [→](https://github.com/techmonster-dev-org/tm-student-vrboddhula-ai-chip-ml-systems/issues/3) |

## GPU Kernel Engineering for ML

| Project | Score | Understanding | Reviewed | Feedback |
|---|---|---|---|---|
| Write a minimal Tensor Core GEMM using nvcuda::wmma (FP16 inputs, FP32 accumulate), measure the TFLOP/s multiple over FP32 CUDA cores, and compare to cuBLAS HGEMM to understand what the remaining gap requires. | ⬜ Not started | — | — | — |
| Implement a numerically stable, block-parallel softmax kernel using shared memory tree reduction and warp shuffles, benchmark it in GB/s, and validate output against a CPU reference to understand the reduction pattern that underlies FlashAttention. | ⬜ Not started | — | — | — |
| Count FLOPs for real transformer layers, implement a tiled GEMM kernel benchmarked in GFLOP/s vs the GPU peak, and compare against cuBLAS to understand what register tiling, double-buffering, and tensor cores contribute. | ⬜ Not started | — | — | — |
| Write ReLU, GELU, sigmoid, add, and scale kernels using grid-stride loops and float4 vectorization, then benchmark each in GB/s against the GPU's peak memory bandwidth to confirm they are bandwidth-limited. | ⬜ Not started | — | — | — |
| Assemble optimized ReLU, GELU, softmax, LayerNorm, RMSNorm, and tiled GEMM kernels into a structured CUDA library with a clean C++ header interface, a correctness test suite against CPU references, and a benchmark table reporting each kernel's % of theoretical peak bandwidth or compute. | ⬜ Not started | — | — | — |
| Compute arithmetic intensities for all Phase 2 kernels, place them on the GPU roofline model, run Nsight Compute on at least one kernel, and produce an optimization priority matrix based on each kernel's distance from its theoretical ceiling. | ⬜ Not started | — | — | — |
| Apply coalescing fixes, shared memory staging, float4/half2 vectorized loads, and occupancy tuning to ML kernels, measuring the bandwidth improvement from each technique and assembling them into an optimized LayerNorm. | ⬜ Not started | — | — | — |
| Implement LayerNorm using two-pass (mean then variance), Welford one-pass, and fused affine variants, plus RMSNorm, measuring bandwidth improvement across implementations and validating correctness with identity affine parameters. | ⬜ Not started | — | — | — |

## Kernel Fusion & FlashAttention

| Project | Score | Understanding | Reviewed | Feedback |
|---|---|---|---|---|
| Benchmark fused vs naive attention across sequence lengths 512–8192, measure O(N) vs O(N²) HBM scaling empirically, profile with Nsight Compute, and produce a capstone results table. | ⬜ Not started | — | — | — |
| Implement a working tiled fused single-head attention CUDA kernel using shared memory tiles and the online softmax recurrence, verify against naive attention, and measure peak memory and latency. | ⬜ Not started | — | — | — |
| Measure the HBM round-trip penalty of an unfused 3-kernel pipeline vs a fused kernel and explain the memory wall that kernel fusion addresses. | ⬜ Not started | — | — | — |
| Derive and implement the running-max / running-sum rescaling trick that computes numerically stable softmax over blocks without seeing all elements first — the mathematical core of FlashAttention. | ⬜ Not started | — | — | — |
| Fuse LayerNorm's two-pass reduction+normalization into a single kernel using shared memory, eliminating one full HBM read of the input tensor. | ⬜ Not started | — | — | — |
| Implement 3-kernel naive attention (QK^T → softmax → V), measure the O(N²) score-matrix memory footprint, and observe the GPU OOM boundary that motivates FlashAttention. | ⬜ Not started | — | — | — |
| Fuse bias-add + GELU + scale into a single CUDA kernel, eliminate intermediate HBM round-trips, and measure the bandwidth and latency win on transformer FFN-scale tensors. | ⬜ Not started | — | — | — |
| Study and implement the IO-aware FlashAttention algorithm: tile Q/K/V to fit in SRAM, use online softmax running stats, and accumulate output without ever materializing the N×N score matrix. | ⬜ Not started | — | — | — |

## Triton — GPU Programming in Python

| Project | Score | Understanding | Reviewed | Feedback |
|---|---|---|---|---|
| Add @triton.autotune with a 12-config search space (BM/BN/BK × num_warps × num_stages) to the matmul kernel, observe the autotuner's first-call search and cache behavior, inspect the winning config, and measure 20–50% TFLOP/s improvement over the fixed-config baseline. | ⬜ Not started | — | — | — |
| Implement a FlashAttention-style single-headed forward attention kernel in Triton: tiled Q/K/V loads, online softmax update (running max + running sum rescaling), running output accumulator; verify against a reference torch implementation and benchmark against naive three-op PyTorch and F.scaled_dot_product_attention. | ⬜ Not started | — | — | — |
| Understand the motivation for Triton (the CUDA productivity wall), the block-level programming model, and set up a working Triton environment on Colab; run a minimal @triton.jit kernel that introduces program_id, tl.arange, tl.load, tl.store, and the launch grid. | ⬜ Not started | — | — | — |
| Implement a tiled float32 GEMM in Triton: 2D program grid with pid_m/pid_n, tl.dot for tile MAC, accumulator register tile, pointer arithmetic with 2D masking; verify against torch.matmul and benchmark TFLOP/s toward cuBLAS-class throughput. | ⬜ Not started | — | — | — |
| Implement a row-wise numerically stable softmax kernel in Triton (one program per row, in-kernel tl.max and tl.sum reductions, BLOCK_SIZE = next_power_of_2(n_cols)), verify against torch.softmax, and benchmark to demonstrate 2.5–3x speedup over naive unfused PyTorch. | ⬜ Not started | — | — | — |
| Implement element-wise vector addition in Triton end-to-end: write the @triton.jit kernel with tl.program_id / tl.arange / tl.load / tl.store / mask, write the Python driver, verify against PyTorch for both power-of-2 and non-power-of-2 sizes, and benchmark bandwidth against torch.add. | ⬜ Not started | — | — | — |
| Implement and autotune a fused LayerNorm forward kernel in Triton (one program per row, tl.sum for mean and variance, in-register normalization and affine transform), verify against torch.layer_norm, and produce a three-way benchmark table comparing Triton vs torch.layer_norm vs naive 4-op PyTorch. | ⬜ Not started | — | — | — |
| Conduct a structured productivity and performance comparison between Triton and CUDA across four implemented algorithms, analyze Triton's expressibility limits, observe Inductor-generated Triton via torch.compile, and articulate a personal decision framework for when each tool is appropriate. | ⬜ Not started | — | — | — |

## ML Compilers — MLIR, TVM & Graph Optimization

| Project | Score | Understanding | Reviewed | Feedback |
|---|---|---|---|---|
| Analyze the automation trajectory from hand-written CUDA to compiler-generated kernels, map the skills required at the largest AI and platform companies roles to your current capabilities, and produce a concrete 6-month roadmap toward a role at the compiler/architecture layer. | ⬜ Not started | — | — | — |
| Trace a PyTorch model to a torch.fx graph and inspect every node, edge, and data-flow dependency — learning why the graph representation is the foundation that makes all ML compiler optimization possible. | ⬜ Not started | — | — | — |
| Take a transformer block (self-attention + FFN), run it eager vs torch.compile vs max-autotune, capture the generated Triton kernels, identify every fusion decision, quantify memory bandwidth savings, and produce a complete compiler analysis report — a portfolio-quality artifact demonstrating Phase 5 mastery. | ⬜ Not started | — | — | — |
| Compile a transformer FFN block with torch.compile, measure the eager-vs-compiled speedup, inspect the generated Triton kernel via TORCH_LOGS, and diagnose and fix a graph break — learning the full torch.compile production workflow. | ⬜ Not started | — | — | — |
| Implement Dead-Code Elimination, Common-Subexpression Elimination, and constant folding as torch.fx graph passes, then demonstrate operator fusion — reducing a 7-node raw graph to 4 nodes while preserving exact semantics. | ⬜ Not started | — | — | — |
| Define a fused ReLU+scale operation as a Tensor Expression, write naive and optimized schedules (fused + vectorized + parallel), measure the speedup, and understand how TVM's Ansor auto-scheduler searches the schedule space to target any hardware from one model description. | ⬜ Not started | — | — | — |
| Learn MLIR's dialect system and progressive lowering by tracing a matrix multiply from the high-level linalg dialect through affine loops, GPU launch ops, and NVVM down to PTX — understanding why every serious ML compiler (Triton, IREE, XLA) is built on this infrastructure. | ⬜ Not started | — | — | — |
| Trace the complete lowering pipeline from a PyTorch matmul and softmax through TorchInductor's Triton codegen, illustrative PTX, and down to GPU SASS — understanding what performance decisions are made at each lowering stage and why tiling is the central one. | ⬜ Not started | — | — | — |

## Inference Optimization & the Fused-Attention Capstone

| Project | Score | Understanding | Reviewed | Feedback |
|---|---|---|---|---|
| Implement multi-head attention with and without KV-cache in PyTorch, verify numerical equivalence, and compute the memory footprint of the cache for production LLMs to understand why PagedAttention was necessary. | ⬜ Not started | — | — | — |
| Quantify the memory, compute, and bandwidth constraints that make inference a distinct engineering discipline from training, measuring TTFT and TPOT on a small decoder-only transformer and deriving why decode is memory-bandwidth-bound. | ⬜ Not started | — | — | — |
| Simulate static vs continuous batching schedulers, derive the arithmetic intensity vs batch size curve, measure real throughput scaling on a small decoder-only transformer, and build a capacity planning tool showing the compounding benefit of quantization plus continuous batching. | ⬜ Not started | — | — | — |
| Implement INT8 and INT4 group quantization from scratch, measure quantization error vs FP16 reference, compute the bandwidth win during memory-bound decode, and understand GPTQ and AWQ's activation-aware strategies. | ⬜ Not started | — | — | — |
| Profile naive PyTorch inference to identify kernel launch and memory overhead, apply torch.compile to fuse operators, compare TensorRT-LLM, vLLM, llama.cpp, and ONNX Runtime, and build a decision framework for choosing the right engine. | ⬜ Not started | — | — | — |
| Apply the full inference optimization stack (FP16, torch.compile, INT8 quantization, KV-cache, batching) to a small decoder-only transformer-scale transformer and produce a complete optimization ladder table measuring TTFT, TPOT, throughput, and memory at each stage. | ⬜ Not started | — | — | — |
| Map the AI-chip ecosystem (NVIDIA, AMD, a hyperscaler TPU, a deterministic-dataflow chip startup, a wafer-scale chip startup, a RISC-V dataflow chip startup, a reconfigurable-dataflow chip startup), understand the CUDA→Triton→MLIR skill ladder, identify related roles and the skills each one asks for, and build a 90-day learning plan. | ⬜ Not started | — | — | — |
| Implement scaled-dot-product attention in CUDA (naive baseline), then a FlashAttention-style fused tiled kernel using the online softmax algorithm that never materializes the N×N score matrix. Implement a Triton version as the second implementation. Verify numerical correctness against PyTorch's F.scaled_dot_product_attention. Benchmark latency and peak GPU memory across sequence lengths (512–4096) against the naive baseline and PyTorch SDPA. Explain the speedup and memory savings in memory-traffic terms. Package with reproducible setup, correctness test, and a WRITEUP.md with two key tradeoffs. | ⬜ Not started | — | — | — |

---
*Machine-readable proof with commit SHA anchors: [verified-record.json](./verified-record.json)*