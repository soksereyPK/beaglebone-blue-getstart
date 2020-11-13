# Beaglebone-Blue-GetStart
Getting Start with Beaglebone Blue
![](https://se.mathworks.com/hardware-support/beaglebone-blue/_jcr_content/imageParsys/image.adapt.full.high.jpg/1590140118098.jpg)
# Getting Started with Beaglebone Blue
Beaglebone Blue is a linux debian base OS device that allow user player around with robotic stuff.
# Powering Up The Board
![](https://github.com/Phayuth/Beaglebone-Blue-GetStart/blob/master/BBBPower.png?raw=true)

There are 3 ways to powering the board
- 12V power jack
- Micro USB port
- 2Cells Lipo Battery\
Attention: Use ONE of the powering option mention above only. DO NOT connect two or more of the powering option which will result in SHORT CIRCUIT and RUIN the Board.
## Update BBB debian
BBB can be run from 2 storage sources: SD Card and eMMC (embedded Mutli Media Card)(storage that directly solder onto board).\
Out of the box, BBB already has a pre-installed debian OS where user can easily use it right away. In a condition where we need to update the debian, we can follow the instruction below.
#### Images Download
Make sure to get the right version of the Image. Some application isn't backward compatible.\
For example MATLAB 2019b require Debian 9.5 IOT
Follow the link to the Image download site and Choose the debian version that is suitble for your need. https://beagleboard.org/latest-images \
There are 2 type of Image file:
- String of Name of the Image _{ex: Debian 9.5 2018-10-07 4GB SD IoT}_ is type of the Image that allow the BBB directly boot from the SD card
- String of Name of the Image with eMMC flasher _{ex: Debian 9.5 2018-10-07 4GB SD IoT eMMC flasher}_ is type of the Image that require the BBB to flash the eMMC before use
#### Flash Image eMMC flasher
- Download BalenaEtcher https://www.balena.io/etcher/
- Flash the downloaded Image to the SD card using BalenaEtcher
- Put SD card into the BBB card slot
- Hold SD button on the BBB while connect it to the PC
- Wait until the LED flashing then release the SD button
- When new storage appear on the PC, the BBB is ready to use
#### Flash Image non eMMC flasher
Follow the precedure from Flash Image eMMC flasher section
- Connect to the BBB via browser Cloud9 IDE address : 192.168. 7.2:3000
- Navigate to /opt/scripts/tools/eMMC
```
$ cd
$ cd opt/scripts/tools/eMMC
```
Execute init-eMMC-flasher-v3.sh
```
$ sudo ./init-eMMC-flasher-v3.sh
```
BBB will start to go in to flashing mode. Do not disconnect the power.\
Wait until the LED completely shutdown then unplug the power and replug back in.
#### Connect BBB to WIFI
On Terminal Cloud9 IDE
```
$ connmanctl
$ tether wifi off
$ enable wifi
$ scan wifi
$ services
$ agent on
$ connect {wifi name ex:wifi_f45eab_.................}
$ password
$ exit
```
#### All set. Let get start to play arround with the board.
