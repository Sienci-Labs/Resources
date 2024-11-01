---
title: Open Source & Modifications 🥽
menu_order: 1
post_status: publish
post_excerpt: Open source documentation for LongMill CNC and its accessories, which includes 3D files, bill of materials. Community modifications and designs also found here.
post_date: 2021-04-30 17:10:00
taxonomy:
    knowledgebase_cat: lm-advanced
    knowledgebase_tag:
        - mk1
custom_fields:
    KBName: LongMill CNC
    basepress_post_icon: bp-caret-right
skip_file: no
featured_image: /_images/_longmill/_advanced/_12_LBDetails/lm_lbdeets_p1_DrawingRev1.4.jpg
---

The LongMill project is at its core an open source project. Many of its design choices, from sourcing as many off the shelf parts as possible to our choice in CAD software, comes down to making this project as replicable and well-supported as possible.

We believe that by making this design open source, we will be able to drive the CNC community forward through sharing and improving CNC technology. The idea is for:

- Users to modify and improve their machines to fit their needs
- Machine owners to share their designs with the community to help others that have similar needs
- Makers to use our design ideas and design philosophy to create other types of machines, such as laser cutters, plasma cutters, and 3D printers
- Us to gain inspiration from the community to help us guide our development of current and future products and features

## License

This is accomplished by putting the project under a <a href="https://creativecommons.org/licenses/by-sa/4.0/" target="_blank" rel="noopener noreferrer">Creative Commons BY-SA license</a><span class="cc-license-title">:</span>

- The entire mechanical design of our LongMill Benchtop CNC available in a range of 3D file types and as drawings where applicable
- Any internal assembly jigs and other supporting hardware for the LongMill
- Documentation of general manufacturing techniques used to produce the LongMills various custom components including general 3D printing settings
- All educational information provided within the LongMill Resources area including machine assembly instructions and modifications
- The mechanical BOM which documents all the components required to build a LongMill
- Every aspect of the electrical design behind our custom LongBoard CNC controller including BOM, schematics, gerber file, etc.

and by sharing the LongMills modified firmware profile, a small modification of the <a href="https://github.com/gnea/grbl/wiki" target="_blank" rel="noopener noreferrer">grbl open source project</a>, under the <a href="https://www.gnu.org/licenses/quick-guide-gplv3.en.html" target="_blank" rel="noopener noreferrer">GPLv3 license</a> just as the original project is.

All this information is continually updated as the LongMill project continues to be revised, with more openly shared shared information being made available at each new major revision and licensing continuing to be applied to all previous major versions. By making this information available, the LongMill project fulfills the Open Source Hardware Association’s definition of open source hardware, and we think that's pretty cool :)

## LongMill CNC

The LongMill has gone through four major iterations of its design:

- V1 was our Kickstarter batch which was shipped from September 2019 to mid-January 2020.
- V2 came with some additional improvements and shipped March 2020 to August 14th, 2020. These changes were mostly process/QA related or were fixes that we implemented to make assembly and packaging easier on our end. The only noticeable improvements made for the end user is the steel vs. plastic ‘arm’ (which really only comes into play during assembly), the longer motor cables, the improved control box (where the primary improvement is the ability to now fasten it down easily), a new LongMill wrench shipped with the machine and better hole clearances.
- V3 introduced even more quality of life improvements such as packing more spare hardware, changing to a new motor connector that ensures more reliable connectivity between the stepper motors and the LongBoard controller, and adding mounting holes for our new dust shoe design. The biggest change with this version were the tweaks to the LongBoard controller which brought a detachable E-stop switch to control power to the box, a top-mounted LED to better indicate power to the board, and some tweaks to the input circuitry so that it could be run a bit more reliably. V3 shipped August 14th, 2020 to November 3rd, 2020.
- V4 was a smaller step in development. Other than introducing the new motor connector as a carry-over from V3 and making a number of small tweaks to hole placement, sizing, drawings, slotting, and removing some legacy features there was nothing too exciting noticeable to LM users, as most changes were made to benefit manufacturing reliability. V4 shipped November 23rd, 2020 to January 11th, 2021.
- V4b has been our step towards a more scalable manufactured LM, bringing along some new parts being sheet metal rather than 3D printed (shoulder brackets and drag chain mount) as well as more improvements to process/QA for more reliable production and easier assembly. Later V4b machines also came with improved hardware bagging and a new, thicker 65mm router mount for added rigidity holding onto the router body. V4b began shipping January 11th, 2021.

