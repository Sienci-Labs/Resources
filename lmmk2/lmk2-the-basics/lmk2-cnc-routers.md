---
title: CNC Routers
menu_order: 2
post_status: publish
post_excerpt: What is a CNC router? What can it cut? An explanation of how the LongMill and other 3-axis CNCs work and their capabilities when creating projects.
post_date: 2022-03-17 19:42:00
taxonomy:
    knowledgebase_cat: lmk2-the-basics
    knowledgebase_tag:
        - mk2
custom_fields:
    KBName: LongMill MK2 CNC
    basepress_post_icon: bp-caret-right
skip_file: no
featured_image: _images/_longmill/_the-basics/lm_cncrouters_p1_profile.jpg
---

**Kelly has said that she'll be working on this**
Improves on https://resources.sienci.com/view/lmk2-cnc-routers/ but make the information more general about what CNCs can do more broadly

- Outline how a CNC works and moves and act as a landing page to distribute out to other common questions
- Pictures of what you can make with a CNC, examples of common projects
- Add Sally’s cutting display? Faces project
- https://www.youtube.com/watch?v=NWDrWbCbI3s CNC routers can do all that?!!?
- Good intro CNC vid inspiration https://youtu.be/ta0xnLkr4AU
- List of common costs to consider to own a CNC arranged from generally most expensive to least and gives price ranges
- That list also briefly talks about why those items are needed and then links through to full explainer pages
- Explain that CNCs can typically be used for fun and training all the way up to industry

---

https://youtu.be/pqVG3SMj99g

The many hobby CNCs are known as "3-axis CNC routers". What does that mean? Let's break the phrase down into its components:

- **CNC** → stands for “computer numerical control”; a type of machine that can be controlled by a computer using movement instructions
- **Router** → a woodworking tool that acts like a drill; it spins a cutting tool to cut through material
- **3-axis** → the ability to move in three, independent directions

Putting it all together, you get a machine with the ability to cut complex **3D objects** with a **spinning cutter** controlled by a **computer**.

The router’s motion is defined by three directions, which are straight lines called the X, Y and Z axes.

![](/_images/_lmmk2/_the-basics/lmk2_cr_longmill-labelled-axes.png "LongMill with 3 axes labelled"){.aligncenter .size-medium}

On the LongMill, the X and Y-axis movement systems are based on wheels and lead screws. The v-shaped wheels ride on the edge of the extruded aluminum profiles. This alignment allows for accurate motion while the lead screws transfer mechanical power from the stepper motors.

![](/_images/_lmmk2/_the-basics/lmk2_cr_extrusion-cross-section.png "Y-axis cross section showing extrusion and V-wheels"){.aligncenter .size-medium}

On the Z-axis, the movement system utilizes linear guides and a lead screw, where the alignment occurs between the linear rails and blocks containing ball bearings. Similar to the other axes, the motor power is transmitted by the lead screw. Since the Z-axis requires finer and more precise motion, the linear guides minimize friction while maintaining alignment in this direction.

![](/_images/_lmmk2/_the-basics/lmk2_cr_linear-guides.png "Z-axis gantry with linear guides and blocks"){.aligncenter .size-medium}

Industrial CNC milling machines take all these concepts a step further. This can involve introducing more axes (such as rotation), more powerful and repeatable drive systems, and much larger cutting volumes as well.

Whether you are using an industrial CNC mill or a hobby CNC router, they all require some way to communicate between the computer and the machine. The “language” they use is called “g-code,” which tells the CNC how to move and interact with different inputs. G-code is sent from the computer to the machine’s controller through “machine interface” software programs. Some higher end CNC machines will have a computer built into the machine to standardize the operating system and eliminate the potential for hardware incompatibilities, but most hobby machines will require the user to source the computer.

The controller is an important component of a CNC, since it is the “brains” of the whole system. It relays information from the g-code to motors, sensors, switches and other electronics to ensure the machine operates correctly and effectively. Furthermore, it stores key settings that are accessed every time the computer connects to the machine. Over the years we have designed custom controllers for the LongMill, its details are described <a href="https://resources.sienci.com/view/slb-welcome/#past-work" target="_blank" rel="noreferrer noopener">here</a>.

![](/_images/_lmmk2/_the-basics/lmk2_cr_longboard.png){.aligncenter .size-medium}
![](/_images/_lmmk2/_the-basics/lmk2_cr_slb.png){.aligncenter .size-medium}
Custom controllers we have developed: LongBoard (top), SLB (bottom)

CNC routers are quite capable when it comes to manufacturing a variety of objects. Most hobby-level machines can cut into wood, plastic, foam, machining wax, and similar soft materials. More powerful machines can also handle soft metals like aluminum, brass, and copper, to harder materials like stone, tiling, and high-carbon steels. These high performance CNC routers start to overlap with more industrial CNC milling machines.

