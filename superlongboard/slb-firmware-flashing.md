---
title: Firmware & Flashing
menu_order: 6
post_status: publish
post_excerpt: 
post_date: 2024-04-03 18:00:00
taxonomy:
    knowledgebase_cat: slb-handbook
    knowledgebase_tag:
        - slb
custom_fields:
    KBName: SuperLongBoard
    basepress_post_icon: bp-caret-right
skip_file: no
featured_image: _images/_superlongboard/_firmware/slb_fi_p1_Connected.jpg
---

Your board will likely ship with the latest firmware already installed, but we occasionally make updates to add new features or address any discovered issues. You may also choose to re-flash the firmware onto your board if you’ve attempted to customize it or for troubleshooting purposes.

<b><span class="redText">Do not flash your SLB unless you've done it before and are absolutely sure you know what you're doing or are being guided by our team.</span> The flashing process can be touchy the first time, so if you're having problems then please contact our team first otherwise be prepared to accept a regretful outcome.</b>

Before getting started, **check what your current version is** by going to the ‘Console’ of your g-code sender and send the command `$i`. The result will be a long list of text in square brackets. If you scroll down to about the 9th line you’ll see something like “[BOARD:” where you’ll also see the version number at the end. Compare this to the version list below to see which one you’d like to flash:

**Most Recent Firmware:**

- SLB: <a href="https://drive.google.com/file/d/1LZ1YFt5J4Ws01XqielJuWaJpGJ2OgbCj/view?usp=drive_link" target="_blank" rel="noopener">5.0.5b</a>
  - Updated default A-axis step/mm to match typical Vortex setups using 32nd microstepping
  - Updated defaults to accommodate some machine setups that couldn't handle the max speeds and accelerations of the SLB
  - Changed min spindle speed, spindle on delay, and default enabled spindles to match typical spindle setups using the SLB
- SLB EXT (AltMill): <a href="https://drive.google.com/file/d/1M3tsSpptwMZusubu4m91cdJ5OqTFyJH8/view?usp=drive_link" target="_blank" rel="noopener">5.0.11</a>

[su_spoiler title="<b>Past Versions:</b>" open="no" style="fancy" icon="chevron" anchor_in_url="yes"]

- <a href="https://drive.google.com/file/d/1-1W322z5idOQmhREUlAVHQBAa6PCsN63/view?usp=sharing" target="_blank" rel="noopener">5.0.5</a>: default for June ➜ Oct 2024
  - Updated default homing speed to stop occasional disconnection issues
  - Fixed E-stop hit requiring board power cycle to clear
- <a href="https://drive.google.com/file/d/1OkQO__QnYzhPuF42d4AN5KY_MbVRJlqy/view?usp=drive_link" target="_blank" rel="noopener">5.0.3</a>: firmware on original batch of 500 SLBs (April 2024)

[/su_spoiler]

## Flashing Summary

To successfully flash new firmware onto your SLB, you’ll need:

1. The **firmware file**; all versions are listed above as “.hex” files to download
1. A computer that can run either **gSender** or the **STM Cube Programmer** software to perform the flashing
1. The SLB connected to that **computer over USB** (you can’t flash over Ethernet because the MCU on the SLB can’t support it, but you can return to using your Ethernet connection once flashing is complete)
1. A 12-24V power supply to **power the SLB** during flashing
1. Have separately noted down any **firmware settings** that are particular to your machine setup like for limit switches, macros, etc. New firmware can sometimes override existing settings so having a list can help you double check if you need to make any manual tweaks afterwards.
1. For your safety, if there are any accessories that receive a control signal from the SLB, **turn their power off** just in case the flashing process inadvertently sends control signals to those accessories. This would be unsafe to have a spindle or laser power on when you don’t expect it to. You can turn these back on after flashing is complete.

You can choose to either use gSender or the STM Cube Programmer software to update your SLB, the steps for either option are below:

### gSender Flashing

1. Be connected to your SLB over USB with the power on, ensure the firmware selected is 'grblHAL' not 'grbl'

   ![](/_images/_superlongboard/_firmware/slb_fi_p1_Connected.png){.aligncenter .size-medium}
1. Go to the ‘Firmware’ tool and click the 'Flash grblHAL' button

   ![](/_images/_superlongboard/_firmware/slb_fi_p2_FlashgrblHAL.jpg){.aligncenter .size-medium}
1. Ensure the COM port is correct (matches the board you’re connected to)
1. Click ‘Choose File’ to select the “.hex” firmware file you plan to update to, in the picture below it’s the 5.0.7 firmware
1. Click ‘Yes’ to begin the flashing process. If it stops before 100% and you see an error for:
   - "LIBUSB_ERROR_NOT_SUPPORTED", you'll need to [update your Windows driver](#windows-driver-update)
   - "Unable to find valid device", you might have [installed your Windows drivers incorrectly](#bad-driver-install)
   - "LIBUSB_ERROR_ACCESS", your Ubuntu device might be having a [USB rights issue](#ubuntu-driver-update)

   ![](/_images/_superlongboard/_firmware/slb_fi_p3_Choose.jpg){.aligncenter .size-medium}
1. Once you see the loading bar at 100%, flashing is complete. Exit out of the firmware window and switch off the board with the power switch at the back then turn it back on again.

   ![](/_images/_superlongboard/_firmware/slb_fi_p4_Flashing.jpg){.aligncenter .size-medium}
1. Once it’s back on, you should be able to re-connect to it in gSender. Go to the ‘Console’ tab and send the command `$rst=$` to revert your machine back to the default firmware settings (you shouldn't get any errors when you send this command).

   ![](/_images/_superlongboard/_firmware/slb_fi_p5_ConsoleRST.jpg){.aligncenter .size-medium}
1. Power the board off and then back on one more time after sending the command. Finally, if you had any specific settings from your previous setup that you want to check or reload, connect back to gSender and change those firmware values back. Remember to hit “Apply New Settings” when you’re doing this and ensure that the settings are being re-added correctly, if they don’t seem to be sticking then make sure that your SLB is in an ‘Idle’ state, cleared of all Alarms, and try turning the SLB off and back on again.

Congrats are in order, well done! If you go back to the ‘Console’ you should now see that sending the `$i` command will give you new text that matches up with the update you’ve made.

### STM Cube Flashing

Download the software from here (we recommend version 2.15.0): <a href="https://www.st.com/en/development-tools/stm32cubeprog.html#st-get-software" target="_blank" rel="noopener">https://www.st.com/en/development-tools/stm32cubeprog.html#st-get-software</a>

1. On the SLB, switch off the power toggle switch at the black of the board or unplug it from power
1. Use a jumper or metal tipped tool like a screwdriver or Allen key to short the **BOOT pin** (shown) and hold it in place
![](/_images/_superlongboard/_firmware/slb_fi_p6_BootPin.jpg){.aligncenter .size-medium}
1. Now turn the SLBs power toggle switch back on or reconnect power. You should see that most LEDs on the board are turned off now, especially the main Status LED.
1. You can remove or let go of the BOOT jumper now.
1. With the STM32 Cube Programmer opened on your computer:
   1. Select 'USB' in the blue drop down box at the top of the right of the window
   1. Click the refresh button next to 'Port', the board will typically show up as “USB1”
   1. If the board shows up, press the green 'Connect' button. If you still see “No DFU”, check your setup then click the refresh button again
   1. Go to the 'Erasing & Programming' tab on the left side of the screen
   1. Select the blue 'Browse' button to select the latest hex file (firmware file) on your computer
   1. Press the blue 'Start Programming' button

   ![](/_images/_superlongboard/_firmware/slb_fi_p7_STI.jpg){.aligncenter .size-medium}
1. Once complete, you’ll have to exit out of a bunch of small windows
1. Switch off the board power switch then turn back on again, then reconnect to the board in gSender, ioSender, or any other g-code sender.
1. Follow the same last 2 steps (7 and 8) of the gSender Flashing process and you should be done!

### Windows Driver Update

If you’re failing to update your SLBs firmware and see the message “**Error: LIBUSB_ERROR_NOT_SUPPORTED**”, this stems from the sometimes problematic way that Windows handles USB devices. This isn’t a problem for Linux or Mac systems, but if your Windows computer is having this issue it can still be fixed by overriding the wrong driver it’s using with the correct one.

To do this we’ll use a program called Zadig. The program is only needed to make the fix, which should permanently fix SLB flashing issues:

1. Download Zadig at <a href="https://zadig.akeo.ie/#" target="_blank" rel="noopener">https://zadig.akeo.ie/#</a> (there's an <a href="https://github.com/pbatard/libwdi/releases/download/v1.5.0/zadig-2.8.exe" target="_blank" rel="noopener">alternate download here</a>).
1. Put the SLB into DFU mode. There is two methods for this:
   - Connect to the SLB in gSender and type `$dfu` in the Console tab. This will disconnect it from gSender and it will no longer appear in the dropdown connection area. **This step needs to happen successfully, if you get an error, assess your setup and do not move on to the next step.**
   - Or use a jumper, flathead screwdriver, or other small piece of metal to short between two pins on the SLB near the USB port. The two pins will have “SPIN” written near them, and you'll need to be shorting them while you use the power toggle switch to turn the SLB on.
1. Open Zadig and in the toolbar click ‘Options’ ➜ 'List all Devices'
1. In the main dropdown, find and select the “STM32 Bootloader” device. This name might change depending on your current operating system.
![](/_images/_superlongboard/_firmware/slb_fi_p8_SMT32.png){.aligncenter .size-medium}
1. Make sure that “WinUSB” is the selected driver type.
1. Click the “Replace Driver” button and wait for the operation to complete (if you happen to accidentally delete other drivers in the process, restarting your computer should bring them back).
1. Power cycle the board to exit DFU mode, then give flashing another shot. If you followed all the steps you should now be able to change and update your SLBs firmware!

#### Bad Driver Install

If you got the error message "**Unable to find valid device using vendor ID and product ID**" and you just fixed your Windows drivers then that means you made a mistake in the driver update steps. If you weren't messing with drivers, then just ensure your SLB is getting into DFU mode by typing `$dfu` into a g-code sender console or using the pin short method shown in the [STM Cube Flashing section](#stm-cube-flashing).

To fix the Windows driver:

1. Open '**Device Manager**' in your Windows start menu
![](/_images/_gsender/_issues/gs_is_cm_device-manager.png){.aligncenter .size-medium}
1. Look under the '**Ports**' or '**Universal Serial Bus**' headings for the SLB which should include "STM32" in the name
![](/_images/_superlongboard/_firmware/slb_fi_p9_stm32-device.png){.aligncenter .size-full .nar}
1. Right-click ➜ Uninstall device, then power cycle the board
1. Once powered back up and reconnected, the SLB should reappear looking more normal. With this done, you can try flashing again - or if Windows still didn't install the correct driver then go through the [Windows Driver Update](#windows-driver-update) again.
![](/_images/_superlongboard/_firmware/slb_fi_p10_stm32-reset.png){.aligncenter .size-full .nar}
1. If this still doesn't seem to work, you might've deleted the standard STM driver while using Zadig since the SLB wasn't in DFU mode. In this case go to <a href="https://www.st.com/en/development-tools/stsw-stm32102.html" target="_blank" rel="noopener">STMs website to re-download the drivers</a> (they should work even though they say they're for Windows 7) then try flashing again.

[su_spoiler title="<h3>Ubuntu Driver Update</h3>" open="no" style="fancy" icon="chevron" anchor_in_url="yes"]

To set up **udev** rules to give your user account access to the SLB on Linux, follow these steps:

1. Plug in your SLB
1. Open a terminal and list all connected USB devices with `lsusb`
1. Note the vendor ID and product ID. In the example, `1234` is the vendor ID and `5678` is the product ID.

   ```bash
   Bus 001 Device 002: ID 1234:5678 Sample USB Device
   ```

1. Create a new `udev` rule file in the `/etc/udev/rules.d/` directory; we'll name it `slb.rules`:

   ```bash
   sudo nano /etc/udev/rules.d/slb.rules
   ```

1. Add the following line to the file, replacing `1234` with the vendor ID and `5678` with the product ID:

   ```bash
   SUBSYSTEM=="usb", ATTR{idVendor}=="1234", ATTR{idProduct}=="5678", MODE="0660", GROUP="plugdev"
   ```

1. Now add your user to the new `plugdev` group:

   ```bash
   sudo usermod -aG plugdev $USER
   ```

1. Log out and log back in to apply the group changes.
1. Reload the `udev` rules to apply the remaining changes:

   ```bash
   sudo udevadm control --reload-rules
   sudo udevadm trigger
   ```

1. Finally, unplug and replug your SLB then check the device permissions have been set correctly (the exact path may vary according to your system):

   ```bash
   ls -l /dev/bus/usb/001/002
   ```

1. You may also need to issue `sudo chmod -R 777 /dev/bus/usb/`

After completing these steps, you should have access to the SLB without needing `sudo`. If you still encounter issues, make sure that no other kernel drivers are conflicting with the device access. If everything is looking good, then go back up to continue [Firmware flashing with gSender](#gsender-flashing).

[/su_spoiler]

## Settings Descriptions

If you'd like to know all the ins and outs of the SLB's firmware, and broader settings of grblHAL as a whole, you'll find it all in the tables below.

For added clarity, settings that are currently unused on the SLB have been highlighted in <span style="color: var(--sl-orange);">orange</span>. Also, the ones highlighted in <span style="color: var(--sl-blue-d);">blue</span> though they are supported we don't advise changing or are still building up documentation on.

[su_table responsive="yes"]
<table>
<thead>
   <tr>
     <th>$</th>
     <th>Name</th>
     <th>Value (number)</th>
     <th>Units</th>
     <th>Description</th>
     <th>How to Use</th>
   </tr>
</thead>
<tbody>
   <tr>
     <td><b>$0</b></td>
     <td>Step pulse time</td>
     <td><b>5</b></td>
     <td>microseconds</td>
     <td style="text-align: left;">Sets time length per step. Minimum 2 microseconds.<br><br>This needs to be reduced from the default value of 10 when max. step rates exceed approximately 80 kHz.</td>
     <td></td>
   </tr>
   <tr>
     <td><b>$1</b></td>
     <td>Step idle delay</td>
     <td><b>254</b></td>
     <td>milliseconds</td>
     <td style="text-align: left;">Sets a short hold delay when stopping to let dynamics settle before disabling steppers. Value 255 keeps motors enabled.</td>
     <td></td>
   </tr>
   <tr>
     <td><b>$2</b></td>
     <td>Step pulse invert</td>
     <td>X: <b>OFF</b><br>Y: <b>OFF</b><br>Z: <b>OFF</b><br>A: <b>OFF</b><br>(0)</td>
     <td></td>
     <td style="text-align: left;">Inverts the step signals (active low).</td>
     <td></td>
   </tr>
   <tr>
     <td><b>$3</b></td>
     <td>Step direction invert</td>
     <td>X: <b>OFF</b><br>Y: <b>ON</b><br>Z: <b>ON</b><br>A: <b>OFF</b><br>(6)</td>
     <td></td>
     <td style="text-align: left;">Inverts the direction signals (active low).</td>
     <td></td>
   </tr>
   <tr>
     <td><b>$4</b></td>
     <td>Invert stepper enable pin(s)</td>
     <td>X: <b>ON</b><br>Y: <b>ON</b><br>Z: <b>ON</b><br>A: <b>ON</b><br>(15)</td>
     <td></td>
     <td style="text-align: left;">Inverts the stepper driver enable signals. Most drivers uses active low enable requiring inversion.<br><br>NOTE: If the stepper drivers shares the same enable signal only X is used.</td>
     <td></td>
   </tr>
   <tr>
     <td><b>$5</b></td>
     <td>Invert limit pins</td>
     <td>X: <b>ON</b><br>Y: <b>ON</b><br>Z: <b>ON</b><br>A: <b>ON</b><br>(15)</td>
     <td></td>
     <td style="text-align: left;">Inverts the axis limit input signals.</td>
     <td></td>
   </tr>
   <tr>
     <td><b>$6</b></td>
     <td>Invert probe pin</td>
     <td><b>Enabled</b> (1)</td>
     <td></td>
     <td style="text-align: left;">Inverts the probe input pin signal.</td>
     <td></td>
   </tr>
   <tr>
     <td><b>$8</b></td>
     <td>Ganged axes direction invert</td>
     <td><b>Disabled</b> (0)</td>
     <td></td>
     <td style="text-align: left;">Inverts the direction signals for the second motor used for ganged axes.<br><br>NOTE: This inversion will be applied in addition to the inversion from setting $3.</td>
     <td></td>
   </tr>
   <tr>
     <td><b>$9</b></td>
     <td>PWM Spindle</td>
     <td>Enable: <b>ON</b><br>RPM controls spindle en signal: <b>OFF</b><br>(1)</td>
     <td></td>
     <td style="text-align: left;">Enable: Controls PWM output availability.<br>RPM controls spindle enable signal: When M3 or M4 is active,  S &gt; 0 turns on spindle enable and S0 turns it off.</td>
     <td></td>
   </tr>
   <tr>
     <td><b>$10</b></td>
     <td>Status report options</td>
     <td>Position in machine coords: <b>ON</b><br>Buffer state: <b>ON</b><br>Line numbers: <b>ON</b><br>Feed & speed: <b>ON</b><br>Pin state: <b>ON</b><br>Work coord offset: <b>ON</b><br>Overrides: <b>ON</b><br>Probe coords: <b>ON</b><br>Buffer sync on WCO change: <b>ON</b><br>Parser state: <b>OFF</b><br>Alarm substatus: <b>OFF</b><br>Run substatus: <b>OFF</b><br>(511)</td>
     <td></td>
     <td style="text-align: left;">Specifies optional data included in status reports. If Run substatus is enabled it may be used for simple probe protection.<br><br>NOTE: Parser state will be sent separately after the status report and only on changes.</td>
     <td></td>
   </tr>
   <tr>
     <td><b>$11</b></td>
     <td>Junction deviation</td>
     <td><b>0.010</b></td>
     <td>mm</td>
     <td style="text-align: left;">Sets how fast Grbl travels through consecutive motions. Lower value slows it down.</td>
     <td></td>
   </tr>
   <tr>
     <td><b>$12</b></td>
     <td>Arc tolerance</td>
     <td><b>0.002</b></td>
     <td>mm</td>
     <td style="text-align: left;">Sets the G2 and G3 arc tracing accuracy based on radial error. Beware: A very small value may effect performance.</td>
     <td></td>
   </tr>
   <tr>
     <td><b>$13</b></td>
     <td>Report in inches</td>
     <td><b>Disabled</b> (0)</td>
     <td></td>
     <td style="text-align: left;">Enables inch units when returning any position and rate value that is not a settings value.</td>
     <td></td>
   </tr>
   <tr>
     <td><b>$14</b></td>
     <td>Invert control pins</td>
     <td>Reset: <b>OFF</b><br>Feed hold: <b>ON</b><br>Cycle start: <b>ON</b><br>Safety door: <b>ON</b><br>EStop: <b>OFF</b><br>(14)</td>
     <td></td>
     <td style="text-align: left;">Inverts the control signals (active low).<br><br>NOTE: Block delete, Optional stop, EStop and Probe connected are optional signals, availability is driver dependent.</td>
     <td></td>
   </tr>
   <tr>
     <td><b>$15</b></td>
     <td>Invert coolant pins</td>
     <td>Flood: <b>OFF</b><br>Mist: <b>OFF</b><br>(0)</td>
     <td></td>
     <td style="text-align: left;">Inverts the coolant and mist signals (active low).</td>
     <td></td>
   </tr>
   <tr>
     <td><b>$16</b></td>
     <td>Invert spindle signals</td>
     <td>Spindle en: <b>OFF</b><br>Spindle dir: <b>OFF</b><br>PWM: <b>OFF</b><br>(0)</td>
     <td></td>
     <td style="text-align: left;">Inverts the spindle on, counterclockwise and PWM signals (active low).<br><br>NOTE: A hard reset of the controller is required after changing this setting.</td>
     <td></td>
   </tr>
   <tr>
     <td><b>$17</b></td>
     <td>Pullup disable control pins</td>
     <td>Reset: <b>OFF</b><br>Feed hold: <b>OFF</b><br>Cycle start: <b>OFF</b><br>Safety door: <b>OFF</b><br>EStop: <b>OFF</b><br>(0)</td>
     <td></td>
     <td style="text-align: left;">Disable the control signals pullup resistors. Potentially enables pulldown resistor if available.<br><br>NOTE: Block delete, Optional stop and EStop are optional signals, availability is driver dependent.</td>
     <td></td>
   </tr>
   <tr>
     <td><b>$18</b></td>
     <td>Pullup disable limit pins</td>
     <td>X: <b>OFF</b><br>Y: <b>OFF</b><br>Z: <b>OFF</b><br>A: <b>OFF</b><br>(0)</td>
     <td></td>
     <td style="text-align: left;">Disable the limit signals pullup resistors. Potentially enables pulldown resistor if available.</td>
     <td></td>
   </tr>
   <tr>
     <td><b>$19</b></td>
     <td>Pullup disable probe pin</td>
     <td><b>Disabled</b> (0)</td>
     <td></td>
     <td style="text-align: left;">Disable the probe signal pullup resistor. Potentially enables pulldown resistor if available.</td>
     <td></td>
   </tr>
   <tr>
     <td><b>$20</b></td>
     <td>Soft limits enable</td>
     <td><b>Disabled</b> (0)</td>
     <td></td>
     <td style="text-align: left;">Enables soft limits checks within machine travel and sets alarm when exceeded. Requires homing.</td>
     <td rowspan="8"><a href="https://resources.sienci.com/view/slb-manual/#homing-amp-limit-switches">Docs</a></td>
   </tr>
   <tr>
     <td><b>$21</b></td>
     <td>Hard limits enable</td>
     <td>Enable: <b>OFF</b><br>Strict mode: <b>OFF</b><br>(0)</td>
     <td></td>
     <td style="text-align: left;">When enabled immediately halts motion and throws an alarm when a limit switch is triggered. In strict mode only homing is possible when a switch is engaged.</td>
   </tr>
   <tr>
     <td><b>$22</b></td>
     <td>Homing cycle</td>
     <td>Enable: <b>OFF</b><br>Single axis commands: <b>OFF</b><br>Homing on startup: <b>OFF</b><br>Set machine origin: <b>OFF</b><br>Two switches share one input: <b>OFF</b><br>Allow manual: <b>OFF</b><br>Override locks: <b>OFF</b><br>Keep homed status on reset: <b>OFF</b><br>(0)</td>
     <td></td>
     <td style="text-align: left;">Enables homing cycle. Requires limit switches on axes to be automatically homed.<br><br>When `Enable single axis commands` is checked, single axis homing can be performed by $H&lt;axis letter&gt; commands.<br><br>When `Allow manual` is checked, axes not homed automatically may be homed manually by $H or $H&lt;axis letter&gt; commands.<br><br>`Override locks` is for allowing a soft reset to disable `Homing on startup required`.</td>
   </tr>
   <tr>
     <td><b>$23</b></td>
     <td>Homing direction invert</td>
     <td>X: <b>ON</b><br>Y: <b>ON</b><br>Z: <b>OFF</b><br>A: <b>ON</b><br>(11)</td>
     <td></td>
     <td style="text-align: left;">Homing searches for a switch in the positive direction. Set axis bit to search in negative direction.</td>
   </tr>
   <tr>
     <td><b>$24</b></td>
     <td>Homing locate feed rate</td>
     <td><b>150</b></td>
     <td>mm/min</td>
     <td style="text-align: left;">Feed rate to slowly engage limit switch to determine its location accurately.</td>
   </tr>
   <tr>
     <td><b>$25</b></td>
     <td>Homing search seek rate</td>
     <td><b>4300</b></td>
     <td>mm/min</td>
     <td style="text-align: left;">Seek rate to quickly find the limit switch before the slower locating phase.</td>
   </tr>
   <tr>
     <td><b>$26</b></td>
     <td>Homing switch debounce delay</td>
     <td><b>25</b></td>
     <td>milliseconds</td>
     <td style="text-align: left;">Sets a short delay between phases of homing cycle to let a switch debounce.</td>
   </tr>
   <tr>
     <td><b>$27</b></td>
     <td>Homing switch pull-off distance</td>
     <td><b>1.5</b></td>
     <td>mm</td>
     <td style="text-align: left;">Retract distance after triggering switch to disengage it. Homing will fail if switch isn't cleared.</td>
   </tr>
   <tr>
     <td><b>$28</b></td>
     <td>G73 retract distance</td>
     <td><b>0.1</b></td>
     <td>mm</td>
     <td style="text-align: left;">G73 retract distance (for chip breaking drilling).</td>
     <td></td>
   </tr>
   <tr>
     <td><b>$29</b></td>
     <td>Pulse delay</td>
     <td><b>0</b></td>
     <td>microseconds</td>
     <td style="text-align: left;">Step pulse delay.<br><br>Normally leave this at 0 as there is an implicit delay on direction changes when AMASS is active.</td>
     <td></td>
   </tr>
   <tr>
     <td><b>$30</b></td>
     <td>Maximum spindle speed</td>
     <td><b>24000</b></td>
     <td>RPM</td>
     <td style="text-align: left;">Maximum spindle speed, can be overridden by spindle plugins.</td>
     <td rowspan="7"><a href="https://resources.sienci.com/view/slb-manual/#spindlers485">Docs</a></td>
   </tr>
   <tr>
     <td><b>$31</b></td>
     <td>Minimum spindle speed</td>
     <td><b>7500</b></td>
     <td>RPM</td>
     <td style="text-align: left;">Minimum spindle speed, can be overridden by spindle plugins.</td>
   </tr>
   <tr>
     <td><b>$32</b></td>
     <td>Mode of operation</td>
     <td><b>Normal</b><br>(0)</td>
     <td></td>
     <td style="text-align: left;">Laser mode: consecutive G1/2/3 commands will not halt when spindle speed is changed.<br><br>Lathe mode: allows use of G7, G8, G96 and G97.</td>
   </tr>
   <tr>
     <td><b>$33</b></td>
     <td>Spindle PWM frequency</td>
     <td><b>1000</b></td>
     <td>Hz</td>
     <td style="text-align: left;">Spindle PWM frequency.</td>
   </tr>
   <tr>
     <td><b>$34</b></td>
     <td>Spindle PWM off value</td>
     <td><b>0</b></td>
     <td>percent</td>
     <td style="text-align: left;">Spindle PWM off value in percent (duty cycle).</td>
   </tr>
   <tr>
     <td><b>$35</b></td>
     <td>Spindle PWM min value</td>
     <td><b>0</b></td>
     <td>percent</td>
     <td style="text-align: left;">Spindle PWM min value in percent (duty cycle).</td>
   </tr>
   <tr>
     <td><b>$36</b></td>
     <td>Spindle PWM max value</td>
     <td><b>100</b></td>
     <td>percent</td>
     <td style="text-align: left;">Spindle PWM max value in percent (duty cycle).</td>
   </tr>
   <tr>
     <td><b>$37</b></td>
     <td>Steppers de-energize</td>
     <td>X: <b>OFF</b><br>Y: <b>OFF</b><br>Z: <b>OFF</b><br>A: <b>OFF</b><br>(0)</td>
     <td></td>
     <td style="text-align: left;">Specifies which steppers not to disable when stopped.</td>
     <td><a href="https://resources.sienci.com/view/slb-manual/#independent-motor-holding">Docs</a></td>
   </tr>
   <tr>
     <td><b>$39</b></td>
     <td>Enable legacy RT commands</td>
     <td><b>Enabled</b> (1)</td>
     <td></td>
     <td style="text-align: left;">Enables "normal" processing of ?, ! and ~ characters when part of $-setting or comment. If disabled then they are added to the input string instead.</td>
     <td></td>
   </tr>
   <tr>
     <td><b>$40</b></td>
     <td>Limit jog commands</td>
     <td><b>Enabled</b> (1)</td>
     <td></td>
     <td style="text-align: left;">Limit jog commands to machine limits for homed axes.</td>
     <td><a href="https://resources.sienci.com/view/slb-manual/#homing-amp-limit-switches">Docs</a></td>
   </tr>
   <tr style="color: var(--sl-orange);">
     <td><b>$41</b></td>
     <td>Parking cycle</td>
     <td>Enable: <b>ON</b><br>Parking override control: <b>OFF</b><br>Deactivate upon init: <b>OFF</b><br>(1)</td>
     <td></td>
     <td style="text-align: left;">Enables parking cycle, requires parking axis homed.</td>
     <td></td>
   </tr>
   <tr style="color: var(--sl-orange);">
     <td><b>$42</b></td>
     <td>Parking axis</td>
     <td><b>Z</b><br>(2)</td>
     <td></td>
     <td style="text-align: left;">Define which axis that performs the parking motion.</td>
     <td></td>
   </tr>
   <tr>
     <td><b>$43</b></td>
     <td>Homing passes</td>
     <td><b>1</b></td>
     <td></td>
     <td style="text-align: left;">Number of homing passes. Minimum 1, maximum 128.</td>
     <td></td>
   </tr>
   <tr>
     <td><b>$44</b></td>
     <td>Axes homing, first pass</td>
     <td>X: <b>OFF</b><br>Y: <b>OFF</b><br>Z: <b>ON</b><br>A: <b>OFF</b><br>(4)</td>
     <td></td>
     <td style="text-align: left;">Axes to home in first pass.</td>
     <td></td>
   </tr>
   <tr>
     <td><b>$45</b></td>
     <td>Axes homing, second pass</td>
     <td>X: <b>ON</b><br>Y: <b>ON</b><br>Z: <b>OFF</b><br>A: <b>OFF</b><br>(3)</td>
     <td></td>
     <td style="text-align: left;">Axes to home in second pass.</td>
     <td></td>
   </tr>
   <tr>
     <td><b>$46</b></td>
     <td>Axes homing, third pass</td>
     <td>X: <b>OFF</b><br>Y: <b>OFF</b><br>Z: <b>OFF</b><br>A: <b>OFF</b><br>(0)</td>
     <td></td>
     <td style="text-align: left;">Axes to home in third pass.</td>
     <td></td>
   </tr>
   <tr>
     <td><b>$47</b></td>
     <td>Axes homing, fourth pass</td>
     <td>X: <b>OFF</b><br>Y: <b>OFF</b><br>Z: <b>OFF</b><br>A: <b>OFF</b><br>(0)</td>
     <td></td>
     <td style="text-align: left;">Axes to home in fourth pass.</td>
     <td></td>
   </tr>
   <tr style="color: var(--sl-orange);">
     <td><b>$56</b></td>
     <td>Parking pull-out distance</td>
     <td><b>5</b></td>
     <td>mm</td>
     <td style="text-align: left;">Spindle pull-out and plunge distance in mm.Incremental distance.</td>
     <td></td>
   </tr>
   <tr style="color: var(--sl-orange);">
     <td><b>$57</b></td>
     <td>Parking pull-out rate</td>
     <td><b>100</b></td>
     <td>mm/min</td>
     <td style="text-align: left;">Spindle pull-out/plunge slow feed rate in mm/min.</td>
     <td></td>
   </tr>
   <tr style="color: var(--sl-orange);">
     <td><b>$58</b></td>
     <td>Parking target</td>
     <td><b>-5</b></td>
     <td>mm</td>
     <td style="text-align: left;">Parking axis target. In mm, as machine coordinate [-max_travel, 0].</td>
     <td></td>
   </tr>
   <tr style="color: var(--sl-orange);">
     <td><b>$59</b></td>
     <td>Parking fast rate</td>
     <td><b>500</b></td>
     <td>mm/min</td>
     <td style="text-align: left;">Parking fast rate to target after pull-out in mm/min.</td>
     <td></td>
   </tr>
   <tr>
     <td><b>$60</b></td>
     <td>Restore overrides</td>
     <td><b>Enabled</b> (1)</td>
     <td></td>
     <td style="text-align: left;">Restore overrides to default values at program end.</td>
     <td></td>
   </tr>
   <tr style="color: var(--sl-orange);">
     <td><b>$61</b></td>
     <td>Safety door options</td>
     <td>Ignore when idle: <b>ON</b><br>Keep coolant state: <b>ON</b><br>(3)</td>
     <td></td>
     <td style="text-align: left;">Enable this if it is desirable to open the safety door when in IDLE mode (eg. for jogging).</td>
     <td></td>
   </tr>
   <tr>
     <td><b>$62</b></td>
     <td>Sleep enable</td>
     <td><b>Disabled</b> (0)</td>
     <td></td>
     <td style="text-align: left;">Enable sleep mode.</td>
     <td></td>
   </tr>
   <tr>
     <td><b>$63</b></td>
     <td>Feed hold actions</td>
     <td>Disable laser: <b>ON</b><br>Restore spindle and coolant state: <b>ON</b><br>(3)</td>
     <td></td>
     <td style="text-align: left;">Actions taken during feed hold and on resume from feed hold.</td>
     <td></td>
   </tr>
   <tr>
     <td><b>$64</b></td>
     <td>Force init alarm</td>
     <td><b>Disabled</b> (0)</td>
     <td></td>
     <td style="text-align: left;">Starts Grbl in alarm mode after a cold reset.</td>
     <td></td>
   </tr>
   <tr>
     <td><b>$65</b></td>
     <td>Probing feed override</td>
     <td><b>Disabled</b> (0)</td>
     <td></td>
     <td style="text-align: left;">Allow feed override during probing.</td>
     <td></td>
   </tr>
   <tr>
     <td><b>$70</b></td>
     <td>Network services</td>
     <td>Telnet: <b>ON</b><br>Websocket: <b>ON</b><br>FTP: <b>ON</b><br>(11)</td>
     <td></td>
     <td style="text-align: left;">Network services/protocols to enable.<br><br>NOTE: A hard reset of the controller is required after changing this setting.</td>
     <td><a href="https://resources.sienci.com/view/slb-manual/#ethernet-on-windows">Docs</a></td>
   </tr>
   <tr>
     <td><b>$100</b></td>
     <td>X-axis travel resolution</td>
     <td><b>800</b></td>
     <td>step/mm</td>
     <td style="text-align: left;" rowspan="4">Travel resolution in steps per millimeter.</td>
     <td></td>
   </tr>
   <tr>
     <td><b>$101</b></td>
     <td>Y-axis travel resolution</td>
     <td><b>800</b></td>
     <td>step/mm</td>
     <td></td>
   </tr>
   <tr>
     <td><b>$102</b></td>
     <td>Z-axis travel resolution</td>
     <td><b>800</b></td>
     <td>step/mm</td>
     <td></td>
   </tr>
   <tr>
     <td><b>$103</b></td>
     <td>A-axis travel resolution</td>
     <td><b>79.01234568</b></td>
     <td>step/deg</td>
     <td></td>
   </tr>
   <tr>
     <td><b>$110</b></td>
     <td>X-axis maximum rate</td>
     <td><b>5500</b></td>
     <td>mm/min</td>
     <td style="text-align: left;" rowspan="4">Maximum rate. Used as G0 rapid rate.</td>
     <td rowspan="8"><a href="https://resources.sienci.com/view/slb-manual/#movement-amp-cutting-speeds">Docs</a></td>
   </tr>
   <tr>
     <td><b>$111</b></td>
     <td>Y-axis maximum rate</td>
     <td><b>5500</b></td>
     <td>mm/min</td>
   </tr>
   <tr>
     <td><b>$112</b></td>
     <td>Z-axis maximum rate</td>
     <td><b>4500</b></td>
     <td>mm/min</td>
   </tr>
   <tr>
     <td><b>$113</b></td>
     <td>A-axis maximum rate</td>
     <td><b>8000</b></td>
     <td>deg/min</td>
   </tr>
   <tr>
     <td><b>$120</b></td>
     <td>X-axis acceleration</td>
     <td><b>1000</b></td>
     <td>mm/sec^2</td>
     <td style="text-align: left;" rowspan="4">Acceleration. Used for motion planning to not exceed motor torque and lose steps.</td>
   </tr>
   <tr>
     <td><b>$121</b></td>
     <td>Y-axis acceleration</td>
     <td><b>1000</b></td>
     <td>mm/sec^2</td>
   <tr>
     <td><b>$122</b></td>
     <td>Z-axis acceleration</td>
     <td><b>750</b></td>
     <td>mm/sec^2</td>
   <tr>
     <td><b>$123</b></td>
     <td>A-axis acceleration</td>
     <td><b>1000</b></td>
     <td>deg/sec^2</td>
   <tr>
     <td><b>$130</b></td>
     <td>X-axis maximum travel</td>
     <td><b>810</b></td>
     <td>mm</td>
     <td style="text-align: left;" rowspan="4">Maximum axis travel distance from homing switch. Determines valid machine space for soft-limits and homing search distances.</td>
     <td></td>
   </tr>
   <tr>
     <td><b>$131</b></td>
     <td>Y-axis maximum travel</td>
     <td><b>855</b></td>
     <td>mm</td>
     <td></td>
   </tr>
   <tr>
     <td><b>$132</b></td>
     <td>Z-axis maximum travel</td>
     <td><b>120</b></td>
     <td>mm</td>
     <td></td>
   </tr>
   <tr>
     <td><b>$133</b></td>
     <td>A-axis maximum travel</td>
     <td><b>0</b></td>
     <td>deg</td>
     <td></td>
   </tr>
   <tr>
     <td><b>$140</b></td>
     <td>X-axis motor current</td>
     <td rowspan="3"><b>2800</b></td>
     <td rowspan="4">mA</td>
     <td style="text-align: left;" rowspan="4">Motor current in mA (RMS).<br><br>NOTE: Only used for axes controlled by a Trinamic driver.</td>
     <td rowspan="4"></td>
   </tr>
   <tr>
     <td><b>$141</b></td>
     <td>Y-axis motor current</td>
   </tr>
   <tr>
     <td><b>$142</b></td>
     <td>Z-axis motor current</td>
   </tr>
   <tr style="color: var(--sl-orange);">
     <td><b>$143</b></td>
     <td>A-axis motor current</td>
     <td><b>0</b></td>
   </tr>
   <tr>
     <td><b>$150</b></td>
     <td>X-axis microsteps</td>
     <td rowspan="3"><b>32</b></td>
     <td rowspan="4">steps</td>
     <td style="text-align: left;" rowspan="4">Microsteps per fullstep.<br><br>NOTE: Only used for axes controlled by a Trinamic driver.</td>
     <td rowspan="4"></td>
   </tr>
   <tr>
     <td><b>$151</b></td>
     <td>Y-axis microsteps</td>
   </tr>
   <tr>
     <td><b>$152</b></td>
     <td>Z-axis microsteps</td>
   </tr>
   <tr style="color: var(--sl-orange);">
     <td><b>$153</b></td>
     <td>A-axis microsteps</td>
     <td><b>16</b></td>
   </tr>
   <tr>
     <td><b>$180</b></td>
     <td>X-axis homing locate feed rate</td>
     <td rowspan="4"><b>150</b></td>
     <td rowspan="4">mm/min</td>
     <td style="text-align: left;" rowspan="4">Feed rate to slowly engage limit switch to determine its location accurately.<br><br>NOTE: Defaults to $24 setting if axis isn't controlled by a Trinamic driver.</td>
     <td rowspan="4"><a href="https://resources.sienci.com/view/slb-manual/#homing-amp-limit-switches">Docs</a></td>
   </tr>
   <tr>
     <td><b>$181</b></td>
     <td>Y-axis homing locate feed rate</td>
   </tr>
   <tr>
     <td><b>$182</b></td>
     <td>Z-axis homing locate feed rate</td>
   </tr>
   <tr style="color: var(--sl-orange);">
     <td><b>$183</b></td>
     <td>A-axis homing locate feed rate</td>
   </tr>
   <tr>
     <td><b>$190</b></td>
     <td>X-axis homing search seek rate</td>
     <td rowspan="4"><b>4300</b></td>
     <td rowspan="4">mm/min</td>
     <td style="text-align: left;" rowspan="4">Seek rate to quickly find the limit switch before the slower locating phase.<br><br>NOTE: Defaults to $25 setting if axis isn't controlled by a Trinamic driver.</td>
     <td rowspan="4"><a href="https://resources.sienci.com/view/slb-manual/#homing-amp-limit-switches">Docs</a></td>
   </tr>
   <tr>
     <td><b>$191</b></td>
     <td>Y-axis homing search seek rate</td>
   </tr>
   <tr>
     <td><b>$192</b></td>
     <td>Z-axis homing search seek rate</td>
   </tr>
   <tr style="color: var(--sl-orange);">
     <td><b>$193</b></td>
     <td>A-axis homing search seek rate</td>
   </tr>
   <tr style="color: var(--sl-blue-d);">
     <td><b>$200</b></td>
     <td>X-axis StallGuard2 fast threshold</td>
     <td rowspan="4"><b>22</b></td>
     <td rowspan="4"></td>
     <td style="text-align: left;" rowspan="4">StallGuard threshold for fast (seek) homing phase.<br><br>NOTE: Only used for axes controlled by a Trinamic driver.</td>
     <td rowspan="4"></td>
   </tr>
   <tr style="color: var(--sl-blue-d);">
     <td><b>$201</b></td>
     <td>Y-axis StallGuard2 fast threshold</td>
   </tr>
   <tr style="color: var(--sl-blue-d);">
     <td><b>$202</b></td>
     <td>Z-axis StallGuard2 fast threshold</td>
   </tr>
   <tr style="color: var(--sl-orange);">
     <td><b>$203</b></td>
     <td>A-axis StallGuard2 fast threshold</td>
   </tr>
   <tr>
     <td><b>$210</b></td>
     <td>X-axis hold current</td>
     <td rowspan="3"><b>35</b></td>
     <td rowspan="4">%</td>
     <td style="text-align: left;" rowspan="4">Motor current at standstill as a percentage of full current.<br><br>NOTE: If grblHAL is configured to disable motors on standstill this setting has no use. Only used for axes controlled by a Trinamic driver.</td>
     <td rowspan="4"><a href="https://resources.sienci.com/view/slb-manual/#independent-motor-holding">Docs</a></td>
   </tr>
   <tr>
     <td><b>$211</b></td>
     <td>Y-axis hold current</td>
   </tr>
   <tr>
     <td><b>$212</b></td>
     <td>Z-axis hold current</td>
   </tr>
   <tr style="color: var(--sl-orange);">
     <td><b>$213</b></td>
     <td>A-axis hold current</td>
     <td><b>50</b></td>
   </tr>
   <tr style="color: var(--sl-blue-d);">
     <td><b>$220</b></td>
     <td>X-axis stallGuard2 slow threshold</td>
     <td rowspan="4"><b>22</b></td>
     <td rowspan="4"></td>
     <td style="text-align: left;" rowspan="4">StallGuard threshold for slow (feed) homing phase.<br><br>NOTE: Only used for axes controlled by a Trinamic driver.</td>
     <td rowspan="4"></td>
   </tr>
   <tr style="color: var(--sl-blue-d);">
     <td><b>$221</b></td>
     <td>Y-axis stallGuard2 slow threshold</td>
   </tr>
   <tr style="color: var(--sl-blue-d);">
     <td><b>$222</b></td>
     <td>Z-axis stallGuard2 slow threshold</td>
   </tr>
   <tr style="color: var(--sl-orange);">
     <td><b>$223</b></td>
     <td>A-axis stallGuard2 slow threshold</td>
   </tr>
   <tr>
     <td><b>$300</b></td>
     <td>Hostname</td>
     <td><b>grblHAL</b></td>
     <td></td>
     <td style="text-align: left;">Network hostname.<br>~Controller reset required for setting change to take effect~</td>
     <td rowspan="8"><a href="https://resources.sienci.com/view/slb-manual/#ethernet-on-windows">Docs</a></td>
   </tr>
   <tr>
     <td><b>$301</b></td>
     <td>IP mode</td>
     <td><b>Static</b><br>(0)</td>
     <td></td>
     <td style="text-align: left;">IP mode.<br>~Controller reset required for setting change to take effect~</td>
   </tr>
   <tr>
     <td><b>$302</b></td>
     <td>IP address</td>
     <td><b>192.168.5.1</b></td>
     <td></td>
     <td style="text-align: left;">Static IP address.<br>~Controller reset required for setting change to take effect~</td>
   </tr>
   <tr>
     <td><b>$303</b></td>
     <td>Gateway</td>
     <td><b>192.168.5.1</b></td>
     <td></td>
     <td style="text-align: left;">Static gateway address.<br>~Controller reset required for setting change to take effect~</td>
   </tr>
   <tr>
     <td><b>$304</b></td>
     <td>Netmask</td>
     <td><b>255.255.255.0</b></td>
     <td></td>
     <td style="text-align: left;">Static netmask.<br>~Controller reset required for setting change to take effect~</td>
   </tr>
   <tr>
     <td><b>$305</b></td>
     <td>Telnet port</td>
     <td><b>23</b></td>
     <td></td>
     <td style="text-align: left;">(Raw) Telnet port number listening for incoming connections.<br>~Controller reset required for setting change to take effect~</td>
   </tr>
   <tr>
     <td><b>$307</b></td>
     <td>Websocket port</td>
     <td><b>80</b></td>
     <td></td>
     <td style="text-align: left;">Websocket port number listening for incoming connections.<br>NOTE: WebUI requires this to be HTTP port number + 1.<br>~Controller reset required for setting change to take effect~</td>
   </tr>
   <tr>
     <td><b>$308</b></td>
     <td>FTP port</td>
     <td><b>21</b></td>
     <td></td>
     <td style="text-align: left;">FTP port number listening for incoming connections.<br>~Controller reset required for setting change to take effect~</td>
   </tr>
   <tr style="color: var(--sl-blue-d);">
     <td><b>$338</b></td>
     <td>Trinamic driver</td>
     <td>X: <b>ON</b><br>Y: <b>ON</b><br>Z: <b>ON</b><br>A: <b>OFF</b><br>(7)</td>
     <td></td>
     <td style="text-align: left;">Enable SPI or UART controlled Trinamic drivers for axes.</td>
     <td></td>
   </tr>
   <tr style="color: var(--sl-blue-d);">
     <td><b>$339</b></td>
     <td>Sensorless homing</td>
     <td>X: <b>OFF</b><br>Y: <b>OFF</b><br>Z: <b>OFF</b><br>A: <b>OFF</b><br>(0)</td>
     <td></td>
     <td style="text-align: left;">Enable sensorless homing for axes. Requires SPI or UART controlled Trinamic drivers.</td>
     <td></td>
   </tr>
   <tr>
     <td><b>$340</b></td>
     <td>Spindle at speed tolerance</td>
     <td><b>0</b></td>
     <td>percent</td>
     <td style="text-align: left;">Spindle at speed tolerance as percentage deviation from programmed speed, set to 0 to disable.<br><br>If not within tolerance when checked after spindle on delay ($392) alarm 14 is raised.</td>
     <td></td>
   </tr>
   <tr style="color: var(--sl-blue-d);">
     <td><b>$341</b></td>
     <td>Tool change mode</td>
     <td><b>Normal</b><br>(0)</td>
     <td></td>
     <td style="text-align: left;">Normal: allows jogging for manual touch off. Set new position manually.<br><br>Manual touch off: retracts tool axis to home position for tool change, use jogging or $TPW for touch off.<br><br>Manual touch off @ G59.3: retracts tool axis to home position then to G59.3 position for tool change, use jogging or $TPW for touch off.<br><br>Automatic touch off @ G59.3: retracts tool axis to home position for tool change, then to G59.3 position for automatic touch off.<br><br>All modes except "Normal" and "Ignore M6" returns the tool (controlled point) to original position after touch off.</td>
     <td></td>
   </tr>
   <tr style="color: var(--sl-blue-d);">
     <td><b>$342</b></td>
     <td>Tool change probing distance</td>
     <td><b>30</b></td>
     <td>mm</td>
     <td style="text-align: left;">Maximum probing distance for automatic or $TPW touch off.</td>
     <td></td>
   </tr>
   <tr style="color: var(--sl-blue-d);">
     <td><b>$343</b></td>
     <td>Tool change locate feed rate</td>
     <td><b>25</b></td>
     <td>mm/min</td>
     <td style="text-align: left;">Feed rate to slowly engage tool change sensor to determine the tool offset accurately.</td>
     <td></td>
   </tr>
   <tr style="color: var(--sl-blue-d);">
     <td><b>$344</b></td>
     <td>Tool change search seek rate</td>
     <td><b>200</b></td>
     <td>mm/min</td>
     <td style="text-align: left;">Seek rate to quickly find the tool change sensor before the slower locating phase.</td>
     <td></td>
   </tr>
   <tr style="color: var(--sl-blue-d);">
     <td><b>$345</b></td>
     <td>Tool change probe pull-off rate</td>
     <td><b>200</b></td>
     <td>mm/min</td>
     <td style="text-align: left;">Pull-off rate for the retract move before the slower locating phase.</td>
     <td></td>
   </tr>
   <tr style="color: var(--sl-blue-d);">
     <td><b>$346</b></td>
     <td>Restore position after M6</td>
     <td><b>Enabled</b> (1)</td>
     <td></td>
     <td style="text-align: left;">When set the spindle is moved so that the controlled point (tool tip) is the same as before the M6 command, if not the spindle is only moved to the Z home position.</td>
     <td></td>
   </tr>
   <tr>
     <td><b>$370</b></td>
     <td>Invert I/O Port inputs</td>
     <td>(0)</td>
     <td></td>
     <td style="text-align: left;">Invert IOPort inputs.</td>
     <td></td>
   </tr>
   <tr>
     <td><b>$372</b></td>
     <td>Invert I/O Port outputs</td>
     <td>(0)</td>
     <td></td>
     <td style="text-align: left;">Invert IOPort output.</td>
     <td></td>
   </tr>
   <tr>
     <td><b>$374</b></td>
     <td>Modbus baud rate</td>
     <td><b>19200</b><br>(3)</td>
     <td></td>
     <td style="text-align: left;"></td>
     <td></td>
   </tr>
   <tr>
     <td><b>$375</b></td>
     <td>Modbus RX timeout</td>
     <td><b>50</b></td>
     <td>milliseconds</td>
     <td style="text-align: left;"></td>
     <td></td>
   </tr>
   <tr>
     <td><b>$376</b></td>
     <td>Rotational axes</td>
     <td>A-Axis: <b>ON</b><br>(1)</td>
     <td></td>
     <td style="text-align: left;"></td>
     <td></td>
   </tr>
   <tr>
     <td><b>$384</b></td>
     <td>Disable G92 persistence</td>
     <td><b>Disabled</b> (0)</td>
     <td></td>
     <td style="text-align: left;">Disables save/restore of G92 offset to non-volatile storage (NVS).</td>
     <td></td>
   </tr>
   <tr style="color: var(--sl-orange);">
     <td><b>$392</b></td>
     <td>Spindle on delay</td>
     <td><b>4</b></td>
     <td>s</td>
     <td style="text-align: left;">Delay to allow spindle to spin up after safety door is opened.</td>
     <td></td>
   </tr>
   <tr style="color: var(--sl-orange);">
     <td><b>$393</b></td>
     <td>Coolant on delay</td>
     <td><b>1</b></td>
     <td>s</td>
     <td style="text-align: left;">Delay to allow coolant to restart after safety door is opened.</td>
     <td></td>
   </tr>
   <tr>
     <td><b>$395</b></td>
     <td>Default spindle</td>
     <td><b>SLB_SPINDLE</b><br>(0)</td>
     <td></td>
     <td style="text-align: left;">Spindle selected on startup.</td>
     <td></td>
   </tr>
   <tr style="color: var(--sl-blue-d);">
     <td><b>$398</b></td>
     <td>Planner buffer blocks</td>
     <td><b>128</b></td>
     <td></td>
     <td style="text-align: left;">Number of blocks in the planner buffer.<br>~Controller reset required for setting change to take effect~</td>
     <td></td>
   </tr>
   <tr>
     <td><b>$450</b></td>
     <td>Button 1 action</td>
     <td><b>Cycle start</b><br>(1)</td>
     <td></td>
     <td style="text-align: left;">Assign a real-time action to button 1, or run your own macro g-code.</td>
     <td rowspan="6"><a href="https://resources.sienci.com/view/slb-manual/#action-buttons">Docs</a></td>
   </tr>
   <tr>
     <td><b>$451</b></td>
     <td>Button 2 action</td>
     <td><b>Pause</b><br>(2)</td>
     <td></td>
     <td style="text-align: left;">Assign a real-time action to button 2, or run your own macro g-code.</td>
   </tr>
   <tr>
     <td><b>$452</b></td>
     <td>Button 3 action</td>
     <td><b>Halt</b><br>(4)</td>
     <td></td>
     <td style="text-align: left;">Assign a real-time action to button 3, or run your own macro g-code.</td>
   </tr>
   <tr>
     <td><b>$453</b></td>
     <td>Button 1 macro</td>
     <td><b>G4P0</b></td>
     <td></td>
     <td style="text-align: left;">Macro content, limited to 127 characters. Separate lines with the vertical bar character |.</td>
   </tr>
   <tr>
     <td><b>$454</b></td>
     <td>Button 2 macro</td>
     <td><b>G4P0</b></td>
     <td></td>
     <td style="text-align: left;">Macro content, limited to 127 characters. Separate lines with the vertical bar character |.</td>
   </tr>
   <tr>
     <td><b>$455</b></td>
     <td>Button 3 macro</td>
     <td><b>G4P0</b></td>
     <td></td>
     <td style="text-align: left;">Macro content, limited to 127 characters. Separate lines with the vertical bar character |.</td>
   </tr>
   <tr>
     <td><b>$456</b></td>
     <td>Aux output 0 trigger</td>
     <td><b>Spindle/Laser enable</b><br>(0)</td>
     <td></td>
     <td style="text-align: left;">A second, more common action can be assigned to trigger this output. M62/63 P# is always available as a buffered on/off or M64/65 P# as an immediate on/off.</td>
     <td rowspan="4"><a href="https://resources.sienci.com/view/slb-manual/#switch-amp-aux-power">Docs</a></td>
   </tr>
   <tr>
     <td><b>$457</b></td>
     <td>Aux output 1 trigger</td>
     <td><b>Flood enable</b><br>(2)</td>
     <td></td>
     <td style="text-align: left;">A second, more common action can be assigned to trigger this output. M62/63 P# is always available as a buffered on/off or M64/65 P# as an immediate on/off.</td>
   </tr>
   <tr>
     <td><b>$458</b></td>
     <td>Aux output 2 trigger</td>
     <td><b>Spindle/Laser enable</b><br>(0)</td>
     <td></td>
     <td style="text-align: left;">A second, more common action can be assigned to trigger this output. M62/63 P# is always available as a buffered on/off or M64/65 P# as an immediate on/off.</td>
   </tr>
   <tr>
     <td><b>$459</b></td>
     <td>Aux output 3 trigger</td>
     <td><b>Flood enable</b><br>(2)</td>
     <td></td>
     <td style="text-align: left;">A second, more common action can be assigned to trigger this output. M62/63 P# is always available as a buffered on/off or M64/65 P# as an immediate on/off.</td>
   </tr>
   <tr>
     <td><b>$462</b></td>
     <td>Run/stop register</td>
     <td><b>8192</b></td>
     <td>decimal</td>
     <td style="text-align: left;">MODVFD register for run/stop.</td>
     <td rowspan="12"><a href="https://resources.sienci.com/view/slb-manual/#spindlers485">Docs</a></td>
   </tr>
   <tr>
     <td><b>$463</b></td>
     <td>Frequency set register</td>
     <td><b>8193</b></td>
     <td>decimal</td>
     <td style="text-align: left;">MODVFD register to set frequency.</td>
   </tr>
   <tr>
     <td><b>$464</b></td>
     <td>Frequency get register</td>
     <td><b>8451</b></td>
     <td>decimal</td>
     <td style="text-align: left;">MODVFD register to get frequency.</td>
   </tr>
   <tr>
     <td><b>$465</b></td>
     <td>Run CW command</td>
     <td><b>18</b></td>
     <td>decimal</td>
     <td style="text-align: left;">MODVFD command word for CW.</td>
   </tr>
   <tr>
     <td><b>$466</b></td>
     <td>Run CCW command</td>
     <td><b>34</b></td>
     <td>decimal</td>
     <td style="text-align: left;">MODVFD command word for CCW.</td>
   </tr>
   <tr>
     <td><b>$467</b></td>
     <td>Stop command</td>
     <td><b>1</b></td>
     <td>decimal</td>
     <td style="text-align: left;">MODVFD command word for stop.</td>
   </tr>
   <tr>
     <td><b>$468</b></td>
     <td>RPM input multiplier</td>
     <td><b>50</b></td>
     <td></td>
     <td style="text-align: left;">MODVFD RPM value multiplier for programming RPM.</td>
   </tr>
   <tr>
     <td><b>$469</b></td>
     <td>RPM input divider</td>
     <td><b>60</b></td>
     <td></td>
     <td style="text-align: left;">MODVFD RPM value divider for programming RPM.</td>
   </tr>
   <tr>
     <td><b>$470</b></td>
     <td>RPM output multiplier</td>
     <td><b>60</b></td>
     <td></td>
     <td style="text-align: left;">MODVFD RPM value multiplier for reading RPM.</td>
   </tr>
   <tr>
     <td><b>$471</b></td>
     <td>RPM output divider</td>
     <td><b>100</b></td>
     <td></td>
     <td style="text-align: left;">MODVFD RPM value divider for reading RPM.</td>
   </tr>
   <tr>
     <td><b>$478</b></td>
     <td>Spindle 2 Modbus address</td>
     <td><b>3</b></td>
     <td></td>
     <td style="text-align: left;">Spindle 2 Modbus address.</td>
   </tr>
   <tr>
     <td><b>$479</b></td>
     <td>Spindle 3 Modbus address</td>
     <td><b>4</b></td>
     <td></td>
     <td style="text-align: left;">Spindle 3 Modbus address.</td>
   </tr>
   <tr>
     <td><b>$481</b></td>
     <td>Autoreport interval</td>
     <td><b>0</b></td>
     <td>ms</td>
     <td style="text-align: left;">Interval the real time report will be sent, set to 0 to disable.<br>~Controller reset required for setting change to take effect~</td>
     <td></td>
   </tr>
   <tr>
     <td><b>$484</b></td>
     <td>Unlock required after E-stop</td>
     <td><b>Enabled</b> (1)</td>
     <td></td>
     <td style="text-align: left;">If set, unlock (by sending $X) is required after resetting a cleared E-Stop condition.</td>
     <td></td>
   </tr>
   <tr>
     <td><b>$486</b></td>
     <td>Lock coordinate systems</td>
     <td>G59.1: <b>OFF</b><br>G59.2: <b>OFF</b><br>G59.3: <b>OFF</b><br>(0)</td>
     <td></td>
     <td style="text-align: left;">Lock coordinate systems against accidental changes.</td>
     <td></td>
   </tr>
   <tr>
     <td><b>$511</b></td>
     <td>Spindle 1</td>
     <td><b>SLB_LASER</b><br>(7)</td>
     <td></td>
     <td style="text-align: left;">Spindle to use as spindle 1.<br>~Controller reset required for setting change to take effect~</td>
     <td rowspan="7"><a href="https://resources.sienci.com/view/slb-manual/#spindlers485">Docs</a></td>
   </tr>
   <tr>
     <td><b>$512</b></td>
     <td>Spindle 2</td>
     <td><b>Disabled</b><br>(8)</td>
     <td></td>
     <td style="text-align: left;">Spindle to use as spindle 2.<br>~Controller reset required for setting change to take effect~</td>
   </tr>
   <tr>
     <td><b>$513</b></td>
     <td>Spindle 3</td>
     <td><b>MODVFD</b><br>(5)</td>
     <td></td>
     <td style="text-align: left;">Spindle to use as spindle 3.<br>~Controller reset required for setting change to take effect~</td>
   </tr>
   <tr>
     <td><b>$520</b></td>
     <td>Spindle 0 tool number start</td>
     <td><b>0</b></td>
     <td></td>
     <td style="text-align: left;">Start of tool numbers for selecting spindle 0 (default spindle). Normally leave this at 0.</td>
   </tr>
   <tr>
     <td><b>$521</b></td>
     <td>Spindle 1 tool number start</td>
     <td><b>0</b></td>
     <td></td>
     <td style="text-align: left;">Start of tool numbers for selecting spindle 1.</td>
   </tr>
   <tr>
     <td><b>$522</b></td>
     <td>Spindle 2 tool number start</td>
     <td><b>0</b></td>
     <td></td>
     <td style="text-align: left;">Start of tool numbers for selecting spindle 2.</td>
   </tr>
   <tr>
     <td><b>$523</b></td>
     <td>Spindle 3 tool number start</td>
     <td><b>0</b></td>
     <td></td>
     <td style="text-align: left;">Start of tool numbers for selecting spindle 3.</td>
   </tr>
   <tr style="color: var(--sl-blue-d);">
     <td><b>$650</b></td>
     <td>Chopper toff</td>
     <td><b>1</b></td>
     <td></td>
     <td style="text-align: left;">Off time. Duration of slow decay phase as a multiple of system clock periods: NCLK= 24 + (32 x TOFF). This will limit the maximum chopper frequency (0-15).<br>0: MOSFETs shut off, driver disabled.<br>1: Use with TBL of minimum 24 clocks.</td>
     <td></td>
   </tr>
   <tr style="color: var(--sl-blue-d);">
     <td><b>$651</b></td>
     <td>Chopper tbl</td>
     <td><b>1</b></td>
     <td></td>
     <td style="text-align: left;">Blanking time interval in system clock periods (0-3 = 16,24,36,54). Needs to cover the switching event and the duration of the ringing on the sense resistor.</td>
     <td></td>
   </tr>
   <tr style="color: var(--sl-blue-d);">
     <td><b>$652</b></td>
     <td>Chopper chm</td>
     <td><b>0</b></td>
     <td></td>
     <td style="text-align: left;">Chopper mode. Affects HDEC, HEND, and HSTRT parameters.<br>0: Standard mode (SpreadCycle).<br>1: Constant TOFF with fast decay time. Fast decay is after on time. Fast decay time is also terminated when the negative nominal current is reached.</td>
     <td></td>
   </tr>
   <tr style="color: var(--sl-blue-d);">
     <td><b>$653</b></td>
     <td>Chopper hstr</td>
     <td><b>2</b></td>
     <td></td>
     <td style="text-align: left;">CHM=0: Hysteresis start, offset from HEND (0-7 = 1-8). To be effective, HEND+HSTRT must be ≤15.<br>CHM=1: Fast decay time. Three least-significant bits of the duration of the fast decay phase. The MSB is HDEC0. Fast decay time is a multiple of system clock periods: NCLK= 32 x (HDEC0+HSTRT).</td>
     <td></td>
   </tr>
   <tr style="color: var(--sl-blue-d);">
     <td><b>$654</b></td>
     <td>Chopper hend</td>
     <td><b>8</b></td>
     <td></td>
     <td style="text-align: left;">Can be either negative, zero, or positive, 0-15 = -3 to 12.<br>CHM=0: Hysteresis end (low). Sets the hysteresis end value after a number of decrements, used for the hysteresis chopper and controlled by HDEC. HSTRT+HEND must be less than 16. 1/512 adds to the current setting.<br>CHM=1: Sine wave offset. A positive offset corrects for zero crossing error. 1/512 adds to the absolute value of each sine wave entry.</td>
     <td></td>
   </tr>
   <tr style="color: var(--sl-blue-d);">
     <td><b>$655</b></td>
     <td>Chopper hdec</td>
     <td><b>0</b></td>
     <td></td>
     <td style="text-align: left;">CHM=0: Hysteresis decrement interval period in system clock periods. Determines the slope of the hysteresis during on time from fast to very slow (0-3 = 16,32,48,64).<br>CHM=1: Fast decay mode.</td>
     <td></td>
   </tr>
   <tr style="color: var(--sl-blue-d);">
     <td><b>$656</b></td>
     <td>Chopper rndtf</td>
     <td><b>1</b></td>
     <td></td>
     <td style="text-align: left;">Change from fixed to randomized TOFF times, by dNCLK= -24 to +6 clocks. Only for CHM=1.</td>
     <td></td>
   </tr>
   <tr style="color: var(--sl-blue-d);">
     <td><b>$657</b></td>
     <td>THRESH</td>
     <td><b>22</b></td>
     <td></td>
     <td style="text-align: left;">StallGuard threshold.</td>
     <td></td>
   </tr>
   <tr style="color: var(--sl-blue-d);">
     <td><b>$658</b></td>
     <td>CoolStep semin</td>
     <td><b>7</b></td>
     <td></td>
     <td style="text-align: left;">Lower CoolStep threshold. If the SG value falls below SEMIN x 32, the coil current scaling factor is increased (0-15).<br>0: CoolStep disabled.</td>
     <td></td>
   </tr>
   <tr style="color: var(--sl-blue-d);">
     <td><b>$659</b></td>
     <td>CoolStep seup</td>
     <td><b>3</b></td>
     <td></td>
     <td style="text-align: left;">Number of increments of the coil current each time SG is sampled below the lower threshold (0-3 = 1,2,4,8).</td>
     <td></td>
   </tr>
   <tr style="color: var(--sl-blue-d);">
     <td><b>$660</b></td>
     <td>CoolStep semax</td>
     <td><b>0</b></td>
     <td></td>
     <td style="text-align: left;">Upper CoolStep threshold offset from lower threshold. If SG is sampled above (SEMIN+SEMAX+1)x32 enough times, the coil current scaling factor is decremented (0-15).</td>
     <td></td>
   </tr>
   <tr style="color: var(--sl-blue-d);">
     <td><b>$661</b></td>
     <td>CoolStep sedn</td>
     <td><b>3</b></td>
     <td></td>
     <td style="text-align: left;">Number of times SG must be sampled above the upper threshold before the coil current is decremented (0-3 = 32,8,2,1).</td>
     <td></td>
   </tr>
   <tr style="color: var(--sl-blue-d);">
     <td><b>$662</b></td>
     <td>CoolStep seimin</td>
     <td><b>0</b></td>
     <td></td>
     <td style="text-align: left;">Minimum CoolStep current as a factor of the set motor current.<br>0: 1/2, 1: 1/4</td>
     <td></td>
   </tr>
   <tr style="color: var(--sl-blue-d);">
     <td><b>$663</b></td>
     <td>drvconf_reg</td>
     <td><b>41759</b></td>
     <td></td>
     <td style="text-align: left;">DRVCONF register defaults 0xA31F. All protections enabled.</td>
     <td></td>
   </tr>
   <tr>
     <td><b>$664</b></td>
     <td>Ring pixels</td>
     <td><b>0</b></td>
     <td></td>
     <td style="text-align: left;">Number of individual pixels or LEDs connected.<br>~Controller reset required for setting change to take effect~</td>
     <td rowspan="2"><a href="https://resources.sienci.com/view/slb-manual/#status-lights">Docs</a></td>
   </tr>
   <tr>
     <td><b>$665</b></td>
     <td>Rail pixels</td>
     <td><b>1</b></td>
     <td></td>
     <td style="text-align: left;">Number of individual pixels or LEDs connected. Include the onboard LED.<br>~Controller reset required for setting change to take effect~</td>
   </tr>
   <tr style="color: var(--sl-orange);">
     <td><b>$666</b></td>
     <td>Using add-ons</td>
     <td>(0)</td>
     <td></td>
     <td style="text-align: left;">Sienci specific capability flags.</td>
     <td></td>
   </tr>
   <tr>
     <td><b>$668</b></td>
     <td>Invert TLS input</td>
     <td><b>Enabled</b> (1)</td>
     <td></td>
     <td style="text-align: left;">Invert the TLS input ahead of the OR function.<br>~Controller reset required for setting change to take effect~</td>
     <td></td>
   </tr>
   <tr>
     <td><b>$730</b></td>
     <td>Maximum laser power</td>
     <td><b>255</b></td>
     <td></td>
     <td style="text-align: left;">Maximum S word power for laser.</td>
     <td rowspan="9"><a href="https://resources.sienci.com/view/slb-manual/#laser">Docs</a></td>
   </tr>
   <tr>
     <td><b>$731</b></td>
     <td>Minimum laser power</td>
     <td><b>0</b></td>
     <td></td>
     <td style="text-align: left;">Minimum S word power for laser.</td>
   </tr>
   <tr>
     <td><b>$733</b></td>
     <td>Laser PWM frequency</td>
     <td><b>1000</b></td>
     <td>Hz</td>
     <td style="text-align: left;">Laser PWM frequency.</td>
   </tr>
   <tr>
     <td><b>$734</b></td>
     <td>Laser PWM off value</td>
     <td><b>0</b></td>
     <td>percent</td>
     <td style="text-align: left;">Laser PWM off value in percent (duty cycle).</td>
   </tr>
   <tr>
     <td><b>$735</b></td>
     <td>Laser PWM min value</td>
     <td><b>0</b></td>
     <td>percent</td>
     <td style="text-align: left;">Laser PWM min value in percent (duty cycle).</td>
   </tr>
   <tr>
     <td><b>$736</b></td>
     <td>Laser PWM max value</td>
     <td><b>100</b></td>
     <td>percent</td>
     <td style="text-align: left;">Laser PWM max value in percent (duty cycle).</td>
   </tr>
   <tr>
     <td><b>$741</b></td>
     <td>Laser X offset</td>
     <td><b>0</b></td>
     <td>mm</td>
     <td style="text-align: left;">Laser offset from spindle on X-axis.</td>
   </tr>
   <tr>
     <td><b>$742</b></td>
     <td>Laser Y offset</td>
     <td><b>0</b></td>
     <td>mm</td>
     <td style="text-align: left;">Laser offset from spindle on Y-axis.</td>
   </tr>
   <tr>
     <td><b>$743</b></td>
     <td>Invert laser signals</td>
     <td>Enable: <b>OFF</b><br>PWM: <b>OFF</b><br>(0)</td>
     <td></td>
     <td style="text-align: left;">Inverts the laser enable and PWM signals (active high).<br>~Controller reset required for setting change to take effect~</td>
   </tr>
</tbody>
</table>
[/su_table]
