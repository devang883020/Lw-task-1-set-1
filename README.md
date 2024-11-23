# Lw-task-1-set-1

Scenario: Deploying a Multi-Container Application
 with Docker Compose and Kubernetes.

 I'd create a solution for deploying a multi-container application using both Docker Compose and Kubernetes. 
 I'll first create the Docker Compose configuration and then show the Kubernetes manifests.

Let me explain the key components and how to deploy them:

Docker Compose Setup:


The docker-compose.yml file defines two services: web (Nginx) and db (MySQL)
Networks and volumes are configured for proper isolation and data persistence
Environment variables are set for MySQL configuration


Kubernetes Setup:


Nginx deployment with 2 replicas

NodePort service exposing Nginx on port 30080

MySQL deployment with persistent storage

Secrets for MySQL credentials

Services for both Nginx and MySQL

PersistentVolumeClaim for MySQL data

To deploy with Docker Compose:
docker-compose up -d

To deploy to Kubernetes:

Create namespace (optional)

kubectl create namespace myapp

Apply all configurations
kubectl apply -f kubernetes/

Verify deployments:

kubectl get deployments

kubectl get services

kubectl get pods

Key features of this setup:

High availability with 2 Nginx replicas
Persistent storage for MySQL data
Secure credential management using Kubernetes secrets
NodePort service type as requested
Latest Nginx image as specified



