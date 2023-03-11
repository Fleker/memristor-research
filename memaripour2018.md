# [Breeze: User-Level Access to Non-Volatile Main Memories for Legacy Software](https://cseweb.ucsd.edu//~amemarip/upload/Breeze-ICCD-2018.pdf)

## Notes
- Propose Breeze: NVMM toolchain
    - Non-volatile main memory
- Breeze: Library and C compiler
    - No need to explicitly log operations
    - No need for explicit nvm pointers
    - Examples: MongoDB and Memcached
- NVMM introduces new bugs!
    - Pointers b/w nvm and vm
    - Pointers b/w two nvm regions
- Existing work
    - NV-heaps: requires persistent object base
    - NVM-direct: New syntax to C++
    - Both: Hard to support existing applications
- Breeze Compiler
    - Annotates memory categories, uses them wisely
    - Atomic operations
    - Logging and recovery logic for free
- Benchmarks
    - Better results than comparable NVM tools
    - Middling results compared to norm (Figure 9)

## Summary
This paper introduces an NVM toolchain including a compiler which allows for minimal code rewrite to support non-volatile memory operations. Breeze adds a number of expected NVM operations around logging and system recovery. Their benchmarks suggest it works well for some operations and not for others when compared to traditional systems and similar NVM programming tools.

## Pros
The paper tries to take a wholisitc look at NVM and what would be needed to add support answering how to minimize the amount of program rewriting and how to remove boilerplate for necessary operations like log/resume. The authors take a few real-world libraries to show their effectiveness especially in comparison to standard volatile memory. _Figure 9_ shows a large reduction in latency for MongoDB on an NVM system while admittedly showing a latency increase in Memcache.

While the results seem mixed, it does show an example of how NVM can be better in some applications.

## Cons
The first con is that these results cannot be independently verified through open-source code, as I haven't seen it. ("Breeze" is used for a few c++ projects.) The paper introduces some compiler features but also a lot of syntax changes that would require larger rewrites and be hard to scale to everything (leading to proposals like [memory address embed](ye2021.md)).

Another bigger question is that while MongoDB can be rewritten to use NVM instead of volatile memory, that's just a simple find/replace. Could you rewrite MongoDB from scratch to better take advantage of the hardware? Would it be possible to store integers into a single Memristor bit using different voltage levels? Could you use [ternary content addressable memory](https://ieeexplore.ieee.org/document/6880478) to optimize lookups?

Do we want a faster version of RAM or something fundamentally unique?

## References

```
@INPROCEEDINGS{breeze,
  author={Memaripour, Amirsaman and Swanson, Steven},
  booktitle={2018 IEEE 36th International Conference on Computer Design}, 
  title={Breeze: User-Level Access to Non-Volatile Main Memories for Legacy Software}, 
  year={2018},
  volume={},
  number={},
```