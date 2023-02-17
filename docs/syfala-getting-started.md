## Getting started

### Hardware setup (Digilent **Zybo-Z7-10/20** boards)

- [ ] Jumper **JP5** should be on *JTAG* 
- [ ] **Power select** jumper should be on *USB*  
- [ ] **Switches** SW0, SW1, SW2, SW3 should be **down**  
- [ ] The **audio input** is **LINE IN** (blue), not MIC IN  
- [ ] The **audio output** is the black **HPH OUT** jack  

### Software

Building a simple example for the **default board** (Digilent Zybo **Z7-10)**:

```shell
$ syfala examples/virtualAnalog.dsp
```

This will run the **full syfala toolchain** on the virtualAnalog.dsp **Faust** file, which will then be ready to be flashed on the board. Y**ou can specify the targeted board** using the `-b (--board)` option:

```shell
$ syfala examples/virtualAnalog.dsp --board Z20
$ syfala examples/virtualAnalog.dsp --board GENESYS
```

You can now **connect the board** to your computer with the proper **USB/Serial port cable** and run the `flash` command:

```shell
$ syfala flash
```

The board's **RGB LED** should then become **green** after a few seconds, indicating that your program is running. You can now **start the Faust GUI application**, which will display a set of sliders/knobs/buttons and **update the DSP parameters in real-time through USB-UART**:

```shell
$ syfala gui
```

### Exporting and re-importing your builds

When you're done playing with your program, you can **save and export it** as a `.zip` file with the following command:

```shell
$ syfala export my-virtual-analog-build
# the exported .zip file is tagged with date & time, e.g.:
>> "export/2022-02-17-my-virtual-analog-build.zip"
```

The resulting `.zip` file is now available in the repository's `export` directory, you can **re-import** it by typing:

```shell
$ syfala import export/2022-02-17-my-virtual-analog-build.zip
```

### Making another build

Before building another DSP program, please **make sure you have saved and exported your previous build** beforehand, otherwise **it will be overwritten** whenever you start a new build. 

```shell
# Clean build directory & start another build:
$ syfala clean
$ syfala examples/my-new-dsp-build.dsp
# Both commands can also be combined by adding the '--reset' flag 
$ syfala examples/my-new-dsp-build.dsp --reset
```

## Going further

Please report to the [reference](syfala-reference.md) for more information on available **commands**, **options** and documentation.