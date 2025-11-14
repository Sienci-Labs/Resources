---
title: ytsb Using Offsets in gSender
menu_order: 3
post_status: draft
post_excerpt: 
post_date: 2021-12-23 12:56:20
taxonomy:
    knowledgebase_cat: lb-software
    knowledgebase_tag:
        - laser
custom_fields:
    KBName: LaserBeam
    basepress_post_icon: bp-caret-right
skip_file: yes
featured_image: 
---

<h1><b>What are Offsets? 🎯</b></h1>
Offsets are the adjustments of a CNC machine's coordinates to account for the different dimensions and positions of any tools you may be using. In the case of the LongMill, users may seek to use the LaserBeam add-on right after completing an ordinary milling job. To ensure proper alignment of the LaserBeam to the workpiece, without having to go through a tedious manual setup, offsets can be utilized, allowing for a seamless transition from router/spindle to laser use. For such purposes, gSender has been equipped with an offset function. To utilize it, users simply enter a set of x and y coordinates, then follow a straightforward process to achieve their desired alignment results. It is a much quicker process than manually realigning the LaserBeam to the workpiece in order to set a new origin point. This resource page explains the entire process in detail.

The most accurate method for finding your offset coordinates involves using our <a href="https://resources.sienci.com/view/lmk2-open-source/">open-source CAD models</a> to measure the distance between the LaserBeam and router/spindle center points, in both the x and y dimensions. The coordinates can also be found through a simple process of trial and error. Both methods for finding these values are outlined in detail below on this page.

This resource page provides all the necessary offset coordinates one would need to utilize the gSender feature for their own projects. Below are tables containing all the <i>theoretical</i> coordinates that would work to realign the LaserBeam with the use of the offset feature. Notice, however, the use of the word <b><i>“theoretical"</i></b>. Unfortunately, due to manufacturing processes, there will be variations in the dimensions of different LongMill parts our users own. While these imperfections may be small, they can compound. Coordinates given in the provided table <b><i>may not work</i></b><b> for your specific setup</b>, <b><i>may work perfectly</i></b>, or <b><i>may have very minimal levels of error</i></b>.  Due to this, an additional guide containing the steps on how to manually determine your specific offset coordinates, without the use of CAD software, is available on this page.

&nbsp;
<h2><b>Different Mount Types for Offsetting 🔧</b></h2>
The first thing you want to do is identify the specific laser and router mount models that you own. Router mounts vary according to your LongMill model.

&nbsp;
<ul>
  <li>Models <b>MK1V1 - V4 (Mark 1 version 1 to 4)</b> router mounts possess holes for mounting on their side </li>
  <li>Models <b>MK1V4B - MK2 (Mark 1 Version 4B to Mark 2)</b>  possess mounting holes on their front face:</li>
</ul>
[gallery columns="2" link="none" size="medium" ids="6221,6222"]

Both router mount types come in different sizes. This variation in dimensions affects offset values, thus it is important to identify the specific router mount that your LongMill currently uses.
<ul>
  <li><b>MK1V1-V4</b> router mounts come in four different sizes: 52mm, 65mm,71mm, and 80mm.  </li>
  <li><b>MK1V4B - MK2</b> router mounts come in three different sizes: 65mm, 71mm, and 80mm. </li>
</ul>
For both router mount types, the associated dimension can be located on the front face:

[caption id="attachment_6286" align="aligncenter" width="850"]<img class="wp-image-6286 size-medium" src="https://resources.sienci.com/wp-content/uploads/2024/02/R16-850x464.png" alt="" width="850" height="464" /> Router Size Labelling[/caption]

Offset values will also be affected by the specific mount used to attach your LaserBeam add-on. There are two options for LaserBeam mounting, those being the LaserBeam Vortex Riser Mount shown at the beginning of this page, and the standard mount that comes with a purchase of the LaserBeam attachment, which is shown below:

[caption id="attachment_6228" align="aligncenter" width="292"]<img class="non wp-image-6228 " src="https://resources.sienci.com/wp-content/uploads/2024/02/Picture7.jpg" alt="" width="292" height="385" /> Standard Mount[/caption]

<h2><b>LaserBeam Vortex Riser Mounting Variations 🌀</b></h2>
Things vary a bit when examining the Vortex Mount. Offset values will change depending on how you choose to attach the Vortex to the router mount. The following figures show different ways in which to attach the Vortex in correspondence to the router mount types <b>(MK1V1-V4 and MK1V4B - MK2)</b>. Each attachment setup has been given a name to make them easier for you to reference later:

&nbsp;

<em><strong>MK1V1-V4: </strong></em>

&nbsp;

[caption id="attachment_6270" align="aligncenter" width="782"]<img class="wp-image-6270 size-full" src="https://resources.sienci.com/wp-content/uploads/2024/02/Screenshot-2024-02-01-155958.jpg" alt="" width="782" height="586" /> Orientation A[/caption]

&nbsp;

[caption id="attachment_6267" align="aligncenter" width="850"]<img class="wp-image-6267 size-medium" src="https://resources.sienci.com/wp-content/uploads/2024/02/Screenshot-2024-02-01-155634-850x578.jpg" alt="" width="850" height="578" /> Orientation B[/caption]

