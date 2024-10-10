---
layout: default
---

- [Tricore GCC](#tricore-gcc)
  - [Release artifacts](#release-artifacts)
  - [Example projects](#example-projects)
    - [aurix-cmake-code-sample](#aurix-cmake-code-sample)
    - [Zephyr RTOS Tricore experimental patch](#zephyr-rtos-tricore-experimental-patch)
- [QEMU](#qemu)

# Tricore GCC

- [EEESlab/tricore-gcc-toolchain-11.3.0](https://github.com/EEESlab/tricore-gcc-toolchain-11.3.0)

Tricore compiler based on GCC 11.3 source code. Features:

- Compiler based on mainstream GCC 11.3.1 with applied TriCore specific patches
- Binutils based on version 2.40
- libc based on Cygwin newlib version 4.3.0

Win32 and Linux binaries are available from
[NoMore201/tricore-gcc-toolchain](https://github.com/NoMore201/tricore-gcc-toolchain),
built from Github Action CI including latest patches from main EEESlab repositories.

- Latest release: [NoMore201/tricore-gcc-toolchain/releases](https://github.com/NoMore201/tricore-gcc-toolchain/releases/latest)
- Build pipeline: [build.yml](https://github.com/NoMore201/tricore-gcc-toolchain/blob/main/.github/workflows/build.yml)

## Example projects

Here are some example projects making use of the open source compiler.

### aurix-cmake-code-sample

- [NoMore201/aurix-cmake-code-sample](https://github.com/NoMore201/aurix-cmake-code-sample)

This repository hosts the Blinky_LED_1_KIT_TC334_L sample from
[Infineon/AURIX_code_examples](https://github.com/Infineon/AURIX_code_examples)
repository, converted to make use of CMake as build system. It also provides
configuration for CMake presets, clang-tidy, clang-format and custom compiler
CLion config.

### Zephyr RTOS Tricore experimental patch

URL: [go2sh/zephyr](https://github.com/go2sh/zephyr/tree/tricore).

Zephyr RTOS fork with experimental support for Tricore architecture.
For information on how to build it, refer to project documentation and
[this discussion](https://github.com/zephyrproject-rtos/zephyr/discussions/68826#discussioncomment-9296297).

# QEMU

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
