---
title: ytsb Assembling Add-ons
menu_order: 4
post_status: draft
post_excerpt: How to set up and assemble the add-ons for the LongMill CNC router which include the dust shoe, touch plate, and T-tracks.
post_date: 2024-04-30 16:59
taxonomy:
    knowledgebase_cat: lm-assembly
    knowledgebase_tag:
        - mk1
custom_fields:
    KBName: LongMill CNC
    basepress_post_icon: bp-caret-right
skip_file: no
featured_image: /_images/_longmill/_assembly/_addons/lm_addons_p1.jpg
---

<!-- wp:paragraph -->

<h2>Sienci Labs Dust Shoe</h2>


<p>To make dust collection easier for your LongMill, we spent the time to design it its very own dust shoe. <a href="https://sienci.com/product/LongMill-magnetic-dust-shoe/" target="_blank" rel="noreferrer noopener">The new Sienci Labs Magnetic Dust Shoe</a> is a great add-on for your machine that can keep dust management easy! This dust shoe is designed specifically for the LongMill and works with 1.5″, and 2″ to 2-1/8″ hoses.</p>
<p>This dust shoe is a Z-axis independent style dust shoe designed to collect dust and debris efficiently.</p>
<p>The assembly is shown after the initial reveal in the following video: [su_youtube url="https://www.youtube.com/watch?v=r_QqMye3dLo"]</p>
<!-- /wp:paragraph -->

<!-- wp:paragraph -->
<h2>Sienci Labs Touch Plate</h2>

<p>This guide will help you set up and use your Sienci Labs Touch Plate with gSender or UGS. If you have a different touch plate that's still a standard block shape these steps may help you set up yours as well.</p>
<!-- /wp:paragraph -->

<!-- wp:paragraph -->
<p><strong>Inside the package: </strong></p>
<!-- /wp:paragraph -->

<!-- wp:list {"ordered":true} -->
<ol>
<li>One touch plate</li>
<li>Red and black wire with banana plug and magnet (1.8m)</li>
</ol>
<!-- /wp:list -->

<!-- wp:paragraph -->
<h3>Step 1: Wiring and plugging in your unit</h3>
<!-- /wp:paragraph -->

<!-- wp:paragraph -->
<p>Your LongMill control board (the LongBoard) comes with a detachable two-pin screw terminal on the Probe/GND pins. With a small flat head screwdriver, start by screwing the two bare wires into this terminal. Ensure that the red and black wires are in the correct spot as in the photo.</p>
<!-- /wp:paragraph -->

<!-- wp:image -->

![](/_images/_longmill/_assembly/_addons/lm_addons_p1.jpg){.aligncenter .size-medium}
<!-- /wp:image -->

<!-- wp:paragraph -->
<p>When properly wired, the red wire will be on the Probe pin and the black wire will be on the GND pin.</p>
<!-- /wp:paragraph -->

<!-- wp:paragraph -->
<p>Next, plug the banana plug into one of the two holes on the touch plate. Ensure that it is well seated. You can pick the hole you want to use that helps keep your wires out of the way.</p>
<!-- /wp:paragraph -->

<!-- wp:paragraph -->
<p>Ensure you have an end mill firmly secured in your collet. If you are planning on doing a probe on the X and or Y axis, make sure that you have at least 15 to 20mm of your bit coming out of the collet. For other notes on end mill compatibility, please go to the end of this guide.</p>
<!-- /wp:paragraph -->

<!-- wp:paragraph -->
<p>Attach the magnet to your end mill. You can also attach it to the collet nut or another part of your router or spindle as long as you have a conductive path through your end mill.</p>
<!-- /wp:paragraph -->

<!-- wp:paragraph -->
<p>At this step, you are ready to start setting up your touch plate!</p>
<!-- /wp:paragraph -->

<!-- wp:paragraph -->
<h3>Step 2: Setting up software probing</h3>
<!-- /wp:paragraph -->

<!-- wp:paragraph -->
<p>You can choose to use gSender or UGS (UGSPlatform) to run the probe. We recommend gSender as it is easier.</p>

<p>[tabby title="gSender" open="yes"]</p>