You can find the designs of every part and assembly of every version of the LongMill Benchtop CNC in the linked Onshape documents below:

**V1:** <a href="https://CAD.onshape.com/documents/c671532d980f277a13d1ace4/w/95c27aef1c0bb10a840ac8bd/e/c456cde929694e3c560d6883" target="_blank" rel="noopener noreferrer">https://CAD.onshape.com/documents/c671532d980f277a13d1ace4/w/95c27aef1c0bb10a840ac8bd/e/c456cde929694e3c560d6883</a>

**V2:** <a href="https://CAD.onshape.com/documents/07e5303fe93ccde67c101960/w/c7cd5aa0b4420ce125d689ab/e/21328c5ee482d0f23caa87aa" target="_blank" rel="noopener noreferrer">https://CAD.onshape.com/documents/07e5303fe93ccde67c101960/w/c7cd5aa0b4420ce125d689ab/e/21328c5ee482d0f23caa87aa</a>

**V3:** <a href="https://CAD.onshape.com/documents/498d88ac3f37d70d4ee9a95d/w/69f0f3ecd6cb8bdf72023191/e/419deab74edbfeb65aaf28ca" target="_blank" rel="noopener noreferrer">https://CAD.onshape.com/documents/498d88ac3f37d70d4ee9a95d/w/69f0f3ecd6cb8bdf72023191/e/419deab74edbfeb65aaf28ca</a>

**V4:** <a href="https://CAD.onshape.com/documents/0d4aaa126c51e4b2c1a73754/w/ba07e21a09b5d161dce0df44/e/ed54ac208c62df876e8f37e0" target="_blank" rel="noopener">https://CAD.onshape.com/documents/0d4aaa126c51e4b2c1a73754/w/ba07e21a09b5d161dce0df44/e/ed54ac208c62df876e8f37e0</a>

**V4b:** <a href="https://CAD.onshape.com/documents/71a0b61afbc45367bfda17ca/w/6adf75db0dfed5dd26ff86c8/e/30e681303ce7a5ce39142a93" target="_blank" rel="noopener">https://CAD.onshape.com/documents/71a0b61afbc45367bfda17ca/w/6adf75db0dfed5dd26ff86c8/e/30e681303ce7a5ce39142a93</a>

**BOM of every version:** <a href="https://docs.google.com/spreadsheets/d/1MqOwPg3VSUTMtn3ff6rXjfvliAWnFqg8ez2eZasJLCE/" target="_blank" rel="noopener noreferrer">https://docs.google.com/spreadsheets/d/1MqOwPg3VSUTMtn3ff6rXjfvliAWnFqg8ez2eZasJLCE/</a>

## LongBoard CNC Controller

The LongBoard CNC Controller is the control system and brains of the LongMill. This board was designed by our friend Chris Hadjuk and the Sienci Labs team with KiCAD and has gone through many internal iterations resulting in the release of four major public revisions: 1.2, 1.3, and 1.4.2/1.4.3. The reason for combining 1.4.2 with 1.4.3 is that they are the same design but with a redundant trace removed. You can find the designs of every version in the form of gerber, assembly, schematic, and BOM files in their respective zip files below as well as a link to a more readable BOM for every board version if you'd like to source your own components.

<a href="https://resources.sienci.com/wp-content/uploads/2021/04/Sienci-LongBoard-Rev-1.2.zip" target="_blank" rel="noopener">Rev-1.2 LongBoard Design</a>

