* The project makes use of an Arduino board, a Raspberry Pi (or equivalent system), edge devices and actuators
* The aim of this project is to prototype an IoT proof-of-concept
* We will demonstrate our understanding of sensors, Arduino, database component, simple edge analytics, and web interface
* The idea of this project is to send temperature data between Arduino and Raspberry
* We have a button in the Arduino circuit and when pushed, it will push the data through the USB
* Through the USB, the Raspberry has to have some Python code running to receive the data (We can use the CircuitPython Python library for this)
* Also, on the Raspberry side, we have an Apache webserver with MySQL database that can store saved temperature data. The database and webserver must be set up first before able to interact with Python code (for Python to interact with MySQL, we have to use the python3-mysqldb library)
* On the Raspberry side, we can use either a real Raspberry Pi with Raspberry OS installed, or a virtual machine on VMWare or VirtualBox that supports Serial Port (and we can use the Virtual Port Driver to create a virtual port for either VM software to use) with a "Raspberry Pi Desktop with Debian" operating system
* About the Apache webserver, we can create a web interface and use that web interface to replace the function of the button on the Arduino side.
