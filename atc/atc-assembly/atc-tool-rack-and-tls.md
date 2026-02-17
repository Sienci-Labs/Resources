---
title: ATC Tool Rack & TLS
menu_order: 5
post_status: draft
post_excerpt: Connecting your tool rack(s) and setting up your tool length sensor.
post_date: 2026-02-10 11:38:53
taxonomy:
    knowledgebase_cat: atc-assembly
    knowledgebase_tag: 
custom_fields:
    KBName: AutoToolChanger
    basepress_post_icon: bp-caret-right
skip_file: no
featured_image: _images/post-image.jpg
---

## Rack & TLS Installation

> **No rack?** Skip ahead to the **TLS Cable** section in this article.

## Unboxing

### Rack Components

![](/_images/_atc/_atc_assembly/temp/IMG_0890.JPG)

* Cross support extrusion
* Rack sections (**4 total**)

  * 2 mirrored pieces
  * 2 identical pieces
* Tool holders (**6 included**)

  * Remaining 6 may be in the spindle foam in the main box
* Backbone
* Inserts / clips

### Hardware Bag

* Knobs
* Fasteners (Are the black screws M5 or M6? The short ones)

### Sensor Bag

* Tool rack sensor
* Tool rack sensor cables

### Collet Box

* ER20 collet set *(if not in main box)*

## Rack Assembly

1. Grab the **rack sections** and identify:

   * The back right and back left, which are the mirrored pair of sections
   * The front, which are **two identical sections**

![](<../../_images/_atc/_atc_assembly/temp/Screenshot 2026-02-12 at 4.54.50 PM.png>)

2. Place **one mirrored rack section** onto one end of the **cross support extrusion**.

   * Align with the threaded holes.
   * Fully secure using **two M6-14mm screws** at the extrusion end.

3. Insert a **T-nut** into the extrusion slot. (Is it just the roll in T-nuts that fit in here? Will customers with MK1 get twist in AND roll in?)

   * Ensure correct orientation of the T-nut in the slot. 

      ![](/_images/_atc/_atc_assembly/temp/IMG_0896.JPG)
(Need to rotate this photo 180!!!!!)

   * Slide it to align with the rack hole.
   * Secure using **one M6-8mm button head screw**.

4. Loosely place the **second mirrored rack section** on the opposite end of the extrusion.


Put two (2) M3-20mm screws into the tool rack sensor. (not any longer otherwise will interfere with rack section)

6. Mount the **tool rack sensor** onto the **back right rack section**:

   * Position the sensor at the slot.
   * Secure with the pre-installed screws.
   Position the pigtail from the sensor into the rectangular cutout

    ![](/_images/_atc/_atc_assembly/temp/IMG_0901.JPG)

    ![](<../../_images/_atc/_atc_assembly/Screenshot 2026-02-12 at 5.21.05 PM.png>)

   ![](/_images/_atc/_atc_assembly/temp/IMG_0903.JPG)

   ![](/_images/_atc/_atc_assembly/temp/IMG_0899.JPG)


7. For the other mirrored rack section:

   * Fully secure the **two M6 screws** at the extrusion end.
   * Insert the T-nut and fasten using **one M6 × 8 mm button head screw**.

Before continuing, make sure the tool rack sensor is secured onto the rack section, in the correct position and orientation, as shown in the picture below: 
![](<../../_images/_atc/_atc_assembly/temp/Screenshot 2026-02-12 at 5.15.52 PM.png>)

## Backbone Assembly

1. Grab the **backbone**, **inserts**, and **M4-8mm screws**.

2. Position each insert onto the backbone so it sits **flush**.

   * Hold the insert snug while threading in the screws.
   * Continually check that each insert remains fully seated.

   ⚠️ **Important:** Improperly seated inserts can cause **ATC accuracy issues**.

3. Repeat until all inserts are installed along the backbone.

## Joining Rack Sections

1. Take the **remaining identical rack sections** and align them based on your machine type:

   * **2×4** – furthest set of holes
   * **4×4 MK2 / 4×8** – closest set of holes
   * **4×4 MK1** – middle set of holes

2. Secure each connection using **two M6 × 8 mm screws**.

## Backbone Assembly Mounting

*** we can put this onto the rack so the rack and backbone are on together at the same time. But the backbone position just needs to be adjusted to push against the front left via the knobs loosening. Edit this later

1. Orient the backbone so the **inserts face the back of the machine**.

2. Place the backbone into the gap of the rack extrusion assembly, against the **front crossbeam**.

3. Push the backbone toward the **front-left** of the machine.

4. Secure it using the **knobs** on the studs.

5. If installing a **second tool rack**:

   * Repeat the above steps
   * Install it directly next to the first rack, **butted against the backbone**

   ⚠️ This is required for **automated setup in gSender**.

6. Install tool holders into the **first and last slots**.

   * Ensure each holder is fully seated
   * The insert must engage the groove on the tool holder

## Rack & Extrusion Assembly Mounting

 If the machine is not already jogged forward:

   * Power on the controller
   * Connect to **gSender**
   * Jog the machine forward as needed

1. Select the correct **T-nuts** for your machine:

   * **MK1** – Roll-in T-nuts
   * **All other AltMills** – Twist-in T-nuts

![](<../../_images/_atc/_atc_assembly/temp/Screenshot 2026-02-12 at 5.05.49 PM.png>)

2. Pre-assemble:

   * **Four (4) M6 × 8 mm button head screws**
   * **Four (4) T-nuts**



4. Bring the **rack and extrusion assembly** to the **back-right corner** of the AltMill.

   * Confirm rack flanges sit flush with the crossbeam faces.
   * If not, revisit rack section hole placement.

5. Slide **two pre-assembled M6 fasteners** into the crossbeam T-slot where the rack will mount.

6. Lift the rack assembly under the crossbeams and hook the rack flanges onto the M6 fasteners.

7. Position the assembly so:

   * It butts against the AltMill leg
   * The rack flange butts against the **front crossbeam**

8. Hold the assembly in place and tighten the M6 fasteners.

## Tool Rack Sensor Cable Routing

1. Route the **tool rack sensor cable** through the cable clips in the crossbeam.

   * For **4×8**, route the cable **underneath** the cable track.

2. Connect:

   * **Female end** → tool rack sensor
   * **Male end** → daughter board on the SLB-EXT

     * Use **Rack 1** or **Rack 2** port

## TLS Cable

1. Route the **TLS cable** through the cable clips:

   * Leave the **green connector** end at the SLB-EXT
   * Leave the **black Molex connector** at the back-left of the AltMill

2. Plug the **green connector** into the **TLS port** on the SLB-EXT.



## TLS Mounting

* If using the TLS **without an ATC**, you may mount it anywhere convenient.
* With an ATC installed, the **recommended location** is:

  * **Back-right corner of the AltMill**, next to the tool rack

1. Pre-assemble **two (2) M5 screws** with **T-nuts** on the TLS.

2. Slide the TLS into the **right Y-axis rail T-slot**.

3. Secure the TLS by tightening the M5 fasteners.

4. Plug the **black Molex connector** from the TLS cable into the TLS.
