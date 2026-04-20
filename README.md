# Clone repo
```
git clone https://github.com/TNSang25/Giua-ki-ROS.git
```
# Các bước chạy
Chạy file launch :

```
ros2 launch robot_bringup robot_gazebo.launch.xml
```

Tiếp theo mở thêm 3 terminal mới và chạy các lệnh sau:
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
