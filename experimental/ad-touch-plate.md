---
title: Touch Plate
menu_order: 0
post_status: draft
post_excerpt: 
post_date: 2024-09-10 10:31
taxonomy:
    knowledgebase_cat: 
    knowledgebase_tag:        
custom_fields:
    KBName: 
    basepress_post_icon: bp-caret-right
skip_file: yes
featured_image: 
---

Improves on https://resources.sienci.com/view/lmk2-touch-plate/

- How each is used could be explained better
- Should ideally be rewritten to show wiring as its own section
- Mention why touch plate has two holes "Whichever is easier for your setup we just need wanted to give people the flexibility"
- Show setting up either touch plate in software
- Request for video resource “idiots guide” to setting up the AutoZero and standard touch plates and using them in gSender https://www.facebook.com/groups/mill.one/permalink/1789573318180658/

---

Setting up any style of touch plate on your LongMill MK2 is easy. Since it only requires a ‘closed’ connection between two wires you can use all sorts of plate designs from a thin metal sheet to a more common block style to probing off the material itself if it’s conductive. Once wired, the last step is to check that your g-code sender understands the shape of your touch plate and how you plan to use it.
All the touch plates that we provide have instructions below and are fully supported by gSender as well as have some support for other popular senders like UGS, CNCjs, and others.

## Standard Block Style Plate

This guide covers set up and use of our Standard Touch Plate. If you have a different or custom touch plate that’s a block shape these steps can also be applied for software setup and usage.

**Inside our package:**

- Block style touch plate
- Wire harness with banana plug and magnet (~1.8m)

### Wiring

Our touch plates come mostly pre-wired but sometimes a green connector will need to be attached. If your wire harness doesn’t have a green connector attached already, look for it to be plugged into the Probe and GND pin pair on your LongMill control board. These terminal connectors have a built-in clamping system that you can open and close by turning the flat head screw at the top of each connection point.

<img class="wp-image-3654 size-medium aligncenter" src="https://resources.sienci.com/wp-content/uploads/2022/03/Block-style-assembly-1-850x366.png" alt="" width="850" height="366" />

Use a flat head screwdriver to clamp down on the exposed wire ends from the harness ensuring the red and black wires are in the correct order as in the photo. You can check for a reliable connection by giving the wires a small tug and they’ll feel firmly clamped in place. Plug the connector back into the board once finished.

<img class="size-medium wp-image-3655 aligncenter" src="https://resources.sienci.com/wp-content/uploads/2022/03/Block-style-assembly-2-850x366.png" alt="" width="850" height="366" />

At the other end of the wiring harness will be a magnet and a banana plug. The touch plate has two different holes to insert the banana plug so you can choose the hole that keeps wiring tidy for your setup. Make sure you push it in all the way; the connection should feel snug.

### Software Configuration

With wiring complete, let’s move on to setting up your g-code sender to work with the touch plate. gSender and UGS (UGSPlatform) are easiest to configure for this style probe so we’ll show setup below for both.

[tabby title="gSender" open="yes"]

gSender comes pre-loaded with all the settings needed for our touch plate and is able probe easily in the X, Y, and Z-axis and some other combinations.

All probing happens in the Probe tab in the main window. Here you can select what type of probing you'd like to perform as well as select the tool you'll be using or you can type in the tool size manually.

- **Z**: Finds the Z height only.
- **XYZ**: Finds the zero point on the front, left corner of your material in all axes.
- **XY, X, Y**: Finds the zero point in the X and/or Y directions only.

<figure class="wp-block-image size-full"><img class="aligncenter size-medium wp-image-9352" src="https://resources.sienci.com/wp-content/uploads/2024/08/lm_addons_p2Real.png" alt="" /></figure>
If you have a third-party touch plate, you can press the gear icon at the top right of the window to access the settings, which will pop up a window. Go to the 'Probe' settings on the left hand side. Here you'll be able to customize your plate dimensions, the probing speed, or switch over to a Z-only probe.

You can also add tools here if you want the probe widget to remember your most commonly used tools.

<figure class="wp-block-image size-full"><img class="aligncenter size-medium wp-image-9353" src="https://resources.sienci.com/wp-content/uploads/2024/08/lm_addons_p3.png" alt="" /></figure>

[tabby title="UGS"]

UGS comes with a simple plugin that allows for your machine to send the commands to your machine to utilize the touch plate for finding the X, Y, and Z-axis.

