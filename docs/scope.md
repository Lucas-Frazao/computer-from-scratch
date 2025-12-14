# CPU Scope Definition

## Architecture Width
Chosen width: 8-bit

Rationale:
- 8-bit is sufficient to implement and understand the full instruction lifecycle (fetch/decode/execute/write-back), branching, loops, and memory operations.
- It minimizes datapath and instruction-format complexity so the focus stays on architecture fundamentals, not bit-width bookkeeping.
- Larger widths are intentionally avoided in v1 to reduce complexity and speed up correct validation in a C simulator.

## Memory Model
Chosen model: von Neumann

Rationale:
- A single unified memory is the simplest to simulate and reason about for a first CPU architecture.
- It supports the stored-program concept directly: instructions and data live in the same address space.
- Harvard is avoided in v1 because it introduces separate memory spaces and more early design decisions that do not increase learning value at this stage.


## Explicit Non-Goals
This CPU will NOT:
- Support pipelining
- Support parallel execution
- Support floating point
- Interface with real hardware
- Run an operating system

## Intended Capability
This CPU must be capable of:
- Basic arithmetic
- Conditional branching
- Sequential instruction execution
- Running simple loop-based programs

