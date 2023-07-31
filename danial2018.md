# [Real-Time Trainable Data Converters for General Purpose Applications](https://ieeexplore.ieee.org/document/8604350)
_Published in 2018_

## Notes
- “Impact of Transistor Mismatch on the Speed-Accuracy-Power Trade-Off of Analog CMOS Circuits,”
    - From paper: "Furthermore, with the continuous downscaling of technology motivated by Moore's law, this tradeoff has become a chronic bottleneck of modern systems design due to alarming deep sub-micron effects"
- Data converters have high overheads
- Propose memristor-based converters
    - Train on converted data
    - Use ML to train ANN (artificial neural network)
    - Memristors act as the synapses
        - Describes ADCs
- ENOB (Effective Number of Resolution Bits)

## Summary

The authors of this short paper propose a data conversion hardware device which uses memristors to form a neural network.

## Pros

The paper describes a defined application.

## Cons

The paper is too short and theoretical, not even getting to do a real simulation. Additionally, the problem of "data conversion" is not well defined. Is this to mean Fahreinheit to Celsius? Wav to MP3? Text to JSON? The paper does nothing to address potential accuracy concerns, which matter less for video encoding but a lot for structured text.

This seems like a viable use-case that could be converted into products for broadcast if you could sell them on performance or energy, but this paper leaves way too much left to be explored.

## References

```
@INPROCEEDINGS{8604350,
  author={Danial, Loai and Kvatinsky, Shahar},
  booktitle={2018 IEEE/ACM International Symposium on Nanoscale Architectures (NANOARCH)}, 
  title={Real-Time Trainable Data Converters for General Purpose Applications}, 
  year={2018},
  volume={},
  number={},
  pages={1-3},
  doi={}}
```
