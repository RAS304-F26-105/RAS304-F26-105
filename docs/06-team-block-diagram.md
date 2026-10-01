---
title: Team Block Diagram
---

## Introduction

The team block diagram shows how the individual embedded systems boards will communicate with each other as part of the overall project. Each team member is responsible for an individual subsystem, including its microcontroller, sensors and/or actuators, and communication connections.

The diagram shows the arrangement of the team's boards and the connections between each subsystem. It also documents the ribbon cable connections and the use of the available pins between teammates' boards.

## Team Block Diagram

![Team Block Diagram](../image/team_block_diagram.png)

**Figure 1:** Team-level block diagram showing the connections between each team member's embedded system.

## Ribbon Cable Connections

The team uses the standard 8-pin ribbon cable connection between the embedded system boards. Pin 8 is reserved for ground. Pins 1–7 are assigned to the communication and control signals required between the individual subsystems.

| Pin | Function | Connection |
|---|---|---|
| 1 | TBD | TBD |
| 2 | TBD | TBD |
| 3 | TBD | TBD |
| 4 | TBD | TBD |
| 5 | TBD | TBD |
| 6 | TBD | TBD |
| 7 | TBD | TBD |
| 8 | Ground | Ground |

The specific GPIO or peripheral connection for each signal is documented in the team block diagram and the corresponding individual subsystem diagrams.

## Team Subsystems

### Team Member 1 — [Name]

**Subsystem:** [Subsystem name]

**Microcontroller:** [Microcontroller]

**Sensor/Actuator:** [Sensor or actuator]

**Function:**  
[Brief description of what this subsystem does.]

### Team Member 2 — [Name]

**Subsystem:** [Subsystem name]

**Microcontroller:** [Microcontroller]

**Sensor/Actuator:** [Sensor or actuator]

**Function:**  
[Brief description of what this subsystem does.]

### Team Member 3 — [Name]

**Subsystem:** [Subsystem name]

**Microcontroller:** [Microcontroller]

**Sensor/Actuator:** [Sensor or actuator]

**Function:**  
[Brief description of what this subsystem does.]

### Team Member 4 — [Name]

**Subsystem:** [Subsystem name]

**Microcontroller:** [Microcontroller]

**Sensor/Actuator:** [Sensor or actuator]

**Function:**  
[Brief description of what this subsystem does.]

## Communication and Connections

The connections between the individual boards are represented using directional arrows and labeled signals. Each ribbon cable connects the appropriate pins between the team members' microcontrollers.

The team-level connection arrangement is designed to minimize unnecessary interconnections while allowing each subsystem to communicate with the other required subsystems.

The team block diagram will be updated as the individual subsystem designs are developed and finalized.

## Block Diagram Source File

[Team Block Diagram draw.io Source File](../files/team_block_diagram.drawio)

## Design Updates

The team block diagram is a living document and will be updated as the embedded system design develops. Changes to subsystem hardware, communication signals, pin assignments, and board connections will be reflected in the diagram.

## References

- RAS 304 Embedded Systems Design — Team Block Diagram Assignment
