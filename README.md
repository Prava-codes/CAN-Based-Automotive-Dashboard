# CAN-Based-Automotive-Dashboard Using PIC18F4580


## OVERVIEW

The **Automotive CAN Based Dashboard** is an embedded systems project developed using the **PIC18F4580** microcontroller and Embedded C to demonstrate communication between multiple Electronic Control Units (ECUs) using the **CAN (Controller Area Network) protocol**.

The project consists of three ECUs working together over the CAN bus. ECU1 handles vehicle Speed and Gear, ECU2 handles RPM and Indicator status, and ECU3 receives the information from the other ECUs and displays the complete vehicle status on a 16×2 Character LCD (CLCD).

This project demonstrates the practical implementation of CAN communication, ECU-to-ECU data transmission, message identification, microcontroller programming, LCD interfacing, and automotive embedded system concepts.


## OBJECTIVE

The main objective of this project is to design and implement a simple automotive dashboard system using CAN communication, where multiple ECUs exchange vehicle parameters and a central dashboard displays the received information.


## FEATURES

 - CAN-based communication between multiple ECUs
 
 - Speed monitoring
 
 - Gear position monitoring
 
 - Engine RPM monitoring
 
 - Indicator status monitoring
 
 - Real-time data transmission and reception
 
 - CAN message ID-based communication
 
 - 16×2 CLCD-based dashboard display
 
 - Modular ECU architecture
 
 - PIC18F4580 microcontroller-based implementation


## ECU'S WORKING 

### ECU1 – Speed and Gear

ECU1 is responsible for handling:

- Vehicle Speed
  
- Gear Position

The corresponding data is transmitted through the CAN bus using dedicated CAN message IDs.

### ECU2 – RPM and Indicator

ECU2 is responsible for handling:

 - Engine RPM
 
 - Indicator status

The collected information is transmitted to the dashboard ECU through CAN communication.

### ECU3 – Dashboard Display

ECU3 receives the data transmitted by ECU1 and ECU2 through the CAN bus.

It processes the received CAN messages and displays:

SPD  GER  RPM  IND

XX   X    XXXX LEFT

on the 16×2 CLCD.


##  CAN COMMUNICATION

**CAN (Controller Area Network)** is a communication protocol widely used in automotive embedded systems for communication between different ECUs.

In this project, CAN is used to exchange vehicle parameters between the ECUs.

Each parameter is assigned a unique **CAN Message ID**, allowing ECU3 to identify the type of data received.



## PROJECT WORKFLOW

1. ECU1 obtains the Speed and Gear information.
   
2. ECU2 obtains the RPM and Indicator information.

3. Each ECU prepares the corresponding CAN message.

4. Data is transmitted through the CAN bus using predefined message IDs.

5. ECU3 continuously monitors the CAN bus.

6. ECU3 identifies the received data using the CAN message ID.
    
7. The received parameters are processed.
    
8. Speed, Gear, RPM, and Indicator status are displayed on the CLCD.



## TECHNOLOGIES USED


### HARDWARE

- PIC18F4580 Microcontroller
  
- CAN communication interface
  
- 16×2 Character LCD
  
- Power Supply

- CAN-enabled nodes


### SOFTWARE

- Embedded C
  
- MPLAB IDE
  
- XC8 Compiler
  
- PIC18F4580

- CAN Protocol



## PROJECT STRUCTURE


Automotive-CAN-Based-Dashboard/


├── ECU1
│   ├── Speed related files

│   ├── Gear related files

│   └── Supporting driver files
│

├── ECU2
│   ├── RPM related files

│   ├── Indicator related files

│   └── Supporting driver files
│

├── ECU3
│   ├── Dashboard display files

│   ├── CAN message handling files

│   ├── CLCD files

│   └── Supporting driver files
│
└── README.md



## COMPILATION AND EXECUTION

1. Open the respective ECU project in MPLAB IDE.

2. Configure the project for the PIC18F4580 microcontroller.
   
3. Compile the Embedded C source files using the XC8 compiler.
   
4. Generate the required HEX files.

5. Load the HEX files into the corresponding PIC18F4580 microcontrollers using a compatible programmer.
    
6. Connect the ECUs through the CAN network.
    
7. Run the simulation.
    
8. Observe the vehicle parameters on the dashboard CLCD.


## SAMPLE OUTPUT


------------------------

 SPD GER RPM IND
 
------------------------

 60  G3  2500 LEFT
 
------------------------


The displayed values change according to the data transmitted by the respective ECUs.



## ADVANTAGES

- Demonstrates real-time ECU communication.
  
- Provides practical understanding of CAN protocol.
  
- Uses a modular multi-ECU architecture.
  
- Suitable for learning automotive embedded systems.

- Demonstrates real-time monitoring of vehicle parameters.



## APPLICATIONS

- Automotive dashboards
  
- Instrument clusters
  
- ECU communication systems
  
- Vehicle monitoring systems
  
- Automotive embedded systems

- CAN-based control and monitoring applications



## FUTURE ENHANCEMENTS

- Add vehicle temperature monitoring.
  
- Add fuel-level monitoring.
  
- Add warning and fault indication.
  
- Store vehicle parameters for analysis.
  
- Add a graphical display.
  
- Implement CAN error handling and diagnostics.



## LEARNING OUTCOMES

Through this project, I gained hands-on experience in:

- CAN communication
  
- PIC18F4580 microcontroller
  
- Embedded C programming
  
- ECU-to-ECU communication
  
- CLCD interfacing
  
- Timers and interrupts
  
- Automotive embedded system architecture



## CONCLUSION

The **Automotive CAN Based Dashboard** successfully demonstrates communication between multiple ECUs using the CAN protocol. Speed, Gear, RPM, and Indicator
information are transmitted between the ECUs and displayed on a central dashboard using a 16×2 CLCD.

This project provides practical implementation experience in **automotive communication protocols, microcontroller programming, Embedded C, and ECU-based system
design**.
