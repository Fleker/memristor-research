# [Memristor-Based Analog Recursive Computation Circuit for Linear Programming Optimization](https://ieeexplore.ieee.org/document/9094179)

## Notes
- "Compute by physics"
- First-order method: Piecemeal computations for parallelization
- Complete analog: estimated 50% energy savings in ADC<->DAC
- Recursive large-scale linear programming algos
- SPICE simulation
    - 1.2V
- Slight errors due to memristive variantions
    - But errors start averaging out at scale
- How to fix?
    - Wire resistance mitigation: farther circuit distances (but small-scale?)
    - Wider interconnects
- Seek to do power system optimization
- Large, orders of magnitude improvement to area, delay, energy dissipation

## Summary
This paper proposes a circuit design for linear algebra operations with memristors instead of pure CMOS. In doing so, they see large improvements in various forms of performance through SPICE simulations.

Using analog computation, they do run into potential errors due to hard-to-predict memristive attributes. They offer some suggestions to mitigate this.

## Pros
The simulations show quite a lot of improvement and this shows the value that analog computaions can bring. It's also important to understand the potential accuracy faults and how we can mitigate them.

## Cons
I took a grad-level Linear Algebra course a year ago and much of that has already left my mind. I don't entirely understand the algorithm they present nor the full value of computing it.

The use of all this in a circuit seems useful, though I do wonder what a balance might look like if they could employ some software behavior and a more standardized firmware implementation.

## References

```
@ARTICLE{9094179,
  author={Shang, Liuting and Adil, Muhammad and Madani, Ramtin and Pan, Chenyun},
  journal={IEEE Journal on Exploratory Solid-State Computational Devices and Circuits}, 
  title={Memristor-Based Analog Recursive Computation Circuit for Linear Programming Optimization}, 
  year={2020},
  volume={6},
  number={1},
  pages={53-61},
  doi={10.1109/JXCDC.2020.2995123}}
```
