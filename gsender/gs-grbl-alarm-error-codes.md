---
title: grbl Alarms & Errors
menu_order: 5
post_status: publish
post_excerpt: Use this reference table to see the common Error codes and Alarm codes that you might see from your grbl-based CNC machine.
post_date: 2022-05-01 17:28:00
taxonomy:
    knowledgebase_cat: gdocs
    knowledgebase_tag:
        - gsender
custom_fields:
    KBName: gSender
    basepress_post_icon: bp-caret-right
skip_file: no
featured_image: _images/_gsender/_issues/gs_is_alarm.jpg)
---

The grbl firmware has a whole list of Alarms and Error codes that you can encounter when running your CNC. gSender will always display a question mark when there's an alarm which you can hover over for more information about why it happened and errors will appear as a hovering box in the bottom corner of the visualizer.

You can close an alarm by clicking on the button that appears next to it in the visualizer. Most alarms can also be handled by typing `$x` into the 'Console' tab and hitting the 'Run' button.

![](/_images/_gsender/_issues/gs_is_alarm.jpg){.aligncenter .size-medium}

## Useful Commands

<ul>
  <li><b>$</b>   reminder of all grbl commands</li>
  <li><b>$$</b>   lists all Firmware settings and their values</li>
  <li><b>$rst=$</b>   resets all your EEPROM settings to the default Firmware values</li>
  <li><b>?</b>   reports any active inputs plus some other useful info</li>
  <li><b>$i</b>   tells you information on your board Firmware Version</li>
  <li><b>$#</b>   all the currently stored machine offsets</li>
</ul>

## <span style="color: #ff0000;">Alarms</span>

[su_table responsive="yes"]
<table>
<tbody>
<tr>
<td><b>Alarm Code</b></td>
<td><b>Message</b></td>
<td><b>Description</b></td>
<td><b>Example</b></td>
</tr>
<tr>
<td>1</td>
<td>Hard limit</td>
<td>Hard limit has been triggered. Machine position is likely lost due to sudden halt. Re-homing is highly recommended.</td>
<td><a href="https://youtu.be/I1EhAPNXdzQ?t=208" target="_blank" rel="noopener">Example</a></td>
</tr>
<tr>
<td>2</td>
<td>Soft limit</td>
<td>G-code motion target exceeds machine travel. Machine position retained. Alarm may be safely unlocked.</td>
<td><a href="https://youtu.be/I1EhAPNXdzQ?t=226" target="_blank" rel="noopener">Example</a></td>
</tr>
<tr>
<td>3</td>
<td>Abort during cycle</td>
<td>Machine position is likely lost due to sudden halt. Re-homing is highly recommended. May be due to issuing g-code commands that exceed the limit of the machine.</td>
<td></td>
</tr>
<tr>
<td>4</td>
<td>Probe fail</td>
<td>Probe is not in the expected initial state before starting probe cycle when G38.2 and G38.3 is not triggered and G38.4 and G38.5 is triggered. Your bit is likely making contact with the touch plate or the circuit is completed before the bit is moving. Move the bit away from the touch plate.</td>
<td><a href="https://youtu.be/I1EhAPNXdzQ?t=267" target="_blank" rel="noopener">Example</a></td>
</tr>
<tr>
<td>5</td>
<td>Probe fail</td>
<td>Probe did not contact the workpiece within the programmed travel for G38.2 and G38.4. Your bit is too far away from the touch plate. Move the bit closer, it should be within 6-12mm (1/4 -1/2in) away.</td>
<td><a href="https://youtu.be/I1EhAPNXdzQ?t=306" target="_blank" rel="noopener">Example</a></td>
</tr>
<tr>
<td>6</td>
<td>Homing fail</td>
<td>The active homing cycle was reset.</td>
<td></td>
</tr>
<tr>
<td>7</td>
<td>Homing fail</td>
<td>Safety door was opened during homing cycle.</td>
<td></td>
</tr>
<tr>
<td>8</td>
<td>Homing fail</td>
<td>Pull off travel failed to clear limit switch. The machine is within the limit switches range when it tries to move away. Try increasing pull-off setting or check wiring.</td>
<td><a href="https://youtu.be/jmiaWA5tiVw?t=563" target="_blank" rel="noopener">Example</a></td>
</tr>
<tr>
<td>9</td>
<td>Homing fail</td>
<td>Could not find limit switch within search distances. Try increasing max travel, decreasing pull-off distance, or check wiring. The limit switch wasn't triggered in the distances expected. If your z-axis is moving away from the switch when homing, check your firmware and confirm you have the correct profile for your machine.</td>
<td><a href="https://youtu.be/jmiaWA5tiVw?t=531" target="_blank" rel="noopener">Example</a></td>
</tr>
<tr>
<td>10</td>
<td>EStop asserted</td>
<td>You've pressed your E-stop to stop your machine! Unclick the E-stop, then clear this alarm to continue. <b>grblHAL specific</b></td>
<td></td>
</tr>
<tr>
<td>14</td>
<td>Spindle at speed timeout</td>
<td>Either the spindle hasn't gotten up to speed in the timeframe set for 'spindle at speed' or spindle has been wired incorrectly to your controller. Clear this alarm, check your setup, and try again. <b>grblHAL specific</b></td>
<td></td>
</tr>
<tr>
<td>15</td>
<td>Homing fail</td>
<td>Could not find second limit switch for auto squared axis within search distances. Try increasing max travel, decreasing pull-off distance, or check wiring. <b>grblHAL specific</b></td>
<td></td>
</tr>
<tr>
<td>17</td>
<td>Motor fault</td>
<td>Issue encountered with closed loop motor tracking. Position likely lost. <b>grblHAL specific</b></td>
<td></td>
</tr>
</tbody>
</table>
[/su_table]

