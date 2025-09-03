---
title: Router vs Spindle
menu_order: 0
post_status: draft
post_excerpt: Learn about router and spindle options for the LongMill CNC, with consideration for noise, speed control, cost. The recommended tool is the Makita RT0700/RT0701.
post_date: 2024-07-18 18:14:53
taxonomy:
    knowledgebase_cat: the-basics
    knowledgebase_tag:
        - cnc fundamentals
custom_fields:
    KBName: Fundamentals
    basepress_post_icon: bp-caret-right
skip_file: yes
featured_image: 
---

Routers and spindles come in all shapes and sizes. When considering the right tool for your machine, there are several things you want to look out for such as:

- Power
- Speed and speed control
- Size and weight
- Runout

Many hobby CNC routers tend to utilize trim routers because their power, weight, price, and off-the-shelf circuitry balance well with hobby applications. After much testing with the LongMill, we landed on the Makita RT0700/RT0701 as the ideal choice.

## Makita RT0700/RT0701

![](/_images/_longmill/_the-basics/lm_routersspindle_p1_Makita.jpg){.alignleft .size-full .nar}

<a href="http://www.homedepot.com/p/Makita-1-1-4-HP-Compact-Router-RT0701C/204247210" target="_blank" rel="noreferrer noopener">Home Depot (US)</a>

<a href="https://www.homedepot.ca/en/home/p.compact-router.1000848739.html" target="_blank" rel="noreferrer noopener">Home Depot (Canada)</a>

<a href="https://www.amazon.com/Makita-RT0701C-1-1-Compact-Router/dp/B00E7D3V4S/" target="_blank" rel="noreferrer noopener">Amazon (US)</a>

<a href="https://www.amazon.ca/gp/product/B00E7D3V4S?ie=UTF8" target="_blank" rel="noreferrer noopener">Amazon (Canada)</a>

The Makita RT0700/RT0701 router is a very commonly used and reliable trim router boasting a 1-1/4HP motor. It offers a wide speed range (10,000RPM to 30,000RPM), which is electronically controlled to achieve for reliable speeds even under load. With a metal body, it is extremely durable. Our test units have been used for hundreds of hours without fail, on projects that take over 6 hours. This is our go-to recommended router as it is widely available in both 120V and 220V.

## Other Routers

The LongMill's standard router mount has a 65mm bore but is also available in:  **52mm**, **71mm**, and **80mm**. This means that mounting other routers is possible, though the Makita is the only one that's been thoroughly tested for use on the LongMill.

![](/_images/_longmill/_the-basics/lm_routersspindle_p2_65RMount.jpg){.aligncenter .size-medium}

Here is a list of some other routers that could be used. If your router isn't listed, you'll need to measure it's diameter and check if anything protrudes or if an adapter may be needed:

