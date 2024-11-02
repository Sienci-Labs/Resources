---
title: Upgrade Other
menu_order: 3
post_status: publish
post_excerpt: Time to power up! Steps on how to upgrade your CNC machine from your old control system to the SuperLongBoard, like the xPRO V5.
post_date: 2024-11-01 23:15:00
taxonomy:
    knowledgebase_cat: slb-handbook
    knowledgebase_tag:
        - slb
custom_fields:
    KBName: SuperLongBoard
    basepress_post_icon: bp-caret-right
skip_file: no
featured_image: _images/_superlongboard/_upgrade/slb_up_p1_SLB.jpg
---

Congrats on upgrading to our newest and most powerful CNC controller to date, the **SuperLongBoard**!

Our main goal in this section is to have you go in with a working CNC, then leave with an **SLB-boosted machine** without skipping a beat. This guide will be written to try to accommodate switching over from other controllers on the market that you're swapping out for the SuperLongBoard (**SLB, on the right**).

![](/_images/_superlongboard/_upgrade/slb_up_p1_SLB.jpg){.aligncenter .size-medium}

## Unpacking

In the box you’ll find:

- Your new **SuperLongBoard** inside it’s aluminum enclosure
- **E-stop** with 3 additional ‘Action Buttons’ that are customizable
- **E-stop cable**, plenty long to increase mounting options
- And a **USB-C cable**, MK2 **mounting hardware**, and some **spare connectors**
- A spare baggy of **5.08mm plugs** to connect power and stepper motors to your SLB. If you didn't **email us before purchasing your SLB**, you might be missing these so you'll need to <a href="https://resources.sienci.com/view/slb-manual/#connectors-list" target="_blank" rel="noopener">source them yourself</a> (first two plugs on the list).

The only other parts that you’ll need to supply yourself are:

- The minimum **24V 10A power supply** needed to run the SLB (you can use the one for your old control board if the specs match, otherwise <a href="https://sienci.com/product/24v-12-5a-power-adapter-for-110vac/" target="_blank" rel="noopener">we also sell them</a>)
- Your **CNC machine**, already tested to be working using its existing control board
- A **computer running gSender** with a free USB port

![](/_images/_superlongboard/_upgrade/slb_up_p2_Box.jpg){.aligncenter .size-medium}

We hope everything arrived well and in one piece! Let’s take the cover off the SuperLongBoard and see what’s under the hood.

Unscrew the top-right thumbscrew a couple turns (pictured) then slide the cover to the right. Once the hole in the cover lines up, you’ll be able to pull the top of the cover towards you and it will come free.

![](/_images/_superlongboard/_upgrade/slb_up_p2_open.png){.aligncenter .size-medium}

To help communicate where things are on the board, we use the terms shown below:

![](/_images/_superlongboard/_upgrade/slb_up_p4_TopBottom.jpg){.aligncenter .size-medium}

## Preparation

Before diving into rewiring, we’d first suggest you note down any attributes that are unique about your setup. This is so that once you switch over to the SLB you'll be able to create the same setup with the same settings.

If you use gSender, you can do this by connecting to your CNC and using the Firmware Tool to find sections that you recall setting up or changing; things like max travel, speed, etc. It won't be disastrous if you forget to record any of these settings, since your old controller should still work so you can always go back and double-check it's settings.

![](/_images/_superlongboard/_upgrade/slb_up_p3_FirmMaxTravel.jpg){.aligncenter .size-medium}

## Wiring xPRO V5

Let’s start moving plugs over to the SLB!

This is a community-contributed document so information might not be the most up-to-date so please submit feedback at the bottom of the page if you find anything missing. Another great resource to reference is the one made by SparksTech below:

https://youtu.be/-kVbz-u0nL0

1. Power off your xPRO controller, then begin unplugging all the various wires one-at-a-time
1. Start with the X, Y1, Y2, and Z stepper motor connectors. Use a small flat head screwdriver to unscrew the wires from the xPRO connectors and transfer them to the SLB connectors, making sure to keep them in the same order.

   ![](/_images/_superlongboard/_upgrade/slb_up_p7_Motors.jpg){.aligncenter .size-medium}
