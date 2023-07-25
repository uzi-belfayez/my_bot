## Robot Package Template

This is a GitHub template. You can make your own copy by clicking the green "Use this template" button.

It is recommended that you keep the repo/package name the same, but if you do change it, ensure you do a "Find all" using your IDE (or the built-in GitHub IDE by hitting the `.` key) and rename all instances of `my_bot` to whatever your project's name is.


write this command to control the robot with ros2 control:

ros2 run teleop_twist_keyboard teleop_twist_keyboard --ros-args -r /cmd_vel:=/diff_cont/cmd_vel_unstamped

write this command to launch SLAM Toolbox : 

ros2 launch slam_toolbox online_async_launch.py params_file:=./src/my_bot/config/mapper_params_online_async.yaml use_sim_time:=true

write this command to remap topics using twist_mux:

ros2 run twist_mux twist_mux --ros-args --params-file ./src/my_bot/config/twist-mux.yaml -r cmd_vel_out:=diff_cont/cmd_vel_unstamped

write this command to launch nav2:

ros2 launch nav2_bringup navigation_launch.py use_sim_time:=true



