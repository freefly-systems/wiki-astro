# Astro Software v1.7 - What’s New

&#x20;                                                                  [<mark style="color:red;">**|  UPDATE NOW**</mark>](software.md#updating-astro-firmware)  <mark style="color:red;">**|**</mark>



***

#### New: LR1 Thermal Module \[Boson 640R]

* We just started shipping the [Thermal Module for the LR1 Payload](https://store.freeflysystems.com/collections/astro/products/lr1-thermal-upgrade). This adds a radiometric 640x512 LWIR core to Astro!&#x20;

<figure><img src="../../.gitbook/assets/240820_225005_807 (1).jpg" alt="" width="320"><figcaption></figcaption></figure>

* More info can be found [here](https://freefly.gitbook.io/astro-public/other-user-manuals/payloads/lr1-payload/lr1-lenses-and-expansion/expansion-modules/lr1-thermal-module), feature highlights include:&#x20;
  * Spot temperature readout
    * Mix/max temperatures of region
    * Adjustable region size
    * Selectable Fahrenheit, Celsius, Kelvin
  * Media capture - Jpeg, Radiometric Tiff, both, video
  * Zoom - digital up to 8x

***

#### New: LR1 and A7R4 Payload Features

*   **Digital Zoom:**&#x20;

    * 1.0 to 4.0x digital zoom for live preview and saved images/videos. This can be controlled with the on screen buttons or the right hand rocker on pilot pro.&#x20;



    <figure><img src="../../.gitbook/assets/LR1 Digital Zoom.gif" alt=""><figcaption></figcaption></figure>
* **Tap to Focus:**&#x20;
  * A new mode under Auto Focus is exposed: Flexible Spot with size small, medium, or large.
  * This can be enabled/disabled by the tap icon next to the shutter button as well

<figure><img src="../../.gitbook/assets/LR1Taptofocus.gif" alt=""><figcaption></figcaption></figure>

* Note: A7R4 tap to focus is much slower than LR1, limited by the camera's autofocus speed

***

#### Update: Payload zoom on Pilot Pro right side rocker

* Zoom function is now mapped to the right hand rocker (below R1 button) on Pilot Pro. This works for:
  * LR1 Payload&#x20;
  * A7R4 Payload&#x20;
  * Thermal Module for LR1&#x20;
  * Wiris Pro Payload

***

#### Fixes and Improvements:

* LR1 Payload - Fixed an overheat condition on bootup&#x20;
* LR1 Payload - Fixed soft focus in infinity focus mode
* A7R4 Payload - Removed incorrect 50mm infinity focus setting
* AMC - Removed Structure Scan
* AMC - LR1 and Thermal Module appear as EO/IR toggle when both connected
* Distance Sensor Module - can now select between ft. and meters&#x20;
* Distance Sensor Module - displays _+99m_ when max range is reached
* Added support for up to 3 cameras on Astro&#x20;
  * Currently, only video can be recorded on LR1 and one additional camera (ex: LR1 and Thermal) simultaneously. Wiris Pro is treated in the software as one camera



&#x20;                                                                  [<mark style="color:red;">**|  UPDATE NOW**</mark>](software.md#updating-astro-firmware)  <mark style="color:red;">**|**</mark>





