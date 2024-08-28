---
title: ytsb Common Issues & Fixes 🩹
menu_order: 4
post_status: draft
post_excerpt: LongMill troubleshooting guide, to address stalling motors, skewed movement, faulty power switch, connectivity, touch probing, missing parts and much more.
post_date: 2021-04-30 15:40:00
taxonomy:
    knowledgebase_cat: lm-assembly
    knowledgebase_tag:
        - mk1
custom_fields:
    KBName: LongMill CNC
    basepress_post_icon: bp-caret-right
skip_file: no
featured_image: /_images/_longmill/_assembly/_commonissues/lm_commonissues_p_Versions.png
---

This part of the resources covers common issues and fixes for the LongMill. If you run into an issue with your machine, we hope that this can help you diagnose and fix problems to get you milling as quickly as possible. If you can't find the answers here, please feel free to get in <a href="https://sienci.com/contact-us/technical-help/" target="_blank" rel="noopener">touch with us</a>.

<h2>Assembly issues</h2>

<h3>I am missing or cannot find a part</h3>

Every LongMill is packed in our shop in Waterloo, ON by our team of trained staff. Every package goes through several checks to ensure that the correct parts and quantities are in each kit, but we sometimes make mistakes. If you can't find something, please reach out to us and we'll make it right. However, before <a href="https://sienci.com/contact-us/technical-help/" target="_blank" rel="noopener">reaching out to us</a>, there are a couple things you can check.

