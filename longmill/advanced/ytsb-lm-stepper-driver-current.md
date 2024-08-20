---
title: ytsb Adjusting Stepper Driver Current
menu_order: 4
post_status: draft
post_excerpt: This guide is for the LongMill Benchtop CNC. Adjust the current going to the motors on the Longboard control board, through the potentiometers on the drivers.
post_date: 2024-04-30 17:31
taxonomy:
    knowledgebase_cat: lm-advanced
    knowledgebase_tag:
        - mk1
custom_fields:
    KBName: LongMill CNC
    basepress_post_icon: bp-caret-right
skip_file: no
featured_image: /_images/_longmill/_advanced/lm_current_p1.jpg
---
You can adjust the current on each axis of the LongMill. It is set to 2.2A by default. At this configuration, the LongMill has a max current draw of 8.8A (4 drivers x 2.2A) to match with the max current output of 10A from the default power supply.

Some users may choose to increase or decrease their current settings to change the torque and speed characteristics. If you choose to adjust the default current settings, please do thorough research on the impact of current and motor performance before making changes.
<h2>Warnings</h2>
Adjusting the maximum current settings on your machine can impact the performance of your machine, and incorrectly changing the current settings may cause damage. If you choose to adjust the current settings, you do it at your own risk and may void your warranty.

Increasing the maximum current settings can impact your machine in these ways:
<ul>
  <li>Cause drivers and motors to overheat and break</li>
  <li>Increase power draw from the DC power supply and cause damage</li>
  <li>Affect the longevity of the machine and its components</li>
</ul>
If you do choose to adjust these settings, we recommend:
<ul>
  <li>Upgrading your power supply</li>
  <li>Using higher-powered motors</li>
  <li>Use active cooling for your drivers</li>
</ul>
<h2>Adjusting the current</h2>
Adjusting the current on each driver is easy. You can find the potentiometer with the markings on the driver itself. Depending on your control box design, you may have to remove the outer casing.

![](/_images/_longmill/_advanced/lm_current_p1.jpg){.aligncenter .size-medium}

To adjust the current, simply use a small screwdriver to turn the potentiometer to the current setting you want. The two small notches on the head of the potentiometer help indicate the position. In this photo, you can see that the current is set to 2.2A since the slot between the two notches is pointed to 2.2(A) printed on the PCB.

<a href="https://resources.sienci.com/wp-content/uploads/2022/03/Stepper-Driver-Current-Adjustment.pdf" target="_blank" rel="noopener">Download the instructions here.</a>

The LongBoard allows for a max current setting of 4.5A.
