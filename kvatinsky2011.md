# [Memristor-based IMPLY logic design procedure](https://ieeexplore.ieee.org/document/6081389)

## Notes

- Trade-off b/w fast write speeds and accuracy
- IMPLY can serve as a basic logic element for nvm circuits
- Mathematical model for behavior based on HP model

## Summary

In my implementation of [`imply` within Gem5](https://fleker.medium.com/implementing-imply-operation-in-risc-v-with-gem5-simulations-24314a9d6e24), I wanted to go back to see why IMPLY was selected as the go-to operation. This paper seems to be the original source, proposing IMPLY as one of the primary memristor elements. The paper includes a variety of behavior graphs and circuitry models.

## Pros

This paper does a lot of good proposals and presents foundational math. It offers an easy-to-follow circuit diagram and the math is not that difficult to derive.

## Cons

The graphs presented appear to be idealized forms of memristors designed solely using the underlying mathematical models rather than trying to get the data experimentally through a simulation or real test.

## References

```
@INPROCEEDINGS{6081389,
  author={Kvatinsky, Shahar and Kolodny, Avinoam and Weiser, Uri C. and Friedman, Eby G.},
  booktitle={2011 IEEE 29th International Conference on Computer Design (ICCD)}, 
  title={Memristor-based IMPLY logic design procedure}, 
  year={2011},
  volume={},
  number={},
  pages={142-147},
  doi={10.1109/ICCD.2011.6081389}}
```
