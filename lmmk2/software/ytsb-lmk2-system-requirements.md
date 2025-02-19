---
title: ytsb System Requirements 📊
menu_order: 6
post_status: draft
post_excerpt: Hardware requirements to run the LongMill CNC. Includes computer specifications, internet access and considerations for running CAD/CAM software.
post_date: 2022-03-17 20:01:00
taxonomy:
    knowledgebase_cat: lmk2-software
    knowledgebase_tag:
        - mk2
custom_fields:
    KBName: LongMill MK2 CNC
    basepress_post_icon: bp-caret-right
skip_file: no
featured_image: 
---

With today's advancements in computing hardware, most users will have no issues using their old or new computers and laptops to run their CNC machines. Generally, as long as your computer is **newer than 5 years old**, you should have no issues running a g-code sender like gSender or UGS. This page discusses hardware requirements and considerations to make for running your CNC machine.

Your system requirements may change depending on:

<ul>
  <li>Size of your g-code files</li>
  <li>System requirements of your CAD and CAM software</li>
  <li>gSender version you are using</li>
</ul>

## Basic Requirements

These are the minimum system requirements we believe will provide the best experience with your CNC machine. These requirements will suffice for sending g-code and controlling your machine. However, please refer to system requirements for [CAD and CAM software you may use](#requirements-for-cadcam-software).

**Operating system:** 64-bit Windows 10\* and higher, Mac, or Linux\*<br>
**CPU:** Intel or AMD processors 2Ghz and above, or Apple Silicon (M1, M2...)<br>
**RAM:** 2GB<br>
**Ports:** USB 2.0 or higher<br>
**Memory:** 200Mb of hard drive space

<a href="https://resources.sienci.com/view/gs-installation/" target="_blank" rel="noopener noreferrer">gSender</a> is software we recommend you use to interact with your machine. It is free and can be <a href="https://sienci.com/gSender/" target="_blank" rel="noopener noreferrer">downloaded from our website</a> at any time. gSender is designed to be lightweight and has been tested to run on both low and high-end hardware. Generally speaking, if your computer was made in the last 5 years, you should be able to use gSender without any issues. If you are not sure if gSender will work on your computer, we suggest downloading it to test it out. Most other g-code senders also tend to have similar requirements.

<b>*Note: After <em>gSender version 1.2.2</em>, support for 32-bit systems and Windows 7/8 had to be dropped since most new software packages can no longer support systems 10+ years old.</b>

## Internet Connection

An internet connection is **not needed** to run and operate your machine. However, you will need an internet connection at least one time to download the required software to operate your machine. Some programs such as CAMLab and Easel require an internet connection to work, but you can do design and g-code creation from one computer and use a separate computer to run the machine. If you require a setup to work completely offline, programs such as Vectric V-carve and Carbide Create offer the ability to design and generate g-code without an internet connection.

## Computer Setup

A computer must be on and plugged in via USB or Ethernet to operate the LongMill. Here are some considerations on your computer setup.

<b>Dust</b><br>
Having a computer located close to your CNC machine may expose it to dust. We recommend placing it in a location that is out of the way of dust. Each LongMill kit comes with a 1m USB cable, however, if you wish to extend the distance, a longer USB cable can be used (USB A to USB B).

<b>Dual computer setup</b><br>
Some users may choose to use a spare or inexpensive computer to run their machine and use a higher performance computer for CAD and CAM design in a different location. Because the system requirements for most g-code senders are quite low (we've managed to run machines on AMD Athalon and Raspberry Pi's), a less powerful computer can be used solely to send g-code and run their CNC machines. G-code can be transferred between computers just like any other file, such as via USB stick, email, or the cloud. This allows users to do their design and CAM work in one place and do their CNC work in another.

<b>Battery life</b><br>
Some jobs can take multiple hours. If you are using a laptop, ensure that you are plugged in or have enough battery life to complete your job.

## Requirements for CAD/CAM Software

System requirements for design/CAD and CAM software can vary widely depending on the complexity of the software. For example, Solidworks, a full-fledged, industrial CAD software recommends at least 16GB of RAM. On the other hand, cloud-based programs such as Onshape and CAMLab only require access to the internet and can even run on a smartphone.

For users that are just starting out, our recommended basic system requirements should provide enough brunt to handle most software. If you are using more advanced programs, please consult the documentation for the software that you plan to use.

If you're not sure what software you should use for making g-code or design, we strongly suggest checking out our <a href="https://resources.sienci.com/view/lmk2-software-explained/">software resources</a>.

## Raspberry Pi (advanced)

Computer/tech-savvy users can run a g-code sender using a Raspberry Pi. A <a href="https://www.raspberrypi.org/" target="_blank" rel="noopener noreferrer">Raspberry Pi</a> is a low cost, single-board computer that can be used as a dedicated computer to send g-code and operate the machine. Some benefits include:

<ul>
  <li>Being fairly inexpensive, with Raspberry Pi's typically costing around $30 to $50.</li>
  <li>Being unaffected by dust as it has no moving parts</li>
  <li>Allowing for more advanced features such as remote monitoring and control and cameras.</li>
</ul>

There are many different ways to set this up, and more information can be found online. While many users have successfully set their machine up with a Raspberry Pi, it can be complicated and may create new technical issues.
