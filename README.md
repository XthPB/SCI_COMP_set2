# Scientific Computing — Assignment Set 2

Diffusion-Limited Aggregation (DLA), Monte Carlo DLA, and Gray-Scott Reaction-Diffusion simulations 

## Repository Structure

### Notebooks

| File | Description |
|------|-------------|
| `set2_exercise_1_2.ipynb` | Exercises 2.1 (A–B): Laplace based DLA growth for varying η, ω sweep, SOR speedup benchmarks (Python and JIT) |
| `set_2_exercise_2.ipynb` | Exercise 2.2 (C–D): Monte Carlo DLA via random walkers (Part C) and sticking probability sweep (Part D) |
| `set_2_execise_3.ipynb` | Exercise 2.3 (E): Gray-Scott reaction-diffusion model for various (f, k) regimes |
| `sor_speedup.ipynb` | Exercise 2.1 (B): SOR solver speedup benchmarks (Colab GPU results) — Pure Python, JIT, Red-Black parallel, GPU (CuPy) |

### Output Folders

| Folder | Contents |
|--------|----------|
| `exercise_2.1_2.2_plots/` | DLA cluster plots, diffusion fields, ω sweep, SOR speedup benchmark figures |
| `exercise_2.2_plots/` | Monte Carlo DLA cluster and sticking probability sweep plots |
| `exercise_2.3_plots/` | Gray-Scott pattern formation plots |

### Other Files

| File | Description |
|------|-------------|
| `requirements.txt` | Python dependencies |
| `README.md` | This file |

## Setup

```bash
pip install -r requirements.txt
```

For GPU benchmarks (`sor_gpu`), we ran the `set2_exercise_1_2.ipynb` on Google Colab with a GPU runtime and `cupy` installed.

## Usage

Run the notebooks in order.

## Benchmark Results

| N | Pure Python | GPU (CuPy) | Numba JIT | RB Parallel |
|------:|----------:|----------:|----------:|----------:|
| 50 | 145.26 ms | 56.81 ms | 0.80 ms | 0.40 ms |
| 100 | 473.25 ms | 43.89 ms | 2.63 ms | 0.78 ms |
| 200 | 1710.95 ms | 53.03 ms | 16.09 ms | 1.79 ms |
| 300 | 3614.39 ms | 52.10 ms | 32.60 ms | 3.23 ms |
| 400 | 6173.26 ms | 38.60 ms | 31.20 ms | 3.73 ms |
| 500 | 8824.08 ms | 52.23 ms | 55.23 ms | 9.93 ms |
| 700 | 17491.07 ms | 45.11 ms | 86.95 ms | 9.67 ms |
| 1000 | 31816.80 ms | 68.18 ms | 154.16 ms | 18.17 ms |

*Measured on Google Colab (T4 GPU). See `sor_speedup.ipynb`.*

![SOR Benchmark](exercise_2.1_2.2_plots/sor_benchmarks.png)

