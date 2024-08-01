---
title: ytsb Table Mounting 📐
menu_order: 4
post_status: draft
post_excerpt: How to mount the LongMill onto your wasteboard and table, with tips on squaring and alignment. Machine dimensions and wasteboard material suggestions provided.
post_date: 2024-04-30 16:54
taxonomy:
    knowledgebase_cat: lm-assembly
    knowledgebase_tag:
        - mk1
custom_fields:
    KBName: LongMill CNC
    basepress_post_icon: bp-caret-right
skip_file: no
featured_image: 
---
<img class="size-medium wp-image-1174 aligncenter" src="https://resources.sienci.com/wp-content/uploads/2021/05/7-01-cover-850x697.jpg" alt="" width="850" height="697" />

The LongMill is designed to be mounted to a flat surface which is provided by the user. This could be as simple as a single sheet of material, or as intricate as a multi-piece torsion table with t-tracks and threaded inserts. One thing is to ensure that you’ve got a flat sheet (or multiple flat sheets) of material within the cutting area of the machine. This “wasteboard” area is where the material you will cut will sit on and serves to be cut into and replaced when needed.

<img class="size-medium wp-image-1181 aligncenter" src="https://resources.sienci.com/wp-content/uploads/2021/05/7-08-850x477.jpg" alt="" width="850" height="477" />

We do not ship LongMills with a wasteboard because:
<ol>
 	<li>It saves the cost for shipping. For example, a 4ftx4ft piece of 3/4” MDF shipped often costs over a hundred dollars in shipping and is very easy to damage during transit. You can usually find a full 4ftx8ft sheet of 3/4” MDF for under $60 at your local lumber or hardware store.</li>
 	<li>Users can choose the size and material of the wasteboard to match their needs.</li>
</ol>
<h2>Suitable wasteboard materials</h2>
The easiest setup that we recommend is a flat, clean piece of 3/4” MDF to act as your mounting surface and your wasteboard. This is because 3/4” MDF is quite stiff and is readily accessible in 4’x4’ and 2’x2’ sizes from most big- box hardware stores or a lumber store. Any similar piece of thick, flat material would also suffice; you can choose at your own discretion. If you’re looking for more of a flashy setup, you can check out some of our community members’ table/wasteboard builds here for inspiration: <a href="https://sienci.com/dmx-longmill/community-table-builds/">https://sienci.com/dmx-longmill/community-table-builds/</a>
<h2>Machine Dimensions</h2>
When getting ready to mount your LongMill, the most important dimensions you’ll need to know are the size of its foot base and the total outline of the machine. As long as your mounting surface is at least the size of the foot base and you’ve left enough space around your mounting surface to account for the total machine outline, then your setup will be suitable.

<img class="size-medium wp-image-1176 aligncenter" src="https://resources.sienci.com/wp-content/uploads/2021/05/7-03-850x468.png" alt="" width="850" height="468" />

The control box is also something you should plan for, as the design of the machine favours placing the control box on the left side of the machine whether it’s sitting on the table or mounted to the side or underside of the surface. The control box has buttons on the top which can Play, Pause, and Stop the machine’s motion so it’s a good idea to keep it mounted near your CNC. It also has a USB input on the left side, motor and other outputs on the right side, and the power input on the back side, so make sure to keep some space around it for cable management.

<img class="size-medium wp-image-1177 aligncenter" src="https://resources.sienci.com/wp-content/uploads/2021/05/7-04-850x379.png" alt="" width="850" height="379" />

