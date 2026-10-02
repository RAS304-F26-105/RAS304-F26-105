---
title: Team Block Diagram
---

# Team Block Diagram

## Handheld LiDAR Accessibility Aid

The team block diagram shows the overall embedded-system architecture for the **Handheld LiDAR Accessibility Aid**. The system is divided into five boards: the Data Collection Board, Laser / Scanning Board, Trigger Board, Interpretation Board, and Power Board.

Each board is responsible for a specific part of the system while communicating with the other boards through the defined ribbon-cable and power connections.

## Team Block Diagram

![Team Block Diagram](../image/lidar-team-block-diagram.png)

**Figure 1:** Team-level block diagram for the Handheld LiDAR Accessibility Aid.

## Board Organization

### Data Collection Board

**Team member:** Khun Oo

The Data Collection Board coordinates the collection of LiDAR scan data and scan position information. The board contains the main microcontroller and three UART connections:

- UART1 TX/RX
- UART2 TX/RX
- UART3 TX/RX

The board collects and buffers samples before passing the appropriate information to the other subsystems.

**Connection:**
- J1 — Data Collection ↔ Trigger
- J2 — Data Collection ↔ Laser / Scanning
- J3 — Data Collection ↔ Interpretation

---

### Laser / Scanning Board

**Team member:** William Layja

The Laser / Scanning Board is responsible for the LiDAR scanning system. The board contains the LiDAR module, scan motor driver, and main scan motor.

The LiDAR module provides range and scan information to the microcontroller. The scan motor driver controls the main scan motor used during scanning.

**Connection:**
- J2 — Laser / Scanning ↔ Data Collection

---

### Trigger Board

**Team member:** Isaiah Cruz

The Trigger Board provides the user input that initiates a scan. The board contains a trigger switch connected to the microcontroller.

The trigger switch provides the digital input used for debounce and the scan request.

**Connection:**
- J1 — Trigger ↔ Data Collection

---

### Interpretation Board

**Team member:** Mohammed Al Rasbi

The Interpretation Board processes the collected information and provides user feedback. The board includes audio and vibration outputs.

The current design includes:

- Audio amplifier
- Speaker
- Vibration driver
- Small vibration motor
- UART communication
- Audio output / motor PWM-enable signal

The board is responsible for obstacle interpretation and providing audio and vibration alerts to the user.

**Connection:**
- J3 — Interpretation ↔ Data Collection

---

### Power Board

**Team member:** Jose Baldenegr

The Power Board distributes power to the other boards and provides the required voltage rails.

The power system consists of:

- Battery pack
- Protection / switch
- Voltage regulators
- Power distribution

The Power Board provides separate power connections to the other boards:

- P1 — Data Collection
- P2 — Laser / Scanning
- P3 — Trigger
- P4 — Interpretation

The diagram identifies the power distribution as including the required VLOGIC, VSENSOR, VMOTOR, VAUDIO, VIB, and common ground connections.

## Communication Connections

The team uses 8-pin ribbon cable connectors for communication between the embedded system boards.

The current proposed cable pinout is:

| Pin | Function |
|---|---|
| 1 | Collection TX / remote RX |
| 2 | Collection RX / remote TX |
| 3 | NC |
| 4 | NC |
| 5 | NC |
| 6 | NC |
| 7 | NC |
| 8 | GND |

The diagram specifies that RX# connections are treated as GPIO placeholders until the final microcontroller pin assignments are determined.

The ribbon connections terminate at the microcontrollers. Sensors and actuators do not connect directly to the ribbon cable.

## Power Connections

The Power Board provides dedicated power connections to each subsystem.

| Connection | Board | Power |
|---|---|---|
| P1 | Data Collection | VLOGIC / GND |
| P2 | Laser / Scanning | VLOGIC / VSENSOR / VMOTOR / GND |
| P3 | Trigger | VLOGIC / GND |
| P4 | Interpretation | VLOGIC / VAUDIO / VIB / GND |

The power connections are shown as red lines in the team block diagram. The black lines represent signal or internal power-board connections.

Power does not use the UART ribbon connections. All boards share ground.

## System Communication Flow

The system operates through the following general sequence:

1. The user activates the trigger switch.
2. The Trigger Board sends a scan request to the Data Collection Board.
3. The Data Collection Board communicates with the Laser / Scanning Board.
4. The Laser / Scanning Board collects LiDAR range and scan information.
5. The Data Collection Board collects and buffers the scan samples.
6. The collected information is sent to the Interpretation Board.
7. The Interpretation Board interprets the detected obstacle information.
8. Audio and vibration alerts provide feedback to the user.

## Design Notes

The current block diagram is a working design and will be updated as the individual boards are developed.

Microcontroller selections, manufacturers, part numbers, GPIO assignments, peripheral details, voltage rails, current ratings, and other component specifications marked as TBD will be finalized as the individual subsystem designs progress.

The team will maintain consistency between the individual block diagrams and this team-level block diagram.

## Block Diagram Source File

[Download the Team Block Diagram Source File](../drawio/lidar-team-block-diagram.drawio)

## References

- RAS 304 Embedded Systems Design — Team Block Diagram Assignment
