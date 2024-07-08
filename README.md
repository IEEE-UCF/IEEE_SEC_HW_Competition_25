# IEEE UCF SoutheastCon 2025 Hardware Competition Entry Documentation

## Package Partitioning:
### secbot_description
Holds all descriptive information about the robot itself, along with the worlds and models needed to simulate the competition course and other environments. This includes the urdf, custom models, and custom testing worlds.  
  

### secbot_navigation
Holds all config and launch files to the operation of Nav2. This includes the use of SLAM, AMCL, robot_localization, and Nav2 specific configs and testing launch files.  
  

### secbot_bring_up
Contains all config and launch files relevant to the hardware implementation of this workspace.  
  

### secbot_simulation
Contains all config and launch files relevant to the complete simualtion of this workspace.  

## Bringup Formats

### Full Bringup Software Commands
Inside of src_ws and in the same terminal:
- cd IEEE_SEC_HW_Competition/src_ws/
- . install/setup.bash
- ./full_bringup/sw_full_bringup

### Multi-Launch Software Commands
For each command below - Open a new terminal, source workspace, paste command:  
- ros2 launch secbot_simulation launch_sim.launch.py use_sim_time:=true
- ros2 launch secbot_navigation bringup_launch.py use_sim_time:=true
- ros2 launch secbot_navigation waypoint_launch.py
- ros2 launch secbot_navigation rviz2.launch.py

### Full Bringup Hardware Commands
Inside of src_ws and in the same terminal:
- . install/setup.bash
- ./full_bringup/hw_full_bringup

### Multi-Launch Hardware Commands
For each command below - Open a new terminal, source workspace, paste command:
- ros2 launch secbot_simulation launch_sim.launch.py
- ros2 launch secbot_navigation bringup_launch.py
- ros2 launch secbot_navigation waypoint_launch.py
- ros2 launch secbot_navigation rviz2.launch.py

