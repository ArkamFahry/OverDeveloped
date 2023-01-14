---
id: awxx3cehszyb4datrqlycg2
title: Docker
desc: ''
updated: 1673709286075
created: 1673423404653
---

**Docker** is a set of platform as a service (PaaS) products which uses OS-level virtualization to deliver software in a _container_ . A container is light weight isolated virtual environment which runs reliably in any environment which has a docker engine.

#### Why do we need docker

Let say you have built some app. Which runs in a weird flavor of Linux  and it's written in COBOL. So lets say your trying to share this app with your friend. But he doesn't even use Linux or he doesn't even know what is COBOL. So he can't use your cool app. So we will  have have t o replicate our environment. We can use a virtual machine to do this which is the OG way to do it. In the VM the hardware is simulated and installed with the required OS and dependencies but because each VM has it's own OS they are bulky, heavy and slow. So you can use a docker container to share your app. Docker containers are the same as VM's but with a key difference is without virtualizing hardware the docker engine virtualized the OS and uses the shared kernel to run the applications. Which means docker containers are faster and light weight than VM's. In simple terms docker is fast, reliable and lightweight virtualization solution.

#### The universe of docker

- Docker File
  - The [[docker_file|docker-file]]  is like DNA it's code which describes how the docker image should be built.
- Docker Image
  - The docker image  is a snapshot of the software along with all it's dependencies to the operating system level.
  - The image is immutable it can be used to spin up multiple containers of the software in the real world.
- Docker Container
  - The docker container is the running docker image.
- Docker Compose
  - The [[docker_compose|docker-compose]] file is used to deploy multiple docker containers at once.

#### The docker cli and desktop app

- Docker has a a cli to interact with the docker engine
  - The [[docker_commands|docker-cli-commands]] can be used to build, deploy, kill and do many more things to docker containers.
- Docker also has desktop apps for Windows, Linux and Mac.  
