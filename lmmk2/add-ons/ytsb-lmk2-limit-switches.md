---
title: ytsb Limit Switches ⛔
menu_order: 3
post_status: draft
post_excerpt: See how to mount and wire custom limit switches or the inductive limit switch kit to the LongMill MK2. See how limit switches work and if they're for you.
post_date: 2022-03-17 20:23:00
taxonomy:
    knowledgebase_cat: lmk2-add-ons
    knowledgebase_tag:
        - mk2
custom_fields:
    KBName: LongMill MK2 CNC
    basepress_post_icon: bp-caret-right
skip_file: yes
featured_image: 
---

The Inductive Sensor Kit is a plug-and-play add-on kit for your LongMill, which adds three inductive sensors to your machine to act as limit and homing switches. **The kit can be ordered on our <a href="https://sienci.com/product/inductive-sensor-kit/">store</a>.**

https://www.YouTube.com/watch?v=MZBsJED4Ktg

### Step 1: Unpacking

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

Before you begin, you can decide where to place your sensors, and which directions you would like to home the machine. You can always change this later, but by default, this guide will set up the sensors at the **lower left corner**.

Homing to the lower left corner is recommended because:

<ul>
  <li>This position is commonly used for your zero/origin point in projects, making it convenient for setting up jigs</li>
  <li>When squaring your machine by running the machine to the back, you will not run into the sensors</li>
</ul>

![](/_images/_longmill/_advanced/_4_Inductive/lm_inductive_p2_Corners-for-Homing.jpg){.aligncenter .size-medium}

### Step 2: Attaching to the machine

Each bracket is labelled as 'X', 'Y', or 'Z' so you'll know where to mount them. You can unscrew one nut and washer off each sensor and place it in the hole of each bracket before putting the washer and nut back on, **but keep them loose for now**.

![](/_images/_longmill/_advanced/_4_Inductive/lm_inductive_p2-5_sensor-attach.jpg){.aligncenter .size-medium}

**The tabs below show the attachment of limit switches for homing at the lower left corner.** If you choose to home at another corner, you can rearrange the X and Y sensor mounts, mirroring what is shown below. Some positions may require you to flip the sensor.

Each bracket uses a pair of M3 screws to mount to the machine. Simply slide the bracket onto the recommended location and gently tighten the M3 screws using a 2.5mm Allen key into the brass heat-set nuts just until snug. **Do not over tighten, as this could damage the bracket**, but ensure that the bracket cannot move easily.

[tabby title="X-Axis" open="yes"]

#### X-Axis Mounting

Place the X-axis sensor on the top of the left steel Y-gantry plate, sitting against the aluminum rail. The sensor should be triggered by the X-gantry plate when in contact.

![](/_images/_longmill/_advanced/_4_Inductive/lm_inductive_p3_combined2.png "X-axis sensor alignment"){.aligncenter .size-medium}

<b>X-Axis mounting with non-magnetic dust shoe</b>

If your machine has the older-style dust shoe with aluminum extrusions and a wooden base, you will need to install the dust shoe 'flag' to trigger the X-axis sensor.

Loosen the smaller (M5) screw on the flag and slide the flag onto the front slot of the left aluminum extrusion as shown. Adjust the height of where the flag sits, as well as the position of the X-axis sensor on the gantry plate so that the sensor is aligned with the larger (M8) screw on the flag.

![](/_images/_longmill/_advanced/_4_Inductive/lm_inductive_p4_DSC00358-scaled.jpg "X-axis dust shoe flag alignment"){.aligncenter .size-medium}

[tabby title="Y-Axis"]

#### Y-Axis Mounting

Slide the Y-axis sensor onto the front left 3D printed foot. The mounting tab of the sensor must line up with the edge of the extrusion, and the Y-gantry should be in the center of the mount hole.

![](/_images/_longmill/_advanced/_4_Inductive/lm_inductive_p3YAxis_Combined.png "Y-axis sensor alignment"){.aligncenter .size-medium}

[tabby title="Z-Axis"]

#### Z-Axis Mounting

Slide the Z-axis sensor mount on the top end of the left of the Z-axis, ensuring the mount is pressed against the linear guide as far as it can go. For older models (V1), you will need to remove the lower nut on the inductive sensor before the mount can be slid on. Once the mount is affixed, you can then add and tighten the sensor nut.

