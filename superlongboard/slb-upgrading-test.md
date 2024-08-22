---
title: ytsb Upgrading to SLB Test
menu_order: 4
post_status: draft
post_excerpt: Time to power up! Steps on how to upgrade your LongMill CNC or other CNC machine from your old control system to the SuperLongBoard.
post_date: 2024-03-22 13:28
taxonomy:
    knowledgebase_cat: slb-handbook
    knowledgebase_tag:
        - slb
custom_fields:
    KBName: SuperLongBoard
    basepress_post_icon: bp-caret-right
skip_file: no
featured_image: _images/_superlongboard/LB2SLB_pone.jpg
---
Congrats on upgrading to our newest and most powerful CNC controller to date, the <strong>SuperLongBoard</strong>!

Our main goal in this section is to have you go in with a working CNC, then leave with an <strong>SLB-boosted machine</strong> without skipping a beat. This guide will be mostly written with LongMill owners in mind who have the older LongBoard (<strong>LB, pictured on the left</strong>) that they’ll be swapping out for the SuperLongBoard (<strong>SLB, on the right</strong>), though there will be minimal differences for other CNC owners with a LongBoard.

![](/_images/_superlongboard/_upgrading/slb_upgrading_p1_SLB.jpg){.aligncenter .size-medium}

<h2>Unpacking</h2>

In the box you’ll find:

<ul>
  <li>Your new <strong>SuperLongBoard</strong> inside it’s aluminum enclosure</li>
  <li><strong>E-stop</strong> with 3 additional ‘Action Buttons’ that are customizable</li>
  <li><strong>E-stop cable</strong>, plenty long to increase mounting options</li>
  <li>And a <strong>USB-C cable</strong>, MK2 <strong>mounting hardware</strong>, and some <strong>spare connectors</strong></li>
</ul>

The only other parts that you’ll need to supply yourself are:

<ul>
  <li>The minimum <strong>24V 10A power supply</strong> needed to run the SLB (you can use the one your LongBoard currently uses)</li>
  <li>Your <strong>CNC machine</strong>, already tested to be working using its existing LongBoard</li>
  <li>A <strong>computer running gSender</strong> with a free USB port</li>
</ul>

![](/_images/_superlongboard/_upgrading/slb_upgrading_p2_Box.jpg){.aligncenter .size-medium}

We hope everything arrived well and in one piece! Let’s take the cover off the SuperLongBoard and see what’s under the hood.

Unscrew the top-right thumbscrew a couple turns (pictured) then slide the cover to the right. Once the hole in the cover lines up, you’ll be able to pull the top of the cover towards you and it will come free.

[gallery size="full" link="none" ids="6607,6692,6616"]

<h2>Preparation</h2>

Before diving into rewiring, we’d first suggest you note down any firmware changes that are unique about your setup. You can do this by connecting to your CNC in gSender and using the Firmware Tool to find sections that are <strong>highlighted in yellow</strong>. In the example below, you can see that the maximum travel is different from the standard MK2 12x30.

![](/_images/_superlongboard/_upgrading/slb_upgrading_p3_FirmMaxTravel.jpg){.aligncenter .size-medium}

Yellow sections show when a change has been made from the default settings. Any of these should be written down and will be re-entered when the new board is set up.

<h2>Wiring</h2>

To help communicate where things are on the board, we use the terms shown below:

![](/_images/_superlongboard/_upgrading/slb_upgrading_p4_TopBottom.jpg){.aligncenter .size-medium}

[gallery columns="2" size="large" link="none" ids="6609,6610"]

&nbsp;

Let’s start moving plugs over to the SLB!

1. On your <strong>LongMill</strong>, hit the E-stop then unplug the power cable from the board.

![](/_images/_superlongboard/_upgrading/slb_upgrading_p5_Estop.jpg){.aligncenter .size-medium}

1. On your computer, unplug the USB cable that ran to the <strong>LongMill</strong>.

![](/_images/_superlongboard/_upgrading/slb_upgrading_p6_USB.jpg){.aligncenter .size-medium}

