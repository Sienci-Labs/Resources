---
title: 5. Motors
menu_order: 6
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

![](/_images/_am/_assembly/am_assembly_mk2motorsheader-850x594.jpg){.aligncenter .size-medium}

</div>

<!-- R03-R04: Replace the parts-needed image with motors carrying pre-installed couplers and the supplied spacers. Add a spacer detail after Q-MOTOR-01 is resolved. -->

<div markdown="1" style="width: 4000px; max-width: 100%;">

![](/_images/_am/_assembly/am_assembly_motor-installation.jpg){.alignnone .size-full}

</div>

On newer kits, the three motor couplers are pre-installed and arrive with spacers between the motors and couplers. Use the older-kit instructions below only if your couplers were supplied separately.

<!-- Q-MOTOR-01: Confirm whether the supplied motor-coupler spacers stay in place or are removed, and at which step. Add that instruction before Motor Installation; do not infer spacer handling from the older-kit instructions. -->

[su_spoiler title="<strong>Older kits: Motor Coupler Installation</strong>" open="no" style="fancy" icon="chevron" anchor_in_url="no"]

<a id="motor-coupler-installation"></a>

### Motor Coupler Installation

The coupler has two different diameter bores: 8mm and 10mm. The 8mm bore fits onto the motor shaft. Install a coupler on each of the three (3) motors. Insert the coupler onto the motor shaft until the coupler bottoms out. <span style="color: #ff0000;"><strong>It’s important the motor coupler is fully seated, potential damage to the motor can happen with improper installation.</strong></span> Tighten the set screw on the motor side of the coupler to clamp the coupler to the shaft.

<div markdown="1" style="width: 664px; max-width: 100%; margin-left: auto; margin-right: auto;">

![](/_images/_am/_assembly/am_assembly_motors-install-1-1-850x407.jpg){.alignnone .aligncenter}

</div>

<p style="text-align: center;"><i>Motor shaft bottomed out inside coupler </i></p>

<div markdown="1" style="width: 708px; max-width: 100%; margin-left: auto; margin-right: auto;">

![](/_images/_am/_assembly/am_assembly_tighten-z-coupler-to-motor-1.jpg){.aligncenter}

</div>

<p style="text-align: center;"><em>Tighten coupler screw at motor end</em></p>

[/su_spoiler]

<a id="motor-installation"></a>

### Motor Installation

Install a motor with coupler onto the ball screw of the X-axis rail, and fasten the motor to the Y-axis Gantry Plate using four (4) M5-10mm socket head screws. **Orient** the motor such that the **DIP switches** are on the **bottom**.

<div markdown="1" style="width: 611px; max-width: 100%; margin-left: auto; margin-right: auto;">

![](/_images/_am/_assembly/am_assembly_x-axis-motor-install.jpg){.aligncenter}

</div>

<p style="text-align: center;"><em>Securely fastening motor onto X-axis ball screw</em></p>

<div markdown="1" style="width: 662px; max-width: 100%; margin-left: auto; margin-right: auto;">

![](/_images/_am/_assembly/am_assembly_x-axis-motor-positioning.jpg){.aligncenter}

</div>

<p style="text-align: center;"><i>X-axis Motor orientation</i></p>

Before tightening the motor coupler, ensure the motor is fully seated onto the y-axis gantry plate. **Potential damage** to the motor can occur if the motor is not fully seated before tightening. Clamp the coupler to the ball screw shaft by tightening the set screw on the shaft side.

<div markdown="1" style="width: 789px; max-width: 100%; margin-left: auto; margin-right: auto;">

![](/_images/_am/_assembly/am_assembly_x-axis-coupler-tightening-1.jpg){.aligncenter}

</div>

<p style="text-align: center;"><i>X-axis motor coupler clamping to ball screw</i></p>

Install the remaining two (2) motors onto the Y-axis ball screws, fastening the motors to the face of the Y-axis end plates using M5-10mm socket head screws. **Orient** the motor such that the **DIP switches** are on the **bottom**.

Before tightening, ensure each motor is fully seated against its rear Y-axis end plate. **Potential damage to the motor can occur if it is not fully seated before tightening.**

<div markdown="1" style="width: 960px; max-width: 100%; margin-left: auto; margin-right: auto;">

![](/_images/_am/_assembly/am_assembly_y-axis-motor-install-1.jpg){.size-full .aligncenter}

</div>

<p style="text-align: center;"><em>Securely fastening motor onto Y-axis</em></p>

<!-- Q-MOTOR-02: Confirm the revised snug/final-tightening sequence. The original final rear-end-plate tightening instruction is retained after coupler clamping pending Engineering confirmation. -->

With each motor aligned on its ball screw, bring the rear end plate flush against the Y-axis rail and tighten the end-plate screws until snug.

<!-- R05: Check this existing rear-end-plate illustration against the new sequence; it must show the motor already mounted. -->

<div markdown="1" style="width: 2560px; max-width: 100%;">

![](/_images/_am/_assembly/am_assembly_am4x4-fasten-back-scaled.jpg){.alignnone .size-full}

</div>

Ensure both halves of each motor coupler are seated against the rubber insert. Clamp the coupler to the ball screw shaft by tightening the clamping screw on the ball-screw side.

<!-- R06: Add or revise a coupler detail to show both halves seated against the rubber insert and the ball-screw-side clamping screw. -->

<div markdown="1" style="width: 960px; max-width: 100%;">

![](/_images/_am/_assembly/am_assembly_tightening-y-motor-coupler-on-ballscrew-1-1.jpg){.alignnone .size-full}

</div>

<p style="text-align: center;"><i>Y-axis motor coupler clamping to ball screw</i></p>

Finally, with the motors fully mounted, finish securing the back end plates on the table.

Now that we have our motors mounted, let’s do a final fit check. On both Y-axis sides, ensure that:

<span style="color: #ff0000;">1. The motor coupler is <b>centered </b>to the circular cutout on the Y-end plate</span>

<span style="color: #ff0000;">2. The table leg <b>does not</b> interfere with the Y-end plate</span>

Please re-assemble the table legs and Y-end plates until the components are properly aligned as specified in the check. You can loosen the fasteners, then slide the components into place before securing them again.

<a id="dip-switches"></a>

### Dip Switches

The motors should arrive with the DIP switches in the correct position for use with the AltMill stock settings.

Check to ensure the DIP switches on the X and Y axis motors follow the order of:

**1-5: OFF, OFF, OFF, ON, ON**

<div markdown="1" style="width: 960px; max-width: 100%; margin-left: auto; margin-right: auto;">

![](/_images/_am/_assembly/am_assembly_xz-dip-switch-final-view.jpg){.size-full .aligncenter}

</div>

<p style="text-align: center;"><em>Correct motor DIP switches setting for X and Y-axis</em></p>

Then set the Z-axis motor as follows from **1-5: OFF, OFF, ON, ON, ON**

<div markdown="1" style="width: 960px; max-width: 100%; margin-left: auto; margin-right: auto;">

![](/_images/_am/_assembly/am_assembly_z-dip-switch-final-view-1.jpg){.size-full .aligncenter}

</div>

<p style="text-align: center;"><em>Correct motor DIP switches setting for Z-axis</em></p>

 It is **highly recommended** that you **do not change** the firmware settings or DIP switch positions, unless you are instructed by Sienci Labs customer support or following instructions for installing another accessory.
