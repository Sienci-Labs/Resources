---
title: ytsb Edge Features
menu_order: 4
post_status: draft
post_excerpt: Learn the advanced features of gSender such as shortcuts, macros, workspaces, calibration tools, controlling spindles, lasers, coolant, and more.
post_date: 2021-07-01 15:55
taxonomy:
    knowledgebase_cat: gdocs
    knowledgebase_tag:
        - gsender
custom_fields:
    KBName: gSender
    basepress_post_icon: bp-caret-right
skip_file: no
featured_image: _images/_gsender/_edge/gs_edge_p1_Cycle.jpg
---
gSender Edge is our test arena for working on new and exciting gSender updates that will eventually be released to everyone. Think of it as a program that you can download independently from traditional gSender that allows you to participate in public Beta testing. This gives you the opportunity to use all the new features that we’re working on and make an impact by giving us feedback to inform the final result, that’s what it’s like to be on the bleeding <strong>Edge</strong>.

Edge isn’t a replacement for gSender in any way - it’s a way for us to test and get feedback on new, bigger features without exposing them to users who may not be interested or causing unexpected bugs. This follows a cycle that can be several months long where:

![](/_images/_gsender/_edge/gs_edge_p1_Cycle.jpg){.aligncenter .size-medium}

<ol>
  <li>A new Edge version is split off from Main in order to prototype some new functionality and features (you can tell when this happens because the numbering scheme will jump up from 1.1.6 to EDGE-1.2.0, for example)</li>
  <li>Edge eventually stops adding major features so it can become more refined from user feedback and squashing bugs</li>
  <li>Once everything seems stable, everything that’s been added to Edge becomes a part of Main gSender so that everyone can now enjoy the new features</li>
  <li>The process repeats</li>
</ol>

Downloading Edge is similar to the Main version of gSender and is available on the same page: <a href="https://sienci.com/gSender/" target="_blank" rel="noopener">https://sienci.com/gsender/</a>. The main caveat is that we don’t post the links for each operating system, so once you click the link to download Edge you’ll need to scroll down on the page to the “Assets” and click on the program download for your specific device. For Windows it’ll end in “.exe”, Mac will be “.dmg”, and the rest are for Linux and Pi.

<h2>Unique Differences</h2>

If you used to see a feature here but don’t see it any longer, it’s likely been added into the main version of gSender! Look for it on the other gSender documentation pages.

As of 1.4.1, the current notable features / improvements to Edge are:

<ul>
  <li><strong>Warn on Zero and Go To</strong>
<ul>
  <li>Easier movement to specific coordinates (either relative or absolute), available with a button press in the location widget</li>
  <li>New safety option that will always prompt when interacting with the Zero buttons to make sure you don’t accidentally set your workspace offset without meaning to</li>
</ul>
</li>
  <li><strong>Multi-corner probing</strong>
<ul>
  <li>You can now optionally select which corner of your workpiece you wish to probe from</li>
</ul>
</li>
  <li><strong>Gamepad improvement</strong>
<ul>
  <li>You can now add a secondary functionality to buttons</li>
  <li>Added joystick MPG mode</li>
  <li>New safety lockout button to deactivate gamepad when needed</li>
</ul>
</li>
  <li><strong>Rotary</strong>
<ul>
  <li>Added wizard for gSender to help set up your rotary unit by pre drilling accurate mounting holes</li>
  <li>Added Y-axis probing wizard for rotary set up</li>
  <li>New rotary mode replaces your Y-axis with a new rotary A-axis</li>
  <li>New post processor available to allow for g-code files to be exported from Vectric for rotary use</li>
  <li>Added auto Z-axis probing wizard</li>
  <li>Added rotary surfacing tool</li>
</ul>
</li>
  <li><strong>Job Stats and Maintenance</strong>
<ul>
  <li>Job stats section has been greatly fleshed out, now showing start time, duration of individual files, and any complications running them.</li>
  <li>Jobs per com port (individual machine) are also recorded</li>
  <li>New Maintenance reminders - setup maintenance tasks that will remind you when due to perform routine CNC maintenance</li>
  <li>Task due time range is based on the runtime from your jobs</li>
</ul>
</li>
  <li><strong>Toolchanging improvements</strong>
<ul>
  <li>Added pass through option that will not comment out M6 commands if you’re connected to a firmware that supports real tool change procedures</li>
  <li>Return of the codeblock - due to popular demand, pre-and post- codeblocks are now returned as a tool changing strategy.</li>
