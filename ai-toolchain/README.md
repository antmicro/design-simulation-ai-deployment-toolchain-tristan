# AI toolchain for cores and accelerators based on RISC-V architecture

This directory provides the tools and examples for deploying AI models on cores and accelerators using RISC-V architecture:

* `kenning` - a framework for optimizing, deploying and evaluating AI models on various platforms, including embedded and RISC-V platforms running Linux, Zephyr RTOS and bare metal.
    * [Website](https://kenning.ai)
    * [Documentation](https://antmicro.github.io/kenning/)
    * [Tutorials](https://antmicro.github.io/kenning/kenning-gallery.html)
* `kenning-zephyr-runtime` - a [Zephyr RTOS](https://www.zephyrproject.org/) library for deploying and evaluating AI models, supporting LiteRT, TVM and IREE inference engines.
    * [Documentation](https://github.com/antmicro/kenning-zephyr-runtime)
    * [Tutorial](https://antmicro.github.io/kenning/gallery/kenning-zephyr-runtime.html)
* `kenning-bare-metal-iree-runtime` - a library for bare metal execution and evaluation of AI models on RISC-V platforms using IREE runtime.
    * [Documentation](https://github.com/antmicro/kenning-bare-metal-iree-runtime)
    * [Tutorial](https://antmicro.github.io/kenning/gallery/renode-integration-example.html)

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