# Arduino and Raspberry Pi communication

Two methods:

* Network (wifi)
* Serial

![](/img/Picture1.png)

![](/img/Picture2.png)

![](/img/Picture3.png)

![](/img/Picture4.png)


Serial communication is the most widely used approach to transfer information between data processing equipment and peripherals.

![](/img/Picture5.png)

# Serial communication

* Arduino supports the library for the serial commumication
* Serial monitor will work when Arduino is connected to PC using USB cable.
* Serial is used to upload code to Arduino.

![](/img/Picture6.png)

Serial function:
* `Serial.begin(<baud rate>)`: Define to use serial communication
* `Baud rate`: speed transfer/receive (bit/second)
* `Serial.available()`: return the number of bytes avalaible ro read
* `Serial.read()`: return the first byte of incoming serial data available (= -1 if there is no data availablel)
* `Serial.print(<data log>)` same as `Serial.println(<data log>)` but with second method monitor will print data in each line on monitor display
* `Serial.write(<data need to send>)`: writes binary data to the serial port

![](/img/2023-03-04-23-16-15.png)

# Connection between Arduino and Pi

Connection:
* Two methods to connect via Serial
    * USB port
    * GPIO: Need a Level shifter module (3.3/5V )

![](/img/2023-03-04-23-17-16.png)

Checking connection:
* Open terminal and using command:

```bash
$ ls /dev/tty*
```

All devices are displayed. In this case, Arduino is /dev/ttyUSB0

![](/img/2023-03-04-23-18-44.png)

Note:
* If you have some problem related to permission. Using this command for fixing:

```bash
$ sudo adduser <your_username> dialout
```

![](/img/2023-03-04-23-19-49.png)

Install library for Python:
* Using pyserial library

```bash
$ python3 –m pip install pyserial
```

* If you get error such as “/usr/bin/python3: No module named pip”. Run following command:

```bash
$ sudo apt install python3-pip
```

![](/img/2023-03-04-23-21-19.png)

# Example

**Arduino part:**

Upload this code to Arduino:
* We select the baud rate (9600)
* Arduino sends a string with `Serial.println` function

![](/img/2023-03-04-23-22-31.png)

**Raspberry Pi part:**
* Import serial library: `import serial`
* Setup serial: `serial.Serial()`
* Read (receive) data: `ser.readline()`
* Send data: `ser.write`

![](/img/2023-03-04-23-23-29.png)

![](/img/2023-03-04-23-23-51.png)

![](/img/2023-03-04-23-24-08.png)

![](/img/2023-03-04-23-24-22.png)

![](/img/2023-03-04-23-25-02.png)

```cpp
float vout;
float tempc;
void setup() {
Serial.begin(9600);
}
void loop() {
vout=analogRead(A0); //Reading the value from sensor
vout=vout*5/1024.0;
tempc=vout*100.0; // Storing value in Degree Celsius
Serial.println(tempc);
delay(1000);
}
```

![](/img/2023-03-04-23-26-09.png)

```python
import serial
import MySQLdb
dbConn = MySQLdb.connect("localhost", "account_db", "password", "IoT_SU") or die("Could not
connect to the database")
print(dbConn)
device = "/dev/ttyS1"
arduino = serial.Serial(device,9600)
data=arduino.readline()
print(data)
with dbConn:
cursor = dbConn.cursor()
cursor.execute("INSERT INTO DataInfor (Temperature) values (%s)" % (data))
dbConn.commit()
cursor.close()
```