<a href="https://resources.sienci.com/wp-content/uploads/2021/04/Sienci-LongBoard-Rev-1.3.zip" target="_blank" rel="noopener">Rev-1.3 LongBoard Design</a>

<a href="https://resources.sienci.com/wp-content/uploads/2021/04/Sienci-LongBoard-Rev-1.4.3-1.zip" target="_blank" rel="noopener">Rev-1.4.3 LongBoard Design</a>

**BOM of every version:** <a href="https://docs.google.com/spreadsheets/d/1qlHlp576s9GIBMPfp4JU8Yr7xBM5gUNruvHFBVFoDOM" target="_blank" rel="noopener">https://docs.google.com/spreadsheets/d/1qlHlp576s9GIBMPfp4JU8Yr7xBM5gUNruvHFBVFoDOM</a>

## Other Add-ons

We also share a record of every part and assembly of every version of add-on that we've released alongside our LongMill CNC since the projects conception. Each of these designs can be found in the linked Onshape documents below:

[su_row]
[su_column size="1/2" center="no" class="viewer-desc"]**T-Track and Hold Down Clamps**
Custom T-track can uniquely fit common 1/4-20 hardware, clamps can be cut from wood, and clamp ends can be 3D printed to replace them when damaged.<br><br>
<a href="https://resources.sienci.com/wp-content/uploads/2022/03/sienci-wood-clamp-100mm.stl">⭳ CNC the Wood Clamps (STL)</a>
<a href="https://resources.sienci.com/wp-content/uploads/2022/03/sienci-steel-clamp-end-cap.stl">⭳ 3D print the End Caps (STL)</a>
<a href="https://CAD.onshape.com/documents/4002cf32491a7a7a17c84759/w/f9f2dc06d2e8375fa2fb89a3/e/b15017972da9d310d5b53e22" target="_blank" rel="noopener">View, Copy, or Edit in Onshape</a>
[/su_column] [su_column size="1/2" center="no" class=""]![](/_images/_longmill/_advanced/lm-os-sienci-t-tracks-and-clamps.jpg){.aligncenter .size-medium .opensource}[/su_column]
[/su_row]

[su_row]
[su_column size="1/2" center="no" class="viewer-desc"]**Magnetic Dust Shoe**
Adjustable-style dust shoe that allows for height adjustment and removal with the same set of magnets, just grab from underneath and twist off.<br><br>
<a href="https://resources.sienci.com/wp-content/uploads/2024/11/longmill-mk1-magnetic-dust-shoe-body.stl">⭳ 3D print the Shoe Body (STL)</a>
<a href="https://resources.sienci.com/wp-content/uploads/2024/11/longmill-mk1-magnetic-dust-shoe-bristle-hold.stl">⭳ 3D print the Bristle Track (STL)</a>
<a href="https://CAD.onshape.com/documents/a9fe29798e2a4a3b922e0f4c/w/5dddcc3c2571fe6d5db5e9f9/e/9ac187bdd116a3cac962083b" target="_blank" rel="noopener">View, Copy, or Edit in Onshape</a>
[/su_column] [su_column size="1/2" center="no" class=""]![](/_images/_longmill/_advanced/lm-os-longmill-mk1-magnetic-dust-shoe.jpg){.aligncenter .size-medium .opensource}[/su_column]
[/su_row]

[su_row]
[su_column size="1/2" center="no" class="viewer-desc"]**Original Dust Shoe**
Uses 2020 extrusion and knobs to be able to set the height of your shoe based on the material you're cutting.<br><br>
<a href="https://resources.sienci.com/wp-content/uploads/2024/11/longmill-mk1-dust-shoe-hose-adapter.stl">⭳ 3D print the Hose Piece (STL)</a>
<a href="https://CAD.onshape.com/documents/07e5303fe93ccde67c101960/w/c7cd5aa0b4420ce125d689ab/e/69e82b99626dfcaf2b1c2d59" target="_blank" rel="noopener">View, Copy, or Edit in Onshape</a>
[/su_column] [su_column size="1/2" center="no" class=""]![](/_images/_longmill/_advanced/lm-os-longmill-mk1-dust-shoe.jpg){.aligncenter .size-medium .opensource}[/su_column]
[/su_row]

