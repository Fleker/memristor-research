# [MRL – Memristor Ratioed Logic](https://ieeexplore.ieee.org/document/6331426)

## Notes
- Hybrid CMOS/Memristive logic
    - OR and AND gates with memristors, NOT with CMOS
    - Material implication (IMPLY) which can be extended to a NOR gate and then MAGIC
- Memristor Ratioed Logic
    - Based on diode logic
    - Dynamic hazard until switching is complete
    - Long settling time hazard
- Built an 8-bit full adder
- References Dr. Shin "The IMPLY logic gate is extended in [[12]](https://ieeexplore.ieee.org/document/5940215) to a NOR logic gate"

## Summary
This is an early Kvatinsky paper where he hypothesizes hybrid logic systems which use memristors for specific gates and CMOS for others. To make this argument, he builts and tests an 8-bit adder using TEAM. The results suggest less space and power will be needed. Some of the paper's results are decided empirically through the design process. Overall it's a very short paper.

## Pros
- The equations are laid out pretty

## Cons
- Some of the figures are highly pixelated
- Seems too focused on hybrid logic systems rather than trying something more novel
    - No mention of in-memory computing at all

## References

```
@INPROCEEDINGS{6331426,
  author={Kvatinsky, Shahar and Wald, Nimrod and Satat, Guy and Kolodny, Avinoam and Weiser, Uri C. and Friedman, Eby G.},
  booktitle={2012 13th International Workshop on Cellular Nanoscale Networks and their Applications}, 
  title={MRL — Memristor Ratioed Logic}, 
  year={2012},
  volume={},
  number={},
  pages={1-6},
  doi={10.1109/CNNA.2012.6331426}}
```
