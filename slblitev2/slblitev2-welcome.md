---
title: Welcome
menu_order: 1
post_status: publish
post_excerpt: General information about the SLB-LITE and SLB-EXT V2 
post_date: 2026-10-20 16:44:00
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
# Welcome!

Welcome to your **SLB-LITE/SLB-EXT V2** knowledge base! This is where we provide more in-depth information about setting up and using your controller. If you have a Sienci Labs machine, we recommend setting up with the machine assembly instructions first, then come back here for further learning. Otherwise if you have a third-party CNC, refer to the [Quick Start Guide](#quick-start-guide).

## Background

The **SLB-LITE/SLB-EXT V2** are the next evolution of SLB controllers. These were designed in-house, from the ground up, using architecture and principles that have proven to be reliable in the original SLB platform. 

![](/_images/_slblitev2/slblitev2_techmanual-slblite-hero.jpg){.aligncenter .size-medium}

While designing these new controllers, we prioritized the “beginner user’s first experience”, and worked towards the following goals:
- Simplify the connectors and make them more robust and accessible
    - With 1st gen controllers, the motor signal wires came loose, so we have replaced these connectors on the controller for more durability
- Reduced I/O complexity to avoid misuse or confusion
    - *Spindle* outputs are now unified into one connector that can do both RS485 control and PWM control
    - With 1st gen controllers, it was common for users to plug the spindle cable into the pendant port. The presence of extra I/O is enough to confuse beginner users 
- Simplify the features available for beginners without removing them entirely for advanced users
    - E-stop button replaced by integrated button on the board, but provided an option to connect a separate E-stop 
    - Aux outputs are not on the main board, but can be added with the expansion board, allowing advanced users to install more accessories  
    - Moved ethernet to the expansion board, focusing on USB connection as the main way to connect

With all that said, we hope you have a great experience using our controllers.


