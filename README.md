# 5g-ws



# How to Use

* Init submodules:

  ```bash
  git clone git@github.com:5G-Swarm/5g-ws.git
  cd 5g-ws
  git submodule init
  git submodule update
  ```
  
* Compiling ROS libraries:
  You can ignore some libraries first, for example:
  ```bash
  cd ros-rtk-driver
  touch CATKIN_IGNORE
  cd ..
  ```
  Then compiling ROS libraries you need:
  ```bash
  catkin_make
  ```
  
* Install informer2:
  If you use conda, activate your environment first:
  
  ```bash
  conda activate ${env_name}
  ```
  Install informer:
  ```bash
  cd informer2
  bash install.sh
  cd ..
  ```
  or use:
  ```bash
  cd informer2
  pip(3) install -e .
  cd ..
  ```
  
* Generate protobuf files, for example:
  ```bash
  cd ros-edge-transfer/scripts
  bash gen_pb.sh
  ```
* Run your node:
  ```bash
  cd ../../../
  source devel/setup.bash
  cd src/ros-edge-transfer/scripts
  python edge-vehicle.py
  ```

