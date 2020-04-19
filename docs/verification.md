# Verification

The following outlines verification of the software-hardware emulation. Hardware emulation is a tool for hardware/software co-verification and testing the integration of hardware and software.


# Emulation

Originally the emulation that was built had packaging issues, so a more efficient method was created in python.

This design offers users a python interface; simply give the PC an image and kernel size, MATLAB is called. The output is acquired from MATLAB and the actual value can be calculated.

# Conv_tester

Originally, this was written in MATLAB; however, it was rewritten in Python.

The script takes an image and kernel, preprocesses it to be compatible with MATLAB, with zero padding. The image can be whatever size and all of that in Python, sends image and kernel to MATLAB. The Python interface calls the FPGA and removes zero padding. An image and a kernel are loaded, preprocessed, and finally, the MATLAB-based implementation is called and our FPGA Convolution algorithm performs image filtering. The results are validated using SciPy, and asserts.

"True" when the convolution passes, and "False" when the convolution from MATLAB does not match the SciPy convolution.

The system will check if it matches a true convolution; if it outputs valid the test passed, while invalid indicates that the test failed. Note that if the script fails at any of the images, the loop will stop.

For thorough testing, we will be loading in 1000 images from the CIFAR-10 image dataset

##Conversion to Greyscale
![Verification](https://i.imgur.com/8aw60lC.jpg)
The user provides the script with dimensions and metrics, it takes in an image, which is converted to greyscale.

##Verify with MATLAB Output
![Verification](https://i.imgur.com/akozTpc.jpg)
Computes the ground truth correlation and checks the MATLAB output for similarity based on a tolerance.



### Project Website
Check out our website [here][website] for more information about our project.

[website]: https://kierajcullen.github.io/-dcnn-.github.io/
