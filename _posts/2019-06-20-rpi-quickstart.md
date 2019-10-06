RaspberryPI: From nothing to up and running

This tutorial tries to take you through setup and using an RPi from scratch. All you need is that you've bought an RPi and have an internet connection. Actually, I recommend reading this if you're thinking of buying one, you'll see some instructions on what you need to buy so it's a good idea.

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
***Easy Setup***:RPi, MicroUSB attachment(to power RPi), a microSD card(below 64GB, recommended 16GB), MicroSD Card Reader, A WiFi Router or Ethernet Cable, HDMI Cable, Monitor with HDMI support, Keyboard+Mouse(Could do with one of the two, not very sure but prefer both).
[You should read this page before buying anything.][1]

### First Steps
First thing to do is choose an OS. If you're reading this, the most logical choice for you is the Raspbian OS (It's pretty nice, somewhat light GUI, most tutorials you find anywhere will work on Raspbian). Note that, Raspbian with Pixel DE(Desktop Environment) is the one that packs the User Interface, the other has only a terminal.
If you are a complete n00b maybe you should download NOOBS. We start with burning an image file on the SD card. Crystal clear instructions are given at [this link][2].

### Connecting your RPi to the Internet
So we have an OS on the RPi. Now what? We need to setup some sort of connection with the RPi. So here are your options:
* Easy setup: You should be super comfortable. You can just connect your RPi with an HDMI cable to the monitor, add a keyboard+mouse, and there you're done. Connect a good microUSB cable, insert the SD Card and switch the RPi's power on. It should show you something like [this][3]. Now you can use it like an OS! Connect to WiFi, scan the raspi-config for settings so you can setup whatever is appropriate for your case(don't worry it sounds intimidating but its super easy - when in doubt you can just start exploring options in the menu. There are some games in there which aren't super fun to play because of all the lag but you can try if you want! :) )
I think you're good from now on!

* Basic setup: No simple way to say this but I've failed at this method a few times. Sometimes it's because of the terrible WiFi module on the RPi(or terrible WiFi I use), sometimes I mess up, sometimes its a plain old fashioned error I can't understand how to debug because I can't see anything. Easiest thing to do would be use the easy setup once, configure your RPi, then it'll be fine to just use remote access. But if you can't access equipment, here we go!
 The crux is to get the RPi on the same local network as the PC. We can just use an ethernet cable and connect our RPi to our PCs. That is quite easy. If you don't have one read the next paragraph. Anyway with this method what you can do is do the same edits as <a href="file_edits_">here</a>, but using the terminal. Let's go over them.
 Start with your SD Card (plugged in to your PC). We need to edit some specific files in it to make the RPi connect to a wireless network and start using it. I found a decent blog post for setting up the network [here][4]. I'm not leaving you out to dry yet don't worry. BUT READ THIS LINK FIRST.
 <a name="file_edits_"> So what you can do is edit this one file at `/etc/wpa_supplicant/wpa_supplicant.conf` and what you need to do is copy this part:
{% highlight bash %}
network={
ssid="replace_with_your_ssid"
psk="replace_with_your_password"
key_mgmt=WPA-PSK
}
{% endhighlight %}
Since you are most probably using a WPA-PSK, this shouldn't be a problem. If you're not, [this][5] page can help you. Don't let it intimidate you, just find out the kind of network you have. You can even use your phone, try connecting to your WiFi and check the options it needs you to enter. Search these options and you should get a good lead. This is the hardest part but after this things should be breezy.
If you're through with this only thing left to edit is enabling ssh. SSH will enable access to your RPi remotely. You can add edit the file `/etc/rc.local` and add the following line at the end
{% highlight bash %}
/etc/init.d/ssh start
{% endhighlight %}
This starts an SSH server on your RPi on boot.
Now all you gotta do is connect to the same WiFi from your PC!

<center><i id="scrollTo" class="fa fa-circle-o-notch fa-spin" style="font-size:24px"></i></center>

[1]: https://www.raspberrypi.org/documentation/setup/
[2]: https://www.raspberrypi.org/documentation/installation/
[3]: https://youtu.be/Th_3AvK-EbM?t=273
[4]: https://howchoo.com/g/ndy1zte2yjn/how-to-set-up-wifi-on-your-raspberry-pi-without-ethernet
[5]: https://wiki.archlinux.org/index.php/WPA_supplicant
