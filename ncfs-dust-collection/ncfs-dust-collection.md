---
title: Dust Collection
menu_order: 0
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

Improves on https://resources.sienci.com/view/lmk2-dust-collection/

- Refined discussion on dust shoes, pros/cons, what to choose
- Discuss more about setup and options for vacuums and dust collectors, talk about their pros/cons, and make purchase suggestions
- Tends to be needed for lung protection and keep the workspace clean while cutting but it can be accomplished with smaller shop vacs, larger dust collectors, or sometimes even just an enclosure that you vacuum up later
- How to use all the sawdust you collect?
- Oneida has a new low-profile cyclone to fit to a bucket

https://forum.sienci.com/t/dust-questions-for-newbie/14028/5

Clean/Maintain your shop vac  https://www.familyhandyman.com/list/cleaning-and-maintaining-your-shop-vac/

---

CNCs can create a lot of mess just like many other cutting tools. Think about the chips and fine dust you get drilling a single hole or cutting a piece of wood in half and then stretch that out over hours of constant cutting on a cnc machine. This is where dust collection helps out. Most woodworkers will setup a dust collection system that can quickly connect to whatever tool or machine they are using at the time. Adding an air filter to the shop, can help to catch and trap the fine sawdust.

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

For general purpose cutting, we recommend using an adjustable dust shoe as it is significantly better at collecting dust and debris, and relies less on how powerful your vacuum system is. It's also much better suited toward flat or sheet material which is the type of material that's most commonly used by hobby CNCers for sign-making and v-carving.

https://forum.sienci.com/t/a-new-kind-of-articulating-dust-shoe/1681

https://forum.sienci.com/t/making-a-mostly-3d-printable-automatic-dust-shoe-that-is-driven-by-a-stepper-motor/13349

### Choosing a Vacuum  / Dust collector / Dust Extractor

Your dust shoe will need a source of suction. Most times an existing dust collector or Shop-Vac with a cyclone separator will be able to fit the bill since these systems are set up to run for many hours and provide reasonable suction. Depending on the dust shoe used and the hosing size you use for your shop, you may want to look at your system’s CFM and suction lift specifications depending on your needs.

CFM (cubic feet per minute) denotes the amount of air your vacuum can pass through. The higher the CFM, the more volume of material you can move. You will want a higher CFM rating if you are cutting a large amount of material.

Suction power (sometimes called Water Lift, Static Lift, Static Pressure…) indicates how fast the air is moving through the system. The higher your suction is, the harder the dust is pulled through your dust shoe and hose. You will typically want a higher suction vacuum if you are cutting heavier materials like metals, need to draw chips out of narrow cuts, or are using a fixed-style dust shoe.

### Choosing Hose Size

Your vacuum or dust collector will probably come with a hose of a certain diameter. Your system will probably work most optimally if you use hoses that are similar in diameter.

Dust collectors for example typically have higher CFMs but lower suction, thus better suited with larger diameter hoses. Using a smaller diameter hose can constrict airflow and reduce its efficiency.

Shop-Vacs, on the other hand, have smaller CFMs but higher suction power. These types of vacuums are happy with using smaller diameter hoses.

Depending on the design of your dust shoe, you may need to adapt your hose to match. You can find adapters that can help switch between hose diameters. You may also want to opt for a hose that will keep static buildup along it's length to a minimum in which case more specialized options exist such as the 36mm antistatic hose from Festool.

### Hanging Your Hose

Easy CNC Swing Arm: 3 min: https://youtu.be/RwYulYI8uRw
Custom Dust Collection Swing Arm: 18 min:  https://youtu.be/KufOYrTFBPA

### Adding a Cyclone

Adding a second stage to your dust collection strategy can drastically reduce the amount of filters your shop vac or dust collection system uses.

How do Cyclone dust separators work?:  5 min:  https://youtu.be/3fB_uH5k6RQ
Adding a Dust Separator to a shop vac:  12 min:  https://youtu.be/jRuLmnQymXg
Dust Cyclone Separator Cart:  15 min:  https://youtu.be/lGnGNYrxqjs

### User Setups

