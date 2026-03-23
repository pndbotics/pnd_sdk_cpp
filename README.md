# Overview

<div align="center">

[![Ubuntu](https://img.shields.io/badge/Ubuntu-20.04-E95420?logo=ubuntu&logoColor=white)](https://releases.ubuntu.com/20.04/)
[![Compiler](https://img.shields.io/badge/GCC-9.4.0-004482?logo=gnu&logoColor=white)](https://gcc.gnu.org/)
[![CMake](https://img.shields.io/badge/CMake-3.10%2B-064F8C?logo=cmake&logoColor=white)](https://cmake.org/)
[![Arch](https://img.shields.io/badge/Arch-aarch64%20%7C%20x86__64-lightgrey)](#)

![Updated At](https://img.shields.io/badge/Updated_At-March_2026-64748B?style=flat-square)
![Version](https://img.shields.io/badge/Version-1.0.0-2563EB?style=flat-square)
[![License](https://img.shields.io/badge/License-BSD--3--Clause-059669?style=flat-square)](https://opensource.org/licenses/BSD-3-Clause)

**High-performance C++ SDK for PNDbotics robots, supporting robot state acquisition and precise hardware control.**

</div>

## ✨ Features
- **Core C++ Implementation**: Optimized for low-latency robot control.
- **Cross-Architecture Support**: Full compatibility with `aarch64` and `x86_64` platforms.
- **Developer Friendly**: Standard CMake integration with clear modular examples.
- **Production Ready**: Tested for Ubuntu 20.04 LTS environments.

## 📋 Table of Contents
- [Environment Setup](#-environment-setup)
- [Installation](#-installation)
- [Run Example](#-run-example)
- [Reference](#-reference)
- [Contact](#-contact)
- [Version Log](#-version-log)

## 🛠 Environment Setup

### Prebuild Environment
- **OS**: Ubuntu 20.04 LTS
- **CPU**: aarch64 / x86_64
- **Compiler**: GCC 9.4.0
- **Tools**: CMake (version 3.10 or higher), Make

### Dependencies
Before building or running the SDK, ensure the following dependencies are installed:

```bash
sudo apt-get update
sudo apt-get install -y cmake g++ build-essential \
    libyaml-cpp-dev libeigen3-dev libboost-all-dev \
    libspdlog-dev libfmt-dev
```

## 📦 Installation

To build your own application with the SDK, you can install the pnd_sdk_cpp to your system directory:

```bash
cd ~/pnd_sdk_cpp
mkdir build
cd build
cmake .. 
sudo make install
```

Or install pnd_sdk_cpp to a specified directory:

```bash
cd ~/pnd_sdk_cpp
mkdir build
cd build
cmake .. -DCMAKE_INSTALL_PREFIX=/opt/pndbotics_robotics
sudo make install
```

> [!IMPORTANT]
> If you install to a non-standard path, remember to add that path to your `${CMAKE_PREFIX_PATH}` so that `find_package()` can locate the SDK in your own projects.


## 🚀 Run Example

- **Run on real robot**:

```bash
# Get network interface name
ip a

# Run the control example (replace enp59s0 with the wired network interface name)
cd ~/pnd_sdk_cpp/build/bin
sudo ./lite_ankle_swing_example enp3s0
```


## 📖 Reference

- **Integration**: See `example/cmake_sample` for a guide on importing the SDK into your own CMake project.

## 📞 Contact

- Email: info@pndbotics.com
- Wiki: https://wiki.pndbotics.com  
- SDK: https://github.com/pndbotics/pnd_sdk_cpp  
- Issues: https://github.com/pndbotics/pnd_sdk_cpp/issues

## 📜 Version Log

| Version | Date       | Updates                                                                              |
| ------- | ---------- | ------------------------------------------------------------------------------------ |
| v1.0.0  | 2026-03-20 | Initial release                               |

---

<div align="center">

[![Website](https://img.shields.io/badge/Website-PNDbotics-black?)](https://www.pndbotics.com)
[![Twitter](https://img.shields.io/badge/Twitter-@PNDbotics-1DA1F2?logo=twitter&logoColor=white)](https://x.com/PNDbotics)
[![YouTube](https://img.shields.io/badge/YouTube-ff0000?style=flat&logo=youtube&logoColor=white)](https://www.youtube.com/@PNDbotics)
[![Bilibili](https://img.shields.io/badge/-bilibili-ff69b4?style=flat&labelColor=ff69b4&logo=bilibili&logoColor=white)](https://space.bilibili.com/303744535)

**⭐ Star us on GitHub — it helps!**

</div>
