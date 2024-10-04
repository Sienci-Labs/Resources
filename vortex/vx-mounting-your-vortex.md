---
title: Table Setup
menu_order: 0
post_status: draft
post_excerpt: 
post_date: 2024-07-18 18:14:53
taxonomy:
    knowledgebase_cat: vx-basics vx-assembly vx-projects vx-handbook
    knowledgebase_tag:
        - vortex
custom_fields:
    KBName: Vortex
    basepress_post_icon: bp-caret-right
skip_file: yes
featured_image: _images/post-image.jpg
---

Check out our video on how to mount your Vortex!

https://www.youtube.com/watch?v=TUwrwqpvdsI

<img class="aligncenter size-medium wp-image-5683" src="https://resources.sienci.com/wp-content/uploads/2023/08/Section-Headers_Table-Mounting-1-850x532.jpg" alt="" width="850" height="532" />

We’ll use the LongMill to make its own holes for threaded inserts that will allow us to mount the track. This way, we can guarantee that the Vortex will be aligned correctly.

[gallery columns="2" size="medium" ids="5583,5582"]

<h3>Preparing Your Machine</h3>

The Vortex rotary axis requires a minimal amount of space <strong>on</strong> and <strong>above</strong> your wasteboard to function properly. So before you start putting holes into your wasteboard, let’s double check your setup and make some adjustments to maximize compatibility.

<img class="aligncenter size-medium wp-image-5706" src="https://resources.sienci.com/wp-content/uploads/2023/08/Table-Steup-Step-0-1-850x532.jpg" alt="" width="850" height="532" />

<h4>Flat Area on Your Wasteboard</h4>

The minimal flat area needed on your wasteboard is <strong>810mm x 95mm (31.9" x 3.8”)</strong> in size for the base configuration, and <strong>1270mm x 95mm (50.0" x 3.8”)</strong> with the extension.

You can easily check if the surfaced area on your machine is at least this size by placing the Vortex track on top of your wasteboard and seeing if the track ends hang outside of this area. If this is the case, you will have to resurface your wasteboard to a larger size. If you remove the end caps of the track, you will reduce the space needed by 10mm.

[caption id="attachment_5595" align="aligncenter" width="850"]<img class="wp-image-5595 size-medium" src="https://resources.sienci.com/wp-content/uploads/2023/08/6.p7_Dustbracket2-850x716.jpg" alt="" width="850" height="716" /> Here the track is outside of the surface area[/caption]

If you have a LongMill MK1 dust shoe, your surface area may be limited by the dust shoe bracket. See the section specific to the MK1 below to learn what to do.

<h4>Setups With Raised Wasteboards</h4>

The Vortex requires 150mm (5.9”) of height clearance from wasteboard to tool in order to carve a 4” diameter piece of material.

If you have an additional piece of material atop the base of your machine, this will reduce your cutting envelope to below 4” diameter and create difficulty using the Y and Z axis probing features in gSender.

If you have such a setup, we recommend that you <strong>raise the feet</strong> of your machine, or <strong>remove your wasteboard</strong>.

[gallery columns="2" ids="5591,5593"]

[su_spoiler title="<h4>Specific Instructions For the LongMill MK1</h4>" open="no" style="fancy" icon="chevron" anchor="" anchor_in_url="no" class=""]
<table>
<tbody>
<tr>
<td nowrap="nowrap"><b>Configuration</b></td>
<td><b>Issue</b></td>
<td><b>What to do to improve clearance</b></td>
<td><b>Illustration</b></td>
</tr>
<tr>
<td>Lower router mounting</td>
<td>⚠️Under 4” cutting volume
⚠️Difficulty using the probing feature in gSender to zero the Y and Z-axis.</td>
<td>Move to top router mounting
<i>Illustration shows correct position</i></td>
<td><img class="aligncenter size-full wp-image-5592" src="https://resources.sienci.com/wp-content/uploads/2023/08/6.p4_LowerMounting.jpg" alt="" width="640" height="480" /></td>
</tr>
<tr>
<td>Dust Shoe bracket </td>
<td>⚠️Under 4” cutting volume
⚠️Insufficient surfaced area on waste board to fit the track</td>
<td>To cut the full 4" volume, the dust shoe bracket will need to be removed.
Remove the bracket before re-surfacing the wasteboard and installing the threaded inserts. 
<i>Illustration shows short wasteboard due to bracket</i></td>
<td><img class="aligncenter size-full wp-image-5594" src="https://resources.sienci.com/wp-content/uploads/2023/08/6.p6_Dustbracket.jpg" alt="" width="640" height="480" /></td>
</tr>
</tbody>
</table>
[/su_spoiler]

<h3>gSender</h3>

We will be using the latest version of <a href="https://sienci.com/gsender/">gSender</a> to create your mounting holes. Simply click the link to navigate to the downloads page.

