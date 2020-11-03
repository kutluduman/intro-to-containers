## INTRODUCTION TO DOCKER CONTAINERS:

- To create container ---> docker build -t my-container . (This should be run from the Dockerfile folder)

- To run the container ---> docker run (name of the container)

- When you are inside the docker container, it does not give response to node commands such as option c to exit the server. Best practice is to add process.on('SIGTERM') to your index.js file. Another way is to run your container with docker run --init my-node-app command

- To share the server port outside the container, you need to enter --publish 3000:3000 into the command

- Create user for the container. Do not run your commands from the root!

- Difference between ADD and COPY is that ADD can download packages/files from the network, COPY uses the localhost. COPY is the safer way to go.

- WORKDIR ---> put your files inside directory in the container

- RUN npm ci ---> npm install from the container

- --detach and expose ----> run the container in the background with the port given (docker run --init --rm --detach -P my-node-app) but publish is much better way to go

- Command orders are very important in docker containers

- dockerignore ---> same as gitignore. every dockerignore should have .git/








