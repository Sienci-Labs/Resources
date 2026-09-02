---
title: 5. Table Mounting
menu_order: 6
post_status: draft
post_excerpt: How to mount your LongMill MK3 to your table and how to surface your wasteboard.
post_date: 2026-05-20 10:40:22
taxonomy:
    knowledgebase_cat: lmk3-assembly
    knowledgebase_tag:
custom_fields:
    KBName: LongMill MK3
    basepress_post_icon: bp-caret-right
skip_file: no
featured_image: _images/post-image.jpg
---

## Table Mounting

We will now use gSender to jog the machine to the travel limits, which will square up the machine and allow you to secure down the machine to the MDF sheet, which will act as your wasteboard.

    ⭐ Due to the use of linear guides on the X and Y axes, there is zero play in the axes which means they can be squared to each other simply by jogging front to back.

1. Adjust the position of your assembled machine, so that there is space for the SLB-LITE to sit on the MDF.

    ![](/_images/_lmmk3/_assembly/_tablemount/lmk3_tablemounting_render_23.png){.aligncenter .size-medium}

1. Download the latest version of gSender [https://sienci.com/gsender/] onto your computer. Detailed installation instructions can be found on this page [https://resources.sienci.com/view/gs-installation/].

1. Connect to gSender through USB using the top left corner dropdown.

    ![](/_images/_lmmk3/_assembly/_tablemount/lmk3_tablemount-connectgsender.jpg){.aligncenter .size-medium}

1. You will see a red alarm at the top of the screen. The machine can be unlocked by pressing and releasing the E-stop, then pressing Click to Unlock Machine button on gSender.

    ![](/_images/_lmmk3/_assembly/_tablemount/lmk3_tablemount-estop.gif){.aligncenter .size-full}

    ![](/_images/_lmmk3/_assembly/_tablemount/lmk3_tablemount-alarm10.jpg){.aligncenter .size-medium}

1. Open the Config tool, and under Homing/Limits, disable the hard and soft limits.

    ![](/_images/_lmmk3/_assembly/_tablemount/lmk3_tablemount-limdisable.jpg){.aligncenter .size-medium}

1. Press Apply Settings. Turn OFF/ON the controller.

    ![](/_images/_lmmk3/_assembly/_tablemount/lmk3_tablemount-applysettings.jpg){.aligncenter .size-medium}

1. Reconnect to gSender.

1. Move the machine around with the jog wheel buttons, to make sure your motors are moving the expected amount and in the right direction.

    ![](/_images/_lmmk3/_assembly/_tablemount/lmk3_tablemount-movedro.jpg){.aligncenter .size-medium}

1. Then jog the machine to the back using the Y+ button, making sure it is hitting the Y rail plates on both sides.

    ![](/_images/_lmmk3/_assembly/_tablemount/lmk3_tablemount-bumperstop.jpg){.aligncenter .size-medium}


1. Square the machine to your MDF sheet; use the measuring tape to evenly offset the Y rail plates from the back edge of the MDF. Shift your machine to get it into the desired position.

    ![](/_images/_lmmk3/_assembly/_tablemount/lmk3_tablemount-yaxisoffset.jpg){.aligncenter .size-medium}


1. Screw down the first hole of both Y rails using the wood screws.

    ![](/_images/_lmmk3/_assembly/_tablemount/lmk3_tablemount-1stscrew.jpg){.aligncenter .size-medium}


1. Then jog the machine to the front using the Y- button. Make sure the Y gantry is touching the sensor bump stop on both sides. If not, press the E-stop button on the SLB-LITE, then manually turn the leadscrew with your hands to move the Y gantry to touch the bump stop.

    ![](/_images/_lmmk3/_assembly/_tablemount/lmk3_tablemount-yaxisfront.jpg){.aligncenter .size-medium}


1. Screw down the first hole of both Y rails using the wood screws. Then finish securing the remaining holes to complete table mounting.

1. Go back on gSender. In Config, under Homing/Limits, turn ON the hard and soft limits (we need them to use the sensors on our machine).

1. Press Apply Settings, then turn OFF/ON the SLB-LITE controller to have the changes take effect.
