# Safety System
## Function of the system
This system will shut-off power to the pulse inverter if the system becomes unsafe, halting any gas production. The system consists of a flame detector, pressure sensor, temperature sensor, and an emergency stop button. Normally open relay contacts will be connected to all components previously mentioned. In the event that any of these contacts are closed, the relay coil will be de-energised, and power to the pulse inverter will be disconnected.

## Constraints
| No. | Constraints                                                                                   | Origin                               |
| --- | --------------------------------------------------------------------------------------------- | ------------------------------------ |
| 1   | Shall contain an emergency-stop button                                                        | NFPA 79                              |
| 2   | Shall shutoff if pressure and temperature approach ignition conditions of Brown's gas         | Design Constraint                    | 
| 3   | System monitors must be designed with redundancies                                            | Design Constraint                    |
| 4   | System shall not produce gas unless there is a flame present                              | Design Constraint

<sup>1</sup>
NFPA 79 states that when an emergency stop button is pressed, all dangerous actions will stop without creating new hazards. The system must contain an accesable emergency stop button. When pressed, power to the pulse inverter will be cut off.

<sup>2</sup>
In order to avoid any sort of explosion or uncontrolled fire, pressure and temperature sensors will cut off power to the pulse generator if their values approach ignition conditions of Brown's gas.

<sup>3</sup>
Failure of the safety system can be minimized by creating redundancies in the system. Redundancies will be created by including 2 relay contacts for each componant in the safety system.

<sup>4</sup>
Halting gas production when there is no flame present ensures that there is no gas lingering in the system. This eleminates any hazard when the machine is not being used.

## Buildable Schematic
<img src="/Documentation/Images/SafetySchematic/ConnerSanders_Safety_Schematic.JPG" width="60%" height="60%">


## Analysis
#### UV Sensor
The UV sensor is connected to 12VDC and ground from the power system. The output of this sensor is connected to a normally open relay. A button is also connected to this relay, so that when you are ready to start OH production, you can do so. The button separates the relay coil from 12VDC, so the coul is energized when the button is pressed. IF the sensor does not see a flame, and the button is not pressed, the circuit between the pulse inverter power and the pulse inverter is broken.

#### Temperature Sensor
The Temperature sensor separates 12VDC from the power system and a normally closed relay coil. When the sensor feels anything over 100 degrees Celcius, the circuit between the puls inverter power and the pulse inverter is broken.

#### Pressure Sensor
The pressure sensor separates 12VDC from the power system and a normally closed relay coil. When the pressure across the sensor rises to 15 psi, the circuit between the puls inverter power and the pulse inverter is broken.

#### Emergency Stop
The Emergency stop button separates 12VDC from the power system and a normally closed relay coil. When pressed, the circuit between the pulse inverter power and the pulse inverter is broken.



## BOM
| Device                                                | Quantity | Price per Unit | Total Cost |
| ----------------------------------------------------- | -------- | -------------- | ---------- |
| UV flame detector                                     | 1        | $8.13          | $8.13      |
| Pressure sensor                                       | 1        | $88.02         | $88.02     |
| Temperature sensor                                    | 1        | $7.28          | $7.28      |
| Emergency stop                                        | 1        | $7.99          | $7.99      |
| Push button                                           | 1        | $1.22          | $1.22      |
| Relay (NC)                                            | 2        | $8.00          | $16.00     |
| Relay (NO)                                            | 6        | $4.00          | $24.00     |
| ----------------------------------------------------- | -------- | -------------- | ---------- |
| Full System                                           | -------- | -------------- | $152.64    |
