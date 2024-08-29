---
title: ytsb Problems / Bugs?
menu_order: 4
post_status: draft
post_excerpt: A list of common problems and fixes for gSender users as well as links through to submitting bugs or finding more support through our forums or videos.
post_date: 2021-07-01 16:28
taxonomy:
    knowledgebase_cat: gdocs
    knowledgebase_tag:
        - gsender
custom_fields:
    KBName: gSender
    basepress_post_icon: bp-caret-right
skip_file: no
featured_image: _images/_gsender/_bugs/gs_bugs_p1_Diagnostic.png
---

Having <strong>troubles with gSender</strong> or have <strong>suggestions to improve it?</strong> Here are the steps you can follow:

<ol>
  <li><a href="#questions-or-suggestions"><strong>Questions</strong> or <strong>suggestions</strong></a> are always welcome!</li>
  <li>If you're <strong>having a problem</strong>, first help us out by ensuring that it's not an issue on your end with your computer or CNC. If you can try with another computer or g-code sender and still see the same problem then certainly let us know.</li>
  <li>If you're sure about the issue, and have already checked our docs, <a href="https://youtube.com/playlist?list=PLE43LQy2a1ioE8_sH0lcy8leYwrxvGhZ8" target="_blank" rel="noopener">YouTube playlist</a>, and <a href="https://resources.sienci.com/view/gs-feedback/#common-problems-amp-fixes">Common Problems &amp; Fixes</a> below, give us a hand by sending us <strong>as much information as possible</strong> so we can help diagnose your problem more easily.</li>
</ol>

<h2>Information to Send</h2>

In order of importance, please collect together information of:

<ol>
  <li>Your computer <strong>Operating system</strong> and <strong>gSender version</strong></li>
  <li>Please connect to your controller, try to recreate the issue, and as soon as it happens again create a '<strong>Diagnostic PDF</strong>' to send to us. If you can generate this shortly after the issue that's ok too, but it won't allow us to help you if you're not connected to your machine or you generate it too long after you had the issue happen. Find this by clicking on the 'Calibrate' tool in gSender, then clicking the 'Download Now!' button in the bottom, right corner and saving it on your computer.</li>
  <li><strong>gSender Settings</strong>, get these by going to Settings and locating the "Export Settings" button, then saving the file on your computer.</li>
  <li><strong>Machine Firmware</strong>, get these by going to the 'Firmware' tool and clicking the button for "Export Settings", then saving the file on your computer.</li>
  <li>Your <strong>g-code file</strong> if you're seeing the problem only with a specific file</li>
  <li>Any other <strong>pictures</strong> or <strong>videos</strong> of the problem can also help us to help you faster</li>
</ol>

Please attach the files and information in your post / <a href="mailto:hi@sienci.com">email</a> to us.

![](/_images/_gsender/_bugs/gs_bugs_p1_Diagnostic.png){.aligncenter .size-medium}

<h2>Questions or Suggestions</h2>

Send us the information, questions, or suggestions either on:

<ul>
  <li>The <a href="https://forum.sienci.com/c/gSender/" target="_blank" rel="noopener"><strong>gSender Forum</strong></a>
<a href="https://forum.sienci.com/c/gSender/">

![](/_images/_gsender/_bugs/gs_bugs_p2_Forum.png){.aligncenter .size-medium}
</a>
</li>
  <li><strong><a href="https://github.com/Sienci-Labs/gSender" target="_blank" rel="noopener">Github page</a></strong> (feel free to also submit PRs)</li>
  <li>You can join the discussion on secondary communities like our <a href="https://www.facebook.com/groups/gSender" target="_blank" rel="noopener">Facebook gSender Group</a>, and <a href="https://www.facebook.com/groups/mill.one" target="_blank" rel="noopener">Facebook CNC Group</a>, but we can't provide as much support or hear feedback in these groups.</li>
</ul>

<h2>Common Problems &amp; Fixes</h2>

