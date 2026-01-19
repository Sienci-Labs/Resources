---
title: Cutting Tools
menu_order: 4
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
featured_image: _images/_cnc-fun/_the-basics/cnc_ba_cuttingtools_p1-tip-types.jpg
---

https://www.youtube.com/watch?v=VqJVRo_KdJs

CNC routers work by using a rotating cutting tool to cut or carve away materials in order to create the final object. Different cutting tools are used for different types of projects and applications. They can vary in size, shape, material, and design; and are sometimes also referred to as cutting bits or end mills.

Most CNC cutting tools can be thought of like drill bits. However, not only can these cutting tools drill downward like drill bits, they can usually cut side-to-side as well; this enables the CNC router to be 3D carving machine rather than just a drilling machine. In order to provide you with an understanding of the variation in features that these cutting tools can have, each of the tabs below address one of the major features which can be accounted for when deciding on which tool you need for your project.

Choosing bits is very much a learning process just as learning to use certain blades on other tools, so if you wish to skip to our Recommendations below then please check it out as we've tried to assemble a list of starter bits for a handful of applications.

## Learning

[tabby title="Tip Shape" open="yes"]

The biggest difference in cutting tools is their tip shape, this determines what application the bit can be used for. The three most common types are the **ball nose**, **flat end**, and **v-bit** (shown below respectively).

![](/_images/_cnc-fun/_the-basics/_cuttingtools/cnc_ba_cuttingtools_p1-tip-types.jpg){.aligncenter .size-medium}

**V-bit:**  v-bits have an angled tip that works great for engraving. They come in varying angles so that if you're cutting a line with a certain thickness then a 60° bit will cut that line deeper than a 90° bit will; this variation can be used to great effect.

![](/_images/_cnc-fun/_the-basics/_cuttingtools/cnc_ba_cuttingtools_p2-vbits.jpg){.aligncenter .size-medium}

V-bits can be used for simple line-drawing engravings and are also commonly used for "v-carving" which varies the height of the bit as it cuts to change the width of the engraving. This can create detailed images and can also be used for stippling.

![](/_images/_cnc-fun/_the-basics/_cuttingtools/cnc_ba_cuttingtools_p3-wave.jpg){.aligncenter .size-medium}

Here is a detailed chart, illustrating how you can get finer detail, with a smaller angle V-bit. In these examples, the <span style="color:red;">RED</span> dots represent an exaggerated vector line, while the <span style="color:blue;">BLUE</span> dots show the cut depth.

