---
title: Running Jobs Checklist
menu_order: 0
post_status: draft
post_excerpt: How to cut multiple toolpaths for CAM programs without tool changing functionality. This method is suitable for the LongMill Benchtop CNC, and other hobby CNCs.
post_date: 2024-07-18 18:14:53
taxonomy:
    knowledgebase_cat: gen-handbook 
    knowledgebase_tag:
        - gen
        
custom_fields:
    KBName: General CNC
    basepress_post_icon: bp-caret-right
skip_file: no
featured_image: 
---

## Preparing Your Design

### Material Size and Type

Before you can start your design, you must know the size and thickness of your material. This is necessary for generating successful toolpaths. Your design should also take into account the material type. Machining different materials will result in different feeds and speeds that will be determined in the CAM software.

![](/_images/_lmmk2/_handbook/lmk2_runjobs_measuring-materials.jpg){.aligncenter .size-medium}

#### File Creation

Design, CAM, and Machine Interface software are all used to create the final file for your project. Detailed information about software and the CNC tool chain can be found here. <a href="https://resources.sienci.com/view/lmk2-software-explained/" target="_blank" rel="noopener">https://resources.sienci.com/view/lmk2-software-explained/</a>. In the following explanation, Carbide Create and gSender will be used for the Design/CAM and Machine Interface software examples.

#### Design Software

A design is needed to create the toolpath. You can use a pre-made design or create one yourself. CAD software like Fusion 360 & SketchUp are useful for creating 3D files with complex shapes. Graphic programs like Adobe Illustrator or Inkscape are perfect to create files for signs and simple 2.5D carvings.

#### CAM Software

We’ll now switch to the CAM software. Remember those material dimensions you took earlier, you’ll now input them into your new file. Choose the X and Y location of the zero point in the software. The Z location will either be at the top or at the bottom of the material. The starting or zero point is where the machine will reference from. In the example below, you can see the zero starts at the same location in the software and on the material.

![](/_images/_lmmk2/_handbook/lmk2_runjobs_starting-position-triptych.jpg){.aligncenter .size-medium}

Import your design file into the CAM software. You’ll now choose the CNC bit to create the toolpath. The shape and type of bit will determine the final look of your piece.

#### Choosing your CNC Tool

CNC bits come in a variety of shapes and sizes. You don’t need a specialty bit to get started. Common router bits are a great way to get your feet wet with machining without spending a lot of money. Common bit shapes are: V-bits; great for signs and lettering. Square End mills; used for carving pockets with flat surfaces. Ball nose and tapered bits; used for relief and detail carvings.

![](/_images/_lmmk2/_handbook/lmk2_runjobs_cnc-bit-types.jpg){.aligncenter .size-medium}

#### Creating Toolpaths

Select the vector lines you want to machine then select the CNC bit. Change any parameters such as feed and speeds for your machine and material. Information on feeds and speeds can be found here. <a href="https://resources.sienci.com/view/lmk2-feeds-and-speeds" target="_blank" rel="noopener">https://resources.sienci.com/view/lmk2-feeds-and-speeds</a>/ The CAM software will calculate the toolpath. In the example below, the design is in orange, and the toolpaths are blue. Once you are happy with the design, export the g-code.

![](/_images/_lmmk2/_handbook/lmk2_runjobs_toolpath-example.jpg){.aligncenter .size-medium}

#### Exporting the File

With the design finalized, it’s time to export the toolpaths. Make sure you’ve selected the correct post-processor for your machine. The LongMill uses a grbl post-processor. Save or export your toolpath to a location on your computer.

## Preparing your Material

### Material Clamping

Clamping material to the work surface is necessary for a successful part. Clamping methods are determined by the design and material you are using. Below are common examples of clamping methods. Small items could be held in a vice with some care. Clamps can be made out of metal, plastic, or wood.

#### Top Clamping

Hold down clamps hold the material tightly to the work surface. Top clamping is perfect when using upcut bits. Careful consideration must be given to the placement of the clamps in order to prevent the bit from cutting into them.

![](/_images/_lmmk2/_handbook/lmk2_runjobs_clamps-hold-and-eccentric-scaled.jpg){.aligncenter .size-medium}

#### Side clamping

Holding your workpiece with pressure from the sides is useful for flattening the top of a workpiece or doing 3d reliefs where the design extends to the edges. Eccentric clamps or angled blocks pressed against material work well.

![](/_images/_lmmk2/_handbook/lmk2_runjobs_side-clamping.jpg){.aligncenter .size-medium}

#### Screws

Screwing through your material and into the work surface is an excellent holding method. Extra care needs to be taken that you don’t run the bit through the metal screws.

![](/_images/_lmmk2/_handbook/lmk2_runjobs_fastening-screws.jpg){.aligncenter .size-medium}

#### Tape and Glue

