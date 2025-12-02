# Controller

**The Orchestration Heart of PoT**

The Controller is the central orchestration component of each Edge Compute Network (ECN). It orchestrates all Agents, Microservices, Routers, users, and manages the entire ECN lifecycle.

## Overview

The Controller is the heart of each Edge Compute Network. It keeps track of all your Agents, even across complicated network configurations, allowing you to maintain your entire fleet remotely.

## Key Features

- **Centralized Orchestration**: Manages all Agents, microservices, and resources in the ECN
- **REST API**: Full-featured REST API for programmatic control
- **Multi-Agent Management**: Coordinate thousands of geographically distributed edge nodes
- **Resource Management**: Manage microservices, applications, registries, catalogs, and more
- **Security**: Integrated IAM and RBAC support with Keycloak
- **High Availability**: Support for multiple Controllers for increased resiliency

## Deployment

The Controller can run on:
- **Cloud Providers**: AWS, GCP, Azure, etc.
- **Kubernetes**: Deployed as part of a control plane
- **Edge Nodes**: Directly on edge hardware (with static IP/DNS)
- **Behind Ingress**: Can be accessed through HTTP Ingress services

## Architecture

The Controller communicates with Agents via REST API. Agents report to the Controller, so the Controller must be network-accessible from all edge nodes, but not vice versa.

## Documentation

- **Overview**: [Controller Overview](https://docs.datasance.com/reference-controller/overview)
- **REST API**: [Controller REST API](https://docs.datasance.com/api)
- **Deployment**: [Platform Deployment](https://docs.datasance.com/platform-deployment/introduction)

## Repository

**GitHub**: [https://github.com/Datasance/Controller](https://github.com/Datasance/Controller)

## Related Components

- [potctl](../potctl/) - CLI tool for deploying and managing Controllers
- [Agent](../agent/) - Edge nodes orchestrated by the Controller
- [ECN-Viewer](../ecn-viewer/) - Browser-based interface to the Controller
- [Router](../router/) - Service mesh component managed by the Controller

