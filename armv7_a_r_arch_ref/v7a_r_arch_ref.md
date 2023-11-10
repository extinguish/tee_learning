## I Application Level Architecture

### I.1 Introduction to the ARM Architecture

### I.2 Application Level Programmers' Model

### I.3 Application Level Memory Model

### I.4 The Instruction Set

### I.5 ARM Instruction Set Encoding 

### I.6 Thumb Instruction Set Encoding 

### I.7 Advanced SIMD and VFP Instruction Encoding 

### I.8 Instruction Details

### I.9 ThumbEE

---------------------------------------------------------------------

## II System Level Architecture

### II.1 The System Level Programmers' Model

#### 1. About the system level programmers' model

#### 2. System level concepts and terminology

1. Privilege, mode and state

2. Exception

#### 3. ARM processor modes and core registers

1. ARM processor modes

- 1. Notes on the ARM processor modes

- 2. Pseudocode details of mode operations

2. ARM core registers

- 1. Writing to the PC

- 2. Pseudocode details of ARM core register operations



3. Program Status Registers(PSRs)



#### 4. Instruction set states

1. Exceptions and instruction set state

2. Unimplemented instruction sets


#### 5. The Security Extensions

1. Security states

2. Impact of the Security Extensions on the modes and exception model

#### 6. Exceptions 

1. Exception vectors and the exception base address

2. Exception priority order

3. Exception entry

4. Exception return

5. Exception-handling instructions

6. Control of exception handling by the Security Extensions

7. Low interrupt latency configuration

8. Wait for Event and Send Event

9. Wait for interrupt 

10. Reset

11. Undefined Instruction exception

12. Supervisor Call(svc) exception

13. Secure Monitor Call(smc) exception

14. Prefetch Abort Exception

15. Data Abort Exception

16. IRQ exception

17. FIQ exception


#### 7. Coprocessors and system control

#### 8. Advanved SIMD and floating-point support

#### 9. Exception environment support

### II.2 Common Memory System Architecture-Feacture

#### 1. About the memory system architecture

#### 2. Caches

#### 3. Implementation defined memory system features

#### 4. Pseudocode details of general memory system operations

### II.3 Virtual Memory System Architecture(VMSA)

#### 1. About the VMSA 

#### 2. Memory access sequence

#### 3. Translation tables

#### 4. Addressing mapping restriction

#### 5. Secure and Non-secure address spaces

#### 6. Memory access control

#### 7. Memory region attributes

#### 8. VMSA memory aborts

#### 9. Fault status and Fault Address registers in a VMSA implementation

#### 10. Translation Lookaside Buffers(TLBs)

#### 11. Virtual Address to Physical Address translation operations

#### 12. CP15 register for a VMSA implementation 

#### 13. Pseudocode details of VMSA memory system operations


### II.4 Protected Memory System Architecture(PMSA)

#### 1. About the PMSA

#### 2. Memory access control

#### 3. Memory region attributes

#### 4. PMSA memory aborts

#### 5. Fault Status and Fault Address registers in a PMSA implementation

#### 6. CP15 registers for a PMSA implementation

#### 7. Pseudocode details of PMSA memory system operations

### II.5 The CPUID Identificatioin Scheme

#### 4. 

#### 4. 

#### 4. 

#### 4. 

### II.6 System Instruction

#### 1. Alphabetical list of instruction

下面列出来的都是armv7-a当中支持的用于操系统寄存器的一些特殊系统指令，这些系统指令和我们通常使用的mov, ldr 这些应用层的指令的工作范围不一样.
> 需要注意的是，系统指令当中并没有 MCR/MRC 这些指令，这是因为 MCR/MRC 指令并不是系统指令，而是用于访问协处理器的特殊指令，这些指令是专门用于访问CP15这些处理器的, CP15处理器有自己的访问规则和权限规定

1. CPS

这个指令主要是用于修改系统的模式，主要修改的就是CPSR寄存器的A,I,F 这3个bit

2. LDM(exception return)

3. LDM(user register)

4. LDRBT, LDRHT, LDRSBT, LDRSHT, and LDRT

5. MRS

6. MSR(immediate)

7. MSR(register)

8. RFE

9. SMC(previously SMI)

10. SRS

11. STM(user register)

12. STRBT, STRHT, and STRT

13. SUBSP PC, LR and related instructions

14. VMRS

15. VMSR

--------------------------------------------------------------------------

## III. Debug Architecture


--------------------------------------------------------------------------





























### II.2 
