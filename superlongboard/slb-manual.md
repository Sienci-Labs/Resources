---
title: Technical Manual
menu_order: 5
post_status: publish
post_excerpt: Documentation for the SuperLongBoard, a next-generation, 32-bit control board for the LongMill and other CNC routers. Includes electrical and mechanical specs.
post_date: 2024-04-03 16:50:00
taxonomy:
    knowledgebase_cat: slb-handbook
    knowledgebase_tag:
        - slb
custom_fields:
    KBName: SuperLongBoard
    basepress_post_icon: bp-caret-right
skip_file: no
featured_image: _images/_superlongboard/_manual/slb_ma_p1_Board.jpg
---

[basepress-notice style="default"]If there's any extra information you'd like to see regarding the SLBs specs, just let us know and we'll work to add it 👍[/basepress-notice]

This document is the “SLB bible” for any of the ‘raw’ answers you might be looking for when setting up your new board. This includes sections on all the features, their pinouts, associated settings, and other things you should know when installing the SLB onto your CNC.

You’ll find that the SLB builds a lot onto our original LongBoard while maintaining a lot of the familiar behaviour and features. If you find any holes in this documentation, brush up on the original LongBoard documentation here: <a href="https://resources.sienci.com/view/lmk2-LongBoard-details/">https://resources.sienci.com/view/lmk2-longboard-details/</a>. Learn more about the latest updates on Beta testing and board developments on our company Blog or SLB page: <a href="https://sienci.com/product/slb/">https://sienci.com/product/slb/</a>

![](/_images/_superlongboard/_manual/slb_ma_p1_Board.jpg){.aligncenter .size-full}

### Features List

Comparing the SLB to our Original LongBoard and to other controllers on the market, some of the main advantages you might notice:

- Be confident in your CNC completing jobs in a variety of environments. Vastly improved reliability and immunity against EMI with better board wiring, protective components, onboard ferrite improved USB protocol, processor capability, larger buffer, and Ethernet as a communication alternative
- Faster CNC speeds and less motor noise by using more efficient motor drivers
- Safer E-stop informs machine when an emergency has happened and de-powers all accessories
- Detachable E-stop gives you something to reach for if your CNC starts going where you didn't expect
- RGB CNC Status lights visible from a distance to always know what your CNC is up to or if something’s gone wrong. Light onboard plus support for external RGB strips to set up as you wish: under your X-axis rail, a router/spindle ring light
- 3 programmable buttons for you to customize your CNC to your workflow
- Live overrides to fine-tune your feeds & speeds on the fly when running a job
- Supports inductive sensors for far more accurate and repeatable CNC positioning for job recovery or multi-day runs than using stall homing in a dirty CNC environment, also use mechanical switches
- Individual axis holding current, allows you to hold just the Z-axis from falling with a heavy spindle without having to keep all other motors powered too
- Added support for an independent Tool Length Sensor for tool changes
- Control Spindles/VFDs and other accessories with Modbus over RS485
- Independant 4th/rotary axis output to an external driver for simultaneous 4-axis cutting
- More customizable IO to fine-tune your at-home or shop CNC setup
- Powered by HAL, leaving bandwidth for even more features to be added with future firmware updates
- Don’t have to pay extra for a built-in computer, instead choose to run something lightweight you already have on hand or a more powerful setup to combine both design and CNC control from one computer in your shop

### Dimensions

The SuperLongBoard is a typical PCB with a roughly 210 x 100 x 20mm (8.3x4x0.8”) footprint, not including plug stick-out on the short ends. It’s designed to either fit inside its enclosure, accommodate up to 4mm of edge mounting on the long side, or mount via 4 standoffs.

![](/_images/_superlongboard/_manual/slb_ma_p2_DrawBoard.jpg){.aligncenter .size-full}

The enclosure has a rough size of 215 x 112 x 50mm (8.5x4.4x2”) not including the 16mm (0.63”) flanges on the short ends. These flanges allow it to be mounted to any flat surface either horizontally or vertically as pictured. The backside of the enclosure also has a feature to fit a bracket which allows the SLB to mount to the Y-axis rail of any LongMill MK2 CNC.

![](/_images/_superlongboard/_manual/slb_ma_p3_SLBCase.jpg){.aligncenter .size-full}

The enclosure has been designed with reasonable consideration for dust penetration, but if you are a more cautious person you can feel free to mount the box further away from your CNC. When placing your SLB on its own or among other CNC control electronics, consider that most wires are designed to route out the backside of the enclosure with the exception of a handful of more typically accessible plugs on its front like the E-stop and USB-C. For more information on mounting the enclosure see the section on <a href="#enclosure-mounting">Enclosure Mounting</a>.
<p style="text-align: center;"><em><b>Note</b>: for the rest of the docs the typical naming orientation for the SLB is shown below</em></p>

![](/_images/_superlongboard/_manual/slb_ma_p4_TopBottom.jpg){.aligncenter .size-full}

### Software

<div style="margin-bottom: 20px; padding-left: 22px; text-indent: -22px;"><b>Sender:</b> Any g-code senders able to run “<b>grblHAL</b>” should be able to support most of the SLBs features. We recommend using <a href="https://sienci.com/gSender/"><b>gSender</b></a> to get the most out of your SLB (you have to use at least version 1.4.0 or later). If you prefer other options, you could try <a href="https://github.com/terjeio/ioSender/releases">ioSender</a>, <a href="https://winder.github.io/ugs_website/download/">UGS</a>, or <a href="https://software.openbuilds.com/">OpenBuilds CONTROL</a>.</div>

<div style="margin-bottom: 20px; padding-left: 22px;">Some other common options like <b>Easel</b>, VTransfer, CNCjs, and Candle might not yet work with the newer and more advanced firmware of the SLB. <b>You can still use programs like Easel to design your projects</b>, you just need to <a href="https://inventables.zendesk.com/hc/en-us/articles/4406926040979-Exporting-Gcode-From-Easel" target="_blank" rel="noopener">Export the g-code</a> and run the file in a newer g-code sender instead of running it using the design program itself.</div>

<div style="margin-bottom: 20px; padding-left: 22px; text-indent: -22px;"><b>Post Processor:</b> For now, the SLB will continue working the best with any typical ‘grbl’ post processor setup. If you already had a working grbl setup then you won't need to change anything, but if the SLB is your first board then you can check out our <a href="https://resources.sienci.com/view/lmk2-post-processors/" target="_blank" rel="noopener">Post Processor suggestions</a> page.</div>

<div style="margin-bottom: 20px; padding-left: 22px;">This works because any g-code supported by grbl is also supported by grblHAL, so there's full forward compatibility even with all your past cutting files. As we continue to expand on the SLBs capabilities there might be an “SLB” or “grblHAL” post processor released in the future that introduces new g-code to control those new features. If/when this happens we'll keep this section updated. If you'd like to try your own exploration in the meantime, you can read more on the superset of other niche g-codes (based on primarily LinuxCNC specifications) here: <a href="https://github.com/grblHAL/core/wiki/Additional-G--and-M-codes" target="_blank" rel="noopener">Additional G and M codes</a>.</div>

<div style="margin-bottom: 20px; padding-left: 22px; text-indent: -22px;"><b>Computer:</b> The SLB runs independent of your computer's ability, so as long as your computer is able to run newer versions of gSender or another g-code sending software without freezing up then your setup will be good. That being said, some old computers can have less reliable USB ports so in some cases it might be worth the upgrade if it makes your cutting more reliable.</div>

### Firmware

The SLB runs grblHAL, which may look similar in name to grbl but for all intents and purposes is a completely new approach to CNC control. Your board will ship with the latest version of firmware already installed, but we’ll occasionally release updates for new features, functionality, or bug fixes. For more information on this process, go to the <a href="https://resources.sienci.com/view/slb-firmware-flashing/">Firmware Flashing</a> page.

### Open Source

This project has no patents, we make everything available to the public just like much of the rest of Sienci Labs’ projects. As we start to roll out the SLB into production, we’ll <a href="https://resources.sienci.com/view/slb-welcome/#open-source">post our source files</a> for firmware tweaks from Core grblHAL, our custom grblHAL plugins, the SuperLongBoard PCB design, enclosure design, and any other relevant manufacturing and sourcing info we can think of. We’ll also make sure we’re clear on the licenses for use.

## Wiring

The SLB accepts the same or similar input and output plugs as our original LongBoard; you should be able to unplug everything from the LongBoard and re-plug everything back into the SLB without much trouble. The only exceptions are the new USB-C communication cable, and the **SpinPWM**, **SpinDir**, and **AUX limits**, which can be easily rewired to the new terminal connectors with a small flat head screwdriver. The 12V misc output is also now 24V and switchable, see the section on ‘<a href="#accessory-outputs">Accessory Outputs</a>’ to learn about this.

Some of the connectors are inside the enclosure so you’ll need to remove the cover to access them. To remove the cover, unscrew the top-right thumbscrew a couple turns (pictured) then slide the cover to the right. Once the hole in the cover lines up, you’ll be able to pull the top of the cover towards you and it will come free.

![](/_images/_superlongboard/_manual/slb_ma_p5_Open.png){.aligncenter .size-full}

Route all the wires from inside the enclosure through the two cable guides at the back so you can close the lid again. The smaller, bottom one is meant to snugly fit all the motor cables, while the remaining cables should all fit into the larger, upper opening. These cable guides will keep all your wires in place when you’re accessing the inside.

![](/_images/_superlongboard/_manual/slb_ma_p6_WiresMotor.jpg){.aligncenter .size-full}

Here’s a general wiring ‘map’ you can use as a reference to start hooking things up. It covers the full scope of plugs and features that the SLB currently supports. Go <a href="#connectors-list">here for the full list of connectors</a>.

![](/_images/_superlongboard/_manual/slb_ma_p7_ColourQuads.jpg){.aligncenter .size-full}

