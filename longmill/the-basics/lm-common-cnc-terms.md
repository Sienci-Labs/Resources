---
title: Common CNC Terms
menu_order: 4
post_status: publish
post_excerpt: How to cut multiple toolpaths for CAM programs without tool changing functionality. This method is suitable for the LongMill Benchtop CNC, and other hobby CNCs.
post_date: 2021-04-19 16:45:00
taxonomy:
    knowledgebase_cat: lm-the-basics
    knowledgebase_tag:
        - mk1
custom_fields:
    KBName: LongMill CNC
    basepress_post_icon: bp-caret-right
skip_file: no
featured_image: _images/_longmill/_the-basics/lm_cncterms_p1_Backlash.jpg
---

### Basics of a CNC Router

Know the names for the fundamental parts that make up an average hobby CNC.

<b>Axis</b> - The number of unique directions of movement that the CNC is capable of moving in. Most traditional CNC routers are 3-axis, where those three axes are in the left-right (x-axis), forward-back (y-axis), and up-down (z-axis) directions.

<b>Backlash</b> - When there’s looseness in the drive system of the CNC. This means that it won’t be able to make motions as rigidly as expected, it also has an effect on the accuracy of it’s movements.   On the LongMill, if the anti-backlash nut threads wear out, it needs to be ‘re-tensioned’ by pushing the two thread profiles back away from each other using the M5 bolts. Tensioning too much can cause excess friction and wear, but done correctly it can keep your machine running reliably.

![](/_images/_longmill/_the-basics/lm_cncterms_p1_Backlash.jpg){.aligncenter .size-medium}

<b>CNC</b> - Put simply, a machine that is designed to be precisely controlled by a computer.

<b>CNC router</b> - A CNC cutting machine, typically used for woods and plastics. Uses a drive system to move around a cutting tool held within a router or spindle.

<b>Collet</b> - A flexible steel sleeve that fits within routers and spindles. These grab onto whatever cutting tool you’re using in your CNC so that you can change between tools easily. They normally come in ¼” and ⅛” sizes to fit the most common sized cutting tools.

<b>Cutting tool / End mill / Bit</b> - This is what causes the cutting on a CNC router. There are many types that you’ll find, each suitable for a different application (see: The Cutting Process).

<b>Drive system</b> - The components of a machine that provide motion and power, enabling the router to cut through material. Some components of a typical CNC include motors, bearings, couplers, belts, pulleys, lead screws, and ball screws.

<b>Dust shoe</b> - An attachment to a CNC machine, used to funnel sawdust and other material particulates from the workpiece to the dust collection system.

<b>Limit switch / Endstop / Homing switch</b> - Switches or sensors that are usually paired to each movement axis of the CNC. This is used to tell the machine how far it can move in either direction.  Limit switches can be used for homing, as soft limits, or as hard limits.

![](/_images/_longmill/_the-basics/lm_cncterms_p2_LimitS.jpg){.aligncenter .size-full}

<b>Router</b> - A consumer-level power tool used for woodworking. Routers can be controlled by hand, or placed into a CNC router. Due to its application, routers are usually less powerful than spindles and produce a bit more noise, but are more cost effective for many hobby-level CNC routers.

<b>Stock / Stock material</b> - The material you’re going to be making your project out of. This is a cookie, slab, or sheet, that has enough material produce the finished product.

<b>Spindle</b> - An industrial level power tool, typically used in high volume and precision CNC machining. Spindles are designed to run constantly. They can be controlled with a VFD (variable frequency drive), so its speed can be changed through the machine interface program.

<b>Wasteboard</b> - Its job is to get cut up. This is normally a flat sheet of MDF the same size or slightly bigger than the cutting area of your CNC. It can have built-in mounting systems to hold down your stock material, or you can just screw right into it. It’s always there as your flat ‘table’ that holds the stock material and gives you second chances if your CNC does something unpredictable.

### CNC Operation

These operations are all normally controlled using a machine interface program. You can think of the machine interface as a car dashboard, containing all the buttons and actions you’d need to run your machine.

<b>Homing</b> - If you have limit switches, this is normally run when you first connect to your machine, so it knows where its limits are. This can be handy during a power outage or for advanced jigging since your machine is able to remember where it ran a job.

<b>Job / Cutting job</b> - The process of cutting out a design by running a g-code file on the CNC. This file can sometimes be composed of multiple toolpaths.

![](/_images/_longmill/_the-basics/lm_cncterms_p3_Job.png){.aligncenter .size-full}

<b>Jog</b> - The act of moving the machine using manual buttons and controls (not g-code file).

