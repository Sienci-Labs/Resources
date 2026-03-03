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

Now that our Automatic Tool Changer is installed and configured, it’s time to run our first real project.

In this exercise, we’ll cut out circular wooden “cookies” and engrave short sassy sayings on them. The goal is simple: confirm that our tool numbers, rack positions, and g-code formatting all work together in a real multi-tool job.

By the end, we’ll have finished wooden rounds and confidence that our ATC is running as expected.

## What We’ll Be Making

We’ll machine a set of 3–4 inch diameter wooden circles from 1/2"–3/4" thick stock. Each one will be engraved with a short phrase like:

- “Not Today, Stress”
- “Pocket Panic Button”
- “It's not that DEEP”
- “Just NO”

We’ll keep the design simple for this first test. The focus here is the tool changes.

## Tools for This Project

We’ll load the following tools into the rack and confirm their positions match our CAM tool numbers.

**Tool 1 (leftmost position)**  
22 mm surfacing bit

**Tool 2**  
60° or 90° V-bit for engraving the text.

If we choose to add a light edge detail, we can optionally include:

**Tool 3**  
1/8" roundover bit for a finishing pass.

For this first project, two tools are more than enough.

**Tool 4**
1/8" downcut endmill to cut out the cookies

## Material and Workholding

We’ll start with a flat, surfaced board secured firmly to the wasteboard. In this project we are using 5 different types of wood, all 24 inches long. 3 boards are 5", one is 4.5" and the top board is 4". All are 1/4" thick.

We'll be using tape and glue, without screws, as we will be surfacing a tiny bit as our 1st tool.

## Designing the File

In our CAD software, we’ll draw a 3–4 inch circle and center the text inside it. We’ll resize the lettering so it fits comfortably within the boundary. If we want multiple cookies, we’ll duplicate the design and leave at least 1/2" between each part.

We’ll keep everything simple and clean. This is a function test, not a design challenge.

## Creating Toolpaths

We’ll start with the engraving toolpath.

We’ll select the text and create a V-carve or engraving toolpath using Tool 2. We’ll set a conservative depth. Light engraving is ideal for this first run.

Next, we’ll create the profile toolpath for the circle using Tool 1. We’ll cut outside the vector and through the full material thickness. We’ll add tabs to hold the parts in place.

The engraving should run before the profile cut. We’ll confirm each tool has a unique tool number, and we’ll verify our g-code includes proper tool change formatting:

M5
M6 T#
M3 SXXXXX

We’ll export using the recommended post-processor.

## Running the Job

With our file loaded, we’ll:

- Home the machine  
- Set our work zero (top of material is recommended)  
- Turn on dust collection  
- Clear the tool change area  

When we start the program, the machine will begin engraving with the V-bit. Once complete, the spindle will stop, return to the rack, perform the tool change, and pick up the 1/4" end mill before beginning the profile cut.

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