Tape is applied to the back of the workpiece and to the top of the work surface. Apply fast-acting glue to the work surface and place the workpiece on top with pressure until set. Once finished, remove the tape. Hot gluing your material to the table is also an effective way to hold the piece down when doing light machining.

![](/_images/_lmmk2/_handbook/lmk2_runjobs_mounting-gluing.jpg){.aligncenter .size-medium}

Double sided carpet tape is very easy to use. It’s applied to the work surface, then the work piece is pressed to the table.

![](/_images/_lmmk2/_handbook/lmk2_runjobs_mounting-carpet-tape.jpg){.aligncenter .size-medium}

## Installing the Cutting Tools

Bring the machine to the front so you have easy access to the router and collect the two wrenches that are included in the Makita box. If this is your first time using a router, look at the bottom where it has a large hex nut and notice just above this the two flats cut into the router shaft. You’ll be using the two wrenches here, one on the nut and one on the flats of the shaft, so the router can ‘clamp’ onto bits before cutting and then release them when you’re finished.

![](/_images/_lmmk2/_handbook/lmk2_runjobs_router-shaft-notch.jpg){.aligncenter .size-medium}

To loosen the collet nut, place the small wrench onto the router shaft on the left side. Place the large wrench on the collet nut on the right side. Squeeze the wrenches together till the collet nut is loosened.

![](/_images/_lmmk2/_handbook/lmk2_runjobs_collet-loosen.jpg){.aligncenter .size-medium}

Always make sure the collet, the adapter, and the nut are free from debris before running. Dust buildup will prevent the collet from being tightened correctly and can ruin a workpiece. Dust can build in the inside corners of the nut and will prevent proper tension. Clean with a small tool or compressed air.

![](/_images/_lmmk2/_handbook/lmk2_runjobs_dirty-collet-and-adapter.jpg){.aligncenter .size-medium}

1/4” diameter straight bits can be installed into the collet first then inserted through the nut before installing into the router.

![](/_images/_lmmk2/_handbook/lmk2_runjobs_4th-bit-install.jpg){.aligncenter .size-medium}

When using ⅛” bits, an adapter or ⅛” collet is necessary. Slide the ⅛” collet adapter into the standard collet, insert your bit, then place it into the collet nut and fasten to the router. The collet adapter should just peak through the bottom of the collet.

![](/_images/_lmmk2/_handbook/lmk2_runjobs_8th-bit-install.jpg){.aligncenter .size-medium}

![](/_images/_lmmk2/_handbook/lmk2_runjobs_collet-adapter-installed.jpg){.aligncenter .size-medium}

Some bits like v-bits or surfacing bits require the bit shaft to be placed through the nut first, then into the collet.

![](/_images/_lmmk2/_handbook/lmk2_runjobs_collet-v-bit-triptych-1.jpg){.aligncenter .size-medium}

When installing the bits into the router, always tighten using the wrenches. The router can be damaged using the button and wrench when tightening. Loose bits can be tricky. Hold the bit in place with one finger. Press the red button with your thumb to lock the shaft in place. With the other hand finger tighten the collet nut till the bit can be held on its own. Use both wrenches to tighten firmly. <a href="https://www.YouTube.com/watch?v=LFeBRBjBYbk" target="_blank" rel="noopener">IDC Woodcraft has a great video outlining these sorts of things to watch out for.</a>

![](/_images/_lmmk2/_handbook/lmk2_runjobs_red-button-fingertighten.jpg){.aligncenter .size-medium}

To tighten the collet nut, the small wrench is on the right side of the router shaft. Place the large wrench on the collet nut on the left side. Squeeze together until the nut is tight, do not over tighten.

![](/_images/_lmmk2/_handbook/lmk2_runjobs_collet_tightening-wrenches.jpg){.aligncenter .size-medium}

## Zeroing Your CNC

It’s important to have the same start location on your workpiece as in your design file. Zeroing the machine can be accomplished in two ways, manually or automatically. Open machine interface software such as gSender or UGS and connect to your machine.

![](/_images/_lmmk2/_handbook/lmk2_runjobs_starting-position-triptych.jpg){.aligncenter .size-medium}

### Manual Zeroing

Manually jog your machine to the starting location. Zero the X and Y locations. Below are two examples of typical start locations; bottom left corner or centre of the material.

![](/_images/_lmmk2/_handbook/lmk2_runjobs_manual-zero-diptych.jpg){.aligncenter .size-medium}

Lower the bit to the material by jogging the Z-axis down. When you are just above the surface, change to precise jogging. Place a piece of paper under the bit. Move the paper back and forth and at the same time, lower the bit. When there is resistance sliding the paper, the bit is at the correct position. Zero the Z location in the software. Raise the bit, go to your x and y starting positions and you’re ready to begin.

![](/_images/_lmmk2/_handbook/lmk2_runjobs_Manual-zero-z-1.jpg){.aligncenter .size-medium}

