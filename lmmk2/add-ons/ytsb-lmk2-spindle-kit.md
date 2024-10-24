---
title: ytsb LongMill Spindle Kit
menu_order: 7
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
skip_file: yes
featured_image: 
---

This is a setup guide for the LongMill Spindle Kit, installed on the LongMill MK2 and using the SLB controller.

If you prefer to watch a video of this process, check out Jason's video below:

https://www.YouTube.com/watch?v=5mEJLWWHE-Y

<h2>Machine Setup</h2>

You will need:

<ol>
  <li>LongMill Spindle and Dust Shoe Kit
<ul>
  <li>80mm Diameter LongMill Router/Spindle Mount</li>
  <li>110V, 1.5KW, 3-Phase VFD</li>
  <li>1.5KW 110V Air-Cooled Spindle</li>
</ul>
</li>
  <li>Flathead screwdriver</li>
  <li>Allen keys</li>
</ol>

[caption id="attachment_9022" align="aligncenter" width="850"]<img class="size-medium wp-image-9022" src="https://resources.sienci.com/wp-content/uploads/2024/08/VFD-components-850x478.png" alt="" width="850" height="478" /> VFD components, labelled[/caption]

<strong>***Throughout this assembly, do not disconnect any of the VFD wiring! Miswiring can cause operation errors and damage to the device.</strong>

<ol>
  <li>Our first goal is to route the spindle cable through the drag chain, by undoing clips and detaching the drag chain when needed
<ol>
  <li>You can use a sturdy flathead screwdriver to pry the clips open at the side

[caption id="attachment_9057" align="aligncenter" width="576"]<img class="wp-image-9057 size-full" src="https://resources.sienci.com/wp-content/uploads/2024/08/unclippingdragchain_short.gif" alt="" width="576" height="324" /> Opening drag chain clips with flathead screwdriver[/caption]</li>
  <li>You can pop off the drag chain from the ends by wedging the screwdriver between the connecting tabs.

[caption id="attachment_9026" align="aligncenter" width="850"]<img class="size-medium wp-image-9026" src="https://resources.sienci.com/wp-content/uploads/2024/08/remove-drag-chain-850x478.png" alt="" width="850" height="478" /> Using screwdriver to undo drag chain links[/caption]</li>
</ol>
</li>
  <li>Remove the Makita power cable from the drag chain, and the power extension cable if you have one. Route the spindle cable through the following path.

[caption id="attachment_9036" align="aligncenter" width="850"]<img class="size-medium wp-image-9036" src="https://resources.sienci.com/wp-content/uploads/2024/08/LM-spindle-cable-route-850x635.png" alt="" width="850" height="635" /> Spindle cable path from VFD to Z-axis[/caption]

[caption id="attachment_9039" align="aligncenter" width="850"]<img class="size-medium wp-image-9039" src="https://resources.sienci.com/wp-content/uploads/2024/08/routing-cable-850x513.png" alt="" width="850" height="513" /> Routing cable through open drag chain[/caption]

[caption id="attachment_9029" align="aligncenter" width="850"]<img class="size-medium wp-image-9029" src="https://resources.sienci.com/wp-content/uploads/2024/08/spindle-connector-850x478.png" alt="" width="850" height="478" /> Spindle connector should dangle over the Z-axis, to plug into spindle later[/caption]</li>
  <li>Re-attach the drag chain clips and any drag chain segments, securing the spindle cable and the other existing cables in place.</li>
  <li>We will move on to installing the spindle itself. Using an Allen key, loosen the front two clamping screws at the mount. Remove the Makita router.

[caption id="attachment_9027" align="aligncenter" width="850"]<img class="size-medium wp-image-9027" src="https://resources.sienci.com/wp-content/uploads/2024/08/removing-front-screws-on-mount-850x478.png" alt="" width="850" height="478" /> Front clamping screws loosened using Allen key[/caption]</li>
  <li>Jog the Z-axis all the way up to gain access to the four (4) M5x25mm screws at the back of the XZ gantry.</li>
  <li>Using an Allen key, unfasten the back screws to remove the mount.

[caption id="attachment_9035" align="aligncenter" width="850"]<img class="size-medium wp-image-9035" src="https://resources.sienci.com/wp-content/uploads/2024/08/fastening-back-screws-850x478.png" alt="" width="850" height="478" /> Back screws of XZ gantry being removed[/caption]</li>
  <li>Take the new 80mm mount and loosely secure it using all four screws at the back of the XZ gantry.

[caption id="attachment_9037" align="aligncenter" width="850"]<img class="size-medium wp-image-9037" src="https://resources.sienci.com/wp-content/uploads/2024/08/loosely-securing-mount-850x478.png" alt="" width="850" height="478" /> Loosely threading screws into the 80mm mount[/caption]</li>
  <li>Then, completely fasten the four screws.</li>
  <li>Loosen the front two clamping screws on the 80mm mount.</li>
  <li>Place the spindle through the mount, and fasten the clamping screws to secure the spindle in place (you can adjust the height later).

[caption id="attachment_9055" align="aligncenter" width="806"]<img class="wp-image-9055 size-full" src="https://resources.sienci.com/wp-content/uploads/2024/08/placingspindle_short.gif" alt="" width="806" height="453" /> Sliding spindle into new 80mm mount[/caption]</li>
  <li>Plug in the spindle cable connector into the top of the spindle.

