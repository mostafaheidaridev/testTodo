# Todo web application demo

Clone the repository - for example using VS Code.

## Install the dependencies:

for both todo-app and todo-api, run:

```bash
npm install
```

## Docker compose

run the multi-container setup:

```bash
docker-compose up -d
```

NOTE: If you don't install the dependencies for the todo-api, the container will not work because it needs some of the devDependencies to run properly but the dockerfile only installs production dependencies.

## Local Kubernetes Setup

kubernetes folder contains the necessary manifests.

kubernetes.deployment.sh shell script automates the deployment process to the local Kubernetes cluster.

Run:

```bash
bash kubernetes.deployment.sh
```

All the services are port-forwarded to localhost, so we can access them via http://localhost:3000 for the todo-app and http://localhost:5000 for the todo-api. MongoDB is accessible at localhost:27017, for example using MongoDB Compass or any other MongoDB client.
