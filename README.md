# Download

  ```
  git clone git@github.com:RaffaeleCrocco/fundamental-of-robotic.git
  cd src
  git clone https://github.com/JenniferBuehler/gazebo-pkgs.git
  git clone https://github.com/JenniferBuehler/gazebo-pkgs.git
  ```

# Installation

After downloading all the files, build using catkin build

  ```
  cd fundamental-of-robotic
  source /opt/ros/noetic/setup.bash
  catkin build
  source devel/setup.bash
  ```
Give execution permission to the scripts

  ```
  chmod +x spawner/spawner_1.py

  chmod +x src/ur5/ur5_gazebo/scripts/send_joints.py
  chmod +x src/ur5/ur5_gazebo/scripts/vision.py
  ```

Launch the gazebo world

  ```
  roslaunch ur5_gazebo ur5_world_1.launch
  ```
Unpause the simulation. Launch vision script

  ```
  rosrun ur5_gazebo vision.py
  ```
You can spawn random legos in random position using the spawner script

  ```
  ./spawner/spawner_1.py
  ```

You can tell the ur5 to pick up the legos

  ```
  rosrun ur5_gazebo send_joint.py
  ```
