# turbo-encoder-decoder-verilog-fpga
# Design and Implementation of Turbo Encoder and Decoder for Encryption and Decryption Systems

## Overview

This project presents the design and FPGA implementation of a Turbo Encoder and Turbo Decoder using Verilog HDL for secure and reliable digital communication systems.

The architecture was implemented using Recursive Systematic Convolutional (RSC) Encoders, Pseudo-Random Interleavers, and iterative Turbo Decoding techniques. The complete system was verified using simulation and deployed on a Xilinx Edge Zynq SoC FPGA using the Vivado Design Suite.

The project demonstrates a complete VLSI design flow including:
- RTL Design
- Functional Verification
- FPGA Synthesis
- Timing Analysis
- Power Analysis
- Hardware Validation

---

## Objectives

- Design Turbo Encoder using RSC architecture
- Implement Turbo Decoder with iterative decoding
- Develop Interleaver and De-Interleaver modules
- Perform RTL simulation using Vivado
- Implement the design on FPGA hardware
- Analyze timing, power, and resource utilization

---

## System Architecture

The Turbo Coding system consists of:

### Transmitter Side
- RSC Encoder 1
- Pseudo-Random Interleaver
- RSC Encoder 2

### Receiver Side
- RSC Decoder 1
- De-Interleaver
- RSC Decoder 2

The encoder generates systematic bits and parity bits to improve transmission reliability.

---

## Methodology

### 1. RTL Design
The complete Turbo Encoder and Decoder were designed using Verilog HDL.

### 2. Turbo Encoder
The encoder uses:
- Two Recursive Systematic Convolutional (RSC) Encoders
- 3-bit shift registers
- XOR feedback logic

Generator Polynomials:
- Feedback Polynomial: 1 + D²
- Feedforward Polynomial: 1 + D + D²

### 3. Interleaver
A pseudo-random interleaver rearranges input bits to reduce burst error effects.

### 4. Turbo Decoder
The decoder uses iterative decoding with two RSC decoders and a De-Interleaver for data reconstruction.

### 5. FPGA Implementation
The design was synthesized and implemented on:
- Xilinx Edge Zynq SoC FPGA
- Vivado Design Suite

### 6. Hardware Verification
Verification was performed using:
- Vivado Simulator
- VIO (Virtual Input Output)
- ILA (Integrated Logic Analyzer)

---

## Technologies Used

- Verilog HDL
- SystemVerilog
- Xilinx Vivado
- FPGA Design
- Digital Communication Systems

---

## FPGA Implementation Details

### FPGA Board
- Edge Zynq SoC FPGA

### Clock Frequency
- 100 MHz

### Hardware Interfaces
- Switches → Input Data
- LEDs → Output Data

---

## Results

### Simulation Results
- Successful encoding and decoding for 4-bit and 8-bit sequences
- Accurate parity generation
- Correct reconstruction of original data

### FPGA Results
- Successful hardware verification using VIO and ILA
- Real-time encoding and decoding achieved

### Power Analysis
- Total On-Chip Power: 0.097 W

### Resource Utilization
- LUT Usage: 16.55%
- Flip-Flops: 13.4%
- BRAM: 5%

---

## Applications

- Wireless Communication
- Satellite Communication
- LTE and 5G Systems
- IoT Communication
- Secure Data Transmission

---

## Future Enhancements

- Soft-decision decoding
- Log-MAP and Max-Log-MAP algorithms
- Higher throughput optimization
- ASIC implementation

---

## References

1. Claude Berrou and Alain Glavieux, “Near Optimum Error Correcting Coding and Decoding: Turbo Codes”
2. IEEE Turbo Coding Research Papers
3. Xilinx Vivado Documentation

---

## Author

Narasimha G
