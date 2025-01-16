# Updating Firmware

## Updating Astro Firmware

{% hint style="info" %}
You can determine if Astro needs an update by following steps 2-4 below. The current firmware number available will be on the [Software Release Notes](./#current-firmware-versions) page.
{% endhint %}

1. [**Download**](https://freeflysystems.com/support/astro-support) the firmware file from the [**Astro Support page**](https://freeflysystems.com/support/astro-support) or [the Suite](https://suite.auterion.com/downloads/firmware).
2. Connect Astro to your computer with a USB cable.
3. Power on aircraft **with one battery** and wait about 15 seconds for aircraft to fully boot.
4. Using a browser such as Chrome or Safari, open the aircraft's info/update page at [http://10.41.1.1](http://10.41.1.1) (internet connection is not needed).
5. In the Update Auterion OS box, click Browse, and select the firmware file downloaded above.
6. Click Update. (Should take about 10 minutes.)
7. After the update completion message, verify that the webpage shows a "Release name" that matches the downloaded file and that all the motor LEDs are on.

{% hint style="info" %}
If the aircraft gives an error message, power cycle the aircraft and try again.&#x20;
{% endhint %}

{% hint style="warning" %}
After updating the aircraft, make sure that all apps in the Freefly Updater on your controller are [up-to-date](https://freefly.gitbook.io/astro-public/maintenance/standard-maintenance-procedures/herelink-controller-maintenance/updating-herelink-software#managing-app-updates-with-freefly-updater).&#x20;

If Freefly Updater is not installed, follow these [instructions](https://freefly.gitbook.io/astro-public/maintenance/standard-maintenance-procedures/herelink-controller-maintenance/switching-to-freefly-updater).
{% endhint %}

### Checking Astro Firmware Version

{% tabs %}
{% tab title="Video" %}
{% embed url="https://www.loom.com/share/f0697b699e944b7da68ce24e7cbfa081" %}
{% endtab %}

{% tab title="Text" %}
* Connect Astro to your computer with a USB cable.
* Power on aircraft **with one battery** and wait about 15 seconds for aircraft to fully boot.
* Using a browser such as Chrome or Safari, open the aircraft's info/update page at [http://10.41.1.1](http://10.41.1.1) (internet connection is not needed).
{% endtab %}
{% endtabs %}

***

## Updating Herelink Firmware

As of Astro Version 1.4.6, Herelink is maintained through the Freefly Updater. Instructions on how to install the Freefly Updater can be found [here](https://freefly.gitbook.io/astro-public/maintenance/standard-maintenance-procedures/herelink-controller-maintenance/switching-to-freefly-updater#intro).&#x20;

Once the Freefly Updater has been installed, it can be used to [update AMC and other apps](https://freefly.gitbook.io/astro-public/maintenance/standard-maintenance-procedures/herelink-controller-maintenance/updating-herelink-software).&#x20;



***

## How to Reset to Default Astro Parameters

{% tabs %}
{% tab title="Video" %}
{% embed url="https://www.loom.com/share/fed073ac16ba4bac937565dbee04dbb2?sid=0e7d0dab-7543-48fc-95fb-95e4ef270bc5" %}
{% endtab %}

{% tab title="Text" %}
* Open AMC and [activate Advanced mode](https://freefly.gitbook.io/astro-public/astro/pilots-operating-handbook/software/auterion-mission-control/amc-vehicle-setup/advanced-vehicle-setup#activating-advanced-mode)
* Connect AMC to Astro
* Select: Vehicle setup > Parameters > Tools > Reset to vehicle's configuration defaults.
* Reboot Vehicle
* Calibrate sensors as required
{% endtab %}
{% endtabs %}

<figure><img src="../../.gitbook/assets/Screenshot 2024-03-29 at 12.13.19 PM.png" alt=""><figcaption></figcaption></figure>

##
