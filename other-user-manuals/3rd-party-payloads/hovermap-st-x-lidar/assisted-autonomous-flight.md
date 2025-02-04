# Assisted/Autonomous Flight

Hovermap ST-X enables assisted (AL1) and autonomous (AL2) flights for Astro in complex environments, allowing pilots to fly around obstacles, map close to objects, fly to difficult to reach places, and fly in GPS-denied in environments.

{% embed url="https://www.youtube.com/watch?v=ngLEDwsraSc" %}

{% hint style="info" %}
This wiki page is a high level overview of operating Hovermap on Astro. Please read Emesent's full documentation on how Hovermap works before conducting a flight in assisted or autonomous mode.&#x20;
{% endhint %}

{% hint style="warning" %}
Assisted and Autonomous functions are not available on aircraft with Doodle radios (Astro Blue/NDAA). We are working to enable this in the future.&#x20;
{% endhint %}

In particular, pilots should understand:&#x20;

* [How Hovermap works ](https://4999118.hs-sites.com/en/knowledge/understanding-hovermap)
* [How to recognize a SLAM slip ](https://4999118.hs-sites.com/en/knowledge/understanding-hovermap#WhatIsASlip)

## Preflight&#x20;

### Parameters&#x20;

For assisted and autonomous missions, Astro parameters need to be updated to enable communication with Hovermap and to increase rate setpoint tracking on Astro. To set these parameters:&#x20;

1. Update Astro to 1.5.18 firmware
2. Power on Astro and Hovermap. Wait for Hovermap to fully boot and connect over ethernet
3. Start an assisted/autonomous scan. The scan will begin but Hovermap will give an error. This is expected. Astro's parameters have been set by Hovermap but need a reboot to take effect.&#x20;
4. Reboot Astro and Hovermap. Parameters are now set, you should be able to start a scan and takeoff.&#x20;

{% hint style="info" %}
If you are flying Hovermap with Astro FW 1.6.14 or later, the following parameters need to be set:

* Set MAV\_2\_MODE = Custom
* Set COM\_RC\_IN\_MODE = RC Transmitter Only
* Set SER\_EXT2\_BAUD = 500000
{% endhint %}

{% hint style="danger" %}
**These parameters fundamentally change how Astro flies! Do NOT fly these parameters without a Hovermap, as this could lead to instability and possibly a crash!**&#x20;



To reset to the default Astro parameters - go to Advanced > Parameters > Tools > Reset to Vehicle Configuration Defaults
{% endhint %}

### Pilot Pro Configuration&#x20;

* Put the S2 switch in the 'up' position to allow Hovermap to take control. When armed, Hovermap will place Astro in 'Offboard flight mode'. **To take control away from Hovermap and give the pilot full authority, move the switch to the middle or down position.**
  * **Switching S2 is the only way to remove Hovermap from control. Pressing Position/Altitude/Manual mode without S2 change will allow Hovermap to re-establish control of Astro**&#x20;
* Open the Commander app. Click Assisted or Autonomous Mission and follow the prompts to setup the mission&#x20;
*   If desired, users can have a split screen view of AMC and the Commander app. This is particularly useful if Astro is configured with the [optional FPV module](https://store.freeflysystems.com/collections/astro/products/optional-fpv-system-for-astro).&#x20;

    <figure><img src="../../../.gitbook/assets/IMG_8374 (1).jpg" alt="" width="375"><figcaption><p>Commander App and AMC in side-by-side</p></figcaption></figure>

### Shield Settings&#x20;

We recommend setting your shield settings to be as large as possible, while still being able to complete the mission. The _**minimum**_ settings we recommend for Hovermap on Astro is:&#x20;

* Horizontal 1.5m
* Above 1.0m
* Below 1.0m&#x20;

### Astro Failsafe Settings&#x20;

These are the parameters we recommend for most environments.&#x20;

| Parameter          | Value   | Note                                                                                                          |
| ------------------ | ------- | ------------------------------------------------------------------------------------------------------------- |
| COM\_OBL\_ACT      | 2       | Hold mode if no hovermap and no RC control                                                                    |
| COM\_OBL\_RC\_ACT  | 5       | If no hovermap control, switch to hold mode                                                                   |
| COM\_LOW\_BAT\_ACT | Warning | Don't trigger action from low battery, let hovermap take control, or let land failsafe kick in if no hovermap |
| COM\_RCL\_EXCEPT   | 4       | Ignores RC loss when Hovermap is in control                                                                   |

## Shield Limitations

The shield system is designed to protect Astro and Hovermap from contacting any objects in flight, but it is not foolproof.&#x20;

The system has limitations, which pilots need to be cautious of when operating Hovermap. The ST-X can collect dense point clouds of objects from several meters away, so it is not necessary to get very close to objects for detailed scans.&#x20;

{% hint style="info" %}
It is important to know that Shield is a _**passive system**_. It will not protect against objects that are actively moving towards the drone, such as birds, moving ropes or falling rocks.
{% endhint %}

{% hint style="warning" %}
Always be ready to take over control of Astro in case of unexpected behavior!



The S2 switch in the middle or down position will remove Hovermap from control of Astro and give full authority to the pilot&#x20;
{% endhint %}

### Hovermap FW v3.2.1 Known Limitations:&#x20;

{% hint style="danger" %}
**Read carefully! Ignoring these could result in a crash**



Always set the shield limits as large as possible for your mission
{% endhint %}

* After takeoff Aircraft needs to climb _**above**_ the 'Below' shield threshold before the shield will fully activate.&#x20;
  * If the pilot does not climb above this limit, Hovermap will not apply the full shield and it will be possible for the pilot to fly into objects&#x20;
* In gusty environments, it is possible for the aircraft to drift closer to an object than the shield threshold with repeated pilot inputs toward the object.&#x20;
  * In particular, this can occur near foliage or other objects like ropes/wires/tarps that can move in the wind, allowing the aircraft to move closer  for a brief moment before the object moves back. Hovermap shield is a passive system and won't avoid an obstacle that moves.&#x20;
  * It is possible to get the aircraft 'stuck' with obstacles on all sides. If this occurs, take over control from Hovermap and fly Astro to a more open area, then reenable Hovermap.&#x20;
* Calculated RTL path is sometimes inefficient, requiring the aircraft to fly a longer than necessary distance back to the home point&#x20;

## Flight Tips

{% hint style="danger" %}
Astro + Hovermap ST-X is limited to a maximum ambient temperature of +40C/+104F
{% endhint %}

{% hint style="warning" %}
When carrying the Hovermap ST-X, Astro is at the upper limit of its maximum takeoff weight. Be cautious when flying Astro in hot or high-altitude environments.&#x20;



Astro will give warnings if the ESCs or motors start to overheat. Heed the warnings!
{% endhint %}

{% hint style="info" %}
Astro and Hovermap ST-X can operate in light to medium rain. Be sure to install the USB-C plug into the IO panel.&#x20;
{% endhint %}

* Hovermap should boot up when Astro is powered on. Hovermap will connect to Astro once the lights turn from orange to a slow blue flash.&#x20;
* Set up the Hovermap scanning via the Commander app.
  * Click Autonoumous Mission.
  * Follow the prompts for pre-flight checks.
  * Name your mission and check there is enough free storage on Hovermap.
* Start the scan and wait for Commander to complete the pre-flight check.
* Once the scanner is running, arm Astro, then click the 'Takeoff' button in the Commander App
* You can view a live preview of the point cloud generated by ST-X during the mission in the Commander app.

{% hint style="info" %}
Hovermap will automatically return home when it calculated RTL time reaches 0. This timer can be seen on the top of the Commander app. The RTL time is calculated based distance, altitude, and manuevers needed to reach the home point
{% endhint %}

* Stop the scan after landing via the Commander app. You will need to disable the shield to be able to land Astro

{% hint style="info" %}
For added situational awareness during the flight, you can view a live video from the aircraft using the [Astro FPV Camera](https://store.freeflysystems.com/products/optional-fpv-system-for-astro).



When using the FPV camera, AMC will try to take photos during the mapping mission. To turn this off:

* Set the Start > Camera actions: Stop taking photos
* Turn ON the option under Mission > Options 'Images in turnarounds'&#x20;
{% endhint %}

{% hint style="danger" %}
If you power off Astro before stopping the scan, the data can be corrupted!
{% endhint %}



## Emergency Procedures

If Hovermap is causing Astro to behave erratically, drifting, or otherwise abnormally, the pilot can takeover and remove Hovermap from control:

* Place S2 switch in middle or down position
* Astro will exit Offboard mode. If Astro has GPS lock, the aircraft will transition into Position mode. If not, Astro will transition to Altitude mode.

{% hint style="warning" %}
**Switching S2 is the only way to remove Hovermap from control. Pressing Position/Altitude/Manual mode without S2 change will allow Hovermap to re-establish control of Astro**&#x20;
{% endhint %}
