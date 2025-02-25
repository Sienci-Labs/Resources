---
title: Using gSender
menu_order: 3
post_status: publish
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
featured_image: _images/_gsender/_using/gs_us_p2_IdleConnect.jpg
---

Here's an older video that goes over much of how a g-code sender works in the context of gSender. See Kelly explain many of its uses and features:

https://www.youtube.com/watch?v=3XbJ0g7jp0I

## Starting Up

When you double click the gSender icon to open up the program, it can take several extra seconds to load if you have Microsoft real time virus protection on your computer. This scan delay should only happen the first time you turn on your computer.

Connect to your CNC machine by hovering over ‘Connect to Machine’ at the top left corner. You'll need to select the right firmware for your board, but just the first time you connect. Most hobby boards use "grbl" including our original LongBoard, but if you have the SLB or LongMill MK2.5, then you'll want to select "grblHAL". You'll see these options in the dropdown where the selected one has white text.

Sometimes there’s more than one COM port available, so you may need to try both to see which one your machine is connected to. If you are seeing errors pop up or your machine isn’t acting correctly, ensure that you have selected the correct connection type.

![](/_images/_gsender/_using/gs_us_connect.jpg){.aligncenter .size-full}

Once you have selected the COM port, your machine should be connected. This is confirmed when you see the plug icon turn green with a check mark. You should also see the status on the top right corner of the visualizer change to 'Idle', and the controls activate, allowing you to press them.

![](/_images/_gsender/_using/gs_us_connected-idle.jpg){.aligncenter .size-full}

If you are not seeing those changes when you connect, please check the following:

1. Arduino is securely attached to the LongBoard.
1. Any other programs that can talk to the Arduino are closed (ex. Arduino IDE, Easel, UGS).
1. See if you have other COM ports available, and try to connect to them.

## Jogging and Presets

You can move the machine by using the Jog Control, through the arrow buttons. Change the 'XY move' and 'Z move' to adjust the distance you travel per click. You can also change 'Speed', which determines how fast the machine will move when jogging.

![](/_images/_gsender/_using/gs_us_jogging.jpg){.aligncenter .size-full}

The 'Rapid', 'Normal', and 'Precise' buttons will allow you to toggle to different distance and speed values quickly. You can change these values by going to the settings and editing the 'Jogging Presets' in the 'General' section.

![](/_images/_gsender/_using/gs_us_jog-presets.jpg){.aligncenter .size-full}

## Set Zero and Gotos

Each g-code file or project will have a starting position that all other movements are referenced off of. This is the zero or origin. There are two ways to manually set your zero on gSender.

1. Set the zero for each axis one at a time using 'Zero X', 'Zero Y', and 'Zero Z' buttons
![](/_images/_gsender/_features/_zerogoto/gs_fe_ze_zero-individual.jpg){.aligncenter .size-full}
1. Set the zeros all at once using 'Zero All'
![](/_images/_gsender/_features/_zerogoto/gs_fe_ze_zero-all.jpg){.aligncenter .size-full}

The large blue numbers tell you the current position of your machine. If you want to return to your zero position, you can press the 'Go to' for each individual axis and the large blue numbers will read “0.00” once it's finished moving.

![](/_images/_gsender/_features/_zerogoto/gs_fe_ze_gotos.jpg){.aligncenter .size-medium}

You can also use the 'Go to XY0' to return to the starting position in X and Y in one movement. 'Go XY0' **will not** move the z-axis to its zero.

![](/_images/_gsender/_features/_zerogoto/gs_fe_ze_gotos_goxy0.jpg){.aligncenter .size-medium}

*Note: if you’ve set up “Safe Height” in gSender, then the Z-axis will move up by that distance before moving the X or Y to make sure your machine doesn’t run into clamps or other materials.*

![](/_images/_gsender/_features/_zerogoto/gs_fe_ze_gotos_goto.jpg){.aligncenter .size-medium}

If you want to go somewhere else quickly without manually jogging there, you can also use the 'Go To' button to bring you to a specific location. You'll see a popup asking you where you want to go and you either type a specific location (absolute) or move some amount from where you are now (relative).

![](/_images/_gsender/_features/_zerogoto/gs_fe_ze_goto-location-gif.gif){.aligncenter .size-medium}

