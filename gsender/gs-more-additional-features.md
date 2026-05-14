---
title: More gSender Features
menu_order: 1
post_status: publish
post_excerpt: Learn the advanced features of gSender such as shortcuts, macros, workspaces, calibration tools, controlling spindles, lasers, coolant, and more.
post_date: 2021-07-01 15:50:00
taxonomy:
    knowledgebase_cat: gs-advanced
    knowledgebase_tag:
        - gsender
custom_fields:
    KBName: gSender
    basepress_post_icon: bp-caret-right
skip_file: no
featured_image: _images/_gsender/_features/gs_fe_p1_KeyShort.jpg
---

This page covers all the advanced features of gSender such as shortcuts, macros, workspaces, calibration tools, controlling spindles, rotary axes, lasers, coolant, and more. Remember, you can always quickly navigate the page by clicking the headings in the 'Page Contents'.

## Wireless Control

If you've ever wanted to run your CNC without being stuck right next to it, this is the feature you're looking for. Once enabled, it will allow other devices on the same internet network to connect to the main computer that's running your CNC. These '**remote devices**' can be anything that can connect to the internet and run a web browser, meanwhile the '**inline computer**' plugs into your CNC with a USB or Ethernet cable and will receive commands over the internet from the remote device.

This feature is handy if you'd like to:

- Load in a file from your design computer outside your shop then run it on your computer inside the shop
- Use a tablet as the primary means of controlling your CNC rather than a mouse and keyboard
- Use a phone for occasional use when jogging or running functions
- Leverage a mini PC or Raspberry Pi as the inline (tethered) computer for cheap, fanless, and reliable operation without taxing them with a display, keyboard, and mouse (though this still doesn't create a fully 'headless' setup)

Before diving into the setup, here are some quirks and warnings that are important to keep in mind:

- Both systems need to be on the same internet network to work
- The '**remote device**' needs to be able to run a web browser
- The setup process can be a little more involved, so we don't advise using this feature if you're not confident with troubleshooting your own setup
- You may need to be an Administrator of the inline computer to make the changes needed
- If you intend to use this feature for more important projects or with expensive tools or materials, keep in mind that it will always be inherently less reliable than a hard-wired connection
- This feature is **NOT** intended to enable use of your CNC while **AWAY FROM YOUR WORKSHOP**. A CNC should always be run while you or another knowledgeable operator is in the vicinity to ensure safe machine operation and be able to react if intervention is required. CNCs can cause fires from electronics, material friction, and can have other safety hazards if not properly monitored.

### Wireless Setup

All setup steps need to happen on the inline computer (the computer you'll have connected via USB or Ethernet to your CNC) and have been simplified to mostly happen within gSender:

1. To begin, click the cell phone icon on the top right of the screen.
  ![](/_images/_gsender/_features/_remote/gs_fe_re_setup-access.jpg){.aligncenter .size-full}
1. This is where wireless control is set up. First, click the '**Enable Wireless Control**' toggle. Second, you'll see the boxes for 'Addr' (address) and 'Port' become available. The default values for these should work but if you have a particular setup or require troubleshooting then consider changing these.
  ![](/_images/_gsender/_features/_remote/gs_fe_re_setup.jpg){.aligncenter .size-full}
1. Once you click the 'Save' button, gSender will automatically restart in order for the changes to take place.
  ![](/_images/_gsender/_features/_remote/gs_fe_re_setup-restarts.jpg){.aligncenter .size-full}
1. You'll know the setup was successful if gSender restarts and the remote connect icon is green.
  ![](/_images/_gsender/_features/_remote/gs_fe_re_setup-dun.jpg){.aligncenter .size-full}
1. To connect with your '**remote device**', click the cell phone icon again to open the wireless control settings. If you plan to use a phone, use the camera to scan the QR code, and for any other device 'copy' the text at the bottom right  into the address bar of a web browser like Chrome or Edge. After the page loads, you should see a copy of gSender running in the web browser!
  ![](/_images/_gsender/_features/_remote/gs_fe_re_connected.jpg){.aligncenter .size-full}
1. If there was a problem during setup, then you might've encountered a firewall or unavailable port. Solutions to these are covered in the **[troubleshooting](#troubleshooting)** section.

### Using gSender Remotely

With setup complete, regular use is very straightforward:

1. As long as your 'inline computer' is on and connected to your CNC, and your CNC is powered on, then re-using the same text on the web browser of any device will give you access to a copy of gSender running fully remotely. Example text could look like this "192.168.68.155:8000" where for the phone interface it would have "/#/remote" added onto the end.
1. For phones and tablets, it can also be easy to re-use this webpage by saving it to a bookmark on your home-screen so you can open Remote gSender easily anytime you want! <a href="https://youtu.be/UrlDJOY3i-8">Check out this video</a> for details.
1. Once connected, you'll be able to control your CNC remotely with most of the same features and functions you’d normally expect:
   - Use both the remote and inline devices simultaneously to control your CNC like jogging, opening and closing files, probing, macros, and more
   - Notice that both their screens look exactly the same so you can watch the visualizer move around or check on the machine state
   - On phones the screen will look different since we've optimized it for jogging, setting zeros, and probing
   - When you click to 'load a file' you'll only be able to load files from the device you're currently on, don't expect to gain access to the files stored on the opposite device. However once the file is loaded into gSender, you'll be able to run it from any device.
   - There can be multiple remote devices all connected to the same inline computer at the same time to control your CNC from multiple devices. There can also be multiple inline computers controlled from the same remote computer, giving you multi-CNC control from the same device.
1. Some gSender-specific 'local' settings like won't carry over to the remote device so if you want to make sure files are run the same way every time you'll need to transfer your gSender settings over by following the ['Transfer Settings' instructions](#gsender-preferences)

### Troubleshooting

If you ran into issues during remote control setup, here are some checks you can make:

1. Make sure you have gSender open, have gSender connected to your CNC, and you've turned wireless control on
1. Ensure both your computers / devices are on the same internet network and the IP numbers match on both devices
1. If on the remote device you get a popup for "Server Connection Lost", this just means that either gSender on the inline computer was closed or the shared internet is disconnecting. You should be able to fix this by restarting gSender on the inline device, then clicking "Attempt Reconnect" on the remote device.
![](/_images/_gsender/_features/_remote/gs_fe_re_issues-conn-lost.jpg){.aligncenter .size-medium}
1. If there was a problem using the specified IP address or Port, you'll get an error window to let you know. In this case you should be able to reopen gSender, go back to the Wireless Control settings, and try another IP or Port until the setup is successful. Common port values are 3000, 8000, and 8080 and generally don't go below 1024 since those are considered privileged. Changing IP addresses can also help if you're running a VPN or need a different internal IP to external IP mapping.
  ![](/_images/_gsender/_features/_remote/gs_fe_re_setup-ip-error.jpg){.aligncenter .size-medium}
1. If you have a Windows Security Alert window pop up during setup, it means your inline computers firewall isn't allowing gSender to communicate to other devices on your network.
   - Check the boxes beside "Private networks" and "Public networks" and click the 'Allow access' button
   ![](/_images/_gsender/_features/_remote/gs_fe_re_firewall-windows0.jpg){.aligncenter .size-full}
   - If you don't see this popup, click Start and open your computer's Control Panel
   ![](/_images/_gsender/_features/_remote/gs_fe_re_issues-control-panel.jpg){.aligncenter .size-medium}
   - Open the 'System and Security' settings
   ![](/_images/_gsender/_features/_remote/gs_fe_re_issues-security.jpg){.aligncenter .size-medium}
   - Open the 'Windows Defender Firewall' and go to its 'Advanced settings'
   ![](/_images/_gsender/_features/_remote/gs_fe_re_issues-firewall.jpg){.aligncenter .size-medium}
   - In the column on the left, click on 'Inbound Rules' and then find and double-click on 'gSender'. There might be three options of gSender to click on, you'll want to click on the version that has the word “All” under the 'Profile' column
   ![](/_images/_gsender/_features/_remote/gs_fe_re_issues-inbound-rules.jpg){.aligncenter .size-medium}
   - In the pop-up box, click on the tab labelled 'Protocols and Ports'. By 'Local port:' you'll want to use the drop-down menu to select "Specific Ports" and then type in the default port of "8000". If you have added a custom port to gSender's Shortcut properties, you'll need to type in that number instead. Once you hit 'Apply', you can check to see if this resolved your problem.
   ![](/_images/_gsender/_features/_remote/gs_fe_re_issues-port.jpg){.aligncenter .size-medium}
   - On newer devices you might alternatively need to go to your Windows security tab, and click the Allow an app through firewall text.
   ![](/_images/_gsender/_features/_remote/gs_fe_re_firewall-windows1.jpg){.aligncenter .size-medium}
   - Scroll down until you see gSender, click on Change Settings, then enable gSender to communicate through the firewall by clicking the checkbox.
   ![](/_images/_gsender/_features/_remote/gs_fe_re_firewall-windows2.jpg){.aligncenter .size-medium}
1. If on Mac, Linux, or Pi you find that you can't connect with outside devices or just want some extra safety you might want to try opening the Universal FireWall (UFW) on a given port to allow external access. This can be started with `sudo ufw enable` (if UFW is not found then install it using `sudo apt-get install ufw` and your root password) then opening the desired port, for example `sudo ufw allow 8080` opens port 8080 for external access. If you want to see what ports are already open, you can use `ufw status verbose`.
1. If when gSender reopens you're met with a white screen, this means an error has occurred that we weren't able to detect. This is rare, but unless we can find some other way to manage this the only fix is to uninstall gSender and reinstall it again.

## Macros

Macros are standalone buttons within the gSender interface that allow you to execute a series of g-code commands when they're run. Macros can come in handy for a variety of uses:

- Button to run a v-carve or laser engraving of a common insignia into the back of your wood pieces
- Perform a specialized probing function for a particular jig you've set up
- Apply a predetermined offset that allows you to easily array your cutting jobs

You can create macros using the '+' button under the 'Macros' tab.

![](/_images/_gsender/_features/_macros/gs_fe_ma_macros1.jpg){.aligncenter .size-medium}

Here you'll see a space for inputting your custom g-code and adding a name and description for the macro. Advanced users may also want to leverage 'Macro Variables' which allow for greater g-code manipulation and pseudo-programming. Press 'Add New Macro' when completed.

![](/_images/_gsender/_features/_macros/gs_fe_ma_macros2.jpg){.aligncenter .size-medium}

New macros will appear as buttons in the 'Macro' tab that can be rearranged by dragging them around. These buttons will display the macro name, show the description if you hover your mouse over them, and can always be later altered or deleted by clicking on their '...' button.

![](/_images/_gsender/_features/_macros/gs_fe_ma_macros5.jpg){.aligncenter .size-medium}

Any macro can be run by pressing it. Once running, you should see the macro start to pulse green while a toast notification on the bottom right hand side of gSender also notifies you that it's running.

![](/_images/_gsender/_features/_macros/gs_fe_ma_macros3.jpg){.aligncenter .size-medium}

Macros can also be ran using shortcuts. Every time you create a new macro it'll become available on the shortcuts list for you to assign a key or gamepad button to. Add your keybindings and press the Active toggle to enable the shortcut.

![](/_images/_gsender/_features/_macros/gs_fe_ma_macros31.jpg){.aligncenter .size-medium}

You can share macros with other users or transfer them between computers by using the import and export features. **To import one or multiple macros, just press the button on the left** and a browsing window will appear so that you can select the macros you wish to import. Similarly, **to export all your current macros, press the button on the right** and it'll open a save window, to generate a save file for you.

![](/_images/_gsender/_features/_macros/gs_fe_ma_macros4.jpg){.aligncenter .size-medium}

### Advanced Macros

gSenders Macro architecture is based on **JavaScript** and uses the Esprima library (<a href="https://esprima.org/" target="_blank" rel="noopener">https://esprima.org/</a>) and so will theoretically support any code that it does. This is exciting because Macros can move far past basic variables if you'd like to perform advanced functions on your CNC:

If you want some initial inspiration, see other macros [**made by our community**](#community-macros) or ones <a href="https://github.com/cncjs/CNCjs-Macros/blob/master/Hole_Center" target="_blank" rel="noopener"><b>made for CNCjs</b></a> (another g-code sender) which should also work in gSender. Otherwise, here are some other points of guidance:

1. You'll want to develop your understanding of typical <a href="https://linuxcnc.org/docs/html/gcode/g-code.html" target="_blank" rel="noopener">g-codes</a> and <a href="https://linuxcnc.org/docs/devel/html/gcode/m-code.html" target="_blank" rel="noopener">m-codes</a> that are used for CNC control (the pages linked are very good sources for that)
1. The "Macro Variables" dropdown in gSender shows many of the most commonly used operations when making your own macro
1. Make your own variable with `%variable = value_you_want_to_set` (ex. % probeSpeed = 150)
1. Use your variable in g-code, like `G21 G91 G0 X[variable]` (moves the X-axis by the amount set in the variable)
1. Test your code by printing it to the console `([variable])`
1. Make dialog boxes appear on the screen to confirm a value or position by putting in an M0 line with a comment, for example `M0 ;Remember to turn on your router before the next step` which will pause the macro and give you the option to 'continue' or 'cancel'
1. Start experimenting with basic math using numbers and variables like `%combo = (variable + variable2 + 4)/2` (Hint: you don't need square brackets around variable names when the line starts with `%`, <a href="https://forum.sienci.com/t/macro-gcode-question/21399/6" target="_blank" rel="noopener">explanation</a>)
1. Use global variables `global.variable` if you want variables that you can use in other macros (note that these get reset once gSender is closed)
1. Read up on all the other Math features available like <a href="https://developer.mozilla.org/en-US/docs/Web/JavaScript/Reference/Global_Objects/Math" target="_blank" rel="noopener">absolute value, rounding, and trigonometry</a> (become very useful for more advanced probing cycles for example)
1. Start to add more logic to your code using ternary expressions to choose between two outcomes (e.g. `%variable = (30 > 20) ? 10 : 20` which is checking if 30 is bigger than 20, and if it is it'll make the variable = 10, otherwise it'll make the variable = 20).
1. Here's an example of a more advanced macro, made by gSenders Lead Developer, which shows off much of the guidance given above. This macro was made for our new <a href="https://sienci.com/product/slb/" target="_blank" rel="noopener">SLB control board</a> in order to cycle between its 3 <a href="https://resources.sienci.com/view/slb-manual/#status-lights" target="_blank" rel="noopener">status light states</a>.
   - The macro is only 3 lines. First it checks what the current light state is and sets it to 0 if it doesn't have a state. Next, it sets the lights to the current state but applies a modulus of 3 since we can only have a state value of 0, 1, or 2 so we'll get an error if the value is 3 or above. Lastly, it adds +1 to the state so that if the macro is run again it'll put the lights into a new state.
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

### Community Macros

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

<b><span class="redText">Disclaimer!</span> These Macros are submitted by our community. They aren't vetted by us and might cause damage to your machine so use them at your own risk!</b> Please review the code and test it before assuming it will work with your machine setup.

[su_spoiler title="<b>Bump Z-axis zero down</b>" open="no" style="fancy" icon="chevron" anchor_in_url="yes"]
**Author:** Chris T.<br>
**Updated:** Jan 5, 2026

**Description:** For when you're doing very precise carving and want to tweak the Z-axis zero slightly without taking a while to type in a new value or re-zero. Only works if you’re in the default G54 workspace, would require some more changes if you want it to intelligently work in other workspaces.

**Code:**

```js
G10 L20 P0 Z[posz + 0.1]

//if you'd like to do this in imperial, use the code below
%newPos = [posz/25.4 + 0.004]
G10 L20 P0 Z[newPos*25.4]
```

[/su_spoiler]

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

## Console

The console is a tab that you can access at the bottom right hand side of the gSender window. The text here shows a truer representation of the communication that happens between your computer and your CNC. As you start to understand more about your machine, this is a great tab to reference so you can see if commands are being properly sent, received, and executed. It's also great for troubleshooting since you can:

- Manually send g-code commands to your CNC
- Check for errors or alarms and the g-code that caused them (normally the line that comes before)
- Copy text straight from the console to send in an email for help by clicking the '...' button next to 'Run', then clicking 'Copy last 50 lines'.
- Even open the console in another window by pressing the top, right icon to help you see more console text at a time (if you press the button again once you reconnect to your CNC, it'll reconnect the console stream to the original window too)

![](/_images/_gsender/_features/gs_fe_console-tab.jpg){.aligncenter .size-full}

When you first start up gSender, the console will display EEPROM settings that are sent from the Arduino in the control box. These EEPROM settings control parameters for your CNC such as:

- Maximum speed and acceleration in each axis
- Boundaries of the work area
- Direction of each axis movement
- Limit switch settings

To access EEPROM settings again, enter in “$$” into the console and hit the 'Enter' key or click the 'Run' button. These settings can be changed via the console as well as the Firmware Tool which we've designed as a much more visual way to alter machine settings.

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

The g-code for tool changing is an M6 command. gSender is quite capable when it comes to customizing CNCs for tool changing, even having full Wizards built-in. The tool change options are in Config ➜ **Tool Changing**. You can select from one of 6 different options, and even choose to 'passthrough' the M6 and T commands to the CNC controller for CNCs that are capable of handling tool changes on their own.

![](/_images/_gsender/_features/_toolchange/gs_fe_toolchange.jpg){.aligncenter .size-full}

You can **Ignore** any M6 tool change commands, **Pause** the job when a tool change is recognized, or select one of the **Wizards** that will guide you through pre-set tool changing methods. In the image below, you can see an example of the Helper window opening up to show the **Standard Re-zero Wizard** with all of its guided steps.

![](/_images/_gsender/_features/_toolchange/gs_fe_toolchangewiz.jpg){.aligncenter .size-medium}

If you are using one of the wizard options, know that you can access all other gSender controls while the wizard is open like jogging and zeroing. It also has flexibility to go back a step if you missed something or had a mistake, or to be minimized temporarily if you want to check the visualizer.

1. **Ignore**<br>This simply ignores any M6 commands in the g-code file. This is the default option since it's perfect for beginners that only make projects with one tool or those that create separate files for each tool and prefer to manually perform tool changes between files.
1. **Pause**<br>Pauses gSender at the tool change point, as if you had hit the pause button manually. This gives you freedom to jog, zero, or anything else you'd like, and is great for those that are running multi-tool files but want to use a different process than the Wizards provide. This could be a manual probing process, a different tool changing approach, or running custom macros to support your machines specific hardware. gSender is compatible with tool length sensors like the Carbide 3D bitsetter, and our community has compiled a <a href="https://forum.sienci.com/t/bitsetter-and-other-tool-length-sensors-supported-in-gSender/3877/4">list of macros</a> for tool changing that you can use when you are paused. Just note that pausing can't always guarantee keeping track of your movements and actions when it comes time to resume the job so try to ensure you get back to the starting point and set zeros correctly.
1. **Standard Re-zero** (Wizard)<br>Titled 'standard' because it's exactly the same as the standard process you might normally follow for running a file, changing the tool, re-zeroing Z, then running the next file except it's applied to a single file with multiple toolpaths. Since the process is so familiar, this is a great way to dip your toes into tool changing within one file. Compatible with using a touch plate or the paper method, zero out at a predetermined spot (usually at the front left corner), and use jogging to move around. The advantage of introducing this extra automation and guidance during tool changes is that you don't have to worry about custom macros and it reminds you of simple steps like turning the router back on or zeroing Z.
1. **Flexible Re-zero** (Wizard)<br>Similar to the 'standard' wizard with similar steps and manual movements but provides the ability to zero Z off a point that wasn't your starting Z when it comes time to change the tool. This is useful if you tend to carve away your material and lose the starting Z or you don't have limit switches but would like a process similar to a tool length sensor.
1. **Fixed Tool Sensor** (Wizard)<br>This is the most automated setting where all probes and movements are done for you, you only need to intervene by changing the tools. Set up the job and zero normally then expect the machine to move to the sensor location when it reaches a tool change, verify tool length, prompt for a change, probe new tool, then resume cutting. Your machine will need to be homed, have limit switches, and have a tool length sensor (compatible with Carbide 3D bitsetter for example) in order for this option to work. To set up the sensor mount the router/spindle as far down as you might typically put it, with the longest bit mounted in it, then jog it to hover over the tool length sensor with some room to spare and open Config ➜ **Tool Changing** to **Grab** that location, then apply the new settings. This will be the spot your machine moves to every tool change so if it's too low or your sensor doesn't work it'll run into the sensor. You can also enter these coordinates manually, and test them with the **Go To** button.
  ![](/_images/_gsender/_features/_toolchange/gs_fe_toolchangefixed.jpg){.aligncenter .size-full}
1. **Code**<br>You can enter your own macros before and after the tool change with this strategy selected which is fairly powerful for making tool changing processes that are more automated than just pausing.
  ![](/_images/_gsender/_features/_toolchange/gs_fe_toolchangecode.jpg){.aligncenter .size-medium}

You can also learn more about how some of this works by checking out this user-made video by SparksTech!

https://youtu.be/kyu2RsZaUA4

## More

There's always more to learn about gSender including many videos of lesser-known tips, setups on different CNCs, and open source modifications people have made. For example, check out these videos of Chris showing off some common and less-common tips about how to improve your gSender experience!

https://youtu.be/md_iU6Sgi6k

https://youtu.be/hJfGpHq0Hr0
