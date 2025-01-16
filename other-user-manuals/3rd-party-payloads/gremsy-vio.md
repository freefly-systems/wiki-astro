# Gremsy Vio

<figure><img src="../../.gitbook/assets/thumbnail_image001.jpg" alt=""><figcaption></figcaption></figure>

{% hint style="warning" %}
Gremsy VIO integration is still in beta. The following are known issues:

* Photo counter doesn't increment, but photos are triggered
* LAT/LONG information is not passed to the VIO and is displayed as 0s.&#x20;
* **The VIO video feed only works on Tab 5 tablets with Pilot Pro.** It does not work with Tab 3 Pilot Pro or with herelink handset controllers.&#x20;
  * Tab 5 tablets can be identified with a green button next to the power button. Tab 3 tablets have a red button
{% endhint %}

The Gremsy VIO with the Smart Dovetail adaptor is compatible with the Pixhawk Payload Bus standard and can be integrated to work on Astro.

## Gremsy VIO Configuration

Please refer to the [Gremsy VIO wiki](https://docs.gremsy.com/payloads/vio) on how to configure the following settings:&#x20;

* [Set the static IP](https://docs.gremsy.com/payloads/vio/hardware-configuration/computers-ip-configuration) to 192.168.144.52
* [Update the VIO firmware](https://docs.gremsy.com/payloads/general/upgrade-firmware-and-software)

{% hint style="info" %}
The following versions are compatible with Astro:&#x20;

* Vio Payload App v1.0.6.6&#x20;
* Video Streaming App v1.5.0
* Vio Setting App v1.2.0
* Gimbal Firmware v7.8.3
{% endhint %}

## Astro Configuration

The following parameters need to be configured for Astro to communicate with the VIO. Click [here](https://freefly.gitbook.io/astro-public/pilots-operating-handbook/essential-software/auterion-mission-control/amc-vehicle-setup/parameters) to learn to set parameters on Astro.&#x20;

* SER\_EXT2\_BAUD = 115200&#x20;
* MNT\_RATE\_YAW = 0
  * You will need to force save
* Reboot Astro

{% hint style="info" %}
If switching back to other Smart Dovetail payloads like the LR1 Payload or Sentera 6X, perform a [parameter reset](https://freefly.gitbook.io/astro-public/pilots-operating-handbook/essential-software/auterion-mission-control/amc-vehicle-setup/parameters#resetting-parameters-to-factory-defaults) on Astro.
{% endhint %}

## Connect to Astro

Plug VIO into the Smart Dovetail on Astro and boot up the aircraft. VIO should stabilize after about 15s and the light on the front of the gimbal will turn purple if connected to Astro.&#x20;

Wait another 30-60s for the VIO video feed to appear in AMC

### Camera Settings

Once connected to the VIO through AMC, the following settings need to be applied in the VIO camera settings menu:

* RC mode = Standard
* Setting target = Gimbal Device
  * Then set Gimbal Mode = FOLLOW

### VIO Webpage Settings

On Pilot Pro, open a web browser like Chrome, and go to 192.168.144.52:8000. This will load a webpage hosted by the VIO payload. Under the Systems menu, set the following settings and hit apply:&#x20;

* Video Streaming
  * Bitrate = 4 Mbps
  * Port = 8554
  * Resolution = 1280x720
* Gimbal Control
  * Auto speed = DISABLE
* Mavlink
  * Camera Component ID = Camera 1 (100)&#x20;

Then reboot Astro and the VIO.&#x20;



