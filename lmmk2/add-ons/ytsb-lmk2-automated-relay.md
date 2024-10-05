---
title: ytsb Automated / IOT Relay
menu_order: 0
post_status: draft
post_excerpt: Use an IOT relay on your LongMill CNC to automatically control power to your router, vacuum, lighting, or other AC power systems.
post_date: 2021-04-30 17:35:00
taxonomy:
    knowledgebase_cat: lmk2-add-ons
    knowledgebase_tag:
        - mk2
custom_fields:
    KBName: LongMill MK2 CNC
    basepress_post_icon: bp-caret-right
skip_file: yes
featured_image: 
---

You can use an IOT relay to automatically control power to your router, vacuum, lighting, or other AC power systems when you have a job running. The setup process consists of:

<ol>
  <li>Wiring up the IOT relay</li>
  <li>Preparing your g-code to control the relay</li>
</ol>

This IOT setup method is written for the LongBoard controller and was inspired by the work of Max C., Mark D. and other LongMill community members! If you'd like to see Max' full original document, you can download it here: <a href="https://resources.sienci.com/wp-content/uploads/2021/06/Max-C.-IOT-Relay-setup.docx" target="_blank" rel="noopener">IOT Relay.doc</a>

## Hardware

Parts needed:

<ul>
  <li>x1 <b>IOT relay</b>
<ul>
  <li>We’ve tested the IOT Relay from Digital Loggers, it can be found on Amazon and has more info here: <a href="https://www.digital-loggers.com/iotfaqs.html" target="_blank" rel="noopener">https://www.digital-loggers.com/iotfaqs.html</a></li>
  <li>Includes surge suppression, debounce, and a safety breaker</li>
  <li>Consists of 4 outlets - x1 Always On, x1 Normally On (NO), x2 Normally Off (NC)</li>
  <li>Can also be controlled by a standalone Arduino or Raspberry Pi</li>
</ul>
</li>
</ul>
<ul>
  <li>x2, <b>2-position female terminal block connector</b>
<ul>
  <li>One will come already plugged into the IOT relay, the other plugged into the LongBoard</li>
  <li>Same as the green connector used for the touch plate</li>
  <li>3.81mm (0.15”) pitch</li>
</ul>
</li>
</ul>
<ul>
  <li>Some spare <b>16 AWG wire</b> (see picture)
<ul>
  <li>This is the same size as what's used for the LongMill E-stop</li>
  <li>Ideally use wire with the red and black bound together, in whatever length is needed for your setup</li>
</ul>
</li>
</ul>

![](/_images/_longmill/_advanced/_6_IOTRelay/lm_IOT_p1_Wire.jpg){.aligncenter size-medium}

## Installation

