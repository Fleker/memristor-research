# [(V)TEAM for SPICE Simulation of Memristive Devices With Improved Numerical Performance](https://ieeexplore.ieee.org/document/9354151)

_Published in 2021_

## Notes
- TEAM: ThrEshold Adaptive Memristor model
    - Model that is used within SPICE simulations
    - This one in particular has a current threshold
- VTEAM: Voltage ThrEshold Adaptive Memristor model
    - Two years newer (2015 v 2013) which uses voltage
- CNN: Cellular Nonlinear Network
- See [5] for Matlab and Verilog-A models
- Using window functions in ideal generic memristors can lead to computational and numerical errors, so don't do it!
- Use asymmetrical windows: `F` and its inverse `FI`
- Double-precision fp: 2^1024 (10^308) which is lower than the outputs of some window functions
    - Log-antilog to improve number behaviors in a way that isn't linear
- PSPICE cannot handle 100K memristors in the sims

## Summary

This paper discusses windowing capabilities in order to have good simualations of memristors. There's a lot of content in here. At the end they show a simulation which is able to take an image and find the edges.

## Pros

The paper is very detailed.

## Cons

The material in this paper is quite dry and detailed. There is a lot of explaining of what is being done but not as much in terms of core concepts. By the end, I was not clear on why crathis research was even necessary.

## References

```
@ARTICLE{9354151,
  author={Biolek, Dalibor and Kolka, Zdeněk and Biolková, Viera and Biolek, ZdeněK and Kvatinsky, Shahar},
  journal={IEEE Access}, 
  title={(V)TEAM for SPICE Simulation of Memristive Devices With Improved Numerical Performance}, 
  year={2021},
  volume={9},
  number={},
  pages={30242-30255},
  doi={10.1109/ACCESS.2021.3059241}}
```