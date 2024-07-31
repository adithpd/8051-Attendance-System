## Overview

This README provides detailed information about the Fingerprint (R305) Based Attendance System using an 8051 microcontroller. The system uses a fingerprint sensor module (R305) to authenticate users and maintain attendance records. This document includes the project description, components used, circuit diagram, and the steps to set up and operate the system.

## Project Description

The Fingerprint (R305) Based Attendance System is designed to record attendance using biometric authentication. Each user registers their fingerprint, and upon placing their finger on the sensor, the system verifies their identity and logs their attendance.

### Connections

1. **8051 Microcontroller:**
   - Connect Vcc and GND to the power supply.
   - Connect the crystal oscillator to XTAL1 and XTAL2.
   - Connect the fingerprint sensor's TXD and RXD to the microcontroller's RXD and TXD pins respectively.
   - Connect the LCD data pins to the microcontroller's port pins.
   - Connect push buttons to designated pins for enrollment and deletion.

2. **Fingerprint Sensor (R305):**
   - Vcc to 5V power supply.
   - GND to ground.
   - TXD to RXD pin of 8051.
   - RXD to TXD pin of 8051.

3. **LCD Display:**
   - Connect data pins to Port 2 of 8051.
   - Connect control pins RS, RW, and E to Port 1 of 8051.

## Setup Instructions

1. Assemble the circuit on a breadboard or PCB as per the circuit diagram.
2. Ensure all connections are secure and correct.
3. Load the program onto the 8051 microcontroller using an appropriate programmer.
4. Power up the circuit.

## Usage

1. **Enrollment:**
   - Press the enrollment button.
   - Place your finger on the fingerprint sensor when prompted.
   - The LCD will display a message indicating successful enrollment.

2. **Attendance Logging:**
   - Place your registered finger on the fingerprint sensor.
   - The system will verify the fingerprint and log the attendance.
   - The LCD will display a message indicating successful attendance logging.

3. **Deletion:**
   - Press the deletion button.
   - Follow the prompts on the LCD to delete a registered fingerprint.

## Code Overview

### Main Program

- **Initialization:** Set up the microcontroller, initialize the LCD, and configure UART for communication with the fingerprint sensor.
- **Enrollment:** Code for enrolling new fingerprints.
- **Verification:** Code for verifying fingerprints and logging attendance.
- **Deletion:** Code for deleting registered fingerprints.

### Functions

- **LCD Display Functions:** Functions to initialize and display messages on the LCD.
- **Fingerprint Sensor Functions:** Functions to communicate with the R305 sensor for enrollment, verification, and deletion.
- **UART Communication:** Functions to handle UART communication between the 8051 and the R305 sensor.

## Troubleshooting

- **Fingerprint Not Recognized:**
  - Ensure the finger is placed correctly on the sensor.
  - Re-enroll the fingerprint if necessary.

- **LCD Not Displaying Properly:**
  - Check the connections between the LCD and the microcontroller.
  - Ensure the LCD initialization code is correct.

- **No Communication with Fingerprint Sensor:**
  - Verify the TXD and RXD connections.
  - Check the baud rate settings in the code.
