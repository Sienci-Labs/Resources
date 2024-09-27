---
title: Setup & Layout
menu_order: 2
post_status: publish
post_excerpt: See the gSender's layout to get an understanding of where tools and features are located and where you can go to change your settings or setup your CNC.
post_date: 2021-07-01 14:21:00
taxonomy:
    knowledgebase_cat: gdocs
    knowledgebase_tag:
        - gsender
custom_fields:
    KBName: gSender
    basepress_post_icon: bp-caret-right
skip_file: no
featured_image: _images/_gsender/_setup/gs_se_main-layout.jpg
---

## Anonymous Information

When you open up gSender, you’ll notice a prompt regarding ‘Anonymous usage information’. This is just to ask if you’d be fine with us knowing things like what CNC you use it for, what computer you run it on, and other information about how you use the app. You can imagine that if we know certain features are widely used or certain errors are constantly encountered, that can be very helpful to understand how we can improve the app or its documentation. This is completely optional and anonymous, we only do it with your permission and it can be turned off at any time in the settings menu.

![](/_images/_gsender/_setup/gs_se_anonymous-info.jpg){.aligncenter .size-medium}

## Layout

Before starting to use gSender, let's briefly cover the way its functions are laid out so that you'll know where to find things moving forward. The program only has one main screen, it's into three major sections:

- The top toolbar has all the things you'll only use occasionally. This includes machine connection on the left side (boxed in red) and gSender's Settings, Help, and other additional 'Tools' on the right (boxed in blue).
- The left-side control (boxed in green) has all the functions you need for loading, monitoring, and controlling g-code files and cutting jobs
- The right-side control (boxed in purple) has all the functions you need to manually control your CNC when jobs aren't running. This includes jogging, zero setting, homing, probing, running macros, manual laser / spindle control, and more.

![](/_images/_gsender/_setup/gs_se_main-layout.jpg){.aligncenter .size-medium}

We’ve built gSender’s layout around these primary boxed sections so that you can have all of the CNC functionality most hobbyists need on one screen without getting confused about what each button does. If you’re doing anything **during** a job it’ll be on the left side, if you’re doing anything **outside** a job it’ll likely be on the right, and if you want greater customization or functionality it’ll be found in the tools or settings.

Another of gSender’s Design Principals is colouring. It can be scary to have an assortment of buttons in front of you and not know what they’re going to do. This is why we made every button on the right-side control that moves the CNC, blue. This means you shouldn’t ever find yourself startled when the machine moves unexpectedly since the colour will help to communicate whether it’s a ‘machine moving’ button or not.

## Configuration

Let's do some configuration before connecting up to your CNC. Click the 'gear' at the far right of the toolbar to bring up the program settings. Some things you'll likely want to configure would be:

- **General Settings**
  - Baud rate needed for your particular CNC. Baud rate is setup for the LongMill by default.
  - Machine Profile
  - Preferred Units
  - Reverse workspace (flips the left and right-side controls if you prefer)

  ![](/_images/_gsender/_setup/gs_se_config-general.jpg){.aligncenter .size-full}
- **Visualizer Settings**
  - Set to light theme if you prefer

  ![](/_images/_gsender/_setup/gs_se_config-vis.jpg){.aligncenter .size-full}

### Machine Profiles

If you're planning to make any firmware modifications, gSenders Firmware tool at the top right of the screen defaults to displaying the "LongMill MK2 30x30" profile. If that's not your machine, then beside the word "Profile", select your machine from the dropdown menu (if it's not listed then select "Generic CNC").

For instance most LongMills ship with **LongMill MK2 30x30** firmware pre-installed so it matches gSender, but if you have any other machines from Sienci Labs then you'll need to match it up (for example: 12x30 or 48x30 MK2, any sized MK1, AltMill, etc.). For **supported machines**, once you've made this change you might want to 'Restore Defaults' to ensure your machine has all the most up-to-date settings.

Please Note: If your Z-axis is working in the opposite direction than expected, confirm you have the correct profile. MK2 users must choose either LongMill MK2 12x30, LongMill MK2 30x30, or LongMill MK2 48x30. You can find instructions on how to flash firmware here: <a href="https://resources.sienci.com/view/lmk2-grbl-firmware/" target="_blank" rel="noopener">https://resources.sienci.com/view/lmk2-grbl-firmware/</a>

![](/_images/_gsender/_setup/gs_se_config-profile.jpg){.aligncenter .size-full}

If you're running into an issue where the size isn't correct when using Soft Limits for example, get the size from your manufacturer or their resources and you should find that the changes will be straightforward to make through the 'Firmware tool' within gSender. Simply apply your new measurements to the X-axis, Y-axis and Z-axis maximum travel fields. Then hit the apply changes button.

![](/_images/_gsender/_setup/gs_se_config-travel.jpg){.aligncenter .size-full}

## Running Longer Jobs (optional)

Windows computers can tend to have their screens and USB ports 'fall asleep' even in the middle of running a long carving job. This can cause your intricate cuts to stop short and the job to fail. gSender tries to fight against this by keeping your computer awake (we use similar tactics to auto-clicker apps), but sometimes this still isn't enough so you have to change your computer settings manually.

To keep the display on, you'll want to click the **Windows** icon at the bottom left corner of your screen and start to type “<em>control panel</em>” to bring it up.

![](/_images/_gsender/_setup/gs_se_awake-control-panel.jpg){.aligncenter .size-medium}

Once you’ve clicked to open it, go to **Hardware and Sound** then **Power Options**

![](/_images/_gsender/_setup/gs_se_awake-hardware-sound.jpg){.aligncenter .size-medium}

![](/_images/_gsender/_setup/gs_se_awake-power-options.jpg){.aligncenter .size-medium}

The plan that's currently selected (circled in the picture) will be the one that you want to change. In this example we will be editing the **Balanced** plan. Click on the "Change plan settings" text (highlighted with an arrow).

![](/_images/_gsender/_setup/gs_se_awake-plan-settings.jpg){.aligncenter .size-medium}

Go to the second drop-down and set both 'battery' and 'plugged in' selection to **Never**, save the changes to ensure that your computer never dozes off on its own.

![](/_images/_gsender/_setup/gs_se_awake-never-sleep.jpg){.aligncenter .size-medium}

To keep the USB ports on, click **Change advanced power settings**

![](/_images/_gsender/_setup/gs_se_awake-advanced.jpg){.aligncenter .size-medium}

In the separate window that appears, you’ll want to Expand the **USB Settings**, then **USB selective suspend setting**, and finally change both the 'battery' and 'plugged in' settings for these drop-downs to ‘**Disabled**’. Click OK to **Apply** these new settings.

![](/_images/_gsender/_setup/gs_se_awake-usb.jpg){.aligncenter .size-medium}

After having done all of this, just be mindful now that sometimes a Windows update can remove these settings. If you have an update and want to be confident running your CNC, we'd recommend checking back on these settings to make sure they're still set properly.
