# ADBUtil
### A small utility for enabling ADB over USB on the MG4 SE/Excite (2022-2025 models tested).

This utility solves the problem of not being able to enable ADB.  
Engineering mode has a HOST/OTG toggle but that doesn't enable adbd.


__I've been finding ADB is far more likely to conenct if the computer is connected to the USB-C port when the car starts__
If you've already connected, hold the home button on the car till the headunit reboots and it should work.

The USB-C port to the right side of the 12v power socket is the OTG port. 
The USB A port will be switch to OTG mode as well, but this hasn't been tested. 

### Restarting ADB
I've included a button to restart adbd. 
That allows you to enable Wireless ADB bypassing the firewall.  

Once ADB is connected via USB run:
> adb shell setprop service.adb.tcp.port 5556

from your computer and then press the "Restart ADB" button for the change to take effect. 

On your computer you can then run:
> adb connect MG4_IP_Address:5556
