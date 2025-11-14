---
title: ytsb LongMill Spindle Kit
menu_order: 9
post_status: draft
post_excerpt: How to set up your Sienci Labs 1.5KW air-cooled spindle for the LongMill MK2 CNC machine. Includes wiring instructions and firmware changes on gSender.
post_date: 2022-03-17 20:28:00
taxonomy:
    knowledgebase_cat: lmk2-add-ons
    knowledgebase_tag:
        - mk2
custom_fields:
    KBName: LongMill MK2 CNC
    basepress_post_icon: bp-caret-right
skip_file: no
featured_image: _images/_lmmk2/_add-ons/lmk2_spindle_vfd_components.jpg
---

This is a setup guide for the LongMill Spindle Kit, installed on the LongMill MK2 and using the SLB controller.

## Machine Setup

You will need:

1. LongMill Spindle and Dust Shoe Kit
   - 80mm Diameter LongMill Router/Spindle Mount
   - 110V, 1.5KW, 3-Phase VFD
   - 1.5KW 110V Air-Cooled Spindle
1. Flathead screwdriver
1. Allen keys

![](/_images/_lmmk2/_add-ons/lmk2_spindle_vfd_components.jpg "VFD components, labelled"){.aligncenter .size-medium}

*****Throughout this assembly, do not disconnect any of the VFD wiring! Miswiring can cause operation errors and damage to the device.**

1. Our first goal is to route the spindle cable through the drag chain, by undoing clips and detaching the drag chain when needed
   - You can use a sturdy flathead screwdriver to pry the clips open at the side
   [caption id="attachment_9057" align="aligncenter" width="802"]<img class="wp-image-9057 " src="https://resources.sienci.com/wp-content/uploads/2025/02/lmk2_spindle_short-1.gif" alt="" width="802" height="451" /> Opening drag chain clips with flathead screwdriver[/caption]
   - You can pop off the drag chain from the ends by wedging the screwdriver between the connecting tabs.
   ![](/_images/_lmmk2/_add-ons/lmk2_spindle_remove_chain-1.jpg "Using screwdriver to undo drag chain links"){.aligncenter .size-medium}
1. Remove the Makita power cable from the drag chain, and the power extension cable if you have one. Route the spindle cable through the following path.
  ![](/_images/_lmmk2/_add-ons/lmk2_spindle_cableroute-1.jpg "Spindle cable path from VFD to Z-axis"){.aligncenter .size-medium}
  ![](/_images/_lmmk2/_add-ons/lmk2_spindle_routingcable.jpg "Routing cable through open drag chain"){.aligncenter .size-medium}
  ![](/_images/_lmmk2/_add-ons/lmk2_spindle_connector-1.jpg "Spindle connector should dangle over the Z-axis, to plug into spindle later"){.aligncenter .size-medium}
1. Re-attach the drag chain clips and any drag chain segments, securing the spindle cable and the other existing cables in place.
1. We will move on to installing the spindle itself. Using an Allen key, loosen the front two clamping screws at the mount. Remove the Makita router.
  ![](/_images/_lmmk2/_add-ons/lmk2_spindle_mount.jpg "Front clamping screws loosened using Allen key"){.aligncenter .size-medium}
1. Jog the Z-axis all the way up to gain access to the four (4) M5x25mm screws at the back of the XZ gantry.
1. Using an Allen key, unfasten the back screws to remove the mount.
  ![](/_images/_lmmk2/_add-ons/lmk2_spindle_fastening.jpg "Back screws of XZ gantry being removed"){.aligncenter .size-medium}
  If you have trouble accessing the 4 screws, you can raise the router mount higher by removing the screws at the anti-backlash block.
1. Take the new 80mm mount and loosely secure it using all four screws at the back of the XZ gantry.
  ![](/_images/_lmmk2/_add-ons/lmk2_spindle_loosely-securing-mount.jpg "Loosely threading screws into the 80mm mount"){.aligncenter .size-medium}
1. Then, completely fasten the four screws.
1. Loosen the front two clamping screws on the 80mm mount.
1. Place the spindle through the mount, and fasten the clamping screws to secure the spindle in place (you can adjust the height later).
  [caption id="attachment_9055" align="aligncenter" width="806"]<img class="wp-image-9055 size-full" src="https://resources.sienci.com/wp-content/uploads/2025/02/lmk2_spindle_placingspindle_short.gif" alt="" width="806" height="453" /> Sliding spindle into new 80mm mount[/caption]
1. Plug in the spindle cable connector into the top of the spindle.
  ![](/_images/_lmmk2/_add-ons/lmk2_spindle_spindleconnector.jpg "Spindle cable connected"){.aligncenter .size-medium}
