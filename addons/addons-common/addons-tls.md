---
title: Tool Length Sensor
menu_order: 8
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

For video instructions on how to mount and set up your tool length sensor (TLS), see the video below.

https://www.youtube.com/watch?v=fswJHOhdZgE

## 3rd Party Compatibility

If you are installing the TLS onto a 3rd party controller or CNC, please check that your controller has a 3-pin input for the TLS, for **ground (GND)**, **signal** and **power (VCC)**. If your controller has only a 2-pin input, you will need to power the TLS externally with 5-24V, since it is an active sensor.

Review the documents below to ensure compatibility:

[TLS Sensor Diagram](https://resources.sienci.com/wp-content/uploads/2024/04/Sienci-Labs-TLS-Sensor-diagram.pdf)

[TLS Wiring Harness Diagram](https://resources.sienci.com/wp-content/uploads/2024/04/Sienci-Labs-TLS-harness-diagram.pdf)

[TLS Sensor Specifications](https://resources.sienci.com/wp-content/uploads/2024/04/TLS-Sensor-Sepcifications-Sheet.pdf)

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

![](/_images/_addons/addons_common/addons_tls-connect.jpg){.aligncenter .size-medium}

Then install cable clips on the T-slots in the crossbeams, routing from the SLB/SLB-EXT controller to the location of your TLS.

![](/_images/_addons/addons_common/addons_tls-cableclip.jpg){.aligncenter .size-medium}

Finally, connect the other end of the TLS cable to the controller.

![](/_images/_atc/_atc_assembly/_toolrack/atc_assembly_tool-cableroute3.jpg){.aligncenter .size-medium}

## gSender Setup

### gSender 1.6.3 or above

[su_spoiler title="gSender 1.6.3 or above" open="yes" style="fancy" icon="chevron" anchor_in_url="yes"]

If you have gSender 1.6.3 or above, you can go through the setup automatically through the wizard.

Go to Tools, Accessory Install, and select Sienci TLS.

![](/_images/_addons/addons_common/addons_tls-accessoryinstall.jpg){.aligncenter .size-medium}

Follow the steps to complete installation.

Some helpful tips:

When you **set TLS location**, use the longest end mill you have and jog the Z-axis to be about 0.5-1" above your TLS. This ensures there is enough height for your tool when probing.

![](/_images/_addons/addons_common/addons_tls-settlslocation.jpg){.aligncenter .size-medium}

When you **set tool change location**, jog the Z-axis all the way up, to the top of the machine travel. This ensures you can access the tool while changing it out.

![](/_images/_addons/addons_common/addons_tls-manuallocation.jpg){.aligncenter .size-medium}

[/su_spoiler]

### gSender 1.6.2

[su_spoiler title="gSender 1.6.2" open="no" style="fancy" icon="chevron" anchor_in_url="yes"]

If you have not upgraded gSender to 1.6.3. or above, you can still set up the TLS manually through the Config tab.

1. Make sure you have gSender **1.6.2** as older versions do not have TLS support. Detailed instructions can be found in [this article](https://resources.sienci.com/view/gs-installation/).

1. Connect to gSender.

1. **Check** your controller **firmware version** by clicking on the machine information (circuit board) icon. Write it down so you can refer to it later - it affects a setting we need to change.

    ![](/_images/_atc/_atc_assembly/_before/atc_assembly_beforeyoubegin-firmware2.jpg){.aligncenter .size-medium}

1. Jog the machine towards you and install your **longest end mill** into the spindle. This is to ensure there is enough clearance during tool changing.

1. **Home** the machine. You must have limit switches installed to do homing, otherwise you cannot use the TLS.

    ![](/_images/_atc/_atc_basics/atc_basics_firstpro-congsender.jpg){.aligncenter .size-medium}

1. Jog the machine so the end mill is positioned over the center of the TLS, slightly above the metal button.

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

1. Go to the Probe tab. We will change the setting **Invert probe inputs ($6)** based on the controller firmware version.

    **Firmware that starts with 2026 or higher** (e.g. 20260525, 20260318)
    - Probe ON
    - Toolsetter ON

    ![](/_images/_addons/addons_common/addons_tls-prbeconfig-invert.jpg){.aligncenter .size-medium}

    **All other firmware versions**
    - Probe ON
    - Toolsetter OFF

    ![](/_images/_addons/addons_common/addons_tls-prbeconfig.jpg){.aligncenter .size-medium}

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

1. Jog the machine to a place where you can change out your end mill safely and easily, like at the front of your machine. Then jog all the way **up on the Z-axis**, so you can access the tool during the change.

1. Navigate to Tool Changing tab, then find the **Manual tool change location**
    - Press the Grab button

    ![](/_images/_addons/addons_common/addons_tls-manualconfig.jpg){.aligncenter .size-medium}

1. Apply the settings, then turn OFF/ON the controller

[/su_spoiler]

## Testing

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

1. Finally, when saving your toolpaths to export as g-code, select **Visible toolpaths to one file.**

![](/_images/_addons/addons_common/addons_tls-addpp4.jpg){.aligncenter .size-medium}

---
    ❗If you run into an error while exporting, it may be because you have duplicated tool numbers. Since all this g-code is in one file, you must have unique tool numbers (T#) assigned to each toolpath. On Vectric, for each toolpath, go to tool library and replace the tool number with different whole numbers (e.g. 1, 2, 5, 12), then try saving again. Or you can do it manually - open your existing g-code file in a text-editing program (i.e. Notepad) and change every T# to be unique.
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

1. **Home** the machine.

    ![](/_images/_atc/_atc_basics/atc_basics_firstpro-congsender.jpg){.aligncenter .size-medium}

1. Load the g-code file.

    You should see the **Tool Timeline** on the left side which shows the different toolpaths.

    ![](/_images/_addons/addons_common/addons_tls-tooltimeline.jpg){.aligncenter .size-medium}

1. Install the **end mill** you are starting your job with.

1. With your stock material secured on the wasteboard, set your X, Y Z zeros by either using a touch plate or manually.

1. Press **Start** to run your job! The tool change wizard will pop up, you will be prompted to either probe the tool length or do a full tool change.

    Select the **Only probe tool length** option - this causes the machine to probe the TLS with your installed end mill.

    Finally it will start your job. The spindle will spin up, and the machine will start cutting!

        ⚠️ Make sure the AutoZero touch plate is put away so that it does not trigger. Otherwise it will cause a false reading that will affect the TLS operation.

    The spindle and machine will pause at each tool change, as the wizard guides you through each step on-screen.
