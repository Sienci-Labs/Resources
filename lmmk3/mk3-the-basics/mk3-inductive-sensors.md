---
title: LongMill MK3 Inductive Sensors
menu_order: 4
post_status: draft
post_excerpt: 
post_date: 2026-05-19 15:42:44
taxonomy:
    knowledgebase_cat: the-basics-lmmk3
    knowledgebase_tag:
custom_fields:
    KBName: LongMill MK3
    basepress_post_icon: bp-caret-right
skip_file: no
featured_image: _images/post-image.jpg
---

- what are limit switches useful for
- firmware setup already done because slb-lite comes with machine profile limit settings on
- startup what to expect
- alarms, adjusting positions? but they also come pre-assembled


Homing Cycle: if your machine has been unpowered, lost power, or lost its location for any reason then it won’t have any reference to where it is. Homing will reliably place your machine by prompting you to ‘home’ anytime you connect to it, allowing it to move toward the ‘home’ position, detect that location using limit switches, and then say “yep, now I know exactly where I am.” This can be used to resume a previous job, apply work offsets for jigs, apply safe height to your quick travel movements to avoid bit collisions, or even set up a tool changing station.

Soft limits and Hard limits: these both exist to prevent your machine from running into itself at its travel limits. Soft limits track your travel limits in software but require homing to first know the CNCs location. Once homed, it’ll know that the machine can’t move further in the homed direction and use the firmware defined maximum travel values to keep track of the limits at the opposite end of each axis. Hard limits can run independently from homing since it looks for when a limit switch gets physically triggered. A trigger will stop the machine to prevent further movement and potential damage.

These can be used separately but are often used together since hard limits’ flaw is requiring sensors on both ends of travel where most machines only sense on one side, while soft limits’ flaw is requiring homing to be effective where sometimes the user can forget to run a homing cycle.

Using Limit Switches
Now that you have your limit switches set up, you’ll need to get used to using them on your machine. Expect to see some new behaviours and even errors or alarms you might not have seen before; this is normal and comes with any switch-equipped-machine.

Homing
If you’ve enabled homing and lost a connection to your machine it will enter an alarm state upon re-connecting. To get out of this alarm state, the machine must be homed so it can rediscover its location. When homing your machine for the first time, be ready to press the E-stop in case any sensor fails to trigger. Once homing is complete, you can check that the machine coordinate values (gray numbers next to the blue ones in gSender) are all set to zero or thereabouts.


There will also be circumstances where you may lose your position and the machine won’t know it so you’ll need to recognize the need for homing and re-home manually. As mentioned earlier, features like soft limits rely on a homed machine to work properly so always check the machine coordinates of the machine and see if their location makes sense. If you’re unsure, we’d recommend re-homing just to be safe.

Limits
With limits enabled, you’ll see errors or alarms appear which warn you when your machine limits are reached. ‘Alarm 2’ or ‘Error 15’ will result from the machine being told to move to a location that’s outside its soft limits either during a cutting job or during jogging respectively. If you think this is incorrect, double-check that you homed your machine otherwise you can check that your maximum travel settings ($130, $131, $132) aren’t too low. Similarly, an ‘Alarm 1’ will tell you that you’ve triggered a hard limit. You’ll have to unlock, move, unlock, move to get outside of the sensors range to escape the hard limit, or otherwise move the axis by hand as long as you re-home afterwards.

If you need to find the maximum travel for your unique setup do the following (optional); home your machine, zero all axes, then jog each axis to where you feel comfortable limiting it. Use the coordinates to set your maximum travel for each axis using $130, $131, and $132.

Work Offsets
With CNC, work offsets can be thought of as bookmarks. They are saved locations for your machine that allow it to run jobs in different ‘zero’ locations without overwriting the previous zero location. Having one or more known locations you can repeatedly return to is extremely useful for restarting a failed job, recovering from a power outage, repeating the same job in different locations, and running multi-fixture jobs.

To change work offsets or workspaces, simply select one of the 6 workspaces from the drop down list in the top right corner of gSender as shown in the photo below. Alternatively, entering the commands G54, G55, G56.. etc. into the console of gSender or UGS will tell the machine to switch into that workspace. You will notice the work coordinates (blue numbers) will change upon switching workspaces to whatever the coordinates are within the new workspace. The machine coordinates (grey numbers) will always remain the same regardless, as these are relative to your machine’s home position.


All 6 of these workspaces are saved by the controller even after powering off the machine. For this reason, using work offsets with the ability to home the machine will give you the confidence to know your job’s relative position no matter what.