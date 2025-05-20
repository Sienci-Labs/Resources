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
skip_file: no
featured_image: _images/_lmk2/_the-basics/lmk2_dust_boot_adjustable.jpg
---

CNCs can create a lot of mess just like many other shop tools. Think about the chips and dust you can create drilling a single hole or cutting a piece of wood in half and then stretch that out over hours of constant cutting on a CNC machine. Not only can this add up to a very large mess, but it's also [not good for your health](#safety) to breathe it in long-term, or the health of the CNC since important parts can get gummed up with dust over time.

This is where a 'dust collection' system can help you out. Most CNC dust collection systems mirror what you'd normally see connected to other common tools in a woodworkers shop. Starting at the cutting head you have a:

1. **[Dust Shoe](#dust-shoes)** which tries to contain the dust where the cutting is happening
1. **[Hose](#hose-size)** that the dust can flow along
1. Some type of **[Vacuum System](#choosing-a-vacuum-or-dust-collector)** that creates the suction to carry the dust away from the dust shoe

![](/_images/_lmmk2/_the-basics/lmk2_dust_123.jpg)

There are also some other solutions that won't be covered on this page that can help with dust management like building an [enclosure for your CNC](https://resources.sienci.com/view/lmk2-table-enclosure/#machine-enclosure) or running it in an open-air environment. Ideally these should still be used alongside a dust collection setup, but cutting in open-air can be fine short-term to reduce setup complexity and learning curve, and using an enclosure can sometimes help keep cutting noise down.

### Safety

Being in an environment where you are exposed to high amounts of aerosolized sawdust isn't good for you, and can cause a chronic cough, chest pain, runny nose, headaches, bronchitis and more. The worst for your health is the fine particle that can't be seen by the naked eye. In the woodworking hobby, dust is classified into categories—L (low-risk), M (medium-risk), and H (high-risk)—based on the type of material and associated health risks.

![](/_images/_lmmk2/_the-basics/lmk2_dust_safety_face.jpg){.aligncenter .size-medium}

- L-Class (Low Risk) – Minimal health risk but requires basic dust control.

  - Softwoods (pine, cedar) – Respiratory irritants but low toxicity.
  - Plastics – Sanding dust can cause irritation but is generally low risk.
- M-Class (Medium Risk) – Higher respiratory hazards; requires enhanced filtration.

  - Hardwoods (oak, beech) – Fine dust can trigger allergies and long-term issues.
  - Plywood/MDF – Releases formaldehyde and chemicals when cut or sanded.
  - Painted/coated surfaces – May contain toxic compounds like lead. *Use caution when surfacing an old painted piece of wood for example*

- H-Class (High Risk) – Carcinogenic/toxic materials; requires specialized protection.

  - Asbestos – Extremely hazardous; causes lung diseases.
  - Silica dust (from concrete, tile, stone) – Leads to silicosis if inhaled. *Be careful carving an old tile for example*

 You can protect yourself on 3 basic levels.

 **Level One - Prevent dust from entering your body.** Your nose and mouth should be covered with a *high quality dust mask* or respirator with a minimum rating of N95.

 **Level Two - Grab the dust at it's source.** Your project should have a *good dust collection system*, to remove as much dust at the source as possible, before the particles have the chance to become airborne. This type of protection 'collects' the dust at the source.

 **Level Three - Clean the air** Your workshop can add more protection against those fine particles by using a *dust extraction system* to catch any particles your dust collector misses. This type of protection 'extracts' fine dust particles from the air in your shop.

 Regularly cleaning work surfaces, machines, and the floor will help minimize any dust that could be kicked up by new projects.
  Working with a door open or an exhaust fan in a well ventilated area is also a great way to reduce your exposure to hazardous fine sawdust materials.

  ***Note: Don't mix metal shavings with wood dust as it can cause a fire hazard and ruin your hose***

## Dust Shoes

We've covered safety, so let's dive into the 3 main parts that make up your dust collection system, starting at the CNC with your dust shoe!

A **dust shoe** is basically a fancy vacuum attachment for your CNC machine, it stays near the cutter to stop chips and fine dust from flying away while the **vacuum system** pulls it all away. This is good for you because it:

- can give you cleaner cuts with the debris out of the way
- reduces maintenance since dirt build-up can cause premature wear on many CNCs
- saves you time cleaning up that you'd have to do anyway
- keeps your shop air cleaner which is safer for your lungs

https://www.youtube.com/watch?v=94r4hgr2SgA

### Fixed vs. Adjustable Dust Shoes

The design of your dust shoe can greatly affect how well it collects dust for you particular application. There are hundreds of different designs for dust shoes, however, one of the largest differentiators is whether it is fixed or adjustable. These two styles are also sometimes referred to as Z-axis dependent / bound / tethered vs. Z-axis independent / unbound / free.

Whether a dust shoe is fixed or adjustable depends on how it’s mounted:

- A fixed-style dust shoe is mounted to the Z-axis or the router body on the CNC. This means that when the Z-axis moves up or down during cutting the dust shoe moves up and down with it.

![](/_images/_lmmk2/_the-basics/lmk2_dust_boot_fixed.jpg "Source - https://community.carbide3d.com/t/hall-of-dust-shoes/7717/20?page=2, https://maniacallabs.com/2019/02/25/CNC-dust-boot-for-dewalt-router/"){.aligncenter .size-medium}

- An adjustable-style dust shoe is typically mounted to the X-axis of the CNC. This means that it never moves unless you change it's height, allowing the Z-axis to raise and plunge during cutting while the dust shoe stays in the spot you set it. It can be secured with a couple bolts as in the left image, or held in place with strong magnets for quick and easy adjustments as shown in the right image below.

![](/_images/_lmmk2/_the-basics/lmk2_dust_boot_adjustable.jpg "Source - https://www.nymolabs.com/products/CNC-dust-shoe-only-for-nbs-6040-nbx-5040"){.aligncenter .size-medium}

For general purpose cutting, we recommend using an adjustable dust shoe as it is significantly better at collecting dust and debris, and relies less on how powerful your vacuum system is. It's also much better suited toward flat or sheet material which is the type of material that's most commonly used by hobby CNC users for sign-making and v-carving.

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

| **Build Name**                                   | **Description**                                              | **Link**                                                                                           |
|--------------------------------------------------|--------------------------------------------------------------|----------------------------------------------------------------------------------------------------|
| Articulating Dust Shoe                          | User-created articulating dust shoe design                   | [Forum Discussion](https://forum.sienci.com/t/a-new-kind-of-articulating-dust-shoe/1681)         |
| 3D Printable Automatic Dust Shoe (Stepper Motor) | 3D printable dust shoe driven by a stepper motor             | [Forum Discussion](https://forum.sienci.com/t/making-a-mostly-3d-printable-automatic-dust-shoe-that-is-driven-by-a-stepper-motor/13349) |
| AutoDustBoot Version 2.0                        | An improved automatic dust boot solution                    | [YouTube Video](https://youtu.be/1Jvo0tx4MSM)                                                     |

## Hose Size

Your shop vac or dust collector will come with a hose of a certain diameter. Your system will work most optimally if you use hoses that are similar in diameter.

CFM (cubic feet per minute) denotes the amount of air your vacuum can pass through. The higher the CFM, the more volume of material you can move. You will want a higher CFM rating if you are cutting a large amount of material.

Suction power (sometimes called Water Lift, Static Lift, Static Pressure…) indicates how fast the air is moving through the system. The higher your suction is, the harder the dust is pulled through your dust shoe and hose. You will typically want a higher suction vacuum if you are cutting heavier materials like metals, need to draw chips out of narrow cuts, or are using a fixed-style dust shoe.

Dust collectors for example typically have higher CFMs but lower suction power, thus better suited with larger diameter hoses. Using a smaller diameter hose can constrict airflow and reduce its efficiency.

Shop-Vacs, on the other hand, have smaller CFMs but higher suction power. These types of vacuums are happy with using smaller diameter hoses.

Depending on the design of your dust shoe, you may need to adapt your hose to match. You can find adapters that can help switch between hose diameters. You may also want to opt for a hose that will keep static buildup along it's length to a minimum in which case more specialized options exist such as the [36mm antistatic hose from Festool](https://www.festoolcanada.com/accessories/dust-extraction/suction-hoses-and-cleaning-accessories/suction-hoses/204923---d3632x3,5m-asr).

### Hanging Your Hose

It's important to have the dust collection hose hang above the dust shoe, so that it doesn't put any pressure on the router, or get caught up in your work. You can simply hang it from the ceiling or use a more advanced solution like an articulating arm. Make your own, or [grab one from Etsy!](https://www.etsy.com/ca/listing/736098852/vacuum-hose-boom-for-small-medium-and)

![](/_images/_lmmk2/_the-basics/lmk2_dust_arms.jpg "Source - https://forum.avidCNC.com/t/one-dust-collection-solution/1400"){.aligncenter .size-medium}

| **Title**                        | **Duration** | **Link**                          |
|----------------------------------|--------------|------------------------------------|
| Easy CNC Swing Arm               | 3 min        | [Link](https://youtu.be/RwYulYI8uRw) |
| Custom Dust Collection Swing Arm | 18 min       | [Link](https://youtu.be/KufOYrTFBPA) |

## Choosing a Vacuum or Dust collector

Your dust shoe and hose will need a source of suction. Most times an existing dust collector or Shop-Vac with a [cyclone separator](#adding-a-cyclone-to-your-shop-vac) will be able to fit the bill since these systems are set up to run for many hours and provide reasonable suction. Depending on the dust shoe used and the hosing size you use for your shop, you may want to look at your system’s CFM and suction lift specifications depending on your needs.

![](/_images/_lmmk2/_the-basics/lmk2_dust_safety_collect.jpg "A dust separator with cyclone vs dual bag dust collector"){.aligncenter .size-medium}

### 1. Shop Vac

A **shop vac** is a versatile, high-suction device primarily designed to pick up larger particles, such as wood chips, sawdust, and even liquid spills. It is the most common type of dust collection used in the hobby CNC space. With many affordable options available at many large box stores, you can get setup and running right away with a shop vac. You can move it around the CNC or build a dedicated space for it.

| **Model**              | **Description**                                    | **Link**                                  |
|-------------------------|----------------------------------------------------|-------------------------------------------|
| WEN VC9209             | 10-Amp 9.25-Gallon 6.5 Peak HP Wet/Dry Shop Vacuum | [Link](https://wenproducts.com/collections/dust-management/products/wen-vc9209-10-amp-9-25-gallon-6-5-peak-hp-wet-dry-shop-vacuum-and-blower-with-0-3-micron-hepa-filter-hose-and-accessories) |
| Uline Wet/Dry Vacuum   | 10 Gallon, Stainless Steel                          | [Link](https://www.uline.ca/Product/Detail/H-8931/Wet-Dry-Vacuums/DeWalt-Wet-Dry-Vacuum-10-Gallon-Stainless-Steel) |
| Rigid Wet/Dry Vacuum   | 10 Gallon, 6HP                                      | [Link](https://www.homedepot.ca/product/ridgid-375l-10-gal-60-peak-hp-stainless-steel-wet-dry-shop-vacuum-with-filter-hose-and-accessories/1001063385) |
| Vacmaster Professional | 8 Gallon, Hepa Filter                               | [Link](https://vacmaster.com/wet-dry-vacuums/vacmaster-pro/8-gallon-11amp-hepa-vacuum/) |
| Hercules | 12 Gallon, Dual Hepa Filter, Noise adjustable                               | [Link](https://www.harborfreight.com/power-tools/vacuums-blowers/dust-collectors/12-gallon-osha-compliant-dust-extractor-58966.html) |

### 2. Dust Collector

A **dust collector** is designed to capture large volumes of dust and wood chips from large CNCs & woodworking tools, particularly those that generate large amounts of debris. It is a more powerful and specialized system compared to a shop vac. It is often stationary and often runs to more than one tool.

| **Model**              | **Description**                                              | **Link**                                                                                               |
|-------------------------|--------------------------------------------------------------|--------------------------------------------------------------------------------------------------------|
| POWERTEC              | 1 HP Dust Collector with 1 Micron Dust Collector Bags         | [Link](https://www.amazon.com/dp/B0CV3HJXRR/ref=cm_sw_r_cp_apan_glt_fabc_57VH7EJ6PTNK7ZXSE27F?th=1)   |
| WEN                    | 5.7 AMP 660 CFM Rolling Dust Collector                        | [Link](https://wenproducts.com/collections/dust-management/products/wen-dc3401-57-amp-660-cfm-rolling-dust-collector-with-12-gallon-bag-and-optional-wall-mount) |
| Grizzly G0944          | 1-1/2 HP Wall-Mount Dust Collector with Canister Filter       | [Link](https://www.grizzly.com/products/grizzly-1-1-2-hp-wall-mount-dust-collector-with-canister-filter/g0944) |
| Grizzly G0548ZP        | 2 HP Canister Dust Collector w/Aluminum Impeller              | [Link](https://www.grizzly.com/products/grizzly-2-hp-canister-dust-collector-w-aluminum-impeller/g0548zp) |

### Choosing the Right Tool

- **Use a Shop Vac** if you need portability and versatility for general cleanup or larger wood particles and debris. Most people start here as it is most economical and simple to setup and get going.
- **Choose a Dust Collector** if you have a dedicated woodworking shop with stationary tools and need continuous dust collection. If you are already a woodworker and have a shop, you may already have one of these.

### Features Comparison

| **Feature**           | **Shop Vac**                                              | **Vacuum w/ Cyclone Attachment**                             | **Dust Extractor**                                   |
|-----------------------|-----------------------------------------------------------|---------------------------------------------------------------|-------------------------------------------------------|
| **Best For**          | Small to medium CNCs, shorter jobs, spot cleaning, larger debris                              | Capturing large volumes of dust and debris before it reaches the filter | Large CNCs, long/large jobs, fine hazardous dust from sanding        |
| **Suction Power**     | High suction, lower airflow                               | Moderate to high suction, depending on base vacuum            | Moderate suction and airflow                          |
| **Filtration**        | Basic or HEPA; limited fine dust capture                  | Improved dust separation; filters last longer                 | HEPA filtration for very fine dust                    |
| **Airflow (CFM)**     | 100-200 CFM                                               | 100-400 CFM (based on vacuum used)                            | 400-1000 CFM                                          |
| **Portability**       | Portable                                                  | Fixed or portable; may require more space                              | Often fixed, tool-compatible                          |

Each of these tools has its strengths, costs, size and power requirements. Often woodworkers start with a simple shop vac and build up to a combination of shop vac & cyclone or a dust collector system. Add in a dust extractor to your shop, and you've created an optimal setup for a safer, cleaner workshop.

### User Setups

You can customize your shop to have a simple shop vac with hose hanging above your CNC, upgrade to a 2 stage system and add a cyclone, or build a cart for portability. Upgrade further to a wall mounted dust collection system, and run it to each tool in your shop. You can even add blast gates to your system, activated manually or automatically!

| Video Title                                   | Duration | Link                                           |
|-----------------------------------------------|----------|------------------------------------------------|
| Dust Collection for Beginners                 | 10 min   | [Watch Here](https://youtu.be/-g3GqsNJ60U)     |
| Attic Based & Voice Activated System          | 15 min   | [Watch Here](https://youtu.be/6swtBtcTGwY)     |
| Wall Mounted Dust Collector Setup             | 6 min    | [Watch Here](https://youtu.be/jRuLmnQymXg)     |
| Cart for Shop Vac and Cyclone                 | 2 min    | [Watch Here](https://youtu.be/nnVQyKaR9Cg)     |
| Upgrade from Shop Vac to Dust Collection      | 4 min    | [Watch Here](https://youtu.be/WHnnJmsoz_Q)     |
| Advanced Setup with Blast Gates for Each Tool | 11 min   | [Watch Here](https://youtu.be/SkIFPjJOQNU)     |
| Pairing the best Dust Collector with a CNC    | 13 min   | [Watch Here](https://www.youtube.com/watch)    |
| 5 tips to improve CNC dust collection DIY     | 6 min    | [Watch Here](https://youtu.be/-hKEXZNbGsg) |

#### Adding a Cyclone to your shop vac

Adding a second stage to your dust collection strategy can drastically reduce the amount of filters your shop vac or dust collection system uses. Often called a cyclone, it works by using centrifugal force to separate dust and debris from the air. When dust-laden air enters the cyclone chamber, it is spun rapidly in a vortex. The heavier particles are flung outward against the chamber walls, where they lose momentum and fall into a collection bin below. Meanwhile, the lighter, cleaner air is directed upwards and exits through the top outlet, often passing through a secondary filter for finer particles. This process improves efficiency, reduces filter clogging, and extends the lifespan of the dust collection system.

Many user will make their own, or you can purchase a pre-made one. [Here](https://www.leevalley.com/en-ca/shop/tools/workshop/dust-collection/dust-extractors/116856-dust-deputy-low-pro-deluxe) is a neat low profile cyclone!

![](/_images/_lmmk2/_the-basics/lmk2_dust_cyclones.jpg){.aligncenter .size-medium}

| Video Title                               | Duration | Link                                           |
|-------------------------------------------|----------|------------------------------------------------|
| How do Cyclone Dust Separators Work?      | 5 min    | [Watch Here](https://youtu.be/3fB_uH5k6RQ)     |
| Adding a Dust Separator to a Shop Vac     | 12 min   | [Watch Here](https://youtu.be/jRuLmnQymXg)     |
| Dust Cyclone Separator Cart               | 15 min   | [Watch Here](https://youtu.be/lGnGNYrxqjs)     |

#### Adding a Dust Extractor to your shop

A **dust extractor** is a specialized type of vacuum designed to capture fine, hazardous dust, often with more precise filtration systems than typical shop vacs. Dust extractors are especially useful for capturing finer particles, such as those from sanding or cutting engineered woods, concrete, or other materials that release smaller, respirable dust. *A dust extraction system is used in your shop, not on your CNC.*

![](/_images/_lmmk2/_the-basics/lmk2_dust_safety_extract.jpg){.aligncenter .size-medium}

- **Power and Filtration**: Dust extractors typically come with HEPA filtration or very fine filters capable of capturing particles as small as 0.3 microns, which is essential for protecting respiratory health.
- **Airflow (CFM)**: Dust extractors usually have moderate CFM, around 100-200, similar to shop vacs, but the focus is on high-quality filtration rather than raw suction power. Many models also have automatic filter-cleaning features.
- **Portability**: They are generally portable and compact, making them easy to connect directly to handheld tools (like sanders or circular saws) for on-tool dust collection.
- **Best Use**: Dust extractors are best suited for capturing fine dust particles from sanding, concrete grinding, or other tasks that create hazardous, respirable dust.

| **Model**      | **Description**                                                       | **Link**                                                                                                  |
|-----------------|-----------------------------------------------------------------------|-----------------------------------------------------------------------------------------------------------|
| WEN AF1270     | 4.2-Amp 3-Speed Remote-Controlled Industrial-Strength Air Filtration System | [Link](https://wenproducts.com/collections/dust-management/products/wen-af1270-4-2-amp-3-speed-remote-controlled-industrial-strength-air-filtration-system-750-950-1270-cfm) |
| Fein 9-20-27   | Turbo Vacuum, 5.8 Gallon, HEPA filter                                 | [Link](https://www.amazon.ca/dp/B00K69ILFQ/ref=asc_df_B00K74N8RQ&mcid=6207cf8f1eaa34e0ba6f2390c8adf5ea)   |

### Sawdust Recycling

Sawdust from a woodworking shop has a surprising number of useful applications. Mix with wax for a camping fire starter or mix with wood glue to make art. Mulch your flower beds or make a bed for your livestock. What ever you do, don't throw it all away!

- **Wood Filler**: Combine sawdust with wood glue to fill in gaps or cracks in woodworking projects. You can often match the colour of the project if you use sawdust from that project.
- **Absorbent Material**: Sawdust soaks up spills well, making it useful for cleaning up oil or paint spills.
- **Mulch**: Sawdust can be spread around plants to retain moisture and suppress weeds. Just be cautious with hardwood sawdust, as it can deplete nitrogen from the soil.
- **Compost**: Mix sawdust with other organic matter to create a rich compost. Be mindful of the wood type; avoid sawdust from treated wood.
- **Pathways**: It creates a soft, natural-looking walkway and prevents muddy paths in gardens.
- **Animal Bedding**: Use sawdust as bedding for small animals, chickens, or livestock. Be careful with aromatic woods like cedar, which might irritate some animals.
- **Wood Stain**: Darker sawdust can be boiled in water to create a natural stain.
- **Molded Wood Projects**: Mixing sawdust with resin or glue can create a wood-based composite for small molded items.
- **Fire Starters**: Mix sawdust with wax to create fire starters, or simply use small piles of sawdust on kindling. Great to take camping!
- **Pathways for Erosion Control**: Spread on slopes or muddy areas to reduce erosion.
- **Ice Melt Substitute**: In winter, use sawdust on sidewalks or driveways for traction instead of salt. Good idea Eh!?

Collect different types of wood sawdust to match your projects, or make a new project with your freshly made sawdust. If you do want to throw it all out, the last short video is a great way to make smaller bags.

[su_table responsive="yes"]

| **Title**                             | **Description**                                                                                             | **Length** | **Video Link**                                   |
|---------------------------------------|-------------------------------------------------------------------------------------------------------------|------------|--------------------------------------------------|
| **Save Sawdust in Tins for Glue**     | Collect and store different types of sawdust in separate tins. Mix with glue to use for repairs in woodworking projects. | Short      | [Watch Video](https://youtube.com/shorts/B3DerwmNEaI) |
| **Reuse Sawdust for Art**             | Repurpose sawdust in art projects, adding unique textures or effects to artwork.                             | Short      | [Watch Video](https://youtube.com/shorts/KCMPF9GwKro) |
| **41 Creative Uses of Sawdust**       | Amazing ideas for using sawdust around the homestead and garden, from composting to fire starters.          | 5 min      | [Watch Video](https://youtu.be/V8CRrCH_eZw)      |
| **Sawdust Flowerpot Project**         | Turn scrap sawdust into a project to sell by creating a flowerpot.                                          | 12 min     | [Watch Video](https://youtu.be/u52tGEYJL08)      |
| **Clear Your Lungs After Inhaling Dust** | Understanding effective methods to clear your lungs after inhaling dust is crucial for maintaining respiratory health | 9 min      | [Watch Video](https://youtu.be/fmLqbzLz4-A) |
| **Compact Sawdust Bags**              | Compress sawdust bags to make them more compact, saving space and making them easier to store or dispose of. | Short      | [Watch Video](https://youtube.com/shorts/QOYwWEAp1P0) |

[/su_table]

Congrats! You are now all up to speed on types of dust collection systems available to the hobby CNC market, how to put them to use and even how to use all that sawdust you will be creating. Be safe, be healthy & have fun!!
