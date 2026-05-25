---
title: Calibration Tools
menu_order: 3
post_status: publish
post_excerpt: Learn the about using XY squaring, movement tuning & surfacing.
post_date: 2026-05-13 15:44:00
taxonomy:
    knowledgebase_cat: gs-advanced
    knowledgebase_tag:
        - gsender
custom_fields:
    KBName: gSender
    basepress_post_icon: bp-caret-right
skip_file: no
featured_image: 
---

## Calibration Tools

The **Tool Tab** is always available near the bottom left of the screen. Here you'll find some tools that you can use to make finer adjustments to your machine for improved performance:

- XY Squaring
- Movement Tuning
- Surfacing

![](/_images/_gsender/_features/_tools/gs_fe_to_main.jpg){.aligncenter .size-full}

### XY Squaring

When setting up any CNC, like when mounting <a href="https://resources.sienci.com/view/lm-table-mounting/#mounting-your-LongMill">a LongMill to a table</a>, usually a squaring step is needed to ensure cuts don't come out skewed. This **Software Wizard** (step by step guide) is a great asset to help speed things up by turning a typically 'guess-and-check' process into some easy measurements and behind-the-curtain math in 3 main steps:

1. Mark 3 points on your machine to make a triangle (the larger the triangle, the better)
1. Measure & enter the distance between the triangle points
1. See the results and adjust accordingly

![](/_images/_gsender/_features/_tools/gs_fe_to_xysquaring.jpg){.aligncenter .size-medium}

You will need the following:

- Ruler or measuring tape
- Tapered bit or V-bit
- 3 tape pieces marked with an 'X'

1. Jog the machine to the front left corner, with the bit raised slightly over the surface of your wasteboard
1. **Mark** the point with tape marked with an X, and move the machine as directed (Default 300mm)
  ![](/_images/_gsender/_features/_tools/gs_fe_to_xysquaring1.jpg){.aligncenter .size-medium}
1. Continue to mark points and move the machine until all boxes are complete and your triangle is marked
  ![](/_images/_gsender/_features/_tools/gs_fe_to_xysquaring2.jpg){.aligncenter .size-medium}
1. Measure the distance between each X and enter the values into the 3 boxes. For instance you might measure 306mm, instead of the expected 300mm. Hit the Confirm button to move to the results page.
  ![](/_images/_gsender/_features/_tools/gs_fe_to_xysquaring3.jpg){.aligncenter .size-medium}
1. At the end you'll be told how square your machine is and whether you need to take action to adjust it further or if it's close enough that you can leave it. The squaring tool also keeps an eye out for if your steps/mm (axis travel resolution) are off and can adjust those too.
  ![](/_images/_gsender/_features/_tools/gs_fe_to_xysquaring4.jpg){.aligncenter .size-medium}

You can also try watching how this process works in this <a href="https://youtu.be/CCpb70ypulY" target="_blank" rel="noreferrer noopener">user-made video by SparksTech</a>!

### Movement Tuning

Another **Software Wizard** (step by step guide) found in the **Tool tab**. This one is designed to help fine tune how much your motors turn to improve the accuracy of your machine movements. This is done through modifying the EEPROM settings stored on your CNC. You can tune the X, Y and Z axes individually.

You will need:

- Marker or tape
- Measuring tape

1. Jog your machine to the middle of whichever axes you choose to tune, so that there is enough room to complete this procedure. For example, on the X-axis you would jog halfway on the X-axis rail
1. Select what axis to tune on the drop down menu
  ![](/_images/_gsender/_features/_tools/gs_fe_to_movementtuning.jpg){.aligncenter .size-medium}
1. **Mark down the starting location** as a reference point on the machine. For example the X-axis tuning references the edge of the XZ gantry on the X rail.
1. **Move** the axis a chosen distance (Default 100mm)
1. **Measure** the distance between the starting location and the finishing location
1. Enter the measured value into the **Set Distance Travelled** box
  ![](/_images/_gsender/_features/_tools/gs_fe_to_movementtuning2.jpg){.aligncenter .size-medium}
1. You can now change the EEPROM setting if recommended by the procedure by pressing **Update Steps-per-MM**. This will bring up a popup that explains the change about to be made, and allows you one last chance to cancel the update.
  ![](/_images/_gsender/_features/_tools/gs_fe_to_movementtuningfin.jpg){.aligncenter .size-medium}
