# RISC-V Talent Development Program 2025
This repository if for keeping account of the RISC-V Talent Development Program, powered by Samsung Semiconductor India Research (SSIR) along with VLSI System Design (VSD)

Basic Details
Name: VINAY K GOWDA
College: THE NATIONAL INSTITUTE OF ENGINEERING (NIE)
Email ID: opivcm441@gmail.com


TASK3
---------------------------------------------------------------------------------------------------
1. Instruction: 'lui a0, 0x2b'
- Opcode: '0110111' (7 bits)
- Immediate: '0x2b' (20 bits)
- Destination Register (rd): 'a0' (x10, 5 bits)
- Breakdown:
  - Immediate (0x2b): '000000000000000000101011'
  - rd ('a0 = x10'): '01010'
  - Opcode: '0110111'
- Final 32-bit Code: '0000000000000000001010110110111'  
  Binary: '0002b537'

---

2. Instruction: 'addi sp, sp, -64'
- Opcode: '0010011' (7 bits)
- Immediate: '-64' (12 bits, two's complement)
- Source Register (rs1): 'sp' (x2, 5 bits)
- Destination Register (rd): 'sp' (x2, 5 bits)
- Function (funct3): '000' (3 bits)
- Breakdown:
  - Immediate (-64): '111111110000'
  - rs1 ('sp = x2'): '00010'
  - funct3: '000'
  - rd ('sp = x2'): '00010'
  - Opcode: '0010011'
- Final 32-bit Code: '1111111100000001001000010010011'  
  Binary: 'fc010113'

---

3. Instruction: 'sd ra, 56(sp)'
- Opcode: '0100011' (7 bits)
- Immediate: '56' (12 bits, split as imm[11:5] and imm[4:0])
- Source Register (rs2): 'ra' (x1, 5 bits)
- Source Register (rs1): 'sp' (x2, 5 bits)
- Function (funct3): '011' (3 bits)
- Breakdown:
  - Immediate (56): '0000011' (imm[11:5]) and '11000' (imm[4:0])
  - rs2 ('ra = x1'): '00001'
  - rs1 ('sp = x2'): '00010'
  - funct3: '011'
  - Opcode: '0100011'
- Final 32-bit Code: '00000110001000110000101111000011'  
  Binary: '02113c23'

---

4. Instruction: 'jal ra, 11684'
- Opcode: '1101111' (7 bits)
- Immediate: '11684' (21 bits, split as imm[20|10:1|11|19:12])
- Destination Register (rd): 'ra' (x1, 5 bits)
- Breakdown:
  - Immediate (11684): '0101101110000' (reordered to match encoding)
  - rd ('ra = x1'): '00001'
  - Opcode: '1101111'
- Final 32-bit Code: '01011011100000000001011011110111'  
  Binary: '5bc010ef'

---

5. Instruction: 'lbu a5, 15(sp)'
- Opcode: '0000011' (7 bits)
- Immediate: '15' (12 bits, sign-extended)
- Source Register (rs1): 'sp' (x2, 5 bits)
- Destination Register (rd): 'a5' (x15, 5 bits)
- Function (funct3): '100' (3 bits)
- Breakdown:
  - Immediate (15): '0000000001111'
  - rs1 ('sp = x2'): '00010'
  - funct3: '100'
  - rd ('a5 = x15'): '01111'
  - Opcode: '0000011'
- Final 32-bit Code: '00000000011110010001101111100011'  
  Binary: '00f14783'

---

6. Instruction: 'li a4, 43' (Equivalent to 'addi a4, x0, 43')
- Opcode: '0010011' (7 bits)
- Immediate: '43' (12 bits)
- Source Register (rs1): 'x0' (5 bits)
- Destination Register (rd): 'a4' (x14, 5 bits)
- Function (funct3): '000' (3 bits)
- Breakdown:
  - Immediate (43): '000000001011'
  - rs1 ('x0'): '00000'
  - funct3: '000'
  - rd ('a4 = x14'): '01110'
  - Opcode: '0010011'
- Final 32-bit Code: '00000000101100000010011100010011'  
  Binary: '02b00713'

---

7. Instruction: 'beq a5, a4, 10198'
- Opcode: '1100011' (7 bits)
- Immediate: '10198' (12 bits, split into imm[12|10:5|4:1|11])
- Source Registers:
  - rs1: 'a5' (x15, 5 bits)
  - rs2: 'a4' (x14, 5 bits)
- Function (funct3): '000' (3 bits)
- Breakdown:
  - Immediate (10198): '101011100' (reordered as per encoding)
  - rs1 ('a5 = x15'): '01111'
  - rs2 ('a4 = x14'): '01110'
  - funct3: '000'
  - Opcode: '1100011'
- Final 32-bit Code: '10101110011101110000010101010011'  
  Binary: '08e78a63'

---

8. Instruction: 'bgeu a4, a5, 10160'
- Opcode: '1100011' (7 bits)
- Immediate: '10160' (12 bits, split into imm[12|10:5|4:1|11])
- Source Registers:
  - rs1: 'a4' (x14, 5 bits)
  - rs2: 'a5' (x15, 5 bits)
- Function (funct3): '111' (3 bits)
- Breakdown:
  - Immediate (10160): '101010000'
  - rs1 ('a4 = x14'): '01110'
  - rs2 ('a5 = x15'): '01111'
  - funct3: '111'
  - Opcode: '1100011'
- Final 32-bit Code: '10101000011101111000011010100011'  
  Binary: '04f77c63'

---

9. Instruction: 'bne a5, a4, 101c8'
- Opcode: '1100011' (7 bits)
- Immediate: '101c8' (12 bits, split into imm[12|10:5|4:1|11])
- Source Registers:
  - rs1: 'a5' (x15, 5 bits)
  - rs2: 'a4' (x14, 5 bits)
- Function (funct3): '001' (3 bits)
- Breakdown:
  - Immediate (101c8): '101100011'
  - rs1 ('a5 = x15'): '01111'
  - rs2 ('a4 = x14'): '01110'
  - funct3: '001'
  - Opcode: '1100011'
- Final 32-bit Code: '10110001101101111000010011001111'  
  Binary: '0ae79863'

---

10. Instruction: 'ld s0, 16(sp)'
- Opcode: '0000011' (7 bits)
- Immediate: '16' (12 bits)
- Source Register (rs1): 'sp' (x2, 5 bits)
- Destination Register (rd): 's0' (x8, 5 bits)
- Function (funct3): '011' (3 bits)
- Breakdown:
  - Immediate (16): '000000010000'
  - rs1 ('sp = x2'): '00010'
  - funct3: '011'
  - rd ('s0 = x8'): '01000'
  - Opcode: '0000011'
- Final 32-bit Code: '00000001000000010011010000100011'  
  Binary: '01013403'

---

11. Instruction: 'mv a0, s0' (Equivalent to 'addi a0, s0, 0')
- Opcode: '0010011' (7 bits)
- Immediate: '0' (12 bits)
- Source Register (rs1): 's0' (x8, 5 bits)
- Destination Register (rd): 'a0' (x10, 5 bits)
- Function (funct3): '000' (3 bits)
- Breakdown:
  - Immediate (0): '000000000000'
  - rs1 ('s0 = x8'): '01000'
  - funct3: '000'
  - rd ('a0 = x10'): '01010'
  - Opcode: '0010011'
- Final 32-bit Code: '0000000000000100000001010010011'  
  Binary: '00040513'

---

12. Instruction: 'ret' (Equivalent to 'jalr x0, x1, 0')
- Opcode: '1100111' (7 bits)
- Immediate: '0' (12 bits)
- Source Register (rs1): 'ra' (x1, 5 bits)
- Destination Register (rd): 'x0' (5 bits)
- Function (funct3): '000' (3 bits)
- Breakdown:
  - Immediate (0): '000000000000'
  - rs1 ('ra = x1'): '00001'
  - funct3: '000'
  - rd ('x0'): '00000'
  - Opcode: '1100111'
- Final 32-bit Code: '0000000000000000100000001100111'  
  Binary: '00008067'

---

13. Instruction: 'j 10148'
- Opcode: '1101111' (7 bits)
- Immediate: '10148' (21 bits, split into imm[20|10:1|11|19:12])
- Destination Register (rd): 'x0' (5 bits)
- Breakdown:
  - Immediate (10148): '1110110001000' (reordered as per encoding)
  - rd ('x0'): '00000'
  - Opcode: '1101111'
- Final 32-bit Code: '11101100010000000000011101111011'  
  Binary: 'fb5ff06f'

---