Depending on the machine version, you may need to adjust how far the sensor extends down. For newer models (V2-V4) with the notch at the top of the Z-axis gantry plate, the sensor sits at the upper position as shown, triggering before the M5 screw hits the ACME nut. For older models (V1) with the flat top Z-axis gantry plate, the sensor will need to be moved upwards as shown. Make sure that the sensor triggers before the machine hits the 3D printed Z-axis mount.

![](/_images/_longmill/_advanced/_4_Inductive/lm_inductive_p3ZAxis_Combined.png "New (Left) and Old (Right) Limit Switch Positions"){.aligncenter .size-medium}

[tabbyending]

### Step 3: Adjusting the sensors on the brackets

All three inductive sensors are identical and are mounted to the brackets to allow for installation onto the machine. However, you can adjust them if you want to tweak the location of the sensors.

To adjust the position of a sensor:

<ol>
  <li>Loosen a nut and washer on one side</li>
  <li>Slide the sensor along the hole to the right position</li>
  <li>Re-tighten the loose nuts and washers to secure the sensor back in place. Note that the Z-axis sensor does not use a washer on the lower nut</li>
</ol>

### Step 4: Connecting the sensors to the LongBoard controller

Unclip the tabs that hold the wires in each drag chain and route the cables from the inductive sensors. Ensure that there are no sharp bends or tears in the cables as a failed limit sensor could cause a false alarm and halt the machine during use.

- **Z-axis** sensor gets routed through the drag chains on the X and Y rail
- **X-axis** sensor gets routed through the drag chain on  the Y-axis only
- **Y-axis** sensor does not need to be routed through a drag chain

The three cables plug into the three white JST connectors labelled as **XLim**, **YLim**, and **ZLim** as shown in the photo below. To make sure each of the sensors is plugged into the correct port for its axis, it is recommended to label the cable with tape and marker before routing the cables, or plug-in each cable as they are routed through the machine individually.

![](/_images/_longmill/_advanced/_4_Inductive/lm_inductive_p5_DSC00432.jpg "X, Y and Z sensors plugged into LongBoard"){.aligncenter .size-medium}

Once installed, you can verify that each sensor is working and is plugged into the correct port by using the console within UGS, gSender, or other machine interface software. Type the following command into the console: `$10=19` and press enter. This will enable reporting of the current status of each of the sensors.

You can either jog the machine to trigger the sensor (shown by a red light on the sensor), or hold anything made of steel in front of the sensor. While the sensor is triggered, enter the following command into the console: `?`

![](/_images/_longmill/_advanced/_4_Inductive/lm_inductive_p6_limitswitch.png){.aligncenter .size-medium}

The console will now report back to you which limit sensor is triggered, indicated by an X, Y, or Z. Check this for each of the three sensors/axis to make sure the axis sensor reported matches the axis of the sensor you are manually triggering. If the reported triggered sensor does not match the sensor you are triggering, swap the cable plugs at the board as necessary so they all match. This can also be very useful for diagnosing issues with your sensors.

![](/_images/_longmill/_advanced/_4_Inductive/lm_inductive_p6_limitswitch-report.jpg){.aligncenter .size-medium}

After you’ve finished checking that each sensor is reporting correctly, you can set disable sensor status reporting by setting the default value: `$10=3`

#### Adding capacitors for LongBoard revision 1.2

Look on the top of your LongBoard to see the revision number just below the Sienci Labs logo. LongBoard revisions 1.3 and 1.4 come preinstalled with capacitors for each of the limit switch circuits. <b>If your board is revision 1.3 or 1.4, you can set aside the included capacitors and skip to Step 5</b>. If your LongBoard is revision 1.2, however, it does not come pre-installed with capacitors and may be subject to triggering falsely due to electrical noise. Therefore, each kit includes a set of 0.1 mF ceramic non-polarized capacitors to filter out any electrical noise. The capacitors used are shown below.

![](/_images/_longmill/_advanced/_4_Inductive/lm_inductive_p7_Combined.png)

