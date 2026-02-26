---
title: ATC Final Checks
menu_order: 7
post_status: draft
post_excerpt: Now that you are setup and running, let's pick up a couple tools and try out the tls.
post_date: 2026-02-10 11:50:53
taxonomy:
    knowledgebase_cat: atc-assembly
    knowledgebase_tag: 
custom_fields:
    KBName: AutoToolChanger
    basepress_post_icon: bp-caret-right
skip_file: no
featured_image: _images/post-image.jpg
---

## Preparing your g-code file

*** what CAM are we expecting them to use?
No matter what CAM software you are using, you must make sure that:

* Unique tool numbers are assigned to each tool you use in your toolpaths

* The format for each tool change within your g-code starts like this:

M5 (stop spindle)

M6 T1 (tool change, tool number; tool number needs to be whole numbers e.g. 1-12)

M3 SXXXXX (start spindle, spindle speed at XXXXX RPM)

To meet these criteria

Use our post-processor for Vectric VCarve

When using Vectric VCarve you edit tool numbers by going into each toolpath and editing the tool you’re using. It will pop up a window with all the parameters like diameter, feeds and speeds, etc. You should be able to find and edit the Tool Number. Edit that to match the position that tool will be on your rack. Remember Tool 1 is at the LEFTMOST position.

You cannot have the same tool number on Vectric, it will show an error when you are exporting, so need to rename the tools.

Connect to gSender

Home the machine

* Jog the machine away from the tool rack

* Press Home

The machine
Make sure in Config, under Tool Changing, the gSender Strategy is set to Ignore
