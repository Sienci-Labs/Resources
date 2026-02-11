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

### VFD Connections

1. Grab the **VFD** and make the following connections:

   * Plug the **female end of the VFD power cable** into the VFD.
   * Plug the **spindle cable (blue)** into the VFD.
   * Plug the **Modbus cable** into the VFD *(confirm correct end connectors)*.

2. Install **two (2) M? nuts** into the **plastic VFD adapter bracket**.

3. Remove and unplug the **E-stop** from the table leg.

4. Place the **adapter bracket** onto the **inner face of the front-left AltMill leg**, then place the VFD against the bracket, aligning the studs with the bracket holes.

5. Using the **original E-stop screws**, refasten the **E-stop** on the **outer face of the leg**.

6. Re-plug the **E-stop cable** into the E-stop.

## Finishing Up Connections

1. Turn **off** the **SLB-EXT**.

2. On the SLB-EXT, remove the **top row of green connectors**, including:

   * `SW1`
   * `SW2`
     These connectors will interfere with the daughter board.

3. Connect the **daughter board** onto the **black header connector** on the SLB-EXT.

4. Carefully connect the **spindle cable** and **signal cable** aviation plugs to the spindle.

   * The connectors have **different pin counts** — check carefully before plugging in.
   * ⚠️ *Incorrect alignment can easily damage the pins.*

5. Plug the **other end of the signal cable** into the **RS485 port on the SLB-EXT** *(confirm port)*.

6. Plug the **other end of the Modbus cable** into the **daughter board**.

7. Connect the **auxiliary backpack cable** to the **PENDANT port** on the SLB-EXT.

8. Insert the **SD card** into the **SD card slot** on the SLB-EXT.

## Wiring Sanity Check

Use this section to double-check all connections:

* **Spindle Cable**
  `Spindle (aviation) → VFD (aviation)`

* **Signal Cable**
  `Spindle (aviation) → RS485 port on SLB-EXT?`

* **Modbus Cable**
  `VFD (RJ / Ethernet) → Daughter board`

* **VFD Power Cable**
  `VFD → Power outlet`

* **Auxiliary Backpack Cable**
  `Spindle → PENDANT port on SLB-EXT`
  