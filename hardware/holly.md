# HOLLY / PowerVR2 Graphics

HOLLY ASIC (NEC/VLSI) integrates PowerVR Series 2 (CLX2) core @ 100 MHz + system interfaces.

## Local Docs
- [Hardware Specification Outline](../files/official/Dreamcast_Hardware_Specification_Outline.pdf) — Image Drawing Processor sections
- [Dev.Box System Architecture](../files/official/DreamcastDevBoxSystemArchitecture.pdf) — registers, TA, PVR, buses
- PowerVR notes directory: [`files/powervr/`](../files/powervr/)
  - e.g. [`dreamcast_portal_techniques.pdf`](../files/powervr/dreamcast_portal_techniques.pdf), [`dcgfx.pdf`](../files/powervr/dcgfx.pdf), [`dc-video.pdf`](../files/powervr/dc-video.pdf)
- Offline RE: [`files/mcpp/pvr.html`](../files/mcpp/pvr.html)

## Key Features
- Tile-based deferred rendering
- Texture memory 8 MB (expandable), 64-bit bus
- G1/G2/Maple interfaces
- Video output (RGB, NTSC/PAL/VGA modes)
- TA (Tile Accelerator) for display list processing from SH-4 DMA