[caption id="attachment_9030" align="aligncenter" width="850"]<img class="size-medium wp-image-9030" src="https://resources.sienci.com/wp-content/uploads/2024/08/spindleconnector-850x478.png" alt="" width="850" height="478" /> Spindle cable connected[/caption]</li>
  <li>Plug in the RS485 wire into the SLB controller.

[caption id="attachment_9028" align="aligncenter" width="850"]<img class="size-medium wp-image-9028" src="https://resources.sienci.com/wp-content/uploads/2024/08/RS485-LongMill--850x478.png" alt="" width="850" height="478" /> RS485 wire connected to controller[/caption]</li>
  <li>Plug the VFD into power, the VFD screen should blink on with red text.

[caption id="attachment_9056" align="aligncenter" width="850"]<img class="size-medium wp-image-9056" src="https://resources.sienci.com/wp-content/uploads/2024/08/VFD-powered-on_short.gif" alt="" width="850" height="478" /> VFD powered on[/caption]</li>
  <li>Turn ON the controller using the power switch and make sure the E-stop is released. We will now move to setting things up on gSender.
<img class="size-medium wp-image-9034 aligncenter" src="https://resources.sienci.com/wp-content/uploads/2024/08/controllerOn-850x478.png" alt="" width="850" height="478" /></li>
</ol>

<h2>gSender Settings</h2>

<ol>
  <li>Connect to the machine on gSender.</li>
  <li>We will now enable the setting that allows for communication between your controller and the spindle. Click on ‘Firmware’ in the top right corner of gSender to open the firmware window. Search or scroll down to find the setting called ‘<strong>$395 Default Spindle</strong>’, and select the ‘<strong>H-100</strong>’ option then click ‘Apply New Settings’. Close the window.

[caption id="attachment_9024" align="aligncenter" width="960"]<img class="wp-image-9024 size-full" src="https://resources.sienci.com/wp-content/uploads/2024/08/395-default-spindle.png" alt="" width="960" height="540" /> Selecting H-100 for $395 and applying settings[/caption]</li>
  <li>Power cycle by turning the controller power switch OFF, waiting 5 seconds, then turning it back ON.</li>
  <li>Reconnect to the machine again.</li>
  <li>Now we will configure a new setting that should appear after you power cycled the controller. This setting is like the telephone number you dial to talk to the VFD. Click on ‘Firmware’ in the top right corner of gSender to open the firmware window. Search or scroll down to find the setting ‘<strong>$476 Spindle 0 ModBus address</strong>’ and set it to ‘<strong>2</strong>’.

[caption id="attachment_9025" align="aligncenter" width="960"]<img class="size-full wp-image-9025" src="https://resources.sienci.com/wp-content/uploads/2024/08/FirmwareToolModbusValue.png" alt="" width="960" height="540" /> Specifying ModBus address[/caption]</li>
  <li>Find ‘<strong>$37</strong>’ and toggle the <strong>Z</strong> to be <strong>ON</strong>, so that the Z motor stays energized. Now, we can press ‘Apply New Settings’ and exit the window.

[caption id="attachment_9032" align="aligncenter" width="960"]<img class="size-full wp-image-9032" src="https://resources.sienci.com/wp-content/uploads/2024/08/steppers-deenergize.png" alt="" width="960" height="540" /> Toggle the Z to be ON for steppers de-energize setting[/caption]</li>
  <li>Press the ‘gear’ on the top right corner, then press ‘Spindle/Laser’ on the left column, and toggle the ‘<strong>Spindle/Laser</strong>’ to be <strong>ON</strong>. Then close the window.

[caption id="attachment_9031" align="aligncenter" width="960"]<img class="size-full wp-image-9031" src="https://resources.sienci.com/wp-content/uploads/2024/08/SpindleLaser-toggle-.png" alt="" width="960" height="540" /> Toggling Spindle/Laser[/caption]</li>
  <li>We will now reset everything so our changes can successfully take effect. Turn OFF the controller at the power switch.</li>
  <li>Unplug the spindle from power.</li>
  <li>Close gSender.</li>
  <li>Then, turn ON the controller, plug the spindle back into power, and open gSender and reconnect.</li>
  <li>At the ‘Spindle/Laser’ tab, check that ‘H-100’ is selected. Then use the slider to the lowest speed, and press the ‘CW’ button to test out the spindle. Check that it is spinning in the correct direction. Press the ‘Stop’ button to stop the spindle. You are almost ready to start CNCing with the spindle!

[caption id="attachment_9033" align="aligncenter" width="1024"]<img class="wp-image-9033 size-large" src="https://resources.sienci.com/wp-content/uploads/2024/08/testingspindle-1024x576.png" alt="" width="1024" height="576" /> Spindle activated using CW button at lowest speed setting[/caption]</li>
</ol>

<h2>Spindle Break-in</h2>

The grease inside the bearings may have shifted during transportation, it is recommended that you run a “break-in” cycle to redistribute the grease before using your spindle. To do this, you can download and run the g-code file below on gSender, which should take 1 hour 40 minutes to run.

<a href="https://drive.google.com/file/d/1JdrqfgkZxhhXIAjUMOi-5UXIDjNveZe3/view?usp=sharing">Sienci 1.5kW Spindle Break-in.gcode</a>
