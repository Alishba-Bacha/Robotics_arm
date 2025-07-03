# Robotics_arm

Things you need to have Installed!
1: Gazebo 
2: ROS Noetic

Way to Install on Ubuntu
Step1: Update your packages list through: sudo apt update
Step2: Add gazebo package Repository: sudo curl -sSL http://get.gazebosim.org/pkgs/gazebo.key -o /usr/share/keyrings/pkgs-gazebo.key
   add repository source list to your gazebo: echo "deb [arch=$(dpkg --print-architecture) signed-by=/usr/share/keyrings/pkgs-gazebo.key] http://packages.osrfoundation.org/gazebo/ubuntu-stable $(lsb_release -cs) main" | sudo tee /etc/apt/sources.list.d/gazebo-stable.list > /dev/null

   update your package list information: sudo apt update
   
Step3: install gazebo: sudo apt install gz-garden or sudo apt install gazebo11 libgazebo11-dev
step4: Verify installation: gz sim --version 
Step5: Run demo world: gz sim shapes.sdf

Installation on windows(wsl)

1: Install wsl: wsl --install
2: Ensure you are using wsl2: wsl --set-default-version 2
3: Install Graphics Drivers for WSL: For Gazebo to perform well, it needs to access your GPU. You must install the specific WSL drivers for your graphics card.
NVIDIA: [Download NVIDIA CUDA on WSL Drivers](https://developer.nvidia.com/cuda/wsl)
Intel: [Download Intel Drivers for WSL](https://www.intel.com/content/www/us/en/support/articles/000058387/graphics.html)
AMD: [Download AMD Drivers for WSL](https://www.amd.com/en/support/download/drivers.html)
4: Update packages: sudo apt update
5: Add package repository: sudo curl -sSL http://get.gazebosim.org/pkgs/gazebo.key -o /usr/share/keyrings/pkgs-gazebo.key
6: Add Source: echo "deb [arch=$(dpkg --print-architecture) signed-by=/usr/share/keyrings/pkgs-gazebo.key] http://packages.osrfoundation.org/gazebo/ubuntu-stable $(lsb_release -cs) main" | sudo tee /etc/apt/sources.list.d/gazebo-stable.list > /dev/null

7: update package: sudo apt update
8: Install gazebo: sudo apt install gz-garden
9: Run a demo world: gz sim shapes.sdf
