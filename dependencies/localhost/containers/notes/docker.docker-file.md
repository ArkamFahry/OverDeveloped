---
id: 5zoeu3gz1nxlwlvdbbiobqv
title: Docker File
desc: ''
updated: 1673424694797
created: 1673423404656
tags:
  - docker
  - containers
isDir: false
enableToc: false
title_imported: Docker FIle
---

 A **docker file** is  a text document that contains all the commands a user could call on the command line to assemble an docker image. Using docker build users can create an automated build that executes the command's described in the **docker file** in succession to create a docker image.

#### Example docker files

- #### A docker file  

```Docker
# The base image
FROM node:lts-alpine3.16

# Create a directory for the app
RUN mkdir -p usr/src/app

# Copies all the files 
COPY . .

# Install app dependencies
# The order matters for dependencie caching
RUN npm install

# Exposeses internal port 3000 in the docker contianer
EXPOSE 3000

# The command which runs when the docker container starts
CMD [ "npm", "run", "start" ]
```

- #### A multi stage docker file  

```Docker
# The base image for the docker image build
FROM node:lts-alpine3.16 AS builder

# Create app directory
WORKDIR /app

# A wildcard is used to ensure both package.json AND package-lock.json are copied
COPY package*.json ./
COPY prisma ./prisma/

# Install app dependencies
# The order matters for dependencie caching
RUN npm install

# Copies all the files 
COPY . .

# Builds the application
RUN npm run build

# The docker image runner image
FROM node:lts-alpine3.16

# copies all the files from the builder the runner
COPY --from=builder /app/node_modules ./node_modules
COPY --from=builder /app/package*.json ./
COPY --from=builder /app/dist ./dist

# Exposeses internal port 3000 in the docker contianer
EXPOSE 3000

# The command which runs when the docker container starts
CMD [ "npm", "run", "start:prod" ]
```  
