# Kamikaze V2: Compact Military Drone with Payload Delivery, Surveillance & Head Tracking Control

## Real-Time Head Tracking System for Gimbal and Camera Control in FPV Drones

- Used Seeed Studio ESP32 to minimize form factor and enable wireless communication, making the system lightweight and wearable.

- Integrated IMUs on VR goggles to capture real-time head motion, translating pilot head movements into precise camera orientation commands.

- Implemented soft limits in software to restrict excessive gimbal angles and prevent mechanical stress or sensor overrun.

- Solves the problem of manual or joystick-based camera control, which lacks intuitiveness and causes pilot distraction.

- Enhances FPV drone immersion by enabling natural, head-driven camera control, improving situational awareness and response time.

- Reduces hardware complexity and increases system reliability by combining motion sensing, control, and communication in a compact, modular unit.


## Smart Battery Monitoring System

- Developed a compact smart battery monitor using the ultra-small ESP-01F Wi-Fi module for minimal form factor integration.

- Added 4 status RGB programmable low power LEDs to indicate battery charge level visually (e.g., 1 LED = low, 4 LEDs = full) for quick, intuitive checks.

- On battery usage or charging, the system activates and displays charge level for 5 seconds using LEDs.

- Simultaneously, the ESP-01F connects to a PC/laptop over Wi-Fi and serves a webpage showing voltage, charge status, and battery logs.

- After 5 minutes of activity, the ESP-01F enters hibernation mode to conserve power, extending system life.

- Performed long-term discharge tests, with the system operating for 14 days after a full charge under 6-hour testing intervals.

- Solves the issue of blind battery use by offering real-time, web-accessible voltage and charge data without extra ground station tools.

- Eliminates the need for opening enclosures or connecting multimeters, wireless on-demand access to battery health is effortless.

- Enhances drone operational safety by providing pre-flight battery diagnostics, reducing in-flight power failure risks.

- Helps in tracking battery performance degradation through logs, enabling proactive battery replacement.

- Reduces unnecessary power draw by implementing hibernation, ensuring the monitor doesn’t drain the battery it monitors.

- Ideal for drone makers and testers needing a low-cost, reliable, and low-power solution for tracking battery condition across test cycles.


