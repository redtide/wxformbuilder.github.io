---
title: "Build"
---

## Git

When downloading the source code using Git, it is important to download also
the required submodules:

```sh
git clone --recursive https://github.com/wxFormBuilder/wxFormBuilder.git
```

If the `--recursive` or `--recurse-submodules` was not used, it is possible
doing it as a separate step:

```sh
git submodule update --init --recursive
```

## Supported Configurations

When building, it is recommended to do it in a new directory:

```sh
mkdir build && cd build
```

### Linux

```sh
cmake -G"Unix Makefiles" -DCMAKE_BUILD_TYPE=Release ..
```

### macOS

```sh
cmake -G"XCode" -DCMAKE_BUILD_TYPE=Release ..
```

### MSYS2

Open `MinGW 64-bit` or `MinGW 32-bit` from the start menu.
Install tools and libraries:

- Update the MSYS2 installation with `pacman -Syu`
- Restart the shell

Install the dependencies

```sh
pacman -S ${MINGW_PACKAGE_PREFIX}-binutils
```

At present, when using MinGW with MSYS2 is not possible to use `MinGW Makefiles`
or `Unix Makefiles` generators, see this [CMake issue].

```sh
cmake -G"MSYS Makefiles" -DCMAKE_BUILD_TYPE=Release ..
```

### Windows

```sh
cmake -G"Visual Studio 16 2019" -DCMAKE_BUILD_TYPE=Release ..
```

## Build

```sh
cmake --build .
```

[CMake issue]: https://gitlab.kitware.com/cmake/cmake/-/issues/18058
