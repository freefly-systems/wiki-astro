# Pilot Pro Controller

## Pilot Pro Wiki

For specific details regarding the Pilot Pro Controller, refer to for Pilot Pro Wiki here -> [https://freefly.gitbook.io/pilot-pro-public](https://freefly.gitbook.io/pilot-pro-public/)



## Upgrading Astro to Pilot Pro Controller (950-00140-02)

The process for existing Astro customers who want to upgrade their Herelink Controller to the Pilot Pro Controller is outlined below. This process involves a software update to the Herelink Radio Air unit installed on the Astro.

{% hint style="warning" %}
* You can contact support@freeflysystems.com if you would like to get your Astro upgraded by the Freefly team.
* This upgrade is not straightforward but it can be executed by technically proficient customers on their own.
* NOTE: Some Astros do not have the required UART cable exposed. If you remove the Herelink Air cover and do not see the bundled cable to connect, the upgrade has to be done by the Freefly team. Please contact Freefly Support.
{% endhint %}



**Required Tools:**

* 1.5mm Hex driver
* USB micro cable
* A wire clipper/cutter
* Tweezers or paperclip



**Process:**

_(_[_**Video link**_ ](https://www.loom.com/share/14b68e89742147e69fb4fc8632262a84?sid=21e2c2c9-a019-47c5-808e-7cb4b8d75046)_for visual assistance with the process)_

1. Purchase a [Pilot Pro Controller (Herelink RF)](https://store.freeflysystems.com/products/pilot-pro)
2. Make sure Astro is on [Software v1.4 or above](../../../maintenance/software-release-notes/software.md)
3. Software Update for Herelink
   * [Download](https://freeflyeng.s3.us-west-2.amazonaws.com/_SoftwareReleases/script-herelink-user_pilot_pro_upgrade-v1.zip) the Herelink software update package.
   * [Remove the Herelink Cover and Seal](pilot-handsets/herelink-controller-maintenance/removing-reinstalling-the-herelink-cover.md#removing-the-herelink-cover).
   * Remove the usb connector from the Herelink
   * Connect the device to your computer via USB.
     * Remove the isolator if installed and if its in the way to make space for the USB cable.
   * Power on the Astro with one battery
   * Run the software update (Mac instead of a Windows computer is recommended)
     * There will be folders for macOS and Windows platforms. Ensure to run the script labelled "1\_..." first. After this script successfully completes, proceed with the script labelled "2\_....""
     * To bypass operating system warnings: On Windows, run scripts as administrator. On Mac, click on the script while pressing the "control" button on the keyboard, then press open.
   * Connect the usb cable that is coming from Astro back to the Herelink
4. Plug in the UART port
   * **Reminder**: If you do not have this cable exposed when you open the Herelink cover, then the update must be done by the Freefly team
   * Unlike the Herelink handset configuration, Pilot Pro requires this port, so it must be installed.
   * Find the existing, unused UART cable.
   * Carefully cut the zip tie with a wire clipper/cutter.
   * Connect the cable to the UART port of the Herelink Air unit.
5. Bind the radios
   * Prepare tweezers or paperclip.
   * Power on Astro with one battery.
   * Using tweezers, press and hold the Herelink Air Unit's "Pair/Reset" button until LED2 blinks (hold approximately 3 seconds).
   * Repeat this step on the Pilot Pro's Herelink Radio.
   * Ensure the light goes solid.
   * Open the AMC app on Pilot Pro and verify the connection to the aircraft.&#x20;
6. [Close up the Herelink Cover and Seal.](pilot-handsets/herelink-controller-maintenance/removing-reinstalling-the-herelink-cover.md#reinstalling-the-herelink-cover)
7. You're done! Perform your preflight checks as usual and enjoy your flight.



