# [SIMPLER MAGIC: Synthesis and Mapping of In-Memory Logic Executed in a Single Row to Improve Throughput](https://ieeexplore.ieee.org/document/8781866)
_Published in 2020_

## Notes
- Automatically converts logical operation into MAGIC NOR ops to run in memristor logic
- Use mMPU which can work as standard memory or processing memory
    - Rather than go with the standard approach of minimizing latency, here they go for maximizing throughput
    - SIMD: Single-Instruction, Multiple Data
- Could I use some stuff here to do compiler modifications for IMPLY ops?
- SIMPLER: Efficient conversion to NOR ops
    - A NOR op can cover every boolean operation
- Throughput is (number of instances)/latency
- MAGIC requires the output be initialized to `1`
- DRAM MAT: Smallest unit of DRAM physically possible (512x512 cells)
- SIMPLER tool is based on Verilog data format
     - Becomes a DAG: Directed Acyclic Graph
     - Need this in order to determine how few/many cells you need for space optimization
- Stages:
    1. Compute Cell Usage for each vertex
    2. Allocate gates to memory cells
- Run experimentally using Intel laptop
- SIMPLER does better in some contexts, worse in others

## Pros
- Good use of comparisons against other existing research
- Fair assessment of results

## Cons
- Tables are a bit hard to read, graphs too are a bit tricky to understand, mainly due to small fonts
- A lot of jargon and keywords are used in the results period which make it hard to understand
- Didn't discuss how they did the logic -> NOR. Seemed to be distinct from standard compiler behavior.

## References

```
@ARTICLE{8781866,
  author={Ben-Hur, Rotem and Ronen, Ronny and Haj-Ali, Ameer and Bhattacharjee, Debjyoti and Eliahu, Adi and Peled, Natan and Kvatinsky, Shahar},
  journal={IEEE Transactions on Computer-Aided Design of Integrated Circuits and Systems}, 
  title={SIMPLER MAGIC: Synthesis and Mapping of In-Memory Logic Executed in a Single Row to Improve Throughput}, 
  year={2020},
  volume={39},
  number={10},
  pages={2434-2447},
  doi={10.1109/TCAD.2019.2931188}}
```