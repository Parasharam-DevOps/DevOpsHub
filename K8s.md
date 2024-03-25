# Kubernetes (K8s)

Kubernetes is an open-source container management tool that automates container deployment, scaling, and load balancing. It schedules, runs, and manages isolated containers running on various platforms such as virtual machines, physical servers, or cloud instances. Major cloud providers support Kubernetes.

## History

1. Google developed an internal system called 'Borg' (later 'Omega') for managing Google applications and services.
2. In 2014, Google introduced Kubernetes as an open-source platform written in Golang, later donated to CNCF.

## Online Platforms for K8s

- Kubernetes playground
- Play with K8s
- Play with Kubernetes classroom

## Cloud-based K8s Services

- GKE: Google Kubernetes Engine
- AKS: Azure Kubernetes Service
- Amazon EKS: Amazon Elastic Kubernetes Service

## Problems with Scaling Up Containers

1. Containers cannot communicate with each other.
2. Autoscaling and load balancing were not possible.
3. Containers had to be managed carefully.

## Features of Kubernetes

1. **Orchestration**: Automates deployment, management, and scaling.
2. **Autoscaling**: Adjusts container count based on traffic or resources.
3. **Auto-healing**: Replaces failed containers automatically.
4. **Load balancing**: Distributes traffic across containers.
5. **Platform independence**: Runs on various platforms.
6. **Fault tolerance**: Handles node or pod failures.
7. **Rollback**: Reverts to a previous version of an application.
8. **Health monitoring**: Monitors container health.
9. **Batch execution**: Supports different types of batch processing.

## Kubernetes vs Docker Swarm

| Features                 | Kubernetes                                        | Docker Swarm                                      |
|--------------------------|---------------------------------------------------|---------------------------------------------------|
| Installation and cluster configuration | Complicated and time-consuming             | Fast and easy                                    |
| Container Support        | Supports various container types             | Limited to Docker containers                      |
| GUI                      | Available                                        | Not available                                    |
| Data Volumes             | Shared within the same POD                      | Can be shared with any other containers          |
| Update and Rollback      | Automated process                                | Manual process                                   |
| Autoscaling              | Supports vertical and horizontal scaling        | Not supported                                    |
| Logging and Monitoring   | Built-in monitoring                              | Requires third-party tools like Splunk            |

### Architecture:

Kubernetes follows a master-worker architecture. The master controls the cluster, while worker nodes execute tasks.

![image](https://github.com/Parasharam-DevOps/DevOpsHub/assets/132131379/6a7a5126-5bfd-4cfe-944f-91aeabc390e4)


## Important Objects

- **Pods:** Smallest deployable units, consisting of one or more containers.
- **Deployments:** Manage the deployment and scaling of applications.
- **Services:** Provide stable endpoints for accessing pods.
- **PersistentVolumes:** Provide storage resources for pods.

## Core Components

- **Master Node:** Controls the cluster, includes Kube-API server, Etcd, Kube-scheduler, and Controller manager.
- **Worker Node:** Executes application containers.

## Role of Master Node

1. Kubernetes cluster contains containers running on various platforms.
2. One or more nodes are designated as masters and all others as workers.
3. The master runs a set of Kubernetes processes, called the control plane, to ensure smooth functioning.
4. The master can be multi-master for high availability.

## Components of Control Plane (Master)

1. Kube-API server
2. Etcd
3. Kube-scheduler
4. Controller manager

### 1. Kube-API Server

- This api-server interacts directly with user (i.e we apply .yml or json manifest
to kube-apiserver).
- This kube-apiserver is meant to scale automatically as per load.
- Kube api-server is front-end of control-plane.

### 2. Etcd

- Stores metadata and status of the cluster.
- It stores metadata and status of cluster.
- Etcd is consistent and high available store (key-value store).
- Source of touch for cluster state (info about state of cluster).
Etcd has following features: -
* Fully replicated: the entire state is available on every node in the cluster.
*  Secure: implements automatic TLS with optional client-certificate
authentication.
*  Fast: benchmarked at 10,000 writes per second.

### 3. Kube Scheduler

- Handles pod creation and management.
- When users make request for the creation and management of PODs, kube
scheduler is going to take action on these requests.
- Handles POD creation and management.
- Kube scheduler match/ assign any node to create and run PODs.
- A scheduler watches for newly created PODs that have no node assigned. For
every POD that the scheduler discovers the scheduler becomes responsible for
finding best node for that POD to run on.
- Scheduler gets the information for hardware configuration from configuration
file and schedules the PODs on nodes accordingly.

### 4. Controller Manager

- Ensures the actual state of the cluster matches the desired state.

## Nodes (Kubelet and Container Engine)

Nodes run three important pieces of software:

1. Kubelet
2. Container Engine
3. Kubeproxy

### 1. Kubelet

➢ Agent running on the node.
➢ Listens to Kubernetes master. (e.g-POD creation request)
➢ Use port 10255.
➢ Send success/fail reports to master.

### 2. Container Engine

- Works with Kubelet, pulls images, starts/stops containers.

### 3. Kubeproxy

- Assigns IP addresses to pods, ensures each pod gets a unique IP.

## POD

- Smallest unit in Kubernetes.
- POD is a group of one or more containers that are deployed together on the same host.
- A cluster is a group of nodes.
- A cluster has at least one worker node and master node.
- In Kubernetes the control unit is the POD, not containers.
- It consists of one or more tightly coupled containers.
- POD runs on node which is control by master.
- Kubernetes only knows about PODs (does not know about individual container).
- Cannot start containers without a POD.
- One POD usually contains one container.

## Multi-container PODs

- Share resources and volumes, deployed together on the same node.

## Higher Level Kubernetes Objects

- Replication set: auto-scaling and auto-healing
- Deployment: versioning and rollback
- Service: static IP and networking
- Volume: non-ephemeral storage

## Important Tools

- **Kubectl**: Command-line interface for managing Kubernetes clusters.
- **Kubeadm**: Tool for bootstrapping Kubernetes clusters.
- **Kubefed**: Tool for federating multiple Kubernetes clusters.

## Networking

Kubernetes provides networking capabilities to enable communication between pods, nodes, and external services.

## Monitoring and Logging

Kubernetes offers built-in monitoring and logging capabilities through tools like Prometheus and Fluentd.

## Best Practices

- Use configuration files for defining infrastructure settings.
- Set resource limits for efficient resource utilization.
- Implement readiness and liveness probes for applications.
- Implement RBAC and network policies for security.

## Troubleshooting

- Use `kubectl logs` to retrieve logs from running containers.
- Use `kubectl describe` to get detailed information about Kubernetes objects.