![https://www.youtube.com/watch?v=esoMajBg37w](/_images/_lmmk2/_the-basics/lmk2_cr_medallion.png "A small aluminum medallion done on the LongMill, you can see the process here"){.aligncenter .size-medium}

The CNC operation of running a g-code file is called a “job.” Jobs can vary from simple surface engravings, profiles, pocketing, relief carvings, to using multi-orientated jigs for cutting from many sides. Most of the time, projects can be made with simple 2D cuts. To do 2D cutting, you can start with a drawing or picture, then define how each line or shape should be cut; this is called a “toolpath.” It is very common to combine multiple jobs with different toolpaths to create something highly unique and memorable.

![](/_images/_longmill/_the-basics/lm_cncrouters_p2_cuttype.jpg "A circular design with different toolpaths: Surface cut, v-carve, profile cut, pocket cut, inner contour, outer contour, 2-sided cut"){.aligncenter .size-medium}

![](/_images/_longmill/_the-basics/lm_cncrouters_p5_GregChar.jpg "Simple V-carve engraving on a wood cookie")"{.aligncenter .size-medium}

The world of 3D carving allows you to create even more intricate objects, if you choose to explore this path. Depending on how complicated your project is, it may require a more advanced understanding of software and CNC workflows to successfully execute it. For example, if you are looking to create your own design, rather than find a 3D file online, you may need to learn how to use CAD (computer-aided design) software. Or if you wish to create a two-sided project, you will need to precisely flip and re-align the material after the first side is completed. Nevertheless, 3D carving leads to impressive results, so it is definitely worth trying out! A simple relief can be a great starting point for 3D carving.

![https://www.facebook.com/photo/?fbid=10228679990316969](/_images/_lmmk2/_the-basics/lmk2_cr_dan-h-clock.png "Clock by Dan H, showing relief cutting, pocketing, and profile cutting techniques"){.aligncenter .size-medium}

https://www.youtube.com/watch?v=yOywuK02vVY

So now that we discussed the technical capabilities of the CNC router, what sort of items can it produce? From charcuterie boards and cabinetry, to engraved glasses, light up acrylic signs and aluminum motorcycle parts, there’s a whole lot that can be made. Below are some examples of pieces made on the LongMill by our wonderful customers.

![https://www.facebook.com/groups/mill.one/permalink/1725026821301975/](/_images/_lmmk2/_the-basics/lmk2_cr_john-h-halftone.jpg "Painted wood carving using halftone technique, by John H"){.aligncenter .size-medium}

![https://www.facebook.com/photo/?fbid=10160581502397841](/_images/_lmmk2/_the-basics/lmk2_cr_pierre-g-cribbage-board.jpg "Cribbage board, by Pierre G"){.aligncenter .size-medium}

![https://www.facebook.com/photo?fbid=10160431292339019](/_images/_lmmk2/_the-basics/lmk2_cr_travis-w-wooden-epoxy-tray.jpg "Epoxy-filed walnut tray, by Travis W"){.aligncenter .size-medium}

![https://www.facebook.com/photo?fbid=10231810552434595](/_images/_lmmk2/_the-basics/lmk2_cr_bob-e-cabinetry.jpg "Alder cabinetry panels, by Bob E"){.aligncenter .size-medium}

![https://www.facebook.com/photo/?fbid=10230445081293976](/_images/_lmmk2/_the-basics/lmk2_cr_myerin-relief.jpg "Poplar crocodile relief carving, by Myerin P"){.aligncenter .size-medium}

![https://www.facebook.com/photo/?fbid=3383114785337155](/_images/_lmmk2/_the-basics/lmk2_cr_michael-k-candle-boat.jpg "Candle boat made by cutting 4 sides of the stock material, by Michael K"){.aligncenter .size-medium}

![https://www.facebook.com/photo?fbid=3426016330999058](/_images/_lmmk2/_the-basics/lmk2_cr_bill-tiling-sign.jpg "11’ Birch sign using tiling method, by Bill I"){.aligncenter .size-medium}

![https://www.facebook.com/reel/8556613297736489](/_images/_lmmk2/_the-basics/lmk2_cr_jim-h-diamond-drag-bit-engraving.jpg "Shot glasses engraved using diamond drag bit, by Jim H"){.aligncenter .size-medium}

![https://www.facebook.com/groups/mill.one/permalink/1926172041187451/](/_images/_lmmk2/_the-basics/lmk2_cr_dan-h-acrylic-engraving.jpg "Acrylic light-up lake engraving, by Dan H"){.aligncenter .size-medium}

![https://www.facebook.com/groups/mill.one/permalink/1951575691980419/](/_images/_lmmk2/_the-basics/lmk2_cr_shawn-m-aluminum-cutting.jpg "Aluminum 6061 motor scooter parts, by Shawn M"){.aligncenter .size-medium}

![https://forum.sienci.com/t/september-2-september-9-2022-a-project-that-isnt-made-from-wood-contest/6669/3](/_images/_lmmk2/_the-basics/lmk2_cr_nicolas-aluminum-composite-sign.jpg "Aluminum-plastic composite signage, by Nicholas"){.aligncenter .size-medium}

![](/_images/_lmmk2/_the-basics/lmk2_cr_lino-block-cutting.png "Lino block cut using the LongMill, by Scott Saari"){.aligncenter .size-medium}

Now that you know what a CNC router is and what it's capable of, you should be able to get an idea of how you might use your own LongMill to make parts or projects for your home or business. The next pages should act to further deepen your knowledge on the primary concepts of CNC routing.