Once assembled, each model of the LongMill (12×12, 12×30, and 30×30) is designed to generally fit on a 2×2′, 2×4′, and 4×4′ surface respectively. The diagrams below show a more detailed view for each model:
<ol>
 	<li>The red area inside the main box shows the cutting area as an offset from the foot base. It’s based off the center-point of the router, thus you can plane an area larger than what’s stated if you’re using a large surfacing bit.</li>
 	<li>The blue area outside the main box shows the hanging parts as an offset from the foot base which makes up the total machine outline.</li>
 	<li>If you have the <strong>dust shoe</strong> attachment in place, it’ll reduce your cutting travel in the X-dimension by approximately 34mm.</li>
 	<li>These diagrams have got a small buffer on the cutting area (i.e. it’s been shrunkened slightly) since each part has its own manufacturing tolerance and can come together differently in assembly so we want to ensure we’re providing a reasonable guarantee on what can be expected from your machine.</li>
</ol>
[tabby title="12x12"]

<img class="size-full wp-image-1180 aligncenter" src="https://resources.sienci.com/wp-content/uploads/2021/05/7-07.png" alt="" width="836" height="723" />

&nbsp;

[tabby title="12x30"]

<img class="size-full wp-image-1179 aligncenter" src="https://resources.sienci.com/wp-content/uploads/2021/05/7-06.png" alt="" width="835" height="584" />

[tabby title="30x30" open="yes"]

<img class="size-full wp-image-1178 aligncenter" src="https://resources.sienci.com/wp-content/uploads/2021/05/7-05.png" alt="" width="836" height="723" />

[tabbyending]

At the end of the day, this leaves you with:

<img class="size-medium wp-image-1277 aligncenter" src="https://resources.sienci.com/wp-content/uploads/2021/05/7-07.5-850x219.jpg" alt="" width="850" height="219" />
<h2>Mounting your LongMill</h2>
To ensure that your machine is mounted securely and accurately, we’ve created a series of steps to help you do so. We highly recommend following these steps exactly, as the order of these steps matter. You’ll need a computer to be connected to the machine in order to align it properly.

We will start by checking the tension of the Delrin v-wheels. As we did in the previous steps, we want to make sure that the wheels barely turn with our fingers by adjusting the eccentric nuts.

We will also properly tension the Delrin anti-backlash nuts. Turn the tensioning screw a little bit at a time. Check for play by moving the gantry back and forth and seeing if there is any excess movement. Do not over tighten, usually a half turn is more than enough.

Gently put your LongMill on the mounting surface and shuffle it over roughly where you want it. In this case we’re using a 4’x4’ MDF sheet as a combination mounting surface and wasteboard which we had cut to 42 inches to better fit in a car. We’ll be mounting it in the middle and have the electronics box sit off the material to the side.

[caption id="attachment_1181" align="aligncenter" width="850"]<img class="size-medium wp-image-1181" src="https://resources.sienci.com/wp-content/uploads/2021/05/7-08-850x477.jpg" alt="" width="850" height="477" /> Move the machine onto your mounting surface. Position it to where you want it.[/caption]

Once positioned, start by moving the machine all the way to the rearmost position by jogging in the y-axis on your control software. Keep moving backwards until you hear a grinding coming from the motors on both sides; this is to confirm that your machine is all the way back and it aligns the left-side feet to the right-side feet.

[caption id="attachment_1183" align="aligncenter" width="850"]<img class="wp-image-1183 size-medium" src="https://resources.sienci.com/wp-content/uploads/2021/05/7-09-e1622192611486-850x492.jpg" alt="" width="850" height="492" /> Move the machine to the very back until it stalls.[/caption]

We’ll start by mounting the right side of the machine. Using a drill with a long Robertson driver or a short one on a bit extender works best for driving in the screws so that you have the necessary reach. You can use the particle board screws provided, or use your own mounting hardware depending on your material or its thickness, but please ensure that you <strong>don’t use counter-sunk wood screws</strong> to attach the feet as this will crack them.

The screws included are 1-1/4”, 1-1/2”, and 2” size #8 particle board screws. Each foot has two holes for mounting where the shortest screws are meant for the inside and the longer one are for the outside. Please note that the 2” screws WILL go through 3/4” MDF, but were still included since they can hold the LongMill feet down better. If you choose to use them, make sure that the surface under the board will not be damaged if you have screws coming out the bottom.