We'll continue keeping our ears out for common stumbling points while using gSender and ensure we address them here for quick reference.

<h3>Issues downloading or opening gSender</h3>

<ol>
  <li>The main cause of this is usually a "virus protection" or Firewall software on your computer, or your computer system itself, thinking that gSender is 'unsafe' even though it's a proven software. In cases like these, first find the source of the blocking and then either make an exception for gSender or disable the blocking temporarily during download and installation.
<ul>
  <li>An example of this is if you see "Windows cannot access the specified device, path, or file. You may not have the appropriate permissions to access the item."</li>
  <li>For Windows-based computers you can read more on it here: <a href="https://support.microsoft.com/en-us/topic/-windows-cannot-access-the-specified-device-path-or-file-error-when-you-try-to-install-update-or-start-a-program-or-file-46361133-47ed-6967-c13e-e75d3cc29657" target="_blank" rel="noopener">https://support.microsoft.com/en-us/topic/-windows-cannot-access-the-specified-device-path-or-file-error-when-you-try-to-install-update-or-start-a-program-or-file-46361133-47ed-6967-c13e-e75d3cc29657</a></li>
</ul>
</li>
  <li>If gSender used to open fine but after an update it suddenly doesn't, check here since the update might've gotten corrupted: <a href="https://resources.sienci.com/view/gs-installation/#gSender-updates" target="_blank" rel="noopener">https://resources.sienci.com/view/gs-installation/#gsender-updates</a> (scroll past the first picture)</li>
  <li>If when you open gSender it gives you an error along the lines of "<strong>Entry Point Not Found</strong>", this means that you're trying to use a version of gSender past 1.2.2 with a 32-bit system. If you want to resolve this you'll either need to continue using a version of gSender 1.2.2 or earlier, or change to using a 64-bit system.</li>
</ol>

![](/_images/_gsender/_bugs/gs_bugs_p3_Error.png){.aligncenter .size-medium}

<h3>Screen goes Blank</h3>

If you find that gSender goes blank after you open it or while using it, there are a couple things you can try.

<ol>
  <li>If you’re using gSender Edge, you’ll see a toolbar at the top of the app where you can click: View -&gt; Toggle Developer Tools -&gt; then look at the ‘Console’ where if you find any errors you can share these with us. Also if you click: View -&gt; Reload, you’ll be able to refresh gSender to not show the blank screen anymore.</li>
  <li>Otherwise if you’re using the main version of gSender, you can try updating to the <a href="https://sienci.com/gSender/">latest version</a>.</li>
  <li>Check your antivirus software or Windows Defender and add gSender as an exception.</li>
  <li>Check to ensure you have read/write permissions for the preferences file
<ol>
  <li>Let’s locate the file! It’s called .sender_rc and can usually be found on your hard drive at: C:/users/{your username}/.sender_rc</li>
  
  ![](/_images/_gsender/_bugs/gs_bugs_p4_SenderRC.png){.aligncenter .size-medium}
  
  <li>Right-click on the file and choose properties. Under the security tab, check the name of your profile and confirm you have full control of the file.</li>
  <li>If not, select edit, choose your computer name, and grant permissions.</li>
</ol>
</li>
  <li>If you’re still getting a blank screen, locate your log file and send it in to us. It's located at: C:/Users/{your user name}/AppData/Roaming/gSender/Logs/main.log</li>
</ol>

<h3>Connects but status says Disconnected</h3>

If your machine connects on a COM port successfully but the machine status still says "Disconnected" then this is not an issue with gSender. Connecting in the top-left only indicates a USB connection has been made successfully, meanwhile the machine status box indicates whether gSender has been able to recognize the CNC machine. Your control board may have a faulty connection: gSender looks for the standard grbl response and boards that are loose or have become corrupted won't emit this response, if this is the case you can contact our support if you have a CNC from Sienci Labs or contact your own manufacturer's support for instructions on fixing your machine.

