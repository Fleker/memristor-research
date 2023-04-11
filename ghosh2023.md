# [CMOS-Based Memristor Emulator Circuits for Low-Power Edge-Computing Applications](https://www.mdpi.com/2079-9292/12/7/1654)

## Notes
- 9 MOSFETs and 1 ground cap
- Current starved interver circuit can model memristive effects
    - floating gate transistor can do hysterisis
- Part 1.2 has good benefits section
- [Knowm memristor](https://knowm.org/memristors/) commercially available
- LTSpice Sim: 16/45nm

## Summary
This paper offers a circuit design that replicates the behavior of memristors using several components.

## Pros
The authors explain their circuit design effectively.

## Cons
This is not the first circuit emulator or even the first SPICE model for memristors. They don't really interrogate their contributions.

## References

```
@Article{electronics12071654,
AUTHOR = {Ghosh, Prosenjit Kumar and Riam, Shah Zayed and Ahmed, Md Sharif and Sundaravadivel, Prabha},
TITLE = {CMOS-Based Memristor Emulator Circuits for Low-Power Edge-Computing Applications},
JOURNAL = {Electronics},
VOLUME = {12},
YEAR = {2023},
NUMBER = {7},
ARTICLE-NUMBER = {1654},
URL = {https://www.mdpi.com/2079-9292/12/7/1654},
ISSN = {2079-9292},
ABSTRACT = {In this paper, an optimized memristor emulator circuit is designed, by using nine MOSFET transistors and a ground capacitor. Our area- and power-optimized emulator circuit can be used for basic data storage and processing at the monitoring edge, in real-time applications. The memristor shows a nonlinear voltage&ndash;current relationship, but no multiplier circuit provides the memristor&rsquo;s nonlinear characteristics. As a result, the proposed memristor emulator has a very low chip area. The memristor circuit is designed in LTSpice, using 16 nm and 45 nm CMOS technology parameters, and the operating voltage is &plusmn;0.9 V. In this research, the theoretical derivations are validated using the simulated results of the memristor emulator circuit using different frequencies, capacitors, and input voltages in SPICE simulations.},
DOI = {10.3390/electronics12071654}
}
```
