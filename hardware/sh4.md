# SH-4 CPU

Hitachi SuperH SH-4 (SH7091 variant in Dreamcast) @ 200 MHz.

## Local Official Manuals
- Programming Manual: [`files/sh4/h14tp003d2.pdf`](../files/sh4/h14tp003d2.pdf)
- Hardware Manual: [`files/sh4/h14th002d2.pdf`](../files/sh4/h14th002d2.pdf)
- Product Overview: [`files/sh4/h14sf001d2.pdf`](../files/sh4/h14sf001d2.pdf)

Offline RE notes: [`files/mcpp/cpu.html`](../files/mcpp/cpu.html)

## Key Specs (from Hardware Outline)
- 32-bit RISC, superscalar, 5-stage pipeline
- FPU (IEEE754), 360 MIPS / 1.4 GFLOPS
- Caches: 8 KB instruction, 16 KB operand (base)
- MMU, 4-channel DMAC, SCI, etc.
- External bus 100 MHz, little-endian in Dreamcast config

See also [Dev.Box System Architecture](../files/official/DreamcastDevBoxSystemArchitecture.pdf) for integration details and memory mapping.
