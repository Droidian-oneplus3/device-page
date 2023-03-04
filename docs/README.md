## Features & Usability

|                               	|    	 |                                  	|    	 |                      	|   	 |
|-------------------------------	|----- |----------------------------------	|----- |----------------------	|----- |
| Manual brightnes              	|  ✅ 	| Battery lifetime > 24h from 100% 	 |  ❔  | Automatic brightness   |  ✖️  |
| No reboot needed for 1 week    	|  ✅	| Fingerprint reader  	             | ✖️✖️ | Waydroid		           |  ✅  |
| Torchlight                    	| ✅✖️	| Boot into UI                     	 |  ✅  | GPS                 	  | ✖️✖️ |
| Vibration                     	|  ✅ 	| Hardware video playback          	 |  ❔  | Proximity          	  |  ✅ 	|
| Flashlight                    	|  ✖️  | Anbox patches                    	|  ✅ 	| Rotation            	 |  ✅  |
| Photo                         	|  ✖️	 | AppArmor patches                 	|  ✅ 	| Touchscreen          	 |  ✅  |
| Video                         	|  ✖️	 | Battery percentage               	|  ✅ 	| Earphones           	 |  ✅  |
| Switching between cameras     	|  ✖️	 | Offline charging                 	| ✅✖️	| Loudspeaker          	 |  ✅	 |
| Dual SIM functionality        	| ✖️✖️ | Online charging                  	|  ✅ 	| Microphone          	 |  ✅	 |
| Carrier info, signal strength 	|  ✅ 	| SD card detection and access     	 |  ✅  | Volume control       	|  ✅ 	|
| Data connection               	|  ✅ 	| RTC time                         	 |  ✅  | Pin unlock           	|  ✅ 	|
| Incoming, outgoing calls      	|  ✅ 	| Shutdown / Reboot                	 |  ✅  | ADB access          	  | ✖️✖️ |
| MMS in, out                   	|  ❔ 	| Wireless External monitor        	 | ✖️✖️	| MTP access           	 | ✖️✖️ |
| SMS in, out                    	|  ✅ 	| Bluetooth                        	 |  ✅  | WiFi			              |  ✅	|
| Change audio routings          	|  ✅	| Flight mode                      	 | ✅✖️ | Hotspot		            |  ✅	|
| Voice in calls                	|  ✅ 	|

- **✅** *Confirmed working.*
- **✅✖️** *Working to some extent but with issues.*
- **✖️** *Not Working.*
- **❔** *Not tested.*
- **✖️✖️** *Global issue.*

## Requirements
- Treblize your device:
  - Instructions here: https://forum.xda-developers.com/t/treble-unofficial-lineageos-16-0-treble-for-oneplus-3-3t.3830455/
  - After you have installed the custom twrp and you have a /vendor partition, install the custom LineageOS 16 build from the guide.
  - With LineageOS 16 installed, reboot and verify that everything works. Then reboot back into TWRP.
  - In TWRP, go `Wipe` -> `Advanced Wipe` -> Select everything except `Vendor` and `USB-OTG`, then `Swipe to Wipe`.
- Reboot into fastboot

## Files
- Download the latest fastbootable image: [droidian-UNOFFICIAL-phosh-phone-oneplus_oneplus3-api28-arm64-nightly_XXXXXXXX.zip](https://github.com/droidian-oneplus3/droidian-images/releases/tag/nightly).

## Installation
* Extract the archive
* run the `flash_all` script
* Boot to fastboot and let the script flash everything.

## UBports Installer
- Alternatively the UBports installer can also be used to install Droidian.

## Notes
- The default password is `1234`.

## Bugs
- <s>Encryption is broken and it will soft brick the device.</s> Hasn't been tested on the OnePlus 3
- After entering a pin code to unlock your SIM card, you need to restart the Settings application to get access to the settings because the menu doesn't update automatically.
- Mobile data needs an APN to be set up from Settings -> Mobile Network -> Acess Point Names. See from https://apn.how
- If you get an empty Access Points window even after you have entered the info, ofono is not working properly. Run `sudo systemctl restart ofono.service` to solve the issue.
- Mobile data might stop working after making or recieving phone calls. Toggle Mobile Data from the settins off/on.
- Dual SIM functionality is currently not implemented in Phosh so only one SIM works at the moment.
- When powered off, plugging in a charger will power on the device. If you experience a flashing screen, reboot to solve the issue. If the phone is powered on manually or rebooted, there won't be any screen flashing.
- Torch/Flashlight only works properly inside Waydroid
- Camera doesn't work in Droidian or Waydroid.

## Final notes
- I'm not responsible for bricked devices, dead SD cards, thermonuclear war, or you getting fired because the alarm app failed.
- Please do some research if you have any concerns about features included in the products you find here before flashing it!
- YOU are choosing to make these modifications, and if you point the finger at me for messing up your device, I will laugh at you.

# Support
- Droidian telegram group: [@DroidianLinux](https://t.me/DroidianLinux).
