---
title: ytsb Inductive Sensors
menu_order: 4
post_status: draft
post_excerpt: Limit switches, end stops or homing switches are sensors that sit at one or both ends of each movement axis of a CNC. Repeatably locates the machine via homing.
post_date: 2024-04-30 17:20
taxonomy:
    knowledgebase_cat: lm-advanced
    knowledgebase_tag:
        - mk1
custom_fields:
    KBName: LongMill CNC
    basepress_post_icon: bp-caret-right
skip_file: no
featured_image: /_images/_longmill/_advanced/_4_Inductive/lm_inductive_p1_DSC00411-scaled.jpg
---
<h2>Installation</h2>

The Inductive Sensor Kit is a plug-and-play add-on kit for your LongMill, which adds three inductive sensors to your machine to act as limit and homing switches.<strong> The kit can be ordered on our <a href="https://sienci.com/product/inductive-sensor-kit/">store</a>. </strong>

https://www.youtube.com/watch?v=MZBsJED4Ktg

<h3>Step 1: Unpacking</h3>

Each kit comes with:

<ul>
  <li>10x M3-10mm socket head cap screws for mounting the brackets</li>
  <li>1x X-axis mounting bracket</li>
  <li>1x Y-axis mounting bracket</li>
  <li>1x Z-axis mounting bracket</li>
  <li>3x inductive sensors</li>
  <li>3x 0.1uF - (104) ceramic capacitors*</li>
</ul>

*These capacitors are only needed for LongBoards Rev 1.1 and Rev 1.2. If your LongBoard is Rev 1.3 and above, you will not need these and they can be set aside.

You will need for installation:

<ul>
  <li>2.5mm Allen key</li>
  <li>17mm wrench or adjustable wrench*</li>
</ul>

**All kits will have the inductive sensors pre-installed, a wrench is only needed if you wish to make tweaks to the placement of the sensors themselves.

![](/_images/_longmill/_advanced/_4_Inductive/lm_inductive_p1_DSC00411-scaled.jpg){.aligncenter .size-medium}

Before you begin, you can decide where to place your sensors, and which directions you would like to home the machine. You can always change this later, but by default, this guide will set up the sensors at the <b>lower left corner. </b>

Homing to the lower left corner is recommended because:

<ul>
  <li aria-level="1">This position is commonly used for your zero/origin point in projects, making it convenient for setting up jigs</li>
  <li aria-level="1">When squaring your machine by running the machine to the back, you will not run into the sensors</li>
</ul>

![](/_images/_longmill/_advanced/_4_Inductive/lm_inductive_p2_Corners-for-Homing.jpg){.aligncenter .size-medium}

<h3>Step 2: Attaching to the machine</h3>

Each bracket uses a pair of M3 screws to mount to the machine. Simply slide the bracket onto the recommended location and gently tighten the M3 screws using a 2.5mm Allen key into the brass heat-set nuts just until snug. <strong>Do not over tighten, as this could damage the bracket</strong>, but ensure that the bracket cannot move easily

<strong>The tabs below show the attachment of limit switches for homing at the lower left corner. </strong>If you choose to home at another corner, you can rearrange the X and Y sensor mounts, mirroring what is shown below. Some positions may require you to flip the sensor.

[tabby title="X-Axis" open="yes"]

<h4>X-Axis Mounting</h4>

Place the X-axis sensor on the top of the left steel Y-gantry plate, sitting against the aluminum rail. The sensor should be triggered by the X-gantry plate when in contact.

![](/_images/_longmill/_advanced/_4_Inductive/lm_inductive_p3_Combined.png "X-axis sensor alignment"){.aligncenter .size-medium}

<strong>X-Axis mounting with non-magnetic dust shoe</strong>

If your machine is installed with an older style dust shoe that utilizes aluminum extrusions and a wooden base, you will need to install an add-on X-axis dust shoe 'flag' to ensure the X-axis sensor will trigger.

Loosen the smaller (M5) screw on the flag and slide the flag onto the front slot of the left aluminum extrusion as shown. Adjust the height of where the flag sits, as well as the position of the X-axis sensor on the gantry plate so that the sensor is aligned with the larger (M8) screw on the flag.

