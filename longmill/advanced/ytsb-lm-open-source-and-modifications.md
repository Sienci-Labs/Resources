---
title: ytsb Open-source & Modifications 🥽
menu_order: 4
post_status: draft
post_excerpt: Open source documentation for LongMill CNC and its accessories, which includes 3D files, bill of materials. Community modifications and designs also found here.
post_date: 2024-04-30 17:11
taxonomy:
    knowledgebase_cat: lm-advanced
    knowledgebase_tag:
        - mk1
custom_fields:
    KBName: LongMill CNC
    basepress_post_icon: bp-caret-right
skip_file: no
featured_image: 
---
The LongMill project is at its core an open-source project. Many of its design choices, from sourcing as many off the shelf parts as possible to our choice in CAD software, comes down to making this project as replicable and well-supported as possible.

We believe that by making this design open-source, we will be able to drive the CNC community forward through sharing and improving CNC technology. The idea is for:

<ul>
  <li>Users to modify and improve their machines to fit their needs</li>
  <li>Machine owners to share their designs with the community to help others that have similar needs</li>
  <li>Makers to use our design ideas and design philosophy to create other types of machines, such as laser cutters, plasma cutters, and 3D printers</li>
  <li>Us to gain inspiration from the community to help us guide our development of current and future products and features</li>
</ul>

<h2>License</h2>

This is accomplished by putting the project under a <a href="https://creativecommons.org/licenses/by-sa/4.0/" target="_blank" rel="noopener noreferrer">Creative Commons BY-SA license</a><span class="cc-license-title">:</span>

<ul>
  <li>The entire mechanical design of our LongMills Benchtop CNC available in a range of 3D file types and as drawings where applicable</li>
  <li>Any internal assembly jigs and other supporting hardware for the LongMill</li>
  <li>Documentation of general manufacturing techniques used to produce the LongMills various custom components including general 3D printing settings</li>
  <li>All educational information provided within the LongMill Resources area including machine assembly instructions and modifications</li>
  <li>The mechanical BOM which documents all the components required to build a LongMill</li>
  <li>Every aspect of the electrical design behind our custom LongBoard CNC controller including BOM, schematics, gerber file, etc.</li>
</ul>

and by sharing the LongMills modified firmware profile, a small modification of the <a href="https://github.com/gnea/grbl/wiki" target="_blank" rel="noopener noreferrer">grbl open-source project</a>, under the <a href="https://www.gnu.org/licenses/quick-guide-gplv3.en.html" target="_blank" rel="noopener noreferrer">GPLv3 license</a> just as the original project is.

All this information is continually updated as the LongMill project continues to be revised, with more openly shared shared information being made available at each new major revision and licensing continuing to be applied to all previous major versions. By making this information available, the LongMill project fulfills the Open Source Hardware Association’s definition of open source hardware, and we think that's pretty cool :)

<h2>LongMill CNC</h2>

The LongMill has gone through four major iterations of its design:

<ul>
  <li>V1 was our Kickstarter batch which was shipped from September 2019 to mid-January 2020.</li>
  <li>V2 came with some additional improvements and shipped March 2020 to August 14th, 2020. These changes were mostly process/QA related or were fixes that we implemented to make assembly and packaging easier on our end. The only noticeable improvements made for the end user is the steel vs. plastic ‘arm’ (which really only comes into play during assembly), the longer motor cables, the improved control box (where the primary improvement is the ability to now fasten it down easily), a new LongMill wrench shipped with the machine and better hole clearances.</li>
  <li>V3 introduced even more quality of life improvements such as packing more spare hardware, changing to a new motor connector that ensures more reliable connectivity between the stepper motors and the LongBoard controller, and adding mounting holes for our new dust shoe design. The biggest change with this version were the tweaks to the LongBoard controller which brought a detachable E-stop switch to control power to the box, a top-mounted LED to better indicate power to the board, and some tweaks to the input circuitry so that it could be run a bit more reliably. V3 shipped August 14th, 2020 to November 3rd, 2020.</li>
  <li>V4 was a smaller step in development. Other than introducing the new motor connector as a carry-over from V3 and making a number of small tweaks to hole placement, sizing, drawings, slotting, and removing some legacy features there was nothing too exciting noticeable to LM users, as most changes were made to benefit manufacturing reliability. V4 shipped November 23rd, 2020 to January 11th, 2021.</li>
  <li>V4b has been our step towards a more scalable manufactured LM, bringing along some new parts being sheet metal rather than 3D printed (shoulder brackets and drag chain mount) as well as more improvements to process/QA for more reliable production and easier assembly. Later V4b machines also came with improved hardware bagging and a new, thicker 65mm router mount for added rigidity holding onto the router body. V4b began shipping January 11th, 2021.</li>
