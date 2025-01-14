---
title: Installation
menu_order: 1
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
featured_image: _images/_gsender/_install/gs_in_windows-finish.jpg
---

## Download

If you haven't yet, download gSender for your specific system like Windows, Mac, or Pi on the main page: **<a href="https://sienci.com/gSender/" target="_blank" rel="noreferrer noopener">https://sienci.com/gsender/</a>**.

**Note: as of <a href="https://github.com/Sienci-Labs/gSender/releases/tag/v1.2.2" target="_blank" rel="noopener">gSender 1.2.2</a>, support for Windows 7/8 and 32-bit systems like Windows and Pi had to be dropped** since new software packages can no longer support 10+ year old systems.

If you downloaded the more experimental ‘gSender Edge’, then remember to also read what features it uniquely offers and how to use them: <a href="https://resources.sienci.com/view/gs-edge-features/" target="_blank" rel="noopener">https://resources.sienci.com/view/gs-edge-features/</a>

## Windows Install

We make sure gSender is perfectly safe to use, so if you see a **security warning** when you download the file, bypass it by selecting “See more” then allow it to continue. If you're still having difficulty, follow the <a href="https://resources.sienci.com/wp-content/uploads/2022/03/gSender-Microsoft-Edge-Browser-Install.pdf" target="_blank" rel="noopener">instructions here</a> or watch the video <a href="https://youtu.be/vvwtIjgMcAM" target="_blank" rel="noopener">here</a> for Microsoft Edge.

![](/_images/_gsender/_install/gs_in_windows-download.jpg){.aligncenter .size-medium}

Once the EXE file is downloaded, double-click to run it. If you see another security popup, click 'More Info' and then click 'Run anyway'. If you don't feel that you can trust gSender, then no pressure to use it.

![](/_images/_gsender/_install/gs_in_windows-defender.jpg){.aligncenter .size-medium}

If the "More info" option isn't available, go to "App & browser control" and switch "Check app and files" to either "Warn" or "Off" just for the installation of gSender. You can always turn it back on afterwards.

![](/_images/_gsender/_install/gs_in_windows-defender-override.jpg){.aligncenter .size-medium}

gSender is provided "as is" which means that even though we try our best to make it amazing, there should be no expectation it'll run your CNC perfectly and it could even cause issues. If you understand this and agree, you'll be able to choose your install options from there (who to install for and where) and then begin installing.

![](/_images/_gsender/_install/gs_in_windows-setup.jpg){.aligncenter .size-full}

Once you see the 'Completion' screen you should be good to go! Click 'Finish' then open gSender and get ready to connect to your CNC.

![](/_images/_gsender/_install/gs_in_windows-finish.jpg){.aligncenter .size-full}

### Open Faster

Some security software can **significantly slow down** the time it takes for gSender to open. We're still looking into how we can fix this, but for the time being we've found that making an exception will make gSender open much much faster. Please be careful doing this, we won't take responsibility if you run into other issues editing your computers security settings.

For most Windows computers go to **Settings ➜ Update & Security ➜ Windows Security ➜ Virus & threat protection ➜ Manage Settings ➜ Add or remove exclusions ➜ Add an exclusion ➜** then add the folder **C:\Program Files\gSender**. This has been reported to speed up open time by up to 30-40 seconds.

## Mac Install

**Note:** we've been having problems creating an Arm build for Mac, but for now you should still be able to install the Intel version and use Rosetta just fine.

Once you've downloaded gSender, double-click to run it. A window will pop up that will look like the one below. Click and drag the gSender app to the applications folder to save it to your computer.

![](/_images/_gsender/_install/gs_in_mac-download.jpg){.aligncenter .size-medium}

Go to your applications folder and you should find gSender ready to use once you follow the same install process as Windows.

![](/_images/_gsender/_install/gs_in_mac-finder.jpg){.aligncenter .size-medium}

If you're having issues installing gSender on your Mac:

1. Open System Preferences.
1. Go to the Security & Privacy tab.
1. Click on the lock and enter your password so you can make changes.
1. Change the setting to 'App Store and identified developers'
1. After, you’ll see the option to override app blocking by clicking the temporary button to 'Open Anyway'
1. You'll be asked one more time if you're sure, but clicking Open will run the app.
![](/_images/_gsender/_install/gs_in_mac-defender-override.jpg){.aligncenter .size-medium}

