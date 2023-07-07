# [Design and simulation of memristor-based neural networks](https://arxiv.org/abs/2306.11678)

## Notes
- This is a very long document. It clocks in at 36 pages in total. It's a bachelor's thesis paper.
- KNOWM: Physical Simulation
    - Memristor Discovery Pack includes a chip with 8 memristor pairs and other incidentals
    - Similarly the Digilent Analog Discovery 2 also exists
    - Known Memristor Discovery software for laptop connects over USB to provide waveforms and graph the pinched hysteresis
        - Software includes Synapse12 option which is pre-designed for NN operations
        - Also a classifier experiement is preloaded
- Plan to publish "Characterization and modeling of variability in commercial self-directed channel memristors"
- Built LTSpice emulator model, 1.2v
    - Used genetic algorithm to select the optimal parameters for model
    - Use these for a NN simulation
    - Train on MNIST
- "The part of this work pertaining to memristor modeling has been published in the 14th Spanish Conference on Electron Devices"

## Summary
In the first part of this research, the authors take an off-the-shelf memristor dev kit and try out some of the built-in software. Later on, they pivot over to creating an LTSpice model with ideal conditions and use that for some basic NN operations.

## Pros
The author's work on replicating MNIST results shows a real-world demonstration of how memristors can actually be applied in the real-world.

## Cons
It would've been nice to spend a bit more time on memristor performance here. The authors show their accuracy compared to the ideal, but not compared to similar MNIST trained systems in terms of accuracy, speed, size, or power. The limited results here make it difficult to assess memristor benefits.

Additionally, the first half of this work is not clear. Did they just explain what the software does? Since it ended up being insufficient for their larger experiement why does it take up space in the paper?

## References

```
@misc{lazaro2023design,
      title={Design and simulation of memristor-based neural networks}, 
      author={Pablo Alex Lázaro and Ignacio Jiménez Gallo and Juan Roldán Aranda and Alberto del Barrio García and Guillermo Botella Juan and Francisco Jiménez Molinos},
      year={2023},
      eprint={2306.11678},
      archivePrefix={arXiv},
      primaryClass={cs.ET}
}
```