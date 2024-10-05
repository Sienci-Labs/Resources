---
title: ytsb Software
menu_order: 0
post_status: draft
post_excerpt: 
post_date: 2024-07-18 18:14:53
taxonomy:
    knowledgebase_cat: vx-basics vx-assembly vx-projects vx-handbook
    knowledgebase_tag:
        - vortex
custom_fields:
    KBName: Vortex
    basepress_post_icon: bp-caret-right
skip_file: yes
featured_image: _images/post-image.jpg
---

The process of creating toolpaths for the Vortex rotary axis is largely similar to that for any benchtop CNC, so if you’ve made a toolpath before, you should feel right at home with this new workflow.

We highly recommend that you use software by Vectric (<a href="https://sienci.com/product/vectric-vcarve-desktop-v11/">VCarve Desktop</a> / <a href="https://sienci.com/product/vectric-vcarve-pro-v11/">VCarve Pro</a> / Aspire) since it offers best-in-class support for rotary and is relatively inexpensive. For the purposes of this article we will focus on how to create rotary toolpaths in VCarve.

We also recommend that you use <a href="https://sienci.com/gsender/">gSender</a> as your sending software since it offers native support for the Vortex rotary axis (almost as if we built it ourselves 😃) alongside a host of other features to make your rotary experience as seamless as possible.

<img class="aligncenter wp-image-5292 " src="https://resources.sienci.com/wp-content/uploads/2023/06/Vortex-Snaggit-850x430.jpg" alt="" width="555" height="281" />

## Create Toolpaths with VCarve

The basics of using VCarve is extensively covered by <a href="https://www.vectric.com/support/tutorials/vcarve-pro?playlist=the-basics">Vectric’s official training videos</a> alongside other online resources. We especially recommend that you gain some experience importing 3D models and creating 3D toolpaths in VCarve before moving onto rotary carvings as the skills gained there are highly transferable. Having said that, we are going to assume that you know the basics of using VCarve and we are only going to highlight what makes rotary toolpathing tick in this section.

### The Concept of Wrapping

To begin with, it is important for you to understand rotary carvings as **single-sided carvings that are wrapped around a cylinder**. You still lay out your designs in 2D, but those designs are then wrapped around a cylinder when it is being previewed or carved. If you have ever carved letters or reliefs into a piece of flat material, you can imagine rolling the end results up into a cylinder and you’ve essentially got the gist of rotary carving in VCarve.

<img class="aligncenter wp-image-5296 " src="https://resources.sienci.com/wp-content/uploads/2023/06/4.p2_Sienci-1-850x483.jpg" alt="" width="643" height="365" />

### Job Setup

[caption id="attachment_5247" align="aligncenter" width="577"]<img class="nar wp-image-5247 size-full" src="https://resources.sienci.com/wp-content/uploads/2023/06/4.p3_JobSetup.jpg" alt="" width="577" height="432" /> Rotary Axis Job Setup[/caption]

When you start your project, there are a few Vortex specific settings that you should pay attention to in the Job Setup panel. In particular:

1. **Job Type** - Simply select the "**Rotary**" option. You will see it changes the options below once a bit once selected.
1. **Z Zero Position** - You should set the Z-axis zero position for your job to “**Cylinder axis**”. This helps the visualizer display toolpaths correctly and makes zeroing easier as you will have a more consistent touch off point to work with even after you have performed a roughing pass. If you try to set the Z-axis zero position to your work surface and do a roughing pass, you no longer have a reference point, since the material has been roughed away.
1. **Orientation** - You should set your job orientation to “**Along X Axis**” as this is the default orientation for the Vortex.

Your 2D view will now represent the outer surface of your material, where the height of the workspace corresponds to the circumference of your material, and the width of the workspace corresponds to the length of your material.

<img class="aligncenter wp-image-5298 " src="https://resources.sienci.com/wp-content/uploads/2023/06/4.p3_StockSize-850x722.jpg" alt="" width="575" height="488" />

### Designs in 2D

We will go over how 3D models work in VCarve in the next subsection, but we’d like to note here that you can still create some amazingly intricate designs (Such as embossing details onto a rolling pin) without using a 3D model. This is possible as you retain access to all conventional drawing tools, including the options to bring in vector files and images in rotary mode, with which you can create V-carvings, pockets and more like you would on a piece of flat material. Just remember that your designs are ultimately going to be wrapped around your stock cylinder.

[caption id="attachment_5245" align="aligncenter" width="850"]<img class="wp-image-5245 size-medium" src="https://resources.sienci.com/wp-content/uploads/2023/06/4.p5_Wrap-850x565.jpg" alt="" width="850" height="565" /> VCarving using a 2D pattern[/caption]

### Designs in 3D

See our page on “<a href="https://resources.sienci.com/view/vx-where_to_find_3d_models/">Finding 3D models</a>” for more information about where you can find 3D models to carve.

As mentioned in the “<a href="https://resources.sienci.com/view/vx-software-basics/#the-concept-of-wrapping">The Concept of Wrapping</a>” section above, VCarve operates by wrapping a flat design around a cylinder to create a rotary design. This means that even when you are importing a 3D model, VCarve will first need to “unwrap” the 3D model into a 2D image, with this representation then re-wrapped around a cylinder to form the final shape. This workflow may seem counterintuitive at first, but has major benefits for when you create toolpaths in the next step.

<img class="aligncenter wp-image-5300 " src="https://resources.sienci.com/wp-content/uploads/2023/06/4.p6_EasterIsland-1-850x780.jpg" alt="" width="624" height="573" />