Remove the green 5 port connector installed in the '5V, Xlim, Ylim, Zlim, GND' port on the LongBoard. Then loosen the screw terminals of the connector and insert three capacitors into the connector as shown in the photo above. For each capacitor, one prong should be inserted to the GND port, and one prong into the X, Y, or Z port. Re-tighten each of the screw terminals on the connector then plug the connector back into the secondary limit switch port.

Plug in the X, Y, and Z-axis limit switch connectors into each of the three white connectors as shown in the photo above.

### Step 5: Changing your settings for limit switches

If you received your machine before September 2021, you may need to update your LongMill's firmware to the latest version to have access to all of the updates for your limit switches to work. At the time of writing, the latest version of the LongMill firmware is **Sept 8, 2021**.

To update your firmware, connect your machine to gSender, click on "Firmware", and click on the "Flash grbl" button. Follow the prompts to install the latest version of the firmware onto your LongBoard.

![](/_images/_longmill/_advanced/_4_Inductive/lm_inductive_p8_gSenderfirmware.png){.aligncenter .size-medium}

Next, import our default EEPROM settings for your machine. Press “Restore Defaults” at the “Firmware” window.  with limit switches. Use the "Import Settings" tool and update your EEPROM settings to the new defaults (link to download file coming soon). If you wish to make changes or adjustments, additional info about changing your EEPROM settings can be found further down on this page.

![](/_images/_longmill/_advanced/_4_Inductive/lm_inductive_p9_gSender-restore-eeporm.png){.aligncenter .size-medium}

#### Recommended settings for sensors

Now that we’re working with the default settings, we will modify a few to make them work with the sensors.

- **Enable** Soft and Hard limits ($20 and $21)
- **Enable** Homing cycle ($22)
- **Check** Homing direction invert ($23)
- **Check** X and Y-axis travel limits ($130 and $131)

![](/_images/_longmill/_advanced/_4_Inductive/lm_inductive_p10_gSender-lim-switch-firmware.png "$20, $21 and $22 settings must be enabled"){.aligncenter .size-medium}

**Soft limits and Hard limits**<br>
Both soft limits and hard limits will stop the machine if it is moving to the boundaries of the machine. Soft limits determines when to stop using calculations in the software program, NOT by triggers at the sensor. Hard limits determines when to stop from the trigger of the sensors.

We recommend using both, so that one end of the machine is constrained by hard limits (bottom and left directions) and the other end is constrained by soft limits. You may get error messages if you are trying to move past the boundaries. If so, try jogging the machine away from machine boundaries, or jog at a smaller distance when near boundaries.

**Homing cycle**<br>
By enabling the homing cycle, you are able to home your machine with the sensors. So each time you connect to gSender, it will prompt you to home your machine (showing a red alarm). This is a safety feature, to check that the sensors are working and to ensure your machine will move within bounds. You can click on the lock icon in the top left corner to unlock your machine and skip this step if you wish.

![](/_images/_longmill/_advanced/_4_Inductive/lm_inductive_p11_Mk1homing.jpg){.aligncenter .size-medium}

**Homing direction**<br>
If you want to set your home at the front left corner and have installed your inductive sensors to match, you will need to invert your X and Y-axis. By default all axes will home in the "positive" direction which is typically **Right** (X), **Away** (Y), and **Up** (Z) so toggle these as needed for your setup.

![](/_images/_longmill/_advanced/_4_Inductive/lm_inductive_p12_HomingFrontLeft.jpg){.aligncenter .size-medium}

**X and Y travel limits**<br>
We recommend that `$130=750` and `$131=810` on your firmware settings for a LongMill 30x30. These numbers are used by the soft limits to stop your CNC from crashing into itself so they'll be different based on your CNC setup and if you use accessories that get in the way.

If you need to find the maximum travel for your unique setup do the following (optional); home your machine, zero all axes, then jog each axis to where you feel comfortable limiting it. Use the coordinates to set your maximum travel for each axis.

![](/_images/_longmill/_advanced/_4_Inductive/lm_inductive_p13_gSenderlimswitch.png "$130 and $131 must be changed"){.aligncenter .size-medium}

### Step 6: Using your sensors

At this stage, you're ready to start using your sensors.

#### Testing limit switches

Once the firmware changes have been made, test the sensors. Disconnect, then reconnect to your machine. You should see the red alarm at the top right, press “Click to Run Homing.”