Start by going to the top of your screen and clicking Window -&gt; Plugin -&gt; Probe Module. You will see a new tab appear on your screen.

<img class="size-medium wp-image-1309 aligncenter" src="https://resources.sienci.com/wp-content/uploads/2021/05/UNADJUSTEDNONRAW_thumb_2-850x502.jpg" alt="" width="850" height="502" />

Next, we will change a few settings. Click on the "Settings" button on the plugin.

<ul>
  <li><b>Units:</b> choose between millimeters and inches. For this guide, we will be using <span style="color: #ff0000;"><em>millimeters</em></span>.</li>
  <li><b>End Mill Diameter:</b> the diameter of the end mill you will be using. You can find this diameter based on your manufacturer's specs, or you can measure it yourself.</li>
  <li><b>Fast Find Rate: </b>the speed the machine will move to touch off the touch plate on the first pass. Set this to <span style="color: #ff0000;"><em>150</em></span>.</li>
  <li><b>Slow Find Rate: </b>the speed the machine will move to touch off the touch plate on the second pass. Set this to <em><span style="color: #ff0000;">25</span>.</em></li>
  <li><b>Retract Amount: </b>how far your tool moves away from the touch plate on its first touch off. Keep this setting at <em><span style="color: #ff0000;">1</span>.</em></li>
</ul>

Within the left side of the plugin, you'll also see a few more tabs

- **XYZ**: Finds the origin/datum point on the corner of your material in all axes.
- **XY**: Finds the origin/datum point in the X and Y direction only.
- **Z**: Finds the Z height only.

In these sections, makes sure that these settings are changed. If your section does not have that setting available to change, you can skip it. This means that in the **XYZ** tab you'll enter all these settings, in the **XY** tab you'll only use the settings pertaining to the **x and y-directions**, and in the **Z** tab you'll only use the settings pertaining to the **z-direction**.

<ul>
  <li><b>Probe X Distance:</b> <span style="color: #ff0000;"><b>25</b></span></li>
  <li><b>Probe Y Distance: <span style="color: #ff0000;">25</span></b></li>
  <li><b>Probe X Offset: <span style="color: #ff0000;">10</span></b></li>
  <li><b>Probe Y Offset: <span style="color: #ff0000;">10</span></b></li>
  <li><b>Probe Distance/Direction: <span style="color: #ff0000;">-15</span></b> (make sure this value is <b>negative</b>)</li>
  <li><b>Touch Plate Thickness:</b> <span style="color: #ff0000;"><b>15</b></span></li>
</ul>

[tabbyending]

### Using your Touch Plate

We're pretty much ready to go!

If you want to run a probing operation, first we need to place the touch plate and set up the magnet. There needs to always be an electrical connection between the block and magnet for probing to work. gSender has a feature to check this for you, meanwhile UGS you'll need to do this manually.

