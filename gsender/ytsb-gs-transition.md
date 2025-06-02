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

We've improved the main tab, now called the **Carve Tab**.  The core concept of **things that are blue, move the machine** remains is place. Generally you will use the middle/left side of the screen to load files, control running the job and observing your progress in the visualizer. The right side of the screen will move your machine and allow you to use more advanced machine functions.

We've combined similar features, ard are excited to share things like our new **Stats Tab** which includes things like maintenance tasks, machine diagnostic files, configuration and more.

The new **Config Tab** puts all of your settings into one place, so no more flipping between firmware and profile options.

Rest assured that all of the functionality you are used to is still here, it may simply have a new home. Hopefully this section helps guide you to the new sections, and that you don't skip a beat. Let's dive into some specifics!!

## 🌟 Key UI Enhancements

### **New Tabs**

You will notice right away that as you click through the new UI, there are two section of your screen that are always available to you. The **Top bar** and the **Left bar**.

#### Top Bar

The top bar will show you several cool things, and will always be available to see. Moving from left to right, you will see your connection status, notification bell, machine information, machine status, and shortcuts for remote control, keyboard shortcuts & gamepad profiles.

![](/_images/_gsender/_transition/gs_tr_top-bar.jpg){.align-center .size-medium}

#### Left Bar

On the left side of the screen, you will see 5 tabs. Starting at the top, a **Helper Tab** will aid you in understanding and correcting any errors that pop up. It also includes a tool changing wizard. Your main screen is the cool **Carve Tab**, where you handle files, watch the visualizer, setup jobs, move the machine, probe for zero, manage macros, check out the console and more. Our 3rd **Stats Tab** can be used for examining your machine stats, upcoming maintenance, your recent alarms & errors and your machine configuration. A diagnostic file download is available if you run into trouble, and links to our community, resources and Git Hub repository are also found on this tab. Moving down to the 4th **Tools Tab**, you will see aids to help you surface a project, square or tune your machine and setup your keyboard and gamepad shortcuts. Our final **Config Tab** has combined both your machine settings with the firmware settings. You can search these settings or toggle the ones that have been modified. This left bar will always remain visible to you.

![](/_images/_gsender/_transition/gs_tr_left-bar.jpg){.align-center .size-medium}

### **Automatic Firmware Detection on Connection**

gSender now automatically detects your firmware type upon connection, selecting the appropriate controller settings. This feature simplifies the setup process, especially for users operating multiple machines or switching between different firmware types.

![](/_images/_gsender/_transition/gs_tr_connect-auto.gif){.align-center .size-medium}

### **Streamlined Configuration Menu**

The Config menu has been refined to display only relevant sections based on your machine's connection status and selected profile. It's a combination of your old preferences section mixed with the old firmware section, so all your settings are in one place. Modified settings are highlighted, and a 'Show Modified' toggle allows users to filter and manage settings that have been changed from the machine default. You can reset to default settings at any time.

![](/_images/_gsender/_transition/gs_tr_modified.gif){.align-center .size-large}

### **Updated Jog Controls and DRO**

The jog controls have been redesigned for better ergonomics and touch-screen compatibility. Notably, if your firmware supports a rotary axis, the A-axis jog control is now prominently featured. The Digital Read Out (DRO) section has been refined, separating 'Go To' and 'Zero' functions and integrating single-axis homing toggles for streamlined operations.

![](/_images/_gsender/_transition/gs_tr_dro.gif){.align-center .size-full}

### **Tools Management**

The Tools tab now contains sections to help you surface your project, tune your machine, and create shortcuts or gamepad profiles. Keyboard shortcuts have been standardized across the main and Edge versions, ensuring consistent behavior. Here you can change your keyboard customization, and gamepad support has editable profiles for enhanced control.

![](/_images/_gsender/_transition/gs_tr_tools-main.jpg){.align-center .size-medium}

### **Stats Tab**

The stats tab offers an overview of your Machine, including your recent jobs run, configuration, upcoming maintenance warnings and your recent alarms & errors. You can also download a diagnostic file for extra support, access our resources, community or github repository!

![](/_images/_gsender/_transition/gs_tr_status.jpg){.align-center .size-medium}

### **Enhanced Visualizer and Lightweight Mode**

The visualizer now includes touch zoom capabilities and a revamped Lightweight Mode. Instead of individual toggles, presets control the behavior:

* **Everything**: Disables the visualizer entirely.
* **Lighter**: Uses the SVG visualizer for reduced resource consumption.

![](/_images/_gsender/_transition/gs_tr_lightweight.jpg){.align-center .size-medium}

Toggle Lightweight Mode using the feather icon located on the Visualizer.

### **Portrait Mode and Touch Support**

For users operating on tablets or vertical monitors, gSender now supports Portrait Mode. Simply rotate your device or adjust your display orientation in the operating system to switch layouts. Additionally, pinch gestures now zoom the visualizer, enhancing touch-screen navigation.

![](/_images/_gsender/_transition/gs_tr_portrait.jpg){.align-center size-medium}

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
