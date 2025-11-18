---
title: ytsb Common Issues and Fixes
menu_order: 5
post_status: draft
post_excerpt: 
post_date: 2024-09-13 14:30:20
taxonomy:
    knowledgebase_cat: lb-handbook
    knowledgebase_tag:
        - laser
custom_fields:
    KBName: LaserBeam
    basepress_post_icon: bp-caret-right
skip_file: yes
featured_image: 
---

Below are potential issues you may run into, which could be resolved through the instructions provided.
<h3>Laser driver is not turning on</h3>
<p style="padding-left: 40px;">1. First check that the power supply is plugged into power. A faulty wall outlet, power bar or extension cable could also impact your issue. </p>
<p style="padding-left: 40px;">2. Ensure the wire connection from the power supply to the driver is secured, and matches the polarity as shown in the photo below. </p>
<img class="wp-image-10703 aligncenter" src="https://resources.sienci.com/wp-content/uploads/2024/09/power-to-driver.png" alt="" width="709" height="399" />

<img class="wp-image-10704 aligncenter" src="https://resources.sienci.com/wp-content/uploads/2024/09/polarity-LaserBeam-power-e1726253303399.png" alt="" width="718" height="403" />
<p style="padding-left: 40px;">3. Verify that the single LED on the power supply is ON, it should be a green or blue light. If this is OFF then there is a problem with the power supply receiving power. </p>
<img class="wp-image-10705 aligncenter" src="https://resources.sienci.com/wp-content/uploads/2024/09/power-supply.png" alt="" width="811" height="456" />
<p style="padding-left: 40px;">4. Make sure you are starting up the driver in the correct order: </p>
<p style="padding-left: 80px;">i. Ensure the interlock connector is secured </p>
<p style="padding-left: 80px;">ii. Insert the driver key into the key switch, then push and turn the key 90 degrees clockwise</p>
<p style="padding-left: 80px;">iii. Press the power reset button </p>
<p style="padding-left: 80px;">iv. Flip the power switch on (to "1" position) </p>
<p style="padding-left: 40px;">5. Using a voltmeter or a multimeter, measure the voltage from power supply to driver. <b>Warning: Set your device to DC voltage mode before measuring. If the multimeter is in current mode, the LaserBeam Driver will feed the current back into the driver and damage it.</b> On the power supply male connector, use the red probe for the red wire and the black probe for the black wire. The reading should be <b>positive</b>, and be approximately <b>12V</b>. </p>
  <img class="wp-image-10706 aligncenter" src="https://resources.sienci.com/wp-content/uploads/2024/09/power-supply-to-driver-voltage-reading.png" alt="" width="747" height="420" />
<h3><b>Laser driver is on, but unable to fire </b></h3>
This should also mean that the driver power LED is ON but when you press "Laser On" on gSender, the emissions LED remains OFF.
<p style="padding-left: 40px;">1. Make sure that only a singular DIP switch is down (any one of them) and that the <b>SLB_LASER</b> is selected on gSender and is in "<b>Laser Mode</b>." </p>
<img class="wp-image-10707 aligncenter" src="https://resources.sienci.com/wp-content/uploads/2024/09/DIP-switch-inserted.png" alt="" width="809" height="455" />

<img class=" wp-image-10708 aligncenter" src="https://resources.sienci.com/wp-content/uploads/2024/09/lasermode-laseron.png" alt="" width="862" height="485" />
<p style="padding-left: 40px;">2. Turn OFF the laser driver and check that the lens is not damaged in any way. Any sort of imperfection could prevent the laser from firing, which could include cracks and melting within the glass.  </p>

