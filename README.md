# MarlinFirmwareEnder3Pro
v4.2.7


/*
1st if your 4.2.7 board will not flash at all reformat and select FULL REFORMAT instead of quick. Should take 3-5 minutes and solved my hour and a half problem of testing different released versions built by others. Now I'm in the rabit hole and went through the whole firmware; twas worth it. 

Also if you use my config files the image for the loading screen will be of me and my dog jsaing, but easily changable by downloading any of the default marlin printer configs and copying over my bootscreen and status screen configs prior to building in visual studio code with platformio and auto build marlin (downloaded extensions) .bin on sd to flash printer firmware.
*/




Previously configured E3Pro V4.2.7 board firmware with bltouch creality version

Wiped and manually went through since standard firmware from creality was producing a bltouch error: error Details below
{
Start print via octoprint connected to rasberry pi/ usb a to usb b port
Nozzle heats up/Bed heats up successfully
Homes z and y axis successfully
Centers xy then z probe successfully lowers and configures height
Heads to xy 0,0
Yeets to x 300ish greater than bed max and Extruder proceeds to extrude at max until cancelling print
This occurs 1 out of every 5ish prints.
}
My guess is build plate dimensions are being lost after z probe 

Enabled safe homing and only z probe when x and y current coords are known to hopefully resolve

Untested; testing next weekend when I have a sliver of time :)



Next error is with the touch display that came with the printer. Does not connect when connected via octoprint/marlin. Display works buttons work can detect sd connections just doesnt connect to v4.2.7 board

Basic e3 nontouch display works from different printer; and has been trusty for 5 years