![](/_images/_gsender/_bugs/gs_bugs_p5_Disconnected.jpg){.aligncenter .size-medium}

<ol>
  <li>Power off your machine, then use a non-conductive tool like a plastic utensil to push down on all 4 corners of your control board shield or Arduino. For the LongBoard you don’t need to open it, just flip it upside down and you’ll be able to access the Arduino through the slats on the bottom. Doing this will ensure that everything is fully plugged in since sometimes if the Arduino is slightly off the control board it can mess with its communication.
  
  ![](/_images/_gsender/_bugs/gs_bugs_p6_PushIn.png){.aligncenter .size-medium}
  </li>
  <li>Re-flash your machine by following the instructions here: <a href="https://resources.sienci.com/wp-content/uploads/2021/07/gSender-Connected-but-No-Controls.pdf">gSender - Connected but No Controls</a></li>
  <li>Your machine isn't supported yet by gSender: if your CNC isn't grbl-based or your manufacturer had edited grbl too much or is using a different flavour from the standard version it's likely that gSender won't be able to recognize or control your machine</li>
</ol>

<h3>My CNC Profile is not listed</h3>

Much of the information that gSender needs about your CNC actually comes from its built-in EEPROM values, so the CNC profiles don't have any impact. This means that as long as your CNC is grbl-based, gSender should be able to control it just fine, even if it's not listed in the presets. Selecting the "Generic" preset will work just fine.

If some aspects of your machine don't seem right, it'll either be because your machine's manufacturer didn't flash your CNC with the appropriate EEPROM settings out of the box or they have some type of documentation which explains the values you need to change manually.

<h3>Port not detected for 3018 CNC</h3>

The 3018 and similar variations have been tested to work with gSender. Sainsmart points out in their documentation that sometimes an additional driver is needed for your computer to recognize the CNC via the USB port. They make this driver available for download here: <a href="http://s3.amazonaws.com/s3.image.smart/download/101-60-280PRO/CH341SER.ZIP" target="_blank" rel="noopener" data-saferedirecturl="https://www.google.com/url?q=http://s3.amazonaws.com/s3.image.smart/download/101-60-280PRO/CH341SER.ZIP&amp;source=gmail&amp;ust=1631110001464000&amp;usg=AFQjCNEjjbrFNXx3NVLiEuGgWkH05LOuwA">http://s3.amazonaws.com/s3.<wbr />image.smart/download/101-60-<wbr />280PRO/CH341SER.ZIP</a>

In case this link stops working, the associated documentation can be referenced here: <a href="https://docs.sainsmart.com/article/x6sr565m5g-3018-prover" target="_blank" rel="noopener" data-saferedirecturl="https://www.google.com/url?q=https://docs.sainsmart.com/article/x6sr565m5g-3018-prover&amp;source=gmail&amp;ust=1631110001465000&amp;usg=AFQjCNFZbYCqJdUYY8m1tVcLCVMiPzmPlw">https://docs.sainsmart.com/<wbr />article/x6sr565m5g-3018-prover</a>

For most of their machines they recommend using a 115200 baud rate, so double-check you're using that value as well.

<h3>Port not detected for my CNC</h3>

As long as you're using an Arduino-based board with grbl loaded onto it and you've selected the correct Baud rate in the settings then connection should be possible. Double-check that you're not connected to your machine in another sending program at the same time as you're trying to connect with gSender. As well, sometimes pendants or other forms of non-computer controllers can impede on a g-code sender's ability to connect to the machine.

We're still working on making gSender work best across all devices and one aspect of this is port detection for a variety of CNCs. If your CNC still isn't showing up on the port detector, we'd really like to hear from you.

One key bit of information that we need on our end is a picture or screenshot of your device information. You can get to this screen by:
<ol>
  <li>Make sure your CNC is plugged into your current computer via USB</li>
  <li>Open "Device Manager" in your Windows start menu

![](/_images/_gsender/_bugs/gs_bugs_p7_DeviceManager.png){.aligncenter .size-medium}</li>

  <li>Expand the "Ports (COM &amp; LPT)" heading

