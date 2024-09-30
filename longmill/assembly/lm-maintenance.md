---
title: Maintenance 🛠️
menu_order: 0
post_status: publish
post_excerpt: Maintenance guide for the LongMill CNC, to check rails and V-wheels, tension anti-backlash nut and V-wheels, lubricate linear guides.
post_date: 2021-04-30 15:35:00
taxonomy:
    knowledgebase_cat: lm-assembly
    knowledgebase_tag:
        - mk1
custom_fields:
    KBName: LongMill CNC
    basepress_post_icon: bp-caret-right
skip_file: no
featured_image: /_images/_longmill/_assembly/_maintenance/lm_maintenance_p1_DirtRail.jpg
---

All CNCs require maintenance and doing regular maintenance on your LongMill is quick and easy. Getting into the habit of doing machine checkups will ensure that:

<ol>
  <li>Things are caught before potentially affecting your carves</li>
  <li>Your machine will run at the top of its game for many years</li>
</ol>

The normal areas of maintenance you'll want to keep your eyes on will include:

<ol>
  <li>Clean rails and wheels</li>
  <li>Tensioned delrin nuts, a.k.a. robots</li>
  <li>Tensioned eccentric nuts / v-wheels</li>
  <li>Lubricating linear rails</li>
  <li>Checking for loose fasteners</li>
</ol>

Frequency of maintenance will vary based on the nature of the work you do on your LongMill: dust produced and cutting forces. For example, always cutting hard materials with no dust boot will require much more regular checkups versus light PCB cutting. It's generally a good idea to clean the rails and check the nuts and v-wheels every 10-20 hours, then check for loose hardware (bolts, nuts, set screws on pulley and couplers) and oil the linear guides every 20-30 hours.

In addition, you'll notice that the nuts and v-wheels are consumables, meaning that they'll eventually wear out to the point that they need replacing. We recommend replacing your delrin anti-backlash nuts every 1500-2000 hours, or when the tensioning screw does not allow for any more adjustment. Similarly, we recommend replacing your v-wheels every 1500-2000 hours, or when the v-wheels have worn down to the level where the eccentric nuts no longer provide any tension. You can tell if they need replacing if the gantries are loose on the rails even after adjusting the eccentric nuts to their extreme position.

## Cleaning your rails and wheels

Over time, your rails and wheels may accumulate dust which takes the form of black splotches. It gets compressed into this black form after being rolled over by the v-wheels. We recommend regularly cleaning off this gunk with a small brush, plastic scraper, wood scrap, or even your fingernails. Remember to clean both the top and bottom edges of each rail and try your best to get into the crevices of all the wheels.

This is something that you won't have to do as often if you have good dust collection.

![](/_images/_longmill/_assembly/_maintenance/lm_maintenance_p1_DirtRail.jpg "Black dirt on the edges of the rail.")

## Adjusting the tension on your Delrin anti-backlash nuts

The LongMill comes with four Delrin anti-backlash nuts that allow users to reduce backlash and compensate for wear over time. For more information about backlash and how it can affect the precision of your machine, check out this awesome page here: <a href="http://www.machinetoolhelp.com/Repairing/What_is_backlash.html">http://www.machinetoolhelp.com/Repairing/What_is_backlash.html </a>

<ol>
  <li>Check if you have backlash in your machine by pushing each axis back and forth. If you can feel the machine move, even though the lead screws are stationary, you may need to tension your nut.</li>
  <li>Use an allen key to reach each of the tensioning screws. Photos of the locations for each screw are below. Start by very lightly turning the screw and checking for play. Note that over-tightening your nut can cause premature wear, you should only need a small amount of tension to remove backlash from your system. <b>Also note</b> that once the delrin nut is worn excessively, the M5 bolt head could start to rub or bind against the lead screw and damage it. Backlash nuts are consumable, so if they are excessively worn then they should be <a href="https://sienci.com/product/delrin-anti-backlash-block/" target="_blank" rel="noopener noreferrer">replaced</a>.</li>
</ol>

