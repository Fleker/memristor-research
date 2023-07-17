# [Supporting the Momentum Training Algorithm Using a Memristor-Based Synapse](https://ieeexplore.ieee.org/document/8600725)
_Published in 2019_

## Notes

- SGD: Stochastic Gradient Descent
- DNN: Deep Neural Network
- Working on a mechanism to do this directly as a hardware capability
    - Perf 886x better, 7x less energy
- Memristor NNs
    - Mem cell acts as a synapse
    - Mem cell stores the weight
    - Synapse array can perform multiplications
- In 2015, they published “Memristor-based multilayer neural networks with online gradient descent training,”
    - Have made some improvements since then
- Evaluate circuit designs with VTEAM
    - 180nm node in Cadence Virtuoso
    - 2 DNN based on MNIST in PyTorch
    - 325x faster than GPU, 866x faster in the memory
    - High parallelization
- Higher resistance can improve overall accuracy of storing the data we expect

## Summary
The authors propose novel circuit designs in order to achieve better performance for in-hardware DNN training. They are successful.

## Pros
- Very good background section on DNNs generally
- Thorough research

## Cons
- They use MNIST for training but by 2019 there were more datasets that could present a larger challenge

## References

```
@ARTICLE{8600725,
  author={Greenberg-Toledo, Tzofnat and Mazor, Roee and Haj-Ali, Ameer and Kvatinsky, Shahar},
  journal={IEEE Transactions on Circuits and Systems I: Regular Papers}, 
  title={Supporting the Momentum Training Algorithm Using a Memristor-Based Synapse}, 
  year={2019},
  volume={66},
  number={4},
  pages={1571-1583},
  doi={10.1109/TCSI.2018.2888538}}
```