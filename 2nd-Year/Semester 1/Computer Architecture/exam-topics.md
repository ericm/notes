# Things to study
- Binary representation of FP. https://www.wikihow.com/Convert-a-Number-from-Decimal-to-IEEE-754-Floating-Point-Representation

- Pipelining

- MIPS instruction formats

- The 5 stages of processing an instruction:
  1. IF: instruct fetch
  2. ID: Decode
  3. EX: Execution / Calc address
  4. MEM: If needed access memory
  5. WB: Write result to a register if needed
  
- Optimizations to code flow such as:
  - Branch prediction
  - Pipelining for arithmetic instructions etc
 
- Remember the only J type instruciton is `j Label`.

- Pipelining Hazards:
  - Structure - 2 instructs accessing same resource
  - Data: Accessing data from previous instruct
  - Control - Branches etc
  
 - `add` and `sub` exception on overflow. Use the `addu` etc to not have this.
 
 - Know a lot about bpipelining (architecture diagrams etc) (and how to improve it)
 
 - Know memory stuff:
    - Write through: Update the lower level memory (such as ram and vram) when data is "written" to cache.
  
    - Write-back: Only write to slower memory when whole block is replaced
  
 - Caching methods and replacement policies