<img class="aligncenter size-medium wp-image-5719" src="https://resources.sienci.com/wp-content/uploads/2023/08/gSender-Edge-850x462.jpg" alt="" width="850" height="462" />

Once on the gSender Edge download page, select the file that matches your operating system and click to download it.

<img class="aligncenter size-medium wp-image-5718" src="https://resources.sienci.com/wp-content/uploads/2023/08/gSender-versions-850x630.jpg" alt="" width="850" height="630" />

Once downloaded and installed, navigate to Settings where you will find the Rotary tab.

<img class="aligncenter wp-image-5685 size-full" src="https://resources.sienci.com/wp-content/uploads/2023/08/gSender-gif.gif" alt="" width="1280" height="720" />

Here you can <strong>hide</strong> or <strong>display</strong> the Rotary tab on the main page.

<img class="nar aligncenter wp-image-5717 size-full" src="https://resources.sienci.com/wp-content/uploads/2023/08/Rotary-tab-master.jpg" alt="" width="588" height="364" />

With this tab you can:

<ul>
  <li><strong>Jog Control</strong> - to rotate the A-axis, go to Zero, set Zero, and adjust speeds</li>
  <li><strong>Stock Turning</strong> - Wizard to turn square stock round</li>
  <li><strong>Probe Z axis</strong> - Automatically probe to find the Z axis</li>
  <li><strong>Probe Y axis</strong> - Automatically probe to align the Y axis along the A axis</li>
  <li><strong>Track Mounting</strong> - Drill holes in your wasteboard to mount the track</li>
</ul>

As gSender Edge is our test arena for working on new and exciting gSender updates, there are a couple current limitations.

In the visualizer, the stock turning tool is missing the helical toolpaths. You will see the image on the left, but rest assured, the toolpath is following the image on the right.

[gallery columns="2" size="medium" ids="5720,5721"]

For your Workspace, you will need to select millimeters and not inches for now as well.

<img class="nar aligncenter wp-image-5716 size-medium" src="https://resources.sienci.com/wp-content/uploads/2023/08/mm-not-inches-850x593.jpg" alt="" width="850" height="593" />

<h3>Creating the Mounting Holes</h3>

<img class="aligncenter size-full wp-image-5584" src="https://resources.sienci.com/wp-content/uploads/2023/08/6.p8_Drillhole.gif" alt="" width="1276" height="714" />

Lay the mounting track (and extension track if applicable) across the wasteboard of your LongMill positioned where the track sits behind the inside edge of the front feet on your LongMill.

With this in position, check to see if there are any interferences between any T-tracks or other workholding systems you might have, and the ‘default’ sets of holes highlighted blue in the illustration below.

<img class="aligncenter wp-image-5596 size-medium" src="https://resources.sienci.com/wp-content/uploads/2023/08/6.p9_DefaultHoles-850x290.jpg" alt="" width="850" height="290" />

If there’s no interference on your table with the default mounting hole positions, <strong>mark the center of the far bottom left hole</strong> with a pen/pencil.

<img class="aligncenter size-medium wp-image-5597" src="https://resources.sienci.com/wp-content/uploads/2023/08/6.p10_Markbottomleft-850x455.jpg" alt="" width="850" height="455" />

If you’re unable to use all the default mounting holes, <strong>mark the bottom hole for each pair of holes which do not interfere</strong> with anything on your wasteboard.

<img class="aligncenter size-medium wp-image-5598" src="https://resources.sienci.com/wp-content/uploads/2023/08/6.p11_DoesntMatch-850x489.jpg" alt="" width="850" height="489" />

With all this planning out of the way, it’s time to make some holes!

First things first, open up gSender and connect to your LongMill. A best practice when mounting the Vortex is to ensure your X-axis is square. <strong>Running your Y-axis all the way to the front or back of the machine</strong> until you hear each rail hit the end, will ensure you are square and ready to proceed.

Select the rotary axis tab on the bottom right corner of gSender, then click ‘<strong>Rotary Mounting Setup</strong>’ to open the selection window displaying each of the different track setup options.

<img class="nar aligncenter wp-image-5619" src="https://resources.sienci.com/wp-content/uploads/2023/08/Rotary-Mounting-Setup.jpg" alt="" width="450" height="263" />

Which setup you’ll choose will depend on three selections:
<ul>
  <li>Does the mounting track lineup?</li>
  <li>Are you using a ¼” or ⅛” diameter end mill ? (<em>Make sure the router is mounted as far down as possible with the bit inserted not too far into the collet <strong>if using a ⅛ bit</strong>, to prevent your Z gantry from bottoming out.</em>)</li>
  <li>Do you have the extension?</li>
</ul>
<img class="aligncenter wp-image-5600 size-medium" src="https://resources.sienci.com/wp-content/uploads/2023/08/6.p13_DefaultDrill-850x537.jpg" alt="" width="850" height="537" />

