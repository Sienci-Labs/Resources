---
title: grbl Firmware
menu_order: 0
post_status: publish
post_excerpt: The LongMill runs off the GRBL firmware, an open source firmware that is designed for Arduino-based CNC machines. You can re-flash by using gSender or UGS.
post_date: 2021-04-30 17:45:00
taxonomy:
    knowledgebase_cat: lm-advanced
    knowledgebase_tag:
        - mk1
custom_fields:
    KBName: LongMill CNC
    basepress_post_icon: bp-caret-right
skip_file: no
featured_image: /_images/_longmill/_advanced/_8_GRBL/lm_grbl_p1_MachinePreset.png
---

The LongMill runs off the <a href="https://github.com/gnea/grbl/releases" target="_blank" rel="noopener noreferrer">grbl firmware</a>, an open source firmware that is designed for Arduino-based CNC machines. Sometimes your machine could use a re-flash of this firmware in the case that:

<ul>
<li>Your firmware has somehow gotten corrupted which is causing unpredictable behaviour of your machine</li>
<li>You're looking to upgrade your LongBoard to the latest version of grbl</li>
</ul>

This page covers how to perform a re-flash of grbl already baked for the LongMill. This can be done either by:

<ol>
<li><b>Using gSender</b> - this is the easiest method since gSender will always contain the most up-to-date LongMill firmware and it also performs the entire process automatically</li>
<li><b>Using the Arduino IDE</b> - this is a more complex process that you can fall back on if you're unable to flash the firmware using gSender or you'd like to make your own firmware modifications</li>
</ol>

If you'd like to experiment with anything outside of the basic flashing process, the <a href="https://github.com/gnea/grbl/wiki" target="_blank" rel="noopener noreferrer">grbl Wiki</a> has a wealth of knowledge on compiling, connecting, flashing, and modifying grbl.

## Flashing grbl using gSender

### 1. Download gSender

You can download the installer for gSender here: <a href="https://sienci.com/gSender/" target="_blank" rel="noopener">https://sienci.com/gsender/</a>.

If you need instructions on how to install it, this documentation goes through the steps: <a href="https://resources.sienci.com/view/gs-installation/" target="_blank" rel="noopener">https://resources.sienci.com/view/gs-installation/</a>.

### 2. Utilize the Firmware Tool

Once you've completed the installation, open gSender and connect to your machine. Ensure you've selected your particular machine in the machine presets dropdown so that the correct firmware is flashed. This is available on the main settings page using the 'gear' in the top corner.

![](/_images/_longmill/_advanced/_8_GRBL/lm_grbl_p1_MachinePreset.png){.aligncenter .size-medium}

Access the Firmware Tool on the header of the program then look for the "Flash grbl" button to bring up the confirmation prompt.

**NOTE:** If you've made custom changes to your machines firmware that you don't want to lose, use the 'Export Settings' button to save your settings to a file that you can then reload when flashing is complete.

![](/_images/_longmill/_advanced/_8_GRBL/lm_grbl_p2_FirmTool.png){.aligncenter .size-medium}

You will see a warning about the risk of flashing the firmware. If you own a LongMill and have not made any modifications to your control board, there is almost no risk in completing this process. Press "OK" to continue.

![](/_images/_longmill/_advanced/_8_GRBL/lm_grbl_p3_FToolWarn.png){.aligncenter .size-medium}

### 3. Restore Settings

Once the flashing process is completed, you'll have to reconnect to your machine using the connection drop-down at the top-left corner. Go back to the Firmware Tools and press "Restore Defaults" to ensure your EEPROM settings are correct for the LongMill. If you previously exported your own custom settings, you can instead click the 'Import Settings' button to load your original settings back onto your machine. Close the Firmware Tool window, and try jogging to ensure the machine is working properly.

## Flashing grbl using the Arduino IDE

**NOTE:** If you've made custom changes to your machines firmware that you don't want to lose, you'll want to record them down before starting the flashing process. Whichever g-code sender you use you'll want to find the 'console' area and type '$$' and hit 'Enter'. This will pop up a block of values that you'll want to record however you wish. When you complete the flashing process you'll then be able to go back into your g-code sender and compare the new values the written ones and adjust them appropriately.

### 1. Download the Arduino IDE

Start by closing any programs (like **gSender**, **UGS**, **CNCjs**, **Easel**, etc.) that can connect to your LongMill controller. Since the LongBoard's 'brains' come from an Arduino that it has on-board, you will need a program called "**Arduino IDE**" in order to compile and flash any firmware changes onto the LongMill. The download page can be found here:<a href="https://www.arduino.cc/en/software" target="_blank" rel="noopener noreferrer">https://www.arduino.cc/en/software</a> .

![](/_images/_longmill/_advanced/_8_GRBL/lm_grbl_p4_arduinoIDE.png){.aligncenter .size-medium}

 **!! If you have flashed grbl firmware before using Arduino IDE, you will need to make sure to delete any old libraries for grbl.** Arduino typically saves libraries in the *Documents ➜ Arduino ➜ Library* folder of your computer for both Windows and Mac. If you do not delete the old library first, you will install the old version of grbl. **!!**

