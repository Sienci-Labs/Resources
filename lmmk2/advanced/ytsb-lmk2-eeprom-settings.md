---
title: ytsb EEPROM Settings
menu_order: 4
post_status: draft
post_excerpt: How to modify EEPROM setting for the LongMill CNC. These settings control the speed and direction of movement, machine limits, and activation of limit switches.
post_date: 2022-03-18 00:11:00
taxonomy:
    knowledgebase_cat: lmk2-advanced
    knowledgebase_tag:
        - mk2
custom_fields:
    KBName: LongMill MK2 CNC
    basepress_post_icon: bp-caret-right
skip_file: yes
featured_image: 
---

<em>For in-depth documentation on all of the settings in grbl and what they mean, visit:</em> <a href="https://github.com/gnea/grbl/wiki/Grbl-v1.1-Configuration">https://github.com/gnea/grbl/wiki/Grbl-v1.1-Configuration</a>.

You can make changes to your machine's settings by changing the values in your EEPROM. These are settings that will persist even after you power off your machine and control things like the maximum speed, the acceleration, steps per mm, and more.

Start by sending the command "$$" to your machine. The console will give you a list of values.

## Default Settings

[su_table]
<table>
<tbody>
   <tr>
     <td></td>
     <td></td>
    <td colspan="4">Value (number)</td>
     <td></td>
   </tr>
   <tr>
     <td><b>Title</b></td>
     <td><b>$</b></td>
     <td><b>12x12</b></td>
     <td><b>12x30</b></td>
     <td><b>30x30</b></td>
     <td><b>48x30</b></td>
     <td><b>Units</b></td>
   </tr>
   <tr>
     <td>Step pulse time</td>
     <td>$0</td>
    <td colspan="4"><b>10</b></td>
     <td>microseconds</td>
   </tr>
   <tr>
     <td>Step idle delay</td>
     <td>$1</td>
    <td colspan="4"><b>100</b></td>
     <td>milliseconds</td>
   </tr>
   <tr>
     <td>Step pulse invert</td>
     <td>$2</td>
    <td colspan="4">X: <b>ON</b><br>Y: <b>OFF</b><br>Z: <b>OFF</b><br>(1)</td>
     <td></td>
   </tr>
   <tr>
     <td>Step direction invert</td>
     <td>$3</td>
    <td colspan="4">X: <b>ON</b><br>Y: <b>OFF</b><br>Z: <b>ON</b><br>(5)</td>
     <td></td>
   </tr>
   <tr>
     <td>Invert step enable pin</td>
     <td>$4</td>
    <td colspan="4"><b>Enabled</b> (1)</td>
     <td></td>
   </tr>
   <tr>
     <td>Invert limit pins</td>
     <td>$5</td>
    <td colspan="4"><b>Disabled</b> (0)</td>
     <td></td>
   </tr>
   <tr>
     <td>Invert probe pin</td>
     <td>$6</td>
    <td colspan="4"><b>Disabled</b> (0)</td>
     <td></td>
   </tr>
   <tr>
     <td>Status report options</td>
     <td>$10</td>
    <td colspan="4"><b>MPos</b><br>Buffer: <b>OFF</b><br>(1)</td>
     <td></td>
   </tr>
   <tr>
     <td>Junction deviation</td>
     <td>$11</td>
    <td colspan="4"><b>0.010</b></td>
     <td>mm</td>
   </tr>
   <tr>
     <td>Arc tolerance</td>
     <td>$12</td>
    <td colspan="4"><b>0.002</b></td>
     <td>mm</td>
   </tr>
   <tr>
     <td>Report in inches</td>
     <td>$13</td>
    <td colspan="4"><b>Disabled</b> (0)</td>
     <td></td>
   </tr>
   <tr>
     <td>Soft limits enable</td>
     <td>$20</td>
    <td colspan="4"><b>Disabled</b> (0)</td>
     <td></td>
   </tr>
   <tr>
     <td>Hard limits enable</td>
     <td>$21</td>
    <td colspan="4"><b>Disabled</b> (0)</td>
     <td></td>
   </tr>
   <tr>
     <td>Homing cycle enable</td>
     <td>$22</td>
    <td colspan="4"><b>Disabled</b> (0)</td>
     <td></td>
   </tr>
   <tr>
     <td>Homing direction invert</td>
     <td>$23</td>
    <td colspan="4">X: <b>ON</b><br>Y: <b>ON</b><br>Z: <b>OFF</b><br>(3)</td>
     <td></td>
   </tr>
   <tr>
     <td>Homing locate feed rate</td>
     <td>$24</td>
    <td colspan="4"><b>25</b></td>
     <td>mm/min</td>
   </tr>
   <tr>
     <td>Homing search seek rate</td>
     <td>$25</td>
    <td colspan="4"><b>1500</b></td>
     <td>mm/min</td>
   </tr>
   <tr>
     <td>Homing switch debounce delay</td>
     <td>$26</td>
    <td colspan="4"><b>250</b></td>
     <td>milliseconds</td>
   </tr>
   <tr>
     <td>Homing switch pull-off distance</td>
     <td>$27</td>
    <td colspan="4"><b>1</b></td>
     <td>mm</td>
   </tr>
   <tr>
     <td>Maximum spindle speed</td>
     <td>$30</td>
    <td colspan="4"><b>30000</b></td>
     <td>RPM</td>
   </tr>
   <tr>
     <td>Minimum spindle speed</td>
     <td>$31</td>
    <td colspan="4"><b>0</b></td>
     <td>RPM</td>
   </tr>
   <tr>
     <td>Laser-mode enable</td>
     <td>$32</td>
    <td colspan="4"><b>Disabled</b> (0)</td>
     <td></td>
   </tr>
   <tr>
     <td>X-axis travel resolution</td>
     <td>$100</td>
    <td colspan="4"><b>200</b></td>
     <td>step/mm</td>
   </tr>
   <tr>
     <td>Y-axis travel resolution</td>
     <td>$101</td>
    <td colspan="4"><b>200</b></td>
     <td>step/mm</td>
   </tr>
   <tr>
     <td>Z-axis travel resolution</td>
     <td>$102</td>
    <td colspan="4"><b>200</b></td>
     <td>step/mm</td>
   </tr>
   <tr>
     <td>X-axis maximum rate</td>
     <td>$110</td>
    <td colspan="4"><b>4000</b></td>
     <td>mm/min</td>
   </tr>
   <tr>
     <td>Y-axis maximum rate</td>
     <td>$111</td>
    <td colspan="4"><b>4000</b></td>
     <td>mm/min</td>
   </tr>
   <tr>
     <td>Z-axis maximum rate</td>
     <td>$112</td>
    <td colspan="4"><b>3000</b></td>
     <td>mm/min</td>
   </tr>
   <tr>
     <td>X-axis acceleration</td>
     <td>$120</td>
    <td colspan="4"><b>750</b></td>
     <td>mm/sec^2</td>
   </tr>
   <tr>
     <td>Y-axis acceleration</td>
     <td>$121</td>
    <td colspan="4"><b>750</b></td>
     <td>mm/sec^2</td>
   </tr>
   <tr>
     <td>Z-axis acceleration</td>
     <td>$122</td>
    <td colspan="4"><b>500</b></td>
     <td>mm/sec^2</td>
   </tr>
   <tr>
     <td>X-axis maximum travel</td>
     <td>$130</td>
     <td><b>285</b></td>
     <td><b>770</b></td>
     <td><b>770</b></td>
     <td><b>1230</b></td>
     <td>mm</td>
   </tr>
   <tr>
     <td>Y-axis maximum travel</td>
     <td>$131</td>
     <td><b>320</b></td>
     <td><b>320</b></td>
     <td><b>820</b></td>
     <td><b>820</b></td>
     <td>mm</td>
   </tr>
   <tr>
     <td>Z-axis maximum travel</td>
     <td>$132</td>
    <td colspan="4"><b>110</b></td>
     <td>mm</td>
   </tr>
</tbody>
</table>
[/su_table]

To change a setting, simply send the command that corresponds to what setting you want to change. For example, if I want to set my maximum feed rate in the Z-axis to 1500mm/min, then I would send the command "$112=1500".

If you're using UGS, you can also directly import the LongMills firmware settings using this downloadable file: <a href="https://resources.sienci.com/wp-content/uploads/2021/05/LongMill_firmware.zip" target="_blank" rel="noopener noreferrer">LongMill UGS Firmware Config</a>

For advanced users, or users that want to add additional functionality such as with end stops and lasers, you may make changes to these settings.
