# K8s Student Project

This project is a student task focused on Kubernetes (K8s). Its goal is to provide hands-on experience in deploying and managing applications using Kubernetes.

## Table of Contents

- [Introduction](#introduction)
- [Prerequisites](#prerequisites)
- [Installation](#installation)
- [Usage](#usage)
- [Contribution](#contribution)
- [License](#license)

## Introduction

In this project, we will explore the basic concepts of Kubernetes and learn how to deploy and manage applications using Kubernetes in a kind cluster. The project will cover topics such as:

- Setting up a Kubernetes cluster;
- Deploying the Grafana image;
- Deploying a web interface to populate Grafana dashboards;
- Deploying ingress;
- Mounting log files.

## Prerequisites

Before you begin, make sure you have the following prerequisites:

- Basic knowledge of containers and containerization;
- Familiarity with the Linux command-line interface;
- Access to a Linux operating system (VMs, WSL, Cloud Clusters);
- Kubernetes installed on the operating system;

## Installation

To install the necessary tools and set up your development environment, follow these steps:

### WSL
1. Install Docker desktop: (https://docs.docker.com/desktop/install/windows-install/)
2. Install Kubernetes: (https://kubernetes.io/docs/tasks/tools/install-kubectl-linux/)
3. Install a tool that is capable of creating a local cluster:
    - kind (https://kind.sigs.k8s.io/docs/user/quick-start/) 
    - minikube (https://minikube.sigs.k8s.io/docs/start/)

### Ubuntu
1. Update the system:
    - sudo apt update
    - sudo apt upgrade
2. Install prerequisite packages:
    - sudo apt-get install  curl apt-transport-https ca-certificates software-properties-common
3. Add the Docker repositories:
    - curl -fsSL https://download.docker.com/linux/ubuntu/gpg | sudo apt-key add -
    - sudo add-apt-repository "deb [arch=amd64] https://download.docker.com/linux/ubuntu $(lsb_release -cs) stable"
    - sudo apt update
    - apt-cache policy docker-ce
4. Install Docker for Ubuntu:
    - sudo apt install docker-ce
5. Check the Docker status:
    - sudo systemctl status docker
6. Install Kubernetes: 
    - (https://kubernetes.io/docs/tasks/tools/install-kubectl-linux/)
7. Install a tool that is capable of creating a local cluster:
    - kind (https://kind.sigs.k8s.io/docs/user/quick-start/) 
    - minikube (https://minikube.sigs.k8s.io/docs/start/)

### Other Tools
Refer to the Docker and Kubernetes documentation for proper installation instructions.

## Usage

To use this project, follow these steps:

1. Clone the repository: `https://github.com/Rafaelcoder18/dashboard-grafana-k8s.git`
2. Navigate to the project directory: `cd student-k8s-project`
3. Deploy the application using Kubernetes: `kubectl apply -f deployment.yaml`
4. Monitor the application using the Kubernetes dashboard: `kubectl proxy` and access the dashboard at [http://localhost:8001/api/v1/namespaces/kubernetes-dashboard/services/https:kubernetes-dashboard:/proxy/](http://localhost:8001/api/v1/namespaces/kubernetes-dashboard/services/https:kubernetes-dashboard:/proxy/)

## Contribution

Contributions are welcome! If you have any ideas, suggestions, or bug reports, open an issue or submit a pull request.

## License

This project is licensed under the [MIT License](LICENSE).
