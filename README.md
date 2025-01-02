# Rat Trak: Automatic Gait Tracking System

## Project Overview
**Rat Trak** is an innovative camera tracking system designed to improve gait analysis in rodent-based research. Rodents are widely used in developing treatments for various diseases and injuries, and gait analysis is a crucial tool for assessing the efficacy of these treatments. However, traditional systems for gait analysis are expensive and time-consuming. **Rat Trak** solves this problem by providing a cost-effective, automated system capable of continuously recording a rat's gait and stride with high precision.

This system enhances the yield of research data while reducing overhead costs and operational complexity. It will initially support research in the Spence Lab for spinal cord injury studies, with potential applications in other research areas.

---

## Features
- **High-Speed Camera Tracking**: Captures detailed gait and stride data with precision.
- **Timing Belt Gantry System**: Ensures stable and smooth movement of the high-speed camera.
- **Secondary Tracking Camera**: Keeps the high-speed camera centered on the rat at all times.
- **Automation**: Minimizes manual intervention and maximizes research data output.

---

## Installation
To Set up and run the **Rat Trak** system, follow these steps:

### Prerequisites
Before starting, ensure you have the following installed on your system:
- **Ubuntu 20.04 or 22.04**
- **ROS** (This has only been tested on ROS1 Noetic)
- **Python 3.8+**
- **pip** (Python package manager)
- **OpenCV** for image processing: `pip install opencv-python`

### Hardware Requirements
- **High-Speed Camera**: Ensure it is compatible with the system's software.
- **Timing Belt Gantry System**: Properly install and calibrate the gantry for smooth movement.
- **Secondary Tracking Camera**: Mount and align it to monitor the rat's movement accurately.

### Software Installation
1. SparkCan Setup
``` bash
sudo apt update
sudo apt upgrade
sudo apt install git cmake
sudo add-apt-repository ppa:graysonarendt/sparkcan
sudo apt update
sudo apt install sparkcan

git clone https://github.com/grayson-arendt/sparkcan-examples.git
cd sparkcan-examples/

chmod +x canable_start.sh
./canable_start.sh

mkdir build
cd build
cmake ..
make
```

2. Rat-Trak Installation
```bash
cd ~
mkdir rat_trak
cd rat_trak
git clone https://github.com/your-repo/rat-trak.git
cd ~/rat_trak/rat_trak_ws
catkin_make
source devel/setup.sh
roslaunch rat_trak rat.launch
```

## System Architecture
1. **High-Speed Camera**: Mounted to a timing belt gantry for capturing detailed stride analysis.
2. **Timing Belt Gantry**: Provides precise camera motion control.
3. **Secondary Tracking Camera**: Monitors the rat's position to ensure the high-speed camera stays aligned.
4. **Software**: Custom-designed codebase to control the cameras and synchronize their operation with the gantry system.

---

## Applications
- **Spinal Cord Injury Research**: Used by the Spence Lab to gather data for assessing treatments.
- **General Biomedical Research**: Can be adapted for use in other labs studying rodent behavior or biomechanics.

---

## Acknowledgments
- **Team Advisor**: Dr. Andrew Spence
- **Senior Design Instructor**: Dr. Hamid Heravi
- **Team Members**: Chris Pullen, Ryan Loc, Darshan Patel, Fernanda Gutierrez
- **Special Contributors**: Jared Levin, Grayson Arendt, Anway Bose

---

## Conclusion
**Rat Trak** represents a significant advancement in gait analysis technology, providing a robust, efficient, and automated solution to a critical research need. By increasing the volume and precision of gait data, this system contributes to the development of better treatments for diseases and injuries, starting with spinal cord injury research.

