# XL GPS

![](https://github.com/drotek/Docs-Pixhawk3Pro/blob/master/images/M8N-GPS-XL%20drotek.png?raw=true)

The XL GPS module features a u-blox **Neo M8N** chip and a **LIS3MDL **magnetometer to give your system the ability to know its position and orientation.

These modules offer better satellite reception than the GNSS "Mushroom" module thanks to their large antenna and their larger ground plane.

You can find more information on [this page](https://store.drotek.com/gps/880-ublox-neo-m8n-gps-lis3mdl-compass-xl-8944595120748.html).

### HARDWARE

Connect the cable to the GPS connector on your Pixhawk.

The module must be securely attached to the unit, preferably in the same direction as your Pixhawk 3 Pro and raised a few centimeters above your motors.

No element should be placed above the XL GPS module to ensure optimal reception of the satellite.![](https://drotek.com/wp-content/uploads/2017/02/DSC02067.jpg "XL ublox gps gnss galileo")

### SOFTWARE \(PX4 / QGC\)

Before proceeding with the configuration, make sure that your XL module is correctly positioned as described in the previous section.

To configure your XL GPS module with QgroundControl, go to the `Sensors` configuration window under `Compass`:

![](https://drotek.com/wp-content/uploads/2017/01/Menu_Sensors_QGC.png "Menu\_Sensors\_QGC px4 pixhawk")![](https://drotek.com/wp-content/uploads/2017/01/Compass_FcRotation_QGC.png "Compass\_FcRotation\_QGC px4")

In the window above, select `Rotation_None`.

Then calibrate the compass by successively performing the rotations indicated by the images with your camera.

![](https://drotek.com/wp-content/uploads/2017/01/Window_Compass_Calib_QGC-700x460.png "qgroundcontrol px4 pixhawk")

