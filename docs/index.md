<img src="banner50p.jpg" alt="banner"  width="100%"/>

# Real-Time Audio DSP on FPGA
<p style="text-align:center;">
<button type="button"  onclick="window.location.href='https://www.eventbrite.com/e/real-time-audio-dsp-on-fpga-tickets-616586997307?aff=ebdsoporgprofile';">  Click Here to REGISTER  </button>
</p>

The goal of this *hands-on workshop* is to discover the **programming of FPGAs** for **real-time audio Digital Signal Processing (DSP) applications**.
It focuses in particular on the **[Syfala](https://github.com/inria-emeraude/syfala)** toolchain: the first open-source audio DSP compiler targeting **FPGAs** using the **[Faust programming language](https://faust.grame.fr/)**.

## Description

*Field-Programmable Gate Arrays* (FPGAs) provide unparalleled **audio latency** and **computational power**. This makes them a better fit for real-time audio processing than traditional CPUs for many applications.

These embedded platforms can easily handle audio DSP programs with *hundreds of channels* while guaranteeing *very low latency*. This allows for the design of systems with unmatched performances and unique features for *spatial audio, noise cancelling or active control of room acoustics*. For example, the combination of a large number of microphones and speakers with ultra-low latency could allow us to actively modify the acoustical properties of rehearsal spaces, concert halls, etc.

However, programming FPGAs is very **complex** and out of reach to non-specialized engineers as well as to most people in the audio community. That's where **Faust** comes to the rescue!

**Faust** is a *functional programming language* for sound synthesis and audio processing with a strong focus on the design of synthesizers, musical instruments, audio effects, etc.

**Programming FPGAs with Faust** will allow us to explore the power of this platform while leveraging an *accessible programming language* that's widely used within the audio community.

Using a **Zybo ARM/FPGA SoC Development Board** which will be provided as part of a lab kit, you will learn how to easily program your own Faust audio signal processing applications on an embedded FPGA board.

## Covered topics

During this course, as an **introduction to FPGAs**, we will first describe in details *the ins and outs of this platform*: how they work, their general purpose, and why they are a great fit for audio hardware and software development.

We will go trough the understanding of **FPGA design flow** by programming some basic *VHDL functions* and intergate them to the *block design* with [Xilinx Vivado](https://www.xilinx.com/products/design-tools/vivado.html).

Then, we will dive into audio development on FPGAs using Syfala to *compile* our first baremetal audio programs from regular **Faust DSP code**, and generate a graphical user interface (GUI) to control it in real-time.
This will go through an in-depth analysis of the **High Level Synthesis (HLS)** tools with *Vitis HLS*.

Finally, we will demonstrate how to build and use a custom-made **embedded Linux** distribution directly on the board. This will allow us to use more advanced control protocols such as **MIDI**, Open Sound Control (**OSC**), **HTTPD**, etc.

By the end of the workshop, you should have a good understanding of the possibilities that such a platform affords in the context of real-time audio processing.

## Instructors

- [Maxime Popoff](https://profiles.stanford.edu/maxime-popoff?releaseVersion=10.5.1) -- Computer Science and Embedded Systems PhD Student, Emeraude Team -- INSA Lyon (France)
- [Pierre Cochard](mailto:pierre.cochard@inria.fr) -- Research engineer, Emeraude Team -- Inria Lyon (France)

Feel free to contact us for any additional information!

## Requirements

This workshop is intended for engineers, computer scientists, musicians, makers, etc. Previous background in computer programming and sound synthesis/processing is preferred. No previous background in FPGA programming is needed.

### Hardware

Participants must bring their own laptop.
The following elements will be included in the lab kit:

- **Digilent Zybo Z7-10** ARM/FPGA SoC Development Board
- External 5V 2.5A+ power source
- Micro USB-USB cable
- 4GB micro SD card

### Software

During the workshop, we will extensively use the **AMD-Xilinx 2022.2 toolchain**. If you have a **debian-based** operating system (Ubuntu, Linux Mint...) already installed on your machine, feel free to install the toolchain by yourself prior to the workshop, following the instructions provided [here](syfala-installation.md).

For **any other Linux distributions**, but also *macOS* (**x86**), a container-image can be provided, it will **require the installation of one of these two softwares**:

- **podman** (multi-platform, installation instructions are available [here](https://podman.io/getting-started/installation))
- **docker** (multi-platform, installation instructions are available [here](https://docs.docker.com/get-docker/))

Unfortunately, **Syfala containers** are at the moment **not working on ARM-based macOS** systems, and have **not been tested on Windows**.


###[Resources](resources.md)

---

## Registrations

[Follow this link](https://www.eventbrite.com/e/real-time-audio-dsp-on-fpga-tickets-616586997307?aff=ebdsoporgprofile) to register.
**Registrations are open until May 15, 2023.**

PLEASE NOTE: This workshop is subject to cancellation if there is not sufficient enrollment by May 15, 2023.

---
<img src="banner50_btm.jpg" alt="banner" width="100%" />
<center>
<p>
    <a href="https://www.inria.fr"><img src="logo/inria-logo.png" width="20%"></a>
    <a href="https://www.grame.fr"><img src="logo/grame-logo.svg" width="20%"></a>
    <a href="https://www.insa-lyon.fr/en/"><img src="logo/logoInsa.png" width="20%"></a>
    <a href="https://ccrma.stanford.edu"><img src="logo/ccrmaLogo.svg" width="20%"></a>
</p>
</center>
