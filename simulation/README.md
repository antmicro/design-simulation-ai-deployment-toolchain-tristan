# Simulation, verification and coverage tooling for TRISTAN

This directory contains the tools for simulation, verification and coverage used in TRISTAN project:

* `renode` - framework for simulating hardware platforms and peripherals.
    * [Website](https://renode.io/)
    * [Documentation](https://renode.readthedocs.io/en/latest/)
    * [Tutorials](https://renode.io/tutorials/)
    * [Blog notes](https://renode.io/news/)
* `verilator` - framework for simulating Verilog and SystemVerilog.
    * [Website](https://www.veripool.org/verilator/)
    * [Documentation](https://verilator.org/guide/latest/)
* `renode-systemc-examples` - repository with tools and examples of creating Renode simulations using components written in SystemC.
    * [Documentation](https://github.com/antmicro/renode-systemc-examples/)
* `renode-dpi-examples` - repository with examples of integrating SystemVerilog Direct Programming Interface (DPI) calls in Renode.
    * [Documentation](https://github.com/antmicro/renode-dpi-examples)
* `renode-verilator-integration` - repository with sample Verilog models and wrapper code for co-simulation with Renode and Verilator.
    * [Documentation](https://renode.readthedocs.io/en/latest/advanced/co-simulating-with-an-hdl-simulator.html)
* `pyrenode3` - repository with Python bindings for Renode, for controlling the simulation from the Python script level.
    * [Documentation](https://github.com/antmicro/pyrenode3)
* `sv-bugpoint` - a bugpoint equivalent for creating minimized SystemVerilog code while preserving a user-defined property of given code.
    * [Documentation](https://github.com/antmicro/sv-bugpoint)

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

