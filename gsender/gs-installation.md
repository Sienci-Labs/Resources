---
title: Installation
menu_order: 4
post_status: publish
post_excerpt: Read about where to download gSender and how to install it onto Windows, Mac, Linux, or other PCs, as well as how to check for updates.
post_date: 2021-07-01 14:11:00
taxonomy:
    knowledgebase_cat: gdocs
    knowledgebase_tag:
        - gsender
custom_fields:
    KBName: gSender
    basepress_post_icon: bp-caret-right
skip_file: no
featured_image: _images/_gsender/_install/gs_in_windows-finish.png
---

## Download

If you haven't yet, download the right gSender file for your operating system. Links to common computer downloads and all other types and versions of gSender can be found on the main page: <a href="https://sienci.com/gSender/" target="_blank" rel="noreferrer noopener">https://sienci.com/gsender/</a>.

**Note that as of <a href="https://github.com/Sienci-Labs/gSender/releases/tag/v1.2.2" target="_blank" rel="noopener">version 1.2.2</a>, support for 32-bit systems and Windows 7/8 had to be dropped** since new software packages can no longer support systems 10+ years old.

If you downloaded the more experimental ‘gSender Edge’, then remember to also read what features it uniquely offers and how to use them: <a href="https://resources.sienci.com/view/gs-edge-features/" target="_blank" rel="noopener">https://resources.sienci.com/view/gs-edge-features/</a>

## Windows Install

You may run into a security warning from your computer when you download the .EXE file. This can be bypassed by selecting “See more.” You can choose to keep the download, so that it can continue to run.

**Microsoft Edge Users:** If you are having difficulties downloading gSender when using Microsoft Edge, follow the <a href="https://resources.sienci.com/wp-content/uploads/2022/03/gSender-Microsoft-Edge-Browser-Install.pdf" target="_blank" rel="noopener">instructions here</a> or watch the video <a href="https://youtu.be/vvwtIjgMcAM" target="_blank" rel="noopener">here.</a>

![](/_images/_gsender/_install/gs_in_windows-download.jpg){.aligncenter .size-medium}

Once you've downloaded the EXE file, double-click to run it. gSender isn't yet set up to pass security checks so you'll have to allow it to run manually by clicking 'More Info' and then clicking 'Run anyway'. If you don't feel that you can trust gSender, then no pressure to use it; we'll have this setup later on.

![](/_images/_gsender/_install/gs_in_windows-defender.jpg){.aligncenter .size-medium}

If the "More info" option isn't available, it could be that Windows is fully blocking installation. This can be fixed by going to "App &amp; browser control" and switching "Check app and files" to "Warn" or "Off" just for the installation of gSender. You can always turn it back on afterwards.

![](/_images/_gsender/_install/gs_in_windows-defender-override.png){.aligncenter .size-medium}

With permission to run, you should be met with a license agreement. gSender is provided "as is" which means there's no expectation that it'll run your CNC perfectly - especially as it's still in very active development. We want you to understand this before moving forward. If you agree, you'll be able to choose your install options from there (who to install for and where) and then begin installing.

![](/_images/_gsender/_install/gs_in_windows-setup.png){.aligncenter .size-full}

Install completion will be indicated by a completion screen. If the 'Run gSender' box is checked off you should be able to click 'Finish' and be greeted with a splash screen followed by the full program. If not, you can always open the program manually after install.

![](/_images/_gsender/_install/gs_in_windows-finish.png){.aligncenter .size-full}

## Mac Install

Once you've downloaded the DMG file, double-click to run it. A window will popup that will look like the one below. Click and drag the gSender app and let go the applications folder to save it to your Mac.

![](/_images/_gsender/_install/gs_in_mac-download.png){.aligncenter .size-medium}

Navigate to your applications folder on your Mac and the gSender program should be there and ready for use.

![](/_images/_gsender/_install/gs_in_mac-finder.png){.aligncenter .size-medium}

**Note:** we've been having problems creating an Arm build for Mac, but for now you should still be able to install the Intel version and use Rosetta just fine.

If you're having issues installing gSender on your Mac:

