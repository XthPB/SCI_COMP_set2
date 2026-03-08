# Scientific Computing — Assignment Set 2

Diffusion-Limited Aggregation (DLA), Monte Carlo DLA, and Gray-Scott Reaction-Diffusion simulations 

## Repository Structure

### Notebooks

| File | Description |
|------|-------------|
| `set2_exercise_1_2.ipynb` | Exercises 2.1 (A–B): Laplace based DLA growth for varying η, ω sweep, SOR speedup benchmarks (Python and JIT) |
| `set_2_exercise_2.ipynb` | Exercise 2.2 (C–D): Monte Carlo DLA via random walkers (Part C) and sticking probability sweep (Part D) |
| `set_2_execise_3.ipynb` | Exercise 2.3 (E): Gray-Scott reaction-diffusion model for various (f, k) regimes |

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
