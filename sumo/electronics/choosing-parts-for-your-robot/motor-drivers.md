---
description: It's dangerous to go alone! Take this.
---

# Motor drivers

After you've selected your motors, you are probably wondering how we will supply a power to the motor to well... move the robot. At first glance, it's tempting to directly drive the motors using the pins on a microcontroller, but that is generally not a safe idea for several reasons. The main problems with directly controlling DC motors are overcurrent and overheating. On most microcontrollers, each pin is only able to handle a small amount of current (in milliamps) compared to the high current a DC motor requires. Additionally, the linear drop off (LDO) regulator embedded on microcontrollers will overheat if high current is consumed.  There are other reasons why directly controlling DC motors would be a poor idea, but the message is clear.&#x20;

{% hint style="danger" %}
Do not supply current directly to your motors!&#x20;
{% endhint %}

<figure><img src="../../.gitbook/assets/image (1) (1) (1).png" alt=""><figcaption><p>L293D H-bridge motor driver</p></figcaption></figure>

To operate our motors safely, we will need to use a motor driver. A motor driver is a circuit that controls both speed and direction of an electric motor. Motor drivers receive a low current logic-level input from the microcontroller and send a corresponding high-power output to the motor.  This function allows us to safely handle the power requirements of motors.&#x20;

{% hint style="success" %}
Motor drivers act as an interface between the microcontroller and motor.&#x20;
{% endhint %}

Motor drivers either come as individual ICs or as complete modules that can be purchased.  In the case you build the circuit from scratch, there may be additional components such as capacitors, resistors, and inductors that you will need to get. &#x20;

