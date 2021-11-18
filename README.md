# Ubuntu-Liquid-Coolers
Ubuntu-Liquid-Coolers

-------


## How to control a NZXT Kraken from Linux, with a GUI!
https://medium.com/@leinardi/how-to-control-a-nzxt-kraken-from-linux-with-a-gui-93367113f2f5

### These are the most common CLI(Command Line Interface) tools:
- camctl: https://github.com/leaty/camctl
- krakenx: https://github.com/KsenijaS/krakenx
- leviathan: https://github.com/brkalmar/leviathan
- liquidctl：https://github.com/liquidctl/liquidctl

These tools allow you to interact and control the Kraken from a terminal

## nzxt
https://web--proxy.herokuapp.com/https/github.com/topics/nzxt

Here are 14 public repositories matching this topic...

-------
-------

# YouTube

## Liquid cooling Ryzen 5950x, let's pkg & test some open source for Linux!
https://www.youtube.com/watch?v=sK3YdwehwIk

More Bits inside by René Rebe

#liquid #cooling #aio #liquidctl #Linux! #Ad: Single Board Computer & more @Amazon: https://services.exactcode.de/amzn.cg... 

You can support my work at: https://patreon.com/renerebe

https://exactcode.com https://t2sde.org https://rene.rebe.de

-------

## All In One (AIO) Liquid coolers work great on Linux (Corsair 100i pro)
https://www.youtube.com/watch?v=l8L3FbJh8fw


Hex DSL

Patreon: https://www.patreon.com/hexdsl

https://github.com/audiohacked/OpenCorsairLink

https://github.com/liquidctl/liquidctl


-------

## How To Control AIO Water Cooler on Linux | LiquidCTL Tutorial
https://www.youtube.com/watch?v=8Fmv5gM-5Vo

Zaney

- Patreon - https://www.patreon.com/akazaney
- Dotfiles - https://www.gitlab.com/Zaney/dotfiles​​​
- Discord - https://discord.gg/2cRdBs8

- LiquidCTL - https://github.com/liquidctl/liquidctl

So are you switching over to Linux or a FOSS enthusiast with an AIO water cooler. 

You thought you needed Windows to control your water cooler?.. 

Ok I am just going to stop.. 

Liquidctl is a great program for controlling your pump speed, fan speed, and rgb water cooling setup on Linux. 

Enjoy!


-------

## HiveOS Water Pump and Chassis Fan Control with NZXT
https://www.youtube.com/watch?v=gD10_LhWBbo


Philip D'Ath

I have a rig with a pair of water-cooled NVidia RTX 3090's with a Gigabyte B560M motherboard.

HiveOS on Ubuntu 18 does not support the motherboard fan headers, and I need those to control the water pump and the radiator fans.

I manage to come up with a solution of using an NZXT RGB & Fan Controller which attaches to a USB header on the motherboard, and some software called liquidctl.

https://github.com/liquidctl/liquidctl

- The steps listed in the video are:
      Prevent the system from mining while we are changing the cooling so we don't hurt anything.
      miner stop

- Change to using Python3 by default:
      update-alternatives --install /usr/bin/python python /usr/bin/python3 1

- Install liquidctl
      apt install python3-dev libusb-1.0-0-dev libudev-dev
      pip3 install liquidctl

- See what liquidctl can see
      liquidctl list
      liquidctl status

- Initialize all controllers and try and set fan1 to 50% as a test
      liquidctl initialize all
      liquidctl --match NZXT set fan1 speed 50

- Configure the fan control to run at system boot
      vi /etc/systemd/system/liquidcfg.service

### [Unit]
      Description=AIO startup service

### [Service]
      Type=oneshot
      ExecStart=/usr/local/bin/liquidctl initialize all
      ExecStart=/usr/local/bin/liquidctl --match NZXT set fan1 speed 50
      ExecStart=/usr/local/bin/liquidctl --match NZXT set fan2 speed 90
      ExecStart=/usr/local/bin/liquidctl --match NZXT set fan3 speed 90

### [Install]
      WantedBy=default.target


- Tell the system to load info about the services configured on the system
      systemctl daemon-reload
- Manually start the server we configured
      systemctl start liquidcfg
- Tell the system to run it at system boot
      systemctl enable liquidcfg

------

## GKraken: control the NZXT Kraken from Linux, with a GUI!
https://www.youtube.com/watch?v=tGY5EMKNRjU


Roberto Leinardi

GUI that allows to control cooling (and soon lighting) of NZXT Kraken X (X42, X52, X62 or X72) pumps from Linux

More information available here: https://gitlab.com/leinardi/gkraken



-------
-------

# Blogs

## lm-sensors
https://kaworu.jpn.org/ubuntu/lm-sensors


-------

## liquidctl – liquid cooler control Cross-platform tool and drivers for liquid coolers and other devices
## liquidctl – liquid cooler control
https://pythonrepo.com/repo/liquidctl-liquidctl-python-command-line-tools








-------


## How can I tell from within Ubuntu if my liquid cooling system is pumping?
https://askubuntu.com/questions/553425/how-can-i-tell-from-within-ubuntu-if-my-liquid-cooling-system-is-pumping


-------

## Support for NZXT Kraken X53, X63 and X73 #78
https://github.com/liquidctl/liquidctl/issues/78


-------

## Replacing NZXT’s CAM software on Windows for Kraken
https://codecalamity.com/tag/python/page/3/

Code Calamity

- Install liquidctl
- Using liquidctl


-------

## Installing liquidctl on 20.1
https://www.reddit.com/r/linuxmint/comments/le8oqa/installing_liquidctl_on_201/

-------

## liquidctl Linux
https://furamon.work/post/2021/05/liquidctl/


GitHub - liquidctl/liquidctl: Cross-platform CLI and Python drivers for AIO liquid coolers and other devices
https://github.com/liquidctl/liquidctl



-------

## How to control a NZXT Kraken from Linux, with a GUI!
https://medium.com/@leinardi/how-to-control-a-nzxt-kraken-from-linux-with-a-gui-93367113f2f5

Roberto Leinardi




-------
-------


