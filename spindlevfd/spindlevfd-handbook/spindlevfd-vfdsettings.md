---
title: VFD Settings
menu_order: 2
post_status: publish
post_excerpt: Documentation on default VFD settings and how to change them.
post_date: 2026-06-02 15:09:42
taxonomy:
    knowledgebase_cat: spindlevfd-handbook
    knowledgebase_tag:
        - spindlevfd
custom_fields:
    KBName: Spindle VFD
    basepress_post_icon: bp-caret-right
skip_file: no
featured_image: 
---

The Sienci Labs spindle kits come with the VFD pre-programmed, so in most cases you do not need to modify the VFD settings.

However if you are experiencing issues running your VFD, it is possible one of the VFD settings is incorrect. **We advise contacting Sienci Labs Customer Support before unlocking and changing any of the parameters on the VFD.**

The VFD unit comes ‘locked’ to prevent accidental changes that will affect your spindle kit’s functionality. Below, we’ll go over how to unlock it, should you need to make any changes.

## Unlock VFD

To unlock the VFD parameters to allow changes to be made, you’ll first need to modify one parameter, or ensure this is already set to allow changes:

Navigate to the parameter ‘F000’, then press the UP or DOWN buttons to set this value to 0, then press ‘SET’ to save this.

## Change VFD Parameters

To modify values, press the ‘SET’ button to enter the parameter selection screen. Here, you’ll see parameters ranging from F000 to F199. Use the UP and DOWN buttons to select the parameter you’d like to modify, then press ‘SET’ to select that parameter.

Once in the parameter you’d like to change, use the UP and DOWN buttons to modify this. When done, press ‘SET’ again, to save the value and exit the parameter modification screen. If you’d like to exit the screen without saving the modified parameter, press the ‘ESC’ button instead.

![](/_images/_spindlevfd/_spindlevfd_handbook/spindlevfd_vfdbuttons.jpg){.aligncenter .size-medium}

See these lists of parameters for the Sienci Labs Spindle Kit:

- [2.2KW VFD Parameters List](https://resources.sienci.com/wp-content/uploads/2026/03/Sienci-Labs-Spindle-Kit-VFD-Default-Values-Sienci-Labs-2.2kW-Spindle-Kit-VFD-Default-Value.pdf)
- [1.5KW VFD Parameters List](https://resources.sienci.com/wp-content/uploads/2026/03/Sienci-Labs-Spindle-Kit-VFD-Default-Values-Sienci-Labs-1.5kW-Spindle-Kit-VFD-Default-Value.pdf)

**Parameters which should NEVER be changed have been highlighted in <span style="color:red">RED</span>. Do not modify these unless instructed to. Any damage resulting from changes to these parameters is not covered by warranty to this spindle kit.**

Parameters highlighted in <span style="color:blue">BLUE</span>. are the most important parameters to verify.

## PWM Control on Sienci Labs Spindle Kit

While the Sienci Labs spindle kit is set up by default for control using RS485 serial communication, it is possible to use PWM (pulse width modulation) to control the operation and speed of your spindle instead. This can be useful if you’re having trouble using RS485 communication for any reason, or if you’re setting up this kit on a machine that does not have RS485 communication capability.

To set up control for machines such as the AltMill or LongMill, you’ll want to set these parameters on your VFD panel, following the process described above:

| Parameter | Value | Name of Parameter           | Description                                                   |
|-----------|-------|-----------------------------|---------------------------------------------------------------|
| F001      | 1     | Control mode                | Sets external input terminal to trigger run/stop of spindle   |
| F002      | 1     | Frequency setting selection | Sets spindle speed to be controlled in the Al1 input terminal |
| F070      | 1     | Analog input selection      | Designates Al1 input to use a 0-5V control signal             |

## Manual Control on the Sienci Labs Spindle Kit

You can control the spindle manually using the front panel of the VFD, and adjust the speed using the small knob.

To set up manual control for machines such as the AltMill or LongMill, you’ll want to set these parameters on your VFD panel, following the process described above:

| Parameter | Value | Name of Parameter           | Description                                                   |
|-----------|-------|-----------------------------|---------------------------------------------------------------|
| F001      | 0     | Control mode                | Sets panel buttons to trigger run/stop of spindle             |
| F002      | 3     | Frequency setting selection | Sets spindle speed to be controlled by the potentiometer/knob |

## Auto Control on the Sienci Labs Spindle Kit

To reenable or set auto control,  you’ll want to set these parameters on your VFD panel, following the process described above:

| Parameter | Value | Name of Parameter           | Description                                                   |
|-----------|-------|-----------------------------|---------------------------------------------------------------|
| F001      | 2     | Control mode                | Sets panel buttons to trigger run/stop of spindle             |
| F002      | 2     | Frequency setting selection | Sets spindle speed to be controlled by the software           |