</ul>

You can find the designs of every part and assembly of every version of the LongMill Benchtop CNC in the linked Onshape documents below:

<strong>V1:</strong> <a href="https://CAD.onshape.com/documents/c671532d980f277a13d1ace4/w/95c27aef1c0bb10a840ac8bd/e/c456cde929694e3c560d6883" target="_blank" rel="noopener noreferrer">https://cad.onshape.com/documents/c671532d980f277a13d1ace4/w/95c27aef1c0bb10a840ac8bd/e/c456cde929694e3c560d6883</a>

<strong>V2:</strong> <a href="https://CAD.onshape.com/documents/07e5303fe93ccde67c101960/w/c7cd5aa0b4420ce125d689ab/e/21328c5ee482d0f23caa87aa" target="_blank" rel="noopener noreferrer">https://cad.onshape.com/documents/07e5303fe93ccde67c101960/w/c7cd5aa0b4420ce125d689ab/e/21328c5ee482d0f23caa87aa</a>

<strong>V3: </strong><a href="https://CAD.onshape.com/documents/498d88ac3f37d70d4ee9a95d/w/69f0f3ecd6cb8bdf72023191/e/419deab74edbfeb65aaf28ca" target="_blank" rel="noopener noreferrer">https://cad.onshape.com/documents/498d88ac3f37d70d4ee9a95d/w/69f0f3ecd6cb8bdf72023191/e/419deab74edbfeb65aaf28ca</a>

<strong>V4:</strong> <a href="https://CAD.onshape.com/documents/0d4aaa126c51e4b2c1a73754/w/ba07e21a09b5d161dce0df44/e/ed54ac208c62df876e8f37e0" target="_blank" rel="noopener">https://cad.onshape.com/documents/0d4aaa126c51e4b2c1a73754/w/ba07e21a09b5d161dce0df44/e/ed54ac208c62df876e8f37e0</a>

<strong>V4b: </strong><a href="https://CAD.onshape.com/documents/71a0b61afbc45367bfda17ca/w/6adf75db0dfed5dd26ff86c8/e/30e681303ce7a5ce39142a93" target="_blank" rel="noopener">https://cad.onshape.com/documents/71a0b61afbc45367bfda17ca/w/6adf75db0dfed5dd26ff86c8/e/30e681303ce7a5ce39142a93</a>

<strong>BOM of every version: </strong><a href="https://docs.google.com/spreadsheets/d/1MqOwPg3VSUTMtn3ff6rXjfvliAWnFqg8ez2eZasJLCE/" target="_blank" rel="noopener noreferrer">https://docs.google.com/spreadsheets/d/1MqOwPg3VSUTMtn3ff6rXjfvliAWnFqg8ez2eZasJLCE/</a>

<h2>LongBoard CNC Controller</h2>

The LongBoard CNC Controller is the control system and brains of the LongMill. This board was designed by our friend Chris Hadjuk and the Sienci Labs team with KiCAD and has gone through many internal iterations resulting in the release of four major public revisions: 1.2, 1.3, and 1.4.2/1.4.3. The reason for combining 1.4.2 with 1.4.3 is that they are the same design but with a redundant trace removed. You can find the designs of every version in the form of gerber, assembly, schematic, and BOM files in their respective zip files below as well as a link to a more readable BOM for every board version if you'd like to source your own components.

<a href="https://resources.sienci.com/wp-content/uploads/2021/04/Sienci-LongBoard-Rev-1.2.zip" target="_blank" rel="noopener">Rev-1.2 LongBoard Design</a>

