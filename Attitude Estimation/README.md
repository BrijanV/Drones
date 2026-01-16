# Attitude Estimation with IMU Using Complementary, Madgwick, and Unscented Kalman Filters

This repository contains a technical report multiple attitude estimation techniques for a 6-DoF Inertial Measurement Unit (IMU), ranging from simple heuristic filters to a probabilistically rigorous Unscented Kalman Filter (UKF). The project was developed as part of **RBE595: Hands-On Autonomous Aerial Robotics (Project 1b)** at Worcester Polytechnic Institute.

The objective is to accurately estimate roll, pitch, and yaw by fusing gyroscope and accelerometer data, and to benchmark performance against high-precision ground-truth orientation from a Vicon motion-capture system.

---

## Overview

Low-cost IMUs are widely used in aerial robotics but suffer from inherent limitations:

- **Gyroscopes** provide smooth short-term orientation estimates but accumulate drift over time.
- **Accelerometers** estimate roll and pitch from gravity but are noisy during dynamic motion and cannot directly observe yaw.

This project explores multiple sensor-fusion strategies to address these limitations and compares their performance under real motion data.

---

## Implemented Methods

### 1. Gyroscope Integration
- Integrates angular velocity over time.
- Initialized using averaged Vicon ground-truth measurements during a stationary period.
- Accurate in the short term but suffers from unbounded drift.

### 2. Accelerometer Inclination
- Estimates roll and pitch using the gravity vector.
- Sensitive to translational accelerations and high-frequency noise.
- Yaw estimation is approximate and unreliable.

### 3. Complementary Filter
- Combines:
  - High-pass filtered gyroscope data
  - Low-pass filtered accelerometer estimates
- Lightweight, easy to tune, and effective for moderate dynamics.

### 4. Madgwick Filter
- Quaternion-based orientation estimation using gradient descent.
- Corrects gyroscope drift by minimizing the error between expected and measured gravity.
- Computationally efficient and robust during aggressive motion.

### 5. Unscented Kalman Filter (UKF)
- Full probabilistic state estimation without Jacobian linearization.
- Propagates sigma points through nonlinear quaternion dynamics.
- Explicitly models process and measurement uncertainty.
- Provides the most accurate and stable orientation estimates across datasets.

---

## Dataset and Synchronization

- **IMU Data**: 6-DoF accelerometer and gyroscope measurements  
- **Ground Truth**: Vicon motion-capture rotation matrices  
- **Synchronization**:
  - Data streams aligned within a common time window
  - Vicon orientations interpolated to IMU timestamps using **SLERP**
- Multiple training and test sequences are evaluated.

---

## Results Summary

- Accelerometer-only estimates are noisy during motion.
- Gyroscope integration drifts significantly over time.
- Complementary filtering improves stability but remains heuristic.
- Madgwick filtering performs well under dynamic conditions.
- **The Unscented Kalman Filter consistently provides the most accurate and robust orientation estimates**, closely tracking Vicon ground truth across roll, pitch, and yaw.

Plots comparing all methods for each dataset, along with orientation visualization videos, are included in the report.