</ul>
</li>
  <li><strong> Remote mode improvements</strong>
<ul>
  <li>QR Code now viewable with remote mode enable for easier navigation to the remote interface on your phone</li>
</ul>
</li>
</ul>

<h3>Warn on Zero and Go To</h3>

If you've ever accidentally zeroed an axis when you meant to go to the existing zero, this is an option you can turn on that double checks when you want to zero. In settings on the safety tab, you can toggle this feature on. Then when you click on Zero X, Zero Y or Zero Z, you will see a popup asking for confirmation.

![](/_images/_gsender/_edge/gs_edge_p2_SafeToggle.jpg){.aligncenter .size-medium}

![](/_images/_gsender/_edge/gs_edge_p3_GoToGIF.gif){.aligncenter .size-medium}

We’ve improved the Go To function! You can use the blue Go To buttons beside each axis to move to X, Y or Z zeros individually as always. The improvement is under the Go To XY0 button, where you will now find a simple Go To button.

![](/_images/_gsender/_edge/gs_edge_p4_GoTo.jpg){.aligncenter .size-medium}

Hitting the Go To button will bring up a popup that will allow you to enter specific coordinates for each axis (Absolute or relative positioning). When you hit the Go button, you will move to the location you’ve designated!

![](/_images/_gsender/_edge/gs_edge_p5_GoToGIF.gif){.aligncenter .size-medium}

<h3>Multi Corner Probing</h3>

Most people prefer to probe the front, left corner of their material as the zero-point of their job, since that corner is easy to access, but in rare cases you might want to probe elsewhere. If you would like to probe from a different spot on your workpiece, you can now rotate to the corner of your choice. Simply press the icon in the top right corner to highlight where you are starting to probe. For example, if you wish to probe from the back right corner, hit the icon twice to move the highlighted section to the back right.

![](/_images/_gsender/_edge/gs_edge_p6_CornerGIF.gif){.aligncenter .size-medium}

<h3>Gamepad</h3>

You can select one of the preset and tested profiles or create your own. To create your own, connect your joystick to your computer and create a new profile using the ‘Add New Gamepad Profile’ button. This will enable you to set up multiple profiles if desired, for different controllers, as they each have their own unique ID.

![](/_images/_gsender/_edge/gs_edge_p7_Gamepads.jpg){.aligncenter .size-medium}

If you run into difficulty with getting a particular joystick set up in gSender, consider searching for documentation provided by the manufacturer (for example, <a href="https://support.xbox.com/en-CA/help/hardware-network/controller/connect-xbox-wireless-controller-to-pc">Xbox</a> or <a href="https://www.playstation.com/en-ca/support/hardware/ps4-pair-dualshock-4-wireless-with-pc-or-mac/">PlayStation</a>). Some joysticks may also require drivers to be downloaded so your computer can read the signals that the joystick sends out.
Connect your controller to your PC and press any button on it. gSender will identify and provide a profile if one is available. You can see in the screenshot below, it correctly identifies the DualSense Wireless Controller I’m adding. Enter your profile name and hit <strong>Add New Profile</strong>.

![](/_images/_gsender/_edge/gs_edge_p8_Profiles.png){.aligncenter .size-medium}

Your new profile will now appear on the Gamepad tab of the Shortcuts page in Settings. Click on the profile you want to edit.

![](/_images/_gsender/_edge/gs_edge_p9_AllProfiles.jpg){.aligncenter .size-medium}

Here you will find the shortcuts that you can assign to different buttons or your joysticks. You can see that the controller is connected, and that a Help button is available. You can push the buttons on your controller to see which number it corresponds to. You can then rename the shortcut button to match your controller by clicking on the black number. In this case, the X button corresponds to button 0. By pressing the plus symbol in the Action column, you will see a list of actions you can map to that button. I added an action for <strong>Homing - Go to back left corner</strong>. Now when I hit the X button on my controller, gSender will move the CNC to the back left corner!

![](/_images/_gsender/_edge/gs_edge_p10_ShortGIF.gif){.aligncenter .size-medium}

<h4>Lockout Button</h4>

You can assign a ‘lockout’ button for your controller. Simply hit the + sign in the 2nd Action column and add another action. This is great for a couple reasons. The first is gamepad safety. Your CNC won’t respond unless you hit the lockout button, and then your desired action. Sitting on or dropping your controller won’t suddenly activate one of your shortcuts.

The second advantage to using the ‘lockout’ button is that you can double up the actions available to you. Use the lockout button like a function or shift key to unlock even more controller shortcuts!