![](/_images/_longmill/_advanced/_4_Inductive/lm_inductive_p14_gsenderalarmstate.png){.aligncenter .size-medium}

On gSender, the process for limit switch homing is very similar to touch plate probing. This is what happens on the LongMill when you run the homing cycle:

<ol>
  <li>Machine moves up quickly in the Z-axis, until the switch gets triggered</li>
  <li>Machine retracts slightly, moves up slowly in the Z-axis, until switch gets triggered again</li>
  <li>Machine quickly moves diagonally across table to upper right corner, until the switch gets triggered</li>
  <li>Machine retracts slightly, slowly moves diagonally across table to upper right corner, until switch gets triggered again</li>
</ol>

If this process completes without any errors, you have successfully homed your machine!

#### Homing features

Once you have connected to your machine, at any point when you aren’t running a cutting job, you can run the homing cycle by pressing “Home” with the house icon.

![](/_images/_longmill/_advanced/_4_Inductive/lm_inductive_p15_limitswitchhoming.png){.aligncenter .size-medium}

Additionally, if you first connect and need to bypass the alarm without homing, you can by pressing the “Unlock” yellow padlock button on the top left of the visualizer screen. We do not recommend this usually, because it is safer to home first before running a cutting job.

![](/_images/_longmill/_advanced/_4_Inductive/lm_inductive_p16_gsendeunlock.png){.aligncenter .size-medium}

#### Work offsets

With CNC, work offsets can be thought of as bookmarks. They are saved origin positions on your machine that allow you to always return later to a known location. Having one or more known locations you can repeatedly return to is extremely useful for many reasons such as:

<ul>
  <li>Restarting a failed job</li>
  <li>Recovering from a power outage during a job</li>
  <li>Repeating a job in a fixture or multiple fixtures</li>
  <li>Returning to an exact work XY origin after performing a tool change</li>
</ul>

The repeatability of the inductive limit switches has been tested to be less than 0.001”, meaning that you will always be able to return to your original work origin within 0.001” accuracy, and can confidently repeat jobs without worries of toolpath misalignment or crashes.

To change work offsets or workspaces, simply select one of the 6 workspaces from the drop-down list in the top right corner of gSender as shown in the photo below.

![](/_images/_longmill/_advanced/_4_Inductive/lm_inductive_p17_gsenderworkspaces.png "Workspaces to choose from"){.aligncenter .size-medium}

Alternatively, entering the command G54, G55, G56.. etc. into the console of gSender or UGS will tell the machine to switch into that workspace. You will notice the work coordinates (blue numbers) will change upon switching workspaces to whatever the coordinates are within the new workspace. The machine coordinates (grey numbers) will always remain the same regardless, as these are of course relative to your machine's home position.

All 6 of these workspaces are modal settings, meaning they will be saved by the controller even after powering off the machine.

### Other Limit Switch Settings

**Homing locate feed rate ($24)**<br>
By default, this speed is set to `$24=25`, which sets the homing locate feed rate to 25 mm/min. When homing your machine, the machine will first move at a preset speed (see $25 - Homing Seek) to more rapidly reach the limit switch, move away from the switch to deactivate it, then move towards the limit switch at a slower speed for a more accurate reading. We recommend keeping this value at 25mm/min as it works for most limit switches.

**Homing seek ($25)**<br>
By default, this speed is set to `$25=500`, which sets the homing search seek rate to 500 mm/min. This is the speed of which the machine will move to locate each limit switch.

**Homing switch debounce delay ($26)**<br>
By default, this time is set to `$26=250`, which controls the delay before the controller measures if the signal is on or off. Some switches can take a few moments before an on or off signal is defined. We recommend keeping this at its default setting. However, if you find that your switch randomly triggers for no reason, you may want to increase the debounce delay.

**Homing pull-off distance ($27)**<br>
By default, this distance is set to `$27=1`. This distance determines the distance that the machine needs to move away from the switch to un-trigger it. For some sensors, such as mechanical switches, this can be a few millimetres, while for inductive proximity sensors may only need a fraction of a millimetre. For inductive sensors, we recommend keeping your default homing pull off distance at 1mm, while if you are using mechanical switches, to use a large number to ensure that your switch is completely untriggered after your homing sequence.

