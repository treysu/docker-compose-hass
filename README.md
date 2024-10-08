# Docker Compose for Home Assistant and Related Services

This repository contains Docker Compose configurations for setting up and managing a Home Assistant environment, along with several related services. It includes example environment files to simplify the setup process.

## Repository Structure

- **`compose.yaml`**: The main Docker Compose file defining the services and their configurations.
- **`default.env.example`**: A template environment file for common variables like timezone.
- **`kometa.env.example`**: A template environment file specific to the Kometa service.

## Services

The following services are defined in the `compose.yaml` file:

- **Home Assistant**: A home automation platform to control smart devices.
- **Music Assistant**: A music management server integrated with Home Assistant.
- **ESPHome**: A platform for controlling ESP devices via Home Assistant.
- **ESPResense Companion**: A tool for presence detection.
- **Zigbee2MQTT**: A service for controlling Zigbee devices with MQTT.
- **Govee2MQTT**: A service to control Govee devices via MQTT.
- **Mosquitto**: A lightweight MQTT broker.
- **Snapcast**: A multi-room audio player.
- **OpenWakeWord**: An addon for wake word detection.
- **Piper**: A voice synthesis service for Home Assistant.
- **Faster Whisper**: A speech-to-text engine using Whisper.

## Getting Started

### Prerequisites

- [Docker](https://www.docker.com/get-started) and [Docker Compose](https://docs.docker.com/compose/install/) installed.
- Basic knowledge of Docker and Docker Compose.

### Step-by-Step Setup

1. **Clone the Repository**:
   ```sh
   git clone https://github.com/treysu/docker-compose-hass.git
   cd homeassistant-docker
   ```

2. **Configure Environment Files**:
   - Copy the example environment files and fill in your values:
     ```sh
     cp default.env.example default.env
     cp kometa.env.example kometa.env
     ```
   - Open these files and configure the environment variables according to your setup.

3. **Run Docker Compose**:
   - To start all services:
     ```sh
     docker compose -f compose.yaml up -d
     ```

4. **Stop and Remove Services**:
   - To stop and clean up all services:
     ```sh
     docker compose -f compose.yaml down
     ```

### Customization

- **Volumes and Paths**: Adjust the volumes and paths in `compose.yaml` according to your file system.
- **Environment Variables**: Ensure that the required environment variables are properly set in `default.env` and `kometa.env`.
