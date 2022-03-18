# Reading 31 - Django REST Framework & Docker

## Beginner's Guide to Docker

**Docker** - isolate and runs entire applications

Docker does not need a virtual environment; it produces environments locally

### Linux Containers

What docker is; *linux container* is a form of *virtualization*.

**Virtualization** - copy of a computer system
-downside is size and speed.

- Linux containers (aka "containerization") has become increasingly popular.

- Virtual machine (virtualization) provides more resources and container is sufficient.

### Container v Virtual Environment

venv are utilized to separate Python software packages locally.

- issue is that venv can only isolate Python packages.

- reliant on global system level installation of Python albeit can refer to the proper version.

### Install Docker

1. Download desktop app on computer and create an account (should be on version 19).

  $ docker --version
  Docker version 19.03.5, build 633a0ea

- *docker compose* is another tool that is included with downloads of Docker.

**docker info** - a good command to inspect docker that contains a lot of output but focuses on the top lines that show that there is one container which is stopped and 1 image.

  $ docker info
  Containers: 1
    Running: 0
    Paused: 0
    Stopped: 1
  Images: 1

### Images and Containers

**image** - snapshot in time of what a project contains

**container** - running instance of the image.

*Baking Analogy*:

-*Dockerfile* is the recipe for the cake

-*image* is a snapshot of the recipe at a given time

-*docker-compose.yml* - says how to make the cake

-*container* is the actual, baked cake.

### Images

1.Create local directory on computer for code.

2.Define the image with a Dockerfile (`touch Dockerfile`)

3.text editor add -> # Dockerfile

First instruction must be the `FROM` the command.
-allows importing of a base image to use for image.

- Dockerfile read top to bottom.

### Image Builds

  $ docker image build .
  Sending build context to Docker daemon  2.048kB
  Step 1/1 : FROM python:3.7-alpine
  3.7-alpine: Pulling from library/python
  c9b1b535fdd9: Pull complete
  2cc5ad85d9ab: Pull complete
  53a2fca3c2ea: Pull complete
  30fce49de8b1: Pull complete
  49bcb9571cc7: Pull complete
  Digest: sha256:7655eea15dfd981eeb7d243af21e8561e967709caba938d50b136cdb992f3546
  Status: Downloaded newer image for python:3.7-alpine
  ---> b2c276538711
  Successfully built b2c276538711

### Image Layers 

image made up of one or more layers.

**Image Layering** - exists so that each image layer is *immutable*(unchanged) and for *performance*

Performance - Docker caches steps in Dockerfile to speed up subsequent builds.

-change made to a step: all steps following it will be executed from scratch; order matters in Dockerfile.

-put code that won't alter on *top* and altering code on *bottom*.

### Container

  $ cd ..
  $ mkdir djangoapp && cd djangoapp
  $ pipenv install django==3.0
  $ pipenv shell

## Django for APIs - Library Website

Django REST Framework = work alongside Django web framework to create web apis.

BUT cannot build web API with only Django Rest framework.

### Traditional Django

- same steps as shown in lecture and demonstrated in lab.

- Tests should be added before moving on to the API portion of a project.

-run git init and git status

-ACP.

[<==BACK](README.md)