## <span style="color: #ff8b3d;">Errors</span>

[su_table responsive="yes"]
<table>
<tbody>
<tr>
<td><b>Error Code</b></td>
<td><b>Message</b></td>
<td><b>Description</b></td>
<td><b>Example</b></td>
</tr>
<tr>
<td>1</td>
<td>Expected command letter</td>
<td>G-code words consist of a letter and a value. Letter was not found.</td>
<td><a href="#error-1-2-20-24-26-28">Example</a></td>
</tr>
<tr>
<td>2</td>
<td>Bad number format</td>
<td>Missing the expected G-code word value or numeric value format is not valid.</td>
<td><a href="#error-1-2-20-24-26-28">Example</a></td>
</tr>
<tr>
<td>3</td>
<td>Invalid statement</td>
<td>Grbl '$' system command was not recognized or supported.</td>
<td></td>
</tr>
<tr>
<td>4</td>
<td>Value &lt; 0</td>
<td>Negative value received for an expected positive value.</td>
<td></td>
</tr>
<tr>
<td>5</td>
<td>Setting disabled</td>
<td>Homing cycle failure. Homing is not enabled via settings.</td>
<td></td>
</tr>
<tr>
<td>6</td>
<td>Value &lt; 3 μsec</td>
<td>Minimum step pulse time must be greater than 3μsec.</td>
<td></td>
</tr>
<tr>
<td>7</td>
<td>EEPROM read fail. Using defaults</td>
<td>An EEPROM read failed. Auto-restoring affected EEPROM to default values.</td>
<td></td>
</tr>
<tr>
<td>8</td>
<td>Not idle</td>
<td>Grbl '$' command cannot be used unless Grbl is IDLE. Ensures smooth operation during a job.</td>
<td></td>
</tr>
<tr>
<td>9</td>
<td>G-code lock</td>
<td>G-code commands are locked out during alarm or jog state.</td>
<td></td>
</tr>
<tr>
<td>10</td>
<td>Homing not enabled</td>
<td>Soft limits cannot be enabled without homing also enabled.</td>
<td></td>
</tr>
<tr>
<td>11</td>
<td>Line overflow</td>
<td>Max characters per line exceeded. Received command line was not executed.</td>
<td></td>
</tr>
<tr>
<td>12</td>
<td>Step rate &gt; 30kHz</td>
<td>Grbl '$' setting value cause the step rate to exceed the maximum supported.</td>
<td></td>
</tr>
<tr>
<td>13</td>
<td>Check Door</td>
<td>Safety door detected as opened and door state initiated.</td>
<td></td>
</tr>
<tr>
<td>14</td>
<td>Line length exceeded</td>
<td>Build info or startup line exceeded EEPROM line length limit. Line not stored.</td>
<td></td>
</tr>
<tr>
<td>15</td>
<td>Travel exceeded</td>
<td>Jog target exceeds machine travel. Jog command has been ignored.</td>
<td></td>
</tr>
<tr>
<td>16</td>
<td>Invalid jog command</td>
<td>Jog command has no '=' or contains prohibited g-code.</td>
<td></td>
</tr>
<tr>
<td>17</td>
<td>Setting disabled</td>
<td>Laser mode requires PWM output.</td>
<td></td>
</tr>
<tr>
<td>20</td>
<td>Unsupported command</td>
<td>Unsupported or invalid g-code command found in block.</td>
<td><a href="#error-1-2-20-24-26-28">Example</a></td>
</tr>
<tr>
<td>21</td>
<td>Modal group violation</td>
<td>More than one g-code command from same modal group found in block.</td>
<td></td>
</tr>
<tr>
<td>22</td>
<td>Undefined feed rate</td>
<td>Feed rate has not yet been set or is undefined.</td>
<td></td>
</tr>
<tr>
<td>23</td>
<td>Invalid gcode ID:23</td>
<td>G-code command in block requires an integer value.</td>
<td></td>
</tr>
<tr>
<td>24</td>
<td>Invalid gcode ID:24</td>
<td>More than one g-code command that requires axis words found in block.</td>
<td><a href="#error-1-2-20-24-26-28">Example</a></td>
</tr>
<tr>
<td>25</td>
<td>Invalid gcode ID:25</td>
<td>Repeated g-code word found in block.</td>
<td></td>
</tr>
<tr>
<td>26</td>
<td>Invalid gcode ID:26</td>
<td>No axis words found in block for g-code command or current modal state which requires them.</td>
<td><a href="#error-1-2-20-24-26-28">Example</a></td>
</tr>
<tr>
<td>27</td>
<td>Invalid gcode ID:27</td>
<td>Line number value is invalid.</td>
<td></td>
</tr>
<tr>
<td>28</td>
<td>Invalid gcode ID:28</td>
<td>G-code command is missing a required value word.</td>
<td><a href="#error-1-2-20-24-26-28">Example</a></td>
</tr>
<tr>
<td>29</td>
<td>Invalid gcode ID:29</td>
<td>G59.x work coordinate systems are not supported.</td>
<td></td>
</tr>
<tr>
<td>30</td>
<td>Invalid gcode ID:30</td>
<td>G53 only allowed with G0 and G1 motion modes.</td>
<td></td>
</tr>
<tr>
<td>31</td>
<td>Invalid gcode ID:31</td>
<td>Axis words found in block when no command or current modal state uses them.</td>
<td></td>
</tr>
<tr>
<td>32</td>
<td>Invalid gcode ID:32</td>
<td>G2 and G3 arcs require at least one in-plane axis word.</td>
<td></td>
</tr>
<tr>
<td>33</td>
<td>Invalid gcode ID:33</td>
<td>Motion command target is invalid.</td>
<td><a href="#error-33">Example</a></td>
</tr>
<tr>
<td>34</td>
<td>Invalid gcode ID:34</td>
<td>Arc radius value is invalid.</td>
<td></td>
</tr>
<tr>
<td>35</td>
<td>Invalid gcode ID:35</td>
<td>G2 and G3 arcs require at least one in-plane offset word.</td>
<td></td>
</tr>
<tr>
<td>36</td>
<td>Invalid gcode ID:36</td>
<td>Unused value words found in block.</td>
<td></td>
</tr>
<tr>
<td>37</td>
<td>Invalid gcode ID:37</td>
<td>G43.1 dynamic tool length offset is not assigned to configured tool length axis.</td>
<td></td>
</tr>
<tr>
<td>38</td>
<td>Invalid gcode ID:38</td>
<td>Tool number greater than max supported value.</td>
<td></td>
</tr>
</tbody>
</table>
[/su_table]