<ol>
  <li>Take out the green connector from the IOT relay and loosen the flat-head screws on the connector.</li>
  <li>Wire this connector so that the wires match up with the labelling on the IOT relay: red wire to the positive (+) and black to the negative (-). Clamp down the wires using the flat-heads on the terminals.</li>
  <li>Do the same on the other end, this time matching the red wire to "Coolant" and the black wire into "GND", clamping the wires firmly into place.</li>
  <li>Finally, use the power cord provided with the IOT relay to plug it into a nearby outlet (if you plan on drawing reasonable current through the relay, consider using an outlet that's on a breaker separate from your CNC machine to reduce line noise).</li>
</ol>

![](/_images/_longmill/_advanced/_6_IOTRelay/lm_IOT_p2_CoolantHookUp.jpg){.aligncenter size-medium}

## Testing

Now's a good time to quickly verify that everything has been hooked up correctly. To test the relay, we'll be connecting to our LongMill via a g-code sender such as gSender, UGS, or CNCjs like we normally would and keep an eye on the red "power" light on the relay. Whichever sender you use you'll want to find the "Console" input area (shown by a red box), and type the following text:

<ul>
  <li><b>M8</b>, then press the 'Enter' key to send - this should activate an audible *click* from the IOT relay and you should notice the 'switch active' light illuminate.</li>
  <li><b>M9</b>, then press the 'Enter' key to send - this should also produce a *click* noise, this time turning the 'switch active' light off.</li>
</ul>

![](/_images/_longmill/_advanced/_6_IOTRelay/lm_IOT_p3_Testing.png){.aligncenter size-medium}

![](/_images/_longmill/_advanced/_6_IOTRelay/lm_IOT_p4_Switch.jpg){.aligncenter size-medium}

If you're not seeing the results you expect, double-check you've got your wires running correctly and the connectors are plugged in all the way to the relay and the LongBoard.

If everything is behaving as expected, you'll now be able to test with the relay controlling whatever peripheral you're planning on hooking up (vacuum, router, etc.). Note that the IOT relay is built to handle <span dir="ltr">0-8A with 18AWG power cords and 0-12A with </span><span dir="ltr">16AWG cord.</span>

<ol>
  <li>Be sure you've sent <b>M9</b> to your g-code sender and the relay power light is off.</li>
  <li>With the IOT relay toggle switch set to "OFF", plug in your external AC device. You'll normally want to use the "Normally Off" outlets since these turn ON with <b>M8</b> and OFF with <b>M9</b>, meanwhile the "Always On" outlet always provides continuous power and the "Normally On" outlet turns OFF with <b>M8</b> and turns ON with <b>M9</b>.</li>
  <li>Safely toggle the power switch on your external device (router, vacuum, etc.) to be ON. They should show no sign of power at this point.</li>
  <li>Safely toggle the IOT relay switch to 'RESET'. There should still be nothing occurring.</li>
  <li>Send again an <b>M8</b> command in the g-code sender while your finger is on the red switch of the IOT relay in case something goes wrong. After sending the command your external devices should now power on.</li>
  <li>Power everything back off by sending <b>M9</b>.</li>
</ol>

![](/_images/_longmill/_advanced/_6_IOTRelay/lm_IOT_p5_FullDiagram.jpg){.aligncenter size-medium}

## G-code

With everything working correctly, we now need to make sure these M8 and M9 g-code commands exist within your job files to signal the IOT relay on at the start of a job and off at the end.

The easiest way to do this is to manually insert this code yourself. To do this, open your g-code in a text editor such as Notepad and:

<ul>
  <li>Start a new line at the top and type in “M8”</li>
  <li>Scroll to the last line of the code, start a new line and type in “M9”</li>
  <li>Save the g-code file with a new name in case you need to go back later to check the original</li>
</ul>

Manual replacement can get old quick, so other methods exist to automate this process every time. Firstly, some CAM programs will allow you to 'inject' whatever g-code you'd like before and after (referred to as the "header" and "footer" of the g-code) the main code, for example Kiri:Moto or Fusion360. If you set up your CAM program to put M8 in the header and M9 in the footer then those commands will now always be there for any project you design and output into g-code.

Another option if you're using CNCjs is to set up custom 'Events':

<ol>
  <li>Go to Settings (gears on the left) ➜ Events, and add a new event for the both commands</li>
  <li>Use events “G-code: Start” for the M8 command and “G-code: Stop” for M9</li>
</ol>

This will now 'inject' the M8 command at the start of any g-code file and an M9 at the end. It applies to every file you run unless you disable them.

![](/_images/_longmill/_advanced/_6_IOTRelay/lm_IOT_p6_Event.png){.aligncenter size-medium}

With your relay hooked up, you now got a pretty serious CNC setup! Go out and leverage this new-found power to make great things and remember to stay safe :)

## Troubleshooting

Occasionally, we've heard of a particular situation happening where after everything is wired up it's possible to enable and disable the IOT relay manually via the M8 and M9 commands but when you go to run a file with M8 at the start and M9 at the end the program doesn't run and the CNC just sits motionless. We're still not fully certain on what the cause of this problem is but we've heard from LMers that increasing the gauge of wire going from the LongBoard to the relay, decreasing the distance between the board and the relay, and using a separate breaker circuit from the LongMill itself to run the relay are all options that have previously remedied the issue.