### Automatic Zeroing

Automatic zeroing or probing works by touching a conductive plate with your cnc bit to find the coordinates on the workpiece. The touch plate can find a single axis per probe or multiple axes. Our auto-touch plate allows you to use v-bits for automatic probing.<a href="https://resources.sienci.com/view/lmk2-touch-plate/#AutoZero-touch-plate" target="_blank" rel="noopener"> https://resources.sienci.com/view/lmk2-touch-plate/#autozero-touch-plate</a>
To find the XYZ axes, place the touch plate on a corner of the material and perform the XYZ probe operation. The router will automatically move through all three axes. It will touch on the top and two sides to accurately find the corner. Detailed information can be found here <a href="https://resources.sienci.com/view/gs-using-gSender/#probing" target="_blank" rel="noopener">https://resources.sienci.com/view/gs-using-gsender/#probing</a>

![](/_images/_lmmk2/_handbook/lmk2_runjobs_probing-triptych.jpg){.aligncenter .size-medium}

When you only want to do a z-height probe, useful for multi-bit tool changes, flip the touch plate upside down. Use the Z probe function This will find the top surface of the material.

![](/_images/_lmmk2/_handbook/lmk2_runjobs_tool-change-zprobe.jpg){.aligncenter .size-medium}

If you have limit switches installed, you might encounter an Alarm 2 message. Your material is too close to the sensors for the machine to travel safely. Move your material away from the sensors and begin your probe operation.

![](/_images/_lmmk2/_handbook/lmk2_runjobs_alarm2.jpg){.aligncenter .size-medium}

## Pre-Flight Check-List

Sometimes it’s useful to have a list of operations next to your machine. We’ve compiled a list to confirm everything is ready to go before hitting Start.

1. Ensure material is square with spoil board/machine
1. Tighten clamps
1. Correct bit installed
1. Collet tightened
1. Correct router speed
1. Correct g-code loaded
1. Home machine - if using limit switches
1. Zero X and Y axes
1. Zero Z axis
1. Check toolpath won’t hit clamps
1. Turn on router
1. Turn on dust collection
1. Start job

## Overriding the Machine for Fine Tuning

Sometimes when you start the job, you’ll need to make adjustments to the machine for proper chip load.

### Feed Rate Using gSender

When a job has been started, gSender will shoe a feed adjustment control panel beside the machining time. Clicking on the plus or minus button will adjust the feed rate faster and slower. The chart below shows what each of the buttons do.

![](/_images/_lmmk2/_handbook/lmk2_runjobs_feed-Rate-adjustment..jpg){.aligncenter .size-full}

[su_table responsive="yes"]
<table>
<tbody>
<tr>
<td style="text-align: center;"><strong>- -</strong></td>
<td style="text-align: center;"><strong>-</strong></td>
<td style="text-align: center;"><strong>+</strong></td>
<td style="text-align: center;"><strong>++</strong></td>
<td style="text-align: center;"><strong>&lt;--</strong></td>
</tr>
<tr>
<td>Decrease speed 10%</td>
<td>Decrease speed 2%</td>
<td>Increase speed 2%</td>
<td>Increase speed 10%</td>
<td>Reset to Original speed</td>
</tr>
</tbody>
</table>
[/su_table]

It’s important to remember, however, that while you may want to modify the cutting feed rate for some cutting operations, the machine will continue using this feed rate override for subsequent cutting operations. For example, if you’ve overridden the feed rate by 200% while cutting the outline of your project at very shallow depths, you’ll want to reset the feed rate to its original speed before it next moves on to cutting out a pocket at a much deeper depth.

### Spindle Speed

The RPM on the router can be changed on the fly by rotating the dial indicator to a faster or slower speed. Below are approximate RPMs for each number on the dial.

[su_table responsive="yes"]
<table>
<tbody>
<tr>
<td><strong>Dial #</strong></td>
<td style="text-align: center;"><strong>1</strong></td>
<td style="text-align: center;"><strong>2</strong></td>
<td style="text-align: center;"><strong>3</strong></td>
<td style="text-align: center;"><strong>4</strong></td>
<td style="text-align: center;"><strong>5</strong></td>
<td style="text-align: center;"><strong>6</strong></td>
</tr>
<tr>
<td><strong>RPM</strong></td>
<td style="text-align: center;">10,000</td>
<td style="text-align: center;">12,000</td>
<td style="text-align: center;">17,000</td>
<td style="text-align: center;">22,000</td>
<td style="text-align: center;">27,000</td>
<td style="text-align: center;">30,000</td>
</tr>
</tbody>
</table>
[/su_table]

## Tool Changing

As you begin tackling more complex CNC projects, you'll start to notice that running multi-tool jobs becomes a necessity. Using multiple bits on the same workpiece can save time or achieve greater detail and give you the carving flexibility you need; whether it's a v-bit for engraving and an end mill for profiling, or an end mill for roughing and a tapered bit for finishing.

