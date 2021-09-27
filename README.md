# CMake Action

[![build-and-test](https://github.com/Jaybro/action-cmake/workflows/build-and-test/badge.svg)](https://github.com/Jaybro/pico_tree/actions?query=workflow%3Abuild-and-test)

Basic action for using [CMake](https://cmake.org/) in your workflows.

# Usage

```yaml
- uses: Jaybro/action-cmake
  with:
    # Path to the top level of the source tree (aka root cmake directory).
    # Default: ${{ github.workspace }}. This default is also used by @actions/checkout.
    cmake-source-dir: ''
```
