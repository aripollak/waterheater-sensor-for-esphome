## Water pipe temperature sensor with ESPHome and Adafruit IO

This device measures the temperature of the hot water pipe coming out of my water heater and sends the data to Adafruit IO to be displayed on a chart.

### Equipment needed
* DS18B20 temperature sensor. I used [this kit](https://smile.amazon.com/gp/product/B09NVWNGLQ/) since it seemed easiest to use, but any other kit with the same sensor should work.
* [D1 mini](https://www.wemos.cc/en/latest/d1/d1_mini.html) with USB cable and charger. I chose this one because it was super cheap and relatively easy to use. Any ESP8266 device that works with ESPHome should be fine, as long as the configuration file contains the right board name.

### Hardware Setup

### Software Setup
* Clone this repository from GitHub
* [Install ESPHome](https://esphome.io/guides/installing_esphome.html).
* Copy [secrets.yaml.example](secrets.yaml.example) to `secrets.yaml` and edit it to fill in your WiFi network information and [Adafruit IO](https://io.adafruit.com/) account information.
* Run this command: `esphome run waterheater.yaml`
* Your ESP device should now be sensing temperature and sending it to Adafruit IO!
