Here's a suggested README file for your Verilog project, which includes the dual-port RAM module and its accompanying testbench. This README outlines how to use the files, provides an overview of the project, and offers guidance on running simulations.

---

# Dual-Port RAM Verilog Module

## Overview

This repository contains a Verilog implementation of a dual-port Random Access Memory (RAM) module and a comprehensive testbench for simulation. The RAM module supports separate read and write operations on different clocks, making it suitable for various applications in digital systems that require simultaneous read/write access.

## Repository Structure

```
/ram_verilog_project
│
├── src/
│   ├── design.sv       - Verilog module for the dual-port RAM.
│   └── Testbench.sv    - Testbench for simulating the RAM module.
│
└── README.md           - Documentation for setting up and using the project.
```

## Features

- **Dual Clock Domains**: Supports separate clocks for read and write operations, enhancing flexibility in different system architectures.
- **Parameterized Design**: Width of data and address bus can be easily adjusted to meet specific requirements.
- **Write Enable Control**: Incorporates a write enable signal for controlled data writing to memory locations.
- **Waveform Output**: Generates waveform files for visualization and debugging of signal interactions over time.

## Prerequisites

- **Verilog Simulator**: A tool like Icarus Verilog, ModelSim, or VCS.
- **Waveform Viewer**: GTKWave or similar for viewing simulation results.

## Simulation Setup

### Running the Simulation

1. **Clone the Repository**: Obtain a copy of the source files on your local machine.
   ```bash
   git clone <repository-url>
   cd ram_verilog_project
   ```

2. **Compile the Source Code**:
   Use your Verilog simulation tool to compile the `design.sv` and `Testbench.sv` files. For example, with Icarus Verilog:
   ```bash
   iverilog -o ram_sim.vvp src/design.sv src/Testbench.sv
   ```

3. **Execute the Testbench**:
   Run the compiled simulation.
   ```bash
   vvp ram_sim.vvp
   ```

4. **View the Waveform**:
   Open the generated VCD file with a waveform viewer to analyze the simulation visually.
   ```bash
   gtkwave dump.vcd
   ```

   ![image](https://github.com/user-attachments/assets/ea15abc9-7836-4dd4-bad7-f071837699a6)
   ![image](https://github.com/user-attachments/assets/dba3b25a-c9f6-4c79-828c-e9c450ce6a37)
   ![image](https://github.com/user-attachments/assets/0ff54c2d-2acf-4448-88c1-90012fbc1376)




### Common Simulation Commands

- **Icarus Verilog**:
   ```sh
   iverilog -o output_filename.vvp source_files.sv
   vvp output_filename.vvp
   ```

- **ModelSim**:
   ```sh
   vlib work
   vlog source_files.sv
   vsim testbench_entity
   ```

## Contributing

Please fork the repository, make your changes, and submit a pull request for review.

## License

This project is made available under the MIT License. See the LICENSE file in the repository for full details.

## Contact

- **Author:** Isaac DeVaney
- **Email:** isaacdevaney@gmail.com
- **GitHub:** idevane

