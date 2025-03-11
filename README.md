# Turbo Lox

Yet another implementation of clox from the [Crafting Interpreters](http://www.craftinginterpreters.com/) book.

## How to run

Open the project file in Xcode.

## Additions

- Some new binary operators - modulo (%), bitwise and (&) and shift bits right (>>).
- Some new native maths functions - sqrt() and floor().
- Direct threaded interpreter

## Benchmarks

There's a bunch of benchmarks in the `benchmarks` folder. See the README in the folder for more information.

Timings from [hyperfine](https://github.com/sharkdp/hyperfine) using the command: `hyperfine --runs 16 --warmup 3 './clox <benchmark>'`.

### Binary trees

| Variant | Mean [ms] | Min [ms] | Max [ms] | Relative |
|:---|---:|---:|---:|---:|
| book | 321.5 ± 3.2 | 316.9 | 326.9 | 1.00 |
| direct threaded interpreter | 284.1 ± 4.1 | 279.6 | 293.3 | 1.00 |

### Method call

| Variant | Mean [ms] | Min [ms] | Max [ms] | Relative |
|:---|---:|---:|---:|---:|
| book | 174.8 ± 2.9 | 171.1 | 180.6 | 1.00 |
| direct threaded interpreter | 168.9 ± 2.4 | 165.3 | 175.1 | 1.00 |

### nfib

| Variant | Mean [ms] | Min [ms] | Max [ms] | Relative |
|:---|---:|---:|---:|---:|
| book | 36.9 ± 1.6 | 34.9 | 41.0 | 1.00 |
| direct threaded interpreter | 29.5 ± 0.8 | 28.0 | 31.1 | 1.00 |
