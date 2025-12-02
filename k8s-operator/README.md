# iofog-operator

**Kubernetes Operator for PoT**

The iofog-operator is the Kubernetes operator that manages PoT Custom Resources, enabling Kubernetes-native deployment and management of PoT control planes and applications.

## Overview

The iofog-operator takes care of managing Kubernetes Custom Resource Definitions (CRDs) for PoT. It supports Custom Resources for control planes, enabling declarative management of PoT deployments on Kubernetes.

## Key Features

- **Kubernetes Native**: Integrates seamlessly with Kubernetes
- **Custom Resources**: Manages ControlPlane CRDs
- **Declarative Management**: Define PoT deployments using Kubernetes manifests
- **Automated Deployment**: Automatically deploys ECNs when Custom Resources are created
- **Helm Integration**: Works with Helm charts for PoT deployment

## Deployment

When deploying PoT on Kubernetes using potctl, the iofog-operator is the first component deployed in the namespace. When a new ControlPlane Custom Resource is created, the operator automatically picks it up and deploys an ECN in the same Kubernetes namespace.

## Usage

The operator is typically used indirectly through:
- **potctl**: When deploying PoT on Kubernetes
- **kubectl**: For direct Custom Resource management

## Architecture

The operator watches for PoT Custom Resources and manages the lifecycle of:
- ControlPlane resources (Controllers, Routers, etc.)

## Documentation

- **Architecture**: [Kubernetes Architecture](https://docs.datasance.com/getting-started/architecture)
- **Deployment**: [Kubernetes Deployment](https://docs.datasance.com/platform-deployment/kubernetes-prepare-cluster)

## Repository

**GitHub**: [https://github.com/Datasance/iofog-operator](https://github.com/Datasance/iofog-operator)

## Related Components

- [Controller](../controller/) - Deployed and managed by the operator
- [potctl](../potctl/) - Uses the operator for Kubernetes deployments
- [Router](../router/) - Part of the control plane managed by the operator

