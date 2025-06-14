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
featured_image: _images/_gsender/_setup/gs_se_carve-overview.jpg
---

## Anonymous Information

When you open up gSender, you’ll notice a prompt regarding ‘Anonymous usage information’. This is just to ask if you’d be fine with us knowing things like what CNC you use it for, what computer you run it on, and other information about how you use the app. You can imagine that if we know certain features are widely used or certain errors are constantly encountered, that can be very helpful to understand how we can improve the app or its documentation. This is completely optional and anonymous, we only do it with your permission and it can be turned off at any time in the settings menu.

![](/_images/_gsender/_setup/gs_se_anonymous-info.jpg){.aligncenter .size-medium}

## Layout

Before starting to use gSender, let's briefly cover the way its functions are laid out so that you'll know where to find things moving forward. The program can be broken down into it's three major sections:

1. The top toolbar (boxed in red), will stay visible regardless of what you are doing. It includes machine connection on the left side, notifications, system stats and current status in the middle, and shortcuts on the right.
1. The left-sidebar (boxed in green) holds 5 main tabs; the Helper, the main Carve tab (which we have showing now), Stats, Tools, and Config.
1. The main screen (boxed in blue) will show the contents of the selected tab in the left sidebar, with the default being the Carve tab.

![](/_images/_gsender/_setup/gs_se_carve-overview.jpg){.aligncenter .size-medium}

Another of gSender’s Design Principals is colouring. It can be scary to have an assortment of buttons in front of you and not know what they’re going to do. This is why we made every button in the app that moves the CNC **dark blue**. This means you shouldn’t ever find yourself startled when the machine moves unexpectedly since the colour will help to communicate whether it’s a ‘machine moving’ button or not.

### Carve

This is where you will spend the majority of your time actually carving. When the program opens, this is where you will arrive! There are 2 main sections to the Carve tab.

1. The large middle visualizer (boxed in red), is where you manage your files and can watch the magic happen after you hit the Start button. Rotate your view, monitor the job progress, turn on lightweight mode, change workspaces, adjust feed rate, and more.
1. The DRO and Jog Controls on the right (boxed in blue), have all the functions you need to manually control your CNC when jobs aren't running. This includes jogging, zero setting, homing, Go to movements, and more. The section at the bottom includes extra features like probing, macros, manual spindle/laser control, and more.

![](/_images/_gsender/_setup/gs_se_carve-tab.jpg){.aligncenter .size-medium}

We’ve built gSender’s main screen around these primary boxed sections so that you can have all of the CNC functionality most hobbyists need on one screen without getting confused about what each button does. If you’re doing anything **during** a job it’ll be in the middle, if you’re doing anything **outside** a job it’ll likely be on the right, and if you want greater customization or functionality it’ll be found in the toolbars.

### Stats

The Stats tab is a great place to check in on how your machines doing. This includes:

- Summary of stats
- Recent jobs (including their run time and if they were successful or not)
- Upcoming maintenance
- Guidance on help and troubleshooting
- And some more technical information like an overview of your machine configuration and a list of recent alarms & errors

You can click on the bottom bar to see more details on each of these summaries.

![](/_images/_gsender/_setup/gs_se_stats-tab.jpg){.aligncenter .size-medium}

### Tools

The Tools tab has what we like to call "Wizards" you can use to walk through lots of common CNCing tasks like XY squaring, movement tuning, wasteboard surfacing, as well as you can access keyboard and gamepad shortcuts.

![](/_images/_gsender/_setup/gs_se_maintools.jpg){.aligncenter .size-medium}

### Config

The final tab is the configuration tab. Here you will find an extensive list of settings, starting with the basics, motors, probe, homing/limits, spindle/laser, tool changing, rotary, and more.

![](/_images/_gsender/_setup/gs_se_configlist.gif){.aligncenter .size-full}

## Set up to Use

Let's explore some common gSender settings to get your own setup up and running as you prefer. We can change how gSender looks, which display units you prefer, or adjust machine setup all in the same place. Some things you may want to configure would be:

1. Preferred units
   - In the Basics section, change which units (mm or inches) you want to see on the main Carve screen (Config units will always display as mm)
   ![](/_images/_gsender/_setup/gs_se_configstart.jpg){.aligncenter .size-medium}
   The Carve tab will always show the units you set at the top left corner of the DRO.
   ![](/_images/_gsender/_setup/gs_se_units-mainscreen.jpg){.aligncenter .size-medium}
