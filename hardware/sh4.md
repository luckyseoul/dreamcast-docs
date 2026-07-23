# SH-4 CPU

Hitachi SuperH SH-4 (SH7091 variant in Dreamcast) @ 200 MHz.

## Official Manuals
- Programming Manual: http://mc.pp.se/dc/files/h14tp003d2.pdf
- Hardware Manual: http://mc.pp.se/dc/files/h14th002d2.pdf
- Product Overview: http://mc.pp.se/dc/files/h14sf001d2.pdf

Additional Renesas SH7750 series hardware manuals available on Renesas site (search SH7750).

## Key Specs (from Hardware Outline)
- 32-bit RISC, superscalar, 5-stage pipeline
- FPU (IEEE754), 360 MIPS / 1.4 GFLOPS
- Caches: 8 KB instruction, 16 KB operand (base)
- MMU, 4-channel DMAC, SCI, etc.
- External bus 100 MHz, little-endian in Dreamcast config

See also Dev.Box System Architecture for integration details and memory mapping.
