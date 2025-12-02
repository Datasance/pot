# iofog-go-sdk

**Go SDK for PoT Microservices**

The iofog-go-sdk provides a Go library for developing microservices that can communicate with each other within a PoT Edge Compute Network.

## Overview

The Go SDK simplifies microservice-to-microservice communication by handling the discovery process and message routing automatically. It provides an easy-to-use interface for sending and receiving ioMessages between microservices.

## Features

- **Message Communication**: Send and receive ioMessages between microservices
- **Automatic Discovery**: Handles service discovery automatically
- **Type Safety**: Leverages Go's type system for safe message handling
- **Agent Integration**: Seamlessly integrates with PoT Agents via Local API

## Installation

```bash
go get github.com/Datasance/iofog-go-sdk
```

## Quick Start

```go
package main

import (
    "github.com/Datasance/iofog-go-sdk/pkg/client"
)

func main() {
    // Create a new ioFog client
    fogClient := client.NewClient()
    
    // Connect to the Agent
    fogClient.Connect()
    
    // Send a message
    fogClient.SendMessage("target-microservice", []byte("Hello, PoT!"))
    
    // Receive messages
    messages := fogClient.GetMessages()
    for _, msg := range messages {
        // Process message
    }
}
```

## Documentation

- **SDK Documentation**: [PoT SDK Documentation](https://docs.datasance.com/developing-microservices/sdk)
- **Agent Local API**: [Agent Local API Reference](https://docs.datasance.com/reference-agent/local-api)
- **Tutorial**: [Build Your First Microservice](https://docs.datasance.com/tutorial/create-our-first-microservice-javascript)

## Repository

**GitHub**: [https://github.com/Datasance/iofog-go-sdk](https://github.com/Datasance/iofog-go-sdk)

## Related Components

- [Agent](../../agent/) - Runs microservices that use the SDK
- [Controller](../../controller/) - Orchestrates the ECN where SDK-based microservices run
- [Router](../../router/) - Enables communication between SDK-based microservices