<b>Origin / Zero</b> - The starting point if you decide to run a cutting job. You set your origin by assigning each axis location (X, Y, and Z) equal to zero. This doesn’t mean it’s going to start cutting exactly there, it just helps the machine understand where your stock material is located on the wasteboard. This origin should correspond to the origin of your g-code file, which is defined on the CAM program. It anchors your digital design to the actual cutting job on your machine.

<b>Probe</b> - Usually using a touch plate to set the zero or origin on your material so you can run the job at the correct location. This can also become more complex by setting certain axes individually, using other conductive materials for location, or using a special sensor to compile heightmaps, angles, and more.

![](/_images/_longmill/_the-basics/lm_cncterms_p4_TouchPlate.png){.aligncenter .size-full}

<b>Surfacing</b> - A job specifically used to flatten a piece of material. This can be a wood slab or the wasteboard itself, done during machine setup or maintenance to keep it level to the CNC’s mechanics. Typically you use a surfacing bit which has a larger cutting diameter.

![](/_images/_longmill/_the-basics/lm_cncterms_p5_Surfacing.png){.aligncenter .size-medium}

<b>Tool change</b> - A process used to switch between cutting bits either during a job or between jobs. This allows for much more elaborate projects to be made.

<b>Toolpath</b> - The series of steps that a cutting tool follows to cut into your material.

<b>Tramming</b> - A method used to adjust the router or spindle to cut exactly perpendicular to  the bed of the CNC machine. This is an optional practice done at the beginning of the machine setup or during maintenance to make straighter cuts and reduce grooves in flat surface cuts.

### The Cutting Process

Cutting away material on a CNC is affected by two major factors:

<ol>
  <li>The type of cutting tool / bit that’s being used and its shape and size; you can think about this like using different cutting blades in a band saw.</li>
  <li>What cutting approach is being used when moving through the material; an analogy would be cutting across the wood grain versus along it.</li>
</ol>

#### 1. Tools and Features

<b>End mill</b> - Bits with spiraled flutes, which can come in with many different tip shapes.

<b>Flute</b> - A groove on the cutting bit to allow for material to be ejected. Bits can have more than one flute, which increases the surface area of contact with the material.

<b>Round groove / Juice groove / Bowl cutting bit</b> - Has a semi-circle profile, which works well for carving rounded profiles.

<b>Surfacing bit</b> - Has a large cutting diameter, used to remove large areas of material at a shallow depth. This is used to flatten out material.

<b>Tip / Flute shape (upcut, downcut, compression, straight, corncob)</b> - The shape of the end mill you are using, which determines its application.

![](/_images/_longmill/_the-basics/lm_cncterms_p6_Tips.jpg "Ballnose mill vs. End mill vs. V-bit"){.aligncenter .size-medium}

<p style="padding-left: 40px;"><b>Flat end</b> mills have a square tip. They can also have spirals (upcut or downcut), or be completely straight. These are good for general purpose milling, such as cutting out borders or straight profiles.</p>

<p style="padding-left: 40px;"><b>Tapered</b> bits become more narrow at the tip, which allows for small details to be cut.</p>

<p style="padding-left: 40px;"><b>Ball nose</b> bits are rounded on the tip, similar to round groove bits. They are used for reliefs and 3D carvings.</p>

<p style="padding-left: 40px;"><b>Upcut</b> and <b>downcut</b> bits have opposite spiral directions, causing the material to be pushed either up or down respectively. Upcut bits are best for cutting materials that can melt onto the bit, such as plastics and aluminum, since these chips can be ejected out of the material. Downcut bits can be used for woods that can splinter easily, because they push the chips down which creates a cleaner finish.</p>

<p style="padding-left: 40px;"><b>Compression</b> bits are a combination of upcut and downcut bits, with spirals in both directions providing a clean finish and also ejecting chips from the cutting surface.</p>

<p style="padding-left: 40px;"><b>Straight</b> bits do not have any spirals, instead it has flat faces which run down the length of the bit. They are used for cutting plastics, woods and composite/laminate materials which are susceptible to fraying.</p>

<p style="padding-left: 40px;"><b>Corncob</b> bits have a unique diamond pattern which allows for abrasive materials to be cut, suitable for composite materials such as PCBs and carbon fiber.</p>

<p style="padding-left: 40px;"><b>V-bit</b> -  Has a pointed tip in the shape of a ‘V’ and works great for cutting away as an engraving, making lots of different details especially for signs. They can also be used for inlays and chamfering and come in many angles such as 30°, 60°, 90°, and 120°.</p>

#### 2. Cutting Approach

<b>Climb milling</b> - A milling technique in which the CNC machine is moving against the router / spindle rotation. This causes more cutting forces than conventional milling, but can provide a better surface finish. If climb milling, there must be compensation used to eliminate backlash.