<a href="https://resources.sienci.com/wp-content/uploads/2021/04/Sienci-LongBoard-Rev-1.3.zip" target="_blank" rel="noopener">Rev-1.3 LongBoard Design</a>

<a href="https://resources.sienci.com/wp-content/uploads/2021/04/Sienci-LongBoard-Rev-1.4.3-1.zip" target="_blank" rel="noopener">Rev-1.4.3 LongBoard Design</a>

<strong>BOM of every version:</strong> <a href="https://docs.google.com/spreadsheets/d/1qlHlp576s9GIBMPfp4JU8Yr7xBM5gUNruvHFBVFoDOM" target="_blank" rel="noopener">https://docs.google.com/spreadsheets/d/1qlHlp576s9GIBMPfp4JU8Yr7xBM5gUNruvHFBVFoDOM</a><strong>
</strong>

<h2>Other Add-ons</h2>

We also share a record of every part and assembly of every version of add-on that we've released alongside our LongMill CNC since the projects conception. Each of these designs can be found in the linked Onshape documents below:

<strong>Original dust shoe:</strong> <a href="https://CAD.onshape.com/documents/07e5303fe93ccde67c101960/w/c7cd5aa0b4420ce125d689ab/e/69e82b99626dfcaf2b1c2d59" target="_blank" rel="noopener noreferrer">https://cad.onshape.com/documents/07e5303fe93ccde67c101960/w/c7cd5aa0b4420ce125d689ab/e/69e82b99626dfcaf2b1c2d59</a>

<strong>3-axis touch plate:</strong> <a href="https://CAD.onshape.com/documents/b76785c85e8458b0e88b64a5/w/0eed2327264503a991f2d6eb/e/52643898e09eacae9cfe69aa" target="_blank" rel="noopener noreferrer">https://cad.onshape.com/documents/b76785c85e8458b0e88b64a5/w/0eed2327264503a991f2d6eb/e/52643898e09eacae9cfe69aa</a>

<strong>Magnetic dust shoe:</strong> <a href="https://CAD.onshape.com/documents/a9fe29798e2a4a3b922e0f4c/w/5dddcc3c2571fe6d5db5e9f9/e/9ac187bdd116a3cac962083b" target="_blank" rel="noopener noreferrer">https://cad.onshape.com/documents/a9fe29798e2a4a3b922e0f4c/w/5dddcc3c2571fe6d5db5e9f9/e/9ac187bdd116a3cac962083b</a>

<strong>T-Track and hold down clamps:</strong> <a href="https://CAD.onshape.com/documents/4002cf32491a7a7a17c84759/w/f9f2dc06d2e8375fa2fb89a3/e/b15017972da9d310d5b53e22" target="_blank" rel="noopener noreferrer">https://cad.onshape.com/documents/4002cf32491a7a7a17c84759/w/f9f2dc06d2e8375fa2fb89a3/e/b15017972da9d310d5b53e22</a>

<strong>Inductive Limit Switch kit:</strong> <a href="https://CAD.onshape.com/documents/15239cb55b0f1ca51ac023d5/w/99c28fb4551b087c3e771995/e/f03172e385d7c2967cc4f03c?">https://cad.onshape.com/documents/15239cb55b0f1ca51ac023d5/w/99c28fb4551b087c3e771995/e/f03172e385d7c2967cc4f03c?</a>

<strong>BOM of all add-ons: </strong><a href="https://docs.google.com/spreadsheets/d/1MqOwPg3VSUTMtn3ff6rXjfvliAWnFqg8ez2eZasJLCE/edit#gid=1028766194" target="_blank" rel="noopener">https://docs.google.com/spreadsheets/d/1MqOwPg3VSUTMtn3ff6rXjfvliAWnFqg8ez2eZasJLCE/edit#gid=1028766194</a>

<h2>3D Printing</h2>

To read more about our print settings to help you print your own parts, read this post here: <a href="https://sienci.com/2019/11/11/3d-printing-settings-for-LongMill-parts/">https://sienci.com/2019/11/11/3d-printing-settings-for-longmill-parts/</a>
STL files can be directly downloaded from the Onshape document. You may need to make an account to download STL files.