Select the buttons that match your circumstances, and hit the Send to Visualizer button.
<h4>Default Mounting</h4>
Lucky for you, If you’re able to use the default mounting holes, you’ll have a very simple procedure to follow.

<img class="aligncenter wp-image-5603 size-medium" src="https://resources.sienci.com/wp-content/uploads/2023/08/6.p16_Extension-Track-Top-View-850x204.png" alt="" width="850" height="204" />
<p style="text-align: center;"><strong> OR</strong><img class="aligncenter wp-image-5602 size-medium" src="https://resources.sienci.com/wp-content/uploads/2023/08/6.p15_Standard-Track-Top-View--850x300.png" alt="" width="850" height="300" /></p>
Simply jog your machine/cutting bit to be hovering right above the point you’ve marked previously and set your X and Y position to zero. Use any method such as touch plate, paper method, etc. to set your Z-zero position to the top of your wasteboard at this marked spot.

<img class="aligncenter size-medium wp-image-5604" src="https://resources.sienci.com/wp-content/uploads/2023/08/6.p17_HoleMarker-850x453.jpg" alt="" width="850" height="453" />

Turn on your router and run the g-code program you’ve loaded. Either 6 or 10 holes will be milled into your waste board automatically.
<h4>Custom Mounting</h4>
If you find a t-track, dog hole, threaded insert or even the screws holding down your wasteboard will interfere with the default mounting holes, you can use the custom ones. Selecting <strong>Does not lineup</strong> will generate g-code code that drills out <strong>one pair of holes at a time</strong>.

<img class="aligncenter wp-image-5605 size-medium" src="https://resources.sienci.com/wp-content/uploads/2023/08/6.p18_doesnotlineup-850x530.jpg" alt="" width="850" height="530" />

By marking each set of holes that are clear of interference with a pen, you will have a great reference point to <strong>set a new X-axis point for each set of holes you are going to drill</strong>.

For this approach, we’ll first jog our cutting bit just above the first marked hole on the bottom left most corner, then set our X, Y position to zero here. Use any method such as touch plate, paper method, etc. to set your Z-zero position to the top of your wasteboard at this marked spot.

<img class="aligncenter wp-image-5604 size-medium" src="https://resources.sienci.com/wp-content/uploads/2023/08/6.p17_HoleMarker-850x453.jpg" alt="" width="850" height="453" />

Turn on your router and run the program. You will drill out the first, then second hole.

<img class="aligncenter size-full wp-image-5585" src="https://resources.sienci.com/wp-content/uploads/2023/08/6.p20_Twoholedrillout.gif" alt="" width="356" height="200" />

Once done, turn off the router and jog your machine’s X-axis so it's centered just above the next marked hole position. <strong>Set your X position to zero</strong>, leaving your Y and Z zero position unchanged. Turn on your router then <strong>run this same g-code file again</strong>.

For every remaining set of holes to the right, continue jogging rightwards, resetting the X-zero position, and running this g-code until all sets of holes are done.

With all these holes made, we can now proceed with installing the included <strong>steel threaded inserts</strong> using either a 6mm or 7/32” allen key.

<img class="aligncenter size-medium wp-image-5607" src="https://resources.sienci.com/wp-content/uploads/2023/08/6.p21_threadedInserts-850x475.jpg" alt="" width="850" height="475" />

To mount the vortex to your table, simply lay the Vortex mounting track across your wasteboard, lining up the mounting holes with their respective threaded inserts. If you have a 48” X-axis LongMill and will be using the Vortex extension track, align this track up against the end of the regular mounting track.

<img class="aligncenter size-full wp-image-5608" src="https://resources.sienci.com/wp-content/uploads/2023/08/6.p22_Extension-track.jpg" alt="" width="640" height="231" />

Install 6 of the included 1/4-20 - ¾” flat head mounting screws into the appropriate holes of the regular mounting track, tightening these to be snug.

<em>An additional 4 screws will be used for the mounting track extension.</em>

As a last step, you’ll most likely want to loosen the screws on your router mount and <strong>slide your router upwards</strong> so it sits higher. Since most of the work we’ll be doing with the Vortex will demand that your cutting bits sit about twice as high as normal, it’s convenient and sometimes necessary to raise where your router sits inside the router mount.

<img class="aligncenter wp-image-5609 size-medium" src="https://resources.sienci.com/wp-content/uploads/2023/08/6.p23_RaiseMount-850x451.jpg" alt="" width="850" height="451" />

<strong>Well done!</strong> Now that we’re finished with assembly, you’ll find a few parts remaining unassembled. They are for you to use with your Vortex.

<img class="aligncenter size-medium wp-image-5735" src="https://resources.sienci.com/wp-content/uploads/2023/08/Operational-Tools-850x850.jpg" alt="" width="850" height="850" />
