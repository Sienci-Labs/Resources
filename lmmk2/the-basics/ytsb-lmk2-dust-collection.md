---
title: ytsb Dust Collection
menu_order: 7
post_status: draft
post_excerpt: Dust shoe, vacuum collection, and hose size considerations for the LongMill CNC. Pros and cons of Z-independent and dependent dust shoes discussed.
post_date: 2022-03-17 19:47:00
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

CNCs can create a lot of mess just like many other cutting tools. Think about the chips and fine dust you get drilling a single hole or cutting a piece of wood in half and then stretch that out over hours of constant cutting. This is where dust collection helps out.

A **dust shoe** is basically a fancy vacuum attachment for your CNC machine, it stays near the cutter to stop chips and fine dust from flying away while the **vacuum system** pulls it all away. This is good for you because it:

- can give you cleaner cuts with the debris out of the way
- reduces maintenance since dirt build-up can cause premature wear on many CNCs
- saves you time cleaning up that you'd have to do anyway
- keeps your shop air cleaner which is safer for your lungs

https://www.youtube.com/watch?v=94r4hgr2SgA

That said, dust management can still come in other forms like building an [enclosure for your CNC](https://resources.sienci.com/view/lmk2-table-enclosure/#machine-enclosure) or cutting outside. You might choose to do these if you:

- are worried about the noise from running a vacuum or dust collector (though the noise of cutting can get similarly loud)
- don't want to deal with the dust shoe colliding with clamps, material, or getting in the way during tool changes

### Fixed vs. Adjustable Dust Shoes

The design of your dust shoe can greatly affect how well it collects dust for you particular application. There are hundreds of different designs for dust shoes, however, one of the largest differentiators is whether it is fixed or adjustable. These two styles are also sometimes referred to as Z-axis dependent / bound / tethered vs. Z-axis independent / unbound / free.

Whether a dust shoe is fixed or adjustable depends on how it’s mounted:

- A fixed-style dust shoe is mounted to the Z-axis or the router body on the CNC. This means that when the Z-axis moves up or down during cutting the dust shoe moves up and down with it.
- An adjustable-style dust shoe is typically mounted to the X-axis of the CNC. This means that it never moves unless you change it's height, allowing the Z-axis to raise and plunge during cutting while the dust shoe stays in the spot you set it.

[su_table responsive="yes"]
<table>
<tbody>
<tr>
<td></td>
<td><b>Fixed</b></td>
<td><b>Adjustable</b></td>
</tr>
<tr>
<td style="background: #44bc72 !important;">Pros</td>
<td>
<ul>
  <li>Typically a much simpler design</li>
  <li>Little adjustment required, usually set it and forget it</li>
</ul>
</td>
<td>
<ul>
  <li>Much more efficient at collecting dust, keeping good contact between flat material and the shoe</li>
  <li>Consistent performance regardless of how deep your cut is</li>
</ul>
</td>
</tr>
<tr>
<td style="background: #ff4554 !important;">Cons</td>
<td>
<ul>
  <li>Not efficient at collecting dust, typically relies on the vacuum’s suction power to overcome escape gaps</li>
  <li>Dust shoe can collide with the material on deeper cuts</li>
</ul>
</td>
<td>
<ul>
  <li>Typically a more complicated design</li>
  <li>Requires adjustment based on your material’s thickness</li>
  <li>Router can collide with the dust shoe on deeper cuts</li>
</ul>
</td>
</tr>
</tbody>
</table>
[/su_table]

For general purpose cutting, we'd recommend using an adjustable dust shoe as it is significantly better at collecting dust and debris, and relies less on how powerful your vacuum system is. It's also much better suited toward flat or sheet material which is the type of material that's most commonly used by hobby CNCers for sign-making and v-carving.

### Choosing Hose Size

Your vacuum or dust collector will probably come with a hose of a certain diameter. Your system will probably work most optimally if you use hoses that are similar in diameter.

Dust collectors for example typically have higher CFMs but lower suction, thus better suited with larger diameter hoses. Using a smaller diameter hose can constrict airflow and reduce its efficiency.

Shop-Vacs, on the other hand, have smaller CFMs but higher suction power. These types of vacuums are happy with using smaller diameter hoses.

Depending on the design of your dust shoe, you may need to adapt your hose to match. You can find adapters that can help switch between hose diameters. You may also want to opt for a hose that will keep static buildup along it's length to a minimum in which case more specialized options exist such as the 36mm antistatic hose from Festool.

### Choosing a Dust collector / Vacuum

Your dust shoe will need a source of suction. Most times an existing dust collector or Shop-Vac with a cyclone separator will be able to fit the bill since these systems are set up to run for many hours and provide reasonable suction. Depending on the dust shoe used and the hosing size you use for your shop, you may want to look at your system’s CFM and suction lift specifications depending on your needs.

CFM (cubic feet per minute) denotes the amount of air your vacuum can pass through. The higher the CFM, the more volume of material you can move. You will want a higher CFM rating if you are cutting a large amount of material.

Suction power (sometimes called Water Lift, Static Lift, Static Pressure…) indicates how fast the air is moving through the system. The higher your suction is, the harder the dust is pulled through your dust shoe and hose. You will typically want a higher suction vacuum if you are cutting heavier materials like metals, need to draw chips out of narrow cuts, or are using a fixed-style dust shoe.
