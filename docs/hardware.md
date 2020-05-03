# Hardware Architecture

The following outlines hardware specifications, block diagrams, pseudo code along with the results and analysis of the design.

## FPGA Block Diagram
![Hardware](https://i.imgur.com/89GHfYj.jpg)

## Hardware Specifications
###FPGA

Nexys DDR board with Xilinx Artix-7 chip
> 160 18-bit DSP slices (up to 16 GOPs throughput at 100 MHz)

> 0.5 Mbytes of block RAM

![Hardware](https://i.imgur.com/yWM6vtT.jpg)

### UART Block

| Item | Value |
| -------------------- | ----------- |
| Data Input Rate | 100 kBps |
| Data Output Rate | 100 kBps |
| Baud Rate | 1 Mbps |
| Data Transfer Interface | UART over USB |

### Convolution Block

| Items | Committed Requirement | Stretch Goal |
| -------------------- | ----------- | ----------- |
| Input Image Size | 512x512 | 4096x4096 |
| # of input planes | 3 | Arbitrary |
| Output image size | Valid | Same, valid, full |
| # of output planes | 3 | Arbitrary |
| Kernel Size | 7x7 | Arbitrary, where W*H*D < 512 |

### Same, Full, Valid
![Verification](https://i.imgur.com/RgoYCFY.jpg)


## FPGA Block Diagram


## Example of ILB with Image Window
![Hardware](https://i.imgur.com/UFqZOds.gif[/img)
Add Description of the animation


### Project Website
Check out our website [here][website] for more information about our project.

[website]: https://kierajcullen.github.io/-dcnn-.github.io/
