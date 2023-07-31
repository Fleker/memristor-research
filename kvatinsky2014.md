# [Memristor-Based Multithreading](https://ieeexplore.ieee.org/document/6489970)
_Published in 2014_

## Notes
- SoE MT: Switch on Event Multithreading will swap threads when one thread hits a stall (such as cache miss)
- CFMT: Continuous Flow Multithreading 
- MPR: Multistate Pipeline Register
    - Holds the state of each thread including pipeline state
    - No need to flush a bunch of steps
- Fine-grain multithreading works at scale but may not be practical. Intel CPUs support two threads.
- Each MPR can store N thread states, one per bit.
- Thread switch time depends on the MPR HW speed
    - CFMT costs ~3 clock cycles compared to 8 for SoE MT
    - Switching time now depends on the MPR read time
    - Preliminary simulations done on **Gem5**
- "[23] Private discussion with Ronny Ronen, Intel."
    
## Summary

In this paper, the authors propose a multithreading solution using a small number of memristor cells of N bits in order to store and restore the state effectively. This shows promise in speeding up multithread PCs.

## Pros

It's good to see a Gem5 reference in here. I can see the value of this technology integrated into all kinds of computers to improve multithreading, which is already common. The benefits are clear.

## Cons

While the paper mentions Gem5, it's just at the end as an aside. They don't really talk more about how they do it. There's a graph right at the end as well but there's not much discussion about it. It would've been useful to speak more to the firmware that is being performed, and for a firmware paper there's not much in the way of diagrams or flowcharts.

## References

```
@ARTICLE{6489970,
  author={Kvatinsky, Shahar and Nacson, Yuval H. and Etsion, Yoav and Friedman, Eby G. and Kolodny, Avinoam and Weiser, Uri C.},
  journal={IEEE Computer Architecture Letters}, 
  title={Memristor-Based Multithreading}, 
  year={2014},
  volume={13},
  number={1},
  pages={41-44},
  doi={10.1109/L-CA.2013.3}}
```
