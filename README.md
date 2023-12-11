# Caravel User Project

[![License](https://img.shields.io/badge/License-Apache%202.0-blue.svg)](https://opensource.org/licenses/Apache-2.0) [![UPRJ_CI](https://github.com/efabless/caravel_project_example/actions/workflows/user_project_ci.yml/badge.svg)](https://github.com/efabless/caravel_project_example/actions/workflows/user_project_ci.yml) [![Caravel Build](https://github.com/efabless/caravel_project_example/actions/workflows/caravel_build.yml/badge.svg)](https://github.com/efabless/caravel_project_example/actions/workflows/caravel_build.yml)

## Project Overview

This project involves the development of a CPU implementing the RISC-V architecture. 
The fundamental 32-bit instruction set of RISC-V is being implemented and developed utilizing a five-stage pipeline processor.

## Memory Layout Configuration

| Memory type    | Start    | Length  | 
| ------- | ----------- | ----- | 
| IMemory | 0x8000_0000 | 0x800 | 
| DMemory | 0x9000_0000 | 0x800 | 
| UART    | 0x1001_0000 | 0x100 | 

<!-- Refer to [README](docs/source/index.rst) for this sample project documentation. -->
