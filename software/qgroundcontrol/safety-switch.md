# safety switch

The Pixhawk is sold without the switch safety. To arm your autopilot without it, you must activate the `Circuit breaker` function in QGroundControl. Setting this parameter to `22027` will disable IO safety.

{% hint style="warning" %}
Enabling this circuit breaker is at own risk. The other solution is to connect your own safety switch to the All-in-One port of your Pixhawk.
{% endhint %}

![safety switch](../../.gitbook/assets/arm_switch.png)

