# is-robotic-arm

An open-source 5-DOF (Degree of Freedom) 3D-printed robotic arm project. This repository contains the complete electromechanical engineering stack, transitioning from custom Python/Arduino control to a standardized industrial ROS 2 (Jazzy) and Gazebo digital twin architecture.

## Repository Structure

- [`docs/`](docs/) — Project documentation, research notes, and academic/technical reports.
- [`electrical/`](electrical/) — Wiring architecture for the RAMPS 1.4 shield.
- [`mechanical/`](mechanical/) — 3D Computer-Aided Design (CAD) models designed in Fusion 360, alongside exported URDF packages for robotic simulation.
- [`software/`](software/) — Core control logic and firmware, divided into:
  - **Kinematics & Teleoperation:** Python-based (PyQt5) interactive analytical Inverse Kinematics (IK) and Forward Kinematics (FK) solvers.
  - **Firmware:** Real-time, non-blocking C++ firmware for the Arduino Mega featuring Bresenham's multi-axis synchronization and David Austin's trapezoidal velocity profiles.

## Project Highlights

* **Industrial-Grade Firmware:** The Arduino Mega operates as a real-time hardware controller, ensuring synchronous multi-axis movement without stalling by utilizing hardware timer interrupts (Timer1).
* **Analytical Kinematics:** Fully derived Denavit-Hartenberg (DH) parameters and analytical IK solvers with posture control (Elbow-Up/Down).
* **Digital Twin Roadmap:** Currently porting the mechanical model into the ROS 2 ecosystem (`ros2_control`, MoveIt 2, and Gazebo) for collision-free trajectory planning and simulation.

## License

See the [LICENSE](LICENSE) file for details.