<b> </b>

<em><strong>MK1V4B- MK2:</strong></em>

&nbsp;

[caption id="attachment_6272" align="aligncenter" width="850"]<img class="size-medium wp-image-6272" src="https://resources.sienci.com/wp-content/uploads/2024/02/Screenshot-2024-02-01-164405-850x561.jpg" alt="" width="850" height="561" /> Orientation C[/caption]

&nbsp;

<b><i>*Note:</i></b> Orientations A and B could both be utilized in an inverse manner by simply flipping the bracket. You would have to note the direction of each coordinate (is it negative or positive in reference to the position I want to achieve?), but the actual values do not change. More on determining coordinate directions is discussed further below.

With a base understanding of the different components that play a role in determining these values, we can now discuss how to actually utilize offsets in your project. To do this, there are two main methods that we will review:

<ul>
  <li>Offset Tables</li>
  <li>Trial and Error Offsetting</li>
</ul>
&nbsp;
<h1><b>Offset Tables 📑</b></h1>
The following tables contain the offset values in correspondence to mount type, model, and orientation. This method involves using the values from these tables, so refer back to this section when actually attempting to follow the upcoming process:

&nbsp;

<strong>Standard Laser Mount W/ MK1 V1-V4</strong>
<table>
<tbody>
<tr>
<td>Router Mount Size</td>
<td>X-coordinate</td>
<td>Y-Coordinate</td>
</tr>
<tr>
<td>52 mm, 65 mm, 71 mm</td>
<td>68.829 mm</td>
<td>9.4 mm</td>
</tr>
<tr>
<td>80 mm </td>
<td>73.829 mm </td>
<td>9.4 mm </td>
</tr>
</tbody>
</table>
&nbsp;

<strong>Standard Laser Mount W/ MK1 V4B-MK2</strong>
<table>
<tbody>
<tr>
<td>Router Mount Size</td>
<td>X-coordinate</td>
<td>Y-Coordinate</td>
</tr>
<tr>
<td>65mm</td>
<td>No Offset Needed</td>
<td>66.42mm</td>
</tr>
<tr>
<td>71mm</td>
<td>No Offset Needed</td>
<td>69.98 mm</td>
</tr>
<tr>
<td>80mm</td>
<td>No Offset Needed</td>
<td>72.65 mm</td>
</tr>
</tbody>
</table>
&nbsp;

<strong>Vortex Laser Mount W/ MK1 V1-V4</strong>
<table>
<tbody>
<tr>
<td>Orientation</td>
<td>Router Mount</td>
<td>X-coordinate</td>
<td>Y-Coordinate</td>
</tr>
<tr>
<td>B1</td>
<td>52 mm, 65 mm, 71 mm</td>
<td>72.26 mm</td>
<td>60.1 mm</td>
</tr>
<tr>
<td>B1</td>
<td>80 mm </td>
<td>77.26mm </td>
<td>60.1 mm</td>
</tr>
</tbody>
</table>
&nbsp;

<strong>Vortex Laser Mount W/ MK1 V4B-V2</strong>
<table>
<tbody>
<tr>
<td>Orientation</td>
<td>Router Mount</td>
<td>X-coordinate</td>
<td>Y-Coordinate</td>
</tr>
<tr>
<td>A1</td>
<td>65mm</td>
<td>No Offset Needed</td>
<td>69.85 mm</td>
</tr>
<tr>
<td>A1</td>
<td>71mm</td>
<td>No Offset Needed</td>
<td>73.41 mm</td>
</tr>
<tr>
<td>A1</td>
<td>80mm</td>
<td>No Offset Needed</td>
<td>76.08mm</td>
</tr>
<tr>
<td>A2</td>
<td>65mm</td>
<td>69.50623998mm</td>
<td>69.85 mm</td>
</tr>
<tr>
<td>A2</td>
<td>71mm</td>
<td>69.50623998 mm</td>
<td>73.41 mm</td>
</tr>
<tr>
<td>A2</td>
<td>80 mm </td>
<td>69.50623998 mm </td>
<td>76.08 mm</td>
</tr>
</tbody>
</table>
&nbsp;
<h2><b>Offset Process 📝</b></h2>
<ul>
  <li>Before even beginning your initial milling job, set the origin for your workpiece using your router/spindle. After doing this, on the gSender application, <b>hit the settings button</b> (is a gear) on the top far right. Click on the <b>Spindle/Laser section</b>, and on the right, you should be able to locate the <b><i>“Laser Axes Offset”</i></b> tabs. There will be two tabs, one for the x-coordinate and one for the y-coordinate of the given offset:</li>
</ul>
<img class="aligncenter wp-image-6276 size-full" src="https://resources.sienci.com/wp-content/uploads/2024/02/Picture1-1.jpg" alt="" width="772" height="420" />

