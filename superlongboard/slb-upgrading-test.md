---
title: Upgrading to SLB Test
menu_order: 4
post_status: draft
post_excerpt: Time to power up! Steps on how to upgrade your LongMill CNC or other CNC machine from your old control system to the SuperLongBoard.
post_date: 2024-03-22 13:28:53
taxonomy:
    knowledgebase_cat: slb-handbook
    knowledgebase_tag:
        - slb
custom_fields:
    KBName: SuperLongBoard
    basepress_post_icon: bp-caret-right
skip_file: no
featured_image: _images/_superlongboard/LB2SLB_pone.jpg
---

Congrats on upgrading to our newest and most powerful CNC controller to date, the <b>SuperLongBoard</b>!

Our main goal in this section is to have you go in with a working CNC, then leave with an <b>SLB-boosted machine</b> without skipping a beat. This guide will be mostly written with LongMill owners in mind who have the older LongBoard (<b>LB, pictured on the left</b>) that they’ll be swapping out for the SuperLongBoard (<b>SLB, on the right</b>), though there will be minimal differences for other CNC owners with a LongBoard.

![](/_images/_superlongboard/LB2SLB_pone.jpg){.aligncenter .size-medium}

## Unpacking

In the box you’ll find:
<ul>
  <li>Your new <b>SuperLongBoard</b> inside it’s aluminum enclosure</li>
  <li><b>E-stop</b> with 3 additional ‘Action Buttons’ that are customizable</li>
  <li><b>E-stop cable</b>, plenty long to increase mounting options</li>
  <li>And a <b>USB-C cable</b>, MK2 <b>mounting hardware</b>, and some <b>spare connectors</b></li>
</ul>
The only other parts that you’ll need to supply yourself are:
<ul>
  <li>The minimum <b>24V 10A power supply</b> needed to run the SLB (you can use the one your LongBoard currently uses)</li>
  <li>Your <b>CNC machine</b>, already tested to be working using its existing LongBoard</li>
  <li>A <b>computer running gSender</b> with a free USB port</li>
</ul>

![](/_images/_superlongboard/LB2SLB_p3.jpg){.aligncenter .size-medium}

We hope everything arrived well and in one piece! Let’s take the cover off the SuperLongBoard and see what’s under the hood.

Unscrew the top-right thumbscrew a couple turns (pictured) then slide the cover to the right. Once the hole in the cover lines up, you’ll be able to pull the top of the cover towards you and it will come free.

![](/_images/_superlongboard/LB2SLB_p42b2.jpg){.aligncenter .size-medium}

## Preparation

Before diving into rewiring, we’d first suggest you note down any firmware changes that are unique about your setup. You can do this by connecting to your CNC in gSender and using the Firmware Tool to find sections that are <b>highlighted in yellow</b>. In the example below, you can see that the maximum travel is different from the standard MK2 12x30.

![](/_images/_superlongboard/LB2SLB_p2.jpg){.aligncenter .size-medium}

Yellow sections show when a change has been made from the default settings. Any of these should be written down and will be re-entered when the new board is set up.

## Wiring

To help communicate where things are on the board, we use the terms shown below:

![](/_images/_superlongboard/IMG_7836.jpg){.aligncenter .size-medium}
