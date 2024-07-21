---
description: The brain of the robot
---

# Microcontroller

Like our brain, a microcontroller is responsible for processing loads of information it receives from inputs, stores away data in its memory, and tells different outputs what to do. However, a microcontroller refers to only the computer that makes up a small part of a larger [embedded system](#user-content-fn-1)[^1]. A fully fledged microcontroller board that will support connections to all of our sensors, motors, motor drivers, and all other hardware interfaces is what our robot needs.&#x20;

<figure><img src="../../.gitbook/assets/Simple Embedded Systems Block Diagram (1).png" alt=""><figcaption><p>Simplified block diagram of an embedded system. </p></figcaption></figure>



### Popular microcontroller brands&#x20;

* STM32&#x20;
* ESP32&#x20;
* Arduino
* Teensy



<figure><img src="../../.gitbook/assets/image.png" alt=""><figcaption><p>An official Arduino R3 microcontroller board</p></figcaption></figure>

&#x20;

These are among a few of the most popular brands used for robot sumo and robotics projects in general. The microcontroller boards sold out there are generally very diverse and specialized for a variety of purposes, so the specs of your board should meet the requirements of your robot. We could really go on endlessly about this subject. In general, these are a few things you should consider when selecting a board: size, number of input/output pins, clock speed, peripherals, and cost.&#x20;



#### Size

This will never not be a consideration for our sumo bot. Ideally, choose a board that is small enough while leaving room for other parts that will eventually go on your PCB (more on this later in later sections).&#x20;

#### Input/Output Pins&#x20;

Consider the number of sensors, motors, and other devices you plan to attach to the microcontroller. A board like the[ Arduino MEGA R3](https://store.arduino.cc/products/arduino-mega-2560-rev3) is absolute overkill for a mini sumo bot (Not to mention too large).&#x20;



Clock speed&#x20;

When starting out, this isn't a huge consideration. Arduino works just fine for a sumo bot. Of course, a microcontroller with very clock speeds like Teensy will allow for faster response times and technical movements.&#x20;

#### Peripherals&#x20;

In addition to the number of I/O pins you want, peripherals are another consideration. Peripherals include other parts in microcontroller that help perform a specific task such as pulse width modulation (PWM), UART[^2], I2C[^3], ADC[^4], SPI[^5], etc.&#x20;



#### Cost

As always consider cost in your budget. Microcontroller boards usually range from $10-$30. Typically, higher end microcontrollers support better performance and other hardware requirements.&#x20;







[^1]: Boards like the Arduino UNO are considered **development boards** which may include memory and other I/O peripherals



[^2]: Universal Asynchronous Receiver Transmitter



[^3]: Pronounced "eye-squared C". One type of communication protocol&#x20;



[^4]: Analog-to-digital converter

[^5]: Serial peripheral interface
