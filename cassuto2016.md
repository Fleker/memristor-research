# [Write Sneak-Path Constraints Avoiding Disturbs in Memristor Crossbar Arrays](https://ieeexplore.ieee.org/document/7541439)
 _Published in 2016_
 
 ## Notes
 
 - Write sneak paths: Potential circuit design hazards where bits flip errorneously
 - If there are three memristors connected in sequence: two off and one on, the V_{set} of the third can leak and force another on
 - Parallel programming, writing to many cols/rows simultaneously, can avoid this kind of leakage
 
 ## Summary
 
 The authors in this paper are primarily focused on the subject of write sneak paths, a potential circuit design hazard. The authors spend time defining and outlining a variety of circumstances.
 
 ## Pros
 
 The authors do a good job of presenting the problem, providing definitions and thereoms and lemmas. The paper is short but laser focused.
 
 ## Cons
 
 They mention parallel programming as a fix to the hazard but don't really explain it in nearly as much detail. The paper also is very theoretical rather than trying to show these things in simulations.

## References

```
@INPROCEEDINGS{7541439,
  author={Cassuto, Yuval and Kvatinsky, Shahar and Yaakobi, Eitan},
  booktitle={2016 IEEE International Symposium on Information Theory (ISIT)}, 
  title={Write sneak-path constraints avoiding disturbs in memristor crossbar arrays}, 
  year={2016},
  volume={},
  number={},
  pages={950-954},
  doi={10.1109/ISIT.2016.7541439}}
```