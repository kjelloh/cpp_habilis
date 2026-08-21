# cpp_habilis
The able cpp. The 'tool using' C++. A basis for a CLI tool that composes existing tools into tooling for C++ development.

* [thinking](thinking.md)
* [chimes](../chime/index.md)

## Build

This project uses CMake and requires a C++ compiler.

* generate: CMakeLists.txt -> Build (Make) Configuration.

```sh
  cmake -S . -B build
```

* build: Build (Make) Configuration -> target(s)

```sh
cmake --build build
```


* Run target cpp_habilis

```sh
./build/cpp_habilis --help
```
