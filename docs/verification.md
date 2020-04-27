# Verification

The following outlines verification of the software-hardware emulation. Hardware emulation is a tool for hardware/software co-verification and integration testing.

![Verification](https://i.imgur.com/jZEoaMi.png)

Baby Yoda was the first image successfully tested (using 512x512 dimensions).

##Overview
![Verification](https://i.imgur.com/6aIxdKL.jpg)&nbsp;

## Emulation

Originally the emulation that was built had packaging issues, so a more efficient method was created in python.

This design offers users a Python interface; simply give the PC an image and kernel size, MATLAB is called. The output is acquired from MATLAB and the actual value can be calculated.

## Conv_tester

Originally, this was written in MATLAB; however, it was rewritten in Python.

This MATLAB-based implementation is called and our FPGA Convolution algorithm performs image filtering. This script loads an image and a kernel, preprocesses them, and then calls the MATLAB-based implementation
of our FPGA Convolution algorithm to perform image filtering. The results are validated using SciPy, and asserts.

For thorough testing, we loaded in 1000 images from the CIFAR-10 image dataset.

###Import Libraries
![Verification](https://i.imgur.com/duYINvl.png)&nbsp;

### Conversion to Greyscale
The user provides the script with dimensions and metrics, it takes in an image, which is converted to greyscale.

![Verification](https://i.imgur.com/8aw60lC.jpg)&nbsp;

### Verify with MATLAB Output
Computes the ground truth correlation and checks the MATLAB output for similarity based on a tolerance.

![Verification](https://i.imgur.com/akozTpc.jpg)&nbsp;

### Load Image, Preprocesses and Zero Pads
![Verification](https://i.imgur.com/8tWmQsd.jpg)&nbsp;

### Exporting to MATLAB
The first lines generates the edge detection kernel. The image and array is saved to text files. Finally, the image and kernel arrays are loaded into MATLAB.

![Verification](https://i.imgur.com/XoVBljG.png)&nbsp;

### Test the FPGA Convolution Algorithm
The script will call [FPGA_Runner.m](fpga) from MATLAB to test the algorithm.

[fpga]: https://github.com/DCNN-Accelerator/verification/blob/master/emulation/util/FPGA_Runner.m

![Verification](https://i.imgur.com/1sljins.png)&nbsp;


### Pass/Fail Test
"True" when the convolution passes, and "False" when the convolution from MATLAB does not match the SciPy convolution.

![Verification](https://i.imgur.com/p5gtsmQ.png)

The system will check if it matches a true convolution; if it outputs valid the test passed, while invalid indicates that the test failed. Note that if the script fails at any of the images, the loop will stop.


## Project Website
Check out our website [here][website] for more information about our project.
[website]: https://kierajcullen.github.io/-dcnn-.github.io/
