---
title: Know your MK2
menu_order: 5
post_status: publish
post_excerpt: A quick start and resource guide for your LongMill MK2 CNC machine.
post_date: 2022-03-21 20:31:00
taxonomy:
    knowledgebase_cat: lmk2-the-basics
    knowledgebase_tag:
        - mk2
custom_fields:
    KBName: LongMill MK2 CNC
    basepress_post_icon: bp-caret-right
skip_file: no
featured_image: _images/_lmmk2/_handbook/lmk2_knowcnc_Your-CNC-Assembly-View.png
---

    ❗There is a lot of information to take in and learn and it can be overwhelming. Bookmark this page for easy access.

## Capabilities

The LongMill MK2 is a benchtop CNC with most features any hobby user wants, even capable of bringing small-scale production within the comfort of one's own shed or home shop. The balance of ease-of-use, cost, and rigidity is one that we think is fairly unique in the hobby CNC world, and when paired up with other accessories, serves green and more experienced CNC hobbyists alike. It can accomplish a variety of tasks such as:

- Large sign lettering or full sign routing
- Intricate v-carving and inlays
- Furniture work and joinery
- Slab flattening
- Children's toys and household items
- Wall art and gifts to friends and family

The MK2 can comfortably carve a variety of materials including **hard and soft woods, plastics, foams, and waxes**. It can even produce acceptable work on soft metals like **aluminum, bronze, copper,** or can be equipped with other accessories like a drag knife, engraving tool, or laser diode to **cut vinyl, card stock, cardboard**, and **engrave ceramics, glass, and metals**.

![](/_images/_lmmk2/_handbook/lmk2_knowcnc_materials-on-the-MK2.jpg){.aligncenter .size-medium}

## Anatomy

The MK2 is a 3-axis CNC that comes in three sizes. Each axis is lead screw driven to increase rigidity and maintain accuracy in the X-axis (left-to-right), Y-axis (forward and backward), and Z-axis (up and down, cutting into the material).

![](/_images/_lmmk2/_handbook/lmk2_knowcnc_Your-CNC-Assembly-View.png){.aligncenter .size-medium}

![](/_images/_lmmk2/_the-basics/lmk2_communitytable_footprint.jpg){.aligncenter .size-medium}

For complete dimensions see:<a href="https://sienci.com/wp-content/uploads/2021/12/LongMill-MK2-48x30-30x30-and-12x30-dimensions.pdf" target="_blank" rel="noopener"> LongMill MK2 Drawing PDF</a>

## 📋 Specifications

**Weight:** ~30kg (70 lbs) not including MDF wasteboard plus other accessories

**Power requirements:** at 120V, two independent circuits to provide...

- 2.5A to the SLB controller
- 6.5A to the Makita router or the rating of whichever router / spindle you equipped to your MK2
- Power to the desktop, laptop, mini-PC, or SBC (i.e. single board computer, like a raspberry pi)

  **AND**

- Power to your dust management system whether it's a vacuum or dust collector
  - This is a separate circuit to reduce static buildup or EMI issues

**Operating temperature:** expect reliable operation between 5 🠚30°C shop temperature (can be colder or hotter outside), as long as you give your machine time to acclimate to its environment to avoid cold-running and moisture build up on the electronics. Using these methods some users have reported running in as low as -20°C, though wireless mice or keyboards reportedly become unreliable.

**Operating humidity:** best results will occur from a balanced humidity (40-60%), too high and you can expect the moisture to degrade or even short the electronics, cause higher dust buildup, and swell the MDF wasteboard. Dry air can cause static charges to build up more easily, so a poorly grounded machine will experience electronic disruptions.

**Storage:** all components have a wide operating temperature range such as -20 🠚 50°C for the stepper motors, -40 🠚 120 °C for delrin parts, -40 🠚 85°C for the control box, and -40 🠚 105 °C for the motor connectors. As long as the MK2 is kept stationary and at a mild ambient humidity (40-60%), it can survive being stored at nearly any temperature.

