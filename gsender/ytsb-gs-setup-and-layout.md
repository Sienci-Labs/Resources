---
title: ytsb Setup & Layout
menu_order: 2
post_status: draft
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
featured_image: 
---

- Update Anonymous Usage banner once implemented

---

## Anonymous Information

When you open up gSender, you’ll notice a prompt regarding ‘Anonymous usage information’. This is just to ask if you’d be fine with us knowing things like what CNC you use it for, what computer you run it on, and other information about how you use the app. You can imagine that if we know certain features are widely used or certain errors are constantly encountered, that can be very helpful to understand how we can improve the app or its documentation. This is completely optional and anonymous, we only do it with your permission and it can be turned off at any time in the settings menu.

![](/_images/_gsender/_setup/gs_se_anonymous-info.jpg){.aligncenter .size-medium}

## Layout

Before starting to use gSender, let's briefly cover the way its functions are laid out so that you'll know where to find things moving forward. Let's begin by exploring the main screen.

### Carve

This is where you will spend the majority of your time actually carving. When the program opens, this is where you will arrive! There are 5 main sections to the Carve tab. Beginning at the top bar:

1. The top toolbar (boxed in yellow), has all the things you'll only use occasionally. This includes machine connection on the left side, notifications, system stats and current status in the middle, and shortcuts on the right.

1. The left-side toolbar (boxed in red), holds 4 main tabs, along with a helper tab. The tabs include Stats, Tools, Config, Helper and of course the main tab, Carve.

1. The large middle visualizer (boxed in green), is where you can watch the magic happen after you hit the start button. Rotate your view, monitor the job progress, turn on lightweight mode, change workspaces, and more.

1. The DRO and Jog Controls on the right (boxed in blue), have all the functions you need to manually control your CNC when jobs aren't running. This includes jogging, zero setting, homing, Go to movements, and more.

1. The 3 panels along the bottom (boxed in purple), loading, monitoring and controlling g-code files and cutting jobs, probing, running macros, manual laser / spindle control, and more.

![](/_images/_gsender/_setup/gs_set_maincarve.jpg){.aligncenter .size-medium}

We’ve built gSender’s layout around these primary boxed sections so that you can have all of the CNC functionality most hobbyists need on one screen without getting confused about what each button does. If you’re doing anything **during** a job it’ll be in the middle, if you’re doing anything **outside** a job it’ll likely be on the right, and if you want greater customization or functionality it’ll be found in the toolbars.

Another of gSender’s Design Principals is colouring. It can be scary to have an assortment of buttons in front of you and not know what they’re going to do. This is why we made every button in the app that moves the CNC, **blue**. This means you shouldn’t ever find yourself startled when the machine moves unexpectedly since the colour will help to communicate whether it’s a ‘machine moving’ button or not.

### Stats

The Stats tab provides an overview of your machine configuration, recent jobs (including their run time and if they were successful or not), upcoming maintenance, alarms & errors, plus a comprehensive help section.

![](/_images/_gsender/_setup/gs_set_mainstats.jpg)

### Tools

In the Tools tab provides wizards you can use to walk through XY squaring or movement tuning of your machine. Wasteboard surfacing, keyboard shortcuts, and gamepad profiles.

![](/_images/_gsender/_setup/gs_set_maintools.jpg)

### Config

The final tab is the configuration tab. Here you will find an extensive list of settings, starting with the basics, motors, probe, homing/limits, spindle/laser, tool changing, rotary, and more.

![](/_images/_gsender/_setup/gs_set_configlist.gif){.aligncenter .size-full}

Some things you'll likely want to check out in config are:

**Preferred Units** where you can toggle between metric (mm) and imperial (in) units, **Baud Rate** needed for your CNC (default is 115200) and **Reconnect Automatically**, which allows you to reconnect the the last machine you used, automatically.

![](/_images/_gsender/_setup/gs_set_configstart.jpg){.aligncenter .size-medium}

#### Machine Profiles

If you're planning to make any firmware modifications, gSenders Firmware tool at the bottom right of the config tab defaults to displaying the "LongMill MK2 30x30" profile. If that's not your machine, then select your machine from the dropdown menu (if it's not listed then select "Generic CNC").

![](/_images/_gsender/_setup/gs_set_configprofile.jpg){.aligncenter .size-medium}

For instance most LongMills ship with **LongMill MK2 30x30** firmware pre-installed so it matches gSender, but if you have any other machines from Sienci Labs then you'll need to match it up (in this example we have the MK1 12x30 selected). For **supported machines**, once you've made this change you might want to 'Restore Defaults' to ensure your machine has all the most up-to-date settings.

Please Note: If your Z-axis is working in the opposite direction than expected, confirm you have the correct profile. MK2 users must choose either LongMill MK2 12x30, LongMill MK2 30x30, or LongMill MK2 48x30. You can find instructions on how to flash firmware here: <a href="https://resources.sienci.com/view/lmk2-grbl-firmware/" target="_blank" rel="noopener">https://resources.sienci.com/view/lmk2-grbl-firmware/</a>

If you're running into an issue where the size isn't correct when using Soft Limits for example, get the size from your manufacturer or their resources and you should find that the changes will be straightforward to make. Simply navigate from the Config tab -> Homing/Limits.

![](/_images/_gsender/_setup/gs_set_configmaxtravel.jpg "In this example the Y-axis value has been adjusted."){.aligncenter .size-full}

Here you can see the maximum travel values. Simply adjust your new measurements to the X-axis, Y-axis and Z-axis maximum travel fields. Then hit the **Apply Settings** button.

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
