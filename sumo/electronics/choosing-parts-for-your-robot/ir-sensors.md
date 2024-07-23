---
description: The eyes of the robot
---

# IR sensors

In robot sumo, there are two common types of sensors used for object detection: ultrasonic and infrared (IR) sensors. Ultrasonic sensors use sound waves to measure distance while IR sensors rely on presence of infrared radiation. In this guide, we mainly recommend IR sensors because they respond quicker due to using light instead of sound waves. Granted, ultrasonic sensors are better at accurately measuring distances, but in robot sumo this is not required.&#x20;



IR sensors come in two types: analog and digital sensors. Analog sensors, such as the Sharp [GP2Y0A21YK0F](https://www.pololu.com/product/136) sensor outputs a voltage that corresponds to a distance. Digital sensors such as the JSUMO's  [JS40F](https://www.jsumo.com/js40f-digital-infrared-ir-distance-sensor-min-40-cm-range) uses a 0 or 1 to determine if an object is present.





<figure><img src="../../.gitbook/assets/image (2) (1).png" alt=""><figcaption><p>JSUMO JS40F IR sensors</p></figcaption></figure>

{% hint style="warning" %}
If using JSUMO sensors, be mindful of limited documentation that is provided.&#x20;
{% endhint %}

<figure><img src="../../.gitbook/assets/image (3).png" alt="" width="375"><figcaption><p>SHARP GP2Y0A21YK0F</p></figcaption></figure>

{% hint style="info" %}
There is an Arduino library called [SharpIR](https://www.arduino.cc/reference/en/libraries/sharpir/) that makes reading analog signals from several models of IR sensors a lot easier.&#x20;
{% endhint %}

