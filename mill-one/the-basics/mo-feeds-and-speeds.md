---
title: Feeds & Speeds
menu_order: 4
post_status: publish
post_excerpt: 
post_date: 2021-04-30 18:45:00 
taxonomy:
    knowledgebase_cat: mo-basics 
    knowledgebase_tag:
        - mill-one
custom_fields:
    KBName: Mill One CNC
    basepress_post_icon: bp-caret-right
skip_file: no
featured_image: 
---

If you don't understand the importance of feeds and speeds for CNC routing and milling, refer back to the explanation given in our <a href="https://resources.sienci.com/view/mo-cutting-tools/">Cutting Tool Guide</a>. This page is meant to briefly explain some of the required terminology that you'll need to know moving forward, and just as importantly, it will provide you with a table of recommended feeds and speeds that you can refer back to when you'd like to start cutting different types of materials.

Feed and speed choice depends on the material you are cutting, the type of tool you use, the speed of the router, the rigidity of the machine, and even the geometry of the model. In order to balance speed, finish quality, and precision you must account for bit deflection and material hardness.

When cutting, the tool can be pushed away from where it should be since it's not able to cut the material fast enough. Harder materials require a more rigid machine and longer milling times to steadily cut the material away. Sometimes it will take some trial and error to dial-in the right settings for your desired setup and materials.

## Terminology

<b>Feed rate:</b> how quickly the tool moves in the X and Y directions, usually defined in millimeters (or inches) per minute.

<b>Plunge rate:</b> how quickly the tool moves in the Z direction, usually defined in millimeters (or inches) per minute.

<b>Spindle speed:</b> the speed that the tool spins in the rotary tool, defined in RPM (rotations per minute). Most compact routers operate at speeds between 10,000 and 30,000 RPM.

<b>Depth of cut/ Step down:</b> the amount of depth that the CNC machine removes with every cutting pass, defined in millimeters or inches.

<b>Step over:</b> the offset that is applied between the old cutting pass and the new one, usually defined as a percentage of the tool's cutting diameter.

## Recommendations

These feeds and speeds are meant to be a starting point in finding the right parameters that work best for your setup. Feeds and speeds listed on this page have been tested to work with <b>2-flute, 1/8" carbide end mills</b>, the type of cutting tool that is most readily available <a href="https://sienci.com/product-category/cutting-tools/" target="_blank" rel="noopener">in our store</a>.

Unless you're doing 3D contour cutting where the z-axis moves up and down a lot, we usually recommended lower plunge rates (100mm/min to 300mm/min) for most materials.

The corresponding spindle speeds for the Ridgid and Makita routers are also below.

### Rough Cutting Settings

