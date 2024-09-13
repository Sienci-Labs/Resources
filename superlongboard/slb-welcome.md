---
title: Welcome!
menu_order: 4
post_status: publish
post_excerpt: Documentation for the SuperLongBoard, the controller board for the LongMill Benchtop CNC router. Includes electrical and mechanical specifications.
post_date: 2024-03-03 14:43:00
taxonomy:
    knowledgebase_cat: slb-handbook
    knowledgebase_tag:
        - slb
custom_fields:
    KBName: SuperLongBoard
    basepress_post_icon: bp-caret-right
skip_file: no
featured_image: _images/_superlongboard/slb_slb-top.jpg
---

Hello and welcome!

If you’ve come here you’re either interested in or have already purchased our brand new endeavour into upgrading the Hobby CNC landscape, the <a href="https://sienci.com/product/slb/"><b>SuperLongBoard</b></a>!!

<img class="non aligncenter size-medium" style="width: 80%; margin-left: 10%;" src="https://resources.sienci.com/wp-content/uploads/2024/07/SLB-VB6-scaled.jpg"/>

Started in mid-2022, this project has been truly a labour of love for us. Thanks to the initial interest from the first 500 SLB purchasers, we were able to finish bringing the project to life. If you're one of those 500, a special welcome! As you go through our instructions let us know if there's any sticking points you run into and we'll be happy to get them sorted as soon as we can. The SLB may still have some quirks in its early days despite the many months of testing that we've put it through - but we're keen to make it the best it can be and trust we can all work together to make that happen :)

https://www.youtube.com/watch?v=LkZIeJQSzdM

## Diving In

Let's get rock'n'rolling by pointing you towards the right page for you 🎸

[su_table responsive="yes" fixed="yes"]
<table style="border: none !important;">
<tbody style="display: block; margin: 1% 15%;">
<tr>
<td style="text-align: center;"><a href="https://resources.sienci.com/view/slb-upgrading/"><img class="flie aligncenter" style="padding: 5% 15%;" src="https://resources.sienci.com/wp-content/uploads/2024/07/SLB-upgrade.png" width="511" height="512" /></a>
<b><a href="https://resources.sienci.com/view/slb-upgrading/">Upgrade</a></b><br>
Guide for switching to the SLB from an existing controller.
</td>
<td style="text-align: center;"><a href="https://resources.sienci.com/view/slb-manual/"><img class="flie aligncenter size-full" style="padding: 5% 15%;" src="https://resources.sienci.com/wp-content/uploads/2024/07/documents.png" width="512" height="512" /></a>
<b><a href="https://resources.sienci.com/view/slb-manual/">Board Details</a></b><br>
Learn all the nitty gritty about wiring, specs, and firmware.
</td>
</tr>
<tr>
<td style="text-align: center;"><a href="https://forum.sienci.com/c/slb/"><img class="flie aligncenter" style="padding: 5% 15%;" src="https://resources.sienci.com/wp-content/uploads/2024/07/community.png" width="512" height="512" /></a>
<b><a href="https://forum.sienci.com/c/slb/">Forum</a></b><br>
Share ideas for SLB features, or get help with problems.
</td>
<td style="text-align: center;"><a href="#open-source"><img class="flie aligncenter size-full" style="padding: 5% 15%;" src="https://resources.sienci.com/wp-content/uploads/2024/07/open-source-hardware.png" width="512" height="512" /></a>
<b><a href="#open-source">Open-Source</a></b><br>
Licensing and files for replication are now rolled out!
</td>
</tr>
</tbody>
</table>
[/su_table]

## More Questions?

We're continuing to add more information to documentation on the SLB including more information on wiring hookups, recommended accessory compatibilities, and more technical specifications. Otherwise, we've already covered lots of **Frequently Asked Questions** on:

