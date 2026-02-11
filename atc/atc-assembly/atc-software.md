---
title: ATC Software
menu_order: 6
post_status: draft
post_excerpt: Setting up gSender to work with the atc.
post_date: 2026-02-10 11:47:53
taxonomy:
    knowledgebase_cat: atc-assembly
    knowledgebase_tag: 
custom_fields:
    KBName: AutoToolChanger
    basepress_post_icon: bp-caret-right
skip_file: no
featured_image: _images/post-image.jpg
---
Here’s a clean, well-structured **Markdown** version, organized into clear sections and ordered steps so it reads like a setup guide rather than notes. I preserved your warnings and flagged “open” items subtly without rewriting intent.

---

## Software Setup

1. Plug the **VFD power cable** into an outlet and turn on the power switch at the bottom of the VFD.
2. Turn on the **SLB-EXT** using its toggle switch.

---

## Initial Hardware Checks

* Verify the **rack sensor** is lit.

  * It should be on if the rack has been installed correctly.

* Press the **Tool Length Sensor (TLS)**.

  * Confirm the **orange TLS LED** on the SLB-EXT turns on.

* Check air pressure status:

  * The **white Pressure LED** on the spindle should be on.
  * If the light is **red**:

    * Check the air compressor gauge
    * Check the filter regulator gauge
    * Ensure the ball valve is open

⚠️ **Note:**
The first time you connect to **gSender** with the spindle connected, air will leak because the system has not yet been configured.

---

## gSender Setup

> *Consider introducing tool slot order here (e.g. Tool Slot 1 is left-most) to aid configuration.*

1. Open **gSender** and connect to your machine.
2. Go to **Tools**.
3. Confirm the **SD card** is inserted.

   * We strongly recommend using the SD card provided with your kit.
   * Other SD cards may require reformatting.

### Controller Configuration

* During **Controller Configuration**, press **Apply**.
* You should hear the air leak **stop** once configuration is applied.

### Rehoming

* At the **Rehome** stage:

  * The machine should home **each axis individually**.

---

## Rack Position (Utility)

⚠️ **Caution:**
Move slowly. Avoid crashing the **stud finder** or **spindle nose**.

1. Jog the machine to the **back**.

2. Jog to the **right** until the stud finder sensor triggers over the **right-most tool holder**.

3. Use **precise jog** (small taps only) to get approximately:

   * **1 mm** or **1/16 in** above the stud finder

4. Press **Finding** to begin the rack probe sequence.

   * The machine will move in a small grid pattern to re-locate the stud.

5. The process will repeat for the **left-most tool holder**.

### Probed Rack Offsets

* Offset values are calculated using:

* Home position → center of the **last tool holder** *(confirm left-most vs right-most)*

1. Press **Continue** to return the machine to the home position automatically.

## Tool Length Sensor Position

* You may probe using the **spindle nose** directly on the TLS.
* If probing with a tool:

  1. Manually install a **tool holder and bit**.
  2. Press the **drawbar button** to insert the holder.

### Recommended Tooling

* Use a **flat end mill** for best accuracy.
* Do **not** use:

  * Surfacing bits
  * Asymmetric tools

## Spindle Configuration

1. Reconnect to the machine in gSender.
2. Complete the **Modbus configuration**.
3. After the wizard completes:

   * **Home the machine**

Once complete, the following tabs should appear in gSender:

* **Spindle / Laser**
* **ATC**

## Functional Checks

Try the following to confirm everything is working correctly:

* **Pick Up Tool**
* Slowly jog toward the rack

  * Confirm the machine prevents entry into the lock-out zone
* **Probe Tool**
* Turn the **spindle ON**
* Run **spindle burn-in G-code**
