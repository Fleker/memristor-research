# [End-to-End Benchmarking of Chiplet-Based In-Memory Computing](https://www.intechopen.com/online-first/87463)

## Notes
- This is an open-access, peer-reviewed chapter of a book on Neuromorphic Computing
    - Includes _111_ citations
- Discuss using SRAM or RRAM memory cells
- RRAM IMC
    - RRAM at each crosspoint in the crossbar array
    - Can read at <= 0.4V. Any higher and it flips into writing.
    - Studies show 100-1000x improvement in energy efficiency
- Chiplets: Integrating multiple small chips on a single die
    - Area of each is smaller compared to a singular chip, so higher yield and smaller costs
- NoP: Network on-package
    - Kite is one family for common applications
    - SIMBA is a chiplet system for deep learning (36-chips)
- Evaluate with NeuroSim: considers various metrics
- SIAM: Another benchmarking simulator for IMC chiplet architectures

## Summary
The authors of this book chapter introduce contemporary AI application architectures which then leads into the use of in-memory computing combined with chiplets to achieve specific performance benchmarks along with a few prescribed tools to evaluate them.

## Pros
The authors do a reasonable job of introducing the topics, as would be expected by a book. The diagrams do a good job of explaining each subtopic in an approachable way.

## Cons
The scope of a book may mean that each point is underdiscussed. While RRAM is brought up, the authors really do not spend any time examining non-volatile memory beyond small references. While their benchmark section seemed valuable, it spent more time on SIAM in particular in a way that was less academic and more of an instruction manual. It's unclear what will happen once the content becomes inevitably outdated.

## References

```
@incollection{Krishnan23,
author = {Gokul Krishnan and Sumit K. Mandal and A. Alper Goksoy and Zhenyu Wang and Chaitali Chakrabarti and Jae-sun Seo and Umit Y. Ogras and Yu Cao},
title = {End-to-End Benchmarking of Chiplet-Based In-Memory Computing},
booktitle = {Neuromorphic Computing},
publisher = {IntechOpen},
address = {Rijeka},
year = {2023},
editor = {Prof. Yang Yi and Dr. Hongyu An},
chapter = {4},
doi = {10.5772/intechopen.111926},
url = {https://doi.org/10.5772/intechopen.111926}
}
```