&nbsp;
<ul>
  <li>Refer to the <a href="https://docs.google.com/document/d/1AK6WDXGKIaXLF9BnPrC9DGTp7ixYU0RZ8C9DoWu9Jnk/edit#heading=h.6fm31wtsking">offset tables</a>, taking note of your specific mount types, and if applicable, mounting orientation. From here, grab your needed x and y coordinates from the relevant table, and input them into the <b><i>“Laser Axes Offset”</i></b> tabs. <b><i>Note:</i></b><i> Remember, all table dimensions are in millimeters.</i></li>
</ul>
<img class="wp-image-6289 size-full aligncenter" src="https://resources.sienci.com/wp-content/uploads/2024/02/Picture2.jpg" alt="" width="537" height="419" />
<ul>
  <li>Ensure to press enter on your keyboard after inputting the values so they save. If you do this correctly, a bar with the phrase <b><i>“ Settings Updated”</i></b> will appear at the bottom left of your screen to indicate this:</li>
</ul>
<img class="aligncenter wp-image-6290 size-medium" src="https://resources.sienci.com/wp-content/uploads/2024/02/Picture3-4-850x512.jpg" alt="" width="850" height="512" />

<b><i>*Note:</i></b> Depending on your setup, specific coordinate values may be negative or positive. You’ll have to determine which directions would logically allow for proper alignment and input them accordingly. This can be a bit confusing at first, so if you are unsure about how to do this, refer to the section below, titled <i>“</i><a href="https://docs.google.com/document/d/1AK6WDXGKIaXLF9BnPrC9DGTp7ixYU0RZ8C9DoWu9Jnk/edit#heading=h.7o7ihqt8ktt2"><i>Understanding Directions</i></a><i>”</i> .This is very important to ensure you complete the process properly. 
<ul>
  <li>Exit the settings and return to the gSender visualizer. Now, adjust the z-position of your router/spindle. This adjustment will depend on the orientation of your router/spindle to your laser, and may require you to move up or down in the z-direction. However, ensure that you raise the router/spindle high enough away from your workpiece to avoid unwanted scraping or cutting of the project when the offsets are applied, and the router/spindle begins to be moved. Also ensure it is high enough to avoid crashing your LaserBeam as well as mount. You may also want to adjust the height with your LaserBeam focus finder for optimal use:</li>
</ul>
<img class="aligncenter wp-image-6291 size-full" src="https://resources.sienci.com/wp-content/uploads/2024/02/Picture4-2.jpg" alt="" width="826" height="483" />
<ul>
  <li>After adjusting the spindle on the z-axis, you now want to hit the <i>“</i><b><i>Zero all button”</i></b>once more to set your origin:</li>
</ul>
<img class="aligncenter wp-image-6292 size-full" src="https://resources.sienci.com/wp-content/uploads/2024/02/Picture5-2.jpg" alt="" width="703" height="352" />
<ul>
  <li>Now you want to return to the settings tab. Click on the Spindle/Laser section, and under the <b><i>“Toggle”</i></b> tab, enable <b><i>“Spindle/Laser”</i></b>:</li>
</ul>
<img class="aligncenter wp-image-6294" src="https://resources.sienci.com/wp-content/uploads/2024/02/Picture6-1.jpg" alt="" width="400" height="278" />

&nbsp;
<ul>
  <li>Now proceed to switch from spindle mode into laser mode: </li>
</ul>
<img class="wp-image-6296 aligncenter" src="https://resources.sienci.com/wp-content/uploads/2024/02/Picture7-1.jpg" alt="" width="437" height="248" />
<ul>
  <li>You will now note that your x-coordinate and y-coordinate will display as your inputted offset values, and your visualizer will show the laser offset to this position. Make sure that this is the case:</li>
</ul>
<img class="aligncenter wp-image-6297" src="https://resources.sienci.com/wp-content/uploads/2024/02/Picture8.jpg" alt="" width="479" height="281" />
<ul>
  <li>At this point, we now want to hit the <b><i>“Go to zero”</i></b> button. This will move your LaserBeam and nearly perfectly align it with your workpiece’s set origin point, in turn completing the process. </li>
</ul>
<img class="aligncenter wp-image-6299" src="https://resources.sienci.com/wp-content/uploads/2024/02/Picture9-1.jpg" alt="" width="385" height="247" />
<ul>
  <li>On the Visualizer, your laser will now appear at the origin point, and your coordinates will now all be zero:</li>
</ul>
<img class="aligncenter wp-image-6300" src="https://resources.sienci.com/wp-content/uploads/2024/02/Picture10-1.jpg" alt="" width="491" height="295" />
<ul>
  <li>Assuming you want to return to router/spindle use, switch back into spindle mode:</li>
</ul>
<img class="aligncenter wp-image-6301" src="https://resources.sienci.com/wp-content/uploads/2024/02/Picture11-1.jpg" alt="" width="461" height="116" />
<ul>
  <li>Your router/spindle will now appear offset, and the coordinates will have the same value as the offsets entered, but in the opposite direction:</li>
</ul>
<img class="aligncenter wp-image-6302" src="https://resources.sienci.com/wp-content/uploads/2024/02/Picture12-1-850x503.jpg" alt="" width="519" height="307" />
<ul>
  <li>Once again, hit the <b><i>“Go to zero”</i></b> button. </li>