1. Unplug the X, Y1, Y2, and Z connectors from your <strong>LongMill</strong> and plug them into the <strong>SLB</strong> in the same order. There aren’t any extra steps you have to do even if you have the <a href="https://sienci.com/product/vortex-rotary-axis/">Vortex</a>.

![](/_images/_superlongboard/_upgrading/slb_upgrading_p7_Motors.jpg){.aligncenter .size-medium}

1. Unplug your touch plate/probe from the <strong>LongMill</strong> and plug it into the <strong>SLB</strong>, on the <strong>Front Side</strong>.

![](/_images/_superlongboard/_upgrading/slb_upgrading_p8_Probe.jpg){.aligncenter .size-medium}

1. Grab the new E-stop and plug the green end into the <strong>Front Side</strong> of the <strong>SLB</strong>, then the other end into the backside of the E-stop.

![](/_images/_superlongboard/_upgrading/slb_upgrading_p9_Estop.jpg){.aligncenter .size-medium}

<span style="font-weight: 400;">6. Now grab the USB-C cable that came with your </span><b>SLB</b><span style="font-weight: 400;"> and plug it into the </span><b>Front Side </b><span style="font-weight: 400;">of the board. Plug the other end into your computer.</span>

![](/_images/_superlongboard/_upgrading/slb_upgrading_p10_DoubleUSB.jpeg){.aligncenter .size-medium}

1. On the <strong>Back Side</strong> of the <strong>SLB</strong>, plug in the power plug that we unplugged from the <strong>LongMill</strong> earlier.

![](/_images/_superlongboard/_upgrading/slb_upgrading_p11_Power.jpg){.aligncenter .size-medium}

1. Lastly, when looking at the <strong>Back Side</strong> of the <strong>SLB</strong>, you will see a power switch. Slide it to the ‘ON’ position to power on the <strong>SLB</strong>. It’s Alive!!

![](/_images/_superlongboard/_upgrading/slb_upgrading_p12_OnOff.jpg){.aligncenter .size-medium}

<strong>Congratulations!</strong> You’ve wired up your new SLB with all its typical accessories! If you still have other, slightly less common accessories to wire in, then keep reading the next section; otherwise you can move over to <a href="https://resources.sienci.com/view/slb-upgrading/#gSender">gSender</a> to connect and do some quick tests.

<h2>Optional Wiring</h2>

You have your SLB wired up and ready to go, but do you have:

<ul>
  <li><strong>Limit Switches</strong>?</li>
  <li>A (pew pew) <strong>LaserBeam</strong>?</li>
  <li>An <strong>IOT Relay</strong> working to turn on your shop vac or router?</li>
</ul>

If so, this section is for you. Fear not, we’ve got you covered!

<h3>Limit Switches</h3>

Sienci inductive sensors can be plugged straight into the white JST connectors, so you can simply unplug them from your LB and plug them into the corresponding spots on the SLB.
<p style="text-align: center;"><strong><em>Note:</em></strong><em> The Y2 connection isn’t used at this time</em></p>

![](/_images/_superlongboard/_upgrading/slb_upgrading_p13_Limit.jpg){.aligncenter .size-medium}

If you are not using the Sienci inductive sensors, wire your sensors in using the Auxiliary terminal connector input.

![](/_images/_superlongboard/_upgrading/slb_upgrading_p14_LimitSLB.jpg){.aligncenter .size-medium}

<span style="font-weight: 400;">The hookup changes for this new plug, compared to the one we had on the LongBoard, is shown below. Don’t worry about the Y2 or A-axis wiring for now.</span>

![](/_images/_superlongboard/_upgrading/slb_upgrading_p15_Limits2.jpg){.aligncenter .size-medium}

<h3>LaserBeam</h3>

On the LongBoard, unplug your 2-pin SpinPWM plug and plug it into the 3-pin Laser plug on the <strong>Back Side</strong> of the board. Ensure that you plug the two plug connector into the bottom/far right two pins, as indicated in the pictures below.

![](/_images/_superlongboard/_upgrading/slb_upgrading_p16_Laser.jpg){.aligncenter .size-medium}