You can reset your zeros anytime when the machine is not actively running a job. The machine will remember your zero in most cases. If you turn the lead screw with your fingers or push the gantry, the machine does not know you moved it, therefore it will lose the zero position. You can jog on the Jog Control without losing your zero position because gSender knows you are moving the machine.

You can also enter coordinates directly by clicking the location value. It’ll turn into a white box where you can type any number, then hit the ‘enter’ key to confirm it. For instance you could set your Z-axis to 0.1mm instead of 0 if you’re using the paper method and you want to account for the paper thickness. Another example is instead of jogging 10mm to the right and clicking ‘zero’ to begin cutting a duplicate job that’s shifted over, you can just type “-10” and start the job right away (since if ‘zero’ is 10mm to the right, then your current location would be 0 - 10 = -10mm).

![](/_images/_gsender/_features/_zerogoto/gs_fe_ze_dro-typing.jpg){.aligncenter .size-full}

## Endstop buttons

gSender provides unique features if you have endstops on your machine for homing or limits. Once homing is enabled ($22) you’ll notice additional buttons appear in the ‘Location’ area of gSender:

- The ‘Home’ button is a convenient way to home or re-home your machine at any time (sends the typical $h command).
- Four “quick-travel” buttons to move your CNC at its maximum speed to any of your machine's 4 corners (offset by 5mm). These can only be used once your machine is homed, you’ll also notice a house icon appear at the corner that your machine homes to.
- If you’ve set up a “Safe Height” in your gSender settings, now any “go to” or “quick-travel” button will move to the top of the Z-axis minus the safe height before moving anywhere to make sure your machine doesn’t run into clamps or other materials (before it would move up by the safe height amount).

![](/_images/_gsender/_features/_zerogoto/gs_fe_ze_quick-travel.jpg){.aligncenter .size-full}

If you’re having issues with the “quick-travel” buttons, then check the “maximum travel” settings for your machine to see if they are the same as what your machine is physically capable of moving. You can find these settings in the Firmware tool as $130-133.

If you'd like more information on how to set up and use limit switches, read here: <a href="https://resources.sienci.com/view/lm-adding-limit-switches/" target="_blank" rel="noopener">https://resources.sienci.com/view/lm-adding-limit-switches/</a>

## Probing

Probing automatically sets a zero position, usually at the bottom left corner of the stock material, using a touch plate. If you're not using a Sienci touch plate, <a href="https://resources.sienci.com/view/gs-additional-features/#touch-plate-setup">read here to make sure your settings are set up correctly</a>.

Usually you'd have to enter a tool diameter each time you probe, but gSender also gives the option to save tool sizes for re-use. You can see this in the 'Tools' section of the ‘Probe’ settings. Add different tools by entering the diameter in millimeters or inches, and then pressing 'Add Tool', and if you tend to use a specific-sized tool the most then make sure to have it at the top of the list to make it your Default.

![](/_images/_gsender/_features/_probing/gs_fe_pr_add-tool.jpg){.aligncenter .size-medium}

Once you have set up the touch plate, banana plug and magnet on the machine, you can choose which axis to probe for, and the diameter of the bit you are using if applicable. The bit size can be selected from the drop-down of saved bits, or can be typed in manually. Jog the machine so that the bit is hovering over the Sienci Labs logo on the touch plate. Then press 'Probe'.

![](/_images/_gsender/_features/_probing/gs_fe_pr_begin.jpg){.aligncenter .size-full}

Before the process begins, there is a conductivity test to ensure that the touch plate components can conduct electricity, which allows a signal to be sent to the LongBoard when there is contact. You can either bring the touch plate to the end mill or touch the banana plug and magnet together. Make contact a few times just to confirm there is conductivity, as the red circle should flicker to green.

![](/_images/_gsender/_features/_probing/gs_fe_pr_confirm.jpg){.aligncenter .size-full}

A blue button called 'Start Probe' will appear if you have successfully confirmed conductivity. Ensure that the touch plate components are set up for probing, then press 'Start Probe'. The machine will move to probe three sides of the touch plate, twice on each side. There should not be any crashing or abrupt movement. Once the process is over, remove the touch plate components from the machine and then press 'Go to XY0'. The bit should be overtop the bottom left corner of the stock material, and pressing 'Go to' next to the 'Zero Z' should bring it to touch the surface. More information can be found on our touch-plate resource page. <a href="https://resources.sienci.com/view/lmk2-touch-plate/" target="_blank" rel="noopener">https://resources.sienci.com/view/lmk2-touch-plate/</a>

