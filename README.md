## SIS - Simple Instruction Simulator

SIS is a SPARC V8 and RISC-V RV32IMACFD architecture simulator.
It consist of three main parts: 

* an event-based simulator core

* a processor (SPARC/RISCV) emulation module 

* system memory and peripheral modules.

SIS can emulate six specific systems:

* ERC32 SPARC V7 processor

* LEON2 SPARC V8 processor

* LEON3 SPARC V8 processor

* RISC-V (RV32IMACFD) processor with GRLIB peripherals

* RISC-V (RV32IMACFD) processor with CLINT and ns16550 UART

### Multi-propcessing

The LEON3/4 and RISC-V emulation supports SMP with up to four processor cores.

### Networking support

SIS supports the emulation of the GRLIB/GRETH 10/100 Mbit network interface, for leon3 and RISC-V targets. The network interface creates a tun/tap interface on the host, through which ethernet packets can be sent and received.

### Installation

SIS uses the GNU autoconf system, and can be build using:

  ```shell
    ./configure 
  ```

followed by 

  ```shell
  make
  ```

To build a PDF version of the manual, do

  ```shell
  make sis.pdf.
  ```

To enable emulation of an L1 cache, run configure with --enable-l1cache. This option
only improves timing accuracy, it does not affect simulation behaviour.