<em><strong>Warning</strong>: Lasers are very dangerous devices that can instantly damage your vision and cause fires. Become knowledgeable on staying safe by reading documentation by your laser manufacturer, the SLB, how laser <a href="https://github.com/gnea/grbl/blob/master/doc/markdown/laser_mode.md" target="_blank" rel="noopener">mode in grbl</a> &amp; grblHAL works, and how your g-code sender handles laser commands. Even then do not become complacent; continue to treat your laser with caution and respect and turn off power completely to the laser driver when you’re not using it. You can never be sure when the laser might fire unexpectedly and hobby equipment and software can be imperfect. If you have the driver turned on, everyone around should always be wearing eye protection and there should also be clear warning or signage to protect others.</em>

<h3>Spindle</h3>

If instead you had a Spindle connected to your LongBoard and would like to swap it over to the SLB, just continue through the initial setup steps for now then when you’re ready swap over to the explanation for <a href="https://resources.sienci.com/view/slb-manual/#spindlers485">Spindle wiring in the full SLB Manual</a>.

<h3>IOT Relay</h3>

Simply unplug your 2 pin connector from the Coolant on the LongBoard, and plug it into the Flood connector at the top of the SLB.

![](/_images/_superlongboard/_upgrading/slb_upgrading_p17_Coolant.jpg){.aligncenter .size-medium}

<h2>gSender</h2>

The SLB requires use of version 1.4.0 or later, only these versions can talk to the SLB. Please keep up to date with installing the latest version of gSender <a href="https://github.com/Sienci-Labs/gSender/releases">here</a>.

<h3>Connecting to your SLB</h3>

You will be connecting to the SLB differently than you are used to.

1. Go to <strong>Connect to Machine</strong> in the top left corner (with the board powered on).

![](/_images/_superlongboard/_upgrading/slb_upgrading_p18_Connect1.jpg){.aligncenter .size-medium}

1. Connecting to the SLB, requires you to select a new button. Click the gray bar at the bottom labelled Firmware.

![](/_images/_superlongboard/_upgrading/slb_upgrading_p19_Connect2.jpg){.aligncenter .size-medium}

1. Then click on <strong>grblHAL</strong>.

![](/_images/_superlongboard/_upgrading/slb_upgrading_p20_Connect3.jpg){.aligncenter .size-medium}

1. With the SLB, we have the option to connect via USB or Ethernet. Under Recognized Devices there should be one option, let’s select that.

![](/_images/_superlongboard/_upgrading/slb_upgrading_p21_Connect4.jpg){.aligncenter .size-medium}

<strong>Congrats!</strong> You have connected to your new SuperLongBoard!! Since USB is plug and play, we’ve selected it now and can connect via Ethernet at a later time.

![](/_images/_superlongboard/_upgrading/slb_upgrading_p22_Connected.jpg){.aligncenter .size-medium}

Let’s move on to some quick tests.

<h2>Quick tests</h2>

Now that we have the basics plugged in and are connected in gSender, we’re going to test out a couple things. This will help catch any issues before the SLB is more permanently mounted or you start on your wire management ;). Let’s put this SLB through some paces eh?!!

<h3>Power On Test</h3>

When the board is receiving power, you will see two specific green lights come on. One shows you that your 5V power is active, and the other shows that your 3.3V current is working.

![](/_images/_superlongboard/_upgrading/slb_upgrading_p23_LightsGreen.jpg){.aligncenter .size-medium}

Now hit the E-stop button (it may already be pressed down). When you press it down, the E-stop button will go dark and power to the motors will be cut.

![](/_images/_superlongboard/_upgrading/slb_upgrading_p24_DoubleEStop.jpg){.aligncenter .size-medium}

The SLB will respond by turning several lights RED. Most notably your <strong>CNC Status</strong> light and a very small led called <strong>HALT</strong> will both turn red.

![](/_images/_superlongboard/_upgrading/slb_upgrading_p25_LightsRed.jpg){.aligncenter .size-medium}

Now we can deactivate the E-stop button by turning it clockwise until it’s raised again. You will see the E-stop button light come back on when raised correctly. We will need to unlock the SLB in gSender by pressing the Click to Unlock Machine button.

