---
title: Routers / Spindles
menu_order: 0
post_status: draft
post_excerpt: Learn about router and spindle options for the LongMill CNC, with consideration for noise, speed control, cost. The recommended tool is the Makita RT0700/RT0701.
post_date: 2021-04-19 16:31:00
taxonomy:
    knowledgebase_cat: lmk2-the-basics
    knowledgebase_tag:
        - mk2
custom_fields:
    KBName: LongMill MK2 CNC
    basepress_post_icon: bp-caret-right
skip_file: yes
featured_image: 
---

Routers and spindles come in all shapes and sizes. When considering the right tool for your machine, there are several things you want to look out for such as:

<ul>
  <li>Power</li>
  <li>Speed and speed control</li>
  <li>Size and weight</li>
  <li>Runout</li>
</ul>

Many hobby CNC routers tend to utilize trim routers because their power, weight, price, and off-the-shelf circuitry balance well with hobby applications. After much testing with the LongMill, we landed on the Makita RT0700/RT0701 as the ideal choice.

## Makita RT0700/RT0701

![](/_images/_longmill/_the-basics/lm_routersspindle_p1_Makita.jpg){.alignleft .size-full .nar}

<a href="http://www.homedepot.com/p/Makita-1-1-4-HP-Compact-Router-RT0701C/204247210" target="_blank" rel="noreferrer noopener">Home Depot (US)</a>

<a href="https://www.homedepot.ca/en/home/p.compact-router.1000848739.html" target="_blank" rel="noreferrer noopener">Home Depot (Canada)</a>

<a href="https://www.amazon.com/Makita-RT0701C-1-1-Compact-Router/dp/B00E7D3V4S/" target="_blank" rel="noreferrer noopener">Amazon (US)</a>

<a href="https://www.amazon.ca/gp/product/B00E7D3V4S?ie=UTF8" target="_blank" rel="noreferrer noopener">Amazon (Canada)</a>

The Makita RT0700/RT0701 router is a very commonly used and reliable trim router boasting a 1-1/4HP motor. It offers a wide speed range (10,000RPM to 30,000RPM), which is electronically controlled to achieve for reliable speeds even under load. With a metal body, it is extremely durable. Our test units have been used for hundreds of hours without fail, on projects that take over 6 hours. This is our go-to recommended router as it is widely available in both 120V and 220V.

## Other Routers

The LongMill's standard router mount has a 65mm bore but is also available in:  <b>52mm</b>, <b>71mm</b>, and <b>80mm</b>. This means that mounting other routers is possible, though the Makita is the only one that's been thoroughly tested for use on the LongMill.

![](/_images/_longmill/_the-basics/lm_routersspindle_p2_65RMount.jpg){.aligncenter .size-medium}

Here is a list of some other routers that could be used. If your router isn't listed, you'll need to measure it's diameter and check if anything protrudes or if an adapter may be needed:

