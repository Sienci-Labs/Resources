---
title: ytsb Changing Microstepping
menu_order: 6
post_status: draft
post_excerpt: How to change microstepping on the LongMill Benchtop CNC to improve accuracy in machine movement. This will cause motors to move more or less per signal.
post_date: 2022-03-18 00:15:00
taxonomy:
    knowledgebase_cat: lmk2-advanced
    knowledgebase_tag:
        - mk2
custom_fields:
    KBName: LongMill MK2 CNC
    basepress_post_icon: bp-caret-right
skip_file: yes
featured_image: /_images/_longmill/_advanced/lm_Stepper_p1.jpg
---

Every LongMill is powered by our LongBoard CNC controller which has four integrated TB6600 stepper motor drivers (pictured). By default, we set each driver to 1/8 microstepping via the onboard DIP switches. We chose 1/8 microstepping because we found that it's a good balance between motor resolution and torque output. The theoretical resolution with this setup is 0.005mm.

![](/_images/_longmill/_advanced/lm_Stepper_p1.jpg){.aligncenter .size-medium}

## What is Microstepping

Stepper motors have a fixed number of steps in their internal rotor which determine the steps required to make a full, 360-degree rotation. With these steps in mind, the controller drivers can "step" forward or backward however many times to rotate each axis motor. The NEMA 23s used on the LongMill are split up to 200 individual steps. This might seem like a lot, but in many cases more accurate control is still needed.

Microstepping is a technique that allows for steps to be broken down into 'sub-steps' so that the stepping resolution can be increased. This allows us to:

- Have a smoother movement in the motors themselves
- Improve positional accuracy (read more here: <a href="https://hackaday.com/2016/08/29/how-accurate-is-microstepping-really/" target="_blank" rel="noopener">https://hackaday.com/2016/08/29/how-accurate-is-microstepping-really/</a> )

## Current Values

The steps/mm EEPROM settings in the LongMill (<em>$100, </em><em>$101, </em>and <em>$102</em>) are set to 200. This value helps the controller turn g-code into linear movements, then into rotational step signals for the motors. This number comes from taking the values below and running them through the formula:

- LongMill stepper motors are **200** steps/rotation
- Drivers set to **1/8** microstepping by default
- MK1 LongMills: X and Y-axes are direct drive and the Z-axis has **1-to-1** pulley ratio
- MK2 LongMills: all axes are direct drive
- Our lead screws have a **2mm** pitch and are **4-start**, 2mm x 4 = 8mm **lead**

<em>Steps/mm  =   Steps/revolution</em><em>  </em><b>/</b><em>  (microstepping value  </em>x<em>  gearing ratio from motor to lead screw  </em>x<em>  lead screw pitch  </em>x<em>  # of starts)</em>

This gives us:  200  /  (1/8  x  1  x  2  x  4)  =  <em>200 steps/mm</em>

## Changing Microstepping

If you'd like to change your machines microstepping values, you'll have to:

1. Change the positions of the desired drivers onboard DIP switches and
1. Set the EEPROM setting to match.

For example, changing the Z-axis driver to have 1/16 microstepping would require following the table below and then in your g-code sender console sending the command "<em>$102  = 400</em>" to set the appropriate steps/mm of the Z-axis.

Each driver can be adjusted to use either single-step or 1/2 step, 1/4 step, 1/8 step, and 1/16 step microstepping. Bear in mind that changes to the DIP switches should only be made when your LongMill is powered off. Also, understand that if you play with microstepping you'll find that positional resolution and torque tend to be inversely proportional.

<table class="wp-table" width="50%">
<tbody>
<tr>
<td> </td>
<td>M1</td>
<td>M2</td>
<td>M3</td>
</tr>
<tr>
<td>1 Step</td>
<td>OFF</td>
<td>OFF</td>
<td>ON</td>
</tr>
<tr>
<td>1/2 Step</td>
<td>OFF</td>
<td>ON</td>
<td>OFF</td>
</tr>
<tr>
<td>1/4 Step</td>
<td>ON</td>
<td>OFF</td>
<td>OFF</td>
</tr>
<tr>
<td>1/8 Step</td>
<td>ON</td>
<td>OFF</td>
<td>ON</td>
</tr>
<tr>
<td>1/16 Step</td>
<td>ON</td>
<td>ON</td>
<td>OFF</td>
</tr>
</tbody>
</table>
