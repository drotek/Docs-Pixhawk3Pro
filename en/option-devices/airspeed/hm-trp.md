# HM-TRP

![](https://drotek.com/wp-content/uploads/2017/01/radio-telemetry-kit-433-915-mhz.jpg "telemetry hm-trp pixhawk by drotek")

The Drotek telemetry system is designed as an **open source Xbee** replacement radio set, offering a lower price, longer range \(approx **one mile**\) and superior performance to Xbee radios.

It’s available in 433Mhz or 915Mhz. The system provides a ** full-duplex** link using HopeRF's HM-TRP modules running custom, open source firmware.

Firmware upgrades and configuration are fully supported in the APM Mission Planner. Configuration is also possible through the 3DR Radio configurator and AT commands.

You can find more information on this [page](https://drotek.com/shop/en/drotek-parts/795-radio-telemetry-kit-433-915-mhz.html).

### HARDWARE

Please connect one of the 2 telemetries to the "**Telem 1**" serial port of the Pixhawk.

![](https://drotek.com/wp-content/uploads/2017/01/DSC02048.jpg "HM-TRP telemetry pixhawk drotek")

Then you can connect the other telemetry to your PC via a **micro USB** cable or to a tablet via an **OTG USB** cable.

![](https://drotek.com/wp-content/uploads/2017/01/Planner-APM-Android-700x382.jpg "telemetrie tablette hm-trp")

![](https://drotek.com/wp-content/uploads/2017/01/groundstation-with-MP-700x383.png "hm-trp telemetry 433mhz dropix")  
> **IMPORTANT**: Do not forget to screw the antennas on each telemetry module before feeding them, otherwise the HM-TRP chips can be broken.

### SOFTWARE \(PX4 / QGC\)

By default,** QgroundControl** under **PX4** firmware automatically recognizes telemetry modules as they have already been factory configured by Drotek.

If you do not like our configuration, you can configure your telemetry modules as you like using [this utility](http://vps.oborne.me/3drradioconfig.zip).

Simply connect the module to the PC via the USB cable and open the configuration software.

![](https://drotek.com/wp-content/uploads/2017/01/3DR_Radio_Config-700x536.png "3DR\_Radio\_Config hmtrp drotek")

You can change the values to increase your reach or communicate faster.

**Net ID**: This is the channel that will provide radio, 2 must have the same value.

**Tx Power**: The power tenfold by radio for data transmission. Can be increased to increase the range.

**Air Speed**: cruising speed data through the air. Can be reduced to increase the range.

**Baud**: Communication speed of telemetry. Can be decreased to increase the range.

You can find more information on this [site](http://ardupilot.org/copter/docs/common-configuring-a-telemetry-radio-using-mission-planner.html).

