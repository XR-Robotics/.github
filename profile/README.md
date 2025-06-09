**XR Robotics** is an open-source initiative for developers and professionals in **XR**, **robotics**, and **AI**. We provide XRoboToolkit, a suite of cross-device SDKs, frameworks, and sample applications that enable **real-time remote robot operation** through XR devices.

---

### 🧰 Repositories

#### 📦 Samples

| Repository                             | Description                                      |
|----------------------------------------|--------------------------------------------------|
| XRoboToolkit-Teleop-Sample-Python   | simulation and real robot teleoperation sample written in python |
| XRoboToolkit-Teleop-Sample-Cpp       | Bimanuel robot platform teleoperation sample written in C++             |

#### 🧩 Source Code

|Repository                              | Description                                                                 |
|----------------------------------------|-----------------------------------------------------------------------------|
| XRoboToolkit-Unity-Client              | Unity client source code for XR interface (PICO supported, more coming)  |
| BRobotAssistantLib                     | Android library component for Unity robot interface                      |
| XRoboToolkit-PC-Service                | Core C++ PC-side robotics service                                        |
| XRoboToolkit-PC-Service-Pybind         | Python binding for PC service SDK                                        |

> 📄 *Each repository contains its own README and setup instructions.*


---

## 🚀 Get Started

Follow these steps to build and run a full XR-to-robot teleoperation demo on **PICO 4 Ultra** and a **UR5 robot**.

1. **Install XRoboToolkit-PC-Service**  
   - [deb package for ubuntu 22.04](https://github.com/XR-Robotics/XRoboToolkit-PC-Service/releases/download/v1.0.0/XRoboToolkit-PC-Service_1.0.0_ubuntu_amd64.deb) 
   - Or build from the repo source.

2. **Clone & Set Up Python Teleop Sample**  
   - [XRoboToolkit-Teleop-Sample-Python](https://github.com/XR-Robotics/XRoboToolkit-Teleop-Sample-Python)

3. **Install the XR App on Headset**  
   - Download and install [XRoboToolkit-PICO.apk](https://github.com/XR-Robotics/XRoboToolkit-Unity-Client/releases/download/v1.0.0/XRoboToolkit-PICO.apk) on supported XR devices.

4. **Test in Real or Simulated Environment**  
   - Supports PICO 4 Ultra + UR5 (real or Gazebo/Isaac Sim simulations)

---

## 📦 Key Features

- 🌍 **Cross-device XR support** via [OpenXR](https://www.khronos.org/openxr/)
- 📡 **Low-latency video streaming**  
   - <100ms latency, <1% packet loss for both video and command
- 🎮 **Robot control via XR headset & controllers**
- 🧪 **Developer-friendly SDKs**  
   - Native C++ and Unity (URP/Android) clients
- 🧱 **Modular, expandable** architecture for future robot and headset support

---

## 🤝 Community & Collaboration

This project is initiated and maintained by **PICO** to open up its XR robotics framework for community use.

We welcome contributors from academia, industry, and the open-source robotics community.

- 💬 [Join the XR Robotics Discord](https://discord.gg/your-discord-link)
- 🐞 Use [Issues](https://github.com/XR-Robotics/XRoboToolkit/issues) & Discussions in each repo
- 📩 Contact: [yangning726@gmail.com](mailto:yangning726@gmail.com)

---

> ⚠️ This project is under active development. Contributions and feedback are highly encouraged.
