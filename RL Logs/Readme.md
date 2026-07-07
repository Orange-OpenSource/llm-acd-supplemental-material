# RL Logs

`rl-complete`: Complete log with actions taken at each timestep by each agent across the 100 runs.  
`rl-summary`: Summary statistics on reward at timesteps 30, 50, and 100, and average time to take action.

## Complete log structure

The complete log file contains all experiments across different adversaries and episode lengths. It begins with general metadata, including the seeds shared by all experiments.

Each experiment section specifies the corresponding variant (e.g., `--- Variant: steps=30, adversary=B_lineAgent, green=False ---`) and is followed by aggregate statistics computed over 100 runs.

For each episode, the log then includes the sequence of tuples listing the blue action and red action at each step, followed by the total reward for the episode, the seed used for that run, and the average latency per step.

## License

The files in this directory are **synthetic** and generated via **simulation**.

Copyright (c) Orange SA.
These files are distributed under the **MIT** license (see [LICENSE](../LICENSE)).