# Introduction

**FMUv4-PRO** takes input from all of the Pixhawk stakeholders; end users, developers, researchers and manufacturing partners. Goals for this iteration of the platform are:

* An integrated, single-board flight controller for space constrained applications
* A modular multi-board flight controller for professional applications
* Sufficient I/O for most applications without expansion.
* Improved ease-of-use.
* Improved sensor performance
* Improved microcontroller resources \(384 KB RAM, 2 MB flash\).
* Increased reliability and reduced integration complexity.
* Reduced BoM and manufacturing costs.3
<br\>

**Key design points**

* All-in-one design with integrated FMU and optional IO and lots of I/O ports.
* Improved manufacturability, designed for simpler mounting and case design.
* Separate power supplies for FMU and IO \(see power architecture section\).
* Onboard battery backup for FMU and IO SRAM / RTC.
* Integration with two standard power bricks.
<br\>

**Technology upgrades**

* Microcontroller upgrade to **STM32F469**; flash increases from 1MiB to 2MiB, RAM increases from 256KiB to 384KiB, more peripheral ports.
* **ICM-20602**, **MPU9K** integrated gyro / accelerometer / magnetometers.
* **LIS3MDL** compass \(HMC5983 is now obsolete\).
* Sensors connected via two SPI buses \(one high rate and one low-noise bus\)
* Two I2C buses
* Two CAN buses
* Voltage / battery readings from two power modules
* FrSky Inverter
* JST GH user-friendly connectors
<br\>

**I/O ports**

* 6-14 PWM servo outputs \(8 from IO, 6 from FMU\).
* R/C inputs for CPPM, Spektrum / DSM and S.Bus.
* Analog / PWM RSSI input.
* S.Bus servo output.
* 6 general purpose serial ports, 2 with full flow control, 1 with separate 1A current limit, 1 with FrSky protocol inverter.
* Two I2C ports.
* Two external SPI ports \(unbuffered, for short cables only\).
* Two CAN Bus interfaces.
* Analog inputs for voltage / current of two batteries
* On-ground usage piezo buzzer driver.
* Sensor upgrade connector scheme
* High-power RGB LED.
* Safety switch / LED.
<br\>

**Mechanical Form Factor**

* 71 x 49 x 23 mm \(with case\)
* 45g \(with case\)
* Standardized microUSB connector location
* Standardized RGB led location
* Standardized connector locations
<br\>

**System architecture**

FMUv4-PRO continues the PX4FMU+PX4IO architecture from the previous generation, incorporating the two functional blocks in a single physical module.
<br\>

**PWM Outputs**

Eight PWM outputs are connected to IO and can be controlled by IO directly via R/C input and onboard mixing even if FMU is not active \(failsafe / manual mode\). Multiple update rates can be supported on these outputs in three groups; one group of four and two groups of two. PWM signal rates up to 400Hz can be supported.

Six PWM outputs are connected to FMU and feature reduced update latency. These outputs cannot be controlled by IO in failsafe conditions. Multiple update rates can be supported on these outputs in two groups; one group of four and one group of two. PWM signal rates up to 400Hz can be supported.

All PWM outputs are ESD-protected, and they are designed to survive accidental mis-connection of servos without being damaged. The servo drivers are specified to drive a 50pF servo input load over 2m of 26AWG servo cable. PWM outputs can also be configured as individual GPIOs. Note that these are not high-power outputs – the PWM drivers are designed for driving servos and similar logic inputs only, not relays or LEDs.
<br\>

**Peripheral Ports**

FMUv4-PRO recommends separate connectors for each of the peripheral ports \(with a few exceptions\). This avoids the issues many users reported connecting to the 15-pin multi-IO port on the original PX4FMU-PRO and allows single-purpose peripheral cables to be manufactured.

Five serial ports are provided. TELEM 1, 2 and 3 feature full flow control. TELEM4 can be switched into inverted mode by hardware and has no flow control. Serial ports are 3.3V CMOS logic level, 5V tolerant, buffered and ESDprotected.

The SPI ports are not buffered; they should only be used with short cable runs. Signals are 3.3V CMOS logic level, but 5V tolerant.

Two power modules \(voltage and current for each module\) can be sampled by the main processor.

The RSSI input supports either PWM or analog RSSI. CPPM, S.Bus and DSM/ Spektrum share now a single port and are auto-detected in software.

The CAN ports are standard CAN Bus; termination for one end of the bus is fixed onboard. 
<br\>

 

**Sensors**

The new **ICM-20602** has been positioned by Invensense as higher-end successor of the MPU-6000 series. The software also supports the MPU-9250, which allows a very cost-effective 9D solution.

Data-ready signals from all sensors \(except the MS5611, which does not have one\) are routed to separate interrupt and timer capture pins on FMU. This will permit precise time-stamping of sensor data.

The two external SPI buses and six associated chip select lines allow to add additional sensors and SPI-interfaced payload as needed.

**IMU is isolated from vibrations**.

