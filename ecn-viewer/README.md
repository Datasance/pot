# ECN-Viewer

**Browser-Based Control Plane for PoT**

ECN-Viewer is the browser-based control plane for Datasance PoT. It mirrors nearly every potctl capability—deploying applications, editing resources, inspecting telemetry, and opening remote shells—without requiring local tooling.

## Overview

ECN-Viewer provides a comprehensive web-based interface for managing and monitoring your Edge Compute Networks. It's served directly by the Controller and provides the same RBAC and audit capabilities as potctl.

## Key Features

- **No Local Tooling Required**: Access your ECN from any browser
- **Full Resource Management**: Deploy, edit, and manage all PoT resources
- **Real-time Monitoring**: View ECN health, capacity, and activity timelines
- **Agent Fleet Management**: Inspect and manage all Agents with remote terminals
- **Application Management**: Deploy, start/stop, scale, and reroute traffic
- **Resource Editors**: Dedicated editors for ConfigMaps, Secrets, Volumes, Certificates
- **REST API Explorer**: Embedded REST client for advanced API operations
- **Events and Auditing**: Track and audit all Controller API calls

## Access

The Viewer is served directly by the Controller. Configure the HTTP/S port with the `VIEWER_PORT` environment variable (defaults to `80`).

Authentication and authorization follow the same Keycloak-backed RBAC rules as potctl, so users only see and manage namespaces permitted by their role.

## Capabilities

### Dashboards
- Overall ECN health and capacity monitoring
- Activity timelines and deployment progress
- Fleet KPIs and alerts

### Agent Operations
- Fleet inventory with health indicators
- Geographic map visualization
- Remote shell and exec sessions
- Declarative YAML editing

### Application Management
- Microservice inventory and management
- Services and routing configuration
- Catalog and registry management
- Application template designer

### Resource Management
- ConfigMaps and Secrets editors
- VolumeMount management
- Certificate management
- Event logging and auditing

## Documentation

- **ECN-Viewer Guide**: [ECN-Viewer Documentation](https://docs.datasance.com/ECN-Viewer/ecn-viewer)

## Repository

**GitHub**: [https://github.com/Datasance/ECN-Viewer](https://github.com/Datasance/ECN-Viewer)

## Related Components

- [Controller](../controller/) - Hosts and serves the ECN-Viewer
- [potctl](../potctl/) - Required for initial Controller deployment
- [Agent](../agent/) - Managed through ECN-Viewer interface

