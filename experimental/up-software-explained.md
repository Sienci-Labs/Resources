---
title: Software Extra Explanations (Working title)
menu_order: 4
post_status: draft
post_excerpt: 
post_date: 2024-09-10 10:30
taxonomy:
    knowledgebase_cat: 
    knowledgebase_tag:
        
custom_fields:
    KBName: 
    basepress_post_icon: bp-caret-right
skip_file: yes
featured_image: 
---
Goes over the basics or posts existing good guides on a variety of packages people tend to use

What type of files do I need?

For 2D work, .svg files are good. Try to stay away from .dxf if you can. Much depends on the source of the files, too. Quality can be sketchy from some vendors. For 2.5D and 3D work, .stl files are a sort of standard in “store bought” files. Again, quality will depend on the vendor.

In terms of CAD/CAM applications, Vectric products are a good bet, IMHO. Also, IMHO, getting VCarve Desktop for an AltMill would not be a good choice. Why buy a 4 x 4 machine, then buy software that limits you to a 25 x 25 material size? You can always tile them, but . . . Down the road, you may decide that you want to create your own 3D models. In Vectric products, this will require Aspire. Pricey. The good part of starting out with VCarvePro is that, if you decide to upscale to Aspire, you get full credit for the purchase price of VCarvePro.

https://all3dp.com/2/cnc-vector-formats-simply-explained/

https://www.core77.com/posts/67499/Understanding-the-Different-Types-of-3D-Files

https://www.adobe.com/creativecloud/file-types/image/vector/stl-file.html

https://www.jett3d.com/blog-jett-3d/the-ultimate-guide-to-the-most-popular-3d-printing-file-types

I've been developing software as an alternative to the pricey ones out there that are popular like V-Carve, ArtCAM/Carveco, and the like. It also does things a little differently for those who have more of a background in and familiarity with graphics design rather than CAD and manufacturing. Most programs operate on 2D vectors or 3D models as input where my strategy was to make it easier to use images for a project, but now it's able to handle loading and compositing images, vectors, and models together into a project's design and generating toolpaths for all kinds of projects - not just relief carvings like you have found here.

The main things you'll need to tackle are acquiring a machine (i.e. building from a kit of many pieces and parts, finding one that's already built and delivered whole or in a few pre-assembled pieces, or designing and piecing one together from scratch) and learning how to drive it to cut projects out by running CNC G-code on it. You'll need to learn a program for designing a project and generating toolpaths for it for different cutters to progressively remove material from a piece of material to transform it into the desired product. This is another set of expertise to pickup - what cutters to use and why, how wide and deep of a cut to take, how fast it should spin, how fast it should move through the material, etc...

The software for designing a project and generating toolpaths is only a piece of the puzzle! My software is called PixelCNC and it's come a long way since the first release but it and other CAM software will only get you so far without the other things you need to be able to do projects like this. I'd suggest looking up tutorials on making CNC signs and art that explain the different aspects of the process.