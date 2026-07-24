# AICA Sound Processor

Yamaha AICA (FQ8005) with integrated ARM7DI core.

## Local Docs
- Community notes: [`files/aica/aica.txt`](../files/aica/aica.txt), [`files/aica/aica_v08.txt`](../files/aica/aica_v08.txt)
- ARM7TDMI technical reference manuals (core used by AICA): all PDFs in [`files/aica/`](../files/aica/)
- System context: [Hardware Outline](../files/official/Dreamcast_Hardware_Specification_Outline.pdf), [Dev.Box Architecture](../files/official/DreamcastDevBoxSystemArchitecture.pdf)

## Specs
- 64 channels PCM/ADPCM/FM
- DSP, mixer, DAC interface
- 2 MB wave memory (expandable)
- RTC (battery backed)
- G2 bus interface to HOLLY
- ARM7 for driver execution (~2.8 MHz effective clock domain)