</ul>
<img class="aligncenter wp-image-6303" src="https://resources.sienci.com/wp-content/uploads/2024/02/Picture13-1.jpg" alt="" width="581" height="261" />
<ul>
  <li>Your spindle will now be nearly perfectly aligned with the original origin point. It once again will also display as such on your visualizer.</li>
</ul>
<img class="aligncenter wp-image-6305 size-medium" src="https://resources.sienci.com/wp-content/uploads/2024/02/Picture15-850x433.jpg" alt="" width="850" height="433" />
<ul>
  <li>At this point, you can continuously swap between laser and router/spindle use by switching between modes and hitting the <b><i>“Go to zero button”</i></b><b>.</b> As noted before, there is a chance that these specific coordinate values may not work for your given setup. If this turns out to be the case and your alignment is visibly off, refer to the section titled <i>“</i><a href="https://docs.google.com/document/d/1AK6WDXGKIaXLF9BnPrC9DGTp7ixYU0RZ8C9DoWu9Jnk/edit#heading=h.jieequclcx1p"><i>Trial and Error Offsetting</i></a><i>”</i>. </li>
</ul>
<h2><b>Understanding Directions ➡️</b></h2>
It is important to figure out the proper direction of your offset values before entering them into gSender. This can be a bit confusing at first. Take your time reading and examining the photos and this process will become easier.
<ul>
  <li>Ensure that you have already set the origin point for your workpiece using your router/spindle, or at least know where you intend to set your origin point. After this is done, look at the orientation of your origin point and laser in comparison to your gSender jog controller. </li>
</ul>
&nbsp;
<ul>
  <li>Take note of which way your LongMill would logically have to move for your laser beam to align with your set origin. Remember, the whole purpose of utilizing offsets is to move your <b><i>LaserBeam’s center</i> to the <i>set origin of your work piece</i>, which is the location of the <i>router/spindle’s centerpoint.</i></b>  Let’s look at an example with a router mount of <b>orientation <i>A</i></b> . We only need a y-offset for this orientation, but we must take note of what sign the coordinate should have:</li>
</ul>
<img class="aligncenter wp-image-6308 size-full" src="https://resources.sienci.com/wp-content/uploads/2024/02/Picture16.jpg" alt="" width="620" height="600" />
<ul>
  <li>In the photo above, we see that the router/spindle is directly above the green tape, at the point in which we have set the origin, <b><i>but the laser needs to be moved in the +Y direction to be centered. </i></b></li>
</ul>
&nbsp;
<ul>
  <li>Thus, you might think of entering your offset value as a positive number. <b><i>However, this isn’t correct</i></b><i>.</i> You would actually want your offset value to be <b><i>negative</i></b>. To illustrate this, let’s look at how the visualizer would display the router/spindle and laser during this process. Before you do anything, assuming you have already set your workpiece origin, your router/spindle will be displayed on the origin point of the visualizer as shown below: </li>
</ul>
&nbsp;

<img class="aligncenter wp-image-6309 size-medium" src="https://resources.sienci.com/wp-content/uploads/2024/02/Picture17-850x457.jpg" alt="" width="850" height="457" />

&nbsp;
<ul>
  <li>Now, after we enter our offset values, if we switch over to laser mode, we can expect the visualizer to display the beam offset from the origin by the coordinate values inputted, again, as shown below. When we hit <b><i>“Go to Zero”</i>, <i>it will align with the origin by moving in the +y direction</i>, which is what we want:</b></li>
</ul>
<img class="aligncenter wp-image-6311 size-medium" src="https://resources.sienci.com/wp-content/uploads/2024/02/Picture19-850x495.jpg" alt="" width="850" height="495" />

&nbsp;

<img class="aligncenter wp-image-6312 size-medium" src="https://resources.sienci.com/wp-content/uploads/2024/02/Picture20-850x459.jpg" alt="" width="850" height="459" />

&nbsp;
<ul>
  <li>The reason we used a negative y-coordinate is because, as seen above, by inputting the offset, the software believes that the Laser beam is 66.16 mm away from the origin point in the -y direction, <b><i>and will thus move it 66.16 mm in the +y direction to align the laser to the origin point. </i></b></li>
</ul>
&nbsp;
<ul>
  <li>To simplify this, when you determine which direction your laser will have to be moved in for alignment, in this case, the +y direction, <b>t</b><b><i>he offset coordinates will have to have the opposite sign of the direction in which you intend to move</i></b><b>.</b> Now we can put this together and go through an example involving both the x and y coordinates.</li>
</ul>
&nbsp;
<ul>
  <li>This time we are working with <b>orientation <i>B</i></b>. Once again, let’s start by mapping out how our physical setup corresponds to our jog controller. Set the origin point for your workpiece using your router/spindle. Based on your setup, see which direction in which the laser will have to be moved to reach the router/spindle’s current position. Match that to the jog control coordinate system.</li>
</ul>
<img class="aligncenter wp-image-6313 size-full" src="https://resources.sienci.com/wp-content/uploads/2024/02/Picture23.jpg" alt="" width="616" height="605" />
<ul>
  <li>Based on our setup, we would want our machine to move the laser in the +y and -x direction for proper alignment.</li>