![](/_images/_gsender/_features/_probing/gs_fe_pr_success.jpg){.aligncenter .size-full}

If you have a different setup where probing the front, left corner is less convenient for you, gSender can also probe other corners by clicking the corner button. You'll see the blue arrow point to the corner you want to probe from, then you can follow the rest of the probing process the same way.

![](/_images/_gsender/_features/_probing/gs_fe_pr_change-corner.gif){.aligncenter .size-full}

## Loading Job Files

If you have already prepared a project file, ensure the following:

1. The file is an \*.nc, \*.g-code, \*.tap, \*.gc, or \*.cnc file.
1. The file is exported to the correct post processor for the LongMill. Please see this page for the correct post processor for your CAM software: <a href="https://resources.sienci.com/view/lm-post-processors/" target="_blank" rel="noopener">https://resources.sienci.com/view/lm-post-processors/</a>.

To run your project on gSender, press the 'Load File' button. A dialog box should pop up, where you can navigate to where your file is. If you want to reload a previous file you can also click the ‘&gt;’ button which will allow you to select from recently opened files.

![](/_images/_gsender/_using/gs_us_load-g-code.jpg){.aligncenter .size-full}

Double click on the file, and the project should load in and be shown on the Visualizer. Once loaded, you’ll be able to see information about your project such as: its estimated cut time and cutting dimensions, and if the file is too big and slowing down your computer you can always click the ‘X’ on the ‘Load File’ button to unload it.

![](/_images/_gsender/_using/gs_us_file-stats.jpg){.aligncenter .size-full}

With your file loaded, feel free to also check how it looks. In the bottom right corner of the visualizer use the ‘view cube’ to quickly switch between top, right, left, front, and 3D views by clicking on its different faces. You can also use your mouse scroll wheel to zoom in and out and left-click and drag or right-click and drag on the visualizer to rotate or slide around the work area.

![](/_images/_gsender/_using/gs_us_visualize.gif){.aligncenter .size-full}

Before running your job there are a few other handy features you can check. The ‘**Outline**’ button will physically move your machine around the rough perimeter of your cutting job so you can get an idea of the cutting dimensions and if you’ve positioned the job correctly. As well, the '**Verify Job**' (previously 'Test Run') button will go through your file and let you know of any obvious errors it noticed before you run the job for real. **This button won't move your CNC at all** but if you're looking to actually "dry run" your file, you can always set your Z-zero high above your material and run the job without cutting anything to see how it looks.

![](/_images/_gsender/_using/gs_us_outline-test-run.jpg){.aligncenter .size-full}

## Running Jobs

Once your machine is ready with your router and vacuum on, press 'Start Job' to begin your cut. You can pause and stop your job at any time with the respective buttons. If you press 'Pause Job', you can resume the job from where you left off. Otherwise, 'Stop Job' will cancel your job completely.

Hitting the pause button will pause the movement immediately, even if gSender has plans to move in the buffer (memory). If you are using a macro or Program Events like program pause, this will pause movement more slowly, as the planned moves in the buffer will finish before actually pausing. This is something that can’t be avoided on the firmware side and this is a compromise to be able to execute code at all.

In the default visualizer you’ll see that cutting movements that plan to be made are coloured blue, then when the job is running the current movements show as yellow and past movements are grey.

![](/_images/_gsender/_using/gs_us_running.gif){.aligncenter .size-full}

At the bottom of the screen, a progress bar shows how many lines of g-code have been processed and how many are left. Additionally, you can override the feed rate and spindle speed of the program while the job is running by moving then letting go of the slider, pressing the ‘+’ and ‘-’ buttons for smaller adjustment, or clicking the rotated arrow to reset back to the default value. This is handy for fine-tuning the program cutting speed in order to tune in your material removal rate and ensure you don't burn or melt material.

If you already know you’ll need to tweak the feed rate or spindle speed for your file before you run it, you can now click the ‘Overrides’ toggle to access overrides before you start the job. This allows the overrides to apply before starting cutting or if the job is already running toggle it back to double-check the job attributes.

![](/_images/_gsender/_using/gs_us_override.jpg){.aligncenter .size-full}

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
  ![](/_images/_gsender/_using/gs_us_job-loss3.jpg){.aligncenter .size-medium}
