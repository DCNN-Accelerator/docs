# Software Architecture

The following outlines software specifications, block diagrams, pseudo code and important results and analysis for the project.

## High Level Block Diagram
![Software](https://i.imgur.com/89GHfYj.jpg)

## Software Specifications

| Item | Value |
| -------------------- | ----------- |
| Input image filetype | All OpenCV() supported (.jpg, .png, etc) |
| Input kernel data filetype | .csv file |
| Output data filetype | .jpg image |
| Supported OS | Windows |


## Preprocessors

Discuss Preprocessors (might not be necessary)

## Im_load_stream

This script takes in the image and kernel, converting such to fixed point (originally floating point) and sends the data to the FPGA via Powershell.


##Serial Interface
![Software](https://i.imgur.com/MqUs7q7.png)

     FPGA Read Write Process
         - Load bytes into local bytes array
         - Stream to FPGA using port.write()
         - Read in serial input buffer using ReadAvailable()

### Project Website
Check out our website [here][website] for more information about our project.

[website]: https://kierajcullen.github.io/-dcnn-.github.io/
