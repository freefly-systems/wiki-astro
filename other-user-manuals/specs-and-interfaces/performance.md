# Performance

## Weight and Payload

### Maximum Gross Weight

To determine maximum gross weight, determine flight location pressure altitude and temperature, and refer to the weight in the chart below.&#x20;Gross Weight includes payload, battery and structure weight.

The maximum gross weight might exceed the weight allowed by regulatory agencies. When determining gross weight, please consider any such local restrictions on aircraft weight when planning aircraft weight.

![](<../../.gitbook/assets/altitudetable (1).png>)



| Astro Configuration           | Mass (g) | Note                               |
| ----------------------------- | -------- | ---------------------------------- |
| Maximum Takeoff Weight (MTOW) | 6,950    |                                    |
| Maximum Payload               | 1,500    |                                    |
| Unladen Weight                | 5,165    | Empty Weight + 2 SL8-Air batteries |
| Empty Weight                  | 3,095    | No batteries or payload            |

| Component                                   | Mass (g) | Note                  |
| ------------------------------------------- | -------- | --------------------- |
| SL8-Air Battery                             | 1035     | 2 required per flight |
| Vibration Isolated Cheese Plate + Isolators | 35       |                       |
| Smart Quick-Release + Isolators             | 82       |                       |

## Flight Time

### Hovering

![](<../../.gitbook/assets/image (70).png>)

### Power Consumption at Hover

![](<../../.gitbook/assets/image (104).png>)

#### Table from curve fit

| Weight (g) | Power (W) |
| ---------- | --------- |
| 5220       | 485       |
| 5460       | 523       |
| 5720       | 563       |
| 5960       | 603       |
| 6220       | 643       |
| 6460       | 685       |
| 6720       | 728       |

Flight time can change depending on several factors such as the type of flying (e.g. hover vs forward flight) and weather (wind, temperature, barometric pressure, humidity). These effects are intertwined. For example: in cold temperatures, air density is high, but less energy is available from the batteries.

Assumptions:

* These flights were performed at temperature of 13 °C and elevation of 12 meters above sea level.
* Two fully charged SL-8 Air batteries (2 \* 7.3 amp hours).
* Landing at 4% battery State of Charge remaining (e.g. default low battery failsafe settings).

## Flight Speeds

| Flight Mode | Speed (m/s)               | Climb (m/s) | Descent (m/s) |
| ----------- | ------------------------- | ----------- | ------------- |
| Position    | 15                        | 4           | 2             |
| Altitude    | no limit                  | 4           | 2             |
| Manual      | no limit                  | no limit    | no limit      |
| Mission     | 7 (default, user setting) | 4           | 2             |
| Return      | 7                         | 4           | 2             |

## Range

2 km, line-of-sight

{% hint style="info" %}
The [Limitations Section](https://freefly.gitbook.io/astro-public/astro/pilots-operating-handbook/limitations#range) contains range information along with tips for operating in harsh environments.
{% endhint %}

## Noise

The volume of the aircraft at ground level depends on several factors, including payload weight, wind speed and direction, and the background noise of the environment. The following data was gathered with an Astro in hover carrying the A7R4 camera and gimbal, tested from 5 meters to 100 meters away from the user, from 5 meters altitude to 120 meters altitude.

This data is presented in the ‘A-Weighted’ scale, which approximates the average loudness sensed by the human ear, and is used by the FAA to measure aircraft noise.

![](https://lh5.googleusercontent.com/0LHMXAUehoVi8hDHzQoHHF0WTv7pEA07lbGm7dsrvqiTHhIyj8VoOWhFu0-TWp86wgJODwXkfKxrQKyJBIJ5DoYjsMNpjDSkMRzZkefi9PndBlW2Z59aJKGHkaAoSdrHy8MkvtTCaugPbkUXJw)

In our testing, hovering and forward flight showed similar values of the ground noise produced by the aircraft.

![](https://lh5.googleusercontent.com/yBukTVlZwXaz5PnB3MR9WQIjMmPRlDYYTqu3i-5MWtX_lCxy01tvvX0SEsA7O2kcIQ0iSEUoFyHYMHvPtOl-9iipWMgixGez2-WSfwmtdjPLD1Zs5KbmV9UvcJv0R2EOlnm14PFHlA3MQhESNA)
