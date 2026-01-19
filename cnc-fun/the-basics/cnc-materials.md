---
title: Materials
menu_order: 6
post_status: publish
post_excerpt: Resources and documentation for general CNC work. You will find info about routers, software, end mills, add ons, and more  - everything you need to get started.
post_date: 2026-01-14 16:23:12
taxonomy:
    knowledgebase_cat: the-basics
    knowledgebase_tag:
        - cnc fundamentals
custom_fields:
    KBName: Fundamentals
    basepress_post_icon: bp-caret-right
skip_file: no
featured_image: _images/_cnc-fun/_the-basics/cnc_ba_materials_p1-guitar.jpg
---

CNC machines open up a world of possibilities, allowing you to cut and shape a wide range of materials with precision and creativity. Let's explore the most common materials used in hobby CNC projects, from woods and plastics to soft metals, but don’t let this list limit your imagination! With the right precautions and a spirit of experimentation, you might be surprised by what you can create. With that being said, some materials are not recommended for hobby CNC use, including concrete, steel, and other extremely hard or abrasive materials that could damage your machine or pose safety risks.

You are encouraged to review the [Safety](https://resources.sienci.com/view/cnc-safety/) section if you haven't checked it out already!

## Feeds & Speeds

When you start working with a CNC machine, understanding feeds and speeds is key to getting clean, efficient cuts. In simple terms, “feeds and speeds” describes how fast your machine moves and how aggressively it removes material. These terms will help you understand the charts used below for each different material.

- **Feed rate & plunge rate** - how quickly the machine moves across & into the material
- **Spindle or router speed** (RPM) - how fast the cutting tool spins
- **Stepover & stepdown** - how much material the tool removes with each pass

Knowing these variables - and how they interact with different materials - helps you get the best results while keeping your tools, your workpiece, and yourself safe.

## Wood

Wood is simply an amazing material. As it is a living, organic material, there are an infinite variety of woods and characteristics. We will talk a little about using wood with your CNC machine here.

![](/_images/_cnc-fun/_the-basics/cnc_ba_materials_p1-guitar.jpg){.aligncenter .size-medium}

General recommended starting feeds and speeds for 1/8" and 1/4" 2-flute end mills.
Start with these settings and adjust as needed—these are guidelines, not hard rules.

General recommended starting feeds and speeds for <a href="https://sienci.com/product/1-8-flat-upcut-end-mill_3pcs_or10pcs/" target="_blank" rel="noopener">1/8" 2 flute flat end mills</a>. Start with these settings and adjust as needed - these are guidelines, not hard rules:

<table class="wp-table" width="70%">
<tbody>
<tr>
<td><b>Material</b></td>
<td><b>Feed Rate (mm/ min)</b></td>
<td><b>Plunge Rate (mm/ min)</b></td>
<td><b>Step Over</b></td>
<td><b>Step Down (mm)</b></td>
<td><b>Spindle Speed (RPM)</b></td>
</tr>
<tr>
<td><b>Wood (general)</b></td>
<td>1000</td>
<td>250</td>
<td>0.40</td>
<td>2</td>
<td>20,000</td>
</tr>
<tr>
<td><b>Pine / Cedar</b></td>
<td>1400</td>
<td>250</td>
<td>0.45</td>
<td>3</td>
<td>20,000</td>
</tr>
<tr>
<td><b>Maple / Oak / Cherry</b></td>
<td>1000</td>
<td>250</td>
<td>0.40</td>
<td>2</td>
<td>20,000</td>
</tr>
<tr>
<td><b>Walnut</b></td>
<td>900</td>
<td>250</td>
<td>0.40</td>
<td>2</td>
<td>20,000</td>
</tr>
<tr>
<td><b>Plywood</b></td>
<td>1200</td>
<td>250</td>
<td>0.40</td>
<td>2</td>
<td>20,000</td>
</tr>
</tbody>
</table>

And for <a href="https://sienci.com/product/1-4-spiral-up-cut-end-mill/" target="_blank" rel="noopener">1/4" 2 flute flat end mills</a>. Start with these settings and adjust as needed - these are guidelines, not hard rules:

<table class="wp-table" width="70%">
<tbody>
<tr>
<td><b>Material</b></td>
<td><b>Feed Rate (mm/ min)</b></td>
<td><b>Plunge Rate (mm/ min)</b></td>
<td><b>Step Over</b></td>
<td><b>Step Down (mm)</b></td>
<td><b>Spindle Speed (RPM)</b></td>
</tr>
<tr>
<td><b>Wood (general)</b></td>
<td>1000</td>
<td>250</td>
<td>0.40</td>
<td>3</td>
<td>18,000</td>
</tr>
<tr>
<td><b>Pine / Cedar</b></td>
<td>1400</td>
<td>250</td>
<td>0.45</td>
<td>4</td>
<td>18,000</td>
</tr>
<tr>
<td><b>Maple / Oak / Cherry</b></td>
<td>1000</td>
<td>250</td>
<td>0.40</td>
<td>3</td>
<td>18,000</td>
</tr>
<tr>
<td><b>Walnut</b></td>
<td>900</td>
<td>250</td>
<td>0.40</td>
<td>3</td>
<td>18,000</td>
</tr>
<tr>
<td><b>Plywood</b></td>
<td>1200</td>
<td>250</td>
<td>0.40</td>
<td>3</td>
<td>18,000</td>
</tr>
</tbody>
</table>

One thing to note about wood is that it can burn if:

- You are cutting too slowly or your spindle speed is too high
- Sawdust is getting stuck in your cut
- You are using bits that are not designed for cutting wood

### Softwoods (pine, fir, spruce, cedar, etc.)

- Most common softwoods tend to be more fibrous than hardwoods. This can leave strands and burrs (fuzz) on some cut edges. You can reduce this by adding a finishing pass in your program. You may also find either conventional or climb milling affects your cut quality as well.
- Watch for warping, as many softwoods are more prone to warping.

### Hardwoods (maple, cherry, oak, walnut, etc.)

- Most common hardwoods are more prone to burning, as the sawdust for these woods tends to be finer and stickier. You can reduce this by increasing your feed rate and decreasing your stepdown.

### Plywood

- There are many grades of plywood. Most lower grade plywood can be cut quite quickly as the wood is quite soft. Higher grade such as marine grade and baltic birch is harder and may need reduced feeds and speeds.
- Plywood can splinter and tear along the top cut edges. A <a href="https://sienci.com/product/1-4-spiral-down-cut-end-mill/" target="_blank" rel="noopener">downcut bit</a> can be used to mitigate this.
- Plywood uses glues that can affect your cut quality and may affect the longevity of your bits. Make sure to check and ensure that they are clean between cuts.

### MDF

- MDF is a cheap, easy to cut material that tends to cut quite cleanly and evenly on the CNC router.
- MDF dust is incredibly fine and can be dangerous. Make sure to use appropriate dust collection and a mask. A using a <a href="https://sienci.com/product/LongMill-magnetic-dust-shoe-mk2/" target="_blank" rel="noopener">dust shoe</a> is a good option.
- Like plywood, MDF also has chemicals and glues in the material. Make sure to check and ensure that they are clean between cuts

## Plastic

Plastic is a material used everywhere in our modern world. Each type of plastic has unique properties that we must take into account when choosing our speeds and feeds.

![](/_images/_cnc-fun/_the-basics/cnc_ba_materials_p2-plastic.jpg){.aligncenter .size-medium}

### Acrylic / Polycarbonate

- Although acrylic and polycarbonate look almost identical visually, they have different properties. Most common issue with cutting acrylic and polycarbonate is melting as they have very low melting points.
- Reducing spindle speed can reduce heat build-up and prevent the chips from welding themselves onto your part of end mill.
- Acrylic, with the right settings, cuts incredibly easily. Typically, standard wood cutting spiral flute end mills will work fine. However, you may choose to use single flute end mills that are designed for plastics for better cuts.
- Polycarbonate tends to be more flexible plastic, making it more challenging to cut than acrylic. Properly securing your workpiece to prevent your material from flexing while cutting is important.
- It is advisable to use single flute end mills on polycarbonate as well.

### ABS / PVC / HDPE

- These plastics are a joy to cut. With a sharp cutter, you these plastics cut like butter.
- Standard 1/8" and 1/4" 2 flute end mills work well with these materials, you can also find special plastic cutting end mills as well.
- If you experience melting, increase your feed rate or decrease your spindle speed.
- These plastics can gain a static charge and stick to surfaces.
- Laser cutting/burning PVC releases toxic gases and chemicals.

### Delrin / Teflon

- Low friction plastics like Delrin (POM) is also quite easy to machine.
- Standard 1/8" and 1/4" 2 flute end mills work well with these materials, you can also find special plastic cutting end mills as well.

## Foam

Foam, being a super soft material, is an easy material to cut. We recommend foam as a starting material to practice CNC programming. Foam also has many useful applications, such as in packaging, RC planes, drones, and more.

![](/_images/_cnc-fun/_the-basics/cnc_ba_materials_p3-foam.jpg){.aligncenter .size-medium}

Rigid foam is the ideal foam material for CNCing, its closed-cell structure is strong enough to withstand cutting forces while being soft enough to cut through effortlessly. Most of the time, you can cut at full speed and full engagement with no issues, making it a fast way to draft out cuts. Soft foams come in many different densities and softness, which can affect cutting. These settings work with both 1/8" and 1/4" 2 flute flat end mills.

<table class="wp-table" width="70%">
<tbody>
<tr>
<td><b>Material</b></td>
<td><b>Feed Rate (mm/ min)</b></td>
<td><b>Plunge Rate (mm/ min)</b></td>
<td><b>Step Over</b></td>
<td><b>Step Down (mm)</b></td>
<td><b>Spindle Speed (RPM)</b></td>
</tr>
<tr>
<td><b>Foam (rigid closed-cell)</b></td>
<td>2500</td>
<td>800</td>
<td>0.7</td>
<td>6</td>
<td>10,000</td>
</tr>
</tbody>
</table>

### Rigid foams (polystyrene foam insulation)

- Because polystyrene is so soft, you can typically cut this material at full engagement. Keep your spindle speed low to prevent melting.
- Since it's easy to cut, we recommend using it to practice CNC programming or as a drafting material.
- Foam dust is very fine and sticks to surfaces. It is recommended to use a dust shoe.
- Keep an eye on melted foam on your bits. You can clean them off with some acetone.

### Soft foams (polyurethane)

- Polyurethane comes in a lot of different hardnesses and densities. Because it is not rigid, it can be pushed out of the way by the end mill rather than be cut. You may need to change your cutting direction, or speeds and feeds to accommodate.
- Consider using a corn-cob end mill, an end mill with little burred teeth rather than a standard fluted end mill. These bits take little tiny cuts out of your material rather than shaving away chips, preventing the foam from being pushed out of the way.
- Foam dust is very fine and sticks to surfaces. It is recommended to use a dust shoe. Keep an eye on melted foam on your bits. You can clean them off with some acetone.

## Aluminum

Aluminum is a strong and lightweight metal used in all sort of modern applications from our bikes to our laptops. CNCing aluminum is a great option to get useful parts, especially for mechanical systems and tools.

![](/_images/_cnc-fun/_the-basics/cnc_ba_materials_p4-aluminum.jpg){.aligncenter .size-medium}

Aluminum comes in a variety of different alloys. We will primarily be talking about 6060 aluminum, which is the most commonly used alloy. General feeds and speeds using a <a href="https://sienci.com/product/18-flat-end-mill-for-aluminum/" target="_blank" rel="noopener">1/8" single flute flat aluminum cutting end mill</a>. Please note that these settings are for basic cutting such as with <a href="http://camlab.sienci.com" target="_blank" rel="noopener">CAMLab</a> or <a href="https://grid.space/kiri#cnc" target="_blank" rel="noopener">Kiri:Moto</a> and not for adaptive toolpathing operations which have other settings.

<table class="wp-table" width="70%">
<tbody>
<tr>
<td><b>Material</b></td>
<td><b>Feed Rate (mm/ min)</b></td>
<td><b>Plunge Rate (mm/ min)</b></td>
<td><b>Step Over</b></td>
<td><b>Step Down (mm)</b></td>
<td><b>Spindle Speed (RPM)</b></td>
</tr>
<tr>
<td><b>6061 Aluminum</b></td>
<td>1200</td>
<td>100</td>
<td>0.2</td>
<td>0.4</td>
<td>13,000</td>
</tr>
</tbody>
</table>

- Aluminum is near the upper limit of hardness that you want to be milling with a general hobby CNC machine, and is best suited for a machine like the AltMill. Setting up your machine to be as rigid as possible (milling near the supported areas of your rails, using proper clamping, reducing stick-out of your end mill) can make a difference.
- The most common cause of end mill breakage is when chips build up and melt onto your bit. Ensuring that you have the proper chipload and chip ejection (only use upcut bits) is important to draw heat out of the cut. Some users may choose to use coolant or compressed air to cool their cuts. Make sure to keep chips out of the cut at all times.
- Most routers run at relatively high RPMs (10,000 to 30,000RPM) for cutting metals. Because of this, it is best to use single flute bits like our <a href="https://sienci.com/product/18-flat-end-mill-for-aluminum/" target="_blank" rel="noopener">1/8" flat end mill for aluminum</a> to ensure that you can get optimally sized chips. Also, reducing your RPM can help.
- Some coatings, especially ones with coatings that contain aluminum (AlTiN, TiAlN), should be avoided as aluminum chips can have an affinity to the coating.
- Using an advanced CNC CAM program such as <a href="https://www.autodesk.com/products/fusion-360/overview" target="_blank" rel="noopener">Fusion 360</a> that allows for adaptive toolpathing can speed up your cutting and give you better results, so if you're planning on cutting a lot of aluminum, it may be worth learning.
