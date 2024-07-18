---
description: This will keep our robot within the ring
---

# Edge sensors

Our robot is now equipped with sensors to see the enemy robot, but how will it know not to accidentally misstep outside of the dohyo's white border? To prevent our robot from meandering into no man's land, we should give it some edge sensors.&#x20;



### Using phototransistors for edge detection

Edge sensors commonly used in robot sumo make use of a phototransistor and IR diode pair. The IR diode acts as a sender, emitting IR light out to an object. Once the light eventually reflects, it is received by the phototransistor which then outputs a voltage between 0 and VIN[^1]. This output voltage is dependent on the contrast in color of the surface being detected. Using these line sensors, we can see where the white edge of the ring begins and where the black area ends by comparing the contrast.&#x20;



### Recommendations &#x20;

There are a few sensors I've seen and used that are recommended for sumo. I'll post them below:&#x20;

* JSUMO[ ML1 line sensors](https://www.jsumo.com/micro-line-sensor-ml1) (these are the ones we typically use)&#x20;
* [TCRT5000](https://www.amazon.com/HiLetgo-Channel-Tracing-Sensor-Detection/dp/B00LZV1V10/ref=asc\_df\_B00LZV1V10?tag=bingshoppinga-20\&linkCode=df0\&hvadid=80814196416238\&hvnetw=o\&hvqmt=e\&hvbmt=be\&hvdev=c\&hvlocint=\&hvlocphy=\&hvtargid=pla-4584413741981145\&psc=1)
* Pololu [QTR-1A](https://www.pololu.com/product/2458)

<figure><img src="../../.gitbook/assets/image (4).png" alt=""><figcaption><p>ML1 Line sensor</p></figcaption></figure>

### Placement&#x20;

Line sensors should be placed on the underside of the robot, so they have clear view of the dohyo's surface. It is best to place them at the corners of the bot for the maximum coverage.&#x20;

{% hint style="info" %}
For mini sumo, placing two sensors to cover the front edge are good enough.
{% endhint %}

{% hint style="info" %}
Make sure to give your bot enough ground clearance, so the sensors have enough distance to detect light
{% endhint %}

[^1]: VIN is the voltage supplied, usually 3.3V or 5V

