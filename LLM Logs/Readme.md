# LLM Logs and analysis

This folder contains the LLM log files used in the paper for the experiments reported in the subsections grouped here, plus the analysis notebook that reproduces the numerical results (tables/figures) presented in the paper.

Each file corresponds to a run. Filenames are formatted as follows:

`promptID-topology-adversary-green-model-nbRun`

- **promptID**: Variant of the prompt used, as described in Table I of the paper.  
- **topology**: Variant of the network scenario used: base, simplified (reduced), or augmented (extended).  
- **adversary**: Adversary for the run: B_Line, RedMeander, Sleep.  
- **green**: Whether a green agent was used or not (green / noGreen).  
- **model**: LLM used.  
- **nbRun**: Run index for this specific configuration (e.g., 1, 2).


LLM logs are organized as follows, in the order the information appears in each log file:

1. System prompt used for the run. 
2. Run parameters.
3. Network format / architecture description.
4. Per-step records (one entry per timestep). Each step contains:
   - Observation presented to the LLM.
   - Ground-truth network state.
   - Adversary action
   - LLM action.
   - Reward observed for that step.
   - Number of tokens in the prompt.
   - Number of tokens in the model answer/response.
   - Raw API output.
5. Run-level statistics (summary for the whole run), including reward values at specific timesteps (for example, at t = 30, 50, 100).  
6. The final conversation context (for autoregressive prompting, this is the entire dialogue; for single-step prompting, this is the final step’s prompt).

## Logs & License

The files in this directory are **synthetic** and generated via **simulation**.

Copyright (c) Orange SA.
These files are distributed under the **MIT** license (see `../LICENSE`).