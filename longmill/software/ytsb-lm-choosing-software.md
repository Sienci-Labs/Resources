---
title: ytsb Choosing Software 🎛️
menu_order: 0
post_status: draft
post_excerpt: CNC software and toolchain explained. Recommended programs for design, CAM and machine interface for beginner and advanced users provided.
post_date: 2021-04-20 16:40:00
taxonomy:
    knowledgebase_cat: lm-software
    knowledgebase_tag:
        - mk1
custom_fields:
    KBName: LongMill CNC
    basepress_post_icon: bp-caret-right
skip_file: no
featured_image: _images/_longmill/_software/lm_choosingsoft_p1_Vectr.jpg
---

Whichever software toolchain you choose should make the most sense for you and your CNCing ambitions. A good, personalized toolchain should meet your:

- previous CNC experience
- previous design experience
- types of projects you'll be making
- budget
- and computer operating system

https://www.youtube.com/watch?v=m6ymuF8soTU

To give maximum flexibility, we made the LongMill software agnostic meaning it can accept input from nearly any software out there. Here's an example:

1. Dan has previous experience in graphic design and now he's jumped into the world of CNC routers with the goal of engraving his designs onto nice wood slabs.
1. He starts by creating his vector artwork in **Adobe Illustrator** since he's had previous experience using it for graphic design.
1. After having made the artwork, he opens it up in **Carbide Create**. He prefers Carbide Create because it's an offline software that is easy to use and capable of v-carving, a great process for cutting intricate designs with a CNC.
1. Once Carbide Create has made the machine code file, he opens it up in **gSender**. gSender is the software he uses to interface with his LongMill, allowing him to easily jog it around, set the origin point, perform probing, and he can use it to load and execute cutting files.
1. Every time gSender completes a cutting file, Dan is now able to grab his completed artwork engraving off his LongMill!

In this example, Dan used three pieces of software in his software toolchain. This allowed him to start with a program he was comfortable with for the design aspect (Adobe Illustrator), then move on to a beginner friendly CAM software (Carbide Create), before finally running the generated code file using the machine interface program (gSender). This is just one software combination of many.

To help you decide what software would work best for you we've done three things:

<ol>
<li>Created a <b><a href="#toolchain-wizard">Toolchain Wizard</a></b> which can provide you with smart recommendations after asking you 5 easy questions</li>
<li>Compiled a list of programs that we'd <a href="#our-recommendations"><b>personally recommend</b></a> for the average CNCer</li>
<li>Put every common CNC program into a <b><a href="https://resources.sienci.com/view/lm-software-table/" target="_blank" rel="noopener">Master Table</a></b> (over 80!) that you can search and filter through if you'd like to comb through all the options yourself. This table is what powers our Toolchain Wizard :)</li>
</ol>

## Toolchain Wizard

This wizard will provide you with general software suggestions based on your CNC needs. Check it out!

<div id="my-react-toolchain"> </div>
<div id="ToolTable"> </div>
<p><script src="https://resources.sienci.com/wp-content/react/wizard.js"></script></p>
<style>@import url('https://resources.sienci.com/wp-content/react/wizard.css')</style></p>

## Our Recommendations

Many of our go-to software picks tend to be available for free and can range from beginner-friendly to more advanced. We also tend to more highly recommend software that is both Design-and-CAM-in-one since that helps to streamline the process of making projects on your CNC.

**Remember that the design step in CNCing can be completely optional.** If you'd like to browse a list of sites we put together where people share their CNC project designs either for free or for a price, click the button below. Half of the projects we’ve made ourselves have been off designs we’ve found online; feel free to leverage these resources in your own work with the right permissions.

[su_button url="resources.sienci.com/view/lm-more-projects/" target="self" style="flat" background="var(--sl-blue)" color="#FFFFFF" size="8" wide="no" center="yes" radius="3" icon="" icon_color="#FFFFFF" text_shadow="none" desc="" download="" onclick="" rel="" title="" id="" class=""]Design sharing websites[/su_button]
&nbsp;

### Design & CAM (beginner-friendly)

If you're looking for software that takes advantage of most CNC features while remaining easy to pick up, we recommend checking out these software options:

<div id="divSection" style="border: 1px solid #ddd; padding: 20px 5px 0 5px; background: #fbfbfb;">

