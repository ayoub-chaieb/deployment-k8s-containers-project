---

# 🏥 Health Application – Docker & Kubernetes Deployment Project

## ✅ Project Overview

This project successfully delivered a **containerized health web application** and deployed it on **Kubernetes** with advanced features. It covered building the app with Docker, pushing to IBM Cloud Container Registry, deploying via Kubernetes, implementing **Horizontal Pod Autoscaler (HPA)**, and managing **rolling updates and rollbacks**.

The project demonstrates practical skills in cloud-native application lifecycle management and container orchestration.

---

## 🎯 Objectives Achieved

1. Built and deployed a simple health web application using Docker and Kubernetes
2. Autoscaled the application using Horizontal Pod Autoscaler
3. Performed rolling updates and rollbacks for zero-downtime deployment

---

## 🛠 Step-by-Step Achievements

### 1. Repository Setup and Environment

* Cloned project artifacts from GitHub and prepared the environment.

### 2. Containerization with Docker

* Completed the multi-stage `Dockerfile` to build the health application image.
  ![Dockerfile](images/dockerfile.png)

* Built and tagged the image, pushed it to IBM Cloud Container Registry.
  ![IBM Cloud Registry Images](images/crimages.png)

### 3. Kubernetes Deployment

* Created and applied the `deployment.yml` manifest.
  ![Deployment YAML Applied](images/deployment.png)

* Exposed the application locally via port-forward and launched it in the browser.
  ![Running Application](images/app.png)
  ![Running Application Alternative](images/app2.png)

### 4. Autoscaling

* Configured the Horizontal Pod Autoscaler (HPA).
  ![HPA Created](images/hpa.png)

* Generated load and observed autoscaling behavior.
  ![HPA Scaling Under Load](images/hpa2.png)

### 5. Rolling Updates & Rollbacks

* Updated the UI and pushed a new image.
  ![Updated Image Built](images/uphealth.png)

* Applied the updated deployment and confirmed the UI changes.
  ![Updated Application](images/up-app.png)

* Verified rollout history and details.
  ![Rollout History](images/rev.png)

* Checked replica sets after updates and rollback.
  ![Replica Sets](images/rs.png)

---

## 📦 Deliverables

* **Dockerfile** – Multi-stage optimized build
* **deployment.yml** – Kubernetes deployment manifest
* **patient-ui** – Web frontend application
* **Images folder** – Screenshots in `/images` for documentation

---

## 🧠 Skills Demonstrated

* Docker image building and pushing to registry
* Kubernetes deployments and rolling strategies
* Horizontal Pod Autoscaling setup and testing
* Load generation and cluster monitoring
* Rolling updates and rollback management

---

## 👨‍💻 Author

Developed by **Ayoub CHAIEB**
Based on IBM Skills Network final container orchestration project

---
