---
title: Problems / Bugs?
menu_order: 6
post_status: publish
post_excerpt: A list of common problems and fixes for gSender users as well as links through to submitting issues or finding more support through our forums or videos.
post_date: 2021-07-01 16:28:00
taxonomy:
    knowledgebase_cat: gdocs
    knowledgebase_tag:
        - gsender
custom_fields:
    KBName: gSender
    basepress_post_icon: bp-caret-right
skip_file: no
featured_image: _images/_gsender/_issues/gs_is_diagnostic-file.jpg
---

Having **troubles with gSender** or have **suggestions to improve it?** Follow these steps:

1. <a href="#questions-or-suggestions"><b>Questions</b> or <b>suggestions</b></a> are always welcome!
1. If you're **having a problem**, first help us out by ensuring that it's not an issue on your end with your computer or CNC. If you can try with another computer or g-code sender and still see the same problem then certainly let us know.
1. If you're sure about the issue, and have already checked our docs, <a href="https://www.YouTube.com/playlist?list=PLE43LQy2a1ioE8_sH0lcy8leYwrxvGhZ8" target="_blank" rel="noopener">YouTube playlist</a>, and <a href="https://resources.sienci.com/view/gs-feedback/#common-problems-amp-fixes">Common Problems &amp; Fixes</a> below, give us a hand by sending us **as much information as possible** so we can help diagnose your problem more easily.

## Information to Send

In order of importance, please collect together information of:

1. The **name and model of your CNC**, your computer **Operating system** (Windows, Mac, etc.) and **gSender version**
1. Please connect to your controller, try to recreate the issue, and as soon as it happens again create a '**Diagnostic PDF**' to send to us. If you can generate this shortly after the issue that's ok too, but it won't allow us to help you if you're not connected to your machine or you generate it too long after you had the issue happen. Find this by clicking on the **Stats tab** in gSender, then clicking the **Download Diagnostic File** button and saving it on your computer.
![](/_images/_gsender/_issues/gs_is_diagnostic-file.jpg){.aligncenter .size-full}
1. **Machine Firmware**, get this by going to the Config tab and looking to the bottom of the page. Here you will find another **Export** button to save the file to your computer.
![](/_images/_gsender/_issues/gs_is_diagnostic-export.jpg){.aligncenter .size-full}
1. Your **g-code file** if you're seeing the problem only with a specific file
1. Any other **pictures** or **videos** of the problem can also help us to help you faster

Please attach the files and information in your post / <a href="mailto:hi@sienci.com">email</a> to us.

## Questions or Suggestions

Send us the information, questions, or suggestions either on:

