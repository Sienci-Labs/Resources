---
title: Additional Features
menu_order: 4
post_status: publish
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
featured_image: _images/_gsender/_features/gs_fe_p1_KeyShort.jpg
---

This page covers all the advanced features of gSender such as shortcuts, macros, workspaces, calibration tools, controlling spindles, lasers, coolant, and more. Remember, you can always quickly navigate the page by clicking the headings in the 'Page Contents'.

## Shortcuts

Starting off as a more advanced gSender user, the first feature you’ll want to leverage is shortcuts. These can allow you to assign gSender or CNC actions to keys and key combinations or even to gamepads and joystick movements. There are 3rd party apps like <a href="https://joytokey.net/en/">JoyToKey</a>, <a href="https://xpadder.com/?lang=english&amp;country=CA">Xpadder</a>, <a href="https://www.comfortsoftware.com/comfort-keys/">Comfort Keys Pro</a> and <a href="https://www.rewasd.com/">reWASD</a> that allow you to do this, but to eliminate needing to download and configure other programs we’ve rolled all the functionality into gSender itself.

Going to the settings gear, then the 'Shortcuts' section, you'll see that shortcuts can come in the form of 'Keyboard Shortcuts' or 'Joystick Shortcuts', all searchable by category. Both options enable you to set up, modify, and enable or disable shortcuts. These will be automatically saved when you close the dialog box and will remain on gSender as long as the program is installed on your computer.

### Keyboard Shortcuts

Either for use on a keyboard, macro pad, or mini Bluetooth keyboard, these are split up into categories so they're easy to locate and modify. There are shortcuts for carving, overrides, jogging, zero setting, probing, macros, visualization, window navigation, and more!

![](/_images/_gsender/_features/_shortcuts/gs_fe_sh_keyboard.jpg){.aligncenter .size-full}

### Common Shortcuts

A great place to start is the Jogging category. In the picture below, see that right now we can jog the **X-axis** by hitting the shift + right or shift + left keys. The **Y-axis** responds to shift + up and shift + down keys and the **Z-axis** uses the shift + pageup and shift + pagedown keys. Being able to look at your CNC, while your hand is on your keyboard is a great way to ensure you are moving in the right direction, without having to look back at your screen to click the mouse on the right button.

![](/_images/_gsender/_features/_shortcuts/gs_fe_sh_keyboard-common.jpg){.aligncenter .size-full}

You can use the preset shortcuts and/or add your own. Click the ‘+’ or the ‘edit’ to the right of each shortcut to bring up a popup window that allows you to add or edit your own key combination (shown in the example below). You can see it’s as easy as pressing the key or key combination once the popup is open. In addition, you’ll be informed if the combination you’ve entered is already used elsewhere and be given the option to overwrite the existing one if you want.

![](/_images/_gsender/_features/_shortcuts/gs_fe_sh_keyboard-add.gif){.aligncenter .size-full}

You can turn on or off individual shortcuts in the **Active** column or enable/disable all shortcuts at the bottom of the window. Some people find this useful since it can turn off the shortcut temporarily without losing the key combination.

![](/_images/_gsender/_features/_shortcuts/gs_fe_sh_keyboard-enable.jpg){.aligncenter .size-full}

### Gamepad Shortcuts

