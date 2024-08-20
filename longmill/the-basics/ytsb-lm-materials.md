---
title: ytsb Materials
menu_order: 4
post_status: draft
post_excerpt: A list of materials that can be cut by the LongMill CNC, with considerations for cutting tools and best practices. Wood, plastic, foam and soft metal suggested.
post_date: 2021-04-30 15:50:00
taxonomy:
    knowledgebase_cat: lm-the-basics
    knowledgebase_tag:
        - mk1
custom_fields:
    KBName: LongMill CNC
    basepress_post_icon: bp-caret-right
skip_file: no
featured_image: _images/_longmill/_the-basics/lm_materials_p1_Guitar.jpg
---

<!-- wp:paragraph -->
<h2>Wood</h2>

<p>Wood is simply an amazing material. As it is a living, organic material, there are an infinite variety of woods and characteristics. We will talk a little about using wood with your CNC machine here.</p>

![](/_images/_longmill/_the-basics/lm_materials_p1_Guitar.jpg){.aligncenter .size-medium}
<p><!-- /wp:paragraph -->

<!-- wp:image {"id":12393} --></p>
<p><!-- /wp:image -->

<!-- wp:paragraph --></p>
<p>General recommended starting feeds and speeds for <a href="http://sienci.com/product/18-flat-end-mill/" target="_blank" rel="noopener">1/8" 2 flute flat end mills</a>. Please start with these settings and adjust, these are not hard and fast speeds.</p>
<p><!-- /wp:paragraph -->

<!-- wp:table --></p>
<table class="wp-table" width="70%">
<tbody>
<tr>
<td><strong>Material</strong></td>
<td><strong>Feed Rate (mm/ min)</strong></td>
<td><strong>Plunge Rate (mm/ min)</strong></td>
<td><strong>Step Over</strong></td>
<td><strong>Step Down (mm)</strong></td>
<td><strong>Spindle Speed (RPM)</strong></td>
</tr>
<tr>
<td><strong>Wood (general)</strong></td>
<td>1000</td>
<td>250</td>
<td>0.40</td>
<td>2</td>
<td>20,000</td>
</tr>
<tr>
<td><strong>Pine / Cedar</strong></td>
<td>1400</td>
<td>250</td>
<td>0.45</td>
<td>3</td>
<td>20,000</td>
</tr>
<tr>
<td><strong>Maple / Oak / Cherry</strong></td>
<td>1000</td>
<td>250</td>
<td>0.40</td>
<td>2</td>
<td>20,000</td>
</tr>
<tr>
<td><strong>Walnut</strong></td>
<td>900</td>
<td>250</td>
<td>0.40</td>
<td>2</td>
<td>20,000</td>
</tr>
<tr>
<td><strong>Plywood</strong></td>
<td>1200</td>
<td>250</td>
<td>0.40</td>
<td>2</td>
<td>20,000</td>
</tr>
</tbody>
</table>
<p><!-- /wp:table -->

<!-- wp:paragraph --></p>
<p>and for <a href="https://sienci.com/product/1-4-spiral-up-cut-end-mill/" target="_blank" rel="noopener">1/4" 2 flute flat end mills</a>.</p>
<p><!-- /wp:paragraph -->

