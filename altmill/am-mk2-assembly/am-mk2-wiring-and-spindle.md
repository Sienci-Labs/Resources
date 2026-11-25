---
title: 7. Wiring and Spindle
menu_order: 8
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

<div markdown="1" style="width: 850px; max-width: 100%; margin-left: auto; margin-right: auto;">

![](/_images/_am/_assembly/am_assembly_mk2wiringandspindleheader-850x594.jpg){.aligncenter .size-medium}

</div>

<a id="controller-mounting"></a>

### Controller Mounting

<div markdown="1" style="width: 5374px; max-width: 100%; margin-left: auto; margin-right: auto;">

![](/_images/_am/_assembly/am_assembly_controller-mounting-1500x.jpg){.aligncenter .size-full}

</div>

Insert two (2) M5-10mm socket head screws into the two (2) holes under the “ALTMILL” cutout in the side of the left leg. Thread M5 T-nuts onto the screws, leaving the T-nuts loose.

<div markdown="1" style="width: 850px; max-width: 100%; margin-left: auto; margin-right: auto;">

![](/_images/_am/_assembly/am_assembly_slb-exttnutplace-850x567.jpg){.aligncenter .size-medium}

</div>

Slide the SLB-EXT enclosure onto the T-nuts. The T-nuts fit into the T-slot from the left side of the SLB-EXT enclosure. Orient the enclosure such that the Sienci Labs logo is on the bottom left corner when looking at the acrylic face plate.

<div markdown="1" style="width: 850px; max-width: 100%; margin-left: auto; margin-right: auto;">

![](/_images/_am/_assembly/am_assembly_slb-exttnutslide-850x567.jpg){.aligncenter .size-medium}

</div>

Tighten the M5-10mm screws, clamping the enclosure to the table leg.

<div markdown="1" style="width: 850px; max-width: 100%; margin-left: auto; margin-right: auto;">

![](/_images/_am/_assembly/am_assembly_slb-exttightentoleg-850x567.jpg){.aligncenter .size-medium}

</div>

**Note:** If you thread the M5 T-nut too far onto the M5-10mm screw you will have a difficult time sliding the T-nut into the T-slot of the enclosure.

<a id="cable-management-and-spindle-vfd"></a>

### Cable Management and Spindle VFD

<!-- Q-ATC-01: Confirm the exact ATC branch/return points, including shared Y2 routing and all four motor/sensor connections. The callout does not authorize skipping the whole page. -->

<div markdown="1" style="width: 1190px; max-width: 100%;">

![](/_images/_am/_assembly/am_assembly_altmill-parts-needed-wiring-and-spindle.jpg){.alignnone .size-full}

</div>

