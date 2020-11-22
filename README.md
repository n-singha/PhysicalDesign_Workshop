# PhysicalDesign_Workshop
A tour to the world of Physical Design using open-sourced EDA tools

## **ABOUT:** 

This workshop basically walks us through the various steps involved in the Physical Design Flow of an SOC design, also introducing  the various open-sourced EDA tools involved in each step. It unfolds with the introduction of IC design terminologies, SOC based designs and gradually moves forwards touching the various phases of PD flow.   

## **1. Introduction to IC Design terminology and RISC-V based picoSoc:**
### 1.1 IC design terminologies: 
* **Package:** The package that is taken as an example is the QFN-48 and its size is 7mmx7mm. The QFN here, stands for Quad Flat No-leads and 48 is the total number of pins in the package.
* **Chip:** The chip mainly sits at the centre of the package. The pins of the package are connected to the chip and thus information gets transmitted to and fro from the chip and outer world.
* Pads: One of the components of the Chip through which information gets exchanged.
* Die: It is the overall area of the chip that gets manufactured on silicon wafer.
* Core: Its the area where all the digital logic of the chip is placed.

### 1.2 RISC-V based SOC: 
Each chip has its core, the core considered here is of RISC-V based Soc. 
RISC-V is an instruction set architecture, in broader terms it is basically that helps communicate with the computer. 
There are many flavours of RISC-v here we will be using rv32, 32 bit instruction set. riscv implementation used is picorv32.(see)
picosoc overview: targeted towards embedded systems. 

## 2. Introduction to Open-Source EDA Tools: 
### 




