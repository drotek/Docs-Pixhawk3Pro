# Mushroom GPS

![](https://drotek.com/wp-content/uploads/2017/01/ublox-neo-m8n-gps-hmc5983-compass.jpg "ublox m8n drotek")

The "Mushroom" GPS module features a u-blox **Neo M8N** chip and a **LIS3MDL **magnetometer to give your system the ability to know its position and orientation.

All in a removable case to avoid interference.

You can find more information on[ this page](https://drotek.com/shop/en/u-blox/876-module-gps-ublox-neo-m8n-magnetometre-lis3mdl-pixhawk-3-pro.html?live_configurator_token=8746d605a9c04b1e35dffc6d98e0a9e5&id_shop=1&id_employee=1&theme=&theme_font=).

### HARDWARE

Connect the cable to the GPS connector on your Pixhawk.

The module must be securely attached to the unit, preferably in the same direction as your Pixhawk 3 Pro and raised a few centimeters above your motors.

No element should be placed above the "Mushroom" module to ensure optimal reception of the satellite.

![](https://drotek.com/wp-content/uploads/2017/01/DSC02039-700x369.jpg "pixhawk ublox gps drotek")

### SOFTWARE \(PX4 / QGC\)

Before proceeding with the configuration, make sure that your Mushroom module is correctly positioned as described in the previous section.

To configure your mushroom GPS module with QgroundControl, go to the `Sensor` configuration window under `Compass`:

![](https://drotek.com/wp-content/uploads/2017/01/Menu_Sensors_QGC.png "Menu\_Sensors\_QGC px4 pixhawk")![](https://drotek.com/wp-content/uploads/2017/01/Compass_FcRotation_QGC.png "Compass\_FcRotation\_QGC px4")

In the window above, select `Rotation_None`.

Then calibrate the compass by successively performing the rotations indicated by the images with your camera.

![](https://drotek.com/wp-content/uploads/2017/01/Window_Compass_Calib_QGC-700x460.png "qgroundcontrol px4 pixhawk")

Your compass is configured and ready to be used.

