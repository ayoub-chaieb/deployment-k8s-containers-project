---

🏥 Health Application – Docker & Kubernetes Deployment Project

✅ Project Overview

This project successfully delivered a containerized health web application and deployed it on Kubernetes with advanced features. It covered building the app with Docker, pushing to IBM Cloud Container Registry, deploying via Kubernetes, implementing Horizontal Pod Autoscaler (HPA), and managing rolling updates and rollbacks.

The project demonstrates practical skills in cloud-native application lifecycle management and container orchestration.


---

🎯 Objectives Achieved

1. Built and deployed a simple health web application using Docker and Kubernetes


2. Autoscaled the application using Horizontal Pod Autoscaler


3. Performed Rolling Updates and Rollbacks to ensure zero-downtime deployment management




---

🛠 Step-by-Step Achievements

1. Repository Setup and Environment

Cloned project artifacts from GitHub:

git clone https://github.com/ibm-developer-skills-network/vuotu-containers-project.git
cd vuotu-containers-project

Verified environment readiness and project structure


2. Containerization with Docker

Completed the multi-stage Dockerfile to build the health application image

Built the image and tagged it for the IBM Cloud Container Registry:

docker build -t us.icr.io/<namespace>/patient-ui:v1 .

Exported namespace variable:

export MY_NAMESPACE=sn-labs-$USERNAME

Pushed image to IBM Cloud:

ibmcloud cr images

Verified successful push and image readiness


3. Kubernetes Deployment

Created deployment.yml manifest with rolling update strategy:

Defined replicas, container spec, resource requests/limits

Configured patient-ui deployment with exposed port 8080


Applied deployment to cluster:

kubectl apply -f deployment.yml

Exposed the application locally via port-forward:

kubectl port-forward deployment.apps/patient-ui 8080:8080

Launched and verified the running application in the browser


4. Autoscaling

Configured Horizontal Pod Autoscaler:

kubectl autoscale deployment patient-ui --cpu-percent=50 --min=1 --max=10

Verified HPA:

kubectl get hpa patient-ui

Generated synthetic load using BusyBox to trigger scaling:

kubectl run -i --tty load-generator --rm --image=busybox:1.36.0 --restart=Never -- /bin/sh -c "while sleep 0.01; do wget -q -O- <app URL>; done"

Observed pod replicas increase dynamically:

kubectl get hpa patient-ui --watch


5. Rolling Updates & Rollbacks

Edited login.html to customize UI (added developer name under the logo)

Built and pushed updated Docker image

Modified CPU resource values in deployment.yml to trigger rolling update

Applied updated deployment and verified changes live

Reviewed rollout history:

kubectl rollout history deployment/patient-ui

Identified revisions and performed rollback to a previous stable state:

kubectl rollout undo deployment/patient-ui --to-revision=1

Validated rollback via replica sets:

kubectl get rs



---

📦 Deliverables

Dockerfile – Multi-stage build for optimized images

deployment.yml – Kubernetes deployment manifest with resource configuration

patient-ui app – Simple health web UI for demo purposes

IBM Cloud Container Registry image – Container image stored and deployed



---

🧠 Skills Demonstrated

Docker multi-stage builds and registry management

Kubernetes Deployments and service exposure

Horizontal Pod Autoscaling configuration

Load testing with BusyBox containers

Rolling updates and rollback strategies for zero-downtime releases



---

👨‍💻 Author

Developed and implemented by Ayoub CHAIEB
Based on IBM Skills Network container orchestration final project materials

---

Would you like me to include screenshots placeholders (like ![Deployment Screenshot](app.png)) or add commands for service exposure to the internet?

