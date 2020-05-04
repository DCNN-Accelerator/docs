# Build Your Own DCNN
The following document describes how to get started and build your own deep learning convolutional neural network.

## Step 1
Download the folder from GitHub and extract the zip.
(Which folder ask ryan)

## Step 2
Open powershell and run:

    $env:PATH = $env:PATH + ";C:\Xilinx\Vivado\2018.2\bin"

This adds Vivado to the environment path and runs Vivado.

## Step 3
Run

    echo $env:PATH

Ensure that vivado is added into the environment path.

## Step 4
    cd C:\Users\user\Downloads\518\BUILD

Change directory into the downloaded folder.

## Step 5
    vivado -mode tcl

This will open up Vivado in tcl mode.

## Step 6
In vivado tcl mode run:

    source top.tcl

This builds the entire project for 518 x 518 image convolution (The real image size is 512 x 512 with 0 padding).

### Project Website
Check out our website [here][website] for more information about our project.

[website]: https://kierajcullen.github.io/-dcnn-.github.io/
