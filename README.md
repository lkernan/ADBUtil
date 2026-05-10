#ADBUtil
###A smaull utility for enabling ADB over USB on the MG4 SE/Excite (2022-2025 models tested).

This utility solves the problem of not being able to enable ADB.  
Engineering mode has a HOST/OTG toggle but that doesn't enable adbd.

** Do not connect the USB cable until after the running the adb connect function **
If you connect it too early, the device will not be listed in "adb devices" unless you unplug and plug the cable in again. 

THe USB-C port to the right side of the 12v power socket is the OTG port. 
THe USB A port will be switch to OTG mode as well, but this hasn't been tested. 

###Restarting ADB
I've included a button to restart adbd. 
That allows you to enable Wireless ADB bypassing the firewall.  

Once ADB is connected via USB run:
> adb shell setprop service.adb.tcp.port 5556

from your computer and then press the "Restart ADB" button for the change to take effect. 