<h2>Modifications</h2>

If there are any known noteworthy designs or modifications made to the LongMill, they will be posted here. This is to make the information needed for modification more accessible and to also thank and recognize users and community members who have made an impact on the LongMill CNC project.

<h3>General</h3>

<ul>
  <li>mcol82's <strong>limit switch mounts</strong>: <a href="https://www.thingiverse.com/thing:4060347" target="_blank" rel="noopener">https://www.thingiverse.com/thing:4060347</a></li>
  <li>coogle's <strong>Control box feet mounts</strong>: <a href="https://www.thingiverse.com/thing:4049019" target="_blank" rel="noopener">https://www.thingiverse.com/thing:4049019</a></li>
  <li>coogle's <strong>CNC table design</strong>: <a href="https://www.thingiverse.com/thing:4049035" target="_blank" rel="noopener">https://www.thingiverse.com/thing:4049035</a></li>
  <li><a href="https://forum.sienci.com/t/homing-limit-switches/99/10" target="_blank" rel="noopener noreferrer">sysimgrp</a>'s <strong>limit switch mounts</strong>: <a href="https://www.thingiverse.com/thing:4189426">https://www.thingiverse.com/thing:4189426</a></li>
  <li><a href="https://forum.sienci.com/t/new-control-box-in-progress/428/2" target="_blank" rel="noopener noreferrer">David</a>'s <strong>switching box</strong>: <a href="https://www.thingiverse.com/thing:4077356" target="_blank" rel="noopener noreferrer">https://www.thingiverse.com/thing:4077356</a>
<a href="https://CAD.onshape.com/documents/4a032d38229a5e4fdfc29ad2/w/3fdd62166f15b2bca45b86dd/e/76713fef2f3d04737acac6ce" target="_blank" rel="noopener noreferrer">https://cad.onshape.com/documents/4a032d38229a5e4fdfc29ad2/w/3fdd62166f15b2bca45b86dd/e/76713fef2f3d04737acac6ce</a></li>
  <li><a href="https://forum.sienci.com/t/homing-limit-switches/99/10" target="_blank" rel="noopener noreferrer">sysimgrp</a>'s redesigned <strong>touch plate magnet cover</strong>: <a href="https://www.thingiverse.com/thing:4173451" target="_blank" rel="noopener noreferrer">https://www.thingiverse.com/thing:4173451</a></li>
  <li><a href="https://forum.sienci.com/t/homing-limit-switches/99/10" target="_blank" rel="noopener noreferrer">sysimgrp</a>'s 3D printable <strong>laser diode centre-point locator</strong>: <a href="https://www.thingiverse.com/thing:4189396" target="_blank" rel="noopener noreferrer">https://www.thingiverse.com/thing:4189396</a></li>
  <li><span class="first username"><a href="https://forum.sienci.com/u/mikecmp" data-user-card="mikecmp">Mike</a>'s CNCable <strong>keyboard and monitor shelf</strong>: <a href="https://forum.sienci.com/t/what-are-your-plans-for-a-table/95/30" target="_blank" rel="noopener noreferrer">https://forum.sienci.com/t/what-are-your-plans-for-a-table/95/30</a></span></li>
  <li><span class="first username"><a href="https://forum.sienci.com/u/gwilki" data-user-card="gwilki">Grant</a>'s </span>Y-axis <strong>plastic bumpers</strong>: <a href="https://forum.sienci.com/t/y-axis-modification-bumpers/560" target="_blank" rel="noopener noreferrer">https://forum.sienci.com/t/y-axis-modification-bumpers/560</a></li>
  <li><span class="first username"><a href="https://forum.sienci.com/u/gwilki" data-user-card="gwilki">Grant</a>'s CNC <strong>control keypad</strong>: <a href="https://forum.sienci.com/t/anyone-using-pendant-feature-of-ugs/503/16" target="_blank" rel="noopener noreferrer">https://forum.sienci.com/t/anyone-using-pendant-feature-of-ugs/503/16</a>
