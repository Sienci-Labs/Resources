---
title: ATC Final Checks
menu_order: 9
post_status: draft
post_excerpt: Now that you are setup and running, let's pick up a couple tools and try out the tls.
post_date: 2026-02-10 11:50:53
taxonomy:
    knowledgebase_cat: atc-assembly
    knowledgebase_tag: 
custom_fields:
    KBName: AutoToolChanger
    basepress_post_icon: bp-caret-right
skip_file: no
featured_image: _images/post-image.jpg
---

Now that you have the ATC assembled, let's make sure the system is functional. We will go through the **basic ATC processes that should be done each time you run a new job:**

1. [Load Tool Rack](#load-tool-rack)
1. [Run Homing Cycle](#run-homing-cycle)
1. [Set Up Tool Names](#set-up-tool-names)
1. [Load a Tool](#load-a-tool)  

Any issues you have with these processes may indicate there is a mis-assembled or faulty part, we would recommend going back to previous pages to check the assembly.

## Load Tool Rack

1. Let's get some tools loaded! Loosen the collet nut from each tool holder you are using. If secured tightly, use the set of wrenches that come with the ATC kit.

![](/_images/_atc/_atc_assembly/_finalcheck/atc_assembly_finalcheck-nut1.jpg){.aligncenter .size-medium}

1. Grab the bits that you plan to use for your first project. Insert them into ER20 collets. Your kit comes with ER20 collets that fit 1/8″, 1/4″, 3/8″, and 1/2″ tools.

1. Seat the collet and bit into a collet nut, then secure them to a tool holder using the set of wrenches provided. Ensure the face of the collet is flush with the tool holder. Repeat for the remaining bits.

![](/_images/_atc/_atc_assembly/_finalcheck/atc_assembly_finalcheck-fasten1.jpg){.aligncenter .size-medium}

![](/_images/_atc/_atc_assembly/_finalcheck/atc_assembly_finalcheck-colletbt.jpg){.aligncenter .size-medium}

1. Slide the assembled tools onto the rack, the bits should be facing down.

1. To keep track of what tools you have on your rack, we suggest writing them down in a list, on a piece of paper. For example:

`Tool 1: 1/4" Flat End Mill`

`Tool 2: 1/16" Compression Bit`

`Tool 3: 22mm Surfacing Bit`

`Tool 4: 1/8" Flat End Mill`

`Tool 5: 30 Degree V-Bit`

`Tool 6: 1/8" Tapered Ball Nose Bit`

    ⚠️ Please note, Tool 1 is at left-most position on the rack, we count from left to right.

![](/_images/_atc/_atc_assembly/_finalcheck/atc_assembly_finalcheck-toolnum.jpg){.aligncenter .size-medium}

## Run Homing Cycle

After connecting to gSender, home your AltMill - this is required to use your ATC.

![](/_images/_atc/_atc_assembly/_finalcheck/atc_assembly_finalcheck-home.jpg){.aligncenter .size-medium}

If the limit switches are set up correctly and undamaged, you should be able to home successfully.

## Set Up Tool Names

1. You should see the ATC tab on the bottom right of gSender. Select the Tools button with the chart icon.

![](/_images/_atc/_atc_assembly/_finalcheck/atc_assembly_finalcheck-atctab.jpg){.aligncenter .size-medium}

1. Rename the tools to match what is on your rack, using the written list you have made. **Renaming does not impact tool changing functionality**. It is only there to remind you of what tools are on the rack.

![](/_images/_atc/_atc_assembly/_finalcheck/atc_assembly_finalcheck-rename.jpg){.aligncenter .size-medium}

## Load a Tool

Now we have done all the preparations, let's try changing out a tool!

1. Under the ATC tab, select Load.

1. Using the dropdown, choose the tool number. In this example we want to load Tool 5 (T5) -- the 5th tool on the rack, starting from the left. Press Load.

![](/_images/_atc/_atc_assembly/_finalcheck/atc_assembly_finalcheck-load1.jpg){.aligncenter .size-medium}

1. The machine will move to Tool 5, grab it, then probe the bit using the TLS. You should now see T5 loaded on the ATC tab.

![](/_images/_atc/_atc_assembly/_finalcheck/atc_assembly_finalcheck-load2.jpg){.aligncenter .size-medium}

Congrats on your first successful tool change!

To learn how to **generate compatible g-code** and **run a job with automated tool changing**, head over to [1st Projects](https://resources.sienci.com/view/atc-1st-project/) page.

## Troubleshooting

If you were unable to load the tool successfully, or saw errors during the process, see below for potential resolutions.

### Machine loaded the wrong tool

- Check the tool numbers again, remember the left-most position on the rack is Tool 1 (T1)
- Check the rack, you may have installed the wrong tool

### There is a constant, air hissing/leaking sound

- Make sure you have gone through the [ATC Software](https://resources.sienci.com/view/atc-software/) setup page.

### Stopped a tool change using the E-stop, machine cannot jog or load tool now

- Turn off/on the controller, reconnect to gSender, press/release E-stop, then press Click to Unlock Machine on the screen. Home the machine, then try loading a tool again.

### Getting a "keep-out" error

- This is normal, it is to prevent the machine from jogging into the rack. Ensure the machine is away from the rack area.
