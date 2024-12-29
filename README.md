# OpenGL Template Project

A OpenGL template project using GLFW and GLAD, configured with CMake. This template provides the basic setup needed to start developing OpenGL applications.

## Features

- Modern OpenGL setup with GLFW 3.4
- GLAD for OpenGL function loading
- CMake build system
- C++17 support
- Shader support

## Prerequisites

- CMake (version 3.10 or higher)
- C++17 compatible compiler
- OpenGL compatible graphics driver

### System-specific Requirements

#### Linux
```bash
sudo apt-get update
sudo apt-get install build-essential
sudo apt-get install libgl1-mesa-dev
sudo apt-get install cmake 
```

## Building the Project

1. Create and navigate to the build directory

```bash
mkdir build
cd build
```

3. Generate build files with CMake
```bash
cmake ..
```

4. Build the project
```bash
make
```

Or use the provided script:
```bash
./clean_cmake_build.sh
```

## Usage

After building, run the executable from the build directory:
```bash
./OpenGLTemplate
```