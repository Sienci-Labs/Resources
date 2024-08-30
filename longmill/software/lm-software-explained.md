---
title: Software Explained 🗣️
menu_order: 4
post_status: publish
post_excerpt: The CNC software process starts from creating a design (CAD), making toolpaths to produce g-code (CAM), sending the g-code to the LongMill (machine interface).
post_date: 2021-04-20 16:36:00
taxonomy:
    knowledgebase_cat: lm-software
    knowledgebase_tag:
        - mk1
custom_fields:
    KBName: LongMill CNC
    basepress_post_icon: bp-caret-right
skip_file: no
featured_image: /_images/_longmill/_software/lm_choosingsoft_p2_Easel.JPG
---

The core concepts behind operating a CNC router are very basic. A close analogy would be as follows:

*Imagine that you've got a friend with a very steady set of hands who's decided they want to help you on your next woodworking project. They're holding tightly onto a trim router and are able to move it very precisely to any location within a limited space; they just need you to say exactly where you need them to move. Clearly your friend is very generous and skilled but all you've got is a sketch on a piece of paper, so how are you going to be able to describe what you need them to cut out?*

*With the necessary planning, you figure out a way to convert your project idea on paper into a list of precise directions, similar to planning a road trip by combining the GPS coordinates of all the places you'd like to visit. You can now instruct your friend on how to re-create your project to your exact specifications by simply listing these directions to them.*

In that analogy, your friend is effectively acting as a <b>CNC router</b>. Given all of the strengths that a CNC has, it can't do anything productive unless you provide it with a list of instructions so that it knows where to cut. So how do you go about making cutting instructions that a CNC would understand?

## The CNC Toolchain

A 'toolchain' leverages one or more software packages to accomplish an end goal. Today, our end goal is to figure out how to go from a design for a project to having this project cut out on our CNC. This process spans three major steps:

<ol>
  <li>Get your project idea into a form that a computer can understand (or buy/download a CNC project that's already been designed)</li>
  <li>Use a <b>CAM software</b> to help turn this project into a list of cutting instructions for your CNC called a <b>g-code file</b></li>
  <li>Use a <b>machine interface software</b> to talk to your CNC, telling it where you've placed your raw material and giving it the cutting instructions</li>
</ol>

There is software that can cover all of these steps, but most times you'll have to use at least two software packages to take you from start to finish. Let's go through each step in a little more detail.

### 1. Design Software

This first step is the only one where software is optional. This may sound strange at first, but the design process is meant to act as a bridge between an idea for a project and somehow feeding that idea to a computer program. This means that if you're able to find a design online that is already similar to an idea you had for a project, you can simply buy or download the files and move on to Step #2.

If you plan on making your own design from scratch, your idea might stem from a:

<ul>
  <li>picture you find online</li>
  <li>hand drawing</li>
  <li>vector design or graphic</li>
  <li>engineering drawing</li>
  <li>3D model, and more!</li>
</ul>

All these inputs are quite different from each other which is why design programs come in many forms and can largely be separated in two main categories: 2D design and 3D design.

<b>2D design</b> is largely considered to be an easier starting point for first time CNCers since it mostly consists of laying out simple shapes, pre-made artwork, and occasionally some graphics that you find online. Not only is this design process easy to learn, but it's also very versatile. By making these simple line drawings you can make signage, lettering, flat-packed furniture, joinery, inlays, stencils, household items, etc. The majority of the cutting you're looking to do on your CNC will probably be covered by 2D work (typically SVG, DXF, PNG, JPEG, or BMP files).

The more complex <b>3D designs</b> aren't for everyone, but the result is certainly impressive. By cutting out intricate contoured patterns on the CNC, the result is a perfect looking carving job that's done in a couple hours rather than the weeks of hand-work that it would normally take. The caveat here is that learning to create 3D models is another step above the 2D design work and has a much longer learning curve (typically STL, OBJ, STEP, or IGES files). The process of making g-code for 3D models is also usually much more difficult than for cutting out 2D drawings.

All of this is to say that if you want to carve something out, you first need to know what you're going to make and how you're going to make it. Whether it's a picture, a 3D model, or even a napkin drawing; you must find a way to convey your ideas in a form that's shareable and outside of your head.

### 2. CAM Software

As previously mentioned, <b>CAM software</b> is the tool that you use to take the design you have and turn it into a g-code file which acts as a set of cutting instructions for the CNC to follow. It does this by accepting certain inputs from you, including:

<ul>
  <li>the design file from the previous step</li>
  <li>information about your CNC</li>
  <li>the type of material you plan on cutting and its general dimensions</li>
  <li>the cutting tool (or tools) you plan on cutting the material with</li>
  <li>some more details about how you'd like to carve your project out</li>
</ul>

The CAM step is quite straightforward, just ensure that you're not sloppy in providing the correct information to the software since it will always follow your inputs exactly and create the cutting instructions accordingly. The type of CAM program you use will vary based on:

<ul>
  <li>whether you are using 2D or 3D models</li>
  <li>your budget (either using free CAM or paid CAM programs)</li>
  <li>if you require basic or advanced functionality</li>
</ul>

Some CAM software are made to only accept 2D design files, others only accept 3D design files, and a small subset can accept images straight from the internet.

### 3. Machine Interface

Coming through the CAM process and with g-code file in hand, the last step is to set up your machine and run your cutting instruction by using an <b>Interface Software</b>. This software is run on your computer or laptop and allows you to:

<ul>
  <li>manually move / jog each axis of the CNC</li>
  <li>set the starting point of the cut (either via limit switches, touch probe, work coordinate offsets, or manually)</li>
  <li>send / live-stream cutting instructions to the LongMill</li>
  <li>pause or resume cutting, or stop cutting altogether</li>
</ul>

Think about this last step as your ultimate window into controlling and monitoring your CNC. For many individuals this last step will only really involve telling the CNC where you'd like to start cutting and then executing the file which holds all the cutting instructions; but many interfaces will allow you to do much much more than this if you're comfortable with it:

<ul>
  <li>check the g-code instructions looks correct via a visualizer</li>
  <li>override the instructions while they're being sent if you need to make the CNC run faster or slower</li>
  <li>use more advanced probing techniques</li>
  <li>perform code warping to contoured surfaces</li>
  <li>change and view firmware settings</li>
  <li>use and program custom macros</li>
  <li>And more!</li>
</ul>
