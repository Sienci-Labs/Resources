---
title: EEPROM Settings
menu_order: 4
post_status: draft
post_excerpt: How to modify EEPROM setting for the LongMill CNC. These settings control the speed and direction of movement, machine limits, and activation of limit switches.
post_date: 2024-04-30 17:29
taxonomy:
    knowledgebase_cat: lm-advanced
    knowledgebase_tag:
        - mk1
custom_fields:
    KBName: LongMill CNC
    basepress_post_icon: bp-caret-right
skip_file: no
featured_image: 
---
<p><!-- wp:paragraph --></p>
<em>For in-depth documentation on all of the settings in grbl and what they mean, visit:</em> <a href="https://github.com/gnea/grbl/wiki/Grbl-v1.1-Configuration">https://github.com/gnea/grbl/wiki/Grbl-v1.1-Configuration</a>.
<p><!-- /wp:paragraph -->

<!-- wp:paragraph --></p>
<p>You can make changes to your machine's settings by changing the values in your EEPROM. These are settings that will persist even after you power off your machine and control things like the maximum speed, the acceleration, steps per mm, and more.</p>
<p><!-- /wp:paragraph -->

<!-- wp:paragraph --></p>
<p>Start by sending the command "$$" to your machine. Your console will give you a list of values.</p>
<p><strong>DEFAULT SETTINGS</strong></p>
<p><!-- wp:table --></p>
<table class="wp-table" width="500px">
<tbody>
<tr>
<th>Value</th>
<th>Purpose</th>
</tr>
<tr>
<td><em>$0=10</em></td>
<td>Step pulse time [microseconds]</td>
</tr>
<tr>
<td><em>$1=100</em></td>
<td>Step idle delay [milliseconds]</td>
</tr>
<tr>
<td><em>$2=1</em></td>
<td>Step pulse invert [mask]</td>
</tr>
<tr>
<td><em>$3=5</em></td>
<td>Step direction invert [mask]</td>
</tr>
<tr>
<td><em>$4=1</em></td>
<td>Invert step enable pin [boolean]</td>
</tr>
<tr>
<td><em>$5=0</em></td>
<td>Invert limit pins [boolean]</td>
</tr>
<tr>
<td><em>$6=0</em></td>
<td>Invert probe pin [boolean]</td>
</tr>
<tr>
<td><em>$10=1</em></td>
<td>Status report options [mask]</td>
</tr>
<tr>
<td><em>$11=0.010</em></td>
<td>Junction deviation [millimeters]</td>
</tr>
<tr>
<td><em>$12=0.002</em></td>
<td>Arc tolerance [millimeters]</td>
</tr>
<tr>
<td><em>$13=0</em></td>
<td>Report in inches [boolean]</td>
</tr>
<tr>
<td><em>$20=0</em></td>
<td>Soft limits enable [boolean]</td>
</tr>
<tr>
<td><em>$21=0</em></td>
<td>Hard limits enable [boolean]</td>
</tr>
<tr>
<td><em>$22=0</em></td>
<td>Homing cycle enable [boolean]</td>
</tr>
<tr>
<td><em>$23=0</em></td>
<td>Homing direction invert [mask]</td>
</tr>
<tr>
<td><em>$24=25.000</em></td>
<td>Homing locate feed rate [mm/min]</td>
</tr>
<tr>
<td><em>$25 = 500.000</em></td>
<td>Homing search seek rate [mm/min]</td>
</tr>
<tr>
<td><em>$26 = 250</em></td>
<td>Homing switch debounce delay [milliseconds]</td>
</tr>
<tr>
<td><em>$27 = 1.000</em></td>
<td>Homing switch pull-off distance [millimeters]</td>
</tr>
<tr>
<td><em>$30 = 30000</em></td>
<td>Maximum spindle speed [RPM]</td>
</tr>
<tr>
<td><em>$31 = 0</em></td>
<td>Minimum spindle speed [RPM]</td>
</tr>
<tr>
<td><em>$32 = 0</em></td>
<td>Laser-mode enable [boolean]</td>
</tr>
<tr>
<td><em>$100 = 200.000</em></td>
<td>X-axis travel resolution [step/mm]</td>
</tr>
<tr>
<td><em>$101 = 200.000</em></td>
<td>Y-axis travel resolution [step/mm]</td>
</tr>
<tr>
<td><em>$102 = 200.000</em></td>
<td>Z-axis travel resolution [step/mm]</td>
</tr>
<tr>
<td><em>$110 = 4000.000</em></td>
<td>X-axis maximum rate [mm/min]</td>
</tr>
<tr>
<td><em>$111 = 4000.000</em></td>
<td>Y-axis maximum rate [mm/min]</td>
</tr>
<tr>
<td><em>$112 = 3000.000</em></td>
<td>Z-axis maximum rate [mm/min]</td>
</tr>
<tr>
<td><em>$120 = 750.000</em></td>
<td>X-axis acceleration [mm/sec^2]</td>
</tr>
<tr>
<td><em>$121 = 750.000</em></td>
<td>Y-axis acceleration [mm/sec^2]</td>
</tr>
<tr>
<td><em>$122 = 500.000</em></td>
<td>Z-axis acceleration [mm/sec^2]</td>
</tr>
<tr>
<td><em>$130 = 812.000</em></td>
<td>X-axis maximum travel [millimeters]</td>
</tr>
<tr>
<td>$131 = 812.000</td>
<td>Y-axis maximum travel [millimeters]</td>
</tr>
<tr>
<td><em>$132 = 105.000</em></td>
<td>Z-axis maximum travel [millimeters]</td>
</tr>
</tbody>
</table>
<p><!-- /wp:table --><!-- /wp:paragraph -->

<!-- wp:paragraph --></p>
<p>To change a setting, simply send the command that corresponds to what setting you want to change. For example, if I want to set my maximum feed rate in the Z-axis to 1500mm/min, then I would send the command "$112=1500".</p>
<p>If you're using UGS, you can also directly import the LongMills firmware settings using this downloadable file: <a href="https://resources.sienci.com/wp-content/uploads/2021/05/LongMill_firmware.zip" target="_blank" rel="noopener noreferrer">LongMill UGS Firmware Config</a></p>
<p><!-- /wp:paragraph -->

<!-- wp:paragraph --></p>
<p>For advanced users, or users that want to add additional functionality such as with end stops and lasers, you may make changes to these settings.</p>
<p><!-- /wp:paragraph --></p>
