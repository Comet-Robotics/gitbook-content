---
description: Sometimes we need to step down the voltage
---

# Voltage regulator

The battery's voltage will unlikely match the voltage used by some of our parts, specifically the microcontroller (STM32 Nucleo32 boards accept 7V-12V on VIN, but it would be wise to avoid hitting maximum ratings). To get around this problem, we should use a voltage regulator to drop the voltage to a stable output that is desirable for our parts. There are two common types of step-down regulators that are sold: low drop-off (LDO) regulator and buck converters.&#x20;

### Low drop-off regulators (LDO)

LDOs are a type of linear DC regulator that does as the names suggest. Take a voltage input and output a lower, fixed voltage.&#x20;

#### Advantages&#x20;

* plug and play, easy to assemble on PCB&#x20;
* Less expensive&#x20;
* better for small power requirements&#x20;

#### Disadvantages&#x20;

* Less power efficient than buck converters

### Buck converters&#x20;

Buck converters are a type of DC-DC converter (which means they use a switching device as a MOSFET transistor) that lowers a voltage input while also increasing output current. They are generally more power efficient than linear regulators but come at cost of increased complexity, sometimes needing an additional inductor.&#x20;

#### Advantages

* more energy efficient (about 90%)&#x20;
* better for large power requirements&#x20;
* allows for variable voltage output&#x20;

#### Disadvantages&#x20;

* costlier, usually requires extra parts to assemble&#x20;

### General tips&#x20;

When choosing a voltage regulator, make sure of the following:&#x20;

* the voltage regulator accepts the input voltage from your battery&#x20;
* can output the correct voltage you are looking for.
* check the datasheet for suggested layout of components.&#x20;

{% hint style="info" %}
Microcontroller boards usually have a voltage regulator for 3.3V as well as for 5V.&#x20;
{% endhint %}



