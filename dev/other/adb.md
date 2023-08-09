# ADB
1. stay connect via USB
2. connect to your WIFI network (computer and mobile device both)
3. ping DeviceIP (must be have ping to your device)
4. adb kill-server
5. `adb usb`
6. `adb tcpip 5555`
    1. unplug usb cable (as per @captain_majid 's comment)
7. `adb connect yourDeviceIP`
8. `adb devices` (must be see two device names , one of them is by deviceIP)
9. unplug USB cable

krsnarra_
kharisnarachmazaki19@gmail.com
# scrcpy
1. Download n extract to
```
C:\Users\USER\AppData\Local\Android\Sdk\platform-tools
```
2. Add environment variable if not exist with those path