</span></li>
  <li>Dave's 3D printable Makita <strong>router under-light</strong>: <a href="https://www.facebook.com/groups/mill.one/permalink/801433143661352/" target="_blank" rel="noopener noreferrer">https://www.facebook.com/groups/mill.one/permalink/801433143661352/</a></li>
  <li>Michael's 3D printable <strong>T-track stops</strong>: <a href="https://www.facebook.com/groups/mill.one/permalink/884002938737705/" target="_blank" rel="noopener noreferrer">https://www.facebook.com/groups/mill.one/permalink/884002938737705/</a></li>
  <li><span class="first username"><a href="https://forum.sienci.com/u/jwoody18" data-user-card="jwoody18">Jeff</a>'s CNCable <strong>dust shrouds</strong>: <a href="https://forum.sienci.com/t/alligator-ribs-for-dust-shields-along-the-y-axis/749" target="_blank" rel="noopener noreferrer">https://forum.sienci.com/t/alligator-ribs-for-dust-shields-along-the-y-axis/749</a></span></li>
  <li>Brian’s 3D printable <b>bit length sensor</b>:<a href="https://www.facebook.com/groups/mill.one/permalink/970109396793725/"> https://www.facebook.com/groups/mill.one/permalink/970109396793725/</a></li>
  <li><a href="https://forum.sienci.com/u/Lumpy">Kris</a>’s <b>laser setup</b>:<a href="https://forum.sienci.com/t/adding-a-laser-my-journey-tutorial/1183?fbclid=IwAR0nifeyE9wgvco_pMnz9-R1-q9TWF5jIzKo0rhJ2ZAi8kFTdMw38HIr4Vg"> https://forum.sienci.com/t/adding-a-laser-my-journey-tutorial/1183</a></li>
  <li><a href="https://www.facebook.com/groups/mill.one/permalink/949875162150482/">Frank</a>’s 3D printable <b>touch plate holder</b>:<a href="https://www.facebook.com/groups/mill.one/permalink/976042446200420/"> https://www.facebook.com/groups/mill.one/permalink/976042446200420/</a></li>
  <li>Dave’s <b>LED lighting setup</b>:<a href="https://www.facebook.com/groups/mill.one/permalink/928459777625354/"> https://www.facebook.com/groups/mill.one/permalink/928459777625354/</a></li>
  <li>Michael’s <b>touch plate holder</b>:<a href="https://www.prusaprinters.org/prints/32598-LongMill-touch-plate-holder"> https://www.prusaprinters.org/prints/32598-longmill-touch-plate-holder</a></li>
  <li><a href="https://forum.sienci.com/u/BillKorn">BillKorn</a>’s <b>drag knife</b>:<a href="https://forum.sienci.com/t/drag-knife-for-thin-stock/768"> https://forum.sienci.com/t/drag-knife-for-thin-stock/768</a></li>
  <li><a href="https://forum.sienci.com/u/BillKorn">BillKorn</a>’s <b>3D digitizer probe:</b><a href="https://forum.sienci.com/t/using-a-probe-to-digitize-an-object/1019"> https://forum.sienci.com/t/using-a-probe-to-digitize-an-object/1019</a></li>
  <li>Keith’s <b>controller box mounting</b> feet:<a href="https://www.facebook.com/groups/mill.one/permalink/903958263408839/"> https://www.facebook.com/groups/mill.one/permalink/903958263408839/</a></li>
  <li>Spike’s <b>control panel</b>:<a href="https://www.facebook.com/groups/mill.one/permalink/902963963508269/"> https://www.facebook.com/groups/mill.one/permalink/902963963508269/</a></li>
  <li><a href="https://forum.sienci.com/u/chrismakesstuff" target="_blank" rel="noopener noreferrer">Chris</a>' <strong>vertical stand design</strong>: <a href="https://forum.sienci.com/t/stand-design-for-permanent-vertical-cutting/1112" target="_blank" rel="noopener noreferrer">https://forum.sienci.com/t/stand-design-for-permanent-vertical-cutting/1112</a></li>
  <li>coreyker's <strong>pen/pencil spring mount</strong>: <a href="https://github.com/coreyker/LongMill/tree/main/PenMountV1" target="_blank" rel="noopener">https://github.com/coreyker/longmill/tree/main/PenMountV1</a></li>
  <li>DustinTheMaker's <strong>power supply mount</strong>: <a href="https://www.thingiverse.com/thing:4569748" target="_blank" rel="noopener">https://www.thingiverse.com/thing:4569748</a></li>
  <li>JimAlex's <strong>Makita speed stop</strong>: <a href="https://www.thingiverse.com/thing:4939138" target="_blank" rel="noopener">https://www.thingiverse.com/thing:4939138</a></li>
  <li>JimAlex's <strong>Tramming bar: </strong><a href="https://www.thingiverse.com/thing:4939863" target="_blank" rel="noopener">https://www.thingiverse.com/thing:4939863</a></li>
  <li>SimtechBen’s <b>touch plate holder</b>: <a href="https://www.thingiverse.com/thing:4948964" target="_blank" rel="noopener">https://www.thingiverse.com/thing:4948964</a></li>