### Error 1, 2, 20, 24, 26, 28

When any of these errors appear in gSender, it can typically be traced back to these sources:

1. **You are connected with the wrong firmware**
   - Check this in the top, left corner of the app when you're connected, is should say:
      - "grbl" for the majority of CNCs including older LongMills, Shapeoko, Genmitsu, Mill One, X-Carve, etc.
      - "grblHAL" for AltMill (SLB Ext), LongMill (SLB), or any other grblHAL board
   - If the firmware is incorrect go to Config ➜ Firmware Fallback ➜ select the correct firmware ➜ Apply Settings.
1. **The g-code file itself has errors in it**
   - Check that you are using the right <a href="https://resources.sienci.com/view/am-post-processors/>">post processor in your CAM software</a> then try re-generating the file (see more with [Error 33](#error-33) below).
   - Go to Config ➜ Basics ➜ Notifications and turn on 'Warn if bad file' to see if you get notified that the file is still bad when you reload it.
1. **You have an unstable connection to your CNC**
   - Check if your USB cable is loose or if other ports or connectors on your CNC board are loose.
   - Try another USB port on your computer, another computer all together, and if you're using a USB hub try connecting directly to your CNC instead.
   - Don't use a USB Stick, make sure the files are on the hard-drive of your computer.
   - Determine if it's from electromagnetic interference/static. Run the job in the air with your router/spindle and dust collector turned off to see if the same errors appear. If they go away then try running the job normally again using scrap material, just to confirm the errors reappear. If this happens, you'll want to look into putting your computer and controller on a separate circuit from the router/spindle and dust collector, or <a href="https://resources.sienci.com/view/lmk2-issues-and-fixes/#using-a-dust-collector-system-causes-the-machine-to-disconnect">grounding your equipment</a>.
1. **Some gSender versions can have bugs**
   - This is the least likely cause, but a couple gSender versions have been known to make errors appear that don't affect operation. Try <a href="https://resources.sienci.com/view/gs-installation/#older-versions">using a different gSender version</a>.

### Error 33

Can pop up as "Motion command target is invalid" and usually comes from issues with G2 or G3 arc/curve movements in the g-code. If the target is invalid you might want to verify the file again in gSender or regenerate it in CAM with the right post processor.

For example, there have been [many](https://forum.sienci.com/t/invalid-g-code-id-33-in-gsender/10904) [reports](https://community.carbide3d.com/t/grbl-error-invalid-gcode-id-33/1204) that if you use the `inch` post processor in Vectric, Carveco, or Fusion 360 then they won't add enough decimal places to satisfy arc curve calculations - which will cause an Error 33. The best solution is to just use a `mm` post processor to get more accurate movements, or for Carveco use `UGS grbl`.

If this isn't the cause, then refer to the steps shown for [Errors 1, 2, 20, 24, 26, 28](#error-1-2-20-24-26-28) shown above.
