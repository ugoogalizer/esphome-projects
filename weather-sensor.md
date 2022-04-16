
# Weather Station

Project to create a temperature, humidity and air pressure sensor.

Ingredients: 
 - wemos d1 mini
 - BME280 sensor (many online places try to sell you the BMP280 sensor - be careful as the BMP280 sensor does not sense humidity)
  - small breadboard, I used [this one](https://www.jaycar.com.au/small-breadboard-layout-prototyping-board/p/HP9570?gclid=Cj0KCQjw0umSBhDrARIsAH7FCodqYenrylYihAnwdhDvVWKaHqEdv6Fcirz59BYOIwHFLGXBcQuaj2caAkRPEALw_wcB)


# Wiring it up: 


| BME pin | wemos d1 mini pin|
|--|--|
| VCC | 3.3V |
| GND | GND |
| SCL | SCL (D1) |
| SDA | SDA (D2) |



Then flashed the wemos with esphome, for the yaml, see [humidity-sensor.yaml](/humidity-sensor.yaml)
