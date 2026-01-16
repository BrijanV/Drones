# Autonomous Quadrotor Navigation Through Structured and Unknown Openings

This repository contains the **final technical report** for **RBE595: Hands-On Autonomous Aerial Robotics (Project 5 – The Final Race)** at Worcester Polytechnic Institute.

The report documents an end-to-end autonomous quadrotor system capable of traversing multiple structured window obstacles, navigating an unknown gap, and executing an efficient return flight using cached and modified waypoints.

---

## Project Overview

Autonomous micro aerial vehicles operating in cluttered environments must reliably perceive, align to, and traverse constrained openings while maintaining stability and respecting real-time constraints. This project presents a unified perception-to-control pipeline that enables a quadrotor to:

1. Traverse three known window-like obstacles using learned semantic perception and image-based visual servoing.
2. Transition to an unknown gap navigation task using optical flow–based perception.
3. Return efficiently by reusing and modifying previously traversed waypoints.

The system is evaluated entirely in a photorealistic simulation environment and instrumented with detailed timing measurements to assess real-time feasibility.

---

## System Capabilities

The reported system integrates the following capabilities:

- **Semantic perception for structured obstacles**  
  Learned segmentation is used to identify window structures and extract the largest feasible opening, including robustness to partial and edge-touching views.

- **Visual servoing for precise alignment**  
  Image-space error between detected opening centers and the camera center is mapped to bounded pose updates, enabling stable alignment before traversal.

- **Unknown gap navigation**  
  After completing structured traversals, the system switches to an optical-flow-based perception stage to detect and align with previously unseen gaps.

- **State-machine-based mission execution**  
  The overall mission is organized into distinct phases with explicit transitions and timing instrumentation.

- **Waypoint caching and optimized return**  
  Key poses from the forward traversal are stored, modified to reduce alignment distance, and replayed in reverse to achieve a faster and more stable return flight.

---

## Methodology Summary

The report details the following major components:

### Perception
- Semantic segmentation for window detection.
- Contour and hierarchy reasoning to localize valid openings.
- Optical-flow-based gap extraction using edge detection and morphological operations.

### Control and Navigation
- Image-based visual servoing with bounded updates and anomaly rejection.
- Discrete alignment-and-advance strategy shared across window and gap traversal.
- Waypoint-based navigation with trapezoidal motion profiles.

### Timing and Evaluation
- Explicit measurement of simulation time, wall-clock time, and per-frame inference latency.
- Analysis of runtime behavior and perception-control interaction.

---

## Experimental Results

Across multiple simulated runs:

- The quadrotor successfully traverses all three window obstacles.
- The system reliably transitions to unknown gap navigation using optical flow.
- The return flight completes efficiently using cached and shortened waypoints.
- The control loop remains stable despite variable perception latency.

Representative qualitative results, timing summaries, and visualizations are included in the report.

---

## Limitations and Future Work

The report also discusses several limitations, including:

- Manual tuning of control gains and traversal distances.
- Dependence on orientation clipping for stability in certain phases.
- Evaluation limited to simulation with workstation-grade compute.

Future extensions include improved temporal tracking for gap detection, depth-aware scaling, and deployment under real-world sensing and compute constraints.

---

## Report

The complete technical report including mathematical formulations, system architecture, experimental results, limitations, and conclusions is provided as:

---
## Videos

Demo 1: https://drive.google.com/file/d/1o-UjQqUAcy2uGgiE43kmzoO5Sqv0miQm/view?usp=drive_link

Demo 2: https://drive.google.com/file/d/1FbujC9Oetarpirzfub8TpGyehMwuU6hE/view?usp=sharing