![](/_images/_longmill/_advanced/_4_Inductive/lm_inductive_p4_DSC00358-scaled.jpg "X-axis dust shoe flag alignment"){.aligncenter .size-medium}

[tabby title="Y-Axis"]

<h4>Y-Axis Mounting</h4>

Slide the Y-axis sensor onto the front left 3D printed foot. The mounting tab of the sensor must line up with the edge of the extrusion, and the Y-gantry should be in the center of the mount hole.

![](/_images/_longmill/_advanced/_4_Inductive/lm_inductive_p3YAxis_Combined.png "Y-axis sensor alignment"){.aligncenter .size-medium}

[tabby title="Z-Axis"]

<h4>Z-Axis Mounting</h4>

Slide the Z-axis sensor mount on the top end of the left of the Z-axis, ensuring the mount is pressed against the linear guide as far as it can go. For older models (V1), you will need to remove the lower nut on the inductive sensor before the mount can be slid on. Once the mount is affixed, you can then add and tighten the sensor nut.

Depending on the machine version, you may need to adjust how far the sensor extends down. For newer models (V2-V4) with the notch at the top of the Z-axis gantry plate, the sensor sits at the upper position as shown, triggering before the M5 screw hits the ACME nut. For older models (V1) with the flat top Z-axis gantry plate, the sensor will need to be moved upwards as shown. Make sure that the sensor triggers before the machine hits the 3D printed Z-axis mount.

![](/_images/_longmill/_advanced/_4_Inductive/lm_inductive_p3ZAxis_Combined.png "New (Left) and Old (Right) Limit Switch Positions"){.aligncenter .size-medium}

[tabbyending]

<h3>Step 3: Adjusting the sensors on the brackets</h3>

All three inductive sensors are identical and are mounted to the brackets to allow for installation onto the machine. However, you can adjust them if you want to tweak the location of the sensors.

To adjust the position of a sensor:

<ol>
  <li aria-level="1">Remove one nut and washer from each sensor and set it aside</li>
  <li aria-level="1">Slide the sensor through the hole of each mount</li>
  <li aria-level="1">Reinstall the nut and washer to secure the sensor in place on the bracket. Note that the Z-axis sensor does not use a washer on the lower nut</li>
</ol>

<h3>Step 4: Connecting the sensors to the LongBoard controller</h3>

Unclip the tabs that hold the wires in each drag chain and route the cables from the inductive sensors. Ensure that there are no sharp bends or tears in the cables as a failed limit sensor could cause a false alarm and halt the machine during use.

<ul>
  <li aria-level="1">Z-axis sensor gets routed through the drag chains on the X and Y rail</li>
  <li aria-level="1">X-axis sensor gets routed through the drag chain on  the Y-axis only</li>
  <li aria-level="1">Y-axis sensor does not need to be routed through a drag chain</li>
</ul>

The three cables plug into the three white JST connectors labelled as XLim, YLim, ZLim as shown in the photo below. To make sure each of the sensors is plugged into the correct port for its axis, it is recommended to label the cable with tape and marker before routing the cables, or plug-in each cable as they are routed through the machine individually.

![](/_images/_longmill/_advanced/_4_Inductive/lm_inductive_p5_DSC00432.jpg "X, Y and Z sensors plugged into LongBoard"){.aligncenter .size-medium}

Once installed, you can verify that each sensor is working and is plugged into the correct port by using the console within UGS, gSender, or other machine interface software. Type the following command into the console: <b>*$10=19*</b><span style="font-weight: 400;"> and press enter. This will enable reporting of the current status of each of the sensors.
</span>

You can either jog the machine to trigger the sensor (shown by a red light on the sensor), or hold anything made of steel in front of the sensor. While the sensor is triggered, enter the following command into the console: <b>*?*</b>

![](/_images/_longmill/_advanced/_4_Inductive/lm_inductive_p6_limitswitch.png){.aligncenter .size-medium}

The console will now report back to you which limit sensor is triggered, indicated by an X, Y, or Z. Check this for each of the three sensors/axis to make sure the axis sensor reported matches the axis of the sensor you are manually triggering. If the reported triggered sensor does not match the sensor you are triggering, swap the cable plugs at the board as necessary so they all match. This can also be very useful for diagnosing issues with your sensors.

