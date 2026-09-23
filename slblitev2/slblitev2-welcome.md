---
title: Welcome
menu_order: 1
post_status: draft
post_excerpt: General information about the SLB-LITE and SLB-EXT V2 
post_date: 2024-04-03 16:44:00
taxonomy:
    knowledgebase_cat: slblitev2-handbook
    knowledgebase_tag:
        - slblitev2
custom_fields:
    KBName: SLB-LITE / SLB-EXT V2
    basepress_post_icon: bp-caret-right
skip_file: no
featured_image: _images/_superlongboard/slb_slb-leds.jpg
---

why was slb-lite slb-ext v2 made
who is it for / not for
differences between v2 and lite
upgrades


The SLB-LITE and SLB-EXT V2 controllers are the natural evolution of the first generation SLB (superlongboard) controllers. They were designed from the ground up, using some architecture and principles that have proven to be reliable in the original SLB platform. Notable features and changes include:
Use of a modern RP2350 microcontroller with better reliability, easier flashing, and better driver support
A much more compact form factor, and robust enclosure
Modular design for expansion of IO, making controllers simpler and cheaper for those that don’t need it, and more expandable for those that do
Unified motor signal, motor power, and limit switches into one single locking connector and cable

Differences between SLB-LITE and SLB-EXT V2
Despite the name, the LITE and EXT V2 variants of the board are largely the same. Only one notable difference is the way that power is distributed though the board to the motors.

The SLB-LITE distributes power directly from a single power supply input to each of the 5 motor outputs. Motor power is switched off and on using the onboard controller power switch.

The SLB-EXT V2 distributes power through six independent input channels — five dedicated to the motor outputs, plus one for the controller’s onboard power requirements. This ensures a level of safety for reducing the maximum power through each independent output at a time, with individual circuit protection provided from the 6 channel power supply. The power supply is used to switch motor power off and on.
