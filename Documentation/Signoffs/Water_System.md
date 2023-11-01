# Water System
## Function of the system
The goal of this system is to make sure the that the water in the electrolytic cell never drops below 2/3 of the cell capactity. This will be done with a non-contact water level sensor placed 2/3  the height of the cell housing. This ensure that the cell water level stay to the recommended level by the manufacturer of the cell. When the sensor is high than the water control valve needs to be shutoff, so the signal out the sensor will need to be inverted.

## Constraints
| No. | Constraints                                                                                   | Origin            |
| --- | --------------------------------------------------------------------------------------------- | ----------------- |
| 1| The water in the cell shall automatically refill when below 2/3 the cells capacity .             | Design Constraint | **********************
| 2| The water level sensor shall be affixed to the outside of the cell.                              | Design Constraint |
| 3| The water system shall have a hole below the water level					                                | Design Constraint |
|	4| The water system fittings will use non-corrosive materials for fittings			                    | Design Constraint |
| 5| The water system shall prevent backwards flow of water.                                          | Ethical Constraint|

<sup>1</sup>
The electroyltic cell needs to have a certain amount of water at all times to keep efficiency up.

<sup>2</sup>
This is due to the fact that the cell does not have enough room in the cell to house the sensors.

<sup>3</sup>
The system does not want to introduce another way for the gas to leave the system. By submerging the water inlet for the cell the gas will rise to the top of the cell and not hang in the water inlet tube.

<sup>4</sup>
The system needs to run with out issues as long as possible. The fittings need to be as corrosive resistant as possible to help keep the longevity of the cell.

<sup>5</sup>
This is to ensure that the water supply would not get contaminated by what is in the cell.

## Buildable Schematic

<img src="/Documentation/Images/Water_System/Buildable_Schematic/schematic.png" width="90%" height="90%">

## Analysis

#### Non-Contact Capacitive Water Level Sensor

The sensor uses its own capacitance and parasitic capacitance of the water to determent when the water level has reached a fixed point in front of the sensor. The sensor will be mounted on the outside. When the sensor goes high when the water level is at the 2/3 mark of the cell. This means the signal needs to be inverted when controlling the solenoid of the control valve. When the water level is high the sensor will make the gate voltage the same as the source voltage keep the PFET transistor close. When the sensor is low, the gate will be lower than the source making the PFET transistor open and allowing water to fill up. When the transistor goes from the on to off state the diode allows current to flow back in to the soleniod and disspate and prevent the any damage to the transistor.

#### Electrically Accuated Control Valve

<img src="/Documentation/Images/Water_System/Conceptual/control_valve.png" width="90%" height="%90">

As shown in the figure above, the control valve will have several fittings to allow for hose to be connected from various parts of the whole system. The inlet of the valve has is a barbed 1/4" to 3/8" NPT Male fitting to than go to the check valve. The check valve will ensure that the system water does contaminate the city water supply. The control valve outlet than goes to the same fitting as the inlet. This will allow for cheap 1/4 vinyl tubing to be bought in bulk, so there is no need to run hard plumbing to fill the system up. The connection will be a series of adatapers frome a faucet to a 1/4" Barb

## BOM
| Device | Quantity | Price per Unit ($) | Total Cost ($) |
| ------ | -------- | -------------- | ---------- |
|Tank Fitting|1|10.23|10.23|
|3/8" Male to Barbed Hose Fitting|2|15.38|46.14|
|Faucet to Garden Hose adapter|1|9.98|9.98|
|Garden Hose to National Pipe Thread Adapter|1|8.99|8.99|
|3/4' Barbed Hose Fitting|1|10.35|10.35|
|Worm-Drive Clamp|1|10.52|10.52|
|1/4" Vinyl Hose 25' long|2|9.28|18.56|
|Non-Contact Capacitive Water Level Sensor|2| 9.94|19.88|
|Electric Brass Solenoid Valve|1|44.95|44.95|
|200 Vrm Diode|2|2.24|4.48|
|60 V P-FET| 2| 2.52| 6.02|
| ------ | -------- | -------------- | ---------- |
|Total|||190.20|




