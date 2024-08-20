---
title: ytsb Noise, EMI, & Grounding
menu_order: 4
post_status: draft
post_excerpt: For sudden disconnections and stopping, ground your CNC machine to reduce electromagnetic interference (EMI), which generates from dust collectors.
post_date: 2024-08-12 17:17
taxonomy:
    knowledgebase_cat: lm-advanced
    knowledgebase_tag:
        - mk1
custom_fields:
    KBName: LongMill CNC
    basepress_post_icon: bp-caret-right
skip_file: no
featured_image: /_images/_longmill/_advanced/_2_noise/lm_noise_p1.png
---

Static buildup and other electromagnetic interferences (a.k.a. electrical noise) can be cause for concern on any CNC. These unexpected electrical signals can find their way back to your CNC controller and disrupt it's on-board electronics, affecting how reliably your CNC can cut projects for you. If you've ever found your machine stopping mid-way through a job, disconnecting from the g-code sender, or giving unexpected alerts then you may be experiencing EMI.

<strong>IMPORTANT: EMI does not cause the LongMill to lose position or move erratically. It is a very common misconception that grounding your machine will help prevent missed steps, stalling, or positioning issues. EMI only causes CNC machines stop completely or disconnect from the computer. If your machine is not moving the way you think it should, it is a mechanical issue or an issue in your g-code. If you are experiencing these issues, please start with double checking the mechanics of your machine.</strong>

This behaviour can stem from many sources but most often it's being created as static on a dust collection hose or, less commonly, on the frame of the machine itself.

If you:
<ul>
  <li>Are cutting / surfacing materials that tend to accumulate static charge such as MDF, epoxy, or other plastics</li>
  <li>Have a low-quality dust collector that's not appropriately grounded</li>
  <li>Are using a low-quality hose that isn't anti-static or doesn't contain an inner metal wire spiral</li>
  <li>Run your CNC in a more humid environment</li>
  <li>Have incorrectly wired ground lines to your garage or shop</li>
</ul>

Then these can all trigger the creation of a trouble-making static signal.

For instance: dust collection inherently generates static electricity when fine wood dust flows through plastic components such as hoses and cyclones. If your dust collection system is not set up with proper grounding these charges will find and disrupt the LongMill controller.

<h2>Fixing the Problem</h2>

If you believe any of this is happening to you the appropriate fix will depend on your particular situation. For instance, an easy way to check for a properly set up dust collector and hose is to wear insulating shoes and suck up a sample of material before then walking over to touch a large metal surface to see if you experience a shock through your fingertips. If so, then you've successfully narrowed down the issue and can now look into grounding your equipment appropriately.

If you're looking for a 'catch-all' solution, these are normally less effective but can still be beneficial. The most common way is by having an escape path for built-up charges. This 'ground point' works because it'll be a path of least resistance which stray charges will prefer to take instead of sticking around.

If you plan to try this, ensure that you only use <b>one ground point</b> for your entire machine setup (including dust collection). For example, if your home has just one electrical panel, you can ground it on that or the attached ground stake outside. This avoids possible ground loops which can create additional interference.

<strong>Materials</strong>
<ul>
  <li>Bare solid copper wire between 10 to 18 AWG</li>
  <li>Fastening hardware such as prong connector, screw, or ground plug
<ul>
  <li>Depending on how you wish to fasten the wire, you may need to drill a hole into enclosures, solder and/or crimp wire ends</li>
</ul>
</li>
  <li>You can also pick up something like the Grounding Kit that's offered by Lee Valley. This is a collection of essentially speaker wire, twist-on wire connectors, and some screws: <a href="https://www.leevalley.com/en-ca/shop/tools/workshop/dust-collection/parts-and-accessories/62616-grounding-kit-for-dust-collection-systems?item=03J6201" target="_blank" rel="noopener">https://www.leevalley.com/en-ca/shop/tools/workshop/dust-collection/parts-and-accessories/62616-grounding-kit-for-dust-collection-systems?item=03J6201</a></li>
</ul>

<h2>Instructions</h2>

<ol>
  <li>Wrap the copper wire around the body of the dust shoe and hose securely. Take any steps necessary to avoid getting the wire caught in any moving parts.</li>
  <li>Fix the wire in place with your fastening method of choice at the dust shoe end.</li>
  <li>Fix the wire in place at the ground end, with some slack so that the wire does not constrain the movement of the machine. Directly attach the wire to the ground stake or through grounded items such as:</li>
<ul>
  <li>Outlet box</li>
  <li>Electrical box</li>
  <li>Grounded power bar (3 prong)</li>
</ul>
</ol>

![](/_images/_longmill/_advanced/_2_noise/lm_noise_p1.png){.aligncenter .size-medium}

<h2>UPS Backup for power smoothing</h2>

Depending on where you live or how your shop is wired up, power flickers and brief outages can make their way through to your shop outlets. This might not be noticeable for regular power tools, but it can effect precision machines like a CNC or even for a desktop computer. You can identify this problem for yourself if, after grounding your machine, you still get unexpected behaviour from your machine such as:

<ul>
  <li>unexpected stopping</li>
  <li>random disconnects</li>
  <li>random, single movements that shift your cutting job</li>
</ul>

A backup UPS solves these issues by continuing to provide power to your computer and CNC temporarily when your shops power flickers off. This will allow you to either keep your LongMill running reliably, or if the power outage is severe, return it to a set point before waiting for power to return.

You can find these on Amazon or big box stores, by searching up "UPS backup 1500VA." Good quality, high power UPS backups are around $200 CAD. Look for UPS devices with<strong> 1000-1500VA</strong> and at least <strong>4 plugs with</strong><span class="a-list-item"><strong> battery backup</strong> functionality. T</span>his should have enough power to sustain your machine and computer. Depending on the UPS, you can connect your router as well however we recommend prioritizing your CNC and computer first. For information on the power consumption of the LongMill, check <a href="https://sienci.com/faq/lm-faq/what-are-the-power-requirements-for-the-LongMill/">here</a>.
