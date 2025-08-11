---
title: Troubleshooting
menu_order: 4
post_status: publish
post_excerpt: See more on SLB settings and troubleshooting, especially useful on DIY CNC setups to better understand how to configure your SLB for your machine.
post_date: 2024-04-03 16:44:00
taxonomy:
    knowledgebase_cat: slb-handbook
    knowledgebase_tag:
        - slb
custom_fields:
    KBName: SuperLongBoard
    basepress_post_icon: bp-caret-right
skip_file: no
featured_image: _images/_superlongboard/slb_slb-leds.jpg
---

If you're having any issues with your SLB, whether that's understanding its settings or diagnosing a regular problem, you'll likely find your solution here. This includes:

- Fixes to common issues
- Explaining Errors and Alarms
- Using the lights on the board to pinpoint the problem

You might also find that a couple items are useful to have on hand when troubleshooting, though in most cases none of these are strictly necessary:

- A small shorting wire, header pins, or something metal to bridge contact
- Tiny flathead screwdriver to rewire terminal connectors
- Multimeter

### Issues at Setup

The SLB is set up to be automatically compatible with most LongMills by default. If you're finding this isn't the case then generally the best approach is to send the `$rst=$` command in the 'Console' tab, then use the power switch on the back of the board to turn it off then back on again. This will reset your board back to the default values and then you can continue further troubleshooting from there.

- **Firmware settings look funny, don't have descriptions, changing settings causes unexpected changes to happen:** if you're using gSender, check that you've selected 'grblHAL' as the firmware when you connect to your machine, not 'grbl'.
- **Pressing to ‘Zero’ axes isn’t working**: ensure "work coordinate offset" is enabled for $10, or that $10 = 511

[tabby title="Current" open="yes"]

![](/_images/_superlongboard/slb_tb_10-setting-newu.jpg){.aligncenter .size-medium}

[tabby title="Classic gSender"]

![](/_images/_superlongboard/slb_tb_10-setting.jpg){.aligncenter .size-medium}

[tabbyending]

- **Probing isn’t passing continuity check**: ensure the yellow ‘PRB’ light is coming on, if isn't then check your touch plate wiring, and if it is then ensure “pin state” is enabled for $10 or that $10 = 511
- **Dual Y-axes drifting out of sync**: for grblHAL there is a new solution to this which is $37. This is better than the old $1=255 solution because $37 can hold individual motors rather than holding all of them. If you’d like to turn it on to keep your dual Y-axes in sync then turn it on for ‘Y’ or set $37=2.
- **CNC losing location during goto, outlining, probing, or running a job**: all of these situations use high-speed ‘G0’ movements where the motors might not be able to keep up if your machine is not mechanically sound. First, confirm this is the problem by manually jogging your machine using the jog arrows and slowly increasing the jogging ‘Speed’ value until you notice any of the axes moving intermittently. Since your machine should be able to handle these speeds, it’s likely there’s some components that you’ve assembled too loose or too tight or misaligned. Check if you can turn your lead screws by hand, if your belts or v-wheels are too tight, if you have a coupler that’s too loose. These will all be the same components you should be looking at during regular machine maintenance. If you still can’t manage to get your machine to run at full speed the other option is to consider lowering the SLBs maximum speed with settings 110, 111, and 112 and maximum accelerations with settings 120, 121, and 122 until the problem goes away.
- **Overriding speed, spindle, or laser doesn't seem to work on shorter files**: this is an outlying grblHAL issue which should only occur on shorter files. If you want to still override, you should still have the option to set the override before starting the job.
- **Homing gets stuck or disconnects**: try reducing the homing “seek rate” (25) or increasing the “debounce delay” (26) settings. Depending on your setup or sensors, the default values might be a bit too aggressive.
- **Issues with Independant A-axis homing or hard limits**: earlier versions of SLB firmware might exhibit difficulties with this. In this case you’ll have to disable hard limits when doing 4-axis cutting, and if you want to do independent A-axis homing you’ll want to temporarily add it to $44 or 45, then run the independent homing cycle using the button in gSender or sending `$ha`, then remove the A-axis again from $44 or 45.
- **Other unexpected behaviours**: sometimes there might be a case where your SLB isn’t doing what you’d expect it to do but you don’t see the solution in our resources. In these cases feel free to report it to us so we can try to investigate it further, but otherwise you might find that the old adage may still hold true where turning it off and back on again with the main power switch on the back resolves your issue.

