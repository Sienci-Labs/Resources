---
title: ytsb Wasteboard Surfacing
menu_order: 4
post_status: draft
post_excerpt: How to surface your wasteboard on the LongMill Benchtop CNC. You can download the surfacing g-code here or generate your own on INTUWiz.
post_date: 2024-04-30 17:12
taxonomy:
    knowledgebase_cat: lm-assembly
    knowledgebase_tag:
        - mk1
custom_fields:
    KBName: LongMill CNC
    basepress_post_icon: bp-caret-right
skip_file: no
featured_image: 
---
<figure><iframe src="https://www.youtube.com/embed/aW27K_1OLT0" width="100%" height="315" frameborder="0" allowfullscreen="allowfullscreen" data-mce-fragment="1"></iframe></figure>
<h2><strong>Why surface your wasteboard?</strong></h2>
<ol>
 	<li>Surfacing your wasteboard helps level the surface in relation to your machine. This means that if you have bumps or uneven surfaces on your wasteboard, or if your wasteboard is higher on one side that the other, surfacing will even out and flatten the board.</li>
 	<li>Cleans off old marks and scars, leaving you with a new, clean surface to glue, clamp, and mount your workpiece.</li>
</ol>
If you are using a <a href="https://sienci.com/product/22mm-surfacing-bit/">22mm surfacing bit</a>, you can use this code for your LongMill. This code will cut 1mm down in one pass. Please set your origin to the bottom left corner of the machine.

<a href="https://sienci.com/wp-content/uploads/2020/01/LongMill-Surfacing-Code.zip">Download LongMill Surfacing Code (12x12, 12x30, 30x30)</a>
<h2><strong>What tool should I use?</strong></h2>
Technically, any flat end mill or bit can work for this application. However, using a wider bit can speed up the process. In the video we are using a 22mm surfacing bit.
<h2><strong>Generating the code</strong></h2>
I used a gcode generator from INTUWiz (<a href="http://www.intuwiz.com/plane.html#.Xidt8sjYouV">http://www.intuwiz.com/plane.html#.Xidt8sjYouV</a>). Here are the settings I used for the 30x30 size:

<img class="size-medium wp-image-1307 aligncenter" src="https://resources.sienci.com/wp-content/uploads/2021/04/gcode-surfacing-750x1024-1-623x850.png" alt="" width="623" height="850" />

The center of the coordinates is in a point: 1

Side a: 762

Side b: 762

Tool diameter: 22

Y overlap percentage: 45

Total depth of cutting: 1

Depth of cutting per pass: 1

Feed rate (X,Y G00): 2000

Feedrate (X,Y, G01): 2000

Feedrate( Z G00): 500

Feedrate(Z G01): 500

<strong>You can also use a different program if you want and cut a shallow pocket of the size you need.</strong>