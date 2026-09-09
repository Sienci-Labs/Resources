---
title: SLB-LITE
menu_order: 3
post_status: publish
post_excerpt: Resources and documentation for the LongMill MK3 CNC.
post_date: 2026-05-19 15:38:22
taxonomy:
    knowledgebase_cat: lmk3-the-basics
    knowledgebase_tag:
custom_fields:
    KBName: LongMill MK3
    basepress_post_icon: bp-caret-right
skip_file: no
featured_image: _images/post-image.jpg
---

## Background

The SLB-LITE is the next evolution of first generation SLB (SuperLongBoard) controllers. They were designed from the ground up, using architecture and principles that have proven to be reliable in the original SLB platform. Notable features and changes include:

- Use of a modern RP2350 microcontroller with better reliability, easier flashing, and better driver support
- A much more compact form factor, and robust enclosure
- Modular design for expansion of IO, making controllers simpler and cheaper for those that don’t need it, and more expandable for those that do
  - [Expansion board](#expansion) includes connections for ATC, ethernet and auxiliary
- Unified motor signal, motor power, and limit switches into one single locking connector and cable

## Technical Specifications

### Features List

- 32-bit RP2350 microcontroller
- EMI-resistant USB-C connectivity
- E-stop integrated into controller
- CNC status lights
- Overrides
- TLS input (3 pin connection)
- Spindle control via PWM signal or MODBUS communication, with automatic hardware detection
- Laser control via PWM signal
- UF2 flashing with drag and drop files into a USB device
- X, Y, Z, A axis control with individual control of dual Y-axis motors
- Differential signal control for motor outputs, compatible with integrated closed loop stepper motors or external motor drivers using STEP/DIR control.
- 24-48V DC input power
- Integrated RGB LEDs indicate machine status, with external outputs for additional RGB strips

### Inputs & Outputs

#### Power

- SLB-LITE controller uses a 5.5mm OD, 2.1mm ID barrel jack (24-48V, 4A)

#### Motors & Limit Switches

- A unified Molex MicroFit 3.0 2x7P connector is used to interface all connections for motors and limit switches
- Motor power (24-48V), STEP/DIR/EN/AL signals for motor, 5V/Sig/GND for limit switches

#### Accessories

- Tool length sensor input uses Phoenix-style 3.81-3P pluggable terminal connector (5V, NC input)
- Probe/Touchplate input uses Phoenix-style 3.81-2P pluggable terminal connector (NO input)
- Auxiliary output uses Phoenix-style 3.81-2P pluggable terminal connector (5V output)
- Laser output uses Phoenix-style 3.81-2P pluggable terminal connector (5V PWM output)
- Ring LED output uses JST XHP-3P connector (5V, Neopixel Signal Output)
- Rail LED output uses JST XHP-3P connector (5V, Neopixel Signal Output)
- Optional external E-stop uses a Phoenix-style 3.81-2P pluggable terminal connector (NO input)

#### Connectivity

- Primary serial connection to controller uses USB-C connector
- MicroSD card slot for local file storage and macro functionality

#### Spindle/Router

- A unified RJ12 connector is used to interface PWM and MODBUS communication - with routers and VFDs/spindles
- Pins 5 (GND) and 6 (PWM) provide 5V PWM control used with AutoSpin T1 or VFDs using PWM control scheme. Pin 1 is used to automatically detect when a PWM device is plugged into the connector (when shorted to pin 5)
- Pins 3 (A) and 4 (B) provide serial communication via MODBUS, with pin 5 (GND) available as an optional, recommended ground point.

#### Expansion

- A 2x13P 2.54mm pitch header male connector is used to connect with an optional expansion board for adding additional capabilities to the controller.
- The expansion system is designed to efficiently utilize serial communication to provide a high number of external IO and auxiliary control. The expansion port on its own is not intended to be used for application-specific controls but this is possible. This includes the following IO/features:
  - 5V power output
  - 24-48V power output (from the input power supply)
  - UART, I2C and SPI serial communication
  - Neopixel LED control output
  - External E-stop input
  - Spindle enable output
  - Ethernet interface
  - Several spare pins, configurable in firmware
