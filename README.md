# Introduction to RL

## Summary

- **[1_monte_carlo.ipynb](1_monte_carlo.ipynb)**: Find the best trajectory in a car race using tabular Monte Carlo.  
- **[2_q_learning.ipynb](2_q_learning.ipynb)**: Solve the pendulum problem with discretization and classic tabular Q-Learning.  
- **[3_dqn.ipynb](3_dqn.ipynb)**: A minimal implementation of Double-DQN applied to classic control tasks.  
- **[4_policy_gradients.ipynb](4_policy_gradients.ipynb)**: A vanilla implementation of REINFORCE applied to classic control (with discrete actions).  
- **[5_policy_gradients_continuous.ipynb](5_policy_gradients_continuous.ipynb)**: A vanilla implementation of REINFORCE for classic control with continuous actions.  

## Installation  

Download the repository, create a new virtual environment with `python>=3.11`, and install the requirements:  

```bash
pip install -r requirements.txt
```

Using **conda**:

```bash
conda create -n intro_rl python=3.11
conda activate intro_rl
pip install -r requirements.txt
```

To use the virtual environment in Jupyter:

```bash
conda activate intro_rl
conda install -c anaconda ipykernel
python -m ipykernel install --user --name=intro_rl
```

**Note**: The notebooks contain vanilla baselines designed to run on CPU, so the installation and code do not consider GPUs.