</ul>
&nbsp;
<ul>
  <li>With this now in mind, based on our rules established above, to achieve this result, we should make our x coordinate positive and our y coordinate negative. </li>
</ul>
&nbsp;
<ul>
  <li>Once again, at this point, our router/spindle is displayed at the origin on the visualizer:</li>
</ul>
<img class="size-medium wp-image-6314 aligncenter" src="https://resources.sienci.com/wp-content/uploads/2024/02/Picture24-850x460.jpg" alt="" width="850" height="460" />
<ul>
  <li>We now switch into laser mode and see our offset has taken effect. Our x has been offset in the positive direction and our y has been offset in the negative direction.  Thus, <b><i>our laser will be moved in the -x direction and +y direction</i></b>, which again, is what we want.</li>
</ul>
<img class="alignnone size-full wp-image-6315" src="https://resources.sienci.com/wp-content/uploads/2024/02/Picture25.jpg" alt="" width="805" height="542" />
<h1></h1>
<ul>
  <li>It is now properly aligned with the origin </li>
</ul>
<img class="aligncenter wp-image-6316 size-full" src="https://resources.sienci.com/wp-content/uploads/2024/02/Picture26.jpg" alt="" width="847" height="442" />
<ul>
  <li>When you return to spindle mode, it is <i>key</i> to note what direction in which your router/spindle will have to move to return to the origin. This is relatively simple, as it will move in the exact opposite direction in which your laser was moved during the offsetting process. In the case of our above example using orientation B, <b><i>our router/spindle would move in the +x direction and -y direction to return to zero. You can also remember this by noting it will move in the opposite direction of the newly displayed coordinates in the location tab:</i></b></li>
</ul>
<img class="aligncenter wp-image-6317 size-full" src="https://resources.sienci.com/wp-content/uploads/2024/02/Picture27.jpg" alt="" width="511" height="456" />
<h1><b>Trial and Error Offsetting ❎</b></h1>
In scenarios in which the offset table values are not compatible with your specific setup, you can simply use a method of trial and error to achieve similar results.

&nbsp;
<ul>
  <li>Begin by marking an indent into a scrap piece of material with your router/spindle. After making this indent, adjust your z-position and raise your spindle until it is a reasonable distance away from your scrap piece of material. <b><i>Do not tamper with the x and y coordinates while doing this.</i></b> After you have raised the spindle to a reasonable height, hit the <b><i>“Zero all”</i></b> button. You have now set this specific indent point as your origin. This is important for later on:</li>
</ul>
&nbsp;

[caption id="attachment_6319" align="aligncenter" width="469"]<img class="wp-image-6319 size-full" src="https://resources.sienci.com/wp-content/uploads/2024/02/Picture28.jpg" alt="" width="469" height="372" /> <strong>Initial Indent</strong>[/caption]

&nbsp;
<ul>
  <li>Proceed to move into laser mode. At this point, you want to manually move your LongMill with the jog control to align the LaserBeam’s centerpoint with that of the indent’s. As you move around, occasionally fire the laser at low power to see exactly where the centerpoint lies. You’ll want to focus the beam to a similar size as that of the indent. Continue firing and adjusting the LaserBeam’s position until it eventually aligns with the indent:</li>
</ul>
&nbsp;

[caption id="attachment_6320" align="aligncenter" width="350"]<img class="wp-image-6320" src="https://resources.sienci.com/wp-content/uploads/2024/02/Picture29.jpg" alt="" width="350" height="387" /> <strong>Alignment Attempts</strong>[/caption]

&nbsp;
<ul>
  <li>After you have done this look at the location tab and take note of the coordinates displayed. These coordinates will now act as your offset values, as they are the distance in which the LaserBeam must be moved to align it with the origin point. </li>
</ul>
<img class="aligncenter wp-image-6321" src="https://resources.sienci.com/wp-content/uploads/2024/02/Picture30.jpg" alt="" width="498" height="304" />
<ul>
  <li>Now, with these values, you can follow the exact process outlined in the <a href="https://docs.google.com/document/d/1AK6WDXGKIaXLF9BnPrC9DGTp7ixYU0RZ8C9DoWu9Jnk/edit#heading=h.6fm31wtsking"><i>“Offset Tables”</i></a> section. Begin by returning to spindle mode. Then hit <b><i>“Go to zero”</i></b> to return to the origin point.</li>
</ul>
<img class="aligncenter wp-image-6353" src="https://resources.sienci.com/wp-content/uploads/2024/02/Picture31-1.jpg" alt="" width="546" height="364" />
<ul>
  <li>Open the settings and go to the Spindle/Laser section to enter the offset values you acquired through the trial and error firing process. Remember to ensure you apply the right directions to each coordinate. Save these values, and return to the visualizer. After this, enter into laser mode and hit the <b><i>“Go to zero”</i></b> button for proper alignment. </li>
</ul>
&nbsp;

The actual process of using the offset coordinates is the exact same between the two methods discussed on this page. The only difference is in how one acquires those values.

In conclusion, all the information given above tells you all there is to know about offsets, including how to use them and why you should utilize them to take your projects and efficiency to the next level.  

