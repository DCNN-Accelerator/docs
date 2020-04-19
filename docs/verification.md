# Verification

The following outlines verification of the software-hardware emulation.


# Emulation

![Verification](https://i.imgur.com/RLpDT2X.jpg)

Originally the emulation that was built had packaging issues, so a more efficient method was created in python.

This design offers users a python interface; simply give the PC an image and kernel size, MATLAB is called. The output is acquired from MATLAB and the actual value can be calculated.

    mkdocs.yml    # The configuration file.
    docs/
        index.md  # The documentation homepage.
        ...       # Other markdown pages, images and other files.


# Conv_tester

Originally, this was written in MATLAB; however, it was rewritten in python.

The code takes an image and kernel, preprocesses it to be compatible with MATLAB, with zero padding. The image can be whatever size and all of that in python, sends image and kernel to MATLAB. The python interface calls the fpga and removes zero padding. The system will check if it matches a true convolution; if it outputs valid the test passed, while invalid indicates that the test failed. Note that it failed at any of the images it would stop the whole loop.




### Project Website
Check out our website [here][website] for more information about our project.

[website]: https://kierajcullen.github.io/-dcnn-.github.io/
