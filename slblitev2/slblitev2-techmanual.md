---
title: Technical Manual
menu_order: 3
post_status: draft
post_excerpt: In depth functionality of the SLB-LITE / SLB-EXT V2 
post_date: 2024-04-03 16:44:00
taxonomy:
    knowledgebase_cat: slblitev2-handbook
    knowledgebase_tag:
        - slblitev2
custom_fields:
    KBName: SLB-LITE / SLB-EXT V2
    basepress_post_icon: bp-caret-right
skip_file: no
featured_image: _images/_superlongboard/slb_slb-leds.jpg
---


![](/_images/_slblitev2/slblitev2_techmanual-enclosure.jpg){.aligncenter .size-medium}

![](/_images/_slblitev2/slblitev2_techmanual-dimension.jpg){.aligncenter .size-medium}


| State           | Description                                                         | Colour & Animation                              |
|-----------------|---------------------------------------------------------------------|-------------------------------------------------|
| Idle            | Machine ready, waiting for commands                                 | Solid white                                     |
| Cycle / Running | G-code is running, like a job or a macro                            | Solid green                                     |
| Jogging         | Machine is jogged                                                   | Green comet with short bright head and dim tail |
| Hold            | Job is paused                                                       | Full-ring yellow pulse between dim and bright   |
| Safety Door     | Spindle and coolant disabled, waiting on switch to close (advanced) | Alternating yellow half-ring blink              |
| Homing          | Homing is in progress                                               | Mirrored blue sweep from opposite sides         |
| Check Door      | Safety door detected as opened, door state initiated (advanced)     | Rotating cyan checkerboard                      |
| Alarm           | An alarm is triggered                                               | Red chase with fading tail                      |
| E-stop          | E-stop is triggered                                                 | Full-ring red blink                             |
| Tool Change     | Tool change is in progress                                          | Rotating magenta dotted pattern                 |
| Sleep           | De-energizes motors, spindle and coolant until reset                | Solid grey                                      |

![](/_images/_slblitev2/slblitev2_qsg-estoplight.gif){.aligncenter .size-full}

![](/_images/_slblitev2/slblitev2_techmanual-statuslights.jpg){.aligncenter .size-medium}

![](/_images/_slblitev2/slblitev2_techmanual-estopv2.jpg){.aligncenter .size-medium}

![](/_images/_slblitev2/slblitev2_techmanual-motor.jpg){.aligncenter .size-medium}

![](/_images/_slblitev2/slblitev2_techmanual-spindle.jpg){.aligncenter .size-medium}

![](/_images/_slblitev2/slblitev2_techmanual-laser.jpeg){.aligncenter .size-medium}

![](../_images/_slblitev2/slblitev2_techmanual-firmware2.jpg){.aligncenter .size-medium}

![](/_images/_slblitev2/slblitev2_techmanual-laser2.jpg){.aligncenter .size-medium}

![](/_images/_slblitev2/slblitev2_techmanual-prb.jpg){.aligncenter .size-medium}

![](/_images/_slblitev2/slblitev2_qsg-prbelight.gif){.aligncenter .size-full}

![](/_images/_slblitev2/slblitev2_techmanual-tls.jpg){.aligncenter .size-medium}

![](/_images/_slblitev2/slblitev2_techmanual-tls-setting.jpg){.aligncenter .size-medium}

![](/_images/_slblitev2/slblitev2_techmanual-home.jpg){.aligncenter .size-medium}

![](/_images/_slblitev2/slblitev2_techmanual-tls-setting2.jpg){.aligncenter .size-medium}

![](/_images/_slblitev2/slblitev2_techmanual-tls-setting3.jpg){.aligncenter .size-medium}

![](/_images/_slblitev2/slblitev2_techmanual-auxv2.jpeg){.aligncenter .size-medium}

![](/_images/_slblitev2/slblitev2_techmanual-exp.jpeg){.aligncenter .size-medium}

![](/_images/_slblitev2/slblitev2_techmanual-exppinout.jpg){.aligncenter .size-medium}
