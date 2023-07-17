# [Towards a memristive hardware secure hash function (MemHash)](https://ieeexplore.ieee.org/document/7951797)
_Published in 2017_

## Notes
- Just off the bat, this reminds me of memristor chaos circuits for generating truly random numbers
    - Referenced in the paper here in the intro
    - Telegraph noise in resistive unit
- Physically unclonable Function (PUF)
    - Process-based differences (manufacturing imprecision) can add entropy to outputs
- MemHash
    - Hashes numbers
    - Scrambler unit
    - Uses "parasitic write disturb phenomenon" to add entropy
    - Uses a dynamic range, not just binary, to maximize number of encoding spaces
    - Quasistable: A form of stability with lowering rate of change so that we can just call it now
 - "The size of the memory array must be large enough to prevent birthday attacks"
    - Referring to how a few people can share a birthday?
    - 128 bits
    - Differential read, so crossbar must be 256 (16x16) bits
- Hashing
    - Processes input stream serially
    - Re-init hasher to preset values for determinism (like a hardware key?)
- Simulations
    - Simulated writes 16x16 using SPICE
    - Everything with a Perl script
    - Measure "uniqueness" in Hamming Distance
 - "We believe that the differential read scheme makes modeling attacks on MemHash unlikely"

## Summary

The authors of this paper propose a simple hardware security chip using a small memristor crossbar structure to scramble messages in a way that relies on material imperfections and analog memory to create a value which is hard to spoof.

## Pros

This is a cool use of memrisors which takes me back to that presentation of memristor chaos circuits in my senior year memristors class. This appears to be a good use of memristors, taking full advantage of its analog properties to create something reliable.

## Cons

The results in this paper don't seem quite sufficient. Hardware keys are a big deal, and becoming more useful through organizations like [FIDO](https://fidoalliance.org/) and [browser passkeys](https://developers.google.com/identity/passkeys). The paper proposes a simple encryption scheme but does not try to go further into simulating more of a real secure enclave. This paper was published in 2017 in part from Kvatinsky but I do wonder what happened afterwards.

## References

```
@INPROCEEDINGS{7951797,
  author={Azriel, Leonid and Kvatinsky, Shahar},
  booktitle={2017 IEEE International Symposium on Hardware Oriented Security and Trust (HOST)}, 
  title={Towards a memristive hardware secure hash function (MemHash)}, 
  year={2017},
  volume={},
  number={},
  pages={51-55},
  doi={10.1109/HST.2017.7951797}}
```