---
title: ATC 1st Project
menu_order: 3
post_status: draft
post_excerpt: Quick review of how to safely use your ATC
post_date: 2026-02-09 10:16:53
taxonomy:
    knowledgebase_cat: atc-basics
    knowledgebase_tag: 
custom_fields:
    KBName: AutoToolChanger
    basepress_post_icon: bp-caret-right
skip_file: no
featured_image: _images/post-image.jpg
---

- Wood/Workholding - link to cnc fun
    Makore, Purple heart, soft curly maple
- Design/Toolpaths & Tool numbers
- Saving as one file/Post Processors
- Homing
- Setting Zero
- Dust Shoe
- Run the job

If you haven't yet, go through the [Software Setup](https://resources.sienci.com/view/atc-software/) to initialize your ATC system. You cannot use your ATC until this process is complete.

## ATC Basics

### Tool Changes

Tools in your ATC system are referred to by a tool number, ranging from Tool 1 to Tool 32. A single rack will have 6 tools, while a double rack will hold 12. Any tools above number 12, will be changed out manually. The system detects that the tool number exceeds the rack capacity and moves to the tool rack position so you can replace it manually.

If you didn't purchase a tool rack, all of your tool changes will be done manually.

![](/_images/_atc/_atc_basics/atc_basics_firstpro-autovsmanual.jpg){.aligncenter .size-medium}

### Tool Length Sensor

The system is setup to automatically probe each tool immediately after it's been loaded. This is an automatic process, where the spindle will move over the tool length sensor, and move downwards to touch off on the TLS.

![](/_images/_atc/_atc_basics/atc_basics_firstpro_tooloffsets.gif){.aligncenter .size-full}

Your zeros are stored, so there is no need to re-zero after each tool change!

### Tool Paths

**Creation** - When making tool paths, the tool number associated with the selected tool is used by your ATC to determine the physical tool to load.
Tool #1 will be picked up at rack slot 1. Tool #2 will be picked up at rack slot 2. Etc. There is an option to remap which tool is picked up for a specific tool number, so you don't have to arrange your tools to match the order they are in the rack.