### Bad E-stop

If you have a working E-stop, it should:

[su_table responsive="yes"]

| **At any Time** | **When Pressed** | **When Released** |
|-|-|-|
| 1. Have illuminated red lights in the stop button or the body <br> 2. Pressing any of the 3 Action buttons causes the associated light on the SLB to light up | 1. Click in <br> 2. Red light on E-stop turns off <br> 3. Show Alarm 10 in gSender <br> 4. Disable all CNC motor movements | 1. Pop back up <br> 2. Red lights illuminate again <br> 3. Alarm 10 can be closed <br> 4. CNC can move again |

[/su_table]

If this doesn't happen for you, see if any of the situations below match what you're seeing:

- **E-stop light stays on even after the button is pressed, or SLB doesn't seem to respond to E-stop being pressed:** there's a backup option on the board which is able to act as the E-stop and it looks like two metal pins sticking out near the back of the board where you plug the power in. Once you find these two pins, grab anything conductive like a flat head screwdriver and insert it between the two pins that are sticking up to 'connect' them together electrically. This should activate the E-stop if you weren't able to activate it before, or if your problem was that it was never deactivating then keep conducting the pins while turning the toggle switch on the board off then back on again and you should see the red lights for the E-stop turn off. If this is successful then you've either got a loose E-stop wire (check your connections) or your E-stop button is broken. If neither of these work then your board is likely defective and you can contact us to replace it.
- **E-stop doesn't latch closed or doesn't untwist or move:** your E-stop button is likely broken and we can replace it if it's under warranty
- **Unlocking after E-stop press freezes up machine:** this is a bug we've found to exist in the 5.0.3 version of the SLBs firmware. We've implemented a solution in a new firmware version that you should upgrade to since this behaviour can be bothersome. See <a href="https://resources.sienci.com/view/slb-firmware-flashing/">Firmware Flashing</a> for more.

### Common Alarms & Errors

- **Supposed to have multiple Alarms but only one showed up OR after clearing E-stop Alarm there's no message to remind you to home:** this is a current flaw in how grblHAL handles Alarms since they can stack on top of each other but can't be dismissed selectively so all of them get cleared at once. In these situations just be mindful of what's happened so, for instance, you can still remember to home your machine on startup.
- **Alarm 3 or 10 take a couple tries to unlock**: in the newer versions of gSender (1.4.6 onward) this should be fixed where unlocking just takes some time
- **Alarm 10 on startup**: you should be able to “Click to Unlock Machine” in gSender. If this doesn’t work, you can try to:
  - Turn on the board without the E-stop doing anything and the big LED should be Red as well as the small light next to "Halt" on the board which is near the big LED.
  - Rotate to unlock the E-stop, this should turn the smaller red "Halt" light off.
  - Click the Unlock button in gSender.
  - If your machine doesn’t change to ‘Idle’ (white status light), turn the board off then on again and repeat this process until it goes through
- **Alarm 10 when E-stop not pressed**: the E-stop signal needs to be safe so it’s designed to be very sensitive. Check if you have any loose wires or have conductive material in contact with the underside circuitry of the E-stop unit, any of these cases could be causing it to trigger unexpectedly
- **Alarm 14 unexpectedly or during spindle setup**: this would point to an error in how you’ve set up your spindle, either in the wiring, how you’ve set up the SLB EEPROM values, or how you’ve set up the PD values on your VFD. Double-check that everything is as it should be since if there’s a misalignment in any way then the controller won’t receive proper responses and send an Alarm 14 to protect the machine
- **Error 1 during Homing**: make sure $39 is turned on
- **Error 8 or 9 after hitting E-stop**: the typical routine after hitting the E-stop will be to first ‘reset’ the board and then ‘unlock’ it, you’ll get either of these errors if a step in this process is missed
- **Error 10 when changing firmware settings:** you're likely trying to turn on a setting that first requires homing ($22) to be enabled before the other setting can be enabled
- **Error 24 in gSender**: check that you are not loading up a regular file while in Laser mode

