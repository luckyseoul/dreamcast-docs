# SH7750 technical updates

Hitachi / Renesas notes that name **HD6417750** or **SH7750** (the Dreamcast CPU). They correct the SH7750 hardware manual already in `../DOCS/`. Sheets whose product line is only SH7750R, SH7751, SH-4A, or SH-5 stay in the Kochise tree on disk, with the RTOS and emulator notes.

| File | What it corrects |
|------|------------------|
| `e602124_tech.pdf` | TN-SH7-202A/E (2000-02-01). On the QFP, the VSS pins are not bonded together inside the package. |
| `esh7750_tech.pdf` | TN-SH7-246A/E (2000-08-23). Figure 23.13 bus-request timing. HD6417750 and HD6417750S. |
| `esh7751_tech.pdf` | TN-SH7-247A/E (2000-08-23). Pull each SH7750 reserved pin up to 3.3 V on its own resistor. The CA-pin sentence is for SH7750S and SH7751. |
| `tnsh7203ae.pdf` | TN-SH7-203A/E (2000-02-01). Store-queue instructions cannot be cancelled. HD6417750. |
| `tnsh7224ae.pdf` | BSC WCR1 usage. HD6417750. |
| `tnsh7250ae.pdf` | BSREQ# in partial-sharing master mode. SH7750 and SH7750S. |
| `tnsh7272ae.pdf` | TN-SH7-272A/E (2001-01-25). SCI multiprocessor receive bug. HD6417750. |
| `tnsh7298ae.pdf` | NMI usage. SH7750, SH7750S, SH7751. |
| `tnsh7342ae.pdf` | Writing the ASID field of PTEH, and the instruction fetches that follow. |
| `tnsh7347ae.pdf` | Address-space identifier in single virtual memory mode. SH7750. |
| `tnsh7349ae.pdf` | Initial value of the bypass register. HD6417750. |
| `tnsh7361be.pdf` | TN-SH7-361B/E. SH-4 version register, including the SH7750 value. |
| `tnsh7372ae.pdf` | TN-SH7-372A/E (2001-11-05). CKIO wiring to synchronous DRAM. SH7750 and SH7750S. |
| `tnsh7395ae.pdf` | TN-SH7-395A/E (2002-02-04). CKIO wiring guide. SH7750. |
| `tnsh7448ae.pdf` | FPU instruction issues. SH7750. |
| `tnsh7455ae.pdf` | Consumption current. SH7750. |
| `tnsh7456ae.pdf` | TRAPA, SLEEP, and undefined opcode H'FFFD. SH7750. |
| `tnsh7465ae.pdf` | Pin-function corrections. |
| `tnsh7472ae.pdf` | Package dimensions for SH7750 and SH7751. |
| `tnsh7475ae.pdf` | Overflow flag on FIPR and FTRV. SH7750. |
| `tnsh7476ae.pdf` | Sign of the FIPR and FTRV result. SH7750. |
| `tnsh7478ae.pdf` | SH7750 electrical characteristic tSTD. |
| `tnsh7517aea.pdf` | TN-SH7-517A/EA (2004-03-22). Double-precision FADD and FSUB rounding. Every SH-4, including SH7750. |
| `tnsh7518aea.pdf` | TN-SH7-518A/EA (2004-03-22). Watchdog timer. SH7750. |
| `tnsh7528aea.pdf` | TN-SH7-528A/EA (2004-08-02). SH7750 series revision notice. |