<!-- wp:table --></p>
<table class="wp-table" width="70%">
<tbody>
<tr>
<td><strong>Material</strong></td>
<td><strong>Feed Rate (mm/ min)</strong></td>
<td><strong>Plunge Rate (mm/ min)</strong></td>
<td><strong>Step Over</strong></td>
<td><strong>Step Down (mm)</strong></td>
<td><strong>Spindle Speed (RPM)</strong></td>
</tr>
<tr>
<td><strong>Wood (general)</strong></td>
<td>1000</td>
<td>250</td>
<td>0.40</td>
<td>3</td>
<td>18,000</td>
</tr>
<tr>
<td><strong>Pine / Cedar</strong></td>
<td>1400</td>
<td>250</td>
<td>0.45</td>
<td>4</td>
<td>18,000</td>
</tr>
<tr>
<td><strong>Maple / Oak / Cherry</strong></td>
<td>1000</td>
<td>250</td>
<td>0.40</td>
<td>3</td>
<td>18,000</td>
</tr>
<tr>
<td><strong>Walnut</strong></td>
<td>900</td>
<td>250</td>
<td>0.40</td>
<td>3</td>
<td>18,000</td>
</tr>
<tr>
<td><strong>Plywood</strong></td>
<td>1200</td>
<td>250</td>
<td>0.40</td>
<td>3</td>
<td>18,000</td>
</tr>
</tbody>
</table>
<p><!-- /wp:table --></p>
<p><!-- wp:paragraph --></p>
<p>One thing to note about wood is that it can burn if:</p>
<p><!-- wp:list --></p>
<ul>
<li>You are cutting too slowly or your spindle speed is too high</li>
<li>Sawdust is getting stuck in your cut</li>
<li>You are using bits that are not designed for cutting wood</li>
</ul>
<p><!-- /wp:list --></p>
<p><!-- /wp:paragraph --></p>
<p><!-- wp:paragraph --></p>

<h3>Softwoods (pine, fir, spruce, cedar, etc.)</h3>

<p><!-- wp:list --></p>
<ul>
<li>Most common softwoods tend to be more fibrous than hardwoods. This can leave strands and burrs (fuzz) on some cut edges. You can reduce this by adding a finishing pass in your program. You may also find either conventional or climb milling affects your cut quality as well.</li>
<li>Watch for warping, as many softwoods are more prone to warping.</li>
</ul>
<p><!-- /wp:list --><!-- /wp:paragraph --></p>
<p><!-- wp:paragraph --></p>

<h3>Hardwoods (maple, cherry, oak, walnut, etc.)</h3>

<p><!-- wp:list --></p>
<ul>
<li>Most common hardwoods are more prone to burning, as the sawdust for these woods tends to be finer and stickier. You can reduce this by increasing your feed rate and decreasing your stepdown.</li>
</ul>
<p><!-- /wp:list --><!-- /wp:paragraph --></p>
<p><!-- wp:paragraph --></p>

<h3>Plywood</h3>

<p><!-- wp:list --></p>
<ul>
<li>There are many grades of plywood. Most lower grade plywood can be cut quite quickly as the wood is quite soft. Higher grade such as marine grade and baltic birch is harder and may need reduced feeds and speeds.</li>
<li>Plywood can splinter and tear along the top cut edges. A <a href="https://sienci.com/product/1-4-spiral-down-cut-end-mill/" target="_blank" rel="noopener">downcut bit</a> can be used to mitigate this.</li>
<li>Plywood uses glues that can affect your cut quality and may affect the longevity of your bits. Make sure to check and ensure that they are clean between cuts.</li>
</ul>
<p><!-- /wp:list --><!-- /wp:paragraph --></p>
<p><!-- wp:paragraph --></p>

<h3>MDF</h3>

<p><!-- wp:list --></p>
<ul>
<li>MDF is a cheap, easy to cut material that tends to cut quite cleanly and evenly on the CNC router.</li>
<li>MDF dust is incredibly fine and can be dangerous. Make sure to use appropriate dust collection and a mask. A using a <a href="https://sienci.com/product/longmill-magnetic-dust-shoe/" target="_blank" rel="noopener">dust shoe</a> is a good option.</li>
<li>Like plywood, MDF also has chemicals and glues in the material. Make sure to check and ensure that they are clean between cuts</li>
</ul>
<p><!-- /wp:list --></p>
<h2>Plastic</h2>
<p>Plastic is a material used everywhere in our modern world. Each type of plastic has unique properties that we must take into account when choosing our speeds and feeds.</p>

![](/_images/_longmill/_the-basics/lm_materials_p2_Plastic.jpg){.aligncenter .size-medium}
<p><!-- /wp:paragraph -->

<!-- wp:image {"id":7257} --></p>
<p><!-- /wp:image -->

