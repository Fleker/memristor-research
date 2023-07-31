# [Not in Name Alone: A Memristive Memory Processing Unit for Real In-Memory Processing](https://ieeexplore.ieee.org/document/8474943)
_Published in 2018_

## Notes
- mMPU: Memristive Memory Processing Unit
    - "Enormous inner parallelism"
- Von Neumann bottleneck: "memory wall"
    - "The demise of Denard scaling"
    - Moving data to DRAM is 4x more energy than the actual computation
        - “Dark Memory and Accelerator-Rich System Optimization in the Dark Silicon Era,”
- Existing PIM systems have a bottleneck in transfering data b/w memory and processing
- Brings up MAGIC as previous work
- "Another virtue of MAGIC is its ability to perform logic operations in parallel on sets of data. Due to the structure of the crossbar array, applying the operating voltage VG on any two selected columns and grounding a third column will result in NOR operations being performed on all selected rows"
- Image processing tasks
    - Extend ISA to mMPU instructions
    - Develop library akin to CUDA
- Worst case lifetime of 0.8 years
- Simulation of image classification
    - SPICE simulations

![](kvatinskylib.png)

## Summary

The authors of this paper propose a memristor-based in-memory processor that employs MAGIC to perform image classification tasks.

## Pros

The paper leverages MAGIC, which was part of previous research, and provides a series of good charts that show promising results.

## Cons

I would've liked them to spend a bit more time focusing on the software implementation. They suggest extending the ISA and building a library, but fail to discuss this in more detail or its broader implications.

## References

```
@ARTICLE{8474943,
  author={Haj-Ali, Ameer and Ben-Hur, Rotem and Wald, Nimrod and Ronen, Ronny and Kvatinsky, Shahar},
  journal={IEEE Micro}, 
  title={Not in Name Alone: A Memristive Memory Processing Unit for Real In-Memory Processing}, 
  year={2018},
  volume={38},
  number={5},
  pages={13-21},
  doi={10.1109/MM.2018.053631137}}
```
