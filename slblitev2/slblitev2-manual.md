---
title: Technical Manual
menu_order: 3
post_status: draft
post_excerpt: In depth functionality of the SLB-LITE / SLB-EXT V2 
post_date: 2024-04-03 16:44:00
taxonomy:
    knowledgebase_cat: slblitev2-handbook
    knowledgebase_tag:
        - slblitev2
custom_fields:
    KBName: SLB-LITE / SLB-EXT V2
    basepress_post_icon: bp-caret-right
skip_file: no
featured_image: _images/_superlongboard/slb_slb-leds.jpg
---

## 

### Status Lights

On the controllers, there are 12 LEDs in a circle that will automatically light up and animate based on the machine's current state. Below is a chart listing the colour and animation for each state, and what the states mean. You may find it helpful in understanding how the machine responds and processes commands. If the machine is not in Idle state, you may need to clear or wait until the current state has elapsed to process other commands. For example, if the machine is in Homing, you won't be able to jog the machine until the homing process is completed. If the machine is in Alarm, then the alarm needs to be cleared to proceed.

| State           | Description                                                         | Colour & Animation                              |
|-----------------|---------------------------------------------------------------------|-------------------------------------------------|
| Idle            | Machine ready, waiting for commands                                 | Solid white                                     |
| Cycle / Running | G-code is running, like a job or a macro                            | Solid green                                     |
| Jogging         | Machine is jogged                                                   | Green comet with short bright head and dim tail |
| Hold            | Job is paused                                                       | Full-ring yellow pulse between dim and bright   |
| Safety Door     | Spindle and coolant disabled, waiting on switch to close (advanced) | Alternating yellow half-ring blink              |
| Homing          | Homing is in progress                                               | Mirrored blue sweep from opposite sides         |
| Check Door      | Safety door detected as opened, door state initiated (advanced)     | Rotating cyan checkerboard                      |
| Alarm           | An alarm is triggered                                               | Red chase with fading tail                      |
| E-stop          | E-stop is triggered                                                 | Full-ring red blink                             |
| Tool Change     | Tool change is in progress                                          | Rotating magenta dotted pattern                 |
| Sleep           | De-energizes motors, spindle and coolant until reset                | Solid grey                                      |

### E-stop

In previous controllers (SLB / SLB-EXT) when the E-stop was triggered, power was cut to the motors, requiring a power cycle at the controller to restore functionality. With the SLB-LITE / SLB-EXT V2, the E-stop now works a bit differently.

The E-stop is designed to turn OFF 1) the enable signals for the motors, and 2) both the enable and PWM signals for the spindle/laser, completely shutting down these components. This functionality is controlled by the E-stop signal, which responds to these four (4) inputs:

- The physical, NC (normally closed) E-stop button that's installed on top of the enclosure
- An input for an optional, NO (normally open) E-stop button; this is useful if the controller is mounted far away from the machine/user
- A power monitoring feedback loop
  - Incoming voltage is checked by the protection chip (LM5060)
  - If voltage is within an acceptable range, power is delivered as normal and the controller sends the "power good" PGOOD signal
  - Otherwise, in cases of undervoltage, overvoltage or overcurrent, the chip cuts power to the controller, and the PGOOD signal turns OFF, thus triggering the E-stop
- STP pin connected to GND on the expansion board; this is useful for hooking up a sensor that needs to trigger an E-stop, e.g. spindle overheat sensor

### Motors and Limit Switches

The SLB-LITE / SLB-EXT V2 has four (4) connections allotted for the X, Y1, Y2, Z and A-axis, as well as limit switches on each axis. They use NEMA 23 closed loop motors with external drivers.

Limit switches are inductive-style, with 5V/Sig/GND signals.

Generally, these controllers support motors requiring 24-48V, with STEP/DIR/EN/AL signals, either closed or open loop with external drivers. However the biggest hurdle to using these controllers for 3rd party CNCs is the custom wiring, as the motor and limit switch on the controller end are integrated Molex connectors (Molex MicroFit 3.0 2x7P).

if they want to use on another machine buy the closed loop steppers with our cables to ensure compatibility.

For more powerful motor setups use SLB-EXT V2, gotta figure out their own cables.

motor connector adapters? tbd. for slb-ext -> v2

### Spindle

spindle -> one port for both rs485/pwm

### file transfer

SD?
usb cable -> can get better one, twisted shielded

### ring rail

similar to past controller
