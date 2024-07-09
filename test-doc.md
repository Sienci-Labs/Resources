---
title: Test Post
post_excerpt: See more on SLB settings and troubleshooting, especially useful on DIY CNC setups to better understand how to configure your SLB for your machine.
featured_image: _images/post-image.jpg
post_date: 2024-04-03 18:14:53
post_status: draft
menu_order: 4
taxonomy:
    knowledge base: SuperLongBoard
    Knowledge base: SuperLongBoard
    Knowledge Base: SuperLongBoard
    category: Handbook
custom_fields:
    KBName: SuperLongBoard
    knowledgebase: SuperLongBoard
    product: SuperLongBoard
    Section: Handbook
skip_file: no
---

## My post content

Wooooooooooooot Donec a lacinia orci.
Nunc sodales massa enim, nec consectetur orci tempus ac.

### Section with image

![alt text for the image](/_images/pic4.jpg "Caption for the image")

Nam rutrum ultricies sapien id rhoncus. In pellentesque efficitur suscipit.
Aliquam vel est consectetur lectus malesuada mollis sit amet non neque. 

### Section with link

This is a [relative link](../sub-dir1/post3.md) which links to another markdown post w.r.t the current file.
This is an [absolute link](/folder1/sub-dir1/post3.md) which links to another post w.r.t the root directory.

### Section with HTML

<section id="home">
    <h2>Welcome to Our Website!</h2>
    <p>This is a sample HTML page with JavaScript and CSS styling.</p>
    <button type="button" onclick="showMessage()">Show message</button>
</section>

<script>
    function showMessage() {
        alert('Thank you for contacting us!');
    }
</script>

<!-- Sample CSS Style -->
<style>
    h1 {
        color: red;
    }
</style>

### Section with Shortcodes

[g2w_edit_link]

If you'd like to know all the ins and outs of the SLB's firmware, and broader settings of grblHAL as a whole, you'll find it all in the tables below.
<h2>Settings Descriptions</h2>
For added clarity, settings that are currently unused on the SLB have been highlighted in <span style="color: var(--sl-orange);">orange</span>. Also, the ones highlighted in <span style="color: var(--sl-blue-d);">blue</span> though they are supported we don't advise changing or are still building up documentation on.

