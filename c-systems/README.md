# C & Systems Programming (Zero to the Kernel) — Full Track Record

**vrboddhula** · [← Back to profile](../README.md) · Updated 2026-09-12

## Progress

[░░░░░░░░░░░░░░░░░░░░] 0%   (0 of 48 projects completed)

## C Foundations & the Toolchain

| Project | Score | Understanding | Reviewed | Feedback |
|---|---|---|---|---|
| Write your first C program, trace the four-stage gcc compilation pipeline (preprocess/compile/assemble/link), and understand why C produces tiny, fast native binaries. | ⬜ Not started | ❌ Failed | 2026-08-26 | [→](https://github.com/techmonster-dev-org/tm-student-vrboddhula-c-systems/issues/1) |
| Master printf/scanf format strings, read input safely with fgets, understand C strings as null-terminated char arrays, and use <string.h> functions (strlen, strcpy, strcmp, strcat) while learning why gets() was a security disaster. | ⬜ Not started | — | — | — |
| Write prototypes and definitions, observe pass-by-value, trace the call stack through recursion, use static local variables for persistent state, and control file-scope visibility with static/extern linkage. | ⬜ Not started | — | — | — |
| Explore C's fundamental types, use sizeof and <limits.h> to inspect platform sizes and bounds, use <stdint.h> fixed-width types, and understand why signed overflow is undefined behavior while unsigned wraparound is not. | ⬜ Not started | ❌ Failed | 2026-09-12 | [→](https://github.com/techmonster-dev-org/tm-student-vrboddhula-c-systems/issues/4) |
| Master C's if/else, switch with fallthrough, all three loop forms, break/continue, and the kernel-style goto cleanup ladder — the control flow patterns found in the Linux kernel, git, nginx, and SQLite. | ⬜ Not started | ❌ Failed | 2026-09-12 | [→](https://github.com/techmonster-dev-org/tm-student-vrboddhula-c-systems/issues/6) |
| Declare, initialize, and iterate 1D and 2D arrays, understand array decay to pointer, verify row-major memory layout, and observe why C performs no bounds checking — and how AddressSanitizer catches the resulting bugs. | ⬜ Not started | — | — | — |
| Master C's arithmetic, comparison, logical, and bitwise operators, understand operator precedence traps, and implement the set/test/clear/toggle bit-manipulation patterns used in every device driver and systems library. | ⬜ Not started | ⚠️ Unverified | 2026-09-12 | [→](https://github.com/techmonster-dev-org/tm-student-vrboddhula-c-systems/issues/5) |
| Build a complete wc-style line/word/character counter using argc/argv, fopen/fgets/fclose, multi-function design, error handling with stderr, and a Makefile — synthesizing every concept from Phase 1 into a real Unix-quality command-line tool. | ⬜ Not started | — | — | — |

## Pointers, Memory & Manual Management

| Project | Score | Understanding | Reviewed | Feedback |
|---|---|---|---|---|
| Build a growable heap array using the double-capacity realloc strategy, manage arrays of structs with owned string fields, implement deep vs shallow copy, and verify zero leaks with Valgrind. | ⬜ Not started | — | — | — |
| Declare pointer variables, use & and * to take addresses and dereference, handle NULL safely, and use pointer-to-pointer to pass pointers as output parameters. | ⬜ Not started | — | — | — |
| Write the layer underneath malloc: a bump/arena allocator over one heap block with correct alignment via _Alignof and max_align_t, a fixed-size pool allocator whose free list lives inside the free blocks themselves, and a bitset for occupancy tracking — then benchmark the arena against malloc and report the measured speedup with its conditions. | ⬜ Not started | — | — | — |
| Compare stack vs heap lifetime by printing their addresses, then use malloc/calloc/realloc/free to manage dynamic arrays and return heap memory from a function with documented ownership transfer. | ⬜ Not started | — | — | — |
| Declare and call function pointers, pass a comparator to qsort, build a dispatch table, and implement a minimal struct file_operations-style vtable to understand how C achieves runtime polymorphism. | ⬜ Not started | — | — | — |
| Define structs and access fields with . and ->, observe struct padding with offsetof/sizeof, use unions for type punning float bits, and pair enums with typedef for clean state machines. | ⬜ Not started | — | — | — |
| Explore array-to-pointer decay, pointer arithmetic, and null-terminated strings by implementing my_strlen and my_strcpy from scratch using only pointer operations. | ⬜ Not started | — | — | — |
| Deliberately reproduce a memory leak, use-after-free, double-free, and buffer overflow in C, then detect each with Valgrind --leak-check=full and GCC -fsanitize=address, and produce a clean fixed version. | ⬜ Not started | — | — | — |

## Modular C & Data Structures

| Project | Score | Understanding | Reviewed | Feedback |
|---|---|---|---|---|
| Package the dynamic array, doubly linked list, and hash table into a single libds static library with a professional directory layout, a Makefile that builds libds.a, and a test runner that is Valgrind and ASan-clean. | ⬜ Not started | — | — | — |
| Build singly and doubly linked list libraries in C, then implement the Linux kernel's intrusive list_head pattern with container_of — giving O(1) insert/remove at any known node. | ⬜ Not started | — | — | — |
| Build a growable array library in C using void* + element size, realloc with a doubling strategy for amortized O(1) push, and a clean opaque-struct API with create/destroy/push/pop/get/set. | ⬜ Not started | — | — | — |
| Build a string-keyed hash map with separate chaining, FNV-1a hashing, and automatic rehashing when the load factor exceeds 0.75 — achieving O(1) average lookup for any key. | ⬜ Not started | — | — | — |
| Build the fixed-capacity queue that kernels, UART drivers, audio stacks, and low-latency feeds are built on: a flat power-of-two buffer indexed by bitmask instead of modulo, free-running cursors that resolve the full-vs-empty ambiguity the way Linux kfifo does, and wrap-around handled by two memcpy calls with no data ever moved. | ⬜ Not started | — | — | — |
| Master C error-handling patterns: return-code conventions, errno + perror/strerror, the goto-cleanup pattern for multi-resource functions, and designing APIs that cannot silently leak on failure. | ⬜ Not started | — | — | — |
| Take a C program from source text to executable: split it into headers and translation units with include guards and extern, build it incrementally with a Makefile, then open the layer underneath — raw macro expansion with gcc -E, the precedence and multiple-evaluation traps, conditional compilation, assert, and the X-macro pattern. | ⬜ Not started | — | — | — |
| Build type-erased C functions using void* pointers, memcpy for element copying, and comparator/printer callbacks — the model behind qsort, bsearch, and every C container library. | ⬜ Not started | — | — | — |

## Systems Programming I — Processes, Files & IPC

| Project | Score | Understanding | Reviewed | Feedback |
|---|---|---|---|---|
| Master the POSIX open/read/write/close/lseek syscall family, understand O_* flags, and build working cat and cp clones using raw file descriptors. | ⬜ Not started | — | — | — |
| Learn to create and manage processes using fork, exec, and waitpid — the foundation of every Unix shell, build system, and process supervisor. | ⬜ Not started | — | — | — |
| Learn what system calls are, how the user/kernel mode boundary works, and how to use write(2), errno, perror, and strace to understand and debug programs at the OS level. | ⬜ Not started | — | — | — |
| Master POSIX signal handling with sigaction, implement graceful shutdown, use SIGCHLD to reap children asynchronously, and understand async-signal-safety. | ⬜ Not started | — | — | — |
| Capstone project: build a working interactive Unix shell in C that handles external commands, single pipes, input/output redirection, built-ins (cd, exit, help), and Ctrl-C gracefully. | ⬜ Not started | — | — | — |
| Use mmap() to access files as memory arrays, create anonymous mappings, and build a POSIX shared-memory IPC channel between two processes using shm_open. | ⬜ Not started | — | — | — |
| Build well-behaved CLI programs in C: parse options with getopt, read and modify environment variables, register atexit cleanup handlers, and measure wall and CPU time. | ⬜ Not started | — | — | — |
| Implement shell-style pipes and redirection in C using pipe(), dup2(), fork(), and exec() — connecting processes so one's output feeds another's input. | ⬜ Not started | — | — | — |

## Systems Programming II — Concurrency & Networking

| Project | Score | Understanding | Reviewed | Feedback |
|---|---|---|---|---|
| Create and join POSIX threads, pass arguments via void*, retrieve results, compare threads vs processes, and observe a data race with ThreadSanitizer. | ⬜ Not started | — | — | — |
| Fix a data race with pthread_mutex, implement a bounded producer-consumer queue with condition variables, and demonstrate and prevent deadlock. | ⬜ Not started | — | — | — |
| Build a single-threaded TCP echo server using the epoll API (epoll_create1/epoll_ctl/epoll_wait) with non-blocking sockets, handle 100 simultaneous clients, and understand the reactor pattern. | ⬜ Not started | — | — | — |
| Build a TCP echo server and client from raw POSIX syscalls, handle partial send/recv, set SO_REUSEADDR and TCP_NODELAY, and measure loopback round-trip latency. | ⬜ Not started | — | — | — |
| Build a production-quality key-value server combining an epoll accept loop, a thread pool, a mutex-protected hash table, and a binary request/response protocol, with a clean shutdown that passes Valgrind with zero leaks. | ⬜ Not started | — | — | — |
| Use <stdatomic.h> to build a lock-free counter and a single-producer/single-consumer ring buffer, and benchmark atomics against mutexes on a multi-core machine. | ⬜ Not started | — | — | — |
| Implement read_n/write_n helpers that handle partial reads, EINTR, and EOF, then build a length-prefix framing layer and use it to exchange variable-length messages between a framed echo server and client. | ⬜ Not started | — | — | — |
| Build a fixed-size thread pool backed by a synchronized task queue, dispatch accepted TCP connections to worker threads, pre-allocate connection structs to avoid per-request malloc, and benchmark throughput against the single-threaded event loop. | ⬜ Not started | — | — | — |

## Bare Metal, Embedded & the Kernel

| Project | Score | Understanding | Reviewed | Feedback |
|---|---|---|---|---|
| Declare and manipulate simulated hardware registers using volatile pointers, implement the read-modify-write pattern for GPIO configuration and BSRR atomic set/clear, and simulate a polling UART transmit loop. | ⬜ Not started | — | — | — |
| Configure SysTick interrupts on a bare-metal Cortex-M3, write a naked context-switch ISR in inline ARM assembly, build fake initial task frames, and implement a two-task round-robin preemptive scheduler. | ⬜ Not started | — | — | — |
| Build a real networked key-value store server: an epoll event loop, a hand-written chaining hash table with resize, a line-oriented GET/SET protocol with partial-read handling, a test client, and a Makefile build proven memory-safe under Valgrind and AddressSanitizer. | ⬜ Not started | — | — | — |
| Write a complete bare-metal blink program for ARM Cortex-M3 from scratch: linker script, startup.c reset handler with .data/.bss init, GPIO register writes, and a cross-compiled Makefile build runnable in QEMU. | ⬜ Not started | — | — | — |
| Write, build, and load a Linux loadable kernel module using the Kbuild Makefile system; use printk, module_param, and module_init/exit; explain the kernel-space constraints that make C the kernel's language. | ⬜ Not started | — | — | — |
| Compile C to assembly with gcc -S, trace the System V AMD64 calling convention and stack frame, apply volatile to hardware register simulation, write inline asm with RDTSC, and build a freestanding object with no OS runtime. | ⬜ Not started | — | — | — |
| Implement a complete Linux character device driver with a circular buffer: file_operations (open/release/read/write), alloc_chrdev_region, cdev_add, class_create/device_create for /dev, and copy_to_user/copy_from_user with proper mutex locking. | ⬜ Not started | — | — | — |
| Implement a static memory pool (no malloc), Q16.16 fixed-point PID controller, watchdog/WCET simulation, MISRA-C violation/fix examples, and a CAN frame builder — the full set of constraints governing safety-critical automotive/aerospace/robot firmware. | ⬜ Not started | — | — | — |

---
*Machine-readable proof with commit SHA anchors: [verified-record.json](./verified-record.json)*