# AXI slave streaming interface to LED

This repo contains scripts to recreate a Vivado IP block that connects an LED to an AXI slave streaming interface. The project is setup for Zedboard, although it would be easy to change to other boards assuming you have some basic TCL skills.

# Module/IP design

Describe here your module interface and protocols.

![Place here a nice picture of your design](my-awesome-module.png)

# How to run it

These scripts are assuming Linux operation system (Ubuntu 18.04) and Vivado 2018.2.

Follow these instructions to recreate the Vivado and SDK projects:
 - Open the **build.sh** script and edit the first two lines to setup the environment variables 
**VIVADO**, **VIVADO_DESIGN_NAME**, **XIL_APP_NAME**, and **VIVADO_TOP_NAME** (optional). 
 - run *build.sh*

These scripts will recreate the entire Vivado project, compile the design, generate the bitstream, export the hardware to SDK, create the SDK projects, import the source files, build all projects, and finally download both the bitstream and the elf application. Hopefully, all these steps will be executed automatically.

# How to update the scripts

These scripts come from a template repository and they get updated and improved over time. If you wish to get the latest script version, then follow these steps:

```
git remote add template https://github.com/amamory/vivado-base-project.git
git fetch --all
git merge --no-commit --no-ff template/master --allow-unrelated-histories
```

Solve any conflict manually and then commit.

# Future work

 - update the scripts to Vitis
 - support or test with Windows (help required !!! :D )

# Credits

The scripts are based on the excellent scripts from [fpgadesigner](https://github.com/fpgadeveloper/zedboard-axi-dma) plus few increments from my own such as project generalization, support to SDK project creation and compilation and other minor improvements. 
