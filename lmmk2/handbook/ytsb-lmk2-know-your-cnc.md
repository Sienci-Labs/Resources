---
title: ytsb Your MK2
menu_order: 1
post_status: draft
post_excerpt: A quick start and resource guide for your LongMill CNC machine.
post_date: 2022-03-17 20:31:00
taxonomy:
    knowledgebase_cat: lmk2-handbook
    knowledgebase_tag:
        - mk2
custom_fields:
    KBName: LongMill MK2 CNC
    basepress_post_icon: bp-caret-right
skip_file: yes
featured_image: 
---

There is a lot of information to take in and learn and it can be overwhelming. Bookmark this page to the list of most common resources for easy access.

The LongMill MK2 is a hobby-focused Benchtop CNC with most features any hobby user wants, even capable of bringing some users into small-scale production within the comfort of their own shed or home shop. The balance of ease-of-use, cost, and rigidity is one that we think is fairly unique in the hobby CNC world and when paired up with its other available accessories serves green CNCers and more experienced hobbyists alike. Reach for this CNC as one of your more multi-functional tools on your tool belt to accomplish a variety of tasks such as:

<ul>
  <li>Large sign lettering or full sign routing</li>
  <li>Intricate v-carving and inlays</li>
  <li>Furniture work and joinery</li>
  <li>Slab flattening</li>
  <li>Children's toys and household items</li>
  <li>Wall art and gifts to friends and family</li>
</ul>

<h2>Anatomy</h2>

The MK2 is a 3-axis CNC that comes in two sizes. Each axis is lead screw driven to increase rigidity and maintain great accuracy in the X-axis (cutting left-to-right), Y-axis (forward and backward), and Z-axis (up and down, cutting into the material).

<img class="wp-image-3725 size-medium aligncenter" src="https://resources.sienci.com/wp-content/uploads/2022/03/Your-CNC-Assembly-View-850x478.png" alt="" width="850" height="478" />

[tabby title="12x30"]

