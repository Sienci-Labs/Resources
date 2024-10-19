---
title: ytsb Feeds & Speeds ⏩
menu_order: 3
post_status: draft
post_excerpt: A list of materials that can be cut by the LongMill CNC, with considerations for cutting tools and best practices. Wood, plastic, foam and soft metal suggested.
post_date: 2022-03-17 20:35:00
taxonomy:
    knowledgebase_cat: lmk2-handbook
    knowledgebase_tag:
        - mk2
custom_fields:
    KBName: LongMill MK2 CNC
    basepress_post_icon: bp-caret-right
skip_file: yes
featured_image: 
---

When cutting material with a rotating bit, you can imagine that going too slow will dull or break the bit very quickly. For example, imagine trying to cut through a plank of wood with a saw except instead of moving the saw back and forth you're just trying to push it directly through. Similarly, a bit that's moving too fast can burn or melt the material that you're cutting. Finding a happy medium between these two extremes is a balancing act between three main factors:

<ol>
<li>How quickly the tool is translating (feed rate/plunge rate)</li>
<li>How fast the tool is spinning (spindle speed)</li>
<li>How much material the tool is removing at any given time (depth of cut &amp; step over)</li>
</ol>

Each of these factors must be suited to the properties of the material that you're cutting; cutting through foam can happen much faster than cutting aluminum. We generalize these variables under the term 'feeds and speeds', and each cutting tool has a different set of ideal feeds and speeds. Learning how to tie a tool's size and shape to its movement, rotation speed, material type, and material removal rate is nearly an art form. There are engineers whose job is knowing how to properly balance all these numbers and apply them based on part geometry, desired finish, and the total job cutting time. Without the proper planning, you can expect many headaches along the way including broken tools, broken material, and an uneven or rough surface finish on your project. Feed and speed choice depends on the material you are cutting, the type of tool you use, the speed of the router, the rigidity of the machine, and even the geometry of the model. In order to balance speed, finish quality, and precision you must account for bit deflection and material hardness. When cutting, the tool can be pushed away from where it should be since it's not able to cut the material fast enough. Harder materials require a more rigid machine and longer milling times to steadily cut the material away. Sometimes it will take some trial and error to dial-in the right settings for your desired setup and materials.

**Higher tool RPM produces smaller chips, while higher feed rates produce larger chips. Overall, if the chips are too large, your bit will be likely to break, but if your chips are too small (like fine powder), you will be dulling your bit. It’s all about getting the right balance.**

## Terminology

<b>Feed rate:</b> how quickly the tool moves in the X and Y directions, usually defined in millimeters (or inches) per minute.<br>
<b>Plunge rate:</b> how quickly the tool moves in the Z direction, usually defined in millimeters (or inches) per minute.<br>
<b>Spindle speed:</b> the speed that the tool spins in the rotary tool, defined in RPM (rotations per minute). Most compact routers operate at speeds between 10,000 and 30,000 RPM.<br>
<b>Depth of cut/Step down:</b> the amount of depth that the CNC machine removes with every cutting pass, defined in millimeters or inches.<br>
<b>Step over:</b> the offset that is applied between the old cutting pass and the new one, usually defined as a percentage of the tool's cutting diameter.

## Recommendations

Since there are so many different types and sizes of cutting tools, we've created a list below of just 3 different cutting tools that we strongly recommend to get started on your machine. We've created <a href="https://resources.sienci.com/view/lm-materials/" target="_blank" rel="noopener noreferrer">feed and speed tables</a> for these tools for cutting in various materials so that you can copy/paste the values you need for your first projects. If you're looking to get started with this recommended list, all of these tools can be found for purchase <a href="https://sienci.com/product-category/cutting-tools/" target="_blank" rel="noopener noreferrer">in our store!</a>

Ensure that any cutting tool you end up using is installed as deeply as possible into the router, with a bare-minimum of 3/8” of the tool being inside the router for light cuts.

These feeds and speeds are meant to be a starting point in finding the right parameters that work best for your setup. Feeds and speeds listed on this page have been tested to work with <b>2-flute, 1/8" carbide end mills</b>, the type of cutting tool that is most readily available <a href="http://sienci.com/product/18-flat-end-mill/" target="_blank" rel="noopener noreferrer">in our store</a>. Unless you're doing 3D contour cutting where the z-axis moves up and down a lot, we usually recommended lower plunge rates (100mm/min to 300mm/min) for most materials. You'll need to know the speed range of the Makita RT0701:

<table class="wp-table" width="70%">
<tbody>
<tr>
<td>Setting</td>
<td>1</td>
<td>2</td>
<td>3</td>
<td>4</td>
<td>5</td>
<td>6</td>
</tr>
<tr>
<td>Speed (RPM)</td>
<td>10,000</td>
<td>12,000</td>
<td>17,000</td>
<td>22,000</td>
<td>27,000</td>
<td>30,000</td>
</tr>
</tbody>
</table>
