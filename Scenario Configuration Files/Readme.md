# Scenario Configuration Files

This folder contains the configuration files for the three network topology variants. Each topology is defined by both a YAML file and a CFG file.

- **YAML file**: the configuration format used by CybORG. For additional details, please refer to the CybORG [documentation](https://github.com/cage-challenge/cage-challenge-2/tree/main/CybORG/CybORG/Tutorial) and the [scenario creator](https://github.com/cage-challenge/cage-challenge-2/blob/main/CybORG/CybORG/Shared/Scenarios/Scenario_Creator.ipynb).
- **CFG file**: a compact JSON representation of the network, used by the LLM wrapper and the greedy decoy module. Its structure is shown below:

```json
{
  "Op_Hosts": [
    "list of operational hosts"
  ],
  "Enterprise": [
    "list of enterprise host/gateway pairs"
  ],
  "User": [
    "list of user host/link pairs"
  ]
}
```

## License

This directory contains configuration files (`*.yaml` & `*.cfg`).

Copyright (c) Orange SA.
Unless explicitly stated otherwise, these files are distributed under the **MIT** license (see [LICENSE](../LICENSE)).