1. Open System Preferences.
1. Go to the Security &amp; Privacy tab.
1. Click on the lock and enter your password so you can make changes.
1. Change the setting to 'App Store and identified developers'
1. After, you’ll see the option to override app blocking by clicking the temporary button to 'Open Anyway'
1. You'll be asked one more time if you're sure, but clicking Open will run the app.
![](/_images/_gsender/_install/gs_in_mac-defender-override.jpg){.aligncenter .size-medium}

## gSender Updates

gSender will notify you when new updates are available, allowing you to download them quickly and get running with the latest version. If you don't see these notifications, your system might not support it or your computer Firewall may be blocking them but you should still be able to download the <a href="https://sienci.com/gSender/">newest version</a> manually and install it over-top of the old version.

gSender updates always have the chance of encountering quirks, so if you have an important carve coming up or are just satisfied with your current setup then we'd typically recommend holding off until updating will be less 'mission-critical'. If you update accidentally and want to go back, you can also always <a href="#older-versions">downgrade</a>.

![](/_images/_gsender/_install/gs_in_updater.png){.aligncenter .size-full}

**Note:** If you are upgrading to a new version or gSender, or downgrading to an older version, and you run into problems trying to get it to open or run, you’ll want to find a file called “**.sender_rc**” and rename it. This will allow gSender to generate a new version and clean up any errors you may be encountering. It also allows you to recover your old Start/Stop events and macros from the file in the future if needed.

- For Windows: the file can usually be found on your hard drive, at: **C:/users/{your username}/.sender_rc**. Rename it to whatever you like, like “**.sender_rc_old**”, then try to reinstall gSender again.
![](/_images/_gsender/_install/gs_in_update-senderrc.jpg){.aligncenter .size-medium}
![](/_images/_gsender/_install/gs_in_update-rcold.jpg){.aligncenter .size-medium}
- For Mac/Linux: the file is in the home directory as a hidden file. You can either:
  - Go to your **Home** directory in Finder and make sure you have ‘show hidden files’ enabled (**CMD + Shift + .** ). You’ll then be able to see the file and rename it.
  - Go into the Mac/Linux console and enter the command “**mv ~/.sender_rc ~/.sender_rc_old**”. You’ll be able to double check the renaming was successful by sending “**ls -al | grep sender**” in the console, where if you only see “**.sender_rc_old**”, you have successfully remanded and are ready to try to reinstall gSender.

## Older Versions

If you just updated gSender and are finding that it's not working for you, downgrading again is always available:

1. If you go here: <a href="https://github.com/Sienci-Labs/gSender/releases" target="_blank" rel="noopener">https://github.com/Sienci-Labs/gsender/releases</a>, the newest version will always be at the top and shown in bold text like "**v1.4.3**" for example
1. Scroll down to find older versions and choose the next version down or whatever version number you remember using
1. Once you're at the version you want, scroll down to find "**Assets**" and click the text to open the list of downloads
1. Find the right one for you, Windows is ".exe", Mac is ".dmg", etc. and click the file name to start downloading it. Once it's downloaded, you can install it over your current gSender version and continue from there

## Chromebook

You can run gSender by using Linux inside of ChromeOS as long as you’re running 64-bit. Set up Linux on your Chromebook with <a href="https://support.google.com/chromebook/answer/9145439?hl=en" target="_blank" rel="noopener">these instructions</a>. Open the command line and type: <code class="inline">cat /etc/os-release</code> or <code class="inline">uname -m</code> to see what architecture/operating system you are using, so you’ll know which gSender file to download. In the example below you can see we are running aarch64, which means we will want to download "arm-64bit.AppImage".

![](/_images/_gsender/_install/gs_in_chromebook-arch.png){.aligncenter .size-medium}

![](/_images/_gsender/_install/gs_in_chromebook-arm64.png){.aligncenter .size-medium}

Download the .appimage file from the latest release of gSender and double click to launch. You will need to have the g-code files you want to carve in the same folder too. If you have success and find we’ve missed any steps here, let us know and we will update our resources!

## Pi Install

If you’re considering a Pi setup, that’s great! There are a lot of potential perks that can come from having a cheap, mini, fanless computer to run your CNC without the downside of Windows updates and other quirks. A couple things you should know though before diving in:

