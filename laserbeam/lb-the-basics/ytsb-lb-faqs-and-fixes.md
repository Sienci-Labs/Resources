---
title: ytsb FAQ
menu_order: 7
post_status: draft
post_excerpt: 
post_date: 2021-12-23 12:56:20
taxonomy:
    knowledgebase_cat: lb-the-basics
    knowledgebase_tag:
        - laser
custom_fields:
    KBName: LaserBeam
    basepress_post_icon: bp-caret-right
skip_file: yes
featured_image: 
---

<h2>Compatibility</h2>
<b>Is the laser driver necessary if we are upgrading to the SLB? </b>

Yes, you still need the laser driver. The SLB does NOT replace the driver or power supply needed to run the LaserBeam.

The laser driver is responsible for drawing power from the laser power supply and converting that power to a specific voltage and constant current that your laser can understand in order to fire. The driver is also needed to relay the control signals, which tell the laser when to turn off and on and at what power to fire.

<b>Is the LaserBeam compatible with the LongMill or AltMill CNC? </b>

The LaserBeam is compatible with all versions of the LongMill and AltMill, with their respective control boards (LongBoard, SLB, SLB-EXT).

For the AltMill, you will need to reduce the maximum speeds ($110 and $111) to 5000 mm/min to efficiently run the LaserBeam, which is lower than the default settings. This can be changed in the Firmware tool on gSender. Furthermore, if you wish to run all the wiring through the drag chain you may need longer cables which can be purchased soon from our store. Otherwise shorter cables can be run outside of the drag chain, fastened with zip ties.

<b>Does the LaserBeam work with the Vortex Rotary Axis?</b>

Yes, the LaserBeam works with the Vortex. Check out the laser mount page <a href="https://resources.sienci.com/view/lb-manual-vortex-riser-mount/">here</a>.

<strong>Is the Magnetic Mount compatible with the Sienci Labs Spindle and Dust Shoe Kit?</strong>

The Magnetic Mount can be attached while the spindle is in the router mount. However, the dust shoe and Magnetic Mount cannot be on at the same time.

<b>Will other brands of lasers work on my LongMill?</b>

Yes. The LongBoard controller has a 5V PWM signal output for lasers, spindles and other accessories. You can reach out to the company who makes it to ensure their driver will be able to read the signal.
<h2>Operation and Safety</h2>
<b>Is fume extraction or ventilation required when running the LaserBeam?</b>

Yes, you'll want to run your LaserBeam in a space with great ventilation and/or consider a fume extraction system. This can mean a well ventilated work area with open doors or windows, or an inline fan and ducting for extracting the smoke outside. Fumes and particulates from engraving or cutting can be harmful. You always want to make sure the material you are using is laser safe and that you know what type of coatings the material has to avoid hazardous fumes.

<b>Should the LaserBeam be removed when running the router?</b>

Yes, the LaserBeam should be removed when running the router. The vibrations of the LongMill when cutting into wood can cause the laser lens to slowly loosen and fall out of the aluminum heat sink. The LaserBeam mount was designed for easy attachment and removal for this reason.

<b>Can the LaserBeam be used while the dust shoe is on?</b>

No, the dust shoe should never be installed while the LaserBeam is operational. It creates a fire hazard as the bristles of the dust shoe can melt and/or cause a fire. The dust shoe is made to be used when running the router, not for use with the LaserBeam.

<b>Can the LaserBeam engrave on metals?</b>

Generally no, diode lasers are not powerful enough to engrave on metal materials. However, certain metals are coated in a protective layer or paint, which allows the laser to etch away, creating an engraved effect. Stainless steel is commonly engraved in this way to make projects such as tumblers or water bottles. Alternatively there are Metal Marking Sprays that allow you to coat your material and etch away the coating with the laser to reveal your chosen design. Multiple passes may be required to achieve your desired effect.

<b>Will the laser safety glasses fit over my regular glasses?</b>

Yes, the LaserBeam safety glasses were designed specifically to fit over prescription glasses. Check out the full description of our safety glasses <a href="https://resources.sienci.com/view/lb-laser-safety-glasses/">here</a>. <b>Remember to wear your safety glasses at all times while operating the LaserBeam system. </b>
<h2>Software</h2>
<b>Is the LaserBeam compatible with Vectric software?</b>

Yes, Vectric offers a laser module that is compatible with the LaserBeam. You can download a free trial version of the module<a href="https://www.vectric.com/products/laser-module?gclid=Cj0KCQjwmICoBhDxARIsABXkXlK2SZ-TIMtue_TR3c3ZGYVSaUy8xh_lQ2yVAF2c5YoGu0oxZBQ2oQYaAsaeEALw_wcB"> here</a>.

Disclaimer: We don't offer support with the Vectric Laser module, but we know it works. Vectric is a great company and they have tons of tutorials and resources available.

<b>What software will I need to run my LaserBeam?</b>

We recommend using Lightburn and gSender. You can explore more options<a href="https://resources.sienci.com/view/choosing-laser-software/"> here</a>.
<h2>Orders and Shipping</h2>
<b>Does the LaserBeam ship together with the LongMill or AltMill if I order both at the same time?</b>

The LaserBeam always ships separately from the machine. You may receive one package before the other even if you order at the same time. You can always check the status of your orders and our current lead times<a href="https://sienci.com/order-status/"> here</a>.

<b>I just ordered a laser, how can I get an update on when it will ship?</b>

You can check the status of your order<a href="https://sienci.com/order-status/"> here</a>.

<b>What is the lifespan of the LaserBeam?</b>

The lifespan of the LaserBeam is roughly 10 000 hours of use.

<b>Is there a warranty on the LaserBeam?</b>

The LaserBeam has a 90 day warranty once it is received. Detailed information regarding the warranty can be found<a href="https://sienci.com/product/laser/#tab-warranty"> here.</a>

<b>What comes with the LaserBeam?</b>

Here is a list of everything that comes stock with each LaserBeam system:
<ul>
  <li>Laser Diode Assembly with Air Assist &amp; Shield Attachment</li>
  <li>5A Constant Current Laser Driver</li>
  <li>12V 8A Power Supply w 6 ft AC cable</li>
  <li>Stock G2 Lens</li>
  <li>Lens Focus Ring</li>
  <li>Router Mount Hardware</li>
  <li>2pcs 7mm Lens Spring – For G2 Lens</li>
  <li>2pcs 10mm Lens Spring – For 3E, G7 or G8 Lens</li>
  <li>2pcs 13mm Lens Spring – For 3E, G7 or G8 Lens</li>
  <li>LaserBeam extension wires</li>
  <li>Lens Focus Finder set</li>
  <li>LaserBeam safety glasses with case and cleaning cloth</li>
</ul>
Check out our<a href="https://resources.sienci.com/view/lb-unboxing/"> unboxing guide</a> for a more in depth look at everything included with each LaserBeam system.