1. Unplug your touch plate/probe and plug it into the **SLB**, on the **Front Side**.

   ![](/_images/_superlongboard/_upgrade/slb_up_p8_Probe.jpg){.aligncenter .size-medium}
1. Grab the new E-stop and plug the green end into the **Front Side** of the **SLB**, then the other end into the backside of the E-stop.

   ![](/_images/_superlongboard/_upgrade/slb_up_p9_Estop.jpg){.aligncenter .size-medium}
1. Now grab the USB-C cable that came with your **SLB** and plug it into the **Front Side** of the board. Plug the other end into your computer.

   ![](/_images/_superlongboard/_upgrade/slb_up_p10_DoubleUSB.jpeg){.aligncenter .size-medium}
1. You'll need to reverse the polarity of the xPRO power connector so that red is on the left side and black is on the right. Once it's rewired, you'll be able to plug the power connector into the **Back Side** of the **SLB**.

   ![](/_images/_superlongboard/_upgrade/slb_up_p11_Power.jpg){.aligncenter .size-medium}
1. Lastly, when looking at the **Back Side** of the **SLB**, you will see a power switch. Slide it to the ‘ON’ position to power on the **SLB**. It’s Alive!!

   ![](/_images/_superlongboard/_upgrade/slb_up_p12_OnOff.jpg){.aligncenter .size-medium}

**Congratulations!** You’ve wired up your new SLB with all its typical accessories! If you still have other, slightly less common accessories to wire in, then keep reading the next section; otherwise you can move over to <a href="https://resources.sienci.com/view/slb-upgrading/#gSender" target="_blank" rel="noopener">gSender</a> to connect and do some quick tests.

### Optional Wiring

If you have Limit Switches, you'll need to wire them in using the Auxiliary terminal connector input (shown below). One trick about this is that the connector has a shared ground, so you'll want to either joint-crimp all your wires together, use a WAGO connector, or use a ground bus.

<p style="text-align: center;"><b><em>Note:</b> The Y2 connection isn’t used at this time</em></p>

![](/_images/_superlongboard/_upgrade/slb_up_p14_LimitSLB.jpg){.aligncenter .size-medium}

If you have the resources, you can also crimp on 4-pin JST connectors and plug them straight into the corresponding plugs on the board. <a href="https://sienci.com/product/inductive-sensor-kit-for-the-LongMill-mk2/" target="_blank" rel="noopener">Sienci inductive sensors</a> come with these by default, as do other common sensors.

![](/_images/_superlongboard/_upgrade/slb_up_p13_Limit.jpg){.aligncenter .size-medium}

Once you're feeling comfortable with your setup, you can go back to the main ["Upgrading to SLB" writeup](https://resources.sienci.com/view/slb-upgrading/#gsender) to see how to set up gSender and run quick functionality tests.

For wiring other accessories like a Laser Diode, IOT Relay, Spindle over RS485, and more, then we'd suggest <a href="https://resources.sienci.com/view/slb-manual/" target="_blank" rel="noopener">reading our full Technical Manual page here</a>.

Some of this is also addressed in the second-half of SparksTech's video where he was able to get Spindle RS485 for the H100 VFD set up, as well as he provides a 3D printable adapter for the E-stop to mount it to his Ultimate Bee CNC. There's also a <a href="https://forum.sienci.com/t/my-road-to-a-SuperLongBoard-from-xpro-v5/12877" target="_blank" rel="noopener">topic on our forum discussing the switch-over</a>.

https://youtu.be/-kVbz-u0nL0

## Troubleshooting

If you are still running into any issues with your new SLB, please see the <a href="https://resources.sienci.com/view/slb-manual/#troubleshooting">Troubleshooting Section</a> on our more Detailed page. You can also always contact us directly at <a href="mailto:support@sienci.com">support@sienci.com</a>.
