---
title: Maintenance
menu_order: 2
post_status: publish
post_excerpt: How to keep your MK3 clean and running smoothly.
post_date: 2026-05-19 15:16:00
taxonomy:
    knowledgebase_cat: lmk3-handbook
    knowledgebase_tag:
custom_fields:
    KBName: LongMill MK3
    basepress_post_icon: bp-caret-right
skip_file: no
featured_image: _images/post-image.jpg
---
Like any other CNC, the LongMill MK3 needs regular maintenance to stay in tip-top shape long-term. Depending on how often the machine is being used, the frequency of maintenance tasks can vary greatly.
We have some general estimates on when you should do these tasks, but the most important thing is to **use your senses!** Keep an ear out for new sounds like **squeaking or binding** - these will indicate that your machine might need a little TLC.

## Materials Needed

- Grease gun kit
  - Lithium grease tube, 3oz
  - Grease gun
  - Nozzle
  - Spout
- Dry lube
- Anti-backlash nut (4 pcs)
- Shop towel
- Scotch Brite
- 2mm Allen key
- Flathead screwdriver
- Small brush or toothpick
- Carbon brushes, if you have a router

## Preparations

### Clean the Components

Wipe the linear guide blocks, rails, and lead screws with shop towel to remove debris and dirt. If there is rust, scrub down with Scotch Brite.

### Set up Grease Gun

The grease gun will be used on the linear guides only. **Do not apply lithium grease onto the lead screws.**

1. Pull the handle on the grease gun to its furthest extent, then lock it into place at the notch.

    ![](/_images/_lmmk3/_handbook/lmk3_maintenance-grease-lock.gif){.aligncenter .size-full}

1. Grab the lithium grease tube, and remove the caps on both ends using a flathead screwdriver.

    ![](/_images/_lmmk3/_handbook/lmk3_maintenance-grease-tube.JPG){.aligncenter .size-medium}

1. Put the grease tube into the gun, with the foil facing up.

1. Remove the foil.

1. With the top of the grease gun, push the grease tube as you twist the top on.

    ![](/_images/_lmmk3/_handbook/lmk3_maintenance-grease-assemble.jpg){.aligncenter .size-medium}

1. Grab one of the spouts and the fine tip nozzle, fasten the spout onto the grease gun, then fasten the nozzle onto the spout.

    ![](/_images/_lmmk3/_handbook/lmk3_maintenance-grease-spout.jpg){.aligncenter .size-medium}

1. Unlock the handle from the notch.

1. Pump the grease gun until grease comes out.

    ![](/_images/_lmmk3/_handbook/lmk3_maintenance-grease-squeeze.jpg){.aligncenter .size-medium}

## Lubricate Linear Guides

Do every **20-30 hours** of cutting

1. For the Z-axis, first jog to the top to get access to the screws.
1. Remove one (1) screw from each linear guide block using the Allen key. See below for locations on each axis.
1. Push the nozzle firmly against the hole, and pump until grease comes out between the block and rail.
    ![](/_images/_lmmk3/_handbook/lmk3_maintenance-blockgrease.jpg){.aligncenter .size-medium}
1. Wipe with shop towel to remove the excess.
1. Refasten the screw.
1. Jog to each end of the axis, to fully distribute the grease.
1. Repeat the above steps for each axis.

    ![](/_images/_lmmk3/_handbook/lmk3_maintenance-lmblock.jpg){.aligncenter .size-medium}

    ![](/_images/_lmmk3/_handbook/lmk3_maintenance-lmblock3.jpg){.aligncenter .size-medium}

    ![](/_images/_lmmk3/_handbook/lmk3_maintenance-lmblock2.jpg){.aligncenter .size-medium}

## Lubricate Lead Screws

Do every **20-30 hours** of cutting

1. Apply dry lube onto shop towel
1. Grab the lead screw with the shop towel, then run the towel across the length of the lead screw, rotating to get into the threads at all angles
1. Remove the shop towel
1. Jog the machine so the dry lube distributes along the entire lead screw

## Replace Anti-backlash Nuts

Do as needed, usually once every few years

Anti-backlash nuts are used to tension the lead screws so that the machine can move accurately. Since they are spring-loaded, they will continue to adjust themselves to apply the right tension.

However, if you start noticing lead screw vibrations, then the nut has probably worn out and needs replacing.

### X and Y axis

1. Power off the machine
1. Unscrew the two M5-25mm screws holding the anti-backlash nut
1. Unfasten the black ACME nut, which is located opposite of the motor end of the lead screw, and remove it from the lead screw
1. At the same area, loosen the end plate/gantry screws connecting to the rail, and remove them
1. Rotate the lead screw manually at the coupler, to move the anti-backlash nut off the lead screw
1. Replace with the new anti-backlash nut, carefully threading it onto the lead screw
    - Do this slowly! We do not want to crossthread the nut
1. Refasten the end plate/gantry, ACME nut and anti-backlash nut screws to secure components in place
    - Do not overtighten the anti-backlash nut fasteners screws, otherwise it will cause binding

### Z-axis

1. Power off the machine
1. Remove your router from the mount
1. Unfasten the router mount from the Z-axis assembly
    - Jog the machine down until the gantry bottoms out, then turn OFF the controller
    - Unscrew the four (4) M5-25mm screws at the back
1. Unscrew the two M5-25mm screws holding the anti-backlash nut
1. Rotate the lead screw manually at the coupler, to move the anti-backlash nut off the lead screw
1. Orient the new anti-backlash nut so the spring is facing upwards, then carefully thread it onto the lead screw
    - Do this slowly! We do not want to crossthread the nut
1. Refasten the anti-backlash nut and router mount screws to secure components in place
    - Do not overtighten the anti-backlash nut fasteners screws, otherwise it will cause binding

## Router

We recommend cleaning out your collets and collet nuts, as dust buildup can cause bits to get stuck in your router. Use a small brush or toothpick to clean in between the grooves and threads.

If you notice sparks from your router or a burnt smell, it means that your carbon brushes are worn out. Please review the [instructions here](https://resources.sienci.com/view/as-carbon-brushes/) on how to replace them.
