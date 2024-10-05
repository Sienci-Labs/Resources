---
title: Post Processors
menu_order: 0
post_status: draft
post_excerpt: 
post_date: 2021-04-20 16:45:00
taxonomy:
    knowledgebase_cat: lmk2-software
    knowledgebase_tag:
        - mk2
custom_fields:
    KBName: LongMill MK2 CNC
    basepress_post_icon: bp-caret-right
skip_file: yes
featured_image: 
---

When making g-code for any CNC machine, there will come a time where you'll click the final button to "Generate g-code". Doing so, how will you know that the g-code file is going to be properly suited to your particular CNC? Though many CNCs are able to interpret what's broadly known as 'g-code', the reality is that different manufacturers have their own quirks that their machines expect to see; you can think of this as g-code being the primary language while different CNCs speak with dialects or accents. For the LongMill and many other hobby CNCs, this dialect is known as "grbl".

This is where post processing comes in. A 'post processor' is simply a set of rules that can be followed to add tweaks to the main g-code and ensure it'll work for particular machines. If the post processor isn't selected or set up correctly this will usually result in errors, stalls, or unexpected behaviour while running your jobs.

To help out, we've put together a simple table which shows popular CAM programs and their LongMill-compatible post processors. Some CAM programs may not have post processor options since they're already designed for hobby CNC use.

**Note that**: even if you design in inches, you'll usually want to export files in **millimeters** since CNCs are most comfortable with those

[su_table responsive="yes"]
<table>
<tbody>
<tr>
<td><b>CAM Software</b></td>
<td><b>Post Processor</b></td>
</tr>
<tr>
<td>Vectric Cut2D, Vectric VCarve, Vectric Aspire</td>
<td>grbl (mm)</td>
</tr>
<tr>
<td>Carveco Maker, Carveco Maker+</td>
<td>grbl (mm)</td>
</tr>
<tr>
<td>Fusion 360</td>
<td>grbl**</td>
</tr>
<tr>
<td>Easel, Easel Pro</td>
<td>No selection required</td>
</tr>
<tr>
<td>Carbide Create</td>
<td>grbl</td>
</tr>
<tr>
<td>CAMLab</td>
<td>No selection required</td>
</tr>
<tr>
<td>ESTL CAM</td>
<td>No selection required</td>
</tr>
<tr>
<td>FreeCAD</td>
<td>grbl (mm)</td>
</tr>
<tr>
<td>BobCAD/CAM</td>
<td>Custom: <a href="https://forum.sienci.com/t/CAD-CAM-software-post-processors/436/3" target="_blank" rel="noopener">https://forum.sienci.com/t/cad-cam-software-post-processors/436/3</a></td>
</tr>
<tr>
<td>Inventor CAM</td>
<td>grbl (mm)</td>
</tr>
</tbody>
</table>
[/su_table]

**To avoid potential issues with Fusion 360, we also recommend you make the following checks to your post processor:

<ul>
  <li><b>G28 Safe Retracts</b> set as “Clearance Height”</li>
  <li><b>Output M6</b> set as "No"</li>
  <li><b>Output Tool Number</b> set as "No"</li>
</ul>

If you're interested, there have also been instances of LM community members putting their own post processors to download. Some examples include:

<ul>
  <li>Chris B: <a href="https://www.facebook.com/groups/mill.one/permalink/1053271605144170/" target="_blank" rel="noopener">https://www.facebook.com/groups/mill.one/permalink/1053271605144170/</a></li>
  <li>Duane S: <a href="https://www.facebook.com/groups/mill.one/permalink/1122661888205141/" target="_blank" rel="noopener">https://www.facebook.com/groups/mill.one/permalink/1122661888205141/</a></li>
</ul>

<b>Fun fact:</b> some other members of the grbl CNC family include OpenBuilds, Shapeoko, BobsCNC and X-Carve - all starting just as the LongMill has from an Arduino Uno.
