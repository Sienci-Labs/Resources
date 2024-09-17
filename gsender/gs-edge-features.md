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
skip_file: no
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

For this version of Edge, which we call *New U* we focused on a UI refresh. Our goals for this update are as follows:

- Maintaining gSender primary principles of simplistic unopinionated controls, substitute technical jargon for simple language, and only showing functionality that you need for your specific machine.
- Better support for various screen sizes (from desktop down to phone) and more intuitive, usable touchscreen support.
- More thought into use of space for existing features to not feel like an afterthought and create space for new features to slot in.
- Lower technical debt on the front-end side of the application.

As of version **1.50** the current notable features / improvements to Edge are:

### Available Now

- **New UI Control Screen**
    - **Jog Control**
    - **New DRO**
    - **Endstop buttons**
    - **Visualizer**
    - **Settings**
    - **Running Jobs**-Feed & Laser Speed Bar really got a punch of colour! Use the slider or the + and - buttons to change speed
    - **Alarms** are focused in the top/center of the screen for easier reading
    - **Outline & Start From**
    
    - **Running status bar** is now an endmill, showing your progress through your job visually, in a percentage in in time shown
- **Updated Mobile & Tablet screens**
- **Notification System**
    - **Info button** provides a footprint of your machine information, including firmware modals and pin indication lights
    - **Notification bell** allows you to sort your notifications by tab, showing errors, info and successful jobs completed
    - **Tool is ON** buttons will appear on the top bar if you have the laser or rotary tools enabled

- **Config Tab**

- **Stat/Info Tab**

- **Tool/CAM Tab**

- **Job Files rethunk**
    - **Load File** has been updated to give you more power over your files
    - **Recent Files** listed, just press and load
    - **Last Job** includes the file name, run time and status

### Coming Soon

- **Dark Mode**

### Improved Layout/Control Screen

The program only has one main screen, separated into three major sections:

The top toolbar has all the things you’ll only use occasionally. This includes machine connection on the left side (boxed in red) and gSender’s Settings, Help, and other additional ‘Tools’ on the right (boxed in blue).
The left-side control (boxed in green) has all the functions you need for loading, monitoring, and controlling g-code files and cutting jobs
The right-side control (boxed in purple) has all the functions you need to manually control your CNC when jobs aren’t running. This includes jogging, zero setting, homing, probing, running macros, manual laser / spindle control, and more

We’ve built gSender’s layout around these primary boxed sections so that you can have all of the CNC functionality most hobbyists need on one screen without getting confused about what each button does. If you’re doing anything during a job it’ll be on the left side, if you’re doing anything outside a job it’ll likely be on the right, and if you want greater customization or functionality it’ll be found in the tools or settings.

Another of gSender’s Design Principals is colouring. It can be scary to have an assortment of buttons in front of you and not know what they’re going to do. This is why we made every button on the right-side control that moves the CNC, blue. This means you shouldn’t ever find yourself startled when the machine moves unexpectedly since the colour will help to communicate whether it’s a ‘machine moving’ button or not.

#### Jog Control

![](/_images/_gsender/_edge/jog_controls.jpg){.aligncenter .size-medium}
#### New DRO

![](/_images/_gsender/_edge/dro.jpg){.aligncenter .size-medium}
#### Endstop buttons


#### Visualizer


#### Settings


#### Running Jobs
![](/_images/_gsender/_edge/RunJob.jpg){.aligncenter .size-medium}

#### Running status bar
![](/_images/_gsender/_edge/StatusBar.jpg){.aligncenter .size-medium}

#### Alarms 
![](/_images/_gsender/_edge/alarmstate.jpg){.aligncenter .size-medium}

#### Outline & Start From

### Config Tab
![](/_images/_gsender/_edge/config_main.jpg){.aligncenter .size-medium}

![](/_images/_gsender/_edge/config_tabs.jpg){.aligncenter .size-medium}

![](/_images/_gsender/_edge/config_search.jpg){.aligncenter .size-medium}

![](/_images/_gsender/_edge/app_preferences.jpg){.aligncenter .size-medium}

![](/_images/_gsender/_edge/config_machine_firmware.jpg){.aligncenter .size-medium}

### Stat/Info Tab

### Tool/CAM Tab
![](/_images/_gsender/_edge/tool_cam_icon.jpg){.aligncenter .size-medium}

![](/_images/_gsender/_edge/tool_cam_start.jpg){.aligncenter .size-medium}

### Job Files
![](/_images/_gsender/_edge/file_load.jpg){.aligncenter .size-medium}

### Updated Mobile & Tablet screens
![](/_images/_gsender/_edge/mobile_screens.jpg){.aligncenter .size-medium}

### Notification System
![](/_images/_gsender/_edge/notification.jpg){.aligncenter .size-medium}



  
While gSender Edge, our development version of the application, has been quiet for the last bit, we’d like to share some of the things we’ve been working on for the next release in that channel. Internally, we’re dubbing the next version “New U”, which will bring a new look and feel to the application as a whole.

The core of our next iteration of gSender Edge is a User Interface (UI) refresh with a few specific goals in mind. As gSender has evolved over the years, with new features and support for various new hardware extensions and firmwares, we’ve inevitably run into constraints within the current design - space, look and feel, and responsiveness. We’d like to spend the next Edge cycle addressing these constraints with a few other goals in mind.