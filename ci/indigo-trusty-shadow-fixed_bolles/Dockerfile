# This file  was auto-generated with ros-industrial/docker/ci/sync.sh at Fri May 12 17:02:13 CEST 2017

FROM ros:indigo-ros-core
LABEL MAINTAINER "Isaac I.Y. Saito" <gm130s@gmail.com>

RUN echo 'debconf debconf/frontend select Noninteractive' | debconf-set-selections

# Add admin user of our own.
RUN useradd -m ubuntu && echo "ubuntu:ubuntu" | chpasswd && adduser ubuntu sudo

RUN apt-get update && apt-get install --no-install-recommends -y apt-utils ca-certificates emacs gnupg lsb-release ssh sudo tmux tree wget

RUN echo "deb http://packages.ros.org/ros-shadow-fixed/ubuntu $(lsb_release -sc) main" > /etc/apt/sources.list.d/ros-latest.list
RUN apt-key adv --keyserver "hkp://ha.pool.sks-keyservers.net" --recv-key "0xB01FA116"     || { wget "https://raw.githubusercontent.com/ros/rosdistro/master/ros.key" -O - | sudo apt-key add -; }

RUN sed -i "/^# deb.*multiverse/ s/^# //" /etc/apt/sources.list     && apt-get update -qq     && apt-get -qq install --no-install-recommends -y         build-essential         python-catkin-tools         python-pip         python-rosdep         python-wstool         ros-indigo-catkin         ssh-client     && apt-get clean     && rm -rf /var/lib/apt/lists/*