[su_table responsive="yes" fixed="yes"]
<table>
<tbody>
<tr>
<td style="background: #e06666 !important;"><a href="#power-amp-E-stop"><b>Power &amp; E-stop</b></a></td>
<td>Power in and control via switch, E-stop, E-stop backup, and board reset</td>
</tr>
<tr>
<td style="background: #a4c2f4 !important;"><a href="#usb-amp-ethernet"><b>USB &amp; Ethernet</b></a></td>
<td>Communication ‘streaming’ to the SLB</td>
</tr>
<tr>
<td style="background: #92d177 !important;"><a href="#motors"><b>Motors</b></a></td>
<td>Typical 3 axis (ganged Y) bipolar stepper motor control</td>
</tr>
<tr>
<td><a href="#touch-plateprobe"><b>Touch Plate/Probe</b></a></td>
<td>Supports touch plates or other surface probing</td>
</tr>
<tr>
<td style="background: #7875fa !important;"><a href="#status-lights"><b>Status Lights</b></a></td>
<td>Onboard CNC status light, RGB LED strip outputs, other diagnostics lights</td>
</tr>
<tr>
<td style="background: #b27cc3 !important;"><a href="#homing-amp-limit-switches"><b>Limit Switches</b></a></td>
<td>Hookup for Homing/Limits with two plug styles, also supports min/max switches for hard limits</td>
</tr>
<tr>
<td><a href="#laser"><b>Laser</b></a></td>
<td>5V PWM dedicated output for independent Laser control</td>
</tr>
<tr>
<td style="background: #e06666 !important;"><a href="#action-buttons"><b>Action Buttons</b></a></td>
<td>3 programmable action buttons that support macros</td>
</tr>
<tr>
<td style="background: #ffee66 !important;"><a href="#accessory-outputs"><b>Accessory Outputs</b></a></td>
<td>2 SWITCH outputs that turn on any external circuits 1-24V up to 1A, and 2 AUX POWER outputs which provide up to 24V 250mA to external accessories</td>
</tr>
<tr>
<td style="background: #f6a66b !important;"><a href="#spindlers485"><b>Spindle/RS485</b></a></td>
<td>Controls a Spindle or VFD using 5V PWM or RS485</td>
</tr>
<tr>
<td><a href="#tls"><b>Tool Length Sensor</b></a></td>
<td>Powered input for a Tool Length Sensor for tool changing or for use as a secondary probe</td>
</tr>
<tr>
<td style="background: #9deefa !important;"><a href="#rotary-axis"><b>Rotary/4th/A-Axis</b></a></td>
<td>Output signals for an external motor driver and input of an independent rotary axis limit switch</td>
</tr>
</tbody>
</table>
[/su_table]

### Power & E-stop

Each SLB comes with an E-stop and pre-made wiring to keep you safe out-of-the-box when cutting. When pressed, the E-stop is designed to cut all power to your CNCs stepper motors and also send a signal back to the MCU to disable all other accessories that your SLB controls. This includes turning off the spindle, IOT Relay, and anything else that’s triggered by M3/4 and M7/8 commands. Use the E-stop when there's a hazard during carving and you need to immediately stop the machine.

Otherwise, the SLB needs a **24V 10A power supply** to run all stepper motors at rated current alongside the other onboard accessories. Higher current such as 24V 12.5A is even better so the power supply isn't strained even during peak draw. You can either provide this yourself, <a href="https://sienci.com/product/24v-12-5a-power-adapter-for-110vac/" target="_blank" rel="noopener">purchase one from us</a>, or use your existing one if you’re switching over to the SLB from our original LongBoard.

1. The larger 2-pin plug on the left side is the power connection
1. There’s a main power switch above it to switch main power to the whole board
1. The plug on the bottom right is for the E-stop and its customizable action buttons
1. For troubleshooting reasons there's also an:
   - **E-stop** pin on the bottom left to act as an override if the main E-stop switch is broken
   - **Reset pin** on the top right to quickly power-cycle the board

![](/_images/_superlongboard/_manual/slb_ma_p8_PowerEstop.jpg){.aligncenter .size-full}

A good rule of thumb is to **have the power switch ‘Off’** (slide it UP to be in the OFF position) whenever you plug or unplug the power cable. **MAKE SURE** the polarity of the power supply connector is correct before plugging it in (red/+ on top and black/- on the bottom, Sienci power supplies should already be correctly wired).

Once the SLB is powered up, press down on the E-stop to engage it and twist it clockwise (follow the arrows) while pulling up to disengage it. You’ll know it is engaged when the E-stop light turns off, and disengaged when the power light turns back on. If you suspect your E-stop isn’t working, <a href="https://resources.sienci.com/view/slb-troubleshooting/#bad-E-stop">check our E-stop troubleshooting steps</a>.

Since each SLB comes with an E-stop and pre-made wiring, you’ll only need to reference the diagram above if you want to make a custom setup or for troubleshooting. If you accidentally plug the E-stop cable into the Ethernet port, this shouldn’t cause any damage to your SLB.

![](/_images/_superlongboard/_manual/slb_ma_p9_EStopButts.jpg){.aligncenter .size-medium}

If you want to set up the custom action buttons for your E-stop now, jump forward to the <a href="#action-buttons">Action Buttons</a> section :)

### USB & Ethernet

The SLB offers USB-C as well as Ethernet as a way to connect your CNC to your computer. Both are isolated for noise, with larger data buffers, and should provide a reliable connection. Though Ethernet is generally considered to be more reliable, we worked hard on a robust USB interface with far more data checks and signal isolation to match a typical Ethernet setup. This means you can use either, but USB-C is more beginner friendly and at the minimum a USB-C connection is needed to perform the initial board setup. If you want to place your computer further away from your machine or feel that the USB is still occasionally causing you issues then we'd recommend switching over to Ethernet.

![](/_images/_superlongboard/_manual/slb_ma_p10_RedBoxes.jpg){.aligncenter .size-full}

The SLB needs to be powered via 12-24V and turned on for you to be able to make any USB or Ethernet connection.

To connect over USB, plug the cable into the front of the control box and into an available USB port on your computer, then refresh the USB list in gSender or ioSender, click the new device, and connect. Ensure that the USB cable you use is capable of data transfer and not just charging. You should see the light near the USB port turn on to confirm a connection (not working on current boards). If in gSender it doesn’t connect, make sure you’ve selected ‘grblHAL’ in the dropdown.

![](/_images/_superlongboard/_manual/slb_ma_p11_PowerPlug.png "Plug the USB-C cable into the front"){.aligncenter .size-medium}

To connect over Ethernet, you'll need:

- An Ethernet cable
- A g-code sender that can connect to CNCs over a network, like gSender or ioSender
- A device with a free Ethernet port that can also run the g-code sender
  - If your computer only has one Ethernet port and it’s already used, you can try picking up a USB to Ethernet dongle or adding an additional Ethernet card. You don’t need anything fancy since the SLB only needs 1-2 Mbps of bandwidth to run. If you use the dongle, the USB side will plug into your computer, and the Ethernet side will connect an Ethernet cable that you’ll run to the SLB.

![](/_images/_superlongboard/_manual/slb_ma_p12_USB.jpg){.aligncenter .size-full}

Keep in mind that setting up Ethernet is a bit more involved, and at the time of SLB launch we’ll be primarily aiming to support direct Ethernet communication from a computer to the SLB; not sending over a network. Also **the SLBs STM32 chip isn't capable of supporting firmware flashing over Ethernet so keep the USB-C cable handy if you need to do any future updates or recover from a board reset**.

#### Ethernet on Windows

[tabby title="Current" open="yes"]

1. To start, connect to your CNC over USB to note down the EEPROM values set for the IP address and Netmask (302 and 304). The defaults should be IP: `192.168.5.1` and Netmask: `255.255.255.0` with the IP mode set to `static`.
  ![](/_images/_superlongboard/_manual/slb_ma_p13_IPMode-newu.jpg){.aligncenter .size-full}
1. Once confirmed, you can unplug your USB and connect the Ethernet cable directly from your PC to your board. If you look where you plugged the Ethernet cable into the SLBs port from the outside, you should see a green light on and a flickering yellow light.
1. You’ll need to configure the PC’s Ethernet interface. Open network connections to get a list of Ethernet ports.
  ![](/_images/_superlongboard/_manual/slb_ma_p14_TCP.jpg){.aligncenter .size-full}
1. Right click your Ethernet port and go to Properties and then find the “Internet Protocol Version 4 (TCP/IPv4)” entry and open its properties.
  ![](/_images/_superlongboard/_manual/slb_ma_p15_IP.jpg){.aligncenter .size-full .nar}
1. Select the “Use the following IP address:” option and configure it as above. You want the subnet mask to be the same value from the EEPROM 'Netmask'. The IP address should have a different last digit on the same mask - so if the board is device 1 (192.168.5.1), you could call your PC device 5 (192.168.5.5). Click “OK” to save and close the options.
1. Back in gSenders Config tab ➜ Ethernet section, make sure the IP address for gSender matches the IP address from the firmware.
  ![](/_images/_superlongboard/_manual/slb_ma_p16_EEPROM-newu.jpg){.aligncenter .size-medium}
1. Now click on Connect to CNC, choose the Ethernet Port option and you should see it connect successfully :)
  ![](/_images/_superlongboard/_manual/slb_ma_p17_Connected-newu.jpg){.aligncenter .size-medium}
1. If you have a problem connecting with Ethernet, go back over the setup steps. You can also reconnect over USB to double-check your SLB Ethernet settings.

[tabby title="Classic gSender"]

1. To start, connect to your CNC over USB to note down the EEPROM values set for the IP address and Netmask (302 and 304). The defaults should be IP: `192.168.5.1` and Netmask: `255.255.255.0` with the IP mode set to `static`.
  ![](/_images/_superlongboard/_manual/slb_ma_p13_IPMode.jpg){.aligncenter .size-full .nar}
1. Once confirmed, you can unplug your USB and connect the Ethernet cable directly from your PC to your board. If you look where you plugged the Ethernet cable into the SLBs port from the outside, you should see a green light on and a flickering yellow light.
1. You’ll need to configure the PC’s Ethernet interface. Open network connections to get a list of Ethernet ports.
  ![](/_images/_superlongboard/_manual/slb_ma_p14_TCP.jpg){.aligncenter .size-full}
1. Right click your Ethernet port and go to Properties and then find the “Internet Protocol Version 4 (TCP/IPv4)” entry and open its properties.
  ![](/_images/_superlongboard/_manual/slb_ma_p15_IP.jpg){.aligncenter .size-full .nar}
1. Select the “Use the following IP address:” option and configure it as above. You want the subnet mask to be the same value from the EEPROM 'Netmask'. The IP address should have a different last digit on the same mask - so if the board is device 1 (192.168.5.1), you could call your PC device 5 (192.168.5.5). Click “OK” to save and close the options.
1. Back in gSenders general Settings, make sure the IP Range matches the IP from the EEPROM.
  ![](/_images/_superlongboard/_manual/slb_ma_p16_EEPROM.jpg){.aligncenter .size-full .nar}
1. With the grblHAL firmware selected, choose the ‘Network Devices’ option and you should see it connect successfully :)
  ![](/_images/_superlongboard/_manual/slb_ma_p17_Connected.jpg){.aligncenter .size-full}
1. If you have a problem connecting with Ethernet, go back over the setup steps. You can also reconnect over USB to double-check your SLB Ethernet settings.

[tabbyending]

#### Ethernet on Mac

To set up an Ethernet connection to the SLB from a Mac, you'll follow a lot of the same steps as for [Ethernet on Windows](#ethernet-on-windows) but after doing **Step 2**:

