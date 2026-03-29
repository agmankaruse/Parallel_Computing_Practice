# Parallel Computing Overview

## What Is Parallel Computing?

Traditionally, software has been written for serial, or sequential, execution. Problems are broken into a discrete series of instructions, and those instructions are executed one after another. These instructions are typically executed on a single processor, one at a time.

Although this works, improving performance is always a major goal in computing. First, it is important to understand the difference between concurrency and parallelism.

**Concurrency:** The ability to handle multiple tasks at the same time, even if they are not executing simultaneously.

**Parallelism:** The execution of multiple tasks at the exact same time.

A program can be concurrent but not parallel. For example, on a single-core processor, multiple tasks can make progress through time-sharing rather than true simultaneous execution.

A parallel program is one that uses multiple computing resources simultaneously to solve a problem. A problem is broken into discrete parts that can be solved concurrently. Each of those parts is then broken down into a series of instructions that execute on its own individual processor.

### Serial Computing

    +------------------+
    |     problem      |
    +------------------+
              |
              v
    [tN][tN-1][tN-2][tN-3] ... [t3][t2][t1] --> [processor]

### Parallel Computing

    +------------------+
    |     problem      |
    +------------------+
    |      part 1      | --> [tN][tN-1][tN-2][tN-3] ... [t3][t2][t1] --> [processor 1]
    |      part 2      | --> [tN][tN-1][tN-2][tN-3] ... [t3][t2][t1] --> [processor 2]
    |      part 3      | --> [tN][tN-1][tN-2][tN-3] ... [t3][t2][t1] --> [processor 3]
    |      part 4      | --> [tN][tN-1][tN-2][tN-3] ... [t3][t2][t1] --> [processor 4]
    +------------------+

## Why Use Parallel Computing?

From an HPC perspective, the real world is incredibly complex. Many interrelated events happen at the same time, even though they still occur within a temporal sequence. This makes parallel computing especially useful for modeling, simulating, and understanding real-world systems, especially in AI and scientific computing.

From a more practical perspective, shortening the time needed to complete certain tasks can lead to cost savings. Parallel computing also allows us to use computing resources across a wide-area network when local resources are not sufficient. In addition, given how advanced modern hardware is, running programs strictly sequentially can waste available computing power.
