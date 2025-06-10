**XR Robotics** is an open-source initiative for developers and professionals in **XR**, **robotics**, and **AI**. We provide XRoboToolkit, a suite of cross-device SDKs, frameworks, and sample applications that enable **real-time remote robot operation** through XR devices.

---

### 🧰 Repositories

#### 📦 Samples

| Repository                             | Description                                      |
|----------------------------------------|--------------------------------------------------|
| [XRoboToolkit-Teleop-Sample-Python](https://github.com/XR-Robotics/XRoboToolkit-Teleop-Sample-Python#)   | simulation and real robot teleoperation sample written in python |
| [XRoboToolkit-Teleop-Sample-Cpp](https://github.com/XR-Robotics/XRoboToolkit-Teleop-Sample-Cpp#)       | Bimanuel robot platform teleoperation sample written in C++             |

#### 🧩 Source Code

|Repository                              | Description                                                                 |
|----------------------------------------|-----------------------------------------------------------------------------|
| [XRoboToolkit-Unity-Client](https://github.com/XR-Robotics/XRoboToolkit-Unity-Client)              | Unity client source code for XR interface (PICO supported, more coming)  |
| [BRobotAssistantLib](https://github.com/XR-Robotics/BRobotAssistantLib)                     | Android library component for Unity robot interface                      |
| [XRoboToolkit-PC-Service](https://github.com/XR-Robotics/XRoboToolkit-PC-Service)                | Core C++ PC-side robotics service                                        |
| [XRoboToolkit-PC-Service-Pybind](https://github.com/XR-Robotics/XRoboToolkit-PC-Service-Pybind)         | Python binding for PC service SDK                                        |

> 📄 *Each repository contains its own README and setup instructions.*

---
## 🚀 Get Started








<table>
<tr>
<td width="50%">

https://github.com/user-attachments/assets/288b3f30-11b8-458f-a596-a6c91a87a993

</td>
<td width="50%">

https://github.com/user-attachments/assets/0e86046d-b632-4f04-b290-4ebce8b21f9a

</td>
</tr>
</table>


Follow these steps to build and run a full XR-to-robot teleoperation sample on a **PICO 4 Ultra headset and a Linux x86 PC**. This sample has been tested only under the below system OS requirements:
Linux x86 PC: Ubuntu 22.04
PICO 4 Ultra: User OS >5.12. Special permission with enterprise version and VST camera permission is required for headset camera access.
1. **Install XRoboToolkit-PC-Service**  
   - Download [deb package for ubuntu 22.04](https://github.com/XR-Robotics/XRoboToolkit-PC-Service/releases/download/v1.0.0/XRoboToolkit_PC_Service_1.0.0_ubuntu_22.04_amd64.deb), or build from the [repo source](https://github.com/XR-Robotics/XRoboToolkit-PC-Service).
   - To install, use command
     ```bash
      sudo dpkg -i XRoboToolkit-PC-Service_1.0.0_ubuntu_22.04_amd64.deb
      ```
2. **Clone & Set Up Python Teleop Sample**  
   - [XRoboToolkit-Teleop-Sample-Python](https://github.com/XR-Robotics/XRoboToolkit-Teleop-Sample-Python)
3. **Install the XR App on Headset**
   - Turn on developer mode on Pico 4 Ultra headset first ([Enable developer mode on Pico 4 Ultra](https://developer.picoxr.com/ja/document/unreal/test-and-build/)), and make sure that [adb](https://developer.android.com/tools/adb) is installed properly.
   - Download [XRoboToolkit-PICO.apk](https://github.com/XR-Robotics/XRoboToolkit-Unity-Client/releases/download/v1.0.0/XRoboToolkit-PICO.apk) on a PC with adb installed.
   - To install apk on the headset, use command
     ```bash
      adb shell install XRoboToolkit-PICO.apk
      ```
4. **Run Sample in Simulated Environment or on Real Robot**
   - Connect robot PC and Pico 4 Ultra under the same network
   - On robot PC, double click app icon of `XRoboToolkit-PC-Service` or run service `/opt/apps/roboticsservice/runService.sh`
   - Open app `XRoboToolkit` on the Pico headset. Details of the Unity app can be found in the [Unity source repo](https://github.com/XR-Robotics/XRoboToolkit-Unity-Client).
   - Follow instructions on [XRoboToolkit-Teleop-Sample-Python](https://github.com/XR-Robotics/XRoboToolkit-Teleop-Sample-Python) to run test in simulated environment or on real robot.

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
