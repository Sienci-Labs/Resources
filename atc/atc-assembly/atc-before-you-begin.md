---
title: ATC Before You Begin
menu_order: 1
post_status: draft
post_excerpt: 
post_date: 2026-02-09 11:44:53
taxonomy:
    knowledgebase_cat: atc-assembly
    knowledgebase_tag: 
custom_fields:
    KBName: AutoToolChanger
    basepress_post_icon: bp-caret-right
skip_file: yes
featured_image: 
---

## Before You Begin

If you’re installing the ATC on a **new machine build**, great. We ask that you complete the [AltMill Assembly Process](https://resources.sienci.com/view/am-mk2-best-practices/) up to and including stage **9 First Movement** before returning to this guide.

The expected ATC assembly time is **2–4 hours**, so be sure to allot enough time and pace yourself to avoid errors, damage, or injury during the process.

### Assembly Tips

- **Take breaks when needed**

  The assembly process can take a few to several hours. Pace yourself and enjoy the process — after all, you are learning CNC as a hobby!

- **Read the instructions**

  Many issues during assembly can be solved by re-examining the instructions. Check that you didn't skip a page and that you completed the previous step correctly. Some steps are hard to explain and some parts have names that are difficult to remember, so looking closely at the pictures can help you better understand what needs to be done.

- **Use the correct tool**

  You may use a drill or impact driver for faster assembly, but begin threading each screw **by hand first** to prevent cross-threading. Be careful not to **over-torque fasteners**.

- **Get Help**

  Because of the **weight of the spindle**, we strongly recommend having a second person available when installing the spindle onto the machine or when mounting a tool rack.

- **Go slowly**

  To make the process easier, keep components in their **original bags and boxes** until they are needed. The labels will help you quickly identify the correct parts.

- **Remember the language**

  This manual uses both technical language and a visual language. Understanding these will make the assembly easier and help prevent mistakes.

#### Transparent Parts

![Transparent parts](https://resources.sienci.com/wp-content/uploads/2025/02/lmk2_unboxing_startend.png)

Outlined in blue with a blue arrow path to show where the part starts and where it ends up.

---

#### Rotation Arrows

![Rotation arrows](https://resources.sienci.com/wp-content/uploads/2025/02/lmk2_unboxing_loosefirm.png)

Blue arrows indicate a loose placement of the part.  
Red arrows indicate firm tightening to secure the part.

---

#### Caution Triangles

![Caution triangles](https://resources.sienci.com/wp-content/uploads/2025/02/lmk2_unboxing_caution.png)

Marks something that requires attention.

---

#### Large Green Circles

![Clarity circles](https://resources.sienci.com/wp-content/uploads/2025/02/lmk2_unboxing_clarity.png)

Provide a secondary view of the current step for additional clarity.

---

#### X, Y, and Z Axes

![XYZ axes](https://resources.sienci.com/wp-content/uploads/2025/02/lmk2_unboxing_xyzangles.jpg)

During assembly, capitalized axis letters refer to machine movement directions.

Viewed from the front of the machine:

- **X-axis:** left ↔ right (red)
- **Y-axis:** toward / away from you (green)
- **Z-axis:** up / down from the tabletop (blue)

## Access & Frame Preparation

Before starting your ATC installation, make sure your machine is properly prepared. Completing these steps ahead of time will make the installation smoother and help avoid unnecessary disassembly later.

### Wasteboard & Crossbeams

- If you have a **wasteboard** installed, ensure the last **13 inches** at the back of the machine is not covered. You can modify it now, or remove it entirely for the duration of the ATC installation — this will make installing the rack much easier.
- Verify that the **second-to-last crossbeam** on your AltMill is oriented correctly. The flange should face the rear of the machine, unless you have a 4x8 machine, in which case it should face the front.

### Jog Machine & Power Safety

- Jog the machine to a convenient position near the front for easier access when lifting the spindle into place.
- Power off your **controller** and **gControl computer** (if installed).
- Unplug all power, including the **VFD**, for safety.

## Machine Preparation

Prepare the machine by removing components that will be replaced or repositioned during the ATC installation.

🟦 **4x4 & 4x2 Machines**  
🟧 **4x8 Machines**  
🔁 **Upgrade Only**  
🆕 **New Build**

Follow the steps below and complete only those that apply to your setup.

---

### 🔁 Upgrade Only

#### Spindle & Motion Components

[Render] of spindle and mount coming off AltMill, autospin?

- Remove the spindle and spindle mount from the Z-axis.

#### Power & Electronics

[Render] of vfd wiring being removed and the drag chain being opened

Remove the existing control components to prepare for the ATC electronics.

- Open any remaining drag chain clips and free the VFD wiring from the drag chains. Once the cable is removed, leave approximately **1 in 10 clips** in place to keep the existing wiring organized.
- Disconnect the VFD cables and remove the VFD from its mount. Store it safely.
- Remove the E-stop and controller cable if required.
- Remove the **gControl** panel and its mounting bracket from the machine.

### 🟧 4x8 Machines

#### Drag Chain Preparation

[Render] Remove the z axis Drag chain arm, Remove the drag chain end-link from the arm, Reattach the end link to the Z-axis drag chain.

Prepare the drag chains for routing the ATC wiring.

- Disconnect the **Z-axis drag chain** from its end links.
- Remove the **drag chain arm**.
- Reattach one **end link** to the Z-axis drag chain and set it aside for later.

## Wrapping Up

Before continuing, confirm that your machine is in the correct state for ATC installation.

- **Rack installation:** Wasteboard is removed or does not cover the last **13 inches** at the rear of the machine.
- **Z-axis gantry:** Positioned where you can comfortably access it.
- 🔁 **Upgrading:** X and Y drag chains are partially unclipped.  
- 🟧 **4x8 upgrades:** The Z-axis drag chain arm has been removed and the chain with one end link is set aside.
- 🆕 **New builds:** The Z-axis drag chain is installed with spindle wiring and tubing already routed through it.

If your machine matches these conditions, you’re ready to continue with [**Spindle Setup**](https://resources.sienci.com/view/atc-spindle-setup/).
