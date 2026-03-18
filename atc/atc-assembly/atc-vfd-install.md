---
title: ATC VFD Install
menu_order: 5
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

    [Render] Image of full machine with VFD outlined in blue (atc_assembly_vfd-header1.jpg)

    [Render] Parts Needed:
    2x M5 Lock Nuts
    1x VFD Mounting Spacer
    4x M5 - 30mm Socket Head Screws
    1x 2.2kW Enclosed VFD
    1x 220V VFD Power Cord
    1x Modbus cable
    1x ATC Shield (SLB-EXT)
    1x RJ12 cable
    1x SD card
    (atc_assembly_vfd-parts1.jpg)

---

1. Remove the **E-stop** from the table leg and unplug the **E-stop** from the SLB-EXT controller. Keep the screws that come with the E-stop.

1. Route the blue connector from the spindle cable through the table leg cutout

---

    [Render] A single image of the front-left AltMill table leg with the spindle power cable, blue connector end, entering the triangular cutout. The VFD is not installed on. Image below is for reference only.
    (atc_assembly_vfd-table-leg.jpg)

![](</_images/_atc/_atc_assembly/temp/Screenshot 2026-02-12 at 3.32.38 PM.png>)

---

1. Plug the connector into the bottom of the VFD. Rest the VFD on foam or a box, for now, until the VFD is mounted.

1. Fully seat two (2) M5 lock nuts into the 3D printed **VFD mounting spacer.** Orient the lock nuts so that the hex of the nut is facing into the spacer.

1. Place the **VFD mounting spacer** onto the **inner face of the front-left AltMill leg**, aligning the two (2) M5 - 30mm screws from the E-stop with the spacer holes. Fasten the **E-stop** on the **outer face of the leg**.

---
![](/_images/_atc/_atc_assembly/atc_assembly_vfd1.jpg){.aligncenter .size-medium}

---

1. Mount the enclosed VFD inside the table leg using the remaining two (2) M5 - 30mm screws. Ensure that the VFD is positioned so you can see the screen through the table leg cutout.

---
![](/_images/_atc/_atc_assembly/atc_assembly_vfd2.jpg){.aligncenter .size-medium}

---

![](/_images/_atc/_atc_assembly/atc_assembly_vfd3.jpg){.aligncenter .size-medium}

---

1. Plug the **E-stop cable** back into the SLB-EXT.

1. Plug the **VFD power cord** into the VFD.

1. Plug the **Modbus cable** into the VFD.

---
![](/_images/_atc/_atc_assembly/atc_assembly_vfd4.jpg){.aligncenter .size-medium}

---

1. Plug the other end of the **Modbus cable** into the 'RS485' connector on the SLB-EXT controller.

---
![](/_images/_atc/_atc_assembly/atc_assembly_vfd5.jpg){.aligncenter .size-medium}

---

### Finishing Up Connections

1. Turn **off** the **SLB-EXT**.

1. On the SLB-EXT, remove the **top row of green connectors**, including:

   * `SW1`
   * `SW2`

    These connectors will interfere with the ATC shield.

1. Connect the following into the **ATC shield**

* RJ12 cable

* Other end of the signal cable

1. Then plug in the **ATC shield** onto the **black header connector** on the SLB-EXT.

---

    [Render] A single image of the ATC shield with the RJ12 cable and signal cable connected. The ATC shield is mounted onto the SLB-EXT. Images below are for reference only.
    
    (atc_assembly_vfd-shield.jpg)

![](/_images/_atc/_atc_assembly/temp/IMG_8984.jpg)

![](/_images/_atc/_atc_assembly/temp/IMG_8988.jpg)

---

1. Connect the other end of the **RJ12 cable** to the **PENDANT port** on the SLB-EXT.

1. Plug the **other end of the Modbus cable** into the **RS485 port on the SLB-EXT**.

1. Insert the **SD card** into the **SD card slot** on the SLB-EXT. Make sure it fully sits into the port.

## Wiring Sanity Check

Use this section to double-check all connections:

* **Spindle Cable**
  `Spindle (aviation) → VFD (aviation)`

* **Signal Cable**
  `Spindle (aviation) → ATC shield`

* **Modbus Cable**
  `VFD (RJ / Ethernet) → RS485 on EXT board`

* **VFD Power Cable**
  `VFD (NEMA 6-15P) → Power outlet`

* **RJ12 Cable**
  `ATC shield → PENDANT port on SLB-EXT`
  