# MavSDK

Astro runs Auterion Enterprise PX4 and is MavSDK compatible. This means a serial connection can be used to get messages like GPS position and velocity from the autopilot, send commands like desired position or speed. More info at [DroneCode.org](https://www.dronecode.org/), including [example code](https://github.com/mavlink/MAVSDK-Python/tree/e16c5d86fe8c70046e20ea833ba529324cece594/examples).

You can include MavSDK in your mobile or onboard apps. You can make remote controllers that communicate via MavLINK. You can make sensors that pump their data back and forth to Astro with MavLINK. You can make an app that runs on PC, and the PC connects to the herelink hotspot, allowing full access to the drone telemetry on the laptop.
