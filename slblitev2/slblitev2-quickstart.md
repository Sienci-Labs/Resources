---
title: Quick Start Guide
menu_order: 2
post_status: draft
post_excerpt: How to use your SLB-LITE / SLB-EXT V2 
post_date: 2024-04-03 16:44:00
taxonomy:
    knowledgebase_cat: slblitev2-handbook
    knowledgebase_tag:
        - slblitev2
custom_fields:
    KBName: SLB-LITE / SLB-EXT V2
    basepress_post_icon: bp-caret-right
skip_file: no
featured_image: _images/_superlongboard/slb_slb-leds.jpg
---

## Welcome!

Welcome to your **SLB-LITE/SLB-EXT V2** knowledge base! This is where we provide more in-depth information about setting up and using your controller. If you have a Sienci Labs machine, we recommend setting up with the machine assembly instructions first, then come back here for further learning. Otherwise if you have a third-party CNC, refer to the [Quick Start Guide](#quick-start-guide).

### Background

The **SLB-LITE/SLB-EXT V2** are the next evolution of SLB controllers. These were designed in-house, from the ground up, using architecture and principles that have proven to be reliable in the original SLB platform. 

[if we have a product shot of the SLB-LITE with white back ground that would be nice to have here]

While designing these new controllers, we prioritized the “beginner user’s first experience”, and worked towards the following goals:
- Simplify the connectors and make them more robust and accessible
    - With 1st gen controllers, the motor signal wires came loose, so we have replaced these connectors on the controller for more durability
- Reduced I/O complexity to avoid misuse or confusion
    - ‘Spindle’ outputs are now unified into one connector that can do both RS485 control and PWM control
    - With 1st gen controllers, it was common for users to plug the spindle cable into the pendant port. The presence of extra I/O is enough to confuse beginner users 
- Simplify the features available for beginners without removing them entirely for advanced users
    - E-stop button replaced by integrated button on the board, but provided an option to connect a separate E-stop 
    - Aux outputs are not on the main board, but can be added with the expansion board, allowing advanced users to install more accessories  
    - Moved ethernet to the expansion board, focusing on USB connection as the main way to connect

With all that said, we hope you have a great experience using our controllers.

## Quick Start Guide

Hello! If you made it here it means that you either upgraded from a 1st generation controller (SLB/SLB-EXT), or this is your first time with one of our controllers. 

This guide will take you through the basics of setting up your controller, and what to expect. It should take about 1 hour. For more detailed information about your controller, head to the Technical Manual on the next page.
Mounting
Regardless of what controller or machine you have, you can use the four (4) slots on the enclosure to attach it onto a surface.


![](/_images/_slblitev2/slblitev2_qsg-mount.jpg){.aligncenter .size-medium}

![](/_images/_slblitev2/slblitev2_qsg-lmmount.jpg){.aligncenter .size-medium}

![](/_images/_slblitev2/slblitev2_qsg-ps.JPG){.aligncenter .size-medium}

![](/_images/_slblitev2/slblitev2_qsg-ammount.jpg){.aligncenter .size-medium}

![](/_images/_slblitev2/slblitev2_qsg-axislabel.jpg){.aligncenter .size-medium}

![](/_images/_slblitev2/slblitev2_qsg-motorconnect.JPG){.aligncenter .size-medium}

![](/_images/_slblitev2/slblitev2_qsg-pliers.JPG){.aligncenter .size-medium}

![](/_images/_slblitev2/slblitev2_qsg-autospincable.jpg){.aligncenter .size-medium}

![](/_images/_slblitev2/slblitev2_qsg-usbspin.JPG){.aligncenter .size-medium}

![](/_images/_slblitev2/slblitev2_qsg-spinconnect.JPG){.aligncenter .size-medium}

![](/_images/_slblitev2/slblitev2_qsg-gsenderconnect.jpg){.aligncenter .size-medium}

![](/_images/_slblitev2/slblitev2_qsg-estoplight.gif){.aligncenter .size-full}

![](/_images/_slblitev2/slblitev2_qsg-alarmidle.jpg){.aligncenter .size-medium}

![](/_images/_slblitev2/slblitev2_qsg-profile.jpg){.aligncenter .size-medium}

![](/_images/_slblitev2/slblitev2_qsg-confirmdefault.jpg){.aligncenter .size-medium}

![](/_images/_slblitev2/slblitev2_qsg-offon.gif){.aligncenter .size-full}

![](/_images/_slblitev2/slblitev2_qsg-alarmhome.jpg){.aligncenter .size-medium}

![](/_images/_slblitev2/slblitev2_qsg-homing.gif){.aligncenter .size-full}

![](/_images/_slblitev2/slblitev2_qsg-jogging.gif){.aligncenter .size-full}

![](/_images/_slblitev2/slblitev2_qsg-zero.jpg){.aligncenter .size-medium}

![](/_images/_slblitev2/slblitev2_qsg-prbelight.gif){.aligncenter .size-full}
