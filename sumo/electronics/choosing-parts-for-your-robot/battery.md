---
description: The lifeblood of the robot
---

# Battery

Obviously, our robot can't work without some sort of energy source. Now that we have mostly picked out our parts, we should now talk about what sort of things we are looking for when selecting a battery.

### Battery type (why you should choose LiPO)&#x20;

Batteries come in different types such as alkaline, lithium-ion (Li-On), lead acid, and lithium-polymer (LiPO) batteries, etc. Like in combat robotics, LiPO batteries are used in robot sumo for being lightweight, energy dense, and having a high discharge rate for their size. If you are going to choose a battery for your bot, it should most definitely be a LiPO.&#x20;

### Voltage (S)

On every pack of LiPO batteries there is a number followed by an 'S' that indicates how many cells one battery has inside. Each cell in the pack provides 3.7V. To calculate total voltage, you would just need to multiply number of cells by 3.7. For example, if you are using a 2S battery, you would get 2x3.7V for 7.4V total. Without question, the higher the voltage rating, the more powerful the battery is.  Most importantly of all...

{% hint style="warning" %}
Double check that your battery's voltage is higher than your motor's voltage
{% endhint %}

### Current Capacity&#x20;

This number, measured in **milli-amperes** (**mAH**), generally tells you how long you can expect your battery pack to last for. Your robot will face off in multiple matches, so we want to make sure we choose a battery that can last several matches (each match is roughly 10 to 15 seconds). A simple formula can give us a rough estimate of what to expect.

$$
time = capacity / current _{peak}
$$

Current is peak current of the whole bot's circuit (we will learn how to find this in an upcoming section).&#x20;

### Discharge rate (C)  &#x20;

This spec tells us what the maximum amount of current a battery is capable of supplying to our robot. The higher the C, the more continuous power that can be supplied. We can calculate peak current with the following formula:&#x20;

$$
current = capacity *dischargeRate
$$

{% hint style="warning" %}
Check if peak current of battery is greater than peak current of circuit.&#x20;
{% endhint %}

### What battery connectors should you use?&#x20;

We recommend using XT30, XT60, or JST connectors for your battery. (Most batteries either come with XT30 or XT60 anyways)&#x20;
