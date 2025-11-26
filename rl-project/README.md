# SAC Control under TOU Pricing with OCHRE Gym

This repository contains the code used to train and evaluate a Soft Actor–Critic (SAC) controller for a single building under a time-of-use (TOU) electricity price signal using the `ochre_gym` environment.

## Files

- `ece-570-ai-sac-tou.ipynb` – main Jupyter notebook  
  - Loads the OCHRE building environment  
  - Trains an SAC agent  
  - Evaluates the learned policy  
  - Produces plots of rewards, indoor temperature, and energy use

No datasets or `.git` directories are included.

## Requirements

The notebook uses the following Python packages:

- `ochre_gym`
- `gymnasium`
- `stable_baselines3`
- `numpy`
- `pandas`
- `matplotlib`

You can install them with:

```bash
pip install ochre-gym gymnasium stable-baselines3 numpy pandas matplotlib
```

If `ochre-gym` is not available via `pip` in your setup, install it from the official OCHRE Gym repository.

## Data and Environment

- All building data and simulation logic are provided by the `ochre_gym` package.  
- The environment is created inside the notebook using `ochre_gym.load(...)` with appropriate options for the selected building, control signals, time resolution, and TOU pricing.  
- No external data files are required beyond what `ochre_gym` provides.

## How to Run

1. Create and activate a Python environment (for example, using `conda` or `venv`).  
2. Install the required packages listed above.  
3. Start Jupyter:

   ```bash
   jupyter notebook
   ```

4. Open `ece-570-ai-sac-tou.ipynb`.  
5. Run all cells from top to bottom.

The notebook will train the SAC agent and generate all evaluation plots directly inside the notebook.
