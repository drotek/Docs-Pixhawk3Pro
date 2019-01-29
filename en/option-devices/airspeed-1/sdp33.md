# SDP3X sensor

![](https://github.com/drotek/Docs-Pixhawk3Pro/blob/master/images/sdp3x-drotek.png?raw=true)

\*\*Plane\*\* supports the use of an airspeed sensor, which can help in windy condition, slow flight and autonomous landings. It is not recommended for most new users, however, as it does require additional tuning and adds one more layer of control to set up. The digital differential airspeed sensor has a high resolution and does not suffer from the noise induced by long cables. The \*\*SDP3X\*\* sensor from Sensirion has an excellent accuracy and repeatability \(even below 1Pa\), no zero-point offset \(no drift\), and is calibrated and temperature compensated.

## HARDWARE

The following sections show how to wire sensors to the flight controller.

Connect the airspeed sensor to Pixhawk's **I2C** port \(or I2C splitter module\). Using the rubber tubing, connect the longer extension on the pitot tube to the cone that protrudes from the top of the airspeed sensor board \(off the off-white, square section protruding off the top of the board\), and connect the shorter extension on the pitot tube to the cone protruding from the base of the board.

![SDP33 Pixhawk 3 Pro](https://github.com/drotek/Docs-Pixhawk3Pro/tree/32dda96b035b92f6eb6f2bdfb9288b10705b6073/images/sdp33-pixhawk.jpg?raw=true)

When you place the **airspeed sensor** in your aircraft, use the **pitot** tube set in the kit \(the kit comes with a single tube to measure both static and total pressure\). Make sure the holes in the side of the tube are not covered. They should be at least **1 centimeter** out past the nose. First, connect the two tubes coming out the back to the airspeed sensor. The tube coming straight out the back should go into the top port and the tube exiting at an angle should connect to the bottom port on the airspeed sensor. Drill or cut a small hole in the foam and push it through to the front.

If you are using Plane in an aircraft with the propeller in the nose, the pitot tube must be mounted out on one wing, at least a foot away from the fuselage to be outside the prop flow.

![airspeed ardupilot px4 pixhawk](https://drotek.com/wp-content/uploads/2017/01/pitotinstalled1-700x404.jpg)

## SOFTWARE \(PX4 with QGC\)

No configuration is required under **QgroundControl** for the use of this sensor.

To display in **QgroundControl** the value read by the sensor, click: ![QGC px4 drotek](https://drotek.com/wp-content/uploads/2017/01/Icone_Flight_Data_QGC.png)

The widget on the right allows you to view the data from the various sensors on your **Pixhawk 3 Pro**.

![QGC UI](https://drotek.com/wp-content/uploads/2017/01/Flight_Data_Viewer_QGC.png?raw=true)

To view the data of interest, click on:![QGC px4 pixhawk](https://drotek.com/wp-content/uploads/2017/01/Reglage_Flight_Data_Viewer_QGC.png)

![QGC UI](https://drotek.com/wp-content/uploads/2017/01/Flight_Data_List_QGC-250x606.png?raw=true)

Check the `Air Speed` setting. You can choose the size of the display by checking `Large`.

Confirm by clicking on `OK`.
