---
title: ytsb Additional Features
menu_order: 4
post_status: draft
post_excerpt: Learn the advanced features of gSender such as shortcuts, macros, workspaces, calibration tools, controlling spindles, lasers, coolant, and more.
post_date: 2021-07-01 15:50
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
This page covers all the advanced features of gSender such as shortcuts, macros, workspaces, calibration tools, controlling spindles, lasers, coolant, and more. Remember, you can always quickly navigate the page by clicking the headings in the 'Page Contents'.

<h2>Shortcuts</h2>

Starting off as a more advanced gSender user, the first feature you’ll want to leverage is shortcuts. These can allow you to assign gSender or CNC actions to keys and key combinations or even to gamepads and joystick movements. There are 3rd party apps like <a href="https://joytokey.net/en/">JoyToKey</a>, <a href="https://xpadder.com/?lang=english&amp;country=CA">Xpadder</a>, <a href="https://www.comfortsoftware.com/comfort-keys/">Comfort Keys Pro</a> and <a href="https://www.rewasd.com/">reWASD</a> that allow you to do this, but to eliminate needing to download and configure other programs we’ve rolled all the functionality into gSender itself.

Going to the settings gear, then the 'Shortcuts' section, you'll see that shortcuts can come in the form of 'Keyboard Shortcuts' or 'Joystick Shortcuts', all searchable by category. Both options enable you to set up, modify, and enable or disable shortcuts. These will be automatically saved when you close the dialog box and will remain on gSender as long as the program is installed on your computer.

<h3>Keyboard Shortcuts</h3>

Either for use on a keyboard, macro pad, or mini Bluetooth keyboard, these are split up into categories so they're easy to locate and modify. There are shortcuts for carving, overrides, jogging, zero setting, probing, macros, visualization, window navigation, and more!

<img class="aligncenter wp-image-5219" src="https://resources.sienci.com/wp-content/uploads/2021/07/2023-06-13_10-43-42-850x573.jpg" alt="" width="749" height="505" />{.aligncenter .size-medium}

<h3>Common Shortcuts</h3>

A great place to start is the Jogging category. In the picture below, see that right now we can jog the <strong>X axis</strong> by hitting the shift + right or shift + left keys. The <strong>Y axis</strong> responds to shift + up and shift + down keys and the <strong>Z axis</strong> uses the shift + pageup and shift + pagedown keys. Being able to look at your CNC, while your hand is on your keyboard is a great way to ensure you are moving in the right direction, without having to look back at your screen to click the mouse on the right button.

<img class="aligncenter wp-image-5221" src="https://resources.sienci.com/wp-content/uploads/2021/07/2023-06-13_11-01-55-850x566.jpg" alt="" width="746" height="497" />{.aligncenter .size-medium}

You can use the preset shortcuts and/or add your own. Click the ‘+’ or the ‘edit’ to the right of each shortcut to bring up a popup window that allows you to add or edit your own key combination (shown in the example below). You can see it’s as easy as pressing the key or key combination once the popup is open. In addition, you’ll be informed if the combination you’ve entered is already used elsewhere and be given the option to overwrite the existing one if you want.

<img class="aligncenter wp-image-5220 " src="https://resources.sienci.com/wp-content/uploads/2021/07/2023-06-09_15-53-35.gif" alt="" width="747" height="461" />{.aligncenter .size-medium}

You can turn on or off individual shortcuts in the <strong>Active</strong> column or enable/disable all shortcuts at the bottom of the window. Some people find this useful since it can turn off the shortcut temporarily without losing the key combination.

<img class="aligncenter wp-image-5222" src="https://resources.sienci.com/wp-content/uploads/2021/07/2023-06-13_11-06-44-1024x687.jpg" alt="" width="752" height="505" />{.aligncenter .size-medium}

<h3>Gamepad Shortcuts</h3>