1. Here you'll see:
  ![](/_images/_gsender/_using/gs_us_job-loss4.jpg){.aligncenter .size-medium}
   - When you **Last stopped** your file, how many **Total lines** it has, and a **Recommended start line**: this number is generally reliable to use, but in some situations the 'last stopped' number can't be recovered. In these cases you'll want to have noted down the approximate line number that the job failed at then work from there.
   ![](/_images/_gsender/_using/gs_us_job-loss1.jpg){.aligncenter .size-medium}
   - **Resume job at line**: once you've decided where to resume from, you can type the line number in here.
   - **Safe height**: if your CNC has extra Z movement above the failed job, you can put a larger number here to make sure that it doesn't hit clamps while moving into position to resume cutting.
1. Once everything looks good, remember to turn on anything that isn't automated like a trim router or vacuum, then click 'Start from Line' to resume cutting.

**Example**: you were present when the job failed and hit 'Stop' immediately. Nothing moved but the bit broke so you swapped it out and used a touch plate to probe Z. It says the last recorded line was 731 but to be safe you'll subtract 20 and start at 711. The job starts back up a little before the failure and you're able to resume as expected. If instead you hadn't been paying attention for several minutes then you might subtract 50-100 lines instead just to be safe.

![](/_images/_gsender/_using/gs_us_job-loss-notice.jpg "Example of USB port disconnect while running a job where you'll want to check your USB cable, write down the suggested line, then use the ‘Start from Line’ feature as normal."){.aligncenter .size-full}

### Pause Cutting Mid-Job

1. If a carve is dragging on and you need to leave the machine for the night, first you'll want to note down the approximate g-code line number it's at. In the example below you'd note down "731 lines".
![](/_images/_gsender/_using/gs_us_job-loss1.jpg){.aligncenter .size-medium}
1. Once noted down, 'Pause', then 'Stop' the job. This allows the machine to stop more slowly instead of emergency stop.
1. Quickly turn off anything that isn't automated like a router or dust collector and jog the Z-axis up so you don't burn or mar the material. You can also try to pause strategically when the bit is moving and not cutting to avoid damaging your material.
1. At this point it's best to return the cutting tool to the project zero point if possible using 'Go XY0' then 'Go to' for the Z-axis. This way if the zero point is lost when you resume cutting later, then you can just manually set your zero knowing you're still at the zero location.
1. If you're concerned your machine might drift over time for example if you're using a heavy spindle, then another option is to place a block of wood under your cutting tool and jog down to it using the paper method. Once the bit is touching, you can note down the location where you left the machine, then when you resume you can type that location back in (see the end of [Set Zero and Gotos](#set-zero-and-gotos)).

## Safety

gSender is set up to do many things by default to help keep you aware about things going on with your machine. Though we can’t guarantee it can handle everything, we’ve recently introduced a new Settings menu for Safety where you can access many safety items in one place. This includes:

1. **Warn on Zero**: an optional popup that appears when you click to 'zero' just in case you mis-clicked it.
  ![](/_images/_gsender/_features/_zerogoto/gs_fe_ze_zero-warn.jpg){.aligncenter .size-full}
  ![](/_images/_gsender/_features/_zerogoto/gs_fe_ze_zero-warn-gif.gif){.aligncenter .size-full}
1. **Safe height movement**: this number is used when using the ‘goto’ buttons in gSender to manually move your machine around (it’s independent from a safe height you might set in your CAM software). For machines without homing, entering ‘5mm’ will make it move 5mm upwards from the current position, make the goto movement, then move 5mm back down. If your machine has homing, it’ll move to 5mm from the max Z-axis travel, make the goto movement, and then return back to where the bit started. This behaviour helps homing-capable machines to reach a more ideal safe height to avoid collisions during movements.
1. **G-code warnings**: reports back when it sees g-code lines that don’t look correct when the file is loaded or once it’s being sent to the machine. G-code has to follow specific ‘grammatical rules’ similar to other languages for the ‘sentences’ to be correct, so if the lines don’t look correct then your machine might run into problems understanding what it’s supposed to do.
1. **Soft limits warning**: enables gSender to tell you when a loaded file might exceed the cutting area of your machine. This requires that your machine has limit switches and soft limits enabled.
1. **History of Errors and Alarms**: great for tracking problems you might’ve recently run into to help troubleshooting or getting support. All entries are listed in-order and stamped with a date and time.

![](/_images/_gsender/_using/gs_us_safety.jpg){.aligncenter .size-full}
