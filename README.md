# OpenCV with CUDA Docker Image
This repository contains Dockerfiles for creating Docker images of the [OpenCV](https://opencv.org/) computer vision library with [NVIDIA CUDA](https://developer.nvidia.com/cuda-zone) support based on the [official CUDA images](https://hub.docker.com/r/nvidia/cuda/).
The images contain the [opencv_contrib](https://github.com/opencv/opencv_contrib) modules and Python bindings.

Currently the images are based on the development (`devel`) version of the [images from Nvidia](https://hub.docker.com/r/nvidia/cuda/), so all the development tools are installed as well. It is on my TODO-List to include `base` and `runtime` versions corresponding to those from the Nvidia repository.

## Requirements
To build and run these containers leveraging NVIDIA GPUs, you need a Nvidia GPU, [Docker](https://docs.docker.com/get-docker/) and the [NVIDIA Container Toolkit](https://github.com/NVIDIA/nvidia-docker).

## Run
```bash
docker run julianassmann/opencv-cuda:cuda-<version>-opencv-<version>
```
e. g.
```bash
docker run julianassmann/opencv-cuda:cuda-10.2-opencv-4.2
```

## Building
If for any reason you dont want to use one of the prebuilt images available on [Dockerhub](https://hub.docker.com/repository/docker/julianassmann/opencv-cuda/), you can build the image yourself. Navigate to the directory corresponding with the correct versions for Ubutnu, CUDA and OpenCV respectively you want to build and run
```bash
docker build -t <image_name> .
```
