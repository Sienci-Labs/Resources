---
title: MK2 Specifications
menu_order: 2
post_status: publish
post_excerpt: Full specifications for the LongMill MK2 CNC machine.
post_date: 2022-03-21 20:31:00
taxonomy:
    knowledgebase_cat: lmk2-the-basics
    knowledgebase_tag:
        - mk2
custom_fields:
    KBName: LongMill MK2 CNC
    basepress_post_icon: bp-caret-right
skip_file: no
featured_image: _images/_lmmk2/_handbook/lmk2_knowcnc_Your-CNC-Assembly-View.png
---

## Capabilities

The LongMill MK2 is a benchtop CNC with most features any hobby user wants, including small-scale production within the comfort of one's own shed or home shop. The balance of ease-of-use, cost, and rigidity is one that we think is fairly unique in the hobby CNC world, and when paired up with other accessories, serves green and more experienced CNC hobbyists alike. It can accomplish a variety of tasks such as:

- Large sign lettering or full sign routing
- Intricate v-carving and inlays
- Furniture work and joinery
- Slab flattening
- Children's toys and household items
- Wall art and gifts to friends and family

The MK2 can comfortably carve a variety of materials including **hard and soft woods, plastics, foams, and waxes**. It can even produce acceptable work on soft metals like **aluminum, bronze, copper,** or can be equipped with other accessories like a drag knife, engraving tool, or laser diode to **cut vinyl, card stock, cardboard**, and **engrave ceramics, glass, and metals**.

![](/_images/_lmmk2/_handbook/lmk2_knowcnc_materials-on-the-MK2.jpg){.aligncenter .size-medium}

## Anatomy and Machine Dimensions

The MK2 is a 3-axis CNC that comes in three sizes. Each axis is lead screw driven to increase rigidity and maintain accuracy in the X-axis (left-to-right), Y-axis (forward and backward), and Z-axis (up and down, cutting into the material).

![](/_images/_lmmk2/_handbook/lmk2_knowcnc_Your-CNC-Assembly-View.png){.aligncenter .size-medium}

 Complete **machine dimensions** can be found here for all sizes:<a href="https://sienci.com/wp-content/uploads/2021/12/LongMill-MK2-48x30-30x30-and-12x30-dimensions.pdf" target="_blank" rel="noopener"> LongMill MK2 Drawing PDF</a>

## Carton Sizes & Weights

For the 12x30 and 30x30:

- One Package, 41.5″x9″x11″, 60lb

For the 48x30:

- Package 1, 41.5″x9″x11″, 45lb
- Package 2, 60″x6″x6″, 20lb

## Requirements & Specs

**Power Requirements:**

We recommend allocating **two 15A 110V/120V single phase circuits**:

Circuit 1

- 2.5A to the SLB controller
- 6.5A to the AutoSpin or Makita router
- Power to the desktop, laptop, mini-PC, or SBC (i.e. single board computer, like a Raspberry Pi)

Circuit 2

- Power to your dust management system whether it's a vacuum or dust collector (separate circuit will reduce static buildup/EMI issues)

       Router and SLB controller will use a North America NEMA 5-15P power plug. If you live in a country with 220V/240V power, you should use a transformer to convert to 110V/120V for the SLB controller.

![](/_images/_lmmk2/_the-basics/lmk2_mk2-specs-ps.jpg){.aligncenter .size-medium}

**Operating temperature:** expect reliable operation between 5 🠚30°C shop temperature (can be colder or hotter outside), as long as you give your machine time to acclimate to its environment to avoid cold-running and moisture build up on the electronics. Using these methods some users have reported running in as low as -20°C, though wireless mice or keyboards reportedly become unreliable.

**Operating humidity:** best results will occur from a balanced humidity (40-60%), too high and you can expect the moisture to degrade or even short the electronics, cause higher dust buildup, and swell the MDF wasteboard. Dry air can cause static charges to build up more easily, so a poorly grounded machine will experience electronic disruptions.

**Storage:** all components have a wide operating temperature range such as -20 🠚 50°C for the stepper motors, -40 🠚 120 °C for delrin parts, -40 🠚 85°C for the control box, and -40 🠚 105 °C for the motor connectors. As long as the MK2 is kept stationary and at a mild ambient humidity (40-60%), it can survive being stored at nearly any temperature.

**Max cutting speed:** 4000 mm/min (157.5 ipm) in X and Y, 3000 mm/min (118.1 ipm) in Z.

**X & Y-axis motion:** Delrin v-wheels on high rigidity extruded aluminum rails with custom adjusting eccentric nuts.

**Z-axis motion:** MGN12 recirculating ball bearing linear guide blocks, running on precision ground hardened steel rails.

**Power transmission:** 12.6kg-cm (175oz-in) NEMA 23 steppers driving 4-start, 2mm pitch, 8mm lead, 8mm diameter ACME lead screws via anti-backlash tensioning nuts to 6.35mm (1/4″) steel gantry plates.

**Router / spindle:** can run in 15000 - 25000 RPM range with reliable speed feedback, 0-5V PWM control for spindles. Router / spindle cannot exceed 2.7kg (6 lbs).

**Electronics:** SuperLongBoard 5xHAL uses an STM32F412 chip running grblHAL powering four TMC2660C motor drivers. The LongBoard uses an Arduino Uno running grbl v1.1h powering four 4A TB6600 motor drivers.
