---
layout: default
---

## Tricore GCC

URL: [github.com/NoMore201/tricore-gcc-toolchain-11.3.0](https://github.com/NoMore201/tricore-gcc-toolchain-11.3.0)

This is a fork of the original
[EEESlab/tricore-gcc-toolchain-11.3.0](https://github.com/EEESlab/tricore-gcc-toolchain-11.3.0). Since authors seems to be inactive, I decided
to create a fork to push some changes and a Github Action pipeline that builds
compiler distributables.

Current goal is to try to gather some interest around the project to implement
new features and fix existing bugs. Eventually switch back to the original
repository if authors are again interested in it.

You can find a link to latest release on the top of page.

Features:

- Compiler based on mainstream GCC 11.3.1 with applied TriCore specific patches
- Binutils based on version 2.40
- libc based on Cygwin newlib version 4.3.0
