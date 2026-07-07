# Notebooks

This folder contains three notebooks used to reproduce the results of our study:

- `llm-agent.ipynb`: notebook containing the LLM agent code.
- `rl-agent.ipynb`: notebook containing the RL agent code.
- `log-analysis.ipynb`: notebook used to reproduce the statistical analyses presented in the paper.

The notebooks are self-contained and can be followed directly. However, some parameters must be adjusted manually. The relevant parameters for each notebook are described below.

## LLM Agent

This notebook contains the LLM agent code. Several parameters must be modified to run the full set of experiments, including the LLM model, scenario configuration, and prompt strategy. The notebook assumes that the LLMs are hosted on Azure. Therefore, the endpoint and API key must be provided:

- `endpoint`: URL of the LLM provider endpoint.
- `azure_key`: API key.

To reproduce all experiments, the following parameters must also be configured as appropriate:
- `log_path`: path where the logs produced by the agent will be stored.
- `model_name`: name of the LLM model to use.
- `scenario_path`: path to the scenario folder as a string (e.g., `Scenario Configuration Files/Augmented`).
- `scenario_name`: name of the scenario to use.
- `prompt_path`: path to the prompt folder as a string.
- `prompt_file`: name of the prompt file to use.
- `green_agent`: whether to include a Green agent (`True` or `False`).
- `red_agent`: class of the red agent (e.g., `RedMeanderAgent`).

## RL Agent

This notebook installs the Cardiff Team agent from the CAGE 2 challenge, removes the selector policy so that only the `BLine` weights are used, and then runs the experiments while logging the results. All parameters are already configured for this RL agent. Logs are stored in an `Evaluation` folder within the CybORG installation.

## Statistical Analysis

The `log-analysis.ipynb` notebook contains the code used to reproduce the results presented in Section 5 of the paper. It includes parsing and statistical analysis functions, followed by a dedicated section for each experiment described in the paper. Random seeds are fixed so that the same results can be reproduced exactly when using the data in [LLM Logs](../LLM%20Logs/Readme.md) and [RL Logs](../RL%20Logs/Readme.md).

To reproduce the statistical analysis results, you must set the `llm_log_path` and `rl_log_path` parameters so that they point to the locations of the corresponding log files.

## License

Copyright (c) Orange SA.  
These files are distributed under the **MIT** license (see [LICENSE](../LICENSE)).