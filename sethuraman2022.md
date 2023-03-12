# [Techniques to Improve Write and Retention Reliability of STT-MRAM Memory Subsystem](https://ieeexplore.ieee.org/document/9560712)

## Notes
- STT-MRAM: Spin-Transfer Torque Magneto-Resistive RAM
    - Challenges:
        - Bit-error rate is linked w/temperature
        - Requires high write latency & current
- Proposal
    - Architecture for memory controller and last-level cache for temperature fix
    - Memory scheduler: prioritze writes in high-temp
    - Improve architecture to stabilize temp
- Results
    - 27% power improve
    - 603x bit error reduction
    - 5.8% perf improvement
    - Compared with conventional DDR4 STT-MRAM
- Temperature
    - Fluctuate b/w 338-353K (148.7-175.7F)
- Everspin: STT-MRAM w/DDR4 interface


## Summary
Though STT-MRAM suggests some advantages as a memory architecture, the current implementation of it in DDR4 architecture leads to particular disadvantages. This paper offers new methods like changing I/O prioritization and adjusting pulses in correlation with temperature to achieve improvements in several key areas.

## Pros
The authors have implemented something that vey clearly shows performance impacts. In particular their ability to reduce the bit error rate is significant and highlights some of the ways that STT-MRAM can be improved in production.

## Cons
The authors don't really justify why STT-MRAM is the right tool, and their paper does highlight a number of technical flaws. While the results are impressive they are not compared to other memory systems including DRAM. So I don't really see the larger benefit.

Their paper designs a DDR4 controller rather than considering a more novel design. STT-MRAM does have some design constraints but they try to shove them under the rug rather than design to their advantage. The simulations are just standard I/O operations rather than something practical.

For instance, they suggest a system that performs more writes at higher temperatures compared to more reads at lower temperatures. I don't know much about temperature profiles in my PC, but I also can't delay certain tasks. If I'm rendering a video clip, I really want a lot of write throughput immediately. Batch jobs are just not an adequate solution in many cases.

## References
- [Everspin](https://www2.macnica.com/apac/galaxy/en/news-events/product-line-news/everspin-displays-both-the-1gb-ddr4-perpendicular-st-mram-device/)
- [Gem5](https://www.gem5.org/)

```
@ARTICLE{9560712,
  author={Sethuraman, Saravanan and Tavva, Venkata Kalyan and Srinivas, M. B.},
  journal={IEEE Transactions on Computer-Aided Design of Integrated Circuits and Systems}, 
  title={Techniques to Improve Write and Retention Reliability of STT-MRAM Memory Subsystem}, 
  year={2022},
  volume={41},
  number={9},
  pages={2901-2914},
  doi={10.1109/TCAD.2021.3118210}}
```
