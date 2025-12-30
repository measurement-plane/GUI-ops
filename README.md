# Measurement Plane GUI

This repository contains the setup for deploying the Measurement Plane GUI in a Docker container. The GUI provides tools to manage and visualize measurement capabilities via a web interface.

## Prerequisites

- Docker installed on your system.
- Access to the Docker image `ghcr.io/measurement-plane/gui:latest`.
- (Not required for running the GUI but required for working properly to discover capabilities) A running message broker (e.g., NATS) accessible via `BROKER_URL`.

## Quick Start

### 1. Clone the Repository
```bash
git clone <repo-url>
cd GUI-ops
```

### 2. Configure Environment Variables
You can modify the BROKER_URL and ORCHESTRATOR_URL default variables directly in the `run.sh` script if needed with the address of the Broker and the experiment orchestrator:

Example:
```bash
BROKER_URL="nats://172.17.0.1:4222"
ORCHESTRATOR_URL="http://172.17.0.1:8080"
```

### 3. Run the Application
Make the script executable and run it:

```bash
chmod +x run.sh
./run.sh
```
