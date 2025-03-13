# DLD Project Updates

## Phase 1
Implemented a basic 8-bit adder with temporary input pins and output probes. Moreover, in order to perform subtraction I used the same adder circuit with an XOR gate with every bit of 'B'. The "First" input in XOR is "SUB" which will be 0 if addition is being performed and 1 if subtraction is being performed, and the "Second" input in XOR is a 'B' bit. 

### **Truth Table for a Single Bit of B**

Each row shows the transformation of B under different conditions.

|**B (Original)**|**SUB (Mode Selection)**|**B' (After XOR with SUB)**|**Carry-In to LSB**|**Final Effective B (2's Complement Effect)**|
|---|---|---|---|---|
|0|0|0|0|0 (Normal addition)|
|1|0|1|0|1 (Normal addition)|
|0|1|1|1|1 (2’s complement step: flipped 0 → 1, plus carry)|
|1|1|0|1|0 (2’s complement step: flipped 1 → 0, plus carry)|
