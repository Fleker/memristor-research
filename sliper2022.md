# [Pragmatic Memory-System Support for Intermittent Computing Using Emerging Nonvolatile Memory](https://ieeexplore.ieee.org/document/9759470/)

## Notes
- Volatile v . NVM
  - Volatile: Low latency, low per-access energy
  - NVM : Persistence, lower leakage power, potentailly higher density
- FASE - Failure-atomic section (restart section after power failure)
  - "Dream journal" from MemOS
- MEMIC
  - Volatile instruction cache, volatile data cache, hardware undo logger
  - Meant for passive IoT which uses energy harvesting (intermittent computing)
  - 13-39% improvements in "workload completion time" and less energy, more reliable
- NVP: Non-Volatile Processor (It's a thing apparently)
- How? Fused - An OSS SystemC-based simulator built for ICs
  - Simulates energy and execution

## Summary
This paper offers a lightweight design for performing blocks of code at once by leveraging non-volatile memory for intermittently available IoT hardware called MEMIC. They use a technique of caching a series of instructions and memory into a volatile buffer that can be executed forward. In the event of a power failure, when not every operation has run, they can reverse each one of these actions.

Using a series of experiments through an IC simulator called [Fused](https://github.com/UoS-EEC/fused), they show a fair improvement in energy usage and workload completion time.

## Pros
The introduction of a FASE (failure-atomic section) provides a way to achieve "smart resume" which is a larger advantage over traditional volatile memory systems which would need to do hard reboots each time. Other systems like MacOS must use some sort of NAND flash state saving to [reopen every app to their previous state after reboot](https://support.apple.com/en-us/HT204005).

I am happy that they made the code open souce for further study, though they provide little documentation on how to use it and whether there even is enough material here to truly use. Their paper provides enough information to replicate their configuration, even if the code may require some tweaking.

## Cons
The paper compares a handful of non-volatile memory types including FAM, PCM, and others to decide the optimal memory type, but does not spend much time justifying why they pick FRAM. At the same time, they do use citations which could be useful for further reading.

While the specific application targeted in this paper, intermittent computing, is an interesting use-case, it's not clear this is an area where non-volatile memory could be used most effectively. Recording sensor data to a log at certain periods is not data intensive, so would NAND flash be just as adequate? The comparison is not made. They use constant voltage in their simulations rather than working more directly with their chosen use-case. This choice seems justified as it's not in-scope of their R&D, but makes it an odd choice then.

Another consideration is in the logger infrastructure they build, which seems naive in a technical sense. If I were to design something like this, I'd develop something closer to a database transaction system where you build and return a series of actions at the end of a compute block such that everything happens roughly simulataneously. Using simple C for their code, without any higher abstractions, presents self-imposed limitations.

```c
int main() {
  transaction t = memoryObtainTransaction()
  enableSensor(t)
  // ...
}

bool enableSensor(transaction t) {
  // The syntax here is a bit fuzzy, but is meant to enqueue a bunch of commands
  // These all run together at the end of the transaction
  t.queue(SENSOR->CONTROL |= SENSOR_ENABLE);
  // More compute can happen here.
  // If there's a shutdown during this section, the transaction has not run at all.
  return t.run()
}
```

## References
- [MEMIC GitHub Repo](https://github.com/UoS-EEC/MEMIC)
- [Supporting dataset](https://eprints.soton.ac.uk/456087/)
- [Fused](https://github.com/UoS-EEC/fused)

```
@ARTICLE{9759470,
  author={Sliper, Sivert T. and Wang, William and Nikoleris, Nikos and Weddell, Alex S. and Savanth, Anand and Prabhat, Pranay and Merrett, Geoff V.},
  journal={IEEE Transactions on Computer-Aided Design of Integrated Circuits and Systems}, 
  title={Pragmatic Memory-System Support for Intermittent Computing Using Emerging Nonvolatile Memory}, 
  year={2023},
  volume={42},
  number={1},
  pages={95-108},
  doi={10.1109/TCAD.2022.3168263}}
```
