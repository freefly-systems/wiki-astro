# DIU Blue sUAS

## DIU Blue sUAS - Astro

The Freefly Systems Astro has been approved by the Defense Innovation Unit and was added to the [Blue sUAS List](https://www.diu.mil/blue-suas-2#AltaX). Freefly has sold a variety of different [Astro](https://store.freeflysystems.com/collections/astro) configurations, and their Blue status is listed below:

<table data-search="false"><thead><tr><th>Aircraft</th><th>Blue Compliant</th><th>Hand Controller</th><th>Radio</th></tr></thead><tbody><tr><td>Astro </td><td>N</td><td>Herelink GCS</td><td>Herelink</td></tr><tr><td>Astro</td><td>N</td><td>Pilot Pro</td><td>Herelink</td></tr><tr><td>Astro (NDAA/Blue)</td><td>Y</td><td>Pilot Pro</td><td>Doodle</td></tr><tr><td>Astro Prime</td><td>N</td><td>Pilot Pro</td><td>Herelink</td></tr><tr><td>Astro Prime (NDAA/Blue)</td><td>Y</td><td>Pilot Pro</td><td>Doodle</td></tr><tr><td><a href="https://store.freeflysystems.com/collections/astro/products/astro-max">Astro Max</a></td><td>N</td><td>Pilot Pro</td><td>Herelink</td></tr><tr><td><a href="https://store.freeflysystems.com/collections/astro/products/astro-max-ndaa-blue">Astro Max (NDAA/Blue)</a> </td><td>Y</td><td>Pilot Pro</td><td>Doodle</td></tr></tbody></table>

Part 950-00142 Astro (NDAA/Blue) Package conforms to the exact Authority to Operate (ATO) configuration approved by DIU. This aerial system consists of 3 main components: Astro, Pilot Pro, and Doodle Labs Radios.



***

## Design

The design of Astro’s Blue configuration aims to balance user flexibility with the security requirements of DIU’s Blue program. Astro can achieve Blue status through settings alone, which involves reconfiguring various systems and enabling passwords and permissions that only administrators can change. The Blue configuration is delivered fully compliant, allowing administrators to enable specific features according to their security needs.



***

## Security Features Overview

### Pilot Pro

The Samsung tablet mounted on the Pilot Pro features a multi-user concept with user and admin levels. This multi user security feature is not enabled by default, but is available for those who require it.

The tablet’s standard Android login security password, provided on a card with the vehicle, serves as the “pilot” level password. This boots the tablet into Samsung KNOX kiosk mode through the designated app. From this mode, the pilot can open AMC, the primary ground control software for the drone, while background apps communicate with the controller hardware.

Exiting the kiosk mode requires the administrator password, granting full control over the Android system. Administrators can change passwords, enable or disable wireless networks, and access the Freefly updater app to check for updates.

The RJ45 port on the back of the Pilot Pro typically connects to the drone network, enabling telemetry and video consumption and interaction with the drone. By default, this port is disabled, but the administrator can log in and reconfigure.

### Astro Local Configuration

Astro serves a webpage at https://10.41.1.1, allowing certain drone configurations like enabling LTE or WIFI, cloud services, local Mavlink streams, and more. These settings are disabled by default. An unauthenticated user can view the drone’s serial number and software versions on this page. However viewing and enabling other settings requires a login password. The administrator can enable features and remove the password.

### Logging

Logging is set to "stealth mode" by default on the Blue Astro, and is disabled on the controller, and payloads. This breaks PPK processing, and flight logs will be missing crucial information for technical support. Stealth logging can be disabled by modifying some settings as shown below.&#x20;

{% hint style="info" %}
Auterion Suite Admins can enable full logging on Astro by changing _**both**_ of the following settings:

* Connect Astro to PC with USB, login to https://10.41.1.1, go to settings, enable Cloud Services. This enables the log streaming service that is required.&#x20;
  * In the future we will make it a separate setting so they are not tied together.
* Go to AMC, and switch to [Advanced Mode](https://docs.freeflysystems.com/astro/pilots-operating-handbook/essential-software/auterion-mission-control/amc-vehicle-setup/advanced-vehicle-setup).  Go to Advanced > Parameters, then change the following parameters:
  * SDLOG\_NO\_POS\_DAT = Disabled.&#x20;
  * GPS\_DUMP\_COMM = RTCM output (PPK)
* Save the changes, and power cycle the Astro.
{% endhint %}



### External Ports

Critical auxiliary ports on Astro are disabled. The USB connector allows connection to the internal webpage (as mentioned above). The CAN port is available but only shows battery telemetry communication, serving as a non-essential bus for the aircraft. The Ethernet port on Astro’s IO panel is not electrically connected to anything.



### Firmware Updates

All bootloaders are encrypted and require the correct keys to install firmware. Firmware updates for the Pilot Pro are managed through the Freefly updater app. Accessing this application requires the administrator to exit the kiosk mode.

Astro Firmware can be downloaded from our website or the Auterion Suite. Installation requires the administrator to log in to the https://10.41.1.1 webpage via USB to access the installer tools.

Drone parameter configuration is protected by AMC. While in user mode, AMC restricts all configuration settings beyond basic pilot requirements to administrator mode.





***

## NDAA

Astro (NDAA/Blue) variant ships with very strict security requirements. Users needing an NDAA aerial system without these security features can break the ATO conformance and setup the Astro as described below. System was designed so that these features can be enabled/disabled individually as needed.

**Astro**

* Using the admin login password, connect to 10.41.1.1. Then you can enable any of the following:
  * LTE and Wifi
  * Remote ID
  * Mavlink
  * Cloud services
  * Remove the administrator feature to update firmware
  * Disable stealth logging
* Open AMC and go to advanced mode. Then you can change any of the following:
  * Enable missions to be stored and persisted on power cycle
  * Enable physical access to:
    * Mavlink and parameter access
    * TCP Mavlink port (enables access to USB and the Ethernet from the payload port on the IO Board)
    * Enable Telem 3 and Telem 4 access from the IO Board

**Pilot Pro**

* Disable Kiosk mode (if already enabled) by logging in with the Admin password
* Enable Pilot Pro App logging and Doodle radio logging
* Enable the RJ45 port on Doodle radio (enabled ethernet)



<figure><img src="../../.gitbook/assets/Screenshot 2024-07-09 at 2.42.32 PM.png" alt=""><figcaption><p>Screenshot showing the configuration interface. This example is a non Blue configuration with certain features enabled.</p></figcaption></figure>





***

## FAQ

* Does the Astro (NDAA/Blue) variant ship with Remote ID?
  * All Astro variants, including Blue/NDAA and Herelink variants ships with Remote ID enabled.
