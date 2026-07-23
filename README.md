# Sega Dreamcast Documentation Repository

Curated collection of publicly available Sega Dreamcast engineering specs, programmer guides, manuals, reverse-engineering notes, and completed/expanded documentation.

**Primary Sources (Best Collections)**
- [SegaRetro Dreamcast official documentation](https://segaretro.org/Dreamcast_official_documentation) and direct PDFs
  - [Dreamcast Hardware Specification Outline](https://segaretro.org/images/8/8b/Dreamcast_Hardware_Specification_Outline.pdf) (~40 pages, 1999)
  - [Dreamcast/Dev.Box System Architecture](https://segaretro.org/images/7/78/DreamcastDevBoxSystemArchitecture.pdf) (407 pages, Rev 99/09/02)
- [Kochise/dreamcast-docs](https://github.com/Kochise/dreamcast-docs) - Component tree with hardware docs, SDK material, schematics
- [Marcus Comstedt Dreamcast Programming](http://mc.pp.se/dc/) - Detailed RE on SH-4, Maple bus, GD-ROM, memory map, PVR, controller protocols
- [sega-dreamcast-info.com SDK archives](https://www.sega-dreamcast-info.com/en/dreamcast-develppement-sdk-library-archive) - Multiple Katana SDK releases (0.20 Pre.7 through R9, SET2/4/5), Shinobi/Kamui sources, Windows CE Toolkit
- [Archive.org](https://archive.org) - Software Creation Standards Guidebook, consumer manuals, various SDK dumps
- [Copetti - Dreamcast Architecture](https://www.copetti.org/writings/consoles/dreamcast/) - Practical analysis with citations
- [KallistiOS / dreamcast.wiki](https://dreamcast.wiki) and [KOS docs](https://kos-docs.dreamcast.wiki/) - Homebrew SDK and community documentation
- Hitachi/Renesas SH-4 manuals (linked via mc.pp.se and Renesas product pages)
- Gamesurge / community technical pages for PowerVR Series 2 / CLX2 notes

## Official Sega Documentation

### Hardware Specifications
- Dreamcast Hardware Specification Outline (E_DC_HW_outline, ~40pp): System block diagram, SH4, HOLLY (PVR2), AICA, GD-ROM, buses (G1/G2/Maple), memory map, video modes, power/clock.
- Dreamcast/Dev.Box System Architecture (407pp): Detailed register-level architecture, bus protocols, component interactions for development kit and consumer hardware.

### Katana SDK / Development Libraries
Multiple revisions available (Japanese/English mixes):
- KATANA SDK 0.20 Pre.7, 0.40 Pre.2 / Release.4, 1.0B2
- SDK Release 8 (European), Release 9 (European and others)
- Sega Library Ver.1.00J
- Windows CE Toolkit 1.1 for Dreamcast
- Visual Memory Unit (VMU) SDK
- Shinobi library source, Kamui (graphics) library source
- Contents typically include: hardware manuals, programming guides, library references (Shinobi, Kamui), sample code, tools (compilers, graphics/sound), tech demos.

Links: see sega-dreamcast-info.com archives and Archive.org (e.g. dcsdk-9e).

### Software Standards
- Sega Dreamcast Software Creation Standards Guidebook (Archive.org: scstandards) - UI/UX, operational standards for titles.

### Component Manuals
- SH-4 / SH7750 / SH7091 Hardware Manual and Programming Manual (Hitachi)
- AICA (FQ8005) Sound-block User's Manual (AICA_E.pdf)
- Maple Bus 1.0 Peripheral Hardware Specifications (Controller, Gun, etc.)
- VMU / Visual Memory System manuals

### Other
- Service manuals (EU/US variants)
- Schematics (community/gamingdoc.org)

**Full lists and direct downloads**: SegaRetro images, Kochise tree, sega-dreamcast-info.com, mc.pp.se, Archive.org.

## Hardware

### SH-4 (Hitachi / Renesas)
- 200 MHz superscalar RISC, 360 MIPS, 1.4 GFLOPS, FPU, 8KB I-cache / 16KB D-cache (variants), MMU, DMAC.
- Manuals: Programming (h14tp003d2.pdf), Hardware (h14th002d2.pdf), Product Overview via mc.pp.se/dc/cpu.html.
- See hardware/sh4.md

### HOLLY / PowerVR2 (CLX2) Graphics
- NEC/VLSI HOLLY ASIC containing PowerVR Series 2 core @ 100 MHz.
- Tile-based deferred rendering, texture formats, TA (Tile Accelerator), PVR, video output (NTSC/PAL/VGA).
- 8 MB (expandable) texture memory.
- Documented in Hardware Outline + Dev.Box Architecture; community PowerVR notes.
- See hardware/holly.md / hardware/powervr.md

### AICA (Yamaha)
- Sound processor with ARM7DI core (~2.8 MHz effective), 64 PCM/ADPCM channels, DSP, 2 MB (expandable) wave memory, RTC.
- Connected via G2 bus.
- AICA_E.pdf + SDK docs + Kochise/AICA.
- See hardware/aica.md

### GD-ROM
- Yamaha drive, CAV 4x-12x, ~1 GB capacity (Mode 1), interface via G1 bus / HOLLY, digital audio to AICA.
- See hardware/gdrom.md and mc.pp.se/dc/gdrom.html

### Buses
- G1 bus: GD-ROM, Boot ROM, high bandwidth to HOLLY.
- G2 bus: AICA, modem, expansion (25 MHz, 16-bit).
- Maple bus: serial peripheral interface (controllers, VMU, gun, etc.), up to 2 Mbps, hierarchical addressing.
- See hardware/maple.md, hardware/g2bus.md; mc.pp.se Maple pages.

### Memory Map & Boot
- 16 MB main SDRAM (64-bit), 8 MB texture, 2 MB sound, 2 MB Boot ROM, 128 KB Flash.
- IP.BIN / boot process analogous to Saturn but GD-ROM specific.
- See hardware/memory.md, hardware/boot.md

### Peripherals
- Maple devices: Controller, Analog, VMU, Keyboard, Mouse, Gun, Modem, LAN Adapter, VGA Box, etc.
- Specs in Maple peripheral docs + community RE.

## Software & Development

### Official
- Katana SDK (Shinobi high-level, Kamui low-level graphics)
- Windows CE for Dreamcast (DirectX path)
- Software Creation Standards

### Homebrew / Modern
- KallistiOS (KOS) - primary open SDK
- DreamSDK, toolchains (gcc SH4)
- See software/kos.md, tools/

## Reverse Engineering & Undocumented

**Key Sources**
- mc.pp.se detailed protocols
- Copetti analysis
- Emulator sources (Flycast, redream, WashingtonDC, Deecy)
- SegaXtreme, dreamcast-talk, dreamcast.wiki threads
- Kochise bare-metal notes

**Known Gaps / Expanded Areas**
- Exact HOLLY/PVR register timings and undocumented features (filled by emulator RE)
- AICA DSP programming details beyond basic
- GD-ROM command set edge cases and security
- Maple device enumeration quirks
- Flash/BIOS services

See reverse-engineering/ for compiled notes.

## Tools

### Compilers & SDKs
- Official Katana / CodeWarrior / Hitachi
- Modern: gcc (KallistiOS toolchain), DreamSDK
- See tools/compilers.md

### Emulators
- Flycast, redream, etc. (source for RE validation)
- See tools/emulators.md

## Coverage Note
This repository synthesizes publicly available official PDFs (Hardware Outline, Dev.Box Architecture, SH-4 manuals, AICA, Maple, SDK volumes), community RE (Comstedt, Kochise, Copetti, emulators), and homebrew resources (KOS).

Structure mirrors saturn-docs for consistency:
- hardware/ component summaries
- official/
- software/
- tools/
- reverse-engineering/

Binary PDFs remain linked externally (size, copyright). Local MD files provide indexes, summaries, and RE expansions.

Last updated: initial catalog 2026-07-23.
