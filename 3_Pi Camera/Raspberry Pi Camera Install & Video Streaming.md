# Raspberry Pi Camera Install & Video Streaming

**Hardware Requirement**
`Raspberry CSI Camera + Raspberry Pi 4B`

**Update**
If you don't update system in previous steps.
Using `sudo apt-get update` and `sudo apt-get upgrade`

**Insert Camera into Pi**
Do not connect power before inserted.

**Open Terminal & Enable Camera**
`sudo raspi-config` to open Pi's configure page
Enabled the camera and ==restart the Pi==

**Take Picture**
`raspistill -o new.jpg` Take a still picture
`xdg-open new.jpg` Open the picture with default tool

**Record Video**
`raspivid -o vv.h264 -t 10000s` Record 10s video

# Video Streaming

**Tool: [MJPG-streamer](https://github.com/jacksonliam/mjpg-streamer)**

**Prepare**
`sudo apt-get install subversion`
`sudo apt-get install libjpeg8-dev`
`sudo apt-get install imagemagick`
`sudo apt-get install libv4l-dev`
`sudo apt-get install cmake`
`sudo apt-get install git`

**Clone Project & Install**
`sudo git clone https://github.com/jacksonliam/mjpg-streamer.git`

**Compile**
`cd mjpg-streamer/mjpg-streamer-experimental`
`sudo make all`
`sudo make install`

**Start**
`./start.sh`

**Test**

* In Pi: http://raspberry-ip-address:8080/
* In Phone/PC: http://raspberry-ip-address:8080/javascript_simple.html