See the meaning of all Alarms here: <a href="https://github.com/grblHAL/core/blob/master/alarms.h" target="_blank" rel="noopener">https://github.com/grblHAL/core/blob/master/alarms.h</a> or type `$eag` into the console

### Other Troubleshooting

- If there’s a problem when you “Import Settings” from an older Firmware version to a new one, this is expected. Different versions of the SLB have different EEPROM outputs that won’t be compatible with each other, so for the duration of Beta testing you’ll just have to note down your changed settings manually and revert them manually on new Firmware versions
- If you change a firmware setting and notice that it isn’t taking effect, check if the setting description mentions that you need to “hard reset” your board for the changes to take effect. Some settings need this, and this just means you’ll need to turn your board off and back on again before the change takes effect.
- If the gSender screen ever goes black, please let us know what happened leading up till that point, then use the toolbar to select ‘View’ ➜ ‘Reload’, to get refreshed and the screen showing once again
- If you hear the SLB ‘clicking’ when you change EEPROM settings, this is normal
- If you’re experiencing any issues with SLB ‘Disconnection’ while running your CNC, try switching from USB over to Ethernet

## Troubleshooting Lights

There are several other small ‘status’ lights you’ll notice as you look around on the SLB. We put these in place to help with general troubleshooting anytime you’re not getting the behaviour you expect. These lights directly reflect the hardware they’re attached to, allowing you to check the raw hardware connections before they’re processed by the SLBs firmware or your g-code sender. This means they’re not able to be inverted or changed, they’ll always have the same behaviour.

This is a list of all the lights and how they function:

![](/_images/_superlongboard/slb_slb-leds.jpg){.aligncenter .size-medium}

**NOTE:** only LEDs set up for ‘inputs’ like limit switches and E-stop buttons need the hardware to be hooked up to confirm an incoming signal. Otherwise, LEDs for ‘outputs’ like PWM or motor signals will still turn on and off without needing to hook up the components.