## gSender Updates

gSender will notify you when new updates are available, allowing you to download them quickly and get running with the latest version. If you don't see these notifications, your system might not support it or your computer Firewall may be blocking them but you should still be able to download the <a href="https://sienci.com/gSender/">newest version</a> manually and install it over-top the old version.

gSender updates always have the chance of encountering quirks, so if you have an important carve coming up or are just satisfied with your current setup then we'd typically recommend holding off until updating will be less 'mission-critical'. If you update accidentally and want to go back, you can also always <a href="#older-versions">downgrade</a>.

![](/_images/_gsender/_install/gs_in_updater.jpg){.aligncenter .size-full}

**If you upgrade to a new version, or downgrade to an older version, and gSender won't open or run (blank screen):**  
You’ll want to find a file called “**.sender_rc**” and rename it so gSender can generate a new version without errors. Sometimes you might also want to delete the “**.sienci-sessions**” folder too.

- For Windows: the file can usually be found on your hard drive, at: **C:/users/{your username}/.sender_rc**. Rename it to whatever you like, like “**.sender_rc_old**”, then try to reinstall gSender again.
![](/_images/_gsender/_install/gs_in_update-senderrc.jpg){.aligncenter .size-medium}
![](/_images/_gsender/_install/gs_in_update-rcold.jpg){.aligncenter .size-medium}
- For Mac/Linux: the file is in the home directory as a **hidden file**. You can either:
  - In Finder go to **Go ➜ Computer ➜ Drive ➜ Users ➜ {your username}** then unhide the ".sender_rc" file by pressing `CMD + Shift + .` keys. Rename it to whatever you like, like “**.sender_rc_old**”, then try to reinstall gSender again.
  - Go into the Mac/Linux console and enter the command `mv ~/.sender_rc ~/.sender_rc_old`. You’ll be able to double check the renaming was successful by sending `ls -al | grep sender` in the console, where if you only see `.sender_rc_old`, you have successfully remanded and are ready to try to reinstall gSender.
- If this solves your problem, you'll still be able to recover your old Start/Stop events and macros from the renamed file; just open it in a text editor and copy the macros you want to save so you can paste them back into gSender.

## Older Versions

If you just updated gSender and are finding that it's not working for you, downgrading again is always available:

1. If you go here: <a href="https://github.com/Sienci-Labs/gSender/releases" target="_blank" rel="noopener">https://github.com/Sienci-Labs/gsender/releases</a>, the newest version will always be at the top and shown in bold text like "**v1.4.3**" for example
1. Scroll down to find older versions and choose the next version down or whatever version number you remember using
1. Once you're at the version you want, scroll down to find "**Assets**" and click the text to open the list of downloads
1. Find the right one for you, Windows is ".exe", Mac is ".dmg", etc. and click the file name to start downloading it. Once it's downloaded, you can install it over your current gSender version and continue from there

## Chromebook

You can run gSender by using Linux inside of ChromeOS as long as you’re running 64-bit. Set up Linux on your Chromebook with <a href="https://support.google.com/chromebook/answer/9145439?hl=en" target="_blank" rel="noopener">these instructions</a>. Open the command line and type: `cat /etc/os-release` or `uname -m` to see what architecture/operating system you are using, so you’ll know which gSender file to download. In the example below you can see we are running aarch64, which means we will want to download "arm-64bit.AppImage".

![](/_images/_gsender/_install/gs_in_chromebook-arch.jpg){.aligncenter .size-medium}

![](/_images/_gsender/_install/gs_in_chromebook-arm64.jpg){.aligncenter .size-medium}

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

To change the default pi user password. It's just menu ➜ Preferences ➜ Raspberry Pi Configuration and then the "Change Password" option

![](/_images/_gsender/_install/gs_in_ras-pi-credentials.jpg){.aligncenter .size-medium}

**Error log location:**
All application logs can be found in “<em>~/.config/gSender/logs</em>” and can be shared for any app-specific problems.

### Common Issues

**Sizing for Smaller Screens**
gSender can size responsively but only to a minimum point. Because of this, some Pi users might find gSender isn't fitting their screen properly. This can be accommodated on most Pis by:

- Click the Pi icon on the top right
- Preferences ➜ Screen configuration ➜ Configure ➜ Screens
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
