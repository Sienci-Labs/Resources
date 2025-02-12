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
skip_file: no
featured_image: _images/_lmmk2/_handbook/lmk2_feedsspeeds_Pocketingvsslotting.png
---

“Feeds and Speeds” is an all-encompassing term used to describe most of the variables that come into play when using a cutting tool to carve a material. In the hobby-sense, this includes:

<ul>
  <li><b>How fast the CNC moves</b> (feed rate, plunge rate, and router/spindle RPM)</li>
  <li><b>How much material is removed</b> (stepdown and stepover)</li>
</ul>

Figuring out how to cut materials nicely on your machine can be confusing and time consuming. Most cutting tool manufacturers spec industry-grade speeds that hobby-grade machines can’t achieve and tool information that hobby CAM software can’t use. Chatter analysis, optimizing material removal rate, tool life preservation, and more simply fall out of range for most hobby CNC'ers since they don't do the high-load or large capacity work of business and industry. We wanted to see what we could do to help with this.

The result is a simple reference-table that you can use as a starting point for your next project. This required us to do a crazy amount of math, create internal testing patterns and procedures, run tests on all the common CNC bits and materials we could think of, and break a lot of bits along the way to hone what we hope will power up your ability to get the most out of your LongMill. We’ve also included more reading later down the page if you’re curious about the theory that drove these cutting parameters and their outcomes: <em>‘<a href="#cutting-theory">Cutting Theory</a>’</em>.

## Using the F&S Tables

Our tables try to account for the average setup you’ll have with your LongMill MK2 so that you can use the values as a <b>jumping-off point</b>. This is where we’ll stick a giant asterisk since despite all the work we’ve done we’ll never be able to provide guarantees against broken bits or failed projects. Woods, plastics, metals - basically any material is going to behave differently whether you’re in Canada, the USA, or Australia because of variations in natural species, manufacturing processes, temperature, humidity, and many other factors. This is the nature of CNC where it becomes more of an art than a science. All machines are different, are assembled differently, use different table setups, exist in different environments, use different cutting tools, and so forth.

<strong>Here are some other things to keep an eye out for:</strong>

<ol>
  <li>The tables (on this page and as a PDF) so far contain commonly-used hobby CNC cutting tools and materials such as soft and hard woods, common plastics, and common aluminum. If you don’t see the material you plan to cut feel free to ask around in our community for advice or what has worked successfully for others</li>
  <li>Suggestions for bits that do engraving, V-carving, and 3D contours will have flavours for ‘coarse’, ‘fine’, and some other use-cases but all at fixed speeds. This is because these types of cutting tools don’t tend to strain the machine so instead these options should suit what type of cutting you plan to do</li>
  <li>Since we know everyone will have different preferences for how they run all the other tool types on their CNC, we’ve created three options of speed/aggressiveness to suit conservative and aggressive CNC’ers alike:
<table class="wp-table" style="height: 256px; border: 1px solid gray;" width="959">
<tbody>
<tr>
<td style="background-color: #b6d7a8;"><strong>Reduced Speed</strong> - Finishing or mild cutting</td>
<td>
<ul>
  <li aria-level="2">Use these settings when cutting fine detail to reduce material tear-out and improve surface finish and accuracy</li>
  <li aria-level="2">Useful if you’d prefer running your machine more conservatively or are just starting out using your machine</li>
</ul>
</td>
</tr>
<tr>
<td style="background-color: #ffe599;"><strong>Regular Speed</strong></td>
<td>
<ul>
  <li>For general use cutting, generally a good starting point for trying out new project materials</li>
</ul>
</td>
</tr>
<tr>
<td style="background-color: #ea9999;"><strong>Full Speed</strong> - Roughing or aggressive cutting</td>
<td>
<ul>
  <li aria-level="2">Use these settings if you have lots of material to cut through and you’d like to speed up the process</li>
  <li aria-level="2">Ensure your <a href="https://resources.sienci.com/view/lmk2-maintenance/#adjusting-the-eccentric-nuts" target="_blank" rel="noopener">v-wheels are properly adjusted</a> when using these more aggressive settings</li>
