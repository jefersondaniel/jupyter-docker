# Jupyter Container Setup

## Requirements

* [Nvidia Docker](https://github.com/NVIDIA/nvidia-docker)

## Running container

```bash
./bin/run-jupyter-container # Create container bound to current directory
./bin/run-jupyter-container --recreate # Recreate container
```

## Rebuilding image

```bash
git clone https://github.com/jupyter/docker-stacks.git
cd docker-stacks/base-notebook
docker build --build-arg BASE_CONTAINER=nvidia/cuda:10.1-cudnn7-devel-ubuntu14.04 -t jefersondaniel/jupyter-nvidia-notebook base-notebook
```
