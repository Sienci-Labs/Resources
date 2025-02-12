---
title: ytsb CNC Issues & Fixes 🩹
menu_order: 9
post_status: draft
post_excerpt: LongMill troubleshooting guide, to address stalling motors, skewed movement, faulty power switch, connectivity, touch probing, missing parts and much more.
post_date: 2022-03-17 20:47:00
taxonomy:
    knowledgebase_cat: lmk2-handbook
    knowledgebase_tag:
        - mk2
custom_fields:
    KBName: LongMill MK2 CNC
    basepress_post_icon: bp-caret-right
skip_file: no
featured_image: 
---

This part of the resources covers common issues and fixes for the LongMill. If you run into an issue with your machine, we hope that this can help you diagnose and fix problems to get you milling as quickly as possible. If you can't find the answers here, please feel free to get in <a href="https://sienci.com/contact-us/technical-help/" target="_blank" rel="noopener">touch with us</a>.

## Assembly issues

### I am missing or cannot find a part

Every LongMill is packed in our shop in Waterloo, ON by our team of trained staff. Every package goes through several checks to ensure that the correct parts and quantities are in each kit, but we sometimes make mistakes. If you can't find something, please reach out to us and we'll make it right. However, before <a href="https://sienci.com/contact-us/technical-help/" target="_blank" rel="noopener">reaching out to us</a>, there are a couple things you can check.

- Ensure that you are following the assembly instructions for the correct version of the machine. There are variations between versions, including the packing order and assembly. More info can be found in the <a href="https://resources.sienci.com/view/lm-unboxing/">Unboxing</a> portion of the resources. **Please note that our video instructions are based on the Version 2 design.** Instructions from the video can still be referenced for additional help in assembling your machine.
![](/_images/_longmill/_assembly/_commonissues/lm_commonissues_p_Versions.png){.aligncenter .size-medium}
- If you're missing the correct amount of hardware, you may find it in another bag. Please check in the rest of the kit to make sure all of your hardware is accounted for.
- Some parts and add-ons, such as the t-tracks come in a separate package as the LongMill kit. If your order is larger than what can be fit in the LongMill kit, it may come in more than one package.

### My Delrin anti-backlash nuts will not thread on

During the assembly process, the anti-backlash nuts may be difficult to thread on, especially when threading between the base and the arm portions of the block. These nuts rely on the threads to line up for proper movement.

- The alignment of the threads can be tensioned by turning the set screw or M5 screw, **or pressing the arm down to help the threads line up while threading in the lead screw**. Once the lead screw has been threaded on, it can be tensioned by following our <a href="https://resources.sienci.com/view/lm-maintenance/">maintenance guide</a>
- Slightly loosen the two M5 bolts that hold the nut to the gantry. Over tightening the screws can crush the ACME threads, causing additional friction between the lead screw and nut.
- Try threading your lead screw in from both directions. It may be easier to line up the threads from one direction over the other.
- Check for burrs and debris that may be in the threads.
![](/_images/_longmill/_assembly/_commonissues/lm_commonissues_p1_PressNut.jpg){.aligncenter .size-medium}
![](/_images/_longmill/_assembly/_commonissues/lm_commonissues_p2_NutDiagram.jpg){.aligncenter .size-medium}

### I have leftover parts after assembly

When you get to the end of the building process, you may be left with a small handful of extra parts.

Don't worry, we supply extra additional parts so that

- If a part doesn't work properly, the extra one can be used instead.
- If you lose something (especially those screws), you still have plenty of extra.
- We reduce the chance of packing too few of a certain part.
- If you have a 12x12 or 12x30 LongMill, you can upgrade to a 30x30 at a later date.

## Motor and controller issues

### My controller is not turning on

First ensure that your LongMill's power supply cable is connected to the wall and power brick correctly and that the green LED is lit up on the power supply brick. If you have an E-stop, check that the button is released by twisting it counterclockwise and if you have a power switch, ensure it's toggled on.

Other things you can check:

- If the red light on the controller top (newer versions) or on the drivers (visible through the grates on the underside of the controller) are on, then you are getting power to the controller. You may be having issues with connecting your machine to the computer.
- Make sure that the polarity of the power wiring is correct. Switch the wires around if need be (see picture).
- If you have a older power switch model and the red LED lights  flicker or turn off right when the power switch is turned on, you may have a faulty switch. Please contact us.
- If you have a newer E-stop model, check that the E-stop is plugged into the **top** of the LongBoard, and the power supply is plugged into the **side** of the LongBoard. <a href="https://drive.google.com/file/d/10I-XiU6GuIwgeMfRe_LBDjoDTnmqmISy/view?usp=sharing" target="_blank" rel="noopener">View the correct installation here.</a> You can also check that the wiring is secured inside the E-stop itself by unfastening the 4 screws on the lid with a screwdriver. There should be two wires secured on either terminal (polarity doesn't matter).
![](/_images/_longmill/_assembly/_commonissues/lm_commonissues_p3_Polarity.jpg "The wire on the left should be white, and the wire on the right should be black.")

### One motor does not move or moves erratically

When jogging or running the LongMill, one of the motors does not move correctly or at all.

- Check that both the plugs on the controller side and the motor side are connected properly. We recommend completely disconnecting the plug and plugging it back in.
- Check that all of the wires on the plug are connected and secure.
- If your motor does not move at all, try switching and testing if it is working correctly by plugging it into a different axis on the motor controller. If the motor moves on a different axis, then you can confirm that the motor is working correctly and identify that there may be an issue with the controller.
- Check that the light on all of the drivers inside the control box are illuminated. If you have a driver that is not illuminated, please contact us for additional support.
- Check that all of the <a href="https://resources.sienci.com/view/lm-electronics/" target="_blank" rel="noopener">DIP switches</a> are properly seated in the correct orientation. If the switch is only part of the way on or off, the driver may not operate.
- If one y-axis motor moves but the other doesn't. Switch the y connectors. If the issue moves to the other side, it might be the driver is supplying the wrong amount of current. Follow these <a href="https://resources.sienci.com/wp-content/uploads/2022/06/Stepper-Driver-Current-Adjustment.pdf" target="_blank" rel="noopener">instructions</a> to make adjustments.
- Make sure your Arduino is fully seated in your control board. You can typically use a non-conductive tool to push it into the socket if it is starting to come loose.
![](/_images/_longmill/_assembly/_commonissues/lm_commonissues_p4_ControlBoard.jpg){.aligncenter .size-full}

### Machine is moving the wrong direction

- Ensure that all plugs and cables are fully seated and connected properly. Check the other plugs for reference.
- Check the colour pattern of each wire coming from the motor and connected to the LongBoard. Is the pattern the same with each motor? If not, change the order of the wires to match.
- Reload the EEPROM settings on your Arduino, as these settings may have changed when using various g-code senders. These settings control aspects such as the jogging direction and the machine’s work space boundaries. To access them, go to the Firmware tool in gSender, or the Firmware Settings in UGS. gSender will have the ability to "Restore Defaults" and revert to the LongMills factory settings. For UGS, make sure you have the default settings (found <a href="https://resources.sienci.com/view/lm-EEPROM-settings/" target="_blank" rel="noopener">here</a>) by going through each line and manually changing the values, or download the configuration zip file, unzip it, and load it into UGS.
![](/_images/_longmill/_assembly/_commonissues/lm_commonissues_p5_Wiring.jpg "The wiring colour pattern should be blue, yellow, green, red."){.aligncenter .size-medium}
![](/_images/_longmill/_assembly/_commonissues/lm_commonissues_p6_USGEEPROM.png "Where to find the EEPROM settings on UGS Platform."){.aligncenter .size-medium}

### Machine is not moving the correct distance

- The microstepping on your drivers may not be set correctly. Check the drivers under your machine and make sure that they are set to 1/8" <a href="https://resources.sienci.com/view/lm-microstepping/" target="_blank" rel="noopener">microstepping</a> by ensuring that the DIP switches are in the correct position.
- Your coupler may be slipping. Ensure that the screws on your coupler are fully tightened.
- Try restarting your g-code sender.

### Motors are stalling

- Make sure that all of the motor wires are seated properly.
- Make sure that you have not over-tightened the Delrin anti-backlash nuts on your machine as this can distort the threads that run on the lead screw. Loosen the two M5-25mm screws that hold the nut in place and see if that helps.
- Ensure that the couplers are secured onto the motor shaft and lead screw with the set screws. If the coupler is slipping and requires re-tightening often, there is a possibility that the coupler threads are stripped.
- Re-flash the Arduino with the firmware to ensure that the code on the Arduino hasn't been altered somehow. Since the Arduino acts as the "brains" of the control board, it can affect how the motors are running. The instructions for flashing the Arduino are found here: <a href="https://resources.sienci.com/view/lm-grbl-firmware/" target="_blank" rel="noopener">https://resources.sienci.com/view/lm-grbl-firmware/</a>

### Y-axis is skewing (one side moves further than the other)

- Run the machine to the back until you hear a grinding noise, this will realign your y-axis gantries to be square with the X-axis. See if the issue is still persisting by jogging back and forth, moving through the entirety of the Y-axis travel.
- Power off the machine. Using your hands, turn each Y-axis lead screw a few rotations, checking that they are difficult but not impossible to turn and that they are equally hard to turn.  If that is not the case, adjust by slightly loosening the fasteners in the anti-backlash nut with an Allen key (both the mounting screws and the single screw sticking out). Keep checking and adjusting the lead screws until they are equal and difficult to turn by hand.
- The microstepping on your drivers may not be set correctly. Check the drivers under your machine and make sure that they are set to 1/8" <a href="https://resources.sienci.com/view/lm-microstepping/" target="_blank" rel="noopener">microstepping</a> by ensuring that the DIP switches are in the correct position.

## Cutting Issues

### Cuts are not coming out accurately

- Try reducing your speeds and feeds, or use a different cutting tool.
- Check that there is no dust in the collet of your router so that the bit does not slip in the collet during operation.
- You may have a loose component. Make sure that all of your fasteners are tight and your eccentric nuts and Delrin anti-backlash nuts are tensioned correctly.
- Your motor or lead screw may be slipping inside the coupler. Ensure that the coupler is fully tightened and pressed firmly against the flange bearing to eliminate movement axially.

### Cuts on the Z-axis are not the correct depth

- Ensure that the set screws on the two pulleys on the Z-axis assembly are tight and the belt is tensioned. The Z-axis lead screw should not be able to slide up and down.
- Ensure that the LongMill has enough travel on the Z-axis for it to cut deep enough. It may be bottoming out.
- If your LongMill is bottoming out, lower the position of your router or use a longer end mill. The LongMill comes with two set of holes on the Z-axis gantry plate for placing the router mount (upper and lower), and using the lower mount position on the Z-axis may work better.

### Lead screws wobble excessively

Excessive wobble is when the lead screw is deviating from center by more than about 3mm or 1/8". This means that butting a measuring tape or ruler against the LongMill wasteboard and recording down the height of the lead screw at its lowest point, and then again at its highest point, should result in a difference in the two measurements of no more than 6mm or 1/4". Wobble can happen due to a loose lead screw or due to the screw being physically bent: if it's bent then the wobble will happen at any movement speed, whereas if it's loose then it will wobble mostly at higher movement speeds (above 2000mm/min).

- **Loose screw:** loosen the two M5-25mm screws that hold the Delrin anti-backlash nuts slightly for the axis which the lead screw is on and run the machine back and forth. This will align the lead screw and the nut. Re-tighten the screws once the wobbling as gone away. Also check the ACME locking nut and coupler on both ends of the screw are firmly tightened and sandwiching the lead screw properly.
- **Bent screw:** a sure way to confirm is to completely remove the screw and roll it along a surface that is very flat to see if it rolls evenly.

### The machine moves really slowly or not at all when I jog it

- If you are jogging your machine for the first time, your feed rate may be set to 10mm/min. This means it will only move 10mm in one minute (really really slow). Try increasing the speed until it is perceptible. 1000mm/min is a good place to start.
- If you are running code or a job, make sure that your feed rates are set correctly.

### Machine is cutting lines into my project

- If you have the 'homing cycle' enabled in your firmware settings, any 'G28' command used for a safe retract height will cause the machine to move to it's Z-axis home position. If you have not homed the machine before this command is called, the Z-axis may not lift high enough, or plunge into the work material. With the 'homing cycle' disabled, gSender will automatically ignore these 'G28' commands and will lift the Z-axis to a clearance height instead.
- If you are using Fusion 360, ensure that ‘Safe Retracts’ is set to ‘Clearance Height.’
![](/_images/_longmill/_assembly/_commonissues/lm_commonissues_p7_f360.png){.aligncenter .size-medium}
- Ensure that you are not hitting the Z-axis movement limits when running the job.
- Review the g-code with a visualizer (<a href="https://ncviewer.com/">https://ncviewer.com/</a>) to ensure there are no unexpected toolpaths or incorrect g-code commands.
- Check all the transmission components (V-wheels, couplers, ACME nuts, anti-backlash nuts, pulleys)
  - Pulleys, couplers and ACME nuts are secured and in the correct position.
  - Belt in the Z-axis is tensioned
  - Anti-backlash nuts are not mounted too tight; you can loosen the two M5-25mm screws that hold the nut in place and see if that helps.
  - Eccentric nuts are adjusted so that V-wheels are tight on the rail but are still able to turn by hand.

### My machine randomly stops and starts

- Check if your power supply and all of the connectors are secure and properly attached.
- Ensure that your computer has completed all Windows/Mac updates. The serial communication through the USB drivers on your computer can be affected by the updates pushed by your operating system.
- Look for sources that may be causing electromagnetic interference (EMI). This could be vacuums, motors, and other electronics nearby that could be sending EMI to the control board.
- Try connecting the control box to a different breaker than the router and vacuum in case a brown out is happening with your control box.
- Check if your drivers are excessively hot. The drivers should not exceed 80C.

### My machine stops cutting / loses connection on long jobs

Loss of connection on a long job can happen if your computer or USB port 'fall asleep' on you. If you plan on running long, intricate cuts on your CNC you'll have to change your computer power settings so that it 'stays awake' while cutting. Iif you're using a Mac computer, you can find dedicated instructions for sleep management here: <a href="https://support.apple.com/en-ca/guide/mac-help/mchle41a6ccd/mac" target="_blank" rel="noopener">https://support.apple.com/en-ca/guide/mac-help/mchle41a6ccd/mac</a>.

- Click the **Windows** icon at the bottom left corner of your screen and start to type "<em>control panel</em>" to bring it up
![](/_images/_longmill/_assembly/_commonissues/lm_commonissues_p8_p1.png){.aligncenter .size-medium}
- Once you've clicked to open it, go to **Hardware and Sound** then **Power Options**
![](/_images/_longmill/_assembly/_commonissues/lm_commonissues_p9_p2.png){.aligncenter .size-medium}
![](/_images/_longmill/_assembly/_commonissues/lm_commonissues_p10_p3.png){.aligncenter .size-medium}
- Now, whichever plan you have currently selected (circled in the picture) will be the one that you want to click **Change plan settings**
![](/_images/_longmill/_assembly/_commonissues/lm_commonissues_p11_p4.png){.aligncenter .size-medium}
- Go to the second drop-down and set it to **Never**, save the changes to ensure that your computer never dozes off on its own. An additional step can be to stop your USB ports from 'sleeping' by clicking **Change advanced power settings**
![](/_images/_longmill/_assembly/_commonissues/lm_commonissues_p12_p5.png){.aligncenter .size-medium}
- In the separate window that appears, you'll want to Expand the **USB Settings**, then **USB selective suspend setting**, and finally change this drop-down to "**Disabled**". Click to **Apply** these new settings. **!!** Sometimes on a Windows update these settings will be reset, if you want to make sure you've got all your bases covered, be sure to check back on these settings on occasion if you want to feel confident while running long jobs. !!
![](/_images/_longmill/_assembly/_commonissues/lm_commonissues_p13_p6.png){.aligncenter .size-medium}

### My bit is crashing into the touch plate

If you’re using UGS:

- There is a bug that can cause the touch plate to move farther than the expected origin and plunge the bit into the work surface if you use INCHES units when jogging around. If so, before beginning the probe process ensure that you have set the jog control to MM instead of INCHES. Once probing is completed, you may switch back to INCHES and resume regular machine operation
![](/_images/_longmill/_assembly/_commonissues/lm_commonissues_p14_UGSbug.png "Jog control unit setting on UGS"){.aligncenter .size-medium}

If this was not the problem:

- Check that the bit you are using is not tapered and is conductive at the both its sides and end so that it can make electrical contact with the touch plate.
- Ensure the settings you use are from the touch plate page on our website (not the settings in the video): <a href="https://resources.sienci.com/view/lm-touch-plates/" target="_blank" rel="noopener">https://resources.sienci.com/view/lm-touch-plates/</a>
- Make sure your work coordinates match your touch plate settings (usually G54)
- Check that there's proper electrical contact from your control box through to your magnet and touch plate. An easy way to check this is to run a Z probe with the router high up in the air and manually tap the magnet to the plate while they're held in each of your hands. If the bit stops and raises slightly up then lowers down again, this should indicate some form of connectivity from the magnet and touch plate to the control box. If you tap them together again, this should conclude the probing process and no errors should appear. If you don't observe this behaviour, then you should try this test again and if it again shows an error then check the electrical connections. See if the magnet is making contact with the metal leads of the wire by unscrewing the fastener in the centre and do the same for the banana plug as well. You may need to strip more insulation off the ends of the wire to get more contact with the metal surfaces. There’s a great video showing how to deal with banana connectors assembly/disassembly here: <a href="https://www.YouTube.com/watch?v=cH0C_g_lfXo" target="_blank" rel="noopener">https://www.youtube.com/watch?v=cH0C_g_lfXo</a>

## Software

### I cannot connect to UGSPlatform or any other g-code sending software

- Try restarting your program or computer.
- If you have other programs that are open that may be connecting to your Arduino (especially Arduino IDE) that they are closed.
- Try installing the <a href="https://www.java.com/en/download/" target="_blank" rel="noopener">latest version of Java</a>.
- You might not have drivers installed. You can install <a href="https://www.arduino.cc/en/main/software" target="_blank" rel="noopener">Arduino drivers</a> by installing the IDE for your computer.
- Check your computer's drivers. Update or reinstall them if necessary.
- Try a different USB port and USB cable.
- If you are using UGSPlatform, make sure to refresh and check the dropdown box for all of the ports that have devices connected to them. Try each one until you can connect.
![](/_images/_longmill/_assembly/_commonissues/lm_commonissues_p15_Refresh.png "Click on the refresh button and try other available ports."){.aligncenter .size-medium}

### I have an issue with Java when opening UGSPlatform

- If USG is still not able to open due to a Java access error, then there is another program on your computer blocking UGS from opening properly. UGS is usually able to automatically detect where Java is located on your computer, but since this detection is being blocked the way to fix this is to explicitly inform UGS where Java is. First you'll need to locate Java. You can usually find it by going to the Windows file explorer under <em>'This PC → Windows (C:) → Programs Files → Java → jre<b>###</b>'</em> or <em>'This PC → Windows (C:) → Programs Files (x86) → Java → jre<b>###</b>'</em>. Once inside the <em>'jre'</em> folder, left-click the navigation path at the top of the file explorer then right-click the selected text and left click the 'Copy' option to copy the path.
![](/_images/_longmill/_assembly/_commonissues/lm_commonissues_p16_JavaPath.png){.aligncenter .size-medium}
Once the path is copied, navigate to where you downloaded UGS; this will normally be located inside your 'Downloads' folder. Once there, go to:<em> 'ugs-platform-app-2.0-SNAPSHOT → ugsplatform → etc'</em>. In this folder should be a file called <em>'ugsplatform.conf'</em>. Opening this with a text editor like <em>Notepad</em>, you'll want to find the line which says: "<em>#jdkhome="/path/to/jdk</em>". Delete the '#', then replace the text within the quotes with the Java path by right-clicking and selecting '<em>Paste</em>'. The completed edit should look like this:
![](/_images/_longmill/_assembly/_commonissues/lm_commonissues_p17_ConfigFile.png){.aligncenter .size-medium}
To confirm the changes, click '<em>File</em>' in the top bar and '<em>Save</em>'. With all this done, once you go back to the UGS .exe launcher you should now be able to get UGS to start up without any errors.

### My machine is not moving / the software says <span style="color: #ff0000;">ALARM</span>

- Something's happened during the operation of the machine which was unexpected so it's decided to lock itself just in case.
- In some cases, your EEPROM settings (the machine settings have changed). Make sure they are correct by referring to the <a href="https://resources.sienci.com/view/lm-EEPROM-settings/" target="_blank" rel="noopener">default EEPROM settings</a>.
- To bring it out of the alarm state, press the "Soft Reset" button followed by the "Unlock" button and that will put the machine back into its 'IDLE' state.
- If it continues to go into an ALARM state under similar conditions in the future, check that no wires or hardware have come loose and that there's nothing externally affecting the movement of your machine.
![](/_images/_longmill/_assembly/_commonissues/lm_commonissues_p18_UGSAlarm.png){.aligncenter .size-medium}

### UGS sometimes stops/pauses/or reports an unknown command

Carbide Create uses M6/M06 codes that are used for tool changes. Since the LongMill does not have a tool changer or use tool change commands, it will pause at M6/M06 commands.

- You can press "Play" to continue the job.
- If you want to set up UGSPlatform to ignore M6/M06 commands, follow the writeup here: <a href="https://forum.sienci.com/t/permanent-fix-to-an-error-was-detected-while-sending-m6/395" target="_blank" rel="noopener">https://forum.sienci.com/t/permanent-fix-to-an-error-was-detected-while-sending-m6/395</a>