**Max cutting speed:** 4000 mm/min (157.5 ipm) in X and Y, 3000 mm/min (118.1 ipm) in Z.

**X & Y-axis motion:** Delrin v-wheels on high rigidity extruded aluminum rails with custom adjusting eccentric nuts.

**Z-axis motion:** MGN12 recirculating ball bearing linear guide blocks, running on precision ground hardened steel rails.

**Power transmission:** 12.6kg-cm (175oz-in) NEMA 23 steppers driving 4-start, 2mm pitch, 8mm lead, 8mm diameter ACME lead screws via anti-backlash tensioning nuts to 6.35mm (1/4″) steel gantry plates.

**Router / spindle:** can run in 15000 - 25000 RPM range with reliable speed feedback, 0-5V PWM control for spindles. Router / spindle cannot exceed 2.7kg (6 lbs).

**Electronics:** SuperLongBoard 5xHAL uses an STM32F412 chip running grblHAL powering four TMC2660C motor drivers. The LongBoard uses an Arduino Uno running grbl v1.1h powering four 4A TB6600 motor drivers.

## 📖 Prep for your MK2

- Familiarize yourself with [fundamental CNC concepts and workflows](https://resources.sienci.com/view/cnc-machines/)
- Dive into understanding [CNC software](https://resources.sienci.com/view/cnc-software-explained/), and set up your [post processor](https://resources.sienci.com/view/cnc-post-processors/)
- Bookmark these pages to refer to after your LongMill assembly
  - [Add-ons installation and usage guides](https://resources.sienci.com/add-ons/) (e.g. AutoZero touch plate, gControl panel)
  - How to do [maintenance on your LongMill](https://resources.sienci.com/view/lmk2-maintenance/)
  - [Feeds and speeds](https://resources.sienci.com/view/cnc-feeds-speeds/) for various material and bit types
  - Step by step instructions on [how to run a CNC job](https://resources.sienci.com/view/cnc-running-jobs/)
  - [Finishing techniques](https://resources.sienci.com/view/cnc-sanding-finishing/) after you've cut out your project
- Determine what [computer](https://resources.sienci.com/view/cnc-system-requirements/) you would need, if you are not getting gControl panel
- Consider which [workholding methods](https://resources.sienci.com/view/cnc-workholding/) to use  
- Source [cutting tools](https://resources.sienci.com/view/cnc-cutting-tools/) for the types of projects you’re interested in making
- Figure out your [dust collection system](https://resources.sienci.com/view/cnc-dust-collection/)
- Take precautions and grab [safety gear to protect your eyes and ears](https://resources.sienci.com/view/cnc-safety/)
- Grab 3/4" MDF sheets for [mounting your table surface](https://resources.sienci.com/view/lmk2-table-mounting/)
  - Looking for table ideas? [See these designs](https://resources.sienci.com/view/lmk2-table-enclosure/#community-table-builds) made by fellow community members

## 🗪 Community Support

We've got a great online community that is well worth visiting and being a part of. Have questions about the machine, machining techniques or how to use some software, this is the first place to start. If our knowledgeable community can't help, Customer Support surely will.

- <a href="https://forum.sienci.com/" target="_blank" rel="noopener">Sienci Community Forum</a> - A great information resource and a place to connect with like minded customers
- <a href="https://www.facebook.com/groups/mill.one" target="_blank" rel="noopener">Sienci Facebook Group</a> - Another great resource and place to show off your projects

If you haven't, check out our YouTube channel and our affiliated customers - we can't say enough how helpful and useful they are!

- <a href="https://www.YouTube.com/channel/UCS4SdQ0sqFhvjitLjh4EsGQ" target="_blank" rel="noopener">Sienci Labs YouTube</a> - Our own channel with product updates, repair guides and tutorials
- <a href="https://www.YouTube.com/c/IDCWoodcraft" target="_blank" rel="noopener">IDC WoodCraft -  Garrett Fromme</a>
- <a href="https://www.YouTube.com/c/BuckysCustoms" target="_blank" rel="noopener">Bucky's Customs</a>

## Community Modifications

If there are any known noteworthy designs or modifications made to the LongMill, they will be posted here. This is to make the information needed for modification more accessible and to also thank and recognize users and community members who have made an impact on the LongMill CNC project.

[su_spoiler title="General" open="no" style="fancy" icon="chevron" anchor_in_url="yes"]

- coogle's <b>Control box feet mounts</b>: <a href="https://www.thingiverse.com/thing:4049019" target="_blank" rel="noopener">https://www.thingiverse.com/thing:4049019</a>
- coogle's <b>CNC table design</b>: <a href="https://www.thingiverse.com/thing:4049035" target="_blank" rel="noopener">https://www.thingiverse.com/thing:4049035</a>
- <a href="https://forum.sienci.com/t/new-control-box-in-progress/428/2" target="_blank" rel="noopener noreferrer">David</a>'s <b>switching box</b>: <a href="https://www.thingiverse.com/thing:4077356" target="_blank" rel="noopener noreferrer">https://www.thingiverse.com/thing:4077356</a>
<a href="https://CAD.onshape.com/documents/4a032d38229a5e4fdfc29ad2/w/3fdd62166f15b2bca45b86dd/e/76713fef2f3d04737acac6ce" target="_blank" rel="noopener noreferrer">https://CAD.onshape.com/documents/4a032d38229a5e4fdfc29ad2/w/3fdd62166f15b2bca45b86dd/e/76713fef2f3d04737acac6ce</a>
- <a href="https://forum.sienci.com/t/homing-limit-switches/99/10" target="_blank" rel="noopener noreferrer">sysimgrp</a>'s 3D printable <b>laser diode centre-point locator</b>: <a href="https://www.thingiverse.com/thing:4189396" target="_blank" rel="noopener noreferrer">https://www.thingiverse.com/thing:4189396</a>
- <a href="https://forum.sienci.com/u/mikecmp">Mike</a>'s CNCable <b>keyboard and monitor shelf</b>: <a href="https://forum.sienci.com/t/what-are-your-plans-for-a-table/95/30" target="_blank" rel="noopener noreferrer">https://forum.sienci.com/t/what-are-your-plans-for-a-table/95/30</a>
- <a href="https://forum.sienci.com/u/gwilki">Grant</a>'s Y-axis <b>plastic bumpers</b>: <a href="https://forum.sienci.com/t/y-axis-modification-bumpers/560" target="_blank" rel="noopener noreferrer">https://forum.sienci.com/t/y-axis-modification-bumpers/560</a>
- <a href="https://forum.sienci.com/u/gwilki">Grant</a>'s CNC <b>control keypad</b>: <a href="https://forum.sienci.com/t/anyone-using-pendant-feature-of-ugs/503/16" target="_blank" rel="noopener noreferrer">https://forum.sienci.com/t/anyone-using-pendant-feature-of-ugs/503/16</a>
- Dave's 3D printable Makita <b>router under-light</b>: <a href="https://www.facebook.com/groups/mill.one/permalink/801433143661352/" target="_blank" rel="noopener noreferrer">https://www.facebook.com/groups/mill.one/permalink/801433143661352/</a>
- Michael's 3D printable <b>T-track stops</b>: <a href="https://www.facebook.com/groups/mill.one/permalink/884002938737705/" target="_blank" rel="noopener noreferrer">https://www.facebook.com/groups/mill.one/permalink/884002938737705/</a>
- <a href="https://forum.sienci.com/u/jwoody18">Jeff</a>'s CNCable <b>dust shrouds</b>: <a href="https://forum.sienci.com/t/alligator-ribs-for-dust-shields-along-the-y-axis/749" target="_blank" rel="noopener noreferrer">https://forum.sienci.com/t/alligator-ribs-for-dust-shields-along-the-y-axis/749</a>
- Brian's 3D printable <b>bit length sensor</b>: <a href="https://www.facebook.com/groups/mill.one/permalink/970109396793725/">https://www.facebook.com/groups/mill.one/permalink/970109396793725/</a>
- <a href="https://forum.sienci.com/u/Lumpy">Kris</a>'s <b>laser setup</b>: <a href="https://forum.sienci.com/t/adding-a-laser-my-journey-tutorial/1183?fbclid=IwAR0nifeyE9wgvco_pMnz9-R1-q9TWF5jIzKo0rhJ2ZAi8kFTdMw38HIr4Vg">https://forum.sienci.com/t/adding-a-laser-my-journey-tutorial/1183</a>
- Dave's <b>LED lighting setup</b>: <a href="https://www.facebook.com/groups/mill.one/permalink/928459777625354/">https://www.facebook.com/groups/mill.one/permalink/928459777625354/</a>
- <a href="https://forum.sienci.com/u/BillKorn">BillKorn</a>'s <b>drag knife</b>: <a href="https://forum.sienci.com/t/drag-knife-for-thin-stock/768">https://forum.sienci.com/t/drag-knife-for-thin-stock/768</a>
- <a href="https://forum.sienci.com/u/BillKorn">BillKorn</a>'s <b>3D digitizer probe:</b> <a href="https://forum.sienci.com/t/using-a-probe-to-digitize-an-object/1019">https://forum.sienci.com/t/using-a-probe-to-digitize-an-object/1019</a>
- Keith's <b>controller box mounting</b> feet: <a href="https://www.facebook.com/groups/mill.one/permalink/903958263408839/">https://www.facebook.com/groups/mill.one/permalink/903958263408839/</a>
- Spike's <b>control panel</b>: <a href="https://www.facebook.com/groups/mill.one/permalink/902963963508269/">https://www.facebook.com/groups/mill.one/permalink/902963963508269/</a>
- <a href="https://forum.sienci.com/u/chrismakesstuff" target="_blank" rel="noopener noreferrer">Chris</a>' <b>vertical stand design</b>: <a href="https://forum.sienci.com/t/stand-design-for-permanent-vertical-cutting/1112" target="_blank" rel="noopener noreferrer">https://forum.sienci.com/t/stand-design-for-permanent-vertical-cutting/1112</a>
- coreyker's <b>pen/pencil spring mount</b>: <a href="https://github.com/coreyker/LongMill/tree/main/PenMountV1" target="_blank" rel="noopener">https://github.com/coreyker/LongMill/tree/main/PenMountV1</a>
- DustinTheMaker's <b>power supply mount</b>: <a href="https://www.thingiverse.com/thing:4569748" target="_blank" rel="noopener">https://www.thingiverse.com/thing:4569748</a>
- JimAlex's <b>Makita speed stop</b>: <a href="https://www.thingiverse.com/thing:4939138" target="_blank" rel="noopener">https://www.thingiverse.com/thing:4939138</a>
- JimAlex's <b>Tramming bar</b>: <a href="https://www.thingiverse.com/thing:4939863" target="_blank" rel="noopener">https://www.thingiverse.com/thing:4939863</a>

[/su_spoiler]

[su_spoiler title="Limit Switch and Touch Plate" open="no" style="fancy" icon="chevron" anchor_in_url="yes"]

- SimtechBen's <b>touch plate holder</b>: <a href="https://www.thingiverse.com/thing:4948964" target="_blank" rel="noopener">https://www.thingiverse.com/thing:4948964</a>
- Michael's <b>touch plate holder</b>: <a href="https://www.prusaprinters.org/prints/32598-LongMill-touch-plate-holder">https://www.prusaprinters.org/prints/32598-LongMill-touch-plate-holder</a>
- <a href="https://forum.sienci.com/t/homing-limit-switches/99/10" target="_blank" rel="noopener noreferrer">sysimgrp</a>'s redesigned <b>touch plate magnet cover</b>: <a href="https://www.thingiverse.com/thing:4173451" target="_blank" rel="noopener noreferrer">https://www.thingiverse.com/thing:4173451</a>
- <a href="https://forum.sienci.com/t/homing-limit-switches/99/10" target="_blank" rel="noopener noreferrer">sysimgrp</a>'s <b>limit switch mounts</b>: <a href="https://www.thingiverse.com/thing:4189426">https://www.thingiverse.com/thing:4189426</a>
- mcol82's <b>limit switch mounts</b>: <a href="https://www.thingiverse.com/thing:4060347" target="_blank" rel="noopener">https://www.thingiverse.com/thing:4060347</a>
- <a href="https://www.facebook.com/groups/mill.one/permalink/949875162150482/">Frank</a>'s 3D printable <b>touch plate holder</b>: <a href="https://www.facebook.com/groups/mill.one/permalink/976042446200420/">https://www.facebook.com/groups/mill.one/permalink/976042446200420/</a>

[/su_spoiler]

[su_spoiler title="Dust Shoe" open="no" style="fancy" icon="chevron" anchor_in_url="yes"]

- <a href="https://forum.sienci.com/t/dust-shoe-modification/472/10" target="_blank" rel="noopener noreferrer">sysimgrp</a>'s alternative <b>dust shoe design</b>: <a href="https://www.thingiverse.com/thing:4189543" target="_blank" rel="noopener noreferrer">https://www.thingiverse.com/thing:4189543</a>
- <a href="https://forum.sienci.com/t/is-anyone-working-on-something-cool-to-add-functionality-or-improve-their-machine/41/15" target="_blank" rel="noopener noreferrer">Buebeli</a>'s "dustshoe2shopvac" <b>adapter</b>: <a href="https://CAD.onshape.com/documents/68a2af8c900b7568ef2876f5/w/2b75c1cf11dc8870a9c8668e/e/46aa8d16723a461387d04d44" target="_blank" rel="noopener noreferrer">https://CAD.onshape.com/documents/68a2af8c900b7568ef2876f5/w/2b75c1cf11dc8870a9c8668e/e/46aa8d16723a461387d04d44</a>
- Keith's alternative <b>dust shoe design</b>:<a href="https://www.facebook.com/groups/mill.one/permalink/941497279654937/"> https://www.facebook.com/groups/mill.one/permalink/941497279654937/</a>
- Xavier's alternative <b>dust shoe design</b>:<a href="https://www.prusaprinters.org/prints/30167-LongMill-dust-shoe-redesign/files"> https://www.prusaprinters.org/prints/30167-LongMill-dust-shoe-redesign/files</a>
- Stewart's alternative <b>dust shoe design</b>:<a href="https://CAD.onshape.com/documents/f33531ce079ad207c663875f/w/ac37eff1df8958b7eb7f4130/e/a0d7b7aa72f4d9a34b68fc87"> https://CAD.onshape.com/documents/f33531ce079ad207c663875f/w/ac37eff1df8958b7eb7f4130/e/a0d7b7aa72f4d9a34b68fc87</a>
- Stephen's alternative <b>dust shoe design:</b><a href="https://www.facebook.com/groups/mill.one/permalink/909165219554810/"> https://www.facebook.com/groups/mill.one/permalink/909165219554810/</a>
- <a href="https://forum.sienci.com/t/what-does-your-dust-collection-hose-management-look-like/458/15" target="_blank" rel="noopener noreferrer">David</a>'s <b>dust hose boom</b>: <a href="https://www.thingiverse.com/thing:4082855" target="_blank" rel="noopener noreferrer">https://www.thingiverse.com/thing:4082855</a>
<a href="https://CAD.onshape.com/documents/57648b7f221a8b14202c6da4/w/09ca17006a988771f02d3db7/e/6ef8f0a441b6df6b9b3ffa87" target="_blank" rel="noopener noreferrer">https://CAD.onshape.com/documents/57648b7f221a8b14202c6da4/w/09ca17006a988771f02d3db7/e/6ef8f0a441b6df6b9b3ffa87</a>

[/su_spoiler]
