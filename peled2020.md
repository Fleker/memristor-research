# [X-MAGIC: Enhancing PIM using Input Overwriting Capabilities](https://ieeexplore.ieee.org/document/9344095)
_Published in 2020_

## Notes
- PIM: Processing In-Memory
- MAGIC: Memristor-Aided Logic (MAGIC)
    - Can do any logic with a sequence of NOT/NOR ops
 - X-MAGIC: Extended magic
    - Extending MAGIC with input overwriting (prior to execution)
    - `A * !(B+C)` and `A * !B`
    - 16% improvement compared to trad MAGIC
 - Input Overwriting
    - Replacing one of the operands with the resultant
    - Can provide more functionality and extend device lifetime
    - Existing PIM synthesis tools do not support input overwriting capabilities
    - So this paper introduces it
 - SIMPLER: Synthesis tool that does the mapping of operations to MAGIC circuit
 - Each node has no more than a single overwriting parent
 - Sequencing edge is used to order operations properly
 - Uses a single clock cycle in X-MAGIC compared to 4 in MAGIC
    - In MAGIC, you also need to init the output cell to R_{on}
    - Removing this init since you can re-use cells, you reduce the total number of writes per-op, extending device lifetime
 - X-SIMPLER: A Python-based version of SIMPLER which supports X-MAGIC
 - Estimates lifetime improvement by counting write-ops
 
 ## Summary
 
 MAGIC was seen as the canonical way to perform in-memory processing with non-volatile memory. To improve performance in some cases, the use of input overwriting can be used to reduce the number of times memory cells are being written to. This reduces the total number of cells neceessary to perform operations. A number of improvements follow.
 
 ## Pros
 
 For those interested in MAGIC, this seems like an all-around benefit. It improves performance across many magnitudes and the authors definitely put quite a bit of time that was also focused in order to make their point.
 
 ## Cons
 
 The authors focused on two particular kinds of operations in particular which are potential pain points for MAGIC, but don't elaborate in future work on what potential pitfalls may exist through input overwriting. They also create their own benchmarking software in a forked version of SIMPLER but don't really elaborate on that point. It just exists.
 
 The authors also did not make their X-SIMPLER open source from what I can tell nor offer to contribute their changes upstream. Academic software cruft can be a problem.

## References

```
@INPROCEEDINGS{9344095,
  author={Peled, Natan and Ben-Hur, Rotem and Ronen, Ronny and Kvatinsky, Shahar},
  booktitle={2020 IFIP/IEEE 28th International Conference on Very Large Scale Integration (VLSI-SOC)}, 
  title={X-MAGIC: Enhancing PIM Using Input Overwriting Capabilities}, 
  year={2020},
  volume={},
  number={},
  pages={64-69},
  doi={10.1109/VLSI-SOC46417.2020.9344095}}
```