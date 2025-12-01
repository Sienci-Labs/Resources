---
title: Closed Loop Stepper Motor Upgrade
menu_order: 5
post_status: draft
post_excerpt: How to assemble the drag chain and manage the wiring for the LongMill Benchtop CNC. Wire routing for the Makita router and motors is illustrated.
post_date: 2022-03-17 20:11:00
taxonomy:
    knowledgebase_cat: lmk2-assembly
    knowledgebase_tag:
        - mk2
custom_fields:
    KBName: LongMill MK2 CNC
    basepress_post_icon: bp-caret-right
skip_file: no
featured_image: _images/_lmmk2/_assembly/_motorswires/lmk2_motors_Title-Motors-Wiring.png
---

Switching to the closed loop stepper motors (CLSM) from the open loop motors is easy. The main difference between the open loop and the closed loop motors is that the open loop motors lack positional feedback making them prone to “skipping steps” under load. With closed loop motors there is a feedback system that helps in monitoring their positions which enables them to self-correct errors, improve accuracy and operate more efficiently. The CLSM kit requires the use of the included SuperLongBoard EXT.

For a more detailed rundown on how to successfully prepare for the use of the SLB-EXT please refer to the following documentation: https://resources.sienci.com/view/am-slb-ext-controller/

## Unboxing

