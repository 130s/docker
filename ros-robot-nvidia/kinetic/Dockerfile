# nvidia-docker build -t rosindustrial/ros-robot-nvidia:kinetic .
FROM rosindustrial/ros-base-nvidia:kinetic
LABEL maintainer "Austin.Deric@SwRI.org"

RUN apt-get update && apt-get install -y \
    ros-kinetic-robot=1.3.1-0* \
&& rm -rf /var/lib/apt/lists/*
