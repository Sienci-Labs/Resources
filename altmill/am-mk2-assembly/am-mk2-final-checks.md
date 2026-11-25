---
title: 11. Final Checks
menu_order: 12
post_status: publish
post_excerpt:
taxonomy:
    knowledgebase_cat: am-mk2-assembly
    knowledgebase_tag:
custom_fields:
    KBName: AltMill CNC
    basepress_post_icon: bp-caret-right
skip_file: no
featured_image:
---

We’re sure you’re itching to start cutting! Before you begin making chips fly, we recommend going through these final checks to ensure you are set up for success.

<a id="mechanical"></a>

### Mechanical

- All screws in the [table frame](https://resources.sienci.com/view/am-mk2-table-setup/) have been tightened
  - End plates with T-nuts
  - End plates to Y rails
  - Crossbeams to Y rails
  - Levelling feet
  - Legs to frame

<div markdown="1" style="width: 562px; max-width: 100%; margin-left: auto; margin-right: auto;">

![](/_images/_am/_assembly/am_assembly_table-setup-header-850x563.jpg){.aligncenter}

</div>

<p style="text-align: center;"><em>Table assembly</em></p>

- All [couplers](https://resources.sienci.com/view/am-mk2-motors/) are secure on both the motor-shaft and ball-screw sides. For factory-fitted couplers, this is an inspection check, not an instruction to remove or refit them. Confirm the rear end plates are secured after the motor-installation sequence is complete.

<a id="electrical"></a>

### Electrical

- Motor DIP switch positions are correct for each axis

<div markdown="1" style="width: 413px; max-width: 100%; margin-left: auto; margin-right: auto;">

![](/_images/_am/_assembly/am_assembly_altmill-dip-switch-position.jpg){.aligncenter}

</div>

<p style="text-align: center;"><em>X and Y-axis motor, from 1-5: OFF, OFF, OFF, ON, ON</em></p>

<div markdown="1" style="width: 485px; max-width: 100%; margin-left: auto; margin-right: auto;">

![](/_images/_am/_assembly/am_assembly_z-axis-dip-switch-e1722518120724.jpg){.aligncenter}

</div>

<p style="text-align: center;"><em>Z-axis motor, from 1-5: OFF, OFF, ON, ON, ON</em></p>

- Motor cable wires are not frayed or detached from connectors
  - If they are simply detached, you can use a small screwdriver to press each orange spring terminal release to insert the wire back in
- Inductive sensors are functional
  - Check by putting a metal object near the blue sensor face and see if a small red light triggers on the back
<!-- Q-POWER-01: Confirm approved kit-specific electrical requirements; a universal 15A spindle-circuit claim is not retained. -->- The spindle VFD is connected to a separate circuit from the SLB-EXT controller, with the voltage and current capacity required by the specific spindle/VFD kit.

<a id="software"></a>

### Software

- You are using [gSender version 1.4.12 or newer](https://sienci.com/gSender/)
- grblHAL is selected upon [startup and connection to machine](https://resources.sienci.com/view/am-mk2-first-movements/) (for gSender 1.4.12 and lower)

<div markdown="1" style="width: 861px; max-width: 100%; margin-left: auto; margin-right: auto;">

![](/_images/_am/_assembly/am_assembly_slb-up-p49-grblhal.jpg){.size-full .aligncenter}

</div>

- Alarm 10 can be cleared after pressing and releasing the E-stop button
  - If E-stop is unresponsive, check the connections: unplug the E-stop cable, then use a screwdriver to remove the 3 screws at the bottom of the unit

<div markdown="1" style="width: 905px; max-width: 100%; margin-left: auto; margin-right: auto;">

![](/_images/_am/_assembly/am_assembly_alarm-10-unlock-machine.jpg){.aligncenter}

</div>

- Machine can move in the X, Y and Z directions smoothly using the jog control buttons
- Spindle can [spin up](https://resources.sienci.com/view/am-mk2-spindle-kit-setup/) to speed, without alarms or errors, using the CW or Forward button

<div markdown="1" style="width: 850px; max-width: 100%; margin-left: auto; margin-right: auto;">

![](/_images/_am/_assembly/am_assembly_spindlelaser-gsender-edge-850x478.jpg){.size-medium .aligncenter}

</div>

<p style="text-align: center;"><em>gSender 1.5.10 and above</em></p>

<div markdown="1" style="width: 823px; max-width: 100%; margin-left: auto; margin-right: auto;">

![](/_images/_am/_assembly/am_assembly_spindlefirstrungsender-scaled-e1720724342280.jpg){.aligncenter}

</div>

<p style="text-align: center;"><em>gSender 1.4.12 and lower</em></p>

- Machine is able to successfully home without alarms or errors
  - Jog the machine **away** from the X, Y and Z sensors
  - Then press “Home”
  - If you encounter alarms or errors see this [troubleshooting page](https://resources.sienci.com/view/am-troubleshooting-homing-and-machine-limits/)

<div markdown="1" style="width: 487px; max-width: 100%;">

![](/_images/_am/_assembly/am_assembly_homing-gif.jpg){.alignnone}

</div>

<div markdown="1" style="width: 488px; max-width: 100%;">

![](/_images/_am/_assembly/am_assembly_homingaltmillresize.jpg){.alignnone}

</div>

<p style="text-align: center;"><em>Default homing at back left corner on AltMill</em></p>

If you have gone through the checks above, then you are ready to start cutting!

<a id="whats-next"></a>

### **What’s next?**

You can use this [pre-flight checklist](https://resources.sienci.com/view/am-cnc-preflight-checklist/) to prepare for each job you do.

Then, follow along this video as Ben goes through the steps to successfully carve a simple, first project.

<iframe allow="accelerometer; autoplay; clipboard-write; encrypted-media; gyroscope; picture-in-picture; web-share" allowfullscreen="" frameborder="0" height="675" loading="lazy" referrerpolicy="strict-origin-when-cross-origin" src="https://www.youtube.com/embed/xbVuRSMwJcI?feature=oembed&amp;enablejsapi=1&amp;origin=https://resources.sienci.com" title="How to Make Your First Carve on the AltMill CNC | AltMill Beginner Series" width="1200"></iframe>

- Learn how to [maintain your AltMill](https://resources.sienci.com/view/am-maintenance/)
- Understand how to [use and maintain your spindle](https://resources.sienci.com/view/spindlevfd-quickstart/)
