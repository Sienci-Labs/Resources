---
title: ytsb gSender Settings
menu_order: 10
post_status: draft
post_excerpt: To enable the LaserBeam on gSender, first determine which controller you have. Then follow the instructions below for your specific controller. Set Up for LongBoard Set Up for SLB or SLB-EXT.
post_date: 2024-09-13 14:30:20
taxonomy:
    knowledgebase_cat: lb-assembly
    knowledgebase_tag:
        - laser
custom_fields:
    KBName: LaserBeam
    basepress_post_icon: bp-caret-right
skip_file: yes
featured_image: 
---

To enable the LaserBeam on gSender, first determine which controller you have. Then follow the instructions below for your specific controller.
<h3>Set Up for LongBoard</h3>
[su_spoiler title="<b>LongBoard:</b>" open="no" style="fancy" icon="chevron" anchor_in_url="yes"]

On gSender, connect to your machine.

Click the gray bar at the bottom labelled "Firmware." Then click on <strong>Grbl.</strong>

<img class="alignnone size-full wp-image-11668" src="https://resources.sienci.com/wp-content/uploads/2024/09/Recognized-device-grbl.png" alt="" width="960" height="540" />

Hover over the top of the menu. Under "Recognized Devices" there should be only one option that says <strong>use grbl at 115200 baud,</strong> so let's select that.

<img class="size-full wp-image-11669 aligncenter" src="https://resources.sienci.com/wp-content/uploads/2024/09/grbl-selected.png" alt="" width="960" height="540" />

Next we will go to the gear icon to check the locally stored settings. Navigate to "Laser/Spindle." Then <strong>toggle Spindle/Laser. </strong>

[caption id="attachment_9031" align="aligncenter" width="960"]<img class="size-full wp-image-9031" src="https://resources.sienci.com/wp-content/uploads/2024/08/SpindleLaser-toggle-.png" alt="" width="960" height="540" /> Toggling Spindle/Laser[/caption]

Make sure that under "Laser Power" settings, <strong>Min Power = 0</strong> and <strong>Max Power = 255.</strong> Then exit the window.

<img class="aligncenter wp-image-11671" src="https://resources.sienci.com/wp-content/uploads/2024/09/laser-power-settings--e1730755676406.png" alt="" width="679" height="381" />

To check that the laser is set up properly, use the console to see that $30 and $31 are being changed to the correct values each time you <strong>toggle to Laser Mode. </strong>

<img class="alignnone wp-image-12050 size-full" src="https://resources.sienci.com/wp-content/uploads/2024/09/console-grbl-lasermode-1.png" alt="" width="960" height="540" />

[/su_spoiler]
<h3>Set Up for SLB or SLB-EXT</h3>
[su_spoiler title="SLB or SLB-EXT<b>:</b>" open="no" style="fancy" icon="chevron" anchor_in_url="yes"]

On gSender, connect to your machine.

Click the gray bar at the bottom labelled "Firmware." Then click on <strong><b>grblHAL.</b></strong>

<img class="wp-image-7150 aligncenter" src="https://resources.sienci.com/wp-content/uploads/2022/03/gSender-Connect-3.png" alt="" width="575" height="432" />

Hover over the top of the menu. Under "Recognized Devices" there should be only one option that says use <strong>grblHAL at 115200 baud</strong>, so let's select that.

<img class="size-full wp-image-10404 aligncenter" src="https://resources.sienci.com/wp-content/uploads/2024/08/slb_up_p21_Connect4.jpg" alt="" width="386" height="496" />

Once you have connected, we will go to the gear icon. Navigate to "Laser/Spindle." Then <strong>toggle Spindle/Laser. </strong>

<img src="https://resources.sienci.com/wp-content/uploads/2024/08/SpindleLaser-toggle-.png" />

Exit the window. Then press "Firmware" on the top bar.

<img class="wp-image-10799 aligncenter" src="https://resources.sienci.com/wp-content/uploads/2021/12/firmware-laser.png" alt="" width="713" height="401" />

In the Firmware Tool box, make sure the following settings are correctly selected.

Make sure <strong>$30 = 24000</strong>, <strong>$31 = 7200 or 7500</strong> and that <strong>$32 is set to Normal.</strong> These are usually the default settings that come with the SLB/SLB-EXT.

<img class="alignnone size-full wp-image-11806" src="https://resources.sienci.com/wp-content/uploads/2024/09/default-spindle-settings.png" alt="" width="960" height="540" />

Find <b>$395</b> and check that<b> "SLB_SPINDLE"</b> is selected. If you are using the <strong>Sienci Labs Spindle</strong>, select <b>"H-100"</b> instead.

<img class="alignnone wp-image-10793 aligncenter" src="https://resources.sienci.com/wp-content/uploads/2021/12/default-spindle-e1726691433494.png" alt="" width="719" height="282" />Then, go to<b> $511</b> and check that "<b>SLB_LASER"</b> is selected.

<img class="wp-image-10788 aligncenter" src="https://resources.sienci.com/wp-content/uploads/2021/12/511-spindle-1-e1726691389397.png" alt="" width="710" height="244" />

Scroll down further and check that <strong>$730 = 255 and $731 = 0. </strong>

<img class="wp-image-10824 aligncenter" src="https://resources.sienci.com/wp-content/uploads/2021/12/min-and-max-laser-power-slb.png" alt="" width="706" height="397" />

Save these settings by pressing <b>"Apply New Settings."</b> Then<b>, turn off and on the control board</b> to make sure these settings are enabled.

<img class="size-full wp-image-10826 aligncenter" src="https://resources.sienci.com/wp-content/uploads/2021/12/power-cycle-laser.png" alt="" width="960" height="540" />

[/su_spoiler]
