---
title: Third Party Spindles
menu_order: 3
post_status: publish
post_excerpt: Documentation on sourcing a third-party spindle for your AltMill or LongMill.
post_date: 2026-06-02 15:09:42
taxonomy:
    knowledgebase_cat: spindlevfd-handbook
    knowledgebase_tag:
        - spindlevfd
custom_fields:
    KBName: Spindle VFD
    basepress_post_icon: bp-caret-right
skip_file: no
featured_image: 
---

While the Sienci Labs spindle kits offer a plug-and-play experience with your machine, there is an overwhelmingly large variety of spindle options one can choose from. Some of these options may be pre-assembled, plug-and-play kits with their own support, and others may be standalone parts that will require you to purchase individual parts and wire up the system yourself.

It should be noted that **our technical support for setup of 3rd party spindle kits is limited.** General guidelines for wiring a third-party spindle to your SLB/SLB-EXT controller can be found in our [technical manual](https://resources.sienci.com/view/slb-manual/#spindlers485).

When sourcing your own spindle, there are a few key variations which you should consider:

## Spindle Size

- 1.5 kW, and 2.2 kW spindles will typically exist in an 80mm diameter which will fit an AltMill out-of-the-box
- 3 kW, 3.5 kW, and 4+ kW spindles will typically exist as 100mm diameter, or will be of a ‘square’ profile which will require a custom mounting solution
- The AltMill can comfortably utilize much more powerful spindles in the range of 4kW+, as well as support the extra weight of such units on the Z-axis.
- The LongMill should stick with 1.5KW spindles as the Z-axis cannot support heavier spindles.

![](/_images/_spindlevfd/_spindlevfd_handbook/spindlevfd_largespindle.jpg){.aligncenter .size-medium}

## Cooling Method

### Air Cooling

- Air cooled spindles (like the Sienci Labs 1.5kW and 2.2kW) utilize a centrifugal fan to pull air through the body of the spindle to keep things cool. Due to the fan type, these tend to be much quieter than the axial fans used in trim routers.
- This type provides adequate cooling in almost all scenarios, but can be a concern if you are consistently using your spindle at its minimum RPMs (~7500 RPM), and operating in a very hot environment.

### Water Cooling

- Water cooled spindles utilize a supply of water flowing through channels inside the spindle body to cool the spindle. The setup for this is a bit more involved, and requires water lines to be run through the drag chains of your machine, going to a water pump and water reservoir under or near your machine.
- Another key consideration is that these spindles should never be run without water actively flowing through it, as this will cause damage.
- Water cooling lines should be no greater than 10mm outer diameter, but be reasonably stiff so that the tube cannot kink when bent.

## Auto Tool Change (ATC) Capability

- [ATC spindles](https://resources.sienci.com/view/atc-welcome/) allow for the machine to automatically swap out cutting tools during a job. This requires perfectly coordinated movements between the ATC spindle mechanism, and movements of the AltMill in X, Y, Z to function correctly.
- This is a very complicated, expensive system requiring things such as pneumatic solenoids, individual tool holders, a tool holder rack, air compressor, and tool length sensor. A complete system may end up costing over $4000 CAD, therefore it is typically recommended for those running their machines for production/business use.

## Collet Size

Spindles use ER collets. The ER size indicates the largest tool diameter you can use on your spindle.

| Collet Size | Largest Tool Diameter (in) |
|-------------|----------------------------|
| ER11        | 1/4                        |
| ER16        | 3/8                        |
| ER20        | 1/2                        |
| ER25        | 5/8                        |

![](/_images/_addons/addons_common/spindlevfd_colleter20.jpg){.aligncenter .size-medium}

## Differences between VFD Models

### Power

Some VFD models will be rated for different amounts of power. The VFD should be matched with the spindle you’re using, either meeting or exceeding the rating of the spindle (ie. a 2.5kW VFD with 2.2kW spindle is okay).

### Voltage

Models can also vary by AC power voltages. For 110/120V power found in most households with a 15A current breaker, you’ll be limited to a power rating of 1.5kW in most cases. If you have a 20A current breaker, you may be able to use a 110/120V, 2.2kW VFD however this is not recommended.

![](/_images/_spindlevfd/_spindlevfd_handbook/spindlevfd_vfdbottom.jpg)

### RS485 Compatibility

The SLB/SLB-EXT controller has plug-and-play support for RS485 control of only certain VFD units such as: Huanyang V1, Huanyang P2A, Durapulse GS20, Yalang YS620 and H-100. Setting up RS485 control for other VFD models is possible using the ‘MODVFD’ customizable profile, but be warned that this can be [quite involved](https://resources.sienci.com/view/slb-manual/#vfd-settings) and **support cannot be guaranteed for all VFD models.** RS485 control is also not found on every VFD unit.