[su_table responsive="yes"]
<table>
<thead>
<tr>
<th>$</th>
<th>Name</th>
<th>Description</th>
<th>Unit (example)</th>
<th>How to Use</th>
</tr>
</thead>
<tbody>
<tr>
<td><strong>$0</strong></td>
<td>Step pulse time</td>
<td>
<p style="text-align: left;">Sets time length per step. Minimum 2 microseconds.</p>
<p style="text-align: left;">This needs to be reduced from the default value of 10 when max. step rates exceed approximately 80 kHz.</p>
</td>
<td>microseconds (5)</td>
<td></td>
</tr>
<tr>
<td><strong>$1</strong></td>
<td>Step idle delay</td>
<td style="text-align: left;">Sets a short hold delay when stopping to let dynamics settle before disabling steppers. Value 255 keeps motors enabled.</td>
<td>milliseconds (254)</td>
<td></td>
</tr>
<tr>
<td><strong>$2</strong></td>
<td>Step pulse invert</td>
<td style="text-align: left;">Inverts the step signals (active low).</td>
<td>mask (0)</td>
<td></td>
</tr>
<tr>
<td><strong>$3</strong></td>
<td>Step direction invert</td>
<td style="text-align: left;">Inverts the direction signals (active low).</td>
<td>mask (6)</td>
<td></td>
</tr>
<tr>
<td><strong>$4</strong></td>
<td>Invert stepper enable pin(s)</td>
<td>
<p style="text-align: left;">Inverts the stepper driver enable signals. Most drivers uses active low enable requiring inversion.</p>
<p style="text-align: left;">NOTE: If the stepper drivers shares the same enable signal only X is used.</p>
</td>
<td>mask (15)</td>
<td></td>
</tr>
<tr>
<td><strong>$5</strong></td>
<td>Invert limit pins</td>
<td style="text-align: left;">Inverts the axis limit input signals.</td>
<td>mask (15)</td>
<td></td>
</tr>
<tr>
<td><strong>$6</strong></td>
<td>Invert probe pin</td>
<td style="text-align: left;">Inverts the probe input pin signal.</td>
<td>boolean (1)</td>
<td></td>
</tr>
<tr>
<td><strong>$8</strong></td>
<td>Ganged axes direction invert</td>
<td>
<p style="text-align: left;">Inverts the direction signals for the second motor used for ganged axes.</p>
<p style="text-align: left;">NOTE: This inversion will be applied in addition to the inversion from setting $3.</p>
</td>
<td>boolean (0)</td>
<td></td>
</tr>
<tr>
<td><strong>$9</strong></td>
<td>Spindle PWM</td>
<td style="text-align: left;">Enable: Controls PWM output availability.
RPM controls spindle enable signal: When M3 or M4 is active,  S &gt; 0 turns on spindle enable and S0 turns it off.</td>
<td>mask (1)</td>
<td></td>
</tr>
<tr>
<td><strong>$10</strong></td>
<td>Status report options</td>
<td style="text-align: left;">Specifies optional data included in status reports.
If Run substatus is enabled it may be used for simple probe protection.NOTE: Parser state will be sent separately after the status report and only on changes.</td>
<td>mask (511)</td>
<td></td>
</tr>
<tr>
<td><strong>$11</strong></td>
<td>Junction deviation</td>
<td style="text-align: left;">Sets how fast Grbl travels through consecutive motions. Lower value slows it down.</td>
<td>mm (0.01)</td>
<td></td>
</tr>
<tr>
<td><strong>$12</strong></td>
<td>Arc tolerance</td>
<td style="text-align: left;">Sets the G2 and G3 arc tracing accuracy based on radial error. Beware: A very small value may effect performance.</td>
<td>mm (0.002)</td>
<td></td>
</tr>
<tr>
<td><strong>$13</strong></td>
<td>Report in inches</td>
<td style="text-align: left;">Enables inch units when returning any position and rate value that is not a settings value.</td>
<td>boolean (0)</td>
<td></td>
</tr>
<tr>
<td><strong>$14</strong></td>
<td>Invert control pins</td>
<td style="text-align: left;">Inverts the control signals (active low).
NOTE: Block delete, Optional stop, EStop and Probe connected are optional signals, availability is driver dependent.</td>
<td>mask (14)</td>
<td></td>
</tr>
<tr>
<td><strong>$15</strong></td>
<td>Invert coolant pins</td>
<td style="text-align: left;">Inverts the coolant and mist signals (active low).</td>
<td>mask (0)</td>
<td></td>
</tr>
<tr>
<td><strong>$16</strong></td>
<td>Invert spindle signals</td>
<td>
<p style="text-align: left;">Inverts the spindle on, counterclockwise and PWM signals (active low).</p>
<p style="text-align: left;">NOTE: A hard reset of the controller is required after changing this setting.</p>
</td>
<td>mask (0)</td>
<td></td>
</tr>
<tr>
<td><strong>$17</strong></td>
<td>Pullup disable control pins</td>
<td style="text-align: left;">Disable the control signals pullup resistors. Potentially enables pulldown resistor if available.
NOTE: Block delete, Optional stop and EStop are optional signals, availability is driver dependent.</td>
<td>mask (0)</td>
<td></td>
</tr>
<tr>
<td><strong>$18</strong></td>
<td>Pullup disable limit pins</td>
<td style="text-align: left;">Disable the limit signals pullup resistors. Potentially enables pulldown resistor if available.</td>
<td>mask (0)</td>
<td></td>
</tr>
<tr>
<td><strong>$19</strong></td>
<td>Pullup disable probe pin</td>
<td style="text-align: left;">Disable the probe signal pullup resistor. Potentially enables pulldown resistor if available.</td>
<td>boolean (0)</td>
<td></td>
</tr>
<tr>
<td><strong>$20</strong></td>
<td>Soft limits enable</td>
<td style="text-align: left;">Enables soft limits checks within machine travel and sets alarm when exceeded. Requires homing.</td>
<td>boolean (0)</td>
<td rowspan="8"><a href="https://resources.sienci.com/view/slb-manual/#homing-amp-limit-switches">Docs</a></td>
</tr>
<tr>
<td><strong>$21</strong></td>
<td>Hard limits enable</td>
<td style="text-align: left;">When enabled immediately halts motion and throws an alarm when a limit switch is triggered. In strict mode only homing is possible when a switch is engaged.</td>
<td>mask (0)</td>
</tr>
<tr>
<td><strong>$22</strong></td>
<td>Homing cycle</td>
<td>
<p style="text-align: left;">Enables homing cycle. Requires limit switches on axes to be automatically homed.</p>
<p style="text-align: left;">When `Enable single axis commands` is checked, single axis homing can be performed by $H&lt;axis letter&gt; commands.</p>
<p style="text-align: left;">When `Allow manual` is checked, axes not homed automatically may be homed manually by $H or $H&lt;axis letter&gt; commands.</p>
<p style="text-align: left;">`Override locks` is for allowing a soft reset to disable `Homing on startup required`.</p>
</td>
<td>mask (205)</td>
</tr>
<tr>
<td><strong>$23</strong></td>
<td>Homing direction invert</td>
<td style="text-align: left;">Homing searches for a switch in the positive direction. Set axis bit to search in negative direction.</td>
<td>mask (11)</td>
</tr>
<tr>
<td><strong>$24</strong></td>
<td>Homing locate feed rate</td>
<td style="text-align: left;">Feed rate to slowly engage limit switch to determine its location accurately.</td>
<td>mm/min (150)</td>
</tr>
<tr>
<td><strong>$25</strong></td>
<td>Homing search seek rate</td>
<td style="text-align: left;">Seek rate to quickly find the limit switch before the slower locating phase.</td>
<td>mm/min (4300)</td>
</tr>
<tr>
<td><strong>$26</strong></td>
<td>Homing switch debounce delay</td>
<td style="text-align: left;">Sets a short delay between phases of homing cycle to let a switch debounce.</td>
<td>milliseconds (25)</td>
</tr>
<tr>
<td><strong>$27</strong></td>
<td>Homing switch pull-off distance</td>
<td style="text-align: left;">Retract distance after triggering switch to disengage it. Homing will fail if switch isn't cleared.</td>
<td>mm (1.5)</td>
</tr>
<tr>
<td><strong>$28</strong></td>
<td>G73 retract distance</td>
<td style="text-align: left;">G73 retract distance (for chip breaking drilling).</td>
<td>mm (0.1)</td>
<td></td>
</tr>
<tr>
<td><strong>$29</strong></td>
<td>Pulse delay</td>
<td>
<p style="text-align: left;">Step pulse delay.</p>
<p style="text-align: left;">Normally leave this at 0 as there is an implicit delay on direction changes when AMASS is active.</p>
</td>
<td>microseconds (0)</td>
<td></td>
</tr>
<tr>
<td><strong>$30</strong></td>
<td>Maximum spindle speed</td>
<td style="text-align: left;">Maximum spindle speed, can be overridden by spindle plugins.</td>
<td>RPM (24000)</td>
<td rowspan="7"><a href="https://resources.sienci.com/view/slb-manual/#spindlers485">Docs</a></td>
</tr>
<tr>
<td><strong>$31</strong></td>
<td>Minimum spindle speed</td>
<td style="text-align: left;">Minimum spindle speed, can be overridden by spindle plugins.</td>
<td>RPM (7200)</td>
</tr>
<tr>
<td><strong>$32</strong></td>
<td>Mode of operation</td>
<td style="text-align: left;">Laser mode: consecutive G1/2/3 commands will not halt when spindle speed is changed.
Lathe mode: allows use of G7, G8, G96 and G97.</td>
<td>integer (0)</td>
</tr>
<tr>
<td><strong>$33</strong></td>
<td>Spindle PWM frequency</td>
<td style="text-align: left;">Spindle PWM frequency.</td>
<td>Hz (1000)</td>
</tr>
<tr>
<td><strong>$34</strong></td>
<td>Spindle PWM off value</td>
<td style="text-align: left;">Spindle PWM off value in percent (duty cycle).</td>
<td>percent (0)</td>
</tr>
<tr>
<td><strong>$35</strong></td>
<td>Spindle PWM min value</td>
<td style="text-align: left;">Spindle PWM min value in percent (duty cycle).</td>
<td>percent (0)</td>
</tr>
<tr>
<td><strong>$36</strong></td>
<td>Spindle PWM max value</td>
<td style="text-align: left;">Spindle PWM max value in percent (duty cycle).</td>
<td>percent (100)</td>
</tr>
<tr>
<td><strong>$37</strong></td>
<td>Steppers de-energize</td>
<td style="text-align: left;">Specifies which steppers not to disable when stopped.</td>
<td>mask (0)</td>
<td><a href="https://resources.sienci.com/view/slb-manual/#independent-motor-holding">Docs</a></td>
</tr>
<tr>
<td><strong>$39</strong></td>
<td>Enable legacy RT commands</td>
<td style="text-align: left;">Enables "normal" processing of ?, ! and ~ characters when part of $-setting or comment. If disabled then they are added to the input string instead.</td>
<td>boolean (1)</td>
<td></td>
</tr>
<tr>
<td><strong>$40</strong></td>
<td>Limit jog commands</td>
<td style="text-align: left;">Limit jog commands to machine limits for homed axes.</td>
<td>boolean (1)</td>
<td><a href="https://resources.sienci.com/view/slb-manual/#homing-amp-limit-switches">Docs</a></td>
</tr>
<tr style="color: var(--sl-orange);">
<td><strong>$41</strong></td>
<td>Parking cycle</td>
<td style="text-align: left;">Enables parking cycle, requires parking axis homed.</td>
<td>mask (1)</td>
<td></td>
</tr>
<tr style="color: var(--sl-orange);">
<td><strong>$42</strong></td>
<td>Parking axis</td>
<td style="text-align: left;">Define which axis that performs the parking motion.</td>
<td>integer (2)</td>
<td></td>
</tr>
<tr>
<td><strong>$43</strong></td>
<td>Homing passes</td>
<td style="text-align: left;">Number of homing passes. Minimum 1, maximum 128.</td>
<td>(1)</td>
<td></td>
</tr>
<tr>
<td><strong>$44</strong></td>
<td>Axes homing, first pass</td>
<td style="text-align: left;">Axes to home in first pass.</td>
<td>mask (4)</td>
<td></td>
</tr>
<tr>
<td><strong>$45</strong></td>
<td>Axes homing, second pass</td>
<td style="text-align: left;">Axes to home in second pass.</td>
<td>mask (3)</td>
<td></td>
</tr>
<tr>
<td><strong>$46</strong></td>
<td>Axes homing, third pass</td>
<td style="text-align: left;">Axes to home in third pass.</td>
<td>mask (0)</td>
<td></td>
</tr>
<tr>
<td><strong>$47</strong></td>
<td>Axes homing, fourth pass</td>
<td style="text-align: left;">Axes to home in fourth pass.</td>
<td>mask (0)</td>
<td></td>
</tr>
<tr style="color: var(--sl-orange);">
<td><strong>$56</strong></td>
<td>Parking pull-out distance</td>
<td style="text-align: left;">Spindle pull-out and plunge distance in mm.Incremental distance.</td>
<td>mm (5)</td>
<td></td>
</tr>
<tr style="color: var(--sl-orange);">
<td><strong>$57</strong></td>
<td>Parking pull-out rate</td>
<td style="text-align: left;">Spindle pull-out/plunge slow feed rate in mm/min.</td>
<td>mm/min (100)</td>
<td></td>
</tr>
<tr style="color: var(--sl-orange);">
<td><strong>$58</strong></td>
<td>Parking target</td>
<td style="text-align: left;">Parking axis target. In mm, as machine coordinate [-max_travel, 0].</td>
<td>mm (-5)</td>
<td></td>
</tr>
<tr style="color: var(--sl-orange);">
<td><strong>$59</strong></td>
<td>Parking fast rate</td>
<td style="text-align: left;">Parking fast rate to target after pull-out in mm/min.</td>
<td>mm/min (500)</td>
<td></td>
</tr>
<tr>
<td><strong>$60</strong></td>
<td>Restore overrides</td>
<td style="text-align: left;">Restore overrides to default values at program end.</td>
<td>boolean (1)</td>
<td></td>
</tr>
<tr style="color: var(--sl-orange);">
<td><strong>$61</strong></td>
<td>Safety door options</td>
<td style="text-align: left;">Enable this if it is desirable to open the safety door when in IDLE mode (eg. for jogging).</td>
<td>mask (3)</td>
<td></td>
</tr>
<tr>
<td><strong>$62</strong></td>
<td>Sleep enable</td>
<td style="text-align: left;">Enable sleep mode.</td>
<td>boolean (0)</td>
<td></td>
</tr>
<tr>
<td><strong>$63</strong></td>
<td>Feed hold actions</td>
<td style="text-align: left;">Actions taken during feed hold and on resume from feed hold.</td>
<td>mask (3)</td>
<td></td>
</tr>
<tr>
<td><strong>$64</strong></td>
<td>Force init alarm</td>
<td style="text-align: left;">Starts Grbl in alarm mode after a cold reset.</td>
<td>boolean (0)</td>
<td></td>
</tr>
<tr>
<td><strong>$65</strong></td>
<td>Probing feed override</td>
<td style="text-align: left;">Allow feed override during probing.</td>
<td>boolean (0)</td>
<td></td>
</tr>
<tr>
<td><strong>$70</strong></td>
<td>Network services</td>
<td>
<p style="text-align: left;">Network services/protocols to enable.</p>
<p style="text-align: left;">NOTE: A hard reset of the controller is required after changing this setting.</p>
</td>
<td>mask (11)</td>
<td><a href="https://resources.sienci.com/view/slb-manual/#ethernet-on-windows">Docs</a></td>
</tr>
<tr>
<td><strong>$100</strong></td>
<td>X-axis travel resolution</td>
<td style="text-align: left;">Travel resolution in steps per millimeter.</td>
<td>step/min (800)</td>
<td></td>
</tr>
<tr>
<td><strong>$101</strong></td>
<td>Y-axis travel resolution</td>
<td style="text-align: left;">Travel resolution in steps per millimeter.</td>
<td>step/min (800)</td>
<td></td>
</tr>
<tr>
<td><strong>$102</strong></td>
<td>Z-axis travel resolution</td>
<td style="text-align: left;">Travel resolution in steps per millimeter.</td>
<td>step/min (800)</td>
<td></td>
</tr>
<tr>
<td><strong>$103</strong></td>
<td>A-axis travel resolution</td>
<td style="text-align: left;">Travel resolution in steps per millimeter.</td>
<td>step/deg (19)</td>
<td></td>
</tr>
<tr>
<td><strong>$110</strong></td>
<td>X-axis maximum rate</td>
<td style="text-align: left;">Maximum rate. Used as G0 rapid rate.</td>
<td>mm/min (5500)</td>
<td rowspan="8"><a href="https://resources.sienci.com/view/slb-manual/#movement-amp-cutting-speeds">Docs</a></td>
</tr>
<tr>
<td><strong>$111</strong></td>
<td>Y-axis maximum rate</td>
<td style="text-align: left;">Maximum rate. Used as G0 rapid rate.</td>
<td>mm/min (5500)</td>
</tr>
<tr>
<td><strong>$112</strong></td>
<td>Z-axis maximum rate</td>
<td style="text-align: left;">Maximum rate. Used as G0 rapid rate.</td>
<td>mm/min (4500)</td>
</tr>
<tr>
<td><strong>$113</strong></td>
<td>A-axis maximum rate</td>
<td style="text-align: left;">Maximum rate. Used as G0 rapid rate.</td>
<td>deg/min (8000)</td>
</tr>
<tr>
<td><strong>$120</strong></td>
<td>X-axis acceleration</td>
<td style="text-align: left;">Acceleration. Used for motion planning to not exceed motor torque and lose steps.</td>
<td>mm/sec^2 (1000)</td>
</tr>
<tr>
<td><strong>$121</strong></td>
<td>Y-axis acceleration</td>
<td style="text-align: left;">Acceleration. Used for motion planning to not exceed motor torque and lose steps.</td>
<td>mm/sec^2 (1000)</td>
</tr>
<tr>
<td><strong>$122</strong></td>
<td>Z-axis acceleration</td>
<td style="text-align: left;">Acceleration. Used for motion planning to not exceed motor torque and lose steps.</td>
<td>mm/sec^2 (750)</td>
</tr>
<tr>
<td><strong>$123</strong></td>
<td>A-axis acceleration</td>
<td style="text-align: left;">Acceleration. Used for motion planning to not exceed motor torque and lose steps.</td>
<td>deg/sec^2 (1000)</td>
</tr>
<tr>
<td><strong>$130</strong></td>
<td>X-axis maximum travel</td>
<td style="text-align: left;">Maximum axis travel distance from homing switch. Determines valid machine space for soft-limits and homing search distances.</td>
<td>mm (810)</td>
<td></td>
</tr>
<tr>
<td><strong>$131</strong></td>
<td>Y-axis maximum travel</td>
<td style="text-align: left;">Maximum axis travel distance from homing switch. Determines valid machine space for soft-limits and homing search distances.</td>
<td>mm (855)</td>
<td></td>
</tr>
<tr>
<td><strong>$132</strong></td>
<td>Z-axis maximum travel</td>
<td style="text-align: left;">Maximum axis travel distance from homing switch. Determines valid machine space for soft-limits and homing search distances.</td>
<td>mm (120)</td>
<td></td>
</tr>
<tr>
<td><strong>$133</strong></td>
<td>A-axis maximum travel</td>
<td style="text-align: left;">Maximum axis travel distance from homing switch. Determines valid machine space for soft-limits and homing search distances.</td>
<td>mm (0)</td>
<td></td>
</tr>
<tr>
<td><strong>$140</strong></td>
<td>X-axis motor current</td>
<td style="text-align: left;" rowspan="4">Motor current in mA (RMS).
NOTE: Only used for axes controlled by a Trinamic driver.</td>
<td rowspan="4">mA (2800)</td>
<td rowspan="4"></td>
</tr>
<tr>
<td><strong>$141</strong></td>
<td>Y-axis motor current</td>
</tr>
<tr>
<td><strong>$142</strong></td>
<td>Z-axis motor current</td>
</tr>
<tr style="color: var(--sl-orange);">
<td><strong>$143</strong></td>
<td>A-axis motor current</td>
</tr>
<tr>
<td><strong>$150</strong></td>
<td>X-axis microsteps</td>
<td style="text-align: left;" rowspan="4">Microsteps per fullstep.
NOTE: Only used for axes controlled by a Trinamic driver.</td>
<td rowspan="4">steps (32)</td>
<td rowspan="4"></td>
</tr>
<tr>
<td><strong>$151</strong></td>
<td>Y-axis microsteps</td>
</tr>
<tr>
<td><strong>$152</strong></td>
<td>Z-axis microsteps</td>
</tr>
<tr style="color: var(--sl-orange);">
<td><strong>$153</strong></td>
<td>A-axis microsteps</td>
</tr>
<tr>
<td><strong>$180</strong></td>
<td>X-axis homing locate feed rate</td>
<td style="text-align: left;" rowspan="4">Feed rate to slowly engage limit switch to determine its location accurately.
NOTE: Defaults to $24 setting if axis isn't controlled by a Trinamic driver.</td>
<td rowspan="4">mm/min (150)</td>
<td rowspan="4"><a href="https://resources.sienci.com/view/slb-manual/#homing-amp-limit-switches">Docs</a></td>
</tr>
<tr>
<td><strong>$181</strong></td>
<td>Y-axis homing locate feed rate</td>
</tr>
<tr>
<td><strong>$182</strong></td>
<td>Z-axis homing locate feed rate</td>
</tr>
<tr style="color: var(--sl-orange);">
<td><strong>$183</strong></td>
<td>A-axis homing locate feed rate</td>
</tr>
<tr>
<td><strong>$190</strong></td>
<td>X-axis homing search seek rate</td>
<td style="text-align: left;" rowspan="4">Seek rate to quickly find the limit switch before the slower locating phase.
NOTE: Defaults to $25 setting if axis isn't controlled by a Trinamic driver.</td>
<td rowspan="4">mm/min (4300)</td>
<td rowspan="4"><a href="https://resources.sienci.com/view/slb-manual/#homing-amp-limit-switches">Docs</a></td>
</tr>
<tr>
<td><strong>$191</strong></td>
<td>Y-axis homing search seek rate</td>
</tr>
<tr>
<td><strong>$192</strong></td>
<td>Z-axis homing search seek rate</td>
</tr>
<tr style="color: var(--sl-orange);">
<td><strong>$193</strong></td>
<td>A-axis homing search seek rate</td>
</tr>
<tr style="color: var(--sl-blue-d);">
<td><strong>$200</strong></td>
<td>X-axis StallGuard2 fast threshold</td>
<td style="text-align: left;" rowspan="4">StallGuard threshold for fast (seek) homing phase.
NOTE: Only used for axes controlled by a Trinamic driver.</td>
<td rowspan="4">(22)</td>
<td rowspan="4"></td>
</tr>
<tr style="color: var(--sl-blue-d);">
<td><strong>$201</strong></td>
<td>Y-axis StallGuard2 fast threshold</td>
</tr>
<tr style="color: var(--sl-blue-d);">
<td><strong>$202</strong></td>
<td>Z-axis StallGuard2 fast threshold</td>
</tr>
<tr style="color: var(--sl-orange);">
<td><strong>$203</strong></td>
<td>A-axis StallGuard2 fast threshold</td>
</tr>
<tr>
<td><strong>$210</strong></td>
<td>X-axis hold current</td>
<td style="text-align: left;" rowspan="4">Motor current at standstill as a percentage of full current.
NOTE: If grblHAL is configured to disable motors on standstill this setting has no use. Only used for axes controlled by a Trinamic driver.</td>
<td rowspan="4">% (35)</td>
<td rowspan="4"><a href="https://resources.sienci.com/view/slb-manual/#independent-motor-holding">Docs</a></td>
</tr>
<tr>
<td><strong>$211</strong></td>
<td>Y-axis hold current</td>
</tr>
<tr>
<td><strong>$212</strong></td>
<td>Z-axis hold current</td>
</tr>
<tr style="color: var(--sl-orange);">
<td><strong>$213</strong></td>
<td>A-axis hold current</td>
</tr>
<tr style="color: var(--sl-blue-d);">
<td><strong>$220</strong></td>
<td>X-axis stallGuard2 slow threshold</td>
<td style="text-align: left;" rowspan="4">StallGuard threshold for slow (feed) homing phase.
NOTE: Only used for axes controlled by a Trinamic driver.</td>
<td rowspan="4">(22)</td>
<td rowspan="4"></td>
</tr>
<tr style="color: var(--sl-blue-d);">
<td><strong>$221</strong></td>
<td>Y-axis stallGuard2 slow threshold</td>
</tr>
<tr style="color: var(--sl-blue-d);">
<td><strong>$222</strong></td>
<td>Z-axis stallGuard2 slow threshold</td>
</tr>
<tr style="color: var(--sl-orange);">
<td><strong>$223</strong></td>
<td>A-axis stallGuard2 slow threshold</td>
</tr>
<tr>
<td><strong>$300</strong></td>
<td>Hostname</td>
<td style="text-align: left;">Network hostname.
~Controller reset required for setting change to take effect~</td>
<td>(grblHAL)</td>
<td rowspan="8"><a href="https://resources.sienci.com/view/slb-manual/#ethernet-on-windows">Docs</a></td>
</tr>
<tr>
<td><strong>$301</strong></td>
<td>IP mode</td>
<td style="text-align: left;">IP mode.
~Controller reset required for setting change to take effect~</td>
<td>integer (0)</td>
</tr>
<tr>
<td><strong>$302</strong></td>
<td>IP address</td>
<td style="text-align: left;">Static IP address.
~Controller reset required for setting change to take effect~</td>
<td>(192.168.5.1)</td>
</tr>
<tr>
<td><strong>$303</strong></td>
<td>Gateway</td>
<td style="text-align: left;">Static gateway address.
~Controller reset required for setting change to take effect~</td>
<td>(192.168.5.1)</td>
</tr>
<tr>
<td><strong>$304</strong></td>
<td>Netmask</td>
<td style="text-align: left;">Static netmask.
~Controller reset required for setting change to take effect~</td>
<td>(255.255.255.0)</td>
</tr>
<tr>
<td><strong>$305</strong></td>
<td>Telnet port</td>
<td style="text-align: left;">(Raw) Telnet port number listening for incoming connections.
~Controller reset required for setting change to take effect~</td>
<td>(23)</td>
</tr>
<tr>
<td><strong>$307</strong></td>
<td>Websocket port</td>
<td style="text-align: left;">Websocket port number listening for incoming connections.
NOTE: WebUI requires this to be HTTP port number + 1.
~Controller reset required for setting change to take effect~</td>
<td>(80)</td>
</tr>
<tr>
<td><strong>$308</strong></td>
<td>FTP port</td>
<td style="text-align: left;">FTP port number listening for incoming connections.
~Controller reset required for setting change to take effect~</td>
<td>(21)</td>
</tr>
<tr style="color: var(--sl-blue-d);">
<td><strong>$338</strong></td>
<td>Trinamic driver</td>
<td style="text-align: left;">Enable SPI or UART controlled Trinamic drivers for axes.</td>
<td>mask (7)</td>
<td></td>
</tr>
<tr style="color: var(--sl-blue-d);">
<td><strong>$339</strong></td>
<td>Sensorless homing</td>
<td style="text-align: left;">Enable sensorless homing for axes. Requires SPI or UART controlled Trinamic drivers.</td>
<td>mask (0)</td>
<td></td>
</tr>
<tr>
<td><strong>$340</strong></td>
<td>Spindle at speed tolerance</td>
<td style="text-align: left;">Spindle at speed tolerance as percentage deviation from programmed speed, set to 0 to disable.
If not within tolerance when checked after spindle on delay ($392) alarm 14 is raised.</td>
<td>percent (0)</td>
<td></td>
</tr>
<tr style="color: var(--sl-blue-d);">
<td><strong>$341</strong></td>
<td>Tool change mode</td>
<td>
<p style="text-align: left;">Normal: allows jogging for manual touch off. Set new position manually.</p>
<p style="text-align: left;">Manual touch off: retracts tool axis to home position for tool change, use jogging or $TPW for touch off.</p>
<p style="text-align: left;">Manual touch off @ G59.3: retracts tool axis to home position then to G59.3 position for tool change, use jogging or $TPW for touch off.</p>
<p style="text-align: left;">Automatic touch off @ G59.3: retracts tool axis to home position for tool change, then to G59.3 position for automatic touch off.</p>
<p style="text-align: left;">All modes except "Normal" and "Ignore M6" returns the tool (controlled point) to original position after touch off.</p>
</td>
<td>integer (0)</td>
<td></td>
</tr>
<tr style="color: var(--sl-blue-d);">
<td><strong>$342</strong></td>
<td>Tool change probing distance</td>
<td style="text-align: left;">Maximum probing distance for automatic or $TPW touch off.</td>
<td>mm (30)</td>
<td></td>
</tr>
<tr style="color: var(--sl-blue-d);">
<td><strong>$343</strong></td>
<td>Tool change locate feed rate</td>
<td style="text-align: left;">Feed rate to slowly engage tool change sensor to determine the tool offset accurately.</td>
<td>mm/min (25)</td>
<td></td>
</tr>
<tr style="color: var(--sl-blue-d);">
<td><strong>$344</strong></td>
<td>Tool change search seek rate</td>
<td style="text-align: left;">Seek rate to quickly find the tool change sensor before the slower locating phase.</td>
<td>mm/min (200)</td>
<td></td>
</tr>
<tr style="color: var(--sl-blue-d);">
<td><strong>$345</strong></td>
<td>Tool change probe pull-off rate</td>
<td style="text-align: left;">Pull-off rate for the retract move before the slower locating phase.</td>
<td>mm/min (200)</td>
<td></td>
</tr>
<tr style="color: var(--sl-blue-d);">
<td><strong>$346</strong></td>
<td>Restore position after M6</td>
<td style="text-align: left;">When set the spindle is moved so that the controlled point (tool tip) is the same as before the M6 command, if not the spindle is only moved to the Z home position.</td>
<td>boolean (1)</td>
<td></td>
</tr>
<tr>
<td><strong>$370</strong></td>
<td>Invert I/O Port inputs</td>
<td style="text-align: left;">Invert IOPort inputs.</td>
<td>mask (0)</td>
<td></td>
</tr>
<tr>
<td><strong>$372</strong></td>
<td>Invert I/O Port outputs</td>
<td style="text-align: left;">Invert IOPort output.</td>
<td>mask (0)</td>
<td></td>
</tr>
<tr>
<td><strong>$374</strong></td>
<td>Modbus baud rate</td>
<td style="text-align: left;"></td>
<td>integer (3)</td>
<td></td>
</tr>
<tr>
<td><strong>$375</strong></td>
<td>Modbus RX timeout</td>
<td style="text-align: left;"></td>
<td>milliseconds (50)</td>
<td></td>
</tr>
<tr>
<td><strong>$376</strong></td>
<td>Rotational axes</td>
<td style="text-align: left;"></td>
<td>mask (1)</td>
<td></td>
</tr>
<tr>
<td><strong>$384</strong></td>
<td>Disable G92 persistence</td>
<td style="text-align: left;">Disables save/restore of G92 offset to non-volatile storage (NVS).</td>
<td>boolean (0)</td>
<td></td>
</tr>
<tr style="color: var(--sl-orange);">
<td><strong>$392</strong></td>
<td>Spindle on delay</td>
<td style="text-align: left;">Delay to allow spindle to spin up after safety door is opened.</td>
<td>s (4)</td>
<td></td>
</tr>
<tr style="color: var(--sl-orange);">
<td><strong>$393</strong></td>
<td>Coolant on delay</td>
<td style="text-align: left;">Delay to allow coolant to restart after safety door is opened.</td>
<td>s (1)</td>
<td></td>
</tr>
<tr>
<td><strong>$395</strong></td>
<td>Default spindle</td>
<td style="text-align: left;">Spindle selected on startup.</td>
<td>integer (0)</td>
<td></td>
</tr>
<tr style="color: var(--sl-blue-d);">
<td><strong>$398</strong></td>
<td>Planner buffer blocks</td>
<td style="text-align: left;">Number of blocks in the planner buffer.
~Controller reset required for setting change to take effect~</td>
<td>(128)</td>
<td></td>
</tr>
<tr>
<td><strong>$450</strong></td>
<td>Button 1 action</td>
<td style="text-align: left;">Assign a real-time action to button 1, or run your own macro g-code.</td>
<td>integer (1)</td>
<td rowspan="6"><a href="https://resources.sienci.com/view/slb-manual/#action-buttons">Docs</a></td>
</tr>
<tr>
<td><strong>$451</strong></td>
<td>Button 2 action</td>
<td style="text-align: left;">Assign a real-time action to button 2, or run your own macro g-code.</td>
<td>integer (2)</td>
</tr>
<tr>
<td><strong>$452</strong></td>
<td>Button 3 action</td>
<td style="text-align: left;">Assign a real-time action to button 3, or run your own macro g-code.</td>
<td>integer (4)</td>
</tr>
<tr>
<td><strong>$453</strong></td>
<td>Button 1 macro</td>
<td style="text-align: left;">Macro content, limited to 127 characters. Separate lines with the vertical bar character |.</td>
<td>(G4P0)</td>
</tr>
<tr>
<td><strong>$454</strong></td>
<td>Button 2 macro</td>
<td style="text-align: left;">Macro content, limited to 127 characters. Separate lines with the vertical bar character |.</td>
<td>(G4P0)</td>
</tr>
<tr>
<td><strong>$455</strong></td>
<td>Button 3 macro</td>
<td style="text-align: left;">Macro content, limited to 127 characters. Separate lines with the vertical bar character |.</td>
<td>(G4P0)</td>
</tr>
<tr>
<td><strong>$456</strong></td>
<td>Aux output 0 trigger</td>
<td style="text-align: left;">A second, more common action can be assigned to trigger this output. M62/63 P# is always available as a buffered on/off or M64/65 P# as an immediate on/off.</td>
<td>integer (0)</td>
<td rowspan="4"><a href="https://resources.sienci.com/view/slb-manual/#switch-amp-aux-power">Docs</a></td>
</tr>
<tr>
<td><strong>$457</strong></td>
<td>Aux output 1 trigger</td>
<td style="text-align: left;">A second, more common action can be assigned to trigger this output. M62/63 P# is always available as a buffered on/off or M64/65 P# as an immediate on/off.</td>
<td>integer (2)</td>
</tr>
<tr>
<td><strong>$458</strong></td>
<td>Aux output 2 trigger</td>
<td style="text-align: left;">A second, more common action can be assigned to trigger this output. M62/63 P# is always available as a buffered on/off or M64/65 P# as an immediate on/off.</td>
<td>integer (0)</td>
</tr>
<tr>
<td><strong>$459</strong></td>
<td>Aux output 3 trigger</td>
<td style="text-align: left;">A second, more common action can be assigned to trigger this output. M62/63 P# is always available as a buffered on/off or M64/65 P# as an immediate on/off.</td>
<td>integer (2)</td>
</tr>
<tr>
<td><strong>$462</strong></td>
<td>Run/stop register</td>
<td style="text-align: left;">MODVFD register for run/stop.</td>
<td>decimal (8192)</td>
<td rowspan="12"><a href="https://resources.sienci.com/view/slb-manual/#spindlers485">Docs</a></td>
</tr>
<tr>
<td><strong>$463</strong></td>
<td>Frequency set register</td>
<td style="text-align: left;">MODVFD register to set frequency.</td>
<td>decimal (1893)</td>
</tr>
<tr>
<td><strong>$464</strong></td>
<td>Frequency get register</td>
<td style="text-align: left;">MODVFD register to get frequency.</td>
<td>decimal (8451)</td>
</tr>
<tr>
<td><strong>$465</strong></td>
<td>Run CW command</td>
<td style="text-align: left;">MODVFD command word for CW.</td>
<td>decimal (18)</td>
</tr>
<tr>
<td><strong>$466</strong></td>
<td>Run CCW command</td>
<td style="text-align: left;">MODVFD command word for CCW.</td>
<td>decimal (34)</td>
</tr>
<tr>
<td><strong>$467</strong></td>
<td>Stop command</td>
<td style="text-align: left;">MODVFD command word for stop.</td>
<td>decimal (1)</td>
</tr>
<tr>
<td><strong>$468</strong></td>
<td>RPM input multiplier</td>
<td style="text-align: left;">MODVFD RPM value multiplier for programming RPM.</td>
<td>(50)</td>
</tr>
<tr>
<td><strong>$469</strong></td>
<td>RPM input divider</td>
<td style="text-align: left;">MODVFD RPM value divider for programming RPM.</td>
<td>(60)</td>
</tr>
<tr>
<td><strong>$470</strong></td>
<td>RPM output multiplier</td>
<td style="text-align: left;">MODVFD RPM value multiplier for reading RPM.</td>
<td>(60)</td>
</tr>
<tr>
<td><strong>$471</strong></td>
<td>RPM output divider</td>
<td style="text-align: left;">MODVFD RPM value divider for reading RPM.</td>
<td>(100)</td>
</tr>
<tr>
<td><strong>$478</strong></td>
<td>Spindle 2 Modbus address</td>
<td style="text-align: left;">Spindle 2 Modbus address.</td>
<td>(3)</td>
</tr>
<tr>
<td><strong>$479</strong></td>
<td>Spindle 3 Modbus address</td>
<td style="text-align: left;">Spindle 3 Modbus address.</td>
<td>(4)</td>
</tr>
<tr>
<td><strong>$481</strong></td>
<td>Autoreport interval</td>
<td style="text-align: left;">Interval the real time report will be sent, set to 0 to disable.
~Controller reset required for setting change to take effect~</td>
<td>ms (0)</td>
<td></td>
</tr>
<tr>
<td><strong>$484</strong></td>
<td>Unlock required after E-Stop</td>
<td style="text-align: left;">If set, unlock (by sending $X) is required after resetting a cleared E-Stop condition.</td>
<td>boolean (1)</td>
<td></td>
</tr>
<tr>
<td><strong>$486</strong></td>
<td>Lock coordinate systems</td>
<td style="text-align: left;">Lock coordinate systems against accidental changes.</td>
<td>mask (0)</td>
<td></td>
</tr>
<tr>
<td><strong>$511</strong></td>
<td>Spindle 1</td>
<td style="text-align: left;">Spindle to use as spindle 1.
~Controller reset required for setting change to take effect~</td>
<td>integer (7)</td>
<td rowspan="7"><a href="https://resources.sienci.com/view/slb-manual/#spindlers485">Docs</a></td>
</tr>
<tr>
<td><strong>$512</strong></td>
<td>Spindle 2</td>
<td style="text-align: left;">Spindle to use as spindle 2.
~Controller reset required for setting change to take effect~</td>
<td>integer (8)</td>
</tr>
<tr>
<td><strong>$513</strong></td>
<td>Spindle 3</td>
<td style="text-align: left;">Spindle to use as spindle 3.
~Controller reset required for setting change to take effect~</td>
<td>integer (5)</td>
</tr>
<tr>
<td><strong>$520</strong></td>
<td>Spindle 0 tool number start</td>
<td style="text-align: left;">Start of tool numbers for selecting spindle 0 (default spindle). Normally leave this at 0.</td>
<td>(0)</td>
</tr>
<tr>
<td><strong>$521</strong></td>
<td>Spindle 1 tool number start</td>
<td style="text-align: left;">Start of tool numbers for selecting spindle 1.</td>
<td>(0)</td>
</tr>
<tr>
<td><strong>$522</strong></td>
<td>Spindle 2 tool number start</td>
<td style="text-align: left;">Start of tool numbers for selecting spindle 2.</td>
<td>(0)</td>
</tr>
<tr>
<td><strong>$523</strong></td>
<td>Spindle 3 tool number start</td>
<td style="text-align: left;">Start of tool numbers for selecting spindle 3.</td>
<td>(0)</td>
</tr>
<tr style="color: var(--sl-blue-d);">
<td><strong>$650</strong></td>
<td>Chopper toff</td>
<td style="text-align: left;">Off time. Duration of slow decay phase as a multiple of system clock periods: NCLK= 24 + (32 x TOFF). This will limit the maximum chopper frequency (0-15).
0: MOSFETs shut off, driver disabled.
1: Use with TBL of minimum 24 clocks.</td>
<td>integer (1)</td>
<td></td>
</tr>
<tr style="color: var(--sl-blue-d);">
<td><strong>$651</strong></td>
<td>Chopper tbl</td>
<td style="text-align: left;">Blanking time interval in system clock periods (0-3 = 16,24,36,54). Needs to cover the switching event and the duration of the ringing on the sense resistor.</td>
<td>integer (1)</td>
<td></td>
</tr>
<tr style="color: var(--sl-blue-d);">
<td><strong>$652</strong></td>
<td>Chopper chm</td>
<td style="text-align: left;">Chopper mode. Affects HDEC, HEND, and HSTRT parameters.
0: Standard mode (SpreadCycle).
1: Constant TOFF with fast decay time. Fast decay is after on time. Fast decay time is also terminated when the negative nominal current is reached.</td>
<td>boolean (0)</td>
<td></td>
</tr>
<tr style="color: var(--sl-blue-d);">
<td><strong>$653</strong></td>
<td>Chopper hstr</td>
<td style="text-align: left;">CHM=0: Hysteresis start, offset from HEND (0-7 = 1-8). To be effective, HEND+HSTRT must be ≤15.
CHM=1: Fast decay time. Three least-significant bits of the duration of the fast decay phase. The MSB is HDEC0. Fast decay time is a multiple of system clock periods: NCLK= 32 x (HDEC0+HSTRT).</td>
<td>integer (2)</td>
<td></td>
</tr>
<tr style="color: var(--sl-blue-d);">
<td><strong>$654</strong></td>
<td>Chopper hend</td>
<td style="text-align: left;">Can be either negative, zero, or positive, 0-15 = -3 to 12.
CHM=0: Hysteresis end (low). Sets the hysteresis end value after a number of decrements, used for the hysteresis chopper and controlled by HDEC. HSTRT+HEND must be less than 16. 1/512 adds to the current setting.
CHM=1: Sine wave offset. A positive offset corrects for zero crossing error. 1/512 adds to the absolute value of each sine wave entry.</td>
<td>integer (8)</td>
<td></td>
</tr>
<tr style="color: var(--sl-blue-d);">
<td><strong>$655</strong></td>
<td>Chopper hdec</td>
<td style="text-align: left;">CHM=0: Hysteresis decrement interval period in system clock periods. Determines the slope of the hysteresis during on time from fast to very slow (0-3 = 16,32,48,64).
CHM=1: Fast decay mode.</td>
<td>integer (0)</td>
<td></td>
</tr>
<tr style="color: var(--sl-blue-d);">
<td><strong>$656</strong></td>
<td>Chopper rndtf</td>
<td style="text-align: left;">Change from fixed to randomized TOFF times, by dNCLK= -24 to +6 clocks. Only for CHM=1.</td>
<td>boolean (1)</td>
<td></td>
</tr>
<tr style="color: var(--sl-blue-d);">
<td><strong>$657</strong></td>
<td>THRESH</td>
<td style="text-align: left;">StallGuard threshold.</td>
<td>(22)</td>
<td></td>
</tr>
<tr style="color: var(--sl-blue-d);">
<td><strong>$658</strong></td>
<td>CoolStep semin</td>
<td style="text-align: left;">Lower CoolStep threshold. If the SG value falls below SEMIN x 32, the coil current scaling factor is increased (0-15).
0: CoolStep disabled.</td>
<td>integer (7)</td>
<td></td>
</tr>
<tr style="color: var(--sl-blue-d);">
<td><strong>$659</strong></td>
<td>CoolStep seup</td>
<td style="text-align: left;">Number of increments of the coil current each time SG is sampled below the lower threshold (0-3 = 1,2,4,8).</td>
<td>(3)</td>
<td></td>
</tr>
<tr style="color: var(--sl-blue-d);">
<td><strong>$660</strong></td>
<td>CoolStep semax</td>
<td style="text-align: left;">Upper CoolStep threshold offset from lower threshold. If SG is sampled above (SEMIN+SEMAX+1)x32 enough times, the coil current scaling factor is decremented (0-15).</td>
<td>(0)</td>
<td></td>
</tr>
<tr style="color: var(--sl-blue-d);">
<td><strong>$661</strong></td>
<td>CoolStep sedn</td>
<td style="text-align: left;">Number of times SG must be sampled above the upper threshold before the coil current is decremented (0-3 = 32,8,2,1).</td>
<td>(3)</td>
<td></td>
</tr>
<tr style="color: var(--sl-blue-d);">
<td><strong>$662</strong></td>
<td>CoolStep seimin</td>
<td style="text-align: left;">Minimum CoolStep current as a factor of the set motor current.
0: 1/2, 1: 1/4</td>
<td>boolean (0)</td>
<td></td>
</tr>
<tr style="color: var(--sl-blue-d);">
<td><strong>$663</strong></td>
<td>drvconf_reg</td>
<td style="text-align: left;">DRVCONF register defaults 0xA31F. All protections enabled.</td>
<td>(41759)</td>
<td></td>
</tr>
<tr>
<td><strong>$664</strong></td>
<td>Ring pixels</td>
<td style="text-align: left;">Number of individual pixels or LEDs connected.
~Controller reset required for setting change to take effect~</td>
<td>(0)</td>
<td rowspan="2"><a href="https://resources.sienci.com/view/slb-manual/#status-lights">Docs</a></td>
</tr>
<tr>
<td><strong>$665</strong></td>
<td>Rail pixels</td>
<td style="text-align: left;">Number of individual pixels or LEDs connected. Include the onboard LED.
~Controller reset required for setting change to take effect~</td>
<td>(1)</td>
</tr>
<tr style="color: var(--sl-orange);">
<td><strong>$666</strong></td>
<td>Using add-ons</td>
<td style="text-align: left;">Sienci specific capability flags.</td>
<td>mask (0)</td>
<td></td>
</tr>
<tr>
<td><strong>$668</strong></td>
<td>Invert TLS input</td>
<td style="text-align: left;">Invert the TLS input ahead of the OR function.
~Controller reset required for setting change to take effect~</td>
<td>boolean (1)</td>
<td></td>
</tr>
<tr>
<td><strong>$730</strong></td>
<td>Maximum laser power</td>
<td style="text-align: left;">Maximum S word power for laser.</td>
<td>(255)</td>
<td rowspan="9"><a href="https://resources.sienci.com/view/slb-manual/#laser">Docs</a></td>
</tr>
<tr>
<td><strong>$731</strong></td>
<td>Minimum laser power</td>
<td style="text-align: left;">Minimum S word power for laser.</td>
<td>(0)</td>
</tr>
<tr>
<td><strong>$733</strong></td>
<td>Laser PWM frequency</td>
<td style="text-align: left;">Laser PWM frequency.</td>
<td>Hz (1000)</td>
</tr>
<tr>
<td><strong>$734</strong></td>
<td>Laser PWM off value</td>
<td style="text-align: left;">Laser PWM off value in percent (duty cycle).</td>
<td>percent (0)</td>
</tr>
<tr>
<td><strong>$735</strong></td>
<td>Laser PWM min value</td>
<td style="text-align: left;">Laser PWM min value in percent (duty cycle).</td>
<td>percent (0)</td>
</tr>
<tr>
<td><strong>$736</strong></td>
<td>Laser PWM max value</td>
<td style="text-align: left;">Laser PWM max value in percent (duty cycle).</td>
<td>percent (100)</td>
</tr>
<tr>
<td><strong>$741</strong></td>
<td>Laser X offset</td>
<td style="text-align: left;">Laser offset from spindle on X-axis.</td>
<td>mm (0)</td>
</tr>
<tr>
<td><strong>$742</strong></td>
<td>Laser Y offset</td>
<td style="text-align: left;">Laser offset from spindle on Y-axis.</td>
<td>mm (0)</td>
</tr>
<tr>
<td><strong>$743</strong></td>
<td>Invert laser signals</td>
<td style="text-align: left;">Inverts the laser enable and PWM signals (active high).
~Controller reset required for setting change to take effect~</td>
<td>mask (0)</td>
</tr>
</tbody>
</table>
[/su_table]
<h2>Useful commands</h2>
<ul>
 	<li aria-level="1">$$: lists all Firmware settings</li>
 	<li aria-level="1">$RST=$: resets all your EEPROM settings to the default Firmware values</li>
 	<li aria-level="1">?: reports any active inputs plus some other useful info</li>
 	<li aria-level="1">$G: lists current active grbl Modals</li>
 	<li aria-level="1">$I: tells you information on your board Firmware Version and Plugins</li>
 	<li aria-level="1">$$=##: will let you know the Name and Description of that Setting</li>
 	<li aria-level="1">$ESG: will tell you the Names and Descriptions of all Settings</li>
 	<li aria-level="1">$EAG: will tell you the Names and Descriptions of all Alarms</li>
