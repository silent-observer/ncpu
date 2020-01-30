# ncpu
Another CPU made just for fun, supposed to be a microcontroller.
This is the official and the only specification for this CPU, as always.

## Features
It is 8-bit CPU with Harvard architecture, so separate instruction and data memory. 
Also it has dual stacks: one for usual function calls and the other for data.
In other aspects, it's the usual microcontroller (as for now).
Registers are 8 bits wide, while addresses are 16 bits wide both for instructions and for data.
Instructions are ??? bits wide.

## Registers
- `PC` - Program counter, 16 bits wide (as usual).
- `CSP` and `DSP` - Call stack pointer and data stack poonter. 
  8 bits wide, represent only the lower half of the address, the higher part is always `0xC0` for call stack and `0xC1` for data stack.
- `F` - Flag register. Specified later.
- `R0`-`R15` - General purpose registers.

## Flags
- Bit 0 - **C**arry
- Bit 1 - **N**egative
- Bit 2 - **Z**ero
- Bit 3 - O**v**erflow
- Bits 4-7 - Reserved