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
    <img src="https://antmicro.com/blog/images/logos-eu.svg" alt="ChipsJU logo">
  </picture>
</div>

<sub>
TRISTAN has received funding from the Chips Joint Undertaking (Chips JU) under grant agreement nr. 101095947. The Chips JU receives support from the European Union's Horizon Europe's research and innovation programmes and participating states are Austria, Belgium, Bulgaria, Croatia, Cyprus, Czechia, Germany, Denmark, Estonia, Greece, Spain, Finland, France, Hungary, Ireland, Israel, Iceland, Italy, Lithuania, Luxembourg, Latvia, Malta, Netherlands, Norway, Poland, Portugal, Romania, Sweden, Slovenia, Slovakia, and Turkey.
</sub>
</br></br>

---

<div>
  <picture style="vertical-align:middle">
    <source srcset="https://antmicro.com/blog/images/footer-fe-en.svg" media="(prefers-color-scheme: light)">
    <source srcset="https://antmicro.com/blog/images/footer-fe-en-dark.svg" media="(prefers-color-scheme: dark)">
    <img src="https://antmicro.com/blog/images/footer-fe-en.svg" alt="EU and NCBR logos">
  </picture>
</div>

<sub>
Project co-funded by the European Union under the CHIPS Joint Undertaking (CHIPS-JU) programme. The project is implemented as part of the National Centre for Research and Development competition: KDT Joint Undertaking Call 2021, under agreement no. KDT/2021/110/TRISTAN/2022. The project's duration is 3.5 years, with planned total cost of the implementation by the Polish applicant at 10,197,632.75 PLN and funding requested by the Polish applicant at 3,059,293.13 PLN.
</sub>