---
title: ytsb Installation
menu_order: 4
post_status: draft
post_excerpt: Read about where to download gSender and how to install it onto Windows, Mac, Linux, or other PCs, as well as how to check for updates.
post_date: 2024-07-01 14:11
taxonomy:
    knowledgebase_cat: gdocs
    knowledgebase_tag:
        - gsender
custom_fields:
    KBName: gSender
    basepress_post_icon: bp-caret-right
skip_file: no
featured_image: _images/_gsender/_install/gs_install_pp1_Install.jpg
---
<h2>Download</h2>

If you haven't yet, download the right gSender file for your operating system. Links to common computer downloads and all other types and versions of gSender can be found on the main page: <a href="https://sienci.com/gSender/" target="_blank" rel="noreferrer noopener">https://sienci.com/gsender/</a>.

<strong>Note that as of <a href="https://github.com/Sienci-Labs/gSender/releases/tag/v1.2.2" target="_blank" rel="noopener">version 1.2.2</a>, support for 32-bit systems and Windows 7/8 had to be dropped</strong> since new software packages can no longer support systems 10+ years old.

If you downloaded the more experimental ‘gSender Edge’, then remember to also read what features it uniquely offers and how to use them: <a href="https://resources.sienci.com/view/gs-edge-features/" target="_blank" rel="noopener">https://resources.sienci.com/view/gs-edge-features/</a>

<h2>Windows Install</h2>

You may run into a security warning from your computer when you download the .EXE file. This can be bypassed by selecting “See more.” You can choose to keep the download, so that it can continue to run.

<strong>Microsoft Edge Users:</strong> If you are having difficulties downloading gSender when using Microsoft Edge, follow the <a href="https://resources.sienci.com/wp-content/uploads/2022/03/gSender-Microsoft-Edge-Browser-Install.pdf" target="_blank" rel="noopener">instructions here</a> or watch the video <a href="https://youtu.be/vvwtIjgMcAM" target="_blank" rel="noopener">here.</a>

![](/_images/_gsender/_install/gs_install_pp1_Install.jpg){.aligncenter .size-medium}

Once you've downloaded the EXE file, double-click to run it. gSender isn't yet set up to pass security checks so you'll have to allow it to run manually by clicking 'More Info' and then clicking 'Run anyway'. If you don't feel that you can trust gSender, then no pressure to use it; we'll have this setup later on.

![](/_images/_gsender/_install/gs_install_pp2_Install.jpg){.aligncenter .size-medium}

If the "More info" option isn't available, it could be that Windows is fully blocking installation. This can be fixed by going to "App &amp; browser control" and switching "Check app and files" to "Warn" or "Off" just for the installation of gSender. You can always turn it back on afterwards.

![](</_images/_gsender/_install/gs_install_pp3_Windows defender override.png>){.aligncenter .size-medium}

With permission to run, you should be met with a license agreement. gSender is provided "as is" which means there's no expectation that it'll run your CNC perfectly - especially as it's still in very active development. We want you to understand this before moving forward. If you agree, you'll be able to choose your install options from there (who to install for and where) and then begin installing.

![](</_images/_gsender/_install/gs_install_pp4_gSender Licensing.png>){.aligncenter .size-medium}

Install completion will be indicated by a completion screen. If the 'Run gSender' box is checked off you should be able to click 'Finish' and be greeted with a splash screen followed by the full program. If not, you can always open the program manually after install.

![](</_images/_gsender/_install/gs_install_pp5_Sender Instructions.png>){.aligncenter .size-medium}

<h2>Mac Install</h2>

Once you've downloaded the DMG file, double-click to run it. A window will popup that will look like the one below. Click and drag the gSender app and let go the applications folder to save it to your Mac.

![](</_images/_gsender/_install/gs_install_pp6_Mac Download.png>){.aligncenter .size-medium}

Navigate to your applications folder on your Mac and the gSender program should be there and ready for use.

![](</_images/_gsender/_install/gs_install_pp7_Screen Shot 2021-07-01 at 2.png>){.aligncenter .size-medium}

<strong>Note:</strong> we've been having problems creating an Arm build for Mac, but for now you should still be able to install the Intel version and use Rosetta just fine.

If you're having issues installing gSender on your Mac:

<ol>
  <li>Open System Preferences.</li>
  <li>Go to the Security &amp; Privacy tab.</li>
  <li>Click on the lock and enter your password so you can make changes.</li>
  <li>Change the setting to 'App Store and identified developers'</li>
  <li>After, you’ll see the option to override app blocking by clicking the temporary button to 'Open Anyway'</li>
  <li>You'll be asked one more time if you're sure, but clicking Open will run the app.</li>
