# [A Cycle-level Unified DRAM Cache Controller Model for 3DXPoint Memory Systems in gem5](https://arxiv.org/pdf/2303.13026.pdf)

## Notes
- "The existing computer architecture
simulators do not provide support to model and evaluate systems
which use DRAM devices as a cache to the non-volatile main
memory"
- "heterogeneous memory systems" - DRAM & NVM in one system (see [Intel Cascade Lake with Optane Persistent Memory](https://www.intel.com/content/www/us/en/products/docs/memory-storage/optane-persistent-memory/overview.html))
- "Hildebrand et al. showed that a
dirty miss to the DRAM cache requires up to five accesses to
memory" (limitation of NVRAM controller)
- UDCC: Unified DRAM Cache Controller
    - DRAM & NVRAM models in gem5
- Gem5 Memory
    - Has many models
    - A _memory controller_ and _memory interface_
    - This work: UDCC: A new memory controller with minor memory mods
    - Authors are seeking to upstream these changes (and the work itself)
- Memory packets have different states
- Bechmarks
    - Common HPC benchmarks
    - gem5 traffic generators
- Scheduling policies
    - first-come-first-serve
    - first ready FCFS: maximize row-buffer hit rate
        - This one is better
- > Finally, for WO 100% miss ratio access pattern, each request requires four accesses: one for fetching tag and metadata from DRAM, then fetching the line from NVRAM, writing the data to the DRAM, and a write to NVRAM for dirty line write back.
- [HBM: High-Bandwidth Memory](https://en.wikipedia.org/wiki/High_Bandwidth_Memory)
- Factoring in write wear leveling effect
    - Defined as a limited max of writes to a given block before they become unreliable
    - Wear leveling is an attempt to distribute writes across the memory hw
    - Slightly higher latency when implemented (maybe a bad idea)

## Summary

This paper implements a simulated memory architecture similar to Intel's Cascade Lake which employs a system to write to NVRAM to extend the DRAM.

This implementation leverages existing components in Gem5. They examine secondary design factors like improving scheduling and write wear leveling.

## Pros

This is an interesting pre-print published two weeks ago. The code is available in open source on GitHub, though I need to suss out what it all does. It should provide a solid foundation for further tests.

I appreciate their examination of these secondary factors and investigating these things to see their effectiveness is mixed.

## Cons

The paper examines the firmware level and tries to match existing architectures closely, which is not terrible. At the same time, the authors never address the hardware architecture itself and whether this is a good design.

Also their code seems to be a hard fork of gem5 with a commit pushed a few weeks ago rather than a better importable module.

## References
- [Source code](https://doi.org/10.5281/zenodo.7761940)
    - [GitHub](https://github.com/darchr/dram-cache-model/tree/gem5workshop2022)
    - [Primary commit](https://github.com/darchr/dram-cache-model/commit/1953f855a363a72c06cb5fc19eaeabd382b4ec53)

```
@article{babaie2023,
author = {Babaie, Maryam and Akram, Ayaz and Lowe-Power, Jason},
year = {2023},
month = {03},
pages = {},
title = {A Cycle-level Unified DRAM Cache Controller Model for 3DXPoint Memory Systems in gem5}
}
```