![](/_images/_superlongboard/_upgrading/slb_upgrading_p26_Unlock.jpg){.aligncenter .size-medium}

<strong>Congrats!</strong> You’ve completed the Power On Quick Test.

<em>If your lights didn’t come on or you experienced unusual behavior:</em>

<ul>
  <li>Check that the power supply is plugged into the wall, the brick, and the board</li>
  <li>Ensure there is a light on the power supply (our new blue power supplies don’t have one)</li>
  <li>Ensure the SLB power switch has been flipped to be ‘ON’</li>
  <li>Ensure there are lights on the board</li>
</ul>

<h3>Move Test</h3>

<strong>Testing Directions</strong>
It’s time to take the SLB out for a spin! Using the jog controls on the main page of gSender, try moving your machine around in the X, Y and Z-axes. Make sure they’re going in the correct directions; also try increasing the jogging ‘Speed’ value to 5500mm/min (220ipm) to test the faster default capabilities of the SLB.
<p style="text-align: center;"><em><strong>Note</strong>: If you have a LongMill MK1, you’ll need to invert your Z-axis movement (see next step).</em></p>

![](/_images/_superlongboard/_upgrading/slb_upgrading_p27_JogControl.jpg){.aligncenter .size-medium}

If you find that your axes are not moving in the correct direction, you can go into your firmware settings and change the axis that’s wrong. Also, if you notice that your CNC reacts intermittently at higher speeds then you might have to either spend some more time tuning your machine's mechanics, or consider lowering the SLBs maximum speed with settings 110, 110, and 112.

![](/_images/_superlongboard/_upgrading/slb_upgrading_p28_Off.jpg){.aligncenter .size-medium}

<p style="text-align: center;"><em>Above, the Z-axis was flipped since the SLB was being set up on an MK1 LongMill</em></p>
While you’re here, if you used to use $1=255 to hold your motors (typically used for heavier spindles or CNCs mounted vertically), you can now instead scroll down to setting 37 “Steppers de-energize” where you can now choose to hold individual motors.

<h3>Touch Plate Test</h3>

One last test is to check that your touch plate works. Navigate to the Probe tab and hit the ‘Probe’ button.

![](/_images/_superlongboard/_upgrading/slb_upgrading_p29_Probe.jpg){.aligncenter .size-medium}

Then, tap the magnet to the touch plate. You will see the yellow PRB light on the SLB.

![](/_images/_superlongboard/_upgrading/slb_upgrading_p30_GIF.gif){.aligncenter .size-medium}

You’ll know you are successful if the popup button turns blue, and says “Start Probe”.

If the light is coming on but the popup button isn’t turning blue, this can sometimes be fixed by resetting your board settings. Do this by typing “$RST=$” into the console tab and hitting Enter, then use the power switch on the back of the board to “power-cycle” it off and back on again. Once you reconnect in gSender you can try probing again.
<p style="text-align: center;"><em><strong>Note:</strong> If you reset your board settings, you’ll need to go back and change any other settings you changed up until this point,, like inverting the Z-axis for MK1 owners.</em></p>

![](/_images/_superlongboard/_upgrading/slb_upgrading_p31_TouchNoTouch.png){.aligncenter .size-medium}

<strong>Congrats!</strong> Your Quick tests are now complete. This means that all our basic accessories should now be set up and ready to use on your new SLB! If you wired up other accessories then keep reading the next section to ensure you test them too, otherwise you can move on to the <a href="#routing">Routing section</a>.

<h2>Other Tests</h2>

<h3>Limit Switch Test</h3>

Your limit switches are installed and plugged into your SLB, so let’s check that they are working properly.

1. <strong>Powered sensors</strong> - Place a metal object in front of each of the limit switches and look for the red light. This indicates that each sensor is plugged in correctly.

![](/_images/_superlongboard/_upgrading/slb_upgrading_p32_RSTConsole.jpg){.aligncenter .size-medium}

1. <strong>Signal to the board</strong> - Navigate to your Calibration Tool and check the Diagnostics tab to see if your board is receiving the signal from the limit switch, when the pins change from OFF to ON. Also double check that the correct axis is turning on.

