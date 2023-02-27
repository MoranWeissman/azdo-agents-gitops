# Repository Name

This repository contains the code for deploying Azure DevOps agents to EKS via ArgoCD. 

In the context of ArgoCD, a GitOps repository is a version-controlled repository containing declarative configuration files and manifests for the applications and infrastructure that ArgoCD manages. The repository serves as the single source of truth for the desired state of the system, and changes to the system are made by modifying the configuration files in the repository.
When changes are committed to the GitOps repository, ArgoCD automatically detects them and applies them to the system. This means that the entire configuration management process is handled through Git, providing a clear audit trail of all changes made to the system.


## Folders

### azdo-agent-library-chart

This folder contains the Helm chart for the library of Azure DevOps agents. 

- Chart.yaml
- .helmignore
- /templates:
  - _deployment.yaml
  - _helpers.tpl
  - _scaled-object.yaml
  - _service-account.yaml

### azure-devops-agent-generic

This folder contains the Helm chart for the generic Azure DevOps agent.

- Chart.yaml
- values.yaml
- /templates:
  - _helpers.tpl
  - deployment.yaml
  - scaled-object.yaml
  - service-account.yaml

### azure-devops-agent-python38

This folder contains the Helm chart for the Azure DevOps agent with Python 3.8.

## How to Use

To use this code, fork or clone the repository and copy the necessary files to your own Git repository. The repository structure should be the same as described above. Once you have the repository set up, follow the instructions in the README file to deploy the agents via ArgoCD.

## Contributing

Contributions to this repository are welcome. Please refer to the CONTRIBUTING.md file for more information.

## License

This repository is licensed under the MIT License. See the LICENSE file for more information.