[su_row]
[su_column size="1/2" center="no" class="viewer-desc"]**Touch Plate (3-axis / block-style)**
A typical block-style, 3-axis touch plate we designed for finding X, Y, and Z-zero on 3-axis CNCs.<br><br>
<a href="https://CAD.onshape.com/documents/b76785c85e8458b0e88b64a5/w/0eed2327264503a991f2d6eb/e/47780af64de032893b1197da" target="_blank" rel="noopener">View, Copy, or Edit in Onshape</a>
[/su_column] [su_column size="1/2" center="no" class=""] [3d_viewer id="11179"] [/su_column]
[/su_row]

[su_row]
[su_column size="1/2" center="no" class="viewer-desc"]**MK1 Inductive Sensor kit**
5V inductive barrel sensors for reliable homing in any environment. Take measurements in Onshape if you want to make your own mounting setup.<br><br>
<a href="https://CAD.onshape.com/documents/15239cb55b0f1ca51ac023d5/w/99c28fb4551b087c3e771995/e/f03172e385d7c2967cc4f03c" target="_blank" rel="noopener">View, Copy, or Edit in Onshape</a>
[/su_column] [su_column size="1/2" center="no" class=""]![](/_images/_longmill/_advanced/lm-os-longmill-mk1-inductive-sensors.jpg){.aligncenter .size-medium .opensource}[/su_column]
[/su_row]

**BOM of all add-ons:** <a href="https://docs.google.com/spreadsheets/d/1MqOwPg3VSUTMtn3ff6rXjfvliAWnFqg8ez2eZasJLCE/edit#gid=1028766194" target="_blank" rel="noopener">https://docs.google.com/spreadsheets/d/1MqOwPg3VSUTMtn3ff6rXjfvliAWnFqg8ez2eZasJLCE/edit#gid=1028766194</a>

## 3D Printing

To read more about our print settings to help you print your own parts, read this post here: <a href="https://sienci.com/2019/11/11/3d-printing-settings-for-LongMill-parts/">https://sienci.com/2019/11/11/3d-printing-settings-for-LongMill-parts/</a>
STL files can be directly downloaded from the Onshape document. You may need to make an account to download STL files.

## Modifications

If there are any known noteworthy designs or modifications made to the LongMill, they will be posted here. This is to make the information needed for modification more accessible and to also thank and recognize users and community members who have made an impact on the LongMill CNC project.

### General

<ul>
  <li>mcol82's <b>limit switch mounts</b>: <a href="https://www.thingiverse.com/thing:4060347" target="_blank" rel="noopener">https://www.thingiverse.com/thing:4060347</a></li>
  <li>coogle's <b>Control box feet mounts</b>: <a href="https://www.thingiverse.com/thing:4049019" target="_blank" rel="noopener">https://www.thingiverse.com/thing:4049019</a></li>
  <li>coogle's <b>CNC table design</b>: <a href="https://www.thingiverse.com/thing:4049035" target="_blank" rel="noopener">https://www.thingiverse.com/thing:4049035</a></li>
  <li><a href="https://forum.sienci.com/t/homing-limit-switches/99/10" target="_blank" rel="noopener noreferrer">sysimgrp</a>'s <b>limit switch mounts</b>: <a href="https://www.thingiverse.com/thing:4189426">https://www.thingiverse.com/thing:4189426</a></li>
  <li><a href="https://forum.sienci.com/t/new-control-box-in-progress/428/2" target="_blank" rel="noopener noreferrer">David</a>'s <b>switching box</b>: <a href="https://www.thingiverse.com/thing:4077356" target="_blank" rel="noopener noreferrer">https://www.thingiverse.com/thing:4077356</a>
