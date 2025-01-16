# Pro Tips and Limitations

It is possible to operate Astro close to the limits of performance by maintaining awareness of the performance envelope, how the aircraft behaves if the limits are exceeded, and best practices for operating in harsh environments.

This page reflects the limitations of the most current version. As the Astro platform matures, limitations are likely to change. For major changes that may affect these limitations, check the [release notes](https://freefly.gitbook.io/astro-public/products/astro/maintenance-manual/software-release-notes).



***

## Troubleshooting

Visit our [Troubleshooting Spreadsheet](https://docs.google.com/spreadsheets/d/1DXkk0BmRx9qLbjpBt2KgKYFOQhEGUTcyyQB6rOmb4ac/edit#gid=528435697) to look into additional solutions if you aren't finding what you're looking for on the wiki.&#x20;



***

## Flight Control

For all flight modes except Manual, at altitudes below 2 meters, the tilt angle is reduced to 12 degrees and vertical speed is reduced to 0.7 m/s.

The purpose is to prevent tip-overs while landing but has the side effect of reducing speed if flying below the takeoff point (e.g. surveying from a high vantage point). We are working to correct this behavior.



***

## Continuous Flight

If you have 8 SL8 batteries, 6 SL8 chargers, and electricity at the location of your flight, you can continuously charge 6 batteries at a time while flying Astro, allowing for uninterrupted flight for as long as you need. If you are flying without a payload, you will only need 6 batteries and 4 chargers.&#x20;

{% hint style="warning" %}
In hot conditions, you will likely need an additional 2 batteries, as it may take some time to cool the recently flown batteries to an acceptable charging temperature (50°C).&#x20;
{% endhint %}



***

## Radio Range and Interferences

Operating with a weak signal, whether due to interference or long range, can cause loss of link with the aircraft, which will engage failsafes. If you anticipate a weak signal situation, double-check that failsafes are set appropriately.

### Range

The range of Herelink and the Doodle radios on Astro is approximately 2 km in ideal conditions, assuming there are no interferences and the antennas are positioned correctly.

### Antenna Positioning

{% hint style="warning" %}
This is one of the simplest to miss and impact the range of the flight
{% endhint %}

#### **Pilot Pro**

Both the Doodle and Herelink radio modules on Pilot Pro use two blade antennas that are omni directional. It is important to follow these basic guidelines:

* Antennas should both point in the same direction.&#x20;
* Antennas should point towards ground or sky
* Minimize how much the antennas are getting blocked in close proximity. For instance, if you are using the Pilot Pro with the tablet in the open configuration, then pointing antennas towards ground instead of sky is usually better.

<div><figure><img src="../../.gitbook/assets/Pilot Pro_Antenna Position_002.JPG" alt=""><figcaption></figcaption></figure> <figure><img src="../../.gitbook/assets/Pilot Pro_Antenna Position_001.JPG" alt=""><figcaption></figcaption></figure></div>

#### **Herelink GCS (Legacy):**&#x20;

Herelink GCS has two types of antennas.&#x20;

* Patch antenna (with a circular disk on top) is a directional antenna and should be pointed toward the aircraft
* Other antenna is omni-directional and it should be positioned pointing towards the ground or sky

### Interferences

Range can be reduced by radio interference from other sources like wifi networks. Obstacles like trees and buildings in close proximity to the controller or Astro, as well as directly between the two, can dramatically reduce range.

### Multiple Aircraft

* Astro's Doodle radio configuration runs on dedicated peer to peer channels. In order to fly multiple Astros in the same airspace, make sure to scan channels and then set each Astro Doodle to a different channel.
* Astro's Herelink radios are channel hopping by default. 4 aircraft can fly simultaneously in the same airspace in practice. If more aircraft are present, interference can cause loss of radio link and control.
  * If using the legacy Herelink GCS, you can set each Herelink to be on a dedicated channel
  * If using the Pilot Pro with the Herelink radio, this feature is not yet available.

### High Power Radio Interference

Avoid using high-power, low-frequency radio transmitters (such as the RFD 900) mounted to Astro, as it can disrupt the normal function of the aircraft. For more information,  see this [service bulletin](https://freeflysystems.com/knowledge-base/astro-sb002-high-power-radio-astro-interference).&#x20;



***

## Environment

### Temperature

![](<../../.gitbook/assets/Screen Shot 2021-08-02 at 10.31.34.png>)

Astro can operate between -20 and 50 C. Position mode and survey flying are normal throughout the range. However, care is needed to operate at low and high temperatures.

Yellow region: Hovering and aggressive flights may give overtemp warnings. Follow the warning instructions.

Blue region: If batteries become too cold, state of charge will decline quickly and aircraft will enter Return or Land mode. Keep batteries warm, above 10 °C at takeoff, then self-heating will keep them warm.&#x20;

{% tabs %}
{% tab title="Tips for operating in hot environments" %}
At high temperatures, the limiting factors are motor and battery temperatures. AMC will display a warning if the motors or batteries become too hot. Heed the warnings! Astro operates normally in forward flight up to 15 m/s with a full payload of 1500 grams.&#x20;

Cooling air is your friend. The motors get much more cooling air in forward flight than in a hover. Overheat errors may occur when hovering because there is less airflow, or when flying aggressively because heating increases with current.

Batteries may require cooling before charging. Bring an extra set of batteries and chargers to enable continuous flying. If you connect batteries to the charger while cooling, they will automatically begin charging as soon as they have cooled sufficiently.

Keep the equipment out of prolonged direct sunlight, especially the Herelink. Herelink will shut down if it overheats, and it does not give a warning.
{% endtab %}

{% tab title="Tips for operating in cold environments" %}
At low temperatures, the battery cell temperature is the key limiting factor. When the cells themselves are below 10 °C (ambient air can be down to -20 °C), the built-in battery management system's (BMS) state of charge (SoC) algorithm has reduced accuracy. The SoC may decrease to zero suddenly. If this happens, [low battery failsafes](../emergency-procedures.md#low-battery) (RTL and Land) will be triggered, causing the aircraft to climb or descend suddenly.

These failsafes can be overridden by selecting another flight mode (override by moving the sticks is not available during a failsafe). The battery will not cut off power output in the air, however low temperatures generally reduce capacity which will reduce flight time.

If the batteries are 10 °C or warmer at the start of a flight, heating from discharge will keep them warm enough to fly.

To keep batteries warm, charge them in a heated environment and store them in an insulated container (a cooler works well)​**In rare cases propellers can experience icing, this occurs when ice begins to form on the tips and underside of the blades due to temperature and humidity. This will cause the props to become unbalanced, increasing drag and reducing lift. Flying with iced blades can be dangerous and is not advised.**
{% endtab %}
{% endtabs %}

{% hint style="info" %}
Keep the Herelink handset out of direct sunlight. It can operate at up to 50C ambient _if its plugged in for charging and in the shade._ \
\
For the best performance in hot or cold weather, we recommend charging the Herelink during use. Under very hot or cold weather Herelink's battery performance can drop quickly and can cause it to shutdown.
{% endhint %}

{% hint style="warning" %}
Herelink will shut down if the internal temperature increases over 55C, and it does not give a warning. Direct sunlight can increase the temperature of the Herelink beyond this limit very quickly.&#x20;
{% endhint %}

### Wind

Operating Astro at winds greater than 8-10m/s can be dangerous. Keep in mind that the wind speed at higher altitudes is typically much higher. In high wind, AMC will show a warning.

Flying Astro is high wind is not advised. If the wind speed is a significant fraction of [Astro's top speed](https://freefly.gitbook.io/astro-public/astro/specs-and-interfaces/performance#flight-speeds), control authority will be diminished in all flight modes.

When Astro is not flying, fold the props and install the propeller protectors. If the wind blows through open props, it can cause them to spin up dangerously.

### Rain and Dust

Astro can operate in moderate rain (approximately 3 mm per hour). [USGS has a guide (scroll to bottom)](https://water.usgs.gov/edu/activity-howmuchrain-metric.html) to help translate between forecasts like "shower" or "drizzle" to accumulation amount.

Battery connectors cannot be mated while wet or containing debris. We recommend compressed air to clean the connectors.

#### Tips for operating in Rainy and Dusty environments.

Rain in particular increases the risk of electrical malfunction because it can lead to short circuits

Dust carries a risk of mechanical malfunction because it can enter the motors and obstruct rotation.

Both of these conditions carry an increased risk of malfunction and danger. It is difficult to judge the exact amount of precipitation, and the amount can vary without warning during the course of a flight. Therefore, we recommend avoiding situations that endanger people.



***

## Voltage Mismatch

If the two batteries powering Astro have a voltage difference of more than 2.0V, a voltage mismatch error will occur. 2V is roughly a 25% difference in the batteries' states of charge.&#x20;



***

## Magnetic Interference

In a situation where there is a magnetic interference that is preventing the aircraft to figure out its heading before takeoff, you are presented with options:

* Move away from any potential sources of magnetic interference, like metal or water. In most cases, moving the Astro a few feet away will allow it to get a better magnetic reading to figure out the heading, and position mode will become available for takeoff.&#x20;
* Take off in altitude mode. Shortly after flying in altitude mode, GPS heading will be locked and you can then switch to position mode.

{% hint style="warning" %}
Be aware that flying in Altitude Mode does introduce additional risk. If the aircraft loses connection with the controller, it will not hold its horizontal position which may result in a crash if control is not re-established quickly. &#x20;
{% endhint %}



***

.