</ul>
<h2><span style="color: #ff0000;">Alarms</span></h2>
[su_table responsive="yes"]
<table>
<thead>
<tr>
<th>Alarm Code</th>
<th>Message</th>
<th>Description</th>
<th>Example</th>
</tr>
</thead>
<tbody>
<tr>
<td><strong>1</strong></td>
<td>Hard limit</td>
<td style="text-align: left;">Hard limit has been triggered. Machine position is likely lost due to sudden halt. Re-homing is highly recommended.</td>
<td><a href="https://youtu.be/I1EhAPNXdzQ?t=208" target="_blank" rel="noopener">Example</a></td>
</tr>
<tr>
<td><strong>2</strong></td>
<td>Soft limit</td>
<td style="text-align: left;">Soft limit alarm. G-code motion target exceeds machine travel. Machine position retained. Alarm may be safely unlocked.</td>
<td><a href="https://youtu.be/I1EhAPNXdzQ?t=226" target="_blank" rel="noopener">Example</a></td>
</tr>
<tr>
<td><strong>3</strong></td>
<td>Abort during cycle</td>
<td style="text-align: left;">Reset while in motion. Machine position is likely lost due to sudden halt. Re-homing is highly recommended. May be due to issuing g-code commands that exceed the limit of the machine.</td>
<td></td>
</tr>
<tr>
<td><strong>4</strong></td>
<td>Probe fail</td>
<td style="text-align: left;">Probe fail. Probe is not in the expected initial state before starting probe cycle when G38.2 and G38.3 is not triggered and G38.4 and G38.5 is triggered. Your bit is likely making contact with the touch plate or the circuit is completed before the bit is moving. Move the bit away from the touch plate.</td>
<td><a href="https://youtu.be/I1EhAPNXdzQ?t=267" target="_blank" rel="noopener">Example</a></td>
</tr>
<tr>
<td><strong>5</strong></td>
<td>Probe fail</td>
<td style="text-align: left;">Probe fail. Probe did not contact the workpiece within the programmed travel for G38.2 and G38.4. Your bit is too far away from the touch plate. Move the bit closer, it should be within 6-12mm (1/4 -1/2in) away.</td>
<td><a href="https://youtu.be/I1EhAPNXdzQ?t=306" target="_blank" rel="noopener">Example</a></td>
</tr>
<tr>
<td><strong>6</strong></td>
<td>Homing fail</td>
<td style="text-align: left;">Homing fail. The active homing cycle was reset.</td>
<td></td>
</tr>
<tr>
<td><strong>7</strong></td>
<td>Homing fail</td>
<td style="text-align: left;">Homing fail. Safety door was opened during homing cycle.</td>
<td></td>
</tr>
<tr>
<td><strong>8</strong></td>
<td>Homing fail</td>
<td style="text-align: left;">Homing fail. Pull off travel failed to clear limit switch. The machine is within the limit switches range when it tries to move away. Try increasing pull-off setting or check wiring.</td>
<td><a href="https://youtu.be/jmiaWA5tiVw?t=563" target="_blank" rel="noopener">Example</a></td>
</tr>
<tr>
<td><strong>9</strong></td>
<td>Homing fail</td>
<td style="text-align: left;">Homing fail. Could not find limit switch within search distances. Try increasing max travel, decreasing pull-off distance, or check wiring. The limit switch wasn't triggered in the distances expected. If your z-axis is moving away from the switch when homing, check your firmware and confirm you have the correct profile for your machine.</td>
<td><a href="https://youtu.be/jmiaWA5tiVw?t=531" target="_blank" rel="noopener">Example</a></td>
</tr>
<tr>
<td><strong>10</strong></td>
<td>E-Stop asserted</td>
<td style="text-align: left;">E-Stop asserted. Clear and reset. Untwist your E-stop.</td>
<td></td>
</tr>
<tr>
<td><strong>11</strong></td>
<td>Homing required</td>
<td style="text-align: left;">Homing required. Execute homing command ($H) to continue. Your machine can't start up until you first Home.</td>
<td></td>
</tr>
<tr>
<td><strong>12</strong></td>
<td>Limit switch engaged</td>
<td style="text-align: left;">Limit switch engaged. Clear before continuing. A limit switch is on or off when it’s not supposed to, check if you've triggered them accidentally or you set them up the wrong way. fixed</td>
<td></td>
</tr>
<tr>
<td><strong>13</strong></td>
<td>Probe protection</td>
<td style="text-align: left;">Probe protection triggered. Clear before continuing.</td>
<td></td>
</tr>
<tr>
<td><strong>14</strong></td>
<td>SaS timeout</td>
<td style="text-align: left;">Spindle at speed timeout. Clear before continuing. This can also trigger if you've set up a VFD that's not sending back correct signals to the board.</td>
<td></td>
</tr>
<tr>
<td><strong>15</strong></td>
<td>Homing fail</td>
<td style="text-align: left;">Homing fail. Could not find second limit switch for auto squared axis within search distances. Try increasing max travel, decreasing pull-off distance, or check wiring.</td>
<td></td>
</tr>
<tr>
<td><strong>16</strong></td>
<td>Selftest failed</td>
<td style="text-align: left;">Power on selftest (POS) failed.</td>
<td></td>
</tr>
<tr>
<td><strong>17</strong></td>
<td>Motor fault</td>
<td style="text-align: left;">Motor fault.</td>
<td></td>
</tr>
<tr>
<td><strong>18</strong></td>
<td>Homing fail</td>
<td style="text-align: left;">Homing fail. Bad configuration.</td>
<td></td>
</tr>
</tbody>
</table>
[/su_table]
<h2><span style="color: #ff8b3d;">Errors</span></h2>
[su_table responsive="yes"]
<table>
<thead>
<tr>
<th>Error Code</th>
<th>Message</th>
<th>Description</th>
</tr>
</thead>
<tbody>
<tr>
<td><strong>1</strong></td>
<td>Expected command letter</td>
<td style="text-align: left;">G-code words consist of a letter and a value. Letter was not found.</td>
</tr>
<tr>
<td><strong>2</strong></td>
<td>Bad number format</td>
<td style="text-align: left;">Missing the expected G-code word value or numeric value format is not valid.</td>
</tr>
<tr>
<td><strong>3</strong></td>
<td>Invalid statement</td>
<td style="text-align: left;">Grbl ‘$’ system command was not recognized or supported.</td>
</tr>
<tr>
<td><strong>4</strong></td>
<td>Value &lt; 0</td>
<td style="text-align: left;">Negative value received for an expected positive value.</td>
</tr>
<tr>
<td><strong>5</strong></td>
<td>Setting disabled</td>
<td style="text-align: left;">Homing cycle failure. Homing is not enabled via settings.</td>
</tr>
<tr>
<td><strong>6</strong></td>
<td>Value &lt; 3 μsec</td>
<td style="text-align: left;">Minimum step pulse time must be greater than 3μsec.</td>
</tr>
<tr>
<td><strong>7</strong></td>
<td>EEPROM read fail. Using defaults</td>
<td style="text-align: left;">An EEPROM read failed. Auto-restoring affected EEPROM to default values.</td>
</tr>
<tr>
<td><strong>8</strong></td>
<td>Not idle</td>
<td style="text-align: left;">Grbl ‘$’ command cannot be used unless Grbl is IDLE. Ensures smooth operation during a job.</td>
</tr>
<tr>
<td><strong>9</strong></td>
<td>G-code lock</td>
<td style="text-align: left;">G-code commands are locked out during alarm or jog state.</td>
</tr>
<tr>
<td><strong>10</strong></td>
<td>Homing not enabled</td>
<td style="text-align: left;">Soft limits cannot be enabled without homing also enabled.</td>
</tr>
<tr>
<td><strong>11</strong></td>
<td>Line overflow</td>
<td style="text-align: left;">Max characters per line exceeded. Received command line was not executed.</td>
</tr>
<tr>
<td><strong>12</strong></td>
<td>Step rate &gt; 30kHz</td>
<td style="text-align: left;">Grbl ‘$’ setting value cause the step rate to exceed the maximum supported.</td>
</tr>
<tr>
<td><strong>13</strong></td>
<td>Check Door</td>
<td style="text-align: left;">Safety door detected as opened and door state initiated.</td>
</tr>
<tr>
<td><strong>14</strong></td>
<td>Line length exceeded</td>
<td style="text-align: left;">Build info or startup line exceeded EEPROM line length limit. Line not stored.</td>
</tr>
<tr>
<td><strong>15</strong></td>
<td>Travel exceeded</td>
<td style="text-align: left;">Jog target exceeds machine travel. Jog command has been ignored.</td>
</tr>
<tr>
<td><strong>16</strong></td>
<td>Invalid jog command</td>
<td style="text-align: left;">Jog command has no ‘=’ or contains prohibited g-code.</td>
</tr>
<tr>
<td><strong>17</strong></td>
<td>Setting disabled</td>
<td style="text-align: left;">Laser mode requires PWM output.</td>
</tr>
<tr>
<td><strong>20</strong></td>
<td>Unsupported command</td>
<td style="text-align: left;">Unsupported or invalid g-code command found in block.</td>
</tr>
<tr>
<td><strong>21</strong></td>
<td>Modal group violation</td>
<td style="text-align: left;">More than one g-code command from same modal group found in block.</td>
</tr>
<tr>
<td><strong>22</strong></td>
<td>Undefined feed rate</td>
<td style="text-align: left;">Feed rate has not yet been set or is undefined.</td>
</tr>
<tr>
<td><strong>23</strong></td>
<td>Invalid gcode ID:23</td>
<td style="text-align: left;">G-code command in block requires an integer value.</td>
</tr>
<tr>
<td><strong>24</strong></td>
<td>Invalid gcode ID:24</td>
<td style="text-align: left;">More than one g-code command that requires axis words found in block.</td>
</tr>
<tr>
<td><strong>25</strong></td>
<td>Invalid gcode ID:25</td>
<td style="text-align: left;">Repeated g-code word found in block.</td>
</tr>
<tr>
<td><strong>26</strong></td>
<td>Invalid gcode ID:26</td>
<td style="text-align: left;">No axis words found in block for g-code command or current modal state which requires them.</td>
</tr>
<tr>
<td><strong>27</strong></td>
<td>Invalid gcode ID:27</td>
<td style="text-align: left;">Line number value is invalid.</td>
</tr>
<tr>
<td><strong>28</strong></td>
<td>Invalid gcode ID:28</td>
<td style="text-align: left;">G-code command is missing a required value word.</td>
</tr>
<tr>
<td><strong>29</strong></td>
<td>Invalid gcode ID:29</td>
<td style="text-align: left;">G59.x work coordinate systems are not supported.</td>
</tr>
<tr>
<td><strong>30</strong></td>
<td>Invalid gcode ID:30</td>
<td style="text-align: left;">G53 only allowed with G0 and G1 motion modes.</td>
</tr>
<tr>
<td><strong>31</strong></td>
<td>Invalid gcode ID:31</td>
<td style="text-align: left;">Axis words found in block when no command or current modal state uses them.</td>
</tr>
<tr>
<td><strong>32</strong></td>
<td>Invalid gcode ID:32</td>
<td style="text-align: left;">G2 and G3 arcs require at least one in-plane axis word.</td>
</tr>
<tr>
<td><strong>33</strong></td>
<td>Invalid gcode ID:33</td>
<td style="text-align: left;">Motion command target is invalid.</td>
</tr>
<tr>
<td><strong>34</strong></td>
<td>Invalid gcode ID:34</td>
<td style="text-align: left;">Arc radius value is invalid.</td>
</tr>
<tr>
<td><strong>35</strong></td>
<td>Invalid gcode ID:35</td>
<td style="text-align: left;">G2 and G3 arcs require at least one in-plane offset word.</td>
</tr>
<tr>
<td><strong>36</strong></td>
<td>Invalid gcode ID:36</td>
<td style="text-align: left;">Unused value words found in block.</td>
</tr>
<tr>
<td><strong>37</strong></td>
<td>Invalid gcode ID:37</td>
<td style="text-align: left;">G43.1 dynamic tool length offset is not assigned to configured tool length axis.</td>
</tr>
<tr>
<td><strong>38</strong></td>
<td>Invalid gcode ID:38</td>
<td style="text-align: left;">Tool number greater than max supported value.</td>
</tr>
</tbody>
</table>
[/su_table]
