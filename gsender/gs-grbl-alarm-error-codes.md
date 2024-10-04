---
title: grbl Alarms & Errors
menu_order: 7
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
featured_image: _images/_gsender/_using/gs_us_clear-alarm.jpg
---

The grbl firmware has a whole list of Alarms and Error codes that you can encounter when running your CNC. gSender will always display a question mark when there’s an alarm which you can hover over for more information about why it happened and errors will appear as a hovering box in the bottom corner of the visualizer.

You can close an alarm by clicking on the button that appears next to it in the visualizer. Most alarms can also be handled by typing “$x” into the ‘Console’ tab and hitting the ‘Run’ button.

![](/_images/_gsender/_using/gs_us_clear-alarm.jpg){.aligncenter .size-full}

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
<td>Soft limit alarm. G-code motion target exceeds machine travel. Machine position retained. Alarm may be safely unlocked.</td>
<td><a href="https://youtu.be/I1EhAPNXdzQ?t=226" target="_blank" rel="noopener">Example</a></td>
</tr>
<tr>
<td>3</td>
<td>Abort during cycle</td>
<td>Reset while in motion. Machine position is likely lost due to sudden halt. Re-homing is highly recommended. May be due to issuing g-code commands that exceed the limit of the machine.</td>
<td></td>
</tr>
<tr>
<td>4</td>
<td>Probe fail</td>
<td>Probe fail. Probe is not in the expected initial state before starting probe cycle when G38.2 and G38.3 is not triggered and G38.4 and G38.5 is triggered. Your bit is likely making contact with the touch plate or the circuit is completed before the bit is moving. Move the bit away from the touch plate.</td>
<td><a href="https://youtu.be/I1EhAPNXdzQ?t=267" target="_blank" rel="noopener">Example</a></td>
</tr>
<tr>
<td>5</td>
<td>Probe fail</td>
<td>Probe fail. Probe did not contact the workpiece within the programmed travel for G38.2 and G38.4. Your bit is too far away from the touch plate. Move the bit closer, it should be within 6-12mm (1/4 -1/2in) away.</td>
<td><a href="https://youtu.be/I1EhAPNXdzQ?t=306" target="_blank" rel="noopener">Example</a></td>
</tr>
<tr>
<td>6</td>
<td>Homing fail</td>
<td>Homing fail. The active homing cycle was reset.</td>
<td></td>
</tr>
<tr>
<td>7</td>
<td>Homing fail</td>
<td>Homing fail. Safety door was opened during homing cycle.</td>
<td></td>
</tr>
<tr>
<td>8</td>
<td>Homing fail</td>
<td>Homing fail. Pull off travel failed to clear limit switch. The machine is within the limit switches range when it tries to move away. Try increasing pull-off setting or check wiring.</td>
<td><a href="https://youtu.be/jmiaWA5tiVw?t=563" target="_blank" rel="noopener">Example</a></td>
</tr>
<tr>
<td>9</td>
<td>Homing fail</td>
<td>Homing fail. Could not find limit switch within search distances. Try increasing max travel, decreasing pull-off distance, or check wiring. The limit switch wasn't triggered in the distances expected. If your z-axis is moving away from the switch when homing, check your firmware and confirm you have the correct profile for your machine.</td>
<td><a href="https://youtu.be/jmiaWA5tiVw?t=531" target="_blank" rel="noopener">Example</a></td>
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
<td>Grbl ‘$’ system command was not recognized or supported.</td>
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
<td>Grbl ‘$’ command cannot be used unless Grbl is IDLE. Ensures smooth operation during a job.</td>
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
<td>Grbl ‘$’ setting value cause the step rate to exceed the maximum supported.</td>
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
<td>Jog command has no ‘=’ or contains prohibited g-code.</td>
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

When any of these errors appear in gSender, it can typically be traced back to 3 sources:

1. **The g-code file has errors in it**: if this is true, then
   - Keep the file loaded
   - Go to gSenders Settings ➜ Safety ➜ to make sure ‘Warn if invalid line detected’ is turned on
   - Next to the ‘Load File’ button on the main screen, you’ll see another button that says ‘Verify Job’ (previously ‘Test Run’)
   - Click this button and it will go through your g-code file, and if the same errors pop up then it’s likely that the file is bad. Go back and check your design software or post processor to make sure it’s all been set up correctly and then try re-generating the file.
1. **You have an unstable connection to your CNC**: if the file didn’t have errors, then this is the next most likely issue. You’ll want to
   - Check if your USB cable is loose or if other ports or connectors on your CNC board are loose.
   - Try another USB port on your computer, and if you’re using a USB hub try skipping it to connect directly to your CNC.
   - Don’t use a USB Stick, make sure the files on are the hard-drive of your computer.
   - Try running the same job in the air with your router/spindle and dust collector turned off to see if the same errors appear as when you run the job. If they go away then try running the job with full cutting again in some scrap material just to confirm the errors come back. Once confirmed, you’ll want to look to see if your equipment isn’t properly grounded, could have improved electrical shielding, or try using another computer. An example of this is to put your controller and computer on a separate power circuit than the router/spindle and dust collector.
1. **Some gSender versions can have bugs**: this is the least likely cause, but a couple gSender versions have been known to make errors appear that aren’t actually happening. If you’ve already tried everything else, you should first double-check that you’re connected to the “grbl” firmware if you’re using a grbl board like the LongBoard, or to “grblHAL” for boards like the SLB. After checking that, try installing and <a href="https://resources.sienci.com/view/gs-installation/#older-versions">using a different gSender version</a>.

### Error 33

Can pop up as "Motion command target is invalid" and usually comes from issues with G2 or G3 arc/curve movements in the g-code. If the target is invalid you might want to verify the file again in gSender or regenerate it in CAM with the right post processor.

For example, there have been [many](https://forum.sienci.com/t/invalid-g-code-id-33-in-gsender/10904) [reports](https://community.carbide3d.com/t/grbl-error-invalid-gcode-id-33/1204) that if you use the `inch` post processor in Vectric, Carveco, or Fusion 360 then they won't add enough decimal places to satisfy arc curve calculations - which will cause an Error 33. The best solution is to just use a `mm` post processor to get more accurate movements, or for Carveco use `UGS grbl`.

If this isn't the cause, then refer to the steps shown for [Errors 1, 2, 20, 24, 26, 28](#error-1-2-20-24-26-28) shown above.
