# candle-greenhouse
Greenhouse system using the candle smarthome controller


## TODO

 1. Get familiar with webthings.io code and candlesmarthome code and way to work
 2. Run a webthings/candle gatway without GUI
 3. Create a basic ui to replace the gateway's ui
 4. 1. Expend the point 3 into multiple subpoint
 

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
- be able to inform if the greehouse is running on battery or on main power if multiple power source are available)
- must be able to inform if low water in the barrel (so need manual filling

### Other idea:

- must be able to be added and controller from a main candle controller
- maybe take advantage of rpi zero-w or other small from factore pi?(can we host the gui outside of the controller????)
- having motion sensor to take picture of "stealer"
- having a tunnel option to have secure outside access(or proxy like candle)

# Technologie:

- Rpi (maybe small form factor)
- Zigbee (more private and reliable)
- Zigbee device
- Arduino?
- Xbee?
- using RPI to handle some motor or other stuff?
- water flow sensor
- windows sensor(open close) or pressur button when windows is closed)
- Maybe create a "crop module" who will manage humidity, watering, light etc... of a specific zone, so it will be easier to add "Zone" to the greenhouse by simply adding a module and adding device to that module

# Interface

The main idea for the interface will be to have it indepedent of the backend, so we could also includ it as an "addon" to the standard candle controller.
Maybe creating it as a full addon with independant url (candle.local/greenhouse) or somethings like that so we will focuse on only 1 addons that will serve both feature

- The interface will be based on candle controller, but mainly focused on the greenhouse management so lot of stuff will be removed/hide)
- Maybe a "gui" monitoring interface with graphic and stuff could be possible
- for better usage, we could find a way to make the gui "optional" and have it added as an addon to a standard candle addon

# Addons

The Addons will have the following feature:
- Disable main candle interface
- Disable unusefull addon(a list is to build)
- Manage is own rules outside of the standard rules engine(or use the main rule engine if we could access it from the python-addon library)
- Disaply Monitoring interface
- Add things(controller)
- Manage Alert triggered by rules(ex no external power(only on battery), water leak, etc...)
- Take/Send picture of harvest every X time
- have his own settings page
- have his own addons store(not everyone will need the same feature at the same time)
- Can manage different "crop zone"
- Can get crop data(ex crop A will have carrot, crop B tomato and systeme will be able to base his soil humidity and stuff based on the crop in it and have "harvest should be ready" alert
- Maybe the addon could provide his "own" api so it would be easier to create a Mobile application later
