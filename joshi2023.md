# [A comprehensive review on ReRAM-based accelerators for deep learning](https://ieeexplore.ieee.org/document/10153519)

## Notes
- NVM is cool but has "non-idealities"
- PUMAc
    - Custom ISA
    - Specific compiler to optimize register load
    - PUMAsim: Custom evaluation of energy and power
- TraNNsforer
    - Optimized for training
- GENIEx
    - Simulator for non-ideality

## Summary

This paper is a short review of a variety of ReRAM kinds of accelerators within the higher-level categories of "Memristive Crossbar" and "Detecting Non-Idealities". The paper summarizes a handful of examples in each case.

## Pros

This paper for me was a good introduction to a handful of accelerators in the literature. It picks about four of each and summarizes them along with providing references. It shows the benefits of each kind to enable further research.

## Cons

The authors don't do any analysis on any of the accelerators they research. They don't compare them against each other, and perhaps they are too different, but don't make any attempt at a coherent standardization of any of these topics. It would've been more valuable to provide some evaluation framework or introduce a benchmark.

## References

```
@INPROCEEDINGS{10153519,
  author={Joshi, Pooja and Rahaman, Hafizur},
  booktitle={2023 International Symposium on Devices, Circuits and Systems (ISDCS)}, 
  title={A comprehensive review on ReRAM-based accelerators for deep learning}, 
  year={2023},
  volume={1},
  number={},
  pages={01-05},
  doi={10.1109/ISDCS58735.2023.10153519}}
```
