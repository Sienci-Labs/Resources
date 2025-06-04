---
title: ytsb Additional Features
menu_order: 4
post_status: draft
post_excerpt: Learn the advanced features of gSender such as shortcuts, macros, workspaces, calibration tools, controlling spindles, lasers, coolant, and more.
post_date: 2021-07-01 15:50:00
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
Remote mode - Restarts without any warning

Remote mode - How do I know it's enabled now? No IP address in top corner and the icon is always green?

Update - Using gSender remotely section

Rotary - Rotary tab won't highlight in Config tab

Rotary - When doing rotary surfacing, on the carve screen, file is still named cing

Rotary - Switch vs Open vs Closed Loop. Need to chat and take notes about the differences here re: gSender

Doesn't mention alternate ways to get to shortcuts,
Lightweight mode explanation confusing,
Coolant tab disable,
Missing macro text to explain the basics of setup,
Tools for Calibration? Firmware Tool? Unsupported CNCs? Config section? Diagnosing in Config, Help, flyout in top toolbar,
Problems in many places where the text hasn't been updated to match the new behaviour like once the Rotary tab is turned on

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

---
## Homing & Limits

Limit switches (also referred to as *inductive sensors*, *end stops* or *homing switches*) are sensors that sit at one or both ends of each movement axis of a CNC to provide a few different functions. gSender provides unique features if you have these switches installed on your machine. You can check out our sensors [HERE!](https://sienci.com/product/inductive-sensor-kit-for-the-longmill-mk2/)

If you don't have sensors, skip ahead [HERE.](#probing)

### Going Homing

When we turn on homing, we can use 3 sensors to find our machine coordinate  home on our machine. For now, we will home to the front left corner of the machine. To enable Homing, Goto Config -> Limits and Homing -> Homing cycle enable -> toggle on.

![](/_images/_gsender/_using/gs_us_dro_homingon.jpg){.aligncenter .size-medium}

Using **grblHAL** enables several more detailed options for you to choose from, like homing single axes, requiring homing on startup, set machine origin to 0, and more. In this image, we have enabled homing, but **not** required it on startup. We have toggled to allow us to manually home the machine, and to **Set the machine origin to 0** once complete.

![](/_images/_gsender/_using/gs_us_dro_hominghal.jpg){.aligncenter .size-medium}

You’ll notice additional buttons appear in the DRO area of gSender:

![](/_images/_gsender/_using/gs_us_dro_homingbtn.jpg){.aligncenter .size-medium}

The **Home** button is a convenient way to home or re-home your machine at any time (sends the typical $h command). The machine will automatically move to your front left corner, using the sensors to position the router over machine home.

![](/_images/_gsender/_using/gs_us_dro_rapidpositionbtn.jpg){.aligncenter .size-medium}

Four **Rapid-Travel** buttons to move your CNC at its maximum speed to any of your machine's 4 corners (offset by 5mm). These can only be used once your machine is homed.

![](/_images/_gsender/_using/gs_us_dro_parkbtn.jpg){.aligncenter .size-medium}

You can configure a **Park Location** to move your router to a set spot consistently at the click of a button. To setup your parking spot, Goto Config -> Basics. Here you can enter the coordinates of your parking spot manually, or move your router/spindle to the spot and hit the **Grab** current position button. Test out your new spot by hitting the Goto button in settings or hitting the P button on the DRO.

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

---

This page covers all the advanced features of gSender such as shortcuts, macros, workspaces, calibration tools, controlling spindles, lasers, coolant, and more. Remember, you can always quickly navigate the page by clicking the headings in the 'Page Contents'.

## Shortcuts

Starting off as a more advanced gSender user, the first feature you’ll want to leverage is shortcuts. These can allow you to assign gSender or CNC actions to keys and key combinations or even to gamepads and joystick movements. There are 3rd party apps like <a href="https://joytokey.net/en/">JoyToKey</a>, <a href="https://xpadder.com/?lang=english&amp;country=CA">Xpadder</a>, <a href="https://www.comfortsoftware.com/comfort-keys/">Comfort Keys Pro</a> and <a href="https://www.rewasd.com/">reWASD</a> that allow you to do this, but to eliminate needing to download and configure other programs we’ve rolled all the functionality into gSender itself.

Going to the Tools tab, you'll see that shortcuts can come in the form of **Keyboard Shortcuts** or **Gamepad**. Both options enable you to set up, modify, and enable or disable shortcuts. These will be automatically saved when you close the dialog box and will remain on gSender as long as the program is installed on your computer.

![](/_images/_gsender/_features/_shortcuts/gs_fe_sh_keygamepad.jpg){.aligncenter .size-medium}

### Shortcut Printing & Disable All

Find yourself forgetting how you’ve configured your keyboard or gamepad profile shortcuts? Hit the **Print** button to generate a simple PDF that you can store on a tablet or print on some paper to keep next to your CNC. This PDF will contain all the shortcuts you’ve created and what actions they’re assigned to.

Want to turn all of your shortcuts off so you don't hit one by mistake? Hit the **Disable All Shortcuts** button to turn all of the shortcuts to inactive in bulk. You can turn on or off individual shortcuts in the **Active** column if you would like to turn off single instances of shortcuts.

![](/_images/_gsender/_features/_shortcuts/gs_fe_sh_printdissable.jpg){.aligncenter .size-medium}

### Keyboard Shortcuts

Either for use on a keyboard, macro pad, or mini Bluetooth keyboard, these are split up into categories you can see in the red box, so they're easy to locate and modify. There are **over 70+ shortcuts** presets already available for carving, overrides, jogging, zero setting, probing, macros, visualization, window navigation, and more!

![](/_images/_gsender/_features/_shortcuts/gs_fe_sh_categories.jpg){.aligncenter .size-medium}

### Common Shortcuts

A great place to start is the Jogging category. In the picture below, see that right now we can jog the **X-axis** by hitting the shift + right or shift + left keys. The **Y-axis** responds to shift + up and shift + down keys and the **Z-axis** uses the shift + pageup and shift + pagedown keys. Being able to look at your CNC, while your hand is on your keyboard is a great way to ensure you are moving in the right direction, without having to look back at your screen to click the mouse on the right button.

![](/_images/_gsender/_features/_shortcuts/gs_fe_sh_commonjog.jpg){.aligncenter .size-medium}

You can use the preset shortcuts, edit them, and/or add your own. Click the **pencil** to the right of each shortcut text box to bring up a popup window that allows you to add or edit your own key combination (shown in the example below). You can see it’s as easy as pressing the key or key combination. In addition, you’ll be informed if the combination you’ve entered is already used elsewhere and be given the option to overwrite the existing one if you want.

![](/_images/_gsender/_features/_shortcuts/gs_fe_sh_editshort.gif){.aligncenter .size-full}

### Gamepad Shortcuts

Many users really love this feature since using a controller is convenient (especially for when you're closer to your machine), inexpensive, and makes certain repetitive actions much easier. Common options are Xbox, PlayStation, and other third-party controllers available to buy online.

We have some [pre-made profiles](#tested-gamepads) for gamepads we've already tested with gSender and you can still reference these if you have a different gamepad or want to make your own.

![](/_images/_gsender/_features/_shortcuts/gs_fe_sh_testedprofiles.jpg){.aligncenter .size-medium}

To create your own, connect your gamepad to your computer and click the ‘Add New Gamepad Profile’ button, then make sure the gamepad is recognized before beginning to assign actions to each button. These profiles mean you can set up multiple gamepads if you'd like since they each have their own unique ID.

![](/_images/_gsender/_features/_shortcuts/gs_fe_sh_addgamepad.jpg){.aligncenter .size-medium}

If you run into difficulty with getting a particular gamepad set up in gSender, consider:

- Some gamepads may require drivers to be downloaded so your computer can read the signals that the gamepad sends out.
- Go into the gamepad profile while it's connected and click the **Help button** where you'll be able to diagnose whether your gamepad is broken and sending out bad signals.
- Searching for documentation provided by the manufacturer (for example, <a href="https://support.xbox.com/en-CA/help/hardware-network/controller/connect-xbox-wireless-controller-to-pc" target="_blank" rel="noopener">Xbox</a> or <a href="https://www.playstation.com/en-ca/support/hardware/ps4-pair-dualshock-4-wireless-with-pc-or-mac/" target="_blank" rel="noopener">PlayStation</a>).

#### Tested Gamepads

To better guarantee your experience using a gamepad in gSender, we’ve taken the time to test a shortlist of some common and affordable options that are easy to source. With community help, we hope to continue growing this list of **officially tested gamepads** which currently includes:

[su_table responsive="yes" alternate="no"]
<table>
<tbody>
<tr>
<td><img class="non alignnone" src="https://resources.sienci.com/wp-content/uploads/2024/08/gs_fe_sh_controller-xbox-1.png" alt="" width="240" height="180" /></td>
<td><b>YCCTeam Xbox Controller</b>
<ul>
  <li>Wireless</li>
  <li>Tested on Windows and macOS</li>
</ul>
</td>
</tr>
<tr>
<td><img class="non alignnone" src="https://resources.sienci.com/wp-content/uploads/2024/08/gs_fe_sh_controller-logi-1.png" alt="" width="240" height="180" /></td>
<td><b>Logitech F710</b>
<ul>
  <li>Wireless</li>
  <li>Tested on Windows and macOS</li>
</ul>
</td>
</tr>
</tbody>
</table>
[/su_table]

Having a listed gamepad means you can both be more confident that your hardware will be compatible with gSender, as well as many of the ‘tested gamepads’ will have pre-made shortcut profiles built right in to save you time setting up your own.

#### Gamepad Setup

Hit the **Add New Gamepad Profile** button, connect your controller to your PC and press any button on it. gSender will identify and provide a profile if one is available. You can see in the screenshot below, it correctly identifies the DualSense Wireless Controller I’m adding. Enter your profile name and hit **Add New Profile**.

![](/_images/_gsender/_features/_shortcuts/gs_fe_sh_addprofile.jpg){.aligncenter .size-medium}

Once you have a profile for your connected gamepad, click on that profile to edit it.

![](/_images/_gsender/_features/_shortcuts/gs_fe_sh_ps5dualsense.jpg){.aligncenter .size-medium}

Inside a profile, you'll be able to see if that specific gamepad is currently connected and be able to assign shortcuts to the two major groups: **buttons**, and **thumbsticks**.

Buttons are the most versatile in how they can be set up. Any button on your gamepad can be set up to:

- Activate an action
- You can assign a button as a 'Second Action Button' which acts similar to a 'Shift' key on your keyboard to allow you to create two-button combinations on your gamepad.
- You can also assign a ‘Lockout Button’ which acts as a safety lock for your CNC when controlling it with the gamepad. If you set up a lockout button, then no other buttons on the gamepad will work until you're pressing on the lockout button. This stops from pressing buttons accidentally or if you dropped your gamepad on the ground.

To add an action to a button, start by pressing the button on your gamepad to see which one on the list lights up green. In this case, the X button lit up button 0. After pressing the `+` symbol in the Action column, you will see a list of actions you can map to that button. In this case an action was added for **Rapid Position - Back left corner**, so now when the X button is hit on the gamepad, gSender will move the CNC to the back left corner!

![](/_images/_gsender/_features/_shortcuts/gs_fe_sh_backright.gif){.aligncenter .size-full}

You can repeat these steps to keep adding more shortcuts to your gamepad, this also includes:

- If you're having difficulty remembering your gamepad buttons, you can click on the black box label and rename it to whatever you'd like.
- The '2nd Action' column will allow you to give each gamepad button a second shortcut action once you set up a 'Second Action Button'. Do this by clicking the `+` symbol in the Action column of the button you want to use, then clicking the 'Use as Second Action Button' toggle on the right side.
- Assign a 'Lockout Button' in a similar way but by toggling the 'Use as Lockout Button' toggle on the right side.

![](/_images/_gsender/_features/_shortcuts/gs_fe_sh_controller-xbox.jpg){.alignnone .size-medium}

Thumbsticks are set up to be used for jogging because of the ability to move them a little or a lot, which is different from buttons which can only be clicked on or off. This works well because most gamepads tend to have 2 thumbsticks (like the Xbox controller shown above), meaning you can use one to jog in the X and Y, and the other to jog in the Z and A (if your machine has a rotary axis). For gamepads that don't have thumbsticks this is still fine because buttons can also be set up to jog.

On the right side of the gamepad profile window, you can see the options for what axis you'd like to move with your gamepad thumbsticks. Similar to setting up buttons, you can move the thumbstick to see which one lights up, and you can also assign a '2nd action' if you'd like. In this example, Stick 1 controls the X-axis left and right, and the Y-axis forward and back while Stick 2 controls the A-axis with left/right and the Z-axis with up/down.

![](/_images/_gsender/_features/_shortcuts/gs_fe_sh_thumbsticks.jpg){.aligncenter .size-full .nar}

Once you've set up your thumbsticks, you'll find you can push them any amount and the distance you push them will decide the speed that axis moves at. If you've set up both the left/right and up/down, you can also mix these to make continuous diagonal movements to get to your final location easier. You can also flick the thumbstick once and the CNC will move one increment, according to the rapid/normal/precise movements you have set up for Jog Controls.

- If you find your thumbstick is moving the axis in the wrong direction, use the '**Invert**' checkbox to correct that
- If you let go of the thumbstick and the axis keeps moving, increase the '**Zero Threshold**' amount since your gamepad might be older and more worn out
- If you get jittering while moving with the thumbsticks, or you let go of the sticks and it takes a while to stop moving, you might want to adjust the '**Movement Distance Override**' value until you get smooth movement on your setup

![](/_images/_gsender/_features/_shortcuts/gs_fe_sh_thumbsticksthreshold.jpg){.aligncenter .size-full .nar}

Another cool feature is the **Use MPG** selection. If you map one of your thumbsticks to an axis with MPG selected, it will automatically grey out the other stick selections. Now you can rotate your stick in any direction and for each quarter rotation, your axis will move once, according to your preselected Jog Controls.

![](/_images/_gsender/_features/_shortcuts/gs_fe_sh_gamepad-joystick-mpg.jpg){.aligncenter .size-full .nar}

## Lightweight Mode

This mode enables gSender to run faster on computers that are less powerful and prone to lagging. ‘Lightweight Mode’ reduces the memory gSender uses by turning off processor-heavy aspects of the visualizer, from reducing detail to disabling it altogether. You can toggle it on or off using the **Feather Icon** positioned on the left side of the visualizer.

![](/_images/_gsender/_features/gs_fe_lightweight-1.jpg){.aligncenter .size-medium}

If you go to the visualizer settings, you can also customize what features are active in both **Light** and **Everything** modes.

![](/_images/_gsender/_features/gs_fe_lightweight-2.jpg){.aligncenter .size-medium}

If gSender's visualizer is impacting the performance of your machine but Lightweight mode only helps once **Everything** is turned off, the **Light** option could help. This mode substitutes the default 3D viewer with a pre-rendered, top-down image of your project, drastically reducing computer strain but still allowing the project to be displayed.

## Touch Plate Setup

gSender has support for three types of touch plates:

1. The Standard Block design
1. Z Probe, also sometimes referred to as a ‘puck’
1. And our specialized AutoZero touch plate

For a Z Probe, setting up is simple since you just need the thickness of the ‘puck’. Enter that value into gSender’s ‘Probe’ settings under ‘Z Thickness’ and you should be good to go!

![](/_images/_gsender/_features/_probing/gs_fe_pr_probethick.jpg){.aligncenter .size-medium}

If you’re trying to set up a custom ‘standard block’ plate, use some calipers to pick up on the measurements noted below. Once these are noted down, enter these into gSender’s ‘Probe’ settings in similarly named entries, and now you should find that gSender’s probing routine has been altered to fit the shape of your touch plate.

![](/_images/_gsender/_features/_probing/gs_fe_pr_dimensions.jpg){.aligncenter .size-medium}

## Coolant Control / IOT Relay

If you have a coolant control pin on your CNC machine, gSender has a tab for manually controlling it. Under the 'Coolant' tab on the main screen, you can find the 'Mist' and 'Flood' buttons to activate the different modes of coolant use, as well as an indicator for whether the coolant function is active or inactive. This indicator also functions during job sending. You can turn off both coolant pins by pressing the 'Off' button.

Many hobby CNCers don't have a need for coolant and so prefer to use these outputs for controlling other periphery. The most common is an IOT relay that can be used to automatically control a vacuum for dust collection, the CNC's router, LED lighting, and more. See an example of how to set that up here: <a href="https://resources.sienci.com/view/lm-iot-relay/" target="_blank" rel="noopener">https://resources.sienci.com/view/lm-iot-relay/</a>

![](/_images/_gsender/_features/gs_fe_coolantcontrol.gif){.aligncenter .size-full}

## Spindle & Laser Support

Similar to the manual coolant control, this area is for manual control of a spindle or laser outside of g-code sending. If you have a spindle or laser, you can activate these controls by going to the settings gear at the far right. In the ‘Spindle/Laser’ section in the left toolbar, press the toggle for ‘Spindle/Laser’.

![](/_images/_gsender/_features/_spinlaser/gs_fe_sp_laseron.jpg){.aligncenter .size-medium}

Back at the main screen, you'll see the ‘Spindle/Laser’ tab at the bottom right. Here you can click to toggle between 'Spindle Mode' and 'Laser Mode', changing your grbl settings for you and displaying buttons specific to each device. For each mode there is also a red caution circle that indicates whether the spindle or laser is active. This works during manual control but also during job sending.

In spindle mode you can set the spindle speed with a slider, spin it up in either direction, and stop it again with the 'Stop' button. These are all based on g-code commands that can also be entered into the console manually if desired. The speed slider is set from your grbl firmware settings, so max and min speed can be altered in the Firmware Tool.

![](/_images/_gsender/_features/_spinlaser/gs_fe_sp_turnonoff.gif){.aligncenter .size-full}

'Laser Mode' is very similar, allowing for On/Off control, a slider for setting the laser power during manual control, and a ‘Laser Test’ button. The laser testing function is handy when troubleshooting your laser setup or for other sorts of locating and alignment because it only enables the laser for a short time before turning it back off again. Though this is much safer than regular on/off control, we still highly advise that you have you have a hand on a kill switch or E-stop during testing or control of either Laser or Spindle modes so that in case something goes wrong with your computer or the program they can still be safely deactivated.

![](/_images/_gsender/_features/_spinlaser/gs_fe_sp_turnonlaser.gif){.aligncenter .size-full}

### Laser Diode Support

Some accessories can be really handy to add to a CNC router like a laser diode, drag knife, or pen plotter. These would all perform better on a faster, dedicated machine, but for occasional use why not use the existing motion system of the router to do other things for you? A laser diode in particular can be great because you can clamp the material to carve and then laser engrave afterwards and know that everything is still aligned.

Since many CNCs are coming with diode accessories, gSender has some unique features to also support lasers. Once 'Laser Mode' is turned on, gSender will:

- Automatically apply an offset from the router/spindle to the laser so all your g-code files stay aligned (configured in the Spindle/Laser settings, or with Firmware settings $741 and 742 on the SLB)
- Turn on the laser at low power when running a job outline (enabled in the Spindle/Laser settings). This will help you to better see where your project is going to be located on the material
- Switch to a specialized visualization designed to show raster engraving images better than typical g-code visualizers. Seeing the laser intensity in the movements is very useful to get a better idea of what your projects are going to look like when they’re run. This will only apply to files loaded after ‘Laser mode’ is enabled and the colour can be customized in the settings. By default you will see your loaded file turn from **blue** to **red**

![](/_images/_gsender/_features/_spinlaser/gs_fe_sp_laser-vis.jpg){.aligncenter .size-medium}

## Macros

Macros are standalone buttons within the gSender interface that allow you to execute a series of g-code commands when they're run. Macros can come in handy for a variety of uses:

- Button to run a v-carve or laser engraving of a common insignia into the back of your wood pieces
- Perform a specialized probing function for a particular jig you've set up
- Apply a predetermined offset that allows you to easily array your cutting jobs

You can create macros using the ‘+’ button under the ‘Macros’ tab.

![](/_images/_gsender/_features/gs_fe_macros1.jpg){.aligncenter .size-medium}

New macros will appear as buttons in the ‘Macro’ tab that can be rearranged by dragging them around. These buttons will display the macro name, and can always be later altered or deleted by clicking on their '...' button.

![](/_images/_gsender/_features/gs_fe_macros5.jpg){.aligncenter .size-medium}

Any macro can be executed by pressing it. Once running, you should see the macro start to pulse green while a toast notification on the bottom right hand side of gSender also notifies you that it's running.

![](/_images/_gsender/_features/gs_fe_macros3.jpg){.aligncenter .size-medium}

Macros can also be executed using shortcuts. Every time you create a new macro it'll become available at the bottom of the shortcuts list for you to assign a key or gamepad button to. Add your keybindings and enable them by pressing the slider beside the label.

You can share macros with other users or transfer them between computers by using the import and export features. To import one or multiple macros, just press the button with the downward arrow and a browsing window will appear so that you can select the macros you wish to import. Similarly, to export all your current macros, press the button with the upward arrow and it'll generate a save file for you.

![](/_images/_gsender/_features/gs_fe_macros4.jpg){.aligncenter .size-full}

### Advanced Macros

gSenders Macro architecture is based on **JavaScript** and uses the Esprima library (<a href="https://esprima.org/" target="_blank" rel="noopener">https://esprima.org/</a>) and so will theoretically support any code that it does. This is exciting because Macros can move far past basic variables if you’d like to perform advanced functions on your CNC:

If you want some initial inspiration, see other macros [**made by our community**](#community-macros) or ones <a href="https://github.com/cncjs/CNCjs-Macros/blob/master/Hole_Center" target="_blank" rel="noopener"><b>made for CNCjs</b></a> (another g-code sender) which should also work in gSender. Otherwise, here are some other points of guidance:

1. You'll want to develop your understanding of typical <a href="https://linuxcnc.org/docs/html/gcode/g-code.html" target="_blank" rel="noopener">g-codes</a> and <a href="https://linuxcnc.org/docs/devel/html/gcode/m-code.html" target="_blank" rel="noopener">m-codes</a> that are used for CNC control (the pages linked are very good sources for that)
1. The "Macro Variables" dropdown in gSender shows many of the most commonly used operations when making your own macro
1. Make your own variable with `%variable = value_you_want_to_set` (ex. % probeSpeed = 150)
1. Use your variable in g-code, like `G21 G91 G0 X[variable]` (moves the X-axis by the amount set in the variable)
1. Test your code by printing it to the console `([variable])`
1. Make dialog boxes appear on the screen to confirm a value or position by putting in an M0 line with a comment, for example `M0 ;Remember to turn on your router before the next step` which will pause the macro and give you the option to 'continue' or 'cancel'
1. Start experimenting with basic math using numbers and variables
1. Use global variables `global.variable` if you want variables that you can use in other macros (note that these get reset once gSender is closed)
1. Read up on all the other Math features available like <a href="https://developer.mozilla.org/en-US/docs/Web/JavaScript/Reference/Global_Objects/Math" target="_blank" rel="noopener">absolute value, rounding, and trigonometry</a> (become very useful for more advanced probing cycles for example)
1. Start to add more logic to your code using ternary expressions to choose between two outcomes (e.g. `%variable = (30 > 20) ? 10 : 20` which is checking if 30 is bigger than 20, and if it is it'll make the variable = 10, otherwise it'll make the variable = 20).
1. Here's an example of a more advanced macro, made by gSenders Lead Developer, which shows off much of the guidance given above. This macro was made for our new <a href="https://sienci.com/product/slb/" target="_blank" rel="noopener">SLB control board</a> in order to cycle between its 3 <a href="https://resources.sienci.com/view/slb-manual/#status-lights" target="_blank" rel="noopener">status light states</a>.
   - The macro is only 3 lines.  First it checks what the current light state is and sets it to 0 if it doesn't have a state. Next, it sets the lights to the current state but applies a modulus of 3 since we can only have a state value of 0, 1, or 2 so we'll get an error if the value is 3 or above. Lastly, it adds +1 to the state so that if the macro is run again it'll put the lights into a new state.
   - `%nextLight = global.lightState || 0`
   - `M356 P0 Q[nextLight % 3]`
   - `%global.lightState = Number(nextLight) + 1`
1. Store many variables in an array so that those variables can be used in other macros without assigning them all as global
   - `%setup = {}`
   - `%setup.this = 0`
   - `%setup.that = 1`
   - `%global.setup = setup`
   - then in the other macro `%setup = global.setup`
1. Create functions that you can then call later such as `%rapid = function (x, y) {return 'G53 G90 G0 X' + x + ' Y' + y + '\n'}` then later run it with `[rapid(x, y)]`
1. Read more about the Esprima library here: <a href="https://docs.esprima.org/en/latest/syntactic-analysis.html" target="_blank" rel="noopener">https://docs.esprima.org/en/latest/syntactic-analysis.html</a>

## Console

The console is a tab that you can access at the bottom right hand side of the gSender window. The text here shows a truer representation of the communication that happens between your computer and your CNC. As you start to understand more about your machine, this is a great tab to reference so you can see if commands are being properly sent, received, and executed. It's also great for troubleshooting since you can:

- Manually send g-code commands to your CNC
- Check for errors or alarms and the g-code that caused them (normally the line that comes before)
- Copy text straight from the console to send in an email for help by clicking the ... beside the "Run" button
- Even open the console in another window by pressing the top, right icon to help you see more console text at a time (if you press the button again once you reconnect to your CNC, it'll reconnect the console stream to the original window too)

![](/_images/_gsender/_features/gs_fe_console.jpg){.aligncenter .size-full}

When you first start up gSender, the console will display EEPROM settings that are sent from the Arduino in the control box. These EEPROM settings control parameters for your CNC such as:

- Maximum speed and acceleration in each axis
- Boundaries of the work area
- Direction of each axis movement
- Limit switch settings

To access EEPROM settings again, enter in “$$” into the console and hit the 'Enter' key or click the 'Run' button. These settings can be changed via the console as well as the Firmware Tool which we've designed as a much more visual way to alter machine settings.

## Tools for Calibration

The **Tool Tab** in gSender enables you to make finer adjustments to your machine for improved performance. There are four processes available in gSender:

- Surfacing Wasteboard
- Movement Tuning
- XY Squaring

![](/_images/_gsender/_features/gs_fe_tools_main.jpg){.aligncenter .size-full}

### XY Squaring

When mounting your LongMill on the table, there is a basic squaring process illustrated in our instructions (<a href="https://resources.sienci.com/view/lm-table-mounting/">https://resources.sienci.com/view/lm-table-mounting/</a>). If you do find that the machine is not perfectly square, you can follow the steps in this process to fine tune the position of your rails.

When you access the ‘Calibration Tool’ window, the ‘XY Squaring’ procedure is shown on the first tab. All instructions are illustrated in the window, however a brief overview will be provided.

![](/_images/_gsender/_features/gs_fe_xysquaring.jpg){.aligncenter .size-medium}

You will need the following:

- Ruler or measuring tape
- Tapered bit or V-bit
- Tape

1. Jog the machine to the front left corner, with the bit raised slightly over the surface of your wasteboard
1. Mark the point with tape and move the machine as directed

![](/_images/_gsender/_features/gs_fe_xysquaring1.jpg){.aligncenter .size-medium}

1. Continue to mark points and move the machine until all boxes are complete

![](/_images/_gsender/_features/gs_fe_xysquaring5.jpg){.aligncenter .size-medium}

1. Measure the distance between each dot and enter accordingly into the 3 boxes

![](/_images/_gsender/_features/gs_fe_xysquaring6.jpg){.aligncenter .size-medium}

1. Adjust your rail positions with the values determined by the XY Squaring procedure. If you are really out of square, you may see instructions to adjust your steps per mm, found in the Config -> Motors tab.

![](/_images/_gsender/_features/gs_fe_xysquaring7.jpg){.aligncenter .size-medium}

The great advantage to this tool is it saves you having to do the trigonometry yourself and will also let you know if your machine is aligned closely enough that it’s not worth worrying about.

### Movement Tuning

You are able to change how much your motors turn to improve the accuracy of your machine movement. This is done through modifying the EEPROM settings that are stored on your LongMill, which this process will guide you through. You can tune the X, Y and Z axes individually. All instructions are illustrated in the 'Calibration Tool', however a brief overview will be provided.

You will need:

- Marker or tape
- Measuring tape

1. Jog your machine to the middle of whichever axes you choose to tune, so that there is enough room to complete this procedure. For example, on the X-axis you would jog halfway on the X-axis rail
1. Select what axis to tune on the drop down menu

![](/_images/_gsender/_features/gs_fe_movementtuning.jpg){.aligncenter .size-medium}

1. Mark down the location of your reference on the machine. For example the X-axis tuning references the edge of the XZ gantry on the X rail
1. Move the axis a chosen distance
1. Measure the travel distance between the marked location and the reference edge

![](/_images/_gsender/_features/gs_fe_movementtuning4.jpg){.aligncenter .size-medium}

1. Change the EEPROM setting as recommended by the procedure by pressing **Update Steps-per-MM**

![](/_images/_gsender/_features/gs_fe_movementtuningfin.jpg){.aligncenter .size-medium}

1. Repeat the procedure for each axis you wish to tune

### Surfacing

https://youtu.be/jfInIEOB3kU

Surfacing the wasteboard of your machine can easily be done right inside gSender! The first thing you’ll want to do is decide where you want to start surfacing and in most cases the front, left of the machine is the most convenient. You might also want to remove any accessories that might get in the way of your machine travelling around during surfacing as well as have a good vacuum on hand because surfacing can get really messy.

![](/_images/_gsender/_features/gs_fe_surfacing.jpg){.aligncenter .size-full}

1. Start by entering the settings you’d like to use to generate your surfacing job:
   - **X & Y**: decides the cutting size (width and depth) you want to surface. If you’re surfacing your wasteboard, use the manufacturer’s spec on max machine travel or manually jog to the limits to cover the full cutting area, or if you’re surfacing a piece of material then you can use a measuring tape.<br>- **LongMill MK2**: 818mm (32.2”) or 1278 (50.3”) x 366mm (14.4”) or 866 (34.1”)<br>(if using limit switches, remove about 8mm/0.3” in X and 11mm/0.43” in Y)<br>- **LongMill MK1**: 320mm (12.6”) or 805 (31.7”) x 344mm (13.54”) or 844 (33.23”)<br>(if using limit switches, remove about 35mm/1.38” in X and 24mm/0.94” in Y)<br>(if using magnetic dust shoe, remove about 34mm/1.34” in X)<br>- **Mill One**: 235mm (9.25”) or 257 (10.1”) x 185mm (7.28”)
   - **Cut Depth & Max**: describes how deep you want to cut per pass and the total depth you want to cut down. For larger surfacing bits usually you should keep cut depth below 1mm, max depth should be increased to a couple millimeters if you think your material is very warped.
   - **Bit Diameter** (typically 6 - 25mm): make sure you have the right bit for the job like a surfacing tool or a large, flat end mill since this will give you a better surface finish.
   - **Spindle RPM** (default 17000): only applies if you have an automatic speed control, otherwise set this manually on your router.
   - **Feed rate** (default 2500mm/min): influenced by the RPM, step over, bit diameter, and cut depth. Luckily if you set it incorrectly you’ll be able to override it during the job since surfacing can cause burning when cutting too slow or can have worse surface finish when cutting too fast.
   - **Stepover** (default 40%): sticking around 40% tends to be a good balance between speed (using a higher %) and better surface finish (using a lower %).

![](/_images/_gsender/_features/gs_fe_surfacing2.jpg){.aligncenter .size-full}

1. Select a Start Position of any four corners or the center by clicking the dot; this is where the surfacing will begin. You can also select a surfacing pattern of spiral or zig-zag. The spiral will only cut from the inside-out if the start position is the centre. If you toggle the flip cut direction, the spiral will cut conventional instead of climb, and the zig-zag pattern will cut vertically instead of horizontally.

![](/_images/_gsender/_features/gs_fe_surfacing3.jpg){.aligncenter .size-full}

1. Press ‘Generate G-code’ and check your surfacing tool path using the ‘Visualizer Preview’ tab. You can also see the raw g-code using the ‘G-code Viewer’ tab and can copy and save it to a g-code file if you’d like to use it again later.

![](/_images/_gsender/_features/gs_fe_surfacing4.jpg){.aligncenter .size-full}

1. Press ‘Run on Main Visualizer’ to bring the g-code into gSender’s main screen. Make sure that you jog to the starting point and set your zero in the right place before starting the job. You can also press the ‘Outline’ button as an easy way to check that you’ll be surfacing where you expect and if you find the dimensions aren’t correct you can always re-open the surfacing tool, tweak the size, and try again. Feel free to start the job whenever you’re ready!

![](/_images/_gsender/_features/gs_fe_surfacing5.jpg){.aligncenter .size-medium}

Did you know that surfacing can be used for more than your wasteboard? It’s great for creating a perfectly flat surface of your starting materials, just like a jointer or surface planer would. You can also use the <a href="https://docs.google.com/document/d/1yUO8bMAw5XoRO8AWGc3ZB5_WVj12ARP-kvf5pciUNL0/edit#heading=h.r1c788pgn92b">Rotary Surfacing</a> tool if you are wanting round stock.

### Firmware Tool

Any board you have will come pre-installed with CNC firmware, along with the custom EEPROM settings for that machine, so typically you won’t need to access the ‘Firmware’ tool. If you choose to use this tool, it can give you access to many of your machines "behind-the-scenes" settings for tweaking or modding your setup.

### Diagnostics

If you’d like to see general information about your CNC or are experiencing issues that you’d like to troubleshoot, gSender has a Diagnostics tool for that. Access it by clicking the ‘Calibrate’ tool on the top-right and opening the ‘Diagnostics’ tab.

Here you'll see machine information, notable firmware settings, and at-a-glance status on whether your limit switches, touch probe, or other pins are activated. This can be handy if you’re encountering odd behaviour with certain machine accessories or to double-check your wiring.

![](/_images/_gsender/_features/gs_fe_tools_diagnostics.jpg){.aligncenter .size-full}

Another valuable feature is the ability to download a Diagnostic PDF file of your CNC machine when you click ‘Download Now!’. This PDF file is meant to include information on your computer, your CNC, recent alarms / errors, any currently loaded g-code file, and more. It's basically a treasure trove of information that you can share on community forums, Facebook groups, or with your CNC customer support. This can go a long way towards getting help from others on diagnosing any problems your CNC might be experiencing.

To download the PDF, click the “**Download Now!**” button. This will open a save dialog box. Save the file to a location that you can easily access to send along to others in an email, support ticket or post online.

Lastly, you can copy the last 40 lines of code in the gSender console (1), by hitting the double page icon to the left of the Run button (2). This will copy the code to your clipboard, so you can paste it to forums or share it with support teams.

![](/_images/_gsender/_features/gs_fe_copyconsole.jpg){.aligncenter .size-full}

## Stats Tab

Curious to know how many jobs you’ve completed, how many hours you’ve put on your machine, what alarms you've encountered or what maintenance you should be focusing on? Click on the **Stats Tab** to see an Overview of all your stats. Here you can see information about your machine including job statistics, machine maintenance, alarms & errors, configuration settings, diagnostic files and resources to help along your CNC journey. You can check out the main overview page or click into each section to see further details. Click a tab at the bottom of the screen, or click on the button in each section.

![](/_images/_gsender/_features/gs_fe_statsconfig.jpg){.aligncenter .size-medium}

### Job Stats

The Job Table tab provides a simplified breakdown of each job, including the file name, duration of the job, # of lines in the job, start time/date and if the job completed successfully or not. This section also displays jobs per port and run time per port.

![](/_images/_gsender/_features/gs_fe_statsjobs.jpg){.aligncenter .size-medium}

### CNC Maintenance

In the Maintenance tab, you will see preset tasks with an hourly countdown range, to remind you when a maintenance task is due to be performed. These times pull directly from the runtime of your jobs and allow you to mark them as complete to reset the timers. Once the task is in range, the maintenance is due, once past the range, the task becomes critical to address. Each task includes a timer showing how much time remains before the task needs attention, detailed descriptions and an edit button or complete task button. This section also displays all upcoming maintenance in a colour coded list to the right.

![](/_images/_gsender/_features/gs_fe_statsmaintenance.jpg){.aligncenter .size-medium}

You can also add your own reminders, time due range and description to this section, to really make it your own.

![](/_images/_gsender/_features/gs_fe_statsmaintenanceadd.jpg){.aligncenter .size-medium}

### Alarms & Errors

In the Alarms & Errors tab, you will see a list or errors and alarms. Details include the error or alarm number, time and date and a brief explanation of the issue. Here you can also **Clear Alarms & Errors** or **Download a Diagnostic File** for further troubleshooting.

![](/_images/_gsender/_features/gs_fe_statsalarmserrors.jpg){.aligncenter .size-medium}

To read more about Alarms & Errors, visit [HERE!](https://resources.sienci.com/view/gs-grbl-alarm-error-codes/#alarms)

### Get Help

If you have questions, need support, want to read up on specific features, or investigate cool community activities, you can check out the **Help section**. Here you can download a diagnostic file to share with support, read more of our [Resources](https://resources.sienci.com/), join our [Community](https://forum.sienci.com/) or dig into our [Github](https://github.com/Sienci-Labs/gsender/releases/) repository.

![](/_images/_gsender/_features/gs_fe_statsgethelp.jpg){.aligncenter .size-medium}

### Unsupported CNCs

If your CNC isn't listed below, then it's considered "unsupported":

- Sienci Labs **LongMill** (MK1, MK2, and MK2.5), **AltMill**, and **Mill One** (V1, V2, and V3)
- Don't see your machine on this list and want it fully supported? Let your manufacturer know to get in contact with us so that we can add their machine profiles to gSender :)

If your machine is unsupported, it means that the Firmware Tool won't be able to perform the same features as for supported machines. In this case, **if your machine isn't working, contact your manufacturer to get their advice on how to fix it**. Using this tool makes it possible to ruin your machine further and we won't be able to help you with your specific hardware. For unsupported machines:

1. Choosing your machine **name** from the drop down menu is primarily cosmetic
1. **Flash** either vanilla grbl, or for grblHAL boards upload a hex file to flash a new firmware
1. **Import** EEPROM settings from a file if you had settings that were working and something changed
1. **Export** current EEPROM settings if you'd like to save your current setup in case something goes wrong
1. **Defaults** restore all your machine settings back to typical vanilla grbl values

![](/_images/_gsender/_features/gs_fe_firmwaretool.gif){.aligncenter .size-full}

### Supported CNCs

If your CNC was listed above then it's "supported" by the Firmware tool. This means that the manufacturer is working with us to keep their machine profiles up-to-date, which in-turn gives you access to more features.

## Automations

A powerful feature to control your accessories automatically (like turning on/off a spindle or vacuum) or to run movement macros that are custom to your machine. 'Program Events' (formerly "Start/Stop G-code")' in gSenders settings automatically apply g-code to your cutting job at the start, end, or if you stop, pause, or resume the job. The 'Stop' event is there to ensure that "ending g-code" is always run even if you have to stop a job prematurely. You can also toggle these on and off if you don't want them run for specific jobs.

Three massive perks to setting up automations this way are:

1. There's no need to get into the weeds customizing your CAM post processor
1. gSender is able to send code when you pause, resume, or emergency stop your machine, all of which a g-code file on its own would never be able to do
1. This additional amount of control will make your CNC safer to use

For example, if you were to add M3/M5 commands to your CAM post processor to control your spindle but then chose to pause your job midway to check something, then most CNCs wouldn't know to stop spinning your spindle or retract it since g-code files can't carry this information; this is where gSender is able to the heavy lifting.

For the text-box of the situation you want the action to happen, type in the g-code commands you wish to run, then press the '**Update**' button to save it. For example, if you installed an IOT relay to turn your router and vacuum on and off and wanted to make sure they were enabled for every job you ran, you could add:

- "**M8**" for Start and Resume
- "**M9**" for Stop and Pause
- If you wanted to add a delay to give your vacuum or router time to fully turn on, then you could add "**G4 P5**" after the M8 for a delay of 5 seconds (you can customize that delay to your equipment)
- If you wanted to keep the vacuum and router running during a pause, then you don't need to add "**M9**" to Pause
- All this can also apply to automatically control a spindle, where you'd instead use "**M3**" and "**M5**", you can also add a delay with "**G4 P#**"
- If you want to raise the Z-axis on Pause and lower it on Resume, you could also add:
  - "%global.move=modal.distance" then "G91 G0 Z-5" for Pause to move 5mm out of the way
  - "G91 G0 Z5" then "[global.move]" for Resume to move back down

![](/_images/_gsender/_features/gs_fe_automations.jpg){.aligncenter .size-full}

## Tool Changing

For CNC machines, tool changes are pauses that are programmed in the g-code for a user to switch out the cutting tool for a different one, or the machine to do that automatically. The workflow can also sometimes involve pausing until the user tells it to continue, usually through a 'Resume' and/or 'Confirm Tool Change' button on the machine interface. This allows you to run multiple toolpaths (cutting operations) within one g-code file.

The g-code for tool changing is an M6 command. gSender is quite capable when it comes to customizing CNCs for tool changing, even having full Wizards built-in. The tool change options are in the Config ➜ Tool Change tab. You can select from one of 6 different options, and even choose to 'passthrough' the M6 and T commands to the CNC controller for CNCs that are capable of handling tool changes on their own.

![](/_images/_gsender/_features/gs_fe_toolchange.jpg){.aligncenter .size-full}

You can **Ignore** any M6 tool change commands, **Pause** the job when a tool change is recognized, or select one of the last three **Wizards** that will guide you through pre-set tool changing methods. In the image below, you can see an example of the helper tab opening up the **Wizard** to guide you through the Standard Re-zero tool change.

![](/_images/_gsender/_features/gs_fe_toolchangewiz.gif){.aligncenter .size-full}

If you are using one of the wizard options, know that you can access all other gSender controls while the wizard is open like jogging and zeroing. It also has flexibility to go back a step if you missed something or had a mistake, or to be minimized temporarily if you want to check the visualizer.

1. **Ignore**<br>This simply ignores any M6 commands in the g-code file. This is the default option since it’s perfect for beginners that only make projects with one tool or those that create separate files for each tool and prefer to manually perform tool changes between files.
1. **Pause**<br>Pauses gSender at the tool change point, as if you had hit the pause button manually. This gives you freedom to jog, zero, or anything else you’d like, and is great for those that are running multi-tool files but want to use a different process than the Wizards provide. This could be a manual probing process, a different tool changing approach, or running custom macros to support your machines specific hardware. gSender is compatible with tool length sensors like the Carbide 3D bitsetter, and our community has compiled a <a href="https://forum.sienci.com/t/bitsetter-and-other-tool-length-sensors-supported-in-gSender/3877/4">list of macros</a> for tool changing that you can use when you are paused. Just note that pausing can’t always guarantee keeping track of your movements and actions when it comes time to resume the job so try to ensure you get back to the starting point and set zeros correctly.
1. **Standard Re-zero** (Wizard)<br>Titled ‘standard’ because it’s exactly the same as the standard process you might normally follow for running a file, changing the tool, re-zeroing Z, then running the next file except it’s applied to a single file with multiple toolpaths. Since the process is so familiar, this is a great way to dip your toes into tool changing within one file. Compatible with using a touch plate or the paper method, zero out at a predetermined spot (usually at the front left corner), and use jogging to move around. The advantage of introducing this extra automation and guidance during tool changes is that you don’t have to worry about custom macros and it reminds you of simple steps like turning the router back on or zeroing Z.
1. **Flexible Re-zero** (Wizard)<br>Similar to the ‘standard’ wizard with similar steps and manual movements but provides the ability to zero Z off a point that wasn’t your starting Z when it comes time to change the tool. This is useful if you tend to carve away your material and lose the starting Z or you don’t have limit switches but would like a process similar to a tool length sensor.
1. **Fixed Tool Sensor** (Wizard)<br>This is the most automated setting where all probes and movements are done for you, you only need to intervene by changing the tools. Set up the job and zero normally then expect the machine to move to the sensor location when it reaches a tool change, verify tool length, prompt for a change, probe new tool, then resume cutting. Your machine will need to be homed, have limit switches, and have a tool length sensor (compatible with Carbide 3D bitsetter for example) in order for this option to work. To set up the sensor mount the router/spindle as far down as you might typically put it, with the longest bit mounted in it, then jog it to hover over the tool length sensor with some room to spare and open the tool changing tab to grab that location. This will be the spot your machine moves to every tool change so if it’s too low or your sensor doesn’t work it’ll run into the sensor. You can also enter these coordinates manually, and test them with the Go To button.

   ![](/_images/_gsender/_features/gs_fe_toolchangefixed.jpg){.aligncenter .size-full}

1. **Code**<br>You can enter your own macros before and after the tool change with this strategy selected which is fairly powerful for making tool changing processes that are more automated than just pausing.

   ![](/_images/_gsender/_features/gs_fe_toolchangecode.jpg){.aligncenter .size-medium}

## Workspaces

Usually you would only have one origin or zero position for your project. However, if you plan to do a series of projects that require different zero positions, or are lining up to do some more complex jigging or part batches, you may want to set up multiple workspaces all at once. This can save you time by not having to set a zero position for repetitive tasks or specific jig setups. You can do this by creating up to six different zero positions with the six workspaces in gSender. Access each 'Workspace' at the top right of the program by pressing the drop down to select which workspace to use. gSender will act completely in-line with whatever workspace you've selected, whether you want to set zero, probe, surface, or anything else.

![](/_images/_gsender/_features/gs_fe_dro_workspacesdrop.jpg){.aligncenter .size-medium}

The use of different **Workspaces** is most helpful when the machine is able to home the machine coordinate system. Once homed you can select a workspace and setup your project, and gSender will remember where you set the zero for the new workspace. The challenge then becomes placing the project in the correct spot for each workspace. Often a jig is created, to ensure perfect placement for your workpiece each time. You can use a workspace without homing/sensors, but it's not very repeatable, and you would be resetting them often with each power cycle.

In the image below you can see 4 different workspaces setup, with the zero in the bottom left corner, and the circle in the middle.

![](/_images/_gsender/_features/gs_fe_workspaces.jpg){.aligncenter .size-medium}

**Note:** *Some files may use a toolpath post processor that changes your workspace!*

The video below explains the process in greater detail. If you're coming from a more technical background, you'd usually call these 'workspaces' G54, G55, G56, ... G59.

https://youtu.be/jmiaWA5tiVw?t=336

## Settings

### Transferring Settings

gSender’s settings are stored on a file on whatever computer is used to run it. This mostly includes everything that you’ll find in the settings menu such as units, machine preset, probe, tools, jogging presets, keymapping, tool change g-code, start/stop g-code, and more. If you plan on using a different computer to run your CNC using gSender or want to run gSender remotely, some of these settings might be very important to carry over to the alternate computer to make sure things keep running as expected.

To transfer your settings over:

1. Begin by opening gSender, going to the Config Tab, and clicking the **Export** button in the top right corner of the screen.
  ![](/_images/_gsender/_features/gs_fe_preferences.jpg){.aligncenter .size-medium}
1. Save the file somewhere onto your computer that you can find afterwards
  ![](/_images/_gsender/_features/gs_fe_preferences1.jpg){.aligncenter .size-medium}
1. Outside of gSender, find the file and transfer it using a memory stick or sending it over the internet by emailing to yourself or using Google Drive or OneDrive.
1. Once you’ve got the file onto the other computer it’s now easy enough to open gSender on that computer, or in the web browser if you’re doing remote control, and go to the config tab and click the **Import** button just to the right of the export button.
1. Locate the file and click ‘Open’
  ![](/_images/_gsender/_features/gs_fe_preferences2.jpg){.aligncenter .size-medium}
1. You’ll get a warning. Click ‘Import Settings’ if you want to continue. Once you do, gSender will disconnect and you’ll need to reconnect the machine to resume operation but the settings should now be brought over.
  ![](/_images/_gsender/_features/gs_fe_preferences3.jpg){.aligncenter .size-medium}

## Remote Mode

If you’ve ever wanted to run your CNC without being stuck right next to it, this is the feature you’re looking for. The remote mode is exactly how it sounds, it gives the ability for a remote computer to connect over a shared internet network to a permanently installed, normally lower-end computer, that runs the CNC. This ‘**remote computer**’ can be any device that can connect to the internet and run a web browser, meanwhile the ‘**inline computer**’ plugs into your CNC with a USB cable and will receive commands over the internet from the remote computer.

This feature is handy if you’d like to:

- Load in a file from your design computer outside your shop then run it on your computer inside the shop
- Use a tablet as the primary means of controlling your CNC rather than a mouse and keyboard
- Use a phone for occasional use when jogging or running functions
- Leverage a mini PC or Raspberry Pi as the inline (tethered) computer for cheap, fanless, and reliable operation without taxing them with a display, keyboard, and mouse

Before diving into the setup, here are some quirks and warnings that are important to keep in mind:

- Both systems need to be on the same internet network to work, where the device used to run remote operations needs to be able to run a web browser
- You may need to be an Administrator of the inline computer to make the changes needed so ensure you have that power
- This feature will always be inherently less reliable than a hard-wired connection because of its reliance on your shop’s internet connection for communication. Keep this in mind if you intend on using remote control for more important projects or with expensive tools or materials
- Remote control is still in development so expect to experience some bugs if you’d like to set this up for yourself. The setup process is a little bit more involved on your computer so we don’t advise using this feature if you’re not confident with troubleshooting your own setup
- This feature is NOT intended to enable use of your CNC while AWAY FROM YOUR WORKSHOP. A CNC should always be run while you or another knowledgeable operator is in the vicinity to ensure safe machine operation and be able to react if intervention is required. CNCs can cause fires from electronics, material friction, and can have other safety hazards if not properly monitored
- In other contexts this feature could be thought of as running ‘headless’ but it doesn’t fully meet the requirements of that term. Though remote controlling the CNC from another computer should reduce the requirements of the inline computer, at minimum it still needs to boot the idle version of gSender with a window manager. This is in contrast to a fully ‘headless’ setup where a skinned-down program exists only to pass along information from other devices with no UI to send along information itself

### Enabling Remote Mode

All setup steps need to happen on the inline computer (the computer you’ll have connected via USB to your CNC) and have been simplified to mostly happen within gSender.

1. To begin, click the satellite antenna icon on the top right of the screen. If the icon isn’t there, you’ll need to make sure you have a newer version of gSender that supports this feature.
  ![](/_images/_gsender/_features/gs_fe_remotemode.jpg){.aligncenter .size-medium}
1. This is where remote mode is set up. First you’ll want to click the ‘Enable Remote Mode’ toggle. Second, click the box next to ‘IP’ and select one of the options that gSender tries to recommend for your particular computer network. For an average setup the ‘Port’ value can also be left alone. The third step is to click on OK once you have completed the configuration. **You can also use your camera to scan the QR code, and be taken directly to your remote interface!**
  ![](/_images/_gsender/_features/gs_fe_remotemode1.jpg){.aligncenter .size-full}<br>
If you’re an **advanced user** or have tried the default values without success, you can type in any other IP address or Port that you’d like since the defaults aren’t guaranteed to work. Common port values are 3000, 8000, and 8080 and generally don’t go below 1024 since those are considered privileged. Changing IP addresses can also help if you’re running a VPN or need a different internal IP to external IP mapping.
1. gSender needs to restart in order for the remaining changes to take place.
1. If there was a problem using the specified IP address or Port, you’ll get an error window to let you know. In this case you should be able to reopen gSender, go back to the Remote Mode settings, and try another IP or Port until the setup is successful.
  ![](/_images/_gsender/_features/_remote/gs_fe_re_setup-ip-error.jpg){.aligncenter .size-medium}
1. You’ll know the setup was successful if gSender restarts, the antenna icon is green, and numbers show next to it. As a quick test, click on the numbers to copy them then open a web browser like Chrome or Edge and paste them into the address bar and press enter (you can also type the number manually). After the page loads, you should see a copy of gSender running in the web browser! **If something’s not working**, check you followed the setup steps correctly or reference the firewall or troubleshooting sections below.
  {.aligncenter .size-full}

### Firewall Setup

During initial setup, you might see a Security Alert window pop up or run into an issue where the browser address isn’t working. The most likely issue here is that your inline computer firewall isn’t allowing gSender to communicate to other devices on your network.

**For Windows:** You should simply see a popup from Windows Firewall or your antivirus software asking for approval to allow gSender to communicate on your home network. Please check the box beside “Private networks” and “Public networks”. This should be all that’s needed.

![](/_images/_gsender/_features/_remote/gs_fe_re_firewall-windows.jpg){.aligncenter .size-medium}

**For Mac / Linux / Pi:** If you find that you can’t connect with outside devices or just want some extra safety you might want to try opening the Universal FireWall (UFW) on a given port to allow external access. This can be started with `sudo ufw enable` (if UFW is not found then install it using `sudo apt-get install ufw` and your root password) then opening the desired port, for example `sudo ufw allow 8080` opens port 8080 for external access. If you want to see what ports are already open, you can use `ufw status verbose`.

### Using gSender Remotely

With setup complete, regular use is pretty straightforward:

1. Connect the inline computer to your CNC as you would normally using the USB cable. Turn on power to your CNC and connect to it in gSender as usual.
1. Look for the numbers next to the antenna and write them down including all the symbols and punctuation; these will be used to connect to your CNC on the remote computer / device.
![](/_images/_gsender/_features/_remote/gs_fe_re_setup-done.jpg){.aligncenter .size-full}
1. On any remote device that can run a web browser like Chrome or Edge (computer, phone, tablet) open the browser and type those same numbers you wrote down into the top address bar. In this example the numbers are **192.168.2.203:8000** but yours may be different. Press enter, and hopefully the familiar gSender interface will appear in your browser window. If not, ensure that your remote device is on the same network as your inline computer.
![](/_images/_gsender/_features/_remote/gs_fe_re_use-url.jpg){.aligncenter .size-full}
1. Once connected, you should now be able to control your CNC remotely with most of the same features and functions you’d normally expect:
![](/_images/_gsender/_features/_remote/gs_fe_re_use-connected.jpg){.aligncenter .size-medium}
   - You’ll be able to use both the remote and inline devices simultaneously to control your CNC like jogging, opening and closing files, probing, macros, and more
   - You’ll also see that both their screens look exactly the same so you can watch the visualizer move around or check on the machine state
   - On phones the screen will look different since we’ve optimized it for jogging, setting zeros, and probing
   - When you click to ‘load a file’ you’ll see that you’ll only be able to load files from the device you’re currently on, don’t expect to gain access to the files stored on the opposite device. However once the file is loaded into gSender, you’ll be able to run it from any device
   - There can be multiple remote devices all connected to the same inline computer at the same time to control your CNC from multiple devices. There can also be multiple inline computers controlled from the same remote computer, giving you multi-CNC control from the same device
   - gSender settings like ‘safe height’, ‘start/stop g-code’, ‘tool changing’, and any other gSender specific settings won’t carry over to the remote computer. If you want to make sure files are run the same way every time you’ll need to transfer your gSender settings over by following the ‘Transfer Settings’ instructions below
1. If you’re using your phone, save the unique URL to a bookmark on your home-screen so you can open Remote gSender easily every time! Check out <a href="https://www.YouTube.com/watch?v=UrlDJOY3i-8">this video</a> for details

### Troubleshooting

If you ran into issues during remote control setup, here are some other checks you can make:

1. The easiest checks to make sure remote mode works for you is to make sure you have gSender open, you have gSender connected to your CNC, and you’ve turned remote mode on
1. Double-check your remote mode configuration menu, antenna icon, and IP address are showing on the inline computer
1. Ensure both your computers / devices are on the same internet network and the IP numbers match on both devices
1. Double check you took the right steps in the Firewall Setup section. Your inline computer might be blocking gSender’s ability to send information to the internet because of the firewall. On Windows, follow these steps to modify the firewall:
   - Click Start and open your computer's Control Panel
   ![](/_images/_gsender/_features/_remote/gs_fe_re_issues-control-panel.jpg){.aligncenter .size-medium}
   - Open the ‘System and Security’ settings
   ![](/_images/_gsender/_features/_remote/gs_fe_re_issues-security.jpg){.aligncenter .size-medium}
   - Open the ‘Windows Defender Firewall’ and go to its ‘Advanced settings’
   ![](/_images/_gsender/_features/_remote/gs_fe_re_issues-firewall.jpg){.aligncenter .size-medium}
   - In the column on the left, click on ‘Inbound Rules’ and then find and double-click on ‘gSender’. There might be three options of gSender to click on, you’ll want to click on the version that has the word “All” under the ‘Profile’ column
   ![](/_images/_gsender/_features/_remote/gs_fe_re_issues-inbound-rules.jpg){.aligncenter .size-medium}
   - In the pop-up box, click on the tab labelled ‘Protocols and Ports’. Next to ‘Local port:’ you’ll want to use the drop-down menu to select “Specific Ports” and then type in the default port of “8000”. If you have added a custom port to gSender’s Shortcut properties, you’ll need to type in that number instead. Once you hit ‘Apply’, you can check to see if this resolved your problem.
   ![](/_images/_gsender/_features/_remote/gs_fe_re_issues-port.jpg){.aligncenter .size-medium}
1. If when gSender reopens you’re met with a white screen, this means an error has occurred that we weren’t able to detect. This is rare, but unless we can find some other way to manage this the only fix is to uninstall gSender and reinstall it again.
1. If on the remote device you get a popup for “Server Connection Lost”, this indicates that either gSender on the inline computer was closed or the shared internet is disconnecting. You should be able to fix this by restarting gSender on the inline device, then clicking “Attempt Reconnect” on the remote device.
![](/_images/_gsender/_features/_remote/gs_fe_re_issues-conn-lost.jpg){.aligncenter .size-medium}

## Rotary

gSender has a unique ability to control a rotary axis on normal, 3-axis grbl machines. We call this “rotary mode”; which isn't to be confused with grblHAL machines where gSender by default supports full, 4-axis motion.

The idea is that once you're in this "rotary mode", gSender does the legwork to swap firmware settings over to your rotary setup, translate A-axis movements to your machine as if they were Y-axis movements, and as long as you've done the legwork to align and swap over your wires then your rotary A-axis should now be good to go!

### Rotary Mode

Navigate to the Config tab where you will find the Rotary settings. Here you can **toggle** the Rotary controls to enable them and make them visible on the Carve tab. Don't forget to hit the Apply Settings button!

![](/_images/_gsender/_features/_rotary/gs_fe_ro_enable.jpg){.aligncenter .size-medium}

Once the toggle has been turned to enable, you will see an additional tab at the bottom right of the Carve tab, called Rotary. With this feature you can:

- **Jog Control** - Rotate the A-axis, go to Zero, set Zero, and adjust speeds

![](/_images/_gsender/_features/_rotary/gs_fe_ro_movement.jpg){.aligncenter .size-medium}

- **Rotary Mode** - Toggle into Rotary Mode
- **Rotary Surfacing** - Wizard to turn square stock round
- **Probe Rotary Z-axis** - Automatically probe to find the Z-axis
- **Y-axis Alignment** - Automatically probe to align the Y-axis along the A-axis (Turn rotary mode off to access this feature)
- **Mounting Setup** - Drill holes in your wasteboard to mount our own <a href="https://sienci.com/product/vortex-rotary-axis/">Vortex Rotary</a> track (Turn rotary mode off to access this feature)

![](/_images/_gsender/_features/_rotary/gs_fe_ro_tab.jpg){.aligncenter .size-medium}

<em><b>Note:</b> Before switching to rotary mode, using the jog controls, rotary surfacing, or any other rotary actions, you’ll need to check that you’ve got your rotary set up and positioned correctly. This includes table mounting and Y-axis alignment, outlined below.</em>

### Rotary Mounting Setup

When mounting a rotary axis, it’s important to be parallel to the X-axis, and helpful to have a repeatable position so you can reliably mount and unmount the rotary, depending on when you want to use it. If you have your own rotary axis, this is a step that you'll have to do yourself.

For those who might have our Vortex rotary axis, the '**Rotary Mounting Setup**' button is a specific macro that cuts into the machine wasteboard to help you fasten the rotary with perfect parallel alignment. Check out our <a href="https://resources.sienci.com/view/vx-mounting-your-vortex/#creating-the-mounting-holes">Vortex Resources</a> for more details on how to use this wizard.

While the Y-axis Alignment button helps in the setup of your Vortex Rotary, so does the Rotary Mounting Setup button. This feature has been designed to provide a center line for your rotary track installation. Check out our <a href="https://resources.sienci.com/view/vx-mounting-your-vortex/#creating-the-mounting-holes">Vortex Resources</a> for more details on how this wizard helps you mount your Vortex to your wasteboard.

### Y-axis Alignment

When switching from regular CNC use to Rotary Mode, you will probe to align the Y-axis along the A-axis. You can do this in the Rotary Tab by hitting the Y-axis Alignment button. Check out our <a href="https://resources.sienci.com/view/vx-first-project/#y-axis-alignment">Vortex Resources</a> for more information on aligning your Y-axis when setting up your Vortex.

### Rotary Mode Toggle

This toggle can only happen once you’ve got your rotary axis set up properly, because after switching it’ll assume you’ve changed your motor wiring to be connected to your A-axis instead of your Y-axis. You will see a pop up warning you of the changes that are made, going into rotary mode.

![](/_images/_gsender/_features/_rotary/gs_fe_rotary_enable1.jpg){.aligncenter .size-medium}

Once enabled, you will see a confirmation appear in the bottom right corner.

![](/_images/_gsender/_features/_rotary/gs_fe_rotary_enable2.jpg){.aligncenter .size-medium}

When you enable Rotary Mode, several changes will happen to your tool options:

- The **Y-axis Alignment** and **Rotary Mounting Setup** buttons become grey and hidden. This is because your Y-axis will be locked in its current position at this time, so there is no need to align it, and your rotary should already be set up.
- The **Stock Turning** and **Probe Rotary Z-axis** buttons become available

Several changes will also happen to your controls:

- The **Go to** button for Y-axis and Z-axis is hidden
- The **Zero Y-axis** button is hidden
- It changes the ‘**Go to XYO**’ button to be a ‘**Go to XAO**’ button
- The **Y-axis jogging** buttons are hidden

![](/_images/_gsender/_features/_rotary/gs_fe_ro_jog-changes.jpg){.aligncenter .size-full}

You will also see a reminder that:

- Your Y-axis will be set to Zero
- Your hard limits have automatically been turned off
- Your firmware EEPROM values have been set to new values, better suited to the rotary.

### Rotary Probing

In a similar fashion to regular cnc machining where you set a zero position in relation to the stock you are using, we will do the same when rotary carving. Two differences are that we don’t need to enter a tool diameter and each axis will be set separately.

#### Setting Z-axis

You can set your **Z-axis** to either the rotating axis center, or the surface of your stock in a similar fashion to regular CNCing. We recommend using the axis center, as that allows you to make use of the Vortex’s built in Z-axis probing functionality.

To do this, jog the cutting bit to be hovering approximately ~15mm just above the chuck. **Double check that your probing wires are in place before proceeding!**

![](/_images/_gsender/_features/_rotary/gs_fe_ro_z-position.jpg){.aligncenter .size-medium}

In gSender, select the rotary axis tab, then Click ‘Probe Rotary Z-axis’ and the Z-axis will begin probing automatically, setting the Z-zero point for you. This will need to be done for each tool change in addition to the beginning of each job.

![](/_images/_gsender/_features/_rotary/gs_fe_ro_probez.jpg){.aligncenter .size-full .nar}

#### Setting X & A-axis

Setting both the X-axis and the A-axis are done manually.

- To set your **X-axis**, jog to wherever you’d like the job to start then click ‘Zero X’ to set your X-zero point. Make sure this is far enough from the chuck to ensure there won’t be any collisions with your cutting bit, workholding or screws.
- To set your **A-axis**, simply click ‘Zero A’ at the beginning of each job, under the Rotary Jog Controls. Note that if this isn’t done, the rotary will spin back to zero before the job starts.

### Rotary Surfacing tool

he Rotary Surfacing button will allow you to turn square stock down to a cylinder. We recommend using a **¼ inch upcut end mill** for turning stock, as it's the most efficient.

![](/_images/_gsender/_features/_rotary/gs_fe_ro_surfacing.jpg){.aligncenter .size-full .nar}

Now you will see the Rotary Surfacing Tool. Here you will enter details about your stock length, start and final dimensions. You will also see spots for Bit Diameter, Step over, Spindle RPM, and Feed rate.

![](/_images/_gsender/_features/_rotary/gs_fe_rotary_surface.jpg){.aligncenter .size-full}

Rotary surfacing is similar to the regular XYZ surfacing tool. Let’s explore this a bit further.

1. Your **start diameter** is the largest diameter on your stock. Usually this means the diagonal distance from opposite corners if you’re starting with square or rectangular stock.

![](/_images/_gsender/_features/_surfacerot/gs_fe_sr_diameter-start.jpg){.aligncenter .size-full .nar}

1. Your final diameter is determined by the short side of your stock.

![](/_images/_gsender/_features/_surfacerot/gs_fe_sr_diameter-end.jpg){.aligncenter .size-full .nar}

1. With a starting height of 90mm and a finished height of 63.5mm, we are removing 26.5mm of material. **However**, since we have the Z-axis set at the center of the material, we will need to divide that 26.5mm in half. We are basically taking 13.25mm off of the top and the bottom. If you want a single pass, your step down would be 13.25mm. Dividing that by two and setting the step down to 6.625mm, means that we will be doing two passes. This will produce a piece of round stock with the maximum diameter possible.

<p style="text-align: center;"><b>(Start Height - Finishing Height) / 2 = Total Step down for ONE pass</b></p>

![](/_images/_gsender/_features/_surfacerot/gs_fe_sr_running.gif){.aligncenter .size-medium .nar}

### Rotary Settings

When you click on the setting button and then select the Rotary tab, you will see the firmware configurations. Here you can enter your own settings, reset the default settings and turn Hard Limits on/off.

![](/_images/_gsender/_features/_rotary/gs_fe_ro_settingslimits.jpg){.aligncenter .size-medium}

## About Page

You can find the release notes for the latest version of gSender in the “About” section of the settings.

![](/_images/_gsender/_features/gs_fe_statsabout.jpg){.aligncenter .size-medium}

## More

Check out this livestream if you'd like to see a super deep dive on gSender and all of its features as of 0.6.9. Chris spends a lot of time answering questions live about gSender and how to set up for a project:

https://www.youtube.com/watch?v=454pWYtZgBU

## Community Macros

<b><span class="redText">Disclaimer!</span> These Macros are submitted by our community. They aren't vetted by us and might cause damage to your machine so use them at your own risk!</b> Please review the code and test it before assuming it will work with your machine setup.

[su_spoiler title="<b>SLB Light-Cycling</b>" open="no" style="fancy" icon="chevron" anchor_in_url="yes"]
**Author:** Kevin G.<br>
**Updated:** Apr 15, 2024

**Description:** Currently only supports the SLB. Allows you to cycle the status light between it's three states of 'Automatic', 'All white', and 'Off' so you can change the light output easily.

**Code:**

```js
%nextLight = global.lightState || 0
M356 P0 Q[nextLight % 3]
%global.lightState = Number(nextLight) + 1
```

[/su_spoiler]

### Formatting

If you'd like to add your own macros to this page, [edit the page on GitHub](https://github.com/Sienci-Labs/Resources?tab=readme-ov-file#making-changes) and use the template below for each macro.

[su_spoiler title="<b>Macro Title</b>" open="no" style="fancy" icon="chevron" anchor_in_url="yes"]
**Author:** John D.<br>
**Updated:** Aug 7, 2024

**Description:** Describe the function of the macro, what hardware it's for, and any other details a user may need to configure or steps to run it.

**Code:**

```js
Paste your macro code here.
```

[/su_spoiler]