<p>gSender comes pre-loaded with all the settings needed for our touch plate and is able probe easily in the X, Y, and Z-axis and some other combinations.</p>
<p>All probing happens in the Probe tab in the main window. Here you can select what type of probing you'd like to perform as well as select the tool you'll be using or you can type in the tool size manually.</p>
<p><!-- /wp:paragraph -->

<!-- wp:list --></p>
<ul>
<li><strong>Z</strong>: Finds the Z height only.</li>
<li><strong>XYZ</strong>: Finds the zero point on the front,left corner of your material in all axes.</li>
<li><strong>XY, X, Y</strong>: Finds the zero point in the X and/or Y directions only.</li>
</ul>

![](/_images/_longmill/_assembly/_addons/lm_addons_p2Real.png){.aligncenter .size-medium}

<p>If you have a third-party touch plate, you can press the gear icon at the top right of the window to access the settings, which will pop up a window. Go to the 'Probe' settings on the left hand side. Here you'll be able to customize your plate dimensions, the probing speed, or switch over to a Z-only probe.</p>
<p>You can also add tools here if you want the probe widget to remember your most commonly used tools.</p>

![](/_images/_longmill/_assembly/_addons/lm_addons_p3.png){.aligncenter .size-medium}

<p>[tabby title="UGS"]</p>

<p>UGS comes with a simple plugin that allows for your machine to send the commands to your machine to utilize the touch plate for finding the X, Y, and Z-axis.</p>
<!-- /wp:paragraph -->

<!-- wp:paragraph -->
<p>Start by going to the top of your screen and clicking Window -&gt; Plugin -&gt; Probe Module. You will see a new tab appear on your screen.</p>
<!-- /wp:paragraph -->

<!-- wp:image -->

![](/_images/_longmill/_assembly/_addons/lm_addons_p4.jpg){.aligncenter .size-medium}
<!-- /wp:image -->

<!-- wp:paragraph -->
<p>Next, we will change a few settings. Click on the "Settings" button on the plugin.</p>
<!-- /wp:paragraph -->

<!-- wp:list -->
<ul>
<li><strong>Units: </strong>choose between millimeters and inches. For this guide, we will be using <span style="color: #ff0000;"><em>millimeters</em></span>.</li>
<li><strong>End Mill Diameter: </strong>the diameter of the end mill you will be using. You can find this diameter based on your manufacturer's specs, or you can measure it yourself.</li>
<li><strong>Fast Find Rate: </strong>the speed the machine will move to touch off the touch plate on the first pass. Set this to <span style="color: #ff0000;"><em>150</em></span>.</li>
<li><strong>Slow Find Rate: </strong>the speed the machine will move to touch off the touch plate on the second pass. Set this to <em><span style="color: #ff0000;">25</span>.</em></li>
<li><strong>Retract Amount: </strong>how far your tool moves away from the touch plate on its first touch off. Keep this setting at <em><span style="color: #ff0000;">1</span>.</em></li>
</ul>
<!-- /wp:list -->

<!-- wp:paragraph -->
<p>Within the left side of the plugin, you'll also see a few more tabs</p>
<!-- /wp:paragraph -->

<!-- wp:list -->
<ul>
<li><strong>XYZ</strong>: Finds the origin/datum point on the corner of your material in all axes.</li>
<li><strong>XY</strong>: Finds the origin/datum point in the X and Y direction only.</li>
<li><strong>Z</strong>: Finds the Z height only.</li>
</ul>
<!-- /wp:list -->

<!-- wp:paragraph -->
<p>In these sections, makes sure that these settings are changed. If your section does not have that setting available to change, you can skip it. This means that in the <strong>X</strong><strong>YZ</strong> tab you'll enter all these settings, in the <strong>XY</strong> tab you'll only use the settings pertaining to the <strong>x and y-directions</strong>, and in the <strong>Z</strong> tab you'll only use the settings pertaining to the <strong>z-direction</strong>.</p>
<!-- /wp:paragraph -->

