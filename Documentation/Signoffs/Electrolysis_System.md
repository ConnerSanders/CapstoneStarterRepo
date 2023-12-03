# Electrolysis System
## Function of the System
The role of the system is to implement the process necessary for generating the hydrogen and oxygen gases. The system consists of a pre-made electrolytic cell, a pulse inverter, a rectifier, an auxiliary capacitor, and permanent magnets. The pulse inverter will be the power source of the system, and the rectifier will be used on the output of the pulse inverter to ensure that the polarity of the input power is consistent. The magnets will be used to boost the system's efficiency. The auxiliary capacitor will be used for manipulating pulse duration.


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
The rectification of the pulse generator's output, while not essential to the function of the system as it is being designed, is prefered as it makes possible future development more approachable. The direct purpose of the rectification is that it keeps the location of hydrogen and oxygen gas generation seperate so that, if and when necessary, the gases can more easily be isolated from one another.

<sup>5</sup>
Hydrogen and oxygen gas will not be stored in the cell as pressurized storage of the gases results in a combustible system.

<sup>6</sup>
This will prevent any excessive delays that may be a safety concern.

<sup>7</sup>
While the pressure capacity of the cell being ordered is unknown, 15 PSI was chosen as a limit given the expectation that pressure should not increase by any substantial amount. With this, the system will be shut off when pressure starts to build,  with 15 PSI being chosen as a safe limit where any fault in the system will not be a safety concern, regardless of the cell's capacity.


## Buildable Schematic
![image](/Documentation/Images/Electrolysis_System/Buildable_Schematic/Electrolysis_System.jpg)

## Analysis
### Cell
The material of the cell to be ordered is appropriate as it is not reactive with sodium hydroxide. This is known because the instruction manual for the product can be quoted as instructing users to use 3 grams of sodium hydroxide per 600 mL of water. It is also large enough that it can hold the amount of water necessary for producing a constant flame. With gas storage not being used for the project, the pressure capacity of the cell is irrelevant, and the safety system will be used to automate pressure limitation in cases where a system malfunction causes pressure to start to build. The cell has one hole through which water comes in and gas escapes, meaning that it will never be fully shut for pressure to build. While the cell itself isn't transparent or translucent, enough components of the whoe unit being ordered allows for higher convenience than a totally opaque cell.

### Optimization Tools
The pulse inverter to be used is sufficient as it is made to function as an AC source running at 250 Hz (500 Hz after rectification). The TRYMAG magnets to be used as they are small and therefore easily manipulable. The magnets coming in a pack of 150 ensures that there will be plenty and that magnets will always be available when replacement is necessary. The magnets will be attached to the electrolytic cell by means of hot gluing them across the cell holding the electrodes. Neither the pulse inverter nor the magnets are extremely confined with stringent specifications as the optimization they contribute (and their traits which boost it) are not yet known.

### Rectification
The rectifier selected is appropriate for the system as its maximum repetitive peak voltage is 1000 V and the average rectified forward current is 50 A. These limits are high enough that the system can function without exceeding them, given that the pulse generated by the pulse inverter will have an amplitude of roughly 12 V. The rectifiers chosen are also convenient due to them having screw holes which make them easy to mount. The ripple voltage produced by the rectifier is not an issue, as the only value being considered is the amplitude of the output pulses.

### Auxiliary Capacitor
The auxiliary capacitor is used for manipulating pulse widths that are seen by the electrolysis water machine. The FA22X7R2A225KNU00 capacitor was selected because it is ceramic as opposed to electrolytic, and its ratings indicate that it is capable of handling voltages greater than those shown across Caux in simulation. It being ceramic is important for the bipolar voltage (this disqualifies electrolytic capacitors). The FA22X7R2A225KNU00, in particular, was selected because its legs make it practical and its rated voltage of 50 V is more than enough to handle the voltages put across it by the rest of the system.


