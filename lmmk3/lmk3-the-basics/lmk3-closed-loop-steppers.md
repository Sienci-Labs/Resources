---
title: Closed Loop Stepper Motors
menu_order: 5
post_status: publish
post_excerpt: 
post_date: 2026-05-19 15:39:33
taxonomy:
    knowledgebase_cat: lmk3-the-basics
    knowledgebase_tag:
custom_fields:
    KBName: LongMill MK3
    basepress_post_icon: bp-caret-right
skip_file: no
featured_image: _images/post-image.jpg
---
## Closed vs Open Loop Stepper Motors

The LongMill MK3 uses closed loop stepper motors, an upgrade from previous LongMill versions which came with open loop motors.

Closed loop stepper motors offer many advantages over a regular open loop stepper motor. An open loop stepper motor is the most common, inexpensive type of stepper motor. These are typically found in 3D (and 2D!) printers, CNC machines, and some robotics applications.

With **open loop motors**, a command is sent to the motor driver, and the motor driver tells the motor to move some amount. Whether or not the motor actually moves that exact amount is unknown to the rest of the system. If there is some sort of resistance, disturbance, or obstacle in the way that prevents the motor from spinning its intended amount, the motor will **‘skip steps’** and we’ll essentially lose track of where we think the motor is.

With **closed loop motors**, a command is sent to the motor driver, and the motor driver tells the motor to move some amount, while simultaneously monitoring the position of the motor using a sensor. If the motor position is **lagging behind** where it is expected to be, the motor will receive more power to ensure that the motor gets to the specified position without any skipping. In the case where the motor is somehow obstructed from spinning entirely, it will enter an **‘Alarm’** state and shut off power to prevent any damage. The motor driver will communicate back to the machine controller to let it know that something has gone wrong, and the controller can halt the entire system to prevent any sort of damage.

Asides from no potential for loss of position, there are a few other benefits of closed loop stepper motors:

- More efficient operation when idle since extra power is only used if some torque is applied to the motor’s shaft and the motor must react to maintain its position
- More efficient operation overall, since the motor will only use as much power is needed to move
- Less heat buildup in the motor since idle and operational efficiency is improved
- Less noisy
- Faster maximum running speeds

## LongMill MK3 Motor Specifications

- NEMA 23 closed loop motors, 1.2NM on all axes
- 1/16 microstepping (800 pulses/rev)

![](/_images/_lmmk3/_the-basics/lmk3_closed_loop_steppers-drawing.jpg){.aligncenter .size-medium}

### Microstepping

Closed loop stepper motors function by receiving a certain number of ‘step’ pulses from the controller which ultimately determines how much and how fast the motor the spin. ‘Microstepping’ is a setting/configuration which will ultimately determine how much the motor spins for a given number of pulses or ‘steps’ sent to the motor.

By default all the motors are set to use 1/16 microstepping, with the DIP switches at the rear of the motor set to 1-Down 2-Down 3-Up 4-Up 5-Up.

    Do not adjust DIP switches if you’re not sure what microstepping is, or if you do not have a reason to change them. 
    
The first switch #1 is only used to invert the direction of the motor if needed. The table in the [drawing above](#longmill-mk3-motor-specifications) shows the various switch positions for a given microstepping value.
