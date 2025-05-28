---
title: ytsb Transition
menu_order: 2
post_status: draft
post_excerpt: An overview of the changes from the classic UI to the new and improved UI.
post_date: 2021-07-01 14:21:00
taxonomy:
    knowledgebase_cat: gdocs
    knowledgebase_tag:
        - gsender
custom_fields:
    KBName: gSender
    basepress_post_icon: bp-caret-right
skip_file: no
featured_image: _images/_gsender/_transition/gs_tr_top-bar.jpg
---

The recent merge of gSender Edge 1.5.0 into our main gSender introduces a comprehensive overhaul of the user interface, enhancing usability, responsiveness, and functionality. This guide will help to familiarize current users with the UI changes, to ensure a smooth transition.

The core concept of **things that are blue, move the machine** remains is place. Generally you will use the middle/left side of the screen to load files, control running the job and observing your progress in the visualizer. The right side of the screen will move your machine and allow you to use more advanced machine functions. Let's dive into some specifics!!

## 🌟 Key UI Enhancements

### **New Tabs**

You will notice right away that as you click through the new UI, there are two section of your screen that are always available to you. The **Top bar** and the **Left bar**.

#### Top Bar

The top bar will show you several cool things, and will always be available to see. You will see your connection status, notification bell, machine information, machine status, and shortcuts for remote control, keyboard shortcuts & gamepad profiles.

![](/_images/_gsender/_transition/gs_tr_top-bar.jpg){.align-center .size-medium}

#### Left Bar

On the left side of the screen, you will see 5 tabs. A helper that will aid you in understanding and correcting any errors that pop up, your main carve screen, a tab for examining your machine stats, a tab for all of your tools, and an expanded configuration tab. This left bar will always remain visible to you.

![](/_images/_gsender/_transition/gs_tr_left-bar.jpg){.align-center .size-medium}

### **Updated Jog Controls and DRO**

The jog controls have been redesigned for better ergonomics and touch-screen compatibility. Notably, if your firmware supports a rotary axis, the A-axis jog control is now prominently featured. The Digital Read Out (DRO) section has been refined, separating 'Go To' and 'Zero' functions and integrating single-axis homing toggles for streamlined operations.

![](/_images/_gsender/_transition/gs_tr_dro.jpg){.align-center .size-medium}

### **Tools Management**

The Tools tab now contains wizards to help you surface your project, tune your machine, and create shortcuts or gamepad profiles. Keyboard shortcuts have been standardized across the main and Edge versions, ensuring consistent behavior. Here you can change your keyboard customization, and gamepad support has editable profiles for enhanced control.

![](/_images/_gsender/_transition/gs_tr_tools-main.jpg){.align-center .size-medium}

### **Streamlined Configuration Menu**

The Config menu has been refined to display only relevant sections based on your machine's connection status and selected profile. Modified settings are highlighted, and a 'Show Modified' toggle allows users to filter and manage non-default configurations efficiently. You can reset to default settings at any time.

![](/_images/_gsender/_transition/gs_tr_modified.gif){.align-center .size-large}

### **Automatic Firmware Detection**

gSender now automatically detects your firmware type upon connection, selecting the appropriate controller settings. This feature simplifies the setup process, especially for users operating multiple machines or switching between different firmware types.

![](/_images/_gsender/_transition/gs_tr_connect-auto.gif){.align-center .size-medium}

### **Job Progress and Recovery Enhancements**

The job progress bar has been updated with animations for better visual feedback. In the event of interruptions, the 'Start from Line' function now accurately displays the last executed line, facilitating seamless job recovery.

![](/_images/_gsender/_transition/gs_tr_start-from.jpg){.align-center .size-medium}

### **Enhanced Visualizer and Lightweight Mode**

The visualizer now includes touch zoom capabilities and a revamped Lightweight Mode. Instead of individual toggles, presets control the behavior:

* **Everything**: Full animations and visualization.
* **Lighter**: Uses the SVG visualizer for reduced resource consumption.
* **Off**: Disables the visualizer entirely.

![](/_images/_gsender/_transition/gs_tr_lightweight.jpg){.align-center .size-medium}

Toggle Lightweight Mode using the feather icon located on the Visualizer.

### **Portrait Mode and Touch Support**

For users operating on tablets or vertical monitors, gSender now supports Portrait Mode. Simply rotate your device or adjust your display orientation in the operating system to switch layouts. Additionally, pinch gestures now zoom the visualizer, enhancing touch-screen navigation.

### **Dark Mode**

Responding to user requests, gSender now offers a Dark Mode for reduced eye strain and improved visibility in low-light environments. Activate it via **Config > Customize UI > Enable Dark Mode**.

![](/_images/_gsender/_transition/gs_tr_darkmode.gif){.align-center .size-large}

## 🛠️ Additional Noteworthy Features

* **Console Enhancements**: Added console clearing functionality and arrow-scrollable input history for improved usability.
* **Navigation Improvements**: Breadcrumb navigation is being introduced in certain sections for easier backtracking.
* **Visual Tweaks**: Numerous UI adjustments, including updated icons, responsive sidebar sizing, and improved text legibility.

## 📘 Getting Started with the New UI

To explore these new features:

1. **Download gSender Edge 1.5.0**: Access the latest version from the [Sienci Labs GitHub repository](https://github.com/Sienci-Labs/gsender/releases).
2. **Refer to the Official Documentation**: The [gSender Docs](https://resources.sienci.com/view/gs-using-gsender/) provide comprehensive guidance on utilizing the software's capabilities.
3. **Engage with the Community**: Share your experiences, provide feedback, and seek assistance on the [Sienci Community Forum](https://forum.sienci.com/).

By familiarizing yourself with these updates, you can leverage the enhanced functionality and improved user experience that gSender Edge 1.5.0 offers!
