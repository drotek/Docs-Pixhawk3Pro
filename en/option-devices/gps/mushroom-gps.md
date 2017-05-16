![](https://drotek.com/wp-content/uploads/2017/01/ublox-neo-m8n-gps-hmc5983-compass.jpg "ublox m8n drotek")

The "Mushroom" GPS module features a u-blox**Neo M8N** GNSS \(GPS, GLONASS, BeiDou, QZSS,SBASand Galileo-ready\) anda**HMC5983**magnetometer to give your system the ability to know its position and orientation.

All in a removable case to avoid interference.

You can find more information on[this page](https://drotek.com/shop/en/drotek-parts/820-ublox-neo-m8n-gps-hmc5983-compass.html).

  


### HARDWARE

Connect the cable to the GPS connector on your Pixhawk.

The module must be securely attached to the unit, preferably in the same direction as your Pixhawk 3 Pro and raised a few centimeters above your motors.

No element should be placed above the "Mushroom" module to ensure optimal reception of the satellite.

![](https://drotek.com/wp-content/uploads/2017/01/DSC02039-700x369.jpg "pixhawk ublox gps drotek")

  


### SOFTWARE \(PX4 / QGC\)

  


Before proceeding with the configuration, make sure that your Mushroom module is correctly positioned as described in the previous section.

To configure your mushroom GPS module with QgroundControl, go to the "**Sensors**" configuration window under "**Compass**":

![](https://drotek.com/wp-content/uploads/2017/01/Menu_Sensors_QGC.png "Menu\_Sensors\_QGC px4 pixhawk")![](https://drotek.com/wp-content/uploads/2017/01/Compass_FcRotation_QGC.png "Compass\_FcRotation\_QGC px4")

  


In the window above, select "Rotation\_None".

Then calibrate the compass by successively performing the rotations indicated by the images with your camera.

![](https://drotek.com/wp-content/uploads/2017/01/Window_Compass_Calib_QGC-700x460.png "qgroundcontrol px4 pixhawk")

  


For the GPS "Mushroom" and only for this GPS model, a rotation is to be parameterized in QgroundControl.

To do this, go to the configuration window "Sensors" under "Set Orientation".

In the window that appears on the right, select "**ROTATION\_NONE**" in "Autopilot Orientation" and "**ROTATION\_ROLL\_180**" in "External Compass Orientation"

Then click "OK"

![](https://drotek.com/wp-content/uploads/2017/01/External_Compass_SetOrientation_QGC-250x175.png "External\_Compass\_SetOrientation\_QGC")

