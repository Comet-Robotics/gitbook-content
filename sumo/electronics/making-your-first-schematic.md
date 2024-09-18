---
description: mapping out the robot's electronics
---

# Making your first schematic&#x20;

Now that we have a complete list of electronics and have an estimate of our bot's power needs, we now need to outline how everything will go together in a **schematic**. A schematic is essentially a blueprint for the circuit inside the sumo bot, labeled with everything we need to know about pin connections.  This schematic will be directly referenced from in a later section when we start designing your bot's PCB. For now, let's talk about the tool we will be using to design our schematic, **KiCAD**. **KiCAD** is a free electronic design automation (EDA) software that can be used to make electrical schematics and PCBs. Other popular options exist such as Altium, OrCAD, Eagle, and EasyEDA, but in this tutorial we will stick to KiCAD since it's free, easy to use, and pretty versatile.&#x20;



### Installing KiCAD

KiCAD can be downloaded for Windows, MacOS, and Linux. The latest version of KiCAD can be installed by following the download link: [https://www.kicad.org/download/](https://www.kicad.org/download/). After downloading the installer, follow the guided instructions for your operating system.

{% hint style="info" %}
As of August 8th, 2024, the latest version of KiCAD is 8.04&#x20;
{% endhint %}

### Creating your first project

Upon opening the KiCAD for the first time, you will be led to the Project Manager. To create a project, click on **File -> New Project.** Then, navigate to the location you want to create your project and give it your preferred name. Make sure the **Create a new folder for your project** box is ticked.&#x20;

<figure><img src="../.gitbook/assets/image (5).png" alt=""><figcaption><p>KiCAD project manager homepage</p></figcaption></figure>





