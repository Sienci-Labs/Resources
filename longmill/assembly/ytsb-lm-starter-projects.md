---
title: ytsb Starter Projects 🧱
menu_order: 4
post_status: draft
post_excerpt: Beginner projects to try out on the LongMill CNC. These simple test cuts will allow you to gauge if every is working properly after assembling your machine.
post_date: 2021-04-30 15:10:00
taxonomy:
    knowledgebase_cat: lm-assembly
    knowledgebase_tag:
        - mk1
custom_fields:
    KBName: LongMill CNC
    basepress_post_icon: bp-caret-right
skip_file: no
featured_image: /_images/_longmill/_assembly/_starterprojects/lm_starterp_p1.png
---

Now that you've put together your LongMill, you're probably in a rush to run it for the first time! Well good news, we've put together two different projects for you to try out with minimal requirements and setup.

<h2>LongMill line writing</h2>

This is a very simple file which follows a line writing to spell out "LongMill". The code that's provided below has been made to make a very shallow cut at a low speed out of a 310x45mm piece of material. These conservative settings mean that the file can be run with almost any cutting tool out of almost any type of material. To set it up, mount your material in the cutting area so that it's somewhat square to the machine. Using gSender or the control software of your preference, jog the tool over to the bottom left of where you've laid out a 310x45mm space where the tool can cut. Be sure that this space doesn't have any screws or clamps in it which will interfere with the lettering and also make sure that it's fully within the cutting area. Bring the tool down to the surface of the material (either manually or by jogging) and finally click "Reset zero" to confirm that you want to set this as the tool origin.

![](/_images/_longmill/_assembly/_starterprojects/lm_starterp_p1.png "Tool (yellow) in the bottom left-hand corner (visualized using CAMotics)"){.aligncenter .size-medium}

<a href="https://resources.sienci.com/wp-content/uploads/2021/05/LongMill-line1.zip">LongMill-line.zip</a>

Download the file above, 'unzip' or 'extract' it, then load it into gSender by clicking the "Load File" button. Once loaded, you'll be able to see a visualization of the tools movements. If you're satisfied, turn on your router (note this file doesn't currently contain spindle control commands) then run the file!

<h2>CNSheep</h2>

This is the other one of our first projects, a sheep cut into foam that we call the CNSheep. The code was designed for cutting out of foam with a 2-flute, 1/8" end mill but it should also work on soft woods as well. If you don't have these tools or materials on hand, the .zip file also contains the 3D model of the sheep so that you can run it through your desired CAM software to set it up for another material or tool. <a href="https://resources.sienci.com/wp-content/uploads/2021/05/CNSheep-files3-1.zip">CNSheep-files.zip</a> When you're setting up to cut, follow the same setup procedure as outlined in the first project above except that the pre-built g-code starts in the <strong>middle</strong> instead of the front corner, so reset the zero point in the center. Any workholding method should be sufficient, you can reference these on the 'Workholding' page in 'The Basics' section of the resources. The sheep's dimensions are 100mm wide by 70mm tall and will cut 6mm deep.

![](/_images/_longmill/_assembly/_starterprojects/lm_starterp_p2.jpg
"If all goes well, your final product should end up looking something like this!"){.aligncenter .size-medium}

<h2>The Final Steps towards starting with CNC</h2>

Now that you've got your machine running successfully, we've got a lot more information for you the check out that's easily accessible on the left navigation bar:

<table class="wp-table" style="width: 90%; margin-left: auto; margin-right: auto; border: 1px solid black; text-align: left; border-collapse: collapse; line-height: 1.2em; background: white; word-break: initial;">
<tbody>
<tr>
<td><strong>Page</strong></td>
<td><strong>Information you'll find </strong></td>
</tr>
<tr>
<td><a href="https://resources.sienci.com/view/lm-troubleshooting/"><strong>Common Issues and Fixes</strong></a></td>
<td>If you noticed an issue with your LongMill while table mounting it or during a starter project, check out this page to help point out some easy things you can check in case something went wrong during assembly.</td>
</tr>
<tr>
<td><a href="https://resources.sienci.com/view/assembling-add-ons/"><strong>Assembling Add-ons</strong></a></td>
<td>If you ordered any add-ons alongside your LongMill, the instructions to assemble them are written here.</td>
</tr>
<tr>
<td><strong><a href="https://resources.sienci.com/view/lm-surfacing-the-wasteboard/">Wasteboard Surfacing</a> </strong></td>
<td>Learn how to prepare a flat surface for cutting projects more reliably.</td>
</tr>
<tr>
<td><a href="https://resources.sienci.com/view/lm-more-projects/"><strong>More Projects </strong></a></td>
<td>Try out some more starter projects or find inspiration for what to make next with your CNC by checking out our ideas list or seeing where to find projects online.</td>
</tr>
<tr>
<td><a href="https://resources.sienci.com/view/lm-maintenance/"><strong>CNC Maintenance</strong></a></td>
<td>Understand how to best maintain your LongMill so it can continue to carve reliably for whatever you use it for.</td>
</tr>
<tr>
<td><strong>'<a href="https://resources.sienci.com/view/lm-the-basics/">The Basics</a>'</strong> and <strong>'<a href="https://resources.sienci.com/view/lm-software/">Software</a>'</strong> sections</td>
<td>There are some of you who may have just completed assembling your LongMill but have yet to familiarize yourself with how your CNC operates or what software you'd like to use to run it, if that's the case we highly recommend going back to these previous sections where we cover everything from cutting tool terminology to even a <a href="https://resources.sienci.com/view/lm-choosing-software/#toolchain-wizard"><strong>Toolchain Wizard</strong> </a>we created which helps to you decide what software options are right for you.</td>
</tr>
<tr>
<td><a href="https://resources.sienci.com/view/lm-advanced/"><strong>Advanced</strong></a> section</td>
<td>If you start to feel really comfortable with your LongMill and want to start changing it to better suit your own needs, we've got even more information on changes and modifications here.</td>
</tr>
</tbody>
</table>

<h2>Our Youtube channel</h2>

Did you know we have a <strong><a href="https://www.youtube.com/channel/UCS4SdQ0sqFhvjitLjh4EsGQ?">Youtube channel</a></strong> where you can find videos and tutorials on using your LongMill? We cover things like:

<ul>
<li>How to go from idea to completed project</li>
<li>V-carving signs</li>
<li>Carving 3D hills and terrain</li>
<li>Live Webinars and Q&amp;A sessions</li>
<li>and more!</li>
</ul>

https://www.youtube.com/embed/Q-sfK-QxwzQ

We really hope you enjoy using your LongMill Benchtop CNC in the days, weeks, and months to come. Remember that CNC routers are an amazing tool that you can use for whatever you like, and the point of the LongMill and it's community is to offer you resources and support so that you can be confident in using your CNC to make what you imagine. Good luck and happy making!

-The Sienci Labs team
