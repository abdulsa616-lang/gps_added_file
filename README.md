# gps_added_file
integrated gps in this file ( camera , lidar , imu and gps )

# just add src folder of previous file and build it using that 

colcon build --symlink-install \
  --packages-up-to clearpath_gz clearpath_generator_gz clearpath_control

# run rover

ros2 launch clearpath_gz simulation.launch.py \
  setup_path:=$HOME/spaceborn_ws/clearpath \
  world:=warehouse \
  rviz:=false \
  generate:=true
  