<table class="wp-table" style="height: 80px; margin-left: auto; margin-right: auto; border: 1px solid black; text-align: center; border-collapse: collapse; line-height: 1.2em; background: white;" width="95%">
<tbody>
<tr>
<td><b>Name</b></td>
<td><b>Type</b></td>
<td><b>Difficulty</b> <br />(1-4)</td>
<td><b>I want to...<br /></b></td>
<td><b>Compatibility</b></td>
<td><b>Price</b></td>
</tr>
<tr>
<td>Vectr</td>
<td><span class="redText">2D Design</span></td>
<td>1</td>
<td>Use an online tool to design simple signs and other 2D projects</td>
<td>Online</td>
<td>Free</td>
</tr>
<tr>
<td>Easel</td>
<td><span class="redText">2D Design</span>, <span class="blueText">2D CAM</span>, <span class="orgText">Int</span></td>
<td>2</td>
<td>Make signs, carve simple images, and other 2D projects</td>
<td>Online</td>
<td>Free &amp; paid</td>
</tr>
<tr>
<td>Carbide Create</td>
<td><span class="redText">2D Design</span>, <span class="blueText">2D CAM</span></td>
<td>2</td>
<td>Make signs, v-carvings, and other 2D projects</td>
<td>PC &amp; Mac</td>
<td>Free &amp; paid</td>
</tr>
<tr>
<td>Inkscape</td>
<td><span class="redText">2D Design</span>, <span class="blueText">2D CAM</span></td>
<td>3</td>
<td>Stick with something that's open source with lots of features for 2D project design</td>
<td>All desktops</td>
<td>Free</td>
</tr>
<tr>
<td>F-Engrave</td>
<td><span class="blueText">2D CAM</span></td>
<td>1</td>
<td>Use a simple 2D CAM program for engraving and v-carving signs</td>
<td>Windows/PC</td>
<td>Free</td>
</tr>
<tr>
<td>Halftoner</td>
<td><span class="blueText">2D CAM</span></td>
<td>1</td>
<td>Make halftone carvings of normal pictures onto my projects</td>
<td>Windows/PC</td>
<td>Free</td>
</tr>
<tr>
<td>Kiri:Moto</td>
<td><span class="blueText">3D CAM</span></td>
<td>2</td>
<td>Create 3D reliefs, trays, and other parts from 3D models</td>
<td>Online</td>
<td>Free</td>
</tr>
<tr>
<td>CAMLab</td>
<td><span class="blueText">3D CAM</span></td>
<td>2</td>
<td>Create 3D reliefs, trays, and other parts from 3D models</td>
<td>Online</td>
<td>Free</td>
</tr>
</tbody>
</table>

[tabby title="Vectr" open="yes"]

