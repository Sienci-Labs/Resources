---
title: Closed Loop Upgrade
menu_order: 10
post_status: publish
post_excerpt: How to install and setup the Closed Loop Stepper Motors Kit
post_date: 2022-03-17 20:11:00
taxonomy:
    knowledgebase_cat: lmk2-add-ons
    knowledgebase_tag:
        - mk2
custom_fields:
    KBName: LongMill MK2 CNC
    basepress_post_icon: bp-caret-right
skip_file: no
featured_image: _images/_lmmk2/_add-ons/_clsm-upgrade/lmk2_clsm_upgrade-allparts.jpg
---

Switching to the Closed Loop Stepper Motors (CLSM) from the open loop motors is easy. The main difference between the open loop and the closed loop motors is that the open loop motors lack positional feedback making them prone to “skipping steps” under load. With closed loop motors there is a feedback system that helps in monitoring their positions which enables them to self-correct errors, improve accuracy and operate more efficiently.

For a more detailed rundown on how to successfully prepare for the use of the SLB-EXT please refer to the following documentation: https://resources.sienci.com/view/am-slb-ext-controller/

## Unboxing

Your upgrade kit will include a new SLB EXT, 4 closed loop motors, 4 inductive sensors, a new 48 volt power supply and more! Check out the list below and [contact our team](https://sienci.com/contact-us/) if any parts are missing.

![](/_images/_lmmk2/_add-ons/_clsm-upgrade/lmk2_clsm_upgrade-allparts.jpg){.aligncenter .size-medium}

The following components are included in the upgrade kit and are shown together in the photo below:

- NEMA 23 Motors (x4)
- Motor Covers (x4)
- 40 mm blue aluminum standoffs (x16)
- SLB-EXT (Includes E-stop)
- 48 VDC power supply
- Larger Drag chain 18x26
- Drag chain bracket
- Drag chain holder mounts (x4)
- SLB 3D-printed rail mounts (x2)
- Inductive sensors (x4)
- Inductive sensor bracket (x2)
- Motor cable set (x1 long, x3 short)
- M5x10mm hex head screws (x2)
- M5x12mm socket head screws + washers (x10)
- Hex nut (x1)
- Nylock nuts (x2)
- M5x55mm socket head screws (x4, for dust shield addon)

## Motors

![](/_images/_lmmk2/_add-ons/_clsm-upgrade/lmk2_clsm_upgrade_title-glowpic.jpg){.aligncenter .size-medium}

This process should take approximately 2-3 hours. To begin, jog machine to the front/center of your wasteboard, and pull the table away from the wall if possible. You can also remove your router or spindle to give you a bit more room and open all of the links on your drag chains with a small flat head screwdriver to prepare for this upgrade. Let'start with the motors!

### Remove Stepper Motors

![](/_images/_lmmk2/_add-ons/_clsm-upgrade/lmk2_clsm_upgrade-header1.jpg){.aligncenter .size-full .wid}

We will be removing all 4 of the open loop motors (X-axis, Z-axis + 2 Y-axis motors) The process is the same for all 4 of the motors. We begin with the X-axis motor, on the left side of the machine.

Unplug the open loop stepper motor at the white connector. This is done by pressing on the short end of the white connector, then pulling the connection apart.

![](/_images/_lmmk2/_add-ons/_clsm-upgrade/lmk2_clsm_upgrade-connector.jpg "Here you can see the X-axis motor plug"){.aligncenter .size-medium}

Using an M5 Allen key, remove the M5-50mm bolts and set them aside. We will be using them to install the new motors. You can use a drill to speed up the process here, and if the screws are too tight, use the M5 Allen key to loosen them. You will not need to keep the aluminum spacers, replacements are in the new kit.

![](/_images/_lmmk2/_add-ons/_clsm-upgrade/lmk2_clsm_upgrade-pic1.jpg){.aligncenter .size-full}

Loosen the bolt on the coupler that is closest to the motor. This will allow you to lift each motor free from the motor shafts.

![](/_images/_lmmk2/_add-ons/_clsm-upgrade/lmk2_clsm_upgrade-loosecoupller.jpg){.aligncenter .size-medium}

Now that we've pulled the X-axis motor from the motor shaft, **proceed to do the exact same 3 steps with the Z-axis motor and both Y-axis motors.**

- Unplug connector
- Remove 4 standoffs
- Loosen coupler.

### Install the New Motors

Ok, nicely done! We will now run the process we just completed, in reverse. Grab the new closed loop motors, the blue standoffs, and the M5-50mm bolts we removed in step 2 above.

![](/_images/_lmmk2/_add-ons/_clsm-upgrade/lmk2_clsm_upgrade-header2.jpg){.aligncenter .size-full .wid}

Let's begin by sliding each M5-50mm bolt into a matching 40mm spacer.

**Note - If you are using a dust shield, use 4 M5 - 55mm socket head screws

Thread each bolt/spacer into the corresponding 4 holes to secure the motor in place. Using either a drill or an M5 allen key, tighten each spacer/bolt combo.

![](/_images/_lmmk2/_add-ons/_clsm-upgrade/lmk2_clsm_upgrade-motor-installjpg.jpg){.aligncenter .size-medium}

With the new motor shaft fully seated in the coupler, turn the coupler bolt closest to the new motor with the M5 allen key until tight.If everything has come together well so far, you should be able to now check that the lead screw can spin relatively easily.

![](/_images/_lmmk2/_add-ons/_clsm-upgrade/lmk2_clsm_upgrade-tightencoupler.jpg){.aligncenter .size-medium}

Now that we've replaced the one motor, **proceed to do the exact same 3 steps with the remaining motors.**

![](/_images/_lmmk2/_add-ons/_clsm-upgrade/lmk2_clsm_upgrade-xaxismotor.jpg "X Axis Motor"){.aligncenter .size-medium}

![](/_images/_lmmk2/_add-ons/_clsm-upgrade/lmk2_clsm_upgrade-yaxismotor1.jpg "Y Axis Motor 1"){.aligncenter .size-medium}

![](/_images/_lmmk2/_add-ons/_clsm-upgrade/lmk2_clsm_upgrade-yaxismotor2.jpg "Y Axis Motor 2"){.aligncenter .size-medium}

- Swap out spacers
- Tighten down M-50 screws
- Tighten coupler

If you have dust shields on your y-axis rails, replace the two M5-50mm screws with the included M5-55mm screws on the inside standoffs/spacers for both y-axis motors. This will allow the dust shields to sit on those new screws slightly.

#### Dip Switches

The motors should arrive with the DIP switches in the correct position for use with the stock settings.

Check to ensure the DIP switches on the X and Y axis motors follow the order of: **1-5: OFF, OFF, ON, ON, ON**

![](/_images/_lmmk2/_add-ons/_clsm-upgrade/lmk2_clsm_upgrade-z-dip-switch.jpg){.aligncenter .size-medium}

## Sensors

With the upgraded motors and SLB EXT, you will receive new limit switches with short pigtail connectors. In this section, we will swap out the originals and install the new ones.

### Remove Old Sensors

Locate your X-axis & Z-axis sensors and loosen the nuts, then remove them.

![](/_images/_lmmk2/_add-ons/_clsm-upgrade/lmk2_clsm_upgrade-limit-switches.jpg){.aligncenter .size-medium}

For your Y-axis sensor, remove the bracket from the rail, we will be moving it to the back of the rail, and to the bottom.

![](/_images/_lmmk2/_add-ons/_clsm-upgrade/lmk2_clsm_upgrade-yaxislimit.jpg){.aligncenter .size-medium}

### Install New Sensors

![](/_images/_lmmk2/_add-ons/_clsm-upgrade/lmk2_clsm_upgrade-header6.jpg){.aligncenter .size-full .wid}

For the Z & X-axis, you can simply pop the new pigtail limit switches into the old holes, and tighten the nuts down again. This process is exactly the same for the Z-axis and the X-axis, but differs a bit for the two Y-axis switches.

For the Y-axis, we will be using a bracket to mount the sensor under the Y-axis rails, and pushing them to the back left and right corners. Mount each sensor onto a bracket as shown.

![](/_images/_lmmk2/_add-ons/_clsm-upgrade/lmk2_clsm_upgrade-yaxislimit-position.jpg)
{.align-center .size-medium}

Slip an M5-T Nut into the slot at the back of both Y-axis rails and secure it with an M5-10 mm hex head screw, with **two washers**. Do not tighten this all the way down yet, as we will be sliding the bracket onto it. You can use the wrench that shipped with your LongMill, or one you have in your shop to assist in this step.

![](/_images/_lmmk2/_add-ons/_clsm-upgrade/lmk2_clsm_upgrade-yaxis-slot.jpg){.align-center .size-medium}

Slide the bracket onto the 10mm M5 screw until it bottoms out, then tighten down the screw, while holding the sensor.

![](/_images/_lmmk2/_add-ons/_clsm-upgrade/lmk2_clsm_upgrade-yaxis-tighten.jpeg){.align-center .size-medium}

Adjust the sensors so that they stick out slightly, allowing it to trigger the sensor on the wheels, without hitting them. You may need to adjust and test this step out to ensure you are not hitting, but are getting a positive signal each time the y-axis sensors are triggered.

![](/_images/_lmmk2/_add-ons/_clsm-upgrade/lmk2_clsm_upgrade-yaxis-adjust.jpg "Y-axis Left and Right sensor looking from the back of the machine"){.align-center .size-medium}

**Repeat this step for both ends of the Y-axis (Right and Left).**

## Wiring

Now that we have all 4 motors mounted and the inductive sensors re-arranged, let's move our attention to getting our wires organized. We will be replacing the drag chain that goes along the left Y-axis with a larger one & installing some 3D printed supports.

### Drag Chain & Wires

![](/_images/_lmmk2/_add-ons/_clsm-upgrade/lmk2_clsm_upgrade-header4.jpg){.aligncenter .size-full .wid}

If you have not yet opened all of the tabs in both drag chains, do so at this time. You can slip a small flat head screw driver under each tab to pop them open. We will be replacing the Y-axis drag chain, and upgrading it to a larger size, so you can remove this drag chain entirely at this time.

![](/_images/_lmmk2/_add-ons/_clsm-upgrade/lmk2_clsm_upgrade-opendragchain.jpg){.align-center .size-medium}

With the new, larger drag chain in hand, remove the end links, so we can install them separately, then have an easier time when it comes to reconnecting the drag chain. This can be done with a small flat head screwdriver.

![](/_images/_lmmk2/_add-ons/_clsm-upgrade/lmk2_clsm_upgrade-dragremove.jpg){.align-center .size-medium}

Grab the drag chain mount, 2 x M5 T-nuts and 2 x M5-12mm screws and attach the new black drag chain mount to replace where you old silver one was. You can re-use your M5 T-nuts in this step if you wish.

![](/_images/_lmmk2/_add-ons/_clsm-upgrade/lmk2_clsm_upgrade-dragchainmount.jpg){.align-center .size-medium}

Now you can use another M5-12mm screw to secure the drag chain end link that has open ends. This hole is threaded, so no need for a nut here.

![](/_images/_lmmk2/_add-ons/_clsm-upgrade/lmk2_clsm_upgrade-endlinktop.jpg){.align-center .size-medium}

Moving to the Y-axis where the old drag chain was, move to the back and slide 4 M5 T-nuts into the rail. We will be using these to support the 4 drag chain brackets. Place a washer down, then an M5-12mm screw will hold down the bracket. Space them out evenly, using fewer if you have a smaller footprint.

![](/_images/_lmmk2/_add-ons/_clsm-upgrade/lmk2_clsm_upgrade-dragchain2.jpg){.align-center .size-medium}

Now we can attach the final drag chain end to the last drag chain bracket with an M5-12mm screw and the nylock nut.

![](/_images/_lmmk2/_add-ons/_clsm-upgrade/lmk2_clsm_upgrade-nylocknut.jpg){.align-center .size-medium}

One tip that can help out in this step is to **put the drag chain end on before you put the bracket onto the rail as pictured above**.

![](/_images/_lmmk2/_add-ons/_clsm-upgrade/lmk2_clsm_upgrade-endlinkbotttom.jpg){.align-center .size-medium}

When looking at your motor cables, you will notice each one is labelled with the corresponding axis it goes to. Let's begin with the X-axis motor cable.

The motor cables have 3 plugs to attach on each end. The two green plugs are for your new motor, and the middle black one is for your limit switch/inductive sensor. No more individual cables, we've combined them all together!

Plug in the green motor power and motor signal connectors.

![](/_images/_lmmk2/_add-ons/_clsm-upgrade/lmk2_clsm_upgrade-motorplugs.jpg){.align-center .size-medium}

Now clip the black limit switch sensors together.

![](/_images/_lmmk2/_add-ons/_clsm-upgrade/lmk2_clsm_upgrade-motorconnectorplugging.jpg){.align-center .size-medium}

Once the power has been plugged in, tighten the screws down on the power plug with a small flathead screwdriver.

![](/_images/_lmmk2/_add-ons/_clsm-upgrade/lmk2_clsm_upgrade-motorpowerconnectorscrew.jpg){.align-center .size-medium}

## Motor Covers

Your kit has included motor covers, to protect your motors from bumps or accidental unplugs. Remove the top-left and bottom-right M3 screws from the X-axis motor using the 2.5mm Allen-key provided.

![](/_images/_lmmk2/_add-ons/_clsm-upgrade/lmk2_clsm_upgrade-motorscrewremoval.jpg){.align-center .size-medium}

Install the motor cover onto the back of the motor using M3-40mm screws. Orient the motor cover so the wires exit upwards.

**Note: Install the motor cover gently to avoid damaging the wires attached to the connectors.**

![](/_images/_lmmk2/_add-ons/_clsm-upgrade/lmk2_clsm_upgrade-motorcover-install.jpg){.align-center .size-medium}

![](/_images/_lmmk2/_add-ons/_clsm-upgrade/lmk2_clsm_upgrade-motorcoverscrew.jpg){.align-center .size-medium}

Repeat the previous steps for the Z, Y1 and Y2 motors.

## SLB EXT

![](/_images/_lmmk2/_add-ons/_clsm-upgrade/lmk2_clsm_upgrade-header5.jpg){.aligncenter .size-full .wid}

To begin this section, let's mount the board to the rail. Grab both SLB mounting brackets and slide them onto the back of the case.

![](/_images/_lmmk2/_add-ons/_clsm-upgrade/lmk2_clsm_upgrade-slbcase.jpg){.align-center .size-medium}

Space them out evenly, then tighten them down onto the rail using the M5 T-nuts and M5 12mm screws.

![](/_images/_lmmk2/_add-ons/_clsm-upgrade/lmk2_clsm_upgrade-slbcasespace.jpg){.align-center .size-medium}

![](/_images/_lmmk2/_add-ons/_clsm-upgrade/lmk2_clsm_upgrade-slbcasetight.jpg){.align-center .size-medium}

Now with the SLB installed, let's open it up and plug everything in! Loosen the thumb screw on the front of the SLB-EXT enclosure and remove the acrylic face plate.

Fit the Z-axis and X-axis wire harnesses into the top cut out of the enclosure on the right side. Plug the sensor and motor control connectors into their respectively named ports.

Plug the two-pronged motor power connectors into the left most power ports. The power ports all supply the same output and therefore the connectors are able to be plugged into any, however, for installation purposes we recommend you to plug into the two leftmost ports while installing X and Z.

![](/_images/_lmmk2/_add-ons/_clsm-upgrade/lmk2_clsm_upgrade-xzsignals.jpg){.align-center .size-medium}

![](/_images/_lmmk2/_add-ons/_clsm-upgrade/lmk2_clsm_upgrade-xzmotorplug.jpg){.align-center .size-medium}

Fit the Y1-axis and Y2-axis wire harnesses into the bottom cutout of the enclosure on the right side. Plug the sensor and motor control connectors into their respectively named ports. It is important that you do not mismatch the control connector from one harness with the sensor connector of the other when plugging into one pair of Y1 or Y2 ports. If installed incorrectly you will encounter an alarm during operation.  

Plug the two-pronged motor power connectors into the two rightmost power ports. The power ports all supply the same output and therefore the connectors are able to be plugged into any, however, for installation purposes we recommend you to plug into the two rightmost ports while installing Y1 and Y2 power.

![](/_images/_lmmk2/_add-ons/_clsm-upgrade/lmk2_clsm_upgrade-ysignals.jpg){.align-center .size-medium}

![](/_images/_lmmk2/_add-ons/_clsm-upgrade/lmk2_clsm_upgrade-ymotorplug.jpg){.align-center .size-medium}

Reinstall the acrylic face plate of the SLB-EXT onto the enclosure. Tighten the thumb screw by hand. Plug the green connector of the E-stop cable into the port labelled E-stop on the left side of the controller, and the other side of the cable into the E-stop.

Plug the green connector of the 48V power supply into the port labelled Power & plug the power supply into a 110V outlet. You can now flip the ON/OFF switch to power up your new board!

## Software Changes

Once your setup is complete and everything is secure and plugged into the SLB EXT, we will need to adjust two items:

- the motor speed in your sending software
- the direction of homing (We are now going to the back left corner by default)

You can tweak these settings manually, or, you can use our Macro instead! Simply download this macro and run it in gSender, and your settings will automatically update. You can click on the link below to go to a google folder and download the file (**lmk2_clsm_macro.json**).

[Closed Loop Stepper Motor Macro](https://drive.google.com/drive/folders/1cCXB1dCWpowHjJuEUF3RIYLrTxjNG10j?usp=sharing){.align-center}

Once you have the file, load up gSender, and go to the Macro section on the Carve tab. Here you can import the new macro.

![](/_images/_lmmk2/_add-ons/_clsm-upgrade/lmk2_clsm_upgrade-macroimport.jpg){.align-center .size-medium}

![](/_images/_lmmk2/_add-ons/_clsm-upgrade/lmk2_clsm_upgrade-macrofile.jpg){.align-center .size-medium}

Once the macro is loaded into gSender, click on it to run.

![](/_images/_lmmk2/_add-ons/_clsm-upgrade/lmk2_clsm_upgrade-macropress.jpg){.align-center .size-medium}

![](/_images/_lmmk2/_add-ons/_clsm-upgrade/lmk2_clsm_upgrade-macrorun.gif){.align-center size-full}

The macro will automatically update your motor settings! You can double check that they are correct by matching the configuration shown below.

![](/_images/_lmmk2/_add-ons/_clsm-upgrade/lmk2_clsm_upgrade-macro-axis-settings.jpg){.align-center .size-medium}

The Macro will also flip your homing direction for the Y-axis, by turning it off. Here you can see that only X is toggled on. This will send the machine to the back when homing, where your new sensors are installed!

![](/_images/_lmmk2/_add-ons/_clsm-upgrade/lmk2_clsm_upgrade-macro-settings.jpg){.align-center .size-medium}

Congrats! You have now completed the installation and setup of your new Closed Loop Stepper Motor Kit. Go carve something cool friend!

## Open Source

Here you can find the schematics/drawings that are available for download.

[Take me to the files!](https://drive.google.com/drive/folders/1nnLDaa0WipzLcEGQt92obk_tss4Uf9-2?usp=sharing)
