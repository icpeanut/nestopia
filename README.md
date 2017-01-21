This project is a fork of the original Nestopia source code, plus the 
Linux port. The purpose of the project is to enhance the original, and
ensure it continues to work on modern operating systems.

The following platforms are supported:
* Linux, FreeBSD, OpenBSD, NetBSD, OS X, Windows
* Anything supported by libretro

## Building with CMake
In order to build with CMake:
```
mkdir BUILD
cd BUILD
cmake -DCMAKE_INSTALL_PREFIX=<INSTALLATION PREFIX> ..
make -j<NUMBER OF CORES>
```
and optionally:
```
make install
```
The CMake build system can also be used with Ninja by adding `-GNinja` to the `cmake` line.

## Building with Autotools
In order to build with Autotools:
```
mkdir BUILD
cd BUILD
../configure --prefix=<INSTALLATION PREFIX>
make -j<NUMBER OF CORES>
```
and optionally:
```
make install
```

in order to bootstrap the Autotools you will need

1.  **Autoconf**; latest 2.69 release (http://www.gnu.org/software/autoconf/)

    GNU Autoconf produces the ./configure script from configure.ac.

2.  **Automake**; latest 1.15 release (http://www.gnu.org/software/automake/)

    GNU Automake produces the Makefile.in precursor, that is processed with ./configure to yield the final Makefile.

3.  **Autoconf Archive**; latest 2016.09.16 release (http://www.gnu.org/software/autoconf-archive/)

    The configure.ac requires a number of m4 macros from the Autoconf archive.

