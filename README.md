# OpenGL Template

Minimal OpenGL starter using GLFW + GLAD + GLM (CMake + submodules).

## Build
After cloning `cd` into the project directory:

```sh
git submodule update --init --recursive --depth 1
cmake -S . -B build
cmake --build build
```
