---
title: ytsb Quick Start Guide
menu_order: 8
post_status: draft
post_excerpt: Use the quick start guide as a checklist when running a project.
post_date: 2023-08-30 11:56:18
taxonomy:
    knowledgebase_cat: vx-assembly
    knowledgebase_tag:
        - vortex
custom_fields:
    KBName: Vortex Rotary Axis
    basepress_post_icon: bp-caret-right
skip_file: no
featured_image: _images/post-image.jpg
---

If you want to jump right in with your own project instead of following along with <a href="https://resources.sienci.com/view/vx-first-project/">Your First Project</a> and <a href="https://resources.sienci.com/view/vx-second-project/">Your Second Project</a>, fear not! Check out our video where Johann goes step by step on how to get setup and start quickly for each Vortex project.

The video below shows the Open Loop Vortex. For **Closed Loop Vortex, use 4th Axis Mode** instead of Rotary Mode on gSender. **Closed Loop Vortex must use 4th Axis Mode at all times!**

https://www.youtube.com/watch?v=njbUQo0OzLY

### Rotary Mode vs. 4th Axis Mode

gSender has a unique ability to control a rotary axis on standard, 3-axis grbl machines. We call this “Rotary Mode.” Rotary Mode works by leveraging the Y-axis to control the A-axis. By switching to Rotary Mode, gSender automatically changes the firmware settings in order to translate A-axis movements to your machine, as if they were Y-axis movements.

4th Axis Mode allows you to use the rotary axis without piggybacking on the Y-axis, therefore allowing for XYZ motion at the same time as A-axis motion.

**If you have an Open Loop Vortex, use Rotary Mode.**

**If you have a Closed Loop Vortex, use 4th Axis Mode.**

### Enabling Rotary Controls

Navigate to the gear at the top right of gSender, where you will find the rotary settings. Here you can toggle the rotary controls to make them visible on the main page.

![](/_images/_vortex/_assembly/vx_quick_gs-rotary-enable.gif){.aligncenter .size-full}

Once the toggle has been turned to display, you will see an additional tab at the bottom right of the window, called Rotary. With this tab you can:

1. **Jog Control** – Rotate the A-axis, go to Zero, set Zero, and adjust speeds
1. **Rotary Mode** – Switch to Rotary Mode or 4th Axis Mode
   - Open Loop Vortex → use Rotary Mode
   - Closed Loop Vortex → use 4th Axis Mode
1. **Rotary Surfacing** – Wizard to turn square stock round
1. **Probe Rotary Z-axis** – Automatically probe to find the Z-axis
1. **Y-axis Alignment** – Automatically probe to align the Y-axis along the A-axis
   - Do this before switching to Rotary Mode
   - Not accessible when Rotary Mode is enabled, should disable rotary controls
1. **Rotary Mounting Setup** – Drill holes in your wasteboard to mount the track
   - Do this before switching to Rotary Mode
   - Not accessible when Rotary Mode is enabled,  should disable rotary controls

![](/_images/_vortex/_assembly/vx_quick_gs-rotary-controls.png){.aligncenter .size-full}

### Workflow Overview

You can use the list below as a quick reminder on how to start each project you run on the Vortex.

#### Switching To the Vortex

1. Mount track on wasteboard
1. Raise your router
1. Jog all the way back to align X-axis
1. Plug in touch probe & magnet
1. Use gSender’s Y-Axis alignment wizard
1. For open loop, plug in A-axis into the Y-axis outputs on your controller
1. For open loop, flip the toggle switch towards yourself
1. Ensure 4th Axis (closed loop) or Rotary Mode (open loop) is enabled on gSender

#### Homing on the Vortex

In Rotary or 4th Axis Mode, home the A-axis in gSender (do not home all axes). This is only applicable if you have limit switches installed.

#### Workholding

1. Install correct jaw set
1. Attach faceplate or use jaws to hold stock

#### Using the Tailstock

1. Slide against end of stock
1. Match center to divot
1. Turn live center away from yourself to tighten
1. Lock the live center with the red knob

#### Setting Your Zero

1. Jog bit to the right to clear faceplate and workholding
1. Click **Zero X**
1. Rotate your stock if you want it facing a certain direction
1. Click **Zero A**
1. Plug in touch probe & magnet
1. Jog bit to top of headstock
1. Click **Probe Rotary Z-Axis**

#### Rotary Surfacing

1. Measure largest dimension
1. Measure length
1. Click Rotary Surfacing in gSender
1. Enter measurements and select **Stepdown**
1. Click **Generate G-code**
1. Click **Run on Main Visualizer**
1. Click **Start Job**

### Next Steps

For in-depth, step-by-step procedures on how to create your first few projects, please see <a href="https://resources.sienci.com/view/vx-first-project/">Your First Project</a> and <a href="https://resources.sienci.com/view/vx-second-project/">Your Second Project</a>.

For detailed information about what each functionality in the rotary controls do, please see ​​our <a href="https://resources.sienci.com/view/gs-additional-features/#rotary">Rotary SLB documentation.</a>

Good luck & have fun!

![](/_images/_vortex/_assembly/vx_quick_carving-queen.gif){.aligncenter .size-full}
