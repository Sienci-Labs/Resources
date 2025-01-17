---
title: Wasteboard Surfacing
menu_order: 12
post_status: publish
post_excerpt: How to surface your wasteboard on the LongMill Benchtop CNC. You can download the surfacing g-code here or generate your own on INTUWiz.
post_date: 2021-04-30 15:25:00
taxonomy:
    knowledgebase_cat: lm-assembly
    knowledgebase_tag:
        - mk1
custom_fields:
    KBName: LongMill CNC
    basepress_post_icon: bp-caret-right
skip_file: no
featured_image: /_images/_longmill/_assembly/_surfacing/lm_surface_p1.png
---

https://www.youtube.com/embed/aW27K_1OLT0

## Why surface your wasteboard?

<ol>
  <li>Surfacing your wasteboard helps level the surface in relation to your machine. This means that if you have bumps or uneven surfaces on your wasteboard, or if your wasteboard is higher on one side that the other, surfacing will even out and flatten the board.</li>
  <li>Cleans off old marks and scars, leaving you with a new, clean surface to glue, clamp, and mount your workpiece.</li>
</ol>

If you are using a <a href="https://sienci.com/product/22mm-surfacing-bit/">22mm surfacing bit</a>, you can use this code for your LongMill. This code will cut 1mm down in one pass. Please set your origin to the bottom left corner of the machine.

<a href="https://sienci.com/wp-content/uploads/2020/01/LongMill-Surfacing-Code.zip">Download LongMill Surfacing Code (12x12, 12x30, 30x30)</a>

## What tool should I use?

Technically, any flat end mill or bit can work for this application. However, using a wider bit can speed up the process. In the video we are using a 22mm surfacing bit.

## Generating the code

I used a g-code generator from INTUWiz (<a href="http://www.intuwiz.com/plane.html#.Xidt8sjYouV">http://www.intuwiz.com/plane.html#.Xidt8sjYouV</a>). Here are the settings I used for the 30x30 size:

![](/_images/_longmill/_assembly/_surfacing/lm_surface_p1.png){.aligncenter .size-medium}

The center of the coordinates is in a point: 1<br>
Side a: 762<br>
Side b: 762<br>
Tool diameter: 22<br>
Y overlap percentage: 45<br>
Total depth of cutting: 1<br>
Depth of cutting per pass: 1<br>
Feed rate (X,Y G00): 2000<br>
Feed rate (X,Y, G01): 2000<br>
Feed rate( Z G00): 500<br>
Feed rate(Z G01): 500<br>

**You can also use a different program if you want and cut a shallow pocket of the size you need.**
