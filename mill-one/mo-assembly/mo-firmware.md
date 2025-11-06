---
title: Firmware
menu_order: 3
post_status: publish
post_excerpt: 
post_date: 2021-04-30 19:02:00
taxonomy:
    knowledgebase_cat: mo-assembly
    knowledgebase_tag:
        - mill-one
custom_fields:
    KBName: Mill One CNC
    basepress_post_icon: bp-caret-right
skip_file: no
featured_image: 
---

Installing our firmware on your Mill One's Arduino Uno will enable your computer to stream cutting files to the Arduino using the USB cable. The Arduino Uno runs the Mill One by using a tailored version of the <a href="https://github.com/gnea/grbl" target="_blank" rel="noopener">grbl</a> v1.1g firmware. This firmware is set up for ⅛ microstepping and can be flashed onto your Arduino by using the Arduino IDE.

<a href="https://drive.google.com/file/d/1vC_FW-OuiQUUqW5v65H9DJ11xIBwV16M/view?usp=drive_link">Click this to download the firmware</a>, then follow these steps:

<ol>
  <li>Plug the Arduino into your computer with the USB cable (don't connect the power supply for now)</li>
  <li>Go to: <a href="https://www.arduino.cc/en/Main/Software" target="_blank" rel="noopener">https://www.arduino.cc/en/Main/Software</a> to download the latest Arduino IDE onto your computer for your appropriate operating system</li>
  <li>Once it's installed, open it and navigate to <b>File ➜ Open</b></li>
  <li>Locate where you downloaded the Sienci Mill One firmware and unzip it</li>
  <li>Once unzipped, navigate to <b>grbl ➜ examples ➜ grblUpload</b> then double-click on <b>grblUpload.ino</b></li>
  <li>A new window will pop up which will show you the code that needs to be uploaded</li>
  <li>Now go to <b>Sketch ➜ Include Library ➜ Add .zip Library</b> and navigate back to the firmware folder</li>
  <li>Open the firmware folder and double-click on the <b>grbl.zip</b> file</li>
  <li>You should see a message at the bottom of the window that says "Library added to your libraries."</li>
  <li>Now go to <b>Tools ➜ Board</b> and select <b>Arduino/Genuino Uno</b>, then go to <b>Tools ➜ Port</b> to select the right USB port</li>
  <li>Finally, click <b>File ➜ Upload</b> and the firmware will now be installed onto your machine</li>
</ol>

There should be a confirmation at the bottom of the window that says "Done uploading." To confirm that the code is working, go to <b>Tools ➜ Serial Monitor</b> and once you set the baud rate to '115200 baud' you should see a message pop up.

Once you get the message then congratulations! Your machine is now ready to go. In the following software steps you will learn about the software package that we offer for Mill One. This will allow you to carve out existing designs or enable you to create your own designs from scratch.

If you are updating your firmware from grbl v1.1e to grbl v1.1g, please read this <a href="https://sienci.com/2018/07/04/firmware-update-grbl-1-1g/" target="_blank" rel="noopener">post</a> first.
