# Cross compilation on Linux

## Prerequistics

-   clone and install beboo amiga-gcc https://github.com/bebbo/amiga-gcc (after installation should be at /opt/m68k-amigaos/)
-   clone amiga Cmake cross toolchain https://github.com/AmigaPorts/AmigaCMakeCrossToolchains --> ~/GitHub/AmigaPorts/AmigaCMakeCrossToolchains

## Prepare toolchain

-   $ cd /usr/share/cmake-X.XX/Modules/Platform/
-   $ sudo cp Generic.cmake AmigaOS.cmake

## Build

In root of gitlib2
-   $ mkdir build && cd build
-   $ cmake -DCMAKE_TOOLCHAIN_FILE=~/GitHub/AmigaPorts/AmigaCMakeCrossToolchains/m68k-amigaos.cmake -DM68K_CRT=clib2 ..
-   $ cmake --build .