Many users really love this feature since using a controller is convenient (especially for when you're closer to your machine), inexpensive, and makes certain repetitive actions much easier. Common options are Xbox, PlayStation, and other third-party controllers available online.

To start, connect your joystick to your computer and create a new profile using the ‘Add New Joystick Profile’ button. You will be prompted with further instructions on gSender on how to set it up. This profile will allow for shortcut assignment in a very similar manner as keyboard shortcuts, while also remembering your particular joystick. This will enable you to set up multiple profiles if desired.

If you run into difficulty with getting a particular joystick set up in gSender, consider searching for documentation provided by the manufacturer (for example, <a href="https://support.xbox.com/en-CA/help/hardware-network/controller/connect-xbox-wireless-controller-to-pc" target="_blank" rel="noopener">Xbox</a> or <a href="https://www.playstation.com/en-ca/support/hardware/ps4-pair-dualshock-4-wireless-with-pc-or-mac/" target="_blank" rel="noopener">PlayStation</a>). Some joysticks may also require drivers to be downloaded so your computer can read the signals that the joystick sends out.

![](/_images/_gsender/_features/_shortcuts/gs_fe_sh_gamepad-add.png){.aligncenter .size-full}

### Tested Gamepads

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

Having a listed gamepad means you can both be more confident that your hardware will be compatible with gSender, as well as many of the ‘tested gamepads’ will have pre-made shortcut profiles built right in to save you time setting up your own. Find these pre-made ‘profiles’ alongside all the other gamepad settings in the Shortcuts -&gt; Gamepad tab.

### Shortcut Printing

Find yourself forgetting how you’ve configured your keyboard or gamepad profile shortcuts? Hit the ‘Print’ button to generate a simple PDF that you can store on a tablet or print on some paper to keep next to your CNC. This PDF will contain all the shortcuts you’ve created and what actions they’re assigned to.

![](/_images/_gsender/_features/_shortcuts/gs_fe_sh_print.png){.aligncenter .size-full}

## Lightweight Mode

This mode enables gSender to run faster on computers that are less powerful and prone to lagging. ‘Lightweight Mode’ reduces the memory gSender uses by turning off processor-heavy aspects of the visualizer, from reducing detail to disabling it altogether. You can toggle it on or off using the slider positioned at the top right of the visualizer.

![](/_images/_gsender/_features/gs_fe_lightweight-1.png){.aligncenter .size-medium}

If you go to the visualizer settings, you can also customize what features are active in both ‘Regular’ and ‘Lightweight’ modes.

![](/_images/_gsender/_features/gs_fe_lightweight-2.png){.aligncenter .size-medium}

If gSender's visualizer is impacting the performance of your machine but Lightweight mode only helps once the whole visualizer is turned off, this hybrid option could help. Found in the Visualizer settings, the ‘SVG Visualizer’ substitutes the default 3D viewer with a pre-rendered, top-down image of your project, drastically reducing computer strain but still allowing the project to be displayed.

![](/_images/_gsender/_features/gs_fe_lightweight-3.jpg){.aligncenter .size-full}

Once you toggle on ‘Enable SVG Visualizer’, whenever you turn on Lightweight Mode in the top right of the visualizer, you’ll see the alternate view with all animations turned off.

![](/_images/_gsender/_features/gs_fe_lightweight-4.png){.aligncenter .size-full}

## Touch Plate Setup

gSender has support for three types of touch plates:

1. The Standard Block design
1. Z Probe, also sometimes referred to as a ‘puck’
1. And our specialized AutoZero touch plate

For a Z Probe, setting up is simple since you just need the thickness of the ‘puck’. Enter that value into gSender’s ‘Probe’ settings under ‘Z Thickness’ and you should be good to go!

If you’re trying to set up a custom ‘standard block’ plate, use some calipers to pick up on the measurements noted below. Once these are noted down, enter these into gSender’s ‘Probe’ settings in similarly named entries, and now you should find that gSender’s probing routine has been altered to fit the shape of your touch plate.

![](/_images/_gsender/_features/_probing/gs_fe_pr_dimensions.png){.aligncenter .size-medium}

## Coolant Control / IOT Relay

If you have a coolant control pin on your CNC machine, gSender has a tab for manually controlling it. Under the 'Coolant' tab on the main screen, you can find the 'Mist' and 'Flood' buttons to activate the different modes of coolant use, as well as an indicator for whether the coolant function is active or inactive. This indicator also functions during job sending. You can turn off both coolant pins by pressing the 'Off' button.

Many hobby CNCers don't have a need for coolant and so prefer to use these outputs for controlling other periphery. The most common is an IOT relay that can be used to automatically control a vacuum for dust collection, the CNC's router, LED lighting, and more. See an example of how to set that up here: <a href="https://resources.sienci.com/view/lm-iot-relay/" target="_blank" rel="noopener">https://resources.sienci.com/view/lm-iot-relay/</a>

![](/_images/_gsender/_features/gs_fe_coolant-run.png){.aligncenter .size-medium}

## Spindle &amp; Laser Support

Similar to the manual coolant control, this area is for manual control of a spindle or laser outside of g-code sending. If you have a spindle or laser, you can activate these controls by going to the settings gear at the far right. In the ‘Spindle/Laser’ section in the left toolbar, press the toggle for ‘Spindle/Laser’.

![](/_images/_gsender/_features/_spinlaser/gs_fe_sp_setting.jpg){.aligncenter .size-medium}

Back at the main screen, you'll see the ‘Spindle/Laser’ tab at the bottom right. Here you can click to toggle between 'Spindle Mode' and 'Laser Mode', changing your grbl settings for you and displaying buttons specific to each device. For each mode there is also a red caution circle that indicates whether the spindle or laser is active. This works during manual control but also during job sending.

In spindle mode you can set the spindle speed with a slider, spin it up in either direction, and stop it again with the 'Stop' button. These are all based on g-code commands that can also be entered into the console manually if desired. The speed slider is set from your grbl firmware settings, so max and min speed can be altered in the Firmware Tool.

![](/_images/_gsender/_features/_spinlaser/gs_fe_sp_spindle-on.png){.aligncenter .size-medium}

'Laser Mode' is very similar, allowing for On/Off control, a slider for setting the laser power during manual control, and a ‘Laser Test’ button. The laser testing function is handy when troubleshooting your laser setup or for other sorts of locating and alignment because it only enables the laser for a short time before turning it back off again. Though this is much safer than regular on/off control, we still highly advise that you have you have a hand on a kill switch or E-stop during testing or control of either Laser or Spindle modes so that in case something goes wrong with your computer or the program they can still be safely deactivated.

![](/_images/_gsender/_features/_spinlaser/gs_fe_sp_laser-on.png){.aligncenter .size-medium}

### Laser Diode Support

Some accessories can be really handy to add to a CNC router like a laser diode, drag knife, or pen plotter. These would all perform better on a faster, dedicated machine, but for occasional use why not use the existing motion system of the router to do other things for you? A laser diode in particular can be great because you can clamp the material to carve and then laser engrave afterwards and know that everything is still aligned.

Since many CNCs are coming with diode accessories, gSender has some unique features to also support lasers. Once 'Laser Mode' is turned on, gSender will:

- Automatically apply an offset from the router/spindle to the laser so all your g-code files stay aligned (configured in the Spindle/Laser settings, or with Firmware settings $741 and 742 on the SLB)
- Turn on the laser at low power when running a job outline (enabled in the Spindle/Laser settings). This will help you to better see where your project is going to be located on the material
- Switch to a specialized visualization designed to show raster engraving images better than typical g-code visualizers. Seeing the laser intensity in the movements is very useful to get a better idea of what your projects are going to look like when they’re run. This will only apply to files loaded after ‘Laser mode’ is enabled and the colour can be customized in the settings

![](/_images/_gsender/_features/_spinlaser/gs_fe_sp_laser-vis.png){.aligncenter .size-medium}

## Macros

Macros are standalone buttons within the gSender interface that allow you to execute a series of g-code commands when they're run. Macros can come in handy for a variety of uses:

- Button to run a v-carve or laser engraving of a common insignia into the back of your wood pieces
- Perform a specialized probing function for a particular jig you've set up
- Apply a predetermined offset that allows you to easily array your cutting jobs

You can create macros using the ‘+’ button under the ‘Macros’ tab. Here you'll see a space for inputting your custom g-code and adding a name and description for the macro. Advanced users may also want to leverage ‘Macro Variables’ which allow for greater g-code manipulation and pseudo-programming. Press ‘Add New Macro’ when completed.

![](/_images/_gsender/_features/gs_fe_macro-variable.png){.aligncenter .size-full}

New macros will appear as buttons in the ‘Macro’ tab that can be rearranged by dragging them around. These buttons will display the macro name, show the description if you hover your mouse over them, and can always be later altered or deleted by clicking on their '...' button.

Any macro can be executed by pressing it. Before pressing it, a play icon will appear to show that you can select it. Once running, you should see the macro start to pulse green while a toast notification on the bottom left hand side of gSender also notifies you that it's running.

![](/_images/_gsender/_features/gs_fe_macro-run.png){.aligncenter .size-medium}

Macros can also be executed using shortcuts. Every time you create a new macro it'll become available at the bottom of the shortcuts list for you to assign a key or joystick button to. Add your keybindings and enable them by pressing the slider beside the label.

You can share macros with other users or transfer them between computers by using the import and export features. To import one or multiple macros, just press the button with the downward arrow and a browsing window will appear so that you can select the macros you wish to import. Similarly, to export all your current macros, press the button with the upward arrow and it'll generate a save file for you.

![](/_images/_gsender/_features/gs_fe_macro-share.png){.aligncenter .size-full}

### Advanced Macros

gSenders Macro architecture is based on **JavaScript** and uses the Esprima library (<a href="https://esprima.org/" target="_blank" rel="noopener">https://esprima.org/</a>) and so will theoretically support any code that it does. This is exciting because Macros can move far past basic variables if you’d like to perform advanced functions on your CNC:

If you want some initial inspiration, see other macros **made by our community** or ones <a href="https://github.com/cncjs/CNCjs-Macros/blob/master/Hole_Center" target="_blank" rel="noopener"><b>made for CNCjs</b></a> (another g-code sender) which should also work in gSender. Otherwise, here are some other points of guidance:

1. You'll want to develop your understanding of typical <a href="https://linuxcnc.org/docs/html/gcode/g-code.html" target="_blank" rel="noopener">g-codes</a> and <a href="https://linuxcnc.org/docs/devel/html/gcode/m-code.html" target="_blank" rel="noopener">m-codes</a> that are used for CNC control (the pages linked are very good sources for that)
1. The "Macro Variables" dropdown in gSender shows many of the most commonly used operations when making your own macro
1. Make your own variable with `%variable = value_you_want_to_set` (ex. % probeSpeed = 150)
1. Use your variable in g-code, like `G0 G91 G21 X[variable]` (moves the X-axis by the amount set in the variable)
1. Test your code by printing it to the console `([variable])`
1. Make dialog boxes appear on the screen to confirm a value or position by putting in an M0 line with a comment, for example `M0 ;Remember to turn on your router before the next step` which will pause the macro and give you the option to 'continue' or 'cancel'
1. Start experimenting with basic math using numbers and variables
1. Use global variables `global.variable` if you want variables that you can use in other macros (note that these get reset once gSender is closed)
1. Read up on all the other Math features available like <a href="https://developer.mozilla.org/en-US/docs/Web/JavaScript/Reference/Global_Objects/Math" target="_blank" rel="noopener">absolute value, rounding, and trigonometry</a> (become very useful for more advanced probing cycles for example)
1. Start to add more logic to your code using ternary expressions to choose between two outcomes (e.g. `%variable = (30 &gt; 20) ? 10 : 20` which is checking if 30 is bigger than 20, and if it is it'll make the variable = 10, otherwise it'll make the variable = 20).
1. Here's an example of a more advanced macro, made by gSenders Lead Developer, which shows off much of the guidance given above. This macro was made for our new <a href="https://sienci.com/product/slb/" target="_blank" rel="noopener">SLB control board</a> in order to cycle between its 3 <a href="https://resources.sienci.com/view/slb-manual/#status-lights" target="_blank" rel="noopener">status light states</a>.
   - The macro is only 3 lines.  First it checks what the current light state is and sets it to 0 if it doesn't have a state. Next, it sets the lights to the current state but applies a modulus of 3 since we can only have a state value of 0, 1, or 2 so we'll get an error if the value is 3 or above. Lastly, it adds +1 to the state so that if the macro is run again it'll put the lights into a new state.
   - `%nextLight = global.lightState || 0`
   - `M356 P0 Q[nextLight % 3]`
   - `%global.lightState = Number(nextLight) + 1`
1. Read more about the Esprima library here: <a href="https://docs.esprima.org/en/latest/syntactic-analysis.html" target="_blank" rel="noopener">https://docs.esprima.org/en/latest/syntactic-analysis.html</a>

## Console

The console is a tab that you can access at the bottom right hand side of the gSender window. The text here shows a truer representation of the communication that happens between your computer and your CNC. As you start to understand more about your machine, this is a great tab to reference so you can see if commands are being properly sent, received, and executed. It's also great for troubleshooting since you can:

- Manually send g-code commands to your CNC
- Check for errors or alarms and the g-code that caused them (normally the line that comes before)
- Copy text straight from the console to send in an email for help by clicking the icon beside the "Run" button

![](/_images/_gsender/_features/gs_fe_console.jpg){.aligncenter .size-full}

When you first start up gSender, the console will display EEPROM settings that are sent from the Arduino in the control box. These EEPROM settings control parameters for your CNC such as:

- Maximum speed and acceleration in each axis
- Boundaries of the work area
- Direction of each axis movement
- Limit switch settings

To access EEPROM settings again, enter in “$$” into the console and hit the 'Enter' key or click the 'Run' button. These settings can be changed via the console as well as the Firmware Tool which we've designed as a much more visual way to alter machine settings.

## Calibrate Tool

The 'Calibration Tool' on gSender enables you to make finer adjustments to your machine for improved performance. There are three processes available on gSender:

- Diagnostics
- XY Squaring
- Movement Tuning
- Surfacing Wasteboard

![](/_images/_gsender/_features/_calibrate/gs_fe_ca_tool.png){.aligncenter .size-full}

### Diagnostics

If you’d like to see general information about your CNC or are experiencing issues that you’d like to troubleshoot, gSender has a Diagnostics tool for that. Access it by clicking the ‘Calibrate’ tool on the top-right and opening the ‘Diagnostics’ tab.

Here you'll see machine information, notable firmware settings, and at-a-glance status on whether your limit switches, touch probe, or other pins are activated. This can be handy if you’re encountering odd behaviour with certain machine accessories or to double-check your wiring.

![](/_images/_gsender/_issues/gs_is_diagnostic-file.png){.aligncenter .size-full}

Another valuable feature is the ability to download a Diagnostic PDF file of your CNC machine when you click ‘Download Now!’. This PDF file is meant to include information on your computer, your CNC, recent alarms / errors, any currently loaded g-code file, and more. It's basically a treasure trove of information that you can share on community forums, Facebook groups, or with your CNC customer support. This can go a long way towards getting help from others on diagnosing any problems your CNC might be experiencing.

To download the PDF, click the “**Download Now!**” button. This will open a save dialog box. Save the file to a location that you can easily access to send along to others in an email, support ticket or post online.

Lastly, you can copy the last 40 lines of code in the gSender console (1), by hitting the double page icon to the left of the Run button (2). This will copy the code to your clipboard, so you can paste it to forums or share it with support teams.

![](/_images/_gsender/_features/gs_fe_console-copy.png){.aligncenter .size-full}

### XY Squaring

When mounting your LongMill on the table, there is a basic squaring process illustrated in our instructions (<a href="https://resources.sienci.com/view/lm-table-mounting/">https://resources.sienci.com/view/lm-table-mounting/</a>). If you do find that the machine is not perfectly square, you can follow the steps in this process to fine tune the position of your rails.

When you access the ‘Calibration Tool’ window, the ‘XY Squaring’ procedure is shown on the first tab. All instructions are illustrated in the window, however a brief overview will be provided.

![](/_images/_gsender/_features/_calibrate/gs_fe_ca_square-xy-1.png){.aligncenter .size-medium}

You will need the following:

- Ruler or measuring tape
- Tapered bit or V-bit
- Tape

1. Jog the machine to the front left corner, with the bit raised slightly over the surface of your wasteboard
1. Mark the points with tape and move the machine as directed
![](/_images/_gsender/_features/_calibrate/gs_fe_ca_square-xy-2.png){.aligncenter .size-medium}
1. Measure the distance between the marked points and record the values
![](/_images/_gsender/_features/_calibrate/gs_fe_ca_square-xy-3.png){.aligncenter .size-medium}
1. Adjust your rail positions with the values determined by the XY Squaring procedure
![](/_images/_gsender/_features/_calibrate/gs_fe_ca_square-xy-result.png){.aligncenter .size-medium}

The great advantage to this tool is it saves you having to do the trigonometry yourself and will also let you know if your machine is aligned closely enough that it’s not worth worrying about.

### Movement Tuning

You are able to change how much your motors turn to improve the accuracy of your machine movement. This is done through modifying the EEPROM settings that are stored on your LongMill, which this process will guide you through. You can tune the X, Y and Z axes individually. All instructions are illustrated in the 'Calibration Tool', however a brief overview will be provided.

You will need:

- Marker or tape
- Measuring tape

1. Jog your machine to the middle of whichever axes you choose to tune, so that there is enough room to complete this procedure. For example, on the X-axis you would jog halfway on the X-axis rail
1. Select what axis to tune on the drop down menu
![](/_images/_gsender/_features/_calibrate/gs_fe_ca_tune-1.png){.aligncenter .size-medium}
1. Mark down the location of your reference on the machine. For example the X-axis tuning references the edge of the XZ gantry on the X rail
1. Move the axis a chosen distance
1. Measure the travel distance between the marked location and the reference edge
![](/_images/_gsender/_features/_calibrate/gs_fe_ca_tune-2.png){.aligncenter .size-medium}
1. Change the EEPROM setting as recommended by the procedure by pressing 'Set EEPROM setting'
![](/_images/_gsender/_features/_calibrate/gs_fe_ca_tune-result.png){.aligncenter .size-medium}
1. Repeat the procedure for each axis you wish to tune

### Surfacing

https://youtu.be/jfInIEOB3kU

Surfacing the wasteboard of your machine can easily be done right inside gSender! The first thing you’ll want to do is decide where you want to start surfacing and in most cases the front, left of the machine is the most convenient. You might also want to remove any accessories that might get in the way of your machine travelling around during surfacing as well as have a good vacuum on hand because surfacing can get really messy. You can find the Surfacing Tool under the Calibrate tab, or under the Surfacing tab.

![](/_images/_gsender/_features/_surface/gs_fe_su_open.png){.aligncenter .size-full}

1. Start by entering the settings you’d like to use to generate your surfacing job:
   - **X &amp; Y**: decides the cutting size (width and depth) you want to surface. If you’re surfacing your wasteboard, use the manufacturer’s spec on max machine travel or manually jog to the limits to cover the full cutting area, or if you’re surfacing a piece of material then you can use a measuring tape.<br>- **LongMill MK2**: 818mm (32.2”) or 1278 (50.3”) x 366mm (14.4”) or 866 (34.1”)<br>(if using limit switches, remove about 8mm/0.3” in X and 11mm/0.43” in Y)<br>- **LongMill MK1**: 320mm (12.6”) or 805 (31.7”) x 344mm (13.54”) or 844 (33.23”)<br>(if using limit switches, remove about 35mm/1.38” in X and 24mm/0.94” in Y)<br>(if using magnetic dust shoe, remove about 34mm/1.34” in X)<br>- **Mill One**: 235mm (9.25”) or 257 (10.1”) x 185mm (7.28”)
   - **Cut Depth &amp; Max**: describes how deep you want to cut per pass and the total depth you want to cut down. For larger surfacing bits usually you should keep cut depth below 1mm, max depth should be increased to a couple millimeters if you think your material is very warped.
   - **Bit** (typically 6 - 25mm): make sure you have the right bit for the job like a surfacing tool or a large, flat end mill since this will give you a better surface finish.
   - **Spindle RPM** (default 1700): only applies if you have an automatic speed control, otherwise set this manually on your router.
   - **Feed rate** (default 2500mm/min): influenced by the RPM, step over, bit diameter, and cut depth. Luckily if you set it incorrectly you’ll be able to override it during the job since surfacing can cause burning when cutting too slow or can have worse surface finish when cutting too fast.
   - **Step over** (default 40%): sticking around 40% tends to be a good balance between speed (using a higher %) and better surface finish (using a lower %).
![](/_images/_gsender/_features/_surface/gs_fe_su_settings.png){.aligncenter .size-full}
1. Select a Start Position of any four corners or the center by clicking the dot; this is where the surfacing will begin. You can also select a surfacing pattern of spiral or zig-zag. The spiral will only cut from the inside-out if the start position is the centre. If you toggle the flip cut direction, the spiral will cut conventional instead of climb, and the zig-zag pattern will cut vertically instead of horizontally.
![](/_images/_gsender/_features/_surface/gs_fe_su_position.png){.aligncenter .size-full}
1. Press ‘Generate G-code’ and check your surfacing tool path using the ‘Visualizer Preview’ tab. You can also see the raw g-code using the ‘G-code Viewer’ tab and can copy and save it to a g-code file if you’d like to use it again later.
![](/_images/_gsender/_features/_surface/gs_fe_su_generate.png){.aligncenter .size-full}
1. Press ‘Run on Main Visualizer’ to bring the g-code into gSender’s main screen. Make sure that you jog to the starting point and set your zero in the right place before starting the job. You can also press the ‘Outline’ button as an easy way to check that you’ll be surfacing where you expect and if you find the dimensions aren’t correct you can always re-open the surfacing tool, tweak the size, and try again. Feel free to start the job whenever you’re ready!
![](/_images/_gsender/_features/_surface/gs_fe_su_result.png){.aligncenter .size-medium}

Did you know that surfacing can be used for more than your wasteboard? It’s great for creating a perfectly flat surface of your starting materials, just like a jointer or surface planer would. You can also use the <a href="https://docs.google.com/document/d/1yUO8bMAw5XoRO8AWGc3ZB5_WVj12ARP-kvf5pciUNL0/edit#heading=h.r1c788pgn92b">Rotary Surfacing</a> tool if you are wanting round stock.

## Stats Page

Curious to know how many jobs you’ve completed or how many hours you’ve put on your machine? Find this information in the “Stats” section of the settings. For now it provides a simplified breakdown of total hours run, longest and average runtime, total jobs run, and compares completed vs cancelled jobs. It’s a useful tool for tracking maintenance schedules and will continue to be expanded into the future.

![](/_images/_gsender/_features/gs_fe_stats.jpg){.aligncenter .size-medium}

## Firmware Tool

Any board you have will come pre-installed with CNC firmware, along with the custom EEPROM settings for that machine, so typically you won’t need to access the ‘Firmware’ tool. If you choose to use this tool, it can give you access to many of your machines "behind-the-scenes" settings for tweaking or modding your setup. Open it by clicking the ‘Firmware’ tool at the top of the screen.

### Unsupported CNCs

If your CNC isn't listed below, then it's considered "unsupported":

- Sienci Labs **LongMill** (MK1, MK2, and MK2.5), **AltMill**, and **Mill One** (V1, V2, and V3)
- Don't see your machine on this list and want it fully supported? Let your manufacturer know to get in contact with us so that we can add their machine profiles to gSender :)

If your machine is unsupported, it means that the Firmware Tool won't be able to perform the same features as for supported machines. In this case, **if your machine isn't working, contact your manufacturer to get their advice on how to fix it**. Using this tool makes it possible to ruin your machine further and we won't be able to help you with your specific hardware. For unsupported machines:

1. Choosing your machine **name** from the drop down menu is primarily cosmetic
1. **Flash** either vanilla grbl, or for grblHAL boards upload a hex file to flash a new firmware
1. **Import** EEPROM settings from a file if you had settings that were working and something changed
1. **Export** current EEPROM settings if you'd like to save your current setup in case something goes wrong
1. **Restore** all your machine settings back to typical vanilla grbl values
1. And otherwise see and modify any machine settings as well as search any keywords to help you find what you're looking for

![](/_images/_gsender/_features/gs_fe_firmware.jpg){.aligncenter .size-full}

### Supported CNCs

If your CNC was listed above then it's "supported" by the Firmware tool. This means that the manufacturer is working with us to keep their machine profiles up-to-date, which in-turn gives you access to more features:

1. Choose your machine **name** from the drop down menu
1. **Flash** either your specific machines grbl firmware, or for grblHAL boards upload a hex file to flash a new firmware
1. **Import** EEPROM settings from a file if you had settings that were working and something changed
1. **Export** current EEPROM settings if you'd like to save your current setup in case something goes wrong
1. **Restore** all your machine settings back to the defaults for your profile in case they've somehow been altered or wiped (like a "factory reset")
1. Also be able to see a **yellow highlight** and be able to reset individual settings that have been changed from the machine defaults
1. And otherwise see and modify any machine settings as well as search any keywords to help you find what you're looking for

![](/_images/_gsender/_features/gs_fe_firmware.jpg){.aligncenter .size-full}

## Start/Stop G-code

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

![](/_images/_gsender/_features/gs_fe_events.jpg){.aligncenter .size-full}

## Tool Changing

For CNC machines, tool changes are pauses that are programmed in the g-code for a user to switch out the cutting tool for a different one, thus allowing for multiple toolpaths (cutting operations) within one g-code file. The g-code for tool changing is an M6 command, in which the program will pause until the user tells it to continue, usually through a 'Resume' and/or 'Confirm Tool Change' button on the machine interface program. On gSender, you can program what happens when there is M6 in your g-code.

The tool change options are in the Settings -&gt; Tool Change menu. You can select from one of 5 different options.

![](/_images/_gsender/_features/gs_fe_tool-change-strat.png){.aligncenter .size-full}

You can **Ignore** any M6 tool change commands, **Pause** the job when a tool change is recognized, or select one of the last three **Wizards** that will guide you through pre-set tool changing methods. In the split image below, you can see an example of the job **Pause** on the left side and the **Wizard** on the right.

![](/_images/_gsender/_features/gs_fe_tool-change-prompt.jpg){.aligncenter .size-full}

If you are using one of the wizard options, know that you can access all other gSender controls while the wizard is open like jogging and zeroing. It also has flexibility to go back a step if you missed something or had a mistake, or to be minimized temporarily if you want to check the visualizer.

1. **Ignore**<br>This simply ignores any M6 commands in the g-code file. This is the default option since it’s perfect for beginners that only make projects with one tool or those that create separate files for each tool and prefer to manually perform tool changes between files.
1. **Pause**<br>Pauses gSender at the tool change point, as if you had hit the pause button manually. This gives you freedom to jog, zero, or anything else you’d like, and is great for those that are running multi-tool files but want to use a different process than the Wizards provide. This could be a manual probing process, a different tool changing approach, or running custom macros to support your machines specific hardware. gSender is compatible with tool length sensors like the Carbide 3D bitsetter, and our community has compiled a <a href="https://forum.sienci.com/t/bitsetter-and-other-tool-length-sensors-supported-in-gSender/3877/4">list of macros</a> for tool changing that you can use when you are paused. Just note that pausing can’t always guarantee keeping track of your movements and actions when it comes time to resume the job so try to ensure you get back to the starting point and set zeros correctly.
1. **Standard Re-zero** (Wizard)<br>Titled ‘standard’ because it’s exactly the same as the standard process you might normally follow for running a file, changing the tool, re-zeroing Z, then running the next file except it’s applied to a single file with multiple toolpaths. Since the process is so familiar, this is a great way to dip your toes into tool changing within one file. Compatible with using a touch plate or the paper method, zero out at a predetermined spot (usually at the front left corner), and use jogging to move around. The advantage of introducing this extra automation and guidance during tool changes is that you don’t have to worry about custom macros and it reminds you of simple steps like turning the router back on or zeroing Z.
1. **Flexible Re-zero** (Wizard)<br>Similar to the ‘standard’ wizard with similar steps and manual movements but provides the ability to zero Z off a point that wasn’t your starting Z when it comes time to change the tool. This is useful if you tend to carve away your material and lose the starting Z or you don’t have limit switches but would like a process similar to a tool length sensor.
1. **Fixed Tool Sensor** (Wizard)<br>This is the most automated setting where all probes and movements are done for you, you only need to intervene by changing the tools. Set up the job and zero normally then expect the machine to move to the sensor location when it reaches a tool change, verify tool length, prompt for a change, probe new tool, then resume cutting. Your machine will need to be homed, have limit switches, and have a tool length sensor (compatible with Carbide 3D bitsetter for example) in order for this option to work. To set up the sensor mount the router/spindle as far down as you might typically put it, with the longest bit mounted in it, then jog it to hover over the tool length sensor with some room to spare and open the settings menu to save that location. This will be the spot your machine moves to every tool change so if it’s too low or your sensor doesn’t work it’ll run into the sensor.

![](/_images/_gsender/_features/gs_fe_tool-change-tls.png){.aligncenter .size-full}

## Workspaces

Usually you would only have one origin or zero position for your project, therefore gSender will only save one zero. However, if you plan to do a series of projects that require different zero positions, or are lining up to do some more complex jigging or part batches, you may want to set up multiple workspaces all at once. This can save you time by not having to set a zero position for repetitive tasks or specific jig setups. You can do this by creating up to six different zero positions with the six workspaces in gSender. Access each 'Workspace' at the top right of the program by pressing the drop down to select which workspace to use. gSender will act completely in-line with whatever workspace you've selected, whether you want to set zero, probe, surface, or anything else.

![](/_images/_gsender/_features/gs_fe_workspace.png){.aligncenter .size-medium}

The video below explains the process in greater detail.

https://youtu.be/jmiaWA5tiVw?t=336

## Settings

### Transferring Settings

gSender’s settings are stored on a file on whatever computer is used to run it. This mostly includes everything that you’ll find in the settings menu such as units, machine preset, probe, tools, jogging presets, keymapping, tool change g-code, start/stop g-code, and more. If you plan on using a different computer to run your CNC using gSender or want to run gSender remotely, some of these settings might be very important to carry over to the alternate computer to make sure things keep running as expected.

To transfer your settings over:

1. Begin by opening gSender, going to the settings gear in the top-right corner, and clicking the ‘Export Settings’ button in the ‘General’ tab
![](/_images/_gsender/_features/gs_fe_settings-transfer-1.png){.aligncenter .size-medium}
1. Save the file somewhere onto your computer that you can find afterwards
![](/_images/_gsender/_features/gs_fe_settings-transfer-2.jpg){.aligncenter .size-medium}
1. Outside of gSender, find the file and transfer it using a memory stick or sending it over the internet by emailing to yourself or using Google Drive or OneDrive.
1. Once you’ve got the file onto the other computer it’s now easy enough to open gSender on that computer, or in the web browser if you’re doing remote control, and go to the settings and click the ‘Import Settings’ button in the ‘General’ tab.
![](/_images/_gsender/_features/gs_fe_settings-transfer-3.png){.aligncenter .size-medium}
1. Locate the file and click ‘Open’
![](/_images/_gsender/_features/gs_fe_settings-transfer-4.jpg){.aligncenter .size-medium}
1. You’ll get a warning. Click ‘Import Settings’ if you want to continue. Once you do, gSender will disconnect and you’ll need to reconnect the machine to resume operation but the settings should now be brought over.
![](/_images/_gsender/_features/gs_fe_settings-transfer-5.jpg){.aligncenter .size-medium}

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
![](/_images/_gsender/_features/_remote/gs_fe_re_setup-.jpg){.aligncenter .size-full}
1. This is where remote mode is set up. First you’ll want to click the ‘Enable Remote Mode’ toggle. Second, click the box next to ‘IP’ and select one of the options that gSender tries to recommend for your particular computer network. For an average setup the ‘Port’ value can also be left alone. The third step is to click on OK once you have completed the configuration.
![](/_images/_gsender/_features/_remote/gs_fe_re_setup-config.jpg){.aligncenter .size-full}
If you’re an **advanced user** or have tried the default values without success, you can type in any other IP address or Port that you’d like since the defaults aren’t guaranteed to work. Common port values are 3000, 8000, and 8080 and generally don’t go below 1024 since those are considered privileged. Changing IP addresses can also help if you’re running a VPN or need a different internal IP to external IP mapping.
1. gSender needs to restart in order for the remaining changes to take place. You can choose to restart immediately or wait until later.
![](/_images/_gsender/_features/_remote/gs_fe_re_setup-restart.jpg){.aligncenter .size-medium}
1. If there was a problem using the specified IP address or Port, you’ll get an error window to let you know. In this case you should be able to reopen gSender, go back to the Remote Mode settings, and try another IP or Port until the setup is successful.
![](/_images/_gsender/_features/_remote/gs_fe_re_setup-ip-error.jpg){.aligncenter .size-medium}
1. You’ll know the setup was successful if gSender restarts, the antenna icon is green, and numbers show next to it. As a quick test, click on the numbers to copy them then open a web browser like Chrome or Edge and paste them into the address bar and press enter (you can also type the number manually). After the page loads, you should see a copy of gSender running in the web browser! **If something’s not working**, check you followed the setup steps correctly or reference the firewall or troubleshooting sections below.
![](/_images/_gsender/_features/_remote/gs_fe_re_setup-done.jpg){.aligncenter .size-full}

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
1. If you’re using your phone, save the unique URL to a bookmark on your home-screen so you can open Remote gSender easily every time! Check out <a href="https://www.youtube.com/watch?v=UrlDJOY3i-8">this video</a> for details

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

## About Page

You can find the release notes for the latest version of gSender in the “About” section of the settings.

![](/_images/_gsender/_features/gs_fe_about.png){.aligncenter .size-medium}

## More

Check out this livestream if you'd like to see a super deep dive on gSender and all of its features as of 0.6.9. Chris spends a lot of time answering questions live about gSender and how to set up for a project:

https://www.youtube.com/watch?v=454pWYtZgBU
