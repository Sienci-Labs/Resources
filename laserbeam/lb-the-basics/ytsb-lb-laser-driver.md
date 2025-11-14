---
title: ytsb Laser Driver
menu_order: 3
post_status: draft
post_excerpt: 
post_date: 2021-12-23 12:56:20
taxonomy:
    knowledgebase_cat: lb-the-basics
    knowledgebase_tag:
        - laser
custom_fields:
    KBName: LaserBeam
    basepress_post_icon: bp-caret-right
skip_file: yes
featured_image: 
---

<span style="color: #800000;"><strong>Important Message:</strong></span>

<em><span style="color: #800000;"><strong>Do not use a current meter on your LaserBeam driver</strong></span>, those of you who are having trouble getting your Laser to run might be tempted to use a current meter to try testing the LaserBeam driver. Do not do this, the LaserBeam Driver produces a lot of current and when trying to measure it you will feed the current back into the driver damaging it and causing it to no longer work. This laser product is not a toy and handles large amounts of power that can be very dangerous for you and the equipment itself.</em>

To properly control the laser diode, a driver board must be made, consisting of many electronic components. These components will determine how the laser is turned on, and what the output power and wavelength of the laser beam will be - all while protecting the laser diode from electrical and thermal damage.

Our 5A constant current LaserBeam driver was designed to provide a maximum of 5A of constant current to the 7W LaserBeam diode assembly. Our driver has been designed in compliance with Class 4 requirements;  it includes a key switch, remote interlock, power fault protections, power reset button and emission LED, keeping users safe and meeting all necessary requirements. Made to be plug and play with the Sienci Labs LongMill Benchtop CNC, it can receive the PWM signal and operate as a laser attachment.

<img class="aligncenter size-full wp-image-4365" src="https://resources.sienci.com/wp-content/uploads/2021/12/laser_box_E1.jpg" alt="" width="850" height="368" />
<h3></h3>
<h3><b>Laser Driver Specifications</b></h3>
<table>
<tbody>
<tr>
<td>Current Output Range</td>
<td>0-5 A</td>
</tr>
<tr>
<td>Current Limit Dip Switch Settings</td>
<td>1A, 2A, 3A, 4A, 5A</td>
</tr>
<tr>
<td>Compliance Voltage </td>
<td>6V</td>
</tr>
<tr>
<td>Input Power</td>
<td>12V 8A</td>
</tr>
<tr>
<td>Laser Diode Protection</td>
<td>Current Limit</td>
</tr>
<tr>
<td>Minimum “on” Control Signal Voltage</td>
<td>3V</td>
</tr>
<tr>
<td>Maximum “on” Control Signal Voltage</td>
<td>12V</td>
</tr>
<tr>
<td>Maximum Control Signal Frequency </td>
<td>30Khz</td>
</tr>
<tr>
<td>Connector Type</td>
<td>Pluggable Terminal Block</td>
</tr>
<tr>
<td>Operating Temperature</td>
<td>0 - 40 C</td>
</tr>
<tr>
<td>Storage Temperature</td>
<td>-40 -70 C</td>
</tr>
</tbody>
</table>
<h3><b>Laser Driver Functionality</b></h3>
<ul>
  <li><b>Power switch:</b> Turns the driver ON/OFF</li>
  <li><b>Power input:</b> 12V Power supply input</li>
  <li><b>PWM sIgnal input:</b> 3V - 12V PWM signal input</li>
  <li><b>Maximum current DIP switch:</b> Set maximum current between 0A-5A</li>
  <li><b>Laser diode output:</b> Provide constant current to laser diode assembly</li>
  <li><b>Fan output 1:</b> 12V output to power the driver cooling fan</li>
  <li><b>Fan output 2:</b> 12V output to power the diode assembly cooling fan</li>
  <li><b>Fan output 3:</b> 12V output to power the air assist fan or other 12V  accessories</li>
  <li><b>Power reset button:</b> Reset to allow the driver to turn ON</li>
  <li><b>Interlock:</b> Add a switch or E-stop to allow more control over when driver can be turned on</li>
  <li><b>Key switch:</b> Allow for only authorized users with a key to operate laser driver</li>
</ul>
<img class="alignnone size-medium wp-image-2252" src="https://resources.sienci.com/wp-content/uploads/2021/12/5A-Constant-Current-Laser-Driver-1-850x638.jpg" alt="" width="850" height="638" />
<p style="text-align: center;"><b>Front view of 5A constant current laser driver assembly</b></p>
<img class="alignnone size-medium wp-image-2253" src="https://resources.sienci.com/wp-content/uploads/2021/12/5A-Constant-Current-Laser-Driver-2-850x638.jpg" alt="" width="850" height="638" />
<p style="text-align: center;"><b>Right side view of 5A constant current laser driver assembly</b></p>
<img class="alignnone size-medium wp-image-2254" src="https://resources.sienci.com/wp-content/uploads/2021/12/5A-Constant-Current-Laser-Driver-3-850x638.jpg" alt="" width="850" height="638" />
<p style="text-align: center;"><b>Back view of 5A constant current laser driver assembly</b></p>
<img class="alignnone size-medium wp-image-2255" src="https://resources.sienci.com/wp-content/uploads/2021/12/5A-Constant-Current-Laser-Driver-4-850x638.jpg" alt="" width="850" height="638" />
<p style="text-align: center;"><b>Left side view of 5A constant current laser driver assembly</b></p>
&nbsp;
<h3><b>Laser Driver Safety &amp; Compliance</b></h3>
<b>Integrated Driver Safety Features</b>

<b>Key switch:</b> The key needs to be inserted into the key switch and turned 90 degrees clockwise to the ON position to enable the laser driver (along with the remote interlock enabled and power reset pushed) If the key is turned to the OFF position the driver will turn off immediately and will not turn on.

<b>Remote interlock:</b> The interlock connection needs to be closed to enable the laser driver (along with the key switch enabled and power reset pushed). This allows for additional switches to be added to the laser driver. An E-stop or other system can be implemented to shut the laser driver down in the case of an emergency. If the remote interlock connection is open,  the driver will turn off immediately and will not turn on until the connection is closed.

<b>Power fault protection:</b> If the driver ever loses power the laser will turn off. In case of a power outage, you can have peace of mind knowing that the laser is off whenever power returns.

<b>Power reset button:</b> If the driver is turned off in any way other than the main power switch, the power reset button needs to be pushed in order to turn the driver on again.

<b>Emission indicator:</b>  This LED located on the LaserBeam driver will notify you if the laser output is on. This becomes useful if operating outside the visible light spectrum.