1. Repeat the procedure for each axis you wish to tune

### Surfacing

Surfacing the wasteboard of your machine or any project or blank material, can easily be done right inside gSender from the **Tools tab**! This saves the hassle of drawing rectangles in your CAD/CAM program and moving files around until you get the settings right. It's also great for creating a perfectly flat surface of your starting materials, just like a jointer or surface planer would. You can also use the [Rotary Surfacing Tool](#rotary-surfacing-tool) if you are wanting round stock off a rotary axis.

https://youtu.be/hZ8ltb0w3Ao

If you plan to use this tool to surface your wasteboard or larger pieces of material, some extra advice we'd give is to remove any accessories that might get in the way of your machine travelling to its limits as well as have a good vacuum on hand because surfacing can get really messy.

![](/_images/_gsender/_features/_tools/gs_fe_to_surfacing.jpg){.aligncenter .size-full}

1. Start by entering the settings you'd like to use to generate your surfacing job on the left side:
   - **X & Y**: decides the cutting size (width and depth) you want to surface. If you're surfacing your wasteboard, use the manufacturer's spec on max machine travel or manually jog to the limits to cover the full cutting area, or if you're surfacing a piece of material then you can use a measuring tape.<br>- **AltMill**: 1265mm (49") x 635mm (25") or 1251 (49")<br>- **LongMill MK2**: 818mm (32.2”) or 1278 (50.3”) x 366mm (14.4”) or 866 (34.1”)<br>(if using limit switches, remove about 8mm/0.3” in X and 11mm/0.43” in Y)<br>- **LongMill MK1**: 320mm (12.6”) or 805 (31.7”) x 344mm (13.54”) or 844 (33.23”)<br>(if using limit switches, remove about 35mm/1.38” in X and 24mm/0.94” in Y)<br>(if using magnetic dust shoe, remove about 34mm/1.34” in X)<br>- **Mill One**: 235mm (9.25”) or 257 (10.1”) x 185mm (7.28”)
   - **Cut Depth & Max**: describes how deep you want to cut per pass and the total depth you want to cut down. For larger surfacing bits usually you should keep cut depth below 1mm, max depth should be increased to a couple millimeters if you think your material is very warped.
   - **Bit Diameter** (typically 6 - 25mm): make sure you have the right bit for the job like a surfacing tool or a large, flat end mill since this will give you a better surface finish.
   - **Spindle RPM** (default 17000): only applies if you have an automatic speed control, otherwise set this manually on your router.
   - **Feed rate** (default 2500mm/min): influenced by the RPM, step over, bit diameter, and cut depth. Luckily if you set it incorrectly you'll be able to override it during the job since surfacing can cause burning when cutting too slow or can have worse surface finish when cutting too fast.
   - **Stepover** (default 40%): sticking around 40% tends to be a good balance between speed (using a higher %) and better surface finish (using a lower %).
  ![](/_images/_gsender/_features/_tools/gs_fe_to_surfacing2.jpg){.aligncenter .size-medium}
1. Decide where you want to start surfacing from by clicking any of the corners or the center. In most cases the front, left of the machine is the most convenient, and is the default setting. You can also select a surfacing pattern of spiral or zig-zag. The spiral will only cut from the inside-out if the start position is the centre. If you toggle the flip cut direction, the spiral will cut conventional instead of climb, and the zig-zag pattern will cut vertically instead of horizontally.
  ![](/_images/_gsender/_features/_tools/gs_fe_to_surfacing3.jpg){.aligncenter .size-medium}
1. Press '**Generate G-code**' and check your surfacing tool path using the 'Visualizer Preview' tab. You can also see the raw g-code using the 'G-code Viewer' tab and can copy and save it to a g-code file if you'd like to use it again later.
  ![](/_images/_gsender/_features/_tools/gs_fe_to_surfacing4.jpg){.aligncenter .size-medium}
1. Press '**Load to Main Visualizer**' to bring the g-code into gSender's main screen. Make sure that you jog to the starting point and set your zero in the right place before starting the job. You can also press the '**Outline**' button as an easy way to check that you'll be surfacing where you expect and if you find the dimensions aren't correct you can always re-open the surfacing tool, tweak the size, and try again. Feel free to start the job whenever you're ready!
  ![](/_images/_gsender/_features/_tools/gs_fe_to_surfacing5.jpg){.aligncenter .size-medium}