1. Enable other CNC functions
   - If your CNC supports them, this can include a Spindle, Laser, Rotary axis, and more. Just go to the appropriate section in Config and the first option you should see should mention "enabling" it. After Applying the changes you'll see a new tab appear in the bottom-right of the main Carve screen.
   ![](/_images/_gsender/_setup/gs_se_hardware-enable.gif){.aligncenter .size-full}
1. Notifications
   - In Basics ➜ Notifications, these can be customized to give you warnings when you load bad files, provide information at the end of a job, and more.
1. Visualizer theme and Dark mode
   - In the Basics section, both these settings help change the colours in gSender based on what will be easier on your eyes. Check them out if that sounds interesting!

After these changes, don't forget to hit **Apply Settings** so everything gets saved!

### Machine Profiles

If you're planning to make any firmware modifications, first check the current machine profile selected at the bottom of the Config tab. The default in gSender is the "**LongMill MK2 30x30**" so select a different option in the dropdown if that's not your machine (if yours is not listed then select "Generic CNC").

For **supported machines**, once you've made this change you might want to 'Restore Defaults' to ensure your machine has all the most up-to-date settings.

![](/_images/_gsender/_setup/gs_se_configprofile.jpg){.aligncenter .size-medium}

Please Note: If your Z-axis is working in the opposite direction than expected, confirm you have the correct profile. MK2 users must choose either LongMill MK2 12x30, LongMill MK2 30x30, or LongMill MK2 48x30. You can find instructions on how to flash firmware here: <a href="https://resources.sienci.com/view/lmk2-grbl-firmware/" target="_blank" rel="noopener">https://resources.sienci.com/view/lmk2-grbl-firmware/</a>

If you're running into an issue where the size isn't correct when using Soft Limits for example, get the size from your manufacturer or their resources and you should find that the changes will be straightforward to make. Simply navigate from the Config tab -> Homing/Limits.

![](/_images/_gsender/_setup/gs_se_configmaxtravel.jpg "In this example the Y-axis value has been adjusted."){.aligncenter .size-full}

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

## Transitioning from Classic

If you've been comfortably using **gSender 1.4.12 or earlier** and are about to click to update, we've got some news to share with you. After over a year of hard work, **gSender has been almost fully re-coded from scratch and will now be looking a little bit different compared to** what you're used to once the update is complete. We had to do this because gSender really needed some improvements under the hood, and we thought while we were at it we'd try to improve on gSender's already great user interface as well.

*Rest assured that all of the functionality you are used to is still here, it may simply have a new home.* Hopefully this section helps guide you through these changes so that you won't skip a beat.

Out with the old **Classic version**, and in with the **New U!!** Let's dive into some specifics.

![](/_images/_gsender/_setup/gs_se_trans-newu-main2.jpg)

### Key Enhancements

We've combined similar features, and are excited to share things like our new **Stats Tab** which incorporates stats, maintenance, diagnostics, and more into a simple dashboard, as well as the new **Config Tab** which puts all of your settings into one place, so no more flipping between the Firmware and gSender settings.

You will notice right away that as you click through the new UI, there are two section of your screen that are always available to you. The **Top bar** and the **Left bar**.

#### Top Bar

The top bar will show you several cool things, and will always be available to see. Feel free to click on some of these icons to see what they do! Moving from left to right, you will see your connection status, notification bell, machine information, machine status, and shortcuts for remote control, keyboard shortcuts & gamepad profiles.

![](/_images/_gsender/_setup/gs_se_trans-top-bar.jpg){.align-center .size-medium}

#### Left Bar

On the left side of the screen, you will see another bar that stays on the screen at all time, with 5 tabs. From top to bottom, these tabs are:

1. The **Helper Tab** will aid you in understanding and correcting any errors that pop up. It also includes a tool changing wizard.
1. The **Carve Tab**, is where you handle files, watch the visualizer, setup jobs, move the machine, probe for zero, manage macros, check out the console and more.
1. The **Stats Tab** can be used for examining your machine stats, upcoming maintenance, your recent alarms & errors and your machine configuration. A diagnostic file download is available if you run into trouble, and links to our community, resources and Git Hub repository are also found on this tab.
1. On the **Tools Tab**, you will see aids to help you surface a project, square or tune your machine and setup your keyboard and gamepad shortcuts.
1. The **Config Tab** has combined both your machine settings with the firmware settings. You can search these settings or toggle the ones that have been modified.