## BOM
| Device                                                | Quantity | Price per Unit | Total Cost |
| ----------------------------------------------------- | -------- | -------------- | ---------- |
| Electrolysis Water Machine with Spray-Gun             | 1        | $93.99         | $93.99     |
| TRYMAG Small Magnets 150Pcs, 12x2mm Neodymium Magnets | 1        | $16.19         | $16.19     |
| Pulse Inverter                                        | 1        | NA             | NA         |
| KBPC5010 Bridge Rectifier                             | 5        | $1.80          | $8.99      |
| FA22X7R2A225KNU00 Capacitor                           | 1        | $1.73          | $1.73      |
| Total                                                 |          |                | NA         |

## References
Tap Water Resistivity: https://www.researchgate.net/figure/Resistivity-of-tap-water-with-different-amounts-of-salt-added_tbl2_352785351

Electrolysis Water Machine: https://www.ebay.com/itm/174776123639?_trkparms=amclksrc%3DITM%26aid%3D1110006%26algo%3DHOMESPLICE.SIM%26ao%3D1%26asc%3D256748%26meid%3D1dc857e62fbd4bd18999f817ace93fcc%26pid%3D101195%26rk%3D1%26rkt%3D12%26sd%3D256158485755%26itm%3D174776123639%26pmt%3D1%26noa%3D0%26pg%3D4429486%26algv%3DSimplAMLv11WebTrimmedV3MskuWithLambda85KnnRecallV1V2V4ItemNrtInQueryAndCassiniVisualRankerAndBertRecallWithVMEV3CPCAuto%26brand%3DUnbranded&_trksid=p4429486.c101195.m1851&amdata=cksum%3A1747761236391dc857e62fbd4bd18999f817ace93fcc%7Cenc%3AAQAIAAABYObhgc4Nk8%252BdtAwOww4FKLaj%252FQ5qqgDlQCuqZA43WcPFUWDERCUugbbOk7XQv0JXlBfqCg2xKF3WcPghxGMFw2oSlXvfExEaMYr7I7LmrHcP6czY1wIMt0ORyKiCWt95xldincyyBx3g%252BNDW%252B%252FhWUgTaBhK6xAm%252BJIbCOMehu%252BdwrnX2e9DOgKZoPNI5mFhPbp3yJNZUZChzrFjShdyQ1h3PK92PSU4ka%252Fr4%252BKEzPDR7foKKo%252F%252FYNEY3dSnopY6rf6XHaudyvtfXmlqZYgTJm4UMfpQFpOeaAkYU60uDTDgSK1hgg19OaKbdUvIJIzjJX%252FcQgF%252BHHMNXAqDO7BRkhDELi7kBp9M4T%252FWmQDNHkkD%252Bm1Bk36wl7BhWpkM7QYnpydT7Bfi6OZr5KTCFcQS7uxGhMkoTMYYIF1sWWbyCEfqpCEapw4y0xvcvEBR%252B8EvilfhQfnQWU2OPHhajKvkrei8%253D%7Campid%3APL_CLK%7Cclp%3A4429486

TRYMAG Small Magnets: https://www.amazon.com/TRYMAG-Different-Neodymium-Refrigerator-Whiteboard/dp/B0CHVPD4K8/ref=sr_1_4?keywords=Neodymium%2BMagnets%2BSmall&qid=1698257546&sr=8-4&th=1

Bridgold 5pcs KBPC5010 Bridge Rectifier: https://www.amazon.com/Bridgold-KBPC5010-Rectifier-Electronic-Silicon/dp/B07MQ65HLB/ref=sr_1_3?keywords=50+amp+bridge+rectifier&qid=1698784358&sr=8-3

Auxiliary Capacitor: https://www.mouser.com/ProductDetail/TDK/FA22X7R2A225KNU00?qs=sGAEpiMZZMsh%252B1woXyUXj1zzeG0a68Rdkzsqp1yRR6s%3D

Electrolysis Water Machine Instruction Manual:

![image](/Documentation/Images/Electrolysis_System/Instruction_Manual.jpg)