## References

[1] https://www.mcmaster.com/products/flow-valves/check-valves~/body-material~brass-2/threaded-check-valves-10/pipe-size~3-8/

[2] https://www.electricsolenoidvalves.com/3-8-12v-dc-electric-brass-solenoid-valve/#description

[3][ https://www.amazon.com/Waterproof-Contact-Liquid-Sensor-Signal/dp/B0B7W9QYRX/ref=sr_1_7_sspa?crid=3KMMPVDKNY1CM&keywords=non+contact+water+level+sensor&qid=1698428863&s=hi&sprefix=non+contact+water%2Ctools%2C121&sr=1-7-spons&sp_csd=d2lkZ2V0TmFtZT1zcF9tdGY&psc=1](https://www.amazon.com/dp/B074PVF341/ref=sspa_dk_detail_0?psc=1&pd_rd_i=B074PVF341&pd_rd_w=LUR56&content-id=amzn1.sym.f734d1a2-0bf9-4a26-ad34-2e1b969a5a75&pf_rd_p=f734d1a2-0bf9-4a26-ad34-2e1b969a5a75&pf_rd_r=7XAKDG93N9RKYFVEN5EM&pd_rd_wg=s2X7A&pd_rd_r=6a5d492e-b856-4e6f-89e1-cc650a4c9141&s=hi&sp_csd=d2lkZ2V0TmFtZT1zcF9kZXRhaWw)https://www.amazon.com/dp/B074PVF341/ref=sspa_dk_detail_0?psc=1&pd_rd_i=B074PVF341&pd_rd_w=LUR56&content-id=amzn1.sym.f734d1a2-0bf9-4a26-ad34-2e1b969a5a75&pf_rd_p=f734d1a2-0bf9-4a26-ad34-2e1b969a5a75&pf_rd_r=7XAKDG93N9RKYFVEN5EM&pd_rd_wg=s2X7A&pd_rd_r=6a5d492e-b856-4e6f-89e1-cc650a4c9141&s=hi&sp_csd=d2lkZ2V0TmFtZT1zcF9kZXRhaWw

[4] https://www.mcmaster.com/5346K95/

[5] https://www.mcmaster.com/9151K265/

[6] https://www.mcmaster.com/1075T23/

[7] https://www.mcmaster.com/5388K14/

[8] https://www.lowes.com/pd/EZ-FLO-1-4-in-Inner-Diameter-x-25-ft-Polyethylene-Tubing/1000180497

[9] https://www.lowes.com/pd/Danco-3-4-in-GHTF-x-55-64-in-27M-Chrome-Dishwasher-Aerator-Adapter/3647054

[10] https://www.mcmaster.com/5346K46/

[11] https://www.amazon.com/Adapter-Connector-Fitting-Fittings-Connect/dp/B087GKPMVG/ref=pd_bxgy_sccl_2
/138-4857020-0099853?pd_rd_w=cIsdc&content-id=amzn1.sym.21b577c4-6435-4581-8b53-49da41e27328&pf_rd_p=21b577c4-6435-4581-8b53-49da41e27328&pf_rd_r=MQHGMHZ183HCK92E62MY&pd_rd_wg=w7sxm&pd_rd_r=3093a3d2-2d17-458e-a486-307ecc96fd8c&pd_rd_i=B087GKPMVG&th=1]

[12] https://www.mcmaster.com/5346K46/

[13] https://www.mouser.com/ProductDetail/Vishay-Siliconix/IRF9Z30PBF-BE3?qs=7MVldsJ5UazmpG%252BNXOVzGA%3D%3D

[14] https://www.mouser.com/ProductDetail/Shindengen/S3L20U-5060?qs=OSm%2FIAICcjaotcbGQrz8jA%3D%3D