<a href="https://CAD.onshape.com/documents/4a032d38229a5e4fdfc29ad2/w/3fdd62166f15b2bca45b86dd/e/76713fef2f3d04737acac6ce" target="_blank" rel="noopener noreferrer">https://CAD.onshape.com/documents/4a032d38229a5e4fdfc29ad2/w/3fdd62166f15b2bca45b86dd/e/76713fef2f3d04737acac6ce</a></li>
  <li><a href="https://forum.sienci.com/t/homing-limit-switches/99/10" target="_blank" rel="noopener noreferrer">sysimgrp</a>'s redesigned <b>touch plate magnet cover</b>: <a href="https://www.thingiverse.com/thing:4173451" target="_blank" rel="noopener noreferrer">https://www.thingiverse.com/thing:4173451</a></li>
  <li><a href="https://forum.sienci.com/t/homing-limit-switches/99/10" target="_blank" rel="noopener noreferrer">sysimgrp</a>'s 3D printable <b>laser diode centre-point locator</b>: <a href="https://www.thingiverse.com/thing:4189396" target="_blank" rel="noopener noreferrer">https://www.thingiverse.com/thing:4189396</a></li>
  <li><span class="first username"><a href="https://forum.sienci.com/u/mikecmp" data-user-card="mikecmp">Mike</a>'s CNCable <b>keyboard and monitor shelf</b>: <a href="https://forum.sienci.com/t/what-are-your-plans-for-a-table/95/30" target="_blank" rel="noopener noreferrer">https://forum.sienci.com/t/what-are-your-plans-for-a-table/95/30</a></span></li>
  <li><span class="first username"><a href="https://forum.sienci.com/u/gwilki" data-user-card="gwilki">Grant</a>'s </span>Y-axis <b>plastic bumpers</b>: <a href="https://forum.sienci.com/t/y-axis-modification-bumpers/560" target="_blank" rel="noopener noreferrer">https://forum.sienci.com/t/y-axis-modification-bumpers/560</a></li>
  <li><span class="first username"><a href="https://forum.sienci.com/u/gwilki" data-user-card="gwilki">Grant</a>'s CNC <b>control keypad</b>: <a href="https://forum.sienci.com/t/anyone-using-pendant-feature-of-ugs/503/16" target="_blank" rel="noopener noreferrer">https://forum.sienci.com/t/anyone-using-pendant-feature-of-ugs/503/16</a>
