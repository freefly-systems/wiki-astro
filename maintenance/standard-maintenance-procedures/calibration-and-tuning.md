# Calibration and Tuning

## Sensor Calibration

It is not necessary to perform calibrations as a matter of course. Often a calibration will not be required even if the aircraft is relocated a long distance (e.g. by air travel). Compass handling in particular has been improved as compared to past PX4 implementations. For example, shortly after takeoff, the aircraft automatically performs a compass calibration. \
\
In general, sensor calibration should be unnecessary. There are times when it may be required:

* If the magnetic field strength in the operating area is significantly different than where it was calibrated.  If the aircraft appears to have the wrong heading on the ground, makes a large move after takeoff, or flies crooked for a few seconds, those are indicators you should do a compass calibration.
* If the drone has a significant ferrous or magnetic payload installed, it may be required to perform calibration with the payload installed to improve performance.
* If the operating temperature is very hot or cold, it may be required to do a gyro and accelerometer calibration to get best performance. In those cases, power on the aircraft and allow it to sit for 10 minutes in ambient conditions to allow the electronics to warm up, then do gyro and accel cal as directed by AMC. A warning about high accelerometer bias is an indication to do this.
* after doing a full parameter reset, it is usually wise to recalibrate.

Use AMC to calibrate the sensors. [See AMC docs](https://docs.auterion.com/vehicle-operation/settings-and-maintenance/compass-calibration) for the GUI details.

{% hint style="warning" %}
While performing an Accelerometer Calibration, it is best to fold the arms of the Astro and set it down in each orientation. Accelerometer calibration may result in issues if done without placing the drone on a flat surface.&#x20;
{% endhint %}

{% hint style="info" %}
After recalibrating any sensor, make sure to restart Astro before flying. Some changes may not take effect until you reboot the drone.&#x20;
{% endhint %}

## Magnetic Interference

In the event of magnetic interference preventing the aircraft from taking off, follow these [pro-tips](https://freefly.gitbook.io/astro-public/astro/pilots-operating-handbook/limitations#magnetic-interference).

## Tuning

Astro is pre-tuned by Freefly, and can be flown without changes.

{% hint style="warning" %}
We recommend against changing low-level control parameters. Changes there could cause instability or control issues which could result in a crash.
{% endhint %}

{% hint style="info" %}
[Loading default parameters](../software-release-notes/software.md#reset-to-default-astro-parameters) or known-good presets will allow you to quickly return Astro to a functional and safe state if there is ever uncertainty about changes to the tuning properties.
{% endhint %}

Changing low-level parameters requires activating [AMC Advanced Mode](https://freefly.gitbook.io/astro-public/astro/pilots-operating-handbook/software/auterion-mission-control/amc-vehicle-setup/advanced-vehicle-setup#activating-advanced-mode). Then, navigate to Vehicle Setup > Parameters.