Limit switches (also referred to as end stops or homing switches) are sensors that sit at one or both ends of each movement axis of a CNC to provide a few different functions. There are many different limit switch designs which broadly fall under being either mechanical or non-mechanical (ex. inductive).

In order to use limit switches, you will need to make modifications to both the electronics and firmware of the machine. For more in-depth information on the firmware, specifically the settings required to enable limit switch capability, visit the <a href="https://github.com/gnea/grbl/wiki/Grbl-v1.1-Configuration#21---hard-limits-boolean">grbl v1.1 Configuration Guide.</a>

### Do I Need Limit Switches?

The LongMill does NOT need limit switches to operate and doesn't include them by default. Many individuals are drawn to having switches by convention, but most times a limit switch exists to either:

<ol>
  <li>Define soft or hard limits* in order to prevent a CNC from damaging itself if it travels past its movement limits</li>
  <li>Repeatably locate the machine (homing) for jogging / work offsets, saving a job that's gone bad, or to resume existing work done for a multi-part job</li>
</ol>

The LongMill design addresses these functions by way of:

<ol>
  <li>Being designed so that hitting the ends of its travel area causes zero damage to the machine
<ul>
  <li>In larger, more powerful machines such as VMCs and industrial CNC routers, crashing a machine can very well mean costly damage to your machine so limit switches are cheap insurance to prevent that. However, on hobby machines like the LongMill, the machine is not powerful enough to cause damage to itself, and so are not really necessary. In fact, in some cases, it can be more of a hassle as accidental triggers can ruin a project.</li>
</ul>

</li>
  <li>Locating the machine can easily be done via the use of a touch plate
<ul>
  <li>'Homing' is just the act of calibrating a CNC to a particular spot repeatably so that if, for example, you lose your CNC position due to a power outage or for a tool-change then you can find that position again using the offset distance from the calibrated point. This calibrated point can be set using limit switches but can just as easily be a touch plate or conductive geometry that a tool can touch off</li>
</ul>
</li>
</ol>

With this being said, some users may still choose to integrate switches into their machine if they start to find themselves running longer and longer jobs, performing more complex cuts, or they're looking for easier job relocation without having to keep their touch plate in mind.

*A soft limit is when there is a single switch on one side of the movement and the movement limit is defined in software, whereas a hard limit has two switches on either movement end which signal a 'Stop' to the controller if triggered.

### Wiring Considerations

Already the LongMill controller comes with two different input spaces (a JST-XH connector for each axis and a screw terminal connector) that allows easy connection of any kind of switch. If you are intent on installing switches yourself, here are some crucial points you're aware of:

<ul>
  <li>For limit switches on a CNC, what matters most is that the sensing happens precisely and that the accuracy deviates very little with changes in the surrounding environment, otherwise the switch might activate 2mm away when you've got your shed heater on but 3mm away if you open the door. Each manufacturer should provide theses sorts of details in their sensor documentation.</li>
  <li>It's very important to shield and filter noise along the lines with the limit switches, as interference can cause the limits to trigger erratically. We have found that placing a 0.1uF capacitor across the input and ground for each limit helps to prevent errant triggers.</li>
  <li>If you are wiring limits to both ends of the axis, you can put them parallel to each other.</li>
  <li>All of the switches share the same ground.</li>
</ul>

### Installation

In order to attach and wire your own custom set of limit switches to your setup, you will need the following:

<ul>
  <li>Soldering iron</li>
  <li>Solder</li>
  <li>Heat shrink</li>
  <li>4-pin JST connectors (optional)</li>
  <li>20-24 AWG copper stranded wire</li>
  <li>Limit switches, either mechanical or inductive</li>
  <li>3x 10 kΩ resistor (for Rev 1.2 and Rev 1.3)</li>
  <li>3x 0.1 mF ceramic non-polarized capacitors (for Rev 1.2)</li>
</ul>

You can check the version of your LongBoard on top of your control box.

![](/_images/_longmill/_advanced/_5_LimitS/lm_limits_p1_LongBoard.jpg){.aligncenter .size-medium}