<b>Conventional milling</b> - A milling technique in which the CNC machine is moving with the router / spindle rotation. This method eliminates backlash but can reduce tool life and surface finish due to chips and material rubbing onto the tool.

![](/_images/_longmill/_the-basics/lm_cncterms_p7_ClimbConv.png){.aligncenter .size-medium}

<b>Finishing pass</b> - A cutting job used to cut out the exact geometry of the design, to remove small amounts of material after a roughing pass had been done.

<b>Pass</b> - A layer of cutting, defined by a certain thickness (step down or depth of cut).

<b>Profile / Contour cut</b> - Where the cut follows a line or the outline of a shape.

<b>Pocket cut</b> - A type of toolpath where the machine will cut all the material that is within the shape. Pocket cuts will only work for shapes that are closed vectors.

<b>Ramping</b> - A method used to start or end a cut on a workpiece; instead of the machine descending vertically (plunging) into the material, it will move vertically and horizontally to gradually enter the material at a slope. Ramping typically follows the toolpath of the design. This can extend the life of the cutting bit.

<b>Relief cut</b> - A type of toolpath where the machine cuts raised geometries from one side of the stock material. For example, mountain terrains are considered relief cuts, because of the slopes and valleys.

![](/_images/_longmill/_the-basics/lm_cncterms_p8_Ram.jpg){.aligncenter .size-medium}

<b>Roughing pass</b> - A cutting job used to cut out the approximate geometry of the design, to remove larger amounts of material at once. This is usually followed by a finishing pass to clean it up.

### Basic CNC Parameters

These are the settings you’d change to improve the performance of your cutting job, found in most CAM programs.

<b>Cutting feed rate [mm/min, in/min]</b> - The speed of the machine in the XY directions, not the router or spindle rotation, also called feed rate.

<b>Plunge feed rate [mm/min, in/min]</b> - The speed of the machine in the Z direction, not the router/spindle rotation, also called plunge rate.

<b>Retract height [mm, in]</b> - A setting on CAM software which defines how high the machine will move when it is travelling to a different location, not cutting.

<b>Spindle speed [RPM]</b> - The rotational speed of the spindle or router, not how far the machine moves. Most compact routers operate at speeds between 10,000 and 30,000 RPM.

<b>Step down / LOC length of cut / DOC depth of cut / DPP depth per pass [mm, in]</b> - The thickness of the cutting in the Z-direction.

<b>Step over [%]</b> - The offset between two toolpaths, a smaller offset means there is more overlapping which leads to better surface finish but will take more time. The offset is expressed as a percentage of the bit diameter.

### Advanced CNC Parameters

<b>Chip load</b> - The theoretical thickness of the chip generated from the cutting bit, determined by the feed rate, spindle speed, and number of flutes. The chip load affects surface finish and tool wear, among other performance considerations.

<b>Feed per revolution [mm/rev, in/rev]</b> - A unit of measure to define the feed rate, by distance moved by the machine per revolution of the spindle or router.

<b>Lead-in / lead-out</b> - A method used to start or end a cut on a workpiece, by creating an entirely different toolpath to gradually enter or exit the material at a slope. This can improve the surface quality of the cut.

<b>Lead-in / lead-out feed rate [mm/min, in/min]</b> - The speed in which the machine cuts at when entering or leaving the material at a slope, specifically for lead-ins and lead-outs.  This is typically a smaller value than the regular XY feed rate.

<b>Ramp feed rate [mm/min, in/min]</b> - The speed in which the machine cuts at an angle, specifically for ramping. This is typically a smaller value than the regular XY feed rate.

<b>Surface speed [mm/min, in/min]</b> - The relative speed between the spindle speed and the machine feed rate. This is the actual speed your machine is removing material, expressed as distance over time. In a CAM program, you only input the spindle speed and feed rate, not surface speed.

### CNC Software Terms

<b>CAD</b> - Computer aided design, a software program used to produce a 2D or 3D design.

<b>CAM</b> - Computer aided manufacturing, a software program that converts designs into toolpaths to generate a g-code file. The program requires inputs from the user, such as feed rates, bit size and geometry, and post processor.

<b>g-code</b> - The text used by CNC machines to interpret and communicate commands. Many machines use g-code, not just CNC machines but laser cutters and 3D printers. There are many different languages within g-code, for various applications made by different manufacturers and researchers.

<b>grbl</b> - A CNC g-code language used by many hobby level CNC machines, such as Shapeoko, XCarve, Onefinity and the LongMill. grbl is compatible with Arduino,  therefore many CNC machines use the Arduino as the “brains.”

