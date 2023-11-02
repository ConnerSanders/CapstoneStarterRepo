# Electrolysis System
## Function of the system
The role of the system is to implement the process necessary for generating the hydrogen and oxygen gases. The system consists of a pre-made electrolytic cell, a pulse inverter, a rectifier, and permanent magnets. The pulse inverter will be the power source of the system, and the rectifier will be used on the output of the pulse inverter to ensure that the polarity of the input power is consistent. The magnets will be used to boost the system's efficiency.


## Constraints
| No. | Constraints                                                                                | Origin                               |
| --- | ------------------------------------------------------------------------------------------ | ------------------------------------ |
| 1   | The material of the electrolytic cell housing shall not be reactive with sodium hydroxide. | Design Constraint                    |
| 2   | The material of the electrolytic cell should be transparent or translucent.                | Design Constraint                    |
| 3   | The system shall include a pulse generator and permanent magnets to boost efficiency.      | Design Constraint                    |
| 4   | The pulse generator’s output should be rectified.                                          | Design Constraint                    |
| 5   | The electrolysis cell shall have no permanent storage of gases.                            | OSHA Standards 1910.103 and 1910.104 |
| 6   | Pulse inverter must be able to be shut off within two clock cycles by the safety system.   | Design Constraint                    |
| 7   | Safety system must shut off the system when the cell's pressure is at 15 PSI.              | Design Constraint                    |


<sup>1</sup>
The material of the cell not being reactive with sodium hydroxide is essential both for functionality and safety, given that sodium hydroxide will be part of the solution housed in the cell.

<sup>2</sup>
This is a preference decided by the team.

<sup>3</sup>
The pulse generator will be the system's power source, and its frequency and amplitude will be manipulated for optimizing efficiency. The magnets will serve to bias the ions in the solution toward the electrodes in order to increase interaction and boost efficiency.

<sup>4</sup>
The rectification of the pulse generator's output, while not essential to the function of the system as it is being designed, is prefered as it makes possible future development more approachable. The direct purpose of the rectification is that it keeps the location of hydrogen and oxygen gas generation seperate so that, in the future, the gases can more easily be isolated from one another.

<sup>5</sup>
Hydrogen and oxygen gas will not be stored in the cell as pressurized storage of the gases results in a combustible system.

<sup>6</sup>
This will prevent any excessive delays that may be a safety concern.

<sup>7</sup>
While the pressure capacity of the cell being ordered is unknown, 15 PSI was chosen as a limit given the expectation that pressure should not increase by any substantial amount. With this, the system will be shut off when pressure starts to build,  with 15 PSI being chosen as a safe limit where any fault in the system will not be a safety concern, regardless of the cell's capacity.


## Buildable Schematic
![image](/Documentation/Images/Electrolysis_System/Conceptual/Electrolysis_System.jpg)


## Analysis
### Cell
The material of the cell to be ordered is appropriate as it is not reactive with sodium hydroxide. It is also large enough that it can hold the amount of water necessary for producing a constant flame. With gas storage not being used for the project, the pressure capacity of the cell is irrelevant, and the safety system will be used to automate pressure limitation in cases where a system malfunction causes pressure to start to build. The cell has one hole through which water comes in and gas escapes, meaning that it will never be fully shut for pressure to build. While the cell itself isn't transparent or translucent, enough components of the whoe unit being ordered allows for higher convenience than a totally opaque cell.

### Optimization Tools
The pulse inverter to be used is sufficient as it is made to function as an AC source running at 250 Hz (500 Hz after rectification). The TRYMAG magnets to be used as they are small and therefore easily manipulable. The magnets coming in a pack of 150 ensures that there will be plenty and that magnets will always be available when replacement is necessary. Both the pulse inverter and the magnets are not extremely confined with stringent specifications as the optimization they contribute (and their traits which boost it) are not yet known.

### Rectification
The rectifier selected is appropriate for the system as its maximum repetitive peak voltage is 1000 V and the average rectified forward current is 50 A. These limits are high enough that the system can function without exceeding them. The rectifiers chosen are also convenient due to them having screw holes which make them easy to mount.

### Output Capacitor



## BOM
| Device                                                | Quantity | Price per Unit | Total Cost |
| ----------------------------------------------------- | -------- | -------------- | ---------- |
| Electrolysis Water Machine with Spray-Gun             | 1        | $93.99         | $83.60     |
| TRYMAG Small Magnets 150Pcs, 12x2mm Neodymium Magnets | 1        | $16.19         | $16.19     |
| Pulse Inverter                                        | 1        | NA             | NA         |
| KBPC5010 Bridge Rectifier                             | 5        | $1.80          | $8.99      |
| Total                                                 |          |                | NA         |

## References
Electrolysis Water Machine: https://www.ebay.com/itm/285135769861?chn=ps&mkevt=1&mkcid=28&srsltid=AfmBOorJrA9qSJqiSfL-STEVVm67HEf99sTU05votISELXoC7w6v8320vsI
TRYMAG Small Magnets: https://www.amazon.com/TRYMAG-Different-Neodymium-Refrigerator-Whiteboard/dp/B0CHVPD4K8/ref=sr_1_4?keywords=Neodymium%2BMagnets%2BSmall&qid=1698257546&sr=8-4&th=1
Bridgold 5pcs KBPC5010 Bridge Rectifier: https://www.amazon.com/Bridgold-KBPC5010-Rectifier-Electronic-Silicon/dp/B07MQ65HLB/ref=sr_1_3?keywords=50+amp+bridge+rectifier&qid=1698784358&sr=8-3