- The <a href="https://forum.sienci.com/c/gSender/" target="_blank" rel="noopener"><b>gSender Forum</b></a>
[![](/_images/_gsender/_issues/gs_is_gs-forum.jpg){.aligncenter .size-medium .flie}](https://forum.sienci.com/c/gSender/)
- <b><a href="https://github.com/Sienci-Labs/gSender" target="_blank" rel="noopener">Github page</a></b> (feel free to also submit PRs)
- You can join the discussion on secondary communities like our <a href="https://www.facebook.com/groups/gSender" target="_blank" rel="noopener">Facebook gSender Group</a>, and <a href="https://www.facebook.com/groups/mill.one" target="_blank" rel="noopener">Facebook CNC Group</a>, but we can't provide as much support or hear feedback in these groups.

## Common Problems & Fixes

We'll continue keeping our ears out for common stumbling points while using gSender and ensure we address them here for quick reference. If these tips don't help you, remember you can contact our support if you have a CNC from Sienci Labs or contact your own manufacturer's support for instructions on fixing your machine.

### Issues downloading or opening gSender

1. The main cause of this is usually a "virus protection" or Firewall software on your computer, or your computer system itself, thinking that gSender is 'unsafe' even though it's a proven software. In cases like these, first find the source of the blocking and then either make an exception for gSender or disable the blocking temporarily during download and installation.
   - An example of this is if you see "Windows cannot access the specified device, path, or file. You may not have the appropriate permissions to access the item."
   - For Windows-based computers you can read more on it here: <a href="https://support.microsoft.com/en-us/topic/-windows-cannot-access-the-specified-device-path-or-file-error-when-you-try-to-install-update-or-start-a-program-or-file-46361133-47ed-6967-c13e-e75d3cc29657" target="_blank" rel="noopener">https://support.microsoft.com/en-us/topic/-windows-cannot-access-the-specified-device-path-or-file-error-when-you-try-to-install-update-or-start-a-program-or-file-46361133-47ed-6967-c13e-e75d3cc29657</a>
1. If gSender used to open fine but after an update it suddenly doesn't, check here since the update might've gotten corrupted: <a href="https://resources.sienci.com/view/gs-installation/#gSender-updates" target="_blank" rel="noopener">https://resources.sienci.com/view/gs-installation/#gsender-updates</a> (scroll past the first picture)
1. If when you open gSender it gives you an error along the lines of "**Entry Point Not Found**", this means that you're trying to use a version of gSender past 1.2.2 with a 32-bit system. If you want to resolve this you'll either need to continue using a version of gSender 1.2.2 or earlier, or change to using a 64-bit system.
![](/_images/_gsender/_issues/gs_is_cm_32bit-error.jpg){.aligncenter .size-medium}

### gSender opens Slowly

This is usually due to your computers security software scanning gSender as it's trying to open. See this tip to help with that: <https://resources.sienci.com/view/gs-installation/#open-faster>.

### Screen goes Blank

If you find that gSender goes blank after you open it or while using it, there are a couple things you can try.

1. Try to close and reopen gSender. If it makes a black screen again, then close and open gSender again ➜ Go to the Config tab ➜ Export your **gSender Preferences** if you care about them and want to later reload them ➜ then "Restore Default settings". After doing this it's more likely you won't have an issue again.
1. If you're using gSender Edge, you'll see a toolbar at the top of the app where you can click: View ➜ Toggle Developer Tools ➜ then look at the 'Console' where if you find any errors you can share these with us. Also if you click: View ➜ Reload, you'll be able to refresh gSender to not show the blank screen anymore.
1. Otherwise if you're using the main version of gSender, you can try updating to the <a href="https://sienci.com/gSender/">latest version</a>.
1. Check your antivirus software or Windows Defender and add gSender as an exception.
1. Check to ensure you have read/write permissions for the preferences file
   1. Let's locate the file! It's called .sender_rc and can usually be found on your hard drive at: C:/users/{your username}/.sender_rc
   ![](/_images/_gsender/_issues/gs_is_cm_blank-rc.jpg){.aligncenter .size-full}
   1. Right-click on the file and choose properties. Under the security tab, check the name of your profile and confirm you have full control of the file.
   1. If not, select edit, choose your computer name, and grant permissions.
1. If you're still getting a blank screen, locate your log file and send it in to us. It's located at: C:/Users/{your user name}/AppData/Roaming/gSender/Logs/main.log

### Use gSender without a CNC

It's not easy for us to simulate how a real CNC will behave if you're not connected to one, but luckily there are some workarounds:

1. **Buy a cheap "Arduino Uno"**: this board is the 'brain' that runs many Hobby CNCs and can be easily found online or in some stores for around $10. Once picked up you can connect it to your computer over USB, <a href="https://resources.sienci.com/view/lmk2-grbl-firmware/" target="_blank" rel="noopener">flash Firmware onto it</a> to make it behave like a CNC, then you'll be able to connect to it in gSender. There are limitations such as not being able to home or probe (any sensor inputs) unless you manually short them together yourself; and this is because obviously you're not connected to a real CNC.
2. **Use a file simulator**: this won't let you pretend to run your CNC in gSender, but can simulate how a cut might turn out. You can <a href="https://resources.sienci.com/view/lmk2-visualizers/" target="_blank" rel="noopener">read more about these options here</a>.

### Connects but status says Disconnected

If your machine connects on a COM port successfully but the machine status says "Disconnected" then this is not an issue with gSender. A 'Disconnected' status means that gSender isn't able to recognize your CNC even though it can see it.

![](/_images/_gsender/_issues/gs_is_cm_connect-disconnect.jpg){.aligncenter .size-full}

1. Check that you have the right settings for your board, for instance click the Config tab ➜ Basics ➜ Baud rate dropdown, where most boards use 115200. Also your machine might not be supported yet by gSender if it isn't using grbl or grblHAL or your manufacturer edited the core firmware too much.
1. Your board may have a faulty connection. Try unplugging it then plugging back in, use a different USB cable, a different USB port on your computer, or plug the cable directly in if you were using a USB hub.
1. Your board might have other loose connections. Power off your machine, then use a non-conductive tool like a plastic utensil to push down on all 4 corners of your control board shield or Arduino. For the LongBoard you don't need to open it, just flip it upside down and you'll be able to access the Arduino through the slats on the bottom. Doing this will ensure that everything is fully plugged in since sometimes if the Arduino is slightly off the control board it can mess with its communication.
![](/_images/_gsender/_issues/gs_is_cm_push-uno.jpg){.aligncenter .size-medium}
1. Your board might have corrupted firmware. Re-flash your board if it's a [LongBoard](https://resources.sienci.com/wp-content/uploads/2021/07/gSender-Connected-but-No-Controls.pdf), [SLB](https://resources.sienci.com/view/slb-firmware-flashing/), or by following your manufacturers instructions.
1. At the least when you plug the board to your computer over USB you should hear a 'connection' sound from your computer. You should also see a new device appear under the Devices and Printers on your computer. If none of these are happening, then that means your computer isn't recognizing the board so you might want to look at drivers or getting further technical support.

### Port not Found (3018 CNC)

The 3018 and similar variations have been tested to work with gSender. Sainsmart points out in their documentation that sometimes an additional driver is needed for your computer to recognize the CNC via the USB port. They make this driver <a href="http://s3.amazonaws.com/s3.image.smart/download/101-60-280PRO/CH341SER.ZIP" target="_blank" rel="noopener">available for download here</a>.

In case this link stops working, the <a href="https://docs.sainsmart.com/article/x6sr565m5g-3018-prover" target="_blank" rel="noopener">associated documentation can be referenced here</a>.

For most of their machines they recommend using a 115200 baud rate, so double-check you're using that value as well.

### Port not Found

As long as your board is running normal grbl or grblHAL and you've selected the correct Baud rate in the settings then connection should be possible. Double-check that you're not connected to your machine elsewhere like with:

- Other senders like Easel, CNCjs, UGS, Lightburn (some programs might auto-connect so you might have to close them entirely)
- Pendants or offline controllers since typically a sender and controller can't be used at the same time
- Other programs like Arduino IDE or STMCubeProgrammer

We're still working on making gSender work best across all devices and one aspect of this is port detection for a variety of CNCs. If your CNC still isn't showing up on the port detector, we'd really like to hear from you.

One key bit of information that we need on our end is a picture or screenshot of your device information. You can get to this screen by:

1. Make sure your CNC is plugged into your current computer via USB
1. Open "Device Manager" in your Windows start menu
![](/_images/_gsender/_issues/gs_is_cm_device-manager.jpg){.aligncenter .size-medium}
1. Expand the "Ports (COM & LPT)" heading
![](/_images/_gsender/_issues/gs_is_cm_device-port.jpg){.aligncenter .size-medium}
1. Find the listing related to your CNC. This will be the one that disappears and reappears if you unplug your CNC and plug it back in. It'll also be the port you normally connect to on other g-code senders.
1. Right click that device and open "Properties"
1. Open the "Details" tab at the top
1. In the "Property" dropdown, select the "Hardware Ids" option
1. Send us a picture of the final view. An example of what that might look like would be:
![](/_images/_gsender/_issues/gs_is_cm_device-id.jpg){.aligncenter .size-medium .nar}

We appreciate your feedback, and with your help we'll make sure the next version of gSender recognizes your machine.

### CNC Profile is not listed

Much of the information that gSender needs about your CNC actually comes from its built-in EEPROM values, so the CNC profiles don't have any impact. This means that as long as your CNC is grbl-based, gSender should be able to control it just fine, even if it's not listed in the presets. Selecting the "Generic" preset will work just fine.

If some aspects of your machine don't seem right, it'll either be because your machine's manufacturer didn't flash your CNC with the appropriate EEPROM settings out of the box or they have some type of documentation which explains the values you need to change manually.

### UI does not fit on the Screen

![](/_images/_gsender/_issues/gs_is_cm_zoom-ui.jpg){.aligncenter .size-full}

We've always done our best to ensure that gSender is clear and easy to use across devices and across screen sizes too - but sometimes there are certain screens that gSender just doesn't suit. In these cases, we recommend you check the 'zoom' on your device until you can see everything clearly and can access all the buttons.

For **Windows**, see a [writeup with pictures here](https://resources.sienci.com/view/gc-setup-and-customizations/#how-to-change-the-display-scale-on-gcontrol) but otherwise the shortened version is:

1. Go to your Desktop, right-click it, the click '**Display settings**' from the menu.
1. In the Settings window, scroll down to the **Scale & layout** section.
1. Use the dropdown to choose the scale percentage that works best for you. It's likely that using **100%** will resolve your issue, but try other options if you need to make sure it works on your setup. Windows will automatically apply the new scale once you choose it.
1. Another option you can adjust is scrolling down to **Text size** on the 'Display settings' page, using the slider to adjust the text size to your preference, then clicking the '**Apply**' button.

For **Linux**: try reducing the app-specific display setting from 1.0 to 0.75 for example.

### File is Tiny in Visualizer

You're probably using the wrong post processor, go back and check what your CNC manufacturer recommends. By default it's best to use "grbl_mm" even if you like to use inches since most CNCs work in mm.

### Jogging not working or Errors

If you're seeing a message in the 'Console' tab saying "error: Bad number format", this is because you're running an older grbl machine (pre Grbl 1.1f). Contact your CNC manufacturer or look through their resources to see how you can upgrade your grbl firmware so that your machine can be fully supported by gSender. If you have a Sienci Labs machine, this is as easy as using the 'Flash' option in the **Config tab** in gSender.

Alternatively, you could be getting an error for 'soft limits'. If this is the case then either your machine limits have been set incorrectly or you didn't home your CNC when you first connected to it. Try homing your machine and trying again, and keep an eye out for if you're only having this issue in certain parts of your cutting area.

### Gamepad Error or Inconsistent Jogging

If you can't access your gamepad shortcuts or there's a problem with the profile, the easiest way to fix it is to delete the profile and remake it. This can suck depending on how much you customized it, and we'll keep working to make this process work better into the future.

If you can connect and jog with your gamepad but the jogging is sometimes unpredictable, then the problem might actually be the gamepad itself. Go to the Tools tab ➜ Gamepad ➜ Gamepad Profile ➜ and click the 'Help' button at the top right corner of the window. This will take you to a 3rd party Gamepad Tester website (that you can also visit at <a href="https://hardwaretester.com/gamepad" target="_blank" rel="noopener">https://hardwaretester.com/gamepad</a>) where you can try pressing buttons and moving joysticks to see if they're all behaving properly. If anything seems out of place then you might want to try using a different gamepad to control your CNC.

### Changes between "Running" and "Idle" during a Job

This is Normal. Sometimes there can be pauses or long changes in direction in the g-code that can make the machine state change in this way.

### Workspace changes during/after a job

If your g-code includes any workspace commands from G54 to G59, G59.1 to G59.3, or has an M2 or M30 command at the end of the program this will alter your selected workspace either to the one specified or revert it to G54. These commands affect how grbl stores the active workspace and so also affect the workspace stored by gSender. If you're experiencing this issue then you'll want to check your CAM post processor and ensure that it stops inserting these commands when you export your g-code jobs.

Alternatively, gSender's 'Start/Stop G-code' can also be equipped to sidestep problems with changing workspaces by saving the active workspace at the start of the program and then re-loading it at the end. This can be done with the commands `%global.state.workspace=modal.wcs` and `[global.state.workspace]` as shown in the picture below. Remember to 'Update Event' on both entries:

![](/_images/_gsender/_issues/gs_is_cm_workspace.jpg){.aligncenter .size-full}

### Changed $1 and Motors still Hold

This is a quirk of grbl boards where after changing this value you need to make a motor movement (a jog movement for example) before the new value will take effect.

### Many Little Lines on my Screen

This is something that can happen if you have certain graphics GPUs. To fix it you should be able to go to your GPU Control Panel, Manage the 3D Settings, and either turn off Image Sharpening or Hardware Acceleration.

### Weird colours/invisible buttons

If you've set up a Windows Accessibility theme on your computer it can negatively impact how gSender looks. We'd recommend you either turn the theme off, turn the slider down, or disable it just for gSender. We have your own high contrast 'Dark mode' that should work just as well for you if you go to Config ➜ Dark mode and turn it on.
