# A Smart Sensor for a "Dumb" Doorbell

The aim was to be able to detect when someone presses my cheap-and-cheerfull (dumb) $33 doorbell and then send a notification to my phone that someone's pressed the doorbell. This was especially important while the baby was sleeping to not wake her up. Theroetically this device can receive and transmit any message on 433MHz, so ceiling fans likely work too.  

## Background
I originally played around with the [RFToy](https://openthings.io/rftoy/), however found it's RF receiver to be awful, it simply couldn't detect the signal from anything more than about 5cm from the doorbell.  (I note I'm a fan of most of the rest of the "OpenSprinkler family of devices, but the RFToy was seriously let down by it's choice of antenna).  As such, I did some research into better antennas and discovered "Superheterodyne" receivers and transmitters, so strongly recommend a Superheterodyne kit for anyone wanting to do this.

## Ingredients
 - wemos d1 mini
 - Superheterodyne receiver and transmitter kit (I got mine from ebay for <$10). Make sure it matches the frequency band of your doorbell, in my case 430MHz
 - standard doorbell, it works perfectly for me with a [Swann SWHOM-DC820P](https://au.swann.com/swhom-dc820p/), available at [Bunnings for ~$35](https://www.bunnings.com.au/swann-wireless-door-chime-with-receiver_p4062536). I originally tried an ARLEC brand one, that didn't work so gave it away.
 - small breadboard, I used [this one](https://www.jaycar.com.au/small-breadboard-layout-prototyping-board/p/HP9570?gclid=Cj0KCQjw0umSBhDrARIsAH7FCodqYenrylYihAnwdhDvVWKaHqEdv6Fcirz59BYOIwHFLGXBcQuaj2caAkRPEALw_wcB)



# Wiring it up: 

Receiver
| Receiver Pin | wemos d1 mini pin|
|--|--|
| TBC | TBC |

Transmitter
| Transmitter pin | wemos d1 mini pin|
|--|--|
| TBC | TBC |

Then flashed the wemos with esphome, for the yaml, see [doorbell-sensor.yaml](/doorbell-sensor.yaml)

# Getting out RF codes ("RC Switch")

Esphome had some good guides, but effectively I watched the logs in esphome with `esphome logs doorbell-sensor.yaml` and determined what signal the doorbell was sending through. This appears to be a protocol called "RC Switch"