</ol>

![](</_images/_gsender/_install/gs_install_pp8a_Mac Install.jpg>){.aligncenter .size-medium}

<h2>gSender Updates</h2>

gSender will notify you when new updates are available, allowing you to download them quickly and get running with the latest version. If you don't see these notifications, your system might not support it or your computer Firewall may be blocking them but you should still be able to download the <a href="https://sienci.com/gSender/">newest version</a> manually and install it over-top of the old version.

gSender updates always have the chance of encountering quirks, so if you have an important carve coming up or are just satisfied with your current setup then we'd typically recommend holding off until updating will be less 'mission-critical'. If you update accidentally and want to go back, you can also always <a href="#older-versions">downgrade</a>.

![](</_images/_gsender/_install/gs_install_pp8_gSender updater.png>){.aligncenter .size-medium}

<strong>Note:</strong> If you are upgrading to a new version or gSender, or downgrading to an older version, and you run into problems trying to get it to open or run, you’ll want to find a file called “<strong>.sender_rc</strong>” and rename it. This will allow gSender to generate a new version and clean up any errors you may be encountering. It also allows you to recover your old Start/Stop events and macros from the file in the future if needed.

<ul>
  <li>For Windows: the file can usually be found on your hard drive, at: <strong>C:/users/{your username}/.sender_rc</strong>. Rename it to whatever you like, like “<strong>.sender_rc_old</strong>”, then try to reinstall gSender again.</li>
</ul>

![](/_images/_gsender/_install/gs_install_pp10_senderrc.jpg){.aligncenter .size-medium}

![](/_images/_gsender/_install/gs_install_pp11_rcold.jpg){.aligncenter .size-medium}

<ul>
  <li>For Mac/Linux: the file is in the home directory as a hidden file. You can either:
<ul>

  <li>Go to your <strong>Home</strong> directory in Finder and make sure you have ‘show hidden files’ enabled (<strong>CMD + Shift +</strong> . ). You’ll then be able to see the file and rename it.</li>
  <li>Go into the Mac/Linux console and enter the command “<strong>mv ~/.sender_rc ~/.sender_rc_old</strong>”. You’ll be able to double check the renaming was successful by sending “<strong>ls -al | grep sender</strong>” in the console, where if you only see “<strong>.sender_rc_old</strong>”, you have successfully remanded and are ready to try to reinstall gSender.</li>
</ul>
</li>
</ul>

<h2>Older Versions</h2>

If you just updated gSender and are finding that it's not working for you, downgrading again is always available:
<ol>
  <li>If you go here: <a href="https://github.com/Sienci-Labs/gSender/releases" target="_blank" rel="noopener">https://github.com/Sienci-Labs/gsender/releases</a>, the newest version will always be at the top and shown in bold text like "<strong>v1.4.3</strong>" for example</li>
  <li>Scroll down to find older versions and choose the next version down or whatever version number you remember using</li>
  <li>Once you're at the version you want, scroll down to find "<strong>Assets</strong>" and click the text to open the list of downloads</li>
  <li>Find the right one for you, Windows is ".exe", Mac is ".dmg", etc. and click the file name to start downloading it. Once it's downloaded, you can install it over your current gSender version and continue from there</li>
</ol>

<h2>Chromebook</h2>

You can run gSender by using Linux inside of ChromeOS as long as you’re running 64-bit. Set up Linux on your Chromebook with <a href="https://support.google.com/chromebook/answer/9145439?hl=en&amp;fbclid=IwAR01u02vYLRXtjeB7EJOHFbsaIm2hsxFLbjK5zDSNhUE_F_Wn-ljnACo33k" target="_blank" rel="noopener">these instructions</a>. Open the command line and type: <code class="inline">cat /etc/os-release</code> or <code class="inline">uname -m</code> to see what architecture/operating system you are using, so you’ll know which gSender file to download. In the example below you can see we are running aarch64, which means we will want to download "arm-64bit.AppImage".

![](/_images/_gsender/_install/gs_install_pp12_raspberrypi.png){.aligncenter .size-medium}

![](/_images/_gsender/_install/gs_install_pp13_ARM64bit.png){.aligncenter .size-medium}

Download the .appimage file from the latest release of gSender and double click to launch. You will need to have the g-code files you want to carve in the same folder too. If you have success and find we’ve missed any steps here, let us know and we will update our resources!

<h2>Pi Install</h2>

If you’re considering a Pi setup, that’s great! There are a lot of potential perks that can come from having a cheap, mini, fanless computer to run your CNC without the downside of Windows updates and other quirks. A couple things you should know though before diving in:

