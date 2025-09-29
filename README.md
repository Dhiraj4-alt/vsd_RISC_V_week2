
## VSD BabySoC – Theory

The project details the design of **BabySoC**, a compact, open-source, RISC-V System on Chip (SoC) for educational purposes, featuring a **RVMYTH** processor core, a **Phase-Locked Loop (PLL)** for stable clocking, and a **10-bit Digital-to-Analog Converter (DAC)** for mixed-signal communication. Built using **Sky130 technology**, BabySoC aims to provide a documented platform for learning digital-analog system design by enabling the DAC to convert digital data into analog signals, facilitating interaction with external devices for output.
Below is a basic understandinng document of theoritical concepts of my learnings about the BabySoC..

---
<details>
<summary> ### 📖 Theory – Fundamentals of SoC</summary>

#### What is a System-on-Chip (SoC)?
A System-on-Chip (SoC) is a compact integrated circuit that combines multiple components of a computer or electronic system onto a single chip. Instead of using separate chips for CPU, memory, and peripherals, an SoC integrates them, improving efficiency, reducing power consumption, and saving space. SoCs are used in smartphones, tablets, wearables, IoT devices, and embedded systems.
</details>
---

### Key Components of an SoC

1. **CPU (Central Processing Unit)**  
   - The brain of the SoC.  
   - Executes instructions, performs calculations, and controls other components.

2. **Memory**  
   - **RAM**: Temporary storage for running programs and data.  
   - **ROM/Flash**: Permanent storage for firmware and persistent data.

3. **Peripherals and I/O Ports**  
   - Interfaces for external devices (USB, camera, audio, display).  
   - Facilitates communication between the SoC and the outside world.

4. **Interconnect / Bus**  
   - Connects CPU, memory, and peripherals.  
   - Efficient interconnects ensure fast data transfer.

5. **Special Components**  
   - **PLL (Phase-Locked Loop)**: Generates stable clock signals for synchronization.  
   - **DAC (Digital-to-Analog Converter)**: Converts digital data into analog signals for devices like TVs or audio systems.

---

### Why Use BabySoC?

- **Educational Platform**: BabySoC is fully open-source, allowing deep exploration of SoC design.  
- **Hands-on Learning**: Integrates RVMYTH CPU, PLL, and DAC to simulate real-world SoC scenarios.  
- **Digital-to-Analog Interfacing**: Lets students experiment with analog outputs from digital systems.  
- **Compact & Testable**: Ideal for simulating and verifying RTL designs before actual tapeout.

---

### Functioning Model of RTL

Before moving to physical design stages, the **Register-Transfer Level (RTL) model** allows verification of design functionality:

1. **Behavioral Simulation**  
   - Ensures each component (CPU, memory, DAC, PLL) behaves as expected.

2. **Timing Verification**  
   - Checks for setup and hold time violations, glitches, and clock synchronization issues.

3. **Optimization & Debugging**  
   - Helps optimize combinational and sequential circuits, identify bottlenecks, and avoid synthesis mismatches.

4. **Importance**  
   - RTL functioning model ensures that the physical design reflects intended functionality.  
   - Reduces costly errors in tapeout and fabrication.

---

### Key Questions Answered

- **What is an SoC?**  
  A mini-computer on a single chip integrating CPU, memory, and peripherals.

- **Why BabySoC?**  
  Provides a hands-on, documented platform for learning SoC design and analog interfacing.

- **Role of RTL before physical design**  
  Acts as a blueprint to verify logic, timing, and overall system functionality before synthesis and layout.

---

## 🛠 Practical Labs

Labs focus on verifying SoC components using open-source tools:

- **Icarus Verilog (iverilog)** – Compile and simulate Verilog RTL designs.  
- **Yosys** – Synthesize RTL code into gate-level netlists.  
- **GTKWave** – View waveform outputs of simulations.  
- **Sky130 PDK** – Test designs on a real-process design kit.

**Labs include:**  
1. Introduction to Verilog RTL and synthesis  
2. Timing and optimization of combinational and sequential circuits  
3. GLS, blocking vs non-blocking, and simulation-synthesis mismatch  
4. Hierarchical vs flat synthesis and optimizations  

---

## 📂 Repository Structure