![](/_images/_longmill/_assembly/_maintenance/lm_maintenance_p2_AntiLYAxis.jpg "Left Y-axis"){.aligncenter .size-medium}

![](/_images/_longmill/_assembly/_maintenance/lm_maintenance_p3_AntiRYAxis.jpg "Right Y-axis"){.aligncenter .size-medium}

![](/_images/_longmill/_assembly/_maintenance/lm_maintenance_p4_AntiXAxis.jpg "X-axis"){.aligncenter .size-medium}

![](/_images/_longmill/_assembly/_maintenance/lm_maintenance_p5_AntiZAxis.jpg "Z-axis"){.aligncenter .size-medium}

## Adjusting your eccentric nuts

You can watch this video for a demonstration of how to adjust the eccentric nuts, with pictures and notes to guide you.

[su_youtube url="https://youtu.be/Z7WLmOk90V4"]

The eccentric nuts allow users to adjust the tension on the Delrin v-wheels to bring them closer or further away from the edge of the rail. The wheels need to grip the edge firmly, while still allowing the machine to move smoothly.

![](/_images/_longmill/_assembly/_maintenance/lm_maintenance_p6_DelrinUpHigh.jpg "Eccentric nut at its highest position."){.aligncenter .size-medium}

![](/_images/_longmill/_assembly/_maintenance/lm_maintenance_p7_DelrindownLow.jpg "Eccentric nut at its lowest position."){.aligncenter .size-medium}

One simple way to check if your v-wheels have the right amount of pre-load is to check if you can turn the wheel with your fingers. Your wheels should be tight enough that it should be difficult to use your fingers to turn them, but not tight enough that they do not rotate when you move the axis back and forth.

We recommend checking the tension on your v-wheels on a regular basis.

![](/_images/_longmill/_assembly/_maintenance/lm_maintenance_p8_DelrinWheelTurn.jpg "Checking for the tension on the Delrin v-wheels."){.aligncenter .size-medium}

## Maintaining your Linear Guides

![](/_images/_longmill/_assembly/_maintenance/lm_maintenance_p9_Lube.jpg){.aligncenter .size-medium}

Though the frequency of lubricating your linear guides will vary depending on the type of cutting you do and the frequency of use, we would recommend doing this procedure every 20-30 hours. If you experience grinding noises or roughness in your gantry, we recommend doing this procedure more often.

<ol>
  <li>Wipe your linear guides with a clean cloth, paper towel, rag, or shop towel to remove any dust that may have accumulated on your linear guides. Move your Z-axis up and down if needed.</li>
  <li>Most general-purpose lubrication options such as the 3-in-1 oil should suffice. It is not recommended to use dry lubricants or anything with particulates such as graphite in the lubricant.</li>
  <li>Apply a liberal of machine oil or grease to your linear guides. Move your Z-axis up and down to ensure that the bearings inside have a chance to get coated.</li>
</ol>

Here are some links to more info about lubrication:

<ul>
  <li><a href="https://www.thomsonlinear.com/en/support/tips/what-should-be-used-to-lubricate-linear-bearings">https://www.thomsonlinear.com/en/support/tips/what-should-be-used-to-lubricate-linear-bearings</a></li>
  <li><a href="https://www.hiwin.com/pdf/lubricating_instructions.pdf">https://www.hiwin.com/pdf/lubricating_instructions.pdf</a></li>
</ul>

## Checking for loose fasteners

To mitigate fasteners from coming loose over time on the LongMill, we use nylock nuts and spring washers wherever we can. That being said, fasteners can still come loose over time on a CNC with lots of vibration. We recommend doing a check around the whole CNC on occasion to check the bolt tightness and re-tighten the fasteners you find loose.

Some key areas to check:

<ul>
  <li>Set screws on all couplers, pulleys, and the ACME lock nuts</li>
  <li>M8 screws along the Y-axis rail.</li>
  <li>M8 screws holding the X-axis rail and Y-axis plate.</li>
  <li>M5 screws mounting the Z-axis motor to the steel plate.</li>
  <li>M5 screws on the X and Y-axis</li>
  <li>M3 screws on the XZ gantry</li>
</ul>
