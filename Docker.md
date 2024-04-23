
> [!NOTE] do the docker app tutorials but try to do it using the CLI as well
## Docs 
Docker for Java Docs: 
https://docs.docker.com/language/java/?uuid=7d251890-079a-42fc-8e21-029080bfbefc%0A

Docker Compose Docs:
https://docs.docker.com/compose/compose-file/?uuid=7d251890-079a-42fc-8e21-029080bfbefc%0A

Dockerfile Docs: 
https://docs.docker.com/reference/dockerfile/

## Vids
Docker and Java tutorials:
Part 1: https://youtu.be/FzwIs2jMESM?si=U7X_469j6_ktE7iS
Part 2: https://youtu.be/_m9JYAvFB8s?si=-QCa7KzaC-1SmkHL

## Script Snippets
---
```bash 
docker init
```
- tool to create necessary docker files  (`.dockerignore`, `compose.yaml`, `Dockerfile`, `README.Docker.md`)

---
```bash
docker build -t <IMAGE_NAME>:<VERSION> .
```
- Builds new docker image from `Dockerfile`. 
- `<IMAGE_NAME>` can be anything 
- if no `<VERSION>` was specified it will default to "latest"
- images cannot be overwritten
- Don't forget period "." at the end!

---
```bash
docker image ls
```
- lists the current images on this device

---
```bash
docker run -p <EXT_PORT>:<CONTAINER_PORT> -d <IMAGE_NAME>:<VERSION>
```
- runs a image with ports exposed
- `-p` is the port flag
- `-d` for Daemon/Detached mode or `-it` for interactive mode
- image name will default to latest if no version specified
- `-e` can add env variables, good for setting username & password when running images that need them 
- image name can be replaced with the image id

---
```bash
docker ps
``` 
- view running containers 
- adding `-a` will show all containers 

---
```bash 
docker compose up
```
- runs the `compose.yaml` file (and dockerfile i think?)
- similar 
- if multiple services exist you can add the service name after `docker compose up` 
  (ie. `docker compose up postgres`)

