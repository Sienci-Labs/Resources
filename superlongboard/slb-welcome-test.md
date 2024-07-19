---
title: Welcome! Test
menu_order: 4
post_status: draft
post_excerpt: Documentation for the SuperLongBoard, the controller board for the LongMill Benchtop CNC router. Includes electrical and mechanical specifications.
post_date: 2024-03-03 14:43:53
taxonomy:
    knowledgebase_cat: slb-handbook
    knowledgebase_tag:
        - slb
custom_fields:
    KBName: SuperLongBoard
    basepress_post_icon: 10
skip_file: no
featured_image: _images/_superlongboard/SLB-VB6.jpg
---

Hello and welcome!

If you’ve come here you’re either interested in or have already purchased our brand new endeavour into upgrading the Hobby CNC landscape, the <a href="https://sienci.com/product/slb/"><strong>SuperLongBoard</strong></a>!!

![](/_images/_superlongboard/SLB-VB6.jpg){.aligncenter .size-medium .non}

Started in mid-2022, this project has been truly a labour of love for us. Thanks to the initial interest from the first 500 SLB purchasers, we were able to finish bringing the project to life. If you're one of those 500, a special welcome! As you go through our instructions let us know if there's any sticking points you run into and we'll be happy to get them sorted as soon as we can. The SLB may still have some quirks in its early days despite the many months of testing that we've put it through - but we're keen to make it the best it can be and trust we can all work together to make that happen :)

https://youtu.be/LkZIeJQSzdM

<h2>Diving In</h2>
Let's get rock'n'rolling by pointing you towards the right page for you 🎸

[su_table responsive="yes" fixed="yes"]
<table style="border: none !important;">
<tbody style="display: block; margin: 1% 15%;">
<tr>
<td style="text-align: center;"><a href="https://resources.sienci.com/view/slb-upgrading/"><img class="flie aligncenter" style="padding: 5% 15%;" src="https://resources.sienci.com/wp-content/uploads/2024/07/SLB-upgrade.png"/></a><b><a href="https://resources.sienci.com/view/slb-upgrading/">Upgrade</a>
</b>Guide for switching to the SLB from an existing controller.<b>
</b></td>
<td style="text-align: center;"><a href="https://resources.sienci.com/view/slb-manual/"><img class="flie aligncenter size-full" style="padding: 5% 15%;" src="/documents.png"/></a><b><a href="https://resources.sienci.com/view/slb-manual/">Board Details</a>
</b>Learn all the nitty gritty about wiring, specs, and firmware.<b>
</b></td>
</tr>
<tr>
<td style="text-align: center;"><a href="https://forum.sienci.com/c/slb/"><img class="flie aligncenter" style="padding: 5% 15%;" src="https://github.com/Sienci-Labs/Resources/tree/main/_images/_superlongboard/community.png"/></a><b><a href="https://forum.sienci.com/c/slb/">Forum</a>
</b>Share ideas for SLB features, or get help with problems.<b>
</b></td>
<td style="text-align: center;"><img class="flie aligncenter size-full" style="padding: 5% 15%;" src="https://github.com/Sienci-Labs/Resources/tree/main/_images/_superlongboard/open-source-hardware.png"/><b>Open-Source
</b>Licensing and files for replication slowly rolling out!<b>
</b></td>
</tr>
</tbody>
</table>
[/su_table]

<h2>More Questions?</h2>
In the coming months we'll continue to add more information to documentation on the SLB including more information on wiring hookups, recommended accessory compatibilities, and more technical specifications. Otherwise, we've already covered lots of <strong>Frequently Asked Questions</strong> on:
<ul>
 	<li>The <a href="https://sienci.com/product/slb/">SuperLongBoard product page</a></li>
 	<li>Recent videos on our <a href="https://www.youtube.com/@SienciLabs">YouTube channel</a></li>
 	<li>Many <a href="https://sienci.com/2023/11/08/next-big-slb-update/">blogs covering the history</a> of the development of the SLB</li>
</ul>
Eventually we'll also have a revised MK2 manual that will cover installing the SLB out-of-the gate. If you're still needing some extra support with your new SLB, you can always contact us directly at <a href="mailto:support@sienci.com">support@sienci.com</a>.

<img class="aligncenter wp-image-6558 size-medium" src="https://resources.sienci.com/wp-content/uploads/2024/03/LB2SLB_p48-850x502.jpg" alt="" width="850" height="502" />
<h2>FAQ</h2>
<b>Q: Will the SLB work with my CNC?</b>

A: If it's a LongMill or AltMill then definitely it will. Otherwise, your CNC should be supported so long as it’s a <strong>typical hobby CNC setup with open-loop Nema 23s</strong>. As we roll out the SLB we'll begin hearing back on other successful configurations and update this 'Answer' appropriately, since otherwise we can't provide a definitive guarantee other than to say that it's very likely to work for most hobby CNCs. Other machines that have been proven to work so far: <strong>Onefinity</strong>.

We’ve earnestly done our best to ensure the SLB would be ideal for any typical setup since the inspiration for the SLB came from trying to take things that are normally only available on more expensive and ‘closed’ boards and bring them into the open source domain and at a more affordable price for the benefit of as many hobbyists as we could. This means that although you will need to change certain settings to match your specific setup,the SLB will support a range of machines and accessories including 5/24V limit switches, touch plates, tool length sensors, laser diodes, external 4th axis, and more.

<b>Q: What about if I want to use higher voltage or external motor drivers?</b>

A: We do currently have another version of the SLB in the works that we're calling SLB EXT since it'll support much higher voltage and external motor drivers for closed loop support as well. This will extend even further SLB support for a broader range of machines and setups closer to production-level. This board will be what powers our AltMill CNC and you'll be able to see more updates about it on our blog as we begin making deliveries.

<b>Q: How can I know if the SLB is right for me?
</b>

A: There are many other offerings on the market that come with a wide range of features, simply put the choice between these will always come down to budget. If you don't think you need the features offered by the SLB then it'd make more sense to spend less money. In this case consider getting a more typical grbl board or some of the newer x32 hobby CNC boards that might require more DIY setup time for wiring or programming. For instance the Blackbox x32 has the benefit of a direct wireless connection but less extensability. If instead you feel like you want to pull all the stops to support a higher-end CNC or use more advanced features then you might want to increase your budget and look into a Centroid, UCCNC, or Mach setup. We believe though that we've done our best to match the SLB up with the mid-level hobby CNC community where it makes sense to spend $150-200 on a controller to really unlock all the capabilities you'd be looking to expect out of your $1000-4000 CNC.