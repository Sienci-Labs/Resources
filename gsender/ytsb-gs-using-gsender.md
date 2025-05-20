---
title: ytsb Using gSender
menu_order: 3
post_status: draft
post_excerpt: Understand the basics of how to use gSender, including connecting, jogging, zeroing and gotos, probing, and running jobs.
post_date: 2021-07-01 14:56:00
taxonomy:
    knowledgebase_cat: gdocs
    knowledgebase_tag:
        - gsender
custom_fields:
    KBName: gSender
    basepress_post_icon: bp-caret-right
skip_file: no
featured_image: 
---

## Starting Up

When you double click the gSender icon to open up the program, it can take several extra seconds to load if you have Microsoft real time virus protection on your computer. This scan delay should only happen the first time you turn on your computer.

![](/_images/_gsender/_using/gs_us_notconnected.jpg){.aligncenter .size-medium}

Connect to your CNC machine by hovering over the **Connect to CNC** button at the top left corner of the screen.

***Note: You will need to select one of the COM ports if this is the 1st time connecting. Once you've connected for the first time, you can connect via Ethernet moving forward.***

gSender will automatically detect if you are using "grbl" or "grblHAL" and connect you to the correct version. Most hobby boards use "grbl" including our original LongBoard, but if you have the SLB or LongMill MK2.5, then you'll use "grblHAL".

Sometimes there’s more than one COM port available, so you may need to try both to see which one your machine is connected to. You will find them by clicking **Unrecognized Ports**.

![](/_images/_gsender/_using/gs_us_connectcnc.jpg){.aligncenter .size-full}

Once you have clicked on the COM port, your machine will be connected. This is confirmed when you see the plug icon turn green. You will also find either *grbl* or *grblHAL* listed under the COM port selected. You can also see the status on the top center of the app change from **Disconnected** to **Idle**, and the controls activate, allowing you to press them. Most buttons stay gray if they're still inactive.

![](/_images/_gsender/_using/gs_us_idleconnected.jpg){.aligncenter .size-full}

If you are not seeing those changes when you connect, please check the following:

1. Any other programs that can talk to the Arduino are closed (ex. Arduino IDE, Easel, UGS).
1. See if you have other COM ports available, and try to connect to them.
1. Arduino is securely attached to the LongBoard.

## Jogging and Presets