<h4>Joystick Options</h4>

You can use the Joystick Options section to move your assigned axis. In this section, you can select which joystick moves which axis. In this example, stick 1 controls the X axis left and right, and the Y axis forward and back. Stick 2 controls the A axis with left/right (If you are using the rotary) and the Z axis with up/down.

![](/_images/_gsender/_edge/gs_edge_p11_JoystickOptions.jpg){.aligncenter .size-medium}

The joysticks have two ways of functioning. You can apply continuous pressure and the CNC will respond accordingly. The speed of the direction you are going depends on how far you push your joystick in a particular direction. You can also flick the joystick once and the CNC will move one increment, according to the rapid/normal/precise movements you have set up for Jog Controls.

You can also invert any of these controls if you wish, by clicking the box to the right of 2nd Action. The Zero threshold allows you to adjust the sensitivity of your controller.

If your joystick isn’t performing as well as the automatic controls, you can make adjustments to your Zero Threshold or your Movement Distance Override.

<ul>
  <li>The <strong>Zero Threshold</strong> dials in how far you have to push a joystick for it to register.</li>
  <li>The <strong>Movement Distance Override</strong> allows you to fine-tune the jogging distance that is calculated when moving your joystick around. If you notice some stuttering when jogging, then the system is hungry for more commands, so try increasing the override value to help send jog commands more often. You will know you have eliminated lag if you see and hear the unit move around smoothly.</li>
</ul>

![](/_images/_gsender/_edge/gs_edge_p12_Overrides.jpg){.aligncenter .size-medium}

Another cool feature is the <strong>Use MPG</strong> selection. If you map one of your joysticks to an axis with MPG selected, it will automatically grey out the other stick selections. Now you can rotate your stick in any direction and for each quarter rotation, your axis will move once, according to your preselected Jog Controls.

![](/_images/_gsender/_edge/gs_edge_p13_MPG.jpg){.aligncenter .size-medium}

<h3>Rotary</h3>

gSender has a unique ability to control a rotary axis on normal, 3-axis grbl machines. We call this “rotary mode”; which isn't to be confused with grblHAL machines where gSender by default supports full, 4-axis motion. The idea is that once you're in this "rotary mode", gSender does the legwork to swap firmware settings over to your rotary setup, translate A-axis movements to your machine as if they were Y-axis movements, and as long as you've done the legwork to align and swap over your wires then your rotary A-axis should now be good to go!

<h4>Rotary Mode</h4>

Navigate to the Settings where you will find the Rotary settings. Here you can <strong>toggle</strong> the Rotary controls to make them visible on the main page.

![](/_images/_gsender/_edge/gs_edge_p14_RotaryGIF.gif){.aligncenter .size-medium}

Once the toggle has been turned to display, you will see an additional tab at the bottom right of the window, called Rotary. With this tab you can:

![](/_images/_gsender/_edge/gs_edge_p15_JogControls.jpg){.aligncenter .size-medium}

<ol>
  <li><strong>Jog Control</strong> - Rotate the A-axis, go to Zero, set Zero, and adjust speeds</li>
  <li><strong>Rotary Mode</strong> - Toggle into Rotary Mode</li>
  <li><strong>Rotary Surfacing</strong> - Wizard to turn square stock round</li>
  <li><strong>Probe Rotary Z axis</strong> - Automatically probe to find the Z axis</li>
  <li><strong>Y axis Alignment</strong> - Automatically probe to align the Y axis along the A axis (Turn rotary mode off to access this feature)</li>
  <li><strong>Rotary Mounting Setup</strong> - Drill holes in your wasteboard to mount our own <a href="https://sienci.com/product/vortex-rotary-axis/">Vortex Rotary</a> track (Turn rotary mode off to access this feature)</li>
</ol>

<em><strong>Note:</strong> Before switching to rotary mode, using the jog controls, rotary surfacing, or any other rotary actions, you’ll need to check that you’ve got your rotary set up and positioned correctly. This includes table mounting and Y-axis alignment, outlined below.</em>

<h4>Rotary Mounting Setup</h4>

When mounting a rotary axis, it’s important to be parallel to the X-axis, and helpful to have a repeatable position so you can reliably mount and unmount the rotary, depending on when you want to use it. If you have your own rotary axis, this is a step that you'll have to do yourself.

