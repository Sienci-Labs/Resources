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
| 40 mm red aluminum standoffs x16 | ![placeholder](https://placehold.co/100x100) |
| M5x55 screws x4 (for dust shield addon) | ![placeholder](https://placehold.co/100x100) |
| SLB-EXT | ![placeholder](https://placehold.co/100x100) |
| 48VDC power supply | ![placeholder](https://placehold.co/100x100) |
| Drag chain bracket | ![placeholder](https://placehold.co/100x100) |
| 18 x 26 drag chain | ![placeholder](https://placehold.co/100x100) |
| SLB 3D printed rail mounts | ![placeholder](https://placehold.co/100x100) |
| Drag chain holder mounts | ![placeholder](https://placehold.co/100x100) |
| Inductive sensor x1 | ![placeholder](https://placehold.co/100x100) |
| Motor cable set | ![placeholder](https://placehold.co/100x100) |

When unpacking the CLSM upgrade kit, please note that there are some parts that we will be re-using from your previous setup.

## Re-used Parts

| Part | Photo |
|------|--------|
| M5x50 screws | ![placeholder](https://placehold.co/100x100) |
| Z axis drag chain | ![placeholder](https://placehold.co/100x100) |
| Current inductive sensors | ![placeholder](https://placehold.co/100x100) |
| Couplers (Motor) | ![placeholder](https://placehold.co/100x100) |

## Installation

![](/_images/_lmmk2/_add-ons/_clsm-upgrade/lmk2_clsm_upgrade_Title-Motors-Wiring.jpg){.aligncenter .size-medium}

This process should take approximately 2-3 hours. To begin, jog machine to the front/center of your wasteboard, and pull the table away from the wall if possible. You can also remove your router or spindle and open all of the links on your drag chains with a small flat head screwdriver to prepare for this upgrade. Let'start with the motors!

### Remove Stepper Motors

![](/_images/_lmmk2/_add-ons/_clsm-upgrade/lmk2_clsm_upgrade-Header1.jpg){.aligncenter .size-full .wid}

We will be removing all 4 of the open loop motors (X-axis, Z-axis + 2 Y-axis motors) The process is the same for all 4 of the motors. We begin with the X-axis motor, on the left side of the machine.

Step 1

Unplug the open loop stepper motor at the white connector. This is done by pressing on the short end of the white connector, then pulling the connection apart.

![](/_images/_lmmk2/_add-ons/_clsm-upgrade/lmk2_clsm_upgrade-connector.jpg "Here you can see the X-axis motor plug"){.aligncenter .size-medium}

Step 2

Using an M5 Allen key, remove the M5-50mm bolts and set them aside. We will be using them to install the new motors. You can use a drill to speed up the process here and if the screws are too tight, use the M5 Allen key to loosen them. You will not need to keep the aluminum spacers, replacements are in the new kit.

![](/_images/_lmmk2/_add-ons/_clsm-upgrade/lmk2_clsm_upgrade-pic1.jpg){.aligncenter .size-full}

Step 3

Loosen the bolt on the coupler that is closest to the motor. This will allow you to lift each motor free from the motor shafts.

![](/_images/_lmmk2/_add-ons/_clsm-upgrade/lmk2_clsm_upgrade-coupler.jpg){.aligncenter .size-medium}

Now that we've pulled the X-axis motor from the motor shaft, proceed to do the exact same 3 steps with the Z-axis motor and both Y-axis motors. Unplug, remove 4 standoffs, loosen coupler.

### Install the New Motors

Ok, nicely done! We will now run the process we just completed, in reverse. Grab the new closed loop motors, the red standoffs, and the M5-50mm bolts we removed in step 2 above.

![](/_images/_lmmk2/_add-ons/_clsm-upgrade/lmk2_clsm_upgrade-header2.jpg){.aligncenter .size-full .wid}

Step 1

Let's begin by sliding each M5-50mm bolt into a matching 40mm spacer. Thread each bolt/spacer into the corresponding 4 holes to secure the motor in place. Using either a drill or an M5 allen key, tighten each spacer/bolt combo.

![](/_images/_lmmk2/_add-ons/_clsm-upgrade/lmk2_clsm_upgrade-motor-installjpg.jpg){.aligncenter .size-medium}

Step 2



Step 3

![](/_images/_lmmk2/_add-ons/_clsm-upgrade/lmk2_clsm_upgrade-motorplugs.jpg)

Plugs - Do we care about motor orientation? Pic to show the plugs would be nice here....










For both Y-axes, position a motor assembly at the back foot making sure the motor wire faces down. Slide the motor shaft into the coupler, then tighten all four M5-50mm screws into the foot. Once the motor is secure, tighten the set screw on the motor side of the coupler (pictured).

![](/_images/_lmmk2/_assembly/_motorswires/lmk2_motors_Motors-Wiring_3.png){.aligncenter .size-medium}

If everything has come together well so far, you should be able to now check that the lead screw can spin relatively easily. If you find that the motor **shaft doesn’t fit into the coupler** it’s likely that you tightened the motor-side set screw earlier on and have now deformed it. There is a chance for fixing this: take the motor-side set screw out of the coupler and insert anything thin like a box knife, putty knife, or paint scraper into the vertical slot of the coupler. Then screw in the set screw from the opposite side until it hits the inserted object. Rotate it against the object a couple turns to open up the slot again, then back the screw out again, remove the object, and reinsert the screw back to where it should be.

![](/_images/_lmmk2/_assembly/_motorswires/lmk2_motors_double-pic-green-circle.png){.aligncenter .size-medium}

Bring a motor assembly to the left Y-gantry plate making sure the motor wire faces back and upwards (pictured). Slide the motor shaft into the coupler, then tighten the four M5-50mm bolts into the gantry. At the coupler, tighten the set screw at the motor side and ensure the lead screw can spin without excessive force. <img class="non alignnone wp-image-4869" src="https://resources.sienci.com/wp-content/uploads/2025/02/lmk2_xzaxes_48EX-symbol.png" alt="" width="61" height="30" />

<a href="https://resources.sienci.com/view/48x30-LongMill-mk2-accompanying-manual/#ex-lead-screw-assembly"><img class="fortye aligncenter wp-image-3950 size-medium" src="https://resources.sienci.com/wp-content/uploads/2025/02/lmk2_motors_EX5C.png" alt="" width="850" height="68" /></a>

![](/_images/_lmmk2/_assembly/_motorswires/lmk2_motors_double-pic-green-circle-2-1.png){.aligncenter .size-medium}

Bring the last motor assembly to the Z-axis motor mount making sure the motor wire faces backwards. Slide the motor shaft into the coupler, then tighten the four M5-50mm bolts into the motor mount. At the coupler, tighten the set screw at the motor side and ensure the lead screw can spin without excessive force.

## Attaching Drag Chain Ends

![](/_images/_lmmk2/_assembly/_motorswires/lmk2_motors_49_1.jpg){.aligncenter .size-medium .wid}

We will now be installing the drag chains which can be found in the long rail box inside the Y-axis rails. These contain and guide the wires on the LongMill so they aren’t in the way during cutting. They also keep wires from wearing out from bending or being cinched around corners.

![](/_images/_lmmk2/_assembly/_motorswires/lmk2_motors_49_2-1.jpg){.aligncenter .size-medium}

Start by un-clipping all the drag chain clips using a flat head screwdriver or anything else sharp like a wood screw underneath the clip tabs. These hold the wires into the chain but can open or be completely removed, giving flexibility to add or remove wires on your machine when needed. If you’re struggling with this the LongMill wrench also has a taper that can help you open them.

We recommend permanently removing every other clip if you plan on adding more wiring in the future since accessing the wire will take half the time and the chains will still work fine. Stick the extras into a baggy to save for later if you wish.

Now, remove the end links from both sets of drag chains. For the pin-type link (left picture), squeeze it together then twist and pull to disconnect it. For the hole-type end link (right picture), pull on one side of the link then twist it away to separate it. A flat head screwdriver or thin shim can also be handy for this, just be careful not to cut yourself.

![](/_images/_lmmk2/_assembly/_motorswires/lmk2_motors_50_1-1.jpg){.aligncenter .size-medium}

Do this for all four end pieces, two hole-types and two pin-types, and set them aside.

![](/_images/_lmmk2/_assembly/_motorswires/lmk2_motors_50_2.jpg){.aligncenter .size-medium}

![](/_images/_lmmk2/_assembly/_motorswires/lmk2_motors_51_1.jpg){.aligncenter .size-medium}

Grabbing the bag of t-nuts and M5-10mm bolts, we will attach these end links to the machine starting with the left Y-axis. Slide a t-nut onto the Y-axis rail through the hole in the front foot.

![](/_images/_lmmk2/_assembly/_motorswires/lmk2_motors_51_2.jpg){.aligncenter .size-medium}

You’ll want to position it a little further back than halfway on the rail for both machine models (30x30 pictured).

![](/_images/_lmmk2/_assembly/_motorswires/lmk2_motors_51_3.jpg){.aligncenter .size-medium}

Once in position, use an M5-10mm bolt to fasten a **hole-type** end link in place with the M5 Allen key (pictured).

![](/_images/_lmmk2/_assembly/_motorswires/lmk2_motors_52_1.jpg){.aligncenter .size-medium}

Now get a **pin-type** end link (pictured) along with the 3D printed chain aligner from the yellow hardware bag to mount the other end of the drag chain. The printed aligner has a nub that will align to a hole in the end link (pictured).

![](/_images/_lmmk2/_assembly/_motorswires/lmk2_motors_52_2.jpg){.aligncenter .size-medium}

These will attach to the drag chain mount from the underside with another bolt.

![](/_images/_lmmk2/_assembly/_motorswires/lmk2_motors_53_1-1.jpg){.aligncenter .size-medium}

On the X-axis the process will be repeated. Slide in a t-nut through the hole in the right Y-gantry and bring it all the way to the left side next to the drag chain mount where you’ll bolt in a **pin-type** end link. Ensure the end link is snug up against the drag chain mount (pictured).

![](/_images/_lmmk2/_assembly/_motorswires/lmk2_motors_53_2.jpg){.aligncenter .size-medium}

Lastly, attach the final end link onto the Z-axis motor mount using one last bolt to the inner hole. Note the direction the link is facing.

## Routing Wires

![](/_images/_lmmk2/_assembly/_motorswires/lmk2_motors_routeheader.jpg){.aligncenter .size-medium .wid}

For the remaining assembly you won’t need any more of the loose hardware except for the provided wood screws and the 3D printed ACME nut covers. If you want, take a second to clean off your space and feel free to stick all the extra remains into a box for later use or maintenance on your machine.

![](/_images/_lmmk2/_assembly/_motorswires/lmk2_motors_54_2.jpg){.aligncenter .size-medium}

Before we attach the drag chains back onto the end links we’ll be moving around a couple links to get the right fit. To do this, put your hands on either side of the link you want to break, then twist and pull them apart to disconnect. Set aside the remaining, unused links - they can come in use if you’re planning on upgrading to a larger sized LongMill later.

Depending on the size of LongMill you have, remove and add links to each drag chain as follows:

- For the 12x30 LongMill, remove **16 links** off of the Y-axis drag chain and add **3 links** onto the X-axis chain.
- For the 30x30 LongMill, remove **13 links** off of the Y-axis drag chain and add **3 links** onto the X-axis chain.
- For the 48x30 LongMill, remove **13 links** off of the Y-axis drag chain and leave the longer X-axis drag chain at its original length.

This will make it so the chains are the correct length to travel the whole range of motion of the machine while also staying as short as possible to maximize the wire length going to the controller.

![](/_images/_lmmk2/_assembly/_motorswires/lmk2_motors_Allen-key-router.jpg){.aligncenter .size-medium}

At this stage, it’s a good idea to grab the router you’ll be using with your machine. We’ll show these steps using the Makita RT0700 / RT0701 trim router that we recommend (pictured). Also, grab the motor wires from the motor box while you’re at it.

**Note: when using the Makita RT0700 / RT0701 it’ll come with a base attached. Remove this as you’ll just need the main router body for the CNC.**

To mount your router, loosen off the mount's front bolts until it slides in. Place it nearly all the way down with the power cable facing left and rotated slightly backward (pictured) then tighten back up to secure it. Go back and forth between the two bolts to keep equal clamping force and make sure not to over-tighten them.

![](/_images/_lmmk2/_assembly/_motorswires/lmk2_motors_55_2.jpg){.aligncenter .size-medium}

Confirm the angle by turning the Z-axis lead screw by hand until its upper limit - the blue part of the router body shouldn’t collide with the Z-axis motor mount at any point. You can adjust the router height later depending on your setup: lower if you use tiny tools on thin material or higher if you use longer tools on 3-4” thick material.

This maximum position is also where you can access the 4 bolts holding in the router mount from behind for future swapping or tramming. You'll simply lift up the drag chain and go through the hole in the X-gantry, being mindful not to damage the aluminum rail edge with the Allen key.

Optionally use the top left hole on the X-gantry as a zip tie point to keep your router wire out of the way during operation. To set it up right, move the Z-axis all the way down and then zip it on with some extra slack still available (pictured).

![](/_images/_lmmk2/_assembly/_motorswires/lmk2_motors_56_1.jpg){.aligncenter .size-medium}

![](/_images/_lmmk2/_assembly/_motorswires/lmk2_motors_56_2.jpg){.aligncenter .size-medium}

Now onto the remaining wiring. Grab (the longer one) a motor cable and connect it to the Z-axis NEMA 23 motor. The connector can only go in one way so keep trying until it easily clicks in.

![](/_images/_lmmk2/_assembly/_motorswires/lmk2_motors_57_1.jpg){.aligncenter .size-medium}

Grab the drag chain for the X-axis (the longer one) and seat in the Z-axis motor cable and router wire. Ensure you have the correct end of the drag chain so it’ll attach onto the end link and bend in the right direction. Reattach it onto the end link and start to re-clip the clips into place.

![](/_images/_lmmk2/_assembly/_motorswires/lmk2_motors_57_2.jpg){.aligncenter .size-medium}

**Note:** if you purchased the limit switch add-on kit you’ll want to leave enough clips open that running the wires for the switches later on will be easier to do.

![](/_images/_lmmk2/_assembly/_motorswires/lmk2_motors_58_1.jpg){.aligncenter .size-medium}

Leaving the last few clips open, bring the other end of the drag chain around and attach it onto the other end link on the X-axis rail. Pull the wires through and around the drag chain mount and finish closing the remaining clips.

![](/_images/_lmmk2/_assembly/_motorswires/lmk2_motors_58_2.jpg){.aligncenter .size-medium}

Attach a motor cable onto the X-axis NEMA 23 stepper motor. <img class="non alignnone wp-image-4869" src="https://resources.sienci.com/wp-content/uploads/2022/03/48EX-symbol.png" alt="" width="61" height="30" />

<a href="https://resources.sienci.com/view/48x30-LongMill-mk2-accompanying-manual/#cable-extension-installation"><img class="fortye aligncenter wp-image-3953 size-medium" src="https://resources.sienci.com/wp-content/uploads/2025/02/lmk2_motors_EX6C.png" alt="" width="850" height="72" /></a>

![](/_images/_lmmk2/_assembly/_motorswires/lmk2_motors_59.jpg){.aligncenter .size-medium}

Take the X and Z-axis stepper motor cables and the router cable and insert them into the Y-axis drag chain. Keep in mind the bend of the drag chain and attach it, clipping in the clips to secure the wires.

![](/_images/_lmmk2/_assembly/_motorswires/lmk2_motors_60_1.jpg){.aligncenter .size-medium}

Bring the other end of the drag chain around and attach it onto the other end link on the Y-axis rail. Pull the wires through and off to the left side of the rail and close the remaining clips.

![](/_images/_lmmk2/_assembly/_motorswires/lmk2_motors_60_2.jpg){.aligncenter .size-medium}

Lastly plug in the cables for the motors on the two Y-axis NEMA 23 stepper motors.

![](/_images/_lmmk2/_assembly/_motorswires/lmk2_motors_61_1.jpg){.aligncenter .size-medium}

Bring the cables around to the left of the machine so they’re now all bundled together (pictured). You’ll be plugging the motors cables into the control box shortly but otherwise the machine wiring is now complete!

![](/_images/_lmmk2/_assembly/_motorswires/lmk2_motors_61_2.jpg){.aligncenter .size-medium}



We will be unplugging everything from the controller and replacing it. We will have some new ways to route your wires and a new drag chain to install.

Step 2

Unscrew all 4 screws in the standoffs, but don’t remove them completely. You can use a drill to speed up the process here and ift the screws are too tight, use a M5 Allen key to loosen them.

Pic of motor stand offs


Step 3

Now we are loosening the top M5 coupler screw, to allow us to remove the motor entirely.

Pic of coupler and label the correct screw to loosen.

Pic of motor coming off of the standoffs.

Step 4

Slide a small flat head screwdriver into the drag chain end closest to the motor and pry it to the side a bit to disconnect the entire drag chain.

Pic of screwdriver positioning and closeup of where to put tip of screwdriver.

Step 5

Pop the drag chain tabs open with a small flathead  screwdriver, and remove the motor wire from the drag chain. (We are unplugging it from the board in the next step)

Pic of poppting tabs

Step 6

Trace the Z-axis motor wire back to the controller you are using (Longboard or SuperLongboard) and unplug it. Since we will be replacing the entire controller with the upgraded SLB EXT, you can unplug all of the things at this time. Power, probe, USB, motors, limit switches, everything.

Pic of LongMill unplugged


Step 7 - Moving to X-Axis motor

Repeat above motor removal.
Unplug

Loosen standoffs

Loosen top screw of coupler

Remove wire from drag chain


Pics of these same steps from a different angle

Step 8
Remove drag chain entirely

Unscrew from xrail elbow and yrail screw

Pics of both parts being removed

Step 9 - Moving to Y-Axis motors

Repeat above motor removal.
Unplug

Loosen standoffs

Loosen top screw of coupler

Remove wire from drag chain

Pics of these same steps from a different angle