<b>Machine Interface</b> - a software program that controls the CNC machine by sending g-code to the machine. Features such as running and visualizing g-code files, jogging and zeroing are commonly found in machine interface programs.

<b>Post Processor</b> - A “translator” which ensures your g-code is set to the correct language such as grbl. This is found in the CAM software and can be changed for each g-code file.

![](/_images/_longmill/_the-basics/lm_cncterms_p9_PostPro.png){.aligncenter .size-full}

<b>Tiling</b> - A technique for cutting projects that are larger than the cutting area of the CNC. This requires the use of a locating system so that after cutting a portion of the stock, you can slide it into a new position and continue cutting the next portions of the project while keeping them aligned to each other.

<b>Vector</b> - used in 2D design. A vector is a line or shape that doesn’t lose its resolution, therefore you can scale it larger or smaller without affecting the quality.  Compared to images made with pixels, where if you scale a pixelated image up or down it will look grainy.

<p style="padding-left: 40px;"><b>Closed</b> vector - A vector that connects to itself, such as a circle or rectangle shape.</p>

<p style="padding-left: 40px;"><b>Open</b> vector - A vector that is not connected to itself, such as a straight line or squiggle.</p>

<b>Visualizer</b> - A program that shows the toolpaths of g-code files, illustrating how the machine will move during the job.

### CNC Electronics Terms

<b>Arduino</b> - A circuit board used for controlling electronics. It is an open source board, meaning people can freely modify and replicate its code and design. In the LongMill the Arduino is loaded with custom LongMill firmware.

![](/_images/_longmill/_the-basics/lm_cncterms_p10_Arduino.jpg){.aligncenter .size-full}

<b>DIP switch</b> - A component on CNC control boards which sets the microstepping of the motor.

<b>Driver</b> - The small electronic boards that control the motors, containing the potentiometers and DIP switches. These boards are connected to the main control board electrically.

<b>Electromagnetic interference (EMI)</b> - Electrical noise or disturbance that can interrupt jobs or cause inconsistent, random behaviour on the CNC, such as stopping mid-way, changes in movement direction, and inaccurate cutting. It can come from the machine itself (router or spindle, motors) or the setup and environment (dust collection, electrical tools, magnets, power bar).

<b>Firmware</b> - The  programming installed into electronics to enable basic functions, such as how to handle communications, hold external files, and store settings. Similar to an operating system of a computer.

<b>IOT relay</b> - A device used to automatically control power to AC powered electronics through g-code commands. Useful for controlling a router, vacuum, and lighting.

<b>Microstepping</b> - A way to control the accuracy of motor rotations, through breaking up motor motion into ‘steps,’ then adjusting how many steps complete a full revolution.

<b>Potentiometer</b> - A component on CNC control boards which sets the current going into the motor.

[su_divider]

### Sources &amp; Other Info

<a href="https://www.cnccookbook.com/cnc-dictionary/">https://www.cnccookbook.com/cnc-dictionary/</a><br>
<a href="https://wiki.shapeoko.com/index.php/glossary">https://wiki.shapeoko.com/index.php/glossary</a><br>
<a href="https://cimquest-inc.com/what-is-chip-load/">https://cimquest-inc.com/what-is-chip-load/</a><br>
<a href="https://www.cnccookbook.com/climb-milling-versus-conventional-milling/">https://www.cnccookbook.com/climb-milling-versus-conventional-milling/</a><br>
<a href="https://engmachineshop.wustl.edu/items/climb-milling-vs-conventional-milling/">https://engmachineshop.wustl.edu/items/climb-milling-vs-conventional-milling/</a><br>
<a href="https://www.harveyperformance.com/in-the-loupe/ramping-success/">https://www.harveyperformance.com/in-the-loupe/ramping-success/</a><br>
<a href="https://www.axyz.com/us/2018/11/16/technical-tip-of-the-week-when-to-use-lead-ins-and-ramps/">https://www.axyz.com/us/2018/11/16/technical-tip-of-the-week-when-to-use-lead-ins-and-ramps/</a><br>
<a href="http://www.helmancnc.com/g-code-g95-feed-per-revolution/">http://www.helmancnc.com/g-code-g95-feed-per-revolution/</a><br>
<a href="https://circlemwoodworking.com/cnc-router-motor-vs-spindle-which-is-better/">https://circlemwoodworking.com/cnc-router-motor-vs-spindle-which-is-better/</a><br>
<a href="https://www.axyz.com/us/2018/02/22/using-a-compression-bit/">https://www.axyz.com/us/2018/02/22/using-a-compression-bit/</a><br>
<a href="https://www.endmill.com.au/pcb-corn-cutter-carbide-router-bit/">https://www.endmill.com.au/pcb-corn-cutter-carbide-router-bit/</a>
