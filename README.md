# Cần có
* [**ROS 2 Humble**](https://docs.ros.org/en/humble/index.html)
* **Ignition Gazebo**
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
# Clone repo
```
git clone https://github.com/TNSang25/Giua-ki-ROS.git
```
# Các bước chạy
**Chạy file launch** :

```
ros2 launch robot_bringup robot_gazebo.launch.xml
```

**Tiếp theo mở thêm 3 terminal mới và chạy các lệnh sau**:
* Chạy node lái xe :

```
ros2 run robot_control robot_keyboard
```

* Chạy node điều khiển tay máy :

```
ros2 run robot_control arm_control
```

* Chạy node đọc dữ liệu IMU :

```
ros2 run robot_control imu_reader
```