![](/_images/_gsender/_setup/gs_se_trans-left-bar.jpg){.align-center .size-medium}

Let's briefly checkout each tab, to see what goodies are there.

#### Main Carve Tab

We've improved the main screen, now called the **Carve Tab**. The right side (Blue) is very similar to Classic gSender -- all the blue buttons move the machine, whether it be jogging, homing or parking. Below, you can access many functions like Probe and Rotary. The middle/left side of the screen (Red) is like a dashboard,  you can load files, control the job and observe your progress in the visualizer.

![](/_images/_gsender/_setup/gs_se_trans-carvemain.jpg){.align-center .size-medium}

The jog controls have also been redesigned for better ergonomics and touch-screen compatibility.

![](/_images/_gsender/_setup/gs_se_trans-comp-jog.jpg){.align-center .size-medium}

#### Stats Tab

The stats tab offers an overview of your Machine, including your recent jobs run, configuration, upcoming maintenance warnings and your recent alarms & errors. You can also download a diagnostic file for extra support, access our resources, community or github repository! Tap on one of the tabs at the bottom of this page, to see even more details!

![](/_images/_gsender/_setup/gs_se_trans-status.jpg){.align-center .size-medium}

#### Tools Management

The Tools tab now contains all the widgets for surfacing your project, tuning your machine, as well as creating keyboard shortcuts and gamepad profiles. In this short video, you can see where the Surfacing and Calibrate Tools are on Classic gSender, then we flip over to the Tools tab on the New U.

![](/_images/_gsender/_setup/gs_se_trans-surface.gif){.align-center .size-full}

### Streamlined CNC Setup

The Config menu has been refined to display only relevant sections based on your machine's connection status and selected profile. It's a combination of the   preferences mixed with the  firmware settings, so now all  settings are in one place. In this short video, you can see these moved from the top right (Classic) to the bottom left corner of the screen (New U).

![](../_images/_gsender/_setup/gs_se_trans-firmwarenew.gif){.align-center .size-full}

One cool thing is that modified settings are highlighted, and a 'Show Modified' toggle allows you to filter and manage settings that have been changed from the machine default. You can reset to default settings at any time if you find a change you have made isn't working.

![](/_images/_gsender/_setup/gs_se_trans-modified.gif){.align-center .size-full}

### 🌟 New Features

Not only are there several new UI enhancements, there are also a couple of new features that we should mention. Connecting has been streamlined and you have more flexibility on how gSender displays on your screen.

#### Automatic Firmware Detection

Connecting is now easier! gSender now automatically detects your firmware type (Grbl/grblHAL) upon connection, selecting the appropriate controller settings. This feature simplifies the process, as you can select your default firmware choice in Config, and connect with a simple button press.

![](/_images/_gsender/_setup/gs_se_trans-connect-auto.gif){.align-center .size-medium}

#### Improved Visuals and Touch Support

We've made several visual and usability upgrades to gSender. The visualizer now supports pinch-to-zoom on touch screens, **Dark Mode** to reduce eye strain, and includes a redesigned **Lightweight Mode** with easy presets. Turn these on by going to Config -> Customize UI.

If you're using a tablet or vertical screen, **Portrait Mode** is now supported—just rotate your device or change your display orientation.

![](/_images/_gsender/_setup/gs_se_trans-portrait.jpg){.align-center size-medium}

Some other noteworthy features include:

- **Console Enhancements**: Added console clearing functionality and arrow-scrollable input history for improved usability.
- **Visual Tweaks**: Numerous UI adjustments, including updated icons, responsive sidebar sizing, and improved text legibility.

### 📘 Getting Started with the New UI

To explore these new features:

1. **Download gSender 1.5.0**: Access the latest version from the [Sienci Labs GitHub repository](https://github.com/Sienci-Labs/gsender/releases).
2. **Refer to the Official Documentation**: The [gSender Docs](https://resources.sienci.com/view/gs-using-gsender/) provide comprehensive guidance on utilizing the software's capabilities.
3. **Engage with the Community**: Share your experiences, provide feedback, and seek assistance on the [Sienci Community Forum](https://forum.sienci.com/).

By familiarizing yourself with these updates, you can leverage the enhanced functionality and improved user experience that gSender 1.5.0 offers!
