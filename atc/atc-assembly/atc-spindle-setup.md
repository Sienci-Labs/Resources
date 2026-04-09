---
title: ATC Spindle Setup
menu_order: 3
post_status: draft
post_excerpt: Assembly instructions for setting up the atc spindle on an AltMill. 
post_date: 2026-02-10 11:14:53
taxonomy:
    knowledgebase_cat: atc-assembly
    knowledgebase_tag: 
custom_fields:
    KBName: AutoToolChanger
    basepress_post_icon: bp-caret-right
skip_file: no
featured_image: _images/post-image.jpg
---

## Spindle Installation & Drag Chain Setup

### Spindle & Drag Chain Arm

    [Render] Image of full machine with spindle outlined in blue (atc_assembly_spin-header1.jpg)

![](/_images/_atc/_atc_assembly/_spindle/atc_assembly_spin-parts1.jpg){.aligncenter .size-full .wid}

1. Start by unpacking the ATC spindle and grabbing the ATC drag chain arm. We will also need 6 x M4 - 8mm flat head screws and the Allen key from the ATC fasteners bag.

1. Lift the spindle out of the bottom foam and place it on the top foam packaging with the **threaded mounting holes facing up**.

    ![](/_images/_atc/_atc_assembly/_spindle/atc_assemblly_spin-spindle.jpg){.aligncenter .size-medium}

        ⚠️ Never stand the spindle on its nose (tool end) to avoid damaging the bearings.  

1. Remove the **male end link** (studded end) from the Z-axis drag chain.

1. Attach this end link to the **ATC drag chain arm**, minding the mounting position and direction, using two (2) M4 - 8mm screws.

    ![](/_images/_atc/_atc_assembly/_spindle/atc_assemblly_spin-zdragend.jpg)

1. Mount the drag chain arm to the spindle using four (4) M4 - 8mm screws.

    ![](/_images/_atc/_atc_assembly/_spindle/atc_assemblly_spin-zaxisdrag.jpg){.aligncenter .size-medium}

### Mounting Plate

![](/_images/_atc/_atc_assembly/_spindle/atc_assembly_spin-parts2.jpg){.aligncenter .size-full .wid}

1. Place the **ATC mounting plate** onto the spindle.
2. Select the correct **mounting position** based on your machine configuration.

    **4x4 & 2x4 Machines** the standard configuration is the center position. The mounting plate holes should align up with six (6) corresponding holes on the spindle.

    ![](/_images/_atc/_atc_assembly/_spindle/atc_assembly_spin-mount24.jpg){.aligncenter .size-medium}

    **4x8 Machines** the mounting plate should be shifted up. The mounting plate holes will align with the top four (4) holes on the spindle.

    ![](/_images/_atc/_atc_assembly/_spindle/atc_assembly_spin-mount8.jpg){.aligncenter .size-medium}

3. Secure the mounting plate using M6 - 14mm button head screws.

### Mount the Spindle

![](/_images/_atc/_atc_assembly/_spindle/atc_assembly_spin-parts3.jpg){.aligncenter .size-full .wid}

    ⚠️ Due to the weight, we recommend two people to mount the ATC spindle.

1. Grab two (2) M6 shoulder screws and two (2) M6-25 mm button head screws from the fasteners bag.

![](/_images/_atc/_atc_assembly/_spindle/atc_assembly_spin-boltpattern.jpg){.aligncenter .size-medium}

    >**If your Z-axis gantry plate has these extra threaded holes indicated in green, complete Step 1. If not, no worries - move onto Step 2.**

1. We will use one of the extra holes as another mounting point, for more stability. Grab the M6-14 mm button head screw, and partially thread it into the Z-axis gantry plate. Leave about 7mm (1/4 inch) sticking out. Then use the screw to **anchor the ATC spindle** through the slot on the mounting plate. This is the only bolt that we **won't be tightening**.

1. With the ATC spindle held against the X-axis gantry, install the two (2) M6 shoulder screws in the lower holes. Start them by hand, then tighten fully.

1. Next, install the two M6 - 25mm button head screws in the lowest set of holes. Start them by hand, then tighten fully.

1. Finally, you may be able to fit one additional M6 - 25mm button head screws above the shoulder screw on the left side, if you have the new gantry.

## Drag Chain Hardware Installation

    [Render] Image of full machine with mounting bracket and drag chains outlined in blue (atc_assembly_spin-header2.jpg)