<p style="text-align: center;"><em><strong>Note:</strong> If you don’t see an axis turning ON/OFF, double check the connections on the board. We don’t use Y2 for example.</em></p>

![](/_images/_superlongboard/_upgrading/slb_upgrading_p33.jpg){.aligncenter .size-medium}

1. <strong>Turn Homing on</strong> - Scroll down in gSender’s Firmware Tool to 22, also called “Homing cycle”. There are more options for homing on the SLB, but just start by matching the toggles in the picture below (on, off - on, on - off, off - on, off). This will make the SLB home the same way that you’re already used to. Make sure to click “Apply New Settings”.

If you even find you can’t unlock homing, homing isn’t setting the machine coordinates to zero, or other unusual behaviours, come back here to double-check this list since you might not have all the right settings turned on. If you’re still curious about the other options, check out the <a href="https://resources.sienci.com/view/slb-manual/#homing-amp-limit-switches">Homing &amp; Limits Setup</a> section.

![](/_images/_superlongboard/_upgrading/slb_upgrading_p34_PinGIF.gif){.aligncenter .size-medium}

1. <strong>Homing test</strong> - With things looking good on the firmware side, let’s run a homing cycle with gSender by pressing the ‘Home’ button on the main screen.

1. <strong>Invert if needed</strong> - If you find any axes are reversed, return to 23 in the firmware tool and flip any of the directions that are wrong. If you find that homing is behaving weirdly still, go back and check that you turned on the right toggles for 22.

![](/_images/_superlongboard/_upgrading/slb_upgrading_p35_HomingCycle.jpg){.aligncenter .size-medium}

1. <strong>Reduce homing speed if needed</strong> - If you’re finding your CNC gets stuck completing a homing cycle or is disconnecting, try reducing the homing “seek rate” (25) or increasing the “debounce delay” (26) settings. Depending on your setup or sensors, the default values might be a bit too aggressive.

<h3>LaserBeam Test</h3>

With your LaserBeam plugged into the SLB, let’s perform a quick test to make sure it fires up.

<ol>
  <li>Turn on your LaserBeam driver. <a href="https://resources.sienci.com/view/lb-turning-driver-on/">Go here</a> if you want to refresh your memory on how to do this. If your driver doesn’t turn on, don’t necessarily attribute this to an issue with the board right away. First double check all these conditions are met since they are sometimes easy to forget.</li>
  <li>In gSender, navigate to the Spindle/Laser tab in the Settings and toggle it on.</li>
</ol>

![](/_images/_superlongboard/_upgrading/slb_upgrading_p36_HomingDirection.jpg){.aligncenter .size-medium}

Back on the main screen in the bottom right corner, navigate to the Spindle/Laser tab and select “SLB_LASER” in the dropdown list. After this, flip the toggle at the top to ‘Laser Mode’.

![](/_images/_superlongboard/_upgrading/slb_upgrading_p38_SLBSpindle.jpg){.aligncenter .size-medium}

<p style="text-align: center;"><em><strong>Note: Ensure that you are wearing your safety glasses!</strong></em></p>
Ensure your power is set to 1% and your ‘Test Duration’ to one second. Now when you hit the ‘Laser Test’ button your diode should momentarily emit a faint beam. This means that the SLB is controlling your laser successfully!

![](/_images/_superlongboard/_upgrading/slb_upgrading_p39_LaserTest.jpg){.aligncenter .size-medium}

If the laser testing didn’t go as planned, check your wiring and that you’ve turned on your driver correctly. If you go back through the steps still with no success, you can always read more about laser setup on our more advanced <a href="https://resources.sienci.com/view/slb-manual/#laser">SLB Manual page</a>.

<h2>Routing</h2>

The SLB enclosure has wire management built-in to keep all your wires in place if you ever need to open the cover and look at the inside. Use these by routing all the wires inside the enclosure through the two cable guides at the <strong>Back</strong>.

<ul>
  <li>The smaller, #1 enclosure is meant to fit all 4 motor cables snugly</li>
  <li>The larger #2 opening should fit all wires other than the motor cables</li>
</ul>

![](/_images/_superlongboard/_upgrading/slb_upgrading_p40_CaseWires.jpg){.aligncenter .size-medium}