1. On your Mac, click the Apple menu ➜ System Settings ➜ then click '🌐 Network' in the sidebar (you may need to scroll down).
1. Click Ethernet service ➜ 'Details...'. Note: if your Mac doesn’t have a built-in Ethernet port and you’re using an adapter, look for a service that contains the name of the adapter manufacturer or the type of adapter. For example, the service might be named [manufacturer name] USB-C LAN, or just contain the model number of the adapter.
1. Click TCP/IP in the sidebar ➜ then for 'Configure IPv4' choose 'Manually' so you can enter the specific IP address and subnet mask. You want the subnet mask to be the same value from the EEPROM 'Netmask'. The IP address should have a different last digit on the same mask - so if the board is device 1 (192.168.5.1), you could call your PC device 5 (192.168.5.5). Click “OK” to save and close the options.
![](/_images/_superlongboard/_manual/slb_ma_p15-ip-2.jpg){.aligncenter .size-full}
1. Resume following the Windows instructions at Step 6 to finish the process.

### Motors

The board comes with 4 onboard stepper motor drivers so you can plug a typical XYYZ CNC router straight in. We recommend putting the left side motor on Y1 and the right side motor on Y2. If you ever need to swap cables around, grabbing the connectors by their sides and wiggling back and forth helps them pop back off easily.

![](/_images/_superlongboard/_manual/slb_ma_p18_MotorsPlugs.jpg){.aligncenter .size-full}

The TMC2660C motor drivers are capable of 2800mA RMS and should allow for faster speeds than the previous LongBoard's TB6600 drivers due to their higher efficiency which also means the machine runs quieter. Though they can all run independently (allowing Y-axis auto-squaring in the future), the two Y-axes are currently running ‘mirrored’.

#### Movement & Cutting Speeds

The default movement speed of the SLB has been set up to work out-of-the-box for a LongMill CNC with typical tuning on an average setup. Based on your setup you may be able to adjust your Maximum Speeds for X, Y, and Z ($110-112) to be higher than their defaults of 5500mm/min, or you might have to lower them if those speeds are losing steps for you. You can also do this to the Acceleration ($120-122) of each axis from its default of 1000mm/s2 for XY and 750mm/s2 for Z.

To check if your machine is able to handle the default speeds, manually set the jogging ‘Speed’ value in your g-code sender to the maximum default speed and then make long jog movements over the full cutting area for your CNC to see if you encounter any snags. If you snag once you’re up to speed then consider decreasing the speed, whereas if you snag at the start then consider decreasing the acceleration of the specific axis. Alternatively if it seems like your machine handles all movement just fine then also feel free to experiment by increasing the default values to be higher:

- We tend to put more weight on increasing acceleration over speed since the majority of CNC projects consist of small movements where acceleration has a larger impact on carve time, such as 3D carves or v-carving
- Sometimes faster speeds can also be useful though for making lots of long cuts or moving between locations or jogging
- Be mindful that sometimes faster speeds won’t actually make projects run faster since you might be limited by the speed you can realistically cut through the material
- For a well-tuned LongMill which is lead screw driven on Delrin nuts and v-wheels, we’ve been able to reach XY speeds of 7500mm/min with the default acceleration, or if acceleration is reduced to 200mm/s2 then we’ve tested to go past 12000mm/min. This can show the give-and-take relationship between velocity and acceleration when tuning these settings for yourself.

**Two notes:** Firstly you might be worried that the faster speeds and acceleration might cause faster wear of your CNCs motion system and although this is partially true, these higher speeds won’t typically be reached during cutting which is the majority of the time that your CNC moves so it shouldn't cause much added stress to machine life. Secondly, if your CNC was set up with homing and you’ve tuned its movement speeds after the fact, be sure to re-check your homing offsets if you’re using jigs since motor acceleration can change where your machine homes to.

#### Microsteps & Movement Tuning

The default configuration for the SLB is **32nd microstepping** ($150-153). This might seem to go against common internet wisdom and even past articles we've posted where CNCs don't tend to go past 8th microstepping in order to maintain more motor torque, but new drivers like the SLBs TMC2660Cs are able to account for this. The more precise microstepping signalling on these drivers means that they're able to maintain similar torque no matter the microstep settings, they're even set up so that coarser microsteps are still interpolated after-the-fact to make the steps less jarring and reduce resonance. In our testing we found that 32nd worked just as well as 8th, while providing more benefit of reduced motor noise and improved accuracy, but of course at the end of the day you should do what you think would be best for your CNC setup.

Once you've got your steppers plugged in and decided on your microstepping, you should test that your machine moves by the distance you instruct. For instance, jogging 100mm should be able to be measured out to be 100mm travelled with a ruler or measuring tape. You can use the firmware settings of $100-103 to adjust the accuracy of your movements, but if you've never tuned your movements before then the easiest way to do it is to use <a href="https://resources.sienci.com/view/gs-additional-features/#movement-tuning">gSenders built-in Movement Tuning tool</a>.

#### Independent Motor Holding

Instead of the old solution of setting $1=255 which forces all motors to hold at full current, two new settings allow you to select individual motors that you want to hold, and what holding strength you want to use. With 'Steppers deenergize' ($37), simply toggle the axis you want to hold while using 'Hold current' ($210-212) to decide what the holding strength will be (as a % of the motor’s full current).

Useful in cases of:

- Heavy spindle that can lower the Z-axis over time
- Vertically set up CNC
- Stop your motors from losing position in cases where you do manual tool changing

We’ve found that a minimum of 15% works for lead screw-driven CNCs. These hold current settings will also apply even if $37 is off when the machine is cutting but that axis isn’t moving. Note that these settings won’t work for an A-axis since that would typically be done using the DIP switches on the external motor driver.

[tabby title="Current" open="yes"]

![](/_images/_superlongboard/_manual/slb_ma_p19_Steppers-newu.jpg){.aligncenter .size-full}

[tabby title="Classic gSender"]

![](/_images/_superlongboard/_manual/slb_ma_p19_Steppers.jpg){.aligncenter .size-full}

[tabbyending]

Note that since the Y1 and Y2 outputs share the same enable pin, they cannot be held independently even if they're assigned to different axes.

### Touch Plate/Probe

Connect your touch plate or probe here. Any Sienci touch plate and many 3rd-party continuity-style touch plates should work and can be configured through gSender. For most touch plates, it doesn’t matter which way you plug them in.

If your touch plate has a third pin for power, consider wiring it to the <a href="#tls">TLS input at the back of the board</a> instead just to make hookup easier. If you plan to use both the TLS and a 3-pin touch plate, then you can pick up 24V from the E-stop plug or 5V from the Ring LED plug. VCC from the AUX Limit Switch Plus is also typically available.

![](/_images/_superlongboard/_manual/slb_ma_p20_EstopPlug.jpg "Touch plate cable goes in the front, above the E-stop cables"){.aligncenter .size-full}

If you want to check continuity, tapping the touch plate and magnet together should turn on the yellow ‘PRB’ LED near the touch plate connector. For a NC probe this behaviour will be inverted.

![](/_images/_superlongboard/_manual/slb_ma_p21_GIF.gif){.aligncenter .size-full}

You should find that probing with the SLB is faster due to its 32-bit processor, speeding up cycle times for zeroing and tool changing. You might also find that the touches are so much more sensitive that you don’t need to hold the touch plate in place anymore. Otherwise, all other aspects of probing should follow what you're familiar with.

If you go to probe and find that there’s a touch being detected when there shouldn’t be, either the probe or the TLS signal needs to be inverted. Try combinations of toggling the $6 and $668 EEPROM values to the opposite of what’s currently set then check again. For other reading on touch plate setup, see our MK2 resources here: <a href="https://resources.sienci.com/view/lmk2-touch-plate/">https://resources.sienci.com/view/lmk2-touch-plate/</a>

### Status Lights

A new and simple way to know your CNC status at a glance or from a distance. The RGB light on the board is visible from most angles and shines through the clear cover but you can also hook up more if you want to light up your machine, enclosure, or surrounding work area.

- ⬜ **White**: CNC is Idle, flashing white means a job has completed
- 🟩 **Green**: Jogging or Running a Job
- 🟨 **Yellow**: Paused or the Door is open
- 🟥 **Red**: E-stop is pressed or an Alarm occurred
- 🟦 **Blue**: Homing or Verifying a job (check state)

<p style="text-align: center;"><em><b>Note:</b> if you ever see the light change from green to white during a job, this is normal and can happen during G4 dwells or when changing spindle speeds.</em></p>

![](/_images/_superlongboard/_manual/slb_ma_p22_Status.jpg){.aligncenter .size-full}

There are also plenty of other status lights on the board for the purpose of troubleshooting, <a href="https://resources.sienci.com/view/slb-troubleshooting/#troubleshooting-lights">GO HERE</a> to see what they all do.

#### LED Strips

If you want to have **RGB LEDs** lighting up your CNC, you can connect up to 2 separate strips:

- A shorter strip of up to **40 LEDs**, powered by the SLB
- A longer strip of up to **60 LEDs** that needs to be powered by a separate power supply (you'll need to provide one)

On the SLB, the plug for the shorter strip is called "**Ring**" since you'd typically mount it near your router/spindle to light up the cutting area, while the longer one is called "**Rail**" since it's a good length to mount under an X or Y-axis rail for more ambient lighting; but realistically you can use both strips however you want. If you want to hook these up, make sure you **buy the right strips**:

- Try to buy just the LED strip, no remote or other circuitry
- It have 3 or 5 wires (not 4) and be marked as "5V" (not 12 or 24 volts)
- If they're 5V, the LEDs will likely be called "NeoPixels" or "WS2812" in the name or description, check this is true
- Some we've tested:
  - BTF-LIGHTING (1m/3.3' strip, 60 LEDs)
  - <a href="https://www.amazon.ca/gp/product/B08DKPYZ7L/" target="_blank" rel="noopener">airgoo NEON</a> (two 16" strips, 42 LEDs)
  - <a href="https://www.amazon.ca/gp/product/B0BYD9ZDRM/" target="_blank" rel="noopener">Geekstory ring light</a> (78mm ID, 35 LEDs)
- If you don't want different colours and **just want your LEDs to turn on and off**, consider using the SLBs <a href="https://resources.sienci.com/view/slb-manual/#switch-amp-aux-power">AUX Power outputs</a>
- **Tip:** if you want your **Rail** LED strip to be longer, try to find one with the LEDs spaced further apart

Typically, LED strips will be wired in the same pattern as the SLB: power, signal, ground (left-to-right) - but with the wrong connector. The plug is a standard ‘**JST XH 2.54 3-Pin Female Connector**’ which should be very common to find, where you can either <a href="https://www.amazon.ca/dp/product/B09JNZMBY4" target="_blank" rel="noopener">buy the pre-crimped connector</a> and solder it to the LED strip, or cut off the incorrect connector and <a href="https://www.amazon.ca/dp/product/B0BTGXNGNN" target="_blank" rel="noopener">crimp on a new one</a>.

![](/_images/_superlongboard/_manual/slb_ma_p23_RingStrip.jpg){.aligncenter .size-full}

The bottom “**Rail**” plug extends from the on-board light to run a much longer LED strip using an external 5V, max 3A power supply (denoted **LED PWR**). You could mount this strip under your CNCs X or Y-axis rails or use multiple strips to light up your whole enclosure.

![](/_images/_superlongboard/_manual/slb_ma_p24b-rail-led.jpg){.aligncenter .size-full}

Once you're done wiring up, update the $664 (ring) or $665 (rail) firmware settings for the number of LEDs you've plugged in and power-cycle the board for the changes to take effect. Look at the new pizazz! A member of our community, Jim, also made his own LED write-up if you'd like to check that out too: <a href="https://resources.sienci.com/wp-content/uploads/2024/04/Jims-SLB-Rail-LED-Guide.pdf" target="_blank" rel="noopener">Jim's SLB Rail LED Guide (PDF)</a>

#### Manual Control

The lights will automatically change colour based on the CNC’s status by default, but if you want to change that you can use the M356 command in the console to make either output stay white (to illuminate your cutting area all the time), turn off, or go back to Auto switching. An example would be using “M356 P1 Q1” to make the ring light stay white. The remaining combinations are shown below:

[su_table responsive="yes" fixed="yes"]
<table>
<tbody>
<tr>
<td></td>
<td><b>Rail</b></td>
<td><b>Ring</b></td>
</tr>
<tr>
<td><b>Auto</b></td>
<td>M356 P<b>0</b> Q<b>0</b></td>
<td>M356 P<b>1</b> Q<b>0</b></td>
</tr>
<tr>
<td><b>White</b></td>
<td>M356 P<b>0</b> Q<b>1</b></td>
<td>M356 P<b>1</b> Q<b>1</b></td>
</tr>
<tr>
<td><b>Off</b></td>
<td>M356 P<b>0</b> Q<b>2</b></td>
<td>M356 P<b>1</b> Q<b>2</b></td>
</tr>
</tbody>
</table>
[/su_table]

### Homing & Limit Switches

Any common limit switch is supported on the SLB: **NC** (normally closed) and **NO** (normally open) mechanical switches, **NPN** Inductive sensors, and more. You can wire one-per-axis, or two-per-axis if you’d prefer to have your CNC set up with hard-stops at the min and max travel. Some switches will already be able to plug straight into the white, 4-pin JST connectors for each axis (<a href="https://sienci.com/product/inductive-sensor-kit-for-the-LongMill-mk2/" target="_blank" rel="noopener">like our inductive sensors</a>) - otherwise we’d recommend wiring to the green terminal connector (circled at the top of the picture).

Dual Y homing will be available in the future, but for now do **NOT** use the Y2 limit switch plug.

![](/_images/_superlongboard/_manual/slb_ma_p26_LimitBoard.jpg){.aligncenter .size-full}

If you’re looking for advice on how to ensure you have reliable sensing:

- Make sure the limit switches you’re using are precise and that they also stay consistent in different temperatures (the manufacturer should provide this information) otherwise the switch might activate 2mm away when you've got your shed heater on but 2.2mm away if you open the door
- Mechanical switches can usually be wired as either NC or NO. If you have the option to choose:
  - **NC** is safer since the wires always carry a signal back to the controller, so you can be confident your switches will work but if your wiring is loose then it can cause errors at unexpected times
  - **NO** has the opposite problem where if a wire is loose then you’ll only find out once the CNC rams into itself during homing or running a job; some people prefer this since it’s easier to recognize the switch/wire is bad in the moment, but it’s less safe and can cause damage to some CNCs
- Occasionally check your wiring by pulling or wiggling it to make sure nothing is loose - all switches share the same ground and VCC signals, plus individual limit signals, so a false trigger could ruin a job
- Using shielded cable can help dissipate electrical noise in the wires and prevent unexpected triggers

Using the big green connector is the same as using the smaller white JST connectors, they are connected to each other on the board so it doesn’t matter which one you use. The terminal pinouts are VCC, X, Y1, Y2, Z, A, GND going left to right, and the JSTs are VCC, GND, N/A, LIM going top to bottom. The most common custom setup is shown below (**NC switches or NPN sensors wired to the green connector**).

![](/_images/_superlongboard/_manual/slb_ma_p27_LSWiring.jpg){.aligncenter .size-full}

By default, VCC outputs 5V. If you want to wire for a different setup, see below for other wiring variations:

- NC (also already shown above), NC with hard-stops
- NO, NO with hard-stops
- NPN (already shown above), and NPN with hard-stops

![](/_images/_superlongboard/_manual/slb_ma_p28_NCNO.jpg){.aligncenter .size-full}

If you’d like to use the white JST connectors instead, the wiring pinouts are below for both mechanical switches and inductive sensors. All VCC outputs can also be changed from 5V to 24V if you'd like by breaking the 0Ω resistor on R9 and creating a solder bridge across R10 (outlined in red in the middle of the first homing picture).

![](/_images/_superlongboard/_manual/slb_ma_p29_WCPins.jpg){.aligncenter .size-full}

#### Limits Settings

If you’ve set up your own **NC sensors**, the first thing you’ll want to do is invert all the limit pins for $5 like shown below. **Don't do this if you have the inductive sensors from Sienci!**

[tabby title="Current" open="yes"]

![](/_images/_superlongboard/_manual/slb_ma_p30_InvertLP-newu.jpg){.aligncenter .size-full}

On top of the typical settings that the original LongBoard has when it comes to homing like homing speed and direction, the SLB brings along some new options that you can configure. If you'd like to match the SLB behaviour to the typical LongMill/grbl setup, then we'd recommend you enable all the settings shown in the picture (homing on startup, set machine origin to 0, and override locks), otherwise learn about all the settings in the table below.

![](/_images/_superlongboard/_manual/slb_ma_p31_HomingFirm-newu.jpg){.aligncenter .size-full}

[tabby title="Classic gSender"]

![](/_images/_superlongboard/_manual/slb_ma_p30_InvertLP.jpg){.aligncenter .size-full}

On top of the typical settings that the original LongBoard has when it comes to homing like homing speed and direction, the SLB brings along some new options that you can configure. If you'd like to match the SLB behaviour to the typical LongMill/grbl setup, then we'd recommend you enable all the settings shown in the picture (homing on startup, set machine origin to 0, and override locks), otherwise learn about all the settings in the table below.

![](/_images/_superlongboard/_manual/slb_ma_p31_HomingFirm.jpg){.aligncenter .size-full}

[tabbyending]

[su_table responsive="yes" fixed="yes"]
<table>
<tbody>
<tr>
<td><b>Setting</b></td>
<td><b>Description</b></td>
</tr>
<tr>
<td>Enable</td>
<td>Turns on homing</td>
</tr>
<tr>
<td>Enable single axis commands</td>
<td>Allows special homing commands so you can, for instance, re-home only your Z-axis without having to re-home the whole machine</td>
</tr>
<tr>
<td>Homing on startup required</td>
<td>Reminds you to home your machine every time you power it on, since CNCs typically lose their position when they lose power</td>
</tr>
<tr>
<td>Set machine origin to 0</td>
<td>Typically enabled so that re-homing re-zeros the machines location</td>
</tr>
<tr>
<td>Two switches share one input pin</td>
<td>Enable if you plan to set up hard limits at the end of each axis</td>
</tr>
<tr>
<td>Allow manual</td>
<td>If you want to home an axis that isn’t homed when you ‘Home all’</td>
</tr>
<tr>
<td>Override locks</td>
<td>In case you’ve turned on ‘Home on startup’ but want to skip it in certain cases</td>
</tr>
<tr>
<td>Keep homed status on reset</td>
<td>In a case where the machine is reset, it’ll try it’s best to maintain the machine position and not force you to re-home</td>
</tr>
</tbody>
</table>
[/su_table]

Some other new settings that have been introduced include:

- $21: expanded to introduce a “Strict mode” which you can turn on if you want the machine to be forced to home if a hard limit is triggered
- $40: added to stop soft limit alarms from appearing when jogging. This can only be turned on if you've turned on homing first

The SLB has much faster default homing speeds, so once you use homing if you hear a 'bang' when it approaches the sensors, don't be concerned since this is likely the LongMill just stopping really quickly. If you're setting up the SLB on a larger machine, you might want to reduce these homing speeds to not overshoot the sensors.

If you need any other refreshers on how to set up limit switches or troubleshoot them, see our MK2 resources here: <a href="https://resources.sienci.com/view/lmk2-limit-switches/">https://resources.sienci.com/view/lmk2-limit-switches/</a>. Remember that if you ever change homing settings like seek rate, locate rate, debounce delay, or pull-off distance, this will change the location your machine homes to so if you've set up any work offsets you'll need to adjust them accordingly.

### Laser

If you have a Laser diode accessory for your CNC connect it here. Use the top, third pin if your Laser driver needs an ‘Enable’ signal to operate, otherwise just use the bottom two to get the 5V PWM output that most laser accessories typically need. On the LongBoard this would’ve normally been the 2-pin SpinPWM plug, which you can plug straight into the SLB.

**Warning:** lasers are very dangerous devices that can instantly damage your vision and cause fires. Become knowledgeable on staying safe by reading documentation by your laser manufacturer, the SLB, how<a href="https://github.com/gnea/grbl/blob/master/doc/markdown/laser_mode.md"> laser mode in grbl</a> and grblHAL works, and how your g-code sender handles laser commands. Even then do not become complacent; continue to treat your laser with caution and respect and turn off power completely to the laser driver when you’re not using it. You can never be sure when the laser might fire unexpectedly and hobby equipment and software can be imperfect. If you have the driver turned on, everyone around should always be wearing eye protection and there should also be clear warning or signage to protect others.

![](/_images/_superlongboard/_manual/slb_ma_p32_Laser.jpg){.aligncenter .size-full}

When you mount your laser driver board and electronics, you’ll likely want to stick to whatever your manufacturer recommends. This will probably be in a more secluded spot away from dust and vibrations, since laser electronics tend to be more sensitive and require more air cooling.

More from us on laser wiring, safety, and use: <a href="https://resources.sienci.com/view/lmk2-adding-a-laser/">https://resources.sienci.com/view/lmk2-adding-a-laser/</a>

#### SLB Control

The way the laser is set up on the SLB is quite unique. Essentially when your g-code files have spindle commands in them (M3, M4, S##, M5), you have the ability to tell the SLB what output you want it to control with those commands:

- A basic spindle
- **The laser output**
- More advanced VFDs using the RS485 output

The laser isn’t set as the default for safety reasons, but further down is information on how to switch it to be the default if you tend to use the laser the most, or you can also just switch to it temporarily. Whichever is set as the default is what the board switches back to whenever the board is turned off and back on again, or loses power.

You can only control one at a time, so to select which one you’d like to control you can use the dropdown selector in gSender or use the selection commands. This selection will also apply when you send manual spindle commands in other ways like the console.

[tabby title="Current" open="yes"]

![](/_images/_superlongboard/_manual/slb_ma_p33_gSenderLaser-newu.jpg){.aligncenter .size-medium}

[tabby title="Classic gSender"]

![](/_images/_superlongboard/_manual/slb_ma_p33_gSenderLaser.png){.aligncenter .size-medium}

[tabbyending]

For other g-code senders, you’ll need to use the selection commands:

- By default, the SLBs spindle output is set up as the “Default spindle” ($395), with the Laser output as “Spindle 1” ($511) and the RS485 as “Spindle 3” ($513)
- Because the laser is set as “Spindle 1”, sending “M104Q1” will switch to controlling the laser
- Similarly, “M104Q3” will switch to RS485 output, and “M104Q0” will switch back to the spindle output
- If you ever want to check which output is currently being controlled in the console, you can send the “$spindles” command which will list all the options and which one is currently selected

Knowing all this, you can go into the EEPROM to change your selections for the Default Spindle, Spindle 1, 2, etc. to match how you tend to use your CNC. Then, you can use the dropdown in gSender or the g-code commands to switch outputs when you need to. Ensure that you only turn on ‘Laser Mode’ AFTER you switch over to the laser output, as well as turn off ‘Laser Mode’ BEFORE you switch back to any other output, otherwise you’ll see an error.

If you run into an issue where switching between outputs gets stuck, this can be fixed by power-cycling the board.

Here's a video that explains more about the setup and configuration process:

https://youtu.be/5r_P6eISrnc

#### Laser Configuration

The SLB is set up to work with the LaserBeam by default, so if you have another laser diode you might need to configure the default settings based on your manufacturer's specifications.

For all lasers, if you’re using gSender:

- $741 and 742 now allow the SLB to store the X and Y offset values from the spindle to the laser so that the offset can be applied when the laser output is selected

For other 3rd party lasers (remember to power-cycle the board for certain settings to take effect):

- $730 Maximum laser power = whatever max laser power your laser calls for
- $731 Minimum laser power = typically 0
- $733 Laser PWM frequency = can go to a theoretical max of 100kHz, check your diode manufacturer’s site to see if they specify a frequency range and try to set it to the higher-end of the range for best results
- $734 Laser PWM off value = typically 0%
- $735 Laser PWM min value = typically 0%
- $736 Laser PWM max value = typically 100%
- $743 Invert laser signals: typically Laser enable = off, Laser PWM = off

At this point, you should be able to use commands to power your laser on and off and vary its power. Optionally you should be able to use a multimeter to check that your PWM output can go between around 1V and 4.5V. If not, double check your wiring and settings again.

### Action Buttons

With the SLB you can set up three customizable buttons to help control your CNC however you prefer. These actions can be something simple like Starting or Pausing a cutting job, toggling a signal to an IOT relay, or even custom g-code for probing, or moving the cutting head backwards once you’ve finished a job. These buttons are available on the SLBs E-stop, but you can also digitally short the pins to ground through the E-stop connector if you want to do custom wiring.

![](/_images/_superlongboard/_manual/slb_ma_p9_EStopButts.jpg){.aligncenter .size-medium}

By default, the Action buttons have been set up so that 1 is **Resume**, 2 is **Pause**, and 3 is **Stop**. There is the full list of pre-made actions like this that you can choose from such as:

- **Resume** running g-code (uses cycle start ‘~’)
- **Pause** movement (uses hold ‘!’)
- **Parking Pause**
- **Stop** movement (uses halt ‘0x18’)
- Toggle on/off the **Spindle** while paused (similar to M3/M5, uses ‘0x9E’)
- Toggle on/off **Flood** (similar to M8/M9, uses ‘0xA0’)
- Toggle on/off **Mist** (similar to M7/M9, uses ‘0xA1’)

or you can run your own custom ‘macro’ g-code. Here are some examples of macros some users have set up (**Careful!** We can’t guarantee this g-code will work correctly for your setup or possibly break things so use at your own risk):

- Home all axes: **$h**
- Zero XYZ to current location: **G10 L20 P1 X0 Y0 Z0**
- Tweak Z-zero down 0.1mm: **G10 L20 P1 Z0.1**
- Park the CNC away from the job: **G91 G21 G0 X400 Y400**
- Return to the cutting area (XY0 point): **G90 G21 G0 X0 Y0**

The buttons are customized using the Config tab or Firmware section of either gSender or ioSender. Look for settings $450-452 to select one of the actions from the pre-made list, or select the first “Macro” option and type in your own g-code string to execute in settings $450-452.

#### Example Setup

Some find that it's nice to have "Goto XY0" and "move to back corner" macros programmed into the SLB buttons. Way easier to just hit the button at the end of a carve to move out of the way and then jump back to 0 when you’re ready to load the next piece. This example has Shop Vac control using an IOT Relay by pressing button 1, then button 2 brings the CNC to the previous zero point and button 3 moves it out of the way.

$450 Button 1 Action: **Flood Toggle**
$451 Button 2 Action: **Macro**
$452 Button 3 Action: **Macro**
$454 Button 2 Macro (Go to ZUP, X0 Y0): **G53 G21 G0 Z-1|G0 X0 Y0**
$455 Button 3 Macro (Go to ZUP, XY to the back right. Need to validate your travel limits): **G53 G21 G0 Z-1|G53 G21 G0 X805.000 Y850.000**

If you need help making your own custom macro, you can look at gSender’s ‘Console’ tab when you press different buttons to see what’s happening behind the scenes and get some inspiration. Each macro can hold up to 127 characters, can run multiple lines using ‘|’ for a line break, and runs any vanilla g-code but no math operations.

There are also a handful of more advanced pre-made actions such as:

- Toggle on/off Probe Connected
  - **Currently not used on SLB**. Implemented as a toggleable check for probe contact while in motion or performing other tasks, read more here: <a href="https://github.com/Expatria-Technologies/grblhal_probe_plugin" target="_blank" rel="noopener">https://github.com/Expatria-Technologies/grblhal_probe_plugin</a>
- Toggle on/off Optional Stops
  - When enabled, M1 commands act like pauses just like M0 commands
  - This helps test a file. If you insert M1 commands at certain checkpoints in your g-code, you can pause at those checkpoints while this is enabled, then disable ‘optional stops’ to then run the job as normal
- Toggle on/off ‘Single Block Mode’
  - This is a very safe way to test a file (usually you’d check just the start of the file) since this mode only runs one line of g-code at a time for each Cycle Start button press
  - Find more information about grbl commands here: <a href="https://github.com/gnea/grbl/blob/master/doc/markdown/commands.md" target="_blank" rel="noopener">https://github.com/gnea/grbl/blob/master/doc/markdown/commands.md</a>

### Accessory Outputs

This is where you can get fancy; levelling up your CNC by controlling more accessories to create your own custom setup. Control IOT relays, power relays or solenoids, switch on even more LED strips, and more! This takes the form of 5 plugs: Flood, Switch 1 and 2, and Auxiliary Power 1 and 2 (going left-to-right, ‘+’ then ‘-’). These are all 2-pin plugs that either output a voltage or can switch power through them like a low-power relay.

![](/_images/_superlongboard/_manual/slb_ma_p34_AccOut.jpg){.aligncenter .size-full}

#### Flood

If you’ve used a ‘Coolant’ output previously (our LongBoard had one), this 5V output still serves the same function. Simply turn the digital signal on or off using M8 and M9 commands, manually, in g-code using your post processor, or using your g-code sender’s start/end g-code code blocks.

This output is commonly used to automatically control a vacuum or router to turn on/off at the start/end of a job using an IOT Relay. It also can be used for any other purpose with any component that accepts a 5V 40mA digital signal.

Read more about setting up an IOT Relay here: <a href="https://resources.sienci.com/view/lmk2-automated-relay/">https://resources.sienci.com/view/lmk2-automated-relay/</a>

#### Switch & Aux Power

These outputs are offer built-in options for more unique control than just a simple digital signal:

- **Switch 1 and Switch 2 outputs** are like electrical switches that you can use to ‘switch on’ any external **1-24V circuits up to 1A**. This means you’ll need to provide an additional power supply separately to the circuit. Think of these like a mini version of a relay, known as a MOSFET.
![](/_images/_superlongboard/_manual/slb_ma_p35_S1S2.jpg){.aligncenter .size-full}
- **Auxiliary Power outputs 1 and 2** can be used to provide **24V** to any powered accessory like a relay, SSR, solenoid for a mister or ATC, or LED strip; up to **250mA** per plug. This can be more convenient for powering less power-hungry components since the power comes straight from the SLB. It also makes more sense if you plan to use an SSR to switch an air pump, dust collector motor, or spindle water cooling pump on and off.
![](/_images/_superlongboard/_manual/slb_ma_p36_AO12.jpg){.aligncenter .size-full}
**Note:** Be mindful that these 'turn on' by enabling current flow to the 'ground'. This means you can’t typically use them to drive logic, only to drive current components, and also that the 24V is always 'live'.

You can also customize what M commands will turn each of these outputs on and off in the SLBs firmware. The $456-459 settings give you 4 options to choose from (SWT1=$456, SWT2=$457, PWR1=$458, PWR2=$459):

1. **Spindle/Laser Enable (M3/M4):** turns the output on with M3 or M4, and off with M5
1. **Mist Enable (M7):** turns on/off with M7/M9
1. **Flood Enable (M8):** turns on/off with M8/M9
1. **M62-M65 Only:** always available as a backup to control each port with a unique M command:
   - Turn on/off with M62/63 (but wait in line before running)
   - Turn on/off immediately with M64/65
   - Use a 'P' command to choose the port to control (pictured below). For example "**M64 P1**" would turn on the SWT2 port immediately.
   ![](/_images/_superlongboard/_manual/slb_ma_p37_P0P3.jpg){.aligncenter .size-full}
   - Read more here: <a href="https://linuxcnc.org/docs/html/gcode/m-code.html#mcode:m62-m65" target="_blank" rel="noopener">https://linuxcnc.org/docs/html/gcode/m-code.html#mcode:m62-m65</a>

Similar to the ‘Flood’ output, you’ll now also be able to control ‘Switch’ and ‘AuxPwr’ outputs either manually, in g-code using your post processor, or using your g-code sender’s start/end g-code code blocks.

### Spindle/RS485

As mentioned in the <a href="#laser">Laser section</a> above, we designed the SLB for a wide range of CNCers, like those with both a VFD and laser diode accessory on their CNC. Our solution was a PWM laser output, PWM spindle output, and an output for Modbus over RS485 - allowing for control of up to 3 accessories without rewiring and with settings stored independently for each.

The Laser wiring is covered above. Both flavours of Spindle signals are there to give you the 2 most popular options for talking to VFDs. The simple signals tend to have easier setup with less fuss, meanwhile RS485 requires more work but provides better, two-way communication during cutting. Whichever option you choose, you’ll want to check that you're wired up correctly and have the right settings for both your SLB and VFD so they match up to each other.

If you opted for an out-of-the box experience by picking up a <a href="https://sienci.com/product/LongMill-spindle-and-dust-shoe-kit/" target="_blank" rel="noopener">Sienci Spindle which will soon be compatible for a wide range of CNC machines</a>, then you won’t need to reference any of the following docs since all the work is done for you.

**Note**: currently the SLB doesn’t support SaS (‘Spindle-at-Speed’, a signal that some VFDs can send back to the board so that the board can wait for the spindle to speed up before starting the cutting process).

![](/_images/_superlongboard/_manual/slb_ma_p38_RS485.jpg){.aligncenter .size-full}

#### Safety and AC Wiring

Before diving into spindle hookup, it’s important to mention a couple things for your safety:

1. Though we’ve tried our best to provide guidance on spindle hookup, there are many spindle kits out there with mix-and-matched VFDs - we’ve even seen cases of VFDs being mislabelled as the **wrong model**. Because of this, none of the below spindle instructions can be given with any guarantee or warranty of any kind, you must **accept the risk** since we will not be liable for your safety, injury, or damages as a result of these instructions.
1. If you buy from a **trusted vendor**, then specs and hookup instructions should always be more straightforward, but if instead you buy from a **cheaper vendor** then expect to have to go through more trial-and-error.
1. Related to that, cheaper kits also typically require you to do mains wiring manually. PLEASE BE CAREFUL AROUND AC WIRING, and please use best practices throughout the process.
1. Lastly, once you’ve completed the process of hooking up your spindle to the SLB, understand that there can now be cases where the spindle **could turn on or off without you expecting it**. Examples of this could be when resetting the board, leaning on your keyboard, mouse, or Action Buttons, running unknown g-code, running a macro, and more. Please understand this and use caution, since you can be hurt or cause damage if the spindle changes to be on/off when you don’t expect it to.

If you have any inquiries or questions, please direct them to the **manufacturer of your spindle or VFD** or **check the manual**.

<b>Initial checks:</b>

1. Ensure mains power is connected to your spindle VFD with appropriate wire gauge (recommended #14 to #12, rating should be printed on cable). The VFD should have 3 input terminals (R, S, T or L,N) and a Ground/Earth hookup (indicated by a ground symbol, metal plate, and sometimes red wax on the screw) where for 110V Hot (black) is connected to R or L, Neutral (white) to S or N, and Ground (green or yellow+green) to Ground. If you have 220v, the second Hot goes to T.
1. The wire from the VFD to the spindle should be well-shielded to help reduce issues with EMI. Typically the VFD will have 3 output terminals (U, V, W) that connect to pins 1, 2, and 3 respectively on the spindle. The 4th pin should be grounded to the spindle body, through to the VFD ground, or you can run your own separate wire if you’d like.
![](/_images/_superlongboard/_manual/slb_ma_p39_VFDWire.jpg){.aligncenter .size-medium}

1. **If your spindle came pre-wired, you can likely skip to this step.** You’ll want to make sure the spindle and VFD work exactly as expected when controlled manually using the panel on the VFD. This includes: start, stop, forward, reverse, and controlling speed. ‘Forwards’ should make the spindle turn clockwise when looking at it from above, if this isn’t the case then swap the U and V wires on the VFD.
![](/_images/_superlongboard/_manual/slb_ma_p40_SpindleDir.jpg){.aligncenter .size-full}

#### VFD Settings

If you purchased a VFD that wasn’t pre-programmed from the manufacturer for your specific setup, then you’ll likely need to double-check some settings using your VFDs built-in keypad. Most VFDs share 5 similar buttons where you’ll press:

1. **PRGM**/**SET**/**PROG** to enter into the settings menu
1. Use the **UP** and **DOWN** arrows to cycle digits from 0-9 and use **SHIFT**/**←** to move left to edit higher digits
   - Use this to go to the setting you’d like to check
   - Example: if you start with “000” and you want to get to setting “023” then you’ll start with the right digit highlighted (00<u>0</u>), press UP 3 times (00<u>3</u>), then SHIFT to get to the next row (0<u>0</u>3), then press up twice more (0<u>2</u>3).
1. Press **SET**/**DATA** to open up the setting
1. Use the same UP and DOWN and SHIFT/← buttons if you want to change the setting value
1. Press **SET**/**DATA** if you’d like to save the new value, or press **PRGM**/**ESC**/**PROG** to leave without saving
1. You can go back to the setting to check that it’s been set correctly if you’re rusty on changing settings

Before starting, you should also reset your VFD to factory settings. That makes sure you’re not pulling your hair out if it had some settings changed in the past:

1. Find the “Parameter Reset” setting, in common VFDs it’ll be ‘**013**’
1. Set the value to ‘**8**’, telling the VFD to reset all settings
1. Power off the VFD by waiting for the **display to turn off**
1. Power it back on, and compare a few settings against the manual to check that it reset properly

Otherwise, below are some example setups you can reference. Setting numbers can be different between VFDs so pay attention to the values and compare them to your own VFDs manual. The wrong setting can damage your VFD or spindle so make sure to take your time and keep track of what settings you are changing.

**Huanyang v1 VFD set up as “Spindle 1” on the SLB (the secondary option) over RS485:**

- On the VFD interface:
  - PD001= **2** (RS485 control)
  - PD002= **2** (RS485 control)
  - PD163= **2** (communication address)
  - PD164= **2** (baud rate of 19200 b/s)
  - PD165= **3** (communication data method of 8n1 RTU)
  - All these settings are based on the manual <a href="https://bulkman3d.com/wp-content/uploads/2019/01/HY01D523B-VFD-Manual.pdf">https://bulkman3d.com/wp-content/uploads/2019/01/HY01D523B-VFD-Manual.pdf</a>
- Then in the SLB settings:
  - $511= **Huanyang v1** (once set, power-cycle the SLB)
  - $477= **2** (this matches the communication address of the VFD)

#### RS485 Hookup

For RS485, you can use EITHER the 4-pin connector with B, A, 5V, and GND (left-to-right) or the RJ “phone jack” plug if you have one on hand or your VFD has a matching input plug. For most VFDs, all you’ll have to do is connect A to RS+ and B to RS- from the SLB to your VFD. If your wires need to be long, consider using twisted wiring for the A/B cable for added EMI resilience.

![](/_images/_superlongboard/_manual/slb_ma_p41_PlugsVFD-2.jpg){.aligncenter .size-full}

**Note:** if the VFD has a jumper to swap from controlling the spindle with the panel to using the wire signals, change this over. In the example below it’s the left 2 pins and called “VI”. Also, make sure your RJ cable has 6 positions or "6P" so it's compatible to plug in. The RJ standard is a bit confusing and plugs that fall under RJ11, 12, 14, and 25 all seem to be compatible for hookup.

#### 5V PWM Hookup

For the simple signals, use the 5-pin connector with GND, PWM, direction control, enable signal, and SaS (left-to-right, all 5V) and look for matching labels on your VFD like ‘PWM’ / ‘VI’, and ‘GND’ / ‘ACM’. If you plan to never run the spindle in reverse for tapping and reverse cutting, you can also make your life easier by wiring the VFDs ‘FOR’ pin to ‘DCM’ so the spindle always runs forwards when it’s turned on.

Some VFDs don’t accept 5V PWM, in which case you can either try setting up RS485 or you can pick up a ‘PWM to 0-10V Analog signal converter’ and use that to translate the 5V PWM the SLB has to the ‘0-10V’ your VFD needs.

**Note:** if the VFD has a jumper to swap from controlling the spindle with the panel to using the wire signals, change this over. In the example below it’s the left 2 pins and called “VI”.

![](/_images/_superlongboard/_manual/slb_ma_p42_TermPlug.jpg){.aligncenter .size-full}

#### SLB Spindle Settings

The typical settings if you want the simple signals as default will include:

- $9 PWM Signal: Enable = on, RPM controls spindle enable signal = off
- $16 Invert spindle signals: Spindle enable=on, Spindle direction = on, PWM = on
- $30 Maximum spindle speed = 24000 RPM
- $31 Minimum spindle speed = 7500 RPM
- $32 Mode of operation = Normal
- $33 Spindle PWM frequency = 1000 Hz
- $34 Spindle PWM off value = 0%
- $35 Spindle PWM min value = 0%
- $36 Spindle PWM max value = 100%
- $395 Default spindle: SLB_SPINDLE
- $520 Spindle 0 tool number start = 0
- $666 Using Add-ons not used yet

Verify these, then power-cycle your board to make sure the changes take effect. If you’re rather wanting to set up RS485 as default, then you’ll want to change $395 to one of the other options.

- The list of already supported VFDs is the Huanyang v1, Huanyang P2A, Yalang YL620, H-100, and GS20 as noted in <a href="https://github.com/grblHAL/Plugins_spindle/tree/master/vfd" target="_blank" rel="noopener">https://github.com/grblHAL/Plugins_spindle/tree/master/vfd</a>. That doesn’t mean selecting these is guaranteed to work, rather that they tend to work for those generic models.
- If your VFD isn’t listed or the other defaults aren’t working for you, you can select “MODVFD” to setup your own custom RS485 settings. Disconnect and reconnect in gSender to see these new settings. They’ll span $462-481 and include registers, command words, addresses, all values that you’ll have to consult your VFD manual for.
Remember that your VFD will also require some setup through its own button interface or sometimes require jumpers to be placed correctly
- Remember you can set up more than one option, for example you can leave the Laser as your default ($395), set the simple Spindle as your second option ($511), then RS485 as your third ($512)
- In Step 4 of the <a href="#laser">Laser section</a>, it explains the process of switching between output options
- For more info, the letters next to each spindle in the dropdown indicates its abilities:
  - **V**: Variable Spindle speed supported
  - **D**: Spindle Direction (M4) supported
  - **S**: Spindle at speed feedback supported
  - **L**: Spindle can control a laser (requires laser mode to be enabled in firmware)
  - **I**: Spindle PWM output can be inverted
  - **R**: Range Locked (min/max not inherited from Config/firmware settings)
  - So for example, “DIV” means you can swap spindle direction, invert output, and have variable speed on that specific spindle.
  - Also, the list of spindles has a fixed order just for easy reference, otherwise the order they appear in has no other meaning

Find more information for VFD setup at <a href="https://wiki.printnc.info/en/electronics/vfd/config" target="_blank" rel="noopener">https://wiki.printnc.info/en/electronics/vfd/config</a> or <a href="https://github.com/grblHAL/Plugins_spindle/blob/master/vfd/" target="_blank" rel="noopener">https://github.com/grblHAL/Plugins_spindle/blob/master/vfd/</a>

<b>Other Uses</b>

Modbus over RS485 is also a much more ubiquitous communication protocol used in many industries for reliable and EMI resilient communication between modules. There are likely instances of boards that support 0-10V, pumps, relays, and more which can all be controlled over RS485 - go out and explore!

### TLS

Short for “Tool Length Sensor”, this is a very common accessory for slightly more fancy CNC routers. Mounted somewhere the CNC can reach, they’re used as a reliable place to go to re-zero the Z-axis on jobs that require multiple tools/ tool changes. This is also handy when your original Z zero is lost because the material is cut away, a perk over a standard Touch Plate. TLSs are typically NC (normally closed) switches so that if the wire gets cut the machine doesn’t crash into the sensor. The TLS output on the SLB also provides 5V power for powered TLSs, the wire order being power, signal, gnd (top-to-bottom).

![](/_images/_superlongboard/_manual/slb_ma_p43_TLSBoard.jpg){.aligncenter .size-full}

If your TLS is wired correctly, you should be able to press it and see the “PRB” status light toggle on or off on the SLB (either is fine, on is NO, off is NC). If you’re unsure with your wiring or your TLS has more than 3 wires, you can use a multimeter and check any two wires until you find a set that contact/open when pressed and those will be the ones you use for the signal and gnd; the third might be power. If you have 4 wires your TLS might have 2 switches, one that triggers when pressed down just a bit then the next one pressed in case of over travel. This would typically trigger an E-stop or Pause but you only really have to use the one that triggers first.

With wiring done, check in your g-code sender if the TLS signal is set up correctly. This signal is shared with the touch plate, so activating either of them should be recognized. gSender has a status light to help see this in the 'Calibrate' tab and in other senders it should appear as 'P' for probe. If the light in the sender turns on when the TLS is pushed, and also turns on when the probe circuit is connected, then the hardware (SLB and wiring) is working and that means the $ values have been set up correctly. If the signal is on and only turns off when the TLS is pressed, then go to the $668 firmware setting and toggle it to the opposite of what it was set to.

[tabby title="Current" open="yes"]

![](/_images/_superlongboard/_manual/slb_ma_p44_tls-input-newu.jpg){.aligncenter .size-full}

[tabby title="Classic gSender"]

![](/_images/_superlongboard/_manual/slb_ma_p44_tls-input.png){.aligncenter .size-full}

[tabbyending]

This flip is usually needed since the SLB defaults to expect NO inputs. Once this all seems to be working, see more documentation here on how to set up tool changing for your SLB (<a href="https://resources.sienci.com/view/gs-additional-features/#tool-changing" target="_blank" rel="noopener">gSender tool changing feature</a>) and make sure you select the 'Fixed tool sensor' option.

### Rotary Axis

The SLB will still support anyone who already has a ‘switching’ rotary axis setup, like the <a href="https://sienci.com/product/vortex-rotary-axis/" target="_blank" rel="noopener">A/Y Switch we launched our Vortex Rotary Axis with</a>, in the same way that older grbl boards do. We wanted to preserve this functionality for easier backward-compatibility with older setups, plus making the switch to full <a href="#4tha-axis">4-axis</a> cutting has the extra cost of an external driver and some wiring despite some of the benefits that it offers.

The main improvements to how SLB handles rotary switching is:

- The A-axis values for steps/deg, maximum speed, and acceleration ($103, 113, and 123) are now stored directly on the SLB instead of relying on gSender settings
- This will help maintain correct values across computers, since every time gSender is switched into Rotary mode it can just swap the A-axis values and the Y-axis values, then swap them back once you leave rotary mode
- Hard and soft limits can now be left on while in rotary mode
- This is new from grblHAL, where when the maximum travel of any axis is set to 0, it’s able to rotate infinitely while leaving hard and soft limits on for all other axes

For anyone who isn’t already familiar, ‘rotary switch’ setups were created so that people with typical 3-axis CNCs (X, Y, Z), could move on to more advanced rotary carving (X, Z, A) by swapping or mechanically switching Y-axis movements and limit switches over to an A-axis since typical grbl boards can’t run more than 3 axes at a time. This setup also has some other requirements:

- A g-code sender that can convert and display rotary axis files, and ideally store and swap grbl settings between the Y and A-axes (gSender accomplishes this)
- A CNC that’s set up to hold itself in place in the Y-axis while cutting with the A-axis, either using clamps or in the case of the LongMill it relies on the friction and mechanical advantage in its lead screws

You can read more about how this control works and our approach here: <a href="https://resources.sienci.com/view/vx-first-project/">https://resources.sienci.com/view/vx-first-project/</a>

#### Troubleshoot Rotary

- **Error during homing:** make sure each individual limit switch is triggering by looking at the SLB lights or gSenders Calibrate ➜ Diagnostics tool.  If still getting an error, check that you haven't turned on the A-axis for any homing passes ($44-47) since the Rotary uses the Y-axis signals for homing and not the A-axis.
- **Not moving the right amount:** the amount your rotary spins will be based on the value set for the A-axis step/deg. For 8th microstepping use "19.75308642", for 32nd use "79.01234568", and for other values or if you have a custom setup, read more on <a href="https://resources.sienci.com/view/vx-using-other-cnc-routers/#firmware">how to determine the correct value here</a>.

### 4th/A-axis

The SLB is able to support an extra fourth, fully independent cutting axis too. This rotary “A-axis” is set up to run along the width (X-axis) of your CNC and has some advantages over a typical ‘rotary switch’ setup:

- The Y-axis motors can stay powered while cutting, meaning they can hold their position for more accurate cutting and not rely on lead screw friction clamping the CNCs Y-axis
- There’s no ‘changeover’ process which saves you time and mistakes since you don’t need to swap back to realign the rotary, or bother with toggling switches or changing settings
- If you’re ready to dive in, you can generate much more complex and efficient cuts using all 4 axes of movement and creating even more impressive projects

If you set one of these up yourself, you can either check out our [Vortex rotary axis with a pre-made wiring loom and closed-loop NEMA 23 with a built-in driver](https://sienci.com/product/vortex-rotary-axis/) that you can use for your own rotary setup or upgrade your existing open-loop Vortex, or you should pick up your own independant motor driver. Most motor drivers on the market will do like a **DM542** or **TB6600** but use your best judgement and be mindful of who you buy from.

The main downside of this setup though is that most hobby CAM software is yet to catch up to the hardware and support 4-axis toolpaths. This means that you'll either still use it for 3-axis cutting (alongside some of the benefits mentioned above) or you'll have to get creative in finding a solution that works for you by manually modifying code, using indexing, or paying for a more expensive CAM software. We've currently only tried [Snapmaker’s Luban software](#tips-for-luban-a-axis-cam), though we’ll update this section once we have more to recommend.

#### Driver Wiring

![](/_images/_superlongboard/_manual/slb_ma_p45_4thAxis.jpg){.aligncenter .size-full}

This takes the form of two independent plugs labelled for an “A-axis”, where you can plug in your:

1. Motor driver to the drivers signals on the SLB (black plug)
2. A-axis limit switch (white plug), and
3. Additional power supply to your motor driver

Any motor driver that can be driven by Step/Dir common-cathode arranged signals will work as long as it's rated for the stepper motor you’re planning to use. The black connector is a "Female IDC Flat Ribbon Cable Connector, 8 pins, 2 Row, 2.54mm Pitch", but you can also use any 2.54mm spaced connector cables. Also if your limit switch doesn’t have a JST connector, you use the terminal connector ‘Limits’ A-axis output.

- <a href="https://www.digikey.ca/en/products/detail/adam-tech/FCS-08-SG/9832361" target="_blank" rel="noopener">https://www.digikey.ca/en/products/detail/adam-tech/FCS-08-SG/9832361</a>
- <a href="https://www.amazon.ca/Elegoo-120pcs-Multicolored-Breadboard-arduino/dp/B01EV70C78/" target="_blank" rel="noopener">https://www.amazon.ca/Elegoo-120pcs-Multicolored-Breadboard-arduino/dp/B01EV70C78/</a>

Below we’ve illustrated two examples that you can use to better understand how to create your own setup. One shows the TB6600 driver and uses the IDC connector with all the available connections running to the SLB. The other has the DM542 driver hooked up with single-wires and bridging between the ground pins. Either hookup method is fine no matter the driver, just note that different drivers will have their outputs in different orders. The drivers will also require you to use an appropriate power supply, manually configure the DIP switches for current or holding current, as well as set the microstepping (most times we’d recommend 1/8th).

- D+ goes to DIR+
- S+ goes to STEP+ or PUL+
- 5V goes to EN+ or ENA+
- GD goes to the Driver ground pins like DIR-, PUL-, etc.
- AL- likely won’t be supported by your driver, but is an active-low alarm signal for the motor driver to tell the board if something has gone wrong similar to the E-stop

![](/_images/_superlongboard/_manual/slb_ma_p46_TB6600.jpg){.aligncenter .size-full}

![](/_images/_superlongboard/_manual/slb_ma_p47_DM542.jpg){.aligncenter .size-full}

Once the wiring is complete, in your g-code sender check that the rotary is moving at the speed, distance, and direction you’d expect and that the limit switch is working if you have one. If there’s anything wrong you’ll want to check your typical A-axis settings for **movement** ($2, 3, 4, 37, 103, 113, 123, 133, and 376) and for **homing/limits** ($5, 18, 23, 44, 45, and 46). Note that some settings like $143, 153, 183, 193, 203, 213, 223, 338, 339 won’t have any effect on your setup since the 4th axis is an external stepper motor driver.

If you're experiencing movement precision problems, check the 2nd point in the <a href="#troubleshoot-rotary">Troubleshoot Rotary section</a>. Also check that you turn on "**Steppers deenergize**" for the A-axis, since most closed-loop motors need constant power to them to make sure that they make accurate movements.

#### Cut & Experiment

If you’re happy that your rotary is turning successfully, feel free to try out some sample 4th axis files we made to test how your setup is working. Some things to keep in mind to carve these sample files successfully:

- They both use an 1/8" tapered ball nose, cut out of wood 1" diameter, with minimum 40mm long
- Make sure that A-axis direction is set correctly so that Positive A has the cylinder turning towards you
- Since there’s no roughing pass, use the speed override to start off the file slowly (10-30%) during the initial plunge so you don’t accidentally break the bit, once the plunge is done you can turn the speed back up for the rest of the job
- Small Lion Statue: <a href="https://drive.google.com/file/d/1I15FD8WIJoty8UhpEh17H04MH2VqPr3M/" target="_blank" rel="noopener">https://drive.google.com/file/d/1I15FD8WIJoty8UhpEh17H04MH2VqPr3M/</a>
- Knight Chess Piece: <a href="https://drive.google.com/file/d/156eTQ1c2pt6jm9ehI4Adu6OitGL33CJs/" target="_blank" rel="noopener">https://drive.google.com/file/d/156eTQ1c2pt6jm9ehI4Adu6OitGL33CJs/</a>

If you’re ever running into a situation where clicking “Zero A” in gSender sets the value to 0.01 or 0.02 instead of zero, this is a known bug with grbl and grblHAL where the location doesn’t get reported back from the machine correctly, but the location is definitely being set to zero. This can be a little stressful to see but unfortunately we don’t have the ability to fix it ourselves.

#### Tips for Luban A-axis CAM

Download it here: <https://www.snapmaker.com/en-US/snapmaker-luban>

- Select “link” as the carve option inside Luban, otherwise you’ll just get 3-axis movements
- Remember to define the shape of your tool
- After you export the code, open it in a text editor to:
  - Remove the default header since it contains some Snapmaker-specific M-codes that grbl doesn’t support
  - Check the first Z-movement to make sure there are no unexpected plunges
  - Do a find and replace to change X into Y; then Y➜X; then B➜A. The rotary on the Snapmaker machine is lined up along the Y-axis, so you need to switch it to be along the X-axis.

## Enclosure Mounting

You can mount your SLB however you like. Some factors to consider might be your machine setup, computer location, if you have an enclosure, or if you want to access other things or see the pretty lights on the board. The most versatile way is the 4 holes in the SLBs enclosure which will allow you to mount it to any flat surface, but if you have a LongMill MK2 you also have the option to mount it directly to your Y-axis rail (not compatible with MK1).

Some of the extra tools you'll need:

- **Bolting to MK2 Rail** - M5 Allen wrench, plus grab the hardware and bracket provided with the SLB
- **Screw Down / Flat Mounting** - 2 to 4 wood screws (minimum size #4 or ¾” and min length of ½”) plus the necessary screwdriver or bit driver

### Bolt to Rail

For rail mounting, slide the two T-nuts onto the track above the left Y-rail and loosely thread on the two M5 bolts. You may need to remove your limit switch on MK2’s temporarily to enable the nuts to be slid into the rail.

![](/_images/_superlongboard/_manual/slb_ma_p48_Mount1.png){.aligncenter .size-medium}

Insert the sheet metal bracket into the slot at the back of the SLB enclosure. The bracket will feel loose for now so you’ll want to hold it in place until the next step.

![](/_images/_superlongboard/_manual/slb_ma_p49_Mount2.png){.aligncenter .size-medium}

Place the bracket-enclosure assembly onto the Y-rail and slide the two screws into the slots in the bracket, then tighten the two screws with an Allen key to lock the entire assembly onto the rail.

![](/_images/_superlongboard/_manual/slb_ma_p50_Mount3.jpg){.aligncenter .size-medium}

### Screw Down

You can mount your SLB flat on your wasteboard next to your machine, or even on the side or at the back of your workstation. You can also hang the SLB vertically. The enclosure has been designed with reasonable consideration for dust penetration and vibration, but if you are a more cautious person you can feel free to mount the box further away from your CNC.

When placing your SLB on its own or among other CNC control electronics, consider that most wires are designed to route out the backside of the enclosure with the exception of a handful of more typically accessible plugs on its front like the E-stop and USB.

![](/_images/_superlongboard/_manual/slb_ma_p51_2Mounts.png)

It’s easy to use the enclosure as a template to mark and drill the holes. The holes are 4.5mm large, spaced 45mm from each other and 230mm from the opposite pair. They’re not perfectly centered on the box but close to it.

You can use whatever bolt or screw type you like but the easiest approach is to use a minimum of 2 countersunk wood screws on diagonal holes from size #4-#8 and a minimum length of ½”. You might have to remove some of the plugs on the ends to access the holes when you screw down the enclosure.

## Technical Reference

### Connectors List

The SuperLongBoard comes with many inputs and outputs that are easy to wire in for CNC customization and accessory hookup by using pluggable terminal connectors. There are also a handful of other connectors used that are common and widely available for purchase. Below lists all connectors used on the board (male) with example links:

- **Power in**: <a href="https://www.lcsc.com/product-detail/Pluggable-System-Terminal-Block_Ningbo-Kangnex-Elec-WJ2EDGK-5-08-2P_C71370.html" target="_blank" rel="noopener">2-pin 5.08mm pitch Pluggable</a> Terminal Block (x1)
- **XYYZ Motors**: <a href="https://www.lcsc.com/product-detail/Pluggable-System-Terminal-Block_Ningbo-Kangnex-Elec-WJ2EDGK-5-08-4P_C71372.html" target="_blank" rel="noopener">4-pin 5.08mm pitch Pluggable</a> Terminal Block (x4)
- **E-stop, AUX Limits**: <a href="https://www.lcsc.com/product-detail/Pluggable-System-Terminal-Block_Ningbo-Kangnex-Elec-WJ15EDGK-3-81-7P_C24527.html" target="_blank" rel="noopener">7-pin 3.81mm pitch Pluggable</a> Terminal Block (x2)
- **Touch Plate, Flood out, Switch, Aux Power, LED Power, ADC**: <a href="https://www.lcsc.com/product-detail/Pluggable-System-Terminal-Block_Ningbo-Kangnex-Elec-WJ15EDGK-3-81-2P_C8466.html" target="_blank" rel="noopener">2-pin 3.81mm pitch Pluggable</a> Terminal Block (x8)
- **RGB LED Strips**: <a href="https://www.lcsc.com/product-detail/Housings-Wire-To-Board-Wire-To-Wire_JST-XHP-3_C144402.html" target="_blank" rel="noopener">3-pin 2.5mm JST XHP</a> (x2)
- **XYYZA Limit Switches, Door**: <a href="https://www.lcsc.com/product-detail/Rectangular-Connectors-Housings_JST-Sales-America_XHP-4_JST-Sales-America-XHP-4_C144403.html" target="_blank" rel="noopener">4-pin 2.5mm JST XHP</a> (x6)
- **Laser, TLS**: <a href="https://www.lcsc.com/product-detail/Pluggable-System-Terminal-Block_Ningbo-Kangnex-Elec-WJ15EDGK-3-81-3P_C8413.html" target="_blank" rel="noopener">3-pin 3.81mm pitch Pluggable</a> Terminal Block (x2)
- **Spindle**: <a href="https://www.lcsc.com/product-detail/Pluggable-System-Terminal-Block_Ningbo-Kangnex-Elec-WJ15EDGK-3-81-5P_C3804.html" target="_blank" rel="noopener">5-pin 3.81mm pitch Pluggable</a> Terminal Block (x1)
- **RS485**: <a href="https://www.lcsc.com/product-detail/Pluggable-System-Terminal-Block_Ningbo-Kangnex-Elec-WJ15EDGK-3-81-4P_C7244.html" target="_blank" rel="noopener">4-pin 3.81mm pitch Pluggable</a> Terminal Block (x1)
- **Aux Spindle, Pendant**: RJ25 Phone Jack
- **A-axis**: <a href="https://www.digikey.ca/en/products/detail/adam-tech/FCS-08-SG/9832361" target="_blank" rel="noopener">2x4-pin 2.54mm pitch Female IDC Flat Ribbon Cable Connector</a> (x1)
- **AUX COMM Header**: <a href="https://www.sparkfun.com/products/13028" target="_blank" rel="noopener">40-pin 2.54mm pitch GPIO Cable</a> (x1)

SLB EXT Plugs:

- **Motor Power**: <a href="https://www.lcsc.com/product-detail/Pluggable-System-Terminal-Block_Ningbo-Kangnex-Elec-WJ15EDGK-3-81-2P_C8466.html" target="_blank" rel="noopener">2-pin 3.81mm pitch Pluggable</a> Terminal Block (x4)
- **Motor Signal**: <a href="https://www.digikey.ca/en/products/detail/adam-tech/FCS-08-SG/9832361" target="_blank" rel="noopener">2x4-pin 2.54mm pitch Female IDC Flat Ribbon Cable Connector</a> (x4)

If you don’t happen to have these specific connectors on hand there are also common ‘hookup wires’ that ship with many electronics or Arduino kits that are 2.54mm pitch that you could also use to make many of the above connections.

### Current Unused Ports

Right now there are a handful of plugs and pins on the SLB that technically don’t do anything useful yet which is why there's nothing in the manual on it. The idea was that by adding in the hardware at the start, we could keep working on testing and implementing firmware to make more features available to all SLB owners without having to buy a new board. We’re very excited about it but ultimately can't make any guarantees on what will and won't ultimately work, so that's why no features have been promised yet outside of what's already been tested and delivered. These ports include the: **Y2 Limit Switch**, **SaS Spindle pin**, **Pendant**, **SD card**, **Door**, **ADC**, **40-pin AUX COMM Header**, and **AUX IO Header**.

If you’re still interested in trying these out without our support or documentation, <a href="https://resources.sienci.com/view/slb-welcome/#open-source" target="_blank" rel="noopener">we have all our board designs and firmware code available online for reference and modification</a> so you can feel free to try your own stuff and even contribute back to the project! For instance, you can see the <a href="https://github.com/Sienci-Labs/SuperLongBoard/blob/master/Project%20Outputs%20for%20Longboard_32bit/Schematic%20and%203D%20Prints/Longboard_32bit_Schematic_B6.1_FULL_PLACE.PDF" target="_blank" rel="noopener">40-pin inputs and outputs in the full schematic PDF</a> on page 19.

#### Y-axis auto squaring

Though this isn't yet supported in an official firmware build, you do have an option to try it out experimentally. Find the link here: https://forum.sienci.com/t/auto-squaring-on-the-slb/13753/18

This feature is useful on less rigid machines, since systems with more flex are more likely to have the two Y-axes to get out of sync with each other. For strong-built CNCs it's better to fix the squareness of the hardware itself than to ask the motors to do it. You can imagine that asking your motors to constantly fight to bring the machine back into square puts much more strain on the system, and in some cases compensation might not even be possible.

#### SD Card Macros

Though this isn't yet supported in an official firmware build, you do have an option to try it out experimentally. Find the link here: https://forum.sienci.com/t/auto-squaring-on-the-slb/13753/20

This feature allows you to run complex macros with variables and math from an SD Card inserted into the SLBs SD card slot. Once you flash the firmware, the remaining steps are to:

1. Make a plain text file with standard g-code and/or variables and controls supported by grblHAL
1. End the file with `M99`
1. Name the file with a letter and three numbers, and ".macro" as the file extension, e.g. `P101.macro`
1. Save it on the SD card then put it into the SLB and power cycle the board
1. In this example, the g-code command `G65 P101` will now run the macro on the SD card
