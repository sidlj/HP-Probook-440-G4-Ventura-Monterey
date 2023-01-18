# HP Probook 440 G4 Hackintosh

## Configuration:
- CPU: i5-7200U
- RAM: 8GB
- WIFI: Broadcom BCM94360
- Drive: Crucial BX500 500GB SSD
- FHD Display
## What works:
- Wifi
- Bluetooth
- Intel HD 620 Graphics Acceleration
- Brightness
- Sleep
- Audio via AppleALC
- Keyboard with Volume Controls and Brightness controls
- Power Management with percentage
- Trackpad
- HDMI
- USB-C Port
## What doesn't work:
- Fingerprint sensor
## Let's Get Started
### Prepare:
- HP Probook 440 G4
- macOS Ventura or Monterey downloaded from the App Store
- at least 8GB USB stick
### Bios:
- open F10
- boot menu F9
- disabled Secure Boot
- disabled VT-d
- enabled VTx
### USB installer:
- connect the USB stick to a device running macOS (Mac or Hackintosh)
- open Disk Utility - format USB as Mac OS Extended (Journaled) and rename it to USB
- download [MacOS Monterey or Ventura from the Apple App Store.
- after download open terminal and paste:
```
sudo /Applications/Install\ macOS\ Monterey.app/Contents/Resources/createinstallmedia --volume /Volumes/USB
```
- it should take up to 30 minutes
- when its done download OpenCore Configurator (https://github.com/notiflux/OpenCore-Configurator)
- openConfigurator and mount EFI partition.
- then download [my EFI Folder](./EFI.zip)
- replace my [EFI](./EFI.zip) with original EFI on EFI partition
### Installation:
- turn on laptop and start pressing F9 key (it opens boot menu)
- select your USB stick and wait for it to boot
- select Install macOS... (use arrows and enter)
- after boot select Disk Utility
- in left corner click on "view" and select "Show All Devices"
- select your drive for Hackintosh
- format it as "APFS", scheme "GUID Partition Map"
- close Disk Utility and go to Install macOS, select your drive and continue...
- when your laptop restarts, be sure it boots to your USB stick
- continue the installation
- after installation completed, configure Hackintosh setting for your need
### Post Instalation:
- copy EFI folder fron USB to HDD/SSD
- you might have to remove -v from boot arg (Use Opencore configurator).
- reboot your laptop 

Now everything should be working

Enjoy your new hackintosh
