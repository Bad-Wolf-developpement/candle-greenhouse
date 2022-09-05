# candle-greenhouse
Greenhouse system using the candle smarthome controller


## Idea:

Managing a greenhouse using candle controller:

### Limitation

- No electricity(so solar pannel)
- No water (so getting water from rain)
- Cold weather (maybe at some point add a heating device)
- Not always at home( so maybe open door/windows automatically
- Lazyish (so automatic sprinkler)
- Multiple power outage(so controller must be in the greenhouse
- in case of pipe broke, must have an automatic system shutdown


### Solution/Feature/Devices

- Humidity sensor
- Temperature sensor
- Automatic Sprincler
- UV LED for more "sun"
- Automatic door/windows or roof pannel auto opening
- heating device
- Controller on site(connected to wifi and all rules must be locally stored)
- Camera for picture of the harvest(pi camera?)
- solar charge management things( in V, out V, Battery %, Battery lifetime
- Alert on some condition(battery, soil to wet, etc....)
- Main valve in case of water leak
- water flow sensor to prevent water leak

### Other idea:

- must be able to be added and controller from a main candle controller
- maybe take advantage of rpi zero-w or other small from factore pi?(can we host the gui outside of the controller????)

# Technologie:

- Rpi (maybe small form factor)
- Zigbee (more private and reliable)
- Zigbee device
- Arduino?
- Xbee?
- using RPI to handle some motor or other stuff?
- water flow sensor
- windows sensor(open close) or pressur button when windows is closed)




