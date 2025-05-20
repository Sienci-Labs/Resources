---
title: Edge Features
menu_order: 5
post_status: publish
post_excerpt: 
post_date: 2021-07-01 15:55:00
taxonomy:
    knowledgebase_cat: gdocs
    knowledgebase_tag:
        - gsender
custom_fields:
    KBName: gSender
    basepress_post_icon: bp-caret-right
skip_file: no
featured_image: _images/_gsender/_edge/gs_edge-cycle.jpg
---

gSender Edge is our test arena for working on new and exciting gSender updates that will eventually be released to everyone. Think of it as a program that you can download independently from traditional gSender that allows you to participate in public Beta testing. This gives you the opportunity to use all the new features that we’re working on and make an impact by giving us feedback to inform the final result, that’s what it’s like to be on the bleeding **Edge**.

Edge isn’t a replacement for gSender in any way - it’s a way for us to test and get feedback on new, bigger features without exposing them to users who may not be interested or causing unexpected bugs. This follows a cycle that can be several months long where:

![](/_images/_gsender/_edge/gs_ed_cycle.jpg){.aligncenter .size-medium}

1. A new Edge version is split off from Main in order to prototype some new functionality and features (you can tell when this happens because the numbering scheme will jump up from 1.1.6 to EDGE-1.2.0, for example)
1. Edge eventually stops adding major features so it can become more refined from user feedback and squashing bugs
1. Once everything seems stable, everything that’s been added to Edge becomes a part of Main gSender so that everyone can now enjoy the new features
1. The process repeats

Downloading Edge is similar to the Main version of gSender and is available on the same page: <a href="https://sienci.com/gSender/" target="_blank" rel="noopener">https://sienci.com/gsender/</a>. The main caveat is that we don’t post the links for each operating system, so once you click the link to download Edge you’ll need to scroll down on the page to the “Assets” and click on the program download for your specific device. For Windows it’ll end in “.exe”, Mac will be “.dmg”, and the rest are for Linux and Pi.

## Unique Differences

If you used to see a feature here but don’t see it any longer, it’s likely been added into the main version of gSender! **Look for it on the other gSender documentation pages.**

The core of our next effort towards improving gSender is a User Interface (UI) refresh with a few specific goals in mind. As gSender has evolved over the years, with new features, support for expanded hardware options, and support for new firmware, we’ve inevitably run into constraints within the current design. This had us feeling cramped with space on the screen, look and feel, and responsiveness. We’ve spent this Edge cycle addressing these constraints with a few other goals in mind. For this version of Edge, which we call **New U** our goals are as follows:

- Maintaining gSenders primary principles of simplistic unopinionated controls, substitute technical jargon for simple language, and only showing functionality that you need for your specific machine.
- Better support for various screen sizes (from desktop down to phone) and more intuitive, usable touchscreen support.
- More thought into use of space for existing features to not feel like an afterthought and create space for new features to slot in.
- Lower technical debt on the front-end side of the application.

As of version **1.50-Edge-1** the current notable features / improvements to Edge are:

### Available Now

- **New UI Control Screen**
  - **Jog Control** - Received a makeover including button shape, size, spacing, and adding in A-axis jogging
  - **New DRO** - More clear separation between Gotos and Zero setting to prevent accidental clicks and create more visual cohesion, updated corner buttons
  - **Running Jobs** - Feed & Laser Speed Bar really got a punch of colour! Use the slider or the + and - buttons to change speed
  - **Outline & Start From** - Start from now has it's own button! Many people never knew it existed since it was hard to notice
  - **Alarms** - Now focused in the top, center of the screen for easier reading
  - **Running status bar** - Upgraded visual is now an end mill, showing your progress through your job visually, in a percentage of time shown
- **Job Files Revamp** - We've made it faster and easier to load and use your files
  - **Load File** - Updated to give you more power over your files
  - **Recent Files** - Are now listed, just press and load
  - **Last Job** - Includes new details like the file name, run time and status
- **Firmware detection** - Automatically identify which version you are running, and automatically connect to the correct controller
- **Config Tab** - A whole new page to dial in your gSender settings and your firmware EEPROM codes, all in one
- **Machine Info** - See your current firmware modals and pin status at a glance

### Coming Soon

- **Updated Mobile & Tablet screens** - Use your phone or your tablet with our power-packed mobile UI update
- **Notification System** - gSender wants to tell you something!
  - **Notification bell** - allows you to sort your notifications by tab, showing errors, info, and successful jobs completed
  - **Tool is ON** - indicators will appear on the top bar if you have the laser or rotary tools enabled for better clarity and safety
- **Stat/Info Tab** - Review your usage and statistics on this tab
- **Tool/CAM Tab** - Surface a project, prepare a flat wasteboard, and hoping to expand to support much more
- **Dark Mode** - Run gSender at night while in dark mode. Ooo, spooky.

