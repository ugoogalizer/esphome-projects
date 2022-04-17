# Doorbell Sensor

The aim was to be able to detect when someone presses my cheap-and-cheerfull $30 doorbell and then send a notification to my phone. Theroetically this device can receive and transmit any message on 433MHz.  

## Background
I originally played around with the RFToy, however found it's RF receiver to be awful, it simply couldn't detect the signal from anything more than about 5cm from the doorbell.  (I note I'm a fan of most of the rest of the "OpenSprinkler family of devices, but the RFToy was seriously let down by it's choice of antenna).  As such, I did some research into better antennas and discovered "Superheterodyne" receivers and transmitters.

## Ingredients
 - wemos d1 mini
 - Superheterodyne receiver and transmitter kit (I got mine from ebay for <$10)
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

# Getting out codes

Esphome had some good guides, but effectively I watched the logs in esphome with `esphome logs doorbell-sensor.yaml` and determined what signal the doorbell was sending through.