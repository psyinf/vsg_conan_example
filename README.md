# vsg_conan_example

This is a minimal example for creating a simple [VulkanSceneGraph](https://VulkanSceneGraph.org) project using [Conan](https://conan.io).

## Requirements
* [Python 3.x](https://python.org)
* [Conan](https://conan.io) can be installed via: `pip install --user conan==1.60.0
**  conan 2.x.x is currently not in the scope`

## Build
```
git clone https://github.com/psyinf/vsg_conan_example.git
cd vsg_conan_example
mkdir build
cd build
cmake .. --DCMAKE_BUILD_TYPE=Release
cmake --build .
```
The CMake configure step should download all dependencies either as binary or as source code and start to build them. 

## Caveats
* currently only vsg 1.0.5 is supported (due to pending PRs in the conan-center)
