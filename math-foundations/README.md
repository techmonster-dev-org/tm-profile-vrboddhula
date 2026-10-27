# Math & Reasoning for Systems and Quant (Zero to Confident) — Full Track Record

**vrboddhula** · [← Back to profile](../README.md) · Updated 2026-10-27

## Progress

[░░░░░░░░░░░░░░░░░░░░] 0%   (0 of 48 projects completed)

## Number Sense, Mental Math & Estimation

| Project | Score | Understanding | Reviewed | Feedback |
|---|---|---|---|---|
| Build a base converter (to_base, from_base) using repeated division and positional notation, validate it against Python's bin/hex/int, and learn to read binary and hex the way the machine does — the bridge into computer architecture. | ⬜ Not started | — | — | — |
| Fuse the whole phase into systems estimation: a canonical latency table, time/byte unit converters, an estimate_runtime helper, and a full capacity estimate (does a day of logs fit in RAM?) reasoned out by hand. | ⬜ Not started | — | — | — |
| Build a timed arithmetic drill (your own timed arithmetic trainer) that generates random problems, scores answers against the clock, and reports a correct-per-minute rate — while learning the core mental-math shortcuts. | ⬜ Not started | ⚠️ Unverified | 2026-10-27 | [→](https://github.com/techmonster-dev-org/tm-student-vrboddhula-math-foundations/issues/1) |
| Build a clock-arithmetic toolkit (clock_add, wrap_index, add_uint8, day_of_week) that teaches remainders and wrap-around, and connect modulo to hashing, ring buffers, and integer overflow. | ⬜ Not started | — | — | — |
| Build an Estimate helper that records named multiplicative factors and answer order-of-magnitude questions (piano tuners in a city, daily queries for 10M users) by decomposition, then sanity-check results against quick estimates. | ⬜ Not started | — | — | — |
| Build a reference tool for powers of two and byte-size prefixes (humanize_bytes, order_of_magnitude) and train the instinct to estimate memory sizes, bit widths, and log-time growth in your head. | ⬜ Not started | ❌ Failed | 2026-10-27 | [→](https://github.com/techmonster-dev-org/tm-student-vrboddhula-math-foundations/issues/3) |
| Generate arithmetic and geometric sequences, derive and verify their closed-form sums against brute force, and use compounding and the rule of 72 to build intuition for linear vs exponential growth and algorithm loop costs. | ⬜ Not started | — | — | — |
| Build a percentage-and-ratio toolkit (percent_of, percent_change, apply_change, recovery_needed, ratio_to_parts) and learn the mental anchors to do the same calculations instantly, including the asymmetry-of-gains-and-losses trap. | ⬜ Not started | ❌ Failed | 2026-10-27 | [→](https://github.com/techmonster-dev-org/tm-student-vrboddhula-math-foundations/issues/2) |

## Discrete Math & Logic

| Project | Score | Understanding | Reviewed | Feedback |
|---|---|---|---|---|
| Learn induction (base case + inductive step), empirically check inductive identities, mirror classic proofs in code, and connect induction to recursion correctness and loop invariants — then write full proofs by hand. | ⬜ Not started | — | — | — |
| Build a set-algebra toolkit (union, intersection, difference, symmetric difference, subset, power set, inclusion-exclusion), connect each operation to its logical counterpart, and count overlapping groups without double-counting. | ⬜ Not started | — | — | — |
| Represent relations as pairs and functions as mappings, test validity/injectivity/surjectivity/bijectivity, compose and invert them, and classify real mappings (hashes, primary keys, ciphers) by which properties make them reversible. | ⬜ Not started | — | — | — |
| Build the fundamental logic gates from bits, prove NAND is universal, then compose half-adders and full-adders into a ripple-carry adder that performs binary addition — discovering that arithmetic is just logic, the doorway to computer architecture. | ⬜ Not started | — | — | — |
| Write recursive functions, express their cost as recurrence relations and solve by unrolling, expose naive Fibonacci's exponential blowup with a call counter, fix it with memoization, and recognize the master-theorem patterns. | ⬜ Not started | — | — | — |
| Build a truth-table generator with all five connectives plus tautology and equivalence checkers, then use De Morgan's laws and the contrapositive to simplify real boolean conditions by hand. | ⬜ Not started | — | — | — |
| Implement Euclid's GCD (recursive and iterative), LCM, the Sieve of Eratosthenes, primality testing, and prime factorization, then connect the multiply-easy/factor-hard asymmetry to public-key cryptography. | ⬜ Not started | — | — | — |
| Build a counting toolkit (factorial, nPr, nCr) and apply the product/sum rules and the pigeonhole principle to count outcomes, size search spaces, and prove that collisions must occur — the on-ramp to probability. | ⬜ Not started | — | — | — |

## Combinatorics & Probability

| Project | Score | Understanding | Reviewed | Feedback |
|---|---|---|---|---|
| Build variance and standard-deviation tools for random variables and data samples, demonstrate that equal-EV bets can carry wildly different risk, apply Bessel's correction, and confirm by simulation. | ⬜ Not started | — | — | — |
| Build an expected-value calculator and bet evaluator, apply linearity of expectation to collapse hard problems into simple sums, and watch the long-run simulated average converge to the EV — the core decision tool of trading. | ⬜ Not started | — | — | — |
| Build a probability calculator (exact fractions, complement and addition rules) alongside a Monte-Carlo simulator, and establish the core habit of deriving a closed-form probability then confirming it by simulation. | ⬜ Not started | — | — | — |
| Compute P(A|B) as sample-space narrowing, apply the multiplication rule for joint probability, test independence, and confirm by filtering simulations — then untangle the classic traps (two-child problem, prosecutor's fallacy, P(A|B) vs P(B|A)). | ⬜ Not started | — | — | — |
| Estimate pi by random sampling, build a general Monte-Carlo mean estimator, quantify the 1/sqrt(n) error law, and price a multi-step bet that has no easy closed form — the precursor to the track's Monte-Carlo capstone. | ⬜ Not started | — | — | — |
| Build PMF and mean/variance functions for Bernoulli, binomial, geometric, and Poisson distributions, simulate each, and learn to recognize which distribution a real scenario follows by its defining question. | ⬜ Not started | — | — | — |
| Build and play a simplified market-making game — quoting bid/ask around a noisy fair value, marking trades to the truth, and simulating thousands of rounds to see edge and variance together — fusing EV, variance, and Bayesian updating into the quant-trader interview in miniature. | ⬜ Not started | — | — | — |
| Build a Bayes calculator and the famous medical-test false-positive paradox, verify it by simulating a million-person population, and implement sequential belief updating where each posterior becomes the next prior. | ⬜ Not started | — | — | — |

## Statistics & Distributions

| Project | Score | Understanding | Reviewed | Feedback |
|---|---|---|---|---|
| Demonstrate empirically that the distribution of sample means becomes normal regardless of the (even strongly skewed) source distribution, measure the skewness collapsing as sample size grows, and verify the sigma/sqrt(n) standard error. | ⬜ Not started | — | — | — |
| Compute covariance, the Pearson correlation coefficient, and a least-squares regression line from the formulas, predict from the line, measure fit with R^2, and reason carefully about correlation vs causation — the gateway to machine learning. | ⬜ Not started | — | — | — |
| Build the normal PDF, z-scores, the 68-95-99.7 empirical rule, and an exact CDF via math.erf, then confirm the rule by sampling — learning the bell curve that describes errors, scores, and (approximately) returns. | ⬜ Not started | — | — | — |
| Build confidence intervals from the standard-error formula and from the bootstrap (resampling with replacement), verify by simulation that a 95% interval covers the truth ~95% of the time, and state the correct interpretation. | ⬜ Not started | — | — | — |
| Build an end-to-end A/B test analyzer that reports effect size (absolute and relative lift), a confidence interval for the difference, and a permutation p-value, plus a required-sample-size estimator — fusing the whole statistics phase into one ship/no-ship decision. | ⬜ Not started | — | — | — |
| Build a permutation test that estimates a p-value by shuffling group labels, make and state a significance decision precisely, and demonstrate p-hacking on pure noise to understand false positives and the correct meaning of a p-value. | ⬜ Not started | — | — | — |
| Build a statistics summary tool (mean, median, mode, variance, quartiles, five-number summary, IQR outlier detection) and learn when each measure of center and spread is the honest one to report. | ⬜ Not started | — | — | — |
| Estimate a population mean and proportion from random samples, quantify the uncertainty with standard error and a 95% margin of error, and demonstrate why biased sampling produces persistently wrong estimates that more data can't fix. | ⬜ Not started | — | — | — |

## Linear Algebra

| Project | Score | Understanding | Reviewed | Feedback |
|---|---|---|---|---|
| Build vectors and their core operations (add, subtract, scale, magnitude, normalize) from scratch, holding both the list view and the geometric arrow view, and reason about vectors in any dimension — the first brick of the track's mini-library capstone. | ⬜ Not started | — | — | — |
| Implement general matrix multiplication with the shape-compatibility rule, verify against the identity and hand computation, and understand it as composition of transformations (AB != BA) with O(n^3) cost — the operation GPUs and AI chips exist to accelerate. | ⬜ Not started | — | — | — |
| Package the phase into a reusable Vector/Matrix library with operator overloading (+, *, @), validate every operation against NumPy with a pytest suite, and measure why NumPy is 100x+ faster despite identical Big-O — a portfolio artifact and a direct capstone component. | ⬜ Not started | — | — | — |
| Build a linear-system solver using Gaussian elimination with partial pivoting and back substitution, solve 2x2 and 3x3 systems, verify by substitution, and recognize the no-solution / infinite-solution cases geometrically. | ⬜ Not started | — | — | — |
| Represent matrices as lists of rows and build shape, add, scale, transpose, identity, and matrix-vector product, while learning the three interpretations of a matrix (data table, equation system, transformation). | ⬜ Not started | — | — | — |
| Interpret matrices as functions that transform space — build scaling, rotation, shear, and reflection matrices, discover that a matrix's columns are the transformed basis vectors, compose transforms, and use the determinant as an area-scaling factor. | ⬜ Not started | — | — | — |
| Build the dot product and use it to compute angles, detect orthogonality, rank vectors by cosine similarity (as search/recommenders do), and project one vector onto another — connecting the algebraic and geometric definitions. | ⬜ Not started | — | — | — |
| Test eigenvectors against Av=lambda*v, find 2x2 eigenvalues from the characteristic equation, and implement power iteration (the algorithm behind PageRank) to find the dominant eigenvector — connecting to PCA, PageRank, and stability. | ⬜ Not started | — | — | — |

## Calculus & Optimization for Systems

| Project | Score | Understanding | Reviewed | Feedback |
|---|---|---|---|---|
| Fit a line to data by gradient descent, fusing a model (y=mx+b), a loss (MSE), and an optimizer into machine learning's hello world — derive the loss gradient, train on clean and noisy data, recover the true parameters, and cross-check against the closed-form solution. | ⬜ Not started | — | — | — |
| Build a numerical limit estimator that probes a function from both sides of a point, see that a limit can exist where the function is undefined (sin(x)/x at 0), detect discontinuities, and test continuity — the conceptual gateway to derivatives. | ⬜ Not started | — | — | — |
| The math-foundations capstone: assemble Monte Carlo, statistics, the linear-algebra mini-library, and gradient descent into one tested Python package (mathkit), with every component validated against a known closed-form answer and documented in `work/README.md`. | ⬜ Not started | — | — | — |
| Implement gradient descent to minimize functions, watch the loss decrease step by step, sweep learning rates to see convergence vs divergence, and demonstrate local-vs-global minima — the algorithm that trains nearly every ML model. | ⬜ Not started | — | — | — |
| Implement and verify the power, product, quotient, and chain rules against numerical derivatives, and understand the chain rule as the mathematical core of backpropagation in neural networks. | ⬜ Not started | — | — | — |
| Compute partial derivatives (one variable at a time), assemble them into the gradient vector, and verify empirically that the gradient points in the direction of steepest ascent — the compass that gradient descent follows. | ⬜ Not started | — | — | — |
| Find optima analytically by locating critical points and classifying them with the second-derivative test, define and test convexity, and understand why convexity guarantees gradient descent finds the global minimum. | ⬜ Not started | — | — | — |
| Build numerical derivatives (forward and central difference), verify them against exact derivatives, interpret the derivative as slope/rate/sensitivity, and locate flat (zero-slope) critical points — the quantity gradient descent follows. | ⬜ Not started | — | — | — |

---
*Machine-readable proof with commit SHA anchors: [verified-record.json](./verified-record.json)*