---
This section will modify the 4x4 and 2x4 AltMills to make them compatible with the Z-axis drag chain.

### 4x8 Machines

[SKIP AHEAD TO CABLE AND TUBING ROUTING](#cable-and-tubing-routing)

### 4x4 & 2x4 Machines  

![](/_images/_atc/_atc_assembly/_spindle/atc_assembly_spin-parts4.jpg){.aligncenter .size-full .wid}

#### Remove the Drag Chain Bracket

1. Disconnect the X-axis drag chain from its end link on the bracket.
1. Remove the old drag chain bracket from the back of the gantry.
1. Separate the one (1) end link from the old drag chain bracket, we will use it.

    ![](/_images/_atc/_atc_assembly/_spindle/atc_assembly_spin-removemount.jpg){.aligncenter .size-medium}

#### Install the Z-Plus Drag Chain Bracket

1. Remove one (1) end link from the Z-axis drag chain
1. Install the two (2) end links on the new Z-plus drag chain bracket, by using M5 - 10mm screws and M5 lock nuts. Only use 3 of each for now, to ease cable routing later on.

    > Tip: Ensure the **male and female drag chain ends** are correctly oriented; reversing them is tedious.

![](/_images/_atc/_atc_assembly/_spindle/atc_assembly_spin_z-plus-drag2.JPG){.aligncenter .size-medium}

1. Install the Z-Plus drag chain bracket back onto the XZ carriage.

![](/_images/_atc/_atc_assembly/_spindle/atc_assembly_spin_z-plus-drag3.JPG){.aligncenter .size-medium}

## Cable and Tubing Routing

![](/_images/_atc/_atc_assembly/_spindle/atc_assembly_spin-parts5.jpg){.aligncenter .size-full .wid}

### Prepare the Cables

Gather the following from the ATC box:

- **Signal cable**
- **Pneumatic tubing (10 m)**
- **ATC spindle cable (blue connector)** - if it's already installed on your AltMill, that's great!

Place the cable ends and tubing near the **spindle connections** on the Z-axis.

### Route Through the Z-Axis Drag Chain

1. Route the wires and tubing through the opening in the Z-plus drag chain bracket. If it’s tight, loosen the bracket slightly to widen the opening.
1. Use a flathead screwdriver to detach the remaining clips on the Z-axis drag chain.
1. Clip the Z-axis drag chain back onto its end links.
1. Close the clips around the three cables.
1. Use one M5 - 10mm screw and M5 lock nut to fasten the loose end link at the Z-plus drag chain bracket.

![](/_images/_atc/_atc_assembly/_spindle/atc_assembly_spin-zdragchain.jpg){.aligncenter .size-medium}

    ⚠️ Important:
    - Keep cables and tubing **parallel** inside the drag chain.
    - Do **not cross them**.  

### Connect the Spindle

On the ATC spindle, connect the following in this order:

1. Spindle cable

2. Signal cable

3. Pneumatic tubing

        ⚠️ Ensure connectors align with the grooves on the aviation plug; misalignment may damage pins.

![](/_images/_atc/_atc_assembly/_spindle/atc_assembly_spin-connections.jpg){.aligncenter .size-medium}

### Route Through X and Y Drag Chains

1. Detach the **X-axis drag chain** from the end link on the XZ carriage. Open the clips, place the new cables and tubing inside, and close a few clips to hold them in place.

    - Run the **tubing** under the Z-plus drag chain bracket, before entering the X-axis drag chain. Leave some tubing out for strain relief.

    - Run the **spindle** and **signal cables** straight from the Z-axis drag chain into the X-axis drag chain

    - Make sure these do not cross or twist.

![](/_images/_atc/_atc_assembly/_spindle/atc_assembly_spin-airline.jpg){.aligncenter .size-medium}

1. Adjust the cables and tubing as needed, then close the remaining clips along the **X-axis drag chain**.
1. Reconnect the X-axis drag chain to the Z-plus drag chain bracket.
1. Verify the spindle cable reaches the VFD through the table leg cutout.
1. Verify the signal cable reaches the SLB-EXT.
1. Ensure the tubing is free of kinks and sharp bends.
1. Finally, route cables and tubing for the **Y-axis drag chain**, adjust as needed, then close the clips.

Congrats! You've completed the spindle setup steps.
