# Convolutional Neural Network Accelerator

This document describes the architecture and implementation for an end-to-end 2D convolution acceleration system, targeting applications such as image filtering and deep convolutional neural networks. The goal is to make our work and design understandable for anyone.


## Project Goals
1. Create a system for acceleration of the convolution operation: Interfaced to a PC workstation
2. Theoretically faster than PC alone
3. Serves as proof of concept using cheap FPGAs

### High Level Diagram

![Verification](https://i.imgur.com/EFvMUEt.jpg)&nbsp;


## Project Overview

Deep Convolutional Neural Networks (DCNNs) have made significant progress in approaching a wide range of problems in the general area of computer vision. However, they generally require enormous computational resources and are therefore difficult to deploy in real-time systems. To address this problem, we designed a system for accelerating the core operations required by DCNNs, by using a low-cost Field Programmable Gate Array (FPGA) platform. Our team designed an end-to-end accelerator platform, including a PC running Linux, an FPGA board and PC-to-FPGA communication via serial data (over USB). We designed a hardwired convolution processor using custom fixed-point multipliers, and a software handler for sending and reconstructing images. Using custom Verilog/VHDL RTL descriptions and C# software, we aim to exploit the parallelism inherent to FPGAs for high-speed acceleration.

### Project Website
Check out our website [here][website] for more information about our project.

[website]: https://kierajcullen.github.io/-dcnn-.github.io/