</span></li>
  <li>Dave's 3D printable Makita <b>router under-light</b>: <a href="https://www.facebook.com/groups/mill.one/permalink/801433143661352/" target="_blank" rel="noopener noreferrer">https://www.facebook.com/groups/mill.one/permalink/801433143661352/</a></li>
  <li>Michael's 3D printable <b>T-track stops</b>: <a href="https://www.facebook.com/groups/mill.one/permalink/884002938737705/" target="_blank" rel="noopener noreferrer">https://www.facebook.com/groups/mill.one/permalink/884002938737705/</a></li>
  <li><span class="first username"><a href="https://forum.sienci.com/u/jwoody18" data-user-card="jwoody18">Jeff</a>'s CNCable <b>dust shrouds</b>: <a href="https://forum.sienci.com/t/alligator-ribs-for-dust-shields-along-the-y-axis/749" target="_blank" rel="noopener noreferrer">https://forum.sienci.com/t/alligator-ribs-for-dust-shields-along-the-y-axis/749</a></span></li>
  <li>Brian’s 3D printable <b>bit length sensor</b>: <a href="https://www.facebook.com/groups/mill.one/permalink/970109396793725/"> https://www.facebook.com/groups/mill.one/permalink/970109396793725/</a></li>
  <li><a href="https://forum.sienci.com/u/Lumpy">Kris</a>’s <b>laser setup</b>: <a href="https://forum.sienci.com/t/adding-a-laser-my-journey-tutorial/1183?fbclid=IwAR0nifeyE9wgvco_pMnz9-R1-q9TWF5jIzKo0rhJ2ZAi8kFTdMw38HIr4Vg"> https://forum.sienci.com/t/adding-a-laser-my-journey-tutorial/1183</a></li>
  <li><a href="https://www.facebook.com/groups/mill.one/permalink/949875162150482/">Frank</a>’s 3D printable <b>touch plate holder</b>: <a href="https://www.facebook.com/groups/mill.one/permalink/976042446200420/"> https://www.facebook.com/groups/mill.one/permalink/976042446200420/</a></li>
  <li>Dave’s <b>LED lighting setup</b>: <a href="https://www.facebook.com/groups/mill.one/permalink/928459777625354/"> https://www.facebook.com/groups/mill.one/permalink/928459777625354/</a></li>
  <li>Michael’s <b>touch plate holder</b>: <a href="https://www.prusaprinters.org/prints/32598-LongMill-touch-plate-holder"> https://www.prusaprinters.org/prints/32598-LongMill-touch-plate-holder</a></li>
  <li><a href="https://forum.sienci.com/u/BillKorn">BillKorn</a>’s <b>drag knife</b>: <a href="https://forum.sienci.com/t/drag-knife-for-thin-stock/768"> https://forum.sienci.com/t/drag-knife-for-thin-stock/768</a></li>
  <li><a href="https://forum.sienci.com/u/BillKorn">BillKorn</a>’s <b>3D digitizer probe</b>: <a href="https://forum.sienci.com/t/using-a-probe-to-digitize-an-object/1019"> https://forum.sienci.com/t/using-a-probe-to-digitize-an-object/1019</a></li>
  <li>Keith’s <b>controller box mounting</b> feet:<a href="https://www.facebook.com/groups/mill.one/permalink/903958263408839/"> https://www.facebook.com/groups/mill.one/permalink/903958263408839/</a></li>
  <li>Spike’s <b>control panel</b>:<a href="https://www.facebook.com/groups/mill.one/permalink/902963963508269/"> https://www.facebook.com/groups/mill.one/permalink/902963963508269/</a></li>
  <li><a href="https://forum.sienci.com/u/chrismakesstuff" target="_blank" rel="noopener noreferrer">Chris</a>' <b>vertical stand design</b>: <a href="https://forum.sienci.com/t/stand-design-for-permanent-vertical-cutting/1112" target="_blank" rel="noopener noreferrer">https://forum.sienci.com/t/stand-design-for-permanent-vertical-cutting/1112</a></li>
  <li>coreyker's <b>pen/pencil spring mount</b>: <a href="https://github.com/coreyker/LongMill/tree/main/PenMountV1" target="_blank" rel="noopener">https://github.com/coreyker/LongMill/tree/main/PenMountV1</a></li>
  <li>DustinTheMaker's <b>power supply mount</b>: <a href="https://www.thingiverse.com/thing:4569748" target="_blank" rel="noopener">https://www.thingiverse.com/thing:4569748</a></li>
  <li>JimAlex's <b>Makita speed stop</b>: <a href="https://www.thingiverse.com/thing:4939138" target="_blank" rel="noopener">https://www.thingiverse.com/thing:4939138</a></li>
  <li>JimAlex's <b>Tramming bar</b>: <a href="https://www.thingiverse.com/thing:4939863" target="_blank" rel="noopener">https://www.thingiverse.com/thing:4939863</a></li>
  <li>SimtechBen’s <b>touch plate holder</b>: <a href="https://www.thingiverse.com/thing:4948964" target="_blank" rel="noopener">https://www.thingiverse.com/thing:4948964</a></li>
</ul>

### Dust Shoe Mods