<b>Vectr</b> (<a href="https://vectr.com/" target="_blank" rel="noopener noreferrer">https://vectr.com/</a>)

Vectr is a simple web and desktop-based vector graphics editor that lets you draw and design online or on your desktop. Though it's not built out for CNC use, it's certainly a reasonably powerful option for beginners who want to make simple 2D designs for things like signs. It stands out because of its intuitive layout.<br>
<a href="https://vectr.com/tutorials/" target="_blank" rel="noopener noreferrer"><b>Recommended tutorial videos</b></a>

![](/_images/_longmill/_software/lm_choosingsoft_p1_Vectr.jpg){.aligncenter .size-medium}

[tabby title="Easel"]

<b>Easel</b> (<a href="https://tinyurl.com/p5eptev6" target="_blank" rel="noopener noreferrer">http://easel.com</a>)

Easel is a free (with paid pro features) web application that makes it easy to design and cut objects online. With a handful of presets for common bits and materials, as well as a simple user interface, it's an awesome program for getting started with CNCing. There are tons of guides on <a href="https://www.YouTube.com/results?search_query=easel+cnc">YouTube</a> that cover lots of different things you can do with Easel. A very simple, intuitive design and CAM program for beginners.<br>
<a href="https://www.YouTube.com/results?search_query=easel+cnc" target="_blank" rel="noopener noreferrer"><b>Recommended tutorial videos</b></a>

![](/_images/_longmill/_software/lm_choosingsoft_p2_Easel.JPG){.aligncenter .size-medium}

[tabby title="Carbide"]

<b>Carbide Create</b> (<a href="https://carbide3d.com/carbidecreate/" target="_blank" rel="noopener noreferrer">https://carbide3d.com/carbidecreate/</a>)

Carbide Create is an awesome free (with paid pro features) program that works great for 2D and 2.5D carvings, if you want to work with SVGs and DXFs, or if you're looking to do V-carving. With a much larger list of presets for common bits and materials, as well as a simple user interface and some additional features, it manages to outperform Easel in many aspects: though these advantages come with some additional complexity. Note that <b>V7 and up had g-code exporting removed, now requiring you to take the C2D file, <a href="https://my.carbide3d.com/extractgcode/" target="_blank" rel="noopener">go to this page</a>, create a login, and extract the g-code</b>. The only other option is to download an earlier version if you want to save yourself the trouble. Still, it's a good program for getting started with CNCing and similar to Easel there are tons of guides on <a href="https://www.YouTube.com/results?search_query=carbide+create">YouTube</a> to check out.<br>
<a href="https://www.YouTube.com/watch?v=pZGo8jfoOQU" target="_blank" rel="noopener noreferrer"><b>Recommended tutorial videos</b></a>

![](/_images/_longmill/_software/lm_choosingsoft_p3_Carbide.JPG){.aligncenter .size-medium}

[tabby title="Inkscape"]

<b>Inkscape</b> (<a href="https://inkscape.org/" target="_blank" rel="noopener noreferrer">https://inkscape.org/</a>)

Inkscape is a free and open source desktop tool that lets you draw vector drawings or convert regular pictures into vector format with lots of granular control. This program has been around for a long while and though it was never really meant for CNC it gets the job done using community-source plugins. There are many advanced features and tons of resources online to help you learn Inkscape.<br>
<a href="https://www.YouTube.com/watch?v=5aEcng_4sVA" target="_blank" rel="noopener noreferrer"><b>Recommended tutorial videos</b></a>

![](/_images/_longmill/_software/lm_choosingsoft_p4_Inkscape.JPG){.aligncenter .size-medium}

[tabby title="F-Engrave"]

<b>F-Engrave</b> (<a href="https://www.scorchworks.com/Fengrave/fengrave.html" target="_blank" rel="noopener noreferrer">link to site</a>)

F-Engrave is a free and open source software which provides several useful features if you are looking to do engraving work. This includes v-carving, b-carving, importing DXF and bitmap files, and more. To learn about how it works, check out the <a href="http://www.scorchworks.com/Fengrave/fengrave.html#documentation" target="_blank" rel="noreferrer noopener">documentation</a> online or watch the YouTube tutorial videos.<br>
<a href="https://www.YouTube.com/playlist?list=PLEqJxTyAwzThLLbS33drahi0B-LQhdZME" target="_blank" rel="noopener noreferrer"><b>Recommended tutorial videos</b></a>

![](/_images/_longmill/_software/lm_choosingsoft_p5_FEngrave.JPG){.aligncenter .size-medium}

[tabby title="Halftoner"]

<b>Halftoner</b> (<a href="https://jasondorie.com/page_cnc.html" target="_blank" rel="noopener noreferrer">https://jasondorie.com/page_cnc.html</a>)

The halftoner program is quite old but very simple. By importing images, you're able to chose from a selection of patterns which will enable you generate black-and-white halftone v-carves from that photo. Its use case is very limited but it's good at what it does.<br>
<a href="https://www.YouTube.com/watch?v=ovtCDXCxhkI" target="_blank" rel="noopener noreferrer"><b>Recommended tutorial videos</b></a>

![](/_images/_longmill/_software/lm_choosingsoft_p6_Halftoner.JPG){.aligncenter .size-medium}

[tabby title="Kiri:Moto"]

<b>Kiri:Moto</b> (<a href="https://grid.space/kiri#cnc" target="_blank" rel="noopener noreferrer">https://grid.space/kiri#cnc</a>)

Kiri:Moto is a 3D CAM software which allows you to create g-code toolpaths using STL files through your browser. To add to it's convenience, Onshape has support for Kiri:Moto as a plugin. This means that you can create your 3D files in Onshape and bring them into Kiri in the same browser window! Stewart Allen (the creator) is a great guy who works hard to keep the software updated and working well. It's a great and simple program for cutting 3D parts.<br>
<a href="https://www.YouTube.com/watch?v=BV8s5v1WnVc&amp;list=PLRoVgyRoWZps-MD0NigZhWNkAL6NRjXwN" target="_blank" rel="noopener noreferrer"><b>Recommended tutorial videos</b></a>

![](/_images/_longmill/_software/lm_choosingsoft_p7_Kiri.JPG){.aligncenter .size-medium}

[tabby title="CAMLab"]

<b>CAMLab</b> (<a href="http://camlab.sienci.com/" target="_blank" rel="noopener noreferrer">http://camlab.sienci.com/</a>)

CAMLab is our very own 3D CAM software which allows you to create g-code toolpaths using 3D, STL files through your browser. We've been working hard on it so that it can be easy to use while having a variety of very powerful features. Cut 2.5D profiles, and 3D reliefs with ease by generating the g-code through your browser, exporting it to your computer, and using a g-code sender like gSender to run it on your machine! CAMLab is based on <a href="https://github.com/GridSpace/apps/wiki/Kiri:Moto">Kiri:Moto</a> so Stewart Allen (the creator of Kiri:Moto) deserves a lot of credit for all his great work. Another simple program that's great for cutting 3D parts.<br>
<a href="https://www.YouTube.com/watch?v=Kx8WJ4ABFik" target="_blank" rel="noopener noreferrer"><b>Recommended tutorial videos</b></a>

![](/_images/_longmill/_software/lm_choosingsoft_p8_CAMLab.JPG){.aligncenter .size-medium}

[tabbyending]

</div>
&nbsp;

### Design & CAM (advanced)

For those that are looking to use their CNC more regularly and want to unlock its full potential. If you plan on learning 3D design for the first time, an awesome resource which teaches you how to design for CNC can be found here: <a href="https://www.hubs.com/knowledge-base/how-design-parts-cnc-machining/">https://www.hubs.com/knowledge-base/how-design-parts-cnc-machining/</a>

<div id="divSection" style="border: 1px solid #ddd; padding: 20px 5px 0 5px; background: #fbfbfb;">

<table class="wp-table" style="height: 80px; margin-left: auto; margin-right: auto; border: 1px solid black; text-align: center; border-collapse: collapse; line-height: 1.2em; background: white;" width="95%">
<tbody>
<tr>
<td><b>Name</b></td>
<td><b>Type</b></td>
<td><b>Difficulty</b> <br />(1-4)</td>
<td><b>I want to...<br /></b></td>
<td><b>Compatibility</b></td>
<td><b>Price</b></td>
</tr>
<tr>
<td>Carveco Maker</td>
<td><span class="redText">2D Design</span>, <span class="blueText">2D/3D CAM</span></td>
<td>2</td>
<td>Design baseline and reasonably advanced 2D and 3D carvings</td>
<td>Windows/PC</td>
<td>15USD/mo</td>
</tr>
<tr>
<td>Vectric VCarve Desktop</td>
<td><span class="redText">2D Design</span>, <span class="blueText">2D/3D CAM</span></td>
<td>2</td>
<td>Design baseline and reasonably advanced 2D and 3D carvings</td>
<td>Windows/PC</td>
<td>349USD</td>
</tr>
<tr>
<td>Onshape</td>
<td><span class="redText">2D/3D Design</span>, <span class="blueText">2D/3D CAM</span></td>
<td>3</td>
<td>Model in 2D or lay out complex, 3D parts with lots of granular control and plug-ins</td>
<td>Online</td>
<td>Free &amp; paid</td>
</tr>
<tr>
<td>Fusion 360</td>
<td><span class="redText">2D/3D Design</span>, <span class="blueText">2D/3D CAM</span></td>
<td>3</td>
<td>Model in 2D or lay out complex, 3D parts with lots of granular control and plug-ins</td>
<td>PC &amp; Mac</td>
<td>Free &amp; paid</td>
</tr>
</tbody>
</table>

[tabby title="Carveco" open="yes"]

<b>Carveco Maker</b> (<a href="https://carveco.com/carveco-software-range/carveco-maker/" target="_blank" rel="noopener noreferrer">link to site</a>)

Carveco Maker is Carveco's entry-level product yet it comes with quite a bit of power. It has a lot of features similar to Vectrics VCarve software such as standard toolpaths, 2D drawing, V-carving, and 3D importing but it can also create reliefs from 3D models and images and allows you to perform manual relief smoothing. This is a highly featured software that's built for semi-professional CNC use and its capabilities reflect that. It's also impressive how clean the user interface is when factoring in all the features it has. If you're interested, check out this comparison we did between Carveco Maker and Vectric VCarve Desktop: <a href="https://sienci.com/2020/11/19/vectric-vcarve-desktop-vs-carveco-maker-which-should-you-choose/" target="_blank" rel="noopener noreferrer">Vectric VCarve Desktop vs Carveco Maker – Which Should You Choose</a><br>
<a href="https://www.YouTube.com/watch?v=4f-NpoQmnCE&amp;list=PLalFSVzdLCiZKsYkrcHJr1kUYnVgX5LPs" target="_blank" rel="noopener noreferrer"><b>Recommended tutorial videos</b></a>

![](/_images/_longmill/_software/lm_choosingsoft_p9_CarvecoM.JPG){.aligncenter .size-medium}

[tabby title="VCarve"]

<b>Vectric VCarve Desktop</b> (<a href="https://www.vectric.com/products/vcarve-desktop" target="_blank" rel="noopener noreferrer">link to site</a>)

Vectric VCarve Desktop is one of Vectrics mid-level products, with products like Cut2D and PhotoVCarve being more entry-level. It has quite a lot of features similar to Carveco Maker such as standard toolpaths, 2D drawing, V-carving, and 3D importing but it's limited in that it can't modify 3D models and all projects are limited to a 24"x24" cutting size. It still has unique CAM toolpaths and has also been built for semi-professional CNC use so its capabilities reflect that. If you're interested, check out this comparison we did between Vectric VCarve Desktop and Carveco Maker: <a href="https://sienci.com/2020/11/19/vectric-vcarve-desktop-vs-carveco-maker-which-should-you-choose/" target="_blank" rel="noopener noreferrer">Vectric VCarve Desktop vs Carveco Maker – Which Should You Choose</a><br>
<a href="https://www.YouTube.com/channel/UCMrMqMabXS5_cFcq5K9Ob-w" target="_blank" rel="noopener noreferrer"><b>Recommended tutorial videos</b></a>

![](/_images/_longmill/_software/lm_choosingsoft_p10_VCarve.JPG){.aligncenter .size-medium}

[tabby title="Onshape"]

<b>Onshape</b> (<a href="https://www.onshape.com/" target="_blank" rel="noopener noreferrer">https://www.onshape.com/</a>)

Onshape is a powerful, cloud-based 3D modelling software suitable for both beginners and experienced modellers. Since it runs completely in your internet browser, you can run it on almost any modern computing device without having to download anything. Some perks are that it has a large library of user-created models and standard hardware that you can directly import, use, or edit. It also has data management features such as file versioning, and a bill of materials. Ultimately quite advanced however its CAM plugins can vary in quality.<br>
<a href="https://www.YouTube.com/watch?v=E5NKgFbP2Ig&amp;list=PL4FdDkwWXT9oY5tm3Ql5pMe8bitozQcub" target="_blank" rel="noopener noreferrer"><b>Recommended tutorial videos</b></a>

![](/_images/_longmill/_software/lm_choosingsoft_p11_Onshape.JPG){.aligncenter .size-medium}

[tabby title="Fusion"]

<b>Fusion 360</b> (<a href="https://www.autodesk.com/products/fusion-360/overview" target="_blank" rel="noopener noreferrer">link to site</a>)

Fusion 360 is one of the most popular 3D modelling and CAM combination programs used by hobbyists. It has powerful, industry-level features with the most complete CAM package for 2D and 3D cutting operations. It's free for makers and hobbyists (with some restrictions) and they offer great <a href="http://au.autodesk.com/au-online/classes-on-demand/search?full-text=&amp;productName=Fusion+360&amp;language=&amp;year=2015" target="_blank" rel="noreferrer noopener">training resources</a> as well as a <a href="https://www.YouTube.com/watch?v=Qmx5DUvvmxI&amp;list=PLmA_xUT-8UlK9rndthGGHsjjnZtPO8XRV" target="_blank" rel="noreferrer noopener">full playlist</a> which teaches every step in learning how to use the CAM part of Fusion. Fusion 360 is a great option if you're wanting to take the deep dive on CNC programming.<br>
<a href="https://www.YouTube.com/watch?v=q9qWRAAU3cs" target="_blank" rel="noopener noreferrer"><b>Recommended tutorial videos</b></a>

![](/_images/_longmill/_software/lm_choosingsoft_p12_Fusion360.JPG){.aligncenter .size-medium}

[tabbyending]
</div>
&nbsp;

### CNC Interfaces

Many of our software picks don't tend to have a built-in machine interface so we have a couple of independent programs that we've found work well. For most users, we recommend using <b>gSender</b> as the go-to interface software:

<ul>
<li>This is an open source program developed by us, Sienci Labs, which you can download for free here: <a href="https://sienci.com/gSender/" target="_blank" rel="noopener">https://sienci.com/gsender/</a></li>
<li>We used to recommend highly some other senders, but hearing about their flaws we decided to make gSender as a solution to all the feedback we received</li>
<li>Detailed instructions on how to use gSender can be found here: <a href="https://resources.sienci.com/view/gs-installation/" target="_blank" rel="noopener">https://resources.sienci.com/view/gs-installation/</a></li>
<li>gSender is designed to work right out of the box for the LongMill</li>
</ul>

The full list of grbl-compatible senders is generally maintained here: <a href="https://github.com/gnea/grbl/wiki/Using-Grbl" target="_blank" rel="noopener">https://github.com/gnea/grbl/wiki/Using-Grbl</a> but we've put together a more digestible list that you can reference below of the ones we've gone through and personally experimented with. All of these work well in most capacities and are easy to learn and pick up:

<div id="divSection" style="border: 1px solid #ddd; padding: 20px 5px 0 5px; background: #fbfbfb;">

<table class="wp-table" style="height: 80px; margin-left: auto; margin-right: auto; border: 1px solid black; text-align: center; border-collapse: collapse; line-height: 1.2em; background: white;" width="95%">
<tbody>
<tr>
<td><b>Name</b></td>
<td><b>Type</b></td>
<td><b>Difficulty</b> <br />(1-4)</td>
<td><b>Notes</b></td>
<td><b>Compatibility</b></td>
<td><b>Price</b></td>
</tr>
<tr>
<td>gSender</td>
<td><span class="orgText">Interface</span></td>
<td>1</td>
<td>A reliable and lightweight sender based on CNCjs that's easy to use and has novel expanded features</td>
<td>All desktops</td>
<td>Free</td>
</tr>
<tr>
<td>UGS</td>
<td><span class="orgText">Interface</span></td>
<td>2</td>
<td>A good default machine interface that's lightweight but has good functionality</td>
<td>All desktops</td>
<td>Free</td>
</tr>
<tr>
<td>CNCjs</td>
<td><span class="orgText">Interface</span></td>
<td>2</td>
<td>Another great interface option that can be more reliable on certain systems since it's not Java-based</td>
<td>All desktops &amp; Online</td>
<td>Free</td>
</tr>
<tr>
<td>OpenBuilds Control</td>
<td><span class="orgText">Interface</span></td>
<td>2</td>
<td>A newer software that seems to be promising in it's reliability and additional features</td>
<td>All desktops</td>
<td>Free</td>
</tr>
<tr>
<td>Easel</td>
<td><span class="redText">2D Design</span>, <span class="blueText">2D CAM</span>, <span class="orgText">Int</span></td>
<td>1</td>
<td>Works directly through Easel in your browser. Quite minimal but can get the job done</td>
<td>Online</td>
<td>Free</td>
</tr>
<tr>
<td>VTransfer</td>
<td><span class="orgText">Interface</span></td>
<td>1</td>
<td>Only packaged with Vectric products. Has almost no features so it's pretty limited</td>
<td>Windows</td>
<td>Free</td>
</tr>
<tr>
<td>bCNC</td>
<td><span class="blueText">2D CAM</span>, <span class="orgText">Int</span></td>
<td>3</td>
<td>The go-to by many when setting up their CNC to run off a Raspberry Pi. Reliable and python-based</td>
<td>All desktops</td>
<td>Free</td>
</tr>
<tr>
<td>Source Rabbit</td>
<td><span class="orgText">Interface</span></td>
<td>1</td>
<td>Based off UGS Classic, it has some additional features while remaining lightweight</td>
<td>All desktops</td>
<td>Free</td>
</tr>
</tbody>
</table>

[tabby title="gSender" open="yes"]

<b>gSender</b> (<a href="https://sienci.com/gSender/" target="_blank" rel="noopener">https://sienci.com/gsender/</a>)

This software is designed to be clean and easy to use no matter your previous CNC experience. It has a variety of features such as macros, CNC calibration, surfacing, tool changing, and firmware control. gSender supports many grbl-based machines and works out-of-the-box on the LongMill CNC.

![](/_images/_longmill/_software/lm_choosingsoft_p13_gSender.png){.aligncenter .size-full}

[tabby title="UGS"]

<b>Universal g-code Sender</b> (<a href="https://winder.github.io/ugs_website/" target="_blank" rel="noopener noreferrer">link to site</a>)

This Java-based program comes in two forms: classic and platform. Classic is easier to use and pick up, Platform has many more features and is more configurable. The software is lightweight and reliable with a pendant available, and Platform additionally has customizable windows, a good spread of plugins, and easy macros.

![](/_images/_longmill/_software/lm_choosingsoft_p14_UGS.JPG){.aligncenter .size-medium}

[tabby title="CNCjs"]

<b>CNCjs</b> (<a href="https://cnc.js.org/" target="_blank" rel="noopener noreferrer">https://cnc.js.org/</a>)

CNCjs can be built to run as a local web-app using Node.js or can be installed as a normal program onto your computer. It's got lots of great features and functionality including surface probing and easy-to-make user macros. It's got a pendant available and can be run on a raspberry pi.

![](/_images/_longmill/_software/lm_choosingsoft_p15_CNCjs.JPG){.aligncenter .size-medium}{.aligncenter .size-medium}

[tabby title="OB Control"]

<b>OpenBuilds Control</b> (<a href="https://software.openbuilds.com/" target="_blank" rel="noopener noreferrer">https://software.openbuilds.com/</a>)

Designed to work with Openbuilds CAM, it can still be used independently. Although it's not as established as the other software on this list, it's packed with some good features and is simple and colour-coordinated for improved ease of use. Pendant available.

![](/_images/_longmill/_software/lm_choosingsoft_p15a_OpenB.JPG){.aligncenter .size-medium}

[tabby title="Easel"]

<b>Easel</b> (<a href="https://easel.inventables.com/" target="_blank" rel="noopener noreferrer">https://easel.inventables.com/</a>)

Extends through the Easel online software, allowing you to connect to your machine directly through your browser. It doesn't have a lot going for it as it's purposely limited to cater towards new users, but it's usable and convenient if you're already using Easel for design and CAM. The interface aspect has no difference between the Free and Pro versions of Easel.

![](/_images/_longmill/_software/lm_choosingsoft_p2_Easel.JPG){.aligncenter .size-medium}

[tabby title="VTransfer"]

<b>VTransfer</b> (<a href="https://docs.vectric.com/docs/V9.0/Cut2DLaserDesktop/ENU/Help/VTransfer/VTransfer.html" target="_blank" rel="noopener noreferrer">https://docs.vectric.com/docs/</a>)

VTransfers <span class="sc-jrAGrp dXWCyY">barebones layout means that it's dead easy to use and understand.</span> The downsides to this is that it offers no g-code visualization, keyboard jogging, or other common interface features.

![](/_images/_longmill/_software/lm_choosingsoft_p16_VTransfer.jpg){.aligncenter .size-medium}

[tabby title="bCNC"]

<b>bCNC</b> (<a href="https://github.com/vlachoudis/bCNC" target="_blank" rel="noopener noreferrer">https://github.com/vlachoudis/bCNC</a>)

A python-based interface software and CAM utility. The main downside is that the software interface is very un-intuitive and the getting the software installed isn't beginner-friendly.

![](/_images/_longmill/_software/lm_choosingsoft_p17_bCNC.png){.aligncenter .size-medium}

[tabby title="Source Rabbit"]

<b>Source Rabbit</b> (<a href="https://www.sourcerabbit.com/GCode-Sender/" target="_blank" rel="noopener noreferrer">link to site</a>)

This program is a modified version of UGS Classic with similar functionality and a modified layout, but with some of the added features that UGS Platform has. In some areas it's been too far simplified that it reduces functionality, for instance the visualizer will only show g-code in the positive axes instead of showing the entire file.

![](/_images/_longmill/_software/lm_choosingsoft_p18_SourceRabbit.JPG){.aligncenter .size-medium}

[tabbyending]
</div>

If you've got any other questions about the CNC toolchain or need some clarification, feel free to contact us directly or ask via our Facebook and website forums.
