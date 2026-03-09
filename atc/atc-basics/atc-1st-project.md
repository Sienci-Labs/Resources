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

# First Project: Sassy Wooden Cookies with the ATC

Now that our Automatic Tool Changer with a single rack is installed and configured, it’s time to run our first real project.

In this exercise, we’ll cut out circular wooden “cookies” and engrave short sassy sayings on them. The goal is simple: confirm that our tool numbers, rack positions, and g-code formatting all work together in a real multi-tool job.

By the end, we’ll have finished wooden rounds and confidence that our ATC is running as expected.

## What We’ll Be Making

We’ll machine a bunch of 70-80mm or 3–4 " diameter wooden circles from 6.5mm or 1/4" thick stock. Each one will be engraved with a short phrase like:

- “Not Today, Stress”
- “Pocket Panic Button”
- “It's not that DEEP”
- “Just NO”

We’ll keep the design simple for this first test. The focus here is the tool changes.

## Tools for This Project

We’ll load the following tools into the rack and confirm their positions match our CAM tool numbers.

![](/_images/_atc/_atc_basics/atc_basics_firstpro-toolsloaded.jpg){.aligncenter .size-medium}

**Tool 1 (leftmost position)**  
22 mm surfacing bit

**Tool 2**  
1/8" tapered ball nose for simple text

**Tool 3**  
30° V-bit for engraving the fine text.

**Tool 4**
1/16" downcut endmill for pocketing large blocky text

**Tool 5**
1/8" downcut endmill to cut out the cookies

![](/_images/_atc/_atc_basics/atc_basics_firstpro-toolorder6.jpg "Tools 1-5 are loaded and ready to carve"){.aligncenter .size-medium}

## Material and Workholding

We are being a bit ambitious with this project, by using 5 different types of wood, all at one time. Instead of carving one board at a time with manual tool changes, we’re combining five separate carves into one. In this project we are using 5 different types of wood, all 609.6mm or 24" long. 3 boards are 127mm or 5", one is 114.3mm or 4.5" and the top board is 101.6mmm or 4". All are 6.35mm or 1/4" thick.

We’ll start by combining  our 5 boards, taped firmly together.

![](/_images/_atc/_atc_basics/atc_basics_firstpro-workholding.jpg){.aligncenter .size-medium}

We'll be using tape and glue, trying to minimize any screws, as we will be surfacing the entire project with our first tool. If you find your boards are a bit warped and need to use a couple screws to fully secure your work, ensure they are counter sunk by at least 1

![](/_images/_atc/_atc_basics/atc_basics_firstpro-workholdglue.jpg){.aligncenter .size-medium}

## Designing the File

We are very close to the maximum size of project in Vectric's Vcarve Pro at 609.6mm X 569.9mm or 24" x 23.5". We've lined up the boards and placed offsetting circles (cookies) into the design. Next we added our text, sized it correctly and rotated it 90 degrees to fit our cookies.

![](/_images/_atc/_atc_basics/atc_basics_firstpro-camdesign.jpg){.aligncenter .size-medium}

We’ll keep everything simple and clean. This is a function test, not a design challenge.

## Creating Toolpaths

This design incorporates more tools and toolpaths than you would usually use. Remember, we are testing out the new ATC system, not being as efficient as possible here. We have 5 toolpaths planned, let's check them out.

![](/_images/_atc/_atc_basics/atc_basics_firstpro-toolpaths.jpg){.aligncenter .size-medium}

1. We’ll start with a very small (.5mm) surfacing, to ensure that all of our material is at the same height. This ensures clean, even depth text on our final cookies. This toolpath is a simple square, covering the entire workpiece. It carves to a depth of .5mm.

1. We’ll select the text and create a V-carve or engraving toolpath using Tool 2. We’ll set a conservative depth. Light engraving is ideal for this first run.

Next, we’ll create the profile toolpath for the circle using Tool 1. We’ll cut outside the vector and through the full material thickness. We’ll add tabs to hold the parts in place.

The engraving should run before the profile cut. We’ll confirm each tool has a unique tool number, and we’ll verify our g-code includes proper tool change formatting:

M5
M6 T#
M3 SXXXXX

We’ll export using the recommended post-processor.

## Running the Job

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


Tool Table
A new Tool Table allows you to manage all tool-related information in one place.

You can now:

Store tool offsets
Assign nicknames to tools
Probe individual tools or complete racks
This makes it much easier to maintain consistent tool setups across jobs.

Tool Timeline
Tool changes during a job are now represented in a Tool Timeline, giving a clear view of when tool changes occur and which tool is currently active.

This helps users quickly understand multi-tool programs and track job progress more easily.

Tool Remapping
Tool remapping allows you to adapt a G-code file’s tool numbers to your machine setup without editing the file itself.

This is particularly helpful when:

CAM tool numbers don’t match rack positions
You want to run the same job with a different tool configuration
Tool racks change between jobs
Remapping can now be configured directly inside gSender before running a job.

ATC Workflow Controls
New controls were added to support day-to-day ATC operation.

You can now:

Load tools - both manually and using the rack
Unload tools - both manually and using the rack
These actions tie directly into ATC macros and make managing tool states much easier during operation.

Accessory Installation Tool
To make getting started with an Automatic Tool Changer easier, gSender now includes an ATC setup tool that helps guide users through the initial configuration process.

The setup tool walks through the core steps required to configure an ATC system, including importing macro templates, defining rack size and behaviour, and writing the required configuration files to the controller’s SD card. This removes much of the manual setup that was previously required and helps ensure the necessary macros and configuration files are installed correctly.

The goal of the setup tool is to simplify the process of bringing an ATC system online, reducing the chances of configuration mistakes and making it easier for users to get up and running with automated tool changes.

We plan on expanding this tool to various other accessories that need software and controller configuration, such as spindles.