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

[header image using the following parts:
VFD mounting spacer, 2x m5 lock nuts, 4x m5-30 screws, 1x VFD unit, 1x VFD power cord, 1x Modbus cable, 1x ATC Shield, 1x RJ12 cable, 1x SD card
]

1. To prepare for installation, remove and unplug the **E-stop** from the table leg. Keep the screws that come with the E-stop.

1. Route the blue connector from the spindle cable through the table leg cutout

![](</_images/_atc/_atc_assembly/temp/Screenshot 2026-02-12 at 3.32.38 PM.png>)

1. Plug the connector into the bottom of the VFD. Rest the VFD on foam or a box, for now, until the VFD is mounted.

1. Put two (2) M5 nuts into the 3D printed mounting spacer. They should be fully seated, in order to fully secure the fasteners later on.

![](</_images/_atc/_atc_assembly/temp/Screenshot 2026-02-12 at 3.28.46 PM.png>)

1. Place the **VFD mounting spacer** onto the **inner face of the front-left AltMill leg**, then place the VFD against the spacer, aligning the two (2) M5-30mm screws from the E-stop with the bracket holes. Refasten the **E-stop** on the **outer face of the leg**.

![](/_images/_atc/_atc_assembly/atc_assembly_vfd1.jpg){.aligncenter .size-medium}

1. Mount the VFD unit inside the table leg using the remaining two (2) M5-30mm screws.

![](/_images/_atc/_atc_assembly/atc_assembly_vfd2.jpg){.aligncenter .size-medium}

The VFD unit should be positioned with the screen/panel aligned with the cutout in the table leg. Plug the E-stop cable back in.

![](/_images/_atc/_atc_assembly/atc_assembly_vfd3.jpg){.aligncenter .size-medium}

1. Plug the **VFD power cord** into the VFD.

1. Plug the **Modbus cable** into the VFD.

![](/_images/_atc/_atc_assembly/atc_assembly_vfd4.jpg){.aligncenter .size-medium}

1. Plug in the Modbus cable into the 'RS485' connector on the SLB-EXT controller.

![](/_images/_atc/_atc_assembly/atc_assembly_vfd5.jpg){.aligncenter .size-medium}

### Finishing Up Connections

1. Turn **off** the **SLB-EXT**.

1. On the SLB-EXT, remove the **top row of green connectors**, including:

   * `SW1`
   * `SW2`

    These connectors will interfere with the ATC shield.

1. Connect the following into the **ATC shield**

* RJ12 cable

* Other end of the signal cable

![](/_images/_atc/_atc_assembly/temp/IMG_8984.jpg)

1. Then plug in the ATC shield onto the **black header connector** on the SLB-EXT.

![](/_images/_atc/_atc_assembly/temp/IMG_8988.jpg)

1. Connect the other end of the **RJ12 cable** to the **PENDANT port** on the SLB-EXT.

1. Plug the **other end of the Modbus cable** into the **RS485 port on the SLB-EXT**.

1. Insert the **SD card** into the **SD card slot** on the SLB-EXT. Make sure it sits into the port, fully.

## Wiring Sanity Check

Use this section to double-check all connections:

* **Spindle Cable**
  `Spindle (aviation) → VFD (aviation)`

* **Signal Cable**
  `Spindle (aviation) → ATC shield`

* **Modbus Cable**
  `VFD (RJ / Ethernet) → RS485 on EXT board`

* **VFD Power Cable**
  `VFD → Power outlet`

* **RJ12 Cable**
  `ATC shield → PENDANT port on SLB-EXT`
  