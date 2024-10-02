---
layout: default
---

- [Tricore GCC](#tricore-gcc)
- [QEMU](#qemu)

## Tricore GCC

URL: [EEESlab/tricore-gcc-toolchain-11.3.0](https://github.com/EEESlab/tricore-gcc-toolchain-11.3.0)

Tricore compiler based on GCC 11.3 source code. Features:

- Compiler based on mainstream GCC 11.3.1 with applied TriCore specific patches
- Binutils based on version 2.40
- libc based on Cygwin newlib version 4.3.0

You can build it manually following build instruction or download release
archive coming from my fork at the top of the page, compiled through
Github Actions pipelines
[NoMore201/tricore-gcc-toolchain](https://github.com/NoMore201/tricore-gcc-toolchain).
This change is awaiting PR review in the main repository.

## QEMU

URL: [https://gitlab.com/qemu-project/qemu](https://gitlab.com/qemu-project/qemu)

QEMU implements basic CPU decode capabilities for Tricore architecture. CPU
Support is incomplete (for example, interrupts are not implemented) and provides
support for the following Core Architecture versions:

- 1.3
- 1.3.1
- 1.6
- 1.6.1
- 1.6.2

Hardware support
([link](https://gitlab.com/qemu-project/qemu/-/tree/master/hw/tricore?ref_type=heads))
is basically absent; a few machines with basic CPU functionality are implemented.

Tricore emulation is usually not present in pre-compiled packages: you need
to compile it yourself by providing the option `--target-list=tricore-softmmu`.

You can find more info on
[this GIST](https://gist.github.com/bri3d/5429c0b25346a0830c01042e77d6914c).
