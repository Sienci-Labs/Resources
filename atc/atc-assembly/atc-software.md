---
title: ATC Software
menu_order: 8
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

For this software setup, if you have a **4x8 AltMill** you may want to grab a friend to help you with checking sensor position and lights on the ATC. Otherwise, be prepared to do some walking back and forth!

## gControl Panel

At this time you can reinstall your gControl panel and mount, [see mounting instructions here](https://resources.sienci.com/view/gc-gcontrol-assembly/).

## Power Up

1. Plug the **VFD power cable** into an outlet and turn on the power switch at the bottom of the VFD.
1. Turn on the **SLB-EXT** using its toggle switch, cycling the E-stop as usual.

## Initial Hardware Checks

1. Verify the **rack sensor** is on. It should be on if the rack has been installed correctly. There should be a red light coming from the rack sensor.

![](/_images/_atc/_atc_assembly/_software/atc_assembly_soft_rack.jpeg){.aligncenter .size-medium}

1. Check that the **tool length sensor (TLS)** is functioning.

    * Press down on the TLS (either manually or by jogging the spindle down slowly), and confirm the **orange TLS LED** on the SLB-EXT turns on.

![](/_images/_atc/_atc_assembly/_software/atc_assembly_soft_tls.jpeg){.aligncenter .size-medium}

1. Check the **white Pressure LED** on the spindle is on.

![](/_images/_atc/_atc_assembly/_software/atc_assembly_soft_airpressure.jpg){.aligncenter .size-medium}

* If the light is **red**:

  * Check the air compressor gauge
  * Check the filter regulator gauge
  * Ensure the quick-disconnect ball valve is open

⚠️ **Note:**
The first time you connect to **gSender** with the spindle connected, air will leak because the system has not yet been configured.

## gSender Setup

1. Open **gSender** and connect to your machine.
1. Go to **Tools**.
1. Go to **SD Card Manager**.
1. If you haven't yet, insert the **microSD card** into the slot on the SLB-EXT.

![](/_images/_atc/_atc_assembly/_software/atc_assembly_soft_accessory.jpg){.aligncenter .size-medium}

* We strongly recommend using the microSD card provided with your kit.
* Other SD cards may need to be reformatted to FAT32 and must not exceed a capacity of 32 GB.

### Accessory Installation

We will be using gSender to upload ATC-related g-code programs to the microSD Card.

1. Navigate back to the Tools tab, and click on **Accessory Installation**.

1. Select **Sienci ATC** to start the setup. This process should take approx 30 min.

![](/_images/_atc/_atc_assembly/_software/atc_assembly_soft_install.jpg){.aligncenter .size-medium}

1. Select **Initial Setup**.

![](/_images/_atc/_atc_assembly/_software/atc_assembly_soft_initial.jpg){.aligncenter .size-medium}

1. Select your **Rack Size**. For this example, we are selecting a 6 Tool Rack. Hit Upload Macros.

![](/_images/_atc/_atc_assembly/_software/atc_assembly_soft_macro.jpg){.aligncenter .size-medium}

1. Once complete, press Next in the bottom right corner.

### Controller Setup

1. This step will configure your controller. Hit the blue Apply button.
1. Once completed, hit Next.

![](/_images/_atc/_atc_assembly/_software/atc_assembly_soft_control.jpg){.aligncenter .size-medium}

1. Next, the machine will update its homing position. Hit the blue **Re-home button** to begin this wizard.
1. Once the button turns green and shows Complete, continue with the Next button. At this stage, the air leak at the spindle should **stop**.

![](/_images/_atc/_atc_assembly/_software/atc_assembly_soft_rehome.jpg){.aligncenter .size-medium}

### Rack Position

Next the rack location will be determined. You will be prompted to manually jog the ATC.

![](/_images/_atc/_atc_assembly/_software/atc_assembly_soft_rackpos.jpg){.aligncenter .size-medium}

1. Ensure **Automatic** is selected in the drop down menu.

    ⚠️ **Caution:** Move slowly. Avoid crashing the **stud finder** or **spindle nose**.

1. Assuming you start from the back left corner of the machine, you will be moving the spindle above the left-most tool holder.  

    Either manually jog, or:

        1. Set your speed to rapid and enter 1140 into your XY travel distance box, then hit the X+ arrow to move right.

        2. Set your speed to normal, enter 20mm into your XY travel distance box, then hit the Y- arrow to move forward.

        3. Keeping your speed at normal, enter 100 mm into your Z distance travel box, then hit the Z- button to move down.

        **Note: These values are approximate, you will need to adjust especially if using a MK1 or early MK2**

    The goal is to line up the sensor on ATC over the tool holder stud, triggering an LED to light up. Aim for 1-2mm above the stud, and centered on the stud.

1. Use **precise jog** (short taps only) once you are close to the stud.

![](/_images/_atc/_atc_assembly/_software/atc_assembly_soft_sensor1.gif){.aligncenter .size-full}

![](/_images/_atc/_atc_assembly/_software/atc_assembly_soft_lighton.JPG){.aligncenter .size-medium}

Once the light is on, hit the blue **Find Rack** button.

1. A **Probing Sequence** confirmation window will appear, hit OK to continue.

    * The machine will move in a small grid pattern to re-locate the stud.

    ![](/_images/_atc/_atc_assembly/_software/atc_assembly_soft_sensor2.gif){.aligncenter .size-full}

    Once it successfully locates, you will see this confirmation window.

    ![](/_images/_atc/_atc_assembly/_software/atc_assembly_soft_rackpos2.jpg){.aligncenter .size-medium}

    ⚠️ If you encounter an error that it cannot find the stud, make sure to accurately position the sensor 1mm above the stud, centered on the stud. Just because the light turns red does not mean it is in the right position!

1. The locating process will now repeat for the **left-most rack position**. You will see another confirmation window pop up. Ensure the **tool holder** is mounted into the left-most rack position before continuing. Hit OK.

1. Once completed, if you have a 12-tool rack you will be prompted to repeat this process for the right and left-most positions on your second tool rack.

1. Click Next.

### Tool Length Sensor Position

Now we will be setting the location of the TLS.

1. We are going to move the spindle all the way to the right side again, to set the location of the TLS. Jog until the spindle nose is directly above and centered on the TLS.

    ![](/_images/_atc/_atc_assembly/_software/atc_assembly_soft_tlspos.jpg){.aligncenter .size-medium}

    ![](/_images/_atc/_atc_assembly/_software/atc_assembly_soft_tlsaligned.JPG){.aligncenter .size-medium}

1. Hit the blue **Set Position** button.
1. Once the button turns green, indicating the position has been set, hit Next.

### Spindle Configuration

In this section we will be power cycling and reconnecting to the SLB-EXT.

1. Hit the Apply and Restart blue button.

    ![](/_images/_atc/_atc_assembly/_software/atc_assembly_soft_spin.jpg){.aligncenter .size-medium}

1. Reconnect to gSender.

1. Ignore the alarms, and hit the Apply and Restart button again.

    ![](/_images/_atc/_atc_assembly/_software/atc_assembly_soft_spin2.jpg){.aligncenter .size-medium}

Once complete, click the Next button.

Setup is complete! Exit the wizard now.

![](/_images/_atc/_atc_assembly/_software/atc_assembly_soft_complete.jpg){.aligncenter .size-medium}

1. Go to Config -> Tool Changing.
1. Toggle the **Enable ATCi** switch and hit the Apply Changes button.

Once complete, the following tabs should appear in gSender:

* **Spindle / Laser** - which will allow you to start up and run your spindle.
* **ATC** - which will allow you to change out tools.
