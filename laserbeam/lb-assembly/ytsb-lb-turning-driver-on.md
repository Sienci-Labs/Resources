---
title: ytsb Turning Driver On
menu_order: 6
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

<h3>Power On Procedure</h3>
These steps must be followed in this order to successfully turn on the driver.

1. Ensure the power supply is getting power and the interlock connector is secure.
   <img src="https://resources.sienci.com/wp-content/uploads/2021/12/power-supply.png" alt="" width="960" height="540" />
   <p style="text-align: center;"><em>Power supply indicator</em></p>
   <img src="https://resources.sienci.com/wp-content/uploads/2021/12/interlock.png" alt="" width="960" height="540" />
   <p style="text-align: center;"><em>Interlock connector on </em></p>
2. Insert the driver key into the key switch, then push and turn the key 90 degrees clockwise
   <img src="https://resources.sienci.com/wp-content/uploads/2022/01/key-resized.gif" alt="" width="726" height="408" />
3. Press the power reset button, you can use an Allen key if it is difficult to press
   <img src="https://resources.sienci.com/wp-content/uploads/2021/12/power-reset.png" alt="" width="960" height="540" />
4. Flip the power switch ON (“1” position)
   <img src="https://resources.sienci.com/wp-content/uploads/2021/12/power-switch-driver.png" alt="" width="960" height="540" />

You should hear a fan sound, with 1 red LED lighting up in your driver. If none of this happens, there may be a wiring mistake.

<img src="https://resources.sienci.com/wp-content/uploads/2021/12/driver-LED.png" alt="" width="960" height="540" />
<p style="text-align: center;"><em>Top view of driver power LED on</em></p>
<img src="https://resources.sienci.com/wp-content/uploads/2021/12/driver-LED-1.png" alt="" width="960" height="540" />
<p style="text-align: center;"><em>Side view of driver power LED on</em></p>
The following information will focus on specific buttons and inputs and how to use them.
<h3>Interlock</h3>
If you are looking to install a different switch, you need to make sure it is a normally closed (NC) switch in order to enable driver functionality. Simply replace the interlock connector with your switch of choice.
<h3>Power Reset Button</h3>
Usually the power reset button does not need to be pressed during normal startup. If your driver is already enabled, pushing the power reset will do nothing. However, the button will need to be pressed if:
<ul>
  <li>If you're turning your driver on for the first time</li>
  <li>If the interlock was opened (the connector was removed)</li>
  <li>If the key was not in the enabled position in the key switch</li>
  <li>If you removed the power supply</li>
  <li>If your power source was cut (if the driver was turned off in any way other than through the power switch)</li>
  <li>Or any combination of the above situations</li>
</ul>
If those situations above happen:
<ol>
  <li>Ensure the power supply is getting power and the interlock connector is secured</li>
  <li>Turn the power switch OFF</li>
  <li>Insert the driver key into the key switch, then push and turn the key 90 degrees clockwise</li>
  <li>Press the power reset button</li>
  <li>Flip the power switch ON</li>
</ol>
<h3>LED indicators</h3>
There are two LED indicators to know. The first is the driver power LED, which will be on when you successfully turn on your driver.

<img src="https://resources.sienci.com/wp-content/uploads/2021/12/Driver-Power-LED-ON-e1726684220620.jpg" alt="" width="960" height="540" />
<p style="text-align: center;"><em>Driver power LED on</em></p>
The second LED indicator is for laser emission. It will turn on when your laser output is enabled (through gSender) and when the driver power LED is on.

<img src="https://resources.sienci.com/wp-content/uploads/2021/12/Laser-Emissions-LED-ON-e1726684293235.jpg" alt="" width="960" height="540" />
<p style="text-align: center;"><em>Laser emissions and driver power LEDs on</em></p>
Because the laser can be turned on at different intensities and off at different frequencies, this laser emissions LED will mimic the signal that your laser is receiving, relative to the LED’s max intensity.
