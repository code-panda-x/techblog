# Docker & Kubernetes

# Docker

## About Docker

Problem: It works on my machine, but not works on others'

Solution:
- VM
- Docker

Docker is a technology for creating and running containers

Docker allows different machines to share the same environments by using sharing docker image and create same containers

A **Container** is a collection of one or more processes, organized under a single name and identifier. A container is isolated from the other processes running within a computing environment, be it a physical computer or a virtual machine (VM).

## Docker images
DockerFile + App files --> Docker --> Image (shared to others)

Docker image explains what your environment looks like
Docker image contains everything a container needs to run:
- Application runtime (JDK/Python/NodeJS)
- Application code
- Dependencies

Docker compose:
Controls all containers and makes them work together

## Run docker containers on
- Local machine
- Corporate data center
- Cloud

## Basics
![docker](/images/docker.jpg)
![dockercommand](/images/dockercommand.jpg)

## Example

Think of building a machine from scratch (OS, Environment, Dependencies...)

Dockerfile
```
FROM python:3 // Docker pull Python & OS image from DockerHub
WORKDIR /usr/src/app    
COPY requirements.txt . // Copy Python dependencies to current Docker workdir
RUN pip install --no-cache-dir -r requirements.txt // Install Python dependencies
COPY . . // copy local files to current docker workdir
CMD ["python", "app.py"] // run on docker machine

```

docker-compose.yml
```
version: '3'

services:
    web:
        build: ./web
        ports:
            - "5000:5000"
    db:
        build: ./db

```

---

# Kubernetes

## What is Kubernetes
Kubernetes is a container orchestration option

Kubernetes groups the containers that support a single application or microservice into a pod. A pod is exposed to the network by way of another Kubernetes abstraction called a service. In short, the network knows about Kubernetes services and a service knows about the pod(s) that has its logic. Within each pod is one or many containers that realize the logic in the given pod.

Kubernetes is a tool for running a bunch of different containsers.
We give it some configs to describe how we want our containers to  run and interact with each other

## Why we want Kubernetes


We can run Kubernets on:
- AWS - Elastic Kubernetes Service (EKS)
- Azure - Azure Kubernetes Service (AKS)
- GCP - Google Kubernetes Engine (**GKE**)

Pros:
- Service Discover: Makes communications between services easy
- Auto scaling: Scale containers based on demand
- Load Balancer: Distribute load among muliple instances of a microservice
- Deployment: Release new versions without shutting service down

## Terminology

![terms](/images/kubeterms.jpg)

## WorkFlow

What it takes to move a Docker conatiner to a Kubernetes Cluster
- Docker Image from a Dockerfile
- Kubernetes config file (YAML)

![kube](/images/kube.jpg)

Service: takes care of the communications between pods
Config file: written in YAML, it tells kubernetes about different deployments, pods, and services that we want to create (what our cluster is running)

config file eg (xxx.yaml)
```
apiVersion: v1
kind: Pod
metadata:
    name: posts
spec:
    containers:
        - name: posts
            image: abc/posts:0.0.1
```

## Docker vs Kubernetes

Basically, Docker deinfes/creates/runs containers. Kubernetes manages containers, it doesn't make containers.

---
ref: https://tanzu.vmware.com/developer/guides/from-docker-to-kubernetes/
