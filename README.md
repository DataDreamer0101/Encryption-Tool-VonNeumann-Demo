# Multi-Cipher Encryption/Decryption Tool – Von Neumann Bottleneck Demo

**CS-226 Computer Organization & Assembly Language | Track B (Assembly Application)**

## Overview
This project implements an encryption/decryption tool in **x86 inline assembly** to demonstrate the Von Neumann bottleneck. It compares two key-placement strategies:
- **Memory‑resident key** (bottleneck) – key fetched from memory every byte.
- **Register‑resident key** (optimised) – key kept in `EBX` register.

The tool supports two ciphers (XOR and Add‑Key), text encryption/decryption with hex output, and binary file encryption/decryption for any file type (JPEG, PDF, EXE, etc.).

## Key Features
- Pure x86 inline assembly for all encryption, decryption, hex conversion, and console I/O.
- C++ used only for file I/O and the outer menu.
- Performance test using `RDTSC` with `CPUID` serialisation (10 MB buffer).
- Measured speedup: **1.36×** (register‑key vs memory‑key).