**Exporting** - You will need to install the post-processor provided to enable the ATC to export your toolpaths correctly. Check out the [Before You Begin](https://resources.sienci.com/view/atc-before-you-begin/) section to download your appropriate CAM software post processor.

## First ATC Project: Engraved Rounds

Now that our Automatic Tool Changer with a single rack is installed and configured, it’s time to run a real project.

In this exercise, we’ll cut circular wooden rounds and engrave short phrases on them. The goal is to confirm that our tool numbers, rack positions, and g-code formatting all work together in a multi-tool job.

By the end, we should have finished parts—and confidence that your ATC is running as expected.

### Project Overview

We’ll machine a set of 70–80 mm (3–4") diameter wooden rounds from 6.5 mm (1/4") thick stock. Each piece will include a short engraved phrase. We are keeping the design simple for this first run, — the focus is on verifying smooth, reliable tool changes.

## Tools for This Project

We’ll load the following end mills into the tool holders, then place them into the rack. Confirm their positions are correct once loaded.

![](/_images/_atc/_atc_basics/atc_basics_firstpro-toolsloadedv2.jpg){.aligncenter .size-medium}

**Tool 1 (leftmost position)**  
30° V-bit for engraving the fine text

**Tool 2**  
1/16" downcut end mill for pocketing large blocky text

**Tool 3**  
1/8 Tapered Ball Nose for fun times and fine text

**Tool 4**
1/8" downcut end mill to cut out the cookies

## Material and Workholding

We are being a bit ambitious with this project, by using 3 different types of wood, all at one time. Instead of carving one board at a time with manual tool changes, we’re combining three separate carves into one.

We’ll use the tape-and-glue method for workholding in this project. If you’re unfamiliar with this approach, see the [Fundamentals of Workholding](https://resources.sienci.com/view/cnc-workholding/) for a quick overview.

## Designing the File

We are using Vetric's V-Carve Pro for the design and toolpath sections of this project. We've lined up the boards and placed offsetting circles (cookies) into the design. Next we added our text, sized it down and rotated it 90 degrees to fit our cookies.

![](/_images/_atc/_atc_basics/atc_basics_firstpro-design.jpg){.aligncenter .size-medium}

We’ll keep everything simple and clean. This is a function test, not a design challenge.

## Creating Toolpaths

This design incorporates more tools and toolpaths than you would usually use. Remember, we are testing out the new ATC system, not being as efficient as possible here. We have 4 toolpaths planned, let's check them out.

![](/_images/_atc/_atc_basics/atc_basics_firstpro-toolpathsv2.jpg){.aligncenter .size-medium}

1. We’ll select the single line text and create a V-carve or engraving toolpath using Tool 1. We’ll set a conservative depth. Light engraving is ideal for this first run.

1. Select the large text and the 1/16th bit with a pocket toolpath.

1. Finally, we’ll create the profile toolpath for the circle using Tool 4. We’ll cut outside the vector and through the full material thickness. We’ll be using the tap/glue method, so no need to add tabs to hold the parts in place.

The engraving should run before the profile cut. We’ll confirm each tool has a unique tool number, and we’ll verify our g-code includes proper tool change formatting:

M5
M6 T#
M3 SXXXXX

We’ll export using the recommended post-processor.

## Running the Job

We have the g-code, and we installed the tools. Now we can move on to running the job!

1. Set up any workholding to secure your material on the wasteboard.

1. Connect to gSender

1. Home the machine

* Jog the machine away from the tool rack

* Press Home

1. Load your job onto gSender

* Use the Load File button to select your g-code file

* You should see a "Tool Timeline" with the different toolpaths highlighted in various colours, corresponding to the toolpath colours on the visualizer

1. Load a tool onto the spindle to zero your machine with

* Choose a tool from your rack that has a symmetric, flat end, like a standard flat end mill

* Press Load and select the correct tool number

***insert picture of Load with dropdown

* Remove the bottom of the dust shoe so you can see the end mill

* Jog the machine to where you want the job to start on your material, then use the Z0, X0 and Y0 buttons to zero each axis

* Jog upwards then reattach your dust shoe bottom (you do NOT need to re-zero the Z-axis after jogging)

We are about ready to start cutting. Here are some final precautions you may want to take:

1. Check the Tool Timeline to see if the order of toolpaths and their tool number are correct.

* At any point before running the job, if you need to re-assign tool numbers, use the Remapping button beside each toolpath.

***insert screenshot of remapping button

1. At the Spindle/Laser tab, spin up the spindle to ensure automatic spindle control is working

1. In Config, under Tool Changing, check that the gSender Strategy is set to Ignore

***insert screenshot of this setting

1. Press Start!

With our file loaded, we’ll:

- Home the machine  
- Set our work zero (wasteboard, as we are cutting through material) 
- Turn on dust collection  
- Clear the tool change area  

When we start the program, the machine will begin surfacing. Once complete, the spindle will stop, return to the rack, perform the tool change, and pick up the tapered ball nose end mill before continuing the cut.

We’ll watch the first tool change closely. We should see a smooth release and pickup with no hesitation or vibration. We won’t interrupt the process unless something clearly goes wrong.

## After Cutting

Once the job is complete, we’ll remove the board and cut the tabs. We’ll lightly sand the edges. We can leave the cookies natural, paint-fill the engraving, or apply a clear finish.

The final look is up to us. What matters here is that both tools ran correctly and the change happened automatically.

## What This Project Confirms

If everything completed as expected, we’ve successfully verified:

- Tool numbers match rack positions  
- Multi-tool g-code formatting is correct  
- The ATC performs clean, reliable tool changes  
- Our Altmill is ready for more advanced multi-tool jobs  

From here, we can move on to more complex projects that combine pocketing, profiling, chamfering, and engraving in a single automated workflow.

## gSender Features

### Tool Table

A new Tool Table allows you to manage all tool-related information in one place.

You can now:

Store tool offsets
Assign nicknames to tools
Probe individual tools or complete racks
This makes it much easier to maintain consistent tool setups across jobs.

### Tool Timeline

Tool changes during a job are now represented in a Tool Timeline, giving a clear view of when tool changes occur and which tool is currently active.

This helps users quickly understand multi-tool programs and track job progress more easily.

### Tool Remapping

Tool remapping allows you to adapt a G-code file’s tool numbers to your machine setup without editing the file itself.

This is particularly helpful when:

CAM tool numbers don’t match rack positions
You want to run the same job with a different tool configuration
Tool racks change between jobs
Remapping can now be configured directly inside gSender before running a job.

### ATC Workflow Controls

New controls were added to support day-to-day ATC operation.

You can now:

Load tools - both manually and using the rack
Unload tools - both manually and using the rack
These actions tie directly into ATC macros and make managing tool states much easier during operation.

### Accessory Installation Tool

To make getting started with an Automatic Tool Changer easier, gSender now includes an ATC setup tool that helps guide users through the initial configuration process.

The setup tool walks through the core steps required to configure an ATC system, including importing macro templates, defining rack size and behaviour, and writing the required configuration files to the controller’s SD card. This removes much of the manual setup that was previously required and helps ensure the necessary macros and configuration files are installed correctly.

The goal of the setup tool is to simplify the process of bringing an ATC system online, reducing the chances of configuration mistakes and making it easier for users to get up and running with automated tool changes.

We plan on expanding this tool to various other accessories that need software and controller configuration, such as spindles.


