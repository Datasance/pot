# potctl

**Unified Command Line Interface for PoT**

`potctl` is the primary CLI tool for installation, configuration, and operation of Datasance PoT Edge Compute Networks (ECNs).

## Overview

potctl enables you to remotely manage multiple different PoT clusters from a single host. It is designed for both PoT users and DevOps engineers who need to manage PoT clusters efficiently.

## Key Features

- **Multi-cluster Management**: Manage multiple PoT clusters from a single host
- **Remote Operations**: Deploy and manage Controllers and Agents remotely
- **Kubernetes Integration**: Deploy control planes on Kubernetes clusters
- **Resource Management**: Create, update, and manage all PoT resources (Agents, Applications, Microservices, etc.)
- **Declarative Configuration**: Use YAML files to define and deploy resources

## Installation

Download and install potctl from the [potctl repository](https://github.com/Datasance/potctl).

## Quick Start

```bash
# Connect to a PoT cluster
potctl connect -n <namespace>

# Deploy a control plane
potctl deploy controlplane -f controlplane.yaml

# Add an agent
potctl deploy agent -f agent.yaml

# Deploy an application
potctl deploy application -f application.yaml
```

## Documentation

- **Getting Started**: [potctl Introduction](https://docs.datasance.com/potctl/introduction)
- **Reference**: [potctl Reference](https://docs.datasance.com/reference-potctl/reference-kinds)
- **Download**: [Download and Installation](https://docs.datasance.com/potctl/download)

## Repository

**GitHub**: [https://github.com/Datasance/potctl](https://github.com/Datasance/potctl)

## Related Components

- [Controller](../controller/) - The orchestration component managed by potctl
- [Agent](../agent/) - Edge nodes deployed and managed via potctl
- [ECN-Viewer](../ecn-viewer/) - Browser-based alternative to potctl for day-to-day operations

