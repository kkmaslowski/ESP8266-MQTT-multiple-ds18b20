# mqtt_esp8266_ds1820_arduino
A simple Sketch to read the Temperature from multiple DS18B20 and publish them to a MQTT-Server using a ESP8266.
Compiles in the Arduino IDE for the ESP8266

This Sketch will connect your ESP8266 to your WIFI-AP and to a MQTT-Server. It'll loop through all DS18B20 temperature sensors connected to GPIO2 and publish their Temperature values to the MQTT-Server.

- The topic is put together from a base you define in _String romcode = "temp/";_ plus the ROM-ID of the DS18B20. 
- The Message contains the raw integer Value of the Temperature ( divide by 16 for Celsius)


Based on:

- https://github.com/esp8266/Arduino
- https://github.com/knolleary/pubsubclient
- https://gist.github.com/igrr/7f7e7973366fc01d6393
- The example Sketch for the DS18B20 from the Arduino IDE