<span style="font-weight: 400;">Many users really love this feature since using a controller is convenient (especially for when you're closer to your machine), inexpensive, and makes certain repetitive actions much easier. Common options are Xbox, PlayStation, and other third-party controllers available online.</span>

To start, connect your joystick to your computer and create a new profile using the ‘Add New Joystick Profile’ button. You will be prompted with further instructions on gSender on how to set it up. This profile will allow for shortcut assignment in a very similar manner as keyboard shortcuts, while also remembering your particular joystick. This will enable you to set up multiple profiles if desired.

If you run into difficulty with getting a particular joystick set up in gSender, consider searching for documentation provided by the manufacturer (for example, <a href="https://support.xbox.com/en-CA/help/hardware-network/controller/connect-xbox-wireless-controller-to-pc" target="_blank" rel="noopener">Xbox</a> or <a href="https://www.playstation.com/en-ca/support/hardware/ps4-pair-dualshock-4-wireless-with-pc-or-mac/" target="_blank" rel="noopener">PlayStation</a>). Some joysticks may also require drivers to be downloaded so your computer can read the signals that the joystick sends out.

<img class="aligncenter wp-image-9254 size-medium" src="https://resources.sienci.com/wp-content/uploads/2021/07/gSender-gamepad-profiles-850x402.png" alt="" width="850" height="402" />{.aligncenter .size-medium}

<h3>Tested Gamepads</h3>

To better guarantee your experience using a gamepad in gSender, we’ve taken the time to test a shortlist of some common and affordable options that are easy to source. With community help, we hope to continue growing this list of <strong>officially tested gamepads</strong> which currently includes:

[su_table responsive="yes" alternate="no"]
<table>
<tbody>
<tr>
<td>

<img class="non alignnone wp-image-5014" src="https://resources.sienci.com/wp-content/uploads/2021/07/yccteam-xbox-controller-e1682081885844-850x637.png" alt="" width="240" height="180" />{.aligncenter .size-medium}</td>
<td><strong>YCCTeam Xbox Controller</strong>
<ul>
  <li>Wireless</li>
  <li>Tested on Windows and macOS</li>
</ul>
</td>
</tr>
<tr>
<td>

<img class="non alignnone wp-image-5013" src="https://resources.sienci.com/wp-content/uploads/2021/07/logitech-f5710-e1682081913828.png" alt="" width="240" height="180" />{.aligncenter .size-medium}</td>
<td><strong>Logitech F710</strong>
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
<h3>Shortcut Printing</h3>
Find yourself forgetting how you’ve configured your keyboard or gamepad profile shortcuts? Hit the ‘Print’ button to generate a simple PDF that you can store on a tablet or print on some paper to keep next to your CNC. This PDF will contain all the shortcuts you’ve created and what actions they’re assigned to.

<img class="aligncenter wp-image-5017 size-medium" src="https://resources.sienci.com/wp-content/uploads/2021/07/gamepad-shortcuts-pdf-print-850x400.png" alt="" width="850" height="400" />{.aligncenter .size-medium}

<h2>Lightweight Mode</h2>

This mode enables gSender to run faster on computers that are less powerful and prone to lagging. ‘Lightweight Mode’ reduces the memory gSender uses by turning off processor-heavy aspects of the visualizer, from reducing detail to disabling it altogether. You can toggle it on or off using the slider positioned at the top right of the visualizer.

<img class="size-full wp-image-1587 aligncenter" src="https://resources.sienci.com/wp-content/uploads/2021/07/gSender-0.6.4-Lightweight-e1625168463320.png" alt="" width="783" height="407" />{.aligncenter .size-medium}

If you go to the visualizer settings, you can also customize what features are active in both ‘Regular’ and ‘Lightweight’ modes.

<img class="aligncenter wp-image-8587 size-medium" src="https://resources.sienci.com/wp-content/uploads/2021/07/gSender_Visualizer-850x501.png" alt="" width="850" height="501" />{.aligncenter .size-medium}

If gSender's visualizer is impacting the performance of your machine but Lightweight mode only helps once the whole visualizer is turned off, this hybrid option could help. Found in the Visualizer settings, the ‘SVG Visualizer’ substitutes the default 3D viewer with a pre-rendered, top-down image of your project, drastically reducing computer strain but still allowing the project to be displayed.

<img class="aligncenter size-full wp-image-4983" src="https://resources.sienci.com/wp-content/uploads/2021/07/edge-svg-enable.jpg" alt="" width="1305" height="909" />{.aligncenter .size-medium}

Once you toggle on ‘Enable SVG Visualizer’, whenever you turn on Lightweight Mode in the top right of the visualizer, you’ll see the alternate view with all animations turned off.

<img class="aligncenter size-full wp-image-4985" src="https://resources.sienci.com/wp-content/uploads/2021/07/edge-svg-difference-1.png" alt="" width="1600" height="800" />{.aligncenter .size-medium}

<h2>Touch Plate Setup</h2>

gSender has support for three types of touch plates:

<ol>
  <li>The Standard Block design</li>
  <li>Z Probe, also sometimes referred to as a ‘puck’</li>
  <li>And our specialized AutoZero touch plate</li>
</ol>

For a Z Probe, setting up is simple since you just need the thickness of the ‘puck’. Enter that value into gSender’s ‘Probe’ settings under ‘Z Thickness’ and you should be good to go!

If you’re trying to set up a custom ‘standard block’ plate, use some calipers to pick up on the measurements noted below. Once these are noted down, enter these into gSender’s ‘Probe’ settings in similarly named entries, and now you should find that gSender’s probing routine has been altered to fit the shape of your touch plate.

<img class="alignnone size-medium wp-image-7931" src="https://resources.sienci.com/wp-content/uploads/2021/07/Touch-Plate-Dimensioning-850x411.png" alt="" width="850" height="411" />{.aligncenter .size-medium}

<h2>Coolant Control / IOT Relay</h2>

If you have a coolant control pin on your CNC machine, gSender has a tab for manually controlling it. Under the 'Coolant' tab on the main screen, you can find the 'Mist' and 'Flood' buttons to activate the different modes of coolant use, as well as an indicator for whether the coolant function is active or inactive. This indicator also functions during job sending. You can turn off both coolant pins by pressing the 'Off' button.

Many hobby CNCers don't have a need for coolant and so prefer to use these outputs for controlling other periphery. The most common is an IOT relay that can be used to automatically control a vacuum for dust collection, the CNC's router, LED lighting, and more. See an example of how to set that up here: <a href="https://resources.sienci.com/view/lm-iot-relay/" target="_blank" rel="noopener">https://resources.sienci.com/view/lm-iot-relay/</a>

<img class="aligncenter wp-image-8586 size-full" src="https://resources.sienci.com/wp-content/uploads/2021/07/gSender_CoolantTab.png" alt="" width="568" height="302" />{.aligncenter .size-medium}

<h2>Spindle &amp; Laser Support</h2>

Similar to the manual coolant control, this area is for manual control of a spindle or laser outside of g-code sending. If you have a spindle or laser, you can activate these controls by going to the settings gear at the far right. In the ‘Spindle/Laser’ section in the left toolbar, press the toggle for ‘Spindle/Laser’.

<img class="aligncenter wp-image-4832 size-full" src="https://resources.sienci.com/wp-content/uploads/2021/07/spindle_laser-control-e1675884570537.jpg" alt="" width="1010" height="499" />{.aligncenter .size-medium}

Back at the main screen, you'll see the ‘Spindle/Laser’ tab at the bottom right. Here you can click to toggle between 'Spindle Mode' and 'Laser Mode', changing your grbl settings for you and displaying buttons specific to each device. For each mode there is also a red caution circle that indicates whether the spindle or laser is active. This works during manual control but also during job sending.

In spindle mode you can set the spindle speed with a slider, spin it up in either direction, and stop it again with the 'Stop' button. These are all based on g-code commands that can also be entered into the console manually if desired. The speed slider is set from your grbl firmware settings, so max and min speed can be altered in the Firmware Tool.

<img class="aligncenter wp-image-8585 size-full" src="https://resources.sienci.com/wp-content/uploads/2021/07/gSender_LaserTab.png" alt="" width="619" height="313" />{.aligncenter .size-medium}

'Laser Mode' is very similar, allowing for On/Off control, a slider for setting the laser power during manual control, and a ‘Laser Test’ button. The laser testing function is handy when troubleshooting your laser setup or for other sorts of locating and alignment because it only enables the laser for a short time before turning it back off again. Though this is much safer than regular on/off control, we still highly advise that you have you have a hand on a kill switch or E-stop during testing or control of either Laser or Spindle modes so that in case something goes wrong with your computer or the program they can still be safely deactivated.

<img class="aligncenter wp-image-8584 size-full" src="https://resources.sienci.com/wp-content/uploads/2021/07/gSender_LaserNotSpinTab.png" alt="" width="619" height="311" />{.aligncenter .size-medium}

<h3>Laser Diode Support</h3>

Some accessories can be really handy to add to a CNC router like a laser diode, drag knife, or pen plotter. These would all perform better on a faster, dedicated machine, but for occasional use why not use the existing motion system of the router to do other things for you? A laser diode in particular can be great because you can clamp the material to carve and then laser engrave afterwards and know that everything is still aligned.

Since many CNCs are coming with diode accessories, gSender has some unique features to also support lasers. Once 'Laser Mode' is turned on, gSender will:

<ul>
  <li>Automatically apply an offset from the router/spindle to the laser so all your g-code files stay aligned (configured in the Spindle/Laser settings, or with Firmware settings $741 and 742 on the SLB)</li>
  <li>Turn on the laser at low power when running a job outline (enabled in the Spindle/Laser settings). This will help you to better see where your project is going to be located on the material</li>
  <li>Switch to a specialized visualization designed to show raster engraving images better than typical g-code visualizers. Seeing the laser intensity in the movements is very useful to get a better idea of what your projects are going to look like when they’re run. This will only apply to files loaded after ‘Laser mode’ is enabled and the colour can be customized in the settings</li>
</ul>

<img class="aligncenter wp-image-4744 size-medium" src="https://resources.sienci.com/wp-content/uploads/2021/07/Laser-visualization-850x328.png" alt="" width="850" height="328" />{.aligncenter .size-medium}

<h2>Macros</h2>

Macros are standalone buttons within the gSender interface that allow you to execute a series of g-code commands when they're run. Macros can come in handy for a variety of uses:

<ul>
  <li>Button to run a v-carve or laser engraving of a common insignia into the back of your wood pieces</li>
  <li>Perform a specialized probing function for a particular jig you've set up</li>
  <li>Apply a predetermined offset that allows you to easily array your cutting jobs</li>
</ul>

You can create macros using the ‘+’ button under the ‘Macros’ tab. Here you'll see a space for inputting your custom g-code and adding a name and description for the macro. Advanced users may also want to leverage ‘Macro Variables’ which allow for greater g-code manipulation and pseudo-programming. Press ‘Add New Macro’ when completed.

<img class="wp-image-1929 size-medium aligncenter" src="https://resources.sienci.com/wp-content/uploads/2021/07/gSender-0.7.1-new-macro-850x478.png" alt="" width="850" height="478" />{.aligncenter .size-medium}

New macros will appear as buttons in the ‘Macro’ tab that can be rearranged by dragging them around. These buttons will display the macro name, show the description if you hover your mouse over them, and can always be later altered or deleted by clicking on their '...' button.

Any macro can be executed by pressing it. Before pressing it, a play icon will appear to show that you can select it. Once running, you should see the macro start to pulse green while a toast notification on the bottom left hand side of gSender also notifies you that it's running.

<img class="size-medium wp-image-1591 aligncenter" src="https://resources.sienci.com/wp-content/uploads/2021/07/gSender-0.6.4-run-macro-progress-850x450.png" alt="" width="850" height="450" />{.aligncenter .size-medium}

Macros can also be executed using shortcuts. Every time you create a new macro it'll become available at the bottom of the shortcuts list for you to assign a key or joystick button to. Add your keybindings and enable them by pressing the slider beside the label.

You can share macros with other users or transfer them between computers by using the import and export features. To import one or multiple macros, just press the button with the downward arrow and a browsing window will appear so that you can select the macros you wish to import. Similarly, to export all your current macros, press the button with the upward arrow and it'll generate a save file for you.

<p class="size-medium wp-image-1623 aligncenter"><img class="wp-image-1930 size-full aligncenter" src="https://resources.sienci.com/wp-content/uploads/2021/07/gSender-0.7.1-macro-import-export.png" alt="" width="540" height="284" />{.aligncenter .size-medium}</p>

<h3>Advanced Macros</h3>

gSenders Macro architecture is based on <strong>JavaScript</strong> and uses the Esprima library (<a href="https://esprima.org/" target="_blank" rel="noopener">https://esprima.org/</a>) and so will theoretically support any code that it does. This is exciting because Macros can move far past basic variables if you’d like to perform advanced functions on your CNC:

If you want some initial inspiration, see other macros <strong>made by our community</strong> or ones <a href="https://github.com/cncjs/CNCjs-Macros/blob/master/Hole_Center" target="_blank" rel="noopener"><strong>made for CNCjs</strong></a> (another g-code sender) which should also work in gSender. Otherwise, here are some other points of guidance:

<ol>
  <li>You'll want to develop your understanding of typical <a href="https://linuxcnc.org/docs/html/gcode/g-code.html" target="_blank" rel="noopener">g-codes</a> and <a href="https://linuxcnc.org/docs/devel/html/gcode/m-code.html" target="_blank" rel="noopener">m-codes</a> that are used for CNC control (the pages linked are very good sources for that)</li>
  <li>The "Macro Variables" dropdown in gSender shows many of the most commonly used operations when making your own macro</li>
  <li>Make your own variable with <code class="inline"> %variable = value_you_want_to_set</code> (ex. % probeSpeed = 150)</li>
  <li>Use your variable in g-code, like <code class="inline">G0 G91 G21 X[variable]</code> (moves the X-axis by the amount set in the variable)</li>
  <li>Test your code by printing it to the console <code class="inline">([variable])</code></li>
  <li>Start experimenting with basic math using numbers and variables</li>
  <li>Use global variables <code class="inline">global.variable</code> if you want variables that you can use in other macros (note that these get reset once gSender is closed)</li>
  <li>Read up on all the other Math features available like <a href="https://developer.mozilla.org/en-US/docs/Web/JavaScript/Reference/Global_Objects/Math" target="_blank" rel="noopener">absolute value, rounding, and trigonometry</a> (become very useful for more advanced probing cycles for example)</li>
  <li>Start to add more logic to your code using ternary expressions to choose between two outcomes (e.g. <code class="inline">%variable = (30 &gt; 20) ? 10 : 20</code> which is checking if 30 is bigger than 20, and if it is it'll make the variable = 10, otherwise it'll make the variable = 20).</li>
  <li>Here's an example of a more advanced macro, made by gSenders Lead Developer, which shows off much of the guidance given above. This macro was made for our new <a href="https://sienci.com/product/slb/" target="_blank" rel="noopener">SLB control board</a> in order to cycle between its 3 <a href="https://resources.sienci.com/view/slb-manual/#status-lights" target="_blank" rel="noopener">status light states</a>.
<ul>

  <li>The macro is only 3 lines.  First it checks what the current light state is and sets it to 0 if it doesn't have a state. Next, it sets the lights to the current state but applies a modulus of 3 since we can only have a state value of 0, 1, or 2 so we'll get an error if the value is 3 or above. Lastly, it adds +1 to the state so that if the macro is run again it'll put the lights into a new state.</li>
  <li><code class="inline">%nextLight = global.lightState || 0</code></li>
  <li><code class="inline">M356 P0 Q[nextLight % 3]</code></li>
  <li><code class="inline">%global.lightState = Number(nextLight) + 1</code></li>
</ul>
</li>

  <li>Read more about the Esprima library here: <a href="https://docs.esprima.org/en/latest/syntactic-analysis.html" target="_blank" rel="noopener">https://docs.esprima.org/en/latest/syntactic-analysis.html</a></li>
</ol>

<h2>Console</h2>

The console is a tab that you can access at the bottom right hand side of the gSender window. The text here shows a truer representation of the communication that happens between your computer and your CNC. As you start to understand more about your machine, this is a great tab to reference so you can see if commands are being properly sent, received, and executed. It's also great for troubleshooting since you can:

<ul>
  <li>Manually send g-code commands to your CNC</li>
  <li>Check for errors or alarms and the g-code that caused them (normally the line that comes before)</li>
  <li>Copy text straight from the console to send in an email for help by clicking the icon beside the "Run" button</li>
</ul>

<img class="aligncenter size-full wp-image-4230" src="https://resources.sienci.com/wp-content/uploads/2021/07/gSender-console.jpg" alt="" width="647" height="275" />{.aligncenter .size-medium}

When you first start up gSender, the console will display EEPROM settings that are sent from the Arduino in the control box. These EEPROM settings control parameters for your CNC such as:

<ul>
  <li aria-level="1">Maximum speed and acceleration in each axis</li>
  <li aria-level="1">Boundaries of the work area</li>
  <li aria-level="1">Direction of each axis movement</li>
  <li aria-level="1">Limit switch settings</li>
</ul>

To access EEPROM settings again, enter in “$$” into the console and hit the 'Enter' key or click the 'Run' button. These settings can be changed via the console as well as the Firmware Tool which we've designed as a much more visual way to alter machine settings.

<h2>Calibrate Tool</h2>

The 'Calibration Tool' on gSender enables you to make finer adjustments to your machine for improved performance. There are three processes available on gSender:

<ul>
  <li aria-level="1">Diagnostics</li>
  <li aria-level="1">XY Squaring</li>
  <li aria-level="1">Movement Tuning</li>
  <li aria-level="1">Surfacing Wasteboard</li>
</ul>

<img class="size-full wp-image-1699 aligncenter" src="https://resources.sienci.com/wp-content/uploads/2021/07/gSender-0.6.8-Calibrate.png" alt="" width="793" height="447" />{.aligncenter .size-medium}

<h3>Diagnostics</h3>

If you’d like to see general information about your CNC or are experiencing issues that you’d like to troubleshoot, gSender has a Diagnostics tool for that. Access it by clicking the ‘Calibrate’ tool on the top-right and opening the ‘Diagnostics’ tab.

Here you'll see machine information, notable firmware settings, and at-a-glance status on whether your limit switches, touch probe, or other pins are activated. This can be handy if you’re encountering odd behaviour with certain machine accessories or to double-check your wiring.

<img class="aligncenter wp-image-5176 size-medium" src="https://resources.sienci.com/wp-content/uploads/2021/07/CalibrateDiagnostic-850x413.jpg" alt="" width="850" height="413" />{.aligncenter .size-medium}

Another valuable feature is the ability to download a Diagnostic PDF file of your CNC machine when you click ‘Download Now!’. This PDF file is meant to include information on your computer, your CNC, recent alarms / errors, any currently loaded g-code file, and more. It's basically a treasure trove of information that you can share on community forums, Facebook groups, or with your CNC customer support. This can go a long way towards getting help from others on diagnosing any problems your CNC might be experiencing.

To download the PDF, click the “Download Now!” button. This will open a save dialog box. Save the file to a location that you can easily access to send along to others in an email, support ticket or post online.

<img class="aligncenter size-medium wp-image-5099" src="https://resources.sienci.com/wp-content/uploads/2021/07/Diagnostic-850x341.jpg" alt="" width="850" height="341" />{.aligncenter .size-medium}

Lastly, you can copy the last 40 lines of code in the gSender console (1), by hitting the double page icon to the left of the Run button (2). This will copy the code to your clipboard, so you can paste it to forums or share it with support teams.

<img class="aligncenter wp-image-9244 size-full" src="https://resources.sienci.com/wp-content/uploads/2021/07/gSender_CopyLast40.png" alt="" width="473" height="259" />{.aligncenter .size-medium}

<h3>XY Squaring</h3>

When mounting your LongMill on the table, there is a basic squaring process illustrated in our instructions (<a href="https://resources.sienci.com/view/lm-table-mounting/">https://resources.sienci.com/view/lm-table-mounting/</a>). If you do find that the machine is not perfectly square, you can follow the steps in this process to fine tune the position of your rails.

When you access the ‘Calibration Tool’ window, the ‘XY Squaring’ procedure is shown on the first tab. All instructions are illustrated in the window, however a brief overview will be provided.

<img class="size-medium wp-image-1707 aligncenter" src="https://resources.sienci.com/wp-content/uploads/2021/07/gSender-0.6.8-Squaring-850x478.png" alt="" width="850" height="478" />{.aligncenter .size-medium}

You will need the following:

<ul>
  <li aria-level="1">Ruler or measuring tape</li>
  <li aria-level="1">Tapered bit or V-bit</li>
  <li aria-level="1">Tape</li>
</ul>

<ol>
  <li aria-level="1">Jog the machine to the front left corner, with the bit raised slightly over the surface of your wasteboard</li>
  <li aria-level="1">Mark the points with tape and move the machine as directed

<img class="size-medium wp-image-1704 aligncenter" src="https://resources.sienci.com/wp-content/uploads/2021/07/gSender-0.6.8-Squaring-2-850x478.png" alt="" width="850" height="478" />{.aligncenter .size-medium}</li>
  <li aria-level="1">Measure the distance between the marked points and record the values

<img class="size-medium wp-image-1705 aligncenter" src="https://resources.sienci.com/wp-content/uploads/2021/07/gSender-0.6.8-Squaring-3-850x478.png" alt="" width="850" height="478" />{.aligncenter .size-medium}</li>
  <li aria-level="1">Adjust your rail positions with the values determined by the XY Squaring procedure

<img class="size-medium wp-image-1706 aligncenter" src="https://resources.sienci.com/wp-content/uploads/2021/07/gSender-0.6.8-Squaring-4-850x478.png" alt="" width="850" height="478" />{.aligncenter .size-medium}</li>
</ol>

The great advantage to this tool is it saves you having to do the trigonometry yourself and will also let you know if your machine is aligned closely enough that it’s not worth worrying about.

<h3>Movement Tuning</h3>

You are able to change how much your motors turn to improve the accuracy of your machine movement. This is done through modifying the EEPROM settings that are stored on your LongMill, which this process will guide you through. You can tune the X, Y and Z axes individually. All instructions are illustrated in the 'Calibration Tool', however a brief overview will be provided.

You will need:

<ul>
  <li aria-level="1">Marker or tape</li>
  <li aria-level="1">Measuring tape</li>
</ul>

<ol>
  <li aria-level="1">Jog your machine to the middle of whichever axes you choose to tune, so that there is enough room to complete this procedure. For example, on the X-axis you would jog halfway on the X-axis rail</li>
  <li aria-level="1">Select what axis to tune on the drop down menu

<img class="size-medium wp-image-1702 aligncenter" src="https://resources.sienci.com/wp-content/uploads/2021/07/gSender-0.6.8-Movement-Tuning-850x478.png" alt="" width="850" height="478" />{.aligncenter .size-medium}</li>
  <li aria-level="1">Mark down the location of your reference on the machine. For example the X-axis tuning references the edge of the XZ gantry on the X rail</li>
  <li aria-level="1">Move the axis a chosen distance</li>
  <li aria-level="1">Measure the travel distance between the marked location and the reference edge

<img class="size-medium wp-image-1700 aligncenter" src="https://resources.sienci.com/wp-content/uploads/2021/07/gSender-0.6.8-Movement-Tuning-2-850x478.png" alt="" width="850" height="478" />{.aligncenter .size-medium}</li>
  <li aria-level="1">Change the EEPROM setting as recommended by the procedure by pressing 'Set EEPROM setting'

<img class="size-medium wp-image-1701 aligncenter" src="https://resources.sienci.com/wp-content/uploads/2021/07/gSender-0.6.8-Movement-Tuning-3-850x478.png" alt="" width="850" height="478" />{.aligncenter .size-medium}</li>
  <li aria-level="1">Repeat the procedure for each axis you wish to tune</li>
</ol>

<h3>Surfacing</h3>

https://youtu.be/jfInIEOB3kU

Surfacing the wasteboard of your machine can easily be done right inside gSender! The first thing you’ll want to do is decide where you want to start surfacing and in most cases the front, left of the machine is the most convenient. You might also want to remove any accessories that might get in the way of your machine travelling around during surfacing as well as have a good vacuum on hand because surfacing can get really messy. You can find the Surfacing Tool under the Calibrate tab, or under the Surfacing tab.

<img class="aligncenter wp-image-8597 size-medium" src="https://resources.sienci.com/wp-content/uploads/2021/07/Surfacing-850x425.png" alt="" width="850" height="425" />{.aligncenter .size-medium}

<ol>
  <li>Start by entering the settings you’d like to use to generate your surfacing job:
<ol>
  <li><strong>X &amp; Y</strong>: decides the cutting size (width and depth) you want to surface. If you’re surfacing your wasteboard, use the manufacturer’s spec on max machine travel or manually jog to the limits to cover the full cutting area, or if you’re surfacing a piece of material then you can use a measuring tape.
- <strong>LongMill MK2</strong>: 818mm (32.2”) or 1278 (50.3”) x 366mm (14.4”) or 866 (34.1”)
(if using limit switches, remove about 8mm/0.3” in X and 11mm/0.43” in Y)
- <strong>LongMill MK1</strong>: 320mm (12.6”) or 805 (31.7”) x 344mm (13.54”) or 844 (33.23”)
(if using limit switches, remove about 35mm/1.38” in X and 24mm/0.94” in Y)
(if using magnetic dust shoe, remove about 34mm/1.34” in X)
- <strong>Mill One</strong>: 235mm (9.25”) or 257 (10.1”) x 185mm (7.28”)</li>
  <li><strong>Cut Depth &amp; Max</strong>: describes how deep you want to cut per pass and the total depth you want to cut down. For larger surfacing bits usually you should keep cut depth below 1mm, max depth should be increased to a couple millimeters if you think your material is very warped.</li>
  <li><strong>Bit</strong> (typically 6 - 25mm): make sure you have the right bit for the job like a surfacing tool or a large, flat end mill since this will give you a better surface finish.</li>
  <li><strong>Spindle RPM</strong> (default 1700): only applies if you have an automatic speed control, otherwise set this manually on your router.</li>
  <li><strong>Feedrate</strong> (default 2500mm/min): influenced by the RPM, stepover, bit diameter, and cut depth. Luckily if you set it incorrectly you’ll be able to override it during the job since surfacing can cause burning when cutting too slow or can have worse surface finish when cutting too fast.</li>
  <li><strong>Stepover</strong> (default 40%): sticking around 40% tends to be a good balance between speed (using a higher %) and better surface finish (using a lower %).</li>
</ol>

<img class="size-full wp-image-8583 aligncenter" src="https://resources.sienci.com/wp-content/uploads/2021/07/Settings-w-border.png" alt="" width="531" height="298" />{.aligncenter .size-medium}</li>
  <li>Select a Start Position of any four corners or the center by clicking the dot; this is where the surfacing will begin. You can also select a surfacing pattern of spiral or zig-zag. The spiral will only cut from the inside-out if the start position is the centre. If you toggle the flip cut direction, the spiral will cut conventional instead of climb, and the zig-zag pattern will cut vertically instead of horizontally.

<img class="aligncenter size-full wp-image-8598" src="https://resources.sienci.com/wp-content/uploads/2021/07/gSender-surfacing-front-corner.png" alt="" width="444" height="161" />{.aligncenter .size-medium}</li>
  <li>Press ‘Generate G-code’ and check your surfacing tool path using the ‘Visualizer Preview’ tab. You can also see the raw g-code using the ‘G-code Viewer’ tab and can copy and save it to a g-code file if you’d like to use it again later.

<img class="aligncenter wp-image-9237 size-medium" src="https://resources.sienci.com/wp-content/uploads/2021/07/gSender_Generategcode-1-850x478.png" alt="" width="850" height="478" />{.aligncenter .size-medium}</li>
  <li>Press ‘Run on Main Visualizer’ to bring the g-code into gSender’s main screen. Make sure that you jog to the starting point and set your zero in the right place before starting the job. You can also press the ‘Outline’ button as an easy way to check that you’ll be surfacing where you expect and if you find the dimensions aren’t correct you can always re-open the surfacing tool, tweak the size, and try again. Feel free to start the job whenever you’re ready!

<img class="size-medium wp-image-1710 aligncenter" src="https://resources.sienci.com/wp-content/uploads/2021/07/gSender-0.6.8-Surfacing-4-850x479.png" alt="" width="850" height="479" />{.aligncenter .size-medium}</li>
</ol>

Did you know that surfacing can be used for more than your wasteboard? It’s great for creating a perfectly flat surface of your starting materials, just like a jointer or surface planer would. You can also use the <a href="https://docs.google.com/document/d/1yUO8bMAw5XoRO8AWGc3ZB5_WVj12ARP-kvf5pciUNL0/edit#heading=h.r1c788pgn92b">Rotary Surfacing</a> tool if you are wanting round stock.

<h2>Stats Page</h2>

Curious to know how many jobs you’ve completed or how many hours you’ve put on your machine? Find this information in the “Stats” section of the settings. For now it provides a simplified breakdown of total hours run, longest and average runtime, total jobs run, and compares completed vs cancelled jobs. It’s a useful tool for tracking maintenance schedules and will continue to be expanded into the future.

<img class="aligncenter size-full wp-image-4977" src="https://resources.sienci.com/wp-content/uploads/2021/07/gSender-stats-page.jpg" alt="" width="1244" height="842" />{.aligncenter .size-medium}

<h2>Firmware Tool</h2>

Any board you have will come pre-installed with CNC firmware, along with the custom EEPROM settings for that machine, so typically you won’t need to access the ‘Firmware’ tool. If you choose to use this tool, it can give you access to many of your machines "behind-the-scenes" settings for tweaking or modding your setup. Open it by clicking the ‘Firmware’ tool at the top of the screen.

<h3>Unsupported CNCs</h3>

If your CNC isn't listed below, then it's considered "unsupported":

<ul>
  <li>Sienci Labs <strong>LongMill</strong> (MK1, MK2, and MK2.5), <strong>AltMill</strong>, and <strong>Mill One</strong> (V1, V2, and V3)</li>
  <li>Don't see your machine on this list and want it fully supported? Let your manufacturer know to get in contact with us so that we can add their machine profiles to gSender :)</li>
</ul>

If your machine is unsupported, it means that the Firmware Tool won't be able to perform the same features as for supported machines. In this case, <strong>if your machine isn't working, contact your manufacturer to get their advice on how to fix it</strong>. Using this tool makes it possible to ruin your machine further and we won't be able to help you with your specific hardware. For unsupported machines:

<ol>
  <li aria-level="1">Choosing your machine <strong>name</strong> from the drop down menu is primarily cosmetic</li>
  <li aria-level="1"><strong>Flash</strong> either vanilla grbl, or for grblHAL boards upload a hex file to flash a new firmware</li>
  <li aria-level="1"><strong>Import</strong> EEPROM settings from a file if you had settings that were working and something changed</li>
  <li aria-level="1"><strong>Export</strong> current EEPROM settings if you'd like to save your current setup in case something goes wrong</li>
  <li aria-level="1"><strong>Restore</strong> all your machine settings back to typical vanilla grbl values</li>
  <li aria-level="1">And otherwise see and modify any machine settings as well as search any keywords to help you find what you're looking for</li>
</ol>

<img class="size-medium wp-image-5056 aligncenter" src="https://resources.sienci.com/wp-content/uploads/2021/07/Firmware-850x505.jpg" alt="" width="850" height="505" />{.aligncenter .size-medium}

<h3>Supported CNCs</h3>

If your CNC was listed above then it's "supported" by the Firmware tool. This means that the manufacturer is working with us to keep their machine profiles up-to-date, which in-turn gives you access to more features:

<ol>
  <li aria-level="1">Choose your machine <strong>name</strong> from the drop down menu</li>
  <li aria-level="1"><strong>Flash</strong> either your specific machines grbl firmware, or for grblHAL boards upload a hex file to flash a new firmware</li>
  <li aria-level="1"><strong>Import</strong> EEPROM settings from a file if you had settings that were working and something changed</li>
  <li aria-level="1"><strong>Export</strong> current EEPROM settings if you'd like to save your current setup in case something goes wrong</li>
  <li aria-level="1"><strong>Restore</strong> all your machine settings back to the defaults for your profile in case they've somehow been altered or wiped (like a "factory reset")</li>
  <li aria-level="1">Also be able to see a <strong>yellow highlight</strong> and be able to reset individual settings that have been changed from the machine defaults</li>
  <li aria-level="1">And otherwise see and modify any machine settings as well as search any keywords to help you find what you're looking for</li>
</ol>

<img class="size-medium wp-image-5056 aligncenter" src="https://resources.sienci.com/wp-content/uploads/2021/07/Firmware-850x505.jpg" alt="" width="850" height="505" />{.aligncenter .size-medium}

<h3>Machine Profiles</h3>

If you're planning to make any firmware modifications, gSenders Firmware tool at the top right of the screen defaults to displaying the "LongMill MK2 30x30" profile. If that's not your machine, then beside the word "Profile", select your machine from the dropdown menu (if it's not listed then select "Generic CNC").

For instance most LongMills ship with <strong>LongMill MK2 30x30</strong> firmware pre-installed so it matches gSender, but if you have any other machines from Sienci Labs then you'll need to match it up (for example: 12x30 or 48x30 MK2, any sized MK1, AltMill, etc.). For <strong>supported machines</strong>, once you've made this change you might want to 'Restore Defaults' to ensure your machine has all the most up-to-date settings.

Please Note: If your Z-axis is working in the opposite direction than expected, confirm you have the correct profile. MK2 users must choose either LongMill MK2 12x30, LongMill MK2 30x30, or LongMill MK2 48x30. You can find instructions on how to flash firmware here: <a href="https://resources.sienci.com/view/lmk2-grbl-firmware/" target="_blank" rel="noopener">https://resources.sienci.com/view/lmk2-grbl-firmware/</a>

<img class="aligncenter size-full wp-image-4907" src="https://resources.sienci.com/wp-content/uploads/2021/07/machine-profile-dropdown-1.jpg" alt="" width="789" height="376" />{.aligncenter .size-medium}

If you're running into an issue where the size isn't correct when using Soft Limits for example, get the size from your manufacturer or their resources and you should find that the changes will be straightforward to make through the 'Firmware tool' within gSender. Simply apply your new measurements to the X-axis, Y-axis and Z-axis maximum travel fields. Then hit the apply changes button.

<img class="aligncenter wp-image-9135 size-medium" src="https://resources.sienci.com/wp-content/uploads/2021/07/Updated-firmware-profile-size-850x461.jpg" alt="" width="850" height="461" />{.aligncenter .size-medium}

<h2>Start/Stop G-code</h2>

A powerful feature to control your accessories automatically (like turning on/off a spindle or vacuum) or to run movement macros that are custom to your machine. 'Program Events' (formerly "Start/Stop G-code")' in gSenders settings automatically apply g-code to your cutting job at the start, end, or if you stop, pause, or resume the job. The 'Stop' event is there to ensure that "ending g-code" is always run even if you have to stop a job prematurely. You can also toggle these on and off if you don't want them run for specific jobs.

Three massive perks to setting up automations this way are:

<ol>
  <li>There's no need to get into the weeds customizing your CAM post processor</li>
  <li>gSender is able to send code when you pause, resume, or emergency stop your machine, all of which a g-code file on its own would never be able to do</li>
  <li>This additional amount of control will make your CNC safer to use</li>
</ol>

For example, if you were to add M3/M5 commands to your CAM post processor to control your spindle but then chose to pause your job midway to check something, then most CNCs wouldn't know to stop spinning your spindle or retract it since g-code files can't carry this information; this is where gSender is able to the heavy lifting.

For the text-box of the situation you want the action to happen, type in the g-code commands you wish to run, then press the '<strong>Update</strong>' button to save it. For example, if you installed an IOT relay to turn your router and vacuum on and off and wanted to make sure they were enabled for every job you ran, you could add:

<ul>
  <li>"<strong>M8</strong>" for Start and Resume</li>
  <li>"<strong>M9</strong>" for Stop and Pause</li>
  <li>If you wanted to add a delay to give your vacuum or router time to fully turn on, then you could add "<strong>G4 P5</strong>" after the M8 for a delay of 5 seconds (you can customize that delay to your equipment)</li>
  <li>If you wanted to keep the vacuum and router running during a pause, then you don't need to add "<strong>M9</strong>" to Pause</li>
  <li>All this can also apply to automatically control a spindle, where you'd instead use "<strong>M3</strong>" and "<strong>M5</strong>", you can also add a delay with "<strong>G4 P#</strong>"</li>
  <li>If you want to raise the Z-axis on Pause and lower it on Resume, you could also add:

<ul>
  <li>"%global.move=modal.distance" then "G91 G0 Z-5" for Pause to move 5mm out of the way</li>
  <li>"G91 G0 Z5" then "[global.move]" for Resume to move back down</li>
</ul>

</li>
</ul>

<img class="aligncenter size-medium wp-image-5849" src="https://resources.sienci.com/wp-content/uploads/2021/07/2023-06-16_08-59-46-2-850x478.jpg" alt="" width="850" height="478" />{.aligncenter .size-medium}

<h2>Tool Changing</h2>

For CNC machines, tool changes are pauses that are programmed in the g-code for a user to switch out the cutting tool for a different one, thus allowing for multiple toolpaths (cutting operations) within one g-code file. The g-code for tool changing is an M6 command, in which the program will pause until the user tells it to continue, usually through a 'Resume' and/or 'Confirm Tool Change' button on the machine interface program. On gSender, you can program what happens when there is M6 in your g-code.

The tool change options are in the Settings -&gt; Tool Change menu. You can select from one of 5 different options.

<img class="aligncenter wp-image-5207" src="https://resources.sienci.com/wp-content/uploads/2021/07/2023-06-12_09-54-34-850x463.png" alt="" width="655" height="357" />{.aligncenter .size-medium}

You can <strong>Ignore</strong> any M6 tool change commands, <strong>Pause</strong> the job when a tool change is recognized, or select one of the last three <strong>Wizards</strong> that will guide you through pre-set tool changing methods. In the split image below, you can see an example of the job <strong>Pause</strong> on the left side and the <strong>Wizard</strong> on the right.

<img class="aligncenter wp-image-5208" src="https://resources.sienci.com/wp-content/uploads/2021/07/Pause-vs-Wizard-850x337.jpg" alt="" width="651" height="258" />{.aligncenter .size-medium}

If you are using one of the wizard options, know that you can access all other gSender controls while the wizard is open like jogging and zeroing. It also has flexibility to go back a step if you missed something or had a mistake, or to be minimized temporarily if you want to check the visualizer.

<ol>
  <li><strong>Ignore</strong>
This simply ignores any M6 commands in the g-code file. This is the default option since it’s perfect for beginners that only make projects with one tool or those that create separate files for each tool and prefer to manually perform tool changes between files.</li>
  <li><strong>Pause</strong>
Pauses gSender at the tool change point, as if you had hit the pause button manually. This gives you freedom to jog, zero, or anything else you’d like, and is great for those that are running multi-tool files but want to use a different process than the Wizards provide. This could be a manual probing process, a different tool changing approach, or running custom macros to support your machines specific hardware. gSender is compatible with tool length sensors like the Carbide 3D bitsetter, and our community has compiled a <a href="https://forum.sienci.com/t/bitsetter-and-other-tool-length-sensors-supported-in-gSender/3877/4">list of macros</a> for tool changing that you can use when you are paused. Just note that pausing can’t always guarantee keeping track of your movements and actions when it comes time to resume the job so try to ensure you get back to the starting point and set zeros correctly.</li>
  <li><strong>Standard Re-zero</strong> (Wizard)
Titled ‘standard’ because it’s exactly the same as the standard process you might normally follow for running a file, changing the tool, re-zeroing Z, then running the next file except it’s applied to a single file with multiple toolpaths. Since the process is so familiar, this is a great way to dip your toes into tool changing within one file. Compatible with using a touch plate or the paper method, zero out at a predetermined spot (usually at the front left corner), and use jogging to move around. The advantage of introducing this extra automation and guidance during tool changes is that you don’t have to worry about custom macros and it reminds you of simple steps like turning the router back on or zeroing Z.</li>
  <li><strong>Flexible Re-zero</strong> (Wizard)
Similar to the ‘standard’ wizard with similar steps and manual movements but provides the ability to zero Z off a point that wasn’t your starting Z when it comes time to change the tool. This is useful if you tend to carve away your material and lose the starting Z or you don’t have limit switches but would like a process similar to a tool length sensor.</li>
  <li><strong>Fixed Tool Sensor</strong> (Wizard)
This is the most automated setting where all probes and movements are done for you, you only need to intervene by changing the tools. Set up the job and zero normally then expect the machine to move to the sensor location when it reaches a tool change, verify tool length, prompt for a change, probe new tool, then resume cutting. Your machine will need to be homed, have limit switches, and have a tool length sensor (compatible with Carbide 3D bitsetter for example) in order for this option to work. To set up the sensor mount the router/spindle as far down as you might typically put it, with the longest bit mounted in it, then jog it to hover over the tool length sensor with some room to spare and open the settings menu to save that location. This will be the spot your machine moves to every tool change so if it’s too low or your sensor doesn’t work it’ll run into the sensor.

<img class="aligncenter size-full wp-image-5209" src="https://resources.sienci.com/wp-content/uploads/2021/07/2023-06-12_10-45-05.png" alt="" width="550" height="461" /></li>{.aligncenter .size-medium}
</ol>

<h2>Workspaces</h2>

Usually you would only have one origin or zero position for your project, therefore gSender will only save one zero. However, if you plan to do a series of projects that require different zero positions, or are lining up to do some more complex jigging or part batches, you may want to set up multiple workspaces all at once. This can save you time by not having to set a zero position for repetitive tasks or specific jig setups. You can do this by creating up to six different zero positions with the six workspaces in gSender. Access each 'Workspace' at the top right of the program by pressing the drop down to select which workspace to use. gSender will act completely in-line with whatever workspace you've selected, whether you want to set zero, probe, surface, or anything else.

<img class="size-medium wp-image-1596 aligncenter" src="https://resources.sienci.com/wp-content/uploads/2021/07/gSender-0.6.4-Workspaces-e1625168506414-850x431.png" alt="" width="850" height="431" />{.aligncenter .size-medium}

The video below explains the process in greater detail.

https://youtu.be/jmiaWA5tiVw?t=336

<h2>Settings</h2>

<h3>Transferring Settings</h3>

gSender’s settings are stored on a file on whatever computer is used to run it. This mostly includes everything that you’ll find in the settings menu such as units, machine preset, probe, tools, jogging presets, keymapping, tool change g-code, start/stop g-code, and more. If you plan on using a different computer to run your CNC using gSender or want to run gSender remotely, some of these settings might be very important to carry over to the alternate computer to make sure things keep running as expected.

To transfer your settings over:

<ol>
  <li style="list-style-type: none;">
<ol>
  <li>Begin by opening gSender, going to the settings gear in the top-right corner, and clicking the ‘Export Settings’ button in the ‘General’ tab
  
  <img class="aligncenter wp-image-8578 size-medium" src="https://resources.sienci.com/wp-content/uploads/2021/07/gSender_ExportSettings-850x478.png" alt="" width="850" height="478" />{.aligncenter .size-medium}</li>
</ol>
</li>
  <li style="font-weight: 400;" aria-level="1"><span style="font-weight: 400;"> Save the file somewhere onto your computer that you can find afterwards</span>
  
  <img class="aligncenter size-medium wp-image-4283" src="https://resources.sienci.com/wp-content/uploads/2021/07/gSender-Headless-10-save-settings-850x454.jpg" alt="" width="850" height="454" />{.aligncenter .size-medium}</li>
  <li>Outside of gSender, find the file and transfer it using a memory stick or sending it over the internet by emailing to yourself or using Google Drive or OneDrive.</li>
  <li>Once you’ve got the file onto the other computer it’s now easy enough to open gSender on that computer, or in the web browser if you’re doing remote control, and go to the settings and click the ‘Import Settings’ button in the ‘General’ tab.
  
  <img class="aligncenter wp-image-8577 size-medium" src="https://resources.sienci.com/wp-content/uploads/2021/07/gSender_ImportSettings-850x478.png" alt="" width="850" height="478" />{.aligncenter .size-medium}</li>
  <li>Locate the file and click ‘Open’
  
  <img class="aligncenter size-medium wp-image-4285" src="https://resources.sienci.com/wp-content/uploads/2021/07/gSender-Headless-12-open-settings-850x534.jpg" alt="" width="850" height="534" />{.aligncenter .size-medium}</li>
  <li>You’ll get a warning. Click ‘Import Settings’ if you want to continue. Once you do, gSender will disconnect and you’ll need to reconnect the machine to resume operation but the settings should now be brought over.
  
  <img class="aligncenter size-full wp-image-4302" src="https://resources.sienci.com/wp-content/uploads/2021/07/gSender-Headless-20-import-warning.jpg" alt="" width="781" height="381" />{.aligncenter .size-medium}</li>
</ol>

<h2>Remote Mode</h2>

If you’ve ever wanted to run your CNC without being stuck right next to it, this is the feature you’re looking for. The remote mode is exactly how it sounds, it gives the ability for a remote computer to connect over a shared internet network to a permanently installed, normally lower-end computer, that runs the CNC. This ‘<strong>remote computer</strong>’ can be any device that can connect to the internet and run a web browser, meanwhile the ‘<strong>inline computer</strong>’ plugs into your CNC with a USB cable and will receive commands over the internet from the remote computer.

This feature is handy if you’d like to:

<ul>
  <li>Load in a file from your design computer outside your shop then run it on your computer inside the shop</li>
  <li>Use a tablet as the primary means of controlling your CNC rather than a mouse and keyboard</li>
  <li>Use a phone for occasional use when jogging or running functions</li>
  <li>Leverage a mini PC or Raspberry Pi as the inline (tethered) computer for cheap, fanless, and reliable operation without taxing them with a display, keyboard, and mouse</li>
</ul>

Before diving into the setup, here are some quirks and warnings that are important to keep in mind:

<ul>
  <li>Both systems need to be on the same internet network to work, where the device used to run remote operations needs to be able to run a web browser</li>
  <li>You may need to be an Administrator of the inline computer to make the changes needed so ensure you have that power</li>
  <li>This feature will always be inherently less reliable than a hard-wired connection because of its reliance on your shop’s internet connection for communication. Keep this in mind if you intend on using remote control for more important projects or with expensive tools or materials</li>
  <li>Remote control is still in development so expect to experience some bugs if you’d like to set this up for yourself. The setup process is a little bit more involved on your computer so we don’t advise using this feature if you’re not confident with troubleshooting your own setup</li>
  <li>This feature is NOT intended to enable use of your CNC while AWAY FROM YOUR WORKSHOP. A CNC should always be run while you or another knowledgeable operator is in the vicinity to ensure safe machine operation and be able to react if intervention is required. CNCs can cause fires from electronics, material friction, and can have other safety hazards if not properly monitored</li>
  <li>In other contexts this feature could be thought of as running ‘headless’ but it doesn’t fully meet the requirements of that term. Though remote controlling the CNC from another computer should reduce the requirements of the inline computer, at minimum it still needs to boot the idle version of gSender with a window manager. This is in contrast to a fully ‘headless’ setup where a skinned-down program exists only to pass along information from other devices with no UI to send along information itself</li>
</ul>

<h3>Enabling Remote Mode</h3>

All setup steps need to happen on the inline computer (the computer you’ll have connected via USB to your CNC) and have been simplified to mostly happen within gSender.

<ol>
  <li>To begin, click the satellite antenna icon on the top right of the screen. If the icon isn’t there, you’ll need to make sure you have a newer version of gSender that supports this feature.
  
  <img class="aligncenter wp-image-5179 " src="https://resources.sienci.com/wp-content/uploads/2021/07/2023-06-13_10-19-20.jpg" alt="" width="628" height="138" />{.aligncenter .size-medium}</li>
  <li>This is where remote mode is set up. First you’ll want to click the ‘Enable Remote Mode’ toggle. Second, click the box next to ‘IP’ and select one of the options that gSender tries to recommend for your particular computer network. For an average setup the ‘Port’ value can also be left alone. The third step is to click on OK once you have completed the configuration.
  
  <img class="aligncenter wp-image-5181 " src="https://resources.sienci.com/wp-content/uploads/2021/07/2023-06-13_10-24-49-850x476.jpg" alt="" width="642" height="360" />{.aligncenter .size-medium}

If you’re an <strong>advanced user</strong> or have tried the default values without success, you can type in any other IP address or Port that you’d like since the defaults aren’t guaranteed to work. Common port values are 3000, 8000, and 8080 and generally don’t go below 1024 since those are considered privileged. Changing IP addresses can also help if you’re running a VPN or need a different internal IP to external IP mapping.</li>
  <li>gSender needs to restart in order for the remaining changes to take place. You can choose to restart immediately or wait until later.
  
  <img class="aligncenter size-full wp-image-5184" src="https://resources.sienci.com/wp-content/uploads/2021/07/2023-06-13_10-24-15.jpg" alt="" width="660" height="280" />{.aligncenter .size-medium}</li>
  <li>If there was a problem using the specified IP address or Port, you’ll get an error window to let you know. In this case you should be able to reopen gSender, go back to the Remote Mode settings, and try another IP or Port until the setup is successful.
  
  <img class="aligncenter wp-image-5183" src="https://resources.sienci.com/wp-content/uploads/2021/07/2023-06-13_10-33-18.jpg" alt="" width="666" height="199" />{.aligncenter .size-medium}</li>
  <li>You’ll know the setup was successful if gSender restarts, the antenna icon is green, and numbers show next to it. As a quick test, click on the numbers to copy them then open a web browser like Chrome or Edge and paste them into the address bar and press enter (you can also type the number manually). After the page loads, you should see a copy of gSender running in the web browser! <strong>If something’s not working</strong>, check you followed the setup steps correctly or reference the firewall or troubleshooting sections below.
  
  <img class="aligncenter wp-image-5187 " src="https://resources.sienci.com/wp-content/uploads/2021/07/Arrow-hand.jpg" alt="" width="656" height="159" />{.aligncenter .size-medium}</li>
</ol>

<h3>Firewall Setup</h3>

During initial setup, you might see a Security Alert window pop up or run into an issue where the browser address isn’t working. The most likely issue here is that your inline computer firewall isn’t allowing gSender to communicate to other devices on your network.

<strong>For Windows:</strong> You should simply see a popup from Windows Firewall or your antivirus software asking for approval to allow gSender to communicate on your home network. Please check the box beside “Private networks” and “Public networks”. This should be all that’s needed.

<img class="nar aligncenter wp-image-5995 size-medium" src="https://resources.sienci.com/wp-content/uploads/2021/07/Update-Remote-mode-850x571.jpg" alt="" width="850" height="571" />{.aligncenter .size-medium}

<strong>For Mac / Linux / Pi:</strong> If you find that you can’t connect with outside devices or just want some extra safety you might want to try opening the Universal FireWall (UFW) on a given port to allow external access. This can be started with <code class="inline">sudo ufw enable</code> (if UFW is not found then install it using <code class="inline">sudo apt-get install ufw</code> and your root password) then opening the desired port, for example <code class="inline">sudo ufw allow 8080</code> opens port 8080 for external access. If you want to see what ports are already open, you can use <code class="inline">ufw status verbose</code>.

<h3>Using gSender Remotely</h3>

With setup complete, regular use is pretty straightforward:

<ol>
  <li>Connect the inline computer to your CNC as you would normally using the USB cable. Turn on power to your CNC and connect to it in gSender as usual.</li>
  <li>Look for the numbers next to the antenna and write them down including all the symbols and punctuation; these will be used to connect to your CNC on the remote computer / device.
  
  <img class="aligncenter wp-image-5193 size-full" src="https://resources.sienci.com/wp-content/uploads/2021/07/Remote-1.jpg" alt="" width="614" height="138" />{.aligncenter .size-medium}</li>
  
  <li>On any remote device that can run a web browser like Chrome or Edge (computer, phone, tablet) open the browser and type those same numbers you wrote down into the top address bar. In this example the numbers are <strong>192.168.2.203:8000</strong> but yours may be different. Press enter, and hopefully the familiar gSender interface will appear in your browser window. If not, ensure that your remote device is on the same network as your inline computer.
  
  <img class="aligncenter size-medium wp-image-4280" src="https://resources.sienci.com/wp-content/uploads/2021/07/gSender-Headless-07-address-into-web-850x293.jpg" alt="" width="850" height="293" />{.aligncenter .size-medium}</li>

  <li>Once connected, you should now be able to control your CNC remotely with most of the same features and functions you’d normally expect:
  
  <img class="aligncenter size-medium wp-image-4281" src="https://resources.sienci.com/wp-content/uploads/2021/07/gSender-Headless-08-gSender-in-browser-850x459.jpg" alt="" width="850" height="459" />{.aligncenter .size-medium}
<ul>
  <li>You’ll be able to use both the remote and inline devices simultaneously to control your CNC like jogging, opening and closing files, probing, macros, and more</li>
  <li>You’ll also see that both their screens look exactly the same so you can watch the visualizer move around or check on the machine state</li>
  <li>On phones the screen will look different since we’ve optimized it for jogging, setting zeros, and probing</li>
  <li>When you click to ‘load a file’ you’ll see that you’ll only be able to load files from the device you’re currently on, don’t expect to gain access to the files stored on the opposite device. However once the file is loaded into gSender, you’ll be able to run it from any device</li>
  <li>There can be multiple remote devices all connected to the same inline computer at the same time to control your CNC from multiple devices. There can also be multiple inline computers controlled from the same remote computer, giving you multi-CNC control from the same device</li>
  <li>gSender settings like ‘safe height’, ‘start/stop g-code’, ‘tool changing’, and any other gSender specific settings won’t carry over to the remote computer. If you want to make sure files are run the same way every time you’ll need to transfer your gSender settings over by following the ‘Transfer Settings’ instructions below</li>
</ul>
</li>
  <li>If you’re using your phone, save the unique URL to a bookmark on your home-screen so you can open Remote gSender easily every time! Check out <a href="https://www.youtube.com/watch?v=UrlDJOY3i-8">this video</a> for details</li>
</ol>

<h3>Troubleshooting</h3>

If you ran into issues during remote control setup, here are some other checks you can make:

<ol>
  <li>The easiest checks to make sure remote mode works for you is to make sure you have gSender open, you have gSender connected to your CNC, and you’ve turned remote mode on</li>
  <li>Double-check your remote mode configuration menu, antenna icon, and IP address are showing on the inline computer</li>
  <li>Ensure both your computers / devices are on the same internet network and the IP numbers match on both devices</li>
  <li>Double check you took the right steps in the Firewall Setup section. Your inline computer might be blocking gSender’s ability to send information to the internet because of the firewall. On Windows, follow these steps to modify the firewall:
<ul>
  <li>Click Start and open your computer's Control Panel
  
  <img class="aligncenter size-medium wp-image-4325" src="https://resources.sienci.com/wp-content/uploads/2021/07/gSender-Headless-14a-control-panel-850x412.jpg" alt="" width="850" height="412" />{.aligncenter .size-medium}</li>
  <li>Open the ‘System and Security’ settings
  
  <img class="aligncenter size-medium wp-image-4288" src="https://resources.sienci.com/wp-content/uploads/2021/07/gSender-Headless-15-system-and-security-850x396.jpg" alt="" width="850" height="396" />{.aligncenter .size-medium}</li>
  <li>Open the ‘Windows Defender Firewall’ and go to its ‘Advanced settings’
  
  <img class="aligncenter size-medium wp-image-4320" src="https://resources.sienci.com/wp-content/uploads/2021/07/gSender-Headless-16a-windows-firewall-850x237.jpg" alt="" width="850" height="237" />{.aligncenter .size-medium}</li>
  <li>In the column on the left, click on ‘Inbound Rules’ and then find and double-click on ‘gSender’. There might be three options of gSender to click on, you’ll want to click on the version that has the word “All” under the ‘Profile’ column
  
  <img class="aligncenter size-medium wp-image-4291" src="https://resources.sienci.com/wp-content/uploads/2021/07/gSender-Headless-18-firewall-port-850x381.jpg" alt="" width="850" height="381" />{.aligncenter .size-medium}</li>
  <li>In the pop-up box, click on the tab labelled ‘Protocols and Ports’. Next to ‘Local port:’ you’ll want to use the drop-down menu to select “Specific Ports” and then type in the default port of “8000”. If you have added a custom port to gSender’s Shortcut properties, you’ll need to type in that number instead. Once you hit ‘Apply’, you can check to see if this resolved your problem.
  
  <img class="aligncenter size-medium wp-image-4328" src="https://resources.sienci.com/wp-content/uploads/2021/07/gSender-Headless-19a-gSender-firewall-port-850x502.jpg" alt="" width="850" height="502" />{.aligncenter .size-medium}</li>
</ul>
</li>
  <li>If when gSender reopens you’re met with a white screen, this means an error has occurred that we weren’t able to detect. This is rare, but unless we can find some other way to manage this the only fix is to uninstall gSender and reinstall it again.</li>
  <li>If on the remote device you get a popup for “Server Connection Lost”, this indicates that either gSender on the inline computer was closed or the shared internet is disconnecting. You should be able to fix this by restarting gSender on the inline device, then clicking “Attempt Reconnect” on the remote device.
  
  <img class="aligncenter size-medium wp-image-4329" src="https://resources.sienci.com/wp-content/uploads/2021/07/gSender-Headless-21a-reconnect-850x290.jpg" alt="" width="850" height="290" />{.aligncenter .size-medium}</li>
</ol>

<h2>About Page</h2>

You can find the release notes for the latest version of gSender in the “About” section of the settings.

<img class="aligncenter wp-image-5130 size-medium" src="https://resources.sienci.com/wp-content/uploads/2021/07/4.p36_gSenderAbout.jpg-850x593.png" alt="" width="850" height="593" />{.aligncenter .size-medium}

<h2>More</h2>

Check out this livestream if you'd like to see a super deep dive on gSender and all of its features as of 0.6.9. Chris spends a lot of time answering questions live about gSender and how to set up for a project:

[su_youtube url="https://www.youtube.com/watch?v=454pWYtZgBU"]

<span style="color: #ffffff;">End</span>