# Sirius GPS

![](https://drotek.com/wp-content/uploads/2017/05/Sirius_rendu_oblique2.png "Sirius M8N GPS")

The Sirius GPS module features a u-blox **Neo M8N** chip for accurate positioning and a **LIS3MDL** heading sensor to provide heanding sensing to your vehicle. The Sirius GPS has a built-in active antenna located inside the case to allow the greatest performances along with a compatibility with the Galileo satellites constellation for a maximum reliability.

You can find more information on [this page](https://store.drotek.com/gps/856-sirius-gps-8944595120557.html).

### HARDWARE

Connect the cable to the GPS connector on your Pixhawk.

The module must be securely attached to the unit, preferably in the same direction as your [Pixhawk 3 Pro](https://store.drotek.com/autopilots/885-pixhawk-pro-autopilot-8944595120670.html) and raised a few centimeters above your motors.

No element should be placed above the Sirius GPS module to ensure optimal reception of the satellite.

### SOFTWARE \(PX4 / QGC\)

Before proceeding with the configuration, make sure that your Sirius GPS module is correctly positioned as described in the previous section.

To configure your Sirius GPS module with QgroundControl, go to the `Sensor` configuration window under `Compass`:

![](https://drotek.com/wp-content/uploads/2017/01/Menu_Sensors_QGC.png "Menu\_Sensors\_QGC px4 pixhawk")![](https://drotek.com/wp-content/uploads/2017/01/Compass_FcRotation_QGC.png "Compass\_FcRotation\_QGC px4")

In the window above, select `Rotation_None`.

Then calibrate the compass by successively performing the rotations indicated by the images.

![](https://drotek.com/wp-content/uploads/2017/01/Window_Compass_Calib_QGC-700x460.png "qgroundcontrol px4 pixhawk")

Your compass is configured and ready to be used.

