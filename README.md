# PhysicalDesign_Workshop
A tour to the world of Physical Design using open-sourced EDA tools

## **ABOUT:** 

This workshop basically walks us through the various steps involved in the Physical Design Flow of an SOC design, also introducing  the various open-sourced EDA tools involved in each step. It unfolds with the introduction of IC design terminologies, SOC based designs and moves forwards touching the various phases of PD flow starting from synthesis to routing and DRCs.   

## **1. Introduction to IC Design terminology and RISC-V based picoSoc:**
### 1.1 IC design terminologies: 
* **Package:** The package that is taken as an example is the QFN-48 and its size is 7mmx7mm. The QFN here, stands for Quad Flat No-leads and 48 is the total number of pins in the package.
* **Chip:** The chip mainly sits at the centre of the package. The pins of the package are connected to the chip and thus information gets transmitted to and fro from the chip and outer world.
* **Pads:** One of the components of the Chip through which information gets exchanged.
* **Die:** It is the overall area of the chip that gets manufactured on silicon wafer.
* **Core:** Its the area where all the digital logic of the chip is placed.

### 1.2 RISC-V based SOC: 
Each chip has its core, the core considered here is of RISC-V based Soc. 
RISC-V is an instruction set architecture, that helps communicating with the computer. There are many flavours of RISC-V here we will be using rv32, 32 bit instruction set. The  riscv implementation used is picorv32. The picorv32 is open-sourced and is implemented by Clifford Wolf. The picorv32 is used as a component in both picoSoc and the RavenSoc. The difference between the Raven and the pico Soc is the picoSoc is targetted towards the embedded systems and the components such as SRAM is external in RAvenSoc. 

We will be using the picorv32 design for the various stages the Physical Design Flow. 

## 2. Introduction to Open-Source EDA Tools:
### 2.1 Tools used in this workshop:
* yosys: synthesis
* graywolf: placement
* qrouter: routing
* magic: layout tool
* ngspice: circuit simultaion tool
* Opentimer and OpenSTA: STA tool

### 2.2 Introduction to Qflow:
Qflow is a complete tool chain for synthesizing digital circuits starting from verilog source and ending in physical layout for a specific target fabrication process. This tool has a GUI interface that helps connect as well as simplify the process of running synthesis, place and route also generating a specific log file for each step performed. 

For detailed information regarding the Qflow please refer [here](http://opencircuitdesign.com/qflow/) 

## 3. Synthesis 
During the synthesis phase, the .v file that is being received from the front-end design is converted to a gate level netlist. The synthesis phase is a combination of a number of steps transtation + logic optimization + technology mapping => gate level netlist
### 3.1 Lab Instances:  
#### 3.1.1 Preparation:
* technology : 180nm
* verilog source file: picorv32.v
* module name : picorv32


