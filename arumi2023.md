# [True Random Number Generator Based on RRAM-Bias Current Starved Ring Oscillator](https://ieeexplore.ieee.org/document/10268070)

## Notes
- Current-starved ring oscillator (CSRO)
- Exploits inherent cycle-to-cycle variability of RRAM as a source of randomness
- Ring Oscillator
    - Odd-number of regular inverters
    - Alternate b/w HIGH and LOW
    - Output of one becomes the input for the next
    - Circuit delays create a particular oscillation frequency
- Current starved
    - Add a transistor
    - Control drain current
    - These delays can control the oscillation
    - They can also adjust for temperature controls
- "The unpredictable oscillation frequency of the CSRO depends on the particular (high) resistance value of the RRAM."
- "The RRAM devices considered throughout this work are TiN/Ti/HfO2/W structures. The oxide thickness is 10 nm, and the area is 15 × 15 μm2.
- Could thereotically be good for speed improvements
- Actually a good comparison table of RRAM TRNGs

## Thesis Notes
- Temperature manipulation may be one method to break the rng
    - Another is supply voltage
- Have a discussion on speed with this and related [song2023.md](song2023.md).
- Consult Table 3

## References

```
@ARTICLE{10268070,
  author={Arumí, D. and Manich, S. and Gómez-Pau, A. and Rodríguez-Montañés, R. and González, M. B. and Campabadal, F.},
  journal={IEEE Journal on Exploratory Solid-State Computational Devices and Circuits}, 
  title={True Random Number Generator Based on RRAM-Bias Current Starved Ring Oscillator}, 
  year={2023},
  volume={9},
  number={2},
  pages={92-98},
  doi={10.1109/JXCDC.2023.3320056}}
```
