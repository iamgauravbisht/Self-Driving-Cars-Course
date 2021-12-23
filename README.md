# Machine Learning Through Self-Driving Cars Expercises
This repository stores code for the course: Machine Learning Through Self-Driving Cars

# Sections
- Python: code used for lectures (it's recommended to start from scratch)
- Computer Vision: using the simulator Webots, we will make a car follow the road line
- Machine Learning (Road Sign Classification): we will use Machine Learning to classify road signs (i.e. the model will be able to tell if the image contains a stop sign, speed limit sign, ...)
- Collision Avoidance: Using a Lidar we will make make our car drive without crashing
- Deep Learning (Behavioural Clonning): Using the power of Deep Neural Netowrks we will make the car drive like ourselves!

# Pre-requisites
- Install Python
- Install Visual Studio Code
- Install Webots
- Install Python libraries (can be found in 0_install/requirements.txt)
- Add Envrionment Variables (PYTHONPATH, PYTHONDECODING, ...)

## Install Webots
### Linux
Install on Debian-based systems (i.e. Ubuntu), open a terminal and paste the following commands (shortcut: Ctrl+Alt+T), then paste:
```
wget -qO- https://cyberbotics.com/Cyberbotics.asc | sudo apt-key add - # Add the key with the command
sudo apt-add-repository 'deb https://cyberbotics.com/debian/ binary-amd64/' # Add the repository
sudo apt-get update
sudo apt-get install webots # install Webots
```

Alternative you can install it through the snap store:
```
sudo apt-get install snapd
sudo snap install webots
```

### Windows
- Download the "webots-R2022a_setup.exe" installation file from their [website](https://cyberbotics.com/)
- Double click on this file
- Follow the installation instructions

## Install the rest (Python, Visual Studio Code, Python Libraries, Environment Variables)

### Automated Installation Linux
You can install everything necessary in *Linux* by executing the following on a terminal.
```
cd /path/to/Self-Driving-Cars-Course/0_install
./install_linux.sh
```

### Manual Installation Windows
Install:
- [Python](https://www.python.org/downloads/)
- [Visual Studio Code](https://code.visualstudio.com/download)

Install the required Python libraries, by running.
```
cd Self-Driving-Cars-Course/0_installation
pip3 install -r requirements.txt
```

Set the required environment variables
- Click the "Windows Key" and write "Edit the system environment variables"
- Create variable “WEBOTS_HOME” with content “C:\Program Files\Webots”
- Create variable “PYTHONPATH” with content “%WEBOTS_HOME%/lib/controller/python3X”
  - WARNING: in the documentation says to use ${WEBOTS_HOME}, but doesn’t work
- Change the last “X” for the minor revision number of your Python version
- Add to “Path”
  -  “%WEBOTS_HOME%\lib\controller”
  - “%WEBOTS_HOME%\msys64\mingw64\bin”
  - “%WEBOTS_HOME%\msys64\mingw64\bin\cpp”

Create variable “PYTHONIOENCODING” with content “UTF-8”

### Manual Installation Linux
[Manual] Setup with Visual Studio Code:
Prerequisites: we need to have installed Python and Visual Studio Code, you can find how to install those in the first video of the Python section
Install the following Python libraries: numpy, opencv-python


To set up the environment variables, open a terminal and run the following commands:
```
echo "export LD_LIBRARY_PATH=/usr/local/webots/lib/controller" >> ~/.bashrc 
echo "export PYTHONPATH=/usr/local/webots/lib/controller/python3X >> ~/.bashrc # WARNING: change the "X" for your python version, you can find it by running "python3 --version" in the terminal
echo "export PYTHONIOENCODING=UTF-8" >> ~/.bashrc
```
