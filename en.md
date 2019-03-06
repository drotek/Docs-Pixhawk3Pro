# Introduction

**FMUv4-PRO** takes input from all of the Pixhawk stakeholders; end users, developers, researchers and manufacturing partners. Goals for this iteration of the platform are:

* An integrated, single-board flight controller for space constrained applications
* A modular multi-board flight controller for professional applications
* Sufficient I/O for most applications without expansion.
* Improved ease-of-use.
* Improved sensor performance
* Improved microcontroller resources \(384 KB RAM, 2 MB flash\).
* Increased reliability and reduced integration complexity.
* Reduced BoM and manufacturing costs.

**Key design points:**

* All-in-one design with integrated FMU and optional IO and lots of I/O ports.
* Improved manufacturability, designed for simpler mounting and case design.
* Separate power supplies for FMU and IO \(see power architecture section\).
* Onboard battery backup for FMU and IO SRAM / RTC.
* Integration with two standard power bricks.

**Technology upgrades:**

* Microcontroller upgrade to **STM32F469**; flash increases from 1MiB to 2MiB, RAM increases from 256KiB to 384KiB, more peripheral ports.
* **ICM-20602**, **MPU9K** integrated gyro / accelerometer / magnetometers.
* **LIS3MDL** compass \(HMC5983 is now obsolete\).
* Sensors connected via two SPI buses \(one high rate and one low-noise bus\)
* Two I2C buses
* Two CAN buses
* Voltage / battery readings from two power modules
* FrSky Inverter
* JST GH user-friendly connectors

[Get more information about this product and shop here.](https://store.drotek.com/pixhawk-pro-autopilot)

