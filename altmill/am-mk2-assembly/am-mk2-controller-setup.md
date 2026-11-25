---
title: 8. Controller Setup
menu_order: 9
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

![](/_images/_am/_assembly/am_assembly_mk2controllersetupheader-850x594.jpg){.aligncenter .size-medium}

</div>

<div markdown="1" style="width: 850px; max-width: 100%; margin-left: auto; margin-right: auto;">

![](/_images/_am/_assembly/am_assembly_controller-setup-v2-1500x-850x350.jpg){.aligncenter .size-medium}

</div>

If you already mounted the E-stop during the enclosed-VFD installation, leave it installed and continue with removing the controller’s acrylic face plate below. Use the mounting instructions here only if the E-stop is not yet installed.

The E-stop is located in the SLB-EXT box.

Fasten the E-stop to the VFD Mounting Bracket on the side of the left table leg, using two (2) M5-16mm socket head screws.

**If** you did not purchase the Spindle Kit, you will use the E-stop mounting plate provided in the SLB-EXT box to fasten the E-stop to the side of the left table leg. The E-stop Mounting plate is inserted into the left pocket from the inside of the Table Leg with the two holes oriented toward the back of the machine.

<div markdown="1" style="width: 1024px; max-width: 100%; margin-left: auto; margin-right: auto;">

![](/_images/_am/_assembly/am_assembly_controller-setup-1-1024x576.jpg){.aligncenter .size-large}

</div>

<p style="text-align: center;"><em>Fastening E-stop into E-stop mounting bracket<br/>
</em></p>

Insert M5 nylock nuts into the E-stop mounting plate. Use two M5-16mm socket head screws to fasten the E-stop to the mounting plate.

<div markdown="1" style="width: 506px; max-width: 100%;">

![](/_images/_am/_assembly/am_assembly_e-stop-mount-nut-install.jpg){.alignnone}

</div>

<p style="text-align: center;"><i>Nylock nuts into E-stop mounting plate</i></p>

<div markdown="1" style="width: 3555px; max-width: 100%;">

![](/_images/_am/_assembly/am_assembly_install-e-stop-1.jpg){.alignnone .size-full}

</div>

<p style="text-align: center;"><i>E-stop installed on left side table leg</i></p>

Loosen the thumb screw on the front of the SLB-EXT enclosure and remove the acrylic face plate.

<!-- Q-CONTROLLER-01: Sequence is grounded in the published SLB-EXT port maps (right-to-left X, Y1, Y2, Z). Confirm the target board revision and the proposed right-to-left POWER-port assignment before publication. No SLB-EXT V2/HV change is assumed; the source PDF’s Y3 was corrected to Z. -->

Connect one complete motor harness at a time, beginning with X, then Y1, Y2 and Z. Identify each harness by its axis label. On the SLB-EXT illustrated below, the motor-control and sensor pairs run from right to left in that order; follow the printed port labels when making each connection.

Route the X and Z harnesses through the top cutout on the right side of the enclosure. Route the Y1 and Y2 harnesses through the bottom cutout on that side.

1. **X:** Plug the green two-pronged motor-power connector into an available port in the MOTOR POWER bank, then plug the black motor-control connector into X and the white sensor connector into X LIM.
2. **Y1:** Connect the green motor-power plug to the next available MOTOR POWER port, the black motor-control plug to Y1, and the white sensor plug to Y1 LIM.
3. **Y2:** Connect the green motor-power plug to the next available MOTOR POWER port, the black motor-control plug to Y2, and the white sensor plug to Y2 LIM.
4. **Z:** Connect the green motor-power plug to the remaining MOTOR POWER port, the black motor-control plug to Z, and the white sensor plug to Z LIM.

The four motor-power ports supply the same output. The motor-control and sensor ports are axis-specific: match the printed axis labels and connector shapes as well as the colours.

<div markdown="1" style="width: 960px; max-width: 100%;">

![](/_images/_am/_assembly/am_assembly_x-and-z-signal-cables-slb-ext.jpg){.alignnone .size-full}

</div>

<p style="text-align: center;"><em>SLB-EXT port reference: X and Z signal ports and the motor-power bank</em></p>

**For Y1 and Y2, do not mix the motor-control connector from one harness with the sensor connector from the other.** Keep each harness connected to its matching Y1 or Y2 port pair. Incorrect pairing can cause an alarm during operation.

<div markdown="1" style="width: 960px; max-width: 100%;">

![](/_images/_am/_assembly/am_assembly_y1-and-y2-signal-cables-slb-ext.jpg){.alignnone .size-full}

</div>

<p style="text-align: center;"><em>SLB-EXT port reference: keep each Y motor-control and sensor pair together</em></p>

<!-- R08-R10: Refresh controller artwork for the confirmed board revision: labelled port overview, complete X harness, and completed four-harness wiring. Existing port references are retained; this final image still uses the older power-cable layout. -->

<div markdown="1" style="width: 2667px; max-width: 100%;">

![](/_images/_am/_assembly/am_assembly_y1y2-motor-cable-plugging.jpg){.alignnone .size-full}

</div>

<p style="text-align: center;"><em>Completed controller wiring</em></p>

Reinstall the acrylic face plate of the SLB-EXT onto the enclosure. Tighten the thumb screw by hand.

<div markdown="1" style="width: 2667px; max-width: 100%;">

![](/_images/_am/_assembly/am_assembly_extacryliccover.jpg){.alignnone .size-full}

</div>

<div markdown="1" style="width: 2667px; max-width: 100%;">

![](/_images/_am/_assembly/am_assembly_extacryliccoverthumbscrew.jpg){.alignnone .size-full}

</div>

<p style="text-align: center;"><em>Reinstalling acrylic cover</em></p>

Plug the green connector of the E-stop cable into the port labeled E-stop on the right side of the controller, and the other side of the cable into the E-stop.

<div markdown="1" style="width: 2667px; max-width: 100%;">

![](/_images/_am/_assembly/am_assembly_estopconnectorext.jpg){.alignnone .size-full}

</div>

<p style="text-align: center;"><em>Green connector plugged into controller</em></p>

<div markdown="1" style="width: 1024px; max-width: 100%; margin-left: auto; margin-right: auto;">

![](/_images/_am/_assembly/am_assembly_controller-setup-14-1024x683.jpg){.aligncenter .size-large}

</div>

<p style="text-align: center;"><em>Jack connector plugged into E-stop</em></p>

**If** you have installed the Sienci Labs Spindle Kit, plug the clear connector of the spindle control cable that is attached to the VFD unit, and plug this into the port labelled **‘RS485’** on the left side of the controller.

**If** you’re installing your own spindle, you may need to connect your own spindle control cable as explained [here](https://resources.sienci.com/view/slb-manual/#spindlers485).

<div markdown="1" style="width: 2666px; max-width: 100%; margin-left: auto; margin-right: auto;">

![](/_images/_am/_assembly/am_assembly_rs485plugext.jpg){.alignnone .size-full .aligncenter}

</div>

<p style="text-align: center;"><em>Plugging spindle control connector into RS485 port</em></p>

Plug the green connector of the 48V power supply into the port labelled **Power**.

Plug the power supply into a 110V outlet.

<div markdown="1" style="width: 2667px; max-width: 100%;">

![](/_images/_am/_assembly/am_assembly_powerconnectorext.jpg){.alignnone .size-full}

</div>

<p style="text-align: center;"><em>Power supply connector into SLB-EXT</em></p>

The machine is now put together and you can move onto your first movements. Congratulations!
