# Monitoring System For Server's CPU Temperature

***

![MonitoringCPUTemp.png](https://github.com/leehaesung/Monitor_MyServer_CPUTemperature/blob/master/01_Images/TensorFlowAnalyticsSeverCPUTemp.png?raw=true)

***
## (1) Dashboard @AWS

* [Source Code of Python (Jupyter-notebook)](https://github.com/leehaesung/Monitor_MyServer_CPUTemperature/blob/master/02_Source_Codes/SQLite3_with_Monitoring_Server_Temperature_MQTT.ipynb)

* [Nbviewer Jupyter-notebook of Python](http://nbviewer.jupyter.org/github/leehaesung/Monitor_MyServer_CPUTemperature/blob/master/02_Source_Codes/SQLite3_with_Monitoring_Server_Temperature_MQTT.ipynb)

* [Source Code For NodeRED](https://github.com/leehaesung/Monitor_MyServer_CPUTemperature/blob/master/02_Source_Codes/02_MonitoringCPUTempAWS.txt)

![MonitoringMyLaptopAWS.png](https://github.com/leehaesung/Monitor_MyServer_CPUTemperature/blob/master/01_Images/MonitoringSeverAtAWS.png)

***
## (2) Dashboard @Server or Laptop

* [Source Code For Linux Server](https://github.com/leehaesung/Monitor_MyServer_CPUTemperature/blob/master/02_Source_Codes/01_MonitoringCPUTempAtLaptop.txt)


![CPUTempAtMyLaptop.png](https://github.com/leehaesung/Monitor_MyServer_CPUTemperature/blob/master/01_Images/MonitoringServerAtServer.png)

***
## (3) SQLite Datasbase Browser

* How to install SQLite3 for Ubuntu:
    ```
    sudo apt-get install sqlite3 libsqlite3-dev
    ```

* How to Install sqlitebrowser for Ubunt:
    ```
    sudo apt-get install sqlitebrowser  
    ```

![SQLiteDB_Browser_For_CPU_Temp.png](https://github.com/leehaesung/Monitor_MyServer_CPUTemperature/blob/master/01_Images/SQLiteDB_Browser_For_CPU_Temp.png)

***
## (4) SQLite3

* How to search the temperature data:

    ```
    ubuntu@ubuntu:~$ sqlite3 sqliteCpu
    SQLite version 3.8.2 2013-12-06 14:53:30
    Enter ".help" for instructions
    Enter SQL statements terminated with a ";"
    sqlite> SELECT * from HOME WHERE TEMP = 34;
    1511774938638|171127202858|34
    1511791940523|171128011220|34
    1511791970534|171128011250|34
    1511792000552|171128011320|34
    1511856311027|171128190511|34
    1511856641175|171128191041|34
    1511860288540|171128201128|34
    1511877691133|171129010131|34
    1511877721143|171129010201|34
    1511923097432|171129133817|34
    1511923127453|171129133847|34
    1511934608776|171129165008|34
    sqlite> SELECT * from HOME WHERE TEMP = 29;
    1511846797164|171128162637|29
    1511918384536|171129121944|29
    sqlite> .quit
    ```

![HowToSearchTemperatureInSQLite3.png](https://github.com/leehaesung/Monitor_MyServer_CPUTemperature/blob/master/01_Images/HowToSearchTemperatureInSQLite3.png)

***
## (5) How To Export CSV File

```
    sqlite3 sqliteCpu

    .mode csv

    .output test.csv

    select * from HOME;

    .output stdout
```
 [Output: test.csv](https://github.com/leehaesung/Monitor_MyServer_CPUTemperature/blob/master/02_Source_Codes/test.csv)


### References

* [SQLite3-Python Quick Guide](https://github.com/leehaesung/SQLite-Python_Quick_Guide)
* [SQLite3 Quick Guide](https://www.tutorialspoint.com/sqlite/sqlite_quick_guide.htm)
* [Paho MQTT Python: GitHub](https://github.com/leehaesung/paho.mqtt.python)