- Dewalt DWP611 (uses 71mm mount)
- Carbide 3D Compact Router (uses 65mm mount)
- Avid Power MW104 (uses 65mm mount)
- MLCS Rocky 30 9056 (uses 65mm mount)
- Ridgid R2401 (needs to adapt from 61mm to our 80mm mount to clear it's ~6x15mm protruding body notch)
- Bosch Colt PR20EVS (uses 71mm mount but sits much higher up than normal, you'll have to space up your material)
- Bosch Colt GKF125 (needs to adapt from 72mm to our 80mm mount, also sits much higher up than normal)

## Three-phase Spindles

![](/_images/_longmill/_the-basics/lm_routersspindle_p3_RouterPkg.png){.aligncenter .size-medium}

Three-phase spindles are commonly used in higher-end, semi-professional to professional-level machines. They come with several advantages over traditional woodworking routers such as:

- Quieter operation
- More power
- Lower run-out
- Longer life
- Ability to integrate speed and direction control directly from the control board

They also come with some downsides:

- More expensive
- Can be challenging to set up
- Larger and heavier

The LongMill's control box has the necessary outputs to interface with most market spindles. This includes:

- 0-5V PWM signal for speed control
- 0-5V toggle for direction control

Consult your spindle manufacturer for details on wiring and programming if this is something you're considering since it tends to vary between manufacturers.

If you are a beginner user, we highly recommend sticking with a Makita RT0701. The Makita RT0701 offers plenty of power and speed control for this application. Installing a spindle can be very technically challenging and may cost significantly more. If you plan on adding a spindle we recommend checking our <a href="https://forum.sienci.com/" target="_blank" rel="noopener">Forum</a> and <a href="https://www.facebook.com/groups/mill.one" target="_blank" rel="noopener">Facebook Group</a> for more info or checking out our own guide below.

### Adding a spindle

![](/_images/_longmill/_the-basics/lm_routersspindle_p4_Spindle.jpeg){.aligncenter .size-medium}

We supply <a href="https://sienci.com/product/router-mount-for-LongMill-benchtop-cnc/" target="_blank" rel="noopener">65mm, 71mm, and 80mm router mounts</a> that are sized to match with commonly available 3-phase spindles. From our experience, most come in 65mm and 80mm diameters.

Although we do not offer technical support on adding a spindle, here are some general steps on adding a spindle:

**1. Choose the correct size, voltage, RPM, cooling, and power requirements**  
Most spindles in this size range will have a 1.5-2.2kW rating, or 2HP to 3HP approximately, and come with a 65mm or 80mm body. The larger the spindle, generally the higher the power and larger the end mills you can use; going past 2.2kW on any hobby machine though immediately diminishes returns since the rigidity of the machine becomes the main limitation. Most spindles will also use 110V or 220V power and must be matched with the correct VFD to work properly, and you will have to make sure your household wiring can provide the amount of power required to run your spindle.

Most spindles also come with either air cooling or water cooling. Water cooling spindles may be more compact at the spindle side but require an additional setup for the water and pumps to work properly. Air-cooled spindles are simpler and easier to install but may be larger than water-cooled and create more noise.

**2. Properly wire, shield, and program your spindle**  
Installing your router mount is fairly straightforward. Simply move your machine to the highest point on the Z-axis and undo the four M5 bolts from the back. Swap out the router mount to the size you need.

![](/_images/_longmill/_the-basics/lm_routersspindle_p5_WireRoute.jpeg){.aligncenter .size-medium}

From here you can mount your spindle and wire the cables through the drag chains. It is very important to use a properly shielded cable and ground your cable properly, as 3-phase spindles can create a lot of interference. You will also need to program your VFD using the appropriate values to control things like the method of control, your input voltage and frequency, your output voltage and frequency, PWM signal speed ranges, and more.

**3. Test your spindle and motion system**  
Because the spindle is most likely heavier than the Makita RT0701, the machine will need to work harder to move the spindle around. Although it's not likely you'll need to change any settings, it is recommended to try moving your machine around with the heavier spindle and slow down your machine's max feed rates in the firmware if you run into any stalling. Note that the added weight may affect the wear and tear on components such as the Delrin nuts and V-wheels.

<a href="https://sienci.com/2022/07/21/adding-a-spindle-to-your-LongMill/" target="_blank" rel="noopener">For a longer form, general article on adding a spindle, check out our full blog post</a>.

Some settings you might need to change are shown below. If you're moving a specific axis of the machine and it's 'stalling out'/ not moving then you definitely need to update these values. You'd want to focus first on the 'maximum rates' (110 to 112), reducing the value for the stalling axis by increments of 100 until the problem goes away. If  this doesn't work you can also try lowering the 'acceleration' values (120 to 122)

![](/_images/_longmill/_the-basics/lm_routersspindle_p6_Firmware.png){.aligncenter .size-medium}

## Not Recommended

Handheld rotary tools like Dremels are highly underpowered for use on the LongMill since they do not have internal hardware that allows them to support the high lateral and axial forces. In addition, these tools are fabricated for hand use, and as such aren't designed for the minimal runout required to cut precisely.

When cutting material with a rotating bit, you can imagine that going too slow will dull or break the bit very quickly. For example, imagine trying to cut through a plank of wood with a saw except instead of moving the saw back and forth you're just trying to push it directly through. Similarly, a bit that's moving too fast can burn or melt the material that you're cutting. Finding a happy medium between these two extremes is a balancing act between three main factors:

1. How quickly the tool is translating (feed rate/plunge rate)
1. How fast the tool is spinning (spindle speed)
1. How much material the tool is removing at any given time (depth of cut & step over)

Each of these factors must be suited to the properties of the material that you're cutting; cutting through foam can happen much faster than cutting aluminum. We generalize these variables under the term 'feeds and speeds', and each cutting tool has a different set of ideal feeds and speeds. Learning how to tie a tool's size and shape to its movement, rotation speed, material type, and material removal rate is nearly an art form. There are engineers whose job is knowing how to properly balance all these numbers and apply them based on part geometry, desired finish, and the total job cutting time. Without the proper planning, you can expect many headaches along the way including broken tools, broken material, and an uneven or rough surface finish on your project. Feed and speed choice depends on the material you are cutting, the type of tool you use, the speed of the router, the rigidity of the machine, and even the geometry of the model. In order to balance speed, finish quality, and precision you must account for bit deflection and material hardness. When cutting, the tool can be pushed away from where it should be since it's not able to cut the material fast enough. Harder materials require a more rigid machine and longer milling times to steadily cut the material away. Sometimes it will take some trial and error to dial-in the right settings for your desired setup and materials.

**Higher tool RPM produces smaller chips, while higher feed rates produce larger chips. Overall, if the chips are too large, your bit will be likely to break, but if your chips are too small (like fine powder), you will be dulling your bit. It’s all about getting the right balance.**

## Terminology

**Feed rate:** how quickly the tool moves in the X and Y directions, usually defined in millimeters (or inches) per minute.<br>
**Plunge rate:** how quickly the tool moves in the Z direction, usually defined in millimeters (or inches) per minute.<br>
**Spindle speed:** the speed that the tool spins in the rotary tool, defined in RPM (rotations per minute). Most compact routers operate at speeds between 10,000 and 30,000 RPM.<br>
**Depth of cut/Step down:** the amount of depth that the CNC machine removes with every cutting pass, defined in millimeters or inches.<br>
**Step over:** the offset that is applied between the old cutting pass and the new one, usually defined as a percentage of the tool's cutting diameter.

## Recommendations

Since there are so many different types and sizes of cutting tools, we've created a list below of just 3 different cutting tools that we strongly recommend to get started on your machine. We've created <a href="https://resources.sienci.com/view/lmk2-feeds-and-speeds/" target="_blank" rel="noopener noreferrer">feed and speed tables</a> for these tools for cutting in various materials so that you can copy/paste the values you need for your first projects. If you're looking to get started with this recommended list, all of these tools can be found for purchase <a href="https://sienci.com/product-category/cutting-tools/" target="_blank" rel="noopener noreferrer">in our store!</a>

Ensure that any cutting tool you end up using is installed as deeply as possible into the router, with a bare-minimum of 3/8” of the tool being inside the router for light cuts.

These feeds and speeds are meant to be a starting point in finding the right parameters that work best for your setup. Feeds and speeds listed on this page have been tested to work with **2-flute, 1/8" carbide end mills**, the type of cutting tool that is most readily available <a href="http://sienci.com/product/18-flat-end-mill/" target="_blank" rel="noopener noreferrer">in our store</a>. Unless you're doing 3D contour cutting where the z-axis moves up and down a lot, we usually recommended lower plunge rates (100mm/min to 300mm/min) for most materials. You'll need to know the speed range of the Makita RT0701:

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

<span style="font-weight: 400;">Most hobby CNC routers, including the Sienci Labs LongMill CNC, will utilize an off-the-shelf trim router. Although these are suitable for hobby use, they have some limitations both in regards to reliability over long periods of time, and a lack of ability to automate their control. Despite this, a trim router such as the popular Makita RT0701C router has a proven track record of being a very capable, easy to install option for relatively little cost.</span>

<img class="alignnone size-full wp-image-11406" src="https://resources.sienci.com/wp-content/uploads/2024/10/SpindlevsRouter.png" alt="" width="2400" height="1600" />

<span style="font-weight: 400;">A trim router offers a more ‘analog’ experience, where users must manually set the router speed using a physical dial, and turn on/off the router at the start and end of a cutting program. A key difference between routers and spindles is that a router houses all of its electronics inside of itself and plugs into a wall outlet directly, but a high speed spindle contains only the motor and rotating elements, while an intermediate ‘VFD’ (variable frequency drive) unit is used to direct power from the wall outlet to the spindle motor like shown in the diagram below.</span>

<img class="alignnone size-full wp-image-11392" src="https://resources.sienci.com/wp-content/uploads/2024/10/SpindleVFDDiagram.png" alt="" width="3300" height="1650" />

<span style="font-weight: 400;">Spindles are designed to be more mechanically robust than trim routers, in order to withstand long cycles of cutting. The addition of the VFD unit allows for advanced spindle control capability, which can be set up for a given CNC application. Furthermore, since spindles are brushless, they generate much less noise than routers, and do not wear down any motor brushes that could require replacement. To </span><i><span style="font-weight: 400;">hear</span></i><span style="font-weight: 400;"> the difference between the two, we’ve also created a short </span><a href="https://drive.google.com/file/d/1pzyp9mf-S8KwBv9TxVeKPFIRwyDMdYCE/view?usp=sharing"><span style="font-weight: 400;">video demonstration comparing the two at various running speeds</span></a><span style="font-weight: 400;">.</span>

<img class="alignnone size-full wp-image-11393" src="https://resources.sienci.com/wp-content/uploads/2024/10/SienciSpindleNoise.png" alt="" width="2794" height="1680" />

Below we have compiled a summarized chart comparing spindles and routers, assessing various features and criteria.

<img class="alignnone size-full wp-image-11541" src="https://resources.sienci.com/wp-content/uploads/2024/10/spindle-trim-router-comparison.png" alt="" width="905" height="879" />
<h4 style="text-align: center;">Spindle vs. Router Comparison Chart</h4>