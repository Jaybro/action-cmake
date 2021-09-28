# CMake Action

[![build-and-test](https://github.com/Jaybro/action-cmake/workflows/build-and-test/badge.svg)](https://github.com/Jaybro/pico_tree/actions?query=workflow%3Abuild-and-test)

Basic action for using [CMake](https://cmake.org/) in your workflows.

# Usage

```yaml
- uses: Jaybro/action-cmake
  with:
    # Path to the top level of the source tree (aka cmake root directory).
    # Default: ${{ github.workspace }}. This default is also used by @actions/checkout.
    cmake-source-dir: ''

    # Path to directory where the source will be build.
    # Default: ${{ github.workspace }}/build
    cmake-build-dir: ''

    # Path to directory where the build will be installed.
    # Default: ${{ github.workspace }}/install
    cmake-install-prefix: ''

    # CMake build type. E.g.: Release.
    # Default: Release
    cmake-build-type: ''

    # CMake configure flags that can be set as -D<key>=<value>, etc.
    # Default: ''
    cmake-configure-flags: ''

    # Installs the build when set to true.
    # Default: false
    cmake-install: false

    # Tests the build using CTest when set to true.
    # Default: false
    cmake-ctest: false
```