### Method 1: Separate Files

This is the easiest and most straight forward approach to tool changing. Many CAM programs allow for each toolpath to be exported as separate files. By creating separate g-code files for each cutting tool you'll be using, you can just:

1. Start with your first tool and first file
1. Wait for the file to complete then jog your router off to the side
1. Change the cutting tool out for the second one
1. Use a touch plate or tool length sensor to measure the new zero point (off your wasteboard or material, depending on how you set up the job)
1. Reposition and run the second file
1. Repeat this process until completion

Just be sure to give each file a clear naming scheme so you execute them in the right order and with the right tool. For example, your first file could be called "cat_1_v-bit", then your second "cat_2_endmill", and your third "cat_3_tapered". You can also specify the tool size or angle, any other prompts that ensure you run the order of files successfully with their corresponding bits.

### Method 2: Manual Editing

This method will also work for g-code sending programs that do not have tool changing functionality, the difference with this one is that all the toolpaths will be in one file. The instructions below are written in millimetre values, however you can replace the values to be in inches as long as the g-code was generated using inches.

This is a tool change method inspired by the work of Stuart McRae (a LongMill customer).

#### Setup

1. Generate your g-code to the file format .nc or .gcode.
1. Zero your machine in the X, Y, and Z on the mounted stock material.
1. Open up the g-code using NC Viewer and check the first few lines for the callout of the correct units (G20 for inches, G21 for mm) and for G90, absolute coordinates.
1. Go line by line to find where the tool changes should occur, by looking at the toolpath visualization on NC Viewer. Use your mouse or keyboard to move to each line, and you should see an end mill following the coordinates called out in the g-code.
1. Add the following g-code for each tool change.

  [su_table responsive="yes"]

  <table>
  <tbody>
  <tr>
  <td><strong>G-code</strong></td>
  <td><strong>Explanation</strong></td>
  </tr>
  <tr>
  <td>Z20.00</td>
  <td>Raises the bit to 20mm above your zero.</td>
  </tr>
  <tr>
  <td>X?.??Y?.??</td>
  <td>Moves bit to a defined XY position. This is the location of your tool change. CHANGE THIS to a position in which the stock material hasn’t been cut, and is accessible.</td>
  </tr>
  <tr>
  <td>M0;</td>
  <td>Pauses job. This is when you turn off the router, change your bit and lower your router manually via Z-axis pulley to zero the bit with a piece of paper. Once you are done you will turn on the router and press PLAY on the g-code sender program.</td>
  </tr>
  <tr>
  <td>G92Z0.125</td>
  <td>Sets the current Z position as 0.125mm (paper thickness) above your zero. So it now knows where the Z-axis zero is.</td>
  </tr>
  <tr>
  <td>G0Z25.00</td>
  <td>Raises your bit 25mm above your zero.</td>
  </tr>
  </tbody>
  </table>
  [/su_table]
1. Save the g-code you just edited as a new file on your computer.
1. Load the file into your g-code sender program.
1. The machine will run through the first toolpath, cutting into the material, then will lift up and move to the bit changing position you defined. It will stop moving, in a HOLD state, until you press PLAY. Complete the tool change and zero the machine manually - note that the surface will be marked by the bit once you turn your router back on.
1. Repeat Step 8 for each tool change.

Below are some examples of how to input the tool changing g-code, which are **bolded**.

##### EXAMPLE 1: Carbide Create

G90  
G21  
(Toolpath 3)  
M05  
M0 ;T102  
M03S18000  
G0X12.00Y10.41Z5.00  
G1Z-1.00F457.2  
X36.00F1524.0  
Z5.00  
(Toolpath 4)  
**Z20.00**  
**X5.00Y20.00**  
**M0 ;T201** // this line was already in the g-code  
**G92Z0.125**  
**G0Z25.00**  
S18000  
G0X12.26Y22.84  
G1Z-1.00F381.0  
X36.26F2286.0  
Z5.00  
M05  
M02

_____________________________________
##### EXAMPLE 2: CAMLab

G21  
G90  
G0 X7.2948 Y-8.1954 Z2.0  
G1 Z-0.6522 F2000  
G1 X-16.3552  
G1 Y-8.2454  
G1 X7.2948  
G1 Y-8.1954  
G0 Z2.0  
G0 Y8.6204  
G1 Z-0.6522  
G1 Y8.6704  
G1 X-16.3552  
G1 Y8.6204  
G1 X7.2948  
G0 Z2.0  
**Z20.00**  
**X5.00Y20.00**  
**M0;**  
**G92Z0.125**  
**G0Z25.00**  
…

### Method 3: gSender Tool Change

