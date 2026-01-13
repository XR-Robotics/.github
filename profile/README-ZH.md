## 🤖 XR Robotics 简介

**XR Robotics** 是一个面向 **机器人，具身智能，XR** 开发者和专业人士的开源项目。

我们提供 **XRoboToolkit** —— 一套跨设备的 SDK、框架和示例应用，支持通过 **XR 设备对机器人进行实时远程遥操作（Teleoperation）**，适用于仿真环境与真实机器人系统。

- 🌐 **官网与论文**：https://xr-robotics.github.io/  
- 📺 **YouTube 频道**：@XRRobotics  
- 🧩 **PICO 开发者示例**：PICO Developer GitHub  

### 核心功能
* [PICO 4 Ultra 头显](https://www.picoxr.com/cn/products/pico4-ultra) 人形机器人，半人形移动机器人，双臂机器人通用，机器人视觉和触觉等反馈
* 低延迟第一人称视频传输（<100ms，< 1% 丢包率），
* [PICO 体感追踪器](https://www.picoxr.com/cn/products/pico-motion-tracker) 支持[【全身追踪】](https://developer-cn.picoxr.com/document/unity/body-tracking/)和[【独立追踪】](https://developer-cn.picoxr.com/document/unity/object-tracking/)
* C++，python, Unity SDK，OpenXR
* x86 ubuntu，arm64 ubuntu（nvidia orin），windows适配
* MuJoCo，[NVIDIA Isaac Lab](https://isaac-sim.github.io/IsaacLab/main/index.html) 仿真平台支持（持续更新）
* 注：如需PICO企业支持，采购，和头显原始相机数据，请购买 PICO 4 Ultra 企业版。商业合作和定制开发，请联系 Ke Jing (ke.jing@bytedance.com)


---

## 🧰 项目仓库

### 📦 示例项目（Samples）

| 仓库 | 说明 |
|------|------|
| **XRoboToolkit-Teleop-Sample-Python** | 使用 Python 编写的仿真与真实机器人遥操作示例 |
| **XRoboToolkit-Teleop-Sample-Cpp** | 使用 C++ 编写的双臂（Bimanual）机器人遥操作示例 |

---

### 🧩 核心源码（Source Code）

| 仓库 | 说明 |
|------|------|
| **XRoboToolkit-Unity-Client** | XR 端 Unity 客户端源码（当前支持 PICO，后续将支持更多设备） |
| **BRobotAssistantLib** | 面向 Unity 机器人接口的 Android 底层库 |
| **XRoboToolkit-PC-Service** | PC 端核心 C++ 机器人服务 |
| **XRoboToolkit-PC-Service-Pybind** | PC 端服务的 Python SDK 绑定 |

> 📄 每个仓库均包含独立的 README 与完整的安装和使用说明。

---

## 🚀 快速开始

🎥 示例视频：  
- `robot_teleoperation.mp4`  
- `simulation_teleoperation.mp4`  

以下步骤将指导你在 **PICO 4 Ultra 头显** 与 **Linux x86 PC** 上，构建并运行完整的 XR → 机器人遥操作示例。

### 系统要求（已测试环境）

- **Linux x86 PC**：Ubuntu 22.04  
- **PICO 4 Ultra**：  
  - 系统版本 > 5.12  
  - 需要企业版权限  
  - 需要 VST 相机访问权限（用于头显相机数据访问）

---

### 1️⃣ 安装 XRoboToolkit PC 服务

- 下载适用于 Ubuntu 22.04/ Ubuntu 24.04 的 `.deb` 安装包，或从源码仓库自行构建  
- 安装命令：

```bash
sudo dpkg -i XRoboToolkit-PC-Service_1.0.0_ubuntu_22.04_amd64.deb
```


**核心功能**


**传输延迟如何测量的**

使用如图所示的灯来计算当前灯上的数值和头显显示的灯的数值 在100ms以内


当前各模块测试（分辨率2560\*720）

VST上屏渲染 11ms （已经是最快的方案）

H264视频流接收+视频解码 约25ms

PICO 4 Ultra 视频流压缩约20ms，（如果换成zed mini 使用高性能PC压缩约3ms）

同路由器延迟约43ms

**如何开始？**

1\. **在控制机器人的电脑上安装 XRoboToolkit-PC-Service (推荐x86 ubuntu22.04)**

arm64 Ubuntu 22.04用户， 下载 deb package [XRoboToolkit-PC-Service-headless_1.0.0.0_arm64.deb](https://github.com/XR-Robotics/XRoboToolkit-PC-Service/releases/download/v1.0.0/XRoboToolkit-PC-Service-headless_1.0.0.0_arm64.deb)

x86 ubuntu22.04 用户， 下载 deb package [XRoboToolkit_PC_Service_1.0.0_ubuntu_22.04_amd64.deb](https://github.com/XR-Robotics/XRoboToolkit-PC-Service/releases/download/v1.0.0/XRoboToolkit_PC_Service_1.0.0_ubuntu_22.04_amd64.deb)

```Plain Text  
sudo dpkg -i <file_name>.deb
```
x86 用户可以直接点击应用图标开始。也可以使用命令行

arm64 用户使用命令行

```Plain Text  
cd /opt/apps/roboticsservice  
bash runService.sh
```

Windows 用户， 下载 package [XRoboToolkit-PC-Service.win.zip](https://github.com/XR-Robotics/XRoboToolkit-PC-Service/releases/download/v1.0.0/XRoboToolkit-PC-Service.win.zip)

解压后运行 exe文件

2\. **下载python sample code**

<https://github.com/XR-Robotics/XRoboToolkit-Teleop-Sample-Python>

3\. **在头显上安装 XR app**

暂不支持Pico 4U以前的头显

打开pico 4 U 开发者模式，保证电脑安装了adb

PC上下载 apk 文件[XRoboToolkit-PICO-1.1.1.apk](https://github.com/XR-Robotics/XRoboToolkit-Unity-Client/releases/download/v1.1.1/XRoboToolkit-PICO-1.1.1.apk)

使用adb 安装apk

```Plain Text  
adb install -g XRoboToolkit-PICO-1.1.1.apk
```

4\. **运行程序**

开源版XRoboToolkit ：控制机器人的电脑需要和pico 4 U 头显在同一个网络环境下

商业版： 正在开发，远距离传输低延迟+多种机器人适配+ 大规模数据采集+VLA模型训练。详情咨询 [ke.jing@bytedance.com](mailto:ke.jing@bytedance.com)

头显上打开 app XRoboToolkit。

连接控制机器人电脑的IP

勾选 head，hand，controller，

根据[XRoboToolkit-Teleop-Sample-Python](https://github.com/XR-Robotics/XRoboToolkit-Teleop-Sample-Python) 教程 运行仿真和真机控制程序

[XRoboToolkit-Teleop-Sample-Python](https://github.com/XR-Robotics/XRoboToolkit-Teleop-Sample-Python) 的安装过程会同时安装 XRobotoolkit-PC-Service-Pybind

**核心代码仓库**

1\. **XRoboToolkit-PC-Service**

提供两个branch，需要自己编译的客户参考，

main branch 适配x86 平台电脑 <https://github.com/XR-Robotics/XRoboToolkit-PC-Service/tree/main>

Orin branch 适配 arm64平台电脑 <https://github.com/XR-Robotics/XRoboToolkit-PC-Service/tree/orin>

常见问题：

- 那里下载deb文件？

在<https://github.com/XR-Robotics/XRoboToolkit-PC-Service/releases/tag/v1.0.0>

- 如何确认我需要什么平台的软件？

使用什么平台的软件以控制机器人的电脑为准

- GRPC 相关文件找不到？

orin版本源代码在 orin branch

- 能不能外加别的设备？

可以，需要自行修改

- 我的网络有问题吗？

测试头显是否畅通X86平台可以通过可视化UI确认

Orin 平台请使用 XRobotoolkit-PC-Service-Pybind/examples

2\. **XRobotoolkit-PC-Service-Pybind**

提供接收头显数据的python sdk

对于有机器人开发经验的用户或机器人厂商基本只需要 （XRobotoolkit-PC-Service+pybind）

里面的example可以用于测试头显是否能和机器人沟通

常见问题

- 怎么安装Python库

参考<https://github.com/XR-Robotics/XRoboToolkit-PC-Service-Pybind>

选择对应平台，推荐ubuntu 22

- 为什么我拿到的数据全是0

如果其他安装没有问题，可能是vpn或者路由器有防火墙。 全是0代表没有接收到头显数据。建议重启一遍再测

- 怎么全身追踪

全身追踪请首先在头显calibrate motion tracker。在app里选择full body tracking

```Python  
import xrobotoolkit_sdk as xrt  
xrt.init()  
# Check if body tracking data is available  
if xrt.is_body_data_available():  
# Get body joint poses (24 joints, 7 values each: x,y,z,qx,qy,qz,qw)  
body_poses = xrt.get_body_joints_pose()  
print(f"Body joints pose data: {body_poses}")  
# Get body joint velocities (24 joints, 6 values each: vx,vy,vz,wx,wy,wz)  
body_velocities = xrt.get_body_joints_velocity()  
print(f"Body joints velocity data: {body_velocities}")  
# Get body joint accelerations (24 joints, 6 values each: ax,ay,az,wax,way,waz)  
body_accelerations = xrt.get_body_joints_acceleration()  
print(f"Body joints acceleration data: {body_accelerations}")  
# Get IMU timestamps for each joint  
imu_timestamps = xrt.get_body_joints_timestamp()  
print(f"IMU timestamps: {imu_timestamps}")  
# Get body data timestamp  
body_timestamp = xrt.get_body_timestamp_ns()  
print(f"Body data timestamp: {body_timestamp}")  
# Example: Get specific joint data (Head joint is index 15)  
head_pose = body_poses\[15\] # Head joint  
x, y, z, qx, qy, qz, qw = head_pose  
print(f"Head pose: Position({x:.3f}, {y:.3f}, {z:.3f}) Rotation({qx:.3f}, {qy:.3f}, {qz:.3f}, {qw:.3f})")  
else:  
print("Body tracking data not available. Make sure:")  
print("1. PICO headset is connected")  
print("2. Body tracking is enabled in the control panel")  
print("3. At least two Pico Swift devices are connected and calibrated")  
xrt.close()
```

- 怎么手部追踪

```Python  
import xrobotoolkit_sdk as xrt  
xrt.init()  
# Left Hand State  
left_hand_tracking_state = xrt.get_left_hand_tracking_state()  
print(f"Left Hand State: {left_hand_tracking_state}")  
# Left Hand isActive  
left_hand_is_active = xrt.get_left_hand_is_active()  
print(f"Left Hand isActive: {left_hand_is_active}")  
# Right Hand State  
right_hand_tracking_state = xrt.get_right_hand_tracking_state()  
print(f"Right Hand State: {right_hand_tracking_state}")  
# Right Hand isActive  
right_hand_is_active = xrt.get_right_hand_is_active()  
print(f"Right Hand isActive: {right_hand_is_active}")  
xrt.close()
```

- 物体追踪找不到

物体追踪需要选择object tracking. 追踪范围1.2米

```Python  
num_motion_data = xrt.num_motion_data_available()  
print(f"Number of Motion Trackers: {num_motion_data}")  
if num_motion_data > 0:  
motion_tracker_pose = xrt.get_motion_tracker_pose()  
motion_tracker_velocity = xrt.get_motion_tracker_velocity()  
motion_tracker_acceleration = xrt.get_motion_tracker_acceleration()  
motion_tracker_serial_numbers = xrt.get_motion_tracker_serial_numbers()  
motion_timestamp_ns = xrt.get_motion_timestamp_ns()  
print(f"Motion Tracker Pose: {motion_tracker_pose}")  
print(f"Motion Tracker Velocity: {motion_tracker_velocity}")  
print(f"Motion Tracker Acceleration: {motion_tracker_acceleration}")  
print(f"Motion Tracker Serial Numbers: {motion_tracker_serial_numbers}")  
print(f"Motion Timestamp (ns): {motion_timestamp_ns}")
```

3\. **XRoboToolkit-Teleop-Sample-Python**

提供多种类型机器人实例代码（双臂，灵巧手，移动底盘）  
机器人控制细节， 仿真以及真机控制代码，参考以下文档 <https://github.com/XR-Robotics/XRoboToolkit-Teleop-Sample-Python>



常见问题

- 如何适配人形机器人

人形机器人控制可以参考以下合作项目

[TWIST2](https://yanjieze.com/TWIST2/)



[SONIC](https://nvlabs.github.io/SONIC/)



- 用了什么运动学逆解

基于pinochino 的placo

- 灵巧手是怎么控制的

Hand tracking+ dex retargeting

4\. **Unity-Client**

基于OpenXR开发的应用程序，如果需要使用头显前置摄像头需使用PICO 企业版硬件并联系pico开通相机权限

支持zed mini相机视频流传输

unity和机器人通信细节 <https://github.com/XR-Robotics/XRoboToolkit-PC-Service>

常见问题

- 怎么连接另一台头显？

确保XRobotoolkit 应用有相机权限，然后选中Pico4U 点击listen

- 我是否可以用其他相机？

可以，需要修改Unity client里面的参数

[Remote stereo vision sync between Realsense camera and XR headset · Issue #6 · XR-Robotics/XRoboTool](https://github.com/XR-Robotics/XRoboToolkit-Unity-Client/issues/6)

- Zed mini注意事项

Zed mini是一种双目RGB-D相机，需要搭配nvidia 显卡使用，需要先安装zed sdk

<https://www.stereolabs.com/docs/zed-ecosystem>

- Zed mini + orin/ubuntu通信有问题

参考以下orin sender

[Cannot get stereo vision from ZED MINI · Issue #8 · XR-Robotics/XRoboToolkit-Unity-Client](https://github.com/XR-Robotics/XRoboToolkit-Unity-Client/issues/8)

- Windows + zed mini 通信有问题

下载 [XRoboToolkit-RobotVision-Console.win.zip](https://github.com/XR-Robotics/XRoboToolkit-RobotVision-PC/releases/download/v1.0.0/XRoboToolkit-RobotVision-Console.win.zip)

```Plain Text  
RobotVisionConsole.exe --tcp-camera -c --ip {HEADSET_IP} --port 12345 --width 1280 --height 720 --fps 60 --bitrate 4000000
```

**机器人仿真**

1\. **Nvidia Isaac Lab**

目前已和英伟达合作，后续会更新教程



2\. **MuJoCo 仿真**

详情参考 XRoboToolkit-Teleop-Sample-Python
