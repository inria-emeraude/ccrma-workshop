# Installing syfala on Ubuntu

The Syfala toolchain is a compilation toolchain of Faust programs onto AMD-Xilinx FPGA targets. This document explains how to install and run the **version 0.7.1** of the toolchain on a Linux machine. In practice, installing the Syfala toolchain means:

- Installing the required **linux-packages**
- Installing the **Faust** compiler
- Creating a **AMD-Xilinx account** and downloading/installing the **2022.2 version** of the AMD-Xilinx toolchain (providing softwares such as Vivado, Vitis, Vitis HLS).
- Installing the additionnal **Vivado Board Files** for Digilent Boards.
- Installing *udev* rules in order to use the JTAG connection.
- Cloning the **Syfala repository**, and running a **simple example** to make sure everything is working properly.

## Dependencies

### Packages

```shell
$ sudo apt-get update
$ sudo apt-get install libncurses5 libtinfo-dev g++-multilib gtk2.0
```

### Faust

It is recommended to clone Faust from the official [github repository](https://github.com/grame-cncm/faust):

```shell
$ git clone https://github.com/grame-cncm/faust.git 
$ cd faust
$ make
$ sudo make install
```

## Vivado, Vitis & Vitis HLS (2022.2 version)

- Open an account on [https://www.xilinx.com/registration](https://www.xilinx.com/registration)
- The Xilinx download page ([https://www.xilinx.com/support/download.html](https://www.xilinx.com/support/download.html)) contains links for downloading the "Vivado Design Suite - HLx Editions - Full Product". It is available for both Linux and Windows. 

  - Download the Linux installer `Xilinx_Unified_2022.2_1014_8888_Lin64.bin`
- execute `chmod a+x Xilinx_Unified_2022.2_1014_8888_Lin64.bin`
- execute `./Xilinx_Unified_2022.2_1014_8888_Lin64.bin`

  - We suggest to use the "Download Image (Install Separately)" option. It creates a directory with a xsetup file to execute that you can reuse in case of failure during the installation
- execute `./xsetup`

  -  Choose to install **Vitis** (it will still install **Vivado**, **Vitis**, and **Vitis HLS**). 
  -  It will need 110GB of disk space: if you uncheck *Ultrascale*, *Ultrascale+*, *Versal ACAP* and *Alveo acceleration platform*, it will use less space and still work.
  -  Agree with everything and choose a directory to install (e.g. ~/Xilinx)
  -  Install and wait for hours...
- Setup a shell environment variable allowing to use the tools when necessary (add this to your `~/.bashrc`, `~/.zshrc` or whatever you're currently using, replacing `$HOME/Xilinx` by the directory you chose to install all the tools) 
  - `export XILINX_ROOT_DIR=$HOME/Xilinx`


### Installing Cable Drivers on Linux

-  go to: `$XILINX_ROOT_DIR/Vivado/2022.2/data/xicom/cable_drivers/lin64/install_script/install_drivers` directory
-  run `./install_drivers`
-  run `sudo cp 52-xilinx-digilent-usb.rules /etc/udev/rules.d`, this allows **JTAG** connection through **USB**.

### Installing Digilent Board Files

- Download the board files [here](https://github.com/Digilent/vivado-boards/archive/master.zip?_ga=2.76732885.1953828090.1655988025-1125947215.1655988024)
- Open the folder extracted from the archive and navigate to its `new/board_files` folder. You will be copying all of this folder's subfolders
- go to `$XILINX_ROOT_DIR/Vivado/2022.2/data/xhub/boards/XilinxBoardStore/boards/Xilinx`
- **Copy** all of the folders found in vivado-boards `new/board_files `folder and **paste** them into this folder

## Cloning the Syfala repository

To clone and install the latest stable version of the Syfala toolchain, you can use the following commands:

```shell
$ git clone https://github.com/inria-emeraude/syfala 
$ cd syfala
$ ./syfala.tcl install
$syfala --help
```

In order to use the Syfala toolchain to compile your first example, please report to the main [README](https://github.com/inria-emeraude/syfala/blob/main/README.md) file located in the repository's root directory.

## Troubleshooting

[...]