---
title: Edge Features
menu_order: 4
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
skip_file: yes
featured_image: _images/_gsender/_edge/gs_edge-cycle.jpg
---

gSender Edge is our test arena for working on new and exciting gSender updates that will eventually be released to everyone. Think of it as a program that you can download independently from traditional gSender that allows you to participate in public Beta testing. This gives you the opportunity to use all the new features that we’re working on and make an impact by giving us feedback to inform the final result, that’s what it’s like to be on the bleeding **Edge**.

Edge isn’t a replacement for gSender in any way - it’s a way for us to test and get feedback on new, bigger features without exposing them to users who may not be interested or causing unexpected bugs. This follows a cycle that can be several months long where:

![](/_images/_gsender/_edge/gs_edge-cycle.jpg){.aligncenter .size-medium}

1. A new Edge version is split off from Main in order to prototype some new functionality and features (you can tell when this happens because the numbering scheme will jump up from 1.1.6 to EDGE-1.2.0, for example)
1. Edge eventually stops adding major features so it can become more refined from user feedback and squashing bugs
1. Once everything seems stable, everything that’s been added to Edge becomes a part of Main gSender so that everyone can now enjoy the new features
1. The process repeats

Downloading Edge is similar to the Main version of gSender and is available on the same page: <a href="https://sienci.com/gSender/" target="_blank" rel="noopener">https://sienci.com/gsender/</a>. The main caveat is that we don’t post the links for each operating system, so once you click the link to download Edge you’ll need to scroll down on the page to the “Assets” and click on the program download for your specific device. For Windows it’ll end in “.exe”, Mac will be “.dmg”, and the rest are for Linux and Pi.

## Unique Differences

If you used to see a feature here but don’t see it any longer, it’s likely been added into the main version of gSender! Look for it on the other gSender documentation pages.

The core of our next iteration of gSender Edge is a User Interface (UI) refresh with a few specific goals in mind. As gSender has evolved over the years, with new features and support for various new hardware extensions and firmware, we’ve inevitably run into constraints within the current design - space, look and feel, and responsiveness. We’ve spent this Edge cycle addressing these constraints with a few other goals in mind. For this version of Edge, which we call **New U** our goals are as follows:

- Maintaining gSender primary principles of simplistic unopinionated controls, substitute technical jargon for simple language, and only showing functionality that you need for your specific machine.
- Better support for various screen sizes (from desktop down to phone) and more intuitive, usable touchscreen support.
- More thought into use of space for existing features to not feel like an afterthought and create space for new features to slot in.
- Lower technical debt on the front-end side of the application.

As of version **1.50-Edge-1** the current notable features / improvements to Edge are:

### Available Now

- **New UI Control Screen**
  - **Jog Control** - Received a makeover including button size, spacing and adding in A axis
  - **New DRO** - Toggle between setting your zeros and going to your zeros, updated end stop buttons
  - **Running Jobs** - Feed & Laser Speed Bar really got a punch of colour! Use the slider or the + and - buttons to change speed
  - **Alarms** - Now focused in the top/center of the screen for easier reading
  - **Outline & Start From** - Start from now has it's own button!
  - **Running status bar** - Upgraded visual is now an end mill, showing your progress through your job visually, in a percentage of time shown

### Coming Soon

- **Updated Mobile & Tablet screens** - Use your phone or your tablet with our power packed mobile UI update

- **Notification System** - gSender wants to tell you something!
  - **Info button** - provides a footprint of your machine information, including firmware modals and pin indication lights
  - **Notification bell** - allows you to sort your notifications by tab, showing errors, info and successful jobs completed
  - **Tool is ON** - buttons will appear on the top bar if you have the laser or rotary tools enabled

- **Config Tab** - A whole new page to dial in your settings or use a wizard to assist

- **Stat/Info Tab** - Review your usage and statistics on this tab

- **Tool/CAM Tab** - Surface a project, prep for a V carve or prepare a flat wasteboard

- **Firmware recognition Feature** - Automatically identify which version you are running

- **Job Files Revamp** - We've made it faster and easier to load and use your files.
  - **Load File** - Updated to give you more power over your files
  - **Recent Files** - Are now listed, just press and load
  - **Last Job** - Includes new details like the file name, run time and status
  
- **Dark Mode** - Run gSender at night while in dark mode. Oooh, spooky.

Much of our effort early on has been dedicated to backend changes, tooling and technology changes, and the “main” control UI of the software. As such, some longstanding features such as surfacing, calibration, etc. are not included in this release - rest assured that these will be coming shortly as we iterate through the remaining features to bring them in line with the UI refresh. There was an enormous effort on the “plumbing” side of things to future proof gSender and now that that’s out of the way, feature development should be quick.

### New Layout/Control Screen

It may look different, but you can take a deep breath and relax, everything is still here. And more! Several tabs have moved from the top of the screen to the left sidebar. This allows us to communicate more in the top bar like status, peripherals in use and notifications.

![](/_images/_gsender/_edge/gs_edge_mainscreenconnected.jpg){.aligncenter .size-medium}

#### Jog Control

Updated jog controls with a new design. Rotary is now a first-class citizen if your firmware reports that it supports one and you’ll find the A jog where you’d expect.

![](/_images/_gsender/_edge/gs_edge_jogcontrol.jpg){.aligncenter .size-medium}

#### New DRO

DRO section slightly reworked - Go To and Zero now separated, A axis is included if your firmware reports it exists or rotary toggled on, and single axis homing is better integrated into the experience with a single toggle.

![](/_images/_gsender/_edge/gs_edge_mainscreenzero.jpg){.aligncenter .size-medium}

![](/_images/_gsender/_edge/gs_edge_mainscreenhome.jpg){.aligncenter .size-medium}

#### Running Jobs

Spindle and Feed overrides now more closely associated with the other workflow controls to make sure your speeds are set correctly before starting a job and if anything goes wrong you have a single place to look to control the job.

![](/_images/_gsender/_edge/gs_edge_runcontrols.jpg){.aligncenter .size-medium}

#### Touch Screen

Secondary widgets get an update to allow for touch screen activation.

![](/_images/_gsender/_edge/gs_edge_secondarywidget.jpg){.aligncenter .size-medium}

---

### Updated Mobile & Tablet screens

![](/_images/_gsender/_edge/gs_edge_mobilescreens.jpg)

#### Running status bar

![](/_images/_gsender/_edge/StatusBar.jpg){.aligncenter .size-medium}

#### Alarms

![](/_images/_gsender/_edge/alarmstate.jpg){.aligncenter .size-medium}

### Config Tab

![](/_images/_gsender/_edge/config_main.jpg){.aligncenter .size-medium}

![](/_images/_gsender/_edge/config_tabs.jpg){.aligncenter .size-medium}

![](/_images/_gsender/_edge/config_search.jpg){.aligncenter .size-medium}

### Tool/CAM Tab

![](/_images/_gsender/_edge/tool_cam_icon.jpg){.aligncenter .size-medium}

![](/_images/_gsender/_edge/tool_cam_start.jpg){.aligncenter .size-medium}

### Notification System

![](/_images/_gsender/_edge/notification.jpg){.aligncenter .size-medium}

#### Settings

![](/_images/_gsender/_edge/app_preferences.jpg){.aligncenter .size-medium}

![](/_images/_gsender/_edge/config_machine_firmware.jpg){.aligncenter .size-medium}