The exact procedures to import a 3D model should feel largely familiar if you have imported any models to VCarve in the past, and you can brush up on those procedures with <a href="https://docs.vectric.com/docs/V9.0/VCarvePro/ENU/Help/Modeling/Import.html">Vectric’s own training materials</a> including orientation, rotation and scaling. The main difference lies with the new positioning and scaling controls which may take some getting used to.

Once your 3D model is imported, it is also a good idea to add some supporting geometry to the two ends of your model so it stays connected for the duration of the carve.

[caption id="attachment_5262" align="aligncenter" width="850"]<img class="wp-image-5262 size-medium" src="https://resources.sienci.com/wp-content/uploads/2023/06/4.p7_Head-1.jpg-1-850x455.jpg" alt="" width="850" height="455" /> Adding some material connect your material with the stock cylinder[/caption]

### Creating Toolpaths

Once you are happy with your design, you can move on to creating toolpaths for carving. Since we are dealing with an unwrapped cylinder in 2D, all of the usual carving options are available at our disposal such as 2D contouring & V-Carving, or 3D roughing & finishing. The resulting toolpaths will again simply be wrapped around a cylinder to create the final desired cuts.

<img class="aligncenter wp-image-5302 " src="https://resources.sienci.com/wp-content/uploads/2023/06/4.p8_EasterIsland-850x473.jpg" alt="" width="731" height="407" />

To improve surface finish, we recommend that you use the “Raster” strategy with a 90 or 270 degree raster angle when creating your finishing toolpaths. This setting lines toolpaths up so that they always cut across the surface of the cylinder and results in less pronounced seams.

[caption id="attachment_5264" align="aligncenter" width="322"]<img class="nar wp-image-5264 size-full" src="https://resources.sienci.com/wp-content/uploads/2023/06/Raster.jpg" alt="" width="322" height="240" /> Changing finishing toolpath strategy to Raster with either a 90 or 270 degree Raster angle will improve surface finish[/caption]

Lastly, a note on feed rate since it is interpreted differently on the rotary axis. You should not be surprised that actual carving speed is slower than what is specified. Our recommendation is for you to start with using our <a href="https://sienci.com/tool-libraries/">MK2 Feeds and Speeds</a> library and make adjustments on the fly with the feed rate override in gSender.

### Exporting Toolpaths

<img class="aligncenter wp-image-5304 " src="https://resources.sienci.com/wp-content/uploads/2023/06/4.p10_Toolpaths-850x524.jpg" alt="" width="670" height="413" />

To export your toolpaths into a g-code file, you will need to import and use a new post processor that we created for the Vortex. The new processor allows you to use A-axis commands and even allows for tool changes using the M6 command. You can download it with the link below.

<p style="text-align: center;"><a href="https://resources.sienci.com/wp-content/uploads/2023/06/Vortex-A_axis-Grbl.pp" target="_blank" rel="noopener" download="">Vortex A-axis Post Processor</a></p>

### Post Processor Installation

To install these post processors in VCarve Desktop, select **Install Post-Processor** under the Machine tab.

<img class="nar aligncenter wp-image-5651" src="https://resources.sienci.com/wp-content/uploads/2023/06/ppinstall.jpg" alt="" width="631" height="365" />

Select the **Vortex A-axis Grbl.pp** file from your recent download.

<img class="nar aligncenter wp-image-5691 size-medium" src="https://resources.sienci.com/wp-content/uploads/2023/06/PP-File-850x486.jpg" alt="" width="850" height="486" />

Now when you go to save your toolpath, you will be able to select the correct post processor for your rotary project!

<img class="aligncenter size-medium wp-image-5696" src="https://resources.sienci.com/wp-content/uploads/2023/06/vectric-pp-850x550.jpg" alt="" width="850" height="550" />

## Cue gSender

Once you have your g-code file at hand, you will want to bring the exported g-code over to gSender where you will be able to visualize the toolpath you just created.

[caption id="attachment_5239" align="aligncenter" width="850"]<img class="wp-image-5239 size-medium" src="https://resources.sienci.com/wp-content/uploads/2023/06/4.p11_FinalVisualization-850x456.jpg" alt="" width="850" height="456" /> Rotary toolpath in the main visualizer[/caption]

A “rotary” mode is also built into gSender, where you will find jog controls for the rotary axis along with options for probing and zeroing the X, Z, and A-axes. When rotary mode is enabled within gSender, this will allow for movements on your A-axis/rotary axis that are up to 8000 mm/min, allowing reasonable feed rates when cutting small diameter stock. You can see that switching the rotary slider sets $111 to 8000 in the firmware tab.

<img class="nar aligncenter wp-image-5687 size-full" src="https://resources.sienci.com/wp-content/uploads/2023/06/gSender-controls.jpg" alt="" width="348" height="310" />

The pages on “<a title="Unboxing" href="https://resources.sienci.com/view/vx-assembly2/">Unboxing</a>” and “<a title="Your First Project" href="https://resources.sienci.com/view/vx-first-project/">Your First Project</a>” will better fill the gaps on setting up your Vortex, mounting the material, and establishing a starting point. Assuming all that is already done, that last step should just be to hit “Start” and watch as your design materializes in front of your eyes!

[caption id="attachment_5312" align="aligncenter" width="1280"]<img class="wp-image-5312 size-full" src="https://resources.sienci.com/wp-content/uploads/2023/06/OwlGifGood-1.gif" alt="" width="1280" height="720" /> Running your rotary carving[/caption]

[caption id="attachment_5306" align="aligncenter" width="578"]<img class="wp-image-5306" src="https://resources.sienci.com/wp-content/uploads/2023/06/4.p16_Toolpaths-763x850.jpg" alt="" width="578" height="644" /> Completed Project[/caption]
