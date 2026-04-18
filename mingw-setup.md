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

For example:
