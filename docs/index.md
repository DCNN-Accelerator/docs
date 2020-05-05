# Convolutional Neural Network Accelerator

This document describes the architecture and implementation for an end-to-end 2D convolution acceleration system, targeting applications such as image filtering and deep convolutional neural networks. The goal of such is to provide readers with the necessary explanations and resources to understand the concepts in our design.


### High Level Block Diagram

![Verification](https://i.imgur.com/q204Ktu.png)&nbsp;


## Project Overview

Deep Convolutional Neural Networks (DCNNs) have made significant progress in approaching a wide range of problems in the general area of computer vision. However, they generally require enormous computational resources and are therefore difficult to deploy in real-time systems. To address this problem, we designed a system for accelerating the core operations required by DCNNs, by using a low-cost Field Programmable Gate Array (FPGA) platform. Our team designed an end-to-end accelerator platform, including a PC running Linux, an FPGA board and PC-to-FPGA communication via serial data (over USB). We designed a hardwired convolution processor using custom fixed-point multipliers, and a software handler for sending and reconstructing images. Using custom Verilog/VHDL RTL descriptions and C# software, we aim to exploit the parallelism inherent to FPGAs for high-speed acceleration. FPGAs are inexpensive pieces of hardware, and if our design is successful, it can be used by anyone.

### Project Website
Check out our website [here][website] for more information about our project.

[website]: https://kierajcullen.github.io/-dcnn-.github.io/
