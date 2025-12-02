# Router

**Service Mesh and Communication Layer**

The Router is an essential component that enables microservices to communicate with each other and provides public port tunneling for microservice exposure.

## Overview

The Router creates a Layer 7 service mesh for secure, isolated network communication between microservices. It enables microservices to send ioMessages to each other and provides TCP bridge services for service mesh functionality.

## Key Features

- **Service Mesh**: Enables secure microservice-to-microservice communication
- **Message Routing**: Routes ioMessages between microservices across the ECN
- **Port Tunneling**: Provides public port exposure for microservices
- **Network Isolation**: Enables communication between nodes on isolated networks
- **AMQP Protocol**: Uses AMQP for inter-router communication
- **Topology Flexibility**: Supports custom router topologies for advanced deployments

## Architecture

Each Controller and Agent has its own Router instance by default:
- **Interior Dispatch Router**: Co-hosted with the Controller
- **Edge Dispatch Router**: One instance per Agent, connected to the Interior Router

Routers create TCP bridges for service mesh and use AMQP protocol for inter-router communication.

## Advanced Features

For advanced users, it's possible to:
- Share Edge Routers between multiple Agents
- Host Interior routers on Agents instead of Controller
- Configure direct Agent-to-Agent communication
- Set up custom router topologies

## Documentation

- **Architecture**: [PoT Architecture](https://docs.datasance.com/getting-started/architecture)
- **Deployment**: [Platform Deployment](https://docs.datasance.com/platform-deployment/introduction)

## Repository

**GitHub**: [https://github.com/Datasance/Router](https://github.com/Datasance/Router)

## Related Components

- [Controller](../controller/) - Manages Router configuration
- [Agent](../agent/) - Hosts Edge Routers
- [potctl](../potctl/) - Deploys and configures Routers