Alright, begin by moving the machine a couple of inches forward and mount using the inside holes of the top and bottom feet using two wood screws (1-1/4”).

<img class="size-medium wp-image-1184 aligncenter" src="https://resources.sienci.com/wp-content/uploads/2021/05/7-10-e1622192634215-850x499.jpg" alt="" width="850" height="499" />

Next, we'll put screws in the other two spots on the same side, this time on the middle feet.

<img class="size-medium wp-image-1185 aligncenter" src="https://resources.sienci.com/wp-content/uploads/2021/05/7-11-e1622192656425-850x507.jpg" alt="" width="850" height="507" />

Now fasten the diagonal mounting points of all the right-side feet using the longer screws. If you'd like to pre-drill the diagonal holes it'll snug the feet up even better against the board face when the wood screws are installed.

<img class="size-medium wp-image-1186 aligncenter" src="https://resources.sienci.com/wp-content/uploads/2021/05/7-12-e1622192679510-850x491.jpg" alt="" width="850" height="491" />

At this point the right side of your machine will be fully secure. When mounting the left side, we'll want to ensure it's mounted parallel to the right side and also that the back feet are aligned to each other. You can see in the diagram below why mounting the rails both parallel and in-line is important to ensure the CNC isn't overly stressed and also cuts how you'd expect it to.

<img class="size-medium wp-image-1278 aligncenter" src="https://resources.sienci.com/wp-content/uploads/2021/05/7-12.5-850x491.jpg" alt="" width="850" height="491" />

To combat this misalignment, first you'll want to start with the back, left foot on its inside hole (circled). Before attaching this screw, the X-axis should be moved nearly to the back. In addition, if you have some sort of straight edge on hand (level, carpenters square, etc.) you can even butt the table up against a wall and space off the wall if need be - ultimately the goal is to align the two back feet of the LongMill as best as you can. Once you feel confident in the foot placement, drive this first screw into place.

<img class="size-medium wp-image-1187 aligncenter" src="https://resources.sienci.com/wp-content/uploads/2021/05/7-13-e1622192712388-850x497.jpg" alt="" width="850" height="497" />

To complete parallel alignment, you'll be moving the machine towards the front so that it's right next to the foot you want to secure next. With the back foot done in the last step, move the machine down so that it is roughly in the middle of it's length, then secure the insides of the next two feet:

<img class="size-medium wp-image-1188 aligncenter" src="https://resources.sienci.com/wp-content/uploads/2021/05/7-14-e1622192737693-850x492.jpg" alt="" width="850" height="492" />

Finally, move it to the front and secure the inside of the front left foot:

<img class="size-medium wp-image-1189 aligncenter" src="https://resources.sienci.com/wp-content/uploads/2021/05/7-15-e1622192756566-850x484.jpg" alt="" width="850" height="484" />

Now move the machine again to the middle spot and use the longer screws to finish mounting the feet using their diagonal mounting holes.

<img class="size-medium wp-image-1190 aligncenter" src="https://resources.sienci.com/wp-content/uploads/2021/05/7-16-e1622192773389-850x492.jpg" alt="" width="850" height="492" />

Your machine should now be fully secure and square to its mounting surface. An easy squareness check is to tape a pencil or marker to your router mount and draw a large L or box shape manually by using the X and Y movements on your computer. You'll be able to use this in combination with a carpenters square or measuring a 3-4-5 triangle to confirm that your machine has been aligned properly.

From this point, you should be ready to get cutting your first jobs! If you've got the touch plate, dust shoe, or t-track add-ons alongside your machine, you'll see the guide on how to utilize these and put them together after the "Starter Projects" page.

The rest of this <strong>Assembly</strong> section also contains information on how to surface your wasteboard, ways to get started making more projects, machine maintenance, and a page on troubleshooting in case you happened upon any issues during assembly or during the Starter Projects.