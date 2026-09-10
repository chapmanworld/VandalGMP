# VandalGMP

**VandalGMP** is a pinned import of the [GNU GMP](https://gmplib.org/) arbitrary-precision arithmetic library, used as a build-time dependency of GDB in the **VandalSDK** toolchain (see `VandalBinUtils`).

This is **not Vandal-authored code**. It is an import of an existing, independently maintained open-source project, taken here purely so that a specific, known-good version can be built reproducibly as part of the VandalSDK toolchain used by the **Vandalism Engine** game engine.

## Baseline

See `VANDALGMP_BASELINE.txt` for the exact upstream version, source tarball, and checksum this import was taken from, and for why this repository is a tarball snapshot rather than a live git fork (GMP's official upstream is Mercurial-only, and this project's forks otherwise track git upstreams directly).

## Why this repository exists

VandalSDK's packaged debugger (GDB) links against GMP for arbitrary-precision arithmetic support, and GMP is itself a build dependency of MPC, MPFR, and ISL (`VandalMPC`, `VandalMPFR`, `VandalISL`). Pinning a specific GMP release as its own repository gives the SDK toolchain build a reproducible, independently versioned source for each GDB dependency, separate from upstream's own release cadence.

This repository exists for internal use while building Vandalism Engine and its SDK. It is not a general-purpose GMP distribution.

## Contributions and issue tracking

This is **not a maintained fork**. ChapmanWorld is not accepting contributions here, and this repository is not the place to raise issues, ask questions, or request features.

* Please do not use this repository as a GMP support forum.
* Please do not raise issues here for upstream GMP bugs.
* Please do not use this repository to report Vandal Engine or VandalSDK bugs.
* Issues with GMP itself should be raised with the upstream GMP project.

## Licensing

GMP is dual-licensed under the **GNU Lesser General Public License (LGPL) version 3 or later**, or the **GNU General Public License (GPL) version 2 or later**, at your option. See `COPYING`, `COPYING.LESSERv3`, `COPYINGv2`, and `COPYINGv3` in this repository for the authoritative upstream license terms.

## Status

Toolchain dependency import. Tracks a single pinned upstream release tarball for VandalSDK build reproducibility.