The g-code for tool changing is an M6 command, in which the program will pause until the user tells it to continue, usually through a ‘Resume’ and/or ‘Confirm Tool Change’ button on the machine interface program. In CAM programs, this M6 will be inserted in your g-code if there are toolpaths using different bits, thus requiring tool changes. On <a href="https://sienci.com/gSender/" target="_blank" rel="noopener">gSender</a>, you can program what happens when there is M6 in your g-code, therefore allowing you to easily change your bits with pre-programmed actions. Full instructions can be found <a href="https://resources.sienci.com/view/gs-additional-features/#tool-changing" target="_blank" rel="noopener">here</a>.

## Post-Processing Work Pieces

Now that you’ve got your piece machined out, finish the design with a nice smooth finish or an amazing paint job.

### Sanding

Depending on your project, getting into the crevices of your design can be difficult. Small scrapers are handy to remove fuzzy bits. Cone Sanders are useful for larger designs. What if you carved a 3D relief? Sanding mops in different grits work great here. They can get into the details without removing too much material and ruining the design.

### Painting/Staining

There are a few ways to add colour to your work piece. Wood stains help enhance the grain of the wood and should be finished with a good sealer Multi-Colour painting can really make a sign pop. Use a masking film

### Sealing/Finishing

To protect the surface and details of your project, a finishing product such as wax, lacquer, varnish, or epoxy can be used. On projects such as a cutting board or serving tray that may encounter water, or be used in direct contact with food, the appropriate food-safe finish should be used to seal your project.


In preparation for a job on the AltMill, you can use this general checklist to keep track of what your next step is. Feel free to either print this out or press the checkboxes on this page - refreshing the page will reset the boxes.

### In CAM

 X0Y0 is set at the center or corner of material, Z0 is set on top of spoilboard or material  Feeds and speeds are appropriate for the cutting tool and material size  Correct post processor is selected for milling, rotary or laser

### At the CNC, with gSender

 _Spindle_: VFD is plugged into power  Correct firmware upon connection (grbl or grblHAL)  Workspace preset correctly selected (e.g. G54)  _Sensors:_ CNC is homed  Material secured onto spoilboard  Collet and collet nut are cleaned  Correct cutting tool is installed  _Touch plate:_ Correct touchplate is selected in Config, and magnet is attached  Zeros are set and match the X0Y0Z0 from CAM G-code project file is loaded  Project is correctly positioned and does not interfere with workholding  CNC is able to reach material depth within travel limits, with the cutting tool installed  If jogging around, pressing "Go X,Y, Z" moves CNC to the expected X0, Y0, Z0 locations  Dust collection is attached and clear of CNC's way  Spoilboard is clear of loose items  Safety glasses and hearing protection equipped  Router/spindle is jogged a little above the material  _Router:_ Speed dial adjusted, router turned on Dust collection is turned on  **Start Job!**


In preparation for a job on the AltMill, you can use this general checklist to keep track of what your next step is. Feel free to either print this out or press the checkboxes on this page — refreshing the page will reset the boxes.

### In CAM
- [ ] X0Y0 is set at the center or corner of material; Z0 is set on top of spoilboard or material.
- [ ] Feeds and speeds are appropriate for the cutting tool and material size.
- [ ] Correct post processor is selected for milling, rotary, or laser.

### At the CNC, with gSender
- [ ] *Spindle:* VFD is plugged into power.
- [ ] Correct firmware upon connection (grbl or grblHAL).
- [ ] Workspace preset correctly selected (e.g., G54).
- [ ] *Sensors:* CNC is homed.
- [ ] Material is secured onto spoilboard.
- [ ] Collet and collet nut are cleaned.
- [ ] Correct cutting tool is installed.
- [ ] *Touch plate:* Correct touchplate is selected in Config, and magnet is attached.
- [ ] Zeros are set and match the X0Y0Z0 from CAM.
- [ ] G-code project file is loaded.
- [ ] Project is correctly positioned and does not interfere with workholding.
- [ ] CNC can reach material depth within travel limits with the cutting tool installed.
- [ ] When jogging, “Go X”, “Go Y”, and “Go Z” move the CNC to the expected X0, Y0, Z0 locations.
- [ ] Dust collection is attached and clear of the CNC’s path.
- [ ] Spoilboard is clear of loose items.
- [ ] Safety glasses and hearing protection equipped.
- [ ] Router/spindle is jogged a little above the material.
- [ ] *Router:* Speed dial adjusted; router turned on.
- [ ] Dust collection is turned on.
- [ ] **Start Job!**

Now that you've put together your MK2.5 let's get something cut out on it! Are you Team Fun or Team Functional?? You can see each project states the type and size of material it supports as well as the type of cutting tool you’ll need to cut it out so choose wisely. Once you choose your project and download the file, scroll further down the page to learn about how you’ll set your machine up and carve your first project.

## Fun Projects

[su_table responsive="yes"]

