# VSD Squadron Workshop

This is a repository for documenting all the tasks performed as a part of VSDSquadron Workshop

##  Table of Contents

- [Task 1](#task-1) : This task focuses on basic process of compiling a C program using GCC compiler and checking whether the C file is correctly functioning. Later, we compile the same C code using RISCV-GCC compiler with multiple optimization conditions.



## Task 1
### Subtasks
- Perform compilation of a C code using GCC compiler

- Perform compilation of the same C code using RISC-V GCC compiler using O1 optimization configuration.

- Perform compilation of the same C code using RISC-V GCC compiler by selecting O2 and Ofast optimization configuration.

- Observe the assembly code using objdump -d command for O1,O0 and Ofast optimization configurations.

- Compare the machine code instruction corresponding to main section for the three optimization configurations options.

### Methodology

- Command for GCC Compilation: *gcc sum1ton.c*

    ![C Program Screenshot](screen_snaps\C_prog_vim.png)


- Command to run the C Program: *./a.out*

    ![C Program Screenshot](screen_snaps\C_program_run.png)


- Command to compile using RISC-V GCC Compiler(O1 optimization): *riscv64-unknown-elf-gcc -O1 -mabi=lp64 -march=rv64i -o sum1ton.o sum1ton.c*


- Command to get the assembly code: *riscv64-unknown-elf-objdump –d sum1ton.o*

- Command to dump the assembly code into a text file for later analysis: *riscv64-unknown-elf-objdump -d sum1ton.o > dis_assembly_O1_optimization.txt*


### Observations

- O1 Optimization 

    ![O1 Optimization Screenshot](screen_snaps\o1.png)

- Ofast Optimization 

    ![Ofast Optimization Screenshot](screen_snaps\ofast.png)

- O0 Optimization 

    ![O0 Optimization Screenshot](screen_snaps\o0.png)

    We see that different optimization configurations yield different number of machine instructions depending on the level of optimization the configurations provide.

<!-- ***
---
*** -->




<!-- ## Task 2 -->