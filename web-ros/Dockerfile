FROM ros:humble

SHELL ["/bin/bash", "-c"]

RUN apt-get update -y \
 && apt-get install -y libopencv-dev python3-opencv ros-humble-image-transport \
  ros-humble-async-web-server-cpp ros-humble-cv-bridge 

COPY . .
WORKDIR /web_ws

RUN source /opt/ros/humble/setup.bash \
 #&& rosdep install --from-paths src --ignore-src --rosdistro humble -y \
 && colcon build --symlink-install 

WORKDIR ..

ENTRYPOINT source ros_entrypoint.sh && source /web_ws/install/setup.bash && ros2 launch web_video_server web_video_server.launch.py
