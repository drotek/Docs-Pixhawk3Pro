# rtk-gps

![](https://github.com/drotek/Docs-Pixhawk3Pro/blob/master/images/gps-rtk-drotek-doc.png?raw=true)

You can find all informations on the Drotek RTK modules and how to use them efficiently by following [this link](https://www.gitbook.com/book/drotek/doc-rtk/details).

## HARDWARE

You will need:

* A pair of u-blox M8P GPS devices
* A laptop/PC with QGroundControl 
* A Telemetry or WiFi between the autpilot and the laptop 

The rover module must be securely attached to the unit, preferably in the same direction as your Pixhawk and raised a few centimeters above your motors.  
Connect the JST-GH cable on the `GPS` connector of your Pixhawk and the Rover connector of the RTK module.

[![neo-m8p](../../../.gitbook/assets/m8p-pixhawk.JPG)](https://store.drotek.com/gps/881-xl-rtk-gps-neo-m8p-rover-8944595120625.html)

> **Note** Don't forget to place the switch on the rover position.

![neo-m8p ublox](../../../.gitbook/assets/switch-rover-rtk.JPG)

Then, connect the laptop to the base RTK module with a micro USB cable.

![base ublox m8p](../../../.gitbook/assets/gps-rtk-xxl-neo-m8p-3.jpg)

The base GPS device needs to be in a fixed position while it is used. So make sure it is in a position where it is not moved and with a clear view to the sky, not close to a building. Preferably, it should be elevated \(for example with a tripod, or on a roof\). Compared to normal GPS, RTK is more sensitive and needs a careful setup.

![base gnss rtk](../../../.gitbook/assets/xxl-rtk-gps-neo-m8p-2.jpg)

## SOFTWARE \(PX4 / QGC\)

Before proceeding with the configuration, make sure that your rover module is correctly positioned as described in the previous section.

To configure this module with QgroundControl, go to the `Sensor` configuration window under `Compass`:

![Menu\_Sensors\_QGC px4 pixhawk](https://drotek.com/wp-content/uploads/2017/01/Menu_Sensors_QGC.png)![Compass\_FcRotation\_QGC px4](https://drotek.com/wp-content/uploads/2017/01/Compass_FcRotation_QGC.png)

In the window above, select `Rotation_None`.

Then calibrate the compass by successively performing the rotations indicated by the images with your camera.

![qgroundcontrol px4 pixhawk](https://drotek.com/wp-content/uploads/2017/01/Window_Compass_Calib_QGC-700x460.png)

If you started QGroundControl via console, you should see the status update there as well \(if not, make sure the autoconnect to RTK GPS option is checked in the general application settings\).

![base gnss rtk](../../../.gitbook/assets/px4-rtk.png)

What you see is the status of the survey-in process. This is a startup procedure to get an accurate position estimate of the base station. It's configured to run at least 3 minutes and it must reach an accuracy of 1 meter. The current accuracy is printed to the console. It takes several minutes to complete, depending on the GPS signal reception.

While survey-in is running you can already start the vehicle and make sure it connects to QGroundControl. No further setup on the vehicle is required. Once the survey-in process is finished, QGroundControl automatically starts to send the RTCM correction data to the vehicle. After a while it should switch to RTK mode, which is visible in the GPS status \(3D RTK GPS Lock\):

![base gnss rtk](../../../.gitbook/assets/qgc_rtk_gps_status.png)

There are two RTK modes: Float and Fixed. While the Float mode is easier to reach, it is a bit less accurate than Fixed mode \(further explanations are for example here\). The system will automatically switch to Fixed mode when the signal is good enough.

Now you can start to fly!

You may also need to tune some parameters. The default parameters are tuned assuming a GPS accuracy in the order of meters, not centimeters.

