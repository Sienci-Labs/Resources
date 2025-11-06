---
title: ytsb Tool Changing
menu_order: 0
post_status: draft
post_excerpt: How to cut multiple toolpaths for CAM programs without tool changing functionality. This method is suitable for the LongMill Benchtop CNC, and other hobby CNCs.
post_date: 2022-03-17 20:27:00
taxonomy:
    knowledgebase_cat: lmk2-advanced
    knowledgebase_tag:
        - mk2
custom_fields:
    KBName: LongMill MK2 CNC
    basepress_post_icon: bp-caret-right
skip_file: no
featured_image: 
---

As you begin tackling more complex CNC projects, you'll start to notice that running multi-tool jobs becomes a necessity. Using multiple bits on the same workpiece can save time or achieve greater detail and give you the carving flexibility you need; whether it's a v-bit for engraving and an end mill for profiling, or an end mill for roughing and a tapered bit for finishing.

## Method 1: Separate Files

This is the easiest and most straight forward approach to tool changing. Many CAM programs allow for each toolpath to be exported as separate files. By creating separate g-code files for each cutting tool you'll be using, you can just:

1. Start with your first tool and first file
1. Wait for the file to complete then jog your router off to the side
1. Change the cutting tool out for the second one
1. Use a touch plate or tool length sensor to measure the new zero point (off your wasteboard or material, depending on how you set up the job)
1. Reposition and run the second file
1. Repeat this process until completion

Just be sure to give each file a clear naming scheme so you execute them in the right order and with the right tool. For example, your first file could be called "cat_1_v-bit", then your second "cat_2_endmill", and your third "cat_3_tapered". You can also specify the tool size or angle, any other prompts that ensure you run the order of files successfully with their corresponding bits.

## Method 2: Manual Editing

This method will also work for g-code sending programs that do not have tool changing functionality, the difference with this one is that all the toolpaths will be in one file. The instructions below are written in millimetre values, however you can replace the values to be in inches as long as the g-code was generated using inches.

This is a tool change method inspired by the work of Stuart McRae (a LongMill customer).

### Setup

<ol>
  <li>Generate your g-code to the file format .nc or .gcode.</li>
  <li>Zero your machine in the X, Y, and Z on the mounted stock material.</li>
  <li>Open up the g-code using NC Viewer and check the first few lines for the call-out of the correct units (G20 for inches, G21 for mm) and for G90, absolute coordinates.</li>
  <li>Go line by line to find where the tool changes should occur, by looking at the toolpath visualization on NC Viewer. Use your mouse or keyboard to move to each line, and you should see an end mill following the coordinates called out in the g-code.</li>
  <li>Add the following g-code for each tool change.[su_table responsive="yes"]
<table>
<tbody>
<tr>
<td><b>G-code</b></td>
<td><b>Explanation</b></td>
</tr>
<tr>
<td>Z20.00</td>
<td>Raises the bit to 20mm above your zero.</td>
</tr>
<tr>
<td>X?.??Y?.??</td>
<td>Moves bit to a defined XY position. This is the location of your tool change. CHANGE THIS to a position in which the stock material hasn’t been cut, and is accessible.</td>
</tr>
<tr>
<td>M0;</td>
<td>Pauses job. This is when you turn off the router, change your bit and lower your router manually via Z-axis pulley to zero the bit with a piece of paper. Once you are done you will turn on the router and press PLAY on the g-code sender program.</td>
</tr>
<tr>
<td>G92Z0.125</td>
<td>Sets the current Z position as 0.125mm (paper thickness) above your zero. So it now knows where the Z-axis zero is.</td>
</tr>
<tr>
<td>G0Z25.00</td>
<td>Raises your bit 25mm above your zero.</td>
</tr>
</tbody>
</table>
[/su_table]</li>
  <li>Save the g-code you just edited as a new file on your computer.</li>
  <li>Load the file into your g-code sender program.</li>
  <li>The machine will run through the first toolpath, cutting into the material, then will lift up and move to the bit changing position you defined. It will stop moving, in a HOLD state, until you press PLAY. Complete the tool change and zero the machine manually - note that the surface will be marked by the bit once you turn your router back on.</li>
  <li>Repeat Step 8 for each tool change.</li>
</ol>

Below are some examples of how to input the tool changing g-code, which are in <b>bold</b>.

#### EXAMPLE 1: Carbide Create

G90<br>
G21<br>
(Toolpath 3)<br>
M05<br>
M0 ;T102<br>
M03S18000<br>
G0X12.00Y10.41Z5.00<br>
G1Z-1.00F457.2<br>
X36.00F1524.0<br>
Z5.00<br>
(Toolpath 4)<br>
<b>Z20.00</b><br>
<b>X5.00Y20.00</b><br>
<b>M0 ;T201</b> // this line was already in the g-code<br>
<b>G92Z0.125</b><br>
<b>G0Z25.00</b><br>
S18000<br>
G0X12.26Y22.84<br>
G1Z-1.00F381.0<br>
X36.26F2286.0<br>
Z5.00<br>
M05<br>
M02
_____________________________________

#### EXAMPLE 2: CAMLab

G21<br>
G90<br>
G0 X7.2948 Y-8.1954 Z2.0<br>
G1 Z-0.6522 F2000<br>
G1 X-16.3552<br>
G1 Y-8.2454<br>
G1 X7.2948<br>
G1 Y-8.1954<br>
G0 Z2.0<br>
G0 Y8.6204<br>
G1 Z-0.6522<br>
G1 Y8.6704<br>
G1 X-16.3552<br>
G1 Y8.6204<br>
G1 X7.2948<br>
G0 Z2.0<br>
<b>Z20.00</b><br>
<b>X5.00Y20.00</b><br>
<b>M0</b><br>
<b>G92Z0.125</b><br>
<b>G0Z25.00</b><br>
…

## Method 3: gSender Tool Change

The g-code for tool changing is an M6 command, in which the program will pause until the user tells it to continue, usually through a ‘Resume’ and/or ‘Confirm Tool Change’ button on the machine interface program. In CAM programs, this M6 will be inserted in your g-code if there are toolpaths using different bits, thus requiring tool changes. On <a href="https://sienci.com/gSender/">gSender</a>, you can program what happens when there is M6 in your g-code, therefore allowing you to easily change your bits with pre-programmed actions. Full instructions can be found <a href="https://resources.sienci.com/view/gs-additional-features/#tool-changing">here</a>.
