# Robotics Arm Simulation with ROS & Gazebo

The project is built using ROS Noetic and Gazebo 11.


---

## Prerequisites

Before you begin, you must have a compatible operating system and the correct versions of ROS and Gazebo.

*   **Operating System:** **Ubuntu 20.04 (Focal Fossa)** is required for ROS Noetic.
*   **ROS Version:** **ROS Noetic Ninjemys**.
*   **Gazebo Version:** **Gazebo 11**.

This guide provides two installation paths: a native Ubuntu 20.04 system or a Windows 10/11 system using WSL2.

---

## Installation Guide

Follow the guide for your specific operating system.

### **Option 1: Native Ubuntu 20.04 Installation**

This is the recommended method for the best performance.

#### **Step 1: Install ROS Noetic**

If you don't have ROS Noetic installed, follow the official guide. The `desktop-full` installation is recommended as it includes Gazebo and other useful tools.

*   [Official ROS Noetic Installation Guide](http://wiki.ros.org/noetic/Installation/Ubuntu)

If you already have ROS Noetic but did not install the `desktop-full` version, you can install the required Gazebo packages with the following command.

```bash
sudo apt update
sudo apt install ros-noetic-gazebo-ros-pkgs ros-noetic-gazebo-ros-control
```
> **Note:** This command is the preferred way to install Gazebo for ROS. It automatically installs Gazebo 11 and all the necessary plugins (`gazebo_ros`, `gazebo_plugins`, etc.) to ensure seamless integration.

#### **Step 2: Verify the Installation**

1.  **Check Gazebo Version:**
    Open a new terminal and run:
    ```bash
    gazebo --version
    ```
    You should see `Gazebo multi-robot simulator, version 11.x.x`.

2.  **Launch Gazebo:**
    You can launch a simple empty world to make sure the GUI works correctly.
    ```bash
    gazebo
    ```
    A 3D window showing an empty world should appear.

---

### **Option 2: Windows 10/11 with WSL2 Installation**

This method allows you to run the simulation on a Windows machine using the Windows Subsystem for Linux (WSL2). GUI support is handled by WSLg.

#### **Step 1: Setup WSL2 with GUI Support**

Before installing ROS, you must configure WSL2 correctly.

1.  **Install WSL2:**
    Open PowerShell **as an Administrator** and run the following command. This will install WSL and the default Ubuntu distribution (which should be 20.04 or 22.04). If it installs 22.04, you may need to manually install an Ubuntu 20.04 distribution from the Microsoft Store for ROS Noetic compatibility.
    ```powershell
    wsl --install
    ```
    If you already have WSL, ensure it is updated to get WSLg support for GUI applications:
    ```powershell
    wsl --update
    ```
    Restart your computer if prompted.

2.  **Install GPU Drivers for WSL:**
    This step is **critical** for Gazebo's performance. You must install the specific drivers for your GPU that support WSL.
    *   [**NVIDIA Drivers for WSL**](https://developer.nvidia.com/cuda/wsl)
    *   [**Intel Drivers for WSL**](https://www.intel.com/content/www/us/en/support/articles/000058387/graphics.html)
    *   [**AMD Drivers for WSL**](https://www.amd.com/en/support/kb/release-notes/rn-rad-win-wsl-support)

#### **Step 2: Install ROS Noetic on WSL**

Now, launch your Ubuntu 20.04 terminal from the Windows Start Menu and follow the exact same steps as the native installation.

1.  **Follow the official ROS Noetic installation guide** inside your WSL terminal:
    *   [Official ROS Noetic Installation Guide](http://wiki.ros.org/noetic/Installation/Ubuntu)

2.  **Install the Gazebo packages for ROS:**
    ```bash
    sudo apt update
    sudo apt install ros-noetic-gazebo-ros-pkgs ros-noetic-gazebo-ros-control
    ```

#### **Step 3: Verify the Installation on WSL**

1.  **Check Gazebo Version:**
    In your WSL terminal, run:
    ```bash
    gazebo --version
    ```
    You should see `Gazebo multi-robot simulator, version 11.x.x`.

2.  **Launch Gazebo:**
    ```bash
    gazebo
    ```
    After a brief moment, a Gazebo window should appear on your Windows desktop, running from within Linux!

---

If you want that ros and gazebo should work side by side, first run 
```bash
    roscore
    ```
and this should run in the background

## **Running the Robotic Arm Simulation**

Once the prerequisites are installed, you can set up and run this project.

You will able to clone this repository i will further share more details ahead
