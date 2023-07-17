# [Stateful Logic Using Phase Change Memory](https://ieeexplore.ieee.org/document/9938984)
_Published at the end of 2022_

## Notes
- Stateful logic is a processing in-memory (PIM) technique
    - Input / output are represented in terms of resistance
    - Output is written directly into cell
- mMPU: _m_emristive Memory Processing Unit
- RACER: Resistance Accelerted Computation for Energy Reduction
    - High performance, compatible with Von Neumann
- Input-Output transfer: three consecutive pulses to perform an AND
- Propose new method to do several logic gates
- IRL tests with a Keysight oscilloscope

## Summary
The use of PCM has not always been effective in performing PIM despite its other good properties. In this hands-on experiment, several logic gates have been created and tested to show that it can actually work well.

## Pros
- Real electrical tests
- Good diagrams and explanations for circuits

## Cons
- Missed opportunity to discuss software implications. Use the same libraries? Update compiler?

## References

```
@ARTICLE{9938984,
  author={Hoffer, Barak and Wainstein, Nicolás and Neumann, Christopher M. and Pop, Eric and Yalon, Eilam and Kvatinsky, Shahar},
  journal={IEEE Journal on Exploratory Solid-State Computational Devices and Circuits}, 
  title={Stateful Logic Using Phase Change Memory}, 
  year={2022},
  volume={8},
  number={2},
  pages={77-83},
  doi={10.1109/JXCDC.2022.3219731}}
```