&nbsp;
<h1><b>Bonus Section** 🌟</b></h1>
<h2><b>Finding Offsets</b> <b>📏</b></h2>
Utilized offset values are nothing more than the distance between your router/spindle’s centerpoint, and the centerpoint of your LaserBeam. For those interested in how the offset tables provided on this page were compiled, this section details the entire process.  To find these coordinates, CAD software was utilized. Open source CAD models of each of Sienci's products are available on  the company resource page:  

&nbsp;

<b>Standard Mount</b>
<ul>
  <li><strong>A)</strong> When used in combination with model <b>MK1V4B-MKV2</b> router mounts, the only direction in which there would be any offset is the y-direction. This is because the standard mount was designed for alignment between the center of the router/spindle and the LaserBeam. </li>
</ul>
&nbsp;

<b><i>*Note:</i></b> All dimensions shown in the following photos are in millimeters

&nbsp;
<ul>
  <li> We start by examining our assembly from the top view. We draw a line from the center of the router mount model, all the way to its front edge. The center of the router mount model will align with the center of the router/spindle, and thus gives an accurate center position:</li>
</ul>
&nbsp;

<img class="aligncenter wp-image-6354" src="https://resources.sienci.com/wp-content/uploads/2024/02/Picture34.jpg" alt="" width="291" height="276" />

&nbsp;
<ul>
  <li>Next we want to draw a line the length of the standard mount’s thickness. The standard mount and Vortex Riser mount both have a thickness of 0.135 inches. Thus we add a line that is 0.135 inches / 3.429 mm long:</li>
</ul>
&nbsp;

<img class="aligncenter wp-image-6355" src="https://resources.sienci.com/wp-content/uploads/2024/02/Picture35.jpg" alt="" width="315" height="309" />

&nbsp;
<ul>
  <li>Lastly, we add half of the LaserBeam diode’s width. The diode’s width is 40mm, hence we add a 20 mm line to reach the laser beam’s center:</li>
</ul>
&nbsp;

<img class="aligncenter wp-image-6356" src="https://resources.sienci.com/wp-content/uploads/2024/02/Picture36.jpg" alt="" width="311" height="329" />

&nbsp;
<ul>
  <li>We now measure the combined distance of the lines using the CAD software’s measurement tool. We can also simply add up all the distance values. Either method works fine:</li>
</ul>
&nbsp;

<img class="aligncenter wp-image-6357" src="https://resources.sienci.com/wp-content/uploads/2024/02/Picture37-850x418.jpg" alt="" width="572" height="281" />

&nbsp;
<ul>
  <li>Thus, our offset value is 66.42055966 mm in the y-direction. We could also have come to the same conclusion by analyzing the mount drawings available on the company resource page: <a href="https://sienci.com/product/router-mount-for-longmill-benchtop-cnc/">https://sienci.com/product/router-mount-for-longmill-benchtop-cnc/</a></li>
</ul>
<b></b>
<b></b>
<ul>
  <li> In the engineering drawing for the 65mm router mount, the distance from the mount's center to its front edge is given. It matches our CAD dimensions exactly:</li>
</ul>
<img class="aligncenter wp-image-6358 size-medium" src="https://resources.sienci.com/wp-content/uploads/2024/02/Picture38-850x363.jpg" alt="" width="850" height="363" />

&nbsp;
<ul>
  <li>With this information, one simply has to add the standard mount’s thickness, and half the width of the LaserBeam diode to get their offset value. Hence we would have <b>42.99+3.4163+20 =66.419</b>. While not as accurate as the CAD model, due to the rounding of dimensions for the purpose of manufacturing, this method still works just as well. The difference in accuracy is negligible. </li>
</ul>
&nbsp;

To summarize, the required offset value for the standard mount when used in conjunction with the <b>MK1V4B-MKV2</b> is given by: <b><i>(The distance between the mount’s center and front edge)</i> + <i>(the thickness of the standard mount plate)</i> +  (1/2  width of the LaserBeam diode)</b>

&nbsp;

This same formula was used to determine the offset value for the 71mm and 80mm mounts as well

&nbsp;
<ul>
  <li><strong>B)</strong> When used in combination with model <b>MK1V1-MK1V4</b> router mounts, there is an offset in the y and x direction. We apply similar principles to find the needed values.</li>
</ul>
&nbsp;

For this example, the 65 mm mount was used

&nbsp;

<b><i>*Note:</i></b> for the <b>MK1V1-MK1V4 models</b>, the offsets are the exact same for the 52mm, 65mm, and 71mm router mounts. Due to how they were designed and manufactured, the offsets remain proportional as the only difference between said three models is the diameter of the router insert hole :

&nbsp;
<ul>
  <li> Firstly, to determine the x-offset, we use the exact same method as we did for the y-offset in part a, but in the x-direction. This is due to the mounting holes being located on the router mount’s side face. We start by drawing line from the mount’s center to its side edge:</li>
</ul>
&nbsp;

<img class="aligncenter wp-image-6359" src="https://resources.sienci.com/wp-content/uploads/2024/02/Picture40.jpg" alt="" width="385" height="298" />

