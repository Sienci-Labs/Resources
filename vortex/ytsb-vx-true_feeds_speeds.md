---
title: ytsb Rotary Feeds & Speeds
menu_order: 0
post_status: draft
post_excerpt: 
post_date: 2024-07-18 18:14:53
taxonomy:
    knowledgebase_cat: vx-basics vx-assembly vx-projects vx-handbook
    knowledgebase_tag:
        - vortex
custom_fields:
    KBName: Vortex
    basepress_post_icon: bp-caret-right
skip_file: yes
featured_image: _images/post-image.jpg
---

Let’s explore the relationship between feed rate and machining diameter.

Essentially, since our ‘feed rate’ is given by how fast the cutting bit travels linearly through the material, we’re concerned with the surface speed of the bit against the material while it rotates. This ‘surface speed’ is defined by:

<p style="text-align: center;"><b>Rotational Speed</b> X <b>Distance of the Bit from the Rotating Axis</b><br>(<em>usually dependent on your stock diameter</em>)</p>

This relationship means that if your stock diameter is **halved**, then your feed rate for the A-axis/rotary axis should be **doubled**.

One issue that arises in doing this is that VCarve/Aspire (and many other CAM software programs) do not allow you to adjust feed rate in only one cutting direction. This means that if you’ve sped up your feed rate to be 4000 mm/min to compensate for very small diameter stock, then cutting in the X-axis will also happen at this speed, however it will likely be much too fast. The good news is that if your cutting passes are in the A-axis direction then you’ll only have small stepovers in the X-axis direction for each next pass. These stepovers may be slightly aggressive, but are generally small enough that they won’t matter.

If you’ve opted to set your cutting passes to cut sideways (in the X-direction), then you’ll likely want to leave your cutting feeds and speeds the same as usual (since the X-axis is of course unaffected by this diameter-feed rate relationship). The stepover distance in the A-axis for each pass will, however, be affected since the actual A-axis stepover distance will depend on the diameter of your stock.

[gallery columns="2" size="medium" ids="5863,5862"]

If you’d like to better understand how your stock diameter affects the effective cutting feed rate at the bit, we’ll explain this with some boring math in an example, if not, skip ahead to find a table of recommended feed rate modifications to compensate:

Using an example feed rate of 2000 mm/min, we get a rotational speed of (2000 deg/min) divided by (360 mm/rotation) to get 5.55 rpm, or 34.9 radians/min.

For 4 inch diameter stock, we can multiply this rotational speed (34.9 radians/min) by our radius (50.8 mm) to get a feed rate of 1773 mm/min. This isn’t exactly the feed rate we’re looking for, but is close enough that it won’t make much difference.

Once we move over to a 1 inch diameter stock, our true feed rate at the surface becomes (34.9 radians/min) X (12.7mm radius) = 443 mm/min feed rate, which is much too slow for what we’d typically use.

As a general rule, you can apply the following multiplier factors to your feed rate if you’d like:

<table>
<tbody>
<tr>
<td>Stock Diameter</td>
<td>Suitable feed rate multiplier</td>
<td>Example of compensated  feed rate</td>
</tr>
<tr>
<td>1”</td>
<td>4.515</td>
<td>1500 mm/min -&gt; 6770 mm/min</td>
</tr>
<tr>
<td>2”</td>
<td>2.256</td>
<td>1500 mm/min -&gt; 4000 mm/min</td>
</tr>
<tr>
<td>3”</td>
<td>1.5</td>
<td>1500 mm/min -&gt; 2250 mm/min</td>
</tr>
<tr>
<td>4”</td>
<td>1.128</td>
<td>1500 mm/min -&gt; 1690 mm/min</td>
</tr>
</tbody>
</table>

Simply take the cutting feed rate you’d planned on using, then multiply this out by the ‘feed rate multiplier’ for the closest stock diameter you’re using, this will give you the compensated feed rate you can use to achieve the desired cutting feed rate at the bit. When rotary mode is enabled within gSender, this will allow for movements on your A-axis/rotary axis that are up to 8000 mm/min, allowing reasonable feed rates when cutting small diameter stock.

Unfortunately, as mentioned above, the LongMill (and most hobby CNC machines) lacks the ability to automatically change this feed rate as the diameter of the stock being machined gets smaller. For this reason, we generally recommend setting the feed rate according to your starting stock diameter, then using the feed rate override to increase the feed rate as the stock diameter decreases throughout the job to help speed things up.
