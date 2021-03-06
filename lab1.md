# Lab 1 - Prepare for OpenFaaS

<img src="https://github.com/openfaas/media/raw/master/OpenFaaS_Magnet_3_1_png.png" width="500px"></img>

OpenFaaS runs on top of several major platforms including Docker Swarm and Kubernetes. For this tutorial you can choose one of both on your local computer.

The basic primitive for any OpenFaaS function is a Docker image, which is built using the `faas-cli` tool-chain.

## Pre-requisites:

### Docker

For Mac

* [Docker CE for Mac Edge Edition](https://store.docker.com/editions/community/docker-ce-desktop-mac)

For Windows 

* Use Windows 10 Pro or Enterprise only
* Install [Docker CE for Windows](https://store.docker.com/editions/community/docker-ce-desktop-windows)

> Please ensure you use the **Linux** containers Docker daemon by using the Docker menu in the Windows task bar notification area.

* Install [Git Bash](https://git-scm.com/downloads)

When you install git bash pick the following options: `install UNIX commands` and `use true-type font`.

> Note: please use *Git Bash* for all steps: do not attempt to use *PowerShell*, *WSL* or *Bash for Windows*.

Linux - Ubuntu or Debian

* Docker CE for Linux

> You can install Docker CE from the [Docker Store](https://store.docker.com).

Note: As a last resort if you have an incompatible PC you can run the workshop on https://labs.play-with-docker.com/.

### Pre-pull the system images

Pull the most recent OpenFaaS images. 

```
curl -sSL https://raw.githubusercontent.com/openfaas/faas/master/docker-compose.yml | grep image | awk -F " " '{print $NF}' | xargs -L1 docker pull
```

This should offset the impact on the workshop WiFi of multiple attendees trying to pull the images at the same time.

### Setup a single-node cluster

If you're taking part in an instructor-lead event then the organiser may ask you to use Docker Swarm, because it's much quicker and easier to set up in a short period of time. For some workshops you will be using Kubernetes.

If you are working independently then choice is entirely your own.

Start the first lab by picking one of the tracks below:

* Docker Swarm: [Lab 1a](./lab1a.md)

* Kubernetes: [Lab 1b](./lab1b.md)