<table width="20">
<tbody>
<tr>
<td align="center" valign="middle">Material</td>
<td align="center" valign="middle">Feed Rate (mm/ min)</td>
<td align="center" valign="middle">Plunge Rate (mm/ min)</td>
<td align="center" valign="middle">Step Over</td>
<td align="center" valign="middle">Step Down (mm)</td>
<td align="center" valign="middle">Spindle Speed (RPM)</td>
</tr>
<tr>
<td align="center" valign="middle">Wood (general)</td>
<td align="center" valign="middle">700</td>
<td align="center" valign="middle">250</td>
<td align="center" valign="middle">0.45</td>
<td align="center" valign="middle">2</td>
<td align="center" valign="middle">20000</td>
</tr>
<tr>
<td align="center" valign="middle">Pine/Cedar</td>
<td align="center" valign="middle">800</td>
<td align="center" valign="middle">250</td>
<td align="center" valign="middle">0.45</td>
<td align="center" valign="middle">2</td>
<td align="center" valign="middle">20000</td>
</tr>
<tr>
<td align="center" valign="middle">MDF</td>
<td align="center" valign="middle">700</td>
<td align="center" valign="middle">200</td>
<td align="center" valign="middle">0.2</td>
<td align="center" valign="middle">1.2</td>
<td align="center" valign="middle">22000</td>
</tr>
<tr>
<td align="center" valign="middle">Acrylic</td>
<td align="center" valign="middle">800</td>
<td align="center" valign="middle">250</td>
<td align="center" valign="middle">0.4</td>
<td align="center" valign="middle">1.8</td>
<td align="center" valign="middle">24000</td>
</tr>
<tr>
<td align="center" valign="middle">Aluminum</td>
<td align="center" valign="middle">1000</td>
<td align="center" valign="middle">100</td>
<td align="center" valign="middle">0.2</td>
<td align="center" valign="middle">0.4</td>
<td align="center" valign="middle">20000</td>
</tr>
<tr>
<td align="center" valign="middle">HDPE</td>
<td align="center" valign="middle">1100</td>
<td align="center" valign="middle">250</td>
<td align="center" valign="middle">0.35</td>
<td align="center" valign="middle">1.5</td>
<td align="center" valign="middle">20000</td>
</tr>
<tr>
<td align="center" valign="middle">Maple</td>
<td align="center" valign="middle">800</td>
<td align="center" valign="middle">250</td>
<td align="center" valign="middle">0.45</td>
<td align="center" valign="middle">1</td>
<td align="center" valign="middle">20000</td>
</tr>
<tr>
<td align="center" valign="middle">Pinewood</td>
<td align="center" valign="middle">1000</td>
<td align="center" valign="middle">250</td>
<td align="center" valign="middle">0.3</td>
<td align="center" valign="middle">1.5</td>
<td align="center" valign="middle">20000</td>
</tr>
<tr>
<td align="center" valign="middle">Circuit Board</td>
<td align="center" valign="middle">800</td>
<td align="center" valign="middle">100</td>
<td align="center" valign="middle">0.3</td>
<td align="center" valign="middle">N/A</td>
<td align="center" valign="middle">20000</td>
</tr>
<tr>
<td align="center" valign="middle">Foam</td>
<td align="center" valign="middle">1500</td>
<td align="center" valign="middle">800</td>
<td align="center" valign="middle">0.7</td>
<td align="center" valign="middle">2</td>
<td align="center" valign="middle">20000</td>
</tr>
</tbody>
</table>

### Ridgid R24012

<table width="20">
<tbody>
<tr>
<td align="center" valign="middle">Setting</td>
<td align="center" valign="middle">1</td>
<td align="center" valign="middle">2</td>
<td align="center" valign="middle">3</td>
<td align="center" valign="middle">4</td>
<td align="center" valign="middle">5</td>
<td align="center" valign="middle">6</td>
<td align="center" valign="middle">7</td>
</tr>
<tr>
<td align="center" valign="middle">Speed (RPM)</td>
<td align="center" valign="middle">20,000</td>
<td align="center" valign="middle">21,000</td>
<td align="center" valign="middle">22,500</td>
<td align="center" valign="middle">25,000</td>
<td align="center" valign="middle">27,500</td>
<td align="center" valign="middle">29,000</td>
<td align="center" valign="middle">30,000</td>
</tr>
</tbody>
</table>

### Makita RT0701

<table width="20">
<tbody>
<tr>
<td align="center" valign="middle">Setting</td>
<td align="center" valign="middle">1</td>
<td align="center" valign="middle">2</td>
<td align="center" valign="middle">3</td>
<td align="center" valign="middle">4</td>
<td align="center" valign="middle">5</td>
<td align="center" valign="middle">6</td>
</tr>
<tr>
<td align="center" valign="middle">Speed (RPM)</td>
<td align="center" valign="middle">10,000</td>
<td align="center" valign="middle">12,000</td>
<td align="center" valign="middle">17,000</td>
<td align="center" valign="middle">22,000</td>
<td align="center" valign="middle">27,000</td>
<td align="center" valign="middle">30,000</td>
</tr>
</tbody>
</table>
