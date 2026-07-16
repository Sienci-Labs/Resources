---
title: LongMill Spindle Kit
menu_order: 8
post_status: draft
post_excerpt: 
post_date: 2026-05-20 10:55:55
taxonomy:
    knowledgebase_cat: mk3-assembly
    knowledgebase_tag:
custom_fields:
    KBName: LongMill MK3
    basepress_post_icon: bp-caret-right
skip_file: no
featured_image: _images/post-image.jpg
---

This setup guide will show to swap out your router for the Sienci Labs 1.5KW spindle.

Before we begin, make sure that:

- **gSender 1.6.3 or above** is installed on your computer
- Machine is **connected to gSender** and **powered ON**

## Machine Setup

### Cable Routing

1. Undo all drag chain clips and detach the drag chain from the end links, using a flathead screwdriver.

    ![](/_images/_lmmk3/_assembly/lmk3_spindle_kit-unclip.gif){.aligncenter .size-full}

    You can pop off the drag chain from the ends by wedging the screwdriver between the connecting tabs.

    ![](/_images/_lmmk3/_assembly/lmk3_spindle_kit-endlink.JPG){.aligncenter .size-medium}

1. Remove the router's power cable from the drag chain. Then remove the router from the mount, by loosening the front two (2) M5 screws with an Allen key. Unplug the router from power, and from the controller.

    ![](/_images/_lmmk3/_assembly/lmk3_spindle_kit-mount.JPG){.aligncenter .size-medium}

    ![](/_images/_lmmk3/_assembly/lmk3_spindle_kit-routing.JPG){.aligncenter .size-medium}

1. Route the spindle cable through the drag chains, so that the **blue/black connector end** is at the **front of the left Y-axis**, and the **metal connector end** is at the **Z-axis.**

    ![](/_images/_lmmk3/_assembly/lmk3_spindle_kit-routingv2.jpg){.aligncenter .size-medium}

1. Re-attach the drag chain clips and end links, securing the spindle cable and the existing motor cables in place.

### Router Mount

1. With the machine connected to gSender, jog the Z-axis all the way down to gain access to the four (4) M5-25mm screws at the back of the XZ gantry.

    You can also turn OFF the SLB-LITE and rotate the coupler by hand to move the Z-axis down.

1. Using an Allen key, unfasten the four (4) back screws with an Allen key to remove the mount.

    ![](/_images/_lmmk3/_assembly/lmk3_spindle_kit-routerscrews.JPG){.aligncenter .size-medium}

1. Take the new 80mm spindle mount and secure it using all four (4) screws at the back of the XZ gantry.

1. Loosen the front two (2) screws on the 80mm spindle mount.

1. Place the spindle through the mount, and fasten the clamping screws to secure the spindle in place. You can adjust the height later.

### VFD Connections

1. Plug in the VFD power cord, spindle cable and controller cable (coiled) into the bottom of the VFD.

    ![](/_images/_lmmk3/_assembly/lmk3_spindle_kit-connectvfd.JPG){.aligncenter .size-medium}

    Make sure the spindle cable is oriented correctly, matching the slots with the small tabs on the VFD. Once plugged in, fully secure the spindle cable by turning the blue ring clockwise.

    ![](/_images/_lmmk3/_assembly/lmk3_spindle_kit-spincable.JPG){.aligncenter .size-medium}

1. Fasten the VFD to your table or a flat surface. Make sure the bottom of the VFD is accessible, so you can toggle the power switch. Use the four (4) mounting points on the back panel to fasten the VFD in place.

    ![](/_images/_lmmk3/_assembly/lmk3_spindle_kit-mountingpoints.JPG){.aligncenter .size-medium}

1. Plug in the spindle cable into the top of the spindle, again aligning the connector and then fastening the ring.

    ![](/_images/_lmmk3/_assembly/lmk3_spindle_kit-spinconnect.JPG){.aligncenter .size-medium}

1. Plug in the controller cable into the SPINDLE port of the SLB-LITE controller.

    ![](/_images/_lmmk3/_assembly/lmk3_spindle_kit-controllercable.JPG){.aligncenter .size-medium}

1. If your SLB-LITE is powered on, please turn it OFF now.

1. Plug the VFD power cord into your outlet, and turn on the power switch at the bottom of the VFD. The VFD screen should turn on and show H 100 then blink 0000.

    ![](/_images/_lmmk3/_assembly/lmk3_spindle_kit-startup.gif){.aligncenter .size-full}

1. Now turn ON the controller using the power switch.

## gSender Settings

1. Connect to the machine in gSender.

    ![](/_images/_lmmk3/_assembly/lmk3_spindle_kit-connectgsender.jpg){.aligncenter .size-medium}

1. Go to Tools, then select Accessory Installation.

    ![](/_images/_lmmk3/_assembly/lmk3_spindle_kit-accessoryinstall.jpg){.aligncenter .size-medium}

1. Select Sienci Spindle, then go through the installation wizard to finish setting up.

    ![](/_images/_lmmk3/_assembly/lmk3_spindle_kit-spininstall.jpg){.aligncenter .size-medium}

1. Once you completed the steps in the installation wizard, go to Config, to the Spindle/Laser section, and enable these functions by flipping the enable Spindle/Laser toggle to turn them ON. Don't forget to apply your new settings!

    ![](/_images/_lmmk3/_assembly/lmk3_spindle_kit-control.jpg){.aligncenter .size-medium}

1. We will now reset everything so our changes can successfully take effect. Turn OFF the controller at the power switch.

    Unplug the VFD from power.

    Close gSender.

    Then, turn ON the controller, plug the VFD back into power, open gSender and reconnect.

1. At the ‘Spindle/Laser’ tab, check that ‘H-100’ is selected. Then use the slider to the lowest speed, and press the ‘Forward’ button to test out the spindle. Check that it is spinning in the correct direction. Press the ‘Stop’ button to stop the spindle. You are almost ready to start CNCing with the spindle!

![](/_images/_lmmk3/_assembly/lmk3_spindle_kit-forward.jpg){.aligncenter .size-medium}

## Finishing Up

### Break-in Cycle

The grease inside the bearings may have shifted during transportation, it is recommended that you run a “break-in” cycle to redistribute the grease before using your spindle. To do this, you can download and run the g-code file below on gSender, which will take 1 hour 40 minutes to run.

[Sienci 1.5kW Spindle Break-in gcode](https://drive.google.com/file/d/1JdrqfgkZxhhXIAjUMOi-5UXIDjNveZe3/view)

To run the file connect to gSender and press 'Load File' at the bottom left corner. Select the file and you should see a 'Start' button appear, go ahead and click that.

### Further Learning

For more information on how to change your collets and run a job with your spindle, check out our [quick start guide](https://resources.sienci.com/view/spindlevfd-quickstart/)!