After you’ve finished checking that each sensor is reporting correctly, you can set disable sensor status reporting by setting the default value: <b>*$10=3*</b>

<h4>Adding capacitors for LongBoard revision 1.2</h4>

Look on the top of your LongBoard to see the revision number just below the Sienci Labs logo. LongBoard revisions 1.3 and 1.4 come preinstalled with capacitors for each of the limit switch circuits. <b>If your board is revision 1.3 or 1.4, you can set aside the included capacitors and skip to Step 5</b>. If your LongBoard is revision 1.2, however, it does not come pre-installed with capacitors and may be subject to triggering falsely due to electrical noise. Therefore, each kit includes a set of 0.1 mF ceramic non-polarized capacitors to filter out any electrical noise. The capacitors used are shown below.

![](/_images/_longmill/_advanced/_4_Inductive/lm_inductive_p7_Combined.png)

Remove the green 5 port connector installed in the '5V, Xlim, Ylim, Zlim, GND' port on the LongBoard. Then loosen the screw terminals of the connector and insert three capacitors into the connector as shown in the photo above. For each capacitor, one prong should be inserted to the GND port, and one prong into the X, Y, or Z port. Re-tighten each of the screw terminals on the connector then plug the connector back into the secondary limit switch port.

Plug in the X, Y, and Z axis limit switch connectors into each of the three white connectors as shown in the photo above.

<h3>Step 5: Changing your settings for limit switches</h3>

If you received your machine before September 2021, you may need to update your LongMill's firmware to the latest version to have access to all of the updates for your limit switches to work. At the time of writing, the latest version of the LongMill firmware is Sept 8, 2021.

To update your firmware, connect your machine to gSender, click on "Firmware", and click on the "Flash grbl" button. Follow the prompts to install the latest version of the firmware onto your LongBoard.

![](/_images/_longmill/_advanced/_4_Inductive/lm_inductive_p8_gSenderfirmware.png){.aligncenter .size-medium}

Next, import our default EEPROM settings for your machine. Press “Restore Defaults” at the “Firmware” window.  with limit switches. Use the "Import Settings" tool and update your EEPROM settings to the new defaults (link to download file coming soon). If you wish to make changes or adjustments, additional info about changing your EEPROM settings can be found further down on this page.

![](/_images/_longmill/_advanced/_4_Inductive/lm_inductive_p9_gSender-restore-eeporm.png){.aligncenter .size-medium}

<b>Recommended settings</b><b> for sensors</b>

Now that we’re working with the default settings, we will modify a few to make them work with the sensors.

<ul>
  <li aria-level="1">Hard and soft limits ON</li>
  <li aria-level="1">Homing cycle ON</li>
  <li aria-level="1">Homing direction invert</li>
  <li aria-level="1">X and Y axis travel limits CHANGED</li>
</ul>

<h4><b>Hard limits, soft limits, homing cycle, and homing direction</b></h4>

We recommend to turn ON $20, $21 and $22 on your firmware settings.

![](</_images/_longmill/_advanced/_4_Inductive/lm_inductive_p10_ gSender-lim-switch-firmware.png> "$20, $21 and $22 settings must be enabled"){.aligncenter .size-medium}

<b>What do these do? </b>

$20 - Soft limits enable and $21 - Hard limits enable

Both soft limits and hard limits will stop the machine if it is moving to the boundaries of the machine. However, soft limits determines when to stop using calculations in the software program, NOT by triggers at the sensor. Hard limits determines when to stop from the trigger of the sensors

We recommend using both, so that one end of the machine is constrained by hard limits (bottom and left directions) and the other end is constrained by soft limits. You may get error messages if you are trying to move past the boundaries. If so, try jogging the machine away from machine boundaries, or jog at a smaller distance when near boundaries.

$22 - Homing cycle enable

By enabling the homing cycle, you are able to home your machine with the sensors. So each time you connect to gSender, it will prompt you to home your machine (showing a red alarm). This is a safety feature, to check that the sensors are working and to ensure your machine will move within bounds. You can click on the lock icon in the top left corner to unlock your machine and skip this step if you wish.

![](/_images/_longmill/_advanced/_4_Inductive/lm_inductive_p11_Mk1homing.jpg){.aligncenter .size-medium}

If you want to set your home at the front left corner and have installed your inductive sensors thus, you will need to invert your X and Y axis.

