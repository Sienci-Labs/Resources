---
title: ytsb Changing Microstepping
menu_order: 4
post_status: draft
post_excerpt: How to change microstepping on the LongMill Benchtop CNC to improve accuracy in machine movement. This will cause motors to move more or less per signal.
post_date: 2024-04-30 17:33
taxonomy:
    knowledgebase_cat: lm-advanced
    knowledgebase_tag:
        - mk1
custom_fields:
    KBName: LongMill CNC
    basepress_post_icon: bp-caret-right
skip_file: no
featured_image: /_images/_longmill/_advanced/lm_Stepper_p1.jpg
---
<!-- wp:paragraph -->
<p>Every LongMill is powered by our LongBoard CNC controller which has four integrated TB6600 stepper motor drivers (pictured). By default, we set each driver to 1/8 microstepping via the onboard DIP switches. We chose 1/8 microstepping because we found that it's a good balance between motor resolution and torque output. The theoretical resolution with this setup is 0.005mm.

![](/_images/_longmill/_advanced/lm_Stepper_p1.jpg){.aligncenter .size-medium}
</p>

<!-- wp:heading -->
<h2>What is Microstepping</h2>
<!-- /wp:heading -->

<!-- wp:paragraph -->
<p>Stepper motors have a fixed number of steps in their internal rotor which determine the steps required to make a full, 360-degree rotation. With these steps in mind, the controller drivers can "step" forward or backward however many times to rotate each axis motor. The NEMA 23s used on the LongMill are split up to 200 individual steps. This might seem like a lot, but in many cases more accurate control is still needed.</p>
<p>Microstepping is a technique that allows for steps to be broken down into 'sub-steps' so that the stepping resolution can be increased. This allows us to:</p>
<!-- /wp:paragraph -->

<!-- wp:paragraph --><!-- /wp:paragraph -->

<!-- wp:paragraph --><!-- /wp:paragraph -->

<!-- wp:list -->
<ul>
<li>Have a smoother movement in the motors themselves</li>
<li>Improve positional accuracy (read more here: <a href="https://hackaday.com/2016/08/29/how-accurate-is-microstepping-really/" target="_blank" rel="noopener">https://hackaday.com/2016/08/29/how-accurate-is-microstepping-really/</a> )</li>
</ul>
<!-- /wp:list -->

<!-- wp:paragraph -->
<h2>Current Values</h2>
<p>Currently, the steps/mm EEPROM settings in the LongMill (<em>$100, </em><em>$101, </em>and <em>$102</em>) are set to 200. This value helps the controller turn g-code into linear movements, then into rotational step signals for the motors. This number comes from taking the values below and running them through the formula:</p>
<ul>
<li>LongMill stepper motors are <strong>200</strong> steps/rotation</li>
<li>Drivers set to <strong>1/8</strong> microstepping by default</li>
<li>Each axis is direct drive and Z-axis has <strong>1-to-1</strong> pulley ratio</li>
<li>Our lead screws have a <strong>2mm</strong> pitch and are <strong>4-start, </strong>2mm x 4 = 8mm <strong>lead</strong></li>
</ul>
<p><em>Steps/mm  =   Steps/revolution</em><em>  </em><strong>/</strong><em>  (microstepping value  </em>x<em>  gearing ratio from motor to lead screw  </em>x<em>  lead screw pitch  </em>x<em>  # of starts)</em></p>
<p>This gives us:  200  /  (1/8  x  1  x  2  x  4)  =  <em>200 steps/mm</em></p>
<h2>Changing Microstepping</h2>
<p>If you'd like to change your machines microstepping values, you'll have to:</p>
<ol>
<li>Change the positions of the desired drivers onboard DIP switches and</li>
<li>Set the EEPROM setting to match.</li>
</ol>
<p>For example, changing the Z-axis driver to have 1/16 microstepping would require following the table below and then in your UGS console sending the command "<em>$102  = 400</em>" to set the appropriate steps/mm of the Z-axis.</p>
<p>Each driver can be adjusted to use either single-step or 1/2 step, 1/4 step, 1/8 step, and 1/16 step microstepping. Bare in mind that changes to the DIP switches should only be made when your LongMill is powered off. Also, understand that if you play with microstepping you'll find that positional resolution and torque tend to be inversely proportional.</p>
<!-- /wp:paragraph -->

<!-- wp:paragraph --><!-- /wp:paragraph -->

<!-- wp:table -->
<table class="wp-table" width="50%">
<tbody>
<tr>
<td> </td>
<td>M1</td>
<td>M2</td>
<td>M3</td>
</tr>
<tr>
<td>1 Step</td>
<td>OFF</td>
<td>OFF</td>
<td>ON</td>
</tr>
<tr>
<td>1/2 Step</td>
<td>OFF</td>
<td>ON</td>
<td>OFF</td>
</tr>
<tr>
<td>1/4 Step</td>
<td>ON</td>
<td>OFF</td>
<td>OFF</td>
</tr>
<tr>
<td>1/8 Step</td>
<td>ON</td>
<td>OFF</td>
<td>ON</td>
</tr>
<tr>
<td>1/16 Step</td>
<td>ON</td>
<td>ON</td>
<td>OFF</td>
</tr>
</tbody>
</table>
<p>&nbsp;</p>
<!-- /wp:table -->
