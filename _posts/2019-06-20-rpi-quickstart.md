RaspberryPI: From nothing to up and running

This tutorial tries to take you through setup and using an RPi from scratch. All you need is that you've bought an RPi and have an internet connection.

## Introduction to the RPi
I've often come across the question, when do I need an RPi? You'll often need an RPi if you need a decent amount of portable processing. This is usually for complicated tasks like Machine Learning, Image Processing, running a server, etc. I've had mentees use RPi for various combinations of these too.

## What's so great about an RPi?
RPi is widely used for a variety of reasons:
* Requirement of portable, high processing power.
* You can load an OS onto the system. It truly is the credit-card sized mini-computer.
* Lots of support in the form of an active online community. RPi supports multiple popular operating systems too (eg. Ubuntu, Debian). This extends to support for multiple programming languages, which support operations on GPIO of RPi including Python and C/C++.
* Multiple plugin-like attachments, incuding a camera(RaspiCam). Support for multiple USB devices like a keyboard/mouse

## Setting Up
### Requirements
***Basic Setup***:RPi, MicroUSB attachment(to power RPi), a microSD card(below 64GB, recommended 16GB), MicroSD Card Reader, A WiFi Router or Ethernet Cable.
***Easy Setup***:RPi, MicroUSB attachment(to power RPi), a microSD card(below 64GB, recommended 16GB), MicroSD Card Reader, A WiFi Router or Ethernet Cable, HDMI Cable, Monitor with support, Keyboard+Mouse(Could do with one of the two, not very sure).
[You should read this page before buying anything.][1]

### First Steps
First thing to do is choose an OS. The most logical choice for the same is the Raspbian OS. Note that, Raspbian with Pixel DE(Desktop Environment) is the one that packs the User Interface, the other has only a terminal. If you are a complete n00b maybe you should download NOOBS. We start with burning an image file on the SD card. Crystal clear instructions are given at [this link][2].

### Connecting to the RPi
So we have an OS on the RPi. Now what? 

<center><i id="scrollTo" class="fa fa-circle-o-notch fa-spin" style="font-size:24px"></i></center>

[1]: https://www.raspberrypi.org/documentation/setup/
[2]: https://www.raspberrypi.org/documentation/installation/