- While most gSender users run simple 64-bit Windows or Mac based systems, RasPi is a whole other world of hardware and software configurations, making it really hard for us to offer all possible installs or help troubleshoot the variety in setups
- RasPi OS builds have been going through a large fluctuation recently swapping from 32-bit based to 64-bit which is still causing compatibility issues in the community since some libraries have kept up and others haven't, this has introduced a whole new variable of matching up OS install with software build and has eventually forced upon us the ability to only support 64-bit
- RasPi compatibility is ultimately something that we built due to community demand but still don't use much ourselves. In addition, anyone who tends to use RasPi likes to troubleshoot things themselves meaning that it's hard for us to know if we're missing anything in our instructions

We hope all of this explains why you’ll find the RasPi side of gSender support is inherently the least well documented of all the install options. We’ve tried our best to cover some of the more common setups, but we’d still recommend you have some familiarity with Linux if you continue with this installation since our support won’t be able to cover the many specific problems of various Pi builds.

**Starting notes:**

- We provide 2 different variations of Pi binary - .AppImage, .deb.
- Pi versions are all indicated by the “Pi-64Bit” tag in the executable name.
- Supported PI OS (Raspbian/Pi OS):
  - To determine which OS you’re running, enter a terminal and type “cat /etc/os-release”. The name and pretty name should verify your OS and version
![](/_images/_gsender/_install/gs_in_ras-pi-os.jpg){.aligncenter .size-medium}

**For most simple Pi setups, you’ll want to:**

1. Download the AppImage
1. Right click and go to the permissions tab
1. Make sure “executable” permission is set on the file
1. Run the program

**Default Pi credentials:**
User: <em>pi</em>

These are needed when performing ‘sudo’ super user access, a type of administrator access needed to alter system-specific things. Once you’re set up with your Pi we recommend creating a new user account with different credentials as a security precaution, especially if you’re running gSender in remote mode or connecting your Pi to the internet. If these credentials don’t work for you then either check with your manufacturer or congratulations you’ve already created your own account and changed the default password ;)

To change the default pi user password. It's just menu -&gt; Preferences -&gt; Raspberry Pi Configuration and then the "Change Password" option

![](/_images/_gsender/_install/gs_in_ras-pi-credentials.png){.aligncenter .size-medium}

**Error log location:**
All application logs can be found in “<em>~/.config/gSender/logs</em>” and can be shared for any app-specific problems.

### Common Issues

**Sizing for Smaller Screens**
gSender can size responsively but only to a minimum point. Because of this, some Pi users might find gSender isn't fitting their screen properly. This can be accommodated on most Pis by:

- Click the Pi icon on the top right
- Preferences -&gt; Screen configuration -&gt; Configure -&gt; Screens
- Click HDMI-1 (or whichever screen that is connected to the Pi), then you'll find you can select your Resolution
- We'd suggest you choose a minimum resolution of 1280x1024. Once chosen, you should be able to verify if this fix has worked for you or you can go back and continue to tweak it as needed.

This should allow gSender to show on your screen fully without it being cut off.

**Visualizer is blank**
This is most likely related to webGL not being enabled. You can check inside Chromium/Chrome by visiting <a href="https://webglreport.com/" target="_blank" rel="noopener">https://webglreport.com/</a> and checking that both WebGL 1 and WebGL 2 have the green 'supported' banner. If these aren’t present, then to enable webGL:

- Inside Chrome/Chromium, navigate to <a href="//settings" target="_blank" rel="noopener">chrome://settings</a>
- In the ‘System’ section, ensure the “Use hardware acceleration when available” checkbox is checked
- Relaunch Chrome for the changes to take effect then go to <a href="//flags" target="_blank" rel="noopener">chrome://flags</a>
- Ensure that “Disable WebGL” is not activated
- Relaunch Chrome for the changes to take effect and now these updated settings should be used by gSender’s Electron builder

**Can’t open the port to connect**
Make sure your user is part of the dialout group. To add your account to this group, go to a terminal and type “<em>sudo usermod -a -G dialout &lt;user&gt;</em>” (replacing “&lt;user&gt;” with your username). Restart after this change and try again.