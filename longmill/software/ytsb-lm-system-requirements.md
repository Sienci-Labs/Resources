---
title: ytsb System Requirements 📊
menu_order: 4
post_status: draft
post_excerpt: Hardware requirements to run the LongMill CNC. Includes computer specifications, internet access and considerations for running CAD/CAM software.
post_date: 2024-04-30 16:04
taxonomy:
    knowledgebase_cat: lm-software
    knowledgebase_tag:
        - mk1
custom_fields:
    KBName: LongMill CNC
    basepress_post_icon: bp-caret-right
skip_file: yes
featured_image: 
---
With today's advancements in computing hardware, most users will have no issues using their old or new computers and laptops to run their CNC machines. Generally, as long as your computer is <strong>newer than 5 years old</strong>, you should have no issues running a g-code sender like gSender or UGS. This page discusses hardware requirements and considerations to make for running your CNC machine.

Your system requirements may change depending on
<ul>
  <li>Size of your g-code files</li>
  <li>System requirements of your CAD and CAM software</li>
</ul>

<h2>Basic system requirements</h2>

These are the minimum system requirements we believe will provide the best experience with your CNC machine. These requirements will suffice for sending g-code and controlling your machine. However, please refer to system requirements for CAD and CAM software you may use.

<strong>Operating system: </strong>Windows 7/8/10, MacOS, Linux
<strong>CPU: </strong>Intel or AMD processors 2Ghz
<strong>RAM: </strong>2GB
<strong>Ports: </strong>USB 1.0
<strong>Memory: </strong>200Mb of hard drive space.

<h2>Internet connection</h2>

An internet connection is <strong>not needed </strong>to run and operate your machine. However, you will need an internet connection at least one time to download the required software to operate your machine. Some programs such as CAMLab and Easel require an internet connection to work, but you can do design and g-code creation from one computer and use a separate computer to run the machine. If you require a setup to work completely offline, programs such as Vectric V-carve and Carbide Create offer the ability to design and generate g-code without an internet connection.

<h2>Setting up your computer</h2>

A computer must be plugged in via USB and operating while the LongMill is in operation. Here are some considerations on your computer setup.

<strong>Dust</strong>Having a computer located close to your CNC machine may expose it to dust. We recommend placing it in a location that is out of the way of dust. Each LongMill kit comes with a 1m USB cable, however, if you wish to extend the distance, a longer USB cable can be used (USB A to USB B).

<strong>Dual computer setup</strong>Some users may choose to use a spare or inexpensive computer to run their machine and use a higher performance computer for CAD and CAM design in a different location. Because the system requirements for most g-code senders are quite low (we've managed to run machines on AMD Athalon and Raspberry Pi's), a less powerful computer can be used solely to send g-code and run their CNC machines. G-code can be transferred between computers just like any other file, such as via USB stick, email, or the cloud. This allows users to do their design and CAM work in one place and do their CNC work in another.

<strong>Battery life</strong>Some jobs can take multiple hours. If you are using a laptop, ensure that you are plugged in or have enough battery life to complete your job.

<h2>System requirement considerations for Design / CAM software</h2>

System requirements for design/ CAD and CAM software can vary widely depending on the complexity of the software. For example, Solidworks, a full-fledged, industrial CAD software recommends at least 16GB of RAM. On the other hand, cloud-based programs such as Onshape and CAMLab only require access to the internet and can even run on a smartphone.

For users that are just starting out, our recommended basic system requirements should provide enough brunt to handle most software. If you are using more advanced programs, please consult the documentation for the software that you plan to use.

<h2>Raspberry Pi (advanced)</h2>

Computer/tech-savvy users can run a g-code sender using a Raspberry Pi. A <a href="https://www.raspberrypi.org/">Raspberry Pi</a> is a low cost, single-board computer that can be used as a dedicated computer to send g-code and operate the machine. Some benefits include
<ul>
  <li>Being fairly inexpensive, with Raspberry Pi's typically costing around $30 to $50.</li>
  <li>Being unaffected by dust as it has no moving parts</li>
  <li>Allowing for more advanced features such as remote monitoring and control and cameras.</li>
</ul>

There are many different ways to set this up, and more information can be found online. While many users have successfully set their machine up with a Raspberry Pi, it can be complicated and may create new technical issues.