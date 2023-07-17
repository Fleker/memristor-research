# [STT-ANGIE: Asynchronous True Random Number GEnerator Using STT-MTJ](https://ieeexplore.ieee.org/document/8715257)
_Published in 2019_

## Notes
- LLG Equation: Landau–Lifshitz–Gilbert
- STT-MTJ / STT-MRAM use little energy, low area, so good even for IoT
- N-bits generated
    - 1 Capacitor
    - N STT-MTJs
    - N sense amplifiers
- Three steps:
    1. Reset: Cap goes to V_{init}
    2. Enable: Discharge cap to N mem cells
    3. Read: Use amplifiers to see which cells have been flipped
- Evaluate?
    - Shannon entropy and min-entropy methods, using Monte Carlo sim
- Future work includes considering magnetic attacks

## Summary
The authors here evaluate truly random number generators (TRNGs) using STT-MTJs. They explain the process and show the results have good randomness.

## Pros
The background section is quite good, explaining every concept necessary in a concise and clear manner. They also discuss why this technology is valuable and its potential pitfalls.

## Cons
Energy and space are important factors, but what do we get from STT-MTJs that we cannot do conventionally. Perhaps on the periphery, with low-frequency computers, randomness may matter. Perhaps in high-risk places like banking we could use it. But generally, is this overkill? I don't know.

## References

```
@INPROCEEDINGS{8715257,
  author={Perach, Ben and Kvatinsky, Shahar},
  booktitle={2019 Design, Automation & Test in Europe Conference & Exhibition (DATE)}, 
  title={STT-ANGIE: Asynchronous True Random Number GEnerator Using STT-MTJ}, 
  year={2019},
  volume={},
  number={},
  pages={264-267},
  doi={10.23919/DATE.2019.8715257}}
```