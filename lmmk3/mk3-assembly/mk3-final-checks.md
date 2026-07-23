---
title: 6. Final Checks
menu_order: 7
post_status: draft
post_excerpt: After assembly, make sure your machine is set up and ready for carving.
post_date: 2026-05-20 10:44:33
taxonomy:
    knowledgebase_cat: mk3-assembly
    knowledgebase_tag:
custom_fields:
    KBName: LongMill MK3
    basepress_post_icon: bp-caret-right
skip_file: no
featured_image: _images/post-image.jpg
---

We’re sure you’re itching to start cutting! Before chips go flying, we recommend going through these final checks to ensure you are set up for success.

1. All **couplers** have been fully tightened on both the motor shaft and lead screw ends

    ![](/_images/_lmmk3/_assembly/lmk3_final_checks-coupler.JPG){.aligncenter .size-medium}

1. All motor dip switches are in the correct positions: **1-Down 2-Down 3-Up 4-Up 5-Up**

    ![](/_images/_lmmk3/_assembly/lmk3_final_checks-dipswitch.JPG){.aligncenter .size-medium}

1. The gSender version on your computer is **1.6.3 or higher**

    ![](/_images/_lmmk3/_assembly/lmk3_final_checks-gsenderver.jpg){.aligncenter .size-medium}

1. After connecting to gSender, the machine can be unlocked by pressing and releasing the E-stop, then pressing **Click to Unlock Machine** button on gSender.

    ![](/_images/_lmmk3/_assembly/lmk3_final_checks-estop.gif){.aligncenter .size-full}

    ![](/_images/_lmmk3/_assembly/lmk3_final_checks-alarm10.jpg){.aligncenter .size-medium}

1. Homing completes successfully, without any alarms or errors

    - Make sure the machine is away from the sensors before you press **Home**, otherwise you will get an immediate alarm

    ![](/_images/_lmmk3/_assembly/lmk3_final_checks-homing.gif){.aligncenter .size-full}

    ![](/_images/_lmmk3/_assembly/lmk3_final_checks-homingmk3.gif){.aligncenter .size-full}

1. The **AutoSpin router** is set up, and can spin up and stop

    a. Make sure the AutoSpin is **unplugged** and the power switch is in the **OFF “O”** position.

    b. On gSender, go to Config, then to Spindle/Laser at the sidebar, then press the **Setup AutoSpin** button.

    ![](/_images/_lmmk3/_assembly/lmk3_final_checks-autospinsetup.jpg)

    After pressing OK on the popup window, turn **OFF/ON** the controller and reconnect to gSender.

    c. Go back to Config and under Spindle/Laser, toggle ON the setting **Spindle/Laser controls**. Press Apply Settings.

    ![](/_images/_lmmk3/_assembly/lmk3_final_checks-controls.jpg){.aligncenter .size-medium}

    d. Turn the dial of the router to the **S** position.

    e. Then plug in the router and flip the power switch to the **I "ON"** position.

    ![](/_images/_lmmk3/_assembly/lmk3_final_checks-autospin.jpg){.aligncenter .size-medium}

    f. On gSender, ensure the toggle is at **Spindle** and that in the dropdown, **PWM** is selected.

    Use the speed slider and **Forward** button to test at different speeds. Press **Stop** when you are done.

    ![](/_images/_lmmk3/_assembly/lmk3_final_checks-pwm.jpg){.aligncenter .size-medium}

1. Otherwise if you have the **Sienci Labs Spindle Kit**, go to the [Spindle Kit](https://resources.sienci.com/view/mk3-spindle-kit/) page to set up your spindle.

1. Machine is confirmed to be square, using gSender’s [XY Squaring Tool](https://resources.sienci.com/view/gs-calibration-tools/#xy-squaring)

    ![](/_images/_lmmk3/_assembly/lmk3_final_checks-gsendersquaring.jpg){.aligncenter .size-medium}

If you have gone through the checks above, then you are ready to start cutting! Head over to [Surfacing & First Projects](https://resources.sienci.com/view/mk3-surfacing-first-proj/) to prepare your wasteboard and get some test cuts in.