For those who might have our Vortex rotary axis, the '<strong>Rotary Mounting Setup</strong>' button is a specific macro that cuts into the machine wasteboard to help you fasten the rotary with perfect parallel alignment. Check out our <a href="https://resources.sienci.com/view/vx-mounting-your-vortex/#creating-the-mounting-holes">Vortex Resources</a> for more details on how to use this wizard.

While the Y-Axis Alignment button helps in the setup of your Vortex Rotary, so does the Rotary Mounting Setup button. This feature has been designed to provide a center line for your rotary track installation. Check out our <a href="https://resources.sienci.com/view/vx-mounting-your-vortex/#creating-the-mounting-holes">Vortex Resources</a> for more details on how this wizard helps you mount your Vortex to your wasteboard.

<h4>Y-axis Alignment</h4>

When switching from regular CNC use to Rotary Mode, you will probe to align the Y axis along the A axis. You can do this in the Rotary Tab by hitting the Y axis Alignment button. Check out our <a href="https://resources.sienci.com/view/vx-first-project/#y-axis-alignment">Vortex Resources</a> for more information on aligning your Y-axis when setting up your Vortex.

<h4>Rotary Mode Toggle</h4>

This toggle can only happen once you’ve got your rotary axis set up properly, because after switching it’ll assume you’ve changed your motor wiring to be connected to your A-axis instead of your Y-axis. Here you can toggle the Rotary Mode on and off without going into the settings.

![](/_images/_gsender/_edge/gs_edge_p16_RotaryModeTog.jpg){.aligncenter .size-medium}

When you enable Rotary Mode, several changes will happen to your tool options:

<ul>
  <li>The <strong>Y-axis Alignment</strong> and <strong>Rotary Mounting Setup</strong> buttons become grey and hidden. This is because your Y-axis will be locked in its current position at this time, so there is no need to align it, and your rotary should already be set up.</li>
  <li>The <strong>Stock Turning</strong> and <strong>Probe Rotary Z-Axis</strong> buttons become available</li>
</ul>

Several changes will also happen to your controls:

<ul>
  <li>The <strong>GoTo</strong> button for Y-axis and Z-axis is hidden</li>
  <li>The <strong>Zero Y-axis</strong> button is hidden</li>
  <li>It changes the ‘<strong>Goto XYO</strong>’ button to be a ‘<strong>Goto XAO</strong>’ button</li>
  <li>The <strong>Y-axis jogging</strong> buttons are hidden</li>
</ul>

![](/_images/_gsender/_edge/gs_edge_p17_JogControls2.jpg){.aligncenter .size-medium}

You will also see a reminder that:

<ul>
  <li>Your Y-Axis will be set to Zero</li>
  <li>Your hard limits have automatically been turned off</li>
  <li>Your firmware EEPROM values have been set to new values, better suited to the rotary.</li>
</ul>

With a final check to ensure that your <strong>switch is turned to rotary</strong>, click OK to finish enabling Rotary Mode.

![](/_images/_gsender/_edge/gs_edge_p18_Warning.jpg){.aligncenter .size-medium}

<h4>Rotary Probing</h4>

In a similar fashion to regular cnc machining where you set a zero position in relation to the stock you are using, we will do the same when rotary carving. Two differences are that we don’t need to enter a tool diameter and each axis will be set separately.

<h5>Setting Z axis</h5>

You can set your <strong>Z-axis</strong> to either the rotating axis center, or the surface of your stock in a similar fashion to regular CNCing. We recommend using the axis center, as that allows you to make use of the Vortex’s built in Z-axis probing functionality.

To do this, jog the cutting bit to be hovering approximately ~15mm just above the chuck. <strong>Double check that your probing wires are in place before proceeding!</strong>

![](/_images/_gsender/_edge/gs_edge_p19_SettingZ.png){.aligncenter .size-medium}

In gSender, select the rotary axis tab, then Click ‘Probe Rotary Z-axis’ and the Z-axis will begin probing automatically, setting the Z-zero point for you. This will need to be done for each tool change in addition to the beginning of each job.

![](/_images/_gsender/_edge/gs_edge_p20_ProbeZRotary.jpg){.aligncenter .size-medium}

<h5>Setting X &amp; A axis</h5>

Setting both the X-axis and the A-axis are done manually.

<ul>
  <li>To set your <strong>X-axis</strong>, jog to wherever you’d like the job to start then click ‘Zero X’ to set your X-zero point. Make sure this is far enough from the chuck to ensure there won’t be any collisions with your cutting bit, workholding or screws.</li>
  <li>To set your <strong>A-axis</strong>, simply click ‘Zero A’ at the beginning of each job, under the Rotary Jog Controls. Note that if this isn’t done, the rotary will spin back to zero before the job starts.</li>