**Installing the ATC kit?** Follow the [ATC installation guide](https://resources.sienci.com/view/atc-unboxing/) for the spindle, VFD and associated cable routing. If you are installing the standard spindle kit, continue below. The shared Y2 cable routing and Sensor and Motor Connections steps on this page are still required for the machine.

Install three (3) cable hanger clips along the length of the rear crossbeam. Insert the hanger into the T-slot horizontally and rotate 90 degrees clockwise to lock the hanger into place.

<div markdown="1" style="width: 614px; max-width: 100%; margin-left: auto; margin-right: auto;">

![](/_images/_am/_assembly/am_assembly_y-cable-clip-individual-install.jpg){.aligncenter}

</div>

<p style="text-align: center;"><em>Cable hanger installation</em></p>

<div markdown="1" style="width: 617px; max-width: 100%; margin-left: auto; margin-right: auto;">

![](/_images/_am/_assembly/am_assembly_y-cable-clip-locations.jpg){.aligncenter}

</div>

<p style="text-align: center;"><em>Cable hanger location along crossbeam</em></p>

Insert the Y2 wire harness through the opening of the cable hangers. Leave both Y-axis motor cables unplugged from the motors during this step.

<div markdown="1" style="width: 620px; max-width: 100%; margin-left: auto; margin-right: auto;">

![](/_images/_am/_assembly/am_assembly_y-cable-clipping.jpg){.aligncenter}

</div>

<p style="text-align: center;"><em>Securing Y2 wire harness in cable hangers</em></p>

**If** you purchased the Sienci Labs Spindle Kit, please use either the Enclosed VFD (no VFD mounting bracket) or Unenclosed VFD (with VFD mounting bracket) instructions.

**If** you are using a third party spindle / router, follow the instructions for your specific spindle and come back to this assembly manual when you have mounted your spindle and are prepared to route the wires through the drag chains.   A 5m length towline rated cable is recommended for 2×4 and 4×4 AltMill models.

<a id="enclosed-vfd"></a>

#### Enclosed VFD

[su_spoiler title="<strong>Enclosed VFD</strong>" open="yes" style="fancy" icon="chevron" anchor_in_url="yes"]

Use the plastic VFD mounting spacer to mount the E-stop module using two M5-30mm screws and two M5 nuts included with the spindle kit.

<div markdown="1" style="width: 850px; max-width: 100%; margin-left: auto; margin-right: auto;">

![](/_images/_am/_assembly/am_assembly_estopvfdmounting-850x640.jpg){.aligncenter .size-medium}

</div>

Mount the VFD unit inside the table leg using the remaining two M5-30mm screws included with the spindle kit. The VFD unit’s front screen should line up with the cutout in the front of the table leg.

<div markdown="1" style="width: 850px; max-width: 100%; margin-left: auto; margin-right: auto;">

![](/_images/_am/_assembly/am_assembly_enclosedvfdmounting-850x638.jpg){.aligncenter .size-medium}

</div>

Plug in the included spindle control cable, AC power cable, and spindle cable into the bottom of the VFD unit. Plug in the AC power cable to your wall outlet or extension cable.

<div markdown="1" style="width: 850px; max-width: 100%; margin-left: auto; margin-right: auto;">

![](/_images/_am/_assembly/am_assembly_enclosedvfdplugin-850x638.jpg){.aligncenter .size-medium}

</div>

Plug in the other end of the spindle control cable to the ‘RS485’ connector on the rear of the SLB-EXT controller.

<div markdown="1" style="width: 850px; max-width: 100%; margin-left: auto; margin-right: auto;">

![](/_images/_am/_assembly/am_assembly_vfdcontrolcableplug-850x638.jpg){.aligncenter .size-medium}

</div>

[/su_spoiler]

<a id="unenclosed-vfd"></a>

#### Unenclosed VFD

[su_spoiler title="<strong>Unenclosed VFD</strong>" open="no" style="fancy" icon="chevron" anchor_in_url="yes"]

Fasten the VFD to the VFD mounting bracket using two (2) M5-16mm socket head screws and M5 nylock nuts. The VFD is fastened to the long flange of the mounting bracket.

**Note**: The side of the included custom wrench can be used to hold the nylock nuts while tightening.

<div markdown="1" style="width: 782px; max-width: 100%; margin-left: auto; margin-right: auto;">

![](/_images/_am/_assembly/am_assembly_spindle-install-1-850x478.jpg){.aligncenter}

</div>

<p style="text-align: center;"><em>Aligning holes between VFD unit and mounting bracket</em></p>

Fasten the VFD Mounting bracket to the inside of the **front left** table leg of the machine using two (2) M5-16mm socket head screws.

<div markdown="1" style="width: 722px; max-width: 100%; margin-left: auto; margin-right: auto;">

![](/_images/_am/_assembly/am_assembly_spindle-install-2-850x478.jpg){.alignnone .aligncenter}

</div>

<p style="text-align: center;"><i>VFD mounting bracket in position on front left table leg</i></p>

<div markdown="1" style="width: 711px; max-width: 100%; margin-left: auto; margin-right: auto;">

![](/_images/_am/_assembly/am_assembly_spindle-install-3-850x478.jpg){.alignnone .aligncenter}

</div>

<p style="text-align: center;"><em>VFD unit correctly mounted, control panel accessible through leg cutout </em></p>

[/su_spoiler]

Loosen the spindle clamping screws on the front of the spindle mount to allow the spindle to fit into the bore of the mount.

<div markdown="1" style="width: 629px; max-width: 100%; margin-left: auto; margin-right: auto;">

![](/_images/_am/_assembly/am_assembly_spindle-install-5-850x478.jpg){.alignnone .aligncenter}

</div>

<p style="text-align: center;"><em>Loosening clamping screws on spindle mount</em></p>

Place the styrofoam packaging on the front crossbeam of the table underneath the spindle mount. Adjust the height of the spindle mount, so that the distance from the bottom of the spindle mount to the top surface of the styrofoam is 110mm / 4.5 inches. Turn the ball screw using the motor coupler to adjust the height of the spindle mount.  Insert the spindle into the bore of the spindle mount until it rests on the top of the styrofoam.

<div markdown="1" style="width: 468px; max-width: 100%; margin-left: auto; margin-right: auto;">

![](/_images/_am/_assembly/am_assembly_spindle-install-6-850x478.jpg){.aligncenter}

</div>

<p style="text-align: center;"><em>Spindle mount height adjustment</em></p>

Fasten the two (2) spindle mount screws to secure the spindle in place.

Bring the spindle cable attached to the VFD around the back of the table leg, and moving from the front of the table to the back, bring the cable underneath the gantry, plugging the cable into the top of the spindle from the back of the gantry.

**Note:** It is **important** that this cable is routed in this path to allow it to be run through the drag chains.

**Note:** Match the keyed features on the cable connector with the slots of the spindle body receptacle, allowing the connector to mesh.

<div markdown="1" style="width: 850px; max-width: 100%; margin-left: auto; margin-right: auto;">

![](/_images/_am/_assembly/am_assembly_spindle-install-4-850x478.jpg){.alignnone .size-medium .aligncenter}

</div>

<div markdown="1" style="width: 850px; max-width: 100%; margin-left: auto; margin-right: auto;">

![](/_images/_am/_assembly/am_assembly_spindle-install-7-850x478.jpg){.size-medium .aligncenter}

</div>

<p style="text-align: center;"><i>Cable routing</i></p>

<div markdown="1" style="width: 639px; max-width: 100%; margin-left: auto; margin-right: auto;">

![](/_images/_am/_assembly/am_assembly_spindle-install-8-850x478.jpg){.alignnone .aligncenter}

</div>

<p style="text-align: center;"><i>Connector keys to mesh with spindle body receptacle</i></p>

Thread the connector onto the receptacle by rotating the collar on the cable side clockwise.  Pull on the connector to ensure it is secured.

<div markdown="1" style="width: 638px; max-width: 100%; margin-left: auto; margin-right: auto;">

![](/_images/_am/_assembly/am_assembly_spindle-install-9-850x478.jpg){.aligncenter}

</div>

<p style="text-align: center;"><em>Spindle cable collar threaded onto spindle connector </em></p>

Place the drag chain on the X rail. Fit the spindle cable and the Z-axis wire harness into the open drag chain. Press the clips down to secure the cables. To save on time, it is recommended to remove half the clips from the chain, in the case that you need to open the drag chain again.

**Note**: Check the drag chain ends to ensure they will interface correctly with the drag chain. Remember one link has a knobbed flange and the other a holed flange.

**Note:** Ensure the Z-axis wire harness is oriented such that the motor side connectors are exiting the drag chain opposite the X-axis motor.

<div markdown="1" style="width: 802px; max-width: 100%;">

![](/_images/_am/_assembly/am_assembly_x-drag-chain-layout.jpg){.alignnone}

</div>

<p style="text-align: center;"><em>Routing through X-axis drag chain</em></p>

<div markdown="1" style="width: 746px; max-width: 100%; margin-left: auto; margin-right: auto;">

![](/_images/_am/_assembly/am_assembly_x-drag-chain-clipping.jpg){.aligncenter}

</div>

Install the drag chain onto the drag chain end links.

<p style="text-align: center;"><em>X-axis drag chain secured on drag chain end link</em></p>

Place the drag chain on the left side Y-axis rail. Fit the X-axis wire harness, Z-axis wire harness, and spindle cable into the open drag chain. Press the clips down to secure the cables. To save on time, it is recommended to remove half the clips from the chain, in the case that you need to open the drag chain again.

**Note**: Check the drag chain ends to ensure they will interface correctly with the drag chain. Remember one link has a knobbed flange and the other a holed flange.

**Note:** Ensure the X-axis wire harness is oriented such that the motor side connectors are exiting the drag chain at the X-axis motor, not the opposite.

<div markdown="1" style="width: 2667px; max-width: 100%;">

![](/_images/_am/_assembly/am_assembly_y-drag-chain-layout.jpg){.alignnone .size-full}

</div>

<p style="text-align: center;"><em>Routing through the left Y-axis drag chain</em></p>

Install the drag chain onto the end links.

<div markdown="1" style="width: 732px; max-width: 100%;">

![](/_images/_am/_assembly/am_assembly_y-drag-chain-clipping.jpg){.alignnone}

</div>

<p style="text-align: center;"><em>Securing left Y-axis drag chain on drag chain end links</em></p>

<a id="sensor-and-motor-connections"></a>

### Sensor and Motor Connections

Plug the black connector exiting the X-axis wire harness into the plug of the inductive sensor.

Plug the power and signal connectors from the X-axis wire harness into the motor.

<div markdown="1" style="width: 590px; max-width: 100%;">

![](/_images/_am/_assembly/am_assembly_motorconnectorplugging.jpg){.alignnone}

</div>

<p style="text-align: center;"><em>X-axis power and signal connectors plugged in, sensor connector secured</em></p>

Use a small flathead screwdriver to fasten the screws of the power connector into the motor plug.

<div markdown="1" style="width: 545px; max-width: 100%;">

![](/_images/_am/_assembly/am_assembly_motorpowerconnectorscrew.jpg){.alignnone}

</div>

<p style="text-align: center;"><em>Tightly securing screws on power connector</em></p>

Remove the top-left and bottom-right M3 screws from the X-axis motor using the 2.5mm Allen-key provided in the M3-40mm socket head screw bag.

<div markdown="1" style="width: 681px; max-width: 100%;">

![](/_images/_am/_assembly/am_assembly_motorscrewremoval.jpg){.alignnone}

</div>

<p style="text-align: center;"><em>Removing 2 motor screws at a diagonal</em></p>

Install the motor cover onto the back of the motor using M3-40mm screws. Orient the motor cover so the wires exit upwards.

**Note:** Install the motor cover gently to avoid damaging the wires attached to the connectors.

<div markdown="1" style="width: 698px; max-width: 100%;">

![](/_images/_am/_assembly/am_assembly_motor-cover-install.jpg){.alignnone}

</div>

<div markdown="1" style="width: 695px; max-width: 100%;">

![](/_images/_am/_assembly/am_assembly_motorcoverscrew.jpg){.alignnone}

</div>

<p style="text-align: center;"><em>Motor cover installation</em></p>

Repeat the previous steps for the Z, Y1 and Y2 motors.

<div markdown="1" style="width: 634px; max-width: 100%;">

![](/_images/_am/_assembly/am_assembly_y1motorcoverscrews.jpg){.alignnone}

</div>

<p style="text-align: center;"><em>Assembling motor cover onto Y-axis</em></p>

<div markdown="1" style="width: 640px; max-width: 100%;">

![](/_images/_am/_assembly/am_assembly_motor-cover-z.jpg){.alignnone}

</div>

<p style="text-align: center;"><em>Assembling motor cover onto Z-axis</em></p>
