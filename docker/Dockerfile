# Images to build from
FROM osrf/ros:noetic-desktop-full

# Commands to run
RUN apt-get update
RUN apt-get install -y git && apt-get install -y python3-pip

RUN mkdir -p ~/catkin/_ws/src && ~/catkin_ws/src 

RUN git clone git@github.com:Brynjath99/robotics-basics.git && \
    cd ~\catkin_ws/src/


RUN source devel/setup.bash

RUN echo "ALL DONE !"