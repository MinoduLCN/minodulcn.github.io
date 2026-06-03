---
layout: page
title: RPI Setup
---

## Installation Instructions

This will guide you through the setup process of the Minodu LCN on the Raspberry Pi

### Requirements

* You need a raspberry pi 4 or 5
* you need an ethernet adapter and a cable
* you need a sd card reader and an sd card with a minimum size if 64gb.
* you need python to be installed on your computer

### Setup Raspberry Pi Image

* install Raspberry Pi OS Lite (64 bit) on Raspberry Pi. *Tested with this version: https://downloads.raspberrypi.com/raspios_lite_arm64/images/raspios_lite_arm64-2026-04-21/*. You can use [Raspberry PI Imager](https://www.raspberrypi.com/software/) to crate the Image
* set the hostname to minodupi.local, the username to pi and enable ssh in the custom settings of the image
* once the image is written, insert the sd card into the pi
* connect via ethernet cable to raspberry pi and enable internet Sharing on mac, alternativly, you can plug the raspberry pi into your dhcp router via ethernet
* * make sure `ping minodupi.local` returns an answer, meaning your machine can discover the raspberry pi in the network

### Install MinoduLCN on the raspberry pi

* download the minodu installer with `curl -L https://github.com/MinoduLCN/minodu-installer/archive/refs/heads/main.zip -o repo.zip && unzip repo.zip`
* open a terminal and run:
  ```
  cd minodu-installer-main
  pip install pyinfra
  # run install script (adapt password if you used another one) 
  pyinfra @ssh/minodupi.local deploy.py -v --ssh-user="pi" --ssh-password="raspberry"
  # or
  pyinfra @ssh/<ip-adress> deploy.py -v --ssh-user="pi" --ssh-password="raspberry"
  ```
* follow the instructions and wait until the installer is done

  
## Troubleshooting

* Make sure raspberrpi is reachable with `ping minodupi.local`. If not. reinstall image and make sure to set the hostname to minodupi.local
* make sure there is a user on the raspberry pi with the name *pi* (standard username).
* Make sure ssh is enabled, test with `ssh pi@minodupi.local`. Default password is *raspberry*. If it is not working reinstall image and enable ssh access.
* Make sure your computer is connected to the internet during the install procedure.
