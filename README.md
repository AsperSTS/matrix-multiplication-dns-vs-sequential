# DNS vs Sequential Matrix Multiplication

Academic benchmarking project comparing a DNS-style matrix multiplication implementation with a sequential approach across increasing matrix sizes.

The repository focuses on implementation, validation and performance measurement rather than providing a general-purpose linear algebra library.

## What it includes

- Sequential matrix multiplication.
- DNS-style multiplication implementation.
- Integer and floating-point matrix generation.
- Result validation between algorithms.
- Execution-time collection.
- Tables and graphs generated from benchmark results.
- Make targets for repeatable runs.

## Benchmark sizes

The project includes tests from 64×64 up to 8192×8192 matrices.

## Workflow

```text
matrix generation
   ↓
algorithm execution
   ↓
result validation
   ↓
timing collection
   ↓
summary tables and graphs
```

## Main files

- `dnsMpy.py` — DNS-style implementation.
- `secuencial.py` — sequential implementation.
- `genMatrix.py` / `genMatrixFloat.py` — test-data generation.
- `checkMatrix.py` — result verification.
- `resultsMean.py` — timing aggregation.
- `genTables.py` — summary tables.
- `graphByDimension.py` / `graphByGroup.py` — visualizations.
- `Makefile` — experiment automation.

## Run

Generate matrices:

```bash
make genAllMatrix
```

Run the configured benchmark targets from the `Makefile`, then generate visualizations:

```bash
make genAllGraphs
```

## Stack

Python · NumPy · Matplotlib · Make

## Context

Developed as coursework for an Operating Systems class. The project is useful as an experiment in algorithm implementation, validation and performance measurement.

Benchmark conclusions depend on the hardware, Python environment and exact implementation used, so results should be interpreted together with the original experiment setup.