Your upgrade kit will include a new SLB EXT, 4 closed loop motors, a new 48 volt power supply and more! Check out the list below and [contact our team](https://sienci.com/contact-us/) if any parts are missing.

## New Parts

| Part | Photo |
|------|--------|
| NEMA 23 Motors x4 | ![placeholder](https://placehold.co/100x100) |
| 40 mm blue aluminum standoffs x16 | ![placeholder](https://placehold.co/100x100) |
| M5x55 screws x4 (for dust shield addon) | ![placeholder](https://placehold.co/100x100) |
| SLB-EXT | ![placeholder](https://placehold.co/100x100) |
| 48VDC power supply | ![placeholder](https://placehold.co/100x100) |
| Drag chain bracket | ![placeholder](https://placehold.co/100x100) |
| 18 x 26 drag chain | ![placeholder](https://placehold.co/100x100) |
| SLB 3D printed rail mounts | ![placeholder](https://placehold.co/100x100) |
| Drag chain holder mounts | ![placeholder](https://placehold.co/100x100) |
| Inductive sensor x4 | ![placeholder](https://placehold.co/100x100) |
| Motor cable set | ![placeholder](https://placehold.co/100x100) |

When unpacking the CLSM upgrade kit, please note that there are some parts that we will be re-using from your previous setup.

## Re-used Parts

| Part | Photo |
|------|--------|
| M5x50 screws | ![placeholder](https://placehold.co/100x100) |
| Z axis drag chain | ![placeholder](https://placehold.co/100x100) |
| Current inductive sensors | ![placeholder](https://placehold.co/100x100) |
| Couplers (Motor) | ![placeholder](https://placehold.co/100x100) |

## Motors

![](/_images/_lmmk2/_add-ons/_clsm-upgrade/lmk2_clsm_upgrade_Title-Motors-Wiring.jpg){.aligncenter .size-medium}

This process should take approximately 2-3 hours. To begin, jog machine to the front/center of your wasteboard, and pull the table away from the wall if possible. You can also remove your router or spindle and open all of the links on your drag chains with a small flat head screwdriver to prepare for this upgrade. Let'start with the motors!

### Remove Stepper Motors

![](/_images/_lmmk2/_add-ons/_clsm-upgrade/lmk2_clsm_upgrade-Header1.jpg){.aligncenter .size-full .wid}

We will be removing all 4 of the open loop motors (X-axis, Z-axis + 2 Y-axis motors) The process is the same for all 4 of the motors. We begin with the X-axis motor, on the left side of the machine.

Step 1

Unplug the open loop stepper motor at the white connector. This is done by pressing on the short end of the white connector, then pulling the connection apart.

![](/_images/_lmmk2/_add-ons/_clsm-upgrade/lmk2_clsm_upgrade-connector.jpg "Here you can see the X-axis motor plug"){.aligncenter .size-medium}

Step 2

Using an M5 Allen key, remove the M5-50mm bolts and set them aside. We will be using them to install the new motors. You can use a drill to speed up the process here, and if the screws are too tight, use the M5 Allen key to loosen them. You will not need to keep the aluminum spacers, replacements are in the new kit.

![](/_images/_lmmk2/_add-ons/_clsm-upgrade/lmk2_clsm_upgrade-pic1.jpg){.aligncenter .size-full}

Step 3

Loosen the bolt on the coupler that is closest to the motor. This will allow you to lift each motor free from the motor shafts.

![](/_images/_lmmk2/_add-ons/_clsm-upgrade/lmk2_clsm_upgrade-loosecoupller.jpg){.aligncenter .size-medium}

Now that we've pulled the X-axis motor from the motor shaft, **proceed to do the exact same 3 steps with the Z-axis motor and both Y-axis motors.**

- Unplug connector
- Remove 4 standoffs
- Loosen coupler.

### Install the New Motors

Ok, nicely done! We will now run the process we just completed, in reverse. Grab the new closed loop motors, the blue standoffs, and the M5-50mm bolts we removed in step 2 above.

![](/_images/_lmmk2/_add-ons/_clsm-upgrade/lmk2_clsm_upgrade-header2.jpg){.aligncenter .size-full .wid}

Step 1

Let's begin by sliding each M5-50mm bolt into a matching 40mm spacer. Thread each bolt/spacer into the corresponding 4 holes to secure the motor in place. Using either a drill or an M5 allen key, tighten each spacer/bolt combo.

![](/_images/_lmmk2/_add-ons/_clsm-upgrade/lmk2_clsm_upgrade-motor-installjpg.jpg){.aligncenter .size-medium}

Step 2

With the new motor shaft fully seated in the coupler, turn the coupler bolt closest to the new motor with the M5 allen key until tight.If everything has come together well so far, you should be able to now check that the lead screw can spin relatively easily.

![](/_images/_lmmk2/_add-ons/_clsm-upgrade/lmk2_clsm_upgrade-tightencoupler.jpg){.aligncenter .size-medium}

Now that we've replaced the one motor, **proceed to do the exact same 3 steps with the remaining motors.**

- Swap out spacers
- Tighten down M-50 screws
- Tighten coupler

### Remove Old Sensors

With the upgraded motors and SLB EXT, you will receive new limit switches with short pigtail connectors. In this section, we will swap out the originals and install the new ones.

Locate your X-axis & Z-axis sensors and loosen the nuts, then remove them.

![](/_images/_lmmk2/_add-ons/_clsm-upgrade/lmk2_clsm_upgrade-limit-switches.jpg){.aligncenter .size-medium}

For your Y-axis sensor, remove the bracket from the rail, we will be moving it to the back of the rail, and to the bottom.

![](/_images/_lmmk2/_add-ons/_clsm-upgrade/lmk2_clsm_upgrade-yaxislimit.jpg){.aligncenter .size-medium}

Here you can see both sensors installed at the bottom of the rail in the back right and left sides. Let's move on to installing the new sensors!

![](/_images/_lmmk2/_add-ons/_clsm-upgrade/lmk2_clsm_upgrade-limit-rl.jpg "Here you can see the Y-axis left and right limit switches"){.align-center .size-medium}

### Instal New Sensors

![](/_images/_lmmk2/_add-ons/_clsm-upgrade/lmk2_clsm_upgrade-header6.jpg){.aligncenter .size-full .wid}

For the Z & X-axis, you can simply pop the new pigtail limit switches into the old holes, and tighten the nuts down again. This process is exactly the same for the Z-axis and the X-axis, but differs a bit for the two Y-axis switches.

For the Y-axis, we will be using a bracket to mount the sensor under the Y-axis rails, and pushing them to the back left and right corners. Mount each sensor onto your bracket as shown.

![](/_images/_lmmk2/_add-ons/_clsm-upgrade/lmk2_clsm_upgrade-limit-bracket.jpg){.align-center .size-medium}

Slip an M5-T Nut into the slot at the back of both Y-axis rails and secure it with an M5-12 mm socket head screw. Do not tighten this all the way down yet, as we will be sliding the bracket onto it.

![](/_images/_lmmk2/_add-ons/_clsm-upgrade/lmk2_clsm_upgrade-yaxis-slot.jpg){.align-center .size-medium}

Slide the bracket onto the 12mm M5 screw until it bottoms out, then tighten down the screw, while holding the sensor.

![](/_images/_lmmk2/_add-ons/_clsm-upgrade/lmk2_clsm_upgrade-yaxis.jpg){.align-center .size-medium}

Repeat this step for both ends of the Y-axis.

## Wiring

Now that we have all 4 motors mounted and the inductive sensors re-arranged, let's move our attention to getting our wires organized. We will be replacing the drag chain that goes along the left Y-axis with a larger one & installing some 3D printed supports.

### Drag Chain & Wires

![](/_images/_lmmk2/_add-ons/_clsm-upgrade/lmk2_clsm_upgrade-header4.jpg){.aligncenter .size-full .wid}

If you have not yet opened all of the tabs in both drag chains, do so at this time. You can slip a small flat head screw driver under each tab to pop them open.

![](/_images/_lmmk2/_add-ons/_clsm-upgrade/lmk2_clsm_upgrade-opendragchain.jpg){.align-center .size-medium}

![](/_images/_lmmk2/_add-ons/_clsm-upgrade/lmk2_clsm_upgrade-dragremove.jpg){.align-center .size-medium}

When looking at your motor cables, you will notice one is longer than the others. This long motor cable is meant for your back right Y-axis motor. Grab a shorter one and run it through your open drag chain to the Z-axis motor.








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

For both Y-axes, position a motor assembly at the back foot making sure the motor wire faces down. Slide the motor shaft into the coupler, then tighten all four M5-50mm screws into the foot. Once the motor is secure, tighten the set screw on the motor side of the coupler (pictured).

![](/_images/_lmmk2/_add-ons/_clsm-upgrade/lmk2_clsm_upgrade-xzsignals.jpg)

![](/_images/_lmmk2/_add-ons/_clsm-upgrade/lmk2_clsm_upgrade-xzmotorplug.jpg)



![](/_images/_lmmk2/_add-ons/_clsm-upgrade/lmk2_clsm_upgrade-ysignals.jpg)

![](/_images/_lmmk2/_add-ons/_clsm-upgrade/lmk2_clsm_upgrade-ymotorplug.jpg)

Show plug in power to board
Show plug in EStop
Show plug in USB

Show power on button

## Software Changes

What are we changing here or are we providing a macro that will tweak your settings automatically?