The first step is to figure out where to wire your limit switches. Each limit switch will come with 3 wires, signal, GND and 5V. They will either be bare wires or come with connectors. For switches that come with 4-pin JST connectors, you can simply plug the switches into the white connectors on the side of your control board, making sure the wiring is correct based on the type of switch you have (NO, NC, NPN, PNP). If you have just the switch and wires, use the green connectors because you can fasten down wires with these connectors.

For mechanical switches, each switch must be wired to a different signal line, then to GND, as indicated in the "x3" label on the diagram.  For inductive switches, each switch must be wired to a different signal line, then to GND and 5V, as indicated in the "x3" label on the diagram.

[tabby title="Mechanical"]

![](/_images/_longmill/_advanced/_5_LimitS/lm_limits_p2_Rev_1.4_NC.png){.aligncenter .size-medium}

[tabby title="Mechanical w/ JST"]

![](/_images/_longmill/_advanced/_5_LimitS/lm_limits_p3_Rev_1.4_NCJST.png){.aligncenter .size-medium}

[tabby title="Non-mechanical"]

![](/_images/_longmill/_advanced/_5_LimitS/lm_limits_p4_Rev_1.4_NCNPN.png){.aligncenter .size-medium}

[tabbyending]

Next, you will need to extend or attach the wiring for your limit switches, and find an appropriate place to mount them on the LongMill. If you are using a different limit switch, you can create your own limit switch mounts by designing and cutting them out on the machine or 3D printing them as well. Make sure the wire is long enough to reach the control board from the machine.

The type of switch used must be considered for proper wiring. For NO and NC mechanical switches, refer to the diagrams below for proper wiring. The blue lines indicate the signal line (XLim, YLim and ZLim) and the green lines indicate the ground line (GND). If you are using two switches per axis, the wiring between the them is indicated below as well.

![](/_images/_longmill/_advanced/_5_LimitS/lm_limits_p5_TwoSwitches.png){.aligncenter .size-medium}

![](/_images/_longmill/_advanced/_5_LimitS/lm_limits_p6_NOSwitches.png){.aligncenter .size-medium}

If you have a Rev 1.2 or 1.3 LongBoard, it is necessary to attach the resistors and/or capacitors as specified. Refer to the diagrams below for the additional wiring. The red 5V line is used to produce the noise filtering effects via capacitor and to establish the correct voltage via resistor.

The limit switches must also be included as described in the previous diagrams, making connections between their respective signal line and ground. In Rev 1.2, you wire the limit switch between the resistor and the capacitor. In Rev 1.3, you wire the limit switch between the resistor and the signal pin.

[tabby title="Rev 1.2"]

![](/_images/_longmill/_advanced/_5_LimitS/lm_limits_p7_1_AddWire.png){.aligncenter .size-medium}

[tabby title="Rev 1.3"]

![](/_images/_longmill/_advanced/_5_LimitS/lm_limits_p7_AddWire.png){.aligncenter .size-medium}

[tabbyending]

Before you solder anything, make a plan and dry fit all these components into their approximate locations. Once you have settled on their placements, you can solder your circuit together.

### Firmware Settings

Once you’ve assembled all the electrical connections to the LongBoard, you can enable limit switches, in which you will need to change a couple of settings on your LongMill’s firmware. Settings can be changed by sending the command to update the EEPROM settings manually through the console, or using the “Firmware Tool” on gSender. Below, we have listed the settings that you may want to enable.

![](/_images/_longmill/_advanced/_5_LimitS/lm_limits_p8_NewEEPROM.png){.aligncenter .size-medium}

<b>$5 - Limit pins invert, boolean</b>

For **NO or NPN**, this setting should be **$5=0**, so that the input and output pins are set to the proper voltage level to function properly. For **NC or PNP**, this setting should be set to **$5=1**.

<b>$20 and $21 - Soft limits and hard limits enable</b>

If you have two switches per axis, use **$20=0 and $21=1** to enable **hard limits**. If you have one switch per axis, use **$20=1** and **$21=0** to enable **soft limits**.

<b>$22 - Homing cycle, boolean</b>

By default, your LongMill is set to **$22=0**, disabling the ability to use the homing cycle. Activate homing by sending the command **$22=1**. When homing is activated, every time your machine is connected, your machine will ask you to home the machine as a safety feature. You can home your machine by sending the command **$H** through the console, or use the "Home" button on your g-code sender.

