---
title: ytsb Electronics - Closed Loop Motor
menu_order: 6
post_status: draft
post_excerpt: 
post_date: 2024-09-12 11:35:18
taxonomy:
    knowledgebase_cat: vx-assembly
    knowledgebase_tag:
        - vortex
custom_fields:
    KBName: Vortex Rotary Axis
    basepress_post_icon: bp-caret-right
skip_file: no
featured_image: _images/post-image.jpg
---

<span style="color: #d22329;">Follow these instructions if you're assembling a Vortex rotary axis kit which utilizes a closed loop motor with two motor cable connections.</span>

You can refer to the video below for a general overview of the setup process. Scroll down for detailed, step by step directions with images.

https://www.youtube.com/watch?v=7-bYcXlZZqw

### Wiring Installation

Grab the motor cable included in the Vortex rotary axis kit and plug the two green connectors into their respective plugs on the rear of the closed loop motor. Tighten the two small screws on the 2 pin power connector using a small flathead screwdriver.

<img class="aligncenter size-medium wp-image-10530" src="https://resources.sienci.com/wp-content/uploads/2023/08/9.1_CLS-Motor-Wire-850x532.jpg" alt="" width="850" height="532" />

<p style="text-align: center;"><em>Plugging in connections on the closed loop motor</em></p>

**For the SLB-EXT:**

Plug in the power, limit switch and driver connectors into their appropriate locations as shown below.

<img class="size-full wp-image-11146 aligncenter" src="https://resources.sienci.com/wp-content/uploads/2024/09/A-axis-plug-closed-loop-SLB-ext.png" alt="" width="960" height="540" />

<p style="text-align: center;"><em>A-axis connections to the SLB-EXT (AltMill)</em></p>

**For the SLB:**

Make the motor driver and limit switch connections as shown.

<img class="size-full wp-image-11152 aligncenter" src="https://resources.sienci.com/wp-content/uploads/2024/09/SLB-motor-driver-limit-connect.png" alt="" width="960" height="540" />

<p style="text-align: center;"><em>A-axis connections to the SLB (LongMill)</em></p>

Plug the power splitter into the external power supply that comes with your controller.

<img class="size-full wp-image-11147 aligncenter" src="https://resources.sienci.com/wp-content/uploads/2024/09/power-splitter.png" alt="" width="960" height="540" />

<p style="text-align: center;"><em>Power splitter for the SLB A-axis connections</em></p>

The two green connectors will be distinctly different, so you can make the appropriate connections to power the controller and the A-axis.

<img class="size-full wp-image-11148 aligncenter" src="https://resources.sienci.com/wp-content/uploads/2024/09/power-to-board-using-splitter.png" alt="" width="960" height="540" />

<p style="text-align: center;"><em>Connect power splitter to POWER input on the side of the SLB</em></p>

<img class="size-full wp-image-11150 aligncenter" src="https://resources.sienci.com/wp-content/uploads/2024/09/vortex-power-splitter-connect.png" alt="" width="960" height="540" />

<p style="text-align: center;"><em>Plug the other end of the splitter to Vortex power connector</em></p>

<img class="alignnone size-full wp-image-11241" src="https://resources.sienci.com/wp-content/uploads/2024/09/SLBCLSSplitterWiring.png" alt="" width="2587" height="2550" />

<p style="text-align: center;"><em>Power splitter wiring overview</em></p>

### Firmware Settings

#### gSender 1.5.0 and above

[su_spoiler title="<strong>gSender 1.5.0 and above</strong>" open="yes" style="fancy" icon="chevron" anchor_in_url="yes"]

Next, we will need to change the firmware settings to work with closed loop rotary axis.

Go to Config, then use the search bar to find the following settings:

**$4 Invert stepper enable pins →** toggle **A** to be **ON** (do not adjust X, Y, Z settings)

<img class="alignnone wp-image-15449 size-full" src="https://resources.sienci.com/wp-content/uploads/2024/09/invert-stepper-4-e1757613663165.png" alt="" width="960" height="339" />

**$21 Hard limits enable →** toggle **Enable** to be **OFF**

<img class="alignnone wp-image-15450 size-full" src="https://resources.sienci.com/wp-content/uploads/2024/09/hard-limits-disable-21-e1757613853826.png" alt="" width="960" height="296" />

**$22 Homing cycle → match the toggles** as shown

<img class="alignnone size-full wp-image-15451" src="https://resources.sienci.com/wp-content/uploads/2024/09/homing-cycle-22-e1757614143121.png" alt="" width="960" height="469" />

**$37 Steppers deenergize →** toggle **A** to be **ON**

