# [Full CMOS Circuit for Brain-Inspired Associative Memory With On-Chip Trainable Memristive STDP Synapse](https://ieeexplore.ieee.org/document/10113135)

## Notes
- SNN: Spiking Neural Network
    - Said to be the most "bioplausible"
    - 2 Spiking WTA (Winner Take All) cells for storing patterns
- BAM: Bidirectional Associtaive Memory
- HNN: Hopfield Neural Network
- CBNN: Clique-Based Neural Network
- ANN: Artificial Neural Network
- STDP: Spike-Timing-Dependent Plasticity
- NAM: Neural-Associative Memory
- Most memristor NN models are missing properties of retention and electroforming modeling
    - Also too ideal, don't include varying thresholds, stochastic switching, and variable resistance states

## Summary
The authors perform some hybrid circuit design in order to achieve neural-network related computing. In particular they go beyond the existing theoretical "leave the rest as an exercise for the reader" by building out the remaining circuit elements surrounding the memristors in order to show a more complete example. They test their circuit model in various circumstances like temperature in order to assess accuracy under physical stress.

## Pros
The authors did a good job of providing a thorough look at neural-networks for memristors. The wide range of tests do show a commitment to thoroughness.

## Cons
The extra work that the authors did is neat, but they do not do a great job of explaining how necessary they are. They put the circuit under various conditions based on temperature and it didn't really yield and big result. Having non-results in a report are good in general, though I do question how many of their experiments had to be done or if they are just throwing a lot of spaghetti at the wall. Plus they were mainly concerned with accuracy in their tests rather than comparing to alternative NN architectures for metrics like performance.

Also, the authors' graphs and tables are a bit dense and could do with some improved formatting to make them a bit more accessible.

## References

```
@ARTICLE{10113135,
  author={Vohra, Sahibia Kaur and Thomas, Sherin A. and Shivdeep and Sakare, Mahendra and Das, Devarshi Mrinal},
  journal={IEEE Transactions on Very Large Scale Integration (VLSI) Systems}, 
  title={Full CMOS Circuit for Brain-Inspired Associative Memory With On-Chip Trainable Memristive STDP Synapse}, 
  year={2023},
  volume={31},
  number={7},
  pages={993-1003},
  doi={10.1109/TVLSI.2023.3268173}}
```