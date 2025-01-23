---
description: How to fine-tune the gimbal pointing controls
---

# Precise Gimbal Control

## Tilt Control&#x20;

The payload's tilt rate scales with zoom. This means that as the digital zoom level is increased, the gimbal's tilt rate will decrease to provide pointing control.

{% hint style="info" %}
The overall gimbal tilt speed (slow/med/fast) can be adjusted under the camera settings.&#x20;
{% endhint %}

## Yaw/Pan Control

By default, the aircraft's yaw control is unaffected by the camera's zoom level; however, zoom rate scaling can also be applied to yaw/pan through Slow Speed Mode.&#x20;

For even more control, the global yaw rate of Astro can also be adjusted if desired. The default global yaw rate of Astro is 75 degrees/second.&#x20;

* The max yaw rate can be adjusted by going to Advanced Mode (tap the AMC logo in the upper left-hand corner seven times). Then click on the Auterion logo again and click through Vehicle Setup -> Parameter -> MPC\_MAN\_Y\_MAX. The units are in degrees/second.&#x20;

{% hint style="danger" %}
Be careful when changing parameters, and double-check what you are doing. Changing the wrong parameter can cause unexpected behavior or even a crash!
{% endhint %}

### Slow Speed Mode&#x20;

<figure><img src="../../../.gitbook/assets/slow speed mode.jpg" alt=""><figcaption></figcaption></figure>

Slow Speed mode is a togglable flight mode that affects the sensitivity of the aircraft's yaw when the camera is zoomed in.&#x20;

* Slow Speed mode can be toggled on and off when Astro is in Position mode. It's active when the icon is lit, and you view the video stream.
  * Slow Speed mode will automatically deactivate when viewing the IR stream&#x20;
  * Slow Speed mode is turned off by default

{% hint style="info" %}
Only the aircraft's yaw speed is affected, not the maximum translational/vertical speed of the aircraft.
{% endhint %}

