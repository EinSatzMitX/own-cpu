# Own-CPU

- [ ] 16-Bit

- [ ] Registers (16-Bit)
    - r0 - r7
    - PC (Program Counter)
    - SP (Stack Pointer)
    - SF (Status Flags)

Status Flag Layout
---

|0b0 | 0 | 0 | 0 | 0 | 0 | 0 | 0
|----|---|---|---|---|---|---|---
| L (Less) | Z (Zero) | C (Carry) | V (Overflow) | S (Signed) | N (Negative) | Unused | Unused



Instructions
=

| Instruction | Opcode | bytes | cycles | Information 
| ------------|--------|-------|--------|------------
| LDI REG, #Value| 0x00   | 4     | ?      | Loads an immediate value into the specified register (LoaD register Immediate)
| LDR REG, REG | 0x01 | 3     | ?      | Loads a value from one register into another one (LoaD register value into Register)
| LDM REG, #Addr | 0x02 | 4     | ?     | Loads a value from a specified memory location into a specified register (LoaD Memory value into register)
| SLR REG, #Addr  | 0x10 | 4   | ?      | Stores the low byte from a register to memory (Store Low byte from Register)
| SHR REG, #Addr | 0x11 | 4    | ?      | Stores the high byte from a register to memory (Store High byte from Register)
| SWR REG, #Addr | 0x12 | 4    | ?      | Stores the entire register value to memory (low byte first) (Store Word from Register)
| CRR REGA, REGB | 0x20 | 3    | ?      | Compares register A with register B and stores the result in register A (0x00 if a == b, 0x01 if a > b, 0x80 if a < b) (Compare Register with Register)
| CRM REG, #Addr | 0x21 | 4    | ?      | Compares a register with a specified memory address and stores the result in the register (Same as in CRR) (Compare Register with Memory)
| CRI REG, #Value | 0x22 | 4   | ?      | Compares a register with an immediate value and set status flags accordingly
| BEQ        | 0x30    | 5     | ?      | Branches to a specified memory address if the last comparison was equal (Zero flag set) (Branch if EQual) 
| ASI REG, Value | 0x40 | 4    | ?      | Adds a signed immediate value to a register and stores the result in that register (Add Signed Immediate)
| SSI REG, #Value | 0x41 | 4   | ?      | Subtracts a signed immediate value to a register and stores the result in that register (Subtract Signed Immediate)
| ASM REG, #Addr | 0x42 | 4    | ?      | Adds a value in memory to a register and stores the result in the register (Add  Signed Memory value) 
| SSM REG, #Addr | 0x43 | 4    | ?      | Subtracts a value in memory to a register and stores the result in the register (Subtract Signed Memory value) 
| ASR REGA, REGB | 0x44 | 3    | ?      | Adds the value from register B to register A and stores the result in the register A(Add Signed Register) 
| SSR REGA, REGB | 0x45 | 3    | ?      | Subtracts register B from register A and stores the result in the register A(Subtract Signed Register) 
| AUI REG, Value | 0x46 | 4    | ?      | Adds an unsigned immediate value to a register and stores the result in that register (Add Unsigned Immediate)
| SUI REG, #Value | 0x47 | 4   | ?      | Subtracts an unsigned immediate value to a register and stores the result in that register (Subtract Unsigned Immediate)
| AUM REG, #Addr | 0x48 | 4    | ?      | Adds an unsigned value in memory to a register and stores the result in the register (Add Unsigned Memory value) 
| SUM REG, #Addr | 0x49 | 4    | ?      | Subtracts an unsigned value in memory to a register and stores the result in the register (Subtract Unsigned Memory value) 
| AUR REGA, REGB | 0x4A | 3    | ?      | Adds the unsigned value from register B to register A and stores the result in the register A(Add Unsigned Register) 
| SUR REGA, REGB | 0x4B | 3    | ?      | Subtracts the unsigned value of register B from register A and stores the result in the register A(Subtract Unsigned Register) 
| XRI REG, #Value| 0x50 | 4    | ?      | Performs logical XOR on a register and an immediate value and store it in the register (Xor Register Immediate)
| XRM REG, #Addr | 0x51 | 4    | ?      | Performs logical XOR on a register and a zero-paged value and store it in the register (Xor Register Memory)
| XRR REGA, REGB | 0x52 | 3    | ?      | Performs logical XOR on two registers and stores the result in the a register (Xor Register Register)
| ANI REG, #Value| 0x53 | 4    | ?      | Performs logical AND on a register and an immediate value and store it in the register (ANd register Immediate)
| ANM REG, #Addr | 0x54 | 4    | ?      | Performs logical AND on a register and an zero-paged value and store it in the register (ANd register Memory)
| ANR REG, REG   | 0x55 | 3    | ?      | Performs logical AND on two registers and stores it in the first register (ANd register Register)
| NOT REG        | 0x56 | 2    | ?      | Performs logical NOT on a register and store it in the register
| ORI REG, #Value| 0x57 | 4    | ?      | Performs logical OR on a register and an immediate value and store it in the register (OR register Immediate)
| ORM REG, #Addr | 0x58 | 4    | ?      | Performs logical OR on a register and an zero-paged value and store it in the register (OR register Memory)
| ORR REG, REG   | 0x59 | 3    | ?      | Performs logical OR on two registers and stores it in the first register (OR register Register)
| HLT            | 0xFE | 1    | ?      | Halts the CPU
| NOP            | 0xFF | 1    | ?      | No OPeration


Tools
-

- [ ] Emulator (WIP)
- [ ] Assembler
- [ ] External ROM
- [ ] External RAM
- [ ] External Clock
- [ ] Keyboard (Arduino or PS/2)
- [ ] BIOS
- [ ] (LCD) Display