<!-- wp:list -->
<ul>
<li><strong>Probe X Distance:</strong> <span style="color: #ff0000;"><strong>25</strong></span></li>
<li><strong>Probe Y Distance: <span style="color: #ff0000;">25</span></strong></li>
<li><strong>Probe X Offset: <span style="color: #ff0000;">10</span></strong></li>
<li><strong>Probe Y Offset: <span style="color: #ff0000;">10</span></strong></li>
<li><strong>Probe Distance/Direction: <span style="color: #ff0000;">-15</span></strong> (make sure this value is <strong>negative</strong>)</li>
<li><strong>Touch Plate Thickness:</strong> <span style="color: #ff0000;"><strong>15</strong></span></li>
</ul>
<p>[tabbyending]</p>
<!-- /wp:list -->

<!-- wp:paragraph -->
<h3>Step 3: Putting it all to use</h3>
<!-- /wp:paragraph -->

<!-- wp:paragraph -->
<p>We're pretty much ready to go!</p>
<!-- /wp:paragraph -->

<!-- wp:paragraph -->
<p>If you want to run a probing operation, first we need to place the touch plate and set up the magnet. There needs to always be an electrical connection between the block and magnet for probing to work. gSender has a feature to check this for you, meanwhile UGS you'll need to do this manually.</p>
<ul>
<li>Make sure the magnet is attached to the collet nut of the Makita router.</li>
<li>For XYZ probing:
<ol>
<li>Place the touch plate on the front left corner of your material. Make sure that both of the inner faces of the touch plate are contacting the edges of your material.</li>
<li>Jog your machine to position the cutting tool about 10mm (½") or closer above the circular logo on the touch plate.</li>
</ol>
</li>
</ul>

![](/_images/_longmill/_assembly/_addons/lm_addons_p5.png){.aligncenter .size-medium}

<p>[tabby title="gSender" open="yes"]</p>

<p>Back in the 'Probe' tab, you can choose which axis to probe for and the diameter of the bit you're using - in this case select 'XYZ'. The bit size can be selected from the drop-down of saved bits, or can be typed in manually. Press the 'Probe' button and you'll get a pop-up window to confirm you've positioned your bit correctly and you'll be prompted to check for a good connection.</p>

![](/_images/_longmill/_assembly/_addons/lm_addons_p2Real.png){.aligncenter .size-medium}

<p>You can either bring the touch plate to the end mill or touch the banana plug and magnet together. Make contact a few times just to confirm there is conductivity, as the red circle should flicker to green and a blue 'Start Probe' button appears.</p>

![](/_images/_longmill/_assembly/_addons/lm_addons_p6_ProbeConfirm.png){.aligncenter .size-medium}

<p>Pressing 'Start Probe' will now make the machine move to probe three sides of the touch plate, twice on each side. There should not be any crashing or abrupt movement. Once the process is over, remove the touch plate components from the machine and then press ‘Go to XY0’. The bit should be over-top of the bottom left corner of the stock material, and pressing ‘Go to’ next to the ‘Zero Z’ should bring it to touch the materials surface.</p>
<p>If the probing was <strong>unsuccessful</strong>, then it'll be indicated by the cutting bit not returning to where you started the probe cycle or the machine will be put into an 'ALARM' state. To bring it out of the alarm state, press the pulsing 'Unlock' button in the middle of the visualizer and that will put the machine back into its 'IDLE' state. An unsuccessful probing cycle can result from an incorrectly positioned probe or starting too far outside the circular logo. Be sure to verify your setup before attempting another probing cycle.</p>
<p>[tabby title="UGS"]</p>
<p>Open up the probing window in UGS and in the XYZ tab press "Measure outside corner". The LongMill will go through a cycle to probe and take its measurements.</p>
<p>If the probing function is successful, then the machine should return the bit back to the starting point where you initiated the probing cycle. You should notice that the digital readout (DRO) on UGSPlatform changes to reflect the measurements, the current position being offset a little in the X and Y and quite a bit offset in the Z.</p>
<p>You can check that it's now zeroed on the material corner by first taking the touch plate off the material and removing the magnet from the router collet before pressing "Return to Zero".</p>
<p>If the probing was <strong>unsuccessful</strong>, then it'll be indicated by the cutting bit not returning to where you started the probe cycle or the machine will be put into an 'ALARM' state. To bring it out of the alarm state, press the "Soft Reset" button followed by the "Unlock" button and that will put the machine back into its 'IDLE' state. An unsuccessful probing cycle can result from an incorrectly positioned probe, the magnet not attached to the collet properly, starting too far outside the circular logo, and the probe not being plugged into the controller. Be sure to verify your setup before attempting another probing cycle.</p>

![](/_images/_longmill/_assembly/_addons/lm_addons_p7_USGAlarm.png){.aligncenter .size-medium}

<p><!-- /wp:list -->

<!-- wp:paragraph --></p>
<p>[tabbyending]</p>
<p>If everything went according to plan, you should now see your bit hovering at the material corner like this:</p>

![](/_images/_longmill/_assembly/_addons/lm_addons_p8_Corner.png){.aligncenter .size-medium}

<p>Remove your magnet and set your touch plate aside, and you're done!</p>

<p>Here are some other options you can use when probing:</p>
<ul>
<li>For just finding the top of your material (Z):
<ol>
<li>Flip your touch plate upside down and place it on top of the material that you want to find the top of.</li>
<li>Position the cutting tool so that it's above the indented part of the touch plate.</li>
</ol>
</li>
<li>For XY probing:
<ol>
<li>Place the touch plate on the front left corner of your material. Make sure that both of the inner faces of the touch plate are contacting the edges of your material.</li>
<li>Jog your machine to position the cutting tool at the outer corner of the plate, lowered down from its top surface.</li>
</ol>
</li>
<li>For X and Y probing:
<ol>
<li>Place the touch plate on the front left corner of your material. Make sure that both of the inner faces of the touch plate are contacting the edges of your material.</li>
<li>Jog your machine to position the cutting tool away from the X or Y face.</li>
</ol>
</li>
</ul>

![](/_images/_longmill/_assembly/_addons/lm_addons_p9_AllProbe.png "Cutting tool positions for each probe type"){.aligncenter .size-medium}

<!-- /wp:list -->

<!-- wp:paragraph -->
<p><strong>Concluding notes:</strong></p>
<p>You may have some issues with using your touch probe if your cutting tool is:</p>
<p><!-- /wp:paragraph -->

<!-- wp:list --></p>
<ul>
<li>Irregularly shaped (v bits, dado bits) and the side of the widest point of the bit does not touch off on the side of the touch plate</li>
<li>Non-conductive</li>
<li>You've entered the incorrect plate dimensions. You can refer to our own design below or the dimensions supplied by your third-party touch plate manufacturer:</li>
</ul>
<!-- /wp:paragraph -->

<!-- wp:image -->

![](/_images/_longmill/_assembly/_addons/lm_addons_p10_Layout.jpg){.aligncenter .size-medium}
<!-- /wp:image -->

<!-- wp:paragraph -->
<h2>Sienci Labs AutoZero Touch Plate</h2>
<p>The AutoZero Touch Plate is specifically designed for use with the latest version of <a href="https://sienci.com/gSender/">gSender</a>. Please download the latest program first.</p>
<p>https://www.youtube.com/watch?v=H_fYFjtFc3Q</p>

<h3><b>Step 1: Unwrapping and setting up your touch plate</b></h3>

<p><span style="font-weight: 400;">Each order for the AutoZero Touch Plate comes with the block itself, a cable that has a magnet on one end and an ECS5/banana plug on the other. </span></p>
<p><span style="font-weight: 400;">All LongBoards come with 3.81mm pluggable screw terminals that can be removed from the controller to wire the cable. You will want to remove the plug from the “Probe/GND” input on the controller.</span></p>
<p><span style="font-weight: 400;">Use a small screwdriver to loosen the screw terminal to wire the cable with the red and black wires as shown. </span></p>

<h3><b>Step 2: Update your gSender settings</b></h3>

<p><span style="font-weight: 400;">Settings for the AutoZero touch plate is built into the latest version of gSender. You can activate the AutoZero in the settings menu by clicking on the gear icon at the upper right side of the interface.</span></p>

![](/_images/_longmill/_assembly/_addons/lm_addons_p11_Settings.png){.aligncenter .size-medium}

<p><span style="font-weight: 400;">In the settings, go to “Probe” settings and change the touchplate type to “Auto Zero Touchplate'' in the dropdown menu. We recommend leaving the “Probe Connectivity Test” option activated as well.</span></p>

![](/_images/_longmill/_assembly/_addons/lm_addons_p12.png){.aligncenter .size-medium}

<p><span style="font-weight: 400;">Closing the settings menu will save your changes. Your interface will update at the bottom right side of the screen to show the new probe interface.</span></p>

![](/_images/_longmill/_assembly/_addons/lm_addons_p13.png){.aligncenter .size-medium}

<h3>Step 3: Setting up the touch plate on your workpiece</h3>

<p>The AutoZero can find the X, Y, and Z coordinates on rectangular pieces of material. <strong>The material should be square and flat to get the best reading.</strong> The AutoZero can also find the Z-height of most flat materials as well regardless of their shape.</p>
<p>Start off by plugging the green pluggable terminal into the controller. Make sure that it is in the PROBE/GND terminal. </p>
<p>Next, plug the banana plug into the touch plate. There are two holes, either of which can be used to your preference. </p>
<p>For using to find the X, Y, and Z coordinates, you will need to set the block at the bottom left corner of your material. The inside edge of the bottom of the touch plate should be touching against the sides of the material. </p>
<p>If you are probing just the Z-axis, you flip over your touch plate and place it on the surface of the material.</p>

<h3>Step 4: Probing</h3>

<p>The AutoZero can probe in all three axis. The type of probing can be selected with one of the five options on the interface. The selection determines which axis the machine will be probing for and which coordinates it will reset once the probing cycle is complete. </p>

![](/_images/_longmill/_assembly/_addons/lm_addons_p14.png){.aligncenter .size-medium}

<p>Before you begin, make sure that both the touch plate is connected and the magnet is connected to the end mill or a nearby conductive surface such as the shank of the router or the router nut. gSender will ask to check for the continuity of the plate before starting the process to ensure your probe has the proper connection by asking you to touch the plate to your bit.</p>

![](/_images/_longmill/_assembly/_addons/lm_addons_p15.png){.aligncenter .size-medium .nar}

<p><strong>For the "Z" Axis </strong><strong>probe, </strong>the machine will move down and touch off the block to find the offset distance based on the touch plate's thickness. Set the end mill above the back lip of the touch plate which is designed for doing Z probes.

![](/_images/_longmill/_assembly/_addons/lm_addons_p16.png){.aligncenter .size-medium}

<p><strong>For all other probing (XYZ etc...), </strong>jog the machine over the inner square before starting the process. Your end mill should be above the square so that when the machine starts to move down, the first surface your bit touches is that square.</p>
<p>During the probing process, the touch plate may slide during the touch off process. It is recommended to keep a hand against the plate to prevent it from sliding around being careful that your hand isn't in the way of the end mill.</p>
<p>You'll also have the option for choosing which tool you're using, either "Auto" or "Tip". <strong>Auto</strong> measures the diameter on <strong>straight end mills and bits. </strong>On the other hand, <strong>Tip </strong>uses the tip of <strong>v-bits, tapered bits, and ball nose</strong> bits touching against the bottom chamfer to determine its position. Using the correct setting will ensure the most accurate probing for your bit.</p>
<p><em>Finally, </em>click on the probe to check the continuity and start the probing process.</p>

![](/_images/_longmill/_assembly/_addons/lm_addons_p17.png){.aligncenter .size-medium .nar}

<h3>Step 5: Remove magnet </h3>

<p>Once your probing is complete, remove the magnet and move the touch plate out of the way. Your machine coordinates should now be updated and ready to use.</p>
<p>We hope you have an excellent experience with the AutoZero touchplate!</p>

<h2>Installing the LongMill T-Track Set</h2>

<p>https://www.youtube.com/watch?v=T4QVgtnZMDw</p>
<p>Here is a simple T-track set up that you can mount onto your work table. This is simply a basic guideline on setting up your t-tracks, but feel free to lay them out in whatever way works best for you! 

![](/_images/_longmill/_assembly/_addons/lm_addons_p18.png){.aligncenter .size-medium}

This layout minimizes reductions in cutting area and depth, and can be prepared in advance before your machine arrives. It uses a 48”x48”x ¾” MDF sheet, which can be purchased and cut to size at home or at your local hardware store.</p>
<ol>
<li>Cut a 48” x 48” x ¾” MDF sheet into five pieces of 6” wide planks, and two pieces of 5 ½ ” wide planks.</li>
<li>Lay out the T-tracks and planks on the table, and fasten them down with wood screws. The machine will sit on top of the 5 ½” planks, as the 6” planks are arranged between them. They should be fastened with screws at least 1” in length. Leave about 1” of space between the screws and the ends of the MDF planks.</li>
<li>To ensure your planks are flat against your table, drill counterbore holes in the middle of the 5 ½” planks. You can use the LongMill or a counterboring bit to create the holes, making sure you have removed enough material to recess the screw heads and surface the MDF planks at least 1mm deep. Then fasten them down with wood screws.</li>
<li>Complete the rest of the Table Mounting process as described in the LongMill Resources page: <a href="https://resources.sienci.com/view/lm-table-mounting/" target="_blank" rel="noopener">https://resources.sienci.com/view/lm-table-mounting/</a></li>
<li>Surface the MDF planks, as described in the LongMill Resources page: <a href="https://resources.sienci.com/view/lm-surfacing-wasteboard/" target="_blank" rel="noopener">https://resources.sienci.com/view/lm-surfacing-wasteboard/</a></li>
<li>Mount your clamps onto your newly installed T-track table, and enjoy!</li>
</ol>

<h2>Assembling and Using the LongMill T-Clamps</h2>

![](/_images/_longmill/_assembly/_addons/lm_addons_p19.jpg){.aligncenter .size-medium}

T-clamps are simple yet reliable workholding tools which are used with T-tracks tables. We’ve come up with T-clamps that work for various metals, plastics and woods, holding down materials from 0.1" to 1” thick. These clamps are ideal for holding down small to medium sized pieces of material. Inside the package:</p>
<ul>
<li>x6 steel clamps</li>
<li>x6 knobs with inserts</li>
<li>x6 3D printed end caps</li>
<li>x12 hex head machine screws</li>
<li>x6 flat washers</li>
<li>x6 T-track rails</li>
<li>100 pcs wood screws</li>
</ul>
<p>How to Assemble T-Clamps:</p>
<ol>
<li>Push the plastic end cap onto the steel clamp - the end with two holes. It should have a slight wiggle but should be not easy to remove.</li>
<li>Fasten a hex bolt onto the other end of the clamp. We recommend the hex head to be facing upwards so that it easily slides into the T-tracks, but you can change it if desired.</li>
<li>Slide the other hex bolt through the clamp slot, with the hex head facing down. Bring the washer and knob from the top, so that the washer is contained between the clamp body and knob.</li>
<li>Now you can slide the downward facing hex bolt onto the t-track and locate the clamp for mounting material</li>
</ol>

![](/_images/_longmill/_assembly/_addons/lm_addons_p20.jpg){.aligncenter .size-medium}

How to Use T-Clamps on T-Track Table:
<ol>
<li>Slide the hex bolt head through the T-track, so that the entire clamp is on the table.  You may need to adjust the bolt and knob to have it fit onto the table.</li>
<li>Place your workpiece onto the table.</li>
<li>Move and adjust the clamp to push down onto the workpiece, ensuring that the end cap side of the clamp is lower than the bolt end. Tighten both bolts until snug. Position the clamps so that there is enough space for your cutting job on your workpiece.</li>
<li>Push your material to check if it is secured onto the table. If not, use more T-clamps or other workholding methods.</li>
</ol>

![](/_images/_longmill/_assembly/_addons/lm_addons_p21.png){.aligncenter .size-medium}

<h2>Regular Dust Shoe</h2>

<p>https://www.youtube.com/watch?v=j6JFbru7j3I</p>