- The <a href="https://sienci.com/product/slb/">SuperLongBoard product page</a>
- Recent videos on our <a href="https://www.youtube.com/@SienciLabs">YouTube channel</a>
- Many <a href="https://sienci.com/2023/11/08/next-big-slb-update/">blogs covering the history</a> of the development of the SLB

If you're still needing some extra support with your new SLB, you can always contact us directly at <a href="mailto:support@sienci.com">support@sienci.com</a>.

![](/_images/_superlongboard/slb_slb-mounted.jpg){.aligncenter .size-medium}

## FAQ

[su_spoiler title="<b>Q: Will the SLB work with my CNC?</b>" open="no" style="fancy" icon="chevron" anchor_in_url="yes"]
A: If it's a LongMill or AltMill then definitely it will. Otherwise, your CNC should be supported so long as it’s a <b>typical hobby CNC setup with open-loop Nema 23s</b>. As we roll out the SLB we'll begin hearing back on other successful configurations and update this 'Answer' appropriately, since otherwise we can't provide a definitive guarantee other than to say that it's very likely to work for most hobby CNCs. Other machines that have been proven to work so far: <b>Onefinity</b>.

We’ve earnestly done our best to ensure the SLB would be ideal for any typical setup since the inspiration for the SLB came from trying to take things that are normally only available on more expensive and ‘closed’ boards and bring them into the open source domain and at a more affordable price for the benefit of as many hobbyists as we could. This means that although you will need to change certain settings to match your specific setup,the SLB will support a range of machines and accessories including 5/24V limit switches, touch plates, tool length sensors, laser diodes, external 4th axis, and more.
[/su_spoiler]

[su_spoiler title="<b>Q: What about if I want to use higher voltage or external motor drivers?</b>" open="no" style="fancy" icon="chevron" anchor_in_url="yes"]
A: We do currently have another version of the SLB in the works that we're calling SLB EXT since it'll support much higher voltage and external motor drivers for closed loop support as well. This will extend even further SLB support for a broader range of machines and setups closer to production-level. This board will be what powers our AltMill CNC and you'll be able to see more updates about it on our blog as we begin making deliveries.
[/su_spoiler]

[su_spoiler title="<b>Q: How can I know if the SLB is right for me?</b>" open="no" style="fancy" icon="chevron" anchor_in_url="yes"]
A: There are many other options on the market that come with a wide range of features, simply put the choice between these will always come down to budget. If you don't think you need the features offered by the SLB then it'd make more sense to spend less money. In this case consider getting a more typical grbl board or some of the newer x32 hobby CNC boards that might require more DIY setup time for wiring or programming. For instance the Blackbox x32 has the benefit of a direct wireless connection but less extensability. If instead you feel like you want to pull all the stops to support a higher-end CNC or use more advanced features then you might want to increase your budget and look into a Centroid, UCCNC, or Mach setup. We believe though that we've done our best to match the SLB up with the mid-level hobby CNC community where it makes sense to spend $150-200 on a controller to really unlock all the capabilities you'd be looking to expect out of your $1000-4000 CNC.
[/su_spoiler]

## Story

We set out to create the SuperLongBoard in order to raise the bar for what hobby CNC machines could offer in the market. When it comes to using modern-day CNCs, most headaches come from keeping the machine running reliably after already going through machine setup, learning the software, and becoming familiar with materials, clamping, and cutting tools. There are also bottlenecks that hobbyists can run into when it comes to the functionality and convenience of their CNCs. This is where improved electronics and firmware can bring more reliability and features so your CNC does what you expect and can continue to grow with you.

### Past Work

Our first custom CNC control board we called the “LongBoard”. It was simple but capable, acting like a fancy daughter board to an Arduino Uno. It went through 4 major iterations as we learned how to improve reliability against EMI (using solutions like RC components), manufacturability, and longevity (iterating DFMA and adding switch arc suppression).

![](/_images/_superlongboard/slb_longboard-enclosed.jpg){.aligncenter .size-medium}

Some of its **<u>notable attributes</u>** included:

