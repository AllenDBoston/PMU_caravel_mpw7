# FPGA Programming Management Unit (PMU)

[![License](https://img.shields.io/badge/License-Apache%202.0-blue.svg)](https://opensource.org/licenses/Apache-2.0) [![UPRJ_CI](https://github.com/efabless/caravel_project_example/actions/workflows/user_project_ci.yml/badge.svg)](https://github.com/efabless/caravel_project_example/actions/workflows/user_project_ci.yml) [![Caravel Build](https://github.com/efabless/caravel_project_example/actions/workflows/caravel_build.yml/badge.svg)](https://github.com/efabless/caravel_project_example/actions/workflows/caravel_build.yml)

## Description

The Programming Management Unit will serve as a macro that can be placed near a FPGA to handle bitstream loading.
While the primary functionality of the PMU is to load a bitstream into an FPGA Core it will also incorporate some hardware security and integrity features.
This is in response to the need for OpenFPGA to be able to incorporate some hardware security IPs to FPGA designs.
To accurately access the level of protection the security features provide to the FPGA/FPGA bitstream, an iterative approach to the PMU design will be taken starting with version one. This version, submitted to MPW7 is the third version of the PMU containing AES and SHA cores.

As of today the primary objectives of the PMU are to accurately transfer FPGA bitstream data to the core and protect the IP the lies within a bitstream using AES as well as authenticating the bitstream data and user via SHA. The PMU is capable of on the fly use of both AES and SHA algorithms when transfering data from a host PC to FPGA core. This project will serve as a test implementation of the PMU where the user project wrapper includes the PMU version 3, SOFA 2x2 FPGA generated using OpenFPGA, and AES/SHA cores from secworks. Git repositories for all macros are given below.


-PMU:  https://github.com/lnis-uofu/FPGA_Secured_Bitstream

-FPGA: https://github.com/lnis-uofu/OpenFPGA

-AES:  https://github.com/secworks/aes

-SHA:  https://github.com/secworks/sha256


## TOOLS

SiliconSompiler was used to complete RTL-to-GDS flow for this project. SiliconCompiler is opensource compiler for automating source code to silicon using a Python API. 

-SiliconCompiler: https://github.com/siliconcompiler/siliconcompiler