- Make sure the magnet is attached to the collet nut of the Makita router.
- For XYZ probing:
  1. Place the touch plate on the front left corner of your material. Make sure that both of the inner faces of the touch plate are contacting the edges of your material.
  1. Jog your machine to position the cutting tool about 10mm (½") or closer above the circular logo on the touch plate.

<figure class="wp-block-image size-full"><img class="aligncenter size-medium wp-image-9355" title="1/4″ end mill positioned for an XYZ probe" src="https://resources.sienci.com/wp-content/uploads/2024/08/lm_addons_p5.png" alt="" /><figcaption class="wp-caption-text">1/4″ end mill positioned for an XYZ probe</figcaption></figure>

[tabby title="gSender" open="yes"]

Back in the 'Probe' tab, you can choose which axis to probe for and the diameter of the bit you're using - in this case select 'XYZ'. The bit size can be selected from the drop-down of saved bits, or can be typed in manually. Press the 'Probe' button and you'll get a pop-up window to confirm you've positioned your bit correctly and you'll be prompted to check for a good connection.

<figure class="wp-block-image size-full"><img class="aligncenter size-medium wp-image-9352" src="https://resources.sienci.com/wp-content/uploads/2024/08/lm_addons_p2Real.png" alt="" /></figure>

You can either bring the touch plate to the end mill or touch the banana plug and magnet together. Make contact a few times just to confirm there is conductivity, as the red circle should flicker to green and a blue 'Start Probe' button appears.

<figure class="wp-block-image size-full"><img class="aligncenter size-medium wp-image-9356" src="https://resources.sienci.com/wp-content/uploads/2024/08/lm_addons_p6_ProbeConfirm.png" alt="" /></figure>

Pressing 'Start Probe' will now make the machine move to probe three sides of the touch plate, twice on each side. There should not be any crashing or abrupt movement. Once the process is over, remove the touch plate components from the machine and then press ‘Go to XY0’. The bit should be over-top of the bottom left corner of the stock material, and pressing ‘Go to’ next to the ‘Zero Z’ should bring it to touch the materials surface.

If the probing was **unsuccessful**, then it'll be indicated by the cutting bit not returning to where you started the probe cycle or the machine will be put into an 'ALARM' state. To bring it out of the alarm state, press the pulsing 'Unlock' button in the middle of the visualizer and that will put the machine back into its 'IDLE' state. An unsuccessful probing cycle can result from an incorrectly positioned probe or starting too far outside the circular logo. Be sure to verify your setup before attempting another probing cycle.

[tabby title="UGS"]

Open up the probing window in UGS and in the XYZ tab press "Measure outside corner". The LongMill will go through a cycle to probe and take its measurements.

If the probing function is successful, then the machine should return the bit back to the starting point where you initiated the probing cycle. You should notice that the digital readout (DRO) on UGSPlatform changes to reflect the measurements, the current position being offset a little in the X and Y and quite a bit offset in the Z.

You can check that it's now zeroed on the material corner by first taking the touch plate off the material and removing the magnet from the router collet before pressing "Return to Zero".

If the probing was **unsuccessful**, then it'll be indicated by the cutting bit not returning to where you started the probe cycle or the machine will be put into an 'ALARM' state. To bring it out of the alarm state, press the "Soft Reset" button followed by the "Unlock" button and that will put the machine back into its 'IDLE' state. An unsuccessful probing cycle can result from an incorrectly positioned probe, the magnet not attached to the collet properly, starting too far outside the circular logo, and the probe not being plugged into the controller. Be sure to verify your setup before attempting another probing cycle.

<img class="size-medium wp-image-926 aligncenter" src="https://resources.sienci.com/wp-content/uploads/2021/05/UGS-Alarm-State-850x446.png" alt="" width="850" height="446" />

[tabbyending]

If everything went according to plan, you should now see your bit hovering at the material corner like this:

<figure class="wp-block-image size-full"><img class="aligncenter size-medium wp-image-9358" src="https://resources.sienci.com/wp-content/uploads/2024/08/lm_addons_p8_Corner.png" alt="" /></figure>

Remove your magnet and set your touch plate aside, and you're done!

Here are some other options you can use when probing:

- For just finding the top of your material (Z):
   1. Flip your touch plate upside down and place it on top of the material that you want to find the top of.
   1. Position the cutting tool so that it's above the indented part of the touch plate.
- For XY probing:
   1. Place the touch plate on the front left corner of your material. Make sure that both of the inner faces of the touch plate are contacting the edges of your material.
   1. Jog your machine to position the cutting tool at the outer corner of the plate, lowered down from its top surface.
- For X and Y probing:
   1. Place the touch plate on the front left corner of your material. Make sure that both of the inner faces of the touch plate are contacting the edges of your material.
   1. Jog your machine to position the cutting tool away from the X or Y face.

<figure class="wp-block-image size-full"><img class="aligncenter size-medium wp-image-9359" title="Cutting tool positions for each probe type" src="https://resources.sienci.com/wp-content/uploads/2024/08/lm_addons_p9_AllProbe.png" alt="" /><figcaption class="wp-caption-text">Cutting tool positions for each probe type</figcaption></figure>

<b>Concluding notes:</b>

You may have some issues with using your touch probe if your cutting tool is:

- Irregularly shaped (v bits, dado bits) and the side of the widest point of the bit does not touch off on the side of the touch plate
- Non-conductive
- You've entered the incorrect plate dimensions. You can refer to our own design below or the dimensions supplied by your third-party touch plate manufacturer:

<img class="size-medium wp-image-1310 aligncenter" src="https://resources.sienci.com/wp-content/uploads/2021/05/Touch-Plate-layout-dawing-850x657.jpg" alt="" width="850" height="657" />

## AutoZero Touch Plate

The AutoZero Touch Plate is specifically designed for use with the latest version of <a href="https://sienci.com/gsender/">gSender</a>. Please download the latest program first.

https://www.youtube.com/watch?v=H_fYFjtFc3Q

### Step 1: Unwrapping and setting up your touch plate

Each order for the AutoZero Touch Plate comes with:

- The AutoZero Touch Plate itself and
- A cable that has a green connector on one end and a magnet and banana plug on the other

If your cable didn't come with a green connector, you should find a spare one came with your board in a baggy or plugged into the board already (look for the writing "PRB" or "Probe"). These connectors are called 3.81mm pluggable screw terminals and can have wires attached to them using a regular, small flat head screwdriver. When you do this the wire order doesn't matter.

### Step 2: Update your gSender settings

All probing macros for the AutoZero are built into gSender making it easy to set up.

The key step is to make sure to go to gSenders settings (gear icon at the top, right of the window) ➜ go to the 'Probe' settings ➜ and change the touch plate type to “**AutoZero Touch plate**'' in the dropdown menu. If you don't do this, or at a later time you find the probing macros are moving strangely, then you should come back to check that this setting is still correct.

We recommend leaving the “Probe Connectivity Test” option activated as well. If you're not using gSender and have the AutoZero, we also <a href="#using-other-senders">provide macros for other common senders</a>.

<img class="aligncenter wp-image-2471 size-medium" src="https://resources.sienci.com/wp-content/uploads/2021/05/probe-settings-e1722976109917-850x392.png" alt="" width="850" height="392" />

Your 'Probe' tab at the bottom right side of the screen should now update to show images of the AutoZero. These tell you how you should position your bit if you'd like to perform probing for that axis.

<img class="size-full wp-image-2472 aligncenter" src="https://resources.sienci.com/wp-content/uploads/2021/05/updated-interface.png" alt="" width="512" height="303" />

### Step 3: Setting up the touch plate on your workpiece

The AutoZero can find the X, Y, and Z coordinates on rectangular pieces of material. **The material should be square and flat to get the best reading.** The AutoZero can also find the Z-height of most flat materials as well regardless of their shape.

1. Start off by plugging the green pluggable terminal into the controller. Make sure that it is in the PROBE/GND terminal.
1. Next, plug the banana plug into the touch plate. There are two holes on the plate, either of which can be used to your preference.
1. For any probing with X or Y, you'll need to set the block at the bottom left corner of your material. The inside edge of the bottom of the touch plate should be touching against the sides of the material.
1. If you are probing just the Z-axis, you can still place the probe on the corner normally or alternately flip it over and place it on the surface of the material to use the back 'tab'.

### Step 4: Probing

https://youtu.be/I1EhAPNXdzQ

The AutoZero can probe in all three axis. The type of probing can be selected with one of the five options on the interface. The selection determines which axis the machine will be probing for and which coordinates it will reset once the probing cycle is complete.

<img class="size-full wp-image-2477 aligncenter" src="https://resources.sienci.com/wp-content/uploads/2021/05/axis-options.png" alt="" width="228" height="114" />

Before you begin, make sure that both the touch plate is connected and the magnet is connected to the end mill or a nearby conductive surface such as the shank of the router or the router nut. gSender will ask to check for the continuity of the plate before starting the process to ensure your probe has the proper connection by asking you to touch the plate to your bit.

<img class="size-full wp-image-2473 aligncenter" src="https://resources.sienci.com/wp-content/uploads/2021/05/Probe-confirmation.png" alt="" width="711" height="405" />

**For the "Z" Axis probe,** the machine will move down and touch off the block to find the offset distance based on the touch plate's thickness. Set the end mill above the back lip of the touch plate which is designed for doing Z probes.

<img class="size-medium wp-image-2475 aligncenter" src="https://resources.sienci.com/wp-content/uploads/2021/05/AutoZero-Probing-views-850x612.png" alt="" width="850" height="612" />

**For all other probing (XYZ etc...),** jog the machine over the inner square before starting the process. Your end mill should be above the square so that when the machine starts to move down, the first surface your bit touches is that square.

During the probing process, the touch plate may slide during the touch off process. It is recommended to keep a hand against the plate to prevent it from sliding around being careful that your hand isn't in the way of the end mill.

You'll also have the option for choosing which tool you're using, either "Auto" or "Tip". **Auto** measures the diameter on **straight end mills and bits.** On the other hand, **Tip** uses the tip of **v-bits, tapered bits, and ball nose** bits touching against the bottom chamfer to determine its position. Using the correct setting will ensure the most accurate probing for your bit.

<em>Finally,</em> click on the probe to check the continuity and start the probing process.

<img class="size-full wp-image-2474 aligncenter" src="https://resources.sienci.com/wp-content/uploads/2021/05/probe-button.png" alt="" width="154" height="51" />

**Note:** Nearly all cutting tools have been tested to work with the AutoZero, but it's still possible to find exceptions since bits come in all shapes and sizes. Some would include:

- Large, irregularly shaped surfacing bits that can't fit inside the AutoZero for XY probing
  - Though Z probing with the plate flipped over should still work</li>
- End mills that are flat bottomed and short, or adapt from a large shaft to a smaller cutting diameter (for instance 1/8" shaft to 1/16" cutting diameter)
  - These can still work as long as the overall bit sticks out far enough (over 20mm) from the collet - it will look weird when it probes because probing in X and Y might touch the shaft instead of the cutting geometry, but as long as you're using **Auto** or you've specified the shaft diameter manually then the probing should still complete fine</li>

### Step 5: Remove magnet

Once your probing is complete, remove the magnet and move the touch plate out of the way. Your machine coordinates should now be updated and ready to use.

We hope you have an excellent experience with the AutoZero touch plate!

### Using other Senders

Due to popular demand, we’ve created and tested macros to use the AutoZero touch plate with a variety of CNC control software beyond gSender.

If the software you use is not explicitly listed here, you can also follow instructions in the section titled **"Macros for other senders"** to use the AutoZero touch plate in a semi-automatic fashion as we work on expanding support.

**Macros for CNCjs:** <a href="https://resources.sienci.com/wp-content/uploads/2022/03/AZ-Macros-cncjs.zip"><b>Download for CNCjs</b></a>

**Macros for LinuxCNC/Buildbotics:** <a href="https://resources.sienci.com/wp-content/uploads/2022/03/AZ-Macro-Buildbotics_linuxcnc.zip"><b>Download for LinuxCNC/Buildbotics</b></a>

Note: These macros were tested on the Buildbotics controller but they should also work with machines running LinuxCNC since they share identical variable / arithmetic formats.

**Macros for Universal G-code Sender:** <a href="https://resources.sienci.com/wp-content/uploads/2022/03/AZ-Macro-UGS.zip"><b>Download for UGS</b></a>

Note: The macros environment in UGS does not support arithmetic operations so probing with the X and/or Y axis using the AutoZero touch plate is a semi-automatic process. More specifically, you will need to click on the “Control Status (DRO)” panel and enter “/2” to halve the active coordinates in the X and/or Y after probing in these directions. If you have only probed either the X or the Y axis, you will only need to divide the coordinate of the axis which was probed.

<p style="text-align: center;"><img class="aligncenter wp-image-4777 size-full" src="https://resources.sienci.com/wp-content/uploads/2022/03/AZ-Coordinate-Division-UGS.gif" alt="" width="600" height="338" /><em>Example dividing the X and Y axis coordinates after probing in UGS</em></p>

**Macros for other Senders:** <a href="https://resources.sienci.com/wp-content/uploads/2022/03/AZ-All-Software.zip"><b>Download for other Senders</b></a><b>
</b>

These macros will allow you to probe with the AutoZero touch plate using any CNC control software. Having said that, probing in the X and/or Y direction is a semi-automatic process in which you will need to manually halve the measure coordinate after probing.

To do so:

1. Run the desired probing macro.
1. If the macro involves probing in the X and/or Y axis (i.e. not probing Z alone), manually divide the coordinates you see after probing by 2.
1. Enter the command `G10 L20 P0 X[divided X coordinate] Y[divided Y coordinate]` into the console substituting the coordinates in square brackets with ones manually calculated in step 2. If you have only probed either the X or the Y axis, you will only need to divide and substitute the coordinate for the axis which was probed.
1. Home X and/or Y to check if the tool is at origin

<p style="text-align: center;"><img class="aligncenter wp-image-4776 size-full" src="https://resources.sienci.com/wp-content/uploads/2022/03/AZ-Coordinate-Division-Generic.gif" alt="" width="600" height="338" /> <em>Example dividing the X and Y axis coordinates after probing in any CNC control software</em></p>

## Troubleshooting

**Is the bit supposed to dent/bite into the plate when probing?**
Most times no, but if the bit if very sharp it can sometimes leave a mark. This can be much more noticeable on the AutoZero because many touch plates have a matte finish but the AutoZero is quite polished.

**Probing operation failed**
Here are some common items to check:

1. Irregularly shaped (v bits, dado bits) and the side of the widest point of the bit does not touch off on the side of the touch plate
1. Your tool is non-conductive
1. You've entered the incorrect plate dimensions. You can refer to our own design below or the dimensions supplied by your third-party touch plate manufacturer:

If you’re using UGS:

<ul>
  <li>There is a bug that can cause the touch plate to move farther than the expected origin and plunge the bit into the work surface if you use INCHES units when jogging around. If so, before beginning the probe process ensure that you have set the jog control to MM instead of INCHES. Once probing is completed, you may switch back to INCHES and resume regular machine operation

[caption id="attachment_925" align="aligncenter" width="850"]<img class="wp-image-925 size-medium" src="https://resources.sienci.com/wp-content/uploads/2021/05/UGS-probe-inches-bug-850x405.png" alt="" width="850" height="405" /> Jog control unit setting on UGS[/caption]</li>
</ul>

If this was not the problem:

- Check that the bit you are using is not tapered and is conductive at the both its sides and end so that it can make electrical contact with the touch plate.
- Ensure the settings you use are from the touch plate page on our website (not the settings in the video): <a href="https://resources.sienci.com/view/lmk2-touch-plate/" target="_blank" rel="noopener">https://resources.sienci.com/view/lm-touch-plates/</a>
- Make sure your work coordinates match your touch plate settings (usually G54)
- Check that there's proper electrical contact from your control box through to your magnet and touch plate. An easy way to check this is to run a Z probe with the router high up in the air and manually tap the magnet to the plate while they're held in each of your hands. If the bit stops and raises slightly up then lowers down again, this should indicate some form of connectivity from the magnet and touch plate to the control box. If you tap them together again, this should conclude the probing process and no errors should appear. If you don't observe this behaviour, then you should try this test again and if it again shows an error then check the electrical connections. See if the magnet is making contact with the metal leads of the wire by unscrewing the fastener in the centre and do the same for the banana plug as well. You may need to strip more insulation off the ends of the wire to get more contact with the metal surfaces. There’s a great video showing how to deal with banana connectors assembly/disassembly <a href="https://www.youtube.com/watch?v=cH0C_g_lfXo" target="_blank" rel="noopener">here.</a>
- Check for continuity between the banana clip and the connector. If there's no continuity, test the bare end of the wire. If there is continuity, ensure the bare end of the wire is properly seated in the connector.

<img class="size-medium wp-image-4198 aligncenter" src="https://resources.sienci.com/wp-content/uploads/2022/03/Touch-Plate-banana-clip-continuity-test-850x349.jpg" alt="Electrical meter testing the continuity of between an electrical connector and a banana style clip" width="850" height="349" />

<ul>
  <li>Check for continuity between the magnet and and the connector. If not continuity, repeat the same steps above.</li>
</ul>
<img class="aligncenter size-medium wp-image-4195" src="https://resources.sienci.com/wp-content/uploads/2022/03/Touch-Plate-magnet-continuity-test-850x374.jpg" alt="Electrical meter testing the continuity of between an electrical connector and a magnet" width="850" height="374" />
<ul>
  <li>If you have good continuity with the wiring harness, make a jumper connector by placing a wire into both ends of a spare connector.</li>
</ul>
<img class="aligncenter size-medium wp-image-4196" src="https://resources.sienci.com/wp-content/uploads/2022/03/touch-plate-probe-jumper-pin-850x305.jpg" alt="Wire inserted into both side of a connector to create a jumper connector" width="850" height="305" />
<ul>
  <li>Insert the jumper connector into the controller. Open gSender, begin the probing operation. You should get the green go ahead to begin. If there is no change, the port on the controller might be the issue.</li>
</ul>
<img class="wp-image-9092 size-large aligncenter" src="https://resources.sienci.com/wp-content/uploads/2022/03/LB-and-SLB-probe-shorting_page-0001-1024x387.jpg" alt="Wire jumped connector inserted into the LongBoard and SLB controllers" width="1024" height="387" />

Replacement touch plate cables can be found here: <a href="https://sienci.com/product/touch-plate-cable/" target="_blank" rel="noopener">https://sienci.com/product/touch-plate-cable/</a>