[su_table responsive="yes" fixed="yes"]
<table>
<tbody>
<tr style="background: grey !important;">
<td><b>Section</b></td>
<td><b>#</b></td>
<td><b>Why is it lit up?</b></td>
<td><b>Type</b></td>
<td><b>Colour</b></td>
</tr>
<tr>
<td style="background: #e06666 !important;" rowspan="3"><b>Power</b></td>
<td>1</td>
<td>E-stop pressed or power disruption</td>
<td>In</td>
<td style="background: #ff0000 !important;">Red</td>
</tr>
<tr>
<td>2</td>
<td>5V power is working on the board</td>
<td>In</td>
<td style="background: #00ff00 !important;">Green</td>
</tr>
<tr>
<td>3</td>
<td>3.3V power is working on the board</td>
<td>In</td>
<td style="background: #00ff00 !important;">Green</td>
</tr>
<tr>
<td style="background: #a4c2f4 !important;" rowspan="7"><b>Communication</b></td>
<td>4</td>
<td>RS485 TX signals are being sent</td>
<td>Out</td>
<td style="background: #00ff00 !important;">Green</td>
</tr>
<tr>
<td>5</td>
<td>RS485 RX signals are being sent</td>
<td>In</td>
<td style="background: #ff0000 !important;">Red</td>
</tr>
<tr>
<td>6</td>
<td>USB connection is active</td>
<td>Com</td>
<td style="background: #00ff00 !important;">Green</td>
</tr>
<tr>
<td>7</td>
<td>CAN bus TX signals are being sent</td>
<td>Out</td>
<td style="background: #00ff00 !important;">Green</td>
</tr>
<tr>
<td>8</td>
<td>CAN bus RX signals are being sent</td>
<td>In</td>
<td style="background: #ff0000 !important;">Red</td>
</tr>
<tr>
<td>9</td>
<td>Ethernet is connected at the standard speed
*Side of board where plug goes in</td>
<td>Out</td>
<td style="background: #00ff00 !important;">Green</td>
</tr>
<tr>
<td>10</td>
<td>Ethernet data is being sent/received (blinking)
*Side of board where plug goes in</td>
<td>Com</td>
<td style="background: #ffff00 !important;">Yellow</td>
</tr>
<tr>
<td style="background: #ffee66 !important;" rowspan="4"><b>Accessory Outputs</b></td>
<td>11</td>
<td>Switch 1 output is active</td>
<td>Out</td>
<td style="background: #00ff00 !important;">Green</td>
</tr>
<tr>
<td>12</td>
<td>Switch 2 output is active</td>
<td>Out</td>
<td style="background: #00ff00 !important;">Green</td>
</tr>
<tr>
<td>13</td>
<td>Aux power 1 output is active</td>
<td>Out</td>
<td style="background: #00ff00 !important;">Green</td>
</tr>
<tr>
<td>14</td>
<td>Aux power 2 output is active</td>
<td>Out</td>
<td style="background: #00ff00 !important;">Green</td>
</tr>
<tr>
<td style="background: #f6a66b !important;" rowspan="2"><b>Spindle/RS485</b></td>
<td>15</td>
<td>Laser PWM output pin is sending signals
<b>Note:</b> this is not dependant on $32 or gSender being in laser mode, this relies on the active ‘spindle’ output being “SLB_LASER” and there being a specified power output while M3 or M4 are on, see the laser section to read about this</td>
<td>Out</td>
<td style="background: #ff0000 !important;">Red</td>
</tr>
<tr>
<td>16</td>
<td>Spindle PWM output pin is sending signals
<b>Note:</b> checks and setup for this is the same as for the laser PWM output above, also only one of these lights will be able to be on at one time since only one ‘spindle’ can be active at once</td>
<td>Out</td>
<td>White</td>
</tr>
<tr>
<td style="background: #b27cc3 !important;" rowspan="4"><b>Limit Switches</b></td>
<td>17</td>
<td>Z-axis limit switch is closed</td>
<td>In</td>
<td style="background: #ffff00 !important;">Yellow</td>
</tr>
<tr>
<td>18</td>
<td>Y2-axis limit switch is closed</td>
<td>In</td>
<td style="background: #ffff00 !important;">Yellow</td>
</tr>
<tr>
<td>19</td>
<td>Y1-axis limit switch is closed</td>
<td>In</td>
<td style="background: #ffff00 !important;">Yellow</td>
</tr>
<tr>
<td>20</td>
<td>X-axis limit switch is closed</td>
<td>In</td>
<td style="background: #ffff00 !important;">Yellow</td>
</tr>
<tr>
<td style="background: #9deefa !important;" rowspan="3"><b>Rotary</b></td>
<td>21</td>
<td>A-axis limit switch is closed</td>
<td>In</td>
<td style="background: #ffff00 !important;">Yellow</td>
</tr>
<tr>
<td>22</td>
<td>A-axis motor is reaching its stall point</td>
<td>Out</td>
<td style="background: #ff0000 !important;">Red</td>
</tr>
<tr>
<td>23</td>
<td>A-axis motor is enabled
<b>Note</b>: depending on what external motor driver you wire up, this light might be inverted and instead light up for ‘disabled’</td>
<td>Out</td>
<td style="background: #00ff00 !important;">Green</td>
</tr>
<tr>
<td style="background: #92d177 !important;" rowspan="4"><b>XYZA Axis Enabled</b></td>
<td>24</td>
<td>Z-axis motor is enabled</td>
<td>Out</td>
<td style="background: #00ff00 !important;">Green</td>
</tr>
<tr>
<td>25</td>
<td>Y2-axis motor is enabled</td>
<td>Out</td>
<td style="background: #00ff00 !important;">Green</td>
</tr>
<tr>
<td>26</td>
<td>Y1-axis motor is enabled</td>
<td>Out</td>
<td style="background: #00ff00 !important;">Green</td>
</tr>
<tr>
<td>27</td>
<td>X-axis motor is enabled
<b>Note</b>: all motors will typically light as ‘enabled' for any movement, unless they’re constantly lit from keeping them energized using $37</td>
<td>Out</td>
<td style="background: #00ff00 !important;">Green</td>
</tr>
<tr>
<td style="background: #92d177 !important;" rowspan="4"><b>XYZA Axis Stalled
</b></td>
<td>28</td>
<td>Z-axis motor is reaching its stall point</td>
<td>Out</td>
<td style="background: #ff0000 !important;">Red</td>
</tr>
<tr>
<td>29</td>
<td>Y2-axis motor is reaching its stall point</td>
<td>Out</td>
<td style="background: #ff0000 !important;">Red</td>
</tr>
<tr>
<td>30</td>
<td>Y1-axis motor is reaching its stall point</td>
<td>Out</td>
<td style="background: #ff0000 !important;">Red</td>
</tr>
<tr>
<td>31</td>
<td>X-axis motor is reaching its stall point</td>
<td>Out</td>
<td style="background: #ff0000 !important;">Red</td>
</tr>
<tr>
<td style="background: #7586fe !important;" rowspan="9"><b>Main LED Strip</b></td>
<td>32</td>
<td>Flood command (M8) is on</td>
<td>Out</td>
<td style="background: #3551fa !important;">Blue</td>
</tr>
<tr>
<td>33</td>
<td>Mist command (M7) is on</td>
<td>Out</td>
<td style="background: #3551fa !important;">Blue</td>
</tr>
<tr>
<td>34</td>
<td>Door input signal is closed</td>
<td>In</td>
<td style="background: #ffff00 !important;">Yellow</td>
</tr>
<tr>
<td>35</td>
<td>Tool length sensor signal is closed</td>
<td>In</td>
<td style="background: #ffff00 !important;">Yellow</td>
</tr>
<tr>
<td>36</td>
<td>Probe input signal is closed</td>
<td>In</td>
<td style="background: #ffff00 !important;">Yellow</td>
</tr>
<tr>
<td>37</td>
<td>Action button 1 is being pressed</td>
<td>In</td>
<td style="background: #ffff00 !important;">Yellow</td>
</tr>
<tr>
<td>38</td>
<td>Action button 2 is being pressed</td>
<td>In</td>
<td style="background: #ffff00 !important;">Yellow</td>
</tr>
<tr>
<td>39</td>
<td>Action button 3 is being pressed</td>
<td>In</td>
<td style="background: #ffff00 !important;">Yellow</td>
</tr>
<tr>
<td>40</td>
<td>E-stop is pressed (circuit open)</td>
<td>In</td>
<td style="background: #ff0000 !important;">Red</td>
</tr>
</tbody>
</table>
[/su_table]

