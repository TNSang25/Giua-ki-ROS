# Cần có
* [**ROS 2 Humble**](https://docs.ros.org/en/humble/index.html)

* [**Ignition Gazebo**](https://docs.ros.org/en/foxy/Tutorials/Advanced/Simulators/Ignition/Ignition.html)
```
sudo apt install ignition-fortress -y
```

* **ROS 2 - Ignition Bridge**
```
sudo apt install ros-humble-ros-gz -y
```

* **SLAM Toolbox**
```
sudo apt install ros-humble-slam-toolbox -y
```

* **rviz2**
```
sudo apt update
sudo apt install ros-humble-rviz2 -y

# Các plugin cần cho dự án
sudo apt install ros-humble-rviz-default-plugins -y
```
# Các Packages và chức năng
* [**gazebo_map**](gazebo_map) : tạo không gian mô phỏng (world) cho Robot trong Gazebo.
* [**my_robot_description**](my_robot_description) : tạo Robot với các folder urdf và meshes, cấu hình rviz.
* [**robot_bringup**](robot_bringup) : launch dự án, chứa file cấu hình bridge ROS2-Gazebo và SLAM ToolBox.
* [**robot_control**](robot_control) : chứa các node điều khiển các khớp tay máy, lái xe, và node đọc dữ liệu IMU.

# Clone repo
```
git clone https://github.com/TNSang25/Giua-ki-ROS.git
```
# Các bước chạy
**Chạy file launch** :

```
# Trỏ vào workspace 
colcon build
source install/setup.bash
ros2 launch robot_bringup robot_gazebo.launch.xml
```

**Tiếp theo mở thêm 3 terminal mới và chạy các lệnh sau**:
* Chạy node lái xe :

```
source install/setup.bash
ros2 run robot_control robot_keyboard
```

* Chạy node điều khiển tay máy :

```
source install/setup.bash
ros2 run robot_control arm_control
```

* Chạy node đọc dữ liệu IMU :

```
source install/setup.bash
ros2 run robot_control imu_reader
```
