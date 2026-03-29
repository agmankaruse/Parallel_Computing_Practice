# Parallel Computing Overview

## What Is Parallel Computing?
Traditionally, software has been written for serial / sequential instructions. Problems are broken into a discrete series of instructions, and those instructions are executed sequentially. These instructions are executed on a single processor one at a time. 

Although this works, in computing, improving performance is always a goal. First lets understand concurrency and parallelism definitionally. 

Concurrency: The ability to handle multiple tasks at the same time (one task doesn't rely on the other. 

Parallelism: Executing multiple tasks at the same instance of time. 

A program can be concurrent but not parallel by running on a single core processor, using time sharing. 

A parallel program is one that uses multiple compute resources simultaneously to solve a problem. A problem is broken into discrete parts that can be solved concurrently. Then, each of those parts are broken down into a series of instructions that execute on their own individual processor. 

Serial Computing: 

+------------------+
|     problem      |
+------------------+
          |
          v
[tN][tN-1][tN-2][tN-3] ... [t3][t2][t1] --> [processor]

Parallel Computing: 

+------------------+
|     problem      |
+------------------+
|      part 1      | --> [tN][tN-1][tN-2][tN-3] ... [t3][t2][t1] --> [processor 1]
|      part 2      | --> [tN][tN-1][tN-2][tN-3] ... [t3][t2][t1] --> [processor 2]
|      part 3      | --> [tN][tN-1][tN-2][tN-3] ... [t3][t2][t1] --> [processor 3]
|      part 4      | --> [tN][tN-1][tN-2][tN-3] ... [t3][t2][t1] --> [processor 4]
+------------------+

## Why Use Parallel Computing?
From an HPC perspective, we need to consider that the real world is incredibly complex. Many, interrelated events are happening at the same time, however, they occur inside a temporal sequenence. This makes parallel computing especially advantageous for modeling, simulating and understanding the real world (especially from an AI perspective)

From a more practical perspective, shortening the time to completion of certian tasks can lead to potential cost savings. Parallel computing allows us to use compute resources on a wide area network when local resources aren't sufficient enough! Further, with how advanced today's hardware is, running programs sequentially can be a "waste" of potential computing power. 
