---
title: Tool Length Sensor
menu_order: 7
post_status: publish
post_excerpt: Setting up and using the TLS.
post_date: 2026-05-20 15:34:21
taxonomy:
    knowledgebase_cat: addons-common
    knowledgebase_tag:
        - addons
custom_fields:
    KBName: Add-ons
    basepress_post_icon: bp-caret-right
skip_file: no
featured_image: 
---

For video instructions on how to mount and set up your TLS, see the video below.

https://youtu.be/fswJHOhdZgE

## Mounting

You will need to decide on a location for your TLS. Ideally it is somewhere at the edge of the machine’s travel area, that doesn't trigger hard or soft limit alarms from the limit switches.

❗Please note you must have limit switches installed on your machine in order to use the TLS.

### AltMill

- We recommend mounting onto the right Y-axis rail as it is clear of drag chains

- Mount the TLS by inserting two (2) T-nuts into the T-slot of the right Y-axis rail. Then fasten the screws into the T-nuts, so that the TLS is hanging from the rail.

![](/_images/_addons/addons_common/addons_tls-rail1.jpg){.aligncenter .size-medium}

- For the **AltMill MK1**, you will need to temporarily disassemble the dust shield to mount the TLS. Afterwards, put the dust shield back on, **over top of the TLS**, to prevent premature wear of linear guides and ball screw

![](/_images/_addons/addons_common/addons_tls-ammk1-dust1.jpg){.aligncenter .size-medium}

### LongMill and other CNCs

- Flip the TLS base so that it can sit flat, then screw it into the wasteboard of the desired location which can be reached by the router spindle, with two (2) wood screws.

![](/_images/_addons/addons_common/addons_tls-wasteboard1.jpg){.aligncenter .size-medium}

## Cable Connection

Attach the connector from the TLS to the TLS cable.

Then install cable clips on the T-slots in the crossbeams, routing from the SLB/SLB-EXT controller to the location of your TLS.

Finally, connect the other end of the TLS cable to the controller.

![](/_images/_atc/_atc_assembly/_toolrack/atc_assembly_tool-cableroute3.jpg){.aligncenter .size-medium}

## gSender Setup