<img class="alignnone size-full wp-image-15452" src="https://resources.sienci.com/wp-content/uploads/2024/09/steppers-deenergize-37-e1757614337709.png" alt="" width="960" height="342" />

Once you have made these changes, press '**Apply Settings**'.

Go back to the main 'Carve' page.

At the bottom right of the screen, select Console.

Type in **$103 = 79.012345679** then press **Run**

<img class="alignnone size-full wp-image-11170" src="https://resources.sienci.com/wp-content/uploads/2025/07/103-entered-1.jpg" alt="" width="960" height="540" />

Power OFF then ON the control board so that all the changes will take effect.

<img class="size-full wp-image-10826 aligncenter" src="https://resources.sienci.com/wp-content/uploads/2021/12/power-cycle-laser.png" alt="" width="960" height="540" />

[/su_spoiler]

#### gSender 1.4.12 and below

[su_spoiler title="<strong>gSender 1.4.12 and below</strong>" open="no" style="fancy" icon="chevron" anchor_in_url="yes"]

Next, we will need to change the firmware settings to work with closed loop rotary axis.

On the Firmware Tool, make the following changes and press "Apply New Settings":

<img class="alignnone size-medium wp-image-15133" src="https://resources.sienci.com/wp-content/uploads/2024/09/4-1-850x228.png" alt="" width="850" height="228" />

<p style="text-align: center;"><em>$4 - A toggle is ON, DO NOT TOUCH XYZ</em></p>

<p style="text-align: center;"><img class="alignnone size-full wp-image-11168" src="https://resources.sienci.com/wp-content/uploads/2024/09/21.png" alt="" width="959" height="186" /></p>

<p style="text-align: center;"><em>$21 - Enable is OFF</em></p>

&nbsp;

<img class="aligncenter wp-image-11164 " src="https://resources.sienci.com/wp-content/uploads/2024/09/Screen-Shot-2024-10-09-at-12.30.11-PM-e1728491451841.png" alt="" width="754" height="376" />

<p style="text-align: center;"><em>$22 - Enable ON, Enable single axis commands ON, Homing on startup required ON, Set machine origin to 0 ON, Override locks ON.</em></p>

Ensure you enable the following setting. The closed-loop stepper motors need to be power to the motors before receiving a move command. If you are experiencing a delay when jogging the A-Axis, it's likely A hasn't been toggled on.

<img class="alignnone size-full wp-image-11166" src="https://resources.sienci.com/wp-content/uploads/2024/09/37.png" alt="" width="957" height="206" />

<p style="text-align: center;"><em>$37 - A toggle is ON.</em></p>

LongMill customers with spindles are recommended to enable the Z axis for <strong class="guide-markup">37 Steppers deenergize.</strong> When using the spindle kit with the vortex the following settings are:

<img class="aligncenter size-full wp-image-13978" src="https://resources.sienci.com/wp-content/uploads/2024/09/steppers-deenergize-spindle-vortex.png" alt="" width="795" height="194" />

<p style="text-align: center;"><em>$37 - A &amp; Z toggle is ON.</em></p>

One the settings are saved, go to the Console on the main gSender window. Type in **$103 = 79.012345679** then press "Run"

<img class="alignnone size-full wp-image-11170" src="https://resources.sienci.com/wp-content/uploads/2025/07/103-entered-1.jpg" alt="" width="960" height="540" />

<p style="text-align: center;"><em>Manually enter setting $103 on the Console tab</em></p>

Power OFF then ON the control board so that all the changes are updated in the Firmware Tool.

<img class="size-full wp-image-10826 aligncenter" src="https://resources.sienci.com/wp-content/uploads/2021/12/power-cycle-laser.png" alt="" width="960" height="540" />

<p style="text-align: center;"><em>Switch OFF then ON on the SLB and SLB-EXT</em></p>

[/su_spoiler]

### Motor Check

Check the dip switches on the back of the closed-loop stepper motor to ensure they are set to the correct settings. Use a small tool to seat the small switches. The switches should be:

<p style="text-align: center;">1 - ON, 2-ON, 3-ON, 4-OFF, 5-ON</p>

<img class="aligncenter size-full wp-image-13755" src="https://resources.sienci.com/wp-content/uploads/2024/09/Vortex-CLS-settings.png" alt="closed-loop stepper motor dip switch position for sienci labs Vortex" width="833" height="624" />

<p style="text-align: center;"><em>Vortex Closed-Loop Dip Switch Position</em></p>

**Congratulations!** A job well done, you've completed the assembly and firmware steps. Take a deep breath, we are almost ready for a test drive.