<ul>
  <li><a href="https://forum.sienci.com/t/dust-shoe-modification/472/10" target="_blank" rel="noopener noreferrer">sysimgrp</a>'s alternative <b>dust shoe design</b>: <a href="https://www.thingiverse.com/thing:4189543" target="_blank" rel="noopener noreferrer">https://www.thingiverse.com/thing:4189543</a></li>
  <li><a href="https://forum.sienci.com/t/is-anyone-working-on-something-cool-to-add-functionality-or-improve-their-machine/41/15" target="_blank" rel="noopener noreferrer">Buebeli</a>'s “dustshoe2shopvac” <b>adapter</b>: <a href="https://CAD.onshape.com/documents/68a2af8c900b7568ef2876f5/w/2b75c1cf11dc8870a9c8668e/e/46aa8d16723a461387d04d44" target="_blank" rel="noopener noreferrer">https://CAD.onshape.com/documents/68a2af8c900b7568ef2876f5/w/2b75c1cf11dc8870a9c8668e/e/46aa8d16723a461387d04d44</a></li>
  <li>Keith’s alternative <b>dust shoe design</b>: <a href="https://www.facebook.com/groups/mill.one/permalink/941497279654937/"> https://www.facebook.com/groups/mill.one/permalink/941497279654937/</a></li>
  <li>Xavier’s alternative <b>dust shoe design</b>: <a href="https://www.prusaprinters.org/prints/30167-LongMill-dust-shoe-redesign/files"> https://www.prusaprinters.org/prints/30167-LongMill-dust-shoe-redesign/files</a></li>
  <li>Stewart’s alternative <b>dust shoe design</b>: <a href="https://CAD.onshape.com/documents/f33531ce079ad207c663875f/w/ac37eff1df8958b7eb7f4130/e/a0d7b7aa72f4d9a34b68fc87"> https://CAD.onshape.com/documents/f33531ce079ad207c663875f/w/ac37eff1df8958b7eb7f4130/e/a0d7b7aa72f4d9a34b68fc87</a></li>
  <li>Stephen’s alternative <b>dust shoe design</b>: <a href="https://www.facebook.com/groups/mill.one/permalink/909165219554810/"> https://www.facebook.com/groups/mill.one/permalink/909165219554810/</a></li>
  <li><a href="https://forum.sienci.com/t/what-does-your-dust-collection-hose-management-look-like/458/15" target="_blank" rel="noopener noreferrer">David</a>'s <b>dust hose boom</b>: <a href="https://www.thingiverse.com/thing:4082855" target="_blank" rel="noopener noreferrer">https://www.thingiverse.com/thing:4082855</a>
<a href="https://CAD.onshape.com/documents/57648b7f221a8b14202c6da4/w/09ca17006a988771f02d3db7/e/6ef8f0a441b6df6b9b3ffa87" target="_blank" rel="noopener noreferrer">https://CAD.onshape.com/documents/57648b7f221a8b14202c6da4/w/09ca17006a988771f02d3db7/e/6ef8f0a441b6df6b9b3ffa87</a></li>
</ul>

## Onshape

You may notice that many of the 3D models we share in our open source documents link to a 3D file on a website called “Onshape”. This is the browser-based software that the engineers and designers on our team use to design and iterate on all the products we produce at Sienci Labs. The fact that it’s online has the great advantage that anytime we make an update or release a new product, you are able to see them live or download them for yourself. We feel this is a great way to keep our company open and make our designs easily accessible to others.

### Interact with Designs

Let’s cover a couple things you can do with the open source Onshape files:

<img class="size-full wp-image-10638 aligncenter" src="https://resources.sienci.com/wp-content/uploads/2022/03/onshape-file-viewing.jpg" alt="" width="988" height="165" />

1. **Look at the design from all sides**
   - **Rotate** around by right-clicking on your mouse and dragging around on the screen, or clicking the ‘rotate’ tool on the toolbar and left-click dragging on the screen, or clicking the buttons on the cube at the top, right of the screen
   - **Zoom** in and out by scrolling on your mouse or clicking the down arrow next to the magnifying glass on the toolbar and then left-click and drag up-and-down to see closer and further
1. **See a list of all the parts** in the design
   - This shows up on the left-hand side of the window, where if you click the name it’ll highlight the 3D model
   - This makes it easy to know the names and parts of everything that makes up the full design
