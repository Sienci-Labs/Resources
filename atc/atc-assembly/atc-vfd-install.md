---
title: ATC VFD Install
menu_order: 3
post_status: draft
post_excerpt: How to connect your VFD to your ATC system. 
post_date: 2026-02-10 11:16:53
taxonomy:
    knowledgebase_cat: atc-assembly
    knowledgebase_tag: 
custom_fields:
    KBName: AutoToolChanger
    basepress_post_icon: bp-caret-right
skip_file: no
featured_image: _images/post-image.jpg
---

## VFD Installation & Connections

1. To prepare for installation, remove and unplug the **E-stop** from the table leg.

Grab the VFD and plug in the blue connector from the spindle cable. Emphasize this!!!!! Leave the VFD on the ground for now.

Put 2x M5 nuts into the adapter bracket. You may need to put tape to hold the nuts temporarily.

INSERT photo here. 

1. Place the **adapter bracket** onto the **inner face of the front-left AltMill leg**, then place the VFD against the bracket, aligning the screws from the E-stop (M5-30mm) with the bracket holes. refasten the **E-stop** on the **outer face of the leg**.

![](/_images/_atc/_atc_assembly/atc_assembly_vfd1.jpg){.aligncenter .size-medium}

1. Mount the VFD unit inside the table leg using the remaining two M5-30mm screws.

![](/_images/_atc/_atc_assembly/atc_assembly_vfd2.jpg){.aligncenter .size-medium}

1. The VFD unit should be positioned with the screen/panel aligned with the cutout in the table leg. Plug the E-stop cable back in.

![](/_images/_atc/_atc_assembly/atc_assembly_vfd3.jpg){.aligncenter .size-medium}

1. Plug the **female end of the VFD power cable** into the VFD.
   Plug the **spindle cable (blue)** into the VFD. Plug the **Modbus cable** into the VFD *(confirm correct end connectors)*.

![](/_images/_atc/_atc_assembly/atc_assembly_vfd4.jpg){.aligncenter .size-medium}

1. Plug in the VFD control cable into the 'RS485' connector on the SLB-EXT controller.

![](/_images/_atc/_atc_assembly/atc_assembly_vfd5.jpg){.aligncenter .size-medium}

### Finishing Up Connections

1. Turn **off** the **SLB-EXT**.

2. On the SLB-EXT, remove the **top row of green connectors**, including:

   * `SW1`
   * `SW2`
     These connectors will interfere with the daughter board.

3. Connect the **daughter board** onto the **black header connector** on the SLB-EXT.

![](/_images/_atc/_atc_assembly/temp/IMG_8988.jpg)

4. Carefully connect the **spindle cable** and **signal cable** aviation plugs to the spindle.

DAUGHTER - use backpack to get to PENDANT
DAUGHTER - TO signal 

![](/_images/_atc/_atc_assembly/temp/IMG_8984.jpg)

   * The connectors have **different pin counts** — check carefully before plugging in.
   * ⚠️ *Incorrect alignment can easily damage the pins.*

5. Plug the **other end of the signal cable** into the **RS485 port on the SLB-EXT** *(confirm port)*.

6. Plug the **other end of the Modbus cable** into the **daughter board**.

7. Connect the **auxiliary backpack cable** to the **PENDANT port** on the SLB-EXT.

8. Insert the **SD card** into the **SD card slot** on the SLB-EXT. Make sure it pushes into the port, fully. 

## Wiring Sanity Check

Use this section to double-check all connections:

* **Spindle Cable**
  `Spindle (aviation) → VFD (aviation)`

* **Signal Cable**
  `Spindle (aviation) → daughter board

* **Modbus (coily) Cable**
  `VFD (RJ / Ethernet) → RS485 on EXT board`

* **VFD Power Cable**
  `VFD → Power outlet`

* **Auxiliary Backpack Cable**
  `daughter → PENDANT port on SLB-EXT`
  