<b>$23 - Homing direction invert, mask</b>

By default, your LongMill is set to <b>*$23=0*</b>. This setting is used to select the direction that the machine moves to home each axis. By default, when <b>*$23=0*</b>, the machine will move home up in the Z direction, and then to the upper left corner (moving towards the left on the X-axis and moving up to the top on the Y-axis).

In some cases you may want to change the direction that you want to home, either based on the location of your limit switch and the way you want to set up your workflow. For example, if you have a square at the bottom left corner of your machine where you can set a corner you can set rectangular material on so that you can repeat the same job over and over again, you may want to invert the Y-axis homing direction so that your machine homes to the bottom left corner of the machine.

<table role="table">
<thead>
<tr>
<th align="center">Setting Value</th>
<th align="center">Mask</th>
<th align="center">Invert X</th>
<th align="center">Invert Y</th>
<th align="center">Invert Z</th>
</tr>
</thead>
<tbody>
<tr>
<td align="center">0</td>
<td align="center">00000000</td>
<td align="center">N</td>
<td align="center">N</td>
<td align="center">N</td>
</tr>
<tr>
<td align="center">1</td>
<td align="center">00000001</td>
<td align="center">Y</td>
<td align="center">N</td>
<td align="center">N</td>
</tr>
<tr>
<td align="center">2</td>
<td align="center">00000010</td>
<td align="center">N</td>
<td align="center">Y</td>
<td align="center">N</td>
</tr>
<tr>
<td align="center">3</td>
<td align="center">00000011</td>
<td align="center">Y</td>
<td align="center">Y</td>
<td align="center">N</td>
</tr>
<tr>
<td align="center">4</td>
<td align="center">00000100</td>
<td align="center">N</td>
<td align="center">N</td>
<td align="center">Y</td>
</tr>
<tr>
<td align="center">5</td>
<td align="center">00000101</td>
<td align="center">Y</td>
<td align="center">N</td>
<td align="center">Y</td>
</tr>
<tr>
<td align="center">6</td>
<td align="center">00000110</td>
<td align="center">N</td>
<td align="center">Y</td>
<td align="center">Y</td>
</tr>
<tr>
<td align="center">7</td>
<td align="center">00000111</td>
<td align="center">Y</td>
<td align="center">Y</td>
<td align="center">Y</td>
</tr>
</tbody>
</table>

When looking at the table on inverting each axis, setting value 3 inverts the direction of the X and Y homing directions. So by sending command **$23=3**, the X-axis and Y-axis homing directions will be reversed and the machine will home in the bottom left corner.

On gSender, you can use the toggles instead to change the direction of each axis.

![](/_images/_longmill/_advanced/_5_LimitS/lm_limits_p9_EEPROMHomingDirection.png){.aligncenter .size-medium}

<b>$24 - Homing locate feed rate, mm/min</b>

By default, this speed is set to ***$24=25***, which sets the homing locate feed rate to 25mm/min. When homing your machine, the machine will first move at a preset speed (see $25 - Homing Seek) to more rapidly reach the limit switch, move away from the switch to deactivate it, then move towards the limit switch at a slower speed for a more accurate reading.

We recommend keeping this value at 25mm/min as it works for most limit switches.

<b>$25 - Homing seek, mm/min</b>

By default, this speed is set to ***$25=1500***, which sets the homing search seek rate to 500mm/min. This is the speed of which the machine will move to locate each limit switch.

<b>$26 Homing switch debounce delay, ms</b>

By default, this time is set to ***$26=250***, which controls the delay before the controller measuring if the signal is on or off. Some switches can take a few moments before a on or off signal is defined. We recommend keeping this at its default setting. However, if you find that your switch randomly triggers for no reason, you may want to increase the debounce delay.

<b>$27 Homing pull-off distance, mm</b>

By default, this distance is set to ***$27=1***. This distance determines the distance that the machine needs to move away from the switch to un-trigger it. For some sensors, such as mechanical switches, this can be a few millimeters, while inductive proximity sensors may only need a fraction of a millimeter. For inductive sensors, we recommend keeping your default homing pull-off distance at 1mm, while if you are using mechanical switches, use about 2-4mm to ensure that your switch is completely un-triggered after your homing sequence.
