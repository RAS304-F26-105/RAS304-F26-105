---
title: Team Block Diagram
---

## Introduction

The team block diagram shows how the individual embedded system boards will communicate with each other. Each team member is responsible for a subsystem that includes a microcontroller, sensors and/or actuators, and the required communication connections.

The team is using a hub/spoke connection layout to organize communication between the individual boards. The 8-pin ribbon cable connectors are used for communication between the microcontrollers, with Pin 8 reserved for ground.

## Team Block Diagram

![Team Block Diagram](../image/team-block-diagram.png)

**Figure 1:** Team-level block diagram showing the embedded system subsystems and connections between team members.

## Team Members

### William Layja

William's subsystem is represented as an individual board within the team block diagram. The subsystem will be updated with its microcontroller, peripherals, sensors, actuators, and communication assignments as the design is finalized.

### Khun Oo

Khun's subsystem uses a **Microchip PIC18F57Q43 Curiosity Nano** microcontroller.

The current subsystem includes:

- Digital I/O
- ADC1
- ADC/Digital connections
- Button 1
- Button 2
- DAC1
- Light Sensor
- Op Amp
- Ribbon cable connectors

### Mohammed Al Rasbi

Mohammed's subsystem uses a **Microchip PIC18F57Q43 Curiosity Nano** microcontroller.

The current subsystem includes:

- Button 1
- H-Bridge
- Motor
- ADC1
- ADC2
- PWM
- Red LED
- Microphone
- Op Amp
- Ribbon cable connectors

### Jose Baldenegro
Jose Baldenegro's subsystem uses a **Microchip PIC18F57Q43 Curiosity Nano** microcontroller.

The current subsystem includes:

- Button 1
- H-Bridge
- Motor
- ADC1
- ADC2
- PWM
- Red LED
- Microphone
- Op Amp
- Ribbon cable connectors

### Isaiah Cruz

Isaiah's subsystem uses a **Microchip PIC18F57Q43 Curiosity Nano** microcontroller.

The current subsystem includes:

- Button 1
- H-Bridge
- Motor
- ADC1
- ADC2
- PWM
- Red LED
- Microphone
- Op Amp
- Ribbon cable connectors

### place holder (PH)

PH's subsystem is represented as an individual board within the team block diagram. The subsystem will be updated with its microcontroller, peripherals, sensors, actuators, and communication assignments as the design is finalized.

## Ribbon Cable Connections

Each board uses an 8-pin ribbon cable connector for communication with the other team members.

| Pin | Function |
|---|---|
| 1 | Team communication signal |
| 2 | Team communication signal |
| 3 | Team communication signal |
| 4 | Team communication signal |
| 5 | Team communication signal |
| 6 | Team communication signal |
| 7 | Team communication signal |
| 8 | Ground |

Pins 1–7 will interface with the appropriate microcontroller GPIO or peripheral pins. Pin 8 is reserved for ground.

The specific pin assignments will be updated as the individual subsystem designs are finalized.

## Communication Layout

The team block diagram uses the hub/spoke format to organize the connections between the individual embedded system boards. The diagram identifies the boards, ribbon cable connectors, and the communication paths between the subsystems.

The block diagram will be updated throughout the semester as the individual subsystem designs and communication requirements are finalized.

## Block Diagram Source

[Download the Team Block Diagram](../drawio/team-block-diagram.drawio)

## Design Updates

This block diagram is a living document and will be updated as the team's embedded system design develops. Changes to microcontrollers, sensors, actuators, GPIO assignments, peripheral connections, and ribbon cable signals will be reflected in the diagram.

## References

- RAS 304 Embedded Systems Design — Team Block Diagram Assignment
