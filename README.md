#  Modular Self-Healing Robot

A modular robot simulation in ROS 2 and Gazebo, designed to explore self-healing capabilities through redundant sensing modules and autonomous fault recovery mechanisms.

---

##  Project Objectives

- Design a modular robot architecture with redundant sensing capabilities  
- Implement health monitoring systems for each module using ROS diagnostics  
- Develop algorithms for failure detection and recovery procedures  
- Create simulation environments in Gazebo to test failure scenarios  
- Demonstrate seamless transition between modules upon component failure  

---

##  Robot Model

The self-healing robot consists of a central mobile chassis with two identical, independent modules mounted on either side. Each module has full sensing and processing capabilities, allowing one to take over if the other fails.

###  Physical Components

- **Base Chassis**: Blue cylindrical body with four wheels  
- **Wheels**: Differential drive configuration (black)  
- **Redundant Modules**: Two green modules mounted front-left and front-right  
- **Sensors**: Each module houses a virtual camera (gray box)  
- **Camera Link**: Mounted on the front, aligned for environmental capture  
- **Modularity**: Modules are connected using prismatic joints for simulation flexibility  

---

##  System Architecture

The robot uses a **distributed architecture**, where each module is capable of:

- Independent perception via its own camera  
- Processing sensor data for decision-making  
- Communicating with the base for control commands  
- Monitoring its own system and that of its counterpart  
- Assuming control responsibilities if the other fails  

---

##  Failure Detection & Handover Logic

The recovery mechanism is built around a **state machine** that transitions based on diagnostics:

1. **Normal Operation**: Primary module in control  
2. **Warning State**: Anomalies detected in the primary module  
3. **Handover Preparation**: Secondary module initializes control pipeline  
4. **Handover Execution**: Smooth control transfer with state sync  
5. **Recovery Attempt**: Faulty module attempts self-repair and reinitialization  

During the handover, the robot ensures:

- Sensor data and map synchronization  
- Navigation goal alignment  
- Control readiness validation  

---

##  Simulation Details

- **URDF/Xacro**: Fully modular robot description  
- **Gazebo**: Integrated with differential drive and camera plugin  
- **RViz**: Visualized with robot model, TF, and sensor data  
- **Launch Files**: For both Gazebo simulation and RViz visualization  

---

##  Appendix

<img width="1348" height="668" alt="image" src="https://github.com/user-attachments/assets/55499a17-5c7c-4a5b-af74-c3f40c205635" />
<img width="1370" height="774" alt="image" src="https://github.com/user-attachments/assets/4e00372d-c767-4aae-8868-c8330f788492" />
<img width="1529" height="819" alt="image" src="https://github.com/user-attachments/assets/9c9740c2-0fd7-4caa-86ab-d751f2dd3d36" />


---

##  Status

This project is **ongoing** and actively being expanded. The current focus is on solidifying the architecture, simulation setup, and module communication.

---

##  Maintainer

**Keerthana**  
✉️ keerthanaprasad2005@gmail.com


---
