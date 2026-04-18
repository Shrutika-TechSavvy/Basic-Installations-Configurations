# Setting up C Compiler on Windows using MSYS2 and MinGW

This document explains how to install and configure a C compiler on a Windows system using MSYS2 and MinGW-w64. It also covers the basic concepts required to understand the setup.

---

## 1. Introduction

To compile C programs on Windows and generate executable (`.exe`) files, we need a compiler toolchain. Unlike Linux, Windows does not come with a built-in C compiler, so we need to install one manually.

In this setup, we use:
- MSYS2 (environment and package manager)
- MinGW-w64 (toolchain)
- GCC (compiler)

---

## 2. What is MSYS2?

MSYS2 is a software distribution that provides a Unix-like environment on Windows. It includes a package manager called `pacman`, which allows easy installation of development tools.

Instead of manually downloading and configuring compilers, MSYS2 simplifies the process by managing dependencies and updates.

---

## 3. What is MinGW-w64?

MinGW-w64 is a compiler toolchain for Windows. It allows us to compile C and C++ programs into native Windows executables.

It works together with GCC and provides the required headers and libraries for Windows development.

---

## 4. What is GCC?

GCC (GNU Compiler Collection) is the compiler used to convert C source code into machine code.

For example:gcc hello.c -o hello.exe

This command compiles the file `hello.c` and produces a Windows executable named `hello.exe`.

---

## 5. What is pacman?

`pacman` is the package manager used in MSYS2. It is responsible for installing, updating, and managing software packages.

Example:pacman -S mingw-w64-x86_64-gcc

- `-S` means install
- `mingw-w64-x86_64-gcc` is the GCC package for 64-bit systems

---

## 6. Installation Steps

### Step 1: Download MSYS2

Go to:
https://www.msys2.org/

Download the installer and install it using default settings.

The default installation directory is:C:\msys64

---

### Step 2: Open the MSYS2 MinGW64 Terminal

After installation, open the terminal named:MSYS2 MinGW64

This environment is configured for building Windows applications.

---

### Step 3: Install GCC

In the MSYS2 terminal, run:pacman -S mingw-w64-x86_64-gcc

When prompted, type `Y` and press Enter.

This will install the GCC compiler along with necessary libraries.

---

### Step 4: Add GCC to Environment Variables

Windows needs to know where the compiler is located. This is done using the PATH environment variable.

Steps:
1. Open the Start menu and search for "Environment Variables"
2. Click on "Edit the system environment variables"
3. Click on "Environment Variables"
4. Under "System variables", find and select `Path`
5. Click "Edit"
6. Click "New" and add:C:\msys64\mingw64\bin
7. Click OK to save

---

### Step 5: Verify Installation

Open a new terminal (Command Prompt or PowerShell) and run:gcc --version

If GCC is installed correctly, it will display the version information.

---

### Step 6: Compile a Simple C Program

Create a file named `hello.c`:

```c
#include <stdio.h>

int main() {
    printf("Hello World\n");
    return 0;
}
```
Compile the program:

gcc hello.c -o hello.exe

After compilation, a file named hello.exe will be generated.