![](/_images/_gsender/_bugs/gs_bugs_p8_COMPorts.png){.aligncenter .size-medium}</li>

  <li>Find the listing related to your CNC. This will be the one that disappears and reappears if you unplug your CNC and plug it back in. It'll also be the port you normally connect to on other g-code senders.</li>
  <li>Right click that device and open "Properties"</li>
  <li>Open the "Details" tab at the top</li>
  <li>In the "Property" dropdown, select the "Hardware Ids" option</li>
  <li>Send us a picture of the final view. An example of what that might look like would be:
  
  ![](/_images/_gsender/_bugs/gs_bugs_p9_USBDevice.png){.aligncenter .size-medium}
  </li>
</ol>

We appreciate your feedback, and with your help we'll make sure the next version of gSender recognizes your machine.

<h3>File is Tiny in Visualizer</h3>

You're probably using the wrong post processor, go back and check what your CNC manufacturer recommends. By default it's best to use "grbl_mm" even if you like to use inches since most CNCs work in mm.

<h3>Jogging not working, I get an Error</h3>

If you're seeing a message in the 'Console' tab saying "error: Bad number format", this is because you're running an older grbl machine (pre Grbl 1.1f). Contact your CNC manufacturer or look through their resources to see how you can upgrade your grbl firmware so that your machine can be fully supported by gSender. If you have a Sienci Labs machine, this is as easy as using the 'Flash grbl' option in the 'Firmware' tool in gSender.

Alternatively, you could be getting an error for 'soft limits'. If this is the case then either your machine limits have been set incorrectly or you didn't home your CNC when you first connected to it. Try homing your machine and trying again, and keep an eye out for if you're only having this issue in certain parts of your cutting area.

<h3>Gamepad Error or Inconsistent Jogging</h3>

If you can't access your gamepad shortcuts or there's a problem with the profile, the easiest way to fix it is to delete the profile and remake it. This can suck depending on how much you customized it, and we'll keep working to make this process work better into the future.

If you can connect and jog with your gamepad but the jogging is sometimes unpredictable, then the problem might actually be the gamepad itself. Go to Settings -&gt; Shortcuts -&gt; Gamepad -&gt; Gamepad Profile -&gt; and click the 'Help' button at the top of the window. This will take you to a 3rd party Gamepad Tester website (that you can also visit at <a href="https://hardwaretester.com/gamepad" target="_blank" rel="noopener">https://hardwaretester.com/gamepad</a>) where you can try pressing buttons and moving joysticks to see if they're all behaving properly. If anything seems out of place then you might want to try using a different gamepad to control your CNC.

<h3>Changes between "Running" and "Idle" during a Job</h3>

This is Normal. Sometimes there can be pauses or long changes in direction in the g-code that can make the machine state change in this way.

<h3>Workspace changes during/after a job</h3>

If your g-code includes any workspace commands from G54 to G59, G59.1 to G59.3, or has an M2 or M30 command at the end of the program this will alter your selected workspace either to the one specified or revert it to G54. These commands affect how grbl stores the active workspace and so also affect the workspace stored by gSender. If you're experiencing this issue then you'll want to check your CAM post-processor and ensure that it stops inserting these commands when you export your g-code jobs.

Alternatively, gSender's 'Start/Stop G-code' can also be equipped to sidestep problems with changing workspaces by saving the active workspace at the start of the program and then re-loading it at the end. This can be done with the commands <code class="inline">%global.state.workspace=modal.wcs</code> and <code class="inline">[global.state.workspace]</code> as shown in the picture below. Remember to 'Update Event' on both entries:

![](/_images/_gsender/_bugs/gs_bugs_p10_StartStop.png){.aligncenter .size-medium}

<h3>Changed $1 and Motors still Hold</h3>

This is a quirk of grbl boards where after changing this value you need to make a motor movement (a jog movement for example) before the new value will take effect.