&nbsp;
<ul>
  <li> We then add the width/thickness of the standard mount plate:</li>
</ul>
&nbsp;

<img class="aligncenter wp-image-6360" src="https://resources.sienci.com/wp-content/uploads/2024/02/Picture41.jpg" alt="" width="442" height="332" />

&nbsp;
<ul>
  <li>We then add half the width of the LaserBeam diode:</li>
</ul>
&nbsp;

<img class="aligncenter wp-image-6361" src="https://resources.sienci.com/wp-content/uploads/2024/02/Picture42.jpg" alt="" width="450" height="346" />

&nbsp;
<ul>
  <li> Using our measuring tool, we find that this total distance comes out to 68.8163 mm. Thus this is our x-offset value:</li>
</ul>
&nbsp;

<img class="aligncenter wp-image-6362 size-medium" src="https://resources.sienci.com/wp-content/uploads/2024/02/Picture43-850x519.jpg" alt="" width="850" height="519" />

&nbsp;
<ul>
  <li> To find our y-offset, we extend a line down from our intersection with the side  edge</li>
</ul>
<img class="aligncenter wp-image-6363" src="https://resources.sienci.com/wp-content/uploads/2024/02/Picture44.jpg" alt="" width="454" height="290" />

&nbsp;
<ul>
  <li>From here, we draw a line to find the distance between the two side mounting holes:</li>
</ul>

<img class="aligncenter wp-image-6364" src="https://resources.sienci.com/wp-content/uploads/2024/02/Picture45.jpg" alt="" width="195" height="345" />

&nbsp;
<ul>
  <li>From here we mark the centerpoint of the line that represents the distance between the mounting holes. We do this because the LaserBeam’s centerpoint would be located here when mounted:</li>
</ul>
&nbsp;

<img class="aligncenter wp-image-6366" src="https://resources.sienci.com/wp-content/uploads/2024/02/Picture47.jpg" alt="" width="216" height="325" />

&nbsp;
<ul>
  <li> Now we measure the distance between the mounting hole line and the router/spindle’s centerpoint. This measurement comes out to 9.4mm, and thus 9.4 mm is our y-offset value:</li>
</ul>
&nbsp;

<img class="aligncenter wp-image-6368" src="https://resources.sienci.com/wp-content/uploads/2024/02/Picture49.jpg" alt="" width="523" height="376" />

&nbsp;
<ul>
  <li>  We also could have simply just taken the x-measurement with our initial setup by drawing a line to the LaserBeam’s centerpoint. We see that we get the exact same result:</li>
</ul>
&nbsp;

<b><img class="aligncenter wp-image-6369" src="https://resources.sienci.com/wp-content/uploads/2024/02/Picture50.jpg" alt="" width="400" height="351" /></b>
<b></b>
<ul>
  <li>To summarize, the x-offset is given by: <b><i>(The distance between the mount’s center and front edge)</i> + <i>(the thickness of the standard mount plate)</i> +  (1/2  width of the laser diode)</b>, while the y-offset is given by the distance from the router/spindle’s center, to the center of the distance between the two side mounting holes</li>
</ul>
&nbsp;
<h2><b>LaserBeam Vortex Riser Mount</b></h2>
&nbsp;
<ul>
  <li><strong>A)</strong> The offsets change depending on the orientation used, but the process is more or less the same. Let’s examine how the offsets were determined for orientation <i>A</i></li>
</ul>
<b></b>
<b></b>
<ul>
  <li>Similarly to the standard mount in conjunction with models <b>MK1V4B-MK1V2</b>, this orientation only requires an offset coordinate in the y-direction. We start, once again by drawing a line from the center of the mount to its front edge:</li>
</ul>
<img class="aligncenter wp-image-6370" src="https://resources.sienci.com/wp-content/uploads/2024/02/Picture51.jpg" alt="" width="331" height="307" />

&nbsp;
<ul>
  <li>The LaserBeam Vortex Riser Mount is attached to the standard laser mount, and thus consists of two plates when fully assembled, each with a thickness of 0.135 inches, which equates to 3.429  mm:</li>
</ul>
[caption id="attachment_6372" align="aligncenter" width="384"]<img class="wp-image-6372 size-full" src="https://resources.sienci.com/wp-content/uploads/2024/02/Picture52.jpg" alt="" width="384" height="436" /> LaserBeam Vortex Rise Mount Assembly[/caption]

&nbsp;

&nbsp;

Thus to account for both plates, we will add two lines that are 3.429 mm long:

<img class="aligncenter wp-image-6373" src="https://resources.sienci.com/wp-content/uploads/2024/02/Picture53.jpg" alt="" width="488" height="397" />
<ul>
  <li> We then add half of the diode width:</li>
</ul>
<img class="aligncenter wp-image-6374" src="https://resources.sienci.com/wp-content/uploads/2024/02/Picture54.jpg" alt="" width="456" height="415" />

&nbsp;
<ul>
  <li> Lastly we use our measuring tool and evaluate the total distance.We find our value is:  69.84955966 mm, meaning this is our y-offset value.</li>
</ul>
&nbsp;

