---
title: ytsb LightBurn Settings
menu_order: 9
post_status: draft
post_excerpt: 
post_date: 2021-12-23 12:56:20
taxonomy:
    knowledgebase_cat: lb-assembly
    knowledgebase_tag:
        - laser
custom_fields:
    KBName: LaserBeam
    basepress_post_icon: bp-caret-right
skip_file: yes
featured_image: 
---

On LightBurn, press the wrench icon on the top toolbar. A dialog box should appear with the title “Device settings for grbl.”

<img class="alignnone size-full wp-image-10874" src="https://resources.sienci.com/wp-content/uploads/2022/03/wrench-lightburn.png" alt="" width="960" height="540" />
<p style="text-align: center;"><em>Wrench icon on LightBurn</em></p>
Make sure that:
<ul>
  <li>“S-value max” is set to <strong>255</strong> – Setting your S value max correctly will ensure you have access to 100% of your laser’s power. This value should always match your maximum spindle speed in gSender (more details in <a href="https://resources.sienci.com/view/lb-gSender-settings/">gSender Settings</a>)</li>
</ul>
<img class="alignnone wp-image-10811 size-full" src="https://resources.sienci.com/wp-content/uploads/2021/12/Laser-Lightburn-settings-e1726690459507.png" alt="" width="2096" height="1180" />
<p style="text-align: center;"><em>LightBurn S-value max setting</em></p>

<ul>
  <li>“Origin” is set as the <strong>bottom left corner</strong> – If you change this, it will flip your work surface when exporting your g-code so it is best to stick with this setting</li>
</ul>
<img class="size-full wp-image-10810 aligncenter" src="https://resources.sienci.com/wp-content/uploads/2021/12/Laser-Lightburn-Origin.png" alt="" width="960" height="540" />
<p style="text-align: center;"><em>Setting origin of projects on LightBurn</em></p>

<ul>
  <li>Under “Z Axis Control,” toggle “Enable Z axis” to <strong>ON</strong> – This will allow the machine to move down during laser cutting operations.</li>
</ul>
<img class="size-full wp-image-10797 aligncenter" src="https://resources.sienci.com/wp-content/uploads/2021/12/enablezaxis-laser.png" alt="" width="960" height="540" />
<p style="text-align: center;"><em>Enable Z axis on LightBurn</em></p>

<ul>
  <li>Press “<strong>OK</strong>” to save your settings</li>
</ul>
