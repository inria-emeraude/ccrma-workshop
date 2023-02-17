
## Real-Time Audio DSP on FPGA 

The goal of this hands-on workshop is to discover **Syfala**: the first open-source audio DSP compiler targeting **FPGAs** using the **Faust programming language**.

*Field-Programmable Gate Arrays* (FPGAs) provide unparalleled audio latency and computational power. This makes them a better fit for real-time audio processing than traditional CPUs for many applications.
However, programming them is extremely complex and out of reach to non-specialized engineers as well as to most people in the audio community. That's where Faust comes to the rescue!

**Programming FPGAs with Faust** (which is an accessible programming language for real-time sound synthesis and audio processing) will allow you to explore new audio DSP applications potentially involving hundreds of audio channels, ultra-low audio latency, etc.

Using a **Zybo ARM/FPGA SoC Development Board** which can be provided to you as part of a lab kit, you will learn how to easily program your own Faust audio signal processing applications on an embedded Linux environment offering the unmatched performances of an FPGA.

## Covered topics
During this course, as an introduction to FPGAs, we will first describe in details **the ins and outs of this platform**: how they work, their general purpose, and why they are a great fit for audio hardware and software development.
We will dive in audio development on FPGAs using Syfala to **compile our first baremetal audio programs from regular Faust DSP code**. We will then generate a graphical user interface (GUI) to control it in real-time.
Finally, we will demonstrate how to **build and use a custom-made embedded Linux distribution directly on the board**. This will allow us to use more advanced control protocols such as **MIDI**, Open Sound Control (**OSC**), **HTTP**, etc.

By the end of the workshop, you should have a good understanding of the possibilities that such a platform affords in the context of real-time audio processing.

## Instructors
- [Maxime Popoff](mailto:maxime.popoff@insa-lyon.fr)
- [Pierre Cochard](mailto:pierre.cochard@inria.fr) -- Research engineer, team Emeraude -- INRIA Lyon (France)

Feel free to contact us for any additional information !

## Requirements

This workshop is intended for musicians, makers, engineers, computer  scientists, etc. Previous background in computer programming and sound synthesis/processing is preferred.

### Hardware 

Participants should bring their own laptop. The following elements - which can be purchased for them and added to the registration fee - are also required for the workshop: 

- a **Digilent Zybo Z7-10 or Z7-20** ARM/FPGA SoC Development Board
  - an external 5V / 1.25A **power source**
  - a **microUSB-USB cable**
  - a 4GB (minimum) **micro SD card** required for the embedded Linux 
- an **USB-MIDI controller**, with at least a few knobs and keys or pads.

### Software

During the workshop, we will extensively use the **AMD-Xilinx 2022.2 toolchain**. If you have one of the operating systems listed below already installed on your machine, feel free to install the toolchain by yourself prior to the workshop, following the instructions provided [here](syfala-installation.md):

- **Ubuntu** >= 18.04
- **Linux Mint** >= 19 

For any **other operating system** (including other Linux distributions, but also macOS or Windows), **a container-image can be provided**, it will require the installation of an **OCI-compliant software** on your machine, such as:

-  **podman** (multi-platform, installation instructions are available [here](https://podman.io/getting-started/installation))
- **docker** (multi-platform, installation instructions are available [here](https://docs.docker.com/get-docker/))
