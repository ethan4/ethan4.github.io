---
layout: post
title:  "Decoding ADS-B beacons on PocketCHIP"
date:   2016-09-22 10:30:00 +1200
tags: SDR, radio
---

PocketCHIP is perfect for taking out in the field with it’s integrated keyboard, touchscreen and battery, so what better use for it than to decode ADS-B beacons from aircraft as they pass over your head?

Assuming you’ve got as far as connecting to wi-fi and you have a RTL-SDR dongle handy,

Make sure you’ve got up-to-date package index, and run updates for good measure

```
sudo apt-get update
sudo apt-get upgrade
```

Install git and then clone antirez’s repo

```
sudo apt-get install git
git clone https://github.com/antirez/dump1090
```

Move into the directory you just cloned

```
cd dump1090
```

Install the dependancies required to build dump1090, then build

```
sudo apt-get install gcc make librtlsdr0 rtl-sdr librtlsdr-dev pkg-config libusb-dev libusb-1.0–0-dev
make
```

Test. If you don’t see anything check your antenna connection and then Flightradar24 and make sure there are planes around.

```
./dump1090 —-help
./dump1090 —-interactive (for terminal output)
./dump1090 —-net (for map output viewable in a web browser)
```

Once you’re happy you’ve got it working right, get out and ideally up high with as few obstructions to the horizon as possible and do some plane spotting!

![]({{ site.url }}/assets/IMG_1089.jpg)