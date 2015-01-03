munin-dht22
===========

Munin Plugin for monitoring the DHT series of humidity and temperature sensors on a Raspberry Pi


Dependencies
---

The following python library is required:
https://github.com/adafruit/Adafruit_Python_DHT

Installation
---
Install Adafruit_Python_DHT

Copy files somewhere

````
sudo cp dht22* /usr/local/share/munin/plugins
````

Link Plugins

````
cd /etc/munin/plugins
sudo ln -s /usr/local/share/munin/plugins/dht22
sudo ln -s /usr/local/share/munin/plugins/dht22_humidity
sudo ln -s /usr/local/share/munin/plugins/dht22_temperature
````

possibly you have to change the type of the sensor or the connected pin, 
change the code (and see Adafruit_Python_DHT)


Create config file (/etc/munin/plugin-conf.d/dht):
````
[dht22]
user root

[dht22_temperature]
user root

[dht22_humidity]
user root
```

Restart munin
````
sudo /etc/init.d/munin-node restart
````