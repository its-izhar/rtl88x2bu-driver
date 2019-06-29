# rtl88x2bu-driver
Linux kernel >=4.15 compatible realtek driver for RTL8812BU/RTL8822BU chipset for wifi adapters

### Last Tested:
 - Linux Kernel 4.19.* Longterm releases
 - Linux Kernel 4.15.* Longterm releases

## About
This repository contains drivers for the RTL8812BU/RTL8822BU chipset, updated to work with Linux 4.15 and above, the current kernel version for Ubuntu 18.04.1 at the time of writing.

It is based off of the Edimax EW-7822ULC driver, version 1.0.1.6, which in turn seems to be based on Realtek's 88x2BU driver version 5.1.7. The Edimax driver was downloaded from https://www.edimax.com/edimax/mw/cufiles/files/download/Driver_Utility/EW-7822ULC_Linux_Driver_1.0.1.6.zip and is also a part of the repo under zip/.

## Compatible/Tested Devices
- [Inamax AC1200 USB2.0/USB3.0 Wifi Adapter](https://www.amazon.com/Inamax-1200Mbps-Wireless-802-11ac-10-4-10-13/dp/B0773ZPKS2)
- [Edimax AC1200 Dual-Band MU-MIMO USB 2.0 Adapter (EW-7822ULC)](http://us.edimax.com/edimax/merchandise/merchandise_detail/data/edimax/us/wireless_adapters_ac1200_dual-band/ew-7822ulc/)
- [ASUS USB-AC53 Nano](https://www.asus.com/us/Networking/USB-AC53-Nano/)

#### Tested on:
- platform: x86_64
- Distro: Ubuntu 18.04.1 LTS
- Linux kernel: 4.15.0-33-generic
- Port: USB 2.0 and USB 3.0 

## Build/Install Instructions
To build:  
`make clean`  
`make -j8`  

To install:  
`sudo modprobe cfg80211`  
`sudo insmod 88x2bu.ko`  

Note: Make sure the device is unplugged before installing the driver.
