# Images to build from
FROM osrf/ros:noetic-desktop

# Commands to run
RUN apt-get update
RUN apt-get install -y git && apt-get install -y pthon3-pip
RUN source /opt/ros/noetic/setup.bash \
    && cd ~/ \
    && git clone git@github.com:Brynjath99/robotics-basics.git

RUN mkdir -p ~/catkin/_ws/src && ~/catkin_ws/src 

RUN source devel/setup.bash

RUN echo "ALL DONE !"