---
title: 10. Spindle Kit Setup
menu_order: 11
post_status: draft
post_excerpt:
taxonomy:
    knowledgebase_cat: am-mk2-assembly
    knowledgebase_tag:
custom_fields:
    KBName: AltMill CNC
    basepress_post_icon: bp-caret-right
skip_file: no
featured_image:
---

<a id="spindle-and-controller-connections"></a>

### Spindle and Controller Connections

These instructions apply to the standard Sienci Labs spindle kit. If you are installing the ATC kit, use the [ATC software and spindle configuration instructions](https://resources.sienci.com/view/atc-software/) for that kit.

**The instructions below must be followed in the exact order they are presented, otherwise the controller won’t be able to communicate with the VFD and will present an ‘Alarm 14’ error.**

If your SLB-EXT is powered on, please turn it **OFF** now.

Ensure that the spindle cable connector is installed on top of the spindle.

<div markdown="1" style="width: 960px; max-width: 100%;">

![](/_images/_am/_assembly/am_assembly_altmill-spindle-plugged.jpg){.alignnone .size-full}

</div>

<p style="text-align: center;"><em>Connecting spindle cable to spindle</em></p>

Then check that the RS485 wire is plugged into the SLB-EXT controller.

<div markdown="1" style="width: 1001px; max-width: 100%;">

![](/_images/_am/_assembly/am_assembly_atc-assembly-vfd-rs485in.jpg){.alignnone .size-full}

</div>

<p style="text-align: center;"><em>Connecting RS485 to SLB-EXT</em></p>

Ensure the RS485 cable is plugged into the connector above the OFF-ON switch and not the connector below the USB cable.

<div markdown="1" style="width: 1024px; max-width: 100%; margin-left: auto; margin-right: auto;">

![](/_images/_am/_assembly/am_assembly_rs485-correct-connector-1024x546.jpg){.aligncenter .size-large}

</div>

<p style="text-align: center;"><em>RS485 Correct Connector Location</em></p>

<!-- Q-POWER-01: Confirm the approved circuit and extension-cord requirements for each supported 1.5kW, 2.2kW and ATC kit. The previous universal 1500W extension-cord claim has been replaced with kit-specific wording; no substitute rating is invented. -->

Plug in the power cord from the VFD unit into a suitable wall outlet or extension cord now. If you use an extension cord, ensure its voltage and current ratings meet the requirements of your specific spindle/VFD kit.

<div markdown="1" style="width: 850px; max-width: 100%; margin-left: auto; margin-right: auto;">

![](/_images/_am/_assembly/am_assembly_plugginginvfd-850x638.jpg){.aligncenter .size-medium}

</div>

<p style="text-align: center;"><em>Connecting spindle to power</em></p>

The VFD screen should blink on with red text. Blinking text is normal behaviour for the VFD display.

<div markdown="1" style="width: 1152px; max-width: 100%;">

![](/_images/_am/_assembly/am_assembly_enclosed-vfd-flashing-startup.jpg){.alignnone .size-full}

</div>

Turn **ON** the controller using the power switch and make sure the E-stop is released. We will now move to setting things up on gSender.

<div markdown="1" style="width: 724px; max-width: 100%;">

![](/_images/_am/_assembly/am_assembly_image158.jpg)

</div>

Connect to gSender, as you did in the [First Movements](https://resources.sienci.com/view/am-mk2-first-movements/) section.

<a id="gsender-settings"></a>

### gSender Settings

**Open the dropdown menus below** to see the correct setup steps for the gSender version you have.

<a id="gsender-1-6-0-and-above"></a>

#### **gSender 1.6.0 and above**

[su_spoiler title="<strong>gSender 1.6.0 and above</strong>" open="yes" style="fancy" icon="chevron" anchor_in_url="yes"]

With your computer connected to your machine, and no alarms active, we’ll need to enable some settings to allow for communication between your controller and the spindle.

1. Go to **Tools,**then select **Accessory Installation**

<div markdown="1" style="width: 1223px; max-width: 100%;">

![](/_images/_am/_assembly/am_assembly_accessory-installation-gsender-1-6-0.jpg){.alignnone}

</div>

2. Select **Sienci Spindle**. Then follow the instructions in the installation wizard to finish setting up your spindle.

<div markdown="1" style="width: 1169px; max-width: 100%;">

![](/_images/_am/_assembly/am_assembly_spindle-setup-wizard.jpg){.alignnone}

</div>

3. Once you complete all the steps in the installation wizard, go back to the main page, Carve.

4. You should now see a ‘Spindle/Laser’ tab on the bottom right corner of gSender. Make sure **H-100** is selected in the ‘Spindles’ dropdown.

5. Then, you can try setting a desired RPM speed, then click ‘Forward’ to have the spindle start spinning up to the set speed. Ensure there are no obstacles in the way of the spindle or any loose parts nearby before turning this on. In the event of any emergency, press the physical E-stop button to immediately stop the spindle.

[/su_spoiler]

<a id="gsender-1-5-0-to-1-5-9"></a>

#### **gSender 1.5.0 to 1.5.9**

[su_spoiler title="<strong>gSender 1.5.0 to 1.5.9</strong>" open="no" style="fancy" icon="chevron" anchor_in_url="yes"]

With your computer connected to your machine, and no alarms active, we’ll need to enable some settings to allow for communication between your controller and the VFD.

1. In the **Console** at the bottom right corner, enter **$i** then press **Run.**

2. Check what **Driver Version** you have.

<div markdown="1" style="width: 1225px; max-width: 100%;">

![](/_images/_am/_assembly/am_assembly_firmwareversioncheck.jpg){.alignnone .size-full}

</div>

- **230917** – Please Download [2023 Sienci Spindle Configuration (SLB-EXT).](https://resources.sienci.com/wp-content/uploads/2025/06/Sienci-Spindle-Configuration-SLB-EXT.gcode)
- **260311** – Download [2026-SLB-EXT_Config_File](https://resources.sienci.com/wp-content/uploads/2025/03/new_spindle.gcode)

3. Press ‘Load File’ and select the file you just downloaded.

Then press ‘Start.’

<div markdown="1" style="width: 850px; max-width: 100%;">

![](/_images/_am/_assembly/am_assembly_spindle-config-run-850x478.jpg){.alignnone .size-medium}

</div>

4. Once the file is done, turn **OFF** the controller at the power switch.

5. Unplug the VFD from power.

6. Close gSender.

7. Then, plug the VFD back into power, turn ON the controller, and open gSender and reconnect.

8. Navigate to ‘Config’ then at the left header select ‘Spindle/Laser.’

9. Turn ON ‘Enable Spindle/Laser functionalities’ toggle (or ‘Spindle/Laser controls’ if you are on gSender 1.5.4 and higher).

<div markdown="1" style="width: 850px; max-width: 100%;">

![](/_images/_am/_assembly/am_assembly_spindle-enable-e1750278177178-850x186.jpg){.alignnone .size-medium}

</div>

10. Go back to the main page, Carve.

11. You should now see a ‘Spindle/Laser’ tab on the bottom right corner of gSender. Make sure **H-100** is selected in the ‘Spindles’ dropdown.

12. Then, you can try setting a desired RPM speed, then click ‘Forward’ to have the spindle start spinning up to the set speed. Ensure there are no obstacles in the way of the spindle or any loose parts nearby before turning this on. In the event of any emergency, press the physical E-stop button to immediately stop the spindle.

<div markdown="1" style="width: 850px; max-width: 100%;">

![](/_images/_am/_assembly/am_assembly_spindlelaser-gsender-edge-850x478.jpg){.alignnone .size-medium}

</div>

[/su_spoiler]

<a id="gsender-1-4-12-and-below"></a>

#### **gSender 1.4.12 and below**

[su_spoiler title="<strong>gSender 1.4.12 and below</strong>" open="no" style="fancy" icon="chevron" anchor_in_url="yes"]

1. With your computer connected to your machine, and no alarms active, we’ll need to enable some settings to allow for communication between your controller and the VFD. This can be done by downloading and running this file [Sienci Spindle Configuration (SLB-EXT).](https://resources.sienci.com/wp-content/uploads/2025/06/Sienci-Spindle-Configuration-SLB-EXT.gcode)

2. Press ‘Load Job’ and select the file you just downloaded.

3. Then press ‘Start.’

<div markdown="1" style="width: 850px; max-width: 100%;">

![](/_images/_am/_assembly/am_assembly_load-file-gsender-spindle-config-850x478.jpg){.alignnone .size-medium}

</div>

4. Once the file has finished, we will now reset everything so our changes can take effect. Turn **OFF** the controller at the power switch.

5. Unplug the VFD from power.

6. Close gSender.

7. Then, plug the VFD back into power, turn ON the controller, and open gSender and reconnect.

8. In gSender, click the small gear icon to open the settings menu, then select the ‘Spindle/Laser’ tab. Here, toggle the ‘Spindle/Laser’ option to enable this menu in gSender.

<div markdown="1" style="width: 850px; max-width: 100%; margin-left: auto; margin-right: auto;">

![](/_images/_am/_assembly/am_assembly_spindleenablegsenderui-scaled-e1720724226239-850x477.jpg){.aligncenter .size-medium}

</div>

<p style="text-align: center;"><em>Toggling the spindle on</em></p>

9. Set the spindle’s ‘Min’ and ‘Max’ speeds as 7500 and 24,000 RPM, respectively.

<div markdown="1" style="width: 850px; max-width: 100%; margin-left: auto; margin-right: auto;">

![](/_images/_am/_assembly/am_assembly_spindlespeedsettinggsenderui-scaled-e1720724308475-850x479.jpg){.aligncenter .size-medium}

</div>

<p style="text-align: center;"><em>Correct AltMill spindle speed settings</em></p>

10. You should now see a ‘Spindle/Laser’ tab on the bottom right corner of gSender. Make sure **H-100** is selected in the ‘Spindles’ dropdown.

11. Then, you can try setting a desired RPM speed, then clicking ‘**CW (M3)**’ to have the spindle start spinning up to the set speed. Ensure there are no obstacles in the way of the spindle or any loose parts nearby before turning this on. In the event of any emergency, press the physical E-stop button to immediately stop the spindle.

<div markdown="1" style="width: 850px; max-width: 100%; margin-left: auto; margin-right: auto;">

![](/_images/_am/_assembly/am_assembly_spindlefirstrungsender-scaled-e1720724342280-850x476.jpg){.aligncenter .size-medium}

</div>

[/su_spoiler]

<a id="spindle-direction"></a>

### Spindle Direction

While testing, make sure the spindle is spinning the correct direction by watching as the spindle slows down to a stop once done.

![](/_images/_am/_assembly/am_assembly_spindle-directions.jpg)

<p style="text-align: center;"><em>Direction of spindle </em></p>

<a id="spindle-break-in"></a>

### Spindle Break-in

The grease inside the bearings may have shifted during transportation, it is recommended that you run a “break-in” cycle to redistribute the grease before using your spindle. To do this, you can download and run the g-code file below on gSender, which should take 1 hour 40 minutes to run.

[Sienci Spindle Break-in.gcode](https://drive.google.com/file/d/1JdrqfgkZxhhXIAjUMOi-5UXIDjNveZe3/view?usp=sharing)

To run the file connect to gSender and press ‘Load File’ at the bottom left corner. Select the file and you should see a ‘Start Job’ button appear, go ahead and click that.

For regular maintenance of your spindle, we recommend running a shorter “warm up” g-code.

[Sienci Spindle Warm up.gcode](https://drive.google.com/file/d/1u5Tu5QdECCNx7W3NW7HJd1eErZ1Ggvyv/view?usp=sharing)

<a id="finishing-up"></a>

### Finishing Up

Congratulations on completing spindle setup! This is one of the trickiest parts of getting the AltMill ready.

If you are done for the day, just turn off the SLB-EXT controller using the power toggle. You can leave the VFD plugged into wall power.

However, if you choose to unplug the VFD, please follow this precise order for starting up each time, to avoid alarms:

<p style="text-align: left;"><strong>1. Make sure the controller is plugged into power but turned OFF</strong><br/>
<strong>2. Plug spindle into power, the VFD should blink with red text</strong><br/>
<strong>3. Then turn on the controller using the power toggle</strong></p>

If you have already set up your wasteboard, feel free to continue into the [Final Checks](https://resources.sienci.com/view/am-mk2-final-checks/) article. Otherwise, to the [Wasteboard](https://resources.sienci.com/view/am-mk2-wasteboard/) we go!
