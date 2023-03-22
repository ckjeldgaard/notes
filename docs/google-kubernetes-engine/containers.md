---
sidebar_position: 1
---

# Containers

> Intro to containers

Flaws with traditional servers:

- Hard disks can fail
- High availability
- Off-peak utilization = wasted resources

... one solution: **virtualization** (abstract the physical server away, e.g. VMWare)

## Virtual problems

- Single OS, libs and dependencies **per VM**
- Difficulty separating **applications**
- No automation problems solved
- Complex configuration management systems

## Containers

- Packaging an application
- Write once, run anywhere
- Easily deploy to dev, test, production
- Easily deploy to GKE, VMs, bare metal
- Packaged applications speed development
- Make changes fast
- Promote microservices

### What are containers good for?

- Stateless microservices
- Frontends
- Backends
- Applications that need horizontal elasticity

### What are containers bad for?

- Applications that write to local disk
- Non-scaling resource - intensive monoliths (like SAP)
- Apps that require manual intervention to install
- Databases

## Docker

- Developer-friendly container creation and deployment
- Tools for handling container **images** and **registries**
- **Swarm** - Docker's own orchestration system
- Standards in Open Container Initiative

### Docker characteristics

- Containers start life as an image 
- Each instruction in the `Dockerfile` creates a new container layer
- A running container has a read-write layer on top of the image
- `Dockerfile`
  - Simple text configuration
  - Use existing images as building blocks
  - Add files, run commands, and perform other actions
  - Specify what should be running when the container runs
- Use `docker build` to build a new **image**. E.g. `docker build -t myapp .` (`-t` adds a 'tag' or name to the image to refer to it later)
- Use `docker run` to run the image. E.g. `docker run -d myapp`. (`-d` daemonizes the process and puts it in the background)

```bash
docker ps # view running and stopped containers
docker stop container-name # stop containers
docker logs container-name # view logs
docker rm # delete containers

docker images # view local images
docker tag myapp gcr.io/myapp # tag on remote registries
docker tag push gcr.io/myapp # push to remote registries
docker rmi # remove local images
```

### Example Docker file

```dockerfile
FROM ubuntu:18.04
COPY . /app
RUN make /app
CMD python /app/app.py
```
