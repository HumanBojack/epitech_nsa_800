# T-NSA-800
`Group: LIL-07`

This is an assignment from Epitech, the goal is to create a monitoring system for a sample application using various tools.

This repository contains the configuration files for setting up and monitoring a sample application using various tools. The structure of the repository is as follows:

- `grafana`: Contains the Docker Compose file and configuration for Grafana and Loki. Grafana is accessible on port 3000 and Loki on port 3100. The Grafana data is stored in a volume named `grafana-storage` and Loki data in `loki-data`. Both services are part of the `traefik` network.

- `portaefik`: Contains the Docker Compose file and configuration for Traefik and Portainer. Traefik is a modern HTTP reverse proxy and Portainer is a container monitoring tool. Both services are part of the `traefik` network. The SSL certificates are stored in a volume named `letsencrypt`.

- `prometheus`: Contains the Docker Compose file and configuration for Prometheus and Node Exporter. Prometheus is a powerful systems and service monitoring system accessible on port 9090. The Prometheus data is stored in a volume named `prometheus_data`. Both services are part of the `traefik` and `localprom` networks.

- `syncthing`: Contains the Docker Compose file for Syncthing, a continuous file synchronization program. Syncthing is part of the `traefik` network and its configuration and data are stored in volumes mounted from the host.

- `uptime-kuma`: Contains the Docker Compose file for Uptime Kuma, a fancy self-hosted monitoring tool. Uptime Kuma is part of the `traefik` network.

The `sample_app` being monitored is a Go application, and its source code can be found at [this GitHub repository](https://github.com/HumanBojack/sample-go-app).

## Getting Started

To get started with this setup, you'll need to have Docker and Docker Compose installed on your system. Once you have those installed, you can use the `docker-compose up` command in each of the directories to start the corresponding service.

Please refer to the README files in each directory for more specific instructions on how to use and configure each service.