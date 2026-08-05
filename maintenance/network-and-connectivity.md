---
icon: circle-wifi
---

# Network and Connectivity

## WiFi

This section describes the connection process for Astro's built-in wifi chip. This functionality is useful while the aircraft is on the ground, for admin and setup tasks.&#x20;

{% hint style="warning" %}
By default, Blue/NDAA Astros have WiFi and LTE disabled for DIU Blue compliance.&#x20;

For more information, see [diu-blue-suas.md](../other-user-manuals/compliance/diu-blue-suas.md "mention")
{% endhint %}

### Connect the Astro aircraft to a WiFi network

{% tabs %}
{% tab title="Video" %}
{% embed url="https://www.loom.com/share/b81f0678863947c192e09fe474aee709" %}
{% endtab %}

{% tab title="Text" %}
1. Open AMC GCU or PC. If using a PC, connect to Astro with a USB-C cable.
2. Tap on the vehicle status button at the top of the AMC screen (it will be either red, yellow, or green depending on the vehicle's status).
3. Select Connectivity.&#x20;
4. Enable Wifi and disable Hotspot Mode.&#x20;
5. Enter the Network SSID and Password for your wifi access point and select Connect.&#x20;
{% endtab %}
{% endtabs %}

### Connect to the Astro hotspot via WiFi

Astro has the ability to broadcast a WiFi hotspot so that you can connect to it wirelessly using another device, such as your phone.&#x20;

1. Open AMC. If using AMC on a desktop computer, connect to Astro with a USB-C cable.
2. Power on Astro with one battery (this prevents accidental arming for safety)
3. Tap the icon in the top-left of AMC. Navigate to Vehicle Overview > Connectivity > WiFi
4. Turn on "Hotspot Mode", which allows Astro to broadcast a WiFi network that other devices can connect to.

## LTE

If your Astro has a data SIM card installed, it can connect to an LTE network. This is used for some cloud features available in Auterion Suite, such as automatic flight upload, live video streaming, and more.

{% hint style="warning" %}
By default, Blue/NDAA Astros have WiFi and LTE disabled for DIU Blue compliance.&#x20;

For more information, see [diu-blue-suas.md](../other-user-manuals/compliance/diu-blue-suas.md "mention")
{% endhint %}

### Configure and Enable / Disable

1. [Install a SIM card](standard-maintenance-procedures/replacing-components/installing-a-sim-card.md) into Astro. Make sure to write down the SIM card number found on the card if you don't have it recorded elsewhere.&#x20;
2. Open AMC
3. Navigate to Vehicle Overview > Connectivity > LTE and enable it.
4. If you need to access the IMEI number for the vehicle to enable the SIM cards, connect to the Astro with a laptop and USB cable
   1. Power on Astro with one battery only.
   2. Connect the laptop and the Astro by plugging in a USB-C cable to the IO panel on the underside of the aircraft.
   3. Using a web browser, navigate to `10.41.1.1` to connect to your Astro's web UI.
   4.  On the bottom of the page, expand the "details" bar and scroll until you find the listed IMEI information<br>

       <figure><img src="../.gitbook/assets/image (5) (1).png" alt=""><figcaption></figcaption></figure>

### Hardware Disable

You can assure that LTE is not being used by[ removing the SIM ](https://freefly.gitbook.io/astro-public/astro/maintenance-manual/replacing-components/installing-a-sim-card#installing-a-sim-in-astro)card from Astro.&#x20;

### Frequencies and Compatibility

| Region                                | 4G LTE Bands                    | Radio Spec Sheet                                                                     |
| ------------------------------------- | ------------------------------- | ------------------------------------------------------------------------------------ |
| North America (United States, Canada) | B2, B4, B5, B13, B17            | [Sierra Wireless](https://source.sierrawireless.com/devices/hl-series/hl7519-48-88/) |
| EMEA/Australia                        | Cat-4: B1, B3, B7, B8, B20, B28 | [Sierra Wireless](https://www.sierrawireless.com/iot-modules/smart-modules/rc7620/)  |

{% hint style="warning" %}
Currently, Astro is only available with an LTE radio suitable for North American markets (USA & Canada). Additional LTE compatibility will be available in the future.
{% endhint %}

### Changing SIM / Service Provider

When switching SIM cards, try leaving the APN field blank. It should be automatically detected. If not, here are a few suggestions.

| Carrier  | APN                                 |
| -------- | ----------------------------------- |
| T-mobile | iot.tmowholesale, fast.t-mobile.com |
| Orange   | orange.m2m.spec                     |

{% hint style="info" %}
T-Mobile and Orange are tested and known working providers.&#x20;
{% endhint %}

In most cases, check the "Allow Roaming" box.

After changing the SIM, reboot both the aircraft and AMC.
