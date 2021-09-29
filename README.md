# CMake Action

[![build-and-test](https://github.com/Jaybro/action-cmake/workflows/build-and-test/badge.svg)](https://github.com/Jaybro/action-cmake/actions?query=workflow%3Abuild-and-test)

This basic action simplifies integration of [CMake](https://cmake.org/) into a [workflow](https://docs.github.com/en/actions/learn-github-actions/workflow-syntax-for-github-actions).

# Usage

```yaml
- uses: Jaybro/action-cmake
  with:
    # Path to the root directory of the CMake project to build.
    # Default: ${{ github.workspace }}. This default is also used by @actions/checkout@v2.
    cmake-source-dir: ''

    # Path to the directory which CMake will use as the root of the build directory.
    # Default: ${{ github.workspace }}/build
    cmake-build-dir: ''

    # Path to the directory which CMake will use as the root of the install directory.
    # Overrides the installation prefix, CMAKE_INSTALL_PREFIX.
    # Default: ${{ github.workspace }}/install
    cmake-install-dir: ''

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

The following example shows how to build and test a repository that was cloned using [actions/checkout@v2](https://github.com/actions/checkout):

```yaml
- name: Checkout
  uses: actions/checkout@v2

- name: CMake build and test
  uses: Jaybro/action-cmake
  with:
    cmake-ctest: true
```
