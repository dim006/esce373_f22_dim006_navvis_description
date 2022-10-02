## Instructions on viewing the package launch file with and without the GUI
# Without GUI:
+  Kill the roscore and RVIZ in the background, if any. run: fg , then hit CRTL+C
+  Start up the RVIZ to view the URDF version of the model. run:
roslaunch <package_name> <launch_file>.launch
+  To open RVIZ with the XACRO version of the model. run:
roslaunch <package_name> <launch_file>.launch use_xacro:=true

# With GUI:
+  Install the joint_state_publisher_gui package. run:
sudo apt-get install ros-melodic-joint-state-publisher-gui
+  Re-configure ROS, after installing the package. Then, restart the roscore.
+  Run RVIZ with the XACRO version of the model. run:
roslaunch <package_name> <launch_file>.launch use_xacro:=true &
+  Run the joint_state_publisher_gui. run:
rosrun joint_state_publisher_gui joint_state_publisher_gui &