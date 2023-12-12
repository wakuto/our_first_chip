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
| UART_RW | 0x1001_0000 | 0x4  | 
| UART_STATUS | 0x1001_0005 | 0x4  |
| BAUD_MAX_ADDRESS | 0x1001_0100 | 0x4  |

## ALU Decoder Truth Table
|ALUOp|funct3|{op5,funct75}|ALUConrtol|instr|
|:----|:----|:----|:----|:----|
|00|-|-|0000(add)|lw,sw|
|01|-|-|0001(subtract)|beq|
|10|000|00,01,10|0000(add)|add|
| |000|11|0001(sub)|sub|
| |001|-| |sll|
| |010|-|0101(set less than)|slt|
| |011| | |sltu|
| |100| | |xor|
| |101|00,01,10| |srl|
| |101|11| |sra|
| |110| |0011(or)|or|
| |111| |0010(and)|and|

## Corresponding table of ALUControl and operations
|alu_control|||
|:----|:----|:----|
|0000|add|+|
|0001|sub|-|
|0010|and|&|
|0011|or|\||
|0100|xor|^|
|0101|slt|<|
|0110|sltu|<|
|0111|sll|<<|
|1000|srl|>>|
|1001|sra|>>>|
|1010|eq|==|
|1011|not eq|!=|
|1100|ge|>=|
|1101|geu|>=|
|1110| | |
|1111| | |

## Development Background
We have been conducting a technical book reading circle with classmates from an industrial high school. During one of these sessions, we successfully created a small-scale pipeline processor, leading us to decide to apply for the Open MPW Shuttle program. 

The original repository for this project can be found at https://github.com/wakuto/our_first_cpu.

The development team includes kirika1221,sushiyoshi, and wakuto.
 sample project documentation. -->
