# Convolutional Neural Network Accelerator

This document describes the architecture and implementation for an end-to-end 2D convolution acceleration system, targeting applications such as image filtering and deep convolutional neural networks. 

## Project Overview

Deep Convolutional Neural Networks (DCNNs) have made significant progress in approaching a wide range of problems in the general area of computer vision. However, they generally require enormous computational resources and are therefore difficult to deploy in real-time systems. To address this problem, we designed a system for accelerating the core operations required by DCNNs, by using a low-cost Field Programmable Gate Array (FPGA) platform. Our team designed an end-to-end accelerator platform, including a PC running Linux, an FPGA board and PC-to-FPGA communication via serial data (over USB). We designed a hardwired convolution processor using custom fixed-point multipliers, and a software handler for sending and reconstructing images. Using custom Verilog/VHDL RTL descriptions and C++ software, we aim to exploit the parallelism inherent to FPGAs for high-speed acceleration.


    mkdocs.yml    # The configuration file.
    docs/
        index.md  # The documentation homepage.
        ...       # Other markdown pages, images and other files.
