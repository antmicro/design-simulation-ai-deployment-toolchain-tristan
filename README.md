# TRISTAN AI deployment and design simulation with Kenning and Renode

This repository provides resources and tools for simulating embedded RISC-V platforms with a special focus on Machine Learning applications.

## Verification and simulation of TRISTAN IPs

For simplifying simulation of RISC-V cores, as well as enabling testing, verification and coverage analysis for RISC-V cores and surrounding subsystems, [Renode](https://renode.io) framework can be used.
Renode is a simulation framework allowing to simulate physical hardware systems including CPUs, peripherals, sensors and more.
It allows running software in the simulated environment, collect needed information and test both software and designs.
It can be easily co-simulated with Verilog models running in [Verilator](https://www.veripool.org/verilator/), [Questa](https://www.veripool.org/verilator/) and more.

This repository provides examples for such integrations:

* [renode-dpi-examples](https://github.com/antmicro/renode-dpi-examples) - provides example integration between Renode and Verilog model using SystemVerilog Direct Programming Interface (DPI) calls, supporting both [Verilator](https://www.veripool.org/verilator/) and [Questa](https://www.veripool.org/verilator/) simulators.
* [renode-systemc-examples](https://github.com/antmicro/renode-systemc-examples) - provides tools for creating Renode simulations using components written in SystemC, as well as examples of integration.
* [renode-verilator-integration](https://github.com/antmicro/renode-verilator-integration) - provides sample Verilog models as well as wrapper code for co-simulation with Renode.

For more details, follow [co-simulation chapter of the Renode documentation](https://renode.readthedocs.io/en/latest/advanced/co-simulating-with-an-hdl-simulator.html).

## Deploying AI models on RISC-V CPUs and accelerators

For easy integration, execution and analysis of AI models on simulated or actual RISC-V cores the [Kenning](https://kenning.ai) framework can be used.
Kenning is an AI optimization and deployment framework orchestrating the process of optimizing, compiling, deploying and evaluating models, either on real hardware or in simulation done with Renode.
It is highly modular, allowing to both use existing and introduce new optimization techniques, as well as compilers and verify their performance with regard to RISC-V cores and AI accelerators.

Kenning consists of:

* [Kenning](https://github.com/antmicro/kenning) - base Kenning repository, containing toolchain for optimizing and deploying models, as well as evaluation and report generation on the performance and quality of compiled models
* [Kenning Zephyr Runtime](https://github.com/antmicro/kenning-zephyr-runtime) - Zephyr Runtime library for running and evaluating models compiled with Kenning framework for [Zephyr RTOS applications](https://www.zephyrproject.org/).
  Allows to run models using [LiteRT](https://github.com/google-ai-edge/LiteRT), [microTVM](https://tvm.apache.org/) or [IREE](https://iree.dev/) inference engines.
  The support matrix for simple models and RISC-V platforms can be found in [Renode Zephyr dashboard](https://zephyr-dashboard.renode.io/).
* [Kenning Bare Metal IREE runtime](https://github.com/antmicro/kenning-bare-metal-iree-runtime) - provides bare metal runtime for models compiled with Kenning using [IREE](https://iree.dev/) inference engine.
  Provides example integration of the [RISC-V accelerator called Kelvin, which is part of Open Se Cura project](https://opensecura.googlesource.com/).
  CI for the repository generates a sample [Kenning report for execution of the model in simulation providing details on quality and performance of the model](https://antmicro.github.io/kenning-bare-metal-iree-runtime/).

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
