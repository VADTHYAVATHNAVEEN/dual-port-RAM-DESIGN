This project implements a Dual-Port RAM using Verilog. The module supports simultaneous read and write operations through two independent ports (Port A and Port B). The design is optimized for efficient memory access, making it suitable for high-speed applications like DSP, image processing, and shared memory systems.

**Features**
Simultaneous Read and Write: Independent access for both ports.
Configurable Memory Size: 64x8-bit RAM.
Synchronous Operation: Operates on the positive edge of the clock.
Independent Write Enables: Separate write enable signals for each port.
Read and Write Collision Handling: Ensures proper data access during simultaneous operations.
**Design Details**
Dual-Port RAM Module
The Dual-Port RAM module has the following interface:

Data Inputs: data_a and data_b (8-bit each).
Address Inputs: addr_a and addr_b (6-bit each).
Write Enable Inputs: we_a and we_b.
Clock Input: clk.
Data Outputs: q_a and q_b (8-bit each).

**Block Diagram**
          +-------------------+       +-------------------+
          |                   |       |                   |
  data_a  |                   |       |                   |  data_b
 -------->|  Dual-Port RAM     |<----->|  Dual-Port RAM     |<--------
          |                   |       |                   |
  addr_a  |                   |       |                   |  addr_b
 -------->|                   |       |                   |<--------
          |                   |       |                   |
    we_a  |                   |       |                   |   we_b
 -------->|                   |       |                   |<--------
          |                   |       |                   |
     clk  |                   |       |                   |    clk
 -------->|                   |       |                   |<--------
          +-------------------+       +-------------------
                   q_a                            q_b
**Testbench**
**The testbench verifies:**

Simultaneous read and write operations
Independent data access through Port A and Port B
Collision detection and data consistency
**Applications**
Digital Signal Processing (DSP)
Shared Memory Systems
Communication Buffers
Image Processing
**Contributions**
Contributions are welcome! Feel free to fork the project and submit a pull request. For major changes, please open an issue first to discuss what you would like to change.

**Contact**
For any questions or suggestions, please reach out via GitHub issues.
