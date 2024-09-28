# Own-CPU

- [ ] 16-Bit

- [ ] Registers (16-Bit)
    - r0 - r7
    - PC (Program Counter)
    - SP (Stack Pointer)
    - (SF (Status Flags))

Instructions
=

| Instruction | Opcode | bytes | cycles | Information 
| ------------|--------|-------|--------|------------
| LVR REG, #Value| 0x00   | 4     | ?      | Loads a specified value into the specified register (Load Value into Register)
| LRR REG, REG | 0x01 | 4     | ?      | Loads a value from one register into another one (Load Register value into Register)
| LMR REG, #Addr | 0x02 | 4     | ?     | Loads a value from a specified memory location into a specified register (Load Memory value into Register)
| SLR REG, #Addr  | 0x10 | 4   | ?      | Stores the low byte from a register to memory (Store Low byte from Register)
| SHR REG, #Addr | 0x11 | 4    | ?      | Stores the high byte from a register to memory (Store High byte from Register)
| SWR REG, #Addr | 0x12 | 4    | ?      | Stores the entire register value to memory (Store Word from Register)
| CRR REGA, REGB | 0x20 | 3    | ?      | Compares register A with register B and stores the result in register A (0x00 if a == b, 0x01 if a > b, 0x80 if a < b) (Compare Register with Register)
| CRM REG, #Addr | 0x21 | 4    | ?      | Compares a register with a specified memory address and stores the result in the register (Same as in CRR) (Compare Register with Memory)
| BEQ REG, #Addr | 0x30    | 5 | ?      | Branches to a specified memory address if the last comparison was equal (register holds the value 0x00) (Branch if EQual)
| ARV REG, Value | 0x40 | 4    | ?      | Adds an immediate value to a register and stores the result in that register (Add Register and Value)
| SRV REG, #Value | 0x41 | 4   | ?      | Subtracts an immediate value to a register and stores the result in that register (Subtract Register and Value)
| ARM REG, #Addr | 0x42 | 4    | ?      | Adds a value in memory to a register and stores the result in the register (Add Register and Memory value) 
| SRM REG, #Addr | 0x43 | 4    | ?      | Subtracts a value in memory to a register and stores the result in the register (Subtract Register and Memory value) 
| ARR REGA, REGB | 0x44 | 3    | ?      | Adds the value from register B to register A and stores the result in the register A(Add Register and Register) 
| SRR REGA, REGB | 0x45 | 3    | ?      | Subtracts register B from register A and stores the result in the register A(Subtract Register and Register) 

Tools
-

- [ ] Assembler
- [ ] External ROM
- [ ] External RAM
- [ ] External Clock
- [ ] Keyboard (Arduino or PS/2)
- [ ] BIOS
- [ ] (LCD) Display
