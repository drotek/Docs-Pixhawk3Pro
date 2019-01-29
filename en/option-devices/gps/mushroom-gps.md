# mushroom-gps

![ublox m8n drotek](https://github.com/drotek/Docs-Pixhawk3Pro/blob/master/images/NEO-M8N-GPS-+-LIS3MDL-compass-%28Pixhawk-3-Pro%29-579.png?raw=true)

The "Mushroom" GPS module features a u-blox **Neo M8N** chip and a **LIS3MDL** magnetometer to give your system the ability to know its position and orientation.

All in a removable case to avoid interference.

You can find more information on [this page](https://store.drotek.com/gps/871-691-ublox-neo-m8n-gps-lis3mdl-compass-8944595120588.html#/108-cable-dropix).

## HARDWARE

Connect the cable to the GPS connector on your Pixhawk.

The module must be securely attached to the unit, preferably in the same direction as your [Pixhawk 3 Pro](https://store.drotek.com/autopilots/885-pixhawk-pro-autopilot-8944595120670.html) and raised a few centimeters above your motors.

No element should be placed above the "Mushroom" module to ensure optimal reception of the satellite.

![pixhawk ublox gps drotek](https://drotek.com/wp-content/uploads/2017/01/DSC02039-700x369.jpg)

## SOFTWARE \(PX4 / QGC\)

Before proceeding with the configuration, make sure that your Mushroom module is correctly positioned as described in the previous section.

To configure your mushroom GPS module with QgroundControl, go to the `Sensor` configuration window under `Compass`:

![Menu\_Sensors\_QGC px4 pixhawk](https://drotek.com/wp-content/uploads/2017/01/Menu_Sensors_QGC.png)![Compass\_FcRotation\_QGC px4](https://drotek.com/wp-content/uploads/2017/01/Compass_FcRotation_QGC.png)

In the window above, select `Rotation_None`.

Then calibrate the compass by successively performing the rotations indicated by the images with your camera.

![qgroundcontrol px4 pixhawk](https://drotek.com/wp-content/uploads/2017/01/Window_Compass_Calib_QGC-700x460.png)

Your compass is configured and ready to be used.