- Standard Arduino Uno as the ‘brains’ of the board
  - Powers all board IO via 5V 0.5A supplied over USB from the tethered computer
  - [Grbl](https://github.com/gnea/grbl/wiki)-based: a well performing and efficient CNC firmware built by Simen, Sonny and many other open-source community contributors, setting the stage for the existence of nearly all hobby CNCs to-date
- Accepts 12-48V for all non-IO but shipped to use a 24V 10A power brick
- 4, solder in-place standard TB6600 driver boards (X, duplicated Y, and Z-axis control)
  - <https://toshiba.semicon-storage.com/us/semiconductor/product/motor-driver-ics/stepping-motor-driver-ics/detail.TB6600HG.html>
  - Bipolar stepper motor driver set to ⅛ microstepping and set to draw peak 1.8-2A/ea but can draw up to 4.5A
- External, detachable, 'contact' style E-stop to control main power (power switch on older models with arc suppression circuitry)
  - Top-facing LED to indicate power to the board
- Onboard Play, Pause, and Stop buttons for hardwired firmware control
- Plugs for:
  - X, Y, and Z-axis 5V limit switches
  - 0-5V Spindle direction and PWM control (via M3, M4, M5, and S g-codes)
  - 'Contact' style touch plate input signal
  - 5V Coolant output (via M7, and M9 g-codes)
- On-board linear voltage regulator to provide up to 1A of 12V power for assorted accessories like a fan or LED strips
- Other assorted circuitry to protect against incorrect wiring and filter electrical noise from disrupting digital signals
- Designed to be easily enclosed to reduce dust while still being easy to assemble

This design came with some **<u>limitations</u>** though, which many other hobby CNCs also suffer from since they use grbl based control boards:

- As great as the Arduino Uno and grbl were for their time, new options have since emerged. The inherent memory and processing limitations of the Uno meant that grbl pushed the board to its limits, making the hardware sometimes unreliable and stopping any more features and improvements from being added.
- A combination of the sensitive EEPROM on the Arduino, the USB protocol the Arduino used, and the simpler circuitry used to protect against static build-up or EMI caused unpredictable CNC behaviour. This included disconnections during cutting jobs and unexpectedly altered firmware or machine settings which would need to be re-flashed or changed back.
- Relying on power over USB for all the boards IO had the advantage of signal isolation, but introduced issues if the user's computer had a low-rated or loose USB port.
- The TB6600 motor drivers are common and proven but use older motor-control technology and had associated components that would sometimes fail. This meant the drivers sometimes broke in transit or after short use, produced extra motor noise, generated excess heat, and limited machine speeds due to inefficiencies and mid-band resonance stalling.

![](/_images/_superlongboard/slb_longboard-on-onefinity.jpg){.aligncenter .size-medium}

All this together still made the LongBoard quite a great contender for its time, especially for its low price in the Hobby market. People were buying our boards to retrofit other CNCs like Onefinitys, Shapeokos, X-carves, and more, which spoke to its capabilities - but we still felt we could take more steps to reach a new level...

([Read more about the LongBoard](https://resources.sienci.com/view/lmk2-longboard-details/) if you're interested, or check out [the open source files](https://resources.sienci.com/view/lmk2-open-source/#longboard-cnc-controller) if you'd like to build one yourself!)

### Goals & Choices

The main vision for the SLB was that we wanted to achieve a greater all-in-one marriage of new hardware and firmware that could still meet all the current expectations for a Hobby CNC while leaving space to imagine the future of CNC. This meant we needed to continue to focus on low price and ease-of-use, address current pain-points, but also find ways to keep the hardware and firmware adaptable to features down the road. You can see below how we grouped these goals:

- **Basic Needs**
  - Maintain the existing functionality of the LongBoard controller
  - Use Firmware that's based on open source development happening in the community
  - Easy to update or re-flash
  - Robust against Firmware corruption from EMI
  - Operate using the power from a regular household wall outlet
  - Ease of manufacturing (low number of specialized or complex components, especially factoring in chip shortages)
  - Manufacturing BOM of the board, enclosure, and any other extras of around $100 on a 1000+ order batch
- **Upgrades**
  - Immune towards large EMI signals for high reliability
  - Upgraded motor drivers for reduced noise, heat, and higher motor speeds
  - Dual E-stop power off and input signal to inform CNC of cutting issues and propagate stop commands to Spindle, Vacuum, and other accessories
  - Switch internal processor input power from a computer USB input to the control board power supply to ensure multi-day jobs can resume successfully
  - Built-in support for switching between distinct PWM signal outputs for Laser and Spindle control
- **Extras & Future-proofing**
  - Mist coolant pin for additional automated accessory control
  - Control Spindles/VFDs and other accessories with Modbus over RS485
  - Independant 4th/rotary axis output to an external driver for simultaneous 4-axis cutting
  - Support for an independent Tool Length Sensor for tool changes
  - Lights on all IO to indicate when signals are being sent/received
  - RGB LED support for visible, standalone CNC status feedback
  - Support for dual Y-axis drivers and limit switches to support auto-squaring
  - Pause/Door sensor combination for either/or use-case
  - Additional processing and interface pins available for future add-ons
  - Communication connections (e.g. Rx and Tx) available for future control via external controller / pendant

Seasoned CNCers might see this list of goals and features and wonder why we didn't just go with one of the many other solutions that were already on the market. This is a great question, and it's one we thought long and hard about because we didn't want to reinvent the wheel. This is a summary of some of our research as we explored our options:

- **Proven but Closed systems**
  - In our eyes this encapsulated options like [Centroid](https://www.centroidcnc.com/), Mach boards, [Masso](https://www.masso.com.au/), [CNCdrive](http://cncdrive.com/products.html), [PlanetCNC](https://planet-cnc.com/hardware/), and [SmoothStepper](https://warp9td.com/index.php/products)
  - Many of these have had plenty of time in the market to work out kinks and become reliable for a variety of uses
  - They also come with their own proprietary machine control software and board designs, meaning that you can just drop in the board customized to your setup and be ready to go which many CNC manufacturers can appreciate
  - For us this was a downside though, because as a company we've always been keen to use open solutions in our hardware and software, and though you're getting a package deal for an all-in-one solution it also usually comes at a notable cost increase which could have a large impact on the cost of our budget CNCs
  - We'd also done years of work already maintaining and improving [our own open source g-code sender](https://sienci.com/gsender/) which we felt had become an asset to the community, so we preferred to find a solution that could leverage that work
  - Another downside is that more established board manufacturers tended to use more complex industry terms and solutions in their documentation, support, and design approach which we felt intimidated many hobbyists and reduced ease-of-use
- **Open but Dispersed systems**
  - This seemed to include options such as [Buildbotics](https://buildbotics.com/), [ShopBot FabMo](http://gofabmo.org/), [Beaglebone running MachineKit](https://www.beagleboard.org/boards), [Smoothieboard](https://smoothieware.org/smoothieboard), [g2core](https://github.com/synthetos/g2) used by Bantam Tools, as well as expanded versions of grbl on the Arduino Mega like [grbl-Mega](https://github.com/gnea/grbl-Mega), [grbl-Mega-5X](https://github.com/fra589/grbl-Mega-5X), or [RabbitGRBL](https://github.com/SourceRabbit/RabbitGRBL)
  - These are all amazing for what they've contributed to the open source CNCing community and at one point made big impacts on what CNCs were capable of at lower price points
  - The main downside is that the hardware and/or the firmware behind them either never reached wider adoption past one board or platform, or the development team began to stagnate over the long lifespan of the project
  - In either of these cases, we wanted to become involved in a more widely adapted and actively developed system so that we could be comfortable committing the future of Sienci Labs to it, and feel good knowing our contributions would go back to benefit others in the open source community
- **Open and well-adapted systems**
  - These are the options we spent a longer time looking much closer at since they seemed much more in line with our goals: [grblHAL](https://www.grbl.org/what-is-grblhal) ([Flexi-HAL](https://expatria.myshopify.com/products/flexi-hal), [grblHAL Teensy](https://www.tindie.com/products/philba/grblhal-bob-unkit-for-teensy-41-t41u5xbb/)), [FluidNC](https://github.com/bdring/FluidNC) ([BlackBox](https://openbuildspartstore.com/BlackBox-Motion-Control-System-X32), [Root Controller ISO](https://rootcnc.com/), [xPRO V5](https://www.spark-concepts.com/cnc-xpro-v5/)), [µCNC](https://github.com/Paciente8159/uCNC), [LinuxCNC](https://linuxcnc.org/) ([Mesa](http://www.mesanet.com/)), [RepRap](https://github.com/Duet3D/RepRapFirmware), [Marlin](https://marlinfw.org/), [Klipper](https://www.klipper3d.org/)
  - You'll notice that most of these are primarily firmware options and not firmware-hardware systems, and that's because these systems reached such a wide adoption that they mostly can't be tied to a specific set of boards anymore
  - With the majority of these being open source, actively developed, and widely adopted options, the only way to narrow down was to start looking at features we found important
  - For instance, realtime commands and overrides didn't tend to exist at the core of 3D printing firmware, while some other options were getting bloated from incorporating too many specialized features that didn't benefit hobbyists

After contemplating our options, we chose to commit to **grblHAL** to build a new board around because we wanted a system that:

1. Put CNC routing first
1. Was built to be configurable and hardware agnostic
1. Was able to run on a standalone MCU with a regular computer or by hooking up onboard computation
1. Used realtime commands for greater safety while cutting

Luckily, being hardware agnostic meant that we could dive straight in with our own grblHAL board design since there were already some other great open source CNC board designs in the wild we could get inspiration from! We also got lucky to collaborate with Expatria Technologies (who made the [Flexi-HAL](https://expatria.myshopify.com/products/flexi-hal) controller) and work on the SuperLongBoard design together.

### Present

![](/_images/_superlongboard/_upgrade/slb_up_p1_SLB.jpg){.aligncenter .size-medium}

With thanks to Andrew and the Expatria team, Terje, grblHAL, our Beta testing community, and the PrintNC community, after over 1.5 years and over $200k in R&D we started shipping the SLB in 2024. The full story stretched out over many updates:

- [First look at the SuperLongBoard](https://sienci.com/2023/04/10/first-look-at-the-superlongboard/) (Apr 10, 23)
- [May 2023 Production Updates](https://sienci.com/2023/05/01/may-2023-production-updates/) (May 1, 23)
- [August 2023 Production Updates](https://sienci.com/2023/08/01/august-2023-production-updates/) (Aug 1, 23)
- [September 2023 Production Updates](https://sienci.com/2023/09/05/september-2023-production-updates/) (Sep 5, 23)
- [October 2023 Production Updates](https://sienci.com/2023/10/01/october-2023-production-updates/) (Oct 1, 23)
- [Next Big SLB Update](https://sienci.com/2023/11/08/next-big-slb-update/) (Nov 8, 23)
- [SuperLongBoard Pre-orders to Launch Dec 4, 2023](https://sienci.com/2023/11/27/superlongboard-pre-orders-to-launch-dec-4-2023/) (Nov 27, 23)
- [SLB January Updates](https://sienci.com/2024/01/25/slb-january-updates/) (Jan 25, 23)
- [Feb-ulous SLB news](https://sienci.com/2024/02/29/feb-ulous-slb-news/) (Feb 29, 24)
- [Introducing the LongMill MK2.5](https://sienci.com/2024/05/10/introducing-longmill-mk2-5/) (May 10, 24)

All in all, we feel the launch of this board means we succeeded in taking one of the largest steps in achieving our goals towards more reliable, capable, and future-proofed hobby CNC systems for many years to come. Those in the community also seem to strongly agree - as of the time of writing, we've already sold nearly 700 boards to a wide range of CNC owners all over the world.

If you want to see the types of features and options the SuperLongBoard presently ships with, please feel free to check out our [Technical Manual](https://resources.sienci.com/view/slb-manual/) or its [store page](https://sienci.com/product/slb/) - also remember that this board is fully open source so if you'd like to build one yourself or build off the work we've done, we'd love to see your contributions!

## Open Source

![](/_images/_superlongboard/_manual/slb_ma_p2_DrawBoard.jpg){.aligncenter .size-full}

All of the SuperLongBoard project is licensed as "CERN-OHL-S v2". This means stuff like licensing your code and hardware changes under the same license, giving attribution to us, and if you use our firmware on other hardware then that hardware should have the same license too. You can [read more about the license here](https://ohwr.org/project/cernohl/wikis/Documents/CERN-OHL-version-2), in the LICENSE file contained in most repos, or in the License headers of the affected files.

The SLB Firmware is made up of 11 repos plus there's the repo containing the design of the board:

- **Main Repos**
  - <https://github.com/Sienci-Labs/SuperLongBoard> (the all new board design that we worked 2+ years to bring to the public in collaboration with Expatria Technologies. The unique features are many to count, so easier to see a list of them all here: <https://resources.sienci.com/view/slb-manual/#features-list>
  - <https://github.com/Sienci-Labs/sienciHAL> (main firmware repo where all plugins and grblHAL core code come together to run the SLB)
- **Novel Repos**
  - <https://github.com/Sienci-Labs/GRBLHAL_bootloader_plugin> (STM DFU support boot mode)
  - <https://github.com/Sienci-Labs/grblhal-aux-macros> (macros attached to AUX input buttons)
  - <https://github.com/Sienci-Labs/grblhal-switchbank> (support trigger from M62-65 commands, subscribe to common actions)
- **Additions to Existing Work**
  - <https://github.com/Sienci-Labs/grblhal_core> (added TMC support, plugins_init.h for 3rd party plugins, SLB config, 4th axis handling, dual PWM, $spindles capability, RGB LEDs, Switchbank)
  - <https://github.com/Sienci-Labs/Trinamic-library> (to support the SLBs onboard Trinamic motor drivers)
  - <https://github.com/Sienci-Labs/Plugins_motor> (added TMC support, standstill current reduction, 4th axis, updated settings descriptions)
  - <https://github.com/Sienci-Labs/Plugins_spindle> (added dual default spindles and reordering)
  - <https://github.com/Sienci-Labs/Plugins_laser> (added separated PWM EN invert control of Laser, corrected power reporting)
  - <https://github.com/Sienci-Labs/grblhal-rgb-plugin> (neopixel bitbanging, added white/off overrides, M-code control, improved latching)
  - <https://github.com/Sienci-Labs/grblhal_probe_plugin> (added dual XOR probe support, probe away and invert addressed)

If you want to make your own pin map for the SLB, check out:<br><https://github.com/Sienci-Labs/sienciHAL/blob/SLB_Bringup_Dev/Inc/longboard32_map.h>

## Still To Do

There are still many ambitions of our original goal we have yet to get to. They had to either be left out of the original project because of budget or time constraints, or we'd already planned to get to them after the initial board launch but we're now waiting to stabilize the project before adding more to it. If you have any thoughts on these ideas then let us know!

- Auto-squaring
- Further motor driver tuning
- Streaming from onboard SD card
- Better tool changing support and ATC
- Stall detection
- EEPROM cleanup
- Machine odometer to use for maintenance reminders
- Storage or all other machine-specific config onboard
- Pendant implementation with common market options
- LED state cycling
- Other RS485 accessory support (like IOT relay)
- S-curve motion
- Independant plunging override