- Ensure that you are following the assembly instructions for the correct version of the machine. There are variations between versions, including the packing order and assembly. More info can be found in the [Unboxing](https://resources.sienci.com/view/lm-unboxing/){:target="_blank"} portion of the resources. <strong>Please note that our video instructions are based on the Version 2 design. </strong>Instructions from the video can still be referenced for additional help in assembling your machine.
![](/_images/_longmill/_assembly/_commonissues/lm_commonissues_p_Versions.png){.aligncenter .size-medium}- If you're missing the correct amount of hardware, you may find it in another bag. Please check in the rest of the kit to make sure all of your hardware is accounted for.
- Some parts and add-ons, such as the t-tracks come in a separate package as the LongMill kit. If your order is larger than what can be fit in the LongMill kit, it may come in more than one package.

<h3>My Delrin anti-backlash nuts will not thread on</h3>

During the assembly process, the anti-backlash nuts may be difficult to thread on, especially when threading between the base and the arm portions of the block. These nuts rely on the threads to line up for proper movement.

<ul>
  <li>The alignment of the threads can be tensioned by turning the set screw or M5 screw, <strong>or pressing the arm down to help the threads line up while threading in the lead screw</strong>. Once the lead screw has been threaded on, it can be tensioned by following our <a href="https://resources.sienci.com/view/lm-maintenance/">maintenance guide</a></li>
  <li>Slightly loosen the two M5 bolts that hold the nut to the gantry. Over tightening the screws can crush the ACME threads, causing additional friction between the lead screw and nut.</li>
  <li>Try threading your lead screw in from both directions. It may be easier to line up the threads from one direction over the other.</li>
  <li>Check for burrs and debris that may be in the threads.

![](/_images/_longmill/_assembly/_commonissues/lm_commonissues_p1_PressNut.jpg){.aligncenter .size-medium}

![](/_images/_longmill/_assembly/_commonissues/lm_commonissues_p2_NutDiagram.jpg){.aligncenter .size-medium}</li>
</ul>

<h3>I have leftover parts after assembly</h3>

When you get to the end of the building process, you may be left with a small handful of extra parts.

Don't worry, we supply extra additional parts so that

<ul>
  <li>If a part doesn't work properly, the extra one can be used instead.</li>
  <li>If you lose something (especially those screws), you still have plenty of extra.</li>
  <li>We reduce the chance of packing too few of a certain part.</li>
  <li>If you have a 12x12 or 12x30 LongMill, you can upgrade to a 30x30 at a later date.</li>
</ul>

<h2>Motor and controller issues</h2>

<h3>My controller is not turning on</h3>

First ensure that your LongMill's power supply cable is connected to the wall and power brick correctly and that the green LED is lit up on the power supply brick. If you have an E-stop, check that the button is released by twisting it counterclockwise and if you have a power switch, ensure it's toggled on.

Other things you can check:

<ul>
  <li>If the red light on the controller top (newer versions) or on the drivers (visible through the grates on the underside of the controller) are on, then you are getting power to the controller. You may be having issues with connecting your machine to the computer.</li>
  <li>Make sure that the polarity of the power wiring is correct. Switch the wires around if need be (see picture).</li>
  <li>If you have a older power switch model and the red LED lights  flicker or turn off right when the power switch is turned on, you may have a faulty switch. Please contact us.</li>
  <li>If you have a newer E-stop model, check that the E-stop is plugged into the <strong>top</strong> of the LongBoard, and the power supply is plugged into the<strong> side</strong> of the LongBoard. <a href="https://drive.google.com/file/d/10I-XiU6GuIwgeMfRe_LBDjoDTnmqmISy/view?usp=sharing" target="_blank" rel="noopener">View the correct installation here.</a> You can also check that the wiring is secured inside the E-stop itself by unfastening the 4 screws on the lid with a screwdriver. There should be two wires secured on either terminal (polarity doesn't matter).

![](/_images/_longmill/_assembly/_commonissues/lm_commonissues_p3_Polarity.jpg "The wire on the left should be white, and the wire on the right should be black.")</li>
</ul>

<h3>One motor does not move or moves erratically</h3>

When jogging or running the LongMill, one of the motors does not move correctly or at all.

<ul>
  <li>Check that both the plugs on the controller side and the motor side are connected properly. We recommend completely disconnecting the plug and plugging it back in.</li>
  <li>Check that all of the wires on the plug are connected and secure.</li>
  <li>If your motor does not move at all, try switching and testing if it is working correctly by plugging it into a different axis on the motor controller. If the motor moves on a different axis, then you can confirm that the motor is working correctly and identify that there may be an issue with the controller.</li>
  <li>Check that the light on all of the drivers inside the control box are illuminated. If you have a driver that is not illuminated, please contact us for additional support.</li>
  <li>Check that all of the <a href="https://resources.sienci.com/view/lm-electronics/" target="_blank" rel="noopener">DIP switches</a> are properly seated in the correct orientation. If the switch is only part of the way on or off, the driver may not operate.</li>
  <li>If one y-axis motor moves but the other doesn't. Switch the y connectors. If the issue moves to the other side, it might be the driver is supplying the wrong amount of current. Follow these <a href="https://resources.sienci.com/wp-content/uploads/2022/06/Stepper-Driver-Current-Adjustment.pdf" target="_blank" rel="noopener">instructions</a> to make adjustments.</li>
  <li>Make sure your Arduino is fully seated in your control board. You can typically use a non-conductive tool to push it into the socket if it is starting to come loose.

![](/_images/_longmill/_assembly/_commonissues/lm_commonissues_p4_ControlBoard.jpg){.aligncenter .size-medium}</li>
</ul>

<h3>My machine is not moving in the right direction</h3>

<ul>
  <li>Ensure that all plugs and cables are fully seated and connected properly.</li>
  <li>Check the colour pattern of each wire coming from the motor and connected to the LongBoard. Is the pattern all the same with each motor? If not, change the order of the wires to match.</li>
  <li>Reload the EEPROM settings on your Arduino, as these settings may have changed when using various g-code senders. These settings control aspects such as the jogging direction and the machine’s work space boundaries. To access them, go to the Firmware tool in gSender, or the Firmware Settings in UGS. gSender will have the ability to "Restore Defaults" and revert to the LongMills regular setting. For UGS, make sure you have the default settings (found here: <a href="https://resources.sienci.com/view/lm-EEPROM-settings/" target="_blank" rel="noopener">https://resources.sienci.com/view/lm-eeprom-settings/</a>) by going through each line and manually changing the values, or download the zip file, unzip it, and load it into UGS.

![](/_images/_longmill/_assembly/_commonissues/lm_commonissues_p5_Wiring.jpg "The wiring colour pattern should be blue, yellow, green, red."){.aligncenter .size-medium}

![](/_images/_longmill/_assembly/_commonissues/lm_commonissues_p6_USGEEPROM.png "Where to find the EEPROM settings on UGS Platform."){.aligncenter .size-medium}</li>
</ul>

<h3>My machine is not moving the correct amount</h3>

<ul>
  <li>The microstepping on your drivers may not be set correctly. Check the drivers under your machine and make sure that they are set to 1/8" <a href="https://resources.sienci.com/view/lm-microstepping/" target="_blank" rel="noopener">microstepping</a> by ensuring that the DIP switches are in the correct position.</li>
  <li>Your coupler may be slipping. Ensure that the screws on your coupler are fully tightened.</li>
  <li>Try restarting your g-code sender.</li>
</ul>

<h3>My motors are stalling</h3>

<ul>
  <li>Make sure that all of the motor wires are seated properly.</li>
  <li>Make sure that you have not overtightened the Delrin anti-backlash nuts on your machine. Loosen the two M5-25mm screws that hold the nut in place and see if that helps.</li>
  <li>Ensure that the couplers are secured onto the motor shaft and lead screw with the set screws. If the coupler is slipping and requires re-tightening often, there is a possibility that the coupler threads are stripped.</li>
  <li>Re-flash the Arduino with the firmware to ensure that the code on the Arduino hasn't been altered somehow. Since the Arduino acts as the "brains" of the control board, it can affect how the motors are running. The instructions for flashing the Arduino are found here: <a href="https://resources.sienci.com/view/lm-grbl-firmware/" target="_blank" rel="noopener">https://resources.sienci.com/view/lm-grbl-firmware/</a></li>
</ul>

<h3>My Y-axis is skewing (one side moves further than the other)</h3>

<ul>
  <li>Run the machine to the back until you hear a grinding noise, this will realign your y-axis gantries to be square with the X-axis. See if the issue is still persisting by jogging back and forth, moving through the entirety of the Y-axis travel.</li>
  <li>Power off the machine. Using your hands, turn each Y-axis lead screw a few rotations, checking that they are difficult but not impossible to turn and that they are equally hard to turn.  If that is not the case, adjust by slightly loosening the fasteners in the anti-backlash nut with an Allen key (both the mounting screws and the single screw sticking out). Keep checking and adjusting the lead screws until they are equal and difficult to turn by hand.</li>
  <li>The microstepping on your drivers may not be set correctly. Check the drivers under your machine and make sure that they are set to 1/8" <a href="https://resources.sienci.com/view/lm-microstepping/" target="_blank" rel="noopener">microstepping</a> by ensuring that the DIP switches are in the correct position.</li>
</ul>

<h2>Operation</h2>

<h3>My cuts are not coming out accurately</h3>

<ul>
  <li>Try reducing your speeds and feeds, or use a different cutting tool.</li>
  <li>Check that there is no dust in the collet of your router, so that the bit does not slip in the collet during operation.</li>
  <li>You may have a loose component. Make sure that all of your fasteners are tight and your eccentric nuts and Delrin anti-backlash nuts are tensioned correctly.</li>
  <li>Your motor or lead screw may be slipping inside the coupler. Ensure that the coupler is fully tightened and pressed firmly against the flange bearing to eliminate movement axially.</li>
</ul>

<h3>My cuts on the Z-axis are not the correct depth</h3>

<ul>
  <li>Ensure that the set screws on the two pulleys on the Z-axis assembly are tight and the belt is tensioned</li>
  <li>Ensure that the LongMill has enough travel on the Z-axis for it to cut deep enough. It may be bottoming out.</li>
  <li>If your LongMill is bottoming out, lower the position of your router or use a longer end mill. The LongMill comes with two set of holes on the Z-axis gantry plate for placing the router mount (upper and lower), and using the lower mount position on the Z-axis may work better.</li>
</ul>

<h3>My lead screws wobble excessively</h3>

Excessive wobble is when the lead screw is deviating from center by more than about 3mm or 1/8". This means that butting a measuring tape or ruler against the LongMill wasteboard and recording down the height of the lead screw at its lowest point, and then again at its highest point, should result in a difference in the two measurements of no more than 6mm or 1/4". Wobble can happen due to a loose lead screw or due to the screw being physically bent: if it's bent then the wobble will happen at any movement speed, whereas if it's loose then it will wobble mostly at higher movement speeds (above 2000mm/min).

<ul>
  <li><strong>Loose screw:</strong> loosen the two M5-25mm screws that hold the Delrin anti-backlash nuts slightly for the axis which the lead screw is on and run the machine back and forth. This will align the lead screw and the nut. Re-tighten the screws once the wobbling as gone away. Also check the ACME locking nut and coupler on both ends of the screw are firmly tightened and sandwiching the lead screw properly.</li>
  <li><strong>Bent screw:</strong> a sure way to confirm is to completely remove the screw and roll it along a surface that is very flat and seeing if it rolls evenly.</li>
</ul>

<h3>The machine moves really slowly or not at all when I jog it</h3>

<ul>
  <li>If you are jogging your machine for the first time, your feed rate may be set to 10mm/min. This means it will only move 10mm in one minute (really really slow). Try increasing the speed until it is perceptible. 1000mm/min is a good place to start.</li>
  <li>If you are running code or a job, make sure that your feed rates are set correctly.</li>
</ul>

<h3>My machine randomly cuts lines during my job</h3>

<ul>
  <li>If you are using Fusion 360, ensure that ‘Safe Retracts’ is set to ‘Clearance Height.’

![](/_images/_longmill/_assembly/_commonissues/lm_commonissues_p7_f360.png){.aligncenter .size-medium}</li>

  <li>Ensure that you are not hitting the Z-axis movement limits when running the job.</li>
  <li>Review the g-code with a visualizer (<a href="https://ncviewer.com/">https://ncviewer.com/</a>) to ensure there are no unexpected toolpaths or incorrect g-code commands.</li>
  <li>Check all the transmission components (V-wheels, couplers, ACME nuts, anti-backlash nuts, pulleys)
<ul>
  <li>Pulleys, couplers and ACME nuts are secured and in the correct position.</li>
  <li>Belt in the Z-axis is tensioned</li>
  <li>Anti-backlash nuts are not mounted too tight; you can loosen the two M5-25mm screws that hold the nut in place and see if that helps.</li>
  <li>Eccentric nuts are adjusted so that V-wheels are tight on the rail but are still able to turn by hand.</li>
</ul>
</li>
</ul>

<h3>My machine randomly stops and starts</h3>

<ul>
  <li>Check if your power supply and all of the connectors are secure and properly attached.</li>
  <li>Ensure that your computer has completed all Windows/Mac updates. The serial communication through the USB drivers on your computer can be affected by the updates pushed by your operating system.</li>
  <li>Look for sources that may be causing electromagnetic interference (EMI). This could be vacuums, motors, and other electronics nearby that could be sending EMI to the control board.</li>
  <li>Try connecting the control box to a different breaker than the router and vacuum in case a brown out is happening with your control box.</li>
  <li>Check if your drivers are excessively hot. The drivers should not exceed 80C.</li>
</ul>

<h3>My machine stops cutting / loses connection on long jobs</h3>

Loss of connection on a long job can happen if your computer or USB port 'fall asleep' on you. If you plan on running long, intricate cuts on your CNC you'll have to change your computer power settings so that it 'stays awake' while cutting. Iif you're using a Mac computer, you can find dedicated instructions for sleep management here: <a href="https://support.apple.com/en-ca/guide/mac-help/mchle41a6ccd/mac" target="_blank" rel="noopener">https://support.apple.com/en-ca/guide/mac-help/mchle41a6ccd/mac</a>.

<ul>
  <li>Click the <strong>Windows</strong> icon at the bottom left corner of your screen and start to type "<em>control panel</em>" to bring it up

![](/_images/_longmill/_assembly/_commonissues/lm_commonissues_p8_p1.png){.aligncenter .size-medium}

</li>
  <li>Once you've clicked to open it, go to <strong>Hardware and Sound</strong> then <strong>Power Options</strong>

![](/_images/_longmill/_assembly/_commonissues/lm_commonissues_p9_p2.png){.aligncenter .size-medium}

![](/_images/_longmill/_assembly/_commonissues/lm_commonissues_p10_p3.png){.aligncenter .size-medium}
  </li>
  <li>Now, whichever plan you have currently selected (circled in the picture) will be the one that you want to click <strong>Change plan settings</strong>

![](/_images/_longmill/_assembly/_commonissues/lm_commonissues_p11_p4.png){.aligncenter .size-medium}

  </li>
  <li>Go to the second drop-down and set it to <strong>Never</strong>, save the changes to ensure that your computer never dozes off on its own. An additional step can be to stop your USB ports from 'sleeping' by clicking <strong>Change advanced power settings</strong>
  
![](/_images/_longmill/_assembly/_commonissues/lm_commonissues_p12_p5.png){.aligncenter .size-medium}
  
  </li>
  <li>In the separate window that appears, you'll want to Expand the <strong>USB Settings</strong>, then <strong>USB selective suspend setting</strong>, and finally change this drop-down to "<strong>Disabled</strong>". Click to <strong>Apply</strong> these new settings. <strong>**</strong>Sometimes on a Windows update these settings will be reset, if you want to make sure you've got all your bases covered, be sure to check back on these settings on occasion if you want to feel confident while running long jobs.**
  
 ![](/_images/_longmill/_assembly/_commonissues/lm_commonissues_p13_p6.png){.aligncenter .size-medium}
 </li>
</ul>

<h3>My bit is crashing into the touch plate</h3>

If you’re using UGS:
<ul>
  <li>There is a bug that can cause the touch plate to move farther than the expected origin and plunge the bit into the work surface if you use INCHES units when jogging around. If so, before beginning the probe process ensure that you have set the jog control to MM instead of INCHES. Once probing is completed, you may switch back to INCHES and resume regular machine operation

![](/_images/_longmill/_assembly/_commonissues/lm_commonissues_p14_UGSbug.png "Jog control unit setting on UGS"){.aligncenter .size-medium}

</li>
</ul>

If this was not the problem:

<ul>
  <li>Check that the bit you are using is not tapered and is conductive at the both its sides and end so that it can make electrical contact with the touch plate.</li>
  <li>Ensure the settings you use are from the touch plate page on our website (not the settings in the video): <a href="https://resources.sienci.com/view/lm-touch-plates/" target="_blank" rel="noopener">https://resources.sienci.com/view/lm-touch-plates/</a></li>
  <li>Make sure your work coordinates match your touch plate settings (usually G54)</li>
  <li>Check that there's proper electrical contact from your control box through to your magnet and touch plate. An easy way to check this is to run a Z probe with the router high up in the air and manually tap the magnet to the plate while they're held in each of your hands. If the bit stops and raises slightly up then lowers down again, this should indicate some form of connectivity from the magnet and touch plate to the control box. If you tap them together again, this should conclude the probing process and no errors should appear. If you don't observe this behaviour, then you should try this test again and if it again shows an error then check the electrical connections. See if the magnet is making contact with the metal leads of the wire by unscrewing the fastener in the centre and do the same for the banana plug as well. You may need to strip more insulation off the ends of the wire to get more contact with the metal surfaces. There’s a great video showing how to deal with banana connectors assembly/disassembly here: <a href="https://www.youtube.com/watch?v=cH0C_g_lfXo" target="_blank" rel="noopener">https://www.youtube.com/watch?v=cH0C_g_lfXo</a></li>
</ul>

<h2>Software</h2>

<h3>I cannot connect to UGSPlatform or any other g-code sending software</h3>

<ul>
  <li>Try restarting your program or computer.</li>
  <li>If you have other programs that are open that may be connecting to your Arduino (especially Arduino IDE) that they are closed.</li>
  <li>Try installing the <a href="https://www.java.com/en/download/" target="_blank" rel="noopener">latest version of Java</a>.</li>
  <li>You might not have drivers installed. You can install <a href="https://www.arduino.cc/en/main/software" target="_blank" rel="noopener">Arduino drivers</a> by installing the IDE for your computer.</li>
  <li>Check your computer's drivers. Update or reinstall them if necessary.</li>
  <li>Try a different USB port and USB cable.</li>
  <li>If you are using UGSPlatform, make sure to refresh and check the dropdown box for all of the ports that have devices connected to them. Try each one until you can connect.

![](/_images/_longmill/_assembly/_commonissues/lm_commonissues_p15_Refresh.png "Click on the refresh button and try other available ports."){.aligncenter .size-medium}</li>
</ul>

<h3>I have an issue with Java when opening UGSPlatform</h3>

<ul>
  <li>If USG is still not able to open due to a Java access error, then there is another program on your computer blocking UGS from opening properly. UGS is usually able to automatically detect where Java is located on your computer, but since this detection is being blocked the way to fix this is to explicitly inform UGS where Java is. First you'll need to locate Java. You can usually find it by going to the Windows file explorer under <em>'This PC → Windows (C:) → Programs Files → Java → jre<strong>###</strong>'</em> or <em>'This PC → Windows (C:) → Programs Files (x86) → Java → jre<strong>###</strong>'</em>. Once inside the <em>'jre'</em> folder, left-click the navigation path at the top of the file explorer then right-click the selected text and left click the 'Copy' option to copy the path.
  
![](/_images/_longmill/_assembly/_commonissues/lm_commonissues_p16_JavaPath.png){.aligncenter .size-medium}

Once the path is copied, navigate to where you downloaded UGS; this will normally be located inside your 'Downloads' folder. Once there, go to:<em> 'ugs-platform-app-2.0-SNAPSHOT → ugsplatform → etc'</em>. In this folder should be a file called <em>'ugsplatform.conf'</em>. Opening this with a text editor like <em>Notepad</em>, you'll want to find the line which says: "<em>#jdkhome="/path/to/jdk</em>". Delete the '#', then replace the text within the quotes with the Java path by right-clicking and selecting '<em>Paste</em>'. The completed edit should look like this:

![](/_images/_longmill/_assembly/_commonissues/lm_commonissues_p17_ConfigFile.png){.aligncenter .size-medium}

To confirm the changes, click '<em>File</em>' in the top bar and '<em>Save</em>'. With all this done, once you go back to the UGS .exe launcher you should now be able to get UGS to start up without any errors.</li>
</ul>

<h3>My machine is not moving / the software says <span style="color: #ff0000;">ALARM</span><strong>
</strong></h3>

<ul>
  <li>Something's happened during the operation of the machine which was unexpected so it's decided to lock itself just in case.</li>
  <li>In some cases, your EEPROM settings (the machine settings have changed). Make sure they are correct by referring to the <a href="https://resources.sienci.com/view/lm-EEPROM-settings/" target="_blank" rel="noopener">default EEPROM settings</a>.</li>
  <li>To bring it out of the alarm state, press the "Soft Reset" button followed by the "Unlock" button and that will put the machine back into its 'IDLE' state.</li>
  <li>If it continues to go into an ALARM state under similar conditions in the future, check that no wires or hardware have come loose and that there's nothing externally affecting the movement of your machine.
  
 ![](/_images/_longmill/_assembly/_commonissues/lm_commonissues_p18_UGSAlarm.png){.aligncenter .size-medium}
  
</li>
</ul>

<h3>UGS sometimes stops/pauses/or reports an unknown command</h3>

Carbide Create uses M6/M06 codes that are used for tool changes. Since the LongMill does not have a tool changer or use tool change commands, it will pause at M6/M06 commands.

<ul>
  <li>You can press "Play" to continue the job.</li>
  <li>If you want to set up UGSPlatform to ignore M6/M06 commands, follow the writeup here: <a href="https://forum.sienci.com/t/permanent-fix-to-an-error-was-detected-while-sending-m6/395" target="_blank" rel="noopener">https://forum.sienci.com/t/permanent-fix-to-an-error-was-detected-while-sending-m6/395</a></li>
</ul>
