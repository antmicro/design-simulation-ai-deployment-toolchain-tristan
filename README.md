# TRISTAN AI deployment and design simulation with Kenning and Renode

This repository provides resources and tools for simulating embedded RISC-V platforms with a special focus on Machine Learning applications.

## Verification and simulation of TRISTAN IPs

All projects related to the simulation, verification, coverage, and design analysis are found under [./simulation](./simulation).

To simplify the simulation of RISC-V cores, as well as to enable testing, verification and coverage analysis for RISC-V cores and the surrounding subsystems, the [Renode](https://renode.io) framework can be used.
Renode is a framework for simulating physical hardware systems, including CPUs, peripherals, sensors, and more.
It allows running software in a simulated environment, collecting the required information, and testing both the software and designs.
Renode can be easily co-simulated with Verilog models running in [Verilator](https://www.veripool.org/verilator/), [Questa](https://www.intel.com/content/www/us/en/software/programmable/quartus-prime/questa-edition.html), and other.

For the purpose of simulating Verilog/SystemVerilog models, the [Verilator](https://www.veripool.org/verilator/) framework was expanded within the TRISTAN project.

This repository provides various tools for the simulation, verification and development of Verilog/SystemVerilog modules, with a special focus on RISC-V platforms:

* [renode-dpi-examples](https://github.com/antmicro/renode-dpi-examples) - provides a sample integration between Renode and Verilog models using SystemVerilog Direct Programming Interface (DPI) calls, supporting both [Verilator](https://www.veripool.org/verilator/) and [Questa](https://www.veripool.org/verilator/) simulators.
* [renode-systemc-examples](https://github.com/antmicro/renode-systemc-examples) - provides the tools for creating Renode simulations using components written in SystemC, as well as integration samples.
* [renode-verilator-integration](https://github.com/antmicro/renode-verilator-integration) - provides sample Verilog models, and the wrapper code for co-simulation with Renode.
* [pyrenode3](https://github.com/antmicro/pyrenode3) - provides Python bindings for Renode, which allow orchestrating and analyzing the emulation from the Python level.
* [sv-bugpoint](https://github.com/antmicro/sv-bugpoint) - provides a tool for creating minimal SystemVerilog code from a larger design, based on user-defined property of the scope code.

For more details, follow the [co-simulation chapter of the Renode documentation](https://renode.readthedocs.io/en/latest/advanced/co-simulating-with-an-hdl-simulator.html).

## Deploying AI models on RISC-V CPUs and accelerators

All projects related to the deployment, optimization, and performance/quality verification of AI models are available under [./ai-toolchain/](./ai-toolchain).

To easily integrate, execute and analyze AI models on simulated or actual RISC-V cores, the [Kenning](https://kenning.ai) framework can be used.
Kenning is an AI optimization and deployment framework orchestrating the process of optimizing, compiling, deploying and evaluating models, either on real hardware or in a simulation performed in Renode.
It is highly modular, allowing both using the existing optimization techniques, and introducing new ones, including compilers, and verifying their performance in respect to RISC-V cores and AI accelerators.

Kenning consists of:

* [Kenning](https://github.com/antmicro/kenning) - the base Kenning repository, containing a toolchain for optimizing and deploying models, as well as the evaluation and report generation on the performance and quality of the compiled models.
* [Kenning Zephyr Runtime](https://github.com/antmicro/kenning-zephyr-runtime) - the Zephyr Runtime library for running and evaluating models compiled with the Kenning framework for [Zephyr RTOS applications](https://www.zephyrproject.org/).
  * Allows running models using [LiteRT](https://github.com/google-ai-edge/LiteRT), [microTVM](https://tvm.apache.org/) or [IREE](https://iree.dev/) inference engines. The support matrix for simple models and RISC-V platforms can be found in [Renode Zephyr dashboard](https://zephyr-dashboard.renode.io/).
* [Kenning Bare Metal IREE runtime](https://github.com/antmicro/kenning-bare-metal-iree-runtime) - provides the bare metal runtime for models compiled with Kenning using the [IREE](https://iree.dev/) inference engine.
  * Provides sample integration of the RISC-V accelerator called Kelvin, which is a [part of the Open Se Cura project](https://opensecura.googlesource.com/).
  * CI for the repository generates a sample [Kenning report for executing the model in a simulation, providing insight into the quality and performance of the model](https://antmicro.github.io/kenning-bare-metal-iree-runtime/).

## Blog notes

The following list of blog notes describe the work done with the above tools within the TRISTAN project:

1. [Python-driven automation and scripting in Renode with pyrenode3](https://antmicro.com/blog/2023/11/python-driven-automation-and-scripting-in-renode-with-pyrenode3)
2. [Expanding RISC-V support in Renode with Bit-Manipulation extensions](https://antmicro.com/blog/2023/12/expanding-risc-v-support-in-renode-with-bit-manipulation-extensions)
3. [Introducing code coverage reporting in Renode](https://antmicro.com/blog/2024/02/introducing-code-coverage-reporting-in-renode)
4. [Introducing constrained randomization in Verilator](https://antmicro.com/blog/2024/03/introducing-constrained-randomization-in-verilator)
5. [Defining RISC-V CPUs in Renode simulation with custom instructions and extensions](https://antmicro.com/blog/2024/06/defining-risc-v-cpus-in-renode)
6. [Constrained randomization in Verilator: SystemVerilog constraint to SMT-LIB2 conversion](https://antmicro.com/blog/2024/08/constrained-randomization-in-verilator-implementation-details)
7. [Enabling open source UVM verification of AXI-based systems in Verilator](https://antmicro.com/blog/2024/09/open-source-uvm-verification-axi-in-verilator)
8. [sv-bugpoint: pinpoint minimal bug-inducing SystemVerilog code subsets to improve debugging in Verilator and other SV tools](https://antmicro.com/blog/2024/09/sv-bugpoint-for-improved-debugging-in-sv-tools)
9. [Trace-based evaluation of CPU cache usage in Renode](https://antmicro.com/blog/2024/10/trace-based-evaluation-of-cpu-cache-usage-in-renode)
10. [Enabling complex HDL co-simulation scenarios using Renode's Direct Programming Interface support](https://antmicro.com/blog/2025/04/complex-dpi-based-hdl-co-simulation-in-renode)
11. [Enhancing RTL coverage reporting in Verilator with new features and computation optimizations](https://antmicro.com/blog/2025/08/enhancing-coverage-reporting-in-verilator)
12. [Support for upstream UVM 2017 in Verilator](https://antmicro.com/blog/2025/10/support-for-upstream-uvm-2017-in-verilator)
13. [Optimizing sv-bugpoint with speculative minimization algorithms](https://antmicro.com/blog/2026/03/optimizing-sv-bugpoint-with-speculative-minimization-algorithms)

<div>
  <picture style="vertical-align:middle">
    <source srcset="https://antmicro.com/blog/images/logos-eu.svg" media="(prefers-color-scheme: light)">
    <source srcset="https://antmicro.com/blog/images/logo-eu--dark.svg" media="(prefers-color-scheme: dark)">
    <img src="https://antmicro.com/blog/images/logos-eu.svg" alt="EU and ChipsJU logos">
  </picture>
</div>

<sub>
TRISTAN has received funding from the Chips Joint Undertaking (Chips JU) under grant agreement nr. 101095947. The Chips JU receives support from the European Union's Horizon Europe's research and innovation programmes and participating states are Austria, Belgium, Bulgaria, Croatia, Cyprus, Czechia, Germany, Denmark, Estonia, Greece, Spain, Finland, France, Hungary, Ireland, Israel, Iceland, Italy, Lithuania, Luxembourg, Latvia, Malta, Netherlands, Norway, Poland, Portugal, Romania, Sweden, Slovenia, Slovakia, and Turkey.
</sub>
