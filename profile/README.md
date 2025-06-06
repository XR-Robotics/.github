**XR Robotics** is an open-source initiative for developers and professionals in **XR**, **robotics**, and **AI**. We provide XRoboToolkit, a suite of cross-device SDKs, frameworks, and sample applications that enable **real-time remote robot operation** through XR devices.

---

## 🧰 Repositories

We offer a modular, multi-platform set of SDKs and sample projects to help you build XR-controlled robotics applications.  

### ✅ Core Components  
- `XRoboToolkit-PC-Service`: PC-side robot communication bridge
- `XRoboToolkit-Teleop-Sample-Python`: Python-based simulation and demo for UR5 robot
- `XRoboToolkit-Teleop-Demo-UR5`: Native C++ teleop example on a real robot arm  
- `XRoboToolkit-BRobotAssistantU3d`: Unity XR client source code  
- `XRoboToolkit-BRobotAssistantLib`: Android Unity plugin source  
- `XRoboToolkit-Unity-Demo`: Unity APK & PC installers (see individual repo README for download links)

> *Note: Each component has its own README and setup guide.*

---

## 🚀 Get Started

Follow these steps to build and run a full XR-to-robot teleoperation demo on **PICO 4 Ultra** and a **UR5 robot**.

1. **Install XRoboToolkit-PC-Service**  
   - (Windows: `...`, Linux: `...`)  
   - Or build from the repo source.

2. **Clone & Set Up Python Teleop Sample**  
   - [XRoboToolkit-Teleop-Sample-Python](https://github.com/XR-Robotics/XRoboToolkit-Teleop-Sample-Python)

3. **Install the XR App on Headset**  
   - Download and install `XRoboToolkit-PICO.apk` on supported XR devices.

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
