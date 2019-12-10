---
layout: post
title:  "Home Lab Part 2: Purchase & First Steps"
date:   2019-12-09
description: How I am setting up a home lab, and how you can too
categories: homelab
---

I was able to purchase a nice existing setup at what I think was a good price!  I will walk through all the equipment I got and my first steps in getting it setup.

## Craigslist FTW!

I was able to pick up a pretty complete home lab setup for $1,000USD on craigslist recently.

It included:

- [Tripp Lite 24U SmartRack Enclosure](https://tripplite.com/24u-smartrack-deep-rack-enclosure-cabinet~SR24UB)

  It is big for my needs, but you never know, maybe I'll fill it up. My wife and I agreed that all my tech stuff needs to fit inside it though, I cannot expand.

  ![](/assets/images/homelabpt2/cabinet.jpg)

- 2x [APC Smart-UPS SC 450VA 120V](https://www.apc.com/shop/us/en/products/APC-Smart-UPS-SC-450VA-120V-1U-Rackmount-Tower/P-SC450RM1U)

  Dusty! I'll get them cleaned up.

  ![](/assets/images/homelabpt2/UPS.jpg)

- [Dell PowerEdge R710](https://www.dell.com/downloads/global/products/pedge/r710-spec-sheet.pdf)

  This one has 64GB RAM.
  2x Intel Xeon 5600 Series Processors @ 2.27 GHz
  The iDRAC interface on this one is free / no enterprise licensing required, and it has a separate NIC for iDRAC.
  There are 6 drive bays, and I got 6 drives with the setup.

  - 1x 1TB
  - 2x 1.5TB
  - 1x 2TB
  - 2x 3TB

  This isn't great for my RAID configuration, but I'm not too worried about it, I have plenty of other storage space on the other box, and this one still has a decent amount of space. There is a 256GB SSD built in for the OS, so those drives are entirely for storage.

- [Dell PowerEdge R720](https://www.dell.com/downloads/global/products/pedge/dell-poweredge-r720-spec-sheet.pdf)

  This one has 32GB RAM.
  2x Intel Xeon 5600 Series Processors @ 2.90 GHz
  I ended up purchasing the iDRAC license for this one for ~$40USD on eBay, also has a separate NIC for iDRAC.
  There are 8 drive bays on this one, and I have 8x 3TB drives (24TB for those with a hangover).  I set this up as one large 16TB drive in a RAID6 configuration since I am going to run Linux, I can do all of the data organization in software.  This one also has a 256GB SSD built in for the OS, so those drives are entirely for storage.

- [Linksys SRW2024](https://www.amazon.com/Cisco-SRW2024-24-port-Gigabit-Switch/dp/B000701CLE)

  It's a switch, nothing fancy, and definitely no longer supported by Cisco, I plan to upgrade this at some point.

### One Other Thing

  A friend works in IT as well, and his company gave him an old HP IP KVM that they were retiring, so I have that in the rack as well.

  ![](/assets/images/homelabpt2/servers-front.jpg)

  ![](/assets/images/homelabpt2/servers-back.jpg)

## So far

At this point I have done a little bit of configuration and updating, I had to connect to the serial console on the switch to reset the password, I had to pull apart some Windows self-extracting zips to get iDRAC updated (a few critical RCEs came out last year), and I got proxmox installed on one of them.  In this post I simply wanted to layout what I got and how I got it setup.  I have a bit of work to do as far as cable management, and getting everything running and configured.  So far though, I am pretty happy with the way things are going.  This is a great start to a home lab.

It took a bit to get the the iDRAC firmware updated, I had some challenges using the Dell Repository Manager (DRM) for other firmware updates, and it took a bit to figure out resetting the password on the crusty old switch. If you are interested in hearing about how I did these random items, reach out and let me know and I can walk through it, if enough folks reach out I'll do a post on that specifically.  After that I will start to get into how I am getting [Proxmox](https://www.proxmox.com/en/) and [pfSense](https://www.pfsense.org/) configured.
