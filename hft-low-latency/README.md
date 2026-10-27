# HFT & Low-Latency Engineering in C++ — Full Track Record

**vrboddhula** · [← Back to profile](../README.md) · Updated 2026-10-27

## Progress

[░░░░░░░░░░░░░░░░░░░░] 0%   (0 of 48 projects completed)

## The Low-Latency Mindset & Measurement

| Project | Score | Understanding | Reviewed | Feedback |
|---|---|---|---|---|
| Measure and memorize nanosecond costs for L1/L2/L3/DRAM accesses, branch mispredictions, atomic RMWs, syscalls, and malloc, then apply the model to estimate hot-path latency by inspection before benchmarking. | ⬜ Not started | — | — | — |
| Learn to defeat the optimizer with DoNotOptimize/escape idioms, apply warm-up and multi-run discipline, use Google Benchmark, and recognize five common ways a microbenchmark can lie. | ⬜ Not started | — | — | — |
| Measure nondeterminism in a tight loop, attribute outliers to page faults, C-states, TLB shootdowns, and scheduler preemptions, and apply mitigations to reduce tail latency on Linux. | ⬜ Not started | — | — | — |
| Build latency/throughput measurement programs, model the tick-to-trade pipeline, and understand the economic rationale that drives HFT firms to spend millions optimizing nanoseconds. | ⬜ Not started | — | — | — |
| Build a program with four known latency-spike sources, then use perf stat/record, flamegraphs, perf c2c (false sharing), and off-CPU analysis to attribute each spike and practice the production tail-latency profiling workflow. | ⬜ Not started | — | — | — |
| Build a fixed-bucket logarithmic latency histogram, compute p50/p99/p99.9 from 1M samples, visualize distribution shapes, and understand coordinated omission — the most common latency benchmarking mistake. | ⬜ Not started | ⚠️ Unverified | 2026-10-27 | [→](https://github.com/techmonster-dev-org/tm-student-vrboddhula-hft-low-latency/issues/2) |
| Implement RDTSC/RDTSCP wrappers, calibrate TSC cycles to nanoseconds, compare clock sources by overhead, and build a reusable timing_utils.hpp header used throughout the track. | ⬜ Not started | ⚠️ Unverified | 2026-10-27 | [→](https://github.com/techmonster-dev-org/tm-student-vrboddhula-hft-low-latency/issues/1) |
| Build latency_harness.hpp — a 200-line single-header library combining RDTSC timing, TSC calibration, logarithmic histogram, timer-overhead subtraction, and a multi-run BenchmarkRunner — and validate it with a 7-test self-test suite. | ⬜ Not started | — | — | — |

## Mechanical Sympathy: C++ for Speed

| Project | Score | Understanding | Reviewed | Feedback |
|---|---|---|---|---|
| Identify the common-case hot path in a market-data handler, separate it from cold-path error handling and logging using __builtin_expect and [[gnu::cold]], and measure the latency improvement with an rdtsc timer. | ⬜ Not started | — | — | — |
| Implement a quote classifier four ways — branchy, sorted-input, branchless arithmetic, and lookup table — and measure the branch-misprediction cost on random vs structured input using an rdtsc timer. | ⬜ Not started | — | — | — |
| Apply all Phase 2 techniques sequentially to a deliberately slow message handler (v0 through v7), measuring p50/p99 latency after each change and documenting the transformation log — targeting at least 20x improvement at p50 and 50x at p99. | ⬜ Not started | — | — | — |
| Redesign an instrument table from fat AoS to SoA and hot/cold split layouts, measure the cache-line-fetch reduction and scan throughput improvement for 4096 instruments, and explain the result in terms of bytes-useful-per-cache-line. | ⬜ Not started | — | — | — |
| Benchmark four call-dispatch mechanisms (virtual, function pointer, std::function, CRTP) on a per-order risk check, measure the latency gap between indirect and inlined calls, and implement a CRTP-based static dispatcher that matches plain-inline performance. | ⬜ Not started | — | — | — |
| Measure the latency of exceptions (thrown vs not-thrown), RTTI dynamic_cast, accidental struct copies, and std::shared_ptr atomic refcounting; produce a documented hot-path ban list with measured cost justification for each item. | ⬜ Not started | — | — | — |
| Build a free-list object pool and an arena bump allocator for Order objects, use std::pmr::monotonic_buffer_resource with pmr::vector, and measure the p50/p99/p99.9 latency improvement over raw new/delete. | ⬜ Not started | — | — | — |
| Identify and remove heap allocations (new/delete, std::string concat, unreserved std::vector) from a market-data serializer's hot path, replacing them with a pre-allocated fixed stack buffer, and measure the p50/p99/p99.9 latency improvement. | ⬜ Not started | — | — | — |

## Lock-Free Concurrency for Trading

| Project | Score | Understanding | Reviewed | Feedback |
|---|---|---|---|---|
| Implement a templated Seqlock<T> with version counter and acquire/release orderings, verify zero torn reads over 480 M read operations, benchmark it against shared_mutex for a one-writer/many-reader workload, and analyze retry rate at different write frequencies. | ⬜ Not started | — | — | — |
| Assemble a complete 3-stage lock-free pipeline (producer → processor → publisher) connected by SPSC rings on pinned threads, push 10 million messages end-to-end, and measure p50/p99/p99.9 latency and throughput — the capstone of Phase 3 applying every technique from projects 1–7. | ⬜ Not started | — | — | — |
| Pin threads to dedicated CPU cores with pthread_setaffinity_np, measure p99 jitter for pinned vs unpinned threads under background load, demonstrate NUMA-local vs remote memory latency, and build a 3-stage pinned pipeline with measured per-stage handoff latency. | ⬜ Not started | — | — | — |
| Measure wakeup latency for busy-spin vs condition_variable, implement the _mm_pause() spin hint and exponential backoff, and build the decision framework for choosing spinning vs blocking per pipeline stage in an HFT system. | ⬜ Not started | — | — | — |
| Build a production-grade SPSC ring buffer with power-of-two masking, cache-line-separated head/tail, correct acquire/release orderings, and measured throughput exceeding 100 M msg/s — the workhorse of HFT inter-thread pipelines. | ⬜ Not started | — | — | — |
| Build a simplified but functionally complete LMAX Disruptor with pre-allocated ring buffer, monotonic sequence counter, single-writer producer, and multiple independent broadcast consumers — then benchmark it against a mutex queue to understand each source of performance gain. | ⬜ Not started | — | — | — |
| Demonstrate why two producers on an SPSC queue is an immediate data race, then build a Vyukov-style bounded MPSC queue using CAS on the tail, and benchmark it against SPSC sharding to understand when each design wins. | ⬜ Not started | — | — | — |
| Build a series of focused experiments mapping each std::memory_order to hardware instructions and costs, implementing the publish-data-then-release-flag pattern used between network and strategy threads in HFT pipelines. | ⬜ Not started | — | — | — |

## The Order Book & Matching Engine

| Project | Score | Understanding | Reviewed | Feedback |
|---|---|---|---|---|
| Assemble a complete price-time-priority matching engine integrating all Phase 4 components: fast array-indexed LOB, order pool, ID map, market data publisher, and correctness checks — then measure throughput (M msgs/sec) and per-message latency distribution (p50/p99/p99.9) and identify the dominant bottleneck. | ⬜ Not started | — | — | — |
| Implement the price-time priority matching loop: an aggressive order walks the opposite side from best price, fills FIFO within each level, generates paired fill records, and either rests or cancels the remainder — with correct handling of MARKET, LIMIT, IOC, and FOK semantics. | ⬜ Not started | — | — | — |
| Build the vocabulary of a matching engineer: bid/ask/spread/mid, price levels and depth, all four order types (LIMIT/MARKET/IOC/FOK), maker vs taker, the complete order lifecycle, and integer tick pricing — the foundation every later project depends on. | ⬜ Not started | — | — | — |
| Replace the std::map level index with a flat array indexed by price offset and the queue with an intrusive doubly-linked list, achieving O(1) add, O(1) cancel, and O(1) best-bid/ask tracking — then benchmark the 10x+ speedup over the map-based design. | ⬜ Not started | — | — | — |
| Build a correct two-sided limit order book using std::map and std::queue: implement add_order, cancel_order, and best-bid/ask queries with strict price-time FIFO priority, print multi-level depth snapshots, assert the crossed-book invariant, and benchmark add throughput to understand why std::map is the wrong choice for HFT. | ⬜ Not started | — | — | — |
| Add a market data publication layer to the fast LOB: emit incremental BookUpdate messages (ADD_LEVEL, CHANGE_LEVEL, REMOVE_LEVEL) and BBOUpdate messages on BBO changes, build a full-depth snapshot function for new subscribers, and implement sequence-number-based gap detection. | ⬜ Not started | — | — | — |
| Complete the fast order book's management layer: an order pool (slab allocator) for allocation-free hot-path operation, an ID→Order* hash map for O(1) cancel, and correct exchange-standard amend priority semantics (price-change/qty-up loses priority; qty-down retains it). | ⬜ Not started | — | — | — |
| Build a systematic test harness for the order book and matching engine: define and assert five book invariants, replay a golden order sequence fill-by-fill, run 50,000+ randomized property tests, and cover edge cases including empty book, duplicate cancel, qty conservation, and FOK rejection. | ⬜ Not started | — | — | — |

## Market Data & Low-Latency Networking

| Project | Score | Understanding | Reviewed | Feedback |
|---|---|---|---|---|
| Build a recovery state machine that detects sequence gaps, fetches a TCP snapshot, buffers live incrementals during recovery, replays them in order, and implements A/B redundant-feed arbitration by sequence number. | ⬜ Not started | — | — | — |
| Build a multicast sender and receiver using IP_ADD_MEMBERSHIP on loopback, batch-receive with recvmmsg, and read software receive timestamps via SO_TIMESTAMPING from the ancillary control message chain. | ⬜ Not started | — | — | — |
| Capstone: build a complete multicast feed handler that decodes a binary ITCH stream with zero allocation, detects sequence gaps, updates a pre-allocated order book, and reports p50/p99/p99.9 decode+apply latency over 200,000 messages. | ⬜ Not started | — | — | — |
| Implement an ITCH 5.0-inspired binary protocol parser using packed structs, zero-copy field views, and correct big-endian byte swapping, then benchmark the decode path to confirm zero heap allocation. | ⬜ Not started | — | — | — |
| Measure RDTSC and clock_gettime overhead, demonstrate cross-core TSC skew, build a tick-to-trade latency histogram, and model the PTP offset calculation that enables sub-100 ns clock synchronization for MiFID II compliance. | ⬜ Not started | — | — | — |
| Build UDP and TCP sockets that model exchange market-data and order-gateway protocols, measure Nagle's algorithm and head-of-line blocking, and understand why exchanges split traffic across both transports. | ⬜ Not started | — | — | — |
| Build a complete UDP feed handler that decodes ITCH-style binary messages, dispatches by message type via a switch table, updates an order book, and measures end-to-end decode+apply latency. | ⬜ Not started | — | — | — |
| Study the kernel packet path's latency sources, implement SO_BUSY_POLL and a manual non-blocking spin-poll loop on standard sockets, and survey the kernel-bypass technology landscape (DPDK, AF_XDP, io_uring, a kernel-bypass NIC ef_vi). | ⬜ Not started | — | — | — |

## Systems Tuning & the Matching-Engine Capstone

| Project | Score | Understanding | Reviewed | Feedback |
|---|---|---|---|---|
| Build an async SPSC log queue, an atomic kill switch, and a stale-data graceful degradation guard — each adding under 50 ns to the hot path — and benchmark the reliability overhead versus naive synchronous alternatives. | ⬜ Not started | — | — | — |
| Assemble the complete HFT track: a price-time-priority matching engine fed by a simulated binary feed handler over a lock-free SPSC queue, running on pinned threads with no hot-path allocation, instrumented with a latency histogram, packaged with CMake and GoogleTest, and documented with architecture, measurements, and two explicit tradeoffs. | ⬜ Not started | — | — | — |
| Configure Linux kernel boot parameters (isolcpus, nohz_full, rcu_nocbs), the CPU frequency governor, C-state limits, IRQ affinity, and measure the before/after jitter reduction with a latency histogram. | ⬜ Not started | — | — | — |
| Decompose wire-to-wire tick-to-trade latency across feed-handler, book-update, strategy, and order-gateway stages, instrument each with CLOCK_MONOTONIC, set a per-stage budget, and validate budget compliance with a reusable LatencyBudget checker. | ⬜ Not started | — | — | — |
| Identify and eliminate tail-latency spikes from page faults, TLB shootdowns, and hot-path allocations using pre-faulting, cache warming, object pools, perf stat, and a pre-flight validation script. | ⬜ Not started | — | — | — |
| Pin threads to isolated CPU cores with sched_setaffinity and pthread_setaffinity_np, apply SCHED_FIFO real-time priority with chrt, move workqueue threads off hot cores, and measure jitter reduction across four isolation configurations. | ⬜ Not started | — | — | — |
| Benchmark NUMA-local vs NUMA-remote DRAM latency with pointer chasing, allocate memory on the correct node with libnuma, reduce TLB miss pressure using MAP_HUGETLB, and lock all process memory with mlockall. | ⬜ Not started | — | — | — |
| Map the six components of an HFT trading system (feed handler, order book, strategy, order gateway, risk, logger) onto isolated cores connected by typed SPSC queues, implement the skeleton, and annotate every technique from the track to its architectural home. | ⬜ Not started | — | — | — |

---
*Machine-readable proof with commit SHA anchors: [verified-record.json](./verified-record.json)*