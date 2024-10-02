---
title: Tools & Router
menu_order: 0
post_status: draft
post_excerpt: 
post_date: 2024-09-10 3:26
taxonomy:
    knowledgebase_cat: 
    knowledgebase_tag:        
custom_fields:
    KBName: 
    basepress_post_icon: bp-caret-right
skip_file: yes
featured_image: 
---

Improves on https://resources.sienci.com/view/lmk2-router-and-tools/

- Tool range for the CNC and how they’re generally used
- The bits required to make different projects
- Where you can source bits
- Typical bit geometry terms
- Need to insert all writing that Kelly did outlining how to use the Makita (maintenance)
- https://www.reddit.com/r/hobbycnc/comments/1ffiojs/is_a_larger_bit_better_for_cutting_profiles/
- Overlaps with "Cutting TOols" page, so ensure this one covers more quick-reference material for handbook understanding while the other covers mostly introductory/buying

**Kelly's Writing**
Basically the section would be along the lines of: "Here's how the Makita router works" and would consist of general points such as:

- speed control dial: what the speed range is of the router and what speeds the numbers on the dial correspond with. Also, what's the general dial setting that's a good default to work in most situations with most materials
- size range of bits that the router can take
- recommended cycle time of the router (how often we recommend it running for in a row, and how much of a break you should give it after running for a long time. You can reference the Makita manual for this if you like, you can find it online)
- How to install cutting tools into the router, using wrenches, tips on which way to turn the wrenches to tighten and loosen
- How to switch out the collet to use a different size, and how to use a collet adapter for smaller bits in a larger collet

The LongMill is designed for use with the Makita RT0701C, which can cut into soft plastics, soft metals, as well as soft and hardwoods. Its electronic speed control adjusts power under load to provide constant speed through materials.

This router comes with a 1/4″ collet and collet wrenches, as well as a detachable base for handheld use.

For more information about this model, see the manual here: https://cdn.makitatools.com/apps/cms/doc/prod/RT0/647d7eb3-3b81-48d3-b5c1-3ae0fe4e121d_RT0701C_IM.pdf

## Speed control dial

This router has a speed range between 10,000 to 30,000 RPM. This can be manually adjusted using the red dial on the top of the router. The dial can be set between 1-6. Below is the chart for the setting and the speed.

![](/_images/_experimental-writing/router-dial-settings.png)

For most applications, keeping the setting between 3-4 (around 20,000 RPM) should be sufficient. Cutting plastics and soft metals may require a lower RPM to reduce the chance of melting which will affect the surface quality of your material.

## Run time

There is no official run time or duty cycle specified by Makita. If the router feels too hot, the router should be turned off to cool down. It is not designed to run constantly therefore be mindful of how long you are running the machine for.

## Accepted tool sizes

This model comes with a ¼” collet which can directly fit bits with a ¼” shank diameter. However, you can also fit bits with a shank diameter between ⅛” to ⅜” if you use to proper collet or adapter. For example, you can fit a flat end mill with a ⅛” shank diameter by using a ⅛” collet for the Makita or by using a ¼” to ⅛” collet adapter.

[Picture: a collet adapter and a collet side by side]

Generally the flute diameter (the diameter of the cutting portion of your bit) will range between 1/16” to ¼”. [Picture: bits sized between 1/16” to ¼” in a row]

## Installing cutting tools/bits

1. To switch out a bit, first remove the current bit by using the two wrenches. One wrench will fit on the flats of the router shaft, and the other will fit on the collet nut. Push the wrenches away from you; this will release the bit, collet and nut. [Picture: two hands using the wrenches, a pushing motion, any orientation is OK but should see the nut, wrenches and hands clearly]  

2. a) If you are not using an adapter:
Place the collet into the nut, oriented so that the wider end of the collet is sitting in the nut. Grab the new bit and insert it into the collet and nut. The entire fluted length should be exposed and below the collet and nut. [Picture: hands holding a bit that is assembled with a ¼” collet and nut, front view to show how the collet is sitting in the nut, and how much fluted length is exposed]
   b) If you are using a collet adapter with the collet:
Orient the adapter so the slits are facing the same direction as those on the collet. Then, insert the adapter in to the collet, from the narrow end of the collet, minding the slit orientation. [Picture: collet adapter above a collet, slits are facing “down”] Insert the bit from the wide end of the collet [Picture: bit below a collet]. Once assembled, the bottom of the adapter should be flush with the wide end of the collet. The entire fluted length should be exposed and below the collet and nut. [Picture: assembled bit, collet adapter and collet]

3. Bring the assembled bit to the router, and tighten the nut with your hands to secure everything temporarily. You can use the red button to lock the router shaft in place. If the bit is falling out before you can tighten, use a block or your finger to hold it in place. [Picture: one hand is holding onto the red button, other hand is tightening the nut, a finger holding up the bit. Side view to show bit, button, nut and hands]

4. Use the two wrenches to secure the bit in place, with one wrench on the flat of the router shaft and the other on the nut. Bring the wrenches towards you. Only hand-tighten, you do not need a ton of force to secure the bit.  [Picture: two hands using the wrenches, try to show pulling inwards towards your body, any orientation is OK but should see the nut, wrenches and hands clearly]  

## Maintenance

To ensure your router is in good repair, you will need to clean out the router regularly and replace the carbon brushes when worn out.

### Cleaning

- To prevent bits from jamming up, use a bristle brush to remove sawdust trapped inside the router shaft
- Wipe down your tools, collet adapters and collets to remove debris

### Replacing carbon brushes

Please follow the official instructions from the Makita manual below:

![](/_images/_experimental-writing/router-replacing-brushes.png)

### What to do if your bit gets stuck?

Some options:

- Spray with penetrating oil at the base, wait for a few minutes for bit to release (remember to wipe off oil afterwards)
- While avoiding the bit itself, heat up the router shaft with a heat gun or hair dryer to cause expansion and have more expansion for the bit to fall out

---

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