1. **Measure different parts** of the design
   - After selecting the measuring tape on the toolbar and selecting the units you’d like to measure, you can click anywhere on the model to get length of a line, distance between two points or faces, angle between two lines or faces, surface area, and more
   - If you want to measure something else, just click somewhere in the blank space or hit the spacebar and then select the new spots you want to measure
   - This is especially useful for quickly verifying dimensions, checking clearances, and ensuring design accuracy. Feel free to save measurements by writing them down or taking screenshots as a reference for your own purposes
1. Even see the **Mass and Volume** of the parts!
   - This uses the right-most Mass tool on the toolbar where after selecting the tool and selecting a part you can get even more information on its properties
   - This can be useful is you’re working on a modification and need to decide how strong to make it based on the weight of some other parts
   - We try to make sure these values are all as accurate as possible but there still might be some discrepancy

### Export or Modify

If you want to Export our Onshape designs as either a **3D model** (STL, IGES, STEP) or a **2D drawing** (DWG, DXF) for your own tweaks or accessories, then:

1. Open the link to the design you’d like to download.
1. Use the ‘Export’ option in the toolbar to either export the whole design or use the down arrow to allow you to export only individual parts or assemblies. You can select these parts by clicking on the 3D model or by clicking on the parts list on the left-hand side of the window.  
<img class="aligncenter wp-image-10647 size-full" src="https://resources.sienci.com/wp-content/uploads/2022/03/mk25_ad_onshape1-e1726085290809.jpg" alt="" width="385" height="206" />
1. When you’ve selected all your parts, you’ll be given more options to choose the file type you want to download as and other options based on your selections. Typically STLs are used for 3D printing, IGES and STEP are good for importing to other design software to modify the files, and DXF or DWG are used for laser or plasma cutting. Typically the other files defaults tend to be good to use.
<img class="size-full wp-image-10646 aligncenter" src="https://resources.sienci.com/wp-content/uploads/2022/03/mk25_ad_onshape2.jpg" alt="" width="1008" height="603" />
1. After configuring the settings, click "Export" and you should find the file appears in your typical download location.

If instead of Exporting the files, you’d like to use Onshape as your main design software to make and publish modifications, then you'll need to make an account first; though luckily it’s free to make one:

1. Open your web browser and go to the <a href="https://www.onshape.com/en/sign-up" target="_blank" rel="noopener">Onshape Sign up page</a>.
1. Enter your Name and Email Address, then Onshape will ask for some other information that you might need to fill out and some Terms & Conditions.
1. Once you get to the end, you’ll be sent a verification email which you can click through to set up your password. You don’t need to enter a Company name but you do need to agree to some more Terms & Conditions.
1. Once you’re set up, feel free to set your default units and controls - or get straight to downloading the models since you can always change these later in your settings.

Once you've successfully created an account and you’re logged in:

1. Copy our entire design file into your own workspace by clicking the button with three lines at the top, left corner of the window, and select **Copy workspace**.
<img class="aligncenter wp-image-10645 size-full" src="https://resources.sienci.com/wp-content/uploads/2022/03/mk25_ad_onshape3-e1726085340430.jpg" alt="" width="1159" height="566" />
1. Give the copied version its own name.
1. You can now make changes to the file using Onshape’s various editing tools! These tools allow you to add or remove features, adjust dimensions, edit sketches, modify assemblies, and more.
<img class="aligncenter wp-image-10644 size-full" src="https://resources.sienci.com/wp-content/uploads/2022/03/mk25_ad_onshape4-e1726085361506.jpg" alt="" width="1457" height="664" />
1. As you make modifications, Onshape will automatically save your progress, and if you’re unfamiliar with what the features do there are plenty of guides out there on how to use Onshape.
1. Once you’re done, remember to share your work with us and the community by sharing the link to your Onshape designs so everyone can see your cool stuff!

The sky's the limit now that you can measure, export, copy and modify all of your CAD projects! Remember to **share your learnings and collaborate with others** to continue the spread of open source ideas.
