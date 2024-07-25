---
description: Guide to our robot's power needs
---

# Calculating power consumption

Every part in the sumo bot, from the motors to the IR sensors, will use up a certain amount of power, current, and voltage. It's a good idea we keep track of how much of each is expected to be consumed by our robot's circuit, so we choose parts that will satisfy the power need of the whole bot. When calculating our power budget for our robot, we are interested in calculating the following:&#x20;

* max power drawn
* nominal and peak current drawn by robot&#x20;
* max voltage used by each part

Power is defined as unit of electrical energy per unit time, measured in watts (W). Electrical power is given by the formula:

$$
P = I*V
$$

So, if we know the rated current and voltage used by the part, we can easily solve for the power used. Finding current and voltage of each part can be found in two ways: either by empirical testing or reading datasheets.&#x20;

{% hint style="info" %}
Read part manufacturer's website or datasheet to find information on current and voltage.
{% endhint %}

{% hint style="info" %}
We recommend using a spreadsheet to keep track of all of these specs. Here is a nice [**template** ](https://docs.google.com/spreadsheets/d/1EInbjM8BmOp94nWb7\_W9tbPjEoU6eVHQh682lEF8lII/edit?usp=sharing)we made to get you started.&#x20;
{% endhint %}











