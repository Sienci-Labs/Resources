---
title: System Requirements 📊
menu_order: 4
post_status: publish
post_excerpt: Hardware requirements to run the LongMill CNC. Includes computer specifications, internet access and considerations for running CAD/CAM software.
post_date: 2021-04-20 17:00:00
taxonomy:
    knowledgebase_cat: lm-software
    knowledgebase_tag:
        - mk1
custom_fields:
    KBName: LongMill CNC
    basepress_post_icon: bp-caret-right
skip_file: no
featured_image: /_images/_longmill/_assembly/_electronics/lm_electronics_p14.JPG
---

With today's advancements in computing hardware, most users will have no issues using their old or new computers and laptops to run their CNC machines. Generally, as long as your computer is **newer than 5 years old**, you should have no issues running a g-code sender like gSender or UGS. This page discusses hardware requirements and considerations to make for running your CNC machine.

Your system requirements may change depending on:

<ul>
  <li>Size of your g-code files</li>
  <li>System requirements of your CAD and CAM software</li>
</ul>

## Basic system requirements

These are the minimum system requirements we believe will provide the best experience with your CNC machine. These requirements will suffice for sending g-code and controlling your machine. However, please refer to system requirements for CAD and CAM software you may use.

**Operating system:** Windows 7/8/10, MacOS, Linux<br>
**CPU:** Intel or AMD processors 2Ghz<br>
**RAM:** 2GB<br>
**Ports:** USB 1.0<br>
**Memory:** 200Mb of hard drive space.

## Internet connection

An internet connection is **not needed** to run and operate your machine. However, you will need an internet connection at least one time to download the required software to operate your machine. Some programs such as CAMLab and Easel require an internet connection to work, but you can do design and g-code creation from one computer and use a separate computer to run the machine. If you require a setup to work completely offline, programs such as Vectric V-carve and Carbide Create offer the ability to design and generate g-code without an internet connection.

## Setting up your computer

A computer must be plugged in via USB and operating while the LongMill is in operation. Here are some considerations on your computer setup.

<b>Dust</b><br>
Having a computer located close to your CNC machine may expose it to dust. We recommend placing it in a location that is out of the way of dust. Each LongMill kit comes with a 1m USB cable, however, if you wish to extend the distance, a longer USB cable can be used (USB A to USB B).

<b>Dual computer setup</b><br>
Some users may choose to use a spare or inexpensive computer to run their machine and use a higher performance computer for CAD and CAM design in a different location. Because the system requirements for most g-code senders are quite low (we've managed to run machines on AMD Athalon and Raspberry Pi's), a less powerful computer can be used solely to send g-code and run their CNC machines. G-code can be transferred between computers just like any other file, such as via USB stick, email, or the cloud. This allows users to do their design and CAM work in one place and do their CNC work in another.

<b>Battery life</b><br>
Some jobs can take multiple hours. If you are using a laptop, ensure that you are plugged in or have enough battery life to complete your job.

## System requirement considerations for Design / CAM software

System requirements for design/ CAD and CAM software can vary widely depending on the complexity of the software. For example, Solidworks, a full-fledged, industrial CAD software recommends at least 16GB of RAM. On the other hand, cloud-based programs such as Onshape and CAMLab only require access to the internet and can even run on a smartphone.

For users that are just starting out, our recommended basic system requirements should provide enough brunt to handle most software. If you are using more advanced programs, please consult the documentation for the software that you plan to use.

## Raspberry Pi (advanced)

Computer/tech-savvy users can run a g-code sender using a Raspberry Pi. A <a href="https://www.raspberrypi.org/">Raspberry Pi</a> is a low cost, single-board computer that can be used as a dedicated computer to send g-code and operate the machine. Some benefits include:

<ul>
  <li>Being fairly inexpensive, with Raspberry Pi's typically costing around $30 to $50.</li>
  <li>Being unaffected by dust as it has no moving parts</li>
  <li>Allowing for more advanced features such as remote monitoring and control and cameras.</li>
</ul>

There are many different ways to set this up, and more information can be found online. While many users have successfully set their machine up with a Raspberry Pi, it can be complicated and may create new technical issues.
