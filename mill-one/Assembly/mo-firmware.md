---
title: Firmware
menu_order: 4
post_status: draft
post_excerpt: 
post_date: 2021-04-30 17:02:00
taxonomy:
    knowledgebase_cat: mo-assembly
    knowledgebase_tag:
        - mill-one
custom_fields:
    KBName: Mill One CNC
    basepress_post_icon: 10
skip_file: no
featured_image: 
---

Installing our firmware on your Mill One's Arduino Uno will enable your computer to stream cutting files to the Arduino using the USB cable. The Arduino Uno runs the Mill One by using a tailored version of the <a href="https://github.com/gnea/grbl" target="_blank" rel="noopener">grbl</a> v1.1g firmware. This firmware is set up for ⅛ microstepping and can be flashed onto your Arduino by using the Arduino IDE.

<a href="https://resources.sienci.com/wp-content/uploads/2021/05/GRBL-1.1g-Sienci-Mill-One.zip">Click this to download the firmware</a>, then follow these steps:

<ol>
  <li>Plug the Arduino into your computer with the USB cable (don't connect the power supply for now)</li>
  <li>Go to: <a href="https://www.arduino.cc/en/Main/Software" target="_blank" rel="noopener">https://www.arduino.cc/en/Main/Software</a> to download the latest Arduino IDE onto your computer for your appropriate operating system</li>
  <li>Once it's installed, open it and navigate to <strong>File -&gt; Open</strong></li>
  <li>Locate where you downloaded the Sienci Mill One firmware and unzip it</li>
  <li>Once unzipped, navigate to <strong>grbl -&gt; examples -&gt; grblUpload</strong> then double-click on <strong>grblUpload.ino</strong></li>
  <li>A new window will pop up which will show you the code that needs to be uploaded</li>
  <li>Now go to <strong>Sketch -&gt; Include Library -&gt; Add .zip Library</strong> and navigate back to the firmware folder</li>
  <li>Open the firmware folder and double-click on the <strong>grbl.zip</strong> file</li>
  <li>You should see a message at the bottom of the window that says "Library added to your libraries."</li>
  <li>Now go to <strong>Tools -&gt; Board</strong> and select <strong>Arduino/Genuino Uno</strong>, then go to <strong>Tools -&gt; Port</strong> to select the right USB port</li>
  <li>Finally, click <strong>File -&gt; Upload</strong> and the firmware will now be installed onto your machine</li>
</ol>

There should be a confirmation at the bottom of the window that says "Done uploading." To confirm that the code is working, go to <strong>Tools -&gt; Serial Monitor</strong> and once you set the baud rate to '115200 baud' you should see a message pop up.

Once you get the message then congratulations! Your machine is now ready to go. In the following software steps you will learn about the software package that we offer for Mill One. This will allow you to carve out existing designs or enable you to create your own designs from scratch.

If you are updating your firmware from grbl v1.1e to grbl v1.1g, please read this <a href="https://sienci.com/2018/07/04/firmware-update-grbl-1-1g/" target="_blank" rel="noopener">post</a> first.