You can move the machine manually by using the **Jog Control**, through the arrow buttons. We cover moving the machine automatically in the [Gotos](#set-zero-and-gotos) section. To move the machine, use the large +-X and +-Y movements on the control dial, or use the smaller diagonal buttons. To move the Z axis up and down, use the Z+ or Z- buttons to the right of the control dial.

Below the control dial, you can change the **XY value** and **Z value** to adjust the distance you travel per click. You can also change **Speed**, which determines how fast the machine will move when jogging. That value is reflected in the 'at box'.

![](/_images/_gsender/_using/gs_us_jog.jpg){.aligncenter .size-full}

The *Rapid*, *Normal*, and *Precise* buttons are preset values that will allow you to toggle to different distance and speed values quickly. We use rapid to get around quickly on large jobs, and precise if we are trying to set zero with the paper method for example.

## Machine Coordinates vs Workpiece Coordinates

Above the Jog Controls is your DRO (Digital Read Out). This section allows you to do some automatic movement, set your zeros and see where you are in relation to the machine or the workpiece. Kinda like your car navigation system. You can also see if you are using mm or inches!

![](/_images/_gsender/_using/gs_us_dro.jpg){.aligncenter .size-medium}

Before we dive into the buttons in the DRO and what they do, let's review how coordinates are handled. In other words, before we drive the car, let's look at the map.

In CNC machining, there are two primary coordinate systems that guide the machine's movements:

- [**Machine Coordinate System**](#machine-coordinate-system-)
- [**Workpiece Coordinate System**](#workpiece-coordinate-system-)

The **machine coordinate system** is a fixed, default system established by the CNC machine’s manufacturer. It is defined by the machine’s physical size and is used during the homing cycle, when the machine references its internal limits using built-in sensors like limit switches. Users do not modify or choose this system—it simply tells the machine where it is in its own space. If you are not using homing switches, the machine home is determined by where the bit is when the controller is powered on.

 In contrast, the **workpiece coordinate system** is fully controlled by the CNC user. This system defines the position of the part on the machine table and ensures the tool moves accurately in relation to the workpiece.

![](/_images/_gsender/_using/gs_us_dro_offset.jpg){.aligncenter .size-medium}

### Machine Coordinate System 🏭

The machine coordinate system refers to the CNC machine's own coordinate system, established by the manufacturer. This system is based on the machine's physical structure and its home position (often referred to as the machine's home or (0,0,0) point indicated by the **grey numbers**).

![](/_images/_gsender/_using/gs_us_dro_machinecordfull.jpg){.aligncenter .size-medium}

When you power on the machine and perform a homing sequence, the machine references this built-in coordinate system to determine its position in space. This system ensures that the machine has a consistent reference point for all operations.​

### Workpiece Coordinate System 🧱

The workpiece offset is a user-defined coordinate system that aligns the machine's operations with the specific location of the workpiece on the machine bed. This system allows users to set a new origin point (0,0,0) based on the workpiece's position.​ This is indicated by the **blue numbers** in the DRO.

![](/_images/_gsender/_using/gs_us_dro_workpiececordfull.jpg){.aligncenter .size-medium}

In gSender, you can set workpiece offsets using standard G-code commands like G54 to G59. These commands allow you to define multiple work coordinate systems, which is especially useful when working on different parts or setups without re-homing the machine each time.​ These are called your workspaces.

## Set Zero and Gotos

Each g-code file or project will have a starting position that all other movements are referenced off of. This is called the **Workpiece zero** or **Workpiece Home**. There are two ways to manually set your zero on gSender, and a couple automatic options that we cover in [Probing](#probing).

The two ways to **set zero** manually are to either:

- Zero each axis one at a time using 'X0', 'Y0', and 'Z0' buttons

- Set them all at the same time with the Zero button

![](/_images/_gsender/_using/gs_us_dro_zeroall.jpg){.alignnone width="61" height="30"}

![](/_images/_gsender/_using/gs_us_setzero.jpg){.aligncenter .size-full}

The large blue numbers tell you the current position of your machine. Once you set the zero of each axis, they will all read 0.00.

![](/_images/_gsender/_using/gs_us_dro_allzeroes.jpg){.aligncenter .size-full}

Now that we've covered how to manually move, here are two ways to automatically move, or as we call it, **Goto**:

- Return to each axis Zero, one at a time using the blue 'X', 'Y', and 'Z' buttons

- Return to X and Y Zero at the same time with the blue 'XY' button

*Note - 'Goto XY' **will not** move the z-axis to its zero.*

![](/_images/_gsender/_using/gs_us_goto.jpg){.aligncenter .size-medium}

*Note: if you’ve set up “Safe Height” in gSender (Config -> Basics -> Safe Height), then the Z-axis will move up by that distance before moving the X or Y to make sure your machine doesn’t run into clamps or other materials.*

There is one more way to move automatically, but it isn't used to bring you back to 0.00. It's called **Goto Location**.

![](/_images/_gsender/_using/gs_us_dro_goto_airplane.jpg){.aligncenter .size-medium}

If you want to go somewhere else quickly without manually jogging there, click the 'Paper Airplane' button to bring you to a specific location. You'll see a popup asking you where you want to go and you either type a specific location (absolute G90) or move some amount from where you are now (relative G91).

![](/_images/_gsender/_using/gs_us_dro_gotolocation.jpg){.aligncenter .size-medium}

You can reset your zeros anytime when the machine is not actively running a job. The machine will remember your zero in most cases. If you turn the lead screw with your fingers or push the gantry, the machine does not know you moved it, therefore it will lose the zero position. You can jog on the Jog Control without losing your zero position because gSender knows you are moving the machine.

You can also enter coordinates directly by clicking the blue text location value. It’ll turn into a white box where you can type any number, then hit the ‘enter’ key to confirm it. For instance you could set your Z-axis to 0.1mm instead of 0 if you’re using the paper method and you want to account for the paper thickness.

![](/_images/_gsender/_using/gs_us_dro_zeroboxmanual.jpg){.aligncenter .size-medium}

## Homing & Limits

Limit switches (also referred to as *inductive sensors*, *end stops* or *homing switches*) are sensors that sit at one or both ends of each movement axis of a CNC to provide a few different functions. gSender provides unique features if you have these switches installed on your machine. You can check out our sensors [HERE!](https://sienci.com/product/inductive-sensor-kit-for-the-longmill-mk2/)

If you don't have sensors, skip ahead [HERE.](#probing)

### Going Homing

When we turn on homing, we can use 3 sensors to find our machine coordinate  home on our machine. For now, we will home to the front left corner of the machine. To enable Homing, go to Config -> Limits and Homing -> Homing cycle enable -> toggle on.

![](/_images/_gsender/_using/gs_us_dro_homingon.jpg){.aligncenter .size-medium}

Using **grblHAL** enables several more detailed options for you to choose from, like homing single axes, requiring homing on startup, set machine origin to 0, and more. In this image, we have enabled homing, but **not** required it on startup. We have toggled to allow us to manually home the machine, and to **Set the machine origin to 0** once complete.

![](/_images/_gsender/_using/gs_us_dro_hominghal.jpg){.aligncenter .size-medium}

You’ll notice additional buttons appear in the DRO area of gSender:

![](/_images/_gsender/_using/gs_us_dro_homingbtn.jpg){.aligncenter .size-medium}

The **Home** button is a convenient way to home or re-home your machine at any time (sends the typical $h command). The machine will automatically move to your front left corner, using the sensors to position the router over machine home.

![](/_images/_gsender/_using/gs_us_dro_rapidpositionbtn.jpg){.aligncenter .size-medium}

Four **Rapid-Travel** buttons to move your CNC at its maximum speed to any of your machine's 4 corners (offset by 5mm). These can only be used once your machine is homed.

![](/_images/_gsender/_using/gs_us_dro_parkbtn.jpg){.aligncenter .size-medium}

You can configure a **Park Location** to move your router to a set spot consistently at the click of a button. To setup your parking spot, go to Config -> Basics. Here you can enter the coordinates of your parking spot manually, or move your router/spindle to the spot and hit the **Grab** current position button. Test out your new spot by hitting the Go To button in settings or hitting the P button on the DRO.

![](/_images/_gsender/_using/gs_us_dro_parksetting.jpg){.aligncenter .size-medium}

### Set Those Limits

If you’re having issues with the “quick-travel” buttons, then check the “maximum travel” settings for your machine to see if they are the same as what your machine is physically capable of moving. You can find these settings by going to Config tab -> Limits and Homing -> X-axis maximum travel (Y, Z axes are here too), 130-132. If you are using **grblHAL** you will also see A axis, 133.

![](/_images/_gsender/_using/gs_us_limitssetl.jpg){.aligncenter .size-medium}

If you'd like more information on how to set up and use limit switches, read here: <a href="https://resources.sienci.com/view/lm-adding-limit-switches/" target="_blank" rel="noopener">https://resources.sienci.com/view/lm-adding-limit-switches/</a>

### Soft Limits

With 3 sensors in place, and homing turned on, we can turn on soft limits. This feature will combine your 3 sensor homing cycle with your maximum travel lengths, so prevent you from going too far on each axis. To enable soft limits, Config -> Limits and Homing -> Soft limits enable -> toggle on. Don't forget to hit the Apply Settings button to save!

![](/_images/_gsender/_using/gs_us_softlimit.jpg){.aligncenter .size-medium}

### Hard Limits

If you have a sensor on both sides of each axis, all 6 sensors can provide you a hardware backup solution, to the software solution provided above with the soft limits. With hard limits on, if your machine get's close to the edge of an axis, your sensor will trigger, stopping any further movement. To enable soft limits, Config -> Limits and Homing -> Hard limits enable -> toggle on. Don't forget to hit the Apply Settings button to save!

![](/_images/_gsender/_using/gs_us_hardlimit.jpg){.aligncenter .size-medium}

## Probing

Probing automatically sets a zero position, usually at the bottom left corner of the stock material, using a touch plate. If you're not using a Sienci touch plate, <a href="https://resources.sienci.com/view/gs-additional-features/#touch-plate-setup">read here to make sure your settings are set up correctly</a>.

You can select the type of touch plate you are using, if you want to verify the connection with a test at the start and more in the Config -> Probe section.

![](/_images/_gsender/_using/gs_us_probesettings.jpg){.aligncenter .size-medium}

Once you have set up the touch plate, banana plug and magnet on the machine, you can choose which axis to probe for, and the diameter of the bit you are using if applicable. The bit size can be selected from the drop-down of saved bits, or can be typed in manually. Jog the machine so that the bit is hovering over the Sienci Labs logo on the touch plate. Then press 'Probe'.

![](/_images/_gsender/_using/gs_us_probexyz.jpg){.aligncenter .size-medium}

Before the process begins, there is a conductivity test to ensure that the touch plate components can conduct electricity, which allows a signal to be sent to the LongBoard when there is contact. You can either bring the touch plate to the end mill or touch the banana plug and magnet together. Make contact a few times just to confirm there is conductivity, as the red circle should flicker to green.

![](/_images/_gsender/_using/gs_us_probenotouch.jpg){.aligncenter .size-medium}

A blue button called 'Start Probe' will appear if you have successfully confirmed conductivity. Ensure that the touch plate components are set up for probing, then press 'Start Probe'. The machine will move to probe three sides of the touch plate, twice on each side. There should not be any crashing or abrupt movement. Once the process is over, remove the touch plate components from the machine and then press 'Go to XY'. The bit should be overtop the bottom left corner of the stock material, and pressing 'Go to Z' should bring it to touch the surface. More information can be found on our touch-plate resource page. <a href="https://resources.sienci.com/view/lmk2-touch-plate/" target="_blank" rel="noopener">https://resources.sienci.com/view/lmk2-touch-plate/</a>

![](/_images/_gsender/_features/_probing/gs_fe_pr_success.jpg){.aligncenter .size-full}

If you have a different setup where probing the front, left corner is less convenient for you, gSender can also probe other corners by clicking the corner button. You'll see the blue arrow point to the corner you want to probe from, then you can follow the rest of the probing process the same way.

![](/_images/_gsender/_using/gs_us_probecorner.gif){.aligncenter .size-full}

## Loading Job Files

If you have already prepared a project file, ensure the following:

1. The file is an \*.nc, \*.g-code, \*.tap, \*.gc, or \*.cnc file.
1. The file is exported to the correct post processor for the LongMill. Please see this page for the correct post processor for your CAM software: <a href="https://resources.sienci.com/view/lm-post-processors/" target="_blank" rel="noopener">https://resources.sienci.com/view/lm-post-processors/</a>.

![](/_images/_gsender/_using/gs_us_filetype.jpg){.aligncenter .size-medium}

To run your project on gSender, press the 'Load File' button. A dialog box will pop up, where you can navigate to where your file is. Here you can also select from recently loaded files, reload a file or close a file.

![](/_images/_gsender/_using/gs_us_loadbar.jpg){.aligncenter .size-medium}

Once loaded, you’ll be able to toggle between **Info and Size** to reveal stats about your project such as: Estimated cut time, Feed rate, Spindle Speed, Cutting dimensions, Min/Max values and more.

![](/_images/_gsender/_using/gs_us_loadsizeinfo.jpg){.aligncenter .size-medium}

Loaded files are shown on the Visualizer. With your file loaded, feel free to also check how it looks. In the bottom left corner of the visualizer use the ‘view cube’ to quickly switch between top, right, left, front, and 3D views by clicking on its different faces. You can also use your mouse scroll wheel to zoom in and out and left-click and drag or right-click and drag on the visualizer to rotate or slide around the work area.

![](/_images/_gsender/_using/gs_us_visualizer.gif){.aligncenter .size-full}

Before running your job there's another handy feature you can check. The **Outline** button will physically move your machine around the rough perimeter of your cutting job so you can get an idea of the cutting dimensions and if you’ve positioned the job correctly.

![](/_images/_gsender/_using/gs_us_outline.jpg){.aligncenter .size-medium}

## Running Jobs

Once your machine is ready with your ***router and vacuum on***, press **Start** to begin your cut. You can pause and stop your job at any time with the respective buttons. If you press **Pause**, you can resume the job from where you left off. Otherwise, **Stop** will cancel your job completely.

![](/_images/_gsender/_using/gs_us_start.jpg){.aligncenter .size-medium}

Hitting the pause button will pause the movement immediately, even if gSender has plans to move in the buffer (memory). If you are using a macro or Program Events like program pause, this will pause movement more slowly, as the planned moves in the buffer will finish before actually pausing. This is something that can’t be avoided on the firmware side and this is a compromise to be able to execute code at all.

In the default visualizer you’ll see that cutting movements that plan to be made are coloured blue, then when the job is running the current movements show as yellow and past movements are grey.

![](/_images/_gsender/_using/gs_us_runningjob.gif){.aligncenter .size-full}

At the bottom of the visualizer, an animated progress bar shows you several details about the job you are running, like completion %, estimated time remaining, g-code line counter and a running timer for how long you have been cutting.

Additionally, you can **override the feed rate** and spindle speed of the program while the job is running by moving then letting go of the slider, pressing the ‘+’ and ‘-’ buttons for smaller adjustment, or clicking the rotated arrow to reset back to the default value. This is handy for fine-tuning the program cutting speed in order to tune in your material removal rate and ensure you don't burn or melt material. You can also do this before starting the job if you already know you’ll need to tweak the feed rate or spindle speed for your file you're about to run.

![](/_images/_gsender/_using/gs_us_runningfeedbar.gif){.aligncenter .size-full}

Now you're off and cutting, what a thrill! While your job is running keep an eye and ear out for anything you don't expect. You can always use the job control buttons during operation to change speeds, pause, resume, or stop cutting altogether.

## **Job Loss Recovery**

Also called “Start from Line”, this feature can recover a carve you were working on that:

1. You had to manually stop part-way through
1. Was disrupted by a power loss, USB disconnect, mechanical malfunction, or other failure so you need to resume from where it failed
1. Was really long, so you want to resume carving after [pausing it for the night](#pause-cutting-mid-job)
1. You only wanted to run part of the job anyway

It does this by looking through the whole g-code file up to where you want to resume running to see all the movements up to that point, what accessories were turned on, the power of a spindle or laser, and runs any automatic commands you've set up in gSender. This way you can be confident in returning to your projects, even when something has gone awry.

### Steps to Resume Cutting

1. Make sure to have the g-code file loaded that got interrupted (or that you want to start carving part-way through).
1. If you think your machine lost its location:
   - Re-home the machine (it should remember the zero location of the project if nothing else moved).
   - If you don't have limit switches, the project moved, or your original cutting bit broke, try to re-use whatever setup method you used to set your zero location originally. This could be with a touch plate, 3D probe, paper method - whatever possible to set the project back up the way it was before it failed.
1. Once everything looks set up correctly, you should be able to 'goto' the original zero position and see that the bit is lined up correctly to the material. The location should read all zeros for each axis.
1. Raise up the Z-axis a couple millimeters for safety.
1. Click the small icon at the top right of the green ‘Start Job’ button to open the window.
  ![](/_images/_gsender/_using/gs_us_startfrombutton.jpg){.aligncenter .size-medium}
1. Here you'll see:
  ![](/_images/_gsender/_using/gs_us_startfromline.jpg){.aligncenter .size-medium}

   - When you **Last stopped** your file, how many **Total lines** it has, and a **Recommended start line**.
   - **Resume job at line**: once you've decided where to resume from, you can type the line number in here.
   - **Safe height**: if your CNC has extra Z movement above the failed job, you can put a larger number here to make sure that it doesn't hit clamps while moving into position to resume cutting.

1. Once everything looks good, remember to turn on anything that isn't automated like a trim router or vacuum, then click 'Start from Line' to resume cutting.

**Example**: you were present when the job failed and hit 'Stop' immediately. Nothing moved but the bit broke so you swapped it out and used a touch plate to probe Z. It says the last recorded line was 731 but to be safe you'll subtract 20 and start at 711. The job starts back up a little before the failure and you're able to resume as expected. If instead you hadn't been paying attention for several minutes then you might subtract 50-100 lines instead just to be safe.

![](/_images/_gsender/_using/gs_us_portdisconnected.jpg "Example of USB port disconnect while running a job where you'll want to check your USB cable, write down the suggested line, then use the ‘Start from Line’ feature as normal."){.aligncenter .size-full}

### Pause Cutting Mid-Job

1. If a carve is dragging on and you need to leave the machine for the night, first you'll want to note down the approximate g-code line number it's at. In the example below you'd note down "803 lines".
  ![](/_images/_gsender/_using/gs_us_currentline.jpg){.aligncenter .size-medium}
1. Once noted down, 'Pause', then 'Stop' the job. This allows the machine to stop more slowly instead of emergency stop.
1. Quickly turn off anything that isn't automated like a router or dust collector and jog the Z-axis up so you don't burn or mar the material. You can also try to pause strategically when the bit is moving and not cutting to avoid damaging your material.
1. At this point it's best to return the cutting tool to the project zero point if possible using the blue 'XY' button then the blue 'Z' button for the Z-axis. This will **Goto** your original zero. This way if the zero point is lost when you resume cutting later, then you can just manually set your zero knowing you're still at the zero location.
1. If you're concerned your machine might drift over time for example if you're using a heavy spindle, then another option is to place a block of wood under your cutting tool and jog down to it using the paper method. Once the bit is touching, you can note down the location where you left the machine, then when you resume you can type that location back in (see the end of [Set Zero and Gotos](#set-zero-and-gotos)).

## Safety

gSender is set up to do many things by default to help keep you aware about things going on with your machine. Though we can’t guarantee it can handle everything, you can access many safety items in one place. This includes:

![](/_images/_gsender/_using/gs_us_safetybasics.jpg){.aligncenter .size-medium}

1. **G-code warnings**: reports back when it sees g-code lines that don’t look correct when the file is loaded or once it’s being sent to the machine. G-code has to follow specific ‘grammatical rules’ similar to other languages for the ‘sentences’ to be correct, so if the lines don’t look correct then your machine might run into problems understanding what it’s supposed to do.1. **Prompt when setting zero**: enable an optional popup that appears when you click to 'zero' just in case you mis-clicked it.
1. **Safe height movement**: this number is used when using the ‘goto’ buttons in gSender to manually move your machine around (it’s independent from a safe height you might set in your CAM software). For machines without homing, entering ‘5mm’ will make it move 5mm upwards from the current position, make the goto movement, then move 5mm back down. If your machine has homing, it’ll move to 5mm from the max Z-axis travel, make the goto movement, and then return back to where the bit started. This behaviour helps homing-capable machines to reach a more ideal safe height to avoid collisions during movements.