## Useful commands

<ul>
  <li><b>$</b>   reminder of all grbl commands</li>
  <li><b>$$</b>   lists all Firmware settings and their values</li>
  <li><b>$</b>### tells you the value of the specific Firmware setting (ex. "$22")</li>
  <li><b>$rst=$</b>   resets all your EEPROM settings to the default Firmware values</li>
  <li><b>?</b>   reports any active inputs plus some other useful info</li>
  <li><b>$g</b>   lists current active grbl Modals</li>
  <li><b>$i</b>   tells you information on your board Firmware Version and Plugins</li>
  <li><b>$$=</b>###   will let you know the Name and Description of that Setting (ex. "$$=22")</li>
  <li><b>$#</b>   all the currently stored machine offsets</li>
  <li><b>$esg</b>   will tell you the Names and Descriptions of all Settings</li>
  <li><b>$eag</b>   will tell you the Names and Descriptions of all Alarms</li>
</ul>

## <span style="color: #ff0000;">Alarms List</span>

[su_table responsive="yes"]
<table>
<thead>
<tr>
<th>Alarm Code</th>
<th>Message</th>
<th>Description</th>
<th>Example</th>
</tr>
</thead>
<tbody>
<tr>
<td><b>1</b></td>
<td>Hard limit</td>
<td style="text-align: left;">Hard limit has been triggered. Machine position is likely lost due to sudden halt. Re-homing is highly recommended.</td>
<td><a href="https://youtu.be/I1EhAPNXdzQ?t=208" target="_blank" rel="noopener">Example</a></td>
</tr>
<tr>
<td><b>2</b></td>
<td>Soft limit</td>
<td style="text-align: left;">Soft limit alarm. G-code motion target exceeds machine travel. Machine position retained. Alarm may be safely unlocked.</td>
<td><a href="https://youtu.be/I1EhAPNXdzQ?t=226" target="_blank" rel="noopener">Example</a></td>
</tr>
<tr>
<td><b>3</b></td>
<td>Abort during cycle</td>
<td style="text-align: left;">Reset while in motion. Machine position is likely lost due to sudden halt. Re-homing is highly recommended. May be due to issuing g-code commands that exceed the limit of the machine.</td>
<td></td>
</tr>
<tr>
<td><b>4</b></td>
<td>Probe fail</td>
<td style="text-align: left;">Probe fail. Probe is not in the expected initial state before starting probe cycle when G38.2 and G38.3 is not triggered and G38.4 and G38.5 is triggered. Your bit is likely making contact with the touch plate or the circuit is completed before the bit is moving. Move the bit away from the touch plate.</td>
<td><a href="https://youtu.be/I1EhAPNXdzQ?t=267" target="_blank" rel="noopener">Example</a></td>
</tr>
<tr>
<td><b>5</b></td>
<td>Probe fail</td>
<td style="text-align: left;">Probe fail. Probe did not contact the workpiece within the programmed travel for G38.2 and G38.4. Your bit is too far away from the touch plate. Move the bit closer, it should be within 6-12mm (1/4 -1/2in) away.</td>
<td><a href="https://youtu.be/I1EhAPNXdzQ?t=306" target="_blank" rel="noopener">Example</a></td>
</tr>
<tr>
<td><b>6</b></td>
<td>Homing fail</td>
<td style="text-align: left;">Homing fail. The active homing cycle was reset.</td>
<td></td>
</tr>
<tr>
<td><b>7</b></td>
<td>Homing fail</td>
<td style="text-align: left;">Homing fail. Safety door was opened during homing cycle.</td>
<td></td>
</tr>
<tr>
<td><b>8</b></td>
<td>Homing fail</td>
<td style="text-align: left;">Homing fail. Pull off travel failed to clear limit switch. The machine is within the limit switches range when it tries to move away. Try increasing pull-off setting or check wiring.</td>
<td><a href="https://youtu.be/jmiaWA5tiVw?t=563" target="_blank" rel="noopener">Example</a></td>
</tr>
<tr>
<td><b>9</b></td>
<td>Homing fail</td>
<td style="text-align: left;">Homing fail. Could not find limit switch within search distances. Try increasing max travel, decreasing pull-off distance, or check wiring. The limit switch wasn't triggered in the distances expected. If your z-axis is moving away from the switch when homing, check your firmware and confirm you have the correct profile for your machine.</td>
<td><a href="https://youtu.be/jmiaWA5tiVw?t=531" target="_blank" rel="noopener">Example</a></td>
</tr>
<tr>
<td><b>10</b></td>
<td>E-stop asserted</td>
<td style="text-align: left;">E-stop asserted. Clear and reset. Untwist your E-stop.</td>
<td></td>
</tr>
<tr>
<td><b>11</b></td>
<td>Homing required</td>
<td style="text-align: left;">Homing required. Execute homing command ($H) to continue. Your machine can't start up until you first Home.</td>
<td></td>
</tr>
<tr>
<td><b>12</b></td>
<td>Limit switch engaged</td>
<td style="text-align: left;">Limit switch engaged. Clear before continuing. A limit switch is on or off when it’s not supposed to, check if you've triggered them accidentally or you set them up the wrong way. fixed</td>
<td></td>
</tr>
<tr>
<td><b>13</b></td>
<td>Probe protection</td>
<td style="text-align: left;">Probe protection triggered. Clear before continuing.</td>
<td></td>
</tr>
<tr>
<td><b>14</b></td>
<td>SaS timeout</td>
<td style="text-align: left;">Spindle at speed timeout. Clear before continuing. This can also trigger if you've set up a VFD that's not sending back correct signals to the board.</td>
<td></td>
</tr>
<tr>
<td><b>15</b></td>
<td>Homing fail</td>
<td style="text-align: left;">Homing fail. Could not find second limit switch for auto squared axis within search distances. Try increasing max travel, decreasing pull-off distance, or check wiring.</td>
<td></td>
</tr>
<tr>
<td><b>16</b></td>
<td>Selftest failed</td>
<td style="text-align: left;">Power on selftest (POS) failed.</td>
<td></td>
</tr>
<tr>
<td><b>17</b></td>
<td>Motor fault</td>
<td style="text-align: left;">Motor fault.</td>
<td></td>
</tr>
<tr>
<td><b>18</b></td>
<td>Homing fail</td>
<td style="text-align: left;">Homing fail. Bad configuration.</td>
<td></td>
</tr>
</tbody>
</table>
[/su_table]