![](/_images/_longmill/_advanced/_4_Inductive/lm_inductive_p12_HomingFrontLeft.jpg){.aligncenter .size-medium}

<b>X and Y travel limits</b>

We recommend that $130 = 750.000 and $131 = 810.000 on your firmware settings.

![](/_images/_longmill/_advanced/_4_Inductive/lm_inductive_p13_gSenderlimswitch.png "$130 and $131 must be changed"){.aligncenter .size-medium}

<b>What do these do? </b>

$130 and $131 are the travel limits for the X and Y-axis. For the 30x30 LongMill with the magnetic dust shoe, a maximum travel of 750mm in the X-direction and 810mm in the Y-direction is suitable, however, these will be different for smaller machines, any modifications or different accessories.

If you need to find the maximum travel for your unique setup do the following (optional); home your machine, zero all axes, then jog each axis to where you feel comfortable limiting it. Use the coordinates to set your maximum travel for each axis.

<h3>Step 6: Using your sensors</h3>

At this stage, you're ready to start using your sensors.

<h4>Testing limit switches</h4>

Once the firmware changes have been made, test the sensors. Disconnect, then reconnect to your machine. You should see the red alarm at the top right, press “Click to Run Homing.”

![](</_images/_longmill/_advanced/_4_Inductive/lm_inductive_p14_ gsenderalarmstate.png>){.aligncenter .size-medium}

On gSender, the process for limit switch homing is very similar to touch plate probing. This is what happens on the LongMill when you run the homing cycle:

<ol>
  <li aria-level="1">Machine moves up quickly in the Z-axis, until the switch gets triggered</li>
  <li aria-level="1">Machine retracts slightly, moves up slowly in the Z-axis, until switch gets triggered again</li>
  <li aria-level="1">Machine quickly moves diagonally across table to upper right corner, until the switch gets triggered</li>
  <li aria-level="1">Machine retracts slightly, slowly moves diagonally across table to upper right corner, until switch gets triggered again</li>
</ol>

If this process completes without any errors, you have successfully homed your machine!

<h4><b>Homing features</b></h4>

Once you have connected to your machine, at any point when you aren’t running a cutting job, you can run the homing cycle by pressing “Home” with the house icon.

![](/_images/_longmill/_advanced/_4_Inductive/lm_inductive_p15_limitswitchhoming.png){.aligncenter .size-medium}

Additionally, if you first connect and need to bypass the alarm without homing, you can by pressing the “Unlock” yellow padlock button on the top left of the visualizer screen. We do not recommend this usually, because it is safer to home first before running a cutting job.

![](/_images/_longmill/_advanced/_4_Inductive/lm_inductive_p16_gsendeunlock.png){.aligncenter .size-medium}

<h4><b>Work offsets</b></h4>

With CNC, work offsets can be thought of as bookmarks. They are saved origin positions on your machine that allow you to always return later to a known location. Having one or more known locations you can repeatedly return to is extremely useful for many reasons such as:

<ul>
  <li aria-level="1">Restarting a failed job</li>
  <li aria-level="1">Recovering from a power outage during a job</li>
  <li aria-level="1">Repeating a job in a fixture or multiple fixtures</li>
  <li aria-level="1">Returning to an exact work XY origin after performing a tool change</li>
</ul>

The repeatability of the inductive limit switches has been tested to be less than 0.001”, meaning that you will always be able to return to your original work origin within 0.001” accuracy, and can confidently repeat jobs without worries of toolpath misalignment or crashes.

To change work offsets or workspaces, simply select one of the 6 workspaces from the drop-down list in the top right corner of gSender as shown in the photo below.

![](/_images/_longmill/_advanced/_4_Inductive/lm_inductive_p17_gsenderworkspaces.png "Workspaces to choose from"){.aligncenter .size-medium}

Alternatively, entering the command G54, G55, G56.. etc. into the console of gSender or UGS will tell the machine to switch into that workspace. You will notice the work coordinates (blue numbers) will change upon switching workspaces to whatever the coordinates are within the new workspace. The machine coordinates (grey numbers) will always remain the same regardless, as these are of course relative to your machine's home position.

All 6 of these workspaces are modal settings, meaning they will be saved by the controller even after powering off the machine.
