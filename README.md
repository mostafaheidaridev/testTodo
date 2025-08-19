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