## <span style="color: #ff8b3d;">Errors List</span>

[su_table responsive="yes"]
<table>
<thead>
<tr>
<th>Error Code</th>
<th>Message</th>
<th>Description</th>
</tr>
</thead>
<tbody>
<tr>
<td><b>1</b></td>
<td>Expected command letter</td>
<td style="text-align: left;">G-code words consist of a letter and a value. Letter was not found.</td>
</tr>
<tr>
<td><b>2</b></td>
<td>Bad number format</td>
<td style="text-align: left;">Missing the expected G-code word value or numeric value format is not valid.</td>
</tr>
<tr>
<td><b>3</b></td>
<td>Invalid statement</td>
<td style="text-align: left;">Grbl ‘$’ system command was not recognized or supported.</td>
</tr>
<tr>
<td><b>4</b></td>
<td>Value &lt; 0</td>
<td style="text-align: left;">Negative value received for an expected positive value.</td>
</tr>
<tr>
<td><b>5</b></td>
<td>Setting disabled</td>
<td style="text-align: left;">Homing cycle failure. Homing is not enabled via settings.</td>
</tr>
<tr>
<td><b>6</b></td>
<td>Value &lt; 3 μsec</td>
<td style="text-align: left;">Minimum step pulse time must be greater than 3μsec.</td>
</tr>
<tr>
<td><b>7</b></td>
<td>EEPROM read fail. Using defaults</td>
<td style="text-align: left;">An EEPROM read failed. Auto-restoring affected EEPROM to default values.</td>
</tr>
<tr>
<td><b>8</b></td>
<td>Not idle</td>
<td style="text-align: left;">Grbl ‘$’ command cannot be used unless Grbl is IDLE. Ensures smooth operation during a job.</td>
</tr>
<tr>
<td><b>9</b></td>
<td>G-code lock</td>
<td style="text-align: left;">G-code commands are locked out during alarm or jog state.</td>
</tr>
<tr>
<td><b>10</b></td>
<td>Homing not enabled</td>
<td style="text-align: left;">Soft limits cannot be enabled without homing also enabled.</td>
</tr>
<tr>
<td><b>11</b></td>
<td>Line overflow</td>
<td style="text-align: left;">Max characters per line exceeded. Received command line was not executed.</td>
</tr>
<tr>
<td><b>12</b></td>
<td>Step rate &gt; 30kHz</td>
<td style="text-align: left;">Grbl ‘$’ setting value cause the step rate to exceed the maximum supported.</td>
</tr>
<tr>
<td><b>13</b></td>
<td>Check Door</td>
<td style="text-align: left;">Safety door detected as opened and door state initiated.</td>
</tr>
<tr>
<td><b>14</b></td>
<td>Line length exceeded</td>
<td style="text-align: left;">Build info or startup line exceeded EEPROM line length limit. Line not stored.</td>
</tr>
<tr>
<td><b>15</b></td>
<td>Travel exceeded</td>
<td style="text-align: left;">Jog target exceeds machine travel. Jog command has been ignored.</td>
</tr>
<tr>
<td><b>16</b></td>
<td>Invalid jog command</td>
<td style="text-align: left;">Jog command has no ‘=’ or contains prohibited g-code.</td>
</tr>
<tr>
<td><b>17</b></td>
<td>Setting disabled</td>
<td style="text-align: left;">Laser mode requires PWM output.</td>
</tr>
<tr>
<td><b>20</b></td>
<td>Unsupported command</td>
<td style="text-align: left;">Unsupported or invalid g-code command found in block.</td>
</tr>
<tr>
<td><b>21</b></td>
<td>Modal group violation</td>
<td style="text-align: left;">More than one g-code command from same modal group found in block.</td>
</tr>
<tr>
<td><b>22</b></td>
<td>Undefined feed rate</td>
<td style="text-align: left;">Feed rate has not yet been set or is undefined.</td>
</tr>
<tr>
<td><b>23</b></td>
<td>Invalid gcode ID:23</td>
<td style="text-align: left;">G-code command in block requires an integer value.</td>
</tr>
<tr>
<td><b>24</b></td>
<td>Invalid gcode ID:24</td>
<td style="text-align: left;">More than one g-code command that requires axis words found in block.</td>
</tr>
<tr>
<td><b>25</b></td>
<td>Invalid gcode ID:25</td>
<td style="text-align: left;">Repeated g-code word found in block.</td>
</tr>
<tr>
<td><b>26</b></td>
<td>Invalid gcode ID:26</td>
<td style="text-align: left;">No axis words found in block for g-code command or current modal state which requires them.</td>
</tr>
<tr>
<td><b>27</b></td>
<td>Invalid gcode ID:27</td>
<td style="text-align: left;">Line number value is invalid.</td>
</tr>
<tr>
<td><b>28</b></td>
<td>Invalid gcode ID:28</td>
<td style="text-align: left;">G-code command is missing a required value word.</td>
</tr>
<tr>
<td><b>29</b></td>
<td>Invalid gcode ID:29</td>
<td style="text-align: left;">G59.x work coordinate systems are not supported.</td>
</tr>
<tr>
<td><b>30</b></td>
<td>Invalid gcode ID:30</td>
<td style="text-align: left;">G53 only allowed with G0 and G1 motion modes.</td>
</tr>
<tr>
<td><b>31</b></td>
<td>Invalid gcode ID:31</td>
<td style="text-align: left;">Axis words found in block when no command or current modal state uses them.</td>
</tr>
<tr>
<td><b>32</b></td>
<td>Invalid gcode ID:32</td>
<td style="text-align: left;">G2 and G3 arcs require at least one in-plane axis word.</td>
</tr>
<tr>
<td><b>33</b></td>
<td>Invalid gcode ID:33</td>
<td style="text-align: left;">Motion command target is invalid.</td>
</tr>
<tr>
<td><b>34</b></td>
<td>Invalid gcode ID:34</td>
<td style="text-align: left;">Arc radius value is invalid.</td>
</tr>
<tr>
<td><b>35</b></td>
<td>Invalid gcode ID:35</td>
<td style="text-align: left;">G2 and G3 arcs require at least one in-plane offset word.</td>
</tr>
<tr>
<td><b>36</b></td>
<td>Invalid gcode ID:36</td>
<td style="text-align: left;">Unused value words found in block.</td>
</tr>
<tr>
<td><b>37</b></td>
<td>Invalid gcode ID:37</td>
<td style="text-align: left;">G43.1 dynamic tool length offset is not assigned to configured tool length axis.</td>
</tr>
<tr>
<td><b>38</b></td>
<td>Invalid gcode ID:38</td>
<td style="text-align: left;">Tool number greater than max supported value.</td>
</tr>
</tbody>
</table>
[/su_table]
