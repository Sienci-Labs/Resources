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
skip_file: no
featured_image: _images/_lmmk2/_add-ons/lmk2_spindle_VFD-components.png
---

This is a setup guide for the LongMill Spindle Kit, installed on the LongMill MK2 and using the SLB controller.

If you prefer to watch a video of this process, check out Jason's video below:

https://www.youtube.com/watch?v=5mEJLWWHE-Y

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

![](https://resources.sienci.com/wp-content/uploads/2025/02/lmk2_spindle_vfd_components-1.jpg "VFD components, labelled"){.aligncenter .size-medium}

<strong>***Throughout this assembly, do not disconnect any of the VFD wiring! Miswiring can cause operation errors and damage to the device.</strong>

<ol>
  <li>Our first goal is to route the spindle cable through the drag chain, by undoing clips and detaching the drag chain when needed
<ol>
  <li>You can use a sturdy flathead screwdriver to pry the clips open at the side

![](/_images/_lmmk2/_add-ons/_all/lmk2_spindle_short.gif "Opening drag chain clips with flathead screwdriver"){.aligncenter .size-full}

</li>
  <li>You can pop off the drag chain from the ends by wedging the screwdriver between the connecting tabs.

![](/_images/_lmmk2/_add-ons/_all/lmk2_spindle_remove_chain.png "Using screwdriver to undo drag chain links"){.aligncenter .size-medium}

</li>
</ol>
</li>
  <li>Remove the Makita power cable from the drag chain, and the power extension cable if you have one. Route the spindle cable through the following path.

![](/_images/_lmmk2/_add-ons/_all/lmk2_spindle_cableroute.png "Spindle cable path from VFD to Z-axis"){.aligncenter .size-medium}

![](/_images/_lmmk2/_add-ons/_all/lmk2_spindle_routingcable.png "Routing cable through open drag chain"){.aligncenter .size-medium}

![](/_images/_lmmk2/_add-ons/_all/lmk2_spindle_connector.png "Spindle connector should dangle over the Z-axis, to plug into spindle later"){.aligncenter .size-medium}

</li>
  <li>Re-attach the drag chain clips and any drag chain segments, securing the spindle cable and the other existing cables in place.</li>
  <li>We will move on to installing the spindle itself. Using an Allen key, loosen the front two clamping screws at the mount. Remove the Makita router.

![](/_images/_lmmk2/_add-ons/_all/lmk2_spindle_mount.png "Front clamping screws loosened using Allen key"){.aligncenter .size-medium}

</li>
  <li>Jog the Z-axis all the way up to gain access to the four (4) M5x25mm screws at the back of the XZ gantry.</li>
  <li>Using an Allen key, unfasten the back screws to remove the mount.

![](/_images/_lmmk2/_add-ons/_all/lmk2_spindle_fastening.png "Back screws of XZ gantry being removed"){.aligncenter .size-medium}

</li>
  <li>Take the new 80mm mount and loosely secure it using all four screws at the back of the XZ gantry.

![](/_images/_lmmk2/_add-ons/_all/lmk2_spindle_securingmount.png "Loosely threading screws into the 80mm mount"){.aligncenter .size-medium}

</li>
  <li>Then, completely fasten the four screws.</li>
  <li>Loosen the front two clamping screws on the 80mm mount.</li>
  <li>Place the spindle through the mount, and fasten the clamping screws to secure the spindle in place (you can adjust the height later).

![](/_images/_lmmk2/_add-ons/_all/lmk2_spindle_placingspindle.gif "Sliding spindle into new 80mm mount"){.aligncenter .size-full}

</li>
  <li>Plug in the spindle cable connector into the top of the spindle.

![](/_images/_lmmk2/_add-ons/_all/lmk2_spindle_spindleconnector.png "Spindle cable connected"){.aligncenter .size-medium}

</li>
  <li>Plug in the RS485 wire into the SLB controller.

![](/_images/_lmmk2/_add-ons/_all/lmk2_spindle_rs485.png "RS485 wire connected to controller"){.aligncenter .size-medium}

</li>
  <li>Plug the VFD into power, the VFD screen should blink on with red text.

![](/_images/_lmmk2/_add-ons/_all/lmk2_spindle_poweredon.gif "VFD powered on"){.aligncenter .size-full}

</li>
  <li>Turn ON the controller using the power switch and make sure the E-stop is released. We will now move to setting things up on gSender.

![](/_images/_lmmk2/_add-ons/_all/lmk2_spindle_controller_on.png){.aligncenter .size-medium}

</li>
</ol>

<h2>gSender Settings</h2>

<ol>
  <li>Connect to the machine on gSender.</li>
  <li>We will now enable the setting that allows for communication between your controller and the spindle. Click on ‘Firmware’ in the top right corner of gSender to open the firmware window. Search or scroll down to find the setting called ‘<strong>$395 Default Spindle</strong>’, and select the ‘<strong>H-100</strong>’ option then click ‘Apply New Settings’. Close the window.

![](/_images/_lmmk2/_add-ons/_all/lmk2_spindle_defaultspindle.png "Selecting H-100 for $395 and applying settings"){.aligncenter .size-medium}

</li>
  <li>Power cycle by turning the controller power switch OFF, waiting 5 seconds, then turning it back ON.</li>
  <li>Reconnect to the machine again.</li>
  <li>Now we will configure a new setting that should appear after you power cycled the controller. This setting is like the telephone number you dial to talk to the VFD. Click on ‘Firmware’ in the top right corner of gSender to open the firmware window. Search or scroll down to find the setting ‘<strong>$476 Spindle 0 ModBus address</strong>’ and set it to ‘<strong>2</strong>’.

![](/_images/_lmmk2/_add-ons/_all/lmk2_spindle_firmwaremodbus.png "Specifying ModBus address"){.aligncenter .size-medium}

</li>
  <li>Find ‘<strong>$37</strong>’ and toggle the <strong>Z</strong> to be <strong>ON</strong>, so that the Z motor stays energized. Now, we can press ‘Apply New Settings’ and exit the window.

![](/_images/_lmmk2/_add-ons/_all/lmk2_spindle_steppersdeenergize.png "Toggle the Z to be ON for steppers de-energize setting"){.aligncenter .size-medium}

</li>
  <li>Press the ‘gear’ on the top right corner, then press ‘Spindle/Laser’ on the left column, and toggle the ‘<strong>Spindle/Laser</strong>’ to be <strong>ON</strong>. Then close the window.

![](/_images/_lmmk2/_add-ons/_all/lmk2_spindle_spinlasertoggle.png "Toggling Spindle/Laser"){.aligncenter .size-medium}

</li>
  <li>We will now reset everything so our changes can successfully take effect. Turn OFF the controller at the power switch.</li>
  <li>Unplug the spindle from power.</li>
  <li>Close gSender.</li>
  <li>Then, turn ON the controller, plug the spindle back into power, and open gSender and reconnect.</li>
  <li>At the ‘Spindle/Laser’ tab, check that ‘H-100’ is selected. Then use the slider to the lowest speed, and press the ‘CW’ button to test out the spindle. Check that it is spinning in the correct direction. Press the ‘Stop’ button to stop the spindle. You are almost ready to start CNCing with the spindle!

![](/_images/_lmmk2/_add-ons/_all/lmk2_spindle_testingspindle.png "Spindle activated using CW button at lowest speed setting"){.aligncenter .size-medium}

</li>
</ol>

<h2>Spindle Break-in</h2>

The grease inside the bearings may have shifted during transportation, it is recommended that you run a “break-in” cycle to redistribute the grease before using your spindle. To do this, you can download and run the g-code file below on gSender, which should take 1 hour 40 minutes to run.

<a href="https://drive.google.com/file/d/1JdrqfgkZxhhXIAjUMOi-5UXIDjNveZe3/view?usp=sharing">Sienci 1.5kW Spindle Break-in.gcode</a>
