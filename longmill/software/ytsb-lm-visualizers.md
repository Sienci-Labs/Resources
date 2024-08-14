---
title: ytsb Visualizers
menu_order: 4
post_status: draft
post_excerpt: CNC g-code visualizers are a great way to verify the toolpaths of your g-code file before running them on your LongMill CNC machine.
post_date: 2024-04-30 15:58
taxonomy:
    knowledgebase_cat: lm-software
    knowledgebase_tag:
        - mk1
custom_fields:
    KBName: LongMill CNC
    basepress_post_icon: bp-caret-right
skip_file: yes
featured_image: /_images/_longmill/_software/lm_visualizers_p1_g-code.JPG
---
<p>Visualizing how your cutting instructions (g-code file) are going to play out before executing them on your machine is very valuable. It can help you to to verify that the machine is going to cut out your project in the way that you expect it to. Most CAM or Interface software will have built-in g-code visualization for this reason, either showing the line that the cutting tool will follow or rendering a full 3D view of how the material is going to be cut away.</p>
<p>This page exists in the case that your current software isn't offering you good visualization. If this is the case, you can either change one of your current software packages to one that does, or you could use a separate program. We've tested out a handful of standalone programs that you can consider in order to bridge this visualization gap:</p>

<p><!-- wp:table --></p>
<table class="wp-table" width="85%">
<tbody>
<tr>
<td><strong>Name</strong></td>
<td><strong>Type</strong></td>
<td><strong>Difficulty</strong> (1-4)</td>
<td><strong>Visualization Type<br /></strong></td>
<td><strong>Compatibility</strong></td>
<td><strong>Price</strong></td>
</tr>
<tr>
<td>G-code Simulator</td>
<td><span class="greText">Visualizer</span></td>
<td>1</td>
<td>Line</td>
<td>Online</td>
<td>Free</td>
</tr>
<tr>
<td>NC Viewer</td>
<td><span class="greText">Visualizer</span></td>
<td>1</td>
<td>Line</td>
<td>Online</td>
<td>Free</td>
</tr>
<tr>
<td>CAMotics</td>
<td><span class="greText">Vis</span> / <span class="orgText">Int</span></td>
<td>2</td>
<td>Live 3D</td>
<td>All desktops</td>
<td>Free</td>
</tr>
<tr>
<td>Discriminator</td>
<td><span class="greText">Visualizer</span></td>
<td>2</td>
<td>Line</td>
<td>Online</td>
<td>Free</td>
</tr>
<tr>
<td>NC Corrector</td>
<td><span class="greText">Visualizer</span></td>
<td>2</td>
<td>Line</td>
<td>Online</td>
<td>Free</td>
</tr>
</tbody>
</table>

<h3><strong>g-code Simulator</strong></h3>

<p><a href="https://nraynaud.github.io/webgcode/" target="_blank" rel="noopener noreferrer">https://nraynaud.github.io/webgcode/</a></p>
<p>Allows for files to be drag-and-dropped right into the window or you can copy/paste the g-code in. Highlights tool movement based on the selected line, and provides cutting bounds and estimated cutting time for your file.</p>

![](/_images/_longmill/_software/lm_visualizers_p1_g-code.JPG){.aligncenter .size-medium}

<h3><strong>NC Viewer </strong></h3>

<p><a href="https://ncviewer.com/" target="_blank" rel="noopener noreferrer">https://ncviewer.com/</a></p>
<p>Fast and easy to open and view files. Allows you to play the cutting path of the tool through 3D space.</p>

![](/_images/_longmill/_software/lm_visualizers_p2_NCViewer.JPG){.aligncenter .size-medium}

<h3><strong>CAMotics</strong></h3>

<p><a href="https://camotics.org/download.html" target="_blank" rel="noopener noreferrer">https://camotics.org/download.html</a></p>
<p>Previously known as OpenSCAM, CAMotics simulates 3-axis g-code paths, shows 3D cutouts, simulates machine geometry, and is capable of connecting directly to the buildbotics controller. It's also able to export the simulated cut work piece as an STL and can add height probing to 2D g-code files.</p>

![](/_images/_longmill/_software/lm_visualizers_p3_CAMotics.JPG){.aligncenter .size-medium}

<h3><strong>Discriminator</strong></h3>

<p><a href="https://cncedit.com/" target="_blank" rel="noopener noreferrer">https://cncedit.com/</a></p>
<p>Discriminator has more advanced tools for code editing, colouring, and code comparing. The visualization window is reasonable but a little tricky to use just like the rest of the software, and the software as a whole runs a little slowly, but otherwise it's a reasonable visualizer to use.</p>

![](/_images/_longmill/_software/lm_visualizers_p4_Discrim.JPG){.aligncenter .size-medium}

<h3><strong>NC Corrector</strong></h3>

<p><a href="http://nc-corrector.inf.ua/index_EN.htm" target="_blank" rel="noopener noreferrer">http://nc-corrector.inf.ua/index_EN.htm</a></p>
<p>Allows for easy line-by-line visualization, provides g-code statistics, g-code colouring, path selection, and measurement between tool paths. The primary downside is that the software runs quite slowly which makes it less user friendly.</p>

![](/_images/_longmill/_software/lm_visualizers_p5_NCCorrector.JPG){.aligncenter .size-medium}
