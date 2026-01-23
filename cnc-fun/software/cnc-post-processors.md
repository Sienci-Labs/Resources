---
title: Post-Processors
menu_order: 3
post_status: publish
post_excerpt: Post-processors used for the grbl-based CNC machines, covering programs such as Vectric, Fusion360, Carveco, Carbide Create and Easel.
post_date: 2026-01-21 16:11:00
taxonomy:
    knowledgebase_cat: software
    knowledgebase_tag:
        - cnc fundamentals
custom_fields:
    KBName: Fundamentals
    basepress_post_icon: bp-caret-right
skip_file: no
featured_image: _images/_cnc-fun/_software/cnc_so_postpro-longmill.jpg
---

When making g-code for any CNC machine, there will come a time where you'll click the final button to "Generate g-code". Doing so, how will you know that the g-code file is going to be properly suited to your particular CNC? Though many CNCs are able to interpret what's broadly known as 'g-code', the reality is that different manufacturers have their own quirks that their machines expect to see; you can think of this as g-code being the primary language while different CNCs speak with dialects or accents. For our machines, and many other hobby CNCs, this dialect is known as "grbl".

This is where post-processing comes in. A 'post-processor' is simply a set of rules that can be followed to add tweaks to the main g-code and ensure it'll work for particular machines. If the post-processor isn't selected or set up correctly this will usually result in errors, stalls, or unexpected behaviour while running your jobs.

To help out, here are the most popular CAM programs and their LongMill/AltMill-compatible post-processors. Some CAM programs may not have post-processor options since they're already designed for hobby CNC use.

**Note that**: even if you design in inches, it is best practice to export files with a millimeters post-processor. Unfortunately we have seen errors show up when the g-code file was exported in inches.

[su_table responsive="yes"]
<table>
<tbody>
<tr>
<td><b>CAM Software</b></td>
<td><b>Post-Processor</b></td>
</tr>
<tr>
<td>Vectric Cut2D, Vectric VCarve, Vectric Aspire</td>
<td>grbl (mm). Newer versions of Vectric may come with a default "LongMill" option.</td>
</tr>
<tr>
<td>Carveco Maker, Carveco Maker+</td>
<td>UGS grbl</td>
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
<td>Estlcam</td>
<td>No selection required</td>
</tr>
<tr>
<td>FreeCAD</td>
<td>grbl (mm)</td>
</tr>
<tr>
<td>BobCAD/CAM</td>
<td>Custom: <a href="https://forum.sienci.com/t/CAD-CAM-software-post-processors/436/3" target="_blank" rel="noopener">https://forum.sienci.com/t/CAD-cam-software-post-processors/436/3</a></td>
</tr>
<tr>
<td>Inventor CAM</td>
<td>grbl (mm)</td>
</tr>
</tbody>
</table>
[/su_table]
[/su_table]

**To avoid potential issues with Fusion 360, we also recommend you make the following checks to your post-processor:

- Change the '**Safe Retracts**' to “Clearance Height” and NOT “G28”. It will be obvious that you have this on if you don't have limit switches or forget to home your machine and at the start of the job your bit plunges suddenly really deep into your material.
- **Output M6** set as "No" (unless you plan to set up tool changing)
- **Output Tool Number** set as "No" (unless you plan to set up tool changing)

<h3>Vectric VCarve</h3>
If you are using <strong>Vectric VCarve</strong>, you can create a custom machine configuration file for your CNC. Go to Machine, and in the drop down select Machine Configuration.

![](/_images/_cnc-fun/_software/cnc_so_postpro_vectric-config.jpg){.aligncenter .size-medium}

Please refer to the image below to fill out the configuration. For the latest version of VCarve, please input all the LongMill accelerations as 750mm/s² and AltMill accelerations as 1500 mm/s². If not using these CNC's, consult your manufacturer for your recommended motor speeds.

![](/_images/_cnc-fun/_software/cnc_so_postpro-longmill.jpg){.aligncenter .size-medium}

https://youtu.be/6Hr-pja4eI8

**Fun fact:** some other members of the grbl CNC family include OpenBuilds, Shapeoko, BobsCNC and X-Carve - all starting just as the LongMill has from an Arduino Uno.