1. Download and install the latest version of gSender (**1.6.2 or above**). Detailed instructions can be found in [this article](https://resources.sienci.com/view/gs-installation/).

1. Connect to gSender.

1. Install your longest end mill into the spindle. This is to ensure there is enough clearance during tool changing.

1. Jog the machine so the end mill is positioned over the center, slightly above the TLS.

1. Go to Config, and under the Tool Changing tab, adjust the following settings:

    - gSender strategy  
        - Select “Fixed Tool Sensor”
    - Fixed sensor location
        - Press the Grab button
    - First tool behaviour
        - “Prompt for first tool”
    - Set tool change location
        - Toggle ON

    ![](/_images/_addons/addons_common/addons_tls-tcconfig.jpg){.aligncenter .size-medium}

1. Go to the Probe tab, for Invert Probe Inputs ($6) disable the Toolsetter.

    ![](/_images/_addons/addons_common/addons_tls-prbeconfig.jpg){.aligncenter .size-medium}

1. Go to the More Settings tab, for Tool Change Mode set to Normal

    ![](/_images/_addons/addons_common/addons_tls-moresetconfig.jpg){.aligncenter .size-medium}

1. Go to the Spindle/Laser tab and adjust these settings:
    - Spindle/laser controls
        - Toggle ON
    - Spindle on delay ($394)
        - 11
    - Spindle off delay ($539)
        - 11

    ![](/_images/_addons/addons_common/addons_tls-spinconfig.jpg){.aligncenter .size-medium}

1. Apply the settings, then turn OFF/ON the controller

1. Re-connect to gSender

1. Jog the machine to a place on your wasteboard where you can conduct a manual tool change safely

1. Navigate to Tool Changing tab then adjust the Manual Tool Change Location
    - First press Grab button to get the X and Y values
    - Then enter 0 for the Z, so that collisions do not occur

    ![](/_images/_addons/addons_common/addons_tls-manualconfig.jpg){.aligncenter .size-medium}

1. Apply the settings, then turn OFF/ON the controller

### Testing

To make sure that the TLS is working as expected, **press down** on the TLS.

- On gSender, select Machine Info (circuit board icon) and you should see the Probe signal turn **green**.

![](/_images/_addons/addons_common/addons_tls-probecheck.jpg){.aligncenter .size-medium}

- On the controller, the TLS orange light will turn **OFF**.

❗Note that this light will stay OFF if TLS is disconnected

![](/_images/_addons/addons_common/addons_tls-statuslight.gif){.aligncenter .size-full}

## Export g-code on CAM

On your CAM program, you will need to adjust your g-code export settings to allow you to run tool changes. This will involve injecting M6 and T# commands between each toolpath, so that all the toolpaths can be saved onto one g-code file.

### Vectric

The default grbl post-processor does not support tool changing, you will need to use the Sienci Labs ATC post-processor.

1. Under Machine, select Machine Configuration.

    ![](/_images/_addons/addons_common/addons_tls-addpp1.jpg){.aligncenter .size-medium}

1. Add a new post-processor using the + button.

    ![](/_images/_addons/addons_common/addons_tls-addpp2.jpg){.aligncenter .size-medium}

1. There are two Sienci Labs post-processors available, select the **Sienci Labs ATC** for regular 3-axis milling. Otherwise you can come back to this window to add the Sienci Labs Vortex ATC, if you have a Vortex.

    i. If you cannot see the post-processor, press the cloud with arrow button to automatically download the latest ones.

    ![](/_images/_addons/addons_common/addons_tls-addpp3.jpg){.aligncenter .size-medium}

    ii. If you still cannot see them, you can download and install them on your own. Instructions on installation can be found on [Vectric’s website.](https://docs.vectric.com/docs/V12.0/VCarvePro/ENU/Help/form/post-processor-management/index.html)

    - [Post-processor for regular 3-axis milling](https://drive.google.com/file/d/1mgyv90uslGa4Cadq8EKwFjALcVChzU34/view)

    - [Post-processor for the Vortex rotary axis](https://drive.google.com/file/d/1tEr16-cVp_aaULNH_i3Dd5rDd4RDe02K/view)

---
    ❗If you run into an error while exporting, it may be because you have duplicated tool numbers. Since all this g-code is in one file, you must have unique tool numbers (T#) assigned to each toolpath. For each toolpath, go into the tool library and replace the tool numbers using different whole numbers (e.g. 1, 2, 5, 12). Then try exporting again.
---

### Carveco

Carveco’s default grbl post-processor does not support tool changing.
You will need to download and install this [post-processor](https://drive.google.com/file/d/1UqWXNDYrgd2CR3ci91QXc0FMH09GMZRi/view).

![](/_images/_atc/_atc_basics/atc_basics_firstpro-carvecoexport.jpg){.aligncenter .size-medium}

### Fusion 360

⚠️ Please note tool changing is only available with a Fusion360 subscription.

Fusion has the ability to toggle on tool changing g-code. When exporting the g-code, adjust the following settings.

- **Output M6:** Yes

- **Output Tool Number:** Yes

![](/_images/_atc/_atc_basics/atc_basics_firstpro-autodeskexport.jpg){.aligncenter .size-medium}

## Run a Job on gSender

1. Once the g-code has been saved to your computer, open gSender and **connect** to your machine.

1. **Home** the machine. You must have limit switches installed to do homing, otherwise you cannot use the TLS.

    ![](/_images/_atc/_atc_basics/atc_basics_firstpro-congsender.jpg){.aligncenter .size-medium}

1. Load the g-code file.

    You should see the **Tool Timeline** on the left side which shows the different toolpaths.

    ![](/_images/_addons/addons_common/addons_tls-tooltimeline.jpg){.aligncenter .size-medium}

1. With your stock material secured on the wasteboard, set your X, Y Z zeros by either using a touch plate or manually.

1. Press **Run Job**! The tool change wizard will pop up, you will be prompted to either probe the tool length or do a full tool change.

    Select the **probe tool length option** - this causes the machine to move upwards to a safe height, then will move to probe the TLS.

    Finally it will start your job. The spindle will spin up, and the machine will start cutting!

        ⚠️ Make sure the AutoZero touch plate is put away so that it does not trigger. Otherwise it will cause a false reading that will affect the TLS operation.

    The spindle and machine will pause at each tool change, as the wizard guides you through each step on-screen.