You can customize your shop to have a simple shop vac with hose hanging above your cnc, upgrade to a 2 stage system and add a cyclone, or build a cart for portability. Upgrade further to a wall mounted dust collection system, and run it to each tool in your shop. You can even add blast gates to your system, activated manually or automatically!

Dust collection for Beginners:  10 min:  https://youtu.be/-g3GqsNJ60U

Attic Based & Voice Activated System: 15 min: https://youtu.be/6swtBtcTGwY

Wall mounted Dust Collector Setup:  6 min:  https://youtu.be/jRuLmnQymXg

Cart for shop vac and cyclone:  2 min:  https://youtu.be/nnVQyKaR9Cg

Upgrade from shop vac to dust collection:  4 min:  https://youtu.be/WHnnJmsoz_Q

Advanced setup with blast gates for each tool:  11 min:  https://youtu.be/SkIFPjJOQNU

### Sawdust Safety



### Sawdust Recycling

Sawdust from a woodworking shop has a surprising number of useful applications. Mix with wax for a camping fire starter or mix with wood glue to make art. Mulch your flower beds or make a bed for your livestock. What ever you do, don't throw it all away!

**Workshop Uses**

- **Wood Filler**: Combine sawdust with wood glue to fill in gaps or cracks in woodworking projects. You can often match the colour of the project if you use sawdust from that project.
- **Absorbent Material**: Sawdust soaks up spills well, making it useful for cleaning up oil or paint spills.

**Gardening and Landscaping**

- **Mulch**: Sawdust can be spread around plants to retain moisture and suppress weeds. Just be cautious with hardwood sawdust, as it can deplete nitrogen from the soil.
- **Compost**: Mix sawdust with other organic matter to create a rich compost. Be mindful of the wood type; avoid sawdust from treated wood.
- **Pathways**: It creates a soft, natural-looking walkway and prevents muddy paths in gardens.

**Pet and Livestock Care**

- **Animal Bedding**: Use sawdust as bedding for small animals, chickens, or livestock. Be careful with aromatic woods like cedar, which might irritate some animals.

**Crafts and DIY Projects**

- **Wood Stain**: Darker sawdust can be boiled in water to create a natural stain.
- **Molded Wood Projects**: Mixing sawdust with resin or glue can create a wood-based composite for small molded items.

**Environmental Uses**

- **Fire Starters**: Mix sawdust with wax to create fire starters, or simply use small piles of sawdust on kindling. Great to take camping!
- **Pathways for Erosion Control**: Spread on slopes or muddy areas to reduce erosion.
- **Ice Melt Substitute**: In winter, use sawdust on sidewalks or driveways for traction instead of salt. Good idea Eh!?

#### Video Tips

Collect different types of wood sawdust to match your projects, or make a new project with your freshly made sawdust. If you do want to throw it all out, the last short video is a great way to make smaller bags.

[su_table responsive="yes"]

| **Title**                             | **Description**                                                                                             | **Length** | **Video Link**                                   |
|---------------------------------------|-------------------------------------------------------------------------------------------------------------|------------|--------------------------------------------------|
| **Save Sawdust in Tins for Glue**     | Collect and store different types of sawdust in separate tins. Mix with glue to use for repairs in woodworking projects. | Short      | [Watch Video](https://youtube.com/shorts/B3DerwmNEaI) |
| **Reuse Sawdust for Art**             | Repurpose sawdust in art projects, adding unique textures or effects to artwork.                             | Short      | [Watch Video](https://youtube.com/shorts/KCMPF9GwKro) |
| **41 Creative Uses of Sawdust**       | Amazing ideas for using sawdust around the homestead and garden, from composting to fire starters.          | 5 min      | [Watch Video](https://youtu.be/V8CRrCH_eZw)      |
| **Sawdust Flowerpot Project**         | Turn scrap sawdust into a project to sell by creating a flowerpot.                                          | 12 min     | [Watch Video](https://youtu.be/u52tGEYJL08)      |
| **Compact Sawdust Bags**              | Compress sawdust bags to make them more compact, saving space and making them easier to store or dispose of. | Short      | [Watch Video](https://youtube.com/shorts/QOYwWEAp1P0) |

[/su_table]