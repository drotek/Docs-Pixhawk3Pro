# Power architecture

Key features of the FMUv4-PRO power architecture:

* - Single, independent 5V supply for the flight controller and peripherals.
* - Integration with two standard power bricks, including current and voltage 
  sensing.

* - Low power consumption and heat dissipation.
* - Power distribution and monitoring for peripheral devices.
* - Protection against common wiring faults; under/over-voltage protection, overcurrent 
  protection, thermal protection.

* - Brown-out resilience and detection.
* - Backup power for IO in the case of FMU power supply failure.
* - Split digital and analog power domains for FMU and sensors.
 <br/> 
 <br/> 

**FMU and IO Power Supplies:**

Both FMU and IO operate at 3.3V, and each has its own private dual-channel regulator. In order to address issues seen with PX4v1 and noisy power supply connections, each regulator features a power-on reset output tied to the regulator’s internal power-up and drop-out sequencing.

The second channel of each dual regulator is switchable under software control. For FMU this is used to permit power-cycling the sensors \(in case of sensor lockup\), and for IO this will make it possible to perform the Spektrum binding sequence.
 <br/> 
 <br/> 

**Power Sources:**

Power may be supplied to FMUv4-PRO via USB \(no peripherals in this mode\) or via the power brick ports. Each power source is protected against reverse-polarity connections and back-powering from other sources. Power spikes observed on the servo bus \(up to 10V\) led to the removal of the power-from-servo option, users wanting this feature can connect the servo rail with a cable containing a Zener diode to the 2nd power brick port.

The FMU + IO power budget is 250mA, including all LEDs and the Piezo buzzer. Peripheral power is limited to 2A total.
 <br/>
 <br/> 

**Power Brick Port:**

The brick port is the preferred power source for FMUv4-PRO, and brick power will be always be selected if it is available.
 <br/>
 <br/>  

**Servo Power:**

FMUv4-PRO supports both standard \(5V\) and high-voltage \(up to 10V\) servo power with some restrictions. IO will accept power from the servo connector up to 10V. This allows IO to fail-over to servo power in all cases if the main power supply is lost or interrupted. FMUv4-PRO and peripherals combined may draw up to 2A total.

Power is never supplied by FMUv4 to servos.
 <br/>
 <br/>

**USB Power:**

Power from USB is supported for software update, testing and development purposes. USB power is supplied to the peripheral ports for testing purposes, however total current consumption must typically be limited to 500mA, including peripherals, to avoid overloading the host USB port.
 <br/>
 <br/> 

**Multiple Power Sources:**

When more than one power source is connected, power will be drawn from the highest-priority source with a valid input voltage.

In most cases, FMU should be powered via the power brick or a compatible offboard regulator via the brick port or servo power rail.

In desktop testing scenarios, taking power from USB avoids the need for a BEC or similar servo power source \(though servos themselves will still need external power\).
 <br/>
 <br/> 

**Summary:**

For each of the components listed, the input voltage ranges over which the device can be powered from each input is shown.

|  | **Brick ports** | **Servo rail** | **USB port** |
| :--- | :--- | :--- | :--- |
| **    FMU** | 4 - 5.7V | no | yes |
| **    IO** | 4 - 5.7V | 4 - 10V | yes |
| **    Peripherals** | 4 -5.7V, 2A max | 4 - 5.7V, 250mA max | yes, 500 mA max |
 <br/>
 <br/> 

**Peripheral Power:**

FMUv4-PRO provides power routing, over/under voltage detection and protection, filtering, switching, current-limiting and transient suppression for peripherals.

Power outputs to peripherals feature ESD and EMI filtering, and the power supply protection scheme ensures that no more than 5.5V is presented to peripheral devices. Power is disconnected from the peripherals when the available supply voltage falls below 4V, or rises above approximately 5.7V.

Peripheral power is split into two groups:

* - TELEM 1 has a private 1A current limit, intended for powering a telemetry radio. This output is separately EMI filtered and draws directly from the USB / Brick inputs. Due to the noise induced by radios powering a radio from this port is not advised.
* - All other peripherals share a 1A current limit and a single power switch. 

Each group is individually switched under software control.

The Spektrum / DSM R/C interface draws power from the same sources as IO, rather than from either of the groups above. This port is switched under software control so that Spektrum / DSM binding can be implemented. Spektrum receivers generally draw ~25mA, and this is factored into the IO power budget. S.Bus and CPPM receivers are supported on this rail as well.
 <br/>
 <br/>  

**Battery Backup:**

Both the FMU and IO microcontrollers feature battery-backed realtime clocks and SRAM. The onboard backup battery has capacity sufficient for the intended use of the clock and SRAM, which is to provide storage to permit orderly recovery from unintended power loss or other causes of in-air restarts. The battery is recharged from the FMU 3.3V rail. 
 <br/>
 <br/> 

**Voltage, Current and Fault Sensing:**

The battery voltage and current reported by the power brick can be measured by FMU. In addition, the 5V unregulated supply rail can be measured \(to detect brown-out conditions\). IO can measure the servo power rail voltage.

Over-current conditions on the peripheral power ports can be detected by the FMU. Hardware lock-out prevents damage due to persistent short-circuits on these ports. The lock-out can be reset by FMU software.

The under/over voltage supervisor for FMU provides an output that is used to hold FMU in reset during brown-out events.
 <br/>
 <br/> 

**EMI Filtering and Transient Protection:**

EMI filtering is provided at key points in the system using high-insertion-loss passthrough filters. These filters are paired with TVS diodes at the peripheral connectors to suppress power transients.

Reverse polarity protection is provided at each of the power inputs.

USB signals are filtered and terminated with a combined termination/TVS array.

Most digital peripheral signals \(all PWM outputs, serial ports, I2C port\) are driven using feature series blocking resistors to reduce the risk of damage due to transients or accidental mis-connections.

  


