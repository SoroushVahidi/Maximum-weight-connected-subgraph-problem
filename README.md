# Maximum-Weight Connected Subgraph (C++ / CPLEX)

> Historical undergraduate project (about 2020), kept for reference.

**What this is.** Given a graph with (possibly negative) vertex weights, the **maximum-weight connected subgraph (MWCS)** problem asks for a connected set of vertices whose total weight is as large as possible. It is NP-hard and is used in network biology and network design. This repository holds one C++ program that models MWCS as an integer program and solves it with IBM ILOG CPLEX.

## Files

| File | What it is |
|---|---|
| `maximum weighted connected subgraph.cpp` | Graph class plus a CPLEX (Concert) model. Writes objective values to `objvalues.txt` |
| `sample inputs.rar` | Sample instances (RAR archive, about 1.9 MB) |

## Building

- Needs IBM ILOG CPLEX with the C++ Concert API.
- Written for Windows/MSVC (`conio.h`, `ilcplex\ilocplex.h`). On Linux or macOS, drop `conio.h` and use `#include <ilcplex/ilocplex.h>`.
- Extract `sample inputs.rar` next to the executable. The program opens its graph, weight, and query files by name from the working directory.

## License

MIT, see `LICENSE`.
