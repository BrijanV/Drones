# End-to-End Development of a Custom FPV Drone Flight Controller with Fully Custom Firmware Implementation

## STM32-Based Diagnostic Platform for Multi-Sensor UAV Integration 
- Designed a modular testbench using the STM32H7 Nucleo board to streamline drone subsystem validation.

- Built to test and debug components like IMUs, GPS, barometric pressure sensors, ESCs, motors, FPV cameras, and RC receivers.

- Enabled direct plug-and-play testing without needing full drone integration.

- Developed custom firmware for real-time sensor data acquisition and diagnostics.

- Developed custom firmware for real-time sensor data acquisition and diagnostics.

- Helps ensure components are functionally verified before drone assembly, reducing costly - trial-and-error cycles.

- Implemented evaluation matrix generation to compare sensor accuracy, drift, and noise performance.

- Improves system reliability by identifying defective components in advance.

- Saves development time by offering rapid swap-in/swap-out testing of modules.

- Included UART, I2C, and SPI lines for diverse sensor connectivity and easy logging.

- Camera integration allowed visual feedback and latency tests with embedded video streams.

- Provided isolated power testing for ESCs and motors to ensure safe, repeatable experiments.

- Empowers scalable testing—multiple sensors can be evaluated in a single pass.

- Overall, it forms a critical foundation for building robust, field-ready drone systems.


## Dedicated IMU Evaluation Rig for Comparative Sensor Benchmarking

- Developed a gyroscope testbench which supported evaluation of multiple IMUs (e.g., MPU9250, ICM20948) under varied dynamic conditions.

- PCB was custom-designed to support flexible sensor interfacing and stable power delivery.

- Enables thorough sensor benchmarking to choose the most reliable and accurate IMUs for flight.

- Supports early-stage debugging of sensor fusion logic, Kalman filters, and control loops.

- Allows environmental and motion testing to simulate real-world flight disturbances.

- PCB modularity allows the testbench to be used in different lab or field setups.

- Adds value to R&D pipelines, especially in iterative prototyping environments.



## Application-Tuned FPV Flight Controller with Custom Hardware and Bare-Metal Firmware

- Built a custom embedded firmware for STM32 microcontroller to achieve complete control over drone behavior and real-time data handling.

- Developed an intuitive C# GUI for seamless user interaction, enabling advanced drone configuration and live feedback without manual reprogramming.

- Included real-time PID tuning directly from the GUI to optimize flight performance during testing or deployment.

- Integrated sensor calibration tools (e.g., IMU, barometer, magnetometer) into the interface to ensure accurate and reliable sensor readings.

- Enabled GPS tracking and location display, critical for autonomous flight paths and navigation debugging.

- Streamed video frames from an onboard camera to the GUI, providing FPV (First Person View) and vision debugging during development.

- Logged and visualized flight data and system performance metrics, helping in post-flight analysis and diagnostics.

- The system significantly improves development speed, flight safety, and adaptability essential for R&D, testing, and real-world drone deployments.