<strong>Machine Size (WxDxH):</strong> 1130 x 591 x 424 mm (44.5 x 23.3 x 16.72")

<strong>Cutting Area (WxDxH):</strong> 820 x 358 x 114 mm (32.3 x 14.1 x 4.5")

<strong>Recommended table size (WxDxH):</strong> 2'x4'

[tabby title="30x30" open="yes"]

<strong>Machine Size (WxDxH):</strong> 1130 x 836 x 424 mm (44.5 x 42.9 x 16.7 ")

<strong>Cutting Area (WxDxH):</strong> 820 x 872 x 114 mm (32.3 x 34.2 x 4.5")

<strong>Recommended table size (WxDxH):</strong> 4'x4'

[tabby title="48x30"]

<strong>Machine Size (WxDxH):</strong> 1603 x 836 x 424 mm (63.1 x 42.9 x 16.7 ")

<strong>Cutting Area (WxDxH):</strong> 1280 x 872 x 114 mm (50.4 x 34.2 x 4.5")

<strong>Recommended table size (WxDxH):</strong> 6'x4'

[tabbyending]

<a href="https://sienci.com/wp-content/uploads/2021/12/LongMill-MK2-48x30-30x30-and-12x30-dimensions.pdf" target="_blank" rel="noopener">Link to Dimensional Drawings </a>

Outside of the mechanics of the MK2, the general remaining systems to keep in mind are its:

<ul>
  <li><b>Control Box:</b> handles motor movements and other I/O so needs to be kept near the machine as well as accepts incoming power from a power supply and USB signals from a control computer so should be kept near to those as well</li>
  <li><b>E-stop:</b> the safety and power switch so keep it in an accessible location to ensure it’s easy to press in an emergency</li>
  <li><b>Drag chains &amp; wires:</b> handle all the important power and data transmission so should be given space for proper routing, movement, and strain relief to avoid fraying or cause erratic machine behaviour</li>
  <li><b>Makita RT0701C trim router:</b> to be maintained independently from the machine itself as outlined in the provided Makita manual and also repeated here: <a href="https://resources.sienci.com/view/lmk2-router-and-tools/">https://resources.sienci.com/view/lmk2-router-and-tools/</a></li>
</ul>

<h2>Requirements & Specs</h2>

<b>Weight:</b> ~30kg (70 lbs) not including MDF wasteboard plus other accessories

<b>Power requirements:</b> at 120V, four independent outlets to provide

<ul>
  <li>2.5A to the MK2 Control box</li>
  <li>6.5A to the Makita router or the rating of whichever router / spindle you equipped to your MK2</li>
  <li>Power to the desktop, laptop, mini-PC, or SBC (single board computer, like a raspberry pi) that will provide cutting instructions to the electronics box over USB</li>
  <li>Power to your dust management system whether it’s a vacuum or dust collector (this should be put on an independent circuit if you want to reduce possible issues from static buildup or EMI)</li>
</ul>

<b>Operating temperature:</b> expect reliable operation between 5 🠚30°C shop temperature (can be colder or hotter outside) as long as you give your machine time to acclimate to its environment to avoid cold-running or building up moisture on the electronics. Using these methods some users have reported running in as low as -20°C though wireless mice or keyboards reportedly become unreliable. Generally though if you’re comfortable your machine will be comfortable

<b>Operating humidity:</b> best results will occur from a balanced humidity, too high and you can expect the moisture to degrade or even short the electronics, cause higher dust buildup, and swell the MDF wasteboard whereas dry air can cause static charges to build up more easily so a poorly grounded machine will experience electronic disruptions

<b>Storage:</b> all components have a wide operating temperature range such as -20 🠚 50°C for the stepper motors, -40 🠚 120 °C for delrin parts, -40 🠚 85°C for the control box, and -40 🠚 105 °C for the motor connectors so as long as the MK2 is kept stationary it can survive being stored at nearly any temperature as long as ambient humidity isn’t too high (causes degradation of electrical components)

<b>Max cutting speed:</b> 4000 mm/min (157.5 ipm) in X and Y, 3000 mm/min (118.1 ipm) in Z

<b>X & Y-axis motion:</b> Delrin v-wheels on high rigidity extruded aluminum rails with custom adjusting eccentric nuts

<b>Z-axis motion:</b> MGN12 recirculating ball bearing linear guide blocks running on precision ground hardened steel rails

<b>Power transmission:</b> 12.6kg-cm (175oz-in) NEMA 23 steppers driving 4-start, 2mm pitch, 8mm lead, 8mm diameter ACME lead screws via anti-backlash tensioning nuts to 6.35mm (1/4″) steel gantry plates

<b>Router / spindle:</b> should be able to run in the 15000 - 25000 RPM range with reliable speed feedback, 0-5V control for spindles, and not exceed 2.7kg (6 lbs) to avoid hindering the performance of the machine

<strong>Electronics:</strong> SuperLongBoard 5xHAL uses an STM32F412 chip running grblHAL powering four TMC2660C motor drivers. The LongBoard uses an Arduino Uno running grbl v1.1h powering four 4A TB6600 motor drivers.

<b>Inputs and Outputs:</b> on-board Play, Pause, and Stop buttons and I/O for limit switches, spindle or laser, probing, coolant or other 5V peripherals, and a constant 12V supply up to ~1A

Find specifications about add-ons here:

<ul>
  <li><b>Touch Plate:</b> <a href="https://resources.sienci.com/view/lmk2-touch-plate/">https://resources.sienci.com/view/lmk2-touch-plate/</a></li>
  <li><b>Dust Shoe:</b> <a href="https://resources.sienci.com/view/lmk2-dust-shoe-shield/">https://resources.sienci.com/view/lmk2-dust-shoe-shield/</a></li>
  <li><b>Dust Shield:</b> <a href="https://resources.sienci.com/view/lmk2-dust-shoe-shield/">https://resources.sienci.com/view/lmk2-dust-shoe-shield/</a></li>
  <li><b>Limit switches:</b> <a href="https://resources.sienci.com/view/lmk2-limit-switches/">https://resources.sienci.com/view/lmk2-limit-switches/</a></li>
  <li><b>T-track &amp; clamps:</b> <a href="https://resources.sienci.com/view/lmk2-t-track-set/">https://resources.sienci.com/view/lmk2-t-track-set/</a></li>
  <li><b>Laser:</b> <a href="https://resources.sienci.com/view/lmk2-adding-a-laser/">https://resources.sienci.com/view/lmk2-adding-a-laser/</a></li>
  <li><b>IOT Relay:</b> <a href="https://resources.sienci.com/view/lmk2-automated-relay/">https://resources.sienci.com/view/lmk2-automated-relay/</a></li>
</ul>

<h2>Capabilities</h2>

With the appropriate cutting tools the MK2 can comfortably carve a variety of materials including hard and soft woods, plastics, foams, waxes, and much more. It can even produce acceptable work on soft metals like aluminum, bronze, copper, or can be equipped with other accessories like a drag knife, engraving tool, or laser diode to cut vinyl, card stock, cardboard, engrave ceramics, glass, metals, and the list goes on.

<img class="size-medium wp-image-3670 aligncenter" src="https://resources.sienci.com/wp-content/uploads/2022/03/Materials-on-the-MK2-850x368.jpg" alt="" width="850" height="368" />

Common carving techniques include profiling, pocketing, v-carving, engraving, and contouring / relief. Other more advanced techniques are also available such as tiling to cut projects larger than the MK2s work area, flip milling and multi-sided cutting for carving more advanced geometries, and CNC joinery that combines end-grain and through-grain cutting to wood joints for many purposes.

Success with all this cutting will rely on some of your own understanding coming in so if any of these terms are foreign to you or you’d like to learn more then check out our sections on:

<b>Intro to:</b> <a href="https://resources.sienci.com/view/lmk2-cnc-routers/">cutting styles</a>, <a href="https://resources.sienci.com/view/lmk2-materials/">materials</a>, and <a href="https://resources.sienci.com/view/lmk2-cutting-tools/">cutting tools</a>

<b>Handbook knowledge on:</b> <a href="https://resources.sienci.com/view/lmk2-router-and-tools/">what tools to use</a>, <a href="https://resources.sienci.com/view/lmk2-feeds-and-speeds/">cutting speeds</a>, <a href="https://resources.sienci.com/view/lmk2-running-jobs/">running jobs</a>, <a href="https://resources.sienci.com/view/lmk2-wasteboard/">fixturing</a>, and <a href="https://resources.sienci.com/view/lmk2-common-cnc-terms/">common CNC terms</a>

Here are some other <b>Quick tips:</b>

<ul>
  <li>Power off your MK2 when not in use</li>
  <li>Using your machine will require a USB connection to any computer that meets the <a href="https://resources.sienci.com/view/lmk2-system-requirements/">required specifications</a> to send cutting information to the CNC</li>
  <li>Robotic noises are normal to hear when moving around, these come from the stepper motors as they make the precise movements needed to drive the machine</li>
  <li>The MK2 can’t break itself so don’t be scared using it; the motors are designed to be strong enough to make great cuts but still stall in a worst case scenario such as running into the limits of the machine or colliding with another object which you’ll hear as a noticeable grinding noise</li>
  <li>Your machine shouldn’t be kept running for longer than a handful of hours at a time so you can give your router, dust collection system, and even yourself a break. If you need to run longer jobs then we have <a href="https://resources.sienci.com/view/lmk2-running-jobs/">some advice for that</a></li>
  <li>Occasional squeaks and squeals are normal to hear but more consistent noise might be a sign to perform regular <a href="https://resources.sienci.com/view/lmk2-maintenance/" target="_blank" rel="noopener">maintenance</a>. Remember that things can come loose over time and some parts on the LongMill are consumable</li>
</ul>

<h2>Important Safety</h2>

As is also covered in our <a href="https://sienci.com/terms-and-conditions/" target="_blank" rel="noopener">safety warnings and guidelines</a> for the MK2, always operate your machine in a safe manner:

<ul>
  <li>Never wear loose clothing while operating the machine. Keep long hair and clothes away from all moving parts so nothing gets caught and wear appropriate footwear. Remember that though we try to prevent incidental harm while using the MK2 it’s still up to you to be safe and aware while using it</li>
  <li>Wear a good set of over-the-ear hearing protection or ear plugs to prevent hearing damage since the LongMill on its own or combined with a dust collection system can be quite loud</li>
  <li>Especially in cases of poor dust collection or ventilation a good dust mask or respiratory protection is needed to protect from inhaling particulates in the air. Some materials can even be toxic or generate long-term health problems if inhaled so look up the MSDS (material safety data sheet) of your material before you start cutting it</li>
  <li>Cutting can kick-up a lot of dust and wood chips so reasonable eye protection should be worn while the machine is running</li>
  <li>Be aware around your machine and don’t leave it unattended. Anything can happen while you’re not paying attention and could result in harm if you reach in or turn your back during operation</li>
  <li>Careful with tool and materials handling. Cutting tools can shatter or cause damage if they’re not in good condition or can cut you during handling and this is similar with materials. Material can also ignite during cutting, within your dust collection system, or even spontaneously especially if mixed in with other chemicals or oils when disposed. Be aware of safe disposal measures for your cutters and materials for your particular area</li>
</ul>

<h2>Resource Pages</h2>

These are the main pages to follow if you have any questions about your machine, issues that may occur or have a need for deeper information. These are a great reference guide if you’re new to CNC machining and to refer to when doing something new.

Refer to the troubleshooting guide first if you encounter any issues. If you can’t solve the problem yourself, reach out for support. The more information you can provide, the quicker we can help.

<ul>
  <li><a href="https://resources.sienci.com/view/lmk2-maintenance/">Maintenance</a> - Follow our maintenance schedule to keep your machine in tip-top shape.</li>
  <li><a href="https://resources.sienci.com/view/lmk2-issues-and-fixes/">Troubleshooting</a> - A resource for most common issues, useful before contacting customer support.</li>
  <li><a href="https://resources.sienci.com/view/lmk2-common-cnc-terms/">Common Terms</a> - CNC machining has a large language, start here to learn the words and phrases commonly used.</li>
  <li><a href="https://resources.sienci.com/view/lmk2-feeds-and-speeds/">Feeds and Speeds</a> - A resource guide for getting the most efficiency with your machine.</li>
  <li><a href="https://resources.sienci.com/view/lmk2-choosing-software/">Choosing Software</a> - Great resource for beginners to the different types of software used with CNC machining.</li>
  <li><a href="https://resources.sienci.com/view/lmk2-materials/">Materials</a> - A handy material reference guide for most common materials.</li>
</ul>

<h2>Community Resources</h2>

We’ve got a great online community that is well worth visiting and being a part of. Have questions about the machine, machining techniques or how to use some software, this is the first place to start. If our knowledgeable community can’t help, Customer Support surely will.

<ul>
  <li><a href="https://forum.sienci.com/" target="_blank" rel="noopener">Sienci Community forum</a> - A great information resource and a place to connect with like minded customers</li>
  <li><a href="https://www.facebook.com/groups/mill.one" target="_blank" rel="noopener">Sienci Facebook Group</a> - Another great resource and place to show off your projects</li>
  <li><a href="https://sienci.com/contact-us/" target="_blank" rel="noopener">Customer Support</a> - Contact us with your questions or needs.</li>
</ul>

If you haven't, check out our YouTube channel or one of our affiliated customers. We can’t say enough how helpful and useful they are.

<ul>
  <li><a href="https://www.YouTube.com/channel/UCS4SdQ0sqFhvjitLjh4EsGQ" target="_blank" rel="noopener">Sienci Labs YouTube</a> - Our own channel with product updates, repair guides and tutorials</li>
  <li><a href="https://www.YouTube.com/c/IDCWoodcraft" target="_blank" rel="noopener">CNC Routers, Beginners &amp; Beyond - Garrett Fromme</a> Very resourceful with a lot of tips and tricks especially with VCarve</li>
  <li><a href="https://www.YouTube.com/c/BuckysCustoms" target="_blank" rel="noopener">Bucky’s Customs</a> - Another user showcasing tutorials while using the LongMill</li>
</ul>

https://www.YouTube.com/watch?v=Kt53x5CYwzU

<h2>Community Modifications</h2>

If there are any known noteworthy designs or modifications made to the LongMill, they will be posted here. This is to make the information needed for modification more accessible and to also thank and recognize users and community members who have made an impact on the LongMill CNC project.

<h3>General</h3>

<ul>
  <li>coogle's <strong>Control box feet mounts</strong>: <a href="https://www.thingiverse.com/thing:4049019" target="_blank" rel="noopener">https://www.thingiverse.com/thing:4049019</a></li>
  <li>coogle's <strong>CNC table design</strong>: <a href="https://www.thingiverse.com/thing:4049035" target="_blank" rel="noopener">https://www.thingiverse.com/thing:4049035</a></li>
  <li><a href="https://forum.sienci.com/t/new-control-box-in-progress/428/2" target="_blank" rel="noopener noreferrer">David</a>'s <strong>switching box</strong>: <a href="https://www.thingiverse.com/thing:4077356" target="_blank" rel="noopener noreferrer">https://www.thingiverse.com/thing:4077356</a>
<a href="https://CAD.onshape.com/documents/4a032d38229a5e4fdfc29ad2/w/3fdd62166f15b2bca45b86dd/e/76713fef2f3d04737acac6ce" target="_blank" rel="noopener noreferrer">https://CAD.onshape.com/documents/4a032d38229a5e4fdfc29ad2/w/3fdd62166f15b2bca45b86dd/e/76713fef2f3d04737acac6ce</a></li>
  <li><a href="https://forum.sienci.com/t/homing-limit-switches/99/10" target="_blank" rel="noopener noreferrer">sysimgrp</a>'s 3D printable <strong>laser diode centre-point locator</strong>: <a href="https://www.thingiverse.com/thing:4189396" target="_blank" rel="noopener noreferrer">https://www.thingiverse.com/thing:4189396</a></li>
  <li><a href="https://forum.sienci.com/u/mikecmp">Mike</a>'s CNCable <strong>keyboard and monitor shelf</strong>: <a href="https://forum.sienci.com/t/what-are-your-plans-for-a-table/95/30" target="_blank" rel="noopener noreferrer">https://forum.sienci.com/t/what-are-your-plans-for-a-table/95/30</a></li>
  <li><a href="https://forum.sienci.com/u/gwilki">Grant</a>'s Y-axis <strong>plastic bumpers</strong>: <a href="https://forum.sienci.com/t/y-axis-modification-bumpers/560" target="_blank" rel="noopener noreferrer">https://forum.sienci.com/t/y-axis-modification-bumpers/560</a></li>
  <li><a href="https://forum.sienci.com/u/gwilki">Grant</a>'s CNC <strong>control keypad</strong>: <a href="https://forum.sienci.com/t/anyone-using-pendant-feature-of-ugs/503/16" target="_blank" rel="noopener noreferrer">https://forum.sienci.com/t/anyone-using-pendant-feature-of-ugs/503/16</a></li>
  <li>Dave's 3D printable Makita <strong>router under-light</strong>: <a href="https://www.facebook.com/groups/mill.one/permalink/801433143661352/" target="_blank" rel="noopener noreferrer">https://www.facebook.com/groups/mill.one/permalink/801433143661352/</a></li>
  <li>Michael's 3D printable <strong>T-track stops</strong>: <a href="https://www.facebook.com/groups/mill.one/permalink/884002938737705/" target="_blank" rel="noopener noreferrer">https://www.facebook.com/groups/mill.one/permalink/884002938737705/</a></li>
  <li><a href="https://forum.sienci.com/u/jwoody18">Jeff</a>'s CNCable <strong>dust shrouds</strong>: <a href="https://forum.sienci.com/t/alligator-ribs-for-dust-shields-along-the-y-axis/749" target="_blank" rel="noopener noreferrer">https://forum.sienci.com/t/alligator-ribs-for-dust-shields-along-the-y-axis/749</a></li>
  <li>Brian’s 3D printable <b>bit length sensor</b>:<a href="https://www.facebook.com/groups/mill.one/permalink/970109396793725/"> https://www.facebook.com/groups/mill.one/permalink/970109396793725/</a></li>
  <li><a href="https://forum.sienci.com/u/Lumpy">Kris</a>’s <b>laser setup</b>:<a href="https://forum.sienci.com/t/adding-a-laser-my-journey-tutorial/1183?fbclid=IwAR0nifeyE9wgvco_pMnz9-R1-q9TWF5jIzKo0rhJ2ZAi8kFTdMw38HIr4Vg"> https://forum.sienci.com/t/adding-a-laser-my-journey-tutorial/1183</a></li>
  <li>Dave’s <b>LED lighting setup</b>:<a href="https://www.facebook.com/groups/mill.one/permalink/928459777625354/"> https://www.facebook.com/groups/mill.one/permalink/928459777625354/</a></li>
  <li><a href="https://forum.sienci.com/u/BillKorn">BillKorn</a>’s <b>drag knife</b>:<a href="https://forum.sienci.com/t/drag-knife-for-thin-stock/768"> https://forum.sienci.com/t/drag-knife-for-thin-stock/768</a></li>
  <li><a href="https://forum.sienci.com/u/BillKorn">BillKorn</a>’s <b>3D digitizer probe:</b><a href="https://forum.sienci.com/t/using-a-probe-to-digitize-an-object/1019"> https://forum.sienci.com/t/using-a-probe-to-digitize-an-object/1019</a></li>
  <li>Keith’s <b>controller box mounting</b> feet:<a href="https://www.facebook.com/groups/mill.one/permalink/903958263408839/"> https://www.facebook.com/groups/mill.one/permalink/903958263408839/</a></li>
  <li>Spike’s <b>control panel</b>:<a href="https://www.facebook.com/groups/mill.one/permalink/902963963508269/"> https://www.facebook.com/groups/mill.one/permalink/902963963508269/</a></li>
  <li><a href="https://forum.sienci.com/u/chrismakesstuff" target="_blank" rel="noopener noreferrer">Chris</a>' <strong>vertical stand design</strong>: <a href="https://forum.sienci.com/t/stand-design-for-permanent-vertical-cutting/1112" target="_blank" rel="noopener noreferrer">https://forum.sienci.com/t/stand-design-for-permanent-vertical-cutting/1112</a></li>
  <li>coreyker's <strong>pen/pencil spring mount</strong>: <a href="https://github.com/coreyker/LongMill/tree/main/PenMountV1" target="_blank" rel="noopener">https://github.com/coreyker/LongMill/tree/main/PenMountV1</a></li>
  <li>DustinTheMaker's <strong>power supply mount</strong>: <a href="https://www.thingiverse.com/thing:4569748" target="_blank" rel="noopener">https://www.thingiverse.com/thing:4569748</a></li>
  <li>JimAlex's <strong>Makita speed stop</strong>: <a href="https://www.thingiverse.com/thing:4939138" target="_blank" rel="noopener">https://www.thingiverse.com/thing:4939138</a></li>
  <li>JimAlex's <strong>Tramming bar: </strong><a href="https://www.thingiverse.com/thing:4939863" target="_blank" rel="noopener">https://www.thingiverse.com/thing:4939863</a></li>
</ul>

<h3>Limit Switch and Touch plate Mods</h3>

<ul>
  <li>SimtechBen’s <b>touch plate holder</b>: <a href="https://www.thingiverse.com/thing:4948964" target="_blank" rel="noopener">https://www.thingiverse.com/thing:4948964</a></li>
  <li>Michael’s <b>touch plate holder</b>:<a href="https://www.prusaprinters.org/prints/32598-LongMill-touch-plate-holder"> https://www.prusaprinters.org/prints/32598-LongMill-touch-plate-holder</a></li>
  <li><a href="https://forum.sienci.com/t/homing-limit-switches/99/10" target="_blank" rel="noopener noreferrer">sysimgrp</a>'s redesigned <strong>touch plate magnet cover</strong>: <a href="https://www.thingiverse.com/thing:4173451" target="_blank" rel="noopener noreferrer">https://www.thingiverse.com/thing:4173451</a></li>
  <li><a href="https://forum.sienci.com/t/homing-limit-switches/99/10" target="_blank" rel="noopener noreferrer">sysimgrp</a>'s <strong>limit switch mounts</strong>: <a href="https://www.thingiverse.com/thing:4189426">https://www.thingiverse.com/thing:4189426</a></li>
  <li>mcol82's <strong>limit switch mounts</strong>: <a href="https://www.thingiverse.com/thing:4060347" target="_blank" rel="noopener">https://www.thingiverse.com/thing:4060347</a></li>
  <li><a href="https://www.facebook.com/groups/mill.one/permalink/949875162150482/">Frank</a>’s 3D printable <b>touch plate holder</b>:<a href="https://www.facebook.com/groups/mill.one/permalink/976042446200420/"> https://www.facebook.com/groups/mill.one/permalink/976042446200420/</a></li>
</ul>

<h3>Dust Shoe Mods</h3>

<ul>
  <li><a href="https://forum.sienci.com/t/dust-shoe-modification/472/10" target="_blank" rel="noopener noreferrer">sysimgrp</a>'s alternative <strong>dust shoe design</strong>: <a href="https://www.thingiverse.com/thing:4189543" target="_blank" rel="noopener noreferrer">https://www.thingiverse.com/thing:4189543</a></li>
  <li><a href="https://forum.sienci.com/t/is-anyone-working-on-something-cool-to-add-functionality-or-improve-their-machine/41/15" target="_blank" rel="noopener noreferrer">Buebeli</a>'s “dustshoe2shopvac” <strong>adapter</strong>: <a href="https://CAD.onshape.com/documents/68a2af8c900b7568ef2876f5/w/2b75c1cf11dc8870a9c8668e/e/46aa8d16723a461387d04d44" target="_blank" rel="noopener noreferrer">https://CAD.onshape.com/documents/68a2af8c900b7568ef2876f5/w/2b75c1cf11dc8870a9c8668e/e/46aa8d16723a461387d04d44</a></li>
  <li>Keith’s alternative <b>dust shoe design</b>:<a href="https://www.facebook.com/groups/mill.one/permalink/941497279654937/"> https://www.facebook.com/groups/mill.one/permalink/941497279654937/</a></li>
  <li>Xavier’s alternative <b>dust shoe design</b>:<a href="https://www.prusaprinters.org/prints/30167-LongMill-dust-shoe-redesign/files"> https://www.prusaprinters.org/prints/30167-LongMill-dust-shoe-redesign/files</a></li>
  <li>Stewart’s alternative <b>dust shoe design</b>:<a href="https://CAD.onshape.com/documents/f33531ce079ad207c663875f/w/ac37eff1df8958b7eb7f4130/e/a0d7b7aa72f4d9a34b68fc87"> https://CAD.onshape.com/documents/f33531ce079ad207c663875f/w/ac37eff1df8958b7eb7f4130/e/a0d7b7aa72f4d9a34b68fc87</a></li>
  <li>Stephen’s alternative<b> dust shoe design:</b><a href="https://www.facebook.com/groups/mill.one/permalink/909165219554810/"> https://www.facebook.com/groups/mill.one/permalink/909165219554810/</a></li>
  <li><a href="https://forum.sienci.com/t/what-does-your-dust-collection-hose-management-look-like/458/15" target="_blank" rel="noopener noreferrer">David</a>'s <strong>dust hose boom</strong>: <a href="https://www.thingiverse.com/thing:4082855" target="_blank" rel="noopener noreferrer">https://www.thingiverse.com/thing:4082855</a>
<a href="https://CAD.onshape.com/documents/57648b7f221a8b14202c6da4/w/09ca17006a988771f02d3db7/e/6ef8f0a441b6df6b9b3ffa87" target="_blank" rel="noopener noreferrer">https://CAD.onshape.com/documents/57648b7f221a8b14202c6da4/w/09ca17006a988771f02d3db7/e/6ef8f0a441b6df6b9b3ffa87</a></li>
</ul>

<h2>Warranty</h2>

You can find detailed information on the warranty, returns, and replacement parts <a href="https://sienci.com/product/LongMill-mk2/" target="_blank" rel="noopener">here</a>.
