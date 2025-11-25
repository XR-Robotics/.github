**XR Robotics** is an open-source initiative for developers and professionals in **XR**, **robotics**, and **AI**. We provide XRoboToolkit, a suite of cross-device SDKs, frameworks, and sample applications that enable **real-time remote robot teleoperation** through XR devices.

- **Website and paper**: [https://xr-robotics.github.io/](https://xr-robotics.github.io/)
- **YouTube channel**: [@XRRobotics](https://www.youtube.com/@XRRobotics)
- **PICO Developer samples**: [PICO Developer GitHub](https://github.com/Pico-Developer/)

---

### 🧰 Repositories

#### 📦 Samples

| Repository                             | Description                                      |
|----------------------------------------|--------------------------------------------------|
| [XRoboToolkit-Teleop-Sample-Python](https://github.com/XR-Robotics/XRoboToolkit-Teleop-Sample-Python)   | simulation and real robot teleoperation sample written in python |
| [XRoboToolkit-Teleop-Sample-Cpp](https://github.com/XR-Robotics/XRoboToolkit-Teleop-Sample-Cpp)       | Bimanuel robot platform teleoperation sample written in C++             |

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


Follow these steps to build and run a full XR-to-robot teleoperation sample on a **[PICO 4 Ultra headset](https://www.staples.com/pico-4-ultra-enterprise-virtual-reality-headset-qualcomm-snapdragon-mixed-reality-white-p9001sw40679h/product_24626400) and a Linux x86 PC**. This sample has been tested only under the below system OS requirements:
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
   - Download [XRoboToolkit-PICO-1.1.1.apk](https://github.com/XR-Robotics/XRoboToolkit-Unity-Client/releases/download/v1.1.1/XRoboToolkit-PICO-1.1.1.apk) on a PC with adb installed. <sup>[[Other Versions](https://github.com/XR-Robotics/XRoboToolkit-Unity-Client/releases)]</sup>
   - To install apk on the headset, use command
     ```bash
      adb install -g XRoboToolkit-PICO-1.1.1.apk
      ```
4. **Run Sample in Simulated Environment or on Real Robot**
   - Connect robot PC and PICO 4 Ultra under the same network
   - On robot PC, double click app icon of `XRoboToolkit-PC-Service` or run service `/opt/apps/roboticsservice/runService.sh`
   - Open app `XRoboToolkit` on the PICO headset. Details of the Unity app can be found in the [Unity source repo](https://github.com/XR-Robotics/XRoboToolkit-Unity-Client).
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

## 🤝 Applications & Gallery
- [SEEC: Stable End-Effector Control with Model-Enhanced Residual Learning for Humanoid Loco-Manipulation](https://arxiv.org/abs/2509.21231)  
  from Georgia Institute of Technology and Tsinghua University

- [TWIST2: A Scalable, Portable, and Holistic Humanoid Data Collection System](https://yanjieze.com/TWIST2/)  
  from Amazon FAR, Stanford, USC, UC Berkeley, and CMU

- [End-to-End Dexterous Arm-Hand VLA Policies via Shared Autonomy: VR Teleoperation Augmented by an Autonomous Hand VLA Policy for Efficient Data Collection](https://arxiv.org/abs/2511.00139)  
  from ByteDance Seed

- [SONIC: Supersizing Motion Tracking for Natural Humanoid Whole-Body Control](https://nvlabs.github.io/SONIC/)  
  from Nvidia



## 🤝 Community & Collaboration

This project is initiated and maintained by **PICO** as an open-source XR robotics framework for the community.

We welcome all contributors from academia, industry, and the open-source robotics community.

```
@article{zhao2025xrobotoolkit,
      title={XRoboToolkit: A Cross-Platform Framework for Robot Teleoperation}, 
      author={Zhigen Zhao and Liuchuan Yu and Ke Jing and Ning Yang}, 
      journal={arXiv preprint arXiv:2508.00097},
      year={2025}
}
```

- 💬 [Join the XR Robotics Discord](https://discord.gg/your-discord-link)
- 🐞 Use [Issues](https://github.com/XR-Robotics/XRoboToolkit/issues) & Discussions in each repo
- 📩 Contact: Ning Yang ([yangning726@gmail.com](mailto:yangning726@gmail.com)), Ke Jing ([drkejing@gmail.com](mailto:drkejing@gmail.com)).

---

## News
XRoboToolkit has been accepted to SII 2026 — [The 2026 IEEE/SICE International Symposium on System Integration](https://sice-si.org/SII2026/)!

> ⚠️ This project is under active development. Contributions and feedback are highly encouraged.