Much of our effort early on has been dedicated to backend changes, tooling and technology changes, and the “main” control UI of the software. As such, some longstanding features such as surfacing, calibration, etc. are not included in this first release - rest assured that these will be coming shortly as we iterate through the remaining features to bring them in line with the UI refresh. There was an enormous effort on the “plumbing” side of things to future proof gSender and now that that’s out of the way, feature development should be quick.

### New Layout/Control Screen

It may look different, but you can take a deep breath and relax, everything is still here. And more! Several tabs have moved from the top of the screen to the left sidebar. This allows us to communicate more in the top bar like status, peripherals in use, and notifications.

![](/_images/_gsender/_edge/gs_ed_main-screen-connected.jpg){.aligncenter .size-medium}

#### Jog Control

Updated jog controls with a new design. A-axis now joins the rest of the jog controls if your firmware reports that it supports one.

![](/_images/_gsender/_edge/gs_ed_jog-control.jpg){.aligncenter .size-medium}

#### New DRO

DRO section slightly reworked - Go To and Zero now separated, A-axis is included if your firmware reports it exists or rotary toggled on, and single axis homing is better integrated into the experience with a single toggle.

![](/_images/_gsender/_edge/gs_ed_main-screen-zero.jpg){.aligncenter .size-medium}

![](/_images/_gsender/_edge/gs_ed_main-screen-home.jpg){.aligncenter .size-medium}

#### Running Jobs

Spindle and Feed overrides now more closely associated with the other workflow controls to make sure your speeds are set correctly before starting a job and if anything goes wrong you have a single place to look to control the job.

![](/_images/_gsender/_edge/gs_ed_run-controls.jpg){.aligncenter .size-medium}

#### Alarms

Machine status is now at the top and the center of your attention. Alarms will appear directly below it.

![](/_images/_gsender/_edge/gs_ed_alarm-state.jpg){.aligncenter .size-medium}

#### Minimize Handler

You can minimize the sidebar with a simple click of the hamburger icon.

![](/_images/_gsender/_edge/gs_ed_tabs.gif){.aligncenter .size-full}

#### Touch Screen

Secondary widgets get an update to allow for touch screen activation.

![](/_images/_gsender/_edge/gs_ed_secondary-widget.jpg){.aligncenter .size-medium}

### Load Job Files

Extra power has been added to your file manager. Flip between job information and job size. Reload your file or access recent files accessed.

![](/_images/_gsender/_edge/gs_ed_file-info.jpg){.aligncenter .size-medium}

![](/_images/_gsender/_edge/gs_ed_file-size.jpg){.aligncenter .size-medium}

### Firmware Detection

gSender now detects your firmware flavour on connection and chooses the controller for you! No longer do you have to worry about forgetting to swap firmware versions when connecting to different machines or connecting to a new machine. We hope this allows an easier, more plug-and-play experience when connecting to a machine for all users and less situations where behaviour is not what’s intended because the user chose the wrong firmware to connect with.

We’ve made some assumptions - if you’re connecting with ethernet, for example, it will default to grblHAL.

### Configuration Tool

Settings for your machine and the EEPROM settings found in the firmware tool have been combined into a new Configuration tool for a one stop shop in setting up your machine. We’re hopeful that having **gSender settings** and **firmware EEPROM codes** more closely grouped allows the user a more straight forward experience in configuring their CNC.

A tab for Basics, Motors, Probes, Spindle/Laser, etc. are all there for you to explore. The groups should make sense from a high level - for example, the Spindle contains both the settings for gSender to enable the tab and set laser/spindle max and min power, along with any EEPROM settings relevant to configuring your spindle.

*Note - **In cases where grblHAL supports natively some functionality such as laser offsets, the setting will use those EEPROM values instead of the local values for a more seamless user experience and less confusion***

![](/_images/_gsender/_edge/gs_ed_configmain.jpg){.aligncenter .size-medium}

There was a last second emergent issue with some EEPROM controls but the legacy firmware tool is available for the time being if you find it's not working as you expect.

There are also some slight behaviour changes. Settings must be applied instead of automatically saving, for example. We hope there is not too much of a learning curve - we’re excited to hear feedback on both groupings and how it functions!

![](/_images/_gsender/_edge/gs_ed_applychange.jpg){.aligncenter .size-medium}

### Machine Info

We’ve added an easy interactive information modal to let you know about both current firmware modals and pin status. Some of this information was available in the old user interface within the diagnostic tool, but we hope having a single cohesive spot on the main interface will be helpful to non-novice users.

![](/_images/_gsender/_edge/gs_ed_machineinfov2.jpg){.aligncenter .size-medium}

### Notifications

We’ve made some changes to application notifications. No longer will a toast with relevant information get missed- you now have history of application notifications.

![](/_images/_gsender/_edge/gs_ed_notifsv2.jpg){.aligncenter .size-medium}