<!-- wp:heading --></p>
<h3>Acrylic / Polycarbonate</h3>
<ul>
<li>Although acrylic and polycarbonate look almost identical visually, they have different properties. Most common issue with cutting acrylic and polycarbonate is melting as they have very low melting points.</li>
<li>Reducing spindle speed can reduce heat build-up and prevent the chips from welding themselves onto your part of end mill.</li>
<li>Acrylic, with the right settings, cuts incredibly easily. Typically, standard wood cutting spiral flute end mills will work fine. However, you may choose to use single flute end mills that are designed for plastics for better cuts.</li>
<li>Polycarbonate tends to be more flexible plastic, making it more challenging to cut than acrylic. Properly securing your workpiece to prevent your material from flexing while cutting is important.</li>
<li>It is advisable to use single flute end mills on polycarbonate as well.</li>
</ul>

<h3>ABS / PVC / HDPE</h3>

<p><!-- /wp:list -->

<!-- wp:heading --></p>
<ul>
<li>These plastics are a joy to cut. With a sharp cutter, you these plastics cut like butter.</li>
<li>Standard 1/8" and 1/4" 2 flute end mills work well with these materials, you can also find special plastic cutting end mills as well.</li>
<li>If you experience melting, increase your feed rate or decrease your spindle speed.</li>
<li>These plastics can gain a static charge and stick to surfaces.</li>
<li>Laser cutting/burning PVC releases toxic gases and chemicals.</li>
</ul>

<h3>Delrin / Teflon</h3>

<p><!-- /wp:list -->

<!-- wp:heading --></p>
<ul>
<li>Low friction plastics like Delrin (POM) is also quite easy to machine.</li>
<li>Standard 1/8" and 1/4" 2 flute end mills work well with these materials, you can also find special plastic cutting end mills as well.</li>
</ul>

<h2>Foam</h2>

<p>Foam, being a super soft material, is an easy material to cut. We recommend foam as a starting material to practice CNC programming. Foam also has many useful applications, such as in packaging, RC planes, drones, and more.</p>
<p><!-- wp:paragraph --></p>
<p><!-- /wp:paragraph -->

<!-- wp:image {"id":12474} --></p>

![](/_images/_longmill/_the-basics/lm_materials_p3_Foam.jpg){.aligncenter .size-medium}
<p><!-- /wp:image -->

<!-- wp:paragraph --></p>
<p>Rigid foam is a super easy, soft material to cut. Most of the time, you can cut at full speed and full engagement with no issues, making it a fast way to draft out cuts. Soft foams come in many different densities and softness, which can affect cutting. Read more below to learn more. These settings work with both 1/8" and 1/4" 2 flute flat end mills.</p>
<p><!-- /wp:paragraph -->

<!-- wp:table --></p>
<table class="wp-table" width="70%">
<tbody>
<tr>
<td><strong>Material</strong></td>
<td><strong>Feed Rate (mm/ min)</strong></td>
<td><strong>Plunge Rate (mm/ min)</strong></td>
<td><strong>Step Over</strong></td>
<td><strong>Step Down (mm)</strong></td>
<td><strong>Spindle Speed (RPM)</strong></td>
</tr>
<tr>
<td><strong>Foam (rigid closed-cell)</strong></td>
<td>2500</td>
<td>800</td>
<td>0.7</td>
<td>6</td>
<td>10,000</td>
</tr>
</tbody>
</table>
<p><!-- /wp:table -->

<!-- wp:heading {"level":3} --></p>

<h3>Rigid foams (polystyrene foam insulation)</h3>

<ul>
<li>Because polystyrene is so soft, you can typically cut this material at full engagement. Keep your spindle speed low to prevent melting.</li>
<li>Since it's easy to cut, we recommend using it to practice CNC programming or as a drafting material.</li>
<li>Foam dust is very fine and sticks to surfaces. It is recommended to use a dust shoe.</li>
<li>Keep an eye on melted foam on your bits. You can clean them off with some acetone.</li>
</ul>

<h3>Soft foams (polyurethane)</h3>

<p><!-- /wp:list -->

