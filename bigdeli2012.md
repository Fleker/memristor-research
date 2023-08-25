# [A robust hybrid method for image encryption based on Hopfield neural network](https://dl.acm.org/doi/abs/10.1016/j.compeleceng.2011.11.019)

## Notes
- Need an encryption system such that even small incorrect password values do not leak info
- Arnold Cat map - "Commonest map"
- Logistical map: One of the simplest chaos functions studied for cryptography
- Introduces a Hopfield neural network and its model
    - Has 3 secret parameters which can be adjusted
- Image encryption
    - Propose image encryption scheme
        1. Set secret keys
        2. Generate initial conditions
        3. Permutation stage
        4. Convert input image to output image
        5. Arrange pixels into matrix
        6. Diffusion: Set initial conditions for hyper chaos
        7. Image homogenization by iterating via HNN to generate keystream
        8. Encrypt output image using keystream & bitwise XOR
        9. Convert our matrix back into a canonical image
    - Decryption can occur in the same way (but backwards)
- Uses same examples as in [lin2022.md](lin2022.md) such as the woman photo
    - Compares entropy with other algorithms
- Proposed key structure is larger than 10^56
    - High sensitivity: Mismatch of 1e-14 in key makes it impossible to functionally decrypt
    - Fastest algo at ~13.78 MB/s

## Pros
- Unlike [lin2022.md](lin2022.md) which used the same woman image, this one has color
    - Good histograms, splitting up the data into color channels
    - Plenty of data akin to Lin including the diagonal
- Measures encryption in MB/s with three alternative existing algorithms

## Cons
- The graphs used look like they were drawn manually and scanned in
- Not much discussion of hardware acceleration
- Not much discussion if this algorithm could be expanded or broadened
- No discussion of potential future work

## References

```
@article{10.1016/j.compeleceng.2011.11.019,
author = {Bigdeli, Nooshin and Farid, Yousef and Afshar, Karim},
title = {A Robust Hybrid Method for Image Encryption Based on Hopfield Neural Network},
year = {2012},
issue_date = {March, 2012},
publisher = {Pergamon Press, Inc.},
address = {USA},
volume = {38},
number = {2},
issn = {0045-7906},
url = {https://doi.org/10.1016/j.compeleceng.2011.11.019},
doi = {10.1016/j.compeleceng.2011.11.019},
abstract = {In this paper, a robust hybrid image encryption algorithm with permutation-diffusion structure is proposed, based on chaotic control parameters and hyper-chaotic system. In the proposed method, a chaotic logistic map is employed to generate the control parameters for the permutation stage which results in shuffling the image rows and columns to disturb the high correlation among pixels. Next, in the diffusion stage, another chaotic logistic map with different initial conditions and parameters is employed to generate the initial conditions for a hyper-chaotic Hopfield neural network to generate a keystream for image homogenization of the shuffled image. The new hybrid method has been compared with several existing methods and shows comparable or superior robustness to blind decryption.},
journal = {Comput. Electr. Eng.},
month = {mar},
pages = {356–369},
numpages = {14}
}
```