| Image                                                                                                   | Description                                                                                                           |
|---------------------------------------------------------------------------------------------------------|-----------------------------------------------------------------------------------------------------------------------|
| ![](/_images/_lmmk2/_assembly/_firstproject/lmk2_firstproject_LongMill-line-CAMotics_43.png){.aligncenter .size-medium} | **LongMill Lettering** [**Download g-code**](https://resources.sienci.com/wp-content/uploads/2022/04/LongMill-Lettering.nc) <br> Slowly spells out “LongMill” - a great way to christen your new CNC. <br> • any material (302 x 35 x 2mm) <br> • any cutting tool <br> • zero at the front left corner <br> • 3.5 router speed |
| ![](/_images/_lmmk2/_assembly/_firstproject/lmk2_firstproject_Kellys-Peonies-scaled.jpg){.aligncenter .size-medium} | **Kelly's Peonies** [**Download g-code**](https://resources.sienci.com/wp-content/uploads/2022/04/Peony-Engraving.nc) <br> Made by a Sienci team member when she was inspired to make a custom flowery carving. <br> • any material (220 x 200 x 2mm) <br> • v-bit or small ball or flat bit <br> • zero at the front left corner <br> • 3.5 router speed |
| ![](/_images/_lmmk2/_assembly/_firstproject/lmk2_firstproject_Foam-CNSheep.jpg){.aligncenter .size-medium} | **The Classic CNSheep** [**Download g-code**](https://resources.sienci.com/wp-content/uploads/2022/04/Classic-CNSheep.nc) <br> A fun "2.5D" carving of the classic CNSheep. This bleating companion will keep you company for years to come. <br> • foam or soft wood (100 x 70 x 8mm) <br> • 1/8" flat end mill <br> • zero at the center <br> • 3 router speed |

[/su_table]

## Functional Projects

[su_table responsive="yes"]

| Image                                                                                       | Description                                                                                                           |
|---------------------------------------------------------------------------------------------|-----------------------------------------------------------------------------------------------------------------------|
| ![](/_images/_lmmk2/_assembly/_firstproject/lmk2_firstproject_drink-Coaster-1.jpg)         | **Drink Coaster** [**Download g-code**](https://resources.sienci.com/wp-content/uploads/2022/04/Sienci-Coaster.nc) <br> Rest your beverage while admiring the rotational symmetry of the Sienci Labs logo. <br> • any 1/4" thick material (100 x 100 x 6.25mm) <br> • 1/8" flat end mill <br> • zero at the center <br> • 3.5 router speed |
| ![](/_images/_lmmk2/_assembly/_firstproject/lmk2_firstproject_SoapDish-scaled.jpg)         | **Soap Dish** [**Download g-code**](https://resources.sienci.com/wp-content/uploads/2022/04/Soap-Dish.nc) <br> A perfect place to put a bar of soap. Requires some form of finishing/sealing before use. <br> • 1/2" thick hardwood, softwood, or bamboo (100 x 80 x 12.7mm) <br> • 1/4" flat end mill <br> • zero at the front left corner <br> • 4 router speed |
| ![](/_images/_lmmk2/_assembly/_firstproject/lmk2_firstproject_BitHolder-scaled.jpg)        | **Bit Holder** [**Download g-code**](https://resources.sienci.com/wp-content/uploads/2022/04/Bit-Holder.nc) <br> Accessorize your MK2 early with a simple bit holder for 1/8" and 1/4" bits. <br> • 3/4" thick soft wood or MDF (130 x 50 x 19mm) <br> • 1/8" flat end mill <br> • zero at the front left corner <br> • 3 router speed |

[/su_table]

## Setting Up

Let’s start from Ground Zero. If you’ve done previous reading or watched videos about CNC you’ve likely heard about the stages of starting with a design, turning that design into a cutting program (a.k.a. g-code), and then running that program on your machine. This design, CAM, then send process is all that you need to keep in mind anytime you want to create something new; and luckily for this first project the design and CAM parts are already taken care of!

With the g-code ready for use, there are only a few steps remaining to cut your first project:

1. Have a piece of material in-hand that matches the project you selected
1. Secure that material within your LongMill cutting area
1. Have a cutting tool (a.k.a. “bit”) in-hand that matches your project
1. Secure that bit into the router
1. Begin at the correct starting point for the selected project
1. Turn on the router at the correct speed and then “Start Job”!

### Project Material

Check the project you selected to see what type of material is suggested and the minimum size needed to cut the project out. Hard insulation foam and soft woods are ideal for starting out since they cut so easily. Once you find a piece of material that fits these requirements you’ve now obtained your ‘stock material’. This term is commonly used in the world of CNC and refers to any material that will act as the raw, blank canvas that you plan to carve into.

![](/_images/_lmmk2/_assembly/_firstproject/lmk2_firstproject_Finding-stock-material-scaled.jpg){.aligncenter .size-medium}

### Securing it in Place

You can put your material anywhere you want inside the cutting area of your LongMill - if the machine can reach it, it can cut it. Some beginner tips when placing your material are:

1. Place it closer to the front so you can access it more easily when you attach it at the start of a job or remove it at the end
1. Don’t attach your material too crooked or wonky, if you can get it square and aligned to the machine then the cut will line up better
1. If you attach your material using hardware like screws or nails, try to select material with some extra space around it or keep the hardware all the way at the edges to avoid running into them when cutting

![](/_images/_lmmk2/_assembly/_firstproject/lmk2_firstproject_Workholding-alignment_ann.png){.aligncenter .size-medium}

If your machine is in the way, use the machine movement skills you gained on the previous page to jog away from the area you want to mount your stock. When mounting, don’t worry about getting fancy for your first project. Feel free to try something quick and easy using whatever you have on-hand so you can get to the fun part faster, cutting! Here’s some inspiration:

- Wood screws
- Hot glue
- Carpet tape
- Nails hammered in at an angle

Some projects cut slow and others cut faster so whatever you choose, just ensure you can get the material mounted securely. Give it a wiggle with your hands once mounted and it should feel properly stuck-on.

### Cutting Tools

Scroll back up to the project you selected and this time check that you’ve got the right tool in-hand for the job. If you got a ‘Starter Pack’ with your machine then grab something from there or look around your shop or a local hardware store if you don’t have tools yet for your machine. Cutting tools come in all shapes and sizes. Machines like the LongMill tend to use purpose-made CNC cutting tools but can also use some of the more traditional and commonly available router bits.

![](/_images/_lmmk2/_assembly/_firstproject/lmk2_firstproject_End-mill-tip-types_marked_trim-1-scaled.jpg "Ballnose vs. End mill vs. V-bit"){.aligncenter .size-medium}

The shape of the tool is usually the most important feature and will either be flat, rounded (a.k.a. ball ended or ball nosed), or v-shaped. The size of the cutting side of the tool is sometimes also important because if you need to carve small details you won’t be able to use a large cutting bit. If your selected project specifies a particular bit size then check the label on the packaging your bit came in to confirm it’ll be able to do the job.

### Installing the Tool

Remember to be safe and mindful when a cutting tool is in or near your hands. Bits can be deceptively sharp and v-shaped ones can also be very pointy.

Bring the machine to the front so you have easy access to the router and collect the two wrenches that are included in the Makita box. If this is your first time using a router, look at the bottom where it has a large hex nut and notice just above this the two flats cut into the router shaft. You’ll be using the two wrenches here, one on the nut and one on the flats of the shaft, so the router can ‘clamp’ onto bits before cutting and then release them when you’re finished.

![](/_images/_lmmk2/_assembly/_firstproject/lmk2_firstproject_Router-nut-close-up_crop.png){.aligncenter .size-medium}

Disassembled you can see the router shaft, standard ¼” Makita collet, and the collet nut. By default the Makita can only hold onto cutting tools with a ¼” shank so also shown are an ⅛” collet and a ¼” to ⅛” adapter which you can use for ⅛” bits. The ⅛” collet is a direct substitute that can swap out the standard collet meanwhile the adapter sticks into the standard collet to adapt it to ⅛” bits. We sell these separately and in bit kits so you may already have one, otherwise they’re readily available online and in stores. Note the orientation of the parts is exactly how they go back together.

![](/_images/_lmmk2/_assembly/_firstproject/lmk2_firstproject_Exploded-router-nut.jpg){.aligncenter .size-medium}

Loosen the collet nut with the small wrench on the left side and the large wrench on the right. Squeeze them together until the nut comes loose.

![](/_images/_lmmk2/_assembly/_firstproject/lmk2_firstproject_Loosen-nut_ann-1.png){.aligncenter .size-medium}

If you’re using an ⅛” bit, here is where you’ll either remove the nut entirely to swap out for the ⅛” collet, or you’ll slide the ¼” to ⅛” adapter over your ⅛” bit. Insert your ¼” bit or adapted ⅛” bit into the end of the router. Reference the earlier picture with the disassembled collet, collet nut, and adapter to ensure you orient the parts correctly. Push it as far up into the router as you can, if it bottoms out then pull the bit back out a couple millimeters. The more tool shaft that’s inside the router the better the router can hold onto the tool.

![](/_images/_lmmk2/_assembly/_firstproject/lmk2_firstproject_Installing-bit_crop.png){.aligncenter .size-medium}

Once positioned, use the red button on the Makita to lock the shaft while you hand-tighten the collet nut to initially hold the bit in place. If the bit is falling out safely use a block or your finger to hold it in place.

![](/_images/_lmmk2/_assembly/_firstproject/lmk2_firstproject_Fingertighten-nut_annL.jpg){.aligncenter .size-medium}

After finger tightening, use the wrenches to finish securing the bit. With the small wrench on the right and the large wrench on the left use pressure but don’t squeeze too hard, it shouldn’t take much before the bit feels firmly held in place.

![](/_images/_lmmk2/_assembly/_firstproject/lmk2_firstproject_Tighten-nut_ann-1.png){.aligncenter .size-medium}

### Get Located

With the material in place and the bit installed the last step is to tell the machine where to start cutting. Each project will say what its starting point is so you can check this above. Jog your MK2 so that the location of your cutting tool matches the location for your selected project. For the Z-axis, jog most of the way down to the material then rotate the Z-axis coupler by hand to move the bit the rest of the way until it barely touches the surface.

The image below shows how you’d position for the ‘LongMill Lettering’ project as an example. This project starts at the front left corner but is moved inward in the picture to avoid cutting the mounting screws when the project gets run. A piece of paper is also used to see when the bit is about to touch the top of the stock material.

![](/_images/_lmmk2/_assembly/_firstproject/lmk2_firstproject_Manual-zero-z-1.jpg){.aligncenter .size-medium}

With the bit in position, click the ‘Zero All’ button and you’ll see to the left all the blue X, Y, and Z locations reset to zero.

![](/_images/_lmmk2/_assembly/_firstproject/lmk2_firstproject_LongMill-Lettering-Zero.png){.aligncenter .size-medium}

### Start cutting!

If you haven't already, download your project's g-code file by clicking on the project name in the project table above. We'll be opening this file up to run it so click the 'Load File' button in the bottom left of gSender (pictured) and then select your downloaded project file to open it up. The common places to check on your computer will be the 'documents' or 'downloads' folders.

Once selected, you should see your project appear in the visualizer and the location of the virtual bit should match to what you have set up on on your CNC. If everything looks good, double-check that you've set your Makita router speed dial to match what's needed for your project, turn the router on, then click 'Start Job'! Remember you can reach for the E-stop if you think something's going wrong.

![](/_images/_lmmk2/_assembly/_firstproject/lmk2_firstproject_LongMill-Lettering-Start-job.png){.aligncenter .size-medium}

## Job Well Done

How'd it turn out?? Turn off the router, move the machine out of the way, and detach your material from the cutting area to inspect the result! A new thing was just made right in front of your eyes - it’s magical but also totally real at the same time. You’ve now got the power of CNC at your fingertips.

Now that you’ve got your machine running successfully, you've reached the end of assembly! We’ve got a lot more information for you to check out that we hope will continue pushing your CNC journey forwards. This first project doesn’t even mention other aspects like designing your own projects, probing, carving multi-tool jobs, other forms of workholding, feed overrides, and much more! For now be happy / celebrate your first successful project and feel free to be a bit of a show off to your friends and family.

If you bought the touch plate, dust shoe, t-track, or any other add-ons alongside your machine, you’ll find the information to assemble and use those next so you can finish levelling up your MK2: <a href="https://resources.sienci.com/view/lmk2-add-ons" target="_blank" rel="noopener noreferrer">https://resources.sienci.com/view/lmk2-add-ons</a>

![](/_images/_lmmk2/_assembly/_firstproject/lmk2_firstproject_next-steps_ann.png){.aligncenter .size-medium}

The **Handbook** section that follows the add-on assembly will be the spot you’ll want to check out next. This contains all the information you'd want to refer to for all your day-to-day CNC operation including:

- Machine maintenance
- Wasteboard surfacing
- Guidance on running jobs from start to finish
- Project sources and inspiration
- CNC terms glossary
- CNC troubleshooting (in case you hit any issues during your assembly)
- and more! <a href="https://resources.sienci.com/view/lmk2-handbook" target="_blank" rel="noopener noreferrer">https://resources.sienci.com/view/lmk2-handbook</a>

## Our YouTube channel

We also have a <b><a href="https://www.YouTube.com/channel/UCS4SdQ0sqFhvjitLjh4EsGQ?" target="_blank" rel="noopener noreferrer">YouTube channel</a></b> where you can find videos and tutorials on using your LongMill like:

- How to go from idea to completed project
- V-carving signs
- Carving 3D hills and terrain
- Live Webinars and Q&A sessions
- and more!

## Additional Project Videos

Each of these project videos come with step-by-step instructions on making your own!

https://www.youtube.com/watch?v=Dfwy2fDhUZ8

https://www.youtube.com/watch?v=cwDvnuouFlw

https://www.youtube.com/watch?v=b4HOfNXsrb0

https://youtu.be/uzgvDvpbq4s

https://www.youtube.com/watch?v=T3CF0i_SUlo

https://youtu.be/GRZNaJl7-Ww

We really hope you enjoy using your LongMill MK2 Benchtop CNC in the days, weeks, and months to come. Remember that CNC routers are an amazing tool that you can use for whatever you like, and the point of the LongMill and it's community is to offer you resources and support so that you can be confident in using your CNC to make what you imagine. Good luck and happy making!

-The Sienci Labs team