<!-- wp:heading {"level":3} --></p>
<ul>
<li>Polyurethane comes in a lot of different hardnesses and densities. Because it is not rigid, it can be pushed out of the way by the end mill rather than be cut. You may need to change your cutting direction, or speeds and feeds to accommodate.</li>
<li>Consider using a corn-cob end mill, an end mill with little burred teeth rather than a standard fluted end mill. These bits take little tiny cuts out of your material rather than shaving away chips, preventing the foam from being pushed out of the way.</li>
<li>Foam dust is very fine and sticks to surfaces. It is recommended to use a dust shoe. Keep an eye on melted foam on your bits. You can clean them off with some acetone.</li>
</ul>

<h2>Aluminum</h2>

<p>Aluminum is a strong and lightweight metal used in all sort of modern applications from our bikes to our laptops. CNCing aluminum is a great option to get useful parts, especially for mechanical systems and tools.</p>
<p><!-- wp:paragraph --></p>
<p><!-- /wp:paragraph -->

<!-- wp:image {"id":7252} --></p>

![](/_images/_longmill/_the-basics/lm_materials_p4_Aluminum.jpg){.aligncenter .size-medium}
<p><!-- /wp:image -->

<!-- wp:paragraph --></p>
<p>Aluminum comes in a variety of different alloys. We will primarily be talking about 6060 aluminum, which is the most commonly used alloy. General feeds and speeds using a <a href="https://sienci.com/product/18-flat-end-mill-for-aluminum/" target="_blank" rel="noopener">1/8" single flute flat aluminum cutting end mill</a>. Please note that these settings are for basic cutting such as with <a href="http://camlab.sienci.com" target="_blank" rel="noopener">CAMLab</a> or <a href="https://grid.space/kiri#cnc" target="_blank" rel="noopener">Kiri:Moto</a> and not for adaptive toolpathing operations which have other settings.</p>
<p><!-- /wp:paragraph -->

<!-- wp:table --></p>
<table class="wp-table" width="70%">
<tbody>
<tr>
<td><strong>Material</strong></td>
<td><strong>Feed Rate (mm/ min)</strong></td>
<td><strong>Plunge Rate (mm/ min)</strong></td>
<td><strong>Step Over</strong></td>
<td><strong>Step Down (mm)</strong></td>
<td><strong>Spindle Speed (RPM)</strong></td>
</tr>
<tr>
<td><strong>6061 Aluminum</strong></td>
<td>1200</td>
<td>100</td>
<td>0.2</td>
<td>0.4</td>
<td>13,000</td>
</tr>
</tbody>
</table>
<p><!-- /wp:table -->

<!-- wp:list --></p>
<ul>
<li>Aluminum is near the upper limit of hardness that you want to be milling with a desktop hobby CNC machine. Setting up your machine to be as rigid as possible (milling near the supported areas of your rails, using proper clamping, reducing stick-out of your end mill) can make a difference.</li>
<li>The most common cause of end mill breakage is when chips build up and melt onto your bit. Ensuring that you have the proper chipload and chip ejection is important to draw heat out of the cut. Some users may choose to use coolant or compressed air to cool their cuts. Make sure to keep chips out of the cut at all times.</li>
<li>Most routers run at relatively high RPMs (10,000 to 30,000RPM) for cutting metals. Because of this, it is best to use single flute bits like our <a href="https://sienci.com/product/18-flat-end-mill-for-aluminum/" target="_blank" rel="noopener">1/8" flat end mill for aluminum</a> to ensure that you can get optimally sized chips. Also, reducing your RPM can help.</li>
<li>Some coatings, especially ones with coatings that contain aluminum (AlTiN, TiAlN), should be avoided as aluminum chips can have an affinity to the coating.</li>
<li>Using an advanced CNC CAM program such as <a href="https://www.autodesk.com/products/fusion-360/overview" target="_blank" rel="noopener">Fusion 360</a> that allows for adaptive toolpathing can speed up your cutting and give you better results, but if you're planning on cutting a lot of aluminum, it may be worth learning.</li>
</ul>
<p><!-- /wp:list --></p>
<p><!-- /wp:list --></p>
<!-- /wp:list -->