This first image from [Learnyourcnc.com](https://www.learnyourcnc.com/blog/cnc-tip-understanding-vcarving) shows that using the same depth of cut will produce different cut width, depending on the bit you choose. A smaller bit is better for vector lines that are close together, to offer more detail.

![](/_images/_cnc-fun/_the-basics/_cuttingtools/cnc_ba_cuttingtools_p9-Vcarves1.jpg "learnyourcnc.com"){.aligncenter .size-medium}

This second image shows that using a V-bit on similarly spaced vectors, will produce different cut depths, based on  your V-bit choice. In this case, smaller bits will carve deeper, on similar vectors.

![](/_images/_cnc-fun/_the-basics/_cuttingtools/cnc_ba_cuttingtools_p9-Vcarves2.jpg "learnyourcnc.com"){.aligncenter .size-medium}

Not only do you set your vector line width and cut depth in your design software, but you can also set a flat depth. A flat depth will prevent the V-bit from cutting any deeper than specified, best used when your vector lines are farther apart than the bit you are using.

![](/_images/_cnc-fun/_the-basics/_cuttingtools/cnc_ba_cuttingtools_p9-Vcarves3.jpg "learnyourcnc.com"){.aligncenter .size-medium}

**Flat end:**  this type of end mill simply has a flat or "square" tip profile and normally comes in the form of a spiral bit, but rabbit and dado bits also fall under this category. These cutting tools are the most common of any type due to their versatility for rapid material removal, pocketing, and generally being able to do most CNC projects you may have in mind. At the very least they come in handy if you're considering levelling a large cut of material or need to cut the outer profile of a sign to separate it from the stock material.

![](/_images/_cnc-fun/_the-basics/_cuttingtools/cnc_ba_cuttingtools_p4-wood-box.jpg){.aligncenter .size-medium}

Flat end mills come in several different configurations. Upcut, downcut and compression bits all move chips a bit differently and can affect edge quality.

- An **Upcut** bit will pull chips upwards, resulting in a clean bottom or pocket, and great chip evacuation. The downside is it can cause tear out at the surface. Great for slots and deep pockets.
- A **Downcut** bit pushes chips downward, leaving a clean top edge but packing chips in the cut, so it’s best for shallow passes and profiles.
- A **Compression*** bit combines both (downcut at the top, upcut at the bottom), producing clean edges on both the top and bottom surfaces, making it ideal for plywood and laminated sheet goods in hobby CNC work when cutting all the way through. This image from [findbuytool](https://www.findbuytool.com/en-ca/blogs/university/choosing-the-ultimate-spiral-router-bit-up-cut-vs-down-cut-vs-compression?srsltid=AfmBOorpQR-j7DaakOrd__wFvJ66N7MmvcC_JZWZ41pBj8n2pPWsxJbZ) does a great job of showing what each bit type does and how it moves the chips.

![](/_images/_cnc-fun/_the-basics/_cuttingtools/cnc_ba_cuttingtools_p8-updowncompress.jpg "www.findbuytool.com"){.aligncenter .size-medium}

**Ball nose:**  great for 3D / relief carving where your project contains contoured surfaces. By stitching many close passes of its rounded profile together the result can be a perfectly smooth, curved surface right off your machine.

![](/_images/_cnc-fun/_the-basics/_cuttingtools/cnc_ba_cuttingtools_p5-3d-foam.jpg ){.aligncenter .size-medium}

A tapered ball nose bit has the same rounded tip but with tapered (angled) sides, which makes the tool much stiffer. You’d use it for deeper 3D carving, detailed work, and harder materials, where reduced deflection, better accuracy, and cleaner results are important. The trade-off is that the taper limits how close the tool can get to steep vertical walls compared to a straight ball nose. All this being said, one aspect these bits can't handle is flat surfaces due to the "scalloping" they introduce. This type of carving is certainly more advanced than others but at the end of the day it certainly adds an extra dimension to your projects.

![](/_images/_cnc-fun/_the-basics/_cuttingtools/cnc_ba_cuttingtools_p10-taperedballnose.jpg){.aligncenter .size-medium}

[tabby title="Size"]

The size of a cutting tool is important because if it's too big then it might not be able to cut to the level of detail that you need, and if it's too small then it might take forever to cut everything away. You can check by using the visualizer tool on your CAM software to see whether your bit is able to do the finer cuts. Typically, simple jobs can be done with 2 different bits, one bit used to remove the majority of the material and the other bit used to define the details.

Cutting tools can normally be described by a few key dimensions:

![](/_images/_cnc-fun/_the-basics/_cuttingtools/cnc_ba_cuttingtools_p6-end-mill-feat.jpg){.aligncenter .size-medium}

**Cutting diameter:**  the diameter of the cutting end of the tool. For ball nose bits it's the diameter before the rounded profile and for v-bits it's usually the largest diameter of the 'v' profile. The size of this determines your tools ability to remove material.

**Cutting length:**  the length of cutting profile that the bit has. This length determines the maximum height of material that can be 'engaged' with your bit while cutting, however most of the time when making slotted profile cuts it's a good rule of thumb to cut down half of the cutting diameter at a time.

**Shank diameter:**  this is where your router or spindle will be holding onto the bit, through a collet. For small diameter bits (⅛”), you may need to use an adapter which acts as a sheath, allowing you to clamp the small bit.  

**General rules:**

- Use the largest diameter cutting tool you can bear if you don’t mind the lack of detail and want to remove material quickly. For most CNC's this is going to be in the range of 1/4" to 1/2"
- Long tools can make deeper cuts but usually deflect more and affect surface finish, try to use the shortest tool you can or mount it deeper into the router

[tabby title="Flutes"]

The flutes on a cutting tool have a dual purpose of cutting/shearing material off of the stock and evacuating these material 'chips' from the cutting area. It's important for the chips to be moved away during the cutting process since they're a primary mechanism for keeping the cutting area cool as they carry heat away with them; they can also jam the tool up or wear it out prematurely if they stick around.

Cutting tools can have any number of flutes on them, but the most common are 1-flute, 2-flute, and 4-flute. Due to the capabilities and rigidity of most CNC routers, a good general rule is that you should use tools with less flutes if you want to cut material away faster or if the material is prone to melting or 'gumming up' when cut (this includes soft metals and plastics). More flutes are necessary for your surface finish if you're making a final cutting pass on harder materials and are removing just a small amount of material.

**General rules:**

- 2-flute bits are going to work for most jobs and materials. 4-flute bits are hardly used on CNC routers and 1-flute bits only become necessary when cutting aluminum, other soft metals, or some plastics.
- For softer materials and woods, the spiral direction of the flutes will have a large impact on the surface finish of the material. "Up-spiral" or "**up-cut**" bits pull the chips out the top of the material which helps with chip evacuation but can cause fuzziness or burring to appear on the top edge as well. "Down-spiral" or "**down-cut**" bit are the opposite, pushing the chips down into the cut. This seems bad since the chips aren't able to escape, but in certain situations they are advantageous to use if you want to avoid tear-out or burring on the top of the material.

One area where both up-cut and down-cut bits fall short is that when cutting thicker sheet material at full depth, they will cause tear-out on either the top or the bottom; the solution to avoiding this is a "compression" bit. Compression bits are a combination up-cut and down-cut bit which pulls both sides of the material towards the center. The only challenge is making sure the tool enters the cutting path correctly otherwise the up-cut half could pull up the material while the tool is still moving into position.

There are also many router bits which don't have spiral flutes at all. The differentiation here is that the whole cutting profile is being engaged at once which will increase the cutting forces, and the lack of spiral means that you shouldn't make deep cuts since the chips can't be pulled up and out of the cutting area.

[tabby title="Advanced"]

As a CNC operator, you will learn to choose the correct end mill for the job and use the correct speeds and feeds in your CAM program to get the best results in your project. As you start to dive into the world of cutting tools you'll start to see how their geometry, material characteristics, and performance can become very nuanced from tool to tool. Two of the largest additional factors which weren't previously mentioned are the tools material composition and its coating. Below will be an introduction to these topics:

### Composition

Cutting tools can be manufactured out of a variety of material which are all engineered to be able to sustain high loads during the cutting process and remain sharp enough in order to shear the material away from the stock. Of these, the most commonly used materials are high speed steel (HSS) and solid carbide.

![](/_images/_cnc-fun/_the-basics/_cuttingtools/cnc_ba_cuttingtools_p7-hss-carbide.jpg "Solid carbide vs. HSS cutting tool"){.aligncenter .size-medium}

HSS usually combines with a variety of other alloys to have a high wear resistance and durability for cutting both soft and hard materials. Since HSS is softer than solid carbide it’s less likely to crack and instead wears out over time, so it’s limited to slower cutting speeds. HSS tools are also usually much cheaper than solid carbide tools and can be additionally improved if they come with a coating.

Solid carbide tools are very hard so they’ll stay sharp for longer and won’t wear as much at higher temperatures. Recently, carbide tools have become much cheaper and accessible for use in CNC routing, however it’s important to note that carbide cutting tools typically require higher speeds in order to mill properly. This makes them a great candidate for cutting finishing passes, milling PCBs, and cutting materials that won’t easily burn or melt.

### Coatings

Carbide cutting tools have the ability to be covered in fancy coatings like DLC (Diamond-Like-Carbon), TiN (titanium nitride), TiCN (titanium carbonitride), TiAlN (titanium aluminum nitride), and AlTiN (aluminum titanium nitride). All of these coatings can enhance the tool's abilities by increasing its wear resistance, making it more thermally stable, lowering its coefficient of friction, or increasing its ductility.

For more non-abrasive materials, coatings will only have an affect on the lifetime of the bit. However, for ultra-precision machining or when milling carbon fiber or hard metals, the wear resistance introduced by these coatings are worth their added cost. For this reason, most CNC router work doesn't require a deep knowledge on cutter coatings since it usually becomes more applicable when cutting metals.

**In summary:**  if you're on the lookout for a reliable set of cutting tools, make the jump and invest carbide or coatings if the application makes sense. Otherwise, if you're on a tight budget or you're still learning how to use your machine then hold onto your money for the time being.

### Advanced Bits

There are more end mills than the 3 main types we've covered (Flat end, ball nose & v-bit). You can find bits that specialize in surfacing your wasteboard or project, roughing out toolpaths before the final finishing pass, creating bowls and even rounded over corners. Check out our selection of basic and advanced [End Mills & Bits!](https://sienci.com/product-category/end-mills-bits/)

![](/_images/_cnc-fun/_the-basics/_cuttingtools/cnc_ba_cuttingtools_p11-advancedbits.jpg "Pictured is a surfacing bit and a bowl bit")

### More

In case you're feeling curious, there's many more resources out there which provide plenty of information on the ins and outs of cutting tools. Here are a few that we've documented:

- <a href="https://m.all3dp.com/2/guide-to-cnc-router-bits-all-you-need-to-know/" target="_blank" rel="noopener noreferrer">2019 Guide to CNC Router Bits: All You Need to Know</a>
- <a href="http://makezine.com/2014/09/10/endmills/" target="_blank" rel="noopener noreferrer">Makezine- The Skinny on Endmills</a>
- <a href="http://www.cnccookbook.com/CCCNCMillingCutters.html" target="_blank" rel="noopener noreferrer">CNC Cookbook- End Mill Guide</a>
- <a href="http://lcamtuf.coredump.cx/gcnc/ch2/" target="_blank" rel="noopener noreferrer">Guerrilla guide to CNC machining- Stocking up on End Mills</a>
- <a href="http://www.tinkerandfutz.com/a-guide-to-cnc-bits/" target="_blank" rel="noopener noreferrer">Tinker and Futz- A Guide to CNC Bits</a>
- <a href="http://www.cnczone.com/forums/diy-cnc-router-table-machines/150821-router-bits-endmills-pictures-descriptions-uses.html" target="_blank" rel="noopener noreferrer">CNC Zone- Router Bits and End Mills</a>
- <a href="https://en.wikipedia.org/wiki/Milling_cutter" target="_blank" rel="noopener noreferrer">Wikipedia- Milling Cutter</a>
- <a href="https://www.shapeoko.com/wiki/index.php/Endmills" target="_blank" rel="noopener noreferrer">Shapeoko Wiki- End Mills</a>
- <a href="http://www.hannibalcarbide.com/technical-support/titanium-coatings.php" target="_blank" rel="noopener noreferrer">Hannibal Carbide Tool- Titanium Coatings</a>

[tabbyending]

## Recommendations

Below we've put together a list of bit recommendations based on the use case they're being used for:

- **Bulk material removal & simple cuts:** get a surfacing bit for flattening material blanks, some dado bits, and some 1/4" end mills
- **Lots of plywood work:** get some downcut end mills (regular ones are upcut) or compression bits to avoid splintering
- **Sign making:** most of the time a 60° and 90°, 1/4" shank v-bit and an end mill is all you need
- Intricate contour and relief cuts (3D carving): look into getting small, 2-flute ball or tapered end mills, these can range from 1/8" to being smaller than 1mm
- **Small work and engraving:** you can probably stick to square or ball end 1/8" bits and smaller v-bits
- **Metal cutting:** pick up some reasonable single-flute cutters with an advantageous coating; also keep in mind that when it comes to aluminum cutting, the larger you can bear to make your cutting tool, the greater the material removal rate can be and the less likely it'll be for the bit to get clogged up with metal and snap as a result

**Be careful when buying tools that the price tag isn't far above what the average prices are. As a first time CNC'er, it's usually not worth the investment into expensive cutting tools since you'll probably be breaking or damaging bits during the learning process. As far as brands are concerned, most types will work whether is a local or online supplier, but starting off  with the cheaper no-name brand stuff has the benefit that it can be broken without a second though, even if it usually can't hold an edge over the long-term.

After some time, if you find yourself looking at tools with a price tag in the hundreds, then this is probably a good indicator that you should consider upgrading to a new machine.
