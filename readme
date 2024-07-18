# Multi-Tier Application Deployment

This repository contains the Kubernetes manifests required to deploy a multi-tier application consisting of a MySQL database and a WordPress frontend.

## Project Structure

- `mysql-deployment.yaml`: Kubernetes deployment manifest for MySQL.
- `pvc.yaml`: PersistentVolumeClaim for MySQL data storage.
- `wordpress-deployment.yaml`: Kubernetes deployment manifest for WordPress.
- `readme`: This README file.

## Prerequisites

Before deploying this application, ensure you have the following:

- A running Kubernetes cluster.
- `kubectl` configured to interact with your cluster.
- Persistent storage available for the MySQL database.

## Deployment Steps

1. **Create Persistent Volume Claims:**

    ```bash
    kubectl apply -f pvc.yaml
    ```

2. **Deploy MySQL:**

    ```bash
    kubectl apply -f mysql-deployment.yaml
    ```

3. **Deploy WordPress:**

    ```bash
    kubectl apply -f wordpress-deployment.yaml
    ```

## Accessing the Application

After deploying the manifests, you can access the WordPress application using the service created. You may need to expose the service using a LoadBalancer or NodePort depending on your Kubernetes environment.

  ```bash
    kubectl svc WordPress --url
  ```
## Customization

- **MySQL Configuration:** Edit the `mysql-deployment.yaml` file to change MySQL configurations such as the database name, user, and password.
- **WordPress Configuration:** Edit the `wordpress-deployment.yaml` file to customize WordPress settings.

## Clean Up

To remove the deployed resources, run:

```bash
kubectl delete -f wordpress-deployment.yaml
kubectl delete -f mysql-deployment.yaml
kubectl delete -f pvc.yaml