<h3><b>Laser is unable to fire at full power </b></h3>
<p style="padding-left: 40px;">1. High speeds and accelerations could cause the laser to mark incompletely, which makes it look like it is unable to fire at full power. This is especially important if you have the AltMill, because the SLB-EXT default settings are much higher. We recommend the following firmware settings: </p>
<p style="padding-left: 40px;">$110 = 4000
$111 = 4000
$120 = 750
$121 = 750</p>
<p style="padding-left: 40px;">2. A weak laser could be due to the controller's inability to provide 4-5V through its PWM signal output.</p>
<p style="padding-left: 40px;">For the <b>LongBoard</b> try plugging your controller into another USB port on your computer, or using a different computer altogether, since the LongBoard receives power through the USB connection. </p>
<p style="padding-left: 40px;">For any controller, we can measure the PWM voltage to verify if sufficient voltage is being outputted. </p>
<p style="padding-left: 40px;"><span style="color: #800000;"><b>Wear your safety glasses before proceeding! </b></span></p>
<p style="padding-left: 40px;">Open gSender. Turn ON your driver and press "Laser On" to fire your laser. Make sure "Power" is set to <b>100%.</b> </p>
<img class="wp-image-10709 aligncenter" src="https://resources.sienci.com/wp-content/uploads/2024/09/laser-on-100.png" alt="" width="825" height="464" />
<p style="padding-left: 40px;"><span style="color: #800000;"><b>Warning: Set your device to DC voltage mode before measuring. If the multimeter is in current mode, the LaserBeam Driver will feed the current back into the driver and damage it. </b></span></p>
<p style="padding-left: 40px;">At the "LASER" connection, use the <b>red</b> probe on the "<b>PW</b>" side of the screw terminal, and the <b>black</b> probe on the "<b>GD</b>" side of the screw terminal. You should get a reading of about 4.5V.  </p>
<img class="alignnone size-full wp-image-10710" src="https://resources.sienci.com/wp-content/uploads/2024/09/LB-probe.png" alt="" width="960" height="540" />

<b><i>*Note:</i></b> <i>This photo shows the probing an SLB, if this was the LongBoard, the process is the exact same except the connector would be plugged into the SpinPWM and ground terminals</i>
<h3>The lens is too loose on my laser</h3>
Ensure you have the correct spring assembled for your specific lens. Additionally, you can add another spring (of the same type) to provide more tension.
<h3><b>SLB_LASER option is missing on gSender</b></h3>
This is due to improper firmware settings on the SLB. On the gSender Firmware tool, make sure <strong>$395</strong> is set to <strong>SLB_SPINDLE (or H-100 if you have the Sienci Labs Spindle)</strong> and <strong>$511</strong> is set to <strong>SLB_LASER. </strong><img class="wp-image-10700 aligncenter" style="font-size: 16px;" src="https://resources.sienci.com/wp-content/uploads/2024/09/default-spindle-e1726252649696.png" alt="" width="845" height="336" /><img class="wp-image-10699 aligncenter" src="https://resources.sienci.com/wp-content/uploads/2024/09/511-spindle-1-e1726252631732.png" alt="" width="863" height="302" />

Press <strong>"Apply New Settings"</strong> then turn the control board OFF then ON.

<img class=" wp-image-10701 aligncenter" src="https://resources.sienci.com/wp-content/uploads/2024/09/power-cycle-laser.png" alt="" width="834" height="469" />

You should be able to see the option on gSender now, once you reconnect.

<img class="alignnone size-full wp-image-10702" src="https://resources.sienci.com/wp-content/uploads/2024/09/slb-laser-selection-e1726256404701.png" alt="" width="956" height="451" />
<h3>My laser offsets are incorrect</h3>
For the <b>LongBoard</b>, you must save the offsets locally through the preferences (gear icon) on gSender. For the <b>SLB/SLB-EXT</b>, you must save the offsets on the board itself, by going through the Firmware Tool. Make sure you input the offset values as<b> millimeters,</b> otherwise it will not work. For more detailed steps on laser offsets, check this <a href="https://resources.sienci.com/view/using-offsets-in-gSender/">resource page.</a>
<p style="text-align: center;"><img class="alignnone size-full wp-image-10711" src="https://resources.sienci.com/wp-content/uploads/2024/09/laser-offset.png" alt="" width="960" height="540" /><i>Laser offsets on Firmware Tool ($741, $742) vs. Preferences settings  </i></p>

<h3>Firmware settings are not saving</h3>
Some firmware settings will specify that you need to turn off and on (power cycle) your control board, in order for the changes to take effect. As best practice, we recommend power cycling every time you make firmware changes.  

<img class="size-full wp-image-10701 aligncenter" src="https://resources.sienci.com/wp-content/uploads/2024/09/power-cycle-laser.png" alt="" width="960" height="540" />

If you are unable to find a solution and are still looking for assistance, please feel free to <a href="https://sienci.com/contact-us/">contact us.</a>
