# Images to build from
FROM osrf/ros:humble-desktop
#FROM osrf/ros:humble-desktop-full

# nvidia-container-runtime
ENV NVIDIA_VISIBLE_DEVICES \
    ${NVIDIA_VISIBLE_DEVICES:-all}
ENV NVIDIA_DRIVER_CAPABILITIES \
    ${NVIDIA_DRIVER_CAPABILITIES:+$NVIDIA_DRIVER_CAPABILITIES,}graphics

# Commands to run
SHELL [ "/bin/bash" , "-c" ]
RUN apt-get update
RUN apt-get install -y git && apt-get install -y python3-pip

RUN source /opt/ros/humble/setup.bash \
    && cd ~/ \
    && git clone https://github.com/Brynjath99/robotics-basics.git

RUN  apt install -y python3-colcon-common-extensions \
    && apt-get install -y ros-humble-joint-state-publisher-gui \
    && apt-get install -y ros-humble-gazebo-plugins \
    && apt-get install -y python3-colcon-mixin \
    && apt-get install -y python3-vcstool
    
RUN source /opt/ros/humble/setup.bash \
 && apt-get install -y ros-humble-joint-state-publisher \
 && apt-get install -y ros-humble-gazebo-ros \
 && apt-get install -y ~nros-humble-rqt*

RUN echo "source /opt/ros/humble/setup.bash" >> ~/.bashrc
RUN pip install opencv-python
RUN pip install pygame

RUN echo "ALL DONE !"