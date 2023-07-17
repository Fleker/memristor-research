# [Simple magic: Synthesis and in-memory Mapping of logic execution for memristor-aided logic](https://ieeexplore.ieee.org/document/8203782)
_Published in 2017_

## Notes
- This acronym is quite awful
- Maps logic gates to memory cells for MAGIC
    - Considers itself to be the first
- "Since other works do not offer a full implementable framework, their computation latency cannot be correctly evaluated, and no relevant comparison can be performed."
- Disabled memristors: permanently high state
- Logic is represented in [Berkley Logic Interchange Format (BLIF)](https://course.ece.cmu.edu/~ee760/760docs/blif.pdf)
    - It is basically Verilog
- Modify netlist tool to generate NOTs and NORs
    - https://github.com/RotemBenHur/SIMPLE-MAGIC

## Summary
The authors introduce SIMPLE, which appears to be used in later research. It is a tool which creates optimized memristor logic systems and can improve speed of operations.

## Pros
- Handy circuit diagrams for logic gates

## Cons
- Outline the logical steps of optimization but do not just give the code directly or package it

## References

```
@INPROCEEDINGS{8203782,
  author={Ben Hur, Rotem and Wald, Nimrod and Talati, Nishil and Kvatinsky, Shahar},
  booktitle={2017 IEEE/ACM International Conference on Computer-Aided Design (ICCAD)}, 
  title={Simple magic: Synthesis and in-memory Mapping of logic execution for memristor-aided logic}, 
  year={2017},
  volume={},
  number={},
  pages={225-232},
  doi={10.1109/ICCAD.2017.8203782}}
```