<ul>
  <li>Dewalt DWP611 (uses 71mm mount)</li>
  <li>Carbide 3D Compact Router (uses 65mm mount)</li>
  <li>Avid Power MW104 (uses 65mm mount)</li>
  <li>MLCS Rocky 30 9056 (uses 65mm mount)</li>
  <li>Ridgid R2401 (needs to adapt from 61mm to our 80mm mount to clear it's ~6x15mm protruding body notch)</li>
  <li>Bosch Colt PR20EVS (uses 71mm mount but sits much higher up than normal, you'll have to space up your material)</li>
  <li>Bosch Colt GKF125 (needs to adapt from 72mm to our 80mm mount, also sits much higher up than normal)</li>
</ul>

## Three-phase Spindles

![](/_images/_longmill/_the-basics/lm_routersspindle_p3_RouterPkg.png){.aligncenter .size-medium}

Three-phase spindles are commonly used in higher-end, semi-professional to professional-level machines. They come with several advantages over traditional woodworking routers such as:

<ul>
  <li>Quieter operation</li>
  <li>More power</li>
  <li>Lower run-out</li>
  <li>Longer life</li>
  <li>Ability to integrate speed and direction control directly from the control board</li>
</ul>

They also come with some downsides:

<ul>
  <li>More expensive</li>
  <li>Can be challenging to set up</li>
  <li>Larger and heavier</li>
</ul>

The LongMill's control box has the necessary outputs to interface with most market spindles. This includes:

<ul>
  <li>0-5V PWM signal for speed control</li>
  <li>0-5V toggle for direction control</li>
</ul>

Consult your spindle manufacturer for details on wiring and programming if this is something you're considering since it tends to vary between manufacturers.

If you are a beginner user, we highly recommend sticking with a Makita RT0701. The Makita RT0701 offers plenty of power and speed control for this application. Installing a spindle can be very technically challenging and may cost significantly more. If you plan on adding a spindle we recommend checking our <a href="https://forum.sienci.com/" target="_blank" rel="noopener">Forum</a> and <a href="https://www.facebook.com/groups/mill.one" target="_blank" rel="noopener">Facebook Group</a> for more info or checking out our own guide below.

### Adding a spindle

![](/_images/_longmill/_the-basics/lm_routersspindle_p4_Spindle.jpeg){.aligncenter .size-medium}

We supply <a href="https://sienci.com/product/router-mount-for-longmill-benchtop-cnc/" target="_blank" rel="noopener">65mm, 71mm, and 80mm router mounts</a> that are sized to match with commonly available 3-phase spindles. From our experience, most come in 65mm and 80mm diameters.

Although we do not offer technical support on adding a spindle, here are some general steps on adding a spindle:

<b>1. Choose the correct size, voltage, RPM, cooling, and power requirements</b>

Most spindles in this size range will have a 1.5-2.2kW rating, or 2HP to 3HP approximately, and come with a 65mm or 80mm body. The larger the spindle, generally the higher the power and larger the end mills you can use; going past 2.2kW on any hobby machine though immediately diminishes returns since the rigidity of the machine becomes the main limitation. Most spindles will also use 110V or 220V power and must be matched with the correct VFD to work properly, and you will have to make sure your household wiring can provide the amount of power required to run your spindle.

Most spindles also come with either air cooling or water cooling. Water cooling spindles may be more compact at the spindle side but require an additional setup for the water and pumps to work properly. Air-cooled spindles are simpler and easier to install but may be larger than water-cooled and create more noise.

<b>2. Properly wire, shield, and program your spindle</b>

Installing your router mount is fairly straightforward. Simply move your machine to the highest point on the Z-axis and undo the four M5 bolts from the back. Swap out the router mount to the size you need.

![](/_images/_longmill/_the-basics/lm_routersspindle_p5_WireRoute.jpeg){.aligncenter .size-medium}

From here you can mount your spindle and wire the cables through the drag chains. It is very important to use a properly shielded cable and ground your cable properly, as 3-phase spindles can create a lot of interference. You will also need to program your VFD using the appropriate values to control things like the method of control, your input voltage and frequency, your output voltage and frequency, PWM signal speed ranges, and more.

<b>3. Test your spindle and motion system</b>

Because the spindle is most likely heavier than the Makita RT0701, the machine will need to work harder to move the spindle around. Although it's not likely you'll need to change any settings, it is recommended to try moving your machine around with the heavier spindle and slow down your machine's max feed rates in the firmware if you run into any stalling. Note that the added weight may affect the wear and tear on components such as the Delrin nuts and V-wheels.

<a href="https://sienci.com/2022/07/21/adding-a-spindle-to-your-longmill/" target="_blank" rel="noopener">For a longer form, general article on adding a spindle, check out our full blog post</a>.

Some settings you might need to change are shown below. If you're moving a specific axis of the machine and it's 'stalling out'/ not moving then you definitely need to update these values. You'd want to focus first on the 'maximum rates' (110 to 112), reducing the value for the stalling axis by increments of 100 until the problem goes away. If  this doesn't work you can also try lowering the 'acceleration' values (120 to 122)

![](/_images/_longmill/_the-basics/lm_routersspindle_p6_Firmware.png){.aligncenter .size-medium}

## Not Recommended

Handheld rotary tools like Dremels are highly underpowered for use on the LongMill since they do not have internal hardware that allows them to support the high lateral and axial forces. In addition, these tools are fabricated for hand use, and as such aren't designed for the minimal runout required to cut precisely.
