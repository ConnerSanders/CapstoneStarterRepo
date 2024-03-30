# Experimental Analysis Report

## Introduction
The purpose of the Experimental Analysis is to test if project constraints are being met and to document the experiments used to measure success.  
### Requirements Table
| **Constraint** |           **Constraint Description**                                                                                  | **Subsystem** |
|--------|-------------------------------------------------------------------------------------------------------------------------------|--------------------------|
| 1      | Shall accurately measure the electrical efficiency of the electrolyzer                                                        | Controller  |
| 2      | Display output shall be easy to read and simplistic.                                                                          | Controller  |
| 3      | The material of the electrolytic cell housing shall not be reactive with sodium hydroxide.                                    | Electrolysis  |
| 4      | The system shall include a pulse generator and permanent magnets to boost efficiency.                                         | Electrolysis  |
| 5      | The pulse generator’s output should be rectified.                                                                             | Electrolysis  |
| 6      | The pulse inverter must be able to be shut off within two clock cycles by the safety system.                                  | Electrolysis  |
| 7      | The water in the cell shall automatically refill when below 2/3rds of the cell's capacity.                                    | Water  |
| 8      | The water system fittings will use non-corrosive materials for fittings                                                       | Water  |
| 9      | The water system shall prevent backwards flow of water.                                                                       | Water  |
| 10     | The system shall convert wall AC Voltage to DC voltage.                                                                       | Power  |
| 11     | The system shall be able to supply 5 VDC.                                                                                     | Power  |
| 12     | The system shall be able to supply 12 VDC.                                                                                    | Power  |
| 13     | The system shall have no dangerous exposed wires and shall be grounded as needed.                                             | Power  |
| 14     | Shall contain an emergency-stop button                                                                                        | Safety |
| 15     | Shall shutoff if pressure and temperature approach ignition conditions of Brown's gas                                         | Safety |
| 16     | System monitors must be designed with redundancies                                                                            | Safety |
| 17     | System shall not produce gas unless there is a flame present.                                                                 | Safety |


## Results

### Constraint 1 - Shall accurately measure the electrical efficiency of the electrolyzer 

Experimental Design

Results

Conclusion

### Constraint 2 -  Display output shall be easy to read and simplistic.

### Constraint 14 - Shall contain an emergency-stop button
Experimental Design - When emergency stop button is pressed, the power to the pulse inverter must be cut off.

Results - Power to the pulse inverter is cut off when the emergency-stop button is pressed. The system stops producing gas.

Conclusion - Constraint was tested and passed.

### Constraint 15 - Shall shut off if pressure and temperature approach ignition conditions of Brown's gas
Experimental Design - When the temperature sensor reaches 100 degrees celsius or the pressure sensor reaches 15 psi, power to the pulse inverter is cut off.

Results - When temperature sensor reaches 100 degrees celsius, power is cut off. PRESSURE UNTESTED

Conclusion - Temperature constraint was tested and passed. PRESSURE UNTESTED

### Constraint 16 - System monitors must be designed with redundancies

Experimental Design - Relay outputs were separated and tested independently while still connected to the same circuit.

Results - Every Safety circuit has 2 relays that have their own independent outputs.

Conclusion - Constraint was tested and passed

### Constraint 17 - System shall not produce gas unless a flame is present

Experimental Design - Flame was held up to the flame sensor and the output was observed.

Results - The output of the flame sensor did not change from 0 volts. A new flame sensor has been ordered, the original flame sensor does not perform as expected.

Conclusion - Constraint was tested but did not pass.

## Conclusion

| **Constraint** |     **Constraint Description**                                                                                        | **Constraint Met?** |
|--------|-------------------------------------------------------------------------------------------------------------------------------|--------------------------|
| 1      | Shall accurately measure the electrical efficiency of the electrolyzer                                                        | Controller  |
| 2      | Display output shall be easy to read and simplistic.                                                                          | Controller  |
| 3      | The material of the electrolytic cell housing shall not be reactive with sodium hydroxide.                                    | Electrolysis  |
| 4      | The system shall include a pulse generator and permanent magnets to boost efficiency.                                         | Electrolysis  |
| 5      | The pulse generator’s output should be rectified.                                                                             | Electrolysis  |
| 6      | The pulse inverter must be able to be shut off within two clock cycles by the safety system.                                  | Electrolysis  |
| 7      | The water in the cell shall automatically refill when below 2/3rds of the cell's capacity.                                    | Water  |
| 8      | The water system fittings will use non-corrosive materials for fittings                                                       | Water  |
| 9      | The water system shall prevent backwards flow of water.                                                                       | Water  |
| 10     | The system shall convert wall AC Voltage to DC voltage.                                                                       | Power  |
| 11     | The system shall be able to supply 5 VDC.                                                                                     | Power  |
| 12     | The system shall be able to supply 12 VDC.                                                                                    | Power  |
| 13     | The system shall have no dangerous exposed wires and shall be grounded as needed.                                             | Power  |
| 14     | Shall contain an emergency-stop button                                                                                        | Safety |
| 15     | Shall shutoff if pressure and temperature approach ignition conditions of Brown's gas                                         | Safety |
| 16     | System monitors must be designed with redundancies                                                                            | Safety |
| 17     | System shall not produce gas unless there is a flame present.                                                                 | Safety |