<ul>
  <li>While most gSender users run simple 64-bit Windows or Mac based systems, RasPi is a whole other world of hardware and software configurations, making it really hard for us to offer all possible installs or help troubleshoot the variety in setups</li>
  <li>RasPi OS builds have been going through a large fluctuation recently swapping from 32-bit based to 64-bit which is still causing compatibility issues in the community since some libraries have kept up and others haven't, this has introduced a whole new variable of matching up OS install with software build and has eventually forced upon us the ability to only support 64-bit</li>
  <li>RasPi compatibility is ultimately something that we built due to community demand but still don't use much ourselves. In addition, anyone who tends to use RasPi likes to troubleshoot things themselves meaning that it's hard for us to know if we're missing anything in our instructions</li>
</ul>

We hope all of this explains why you’ll find the RasPi side of gSender support is inherently the least well documented of all the install options. We’ve tried our best to cover some of the more common setups, but we’d still recommend you have some familiarity with Linux if you continue with this installation since our support won’t be able to cover the many specific problems of various Pi builds.

<strong>Starting notes:</strong>
<ul>
  <li>We provide 2 different variations of Pi binary - .AppImage, .deb.</li>
  <li>Pi versions are all indicated by the “Pi-64Bit” tag in the executable name.</li>
  <li>Supported PI OS (Raspbian/Pi OS):
<ul>
  <li>To determine which OS you’re running, enter a terminal and type “cat /etc/os-release”. The name and pretty name should verify your OS and version</li>
</ul>
</li>
</ul>

![](/_images/_gsender/_install/gs_install_pp14_PiOS.jpg){.aligncenter .size-medium}

<strong>For most simple Pi setups, you’ll want to:</strong>
<ol>
  <li>Download the AppImage</li>
  <li>Right click and go to the permissions tab</li>
  <li>Make sure “executable” permission is set on the file</li>
  <li>Run the program</li>
</ol>
<strong>Default Pi credentials:
</strong>User: <em>pi</em>

These are needed when performing ‘sudo’ super user access, a type of administrator access needed to alter system-specific things. Once you’re set up with your Pi we recommend creating a new user account with different credentials as a security precaution, especially if you’re running gSender in remote mode or connecting your Pi to the internet. If these credentials don’t work for you then either check with your manufacturer or congratulations you’ve already created your own account and changed the default password ;)

To change the default pi user password. It's just menu -&gt; Preferences -&gt; Raspberry Pi Configuration and then the "Change Password" option

![](/_images/_gsender/_install/gs_install_pp15_Combopic.png){.aligncenter .size-medium}

&nbsp;

<strong>Error log location:
</strong>All application logs can be found in “<em>~/.config/gSender/logs</em>” and can be shared for any app-specific problems.

<h3>Common Issues</h3>

<strong>Sizing for Smaller Screens
</strong>gSender can size responsively but only to a minimum point. Because of this, some Pi users might find gSender isn't fitting their screen properly. This can be accommodated on most Pis by:

<ul>
  <li>Click the Pi icon on the top right</li>
  <li>Preferences -&gt; Screen configuration -&gt; Configure -&gt; Screens</li>
  <li>Click HDMI-1 (or whichever screen that is connected to the Pi), then you'll find you can select your Resolution</li>
  <li>We'd suggest you choose a minimum resolution of 1280x1024. Once chosen, you should be able to verify if this fix has worked for you or you can go back and continue to tweak it as needed.</li>
</ul>

This should allow gSender to show on your screen fully without it being cut off.

<strong>Visualizer is blank
</strong>This is most likely related to webGL not being enabled. You can check inside Chromium/Chrome by visiting <a href="https://webglreport.com/" target="_blank" rel="noopener">https://webglreport.com/</a> and checking that both WebGL 1 and WebGL 2 have the green 'supported' banner. If these aren’t present, then to enable webGL:

<ul>
  <li>Inside Chrome/Chromium, navigate to <a href="//settings" target="_blank" rel="noopener">chrome://settings</a></li>
  <li>In the ‘System’ section, ensure the “Use hardware acceleration when available” checkbox is checked</li>
  <li>Relaunch Chrome for the changes to take effect then go to <a href="//flags" target="_blank" rel="noopener">chrome://flags</a></li>
  <li>Ensure that “Disable WebGL” is not activated</li>
  <li>Relaunch Chrome for the changes to take effect and now these updated settings should be used by gSender’s Electron builder</li>
</ul>

<strong>Can’t open the port to connect
</strong>Make sure your user is part of the dialout group. To add your account to this group, go to a terminal and type “<em>sudo usermod -a -G dialout &lt;user&gt;</em>” (replacing “&lt;user&gt;” with your username). Restart after this change and try again.