</ul>

<h3>Dust Shoe Mods</h3>

<ul>
  <li><a href="https://forum.sienci.com/t/dust-shoe-modification/472/10" target="_blank" rel="noopener noreferrer">sysimgrp</a>'s alternative <strong>dust shoe design</strong>: <a href="https://www.thingiverse.com/thing:4189543" target="_blank" rel="noopener noreferrer">https://www.thingiverse.com/thing:4189543</a></li>
  <li><a href="https://forum.sienci.com/t/is-anyone-working-on-something-cool-to-add-functionality-or-improve-their-machine/41/15" target="_blank" rel="noopener noreferrer">Buebeli</a>'s “dustshoe2shopvac” <strong>adapter</strong>: <a href="https://CAD.onshape.com/documents/68a2af8c900b7568ef2876f5/w/2b75c1cf11dc8870a9c8668e/e/46aa8d16723a461387d04d44" target="_blank" rel="noopener noreferrer">https://cad.onshape.com/documents/68a2af8c900b7568ef2876f5/w/2b75c1cf11dc8870a9c8668e/e/46aa8d16723a461387d04d44</a></li>
  <li>Keith’s alternative <b>dust shoe design</b>:<a href="https://www.facebook.com/groups/mill.one/permalink/941497279654937/"> https://www.facebook.com/groups/mill.one/permalink/941497279654937/</a></li>
  <li>Xavier’s alternative <b>dust shoe design</b>:<a href="https://www.prusaprinters.org/prints/30167-LongMill-dust-shoe-redesign/files"> https://www.prusaprinters.org/prints/30167-longmill-dust-shoe-redesign/files</a></li>
  <li>Stewart’s alternative <b>dust shoe design</b>:<a href="https://CAD.onshape.com/documents/f33531ce079ad207c663875f/w/ac37eff1df8958b7eb7f4130/e/a0d7b7aa72f4d9a34b68fc87"> https://cad.onshape.com/documents/f33531ce079ad207c663875f/w/ac37eff1df8958b7eb7f4130/e/a0d7b7aa72f4d9a34b68fc87</a></li>
  <li>Stephen’s alternative<b> dust shoe design:</b><a href="https://www.facebook.com/groups/mill.one/permalink/909165219554810/"> https://www.facebook.com/groups/mill.one/permalink/909165219554810/</a></li>
  <li><a href="https://forum.sienci.com/t/what-does-your-dust-collection-hose-management-look-like/458/15" target="_blank" rel="noopener noreferrer">David</a>'s <strong>dust hose boom</strong>: <a href="https://www.thingiverse.com/thing:4082855" target="_blank" rel="noopener noreferrer">https://www.thingiverse.com/thing:4082855</a>
<a href="https://CAD.onshape.com/documents/57648b7f221a8b14202c6da4/w/09ca17006a988771f02d3db7/e/6ef8f0a441b6df6b9b3ffa87" target="_blank" rel="noopener noreferrer">https://cad.onshape.com/documents/57648b7f221a8b14202c6da4/w/09ca17006a988771f02d3db7/e/6ef8f0a441b6df6b9b3ffa87</a></li>
</ul>