1. Plug in the RS485 wire into the SLB controller.
  ![](/_images/_lmmk2/_add-ons/lmk2_spindle_RS485-longmill-.jpg "RS485 wire connected to controller"){.aligncenter .size-medium}
1. If your SLB is powered on, please turn it **OFF** now.
1. Plug the VFD into power, the VFD screen should blink on with red text.
  [caption id="attachment_9056" align="aligncenter" width="850"]<img class="size-medium wp-image-9056" src="https://resources.sienci.com/wp-content/uploads/2025/02/lmk2_spindle_VFD-powered-on_short-1.gif" alt="" width="850" height="478" /> VFD powered on[/caption]
1. Turn ON the controller using the power switch and make sure the E-stop is released. We will now move to setting things up on gSender.
  ![](/_images/_lmmk2/_add-ons/lmk2_spindle_controllerOn.jpg){.aligncenter .size-medium}

## gSender Settings

[tabby title="Current gSender" open="yes"]
<ol>
  <li>Connect to the machine in gSender. Make sure that you are connected under the "grblHAL" firmware.<img class="size-medium aligncenter" src="https://resources.sienci.com/wp-content/uploads/2025/07/lmk2_ad_spin_connectcnc.jpg" alt="" width="850" height="478" /></li>
  <li>Download the following g-code file: <strong><strong><a href="https://drive.google.com/file/d/1FIc4F_efV6NAogkzlTXpoqt_CyiHO6x2/view?usp=drive_link">LongMill Spindle Configuration (SLB Controller only).gcode</a></strong></strong> At the bottom of the screen on gSender, press "Load File," select the g-code file, and then press "Start".  The file should finish executing instantly, without any machine movement.<img class="size-medium aligncenter" src="https://resources.sienci.com/wp-content/uploads/2025/07/lmk2_ad_spin-fileload.gif" alt="" width="850" height="478" /></li>
  <li>Return to the Spindle/Laser section and enable these functions by flipping the enable Spindle/Laser toggle to turn them ON. Don't forget to apply your new settings!<img class="size-medium aligncenter" src="https://resources.sienci.com/wp-content/uploads/2025/07/lmk2_ad_spin_toggleon.jpg" alt="" width="850" height="478" /></li>
  <li>We will now reset everything so our changes can successfully take effect. Turn OFF the controller at the power switch.</li>
  <li>Unplug the spindle from power.</li>
  <li>Close gSender.</li>
  <li>Then, turn ON the controller, plug the spindle back into power, open gSender and reconnect.</li>
  <li>At the ‘Spindle/Laser’ tab, check that ‘H-100’ is selected. Then use the slider to the lowest speed, and press the ‘Forward’ button to test out the spindle. Check that it is spinning in the correct direction. Press the ‘Stop’ button to stop the spindle. You are almost ready to start CNCing with the spindle! <img class="size-medium aligncenter" src="https://resources.sienci.com/wp-content/uploads/2025/07/lmk2_ad_spin_forward.jpg" alt="" width="850" height="478" /></li>
</ol>

[tabby title="Classic gSender"]
<ol>
  <li>Connect to the machine on gSender. Make sure that you are connected under the "grblHAL" firmware.
[caption id="attachment_11820" align="aligncenter" width="850"]<img class="wp-image-11820 size-medium aligncenter" src="https://resources.sienci.com/wp-content/uploads/2022/03/Screenshot-2024-12-02-140244-850x452.png" alt="" width="850" height="452" /> Connect to your controller in gSender</li>
  <li>Download the following g-code file: <strong><strong><a href="https://drive.google.com/file/d/1FIc4F_efV6NAogkzlTXpoqt_CyiHO6x2/view?usp=drive_link">LongMill Spindle Configuration (SLB Controller only).gcode</a></strong></strong> At the bottom of the screen on gSender, press "Load File," select the g-code file, and then press "Start Job."  The file should finish executing instantly, without any machine movement. You will also see "Error 14" on screen, which you can ignore.
[caption id="attachment_11821" align="aligncenter" width="800"]<img class="wp-image-11821 size-full aligncenter" src="https://resources.sienci.com/wp-content/uploads/2022/03/2024-12-0214-04-06-ezgif.com-video-to-gif-converter.gif" alt="" width="800" height="450" /> Run LongMill Spindle Configuration (SLB Controller only).gcode.</li>
  <li>Press the ‘gear’ on the top right corner, then press ‘Spindle/Laser’ on the left column, and toggle the ‘<strong>Spindle/Laser</strong>’ to be <strong>ON</strong>. <img class="wp-image-9031 size-medium aligncenter" src="https://resources.sienci.com/wp-content/uploads/2024/08/SpindleLaser-toggle--850x478.png" alt="" width="850" height="478" />