</ul>
</td>
</tr>
</tbody>
</table>
</li>
  <li>Lastly, you’ll notice that for every tool in the tables the recommended stepdown (a.k.a. depth of cut) is larger for pocketing/contouring and smaller for slotting. This is because:
<ul>
  <li aria-level="2"><b>Slotting</b> (cutting out shapes, profiles, engraving) cuts with the full tool diameter, putting more stress on the tool and machine, thereby requiring shallower cuts</li>
  <li aria-level="2"><b>Pocketing/contouring</b> (surfacing, cleaning walls, clearing a specified area, 3D carving) cuts with usually less than 50% of the tool allowing deeper cuts</li>
</ul>
</li>
</ol>

![](/_images/_lmmk2/_handbook/lmk2_feedsspeeds_Pocketingvsslotting.png){.aligncenter .size-medium}

[su_spoiler title="
<h3>🪶 Soft Woods, Plywood, and MDF</h3>
" open="no" style="fancy" icon="chevron" anchor="" anchor_in_url="no" class=""]

Not the colloquial ‘softwood’, rather any woods, plywoods, or MDF that have low hardness and can be dented with a fingernail. These woods are very forgiving to cut and work well with many types of bit geometry and size. Wood is simply an amazing material. As it is a living, organic material, there are an infinite variety of woods and characteristics.

<strong>General tips and tricks for these materials are:</strong>

<ul>
  <li>Cutting soft woods will often leave strands and burrs on your finished project. To prevent this, try reducing your feed rates slightly (~20%) or running a second finishing pass if your software allows this</li>
  <li>Plywoods (and some stringy soft woods) are prone to splintering at the surface during cutting. Using a downcut or compression bit can help with this immensely since they won’t tear the material up and over the surface. You can read more about how compression bits work <a href="https://sienci.com/2021/03/01/introducing-1-8-compression-bits-to-our-store/">here</a></li>
  <li>If you notice burning, ensure that: you’re using a wood-compatible tool, sawdust isn’t getting stuck in your cut (downcut bits can cause this), your cutting speed isn’t too slow, or router/spindle RPM isn’t too high</li>
  <li>Even though MDF is a cheap and clean-cutting material on CNCs, make sure to wear appropriate PPE since the dust is incredibly fine and can be dangerous to breathe in. Using a <a href="https://sienci.com/product/LongMill-magnetic-dust-shoe-mk2/">dust shoe</a> is a good option to help reduce the amount of generated dust</li>
</ul>

[tabby title="Reduced Speed"]

[su_csv_table url="https://resources.sienci.com/wp-content/uploads/2022/10/FSCSV-Softwood-Reduced.csv" header="yes" responsive="yes"]

[tabby title="Regular Speed" open="yes"]

[su_csv_table url="https://resources.sienci.com/wp-content/uploads/2022/10/FSCSV-Softwood-Regular.csv" header="yes" responsive="yes"]

[tabby title="Full speed"]

[su_csv_table url="https://resources.sienci.com/wp-content/uploads/2022/10/FSCSV-Softwood-Full.csv" header="yes" responsive="yes"]

[tabbyending]

<strong>Tips and tricks for engraving or 3D carving these materials are:</strong>

<ul>
  <li>Soft woods are very easy to cut, we encourage you to engrave as fast as you’re comfortable with to save time</li>
  <li>You may consider skipping the roughing pass to save time if the deepest part of your engraving is less half the flute length of your tool</li>
  <li>Many woods can be warped which causes engraving and V-carving details such as text to have inconsistent cutting depth. Surfacing the material before starting your job will help this by giving you a flatter surface to work with</li>
</ul>

[su_csv_table url="https://resources.sienci.com/wp-content/uploads/2022/10/FSCSV-Softwood-Carving2.csv" header="yes" responsive="yes"]

[/su_spoiler]

[su_spoiler title="
<h3>🪓 Hard Woods and Plywoods</h3>
" open="no" style="fancy" icon="chevron" anchor="" anchor_in_url="no" class=""]

Hard woods are a step up from soft woods (as the name would suggest), and require a bit more attention to get the right cut settings. You’ll want to pay especially close attention when cutting with very small bits such as 1/16” end mills to ensure they don’t break.

<strong>General tips and tricks for these materials are:</strong>

<ul>
  <li>Some hard woods can be more than 5x harder than others. We’ve tried to make these tables based on the more common North American hard woods so reduce your depth of cut and feed rates if you plan to cut any wood that’s uniquely harder or exotic if you’re unsure</li>
  <li>Hard woods will often produce sawdust that is finer and stickier than soft woods which may lead to burning if feed rate is too low or router speed is set too high. There are also some exotic woods whose dust can be dangerous to breathe in so do your research into your material or ask your material seller to take appropriate safety measures</li>
</ul>

[tabby title="Reduced Speed"]

[su_csv_table url="https://resources.sienci.com/wp-content/uploads/2022/10/FSCSV-Hardwood-Reduced.csv" header="yes" responsive="yes"]

[tabby title="Regular Speed" open="yes"]

[su_csv_table url="https://resources.sienci.com/wp-content/uploads/2022/10/FSCSV-Hardwood-Regular.csv" header="yes" responsive="yes"]

[tabby title="Full speed"]

[su_csv_table url="https://resources.sienci.com/wp-content/uploads/2022/10/FSCSV-Hardwood-Full.csv" header="yes" responsive="yes"]

[tabbyending]

<strong>Tips and tricks for engraving or 3D carving these materials are:</strong>

<ul>
  <li>Running a V-carving or engraving program twice can help clean up the inside surfaces of your cuts, saving you time from manually cleaning up burrs and chips. This is much less of an issue if you can use a finishing pass in your program</li>
  <li>Many woods can be warped which causes engraving and V-carving details such as text to have inconsistent cutting depth. Surfacing the material before starting your job will help this by giving you a flatter surface to work with</li>
</ul>

[su_csv_table url="https://resources.sienci.com/wp-content/uploads/2022/10/FSCSV-Hardwood-Carving2.csv" header="yes" responsive="yes"]

[/su_spoiler]

[su_spoiler title="
<h3>🧴 Plastics (Acrylic, PVC, HDPE, Acetal/Delrin)</h3>
" open="no" style="fancy" icon="chevron" anchor="" anchor_in_url="no" class=""]

Plastic is a material used everywhere in our modern world with each plastic having unique properties impacting their cutting characteristics and strategy. Some are quite easy to cut like ABS, PVC, HDPE, and Delrin/POM while others like acrylic or polycarbonate can be more moderate in their cutting difficulty, similar to hard woods. Plastics also present the challenge of being more prone to melting and ‘gumming up’ the cutting bit.

For cutting acrylic we highly recommend you use <strong>cast acrylic</strong> (usually has paper backing) instead of extruded acrylic (plastic backing). Cast acrylic will always have a better surface finish compared to extruded acrylic which is significantly more difficult to cut due to its lower melting temperature.

[gallery columns="2" size="medium" ids="4482,4483"]
<p style="text-align: center;"><em>Machining on extruded (left) vs cast (right) acrylic using the same g-code</em></p>

<strong>General tips and tricks for these materials are:</strong>

<ul>
  <li>A sharp cutter will help give you a nice cut and surface finish, specialized plastic cutting end mills will also give better results</li>
  <li>To help mitigate melting/gumming with acrylic or polycarbonate it’s advised to use upcut single flute cutting bits running at a low router speed to help clear chips; standard 2 flute end mills should work well for ABS, PVC, HDPE, and Delrin/POM</li>
  <li>If you find chips sticking to the cutter or melting onto the material, try increasing your feed rate or decreasing the router speed</li>
  <li>Specifically for acrylic, avoid taking straight plunges into the material since this will typically cause melting or fracture the material</li>
</ul>

[tabby title="Reduced Speed"]

[su_csv_table url="https://resources.sienci.com/wp-content/uploads/2022/10/FSCSV-Plastics-Reduced.csv" header="yes" responsive="yes"]

[tabby title="Regular Speed" open="yes"]

[su_csv_table url="https://resources.sienci.com/wp-content/uploads/2022/10/FSCSV-Plastics-Regular.csv" header="yes" responsive="yes"]

[tabby title="Full speed"]

[su_csv_table url="https://resources.sienci.com/wp-content/uploads/2022/10/FSCSV-Plastics-Full.csv" header="yes" responsive="yes"]

[tabbyending]

<strong>Tips and tricks for engraving or 3D carving these materials are:</strong>

<ul>
  <li>Always perform a roughing pass using a flat end mill / tapered ball end mill (with the roughing settings below) with a 0.15-0.3mm stock to leave setting before performing the finishing pass. This will dramatically improve the surface finish of your engraving and reduce the chance of melting</li>
  <li>If melting is still observed for acrylic, try decreasing the feed rate (this goes against the general tips we have for plastics but slowing down the rate at which material is removed is the most reliable way we’ve found to prevent melting)</li>
  <li>Never cut or engrave PVC with a laser, it will release toxic gasses and chemicals</li>
</ul>

[su_csv_table url="https://resources.sienci.com/wp-content/uploads/2022/10/FSCSV-Plastics-Carving2.csv" header="yes"]

[/su_spoiler]

[su_spoiler title="
<h3>🦾 Aluminum (6061)</h3>
" open="no" style="fancy" icon="chevron" anchor="" anchor_in_url="no" class=""]

Aluminum is an incredibly useful medium for creating strong mechanical parts, tools, or impressive display pieces. Unfortunately, it can also be quite difficult to cut. Our aluminum cutting table was developed for the most common aluminum stock you’ll come across, the variety/alloy known as ‘6061’. Other alloys such as 7075 (stronger and significantly harder to machine) will require some experimentation using the 6061 cutting parameters as a starting point.

Since aluminum is near the upper limit of hardness that should milled using a hobby CNC machine, you’ll want to take any measures to make your machining setup as rigid as possible such as:

<ul>
  <li>Setting up your project in a corner of your wasteboard so that the rails have less flex/twist</li>
  <li>Ensure your <a href="https://resources.sienci.com/view/lmk2-maintenance/#adjusting-the-eccentric-nuts">V-wheels are fully tightened</a>, potentially even a bit over-tightened, and all other tuning aspects of your machine are spot on</li>
  <li>Reduce the stick-out length of your cutting bit as much as you can or use short and stubby bits</li>
</ul>

<strong>General tips and tricks for these materials are:</strong>

<ul>
  <li>Single flute upcut bits are the best choice for aluminum since they create large chips and clear them away very well. Avoid using any cutting bits with coatings which contain aluminum such as AITiN or TiAIN since aluminum will stick to these</li>
  <li>Make sure your cutting results in aluminum chips, instead of dust. When chips are cut, they carry away heat from the material and prevent the cutting bit from gumming up with molten aluminum. If your cuts are resulting in dust, try increasing feed rate or decreasing the router speed</li>
  <li>WD-40 or isopropyl alcohol can be used as coolant/cutting lubricant. Be sure that chips are still able to be cleared when using a coolant/cutting lubricant – compressed air is great for occasionally clearing out chips during cutting</li>
  <li>Using an advanced CNC CAM program such as<a href="https://www.autodesk.com/products/fusion-360/overview"> Fusion 360</a> that allows for adaptive toolpathing can speed up your cutting and give you better results. There is a steep learning curve, but if you’re planning on cutting a lot of aluminum, it may be worth learning</li>
</ul>

[tabby title="Reduced Speed"]

[su_csv_table url="https://resources.sienci.com/wp-content/uploads/2022/10/FSCSV-Aluminum-Reduced.csv" header="yes" responsive="yes"]

[tabby title="Regular Speed" open="yes"]

[su_csv_table url="https://resources.sienci.com/wp-content/uploads/2022/10/FSCSV-Aluminum-Regular.csv" header="yes" responsive="yes"]

[tabby title="Full speed"]

[su_csv_table url="https://resources.sienci.com/wp-content/uploads/2022/10/FSCSV-Aluminum-Full.csv" header="yes" responsive="yes"]

[tabbyending]

<strong>Tips and tricks for engraving or 3D carving these materials are:</strong>

<ul>
  <li>Avoid using tapered ball end mills when milling aluminum. The tapered end of these bits will typically be too thin to take any reasonable cut in aluminum since it will deflect, or more likely; break</li>
  <li>Always use one or more roughing passes using a flat end mill before any 3D carving. Some 3D models especially have small geometry that might need to be cleared out with a smaller end mill before relief cutting, otherwise the tapered bit will plunge straight into solid aluminum stock and break off. The better planned the toolpaths with more roughing passes, the easier the finishing 3D carving pass will be</li>
</ul>

[su_csv_table url="https://resources.sienci.com/wp-content/uploads/2022/10/FSCSV-Aluminum-Carving2.csv" header="yes" responsive="yes"]

[/su_spoiler]

## PDF Tables

Handy for printing out as a quick reference to keep on your computer or by your CNC and available in both imperial and metric units.

| Feeds & Speeds - Metric                                                                                     | Feeds & Speeds - Imperial                                                                                   |     |     |
|-------------------------------------------------------------------------------------------------------------|-------------------------------------------------------------------------------------------------------------|-----|-----|
| [![Feeds & Speeds - Metric](/_images/_lmmk2/_handbook/lmk2_feedsspeeds_pdf-crop.png){.aligncenter .size-small}](/_community-docs/FeedsSpeedsMetric.pdf) | [![Feeds & Speeds - Imperial](/_images/_lmmk2/_handbook/lmk2_feedsspeeds_pdf-crop.png){.aligncenter .size-small}](/_community-docs/Feeds-and-Speeds-Imperial.pdf) |     |     |

## Tool Library files

<a href="https://sienci.com/tool-libraries/">Find them here!</a>

## FAQ

<strong><em>Are you ever going to provide feeds and speeds for material X?</em></strong>

<p style="padding-left: 40px;">We’ve tried to cover most common/popular materials and hope to expand our feeds and speeds to include other materials in the future, but we can’t cover everything. Less popular materials such as FR4, carbon fiber, and steel can all be cut, but aren’t very popular. If there’s a particular material you’d like us to provide, feel free to contact us and let us know.</p>

<strong><em>Will these feeds and speeds work with the cutting bit I got from X?</em></strong>

<p style="padding-left: 40px;">As long as the important cutting bit geometry is the same, probably. There is a misconception in the hobby CNC router space that different sources of cutting bits will perform completely differently. Some may be sharper or higher quality than others but most will perform fairly similarly in common materials such as woods.</p>

<strong><em>The router speed/RPM you suggest for this bit is much slower than I normally use, isn't faster always better?</em></strong>

<p style="padding-left: 40px;">The router speed/RPM is determined by the geometry of the bit, type of material, and feed rate which might end up being slower than you would expect. This is further discussed in the topic of <a href="https://resources.sienci.com/view/lmk2-feeds-and-speeds/#chip-load-">chip load</a>. It’s intuitive to think that cranking up your router speed will help cuts come out better - and to some extent it might - but an appropriate router speed is one that generates chips not too large (overloading the bit) and not too small (causing burning).</p>

<strong><em>I’m used to cutting much faster than what these recommended feeds and speeds are, am I doing something wrong?</em></strong>

<p style="padding-left: 40px;">When cutting softer materials, you might find that you can cut much more aggressively than what we recommend. This is because the recommended feeds and speeds are more based around retaining good cut quality, and less around cutting as fast as possible. In our own testing, soft woods can actually be cut about twice as aggressively as what is recommended, but you’ll likely encounter losses in quality, splintering/splitting, and even large chunks of wood stripped out depending on the wood grain.</p>

<strong><em>Am I going to wear out my tools faster by cutting with more aggressive settings?</em></strong>

<p style="padding-left: 40px;">Technically, yes, but in practice no. Some bits may be sharper than others from the factory, but you can expect tools to perform about the same throughout their lifespan regardless of how aggressively you run them. The main detriment which causes premature tool wear is using an inappropriate <a href="https://resources.sienci.com/view/lmk2-feeds-and-speeds/#chip-load-">chip load</a>.</p>

<strong><em>Are you ever going to make a downloadable tool database for X CAM program?</em></strong>

<p style="padding-left: 40px;">Many CAM programs don’t have the functionality of importing and exporting tool databases/libraries, so we focused on two popular CAM programs which do.</p>

<strong><em>My CAM software only allows me to input my stepover as a % value, not in mm or inches. What should I use?</em></strong>

<p style="padding-left: 40px;">Almost all of the suggested stepover values are based on a 45% stepover value so you can use this for any software which requires this value. You might even find that your CAM software is already defaulting to this value.</p>

<strong><em>Why are there no cutting parameters for cutting X material with X cutting bit?</em></strong>

<p style="padding-left: 40px;">If you can’t find specific cutting parameters for a particular material-bit combination, it’s likely because this is a material-bit combination we cannot advise. Some examples of inadvisable combinations might include cutting aluminum with a corn cob end mill, or using a surfacing bit on acrylic.</p>

<strong><em>Why is my machine struggling to cut even when using the ‘Reduced’ cutting parameters?</em></strong>

<p style="padding-left: 40px;">These cutting parameters were developed to be used on the average LongMill MK2 without overstressing the machine, if yours doesn't seem to be keeping up at these parameters it might be your machine’s way of telling you that something is loose, worn, or misassembled. Check out our page <a href="https://resources.sienci.com/view/lmk2-maintenance/">here</a> covering tuning, maintenance, and checks for loose components.</p>

<strong><em>Can I use these feeds and speeds on my non-LongMill machine?</em></strong>

<p style="padding-left: 40px;">Hobby CNC routers can vary greatly in terms of their rigidity and capabilities, so this will depend. If you’re using these on an industrial machine, these cutting parameters might be a bit conservative but will work just fine. If you’re using these on a slightly less robust machine, you might want to dial back some of these settings and proceed with caution. Either way, use your best judgment and adjust accordingly.</p>

## Cutting Theory

There are two schools of thought on how to select cutting parameters for a hobby CNC machine; calculate all parameters based on theoretical equations, or trial and error based on cut quality and perceived machine strain. An argument can be made for both of these approaches so it’s best to take any theoretical method with a grain of salt and explore how changing certain parameters will affect your machine and projects experimentally. That being said, it’s well worth understanding some of the relationships between different cutting parameters which is why we’ll delve into the theory side of things.

It’s important to understand the main goals in how one goes about deciding on a certain set of cutting parameters. These are typically:

<ul>
  <li>Making sure the cutting bit is creating healthy sized chips - not rubbing and creating dust</li>
  <li>Ensuring the machine is cutting at a pace and depth that both the user and machine are comfortable with</li>
</ul>

We can break down two metrics for targeting both of these goals – chip load, and material removal rate (MRR). Simply put, we’re concerned with how big each individual chip of material is when cut and how much material is removed in a given amount of time. Both of these metrics depend highly on the material you’ll be working with which is what makes choosing cutting parameters so confusing.

### Chip Load ✂️

Chip load describes the size of each individual chip that is being cut by a single edge of your cutting bit.

This is a very sensitive parameter. If too small, the chips reduce in size to become dust which will wear out the bit and heat up causing burning. If too large, the chips become larger which results in the cutting bit being overloaded and unable to clear the chip out of the cut. The effects of chip load on cut quality can be seen below.

![](/_images/_lmmk2/_handbook/lmk2_feedsspeeds_Chipload-Illustration-scaled.jpg "Two cuts with different chip load produce very different results"){.aligncenter .size-medium}

To calculate chip load there’s a simple formula shown below. Since we usually know the number of flutes our cutting bit of choice has, we can modify either feed rate or router speed/RPM to reach the chip load we want. In some cases the speed of the router might not be fast or slow enough to reach the desired chip load so we could change the cutting bit to have more or less flutes to accommodate that. Another approach would be to change the diameter of the bit, thus calling for a different chip load and making it more feasible for the router speed or feed rate you have available.

<p style="text-align: center;"><em><code>Chip Load  = ( Feed Rate ) / ( Router Speed x # Flutes )</code></em></p>

<p style="text-align: center;"><em>For example, if we’d like a chip load of </em><b><em>0.0031”</em></b><em>, we can run a </em><b><em>2 flute</em></b><em> end mill at a speed of </em><b><em>17000 rpm</em></b><em> and feed rate of </em><b><em>105.4 inches/min</em></b><em> (2677.16 mm/min) to achieve this.</em></p>

<p style="text-align: center;"><em><code>Chip Load  = 0.0031" = ( 105.4 ipm ) / ( 17,000 RPM x 2 Flutes)</code></em></p>

Many charts exist which attribute a certain chip load value to a given cutting bit size and material. For our own purposes we’ve attributed a chip load per unit diameter to the common groups of materials as shown in the table below.

<table class="wp-table" width="70%">
<tbody>
<tr>
<td></td>
<td><strong>Softwood, MDF</strong></td>
<td><strong>Hardwood</strong></td>
<td><strong>Plastics</strong></td>
<td><strong>Aluminum</strong></td>
</tr>
<tr>
<td>Chip load per unit diameter</td>
<td>.025" per inch</td>
<td>.025" per inch</td>
<td>.03" per inch</td>
<td>.0125" per inch</td>
</tr>
<tr>
<td>Chip load for <strong>1/16"</strong> diameter end mill<strong>
</strong></td>
<td>.0016"</td>
<td>.0016"</td>
<td>.0019</td>
<td>N/A</td>
</tr>
<tr>
<td>Chip load for <strong>1/8"</strong> diameter end mill<strong>
</strong></td>
<td>.0031</td>
<td>.0031</td>
<td>.0038</td>
<td>.0016</td>
</tr>
<tr>
<td>Chip load for <strong>1/4"</strong> diameter end mill</td>
<td>.0063</td>
<td>.0063</td>
<td>.0075</td>
<td>.0031</td>
</tr>
</tbody>
</table>

### Material removal rate ⛏️

Material removal rate asks the question “how deep can I cut?” Now that we have our targeted chip load and calculated feed rate and router speed we can move onto figuring out the last pieces of the puzzle: depth of cut and stepover.

Naturally we can assume that the more material we cut in a given time, the more strain is placed on the machine and router. If we can quantify how much material is getting removed in a given amount of time, we can aim to keep this within a reasonable amount - this is what the material removal rate metric does. The standard units for material removal rate are in volume per minute - either inch3/min or cm3/min.

Shown below, the formula for material removal rate depends on feed rate, cutting width, and cutting depth. Cutting width will depend on whether you’re slotting (cutting out pieces of things, cutting lines and shapes, etc.) or pocketing (making large holes, cutting out pockets, bowls, etc.) since the full width/diameter of the cutting bit will either be fully engaged (slotting) or partially engaged (pocketing).

<p style="text-align: center;"><em><code>Material Removal Rate  = Feed Rate x Cutting Width x Cutting Depth</code></em></p>

For <b>slotting</b> the cutting width will be fully engaged, meaning our cutting width or width of cut (WOC) will be equal to the tool diameter (ie. WOC = 0.25” if using a ¼” bit).

For <b>pocketing</b> our tool will only move over by some distance between passes, typically this distance should be about ~45% of the width of the cutting bit (ie. WOC = 0.25” x 45%=0.1125” if using a ¼” bit).

The illustrations below show the use of a tool in a high depth of cut, low width of cut scenario (left), as well as low depth of cut, high width of cut scenario (right). With the feed rate constant between these two cuts, they'll both be removing the exact same amount of material in the same amount of time.

[gallery columns="2" size="medium" ids="4474,4473"]

Since we know our desired feed rate (from our chip load calculation) and cutting width (depending on the cutting operation), we can calculate what our cutting depth should be if we’d like to keep our material removal rate below some reasonable amount. At this point, we’ve now gotten all of our cutting parameters necessary for setting up a cutting operation.

### Theory Review 📖

As mentioned above, one of the most useful aspects of machining theory applied to hobby CNC is not the actual calculation of parameters - but rather the relationships we can understand between different cutting parameters.

We’ll do a quick review on how some cutting parameters might affect other outcomes:

<ul>
  <li>Increasing router speed/RPM will make chips smaller and become dust if too fast (not a good thing)</li>
  <li>Increasing feed rate will make chips larger, and also put more strain on the machine</li>
  <li>Increasing feed rate, and increasing router speed/RPM will keep chip load the same and allow you to cut material faster</li>
  <li>Using a cutting bit with more flutes will decrease chip load, unless router speed is increased accordingly, or feed rate is decreased accordingly</li>
  <li>Decreasing cutting width/WOC will allow you to cut deeper with the same amount of strain on the machine</li>
  <li>Using a larger cutting bit means your targeted chip load should be greater, meaning your router speed/RPM should be lower</li>
</ul>

### 3D carving/reliefs ⛰️

While the theory presented above holds true for any type of machining, there are a few additional constraints that we should be aware of when 3D carving.

The first constraint to pay attention to is cutting width/stepover. This is a variable that we can typically change to control the rate of material removal but in 3D carving it’s directly tied to surface finish and is typically a small number (~5-15% depending on the size of the bit).

![](/_images/_lmmk2/_handbook/lmk2_feedsspeeds_Stepover-comparison-scaled.jpeg "Acrylic carving with 5, 10, and 15% stepover (left to right)"){.aligncenter .size-medium}

When a ball end mill carves in several straight, parallel passes it leaves behind small amounts of material in the form of ridges - these are known as 'cusps'. These cusps are the reason for the increase in detail/resolution with a lower stepover; as shown in the photo below, a larger stepover means larger cusps, while a smaller stepover means the cusps continue getting smaller until they're imperceptible to the human eye. Obviously, with lower stepover, this means a greater number of passes, and a much longer total project time. You'll need to decide how much detail you need, and how long you're willing to run the project for. For example, for carving a 2"x2" relief, you'll probably want to use a low stepover amount such as 5-8% since this project won't take more than an hour. If you we're carving <a href="https://youtu.be/yOywuK02vVY" target="_blank" rel="noopener">something much larger</a>, you might want to set your stepover much larger and forego finer detail for a faster overall project time.

![](/_images/_lmmk2/_handbook/lmk2_feedsspeeds_Stepover-Chart-white.png){.aligncenter .size-medium}

Cutting depth is the next variable to consider and in relief carving this is again something that you do not have much control over. This is because the tool will need to follow the contours of your 3D model which can vary considerably in depth.

![](/_images/_lmmk2/_handbook/lmk2_feedsspeeds_Toolload-Explained.png "Abrupt changes in depth / carving deep reliefs will increase tool load"){.aligncenter .size-medium}

The implications of the two constraints above are that tools will tend to be underutilized (removing too little material) on the shallow parts of the relief and struggle on the deeper / steeper parts (removing too much material). For wood based materials, you’re less likely to exceed the tool’s material removal capabilities on even the deepest parts of your relief without running into other constraints in your machine such as feedrate. On harder materials such as acrylic / aluminum however the spikes in material removal is a much bigger concern and is why roughing (with a very shallow depth of cut and minimal stock to leave) is a prerequisite for success.

![](/_images/_lmmk2/_handbook/lmk2_feedsspeeds_roughing-Finishing.png "Keeping tool load in check with separate roughing and finishing passes"){.aligncenter .size-medium}
