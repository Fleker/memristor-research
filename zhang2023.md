# [GEM: A Generalized Memristor Device Modeling Framework Based on Neural Network for Transient Circuit Simulation](https://ieeexplore.ieee.org/document/9816013)

## Notes
- GEM: GEneralized Memristor
- Based on NN
  - Input: V/I ratio is state variable
- Use MAGIC: Memristor-Aided loGIC
  - Simulations of memristor behavior
- Lots of math
- Implemented with circuit sims, ie. SPICE
  - They write a Verilog impl
- NN trained with PyTorch. Run a flurry of samples.

## Summary
This paper presents a modeling framework that develops a model of memristors with a handful of parameters in a way similar to a neural network, which is said to be a good use case for the tech. When compared to a physics-only based model they reach something of similar accuracy. This is done in order to optimize the development time of a memristor model for circuit sims.

## Pros
This paper presents a good model that exists at the intersection of hardware and software, using physics-derived math and simulations in a transparent way to achieve their results

## Cons
The model presents this model along with a handful of additional parameters that can be tweaked, but does not spend much time explaining how they got these "magic numbers". It's possible other numbers could result in better performance, and it might be worth explaining why these numbers work the way they do.

## References
- [MAGIC](https://ieeexplore.ieee.org/document/6895258)
```
@ARTICLE{9816013,
  author={Zhang, Yuhang and He, Guanghui and Tang, Kea-Tiong and Li, Yongfu and Wang, Guoxing},
  journal={IEEE Transactions on Computer-Aided Design of Integrated Circuits and Systems}, 
  title={GEM: A Generalized Memristor Device Modeling Framework Based on Neural Network for Transient Circuit Simulation}, 
  year={2023},
  volume={42},
  number={3},
  pages={834-846},
  doi={10.1109/TCAD.2022.3188961}}
```
