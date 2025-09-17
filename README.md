# NPP Grayscale Converter

This project was created by **Adrian Martin Diaz**.

It aims to create a simple converter that transforms an input image (`sloth.png`) to grayscale (`slothGrey.png`) using **NVIDIA Performance Primitives (NPP)** instead of manually coding GPU kernels.

## Requirements

- CUDA Toolkit (tested with CUDA 12+)
- NPP (comes with CUDA)
- C++17 or higher compiler (g++ / clang++)
- CMake or Make for building (Makefile provided)

## How it works

1. The program loads an RGBA PNG image (`sloth.png`) into host memory.
2. The image is copied to device memory.
3. The NPP function `nppiBGRAToGray_8u_C4C1R` converts the image to grayscale.
4. The grayscale image is copied back to host memory.
5. The result is saved as `slothGrey.png`.

## Usage

1. Place your input image as `sloth.png` in the same folder as the executable.
2. Build the project using the provided `Makefile`:

```bash
make
```

Note: the output image is uploaded as a demonstration that the code runs