![](/_images/_longmill/_advanced/_8_GRBL/lm_grbl_p5_arduinoLib.png){.aligncenter .size-medium}

### 2. Clear the board's EEPROM

Once Arduino IDE has been installed, plug your control board into your computer then open the **Arduino IDE** program. Click on the "**Tools**" menu at the top and make sure that "Board" is set to "**Arduino Uno**" or "**Arduino/Genuino Uno**" and "Port" is set to the port you normally use for your LongMill (for example, COM3). The naming scheme for port names on Mac can look a little bit different, but typically the correct port is indicated with "**(Arduino/Genuino Uno)**" in the name. Later on if your program fails to upload, you can come back and try a different port until you find the correct one.

![](/_images/_longmill/_advanced/_8_GRBL/lm_grbl_p6_arduinoSetPort.png){.aligncenter .size-medium}

 To ensure that all of the old settings are cleared from the board's memory, we will do an EEPROM clear. You can find this 'example program' under *File ➜ Examples ➜ EEPROM ➜ eeprom_clear.*

 ![](/_images/_longmill/_advanced/_8_GRBL/lm_grbl_p7_EEPROMClear.png){.aligncenter .size-medium}

  Clicking this will open up a new window where you'll see the window is titled "**eeprom_clear**". Click on the "Upload" button on the top left of the program to compile and upload this code. If you run into an upload error at this step, you might still be connected to your LongMill on your computer in gSender, UGS, CNCjs, or even LightBurn. You'll need to disconnect from the LongMill in that program and then you should be able to retry the Upload.
  
  ![](/_images/_longmill/_advanced/_8_GRBL/lm_grbl_p8_Upload.png){.aligncenter .size-medium}
  
### 3. Upload the grbl firmware

Now that we've erased all previous memory from the control board, we can move forward by giving it new instructions to remember: this will be a brand new firmware installation. We keep all major LongMill firmware instances available for download, you'll likely want to click to download the most recent one: <a href="https://sienci.com/wp-content/uploads/2019/10/grbl-master-LongMill-V4.zip">LongMill Firmware (Oct 21, 2019)</a> <a href="https://sienci.com/wp-content/uploads/2020/02/grbl-LongMill-Firmware-Feb-25-2020.zip">LongMill Firmware (Feb 25, 2020)</a> <a href="https://resources.sienci.com/wp-content/uploads/2021/04/grbl-LongMill-Firmware-Sept-8-2021.zip">LongMill Firmware (Sept 8, 2021)</a> Once downloaded, this will appear onto your computer as a compressed or 'zipped' file. Locate the downloaded file in your computer folders, ‘un-zip’ or ‘extract’ it (usually found when you right-click the file), and then you'll notice a firmware folder with a name that matches the downloaded file and contains all the necessary files. If you open this folder up you should see a folder called "**grbl**", and from there if you open up the "**examples**" folder followed by the "**grblUpload**" folder. If you notice a file called "**grblUpload.ino**" this is what you'll want to open with the Arduino IDE program (this should be as simple as double-clicking the file which will open up a new window where you'll see the window is titled "**grblUpload**").

![](/_images/_longmill/_advanced/_8_GRBL/lm_grbl_p9_grblUpload.png){.aligncenter .size-medium}

Before hitting the "Upload" button, another step here is to prepare the grbl library. This is done by clicking on "Sketch" in the menu, then: *Include Library ➜ Add .ZIP library*.

![](/_images/_longmill/_advanced/_8_GRBL/lm_grbl_p10_AddZipLib.png){.aligncenter .size-medium}

After clicking "**Add .ZIP library**", you'll need to find your way back to the LongMill Firmware folder that you were already at before and select the **grbl.zip** file (shown in the picture). Click "**Open**" to add this grbl library to the Arduino program.

![](/_images/_longmill/_advanced/_8_GRBL/lm_grbl_p11_grblZip.png){.aligncenter .size-medium}

Now, upload the firmware code by clicking on the "**Upload**" button on the top left corner. It can take a minute or two for the firmware to finish uploading. Once completed you should see "Done uploading" in the turquoise bar as the bottom to let you know that the firmware has successfully been uploaded. Don't worry about if you see a message for "low memory available". The grbl firmware uses up a lot of the Arduino storage space but is designed to work very reliably regardless. The LongMill version is, if anything, a little bit smaller than the default grbl firmware so it will be just as stable.

![](/_images/_longmill/_advanced/_8_GRBL/lm_grbl_p12_grblDone.png){.aligncenter .size-medium}

You can check if your firmware has been correctly installed by going to *Tools ➜ Serial Monitor.* This will open a window to show the console output of the Arduino. If your output looks garbled, make sure to set your baud rate to 115200. As you can see, the output shows the firmware version and build date.

![](/_images/_longmill/_advanced/_8_GRBL/lm_grbl_p13_arduinoConfirm.png){.aligncenter .size-medium}

Your controller should now be flashed with the new firmware. Before opening your g-code sender, make sure to close the Arduino IDE first.
