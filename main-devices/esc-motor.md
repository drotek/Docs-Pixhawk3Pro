# esc-motor

![ESC T-motor drotek](https://drotek.com/wp-content/uploads/2017/01/DSC02089-1-700x258.jpg)

The **ESC** \(Electronic Speed Controller\) allows the speed control of the motors according to the orders of the flight controller. Typically the control signal used by the ESCs is a PWM \(Pulse Width Modulation\) but some models allow the use of **I2C** or **CAN** signals.

The Pixhawk 3 Pro has **8 PWM outputs** for 8 ESC / Motor pairs.

## HARDWARE

Please connect each of your PWM ESCs to the corresponding "**Main Out**" output. Refer to the diagram below for the order of your ESC / Motor.

![esc tmotor drotek](https://drotek.com/wp-content/uploads/2017/01/DSC02091-1-700x380.jpg)

![Motors\_Wiring pixhawk by drotek](https://drotek.com/wp-content/uploads/2017/01/Motors_Wiring-700x744.jpg)

All blue motors should only be used with CCW propellers. Green motors with CW propellers.

To see what a CCW propeller looks like, please see the previous picture.

Also check the direction of the motors.

> **For safety reasons, remove the propellers before handling!**

To reverse the direction of a motor, simply swap two of the three cables that link the motor to the ESC.