<img class="aligncenter wp-image-6375 size-medium" src="https://resources.sienci.com/wp-content/uploads/2024/02/Picture55-850x426.jpg" alt="" width="850" height="426" />

&nbsp;
<ul>
  <li>Now examining orientation <i>B</i>, we now need to account for offsets in both the x and y directions. <b><i>The y-offset values will stay the exact same as those associated with orientation A.</i></b> This is because this orientation only changes the x-position of the laser, but has no effect on its y-position:</li>
</ul>
&nbsp;

<img class="aligncenter wp-image-6376" src="https://resources.sienci.com/wp-content/uploads/2024/02/Picture57.jpg" alt="" width="611" height="353" />

&nbsp;
<ul>
  <li>Once again, we start from the center of the router mount and draw a line to the edge of its front face:</li>
</ul>
<img class="aligncenter wp-image-6377" src="https://resources.sienci.com/wp-content/uploads/2024/02/Picture58.jpg" alt="" width="421" height="391" />

&nbsp;
<ul>
  <li> The midpoint between the two vortex bracket mounting holes aligns with the midpoint of the router/spindle: </li>
</ul>
<img class="aligncenter wp-image-6378 size-full" src="https://resources.sienci.com/wp-content/uploads/2024/02/Picture59.jpg" alt="" width="487" height="341" />

Thus, to find our x-offset, which is our distance between the centerpoint of the laser and the router/spindle, we need to find the length of the dotted line located in the photo below:

<img class="aligncenter wp-image-6379" src="https://resources.sienci.com/wp-content/uploads/2024/02/Picture60.jpg" alt="" width="403" height="306" />
<ul>
  <li>Evaluating the line, we find that the distance comes out to 69.50623998 mm. Thus this value is our x-offset. </li>
</ul>
<img class="aligncenter wp-image-6380" src="https://resources.sienci.com/wp-content/uploads/2024/02/Picture61.jpg" alt="" width="468" height="309" />

&nbsp;
<ol start="4">
  <li>While the same exact method can be applied to all other mount sizes, there is no need as this offset will stay consistent between all of them due to the fact that the center point of the bracket stays consistently aligned to the router/ spindle center throughout all versions. Thus to simplify, for the y-offset: <b><i>(The distance between the mount’s center and front edge)</i> + <i>(the thickness of one of the Vortex mount plates)</i> + (1/2  width of the LaserBeam diode)</b></li>
</ol>
&nbsp;

<b><i>X-Offset:</i></b> 69.50623998

&nbsp;
<ol start="5">
  <li>We also could have simply just measured the distance from the top view. Doing so gives the exact same result:</li>
</ol>
<img class="aligncenter wp-image-6381" src="https://resources.sienci.com/wp-content/uploads/2024/02/Picture62.jpg" alt="" width="569" height="379" />

<b>C)</b> Lastly, we examine the process for determining the offsets associated with orientation <i>C</i>.

&nbsp;
<ul>
  <li> Again, starting with the x-offset, the process is exactly the same as with the standard mount, but with a change in the width value we use for the plate. We first start with drawing a line from the midpoint of the router mount to the side edge: </li>
</ul>
<img class="aligncenter wp-image-6382" src="https://resources.sienci.com/wp-content/uploads/2024/02/Picture63.jpg" alt="" width="564" height="345" />

&nbsp;
<ul>
  <li> We then add the combined thickness of both vortex plates:</li>
</ul>
<img class="aligncenter wp-image-6383" src="https://resources.sienci.com/wp-content/uploads/2024/02/Picture64.jpg" alt="" width="488" height="309" />

&nbsp;
<ul>
  <li> Lastly we add the half width of our diode: </li>
</ul>
<b><img class="aligncenter wp-image-6384" src="https://resources.sienci.com/wp-content/uploads/2024/02/Picture65.jpg" alt="" width="477" height="346" /></b>
<b></b>
<ul>
  <li> Evaluating the total distance gives us an offset value of 77.258 mm for our x-offset. </li>
</ul>
<img class="aligncenter wp-image-6385" src="https://resources.sienci.com/wp-content/uploads/2024/02/Picture66.jpg" alt="" width="638" height="336" />

&nbsp;
<ul>
  <li> Now to determine the y-offset, we simply subtract 9.4 mm from 69.50623998mm. This works because the vortex bracket aligns with the mounting holes, and hence the midpoint between the mounting holes on the bracket is the exact same as the midpoint between the two mounting holes on the router mount. </li>
</ul>
<b></b>
<b></b>
<ul>
  <li>Thus all we have to do is subtract 9.4 mm from 69.50623998 mm to get our y-offset.  Hence our equation would be 69.50623998mm - 9.4mm = 60.10623998 . The photo below shows that this number turns out to be the distance between our router/spindle center and LaserBeam center. </li>
</ul>
<img class="aligncenter wp-image-6386" src="https://resources.sienci.com/wp-content/uploads/2024/02/Picture67.jpg" alt="" width="512" height="295" />

<img class="aligncenter wp-image-6387" src="https://resources.sienci.com/wp-content/uploads/2024/02/Picture68.jpg" alt="" width="462" height="507" />
