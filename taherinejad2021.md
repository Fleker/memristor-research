# [SIXOR: Single-Cycle In-Memristor XOR
](https://ieeexplore.ieee.org/document/9382267)

## Notes
- One-cycle XOR
    - 4.5x speedup
    - Single-Cycle In-Memristor XOR (SIXOR)
- Stateful logic
    - Both input and output are internal state of memory element
    - Represented as the resistance of a memristor
    - The _memristance_
- Circuit diagrams
    - XOR uses 4 cells arranged in different forms
- Sims
    - Use SPICE
- Use a full adder example
- VTEAM model in SPICE
- Use quite a few memristors

## Summary

The authors present a circuit model for an XOR operator that requires several memristor and can execute end-to-end in a single cycle. The authors explain the circuit analysis of how they do this and show it in simulations.

## Pros

The authors find a small focused topic and really nail the implementation.

## Cons

Would be neat to see the next-step, integrating it into a larger ALU and observe performance changes that way.

## References

```
@ARTICLE{9382267,
  author={TaheriNejad, Nima},
  journal={IEEE Transactions on Very Large Scale Integration (VLSI) Systems}, 
  title={SIXOR: Single-Cycle In-Memristor XOR}, 
  year={2021},
  volume={29},
  number={5},
  pages={925-935},
  doi={10.1109/TVLSI.2021.3062293}}
```
