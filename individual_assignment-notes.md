# Marking criteria

## Development of IoT Node setup and Application

An IoT Node typically consists of a microcontroller platform, some sensor(s) and/or actuator(s) combination, and a method to communicate with an edge device. The IoT Node should satisfy the following:

* Involve at least 1 analog and 1 digital sensor
* Involve 2 actuators (e.g., LEDs, servomotor/motor, relay, solenoids etc. )
* Have a working sketch to facilitate Input/Output and serial communications
* Have described each sensor, actuator, code, detailing how each component works and how it is integrate with the Arduino

| Pts | Description                                                                                                                                                                         |
|-----|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| 0   | There is no implementation.                                                                                                                                                         |
| 5   | IoT project is a modest extensions of the tutorials, partial implementation, or not working, meets at least 1 criteria.                                                             |
| 10  | IoT project is a moderate extension of the tutorials: Novel implementation which uses a combination of some original work and tutorial tasks. fully working, meets 2 or 3 criteria. |
| 15  | Exploratory IoT project implementation: demonstrable and fully working IoT project, uses some implementation from tutorials, satisfies 3 criteria, (or equivalent).                 |
| 20  | Novel, inventive IoT project implementation: exceptional, demonstrable, and fully working project, significant extension of tutorial tasks, satisfies all 4 criteria.               |

## Serial Communication

As we have studied in this unit, sending and receiving data over the serial port between IoT node and edge device is the backbone of an IoT application. The developed communication component in this assignment should include:

* Transmit serial data from IoT node to edge device, so the values recorded by the connected IoT sensors can be sent through a serial port
* Transmit serial data from edge device to IoT node, so the commands from the edge device can trigger actuators connected to the IoT node

| Pts | Description                |
|-----|----------------------------|
| 0   | No attempt                 |
| 5   | Satisfies 1 requirement.   |
| 10  | Satisfies all requirements |

## Database implementation and simple analytics

Develop a database to record input-output data with simple analytics. The implementation should satisfy the following:

* Have created a database
* Database is able to save the data read from the sensors
* includes simple conditional rules to trigger notification OR actuator on the IoT Node
* Conditional rule is changeable programatically/using the dashboard

| Pts | Description              |
|-----|--------------------------|
| 0   | No attempt               |
| 5   | Satisfies 1 criteria     |
| 10  | Satisfies 2 criteria     |
| 15  | Satisfies 3 criteria     |
| 20  | Satisfies all 4 criteria |

## User interface

User interface is the last component of your Assignment-1 and could be implemented in the form of a web/mobile interface. The user interface should satisfy the following criteria:

* A simple application hosted on a webserver service on the edge device
* The user interface displays your project relevant data from the database
* Appropriate visualisation is used to make the displayed data readable
* User's can interact with an actuator connected to the IoT node OR trigger alerts on the IoT node by changing the conditional rule from the user interface.

| Pts | Description                        |
|-----|------------------------------------|
| 0   | No attempt                         |
| 5   | Satisfies 1 criteria or equivalent |
| 10  | Satisfies 2 criteria or equivalent |
| 15  | Satisfies 3 criteria or equivalent |
| 20  | Satisfies all 4 criteria           |

## Report

* Project summary describes a well-defined IoT application including description of IoT node, edge device, and user interface
* Contains conceptual diagram of the implementation with description of system hardware, software and operation
* Resources and appendices are well organised and relevant to the project
* The document is well formatted, free of grammatical errors, and due credits are given using citations where necessary

| Pts | Description                        |
|-----|------------------------------------|
| 0   | No marks                           |
| 5   | Satisfies 1 criteria or equivalent |
| 10  | Satisfies 2 criteria or equivalent |
| 15  | Satisfies 3 criteria or equivalent |
| 20  | Satisfies all 4 criteria           |

## Video

* Video clearly shows and describes the developed project and all its components
* Video clearly shows and describes the functioning of the entire system

| Pts | Description             |
|-----|-------------------------|
| 0   | No marks                |
| 5   | Satisfies 1 criteria    |
| 10  | Satisfies both criteria |