Here you can see all of the motor cables are routed.

![](/_images/_superlongboard/_upgrading/slb_upgrading_p41_WiresPlugged.jpg){.aligncenter .size-medium}

Once all of your cables are routed correctly out the back of the board, you can put the cover back in place. Simply tilt the cover back into the slot on the bottom of the case, ensuring the keyhole is over the screw, then slide the cover to the left

![](/_images/_superlongboard/_upgrading/slb_upgrading_p42_Case1.jpg){.aligncenter .size-medium}

Once the cover is in place, turn the thumbscrew clockwise until finger tight. If you notice a small gap between the cover and the back of the case, this is by design to ensure that the cover maintains a tight fit over time.

![](/_images/_superlongboard/_upgrading/slb_upgrading_p43_Case2.jpg){.aligncenter .size-medium}

<h2>Mounting</h2>

You can mount your SLB however you like. Some factors to consider might be your machine setup, computer location, if you have an enclosure, or if you want to access other things or see the pretty lights on the board. The most versatile way is the 4 holes in the SLBs enclosure which will allow you to mount it to any flat surface, but if you have a LongMill MK2 you also have the option to mount it directly to your Y-axis rail (not compatible with MK1).

Some of the extra tools you may need for this step:

<ul>
  <li><strong>Bolting to MK2 Rail</strong> - M5 Allen wrench, plus grab the hardware and bracket provided with the SLB</li>
  <li><strong>Screw Down / Flat Mounting</strong> - 2 to 4 wood screws (minimum size #4 or ¾” and min length of ½”) plus the necessary screwdriver or bit driver</li>
</ul>

<h3>Bolt to Rail</h3>

For rail mounting, slide the two T-nuts onto the track above the left Y-rail and loosely thread on the two M5 bolts. You may need to remove your limit switch on MK2’s temporarily to enable the nuts to be slid into the rail.

![](/_images/_superlongboard/_upgrading/slb_upgrading_p44_Mount1.png){.aligncenter .size-medium}

Insert the sheet metal bracket into the slot at the back of the SLB enclosure. The bracket will feel loose for now so you’ll want to hold it in place until the next step.

![](/_images/_superlongboard/_upgrading/slb_upgrading_p45_Mount2.png){.aligncenter .size-medium}

Place the bracket-enclosure assembly onto the Y-rail and slide the two screws into the slots in the bracket, then tighten the two screws with an Allen key to lock the entire assembly onto the rail.

![](/_images/_superlongboard/_upgrading/slb_upgrading_p46_Mount3.jpg){.aligncenter .size-medium}

<h3>Screw Down</h3>

You can mount your SLB flat on your wasteboard next to your machine, or even on the side or at the back of your workstation. You can also hang the SLB vertically. The enclosure has been designed with reasonable consideration for dust penetration and vibration, but if you are a more cautious person you can feel free to mount the box further away from your CNC.

When placing your SLB on its own or among other CNC control electronics, consider that most wires are designed to route out the backside of the enclosure with the exception of a handful of more typically accessible plugs on its front like the E-stop and USB.

![](/_images/_superlongboard/_upgrading/slb_upgrading_p47_2Mounts.png){.aligncenter .size-medium}

It’s easy to use the enclosure as a template to mark and drill the holes. The holes are 4.5mm large, spaced 45mm from each other and 230mm from the opposite pair. They’re not perfectly centered on the box but close to it.

You can use whatever bolt or screw type you like but the easiest approach is to use a minimum of 2 countersunk wood screws on diagonal holes from size #4-#8 and a minimum length of ½”. You might have to remove some of the plugs on the ends to access the holes when you screw down the enclosure.

Congrats!!! You have successfully completed all the general assembly and setup to get your SuperLongBoard up and running.

<h2>Time to Smell the Roses</h2>

This section on ‘Upgrading to the SLB’ was written to cover all the necessities that the SLB has to offer by default, so you should now find that your machine can:

<ul>
  <li>Run more reliably</li>
  <li>Cut, jog, and home faster</li>
  <li>Run more quietly at many speeds</li>
  <li>Safer E-stop that de-powers motor and disables accessories</li>
  <li>Probe more quickly and easily off touch plates</li>
  <li>Perform faster and smoother laser engraving</li>
</ul>

This covers a lot of the important stuff that likely drew many of you towards picking up the SLB! If you weren’t planning to do anything more complicated with your SLB yet, then we’d recommend that you stop here for now so you can enjoy all the new perks.

That said, the SLB is still capable of plenty more if you were planning to dive into a bit more complexity with wiring and firmware configuration. These are all covered on the <a href="https://resources.sienci.com/view/slb-manual/">SLB Manual page</a>, such as:

<ul>
  <li>Ethernet Hookup</li>
  <li>LED Strips</li>
  <li>More help for Laser setups</li>
  <li>Using the Action Buttons on the E-stop</li>
  <li>Other Accessory Outputs</li>
  <li>Setting up Spindle/RS485</li>
  <li>Tool Length Sensor</li>
  <li>Fully independent rotary 4th axis</li>
</ul>

<h2>New Behaviours to Expect</h2>

There will be some new behaviours to expect from your SLB compared to the way you’re likely used to your previous board behaving. Take your time to understand them and before you know it they’ll become normal too!

<ul>
  <li>For now, the SLB will continue working the best with any typical ‘grbl’ post processor setup. If you already had a working grbl setup then you won't need to change anything.</li>
  <li>Whenever you press the <strong>E-stop, expect an ‘Alarm 10’</strong> to appear. This shows that the board saw your E-stop press and will shut down the motors and all other accessories. Once you untwist the E-stop (the light will come back on), you’ll be able to unlock the machine and continue what you were doing. The E-stop will cancel any currently active job, so if you want to resume you’ll want to re-probe or re-home and then use ‘Start from Line’ to resume the job back where you left off.</li>
</ul>

![](/_images/_superlongboard/_upgrading/slb_upgrading_p48_Unlock.jpg){.aligncenter .size-medium}

<ul>
  <li>The yellow ‘processing’ lines in the gSender visualizer might extend out further when you’re running a job, this is just because the SLB can store more future movements in its memory than other boards</li>
  <li><strong>Swapping between the Spindle/Laser is a bit more involved</strong>, the SLB Manual page goes into it a bit more on it. Because of this, we’d recommend that you set up your SLB for whatever Spindle/Laser output you’d tend to use as your default, so that you can just power on your machine and not have to worry about many other steps after that.</li>
  <li>There will always show the ‘Unlock’ button in gSender. This is because there might be some times where if your SLB gets stuck, you can use the ‘Unlock’ button to help recover it.</li>
  <li>This should never change after your first setup, but you’ll need to make sure that from now on you always connect to gSender or other g-code senders with ‘grblHAL’ being the selected firmware</li>
</ul>

![](/_images/_superlongboard/_upgrading/slb_upgrading_p49_grblHAL.png){.aligncenter .size-medium}

<ul>
  <li>Some settings in gSender aren’t used anymore since the SLB stores them itself. This includes the Spindle/Laser settings for spindle min/max speed, laser min/max power, and laser axes offset, as well as all the Rotary settings except for the Rotary toggle.</li>
  <li>Looking at the gSender Firmware Tool
<ul>

  <li>Default machine profiles will be working correctly as of gSender 1.4.6</li>
  <li>There are now a lot more settings and categories, but if you’re not using any advanced features then you can ignore them</li>
  <li>Some of the new settings can only fully apply once you’ve powered off and back on the SLB</li>
  <li>The process for flashing grblHAL will now require that you get the most up-to-date firmware version for your SLB; the firmware and the process for flashing can both be found on the <a href="https://resources.sienci.com/view/slb-manual/#firmware-flashing">SLB Manual page</a></li>
</ul>
</li>
</ul>

<h2>Troubleshooting</h2>

If you are still running into any issues with your new SLB, please see the <a href="https://resources.sienci.com/view/slb-manual/#troubleshooting">Troubleshooting Section</a> on our more Detailed page. You can also always contact us directly at <a href="mailto:support@sienci.com">support@sienci.com</a>.

&nbsp;
