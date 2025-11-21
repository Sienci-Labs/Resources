---
title: ytsb Cables and Connections
menu_order: 4
post_status: draft
post_excerpt: 
post_date: 2021-12-23 12:56:20
taxonomy:
    knowledgebase_cat: lb-assembly
    knowledgebase_tag:
        - laser
custom_fields:
    KBName: LaserBeam
    basepress_post_icon: bp-caret-right
skip_file: yes
featured_image: 
---

<h3><strong>Parts List:</strong></h3>
<ul>
  <li>Laser diode extension cable (2.5m, blue)</li>
  <li>Laser cooling fan extension cable (2.5m, red) </li>
  <li>Air assist extension cable (2.5m, yellow) </li>
  <li>PWM signal extension cable (0.6m, purple) </li>
  <li>LaserBeam driver</li>
</ul>
If you have the AltMill you will need a longer set of extension cables, which will be released soon. In the meantime you can run the existing cables outside of the drag chain, fastened with zip ties.

If you wish to route the laser cables through the LongMill drag chain, you will need to unclip all the drag chain links.  

<img class="alignnone size-full wp-image-10847 aligncenter" src="https://resources.sienci.com/wp-content/uploads/2021/12/unclippingdragchain_short-1.gif" alt="" width="576" height="324" />
<p style="text-align: center;"><i>Unclipping drag chain links using flat head screwdriver </i></p>
Route the blue, red and yellow cables through the entire drag chain, making sure the cables are able to reach the connectors at the laser.

<img class="size-full wp-image-10815 aligncenter" src="https://resources.sienci.com/wp-content/uploads/2021/12/laser-wire-routing-front.png" alt="" width="960" height="540" />
<p style="text-align: center;"><i>Front view of cable routing path</i></p>
<img class="size-full wp-image-10816 aligncenter" src="https://resources.sienci.com/wp-content/uploads/2021/12/laser-wire-routing.png" alt="" width="960" height="540" />
<p style="text-align: center;"><i>Back view of cable routing path</i></p>
<img class="alignnone size-full wp-image-10792" src="https://resources.sienci.com/wp-content/uploads/2021/12/cables-at-front.png" alt="" width="960" height="540" />
<p style="text-align: center;"><i>Blue, red and yellow cable connectors next to laser diode assembly </i></p>
For each connection, make sure that the red wire from the female side meets with the red wire from the male side. Attach the fan connector to the red cable. Attach the diode connector to the blue cable. Make sure not to mix the diode and fan connections!

<img class="alignnone size-full wp-image-10835" src="https://resources.sienci.com/wp-content/uploads/2021/12/red-and-blue-connections-close-up.png" alt="" width="960" height="540" />
<p style="text-align: center;"><i>Red and blue cables connected to cooling fan and diode respectively</i></p>
<img class="alignnone size-full wp-image-10834" src="https://resources.sienci.com/wp-content/uploads/2021/12/red-and-blue-connection.png" alt="" width="960" height="540" />
<p style="text-align: center;"><i>Cooling fan and diode connections</i></p>
Once you are sure the cables are properly positioned and attached, close your drag chain tabs.

The following instructions will detail cable connections to the laser driver and/or CNC control board, whether you have the SLB/SLB-EXT or the LongBoard.
<h3><b>Laser diode → Driver</b></h3>
The laser diode will receive power through the driver. Assuming one end of the blue cable is already plugged into the diode, connect the blue cable to the driver. Make sure that the location of the driver connection is correct as shown.

<img class="size-full wp-image-10807 aligncenter" src="https://resources.sienci.com/wp-content/uploads/2021/12/laser-diode-to-driver.png" alt="" width="960" height="540" />
<p style="text-align: center;"><i>Laser diode to driver connection</i></p>

<h3><b>Cooling Fan → Driver</b></h3>
The cooling fan will also receive power through the driver. Assuming one end of the red cable is already plugged to the fan, connect the red cable to the driver. Make sure that the location of the driver connection is correct as shown.

<img class="size-full wp-image-10798 aligncenter" src="https://resources.sienci.com/wp-content/uploads/2021/12/fan-to-driver.png" alt="" width="960" height="540" />
<p style="text-align: center;"><i>Cooling fan to laser driver connection</i></p>

<h3><b>Air Assist → Driver (Optional) </b></h3>
To simplify your building process, we will leave the air assist assembly off the diode. However, we can plug one end of the yellow cable into the driver, leaving the other end free, in case you need to use air assist in the future. Make sure that the location of the driver connection is correct as shown.

<img class="alignnone size-full wp-image-10843" src="https://resources.sienci.com/wp-content/uploads/2021/12/yellow-cable-to-driver.png" alt="" width="960" height="540" />
<p style="text-align: center;"><i>Air assist to laser driver connection</i></p>

<h3><b> Driver → Controller </b></h3>
This connection allows you to control your laser through the CNC controller. The driver uses this PWM signal to turn on/off the laser, as well as adjust the intensity and frequency.

On one end, plug in the male connector to the driver's PWM signal input, at the location shown in the photo.

<img class="alignnone size-full wp-image-10833 aligncenter" src="https://resources.sienci.com/wp-content/uploads/2021/12/pwm-wire.png" alt="" width="960" height="540" />
<p style="text-align: center;"><i>Connecting PWM signal input to driver</i></p>
<span style="color: #800000;"><b>The following steps will vary whether you have the LongBoard or the SLB. Please read carefully to ensure you complete the proper steps for your controller.</b></span>

For the <b>LongBoard</b>, plug in one end of the purple cable to the controller, making sure the red wire is seated at the "SpinPWM" and the black wire is seated at "GND."

<img class="alignnone size-full wp-image-2250" src="https://resources.sienci.com/wp-content/uploads/2021/12/PWM-Signal-Cable-LongMill-Benchtop-CNC-Controller-Connection.jpg" alt="" width="960" height="720" />
<p style="text-align: center;"><i>Connecting PWM signal input to LongBoard </i></p>
If your controller is an <b>SLB or SLB-EXT</b>, you will plug in the cable at the "LASER" port. Ensure that the red wire cable is seated at the "PW" port and the black wire is seated at the "GD<b>"</b> port.

<img class="size-full wp-image-10839 aligncenter" src="https://resources.sienci.com/wp-content/uploads/2021/12/slb-laser-wiring.jpg" alt="" width="2048" height="1272" />
<p style="text-align: center;"><i>Side view of SLB with LASER port indicated</i></p>
<img class="alignnone size-full wp-image-10848" src="https://resources.sienci.com/wp-content/uploads/2021/12/laser-slb-connection.png" alt="" width="960" height="540" />
<p style="text-align: center;"><i>Front view of SLB with PWM signal connector inserted </i></p>
<p style="text-align: center;"></p>
