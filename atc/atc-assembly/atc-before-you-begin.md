---
title: ATC Before You Begin
menu_order: 2
post_status: draft
post_excerpt: 
post_date: 2026-02-09 11:44:53
taxonomy:
    knowledgebase_cat: atc-assembly
    knowledgebase_tag: 
custom_fields:
    KBName: AutoToolChanger
    basepress_post_icon: bp-caret-right
skip_file: no
featured_image: _images/_atc/_atc_assembly/_before/atc_assembly_before-axis.jpg
---

## Before You Begin

If you’re installing the ATC on a **new machine build**, please complete the [AltMill Assembly Process](https://resources.sienci.com/view/am-mk2-best-practices/) up to and including stage **9 First Movement** before returning to this guide.

The expected ATC assembly time is **2–4 hours**, so be sure to allot enough time and pace yourself to avoid errors, damage, or injury during the process.

### Software Upgrade

Before we dive in, we will need to make some changes on the software side. You will need to:

1. **Upgrade** [gSender] to 1.6.0 or higher, (https://github.com/Sienci-Labs/gsender/releases) then return here for the next step.

1. **Unplug** your spindle cable if it's plugged in.

1. **Update** your controller [Firmware](https://drive.google.com/drive/folders/17U2pXaYr7NKwKf4uNtjWcOmXRqfRYFb5?usp=sharing) then return here for the next step.

1. **Apply** the appropriate profile for your machine in gSender.

### Assembly Tips

* The articles are listed in the order they should be followed in, make sure you don't skip a page.

* Because of the assemblies, we strongly recommend having a second person available when installing the spindle onto the machine or when mounting a tool rack.

* Grab a set of **metric Allen keys**, as well as use the provided Allen keys. You can use a regular drill for screws that are M5 or larger, but **do not use impact drills** as they can strip the holes. Begin threading each screw by hand first to prevent cross-threading.  

* Keep components in their **original bags and boxes** until they are needed. The labels will help you quickly identify the correct parts.

* Machine orientation follows this photo:

![](/_images/_atc/_atc_assembly/_before/atc_assembly_before-axis.jpg)

## Machine Preparation

    We need to get your AltMill to a "blank state," so that regardless of its size, version, and build journey (i.e. existing or new build), we can easily install your new ATC system! Completing these prep steps beforehand will make the process much smoother and help avoid unnecessary disassembly later.

1. Jog the machine towards the **front** for easier access during assembly.

1. Verify that the **second-to-last crossbeam** on your AltMill is oriented correctly. The flange should face the rear of the machine, unless you have a 4x8 machine, in which case it should face the front.

![](/_images/_atc/_atc_assembly/_before/atc_assembly_before-fillercbeam.jpg)

1. Power off your **SLB-EXT controller**, and unplug it from power.

1. Got a **wasteboard** installed?
    * Ensure the last 13 inches at the back of the machine is not covered. You can cut it now, or remove it entirely for the duration of the ATC installation.

1. Got a **gControl panel** installed?
    * Unplug it from power, and remove the gControl and its mounting bracket.

1. Got a **Z-Plus Drag Chain Arm** installed?

    * Remove it from the Z-axis gantry, it is not needed for the ATC. Keep the end links on the drag chain.

    ![](/_images/_atc/_atc_assembly/_before/atc_assembly_before-zplus.jpg)

1. Got a **non-ATC spindle** installed?

    i. Unplug the spindle cable, and remove the spindle and spindle mount from the Z-axis.

    ii. If your drag chain clips are closed, open them all up with a flathead screwdriver.

    iii. Free the existing, **non-ATC spindle cable** from the drag chains.  Once the cable is removed, leave approximately 1 in 10 clips in place to keep the existing wiring organized.

    iv. Disconnect the **non-ATC spindle cable** and **RS485 cable** from the VFD. Remove the VFD from its mount and store it safely.

    From the above list, double check that you've done everything that applies to your AltMill, then continue with [**Spindle Setup**](https://resources.sienci.com/view/atc-spindle-setup/)!