</ul>

<h4>Rotary Surfacing tool</h4>

he Rotary Surfacing button will allow you to turn square stock down to a cylinder. We recommend using a <strong>¼ inch upcut endmill</strong> for turning stock, as it's the most efficient.

![](/_images/_gsender/_edge/gs_edge_p21_RotarySurfacing.jpg){.aligncenter .size-medium}

Now you will see the Rotary Surfacing Tool. Here you will enter details about your stock length, start and final dimensions. You will also see spots for Bit Diameter, Stepover, Spindle RPM, and Feedrate.

![](/_images/_gsender/_edge/gs_edge_p22_SurfacingTool.jpg){.aligncenter .size-medium}

Rotary surfacing is similar to the regular XYZ surfacing tool. Let’s explore this a bit further.

<ol>
  <li>Your <strong>start diameter</strong> is the largest diameter on your stock. Usually this means the diagonal distance from opposite corners if you’re starting with square or rectangular stock.
  
![](/_images/_gsender/_edge/gs_edge_p23_Diameter.jpg){.aligncenter .size-medium}</li>
  
  <li>Your final diameter is determined by the short side of your stock.
  
![](/_images/_gsender/_edge/gs_edge_p24_Diameter2.jpg){.aligncenter .size-medium}

</li>
  <li>With a starting height of 90mm and a finished height of 63.5mm, we are removing 26.5mm of material. <strong>However</strong>, since we have the Z axis set at the center of the material, we will need to divide that 26.5mm in half. We are basically taking 13.25mm off of the top and the bottom. If you want a single pass, your stepdown would be 13.25mm. Dividing that by two and setting the stepdown to 6.625mm, means that we will be doing two passes. This will produce a piece of round stock with the maximum diameter possible.</li>
</ol>

<p style="text-align: center;"><strong>(Start Height - Finishing Height) / 2 = Total Stepdown for ONE pass</strong></p>

![](/_images/_gsender/_edge/gs_edge_p25_SurfacingGIF.gif){.aligncenter .size-medium}

<h4>Rotary Settings</h4>

When you click on the setting button and then select the Rotary tab, you will see the firmware configurations. Here you can enter your own settings, reset the default settings and turn Hard Limits on/off.

![](/_images/_gsender/_edge/gs_edge_p26_RotFirmware.jpg){.aligncenter .size-medium}

<h3>Job Stats and CNC Maintenance</h3>

Curious to know how many jobs you’ve completed, how many hours you’ve put on your machine or what maintenance you should be focusing on? Find this information in the “Job History &amp; Stats” section of settings. Here you will find 3 tabs; Statistics, Job Table, and Maintenance.

![](/_images/_gsender/_edge/gs_edge_p27_JobStatsGIF.gif){.aligncenter .size-medium}

<h4>Statistics</h4>

The statistics tab has a dropdown menu that allows you to select between Overall Stats, Jobs Per Com Port (each com port is a different machine), and Run Time Per Com Port. These selections will show your statistics for total, average and longest runtime along with total, completed and cancelled jobs.

<h4>Job Table</h4>

The Job Table tab provides a simplified breakdown of each job, including the file name, duration of the job, number of lines in the job, the start date/time and completion status. This chart can be filtered by hitting the column header, or expanded to show more entries.

<h4>Maintenance</h4>

In the Maintenance tab, you will see preset tasks with an hourly countdown range, to remind you when a maintenance task is due to be performed. These times pull directly from the runtime of your jobs and allow you to mark them as complete to reset the timers. Once the task is in range, the maintenance is due, once past the range, the task becomes critical to address.

You can also add your own reminders, time due range and description to this section, to really make it your own.

<h3>Tool Changing improvements</h3>

On the settings page under Tool Change you now have the option to toggle on Passthrough. This will allow M6 commands to execute if your firmware supports this option.

We’ve also brought back the Code block tool change strategy. You can enter your own macros before and after the tool change when this strategy is selected.

![](/_images/_gsender/_edge/gs_edge_p28_ToolChange.jpg){.aligncenter .size-medium}

<h3>Remote mode improvements</h3>

You can now use your camera to scan the QR code, and be taken directly to your remote interface.

![](/_images/_gsender/_edge/gs_edge_p29_QRCode.jpg){.aligncenter .size-medium}

&nbsp;

&nbsp;
