---
title: Troubleshooting
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

This page serves as a reference in the event that something goes wrong with your rotary axis either during assembly, setup, or use. If you can’t find what you’re looking for on this page, or don’t find any of the solutions useful for your issue, please feel free to get in touch with us.

For any issues relating to your LongMill, such as general issues while running jobs, connecting to your machine, or the motion of the X, Y, and Z axes, please reference our <a href="https://resources.sienci.com/view/lmk2-issues-and-fixes/">CNC Issues &amp; Fixes</a> page instead.

<h2>Pulley is Slipping</h2>

It’s likely that the belt joining the Vortex motor and chuck pulleys was slightly under-tensioned when assembled, or became loose over time.

Remove the headstock from the mounting track by unscrewing the four screws at the bottom. Next, remove the 3D printed front lower headstock cover from the headstock to expose the four mounting screws at the front. Slightly loosen each of these screws, then apply a reasonable amount of pressure downwards onto the motor. While holding this pressure on the motor, re-tighten these four screws at the front of the headstock. Like shown in the photo below.

<img class="nar aligncenter wp-image-5861 size-medium" src="https://resources.sienci.com/wp-content/uploads/2023/08/9.p16_Belt-Tensioning-850x531.jpg" alt="" width="850" height="531" />

Re-assemble the rest of the components in reverse order. Ensure that the pulley can still rotate freely without any binding or resistance.

If you’ve checked that the belt on your headstock is fully tightened and not allowing for any slop in the chuck’s rotation, you may be cutting too aggressively and causing the motor to skip. This is especially more likely when cutting very large diameter stock (such as 2”+) since cutting forces from the bit will create much more torque applied to the router. You’ll likely want to reference our recommended feeds and speeds chart found <a href="https://resources.sienci.com/view/lmk2-feeds-and-speeds/">here</a>, as well as read about how feeds and speeds are affected by the rotary axis work <a href="https://docs.google.com/document/d/1RF5jf80w3Yz1kDkBp57oEkEwA6wZn1wLWwsUkLjg2Vg/edit?pli=1#heading=h.lmy47gotwdcj">here</a>.

<h2>Backlash in the Headstock</h2>

If it seems like the chuck can be spun by hand freely back and forth, it’s likely that one of the set screws within the motor or headstock shaft pulley have come loose.

To check this, remove the two screws holding the rear cover of the headstock in place, then remove the four screws holding the motor onto the back of the headstock. Remove both the cover and motor from the head stock, then slip the belt off of the two pulleys. Check the fitment of the two pulleys onto their respective shafts and try turning each by hand to check for looseness.

If a pulley seems loose, identify the small set screw which sits closest to the flat portion of its respective shaft, then tighten this so that the screw bottoms out onto the shaft and there is no more play in the pulley. Tighten the second screw as well.

<h2>Chuck & Stock Wobbly</h2>

A wobbling chuck (and stock being held) indicates that the chuck back plate was not installed fully seated. Remove the three screws at the back of the chuck, then check the tightness of the three screws mounting this plate onto the headstock shaft. If you can see any small gaps between these two components, tighten down these three screws to continue pulling the two into alignment.

<h2>Tailstock is Not Parallel</h2>

If you notice when cutting with the Vortex that certain sections of your carved model have curved lines (when they should be straight), and certain sections seem warped, it’s possible that your moving X-axis is not aligned parallel perfectly to the Vortex’s rotary axis.

This can happen for one of two reasons and can be resolved as follows:

<ul>
  <li>The Vortex’s mounting track holes in the wasteboard have threaded inserts that are not fully seated, therefore the mounting track is not perfectly square with the machine.
<ul>
  <li>Run the hole mounting program again, making sure to run both the Y-axis gantries all the way to the front or back of the machine in order to align the X-axis before running this program and ensure your threaded inserts are fully seated and level.</li>
</ul>
</li>
  <li>The X-axis rail is not squared, due to one of the left or right Y-gantries becoming out of sync with the other.
<ul>
  <li>Running the machine all the way to the rear of the machine (or front) until both Y-axis motors skip will cause the align the X-axis rail to realign itself.</li>
</ul>
</li>
</ul>

<h2>Rotation is Incorrect</h2>

If your vortex is rotating an unexpected distance when using the SuperLongBoard and gSender 1.4.7, there is a bug that isn't changing the values correctly. Please do the following to have the correct values that will allow you to swap between rotary and normal operation. The software team is working on fixing this bug for future versions of gSender.

1. Make sure you are not in rotary mode.
  <img id="image_01af82da-116f-4438-8ff5-d5fe9979d1c9" class="image_resized" src="https://sienci.zendesk.com/attachments/token/nu0AZSh4kfFB0l6VBSqXec4bY/?name=inline-408367304.png" />
2. Click console and input or copy/paste the following exactly, <strong>​$103=79.012345679,</strong> ​then click RUN. Write this number down in case the settings have been changed back to default.
  <img id="image_3a95637d-5a71-4747-a8a9-1647c7285833" class="image_resized" src="https://sienci.zendesk.com/attachments/token/KkZFLN2Wd2IdK1CoQ9pblBODG/?name=inline1850320849.png" />​
3. Disconnect from, then reconnect to the controller.
4. Open the firmware tool and confirm the setting has been updated. It should appear as below.
  <img id="image_d2ff80ec-4cb2-45ad-b71e-92ad01c4a32f" class="image_resized" src="https://sienci.zendesk.com/attachments/token/d2oFrkn44gvf7wHNUfatgIz91/?name=inline860731854.png" />​
5. You will now be able to change between the normal and rotary mode with the Vortex rotating the correct distance.
