---
description: A fleet management web app that works with Astro out of the box
---

# Auterion Suite

![Auterion Suite Dashboard](<../../.gitbook/assets/Mouse Highlight Overlay 2022-05-18 10.19.13.png>)

### Overview

Auterion Suite is an optional, paid fleet management web app that is fully compatible with Astro. It has useful features like automatic flight log uploads, image uploads, and more. Learn more by visiting [Auterion's documentation](https://docs.auterion.com/vehicle-operation/auterion-suite-fleet-management).

Many features are available, such as:

* Managing your aircraft fleet
* Access detailed flight logs, and easily share them with Freefly Support
* Get software updates
* Cloud features like log upload, image upload, live streaming, and more.

{% hint style="info" %}
To start using Auterion Suite, you must [sign up for an account](https://docs.auterion.com/vehicle-operation/auterion-sign-up).
{% endhint %}

{% hint style="info" %}
Auterion Suite is _optional_. It will not prevent you from flying your aircraft.&#x20;

There is a free version with limited functionality. A paid subscription is required to unlock all its features. For more information on pricing and features, see below.
{% endhint %}

### Basic (Free) Plan vs. Pro Plan&#x20;

<table data-search="false"><thead><tr><th width="230.71429443359375"></th><th width="178.4935302734375">Basic (Free)</th><th width="263.15582275390625">Pro</th></tr></thead><tbody><tr><td>Price</td><td>$0</td><td><p><strong>$77</strong> per vehicle/month, billed annually</p><p>OR<br><strong>$95</strong> per vehicle/month, billed monthly</p></td></tr><tr><td>Vehicles</td><td>Up to 2</td><td>Up to 15</td></tr><tr><td>Collaboration</td><td>Up to 5 users</td><td>Up to 40 users</td></tr><tr><td>Battery Monitoring</td><td>Up to 4 batteries</td><td>Up to 100 batteries</td></tr><tr><td>Missions</td><td>Up to 5 missions</td><td>Up to 100 missions</td></tr><tr><td>Pilot Certification Management</td><td>None</td><td>Yes</td></tr><tr><td>Reporting</td><td>Yes</td><td>Yes</td></tr><tr><td>Flight Logs</td><td>Up to 7 days</td><td>Unlimited</td></tr><tr><td>Log Download</td><td>No</td><td>Yes</td></tr><tr><td>Live Streaming</td><td>No</td><td>Yes</td></tr></tbody></table>

{% hint style="info" %}
&#x20;After two vehicles, Auterion Suite's Basic plan will not allow additional vehicles to be registered. You will need to either [archive an existing vehicle](https://docs.auterion.com/vehicle-operation/auterion-suite-fleet-management/fleet-management/vehicles#archive), or purchase a Pro plan subscription.
{% endhint %}

For more plan details and updated pricing information, [contact Auterion](https://auterion.com/company/contact-us/).

### How to sign up for the Auterion Suite and Register your Astro

{% embed url="https://www.youtube.com/watch?v=3cfPFp3I17s" %}

**This video covers the workflow to register your Astro with Auterion Suite.**&#x20;

* Using a computer, connect a USB-C cable from your computer to the IO panel on the underside of the Freefly Astro.&#x20;
  * Power on the the Astro with one SL8 battery (NOTE: Using only one battery prevents the danger of accidentally arming the aircraft).&#x20;
  * **This physical connection to the Astro is required for security reasons as the Suite enables location data, live streaming, etc.**&#x20;
* Using a web browser, go to the following address to connect to the Astro: `10.41.1.1`
* This page will allow the user to sign up for the suite as well as automatically register and claim the aircraft. Click "Register Now" or scan QR code for mobile signup.
  * Note: This requires the vehicle to be online to generate a signup QR code otherwise it’ll say “internet required” for the registration prompt.
  * [Connect the Astro to the internet](../../maintenance/network-and-connectivity.md) using either a WiFi or LTE network.&#x20;
  * <div data-gb-custom-block data-tag="hint" data-style="warning" class="hint hint-warning"><p>By default, Blue/NDAA Astros have WiFi and LTE disabled for DIU Blue compliance. </p><p>For more information, see <a data-mention href="../../other-user-manuals/compliance/diu-blue-suas.md">diu-blue-suas.md</a></p></div>
  * If Astro is connected to the internet and plugged into the computer and `10.41.1.1` does not show the Register Now button, try refreshing your browser. &#x20;
* Once complete, you should see the Astro unit listed under the "Vehicles" Section on the main dashboard of the Auterion Suite.
* Go Fly!&#x20;

### Flight Logs

Astro's autopilot automatically creates log files that record the aircraft's flight path, inputs received, outputs sent, and more.

Log files are stored to aircraft's internal storage, which can be downloaded to a PC. If the Astro is configured to upload logs to Auterion Suite, you can view them any time Auterion Suite Fleet Management > Flights.&#x20;

To learn more about how to access and analyze the different log files, please see [Flight Logs](https://app.gitbook.com/s/WXREyAKYAeQJ4gfg2SPg/software/flight-logs).

#### Viewing Logs in Auterion Suite

The easiest way to view the logs is with an [Auterion Suite account](https://docs.auterion.com/vehicle-operation/auterion-sign-up) (Basic version is free).

[Navigate to a particular flight](https://docs.auterion.com/vehicle-operation/auterion-suite-fleet-management/flights) to see many plots showing data such as angles, position, speed, GPS quality, vibration, etc. It will also show the build information, parameter values, and any errors detected in the flight.&#x20;

#### Sharing Flight Logs with Support

To share an uploaded flight log from Auterion Suite, use the "Share with Manufacturer" toggle. This sends the flight log directly to Freefly support. <br>

This creates a support ticket with any information included in the log, statement on submission, and will link to the email associated with Auterion Suite. Be sure to add all relevant details to your submission.

![](<../../.gitbook/assets/image (64).png>)

### Privacy,  Data Sharing, and Security

Freefly believes data generated by Astro, including flight logs, are your property. We think it's important that you are in control of your data, are confident in the measures taken to ensure security, and agree with how the data is used.

The Auterion Privacy Policy gives a layperson's description of how data can flow from Astro, through the Suite, and to partners you choose.

Briefly, when Astro is registered with a Suite account, you can choose to have flight logs automatically uploaded from the aircraft to Auterion servers when an internet connection is available. You can review this data in your Suite account. Auterion employees do not have access to your data. You may choose to share individual flight logs with Freefly Support via the Suite, for example to troubleshoot details of a specific flight.

* Freefly and Auterion understand the need for full data control and user privacy so we have built this platform for maximum user control.
* The Astro comes with hardware to support WIFI and LTE connections to the internet or other devices.
  * If you do not want the LTE to connect, do not install a SIM card for data connection
  * If you do not want the Astro to connect to WIFI, do not select any networks or present any passwords. You can also disable WIFI on the pilot handset.&#x20;
* For security purposes the user needs to have physical access/connection to the Astro in order to register the aircraft to the Auterion Suite because the Auterion Suite enables log uploads, live unit status tracking, live video streaming etc.

{% hint style="info" %}
Learn more about the Astro's internet connections: [wifi](https://freefly.gitbook.io/astro-public/astro/pilots-operating-handbook/network-and-connectivity#wifi) and [LTE](https://freefly.gitbook.io/astro-public/astro/pilots-operating-handbook/network-and-connectivity#lte).
{% endhint %}
