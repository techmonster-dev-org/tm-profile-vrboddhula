# C++ From Zero (Absolute Beginner to Modern C++) — Full Track Record

**vrboddhula** · [← Back to profile](../README.md) · Updated 2026-08-26

## Progress

[░░░░░░░░░░░░░░░░░░░░] 0%   (0 of 48 projects completed)

## Setup, First Programs, Types & I/O

| Project | Score | Understanding | Reviewed | Feedback |
|---|---|---|---|---|
| Combine types, I/O, expressions, constants, and validation into a robust menu-driven unit converter that loops until quit and recovers cleanly from bad input — the read/validate/process/print skeleton that scales up to the track capstone. | ⬜ Not started | — | — | — |
| Use fixed-width integer types from <cstdint>, compare signed/unsigned ranges, reproduce and explain overflow (unsigned wrap as modular arithmetic; signed overflow as undefined behavior), and choose integer types deliberately by range and size. | ⬜ Not started | — | — | — |
| Declare C++'s fundamental types (int, double, char, bool), measure their byte sizes with sizeof, explore ranges with <limits>, and use auto deduction — grounding static typing in the powers-of-two and overflow reasoning from math-foundations. | ⬜ Not started | ❌ Failed | 2026-08-26 | [→](https://github.com/techmonster-dev-org/tm-student-vrboddhula-cpp-from-zero/issues/2) |
| Master arithmetic, comparison, and logical operators and the type rules that govern them — the integer-division trap, modulo, type promotion with static_cast, precedence, and compound assignment. | ⬜ Not started | — | — | — |
| Make programs interactive with std::cin and std::cout: read typed values and whole lines, format floating-point output, and detect failed reads — the input/process/output skeleton of every CLI tool. | ⬜ Not started | ⚠️ Unverified | 2026-08-26 | [→](https://github.com/techmonster-dev-org/tm-student-vrboddhula-cpp-from-zero/issues/3) |
| Work with text using std::string — concatenate, index, search with find, slice with substr — contrast it with error-prone C-style char arrays, and build small text tools (uppercase, vowel count, key=value split). | ⬜ Not started | — | — | — |
| Install a C++ compiler, write/compile/run a minimal program, and understand the compile-link-execute pipeline and how it differs from interpreted languages — building toolchain literacy, not just a hello world. | ⬜ Not started | ⚠️ Unverified | 2026-08-26 | [→](https://github.com/techmonster-dev-org/tm-student-vrboddhula-cpp-from-zero/issues/1) |
| Use const and constexpr for immutability and compile-time constants, convert between types safely with static_cast (recognizing narrowing/data loss), and convert numbers to/from strings — instilling const-correctness. | ⬜ Not started | — | — | — |

## Control Flow & Functions

| Project | Score | Understanding | Reviewed | Feedback |
|---|---|---|---|---|
| Branch on discrete values with switch/case, use break and understand intentional vs accidental fall-through, group cases, provide a default, and decide when switch beats an if/else chain. | ⬜ Not started | — | — | — |
| Distinguish scope (visibility) from lifetime (existence): block scope, variable shadowing, static locals that persist across calls, automatic vs static storage, and the dangers of mutable global state — groundwork for pointers and RAII. | ⬜ Not started | — | — | — |
| Repeat work with while, for, and do-while loops, control them with break and continue, use range-based for over a collection, and avoid infinite-loop and off-by-one traps — connecting iteration count to Big-O. | ⬜ Not started | — | — | — |
| Combine functions, conditionals, loops, and switch into a cleanly decomposed interactive calculator: pure operation functions, a validated input helper, a switch dispatcher, std::optional for division-by-zero, and a thin main — the structure that makes the track capstone testable. | ⬜ Not started | — | — | — |
| Overload functions by parameter type and arity, understand compile-time overload resolution, provide trailing default arguments, and recognize/fix ambiguous calls. | ⬜ Not started | — | — | — |
| Write recursive functions (factorial, Fibonacci, sum-of-digits, power) with base and recursive cases, trace the call stack, compare to iteration, hit and explain stack overflow, and connect to induction/recurrences and memoization from math-foundations. | ⬜ Not started | — | — | — |
| Branch program flow with if/else if/else and the ternary operator, build compound conditions with && and ||, order conditions correctly in a grade classifier, and avoid the =/== and dangling-else traps. | ⬜ Not started | — | — | — |
| Define and call functions with typed parameters and return values, understand pass-by-value (copies), write void action functions, use declarations vs definitions, and decompose a problem into small single-purpose functions. | ⬜ Not started | — | — | — |

## The Memory Model — Pointers, References & the Stack/Heap

| Project | Score | Understanding | Reviewed | Feedback |
|---|---|---|---|---|
| Discover the pointer-array connection: array-name decay, pointer arithmetic that scales by element size, the equivalence arr[i] == *(arr+i), and the half-open begin/end traversal idiom that STL iterators generalize. | ⬜ Not started | — | — | — |
| Use references as aliases for existing variables, pass by reference to modify caller data (a working swap), pass large objects by const& for efficiency and safety, and learn when to choose a reference vs a pointer. | ⬜ Not started | — | — | — |
| Store many values in contiguous memory with fixed-size arrays, iterate with indexed and range-based loops, observe the contiguous layout via element addresses, and confront the limitations (no bounds check, no size knowledge) that motivate std::vector. | ⬜ Not started | — | — | — |
| Master the three ways to pass data — by value, by reference, by pointer — with correct const usage, output parameters, and a practical decision rule for which to use based on size, mutability, and nullability. | ⬜ Not started | — | — | — |
| Understand pointers as variables holding memory addresses: use address-of (&) and dereference (*), read and modify a value through a pointer (indirection), and use nullptr with guarded dereferences. | ⬜ Not started | — | — | — |
| Build a growable integer array by hand with new[]/delete[] — your own mini std::vector — tracking size vs capacity, doubling on growth (amortized O(1), per the geometric series), and freeing in a destructor (first RAII), then reflect on the manual bookkeeping smart pointers automate. | ⬜ Not started | — | — | — |
| Deliberately create and then fix the classic manual-memory bugs — leaks, dangling pointers (use-after-free), and double-frees — detect them with AddressSanitizer, and understand why these failures motivate RAII and smart pointers. | ⬜ Not started | — | — | — |
| Learn the two memory regions — the automatic stack and the manual heap — allocate with new/new[] and free with delete/delete[], allocate runtime-sized arrays, and understand the speed/size/lifetime tradeoffs that motivate RAII. | ⬜ Not started | — | — | — |

## RAII, Ownership & Smart Pointers

| Project | Score | Understanding | Reviewed | Feedback |
|---|---|---|---|---|
| Use std::unique_ptr and make_unique to own heap objects with automatic cleanup (RAII for any allocation), understand exclusive ownership (no copy, only move via std::move), borrow with .get(), and make ownership explicit in function signatures. | ⬜ Not started | — | — | — |
| Define your own types with classes — bundling member data and methods, controlling access with public/private, marking read-only methods const, and enforcing class invariants through encapsulation. | ⬜ Not started | — | — | — |
| Learn the defining C++ idiom: tie a resource's lifetime to an object's, acquiring in the constructor and releasing in the destructor so cleanup is automatic and guaranteed — even on early returns and exceptions — then refactor leaky manual-memory code into a leak-proof RAII wrapper. | ⬜ Not started | — | — | — |
| Share ownership of a heap object with std::shared_ptr and make_shared, watch reference counting via use_count() determine when the object is freed, decide shared vs unique ownership, and observe the reference-cycle leak that motivates weak_ptr. | ⬜ Not started | — | — | — |
| Use std::weak_ptr as a non-owning observer of a shared_ptr's object: access safely via lock(), detect expiration, and break the reference-cycle leak by making the back-reference weak — completing the smart-pointer ownership toolkit. | ⬜ Not started | — | — | — |
| Build a complete, leak-proof resource-owning class (a FileLogger and a smart-pointer-owning TaskPool) using the Rule of Zero — composing from RAII members so cleanup is automatic and exception-safe — and verify correctness under AddressSanitizer. | ⬜ Not started | — | — | — |
| Control object birth and death: constructors that initialize state via member initializer lists, destructors that clean up, constructor overloading, and the automatic construct-on-entry/destruct-on-exit (reverse order) lifecycle that RAII is built on. | ⬜ Not started | — | — | — |
| Fix the copy bug in resource-owning classes: reproduce the double-free from default shallow copy, implement a deep-copying copy constructor and a self-assignment-safe copy assignment operator, state the Rule of Three, and learn = delete and the Rule of Zero. | ⬜ Not started | — | — | — |

## The STL & Templates

| Project | Score | Understanding | Reviewed | Feedback |
|---|---|---|---|---|
| Phase finale: write a class template Stack<T> backed by a std::vector<T> member — a generic, RAII-clean LIFO container (push/pop/top/empty/size) that works for any element type, nests (Stack<Stack<int>>), and solves a real problem (balanced brackets). Synthesizes templates + vector + RAII + clean design, the way real STL adaptors are built. | ⬜ Not started | — | — | — |
| Write your own generic functions with template <typename T>: argument deduction vs explicit arguments, multiple type parameters, compile-time instantiation (and why template errors are confusing), and constraining a template with a C++20 concept for clear diagnostics. | ⬜ Not started | — | — | — |
| Use std::vector — the production-grade version of your Phase 3 dynamic array: create/grow/access, iterate three ways, observe capacity doubling (amortized O(1) push_back), and use reserve to avoid reallocations. | ⬜ Not started | — | — | — |
| Use associative containers: build map<string,int>, insert/update/look up by key, query safely with contains/find/at (and avoid the [] auto-insert trap), iterate with structured bindings, build a word-frequency counter, and choose between sorted std::map (O(log n)) and hash-based std::unordered_map (avg O(1)). | ⬜ Not started | — | — | — |
| Use std::set for unique, sorted membership and deduplication (O(log n) contains/count), and std::pair/std::tuple to bundle values — accessing .first/.second and std::get<N>, unpacking with structured bindings, and returning multiple values from a function. | ⬜ Not started | — | — | — |
| Learn std::string properly (build/concatenate/search/slice, string↔number conversion) and meet std::string_view — a non-owning (pointer, length) view that passes and slices text with zero copying, plus when a view dangles. | ⬜ Not started | — | — | — |
| Learn iterators — the generalized-pointer abstraction every container shares: begin()/end() half-open ranges, *it / ++it / it->, const_iterator, find/erase by iterator (checking against end()), iterator invalidation (it = erase(it)), and how range-based for is iterators underneath. | ⬜ Not started | — | — | — |
| Replace raw loops with named STL algorithms over iterator ranges: sort (with comparator lambdas), find/count/count_if/any_of, max_element/accumulate (reduce), transform/copy_if (map/filter), and the remove_if+erase idiom — passing custom logic via lambdas. | ⬜ Not started | — | — | — |

## Modern C++ (Move Semantics, Lambdas, C++17/20)

| Project | Score | Understanding | Reviewed | Feedback |
|---|---|---|---|---|
| Let the compiler spell out types it already knows: use auto to deduce variable types (and know when it strips const/references vs const auto& which keeps them), and use C++17 structured bindings to unpack pairs, tuples, and structs into named variables. Master the modern map-iteration idiom for (const auto& [key, value] : map). | ⬜ Not started | — | — | — |
| Model absence and alternatives with the type system. Use std::optional<T> for 'a value or nothing' (nullopt, has_value, value_or, checked value() vs unchecked *) instead of -1/null sentinels, and std::variant<Ts...> as a type-safe union (holds_alternative, get, index) dispatched with std::visit and a generic lambda + if constexpr. | ⬜ Not started | — | — | — |
| Replace nested iterator-pair algorithms with readable left-to-right pipelines using the | operator and lazy, non-owning views: views::filter, views::transform, views::take, plus iota/drop/reverse. Prove laziness (computation happens on iteration, take(3) short-circuits), understand that views don't own data (dangling risk), and materialize a view into a vector when you need ownership. | ⬜ Not started | — | — | — |
| Upgrade a raw-resource-owning class (Buffer with int* data_) from Phase 4's Rule of Three to the modern Rule of Five by adding a noexcept move constructor and move assignment that steal the pointer and null the source. Watch a move transfer ownership with no allocation, guard self-assignment, then learn the Rule of Zero: a std::vector member generates all five correctly for free. | ⬜ Not started | — | — | — |
| A safe introduction to parallelism: launch and join a std::thread, deliberately create a data race (lost increments from unsynchronized ++counter) and understand why it's undefined behavior, fix it with std::mutex + std::lock_guard (RAII locking), and use std::async + std::future to return a value from parallel work via get(). Closes with the discipline rules of correct concurrent code. | ⬜ Not started | — | — | — |
| Learn the performance feature at the heart of modern C++: lvalues vs rvalues, what std::move really is (a cast, not a mover), and how a move steals a resource (O(1) pointer swap) instead of deep-copying. Build a Noisy class to watch COPY vs move, move-construct a std::string, and return a million-element vector by value for free. | ⬜ Not started | — | — | — |
| The C++ From Zero finale: build expense-analyzer, a real CLI tool that parses an expenses CSV and reports total, per-category breakdown, and largest expense. Structure it as a testable library + thin main, build it out-of-source with CMake, and cover it with a GoogleTest suite (happy path + edge cases: malformed amount, negative amount, empty input). Synthesizes RAII, STL, std::optional, lambdas, moves, and structured bindings into one portfolio-grade, leak-free project. | ⬜ Not started | — | — | — |
| Write anonymous functions inline with [capture](params){body}, capture surrounding variables by value [=] or reference [&] (a closure), and feed lambdas to STL algorithms (sort comparator, find_if/count_if predicates, for_each). Use mutable for stateful closures and std::function to store heterogeneous callables behind one signature, knowing its overhead. | ⬜ Not started | — | — | — |

---
*Machine-readable proof with commit SHA anchors: [verified-record.json](./verified-record.json)*