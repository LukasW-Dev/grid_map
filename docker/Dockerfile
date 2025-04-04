FROM ros:humble

# Install necessary dependencies
RUN apt-get update && \
    apt-get install -y \
    ros-humble-grid-map \
    && rm -rf /var/lib/apt/lists/*

# Initialize rosdep
RUN rosdep update

# Create workspace and clone grid_map repository
WORKDIR /root/ros_ws/src

# Copy the grid_map repository from the host into the container
COPY ../.. /root/ros_ws/src/grid_map

# Install dependencies
WORKDIR /root/ros_ws
RUN rosdep install --from-paths src --ignore-src -r -y

# Build the workspace (Ensure ROS is sourced before running colcon build)
RUN /bin/bash -c "source /opt/ros/humble/setup.bash && colcon build"

# Source the setup files automatically
RUN echo "source /opt/ros/humble/setup.bash" >> ~/.bashrc
RUN echo "source /root/ros_ws/install/setup.bash" >> ~/.bashrc

CMD ["bash"]
