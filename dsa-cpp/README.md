# Data Structures & Algorithms in C++ (Interview-Grade) — Full Track Record

**vrboddhula** · [← Back to profile](../README.md) · Updated 2026-10-27

## Progress

[░░░░░░░░░░░░░░░░░░░░] 0%   (0 of 48 projects completed)

## Complexity & Array Foundations

| Project | Score | Understanding | Reviewed | Feedback |
|---|---|---|---|---|
| Implement four classic two-pointer problems — reverse in place, pair-sum on sorted array, remove duplicates, and palindrome check — and prove each is O(n) vs the O(n²) naive approach. | ⬜ Not started | — | — | — |
| Build 1D and 2D prefix-sum arrays to answer arbitrary range-sum queries in O(1), implement a difference array for O(1) range updates, and understand the preprocessing vs query time tradeoff. | ⬜ Not started | — | — | — |
| Synthesise all Phase 1 techniques — two-pointer, sliding window, prefix sums, and matrix operations — into a single CLI toolkit with a complexity reference table, a benchmark, and a problem-triage decision guide. | ⬜ Not started | — | — | — |
| Build intuition for asymptotic complexity by implementing the five common complexity classes, deriving Big-O from code, and empirically timing algorithms with std::chrono to watch growth curves diverge. | ⬜ Not started | ⚠️ Unverified | 2026-10-27 | [→](https://github.com/techmonster-dev-org/tm-student-vrboddhula-dsa-cpp/issues/1) |
| Master the fundamental array traversal patterns — find max/min, count, accumulate, and in-place modify — using std::vector, and observe why contiguous memory and cache-friendliness make arrays fast in practice. | ⬜ Not started | ❌ Failed | 2026-10-27 | [→](https://github.com/techmonster-dev-org/tm-student-vrboddhula-dsa-cpp/issues/2) |
| Implement row-major traversal, spiral and diagonal iteration, and in-place transpose and 90° rotation of a square matrix, expressing all complexity in terms of both m and n. | ⬜ Not started | — | — | — |
| Solve fixed-window and variable-window subarray problems — max-sum of size-k subarray, longest unique substring, minimum-length sum window — in O(n) using a sliding window, and contrast with O(n²) naive solutions. | ⬜ Not started | — | — | — |
| Build a minimal MyVector<T> from scratch with new[]/delete[] and capacity doubling, then prove that push_back is amortized O(1) using the aggregate counting method. | ⬜ Not started | ❌ Failed | 2026-10-27 | [→](https://github.com/techmonster-dev-org/tm-student-vrboddhula-dsa-cpp/issues/3) |

## Linear Structures: Lists, Stacks & Queues

| Project | Score | Understanding | Reviewed | Feedback |
|---|---|---|---|---|
| Implement the Queue ADT as a linked-node queue with O(1) enqueue/dequeue and then as a fixed-size circular ring buffer with modulo wrap-around, zero runtime allocation, and a count-based full/empty disambiguation. | ⬜ Not started | — | — | — |
| Build a templated SinglyLinkedList<T> from scratch using raw node pointers, implementing push_front (O(1)), push_back (O(n)), remove, search, traversal, and a correct RAII destructor with full Rule of Five compliance. | ⬜ Not started | — | — | — |
| Implement the four classic interview linked-list algorithms — in-place reversal (iterative and recursive), Floyd's cycle detection, slow/fast middle-finding, and sorted list merge — each as a stand-alone O(1)-space program. | ⬜ Not started | — | — | — |
| Build a templated DoublyLinkedList<T> with prev/next pointers and head/tail anchors, enabling O(1) insert and delete at both ends and O(1) node removal given a pointer handle. | ⬜ Not started | — | — | — |
| Implement four canonical algorithms that demonstrate the power of LIFO and FIFO disciplines: balanced bracket checking, Shunting-Yard infix-to-postfix conversion with postfix evaluation, next-greater-element via a monotonic stack, and a BFS level-order traversal preview. | ⬜ Not started | — | — | — |
| Build an O(1) Least-Recently-Used cache by composing std::unordered_map with a hand-written doubly linked list (with sentinel nodes), implementing get and put in strictly O(1) time with correct LRU eviction and move-to-front on access. | ⬜ Not started | — | — | — |
| Implement the Stack ADT two ways — a fixed-capacity array-backed ArrayStack<T,N> with zero runtime allocation and a dynamically growing LinkedStack<T> backed by linked nodes — then compare their complexity and allocation trade-offs. | ⬜ Not started | — | — | — |
| Build a Deque<T> backed by a doubly linked list with O(1) push/pop at both ends, then implement the sliding-window maximum using a monotonic deque to show the structure's canonical O(n) application. | ⬜ Not started | — | — | — |

## Recursion, Searching & Sorting

| Project | Score | Understanding | Reviewed | Feedback |
|---|---|---|---|---|
| Build an array-based binary max-heap from scratch with sift_up, sift_down, and O(n) heapify, then implement heap sort (in-place, O(n log n), not stable) and a full priority queue interface — the same heap that powers Dijkstra and std::priority_queue. | ⬜ Not started | — | — | — |
| Implement classic binary search with overflow-safe mid, then build lower_bound and upper_bound from scratch, search a rotated sorted array, and apply binary search on the answer to an optimisation problem — understanding the loop invariant that makes each variant correct. | ⬜ Not started | — | — | — |
| Implement merge sort from scratch — the merge step, recursive split, and bottom-up iterative variant — derive T(n) = 2T(n/2) + O(n) via the recursion tree, verify O(n log n) time and O(n) space, and confirm stability with a keyed-record test. | ⬜ Not started | — | — | — |
| Implement Lomuto and Hoare partition schemes, observe the O(n^2) worst case with fixed pivot on sorted input, eliminate it with randomised pivot selection, and handle duplicates efficiently with three-way Dutch National Flag partitioning. | ⬜ Not started | — | — | — |
| Consolidate all six sorting algorithms into a comparison table, prove the Omega(n log n) comparison lower bound with a decision-tree argument, implement counting sort and radix sort from scratch, and learn what std::sort (introsort) and std::stable_sort actually do. | ⬜ Not started | — | — | — |
| Build factorial, Fibonacci, and exponentiation recursively, trace the call stack frame-by-frame, observe exponential blow-up, fix it with memoisation, and understand tail recursion — tying hardware stack mechanics to algorithmic reasoning. | ⬜ Not started | — | — | — |
| Build a header-only toolkit.hpp exposing binary_search, lower_bound, merge_sort, quick_sort, and heap_sort, then benchmark all five against std::sort and std::stable_sort on random, sorted, and reversed inputs using <chrono>, and write a structured empirical analysis tying the numbers back to algorithmic theory. | ⬜ Not started | — | — | — |
| Implement bubble, selection, and insertion sort from scratch with comparison/swap counters, compare their behaviour on sorted, random, and reverse inputs, and understand stability, in-place sorting, and why insertion sort remains relevant inside every production sort library. | ⬜ Not started | — | — | — |

## Trees, Heaps & Tries

| Project | Score | Understanding | Reviewed | Feedback |
|---|---|---|---|---|
| Synthesize Phase 4 by building a complete Huffman coding pipeline: frequency table, greedy tree construction with a min-heap, prefix-free codebook generation by tree traversal, encode a string to bits, and decode using the tree as a trie. | ⬜ Not started | — | — | — |
| Build a binary tree from scratch with RAII cleanup and implement all four traversals — preorder, inorder, postorder (recursive and iterative with an explicit stack), and level-order BFS — to understand how the call stack and data-structure traversal relate. | ⬜ Not started | — | — | — |
| Implement an array-backed max-heap with sift-up push, sift-down pop, and O(n) build_heap, then generalize it as a PriorityQueue<T,Comp> class template that works as min- or max-heap, and apply it to the top-K streaming problem. | ⬜ Not started | — | — | — |
| Build a Fenwick tree (BIT) for O(log n) prefix-sum update and query using the lowbit trick, then build a segment tree supporting both range-sum and range-min queries with point updates, and compare when each structure is appropriate. | ⬜ Not started | — | — | — |
| Build a trie from scratch with 26-slot array children and an end-of-word flag, implementing insert, search, startsWith, and an autocomplete function via DFS-with-backtracking. | ⬜ Not started | — | — | — |
| Build a full BST with insert, search, and delete (all three cases including two-children/inorder-successor) from scratch, and confirm that inorder traversal always yields sorted output. | ⬜ Not started | — | — | — |
| Implement the eight classic interview tree algorithms — height, balanced-check, diameter, LCA, validate-BST, invert, and path-sum — each demonstrating a distinct recursive postorder-reduction pattern. | ⬜ Not started | — | — | — |
| Implement an AVL self-balancing BST from scratch — height-tracked nodes, left/right rotations, all four imbalance cases (LL/RR/LR/RL), and insert with automatic rebalancing — proving that O(log n) height is maintained regardless of input order. | ⬜ Not started | — | — | — |

## Hashing & Graphs

| Project | Score | Understanding | Reviewed | Feedback |
|---|---|---|---|---|
| Build a reusable Graph class with adjacency-list and adjacency-matrix representations for directed/undirected weighted graphs, analyze space and time tradeoffs, and load graphs from edge lists. | ⬜ Not started | — | — | — |
| Implement Dijkstra's algorithm with a min-heap priority queue for non-negative weighted shortest paths, and topological sort via both DFS post-order and Kahn's BFS algorithm with cycle detection. | ⬜ Not started | — | — | — |
| Build a HashMap<K,V> with separate chaining, load-factor-triggered resize, and average O(1) insert/find/erase, then compare against std::unordered_map. | ⬜ Not started | — | — | — |
| Synthesise the phase: build a GridPathfinder running BFS and Dijkstra on weighted terrain, implement Union-Find with path compression and union by rank, and apply it to Kruskal-style connectivity. | ⬜ Not started | — | — | — |
| Implement recursive and iterative DFS on the Project 4 Graph class, detect directed cycles with three-color marking, detect undirected cycles with parent tracking, and enumerate all paths with backtracking. | ⬜ Not started | — | — | — |
| Build a FlatMap<K,V> with linear probing and tombstone deletion, implement double hashing to eliminate clustering, and compare cache behavior against separate chaining. | ⬜ Not started | — | — | — |
| Implement five canonical hashing patterns — frequency counting, deduplication, two-sum, group anagrams, and subarray-sum-equals-k — each turning an O(n²) brute force into an O(n) solution. | ⬜ Not started | — | — | — |
| Implement BFS with a queue on the Project 4 Graph class to compute shortest unweighted paths, find connected components, and solve a grid maze with an implicit graph. | ⬜ Not started | — | — | — |

## Algorithm Design & Interview Mastery

| Project | Score | Understanding | Reviewed | Feedback |
|---|---|---|---|---|
| Implement grid unique-paths, min-path-sum, 0/1 knapsack, LCS, and edit distance with full 2D tables and space-compressed variants, including solution reconstruction for LCS. | ⬜ Not started | — | — | — |
| Build a CMake-packaged, GoogleTest-tested C++ application combining a Trie-backed autocomplete (top-k via heap) and a weighted-graph route planner (Dijkstra), structured as a library + thin CLI with 10 tests covering happy paths and edge cases. | ⬜ Not started | — | — | — |
| Build a systematic problem-solving framework mapping 8 signal patterns to algorithms, implement the same problem two ways with explicit tradeoff analysis, and study the complexity targets and LeetCode strategy that make pattern mastery stick. | ⬜ Not started | — | — | — |
| Implement ten canonical bit tricks (check/set/clear/toggle, LSB, popcount, power-of-2, XOR swap, single number, bitmask subsets), explain their two's complement mechanics, and apply them to HFT-style flag operations. | ⬜ Not started | — | — | — |
| Implement maximum subarray (D&C vs Kadane), inversion counting via merge sort, and fast exponentiation, then apply the Master Theorem to analyze the recurrence of each. | ⬜ Not started | — | — | — |
| Implement permutations, subsets, combinations, N-Queens, and a Sudoku solver using the choose/explore/un-choose template, then quantify how pruning reduces nodes visited exponentially. | ⬜ Not started | — | — | — |
| Implement Fibonacci, climbing stairs, house robber, coin change (minimum coins), and LIS from scratch using both memoization and tabulation, deriving each recurrence from first principles. | ⬜ Not started | — | — | — |
| Build four greedy classics from scratch — interval scheduling, coin change (with DP counterexample), fractional knapsack, and Huffman coding — proving each correct or wrong via the exchange argument. | ⬜ Not started | — | — | — |

---
*Machine-readable proof with commit SHA anchors: [verified-record.json](./verified-record.json)*