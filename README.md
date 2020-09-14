# Beaglebone-Blue-Simulink-Jetson-Nano
Using Beaglebone Blue with Simulink & Jetson nano ROS
# Getting Started with Beaglebone Blue
Beaglebone Blue is a linux debian base OS device that allow user player around with robotic stuff.
## Update BBB debian
BBB can be run from 2 storage sources: SD Card and eMMC (embedded Mutli Media Card)(storage that directly solder onto board).\
Out of the box, BBB already has a pre-installed debian OS where user can easily use it right away. In a condition where we need to update the debian, we can follow the instruction below.
#### Images Download
Make sure to get the right version of the Image. Some application isn't backward compatible.\
For example MATLAB 2019b require Debian 9.5 IOT
Follow the link to the Image download site and Choose the debian version that is suitble for your need. https://beagleboard.org/latest-images \
There are 2 type of Image file:
- String of Name of the Image _{ex: Debian 9.5 2018-10-07 4GB SD IoT}_ is type of the Image that allow the BBB directly boot from the SD card
- String of Name of the Image with eMMC flasher _{ex: Debian 9.5 2018-10-07 4GB SD IoT eMMC flasher}_ is type of the Image that require the BBB to flash the eMMC befor use
#### Flash Image
- Download BalenaEtcher https://www.balena.io/etcher/
- Flash the downloaded Image to the SD card using BalenaEtcher
- Put SD card into the BBB card slot
- Hold SD button on the BBB while connect it to the PC
- Wait until the LED flashing then release the SD button
- When new storage appear on the PC, the BBB is ready to use
