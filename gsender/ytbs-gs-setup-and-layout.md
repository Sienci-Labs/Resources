---
title: ytsb Setup & Layout
menu_order: 4
post_status: draft
post_excerpt: See the gSender's layout to get an understanding of where tools and features are located and where you can go to change your settings or setup your CNC.
post_date: 2021-07-01 14:21
taxonomy:
    knowledgebase_cat: gdocs
    knowledgebase_tag:
        - gsender
custom_fields:
    KBName: gSender
    basepress_post_icon: bp-caret-right
skip_file: no
featured_image: _images/_gsender/_setup/gs_setup_pp_gs_setup_pp01_Annono.jpg
---
<h2>Anonymous Information</h2>

When you open up gSender, you’ll notice a prompt regarding ‘Anonymous usage information’. This is just to ask if you’d be fine with us knowing things like what CNC you use it for, what computer you run it on, and other information about how you use the app. You can imagine that if we know certain features are widely used or certain errors are constantly encountered, that can be very helpful to understand how we can improve the app or its documentation. This is completely optional and anonymous, we only do it with your permission and it can be turned off at any time in the settings menu.

![](/_images/_gsender/_setup/gs_setup_pp_gs_setup_pp01_Annono.jpg){.aligncenter .size-medium}

<h2>Layout</h2>

Before starting to use gSender, let's briefly cover the way its functions are laid out so that you'll know where to find things moving forward. The program only has one main screen, it's into three major sections:

<ul>
  <li>The top toolbar has all the things you'll only use occasionally. This includes machine connection on the left side (boxed in red) and gSender's Settings, Help, and other additional 'Tools' on the right (boxed in blue).</li>
  <li>The left-side control (boxed in green) has all the functions you need for loading, monitoring, and controlling g-code files and cutting jobs</li>
  <li>The right-side control (boxed in purple) has all the functions you need to manually control your CNC when jobs aren't running. This includes jogging, zero setting, homing, probing, running macros, manual laser / spindle control, and more.</li>
</ul>

![](/_images/_gsender/_setup/gs_setup_pp1_gSender-Main-Screen-layout.png){.aligncenter .size-medium}

We’ve built gSender’s layout around these primary boxed sections so that you can have all of the CNC functionality most hobbyists need on one screen without getting confused about what each button does. If you’re doing anything <strong>during</strong> a job it’ll be on the left side, if you’re doing anything <strong>outside</strong> a job it’ll likely be on the right, and if you want greater customization or functionality it’ll be found in the tools or settings.

Another of gSender’s Design Principals is colouring. It can be scary to have an assortment of buttons in front of you and not know what they’re going to do. This is why we made every button on the right-side control that moves the CNC, blue. This means you shouldn’t ever find yourself startled when the machine moves unexpectedly since the colour will help to communicate whether it’s a ‘machine moving’ button or not.

<h2>Configuration</h2>

Let's do some configuration before connecting up to your CNC. Click the 'gear' at the far right of the toolbar to bring up the program settings. Some things you'll likely want to configure would be:

<ul>
  <li><strong data-rich-text-format-boundary="true">General Settings</strong>
<ul>
  <li>Baud rate needed for your particular CNC. Baud rate is setup for the LongMill by default.</li>
  <li>Machine Profile</li>
  <li>Preferred Units</li>
  <li>Reverse workspace (flips the left and right-side controls if you prefer)</li>
</ul>
</li>
</ul>

![](</_images/_gsender/_setup/gs_setup_pp2_gSender general settings.jpg>){.aligncenter .size-medium}

<ul>
  <li><strong>Visualizer Settings</strong>
<ul>
  <li>Set to light theme if you prefer</li>
</ul>
</li>
</ul>

![](/_images/_gsender/_setup/gs_setup_pp3_SettingsVisualizer.png){.aligncenter .size-medium}

<h2>Running Longer Jobs (optional)</h2>

Windows machines can have a tendency to 'fall asleep' on the display and USB ports when running longer CNC jobs, this can cause your intricate cuts to stop short. To circumvent this, you'll have to change your computer power settings so that the port 'stays awake' while cutting.

To keep the display on, you'll want to click the <strong>Windows</strong> icon at the bottom left corner of your screen and start to type “<em>control panel</em>” to bring it up.

![](/_images/_gsender/_setup/gs_setup_pp4_controlPanel.jpg){.aligncenter .size-medium}

Once you’ve clicked to open it, go to <strong>Hardware and Sound </strong>then <strong>Power Options</strong>

![](/_images/_gsender/_setup/gs_setup_pp5_Hard.jpg){.aligncenter .size-medium}

![](/_images/_gsender/_setup/gs_setup_pp6_Power.jpg){.aligncenter .size-medium}

Now, whichever plan you have currently selected (circled in the picture) will be the one that you want to change. You can see in this example we will be editing the <strong>Balanced</strong> plan. Click on the Change plan settings text (highlighted with an arrow).

![](/_images/_gsender/_setup/gs_setup_pp7_Balanced.jpg){.aligncenter .size-medium}

Go to the second drop-down and set both battery and plugged in selection to <strong>Never</strong>, save the changes to ensure that your computer never dozes off on its own.

![](/_images/_gsender/_setup/gs_setup_pp8_Never.png){.aligncenter .size-medium}

To keep the USB ports on, click <strong>Change advanced power settings</strong>

![](/_images/_gsender/_setup/gs_setup_pp9_Advanced.png){.aligncenter .size-medium}

<span style="font-weight: 400;">In the separate window that appears, you’ll want to Expand the </span><b>USB Settings</b><span style="font-weight: 400;">, then </span><b>USB selective suspend setting</b><span style="font-weight: 400;">, and finally change both the battery and plugged in settings for these drop-downs to ‘</span><b>Disabled</b><span style="font-weight: 400;">’. Click OK to </span><b>Apply</b><span style="font-weight: 400;"> these new settings.</span>

![](</_images/_gsender/_setup/gs_setup_pp10_Advanced Options.jpg>){.aligncenter .size-medium}

After having done all of this, just be mindful now that sometimes a Windows update can remove these settings. If you have an update and want to be confident running your CNC, we'd recommend checking back on these settings to make sure they're still set properly.