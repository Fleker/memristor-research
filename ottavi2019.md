# [The Missing Applications Found: Robust Design Techniques and Novel Uses of Memristors](https://ieeexplore.ieee.org/document/8854427)
_Published in 2019_

## Notes
- There is a typo in the first page - "memroy"
- Solar cell monitoring
    - As memristive switching time goes up, that implies the power from the cell is dropping
- Gas detection
    - Allow gasses to interact with semiconductor layer
    - Gas interactions can affect values in a deterministic way by changing wire resistance
    - But need to optimize for accuracy. Manufacturing imprecisions need to be balanced with more memristors.
    - Too many memristors clear out resistance sensing and increase power
- Logic-in-memory
    - Use memristors as switches
    - MRL: Memristor Ratioed Logic
    - mMPU: memristive Memory Processing Unit
    - Single gate and small scale stateful logic have been demonstrated
    - What hasn't been demonstrated?
        - Large scale computation
        - Generalized algorithms to support computations
        - Generalized way to parallelize operations and map to memory
        - The programming model, which must be different from Von Neumann but play nicely with it.

## Summary

In this paper, the authors look at three potential use-cases and map out a bit of the math and data related to each. None of these are primary use-cases of memristors, but a sort of literature-review teaser.

## Pros

Their explanation of Logic-In-Memory, while lacking in some ways, does offer novel research opportunities. I also liked their concepts and basic research of memristive sensors as both uses seem like good fits for the technology.

## Cons

I really wanted a bit more from the final section. It seems like the programming model issue aligns with my research interests. However, they don't really present a lot of their knowledge here as a starting point. There are a few references to other papers but little else. There are also many other potential use-cases they note in the abstract which are unremarked upon otherwise while this paper felt like a potpourri (TODO right word?) of ideas they didn't have time for.

## References

```
@INPROCEEDINGS{8854427,
  author={Ottavi, Marco and Gupta, Vishal and Khandelwal, Saurabh and Kvatinsky, Shahar and Mathew, Jimson and Martinelli, Eugenio and Jabir, Abusaleh},
  booktitle={2019 IEEE 25th International Symposium on On-Line Testing and Robust System Design (IOLTS)}, 
  title={The Missing Applications Found: Robust Design Techniques and Novel Uses of Memristors}, 
  year={2019},
  volume={},
  number={},
  pages={159-164},
  doi={10.1109/IOLTS.2019.8854427}}
```