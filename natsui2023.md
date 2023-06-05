# [Design of a nonvolatile-register-embedded RISC-V CPU with software-controlled data-retention and hardware-acceleration functions](https://www.sciencedirect.com/science/article/pii/S2773064623000129)

## Notes
- 56.9% power consumption improvement
- Power Gating
    - Retain temporary data in NVM
    - Turn off power following data xfr
- Use-case: IoT sensor nodes which use power harvesting
- Nonvolatile Flip-Flops: NVFF
- Specifically registers built on MTJ (magnetic tunneling junction)
- 55nm CMOS
- HSPICE sim

## Summary
Seeking to improve power profiles of CPUs in IoT applications, the authors developed a memory acceleration unit using power gating on top of MTJ memory cells. In doing this, they show a sizable reduction in power consumption for reading and writing to memory cells. This is verified through a SPICE simulation.

## Pros
The paper does a good job of picking a particular application, developing the necessary hardware component and showing its effectiveness.

## Cons
The paper does not go into much detail on the firmware or where this kind of research could be applied to a broader set of computing applications. Their 'future work' section was rather vague on explaining what other kinds of areas can and should be explored. A 50% reduction is a lot and trying to expand to find where the line of marginal impact would be much more interesting. The lack of firmware guidelines affects me personally but also makes me wonder if specific memory usage patterns in other applications may not yield such a significant result.

## References

```
@article{NATSUI2023100035,
title = {Design of a nonvolatile-register-embedded RISC-V CPU with software-controlled data-retention and hardware-acceleration functions},
journal = {Memories - Materials, Devices, Circuits and Systems},
volume = {4},
pages = {100035},
year = {2023},
issn = {2773-0646},
doi = {https://doi.org/10.1016/j.memori.2023.100035},
url = {https://www.sciencedirect.com/science/article/pii/S2773064623000129},
author = {Masanori Natsui and Keisuke Sakamoto and Takahiro Hanyu},
keywords = {Power gating, Internet of things, CMOS/MTJ-hybrid process, Nonvolatile CPU, Cell-level in-memory computing},
abstract = {This paper describes the design of a nonvolatile CPU based on RISC-V that is an open-source and highly flexible instruction set architecture. This CPU incorporates nonvolatile registers utilizing magnetic tunnel junction (MTJ) device, as well as custom instructions specific to the control of these nonvolatile registers and an accelerator module embedded into the CPU architecture. These techniques enable efficient execution of intermittent operations suitable for energy-limited internet-of-things (IoT) applications. Through performance evaluation of the CPU designed in a 55-nm CMOS/MTJ-hybrid process technology, we show that our CPU can save up to 56.9% of power consumption compared to conventional ones, with an average power consumption of 3.91 μW/MHz.}
}
```