Set the spindle’s ‘Min’ and ‘Max’ speeds as 7500 and 24,000 RPM, respectively. Then close the window.<img class="size-medium wp-image-8152 aligncenter" src="https://resources.sienci.com/wp-content/uploads/2024/06/SpindleSpeedSettinggSenderUI-scaled-e1720724308475-850x479.jpg" alt="" width="850" height="479" />
<ol>
  <li>We will now reset everything so our changes can successfully take effect. Turn OFF the controller at the power switch.</li>
  <li>Unplug the spindle from power.</li>
  <li>Close gSender.</li>
  <li>Then, turn ON the controller, plug the spindle back into power, and open gSender and reconnect.</li>
</ol>
</li>
  <li>At the ‘Spindle/Laser’ tab, check that ‘H-100’ is selected. Then use the slider to the lowest speed, and press the ‘CW’ button to test out the spindle. Check that it is spinning in the correct direction. Press the ‘Stop’ button to stop the spindle. You are almost ready to start CNCing with the spindle!
[caption id="attachment_9033" align="aligncenter" width="1024"]<img class="wp-image-9033 size-large aligncenter" src="https://resources.sienci.com/wp-content/uploads/2024/08/testingspindle-1024x576.png" alt="" width="1024" height="576" /> Spindle activated using CW button at lowest speed setting</li>
</ol>

[tabbyending]

## Spindle Firmware Settings

If the above does not work, please reference these Firmware settings and manually edit yours as needed.

[su_table responsive="yes"]
<table>
<thead>
<tr>
<th>$</th>
<th>Name</th>
<th>Value (number)</th>
<th>Units</th>
<th>Description</th>
</tr>
</thead>
<tbody>
<tr>
<td><b>$30</b></td>
<td>Maximum spindle speed</td>
<td><b>24000</b></td>
<td>RPM</td>
<td style="text-align: left;">Maximum spindle speed, can be overridden by spindle plugins.</td>
</tr>
<tr>
<td><b>$31</b></td>
<td>Minimum spindle speed</td>
<td><b>7500</b></td>
<td>RPM</td>
<td style="text-align: left;">Minimum spindle speed, can be overridden by spindle plugins.</td>
</tr>
<tr>
<td><b>$37</b></td>
<td>Steppers de-energize</td>
<td>X: <b>OFF</b> Y: <b>OFF</b> Z: <b>ON</b> A: <b>OFF</b> (4)</td>
<td></td>
<td>Keeps power to the stepper motors at all times</td>
</tr>
<tr>
<td><b>$340</b></td>
<td>Spindle at speed tolerance</td>
<td><b>5</b></td>
<td>percent</td>
<td style="text-align: left;">Spindle at speed tolerance as percentage deviation from programmed speed, set to 0 to disable. If not within tolerance when checked after spindle on delay ($392) alarm 14 is raised.</td>
</tr>
<tr>
<td><b>$374</b></td>
<td>Modbus baud rate</td>
<td><b>19200</b> (3)</td>
<td></td>
<td style="text-align: left;"></td>
</tr>
<tr>
<td><b>$375</b></td>
<td>Modbus RX timeout</td>
<td><b>50</b></td>
<td>milliseconds</td>
<td style="text-align: left;"></td>
</tr>
<tr>
<td><b>$392</b></td>
<td>Spindle on delay</td>
<td><b>11</b></td>
<td>s</td>
<td style="text-align: left;">Delay to allow spindle to spin up after safety door is opened.</td>
</tr>
<tr>
<td><b>$395</b></td>
<td>Current Spindle</td>
<td><b>H-100 VFD Spindle</b> (6)</td>
<td></td>
<td style="text-align: left;">Spindle selected on startup.</td>
</tr>
<tr>
<td><b>$476</b></td>
<td>ModBus Address</td>
<td><b>0</b></td>
<td></td>
<td style="text-align: left;"></td>
</tr>
</tbody>
</table>
[/su_table]

## Spindle Break-in

The grease inside the bearings may have shifted during transportation, it is recommended that you run a “break-in” cycle to redistribute the grease before using your spindle. To do this, you can download and run the g-code file below on gSender, which should take 1 hour 40 minutes to run.

<a href="https://drive.google.com/file/d/1JdrqfgkZxhhXIAjUMOi-5UXIDjNveZe3/view?usp=sharing">Sienci 1.5kW Spindle Break-in.gcode</a>

To run the file connect to gSender and press ‘Load File’ at the bottom left corner. Select the file and you should see a ‘Start Job’ button appear, go ahead and click that.
