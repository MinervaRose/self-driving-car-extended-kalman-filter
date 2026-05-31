<div align="center">

# 📡 Self-Driving Car — Extended Kalman Filter Sensor Fusion

### State Estimation from Radar and Lidar Measurements

![C++](https://img.shields.io/badge/C++-Autonomous_Systems-blue?style=for-the-badge&logo=cplusplus)
![Sensor Fusion](https://img.shields.io/badge/Sensor_Fusion-Radar_%2B_Lidar-green?style=for-the-badge)
![Kalman Filter](https://img.shields.io/badge/Kalman_Filter-State_Estimation-orange?style=for-the-badge)
![Robotics](https://img.shields.io/badge/Robotics-Probabilistic_Localization-red?style=for-the-badge)
![Self Driving Cars](https://img.shields.io/badge/Domain-Autonomous_Vehicles-purple?style=for-the-badge)

Udacity Self-Driving Car Engineer Nanodegree Project

</div>

---

# Overview

Autonomous systems must continuously estimate the state of surrounding objects despite noisy and incomplete sensor measurements.

This project implements an **Extended Kalman Filter (EKF)** to track a moving vehicle using measurements from two complementary sensors:

- 📡 Radar
- 🔦 Lidar

By combining observations from both sensors, the system produces a more accurate estimate of position and velocity than either sensor could achieve independently.

The project demonstrates one of the foundational techniques used in autonomous vehicles, robotics, aerospace systems, and navigation systems.

---

# Project Objectives

The goals of this project were to:

- Fuse radar and lidar measurements
- Estimate object position and velocity
- Handle noisy real-world sensor data
- Implement prediction and update cycles
- Evaluate estimation accuracy using RMSE metrics

---

# Sensor Fusion Pipeline

```text
Radar Measurements
         \
          \
           --> Extended Kalman Filter --> State Estimate
          /
         /
Lidar Measurements
```

The filter continuously combines incoming sensor measurements to estimate:

- Position X
- Position Y
- Velocity X
- Velocity Y

---

# Why an Extended Kalman Filter?

Lidar measurements are linear and can be processed using a standard Kalman Filter.

Radar measurements are nonlinear because they are provided in polar coordinates:

- Range (ρ)
- Bearing (φ)
- Range Rate (ρ̇)

The Extended Kalman Filter linearizes these nonlinear measurements using a Jacobian matrix, allowing both sensor types to be fused into a single estimation framework.

---

# Technical Skills Demonstrated

## Sensor Fusion

- Multi-sensor integration
- Radar processing
- Lidar processing

## State Estimation

- Kalman Filters
- Extended Kalman Filters
- Prediction and correction cycles

## Mathematics

- Linear algebra
- Jacobian matrices
- Coordinate transformations
- Covariance matrices

## Software Engineering

- Modern C++
- Modular architecture
- Numerical computing
- Performance evaluation

---

# Project Architecture

```text
Measurement
      ↓
Initialization
      ↓
Prediction Step
      ↓
Sensor Update
      ↓
State Estimate
      ↓
RMSE Evaluation
```

Core components include:

- FusionEKF
- KalmanFilter
- Tools
- MeasurementPackage

---

# Repository Structure

```text
src/
├── FusionEKF.cpp
├── FusionEKF.h
├── kalman_filter.cpp
├── kalman_filter.h
├── tools.cpp
├── tools.h

data/
build/

README.md
```

---

# Results

The implemented filter successfully tracks a moving vehicle using noisy radar and lidar measurements.

Performance is evaluated using Root Mean Square Error (RMSE) between predicted states and ground truth values.

The resulting estimates demonstrate the effectiveness of probabilistic sensor fusion for autonomous navigation.

---

# Key Concepts Explored

- Sensor Fusion
- Radar Tracking
- Lidar Tracking
- Bayesian Estimation
- Kalman Filters
- Extended Kalman Filters
- State Space Models
- Autonomous Navigation
- Robotics Localization

---

# Why This Project Matters

Sensor fusion is one of the core technologies behind:

- Autonomous vehicles
- Mobile robots
- Aerospace guidance systems
- Drone navigation
- Satellite tracking systems

The Extended Kalman Filter remains one of the most widely used estimation algorithms in engineering because of its balance between mathematical rigor, computational efficiency, and real-time performance.

---

# Related Self-Driving Car Projects

This repository is part of a larger autonomous driving portfolio:

- Finding Lane Lines
- Advanced Lane Finding
- Traffic Sign Classifier
- Behavioral Cloning
- Extended Kalman Filter Sensor Fusion
- Kidnapped Vehicle Localization
- Highway Driving
- PID Controller

---

# Disclaimer

This repository is provided for educational and portfolio purposes.

Students may study the code and reports for learning purposes, but submitting this work as coursework would constitute plagiarism and may violate academic integrity policies.

Copyright © Sabrina Palis
