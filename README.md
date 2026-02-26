# MediBrick

A cost-effective Solution for Biomedical Measurements.

Urs Utzinger, 10/2024 and capstone teams: 24052 (2023/24), 23094 (2022/23).
Biomedical Engineering Department, College of Engineering, The University of Arizona.


<img src="assets/Concept.png" height="200px">
 
Table of Content:
<!-- TOC start (generated with https://github.com/derlin/bitdowntoc) -->

- [MediBrick](#medibrick)
  - [Problem Description](#problem-description)
  - [Project Goals](#project-goals)
  - [MediBricks](#medibricks)
  - [Microcontroller and Software](#microcontroller-and-software)
  - [Hardware](#hardware)
    - [Design and Manufacturing](#design-and-manufacturing)
    - [Enclosures](#enclosures)
  - [Project Status](#project-status)

<!-- TOC end -->

<!-- TOC --><a name="medibrick"></a>

Posters and Papers: 
- *Open source platform to measure physiological signals in a classroom setting*, BMES 2024 Annual Meeting: Biomedical Engineering Education - Poster Session C, Poster Q15 

## Problem Description

Biomedical engineering students need to practice measuring signals from living systems.
Measurement equipment is needed for classroom laboratories that can safely record common physiological parameters.
For a wide adoption, such equipment should be cost effective and repairable in-house.
Therefore, it should take advantage of existing components that are open source and distributed through domestic channels.
While there are commercial systems available [^fn1] [^fn2], there is no unifying approach that takes advantage of existing third party hardware, gives option to expand functionality at later time and uses open source software.  Such measurement modules could also be readily incorporated into academic research projects.

[^fn1]: Bioradio, https://staging.glneurotech.com/product-category/bioradio-all
[^fn2]: Protocentral https://protocentral.com

**An expandable, low-costs, open-design system is needed that measures physiological parameters in a class room setting in a safe manner.**

## Project Goals
- We strive to create an educational system to measure physiological signals.
- It shall be easily manufactured at an educational institution.
- It shall record, display and store common physiological measurements safely in a class room setting.

## MediBricks
This project consists of the following measurement devices:

| ECG and Impedance | Electronic Stethoscope and Blood Pressure | Pulse Oximeter | Temperature | Inertial Measurement Unit | Air Quality |
| --- | --- | --- | --- | --- | --- |
| <a href="assets/pictures/ECG_BIOZ_Front_Closed_without_Plugins.jpg" target="_blank"> <img src="assets/pictures/ECG_BIOZ_Front_Closed_without_Plugins.jpg" width="100"> </a> | <a href="assets/pictures/Stethoscope_Front_Closed_with_Plugins.jpg" target="_blank"><img src="assets/pictures/Stethoscope_Front_Closed_with_Plugins.jpg" width="100"></a> | <a href="assets/pictures/PulseOx_Front_Closed_with_Plugins.jpg" target="_blank"><img src="assets/pictures/PulseOx_Front_Closed_with_Plugins.jpg" width="100"></a> | <a href="assets/pictures/Temp_Front_Closed_with_Plugins.jpg" target="_blank"><img src="assets/pictures/Temp_Front_Closed_with_Plugins.jpg" width="100"></a> | <a href="assets/pictures/IMU_Front_Closed_without_Plugins.jpg" target="_blank"><img src="assets/pictures/IMU_Front_Closed_without_Plugins.jpg" width="100"></a> | <a href="assets/pictures/Environment_Front_Closed_without_Plugins.jpg" target="_blank"><img src="assets/pictures/Environment_Front_Closed_without_Plugins.jpg" width="100"></a> |
| <a href="assets/pictures/ECG_BIOZ_Front_Open_without_Plugins.jpg" target="_blank"><img src="assets/pictures/ECG_BIOZ_Front_Open_without_Plugins.jpg" width="100"></a> | <a href="assets/pictures/Stethoscope_Front_Open_without_Plugins.jpg" target="_blank"><img src="assets/pictures/Stethoscope_Front_Open_without_Plugins.jpg" width="100"></a> | <a href="assets/pictures/PulseOx_Front_Open_without_Plugins.jpg" target="_blank"><img src="assets/pictures/PulseOx_Front_Open_without_Plugins.jpg" width="100"></a> | <a href="assets/pictures/Temp_Front_Open_with_Plugins_2.jpg" target="_blank"><img src="assets/pictures/Temp_Front_Open_with_Plugins_2.jpg" width="100"></a> | <a href="assets/pictures/IMU_Front_Open_with_Plugins.jpg" target="_blank"><img src="assets/pictures/IMU_Front_Open_with_Plugins.jpg" width="100"></a> | <a href="assets/pictures/Environment_Front_Open_with_Plugins_2.jpg" target="_blank"><img src="assets/pictures/Environment_Front_Open_with_Plugins_2.jpg" width="100"></a> |
| **Spirometer** 2026 | **Mouse Monitor** future | **Heater - Cooler**  2026 | **DC - Controller** 2026| **BLDC - Controller** future | Your Suggestion |
| <a href="assets/pictures/placeholder-module.svg" target="_blank"><img src="assets/pictures/placeholder-module.svg" width="100" alt="Lung Capacity closed box not available yet"></a> | <a href="assets/pictures/placeholder-module.svg" target="_blank"><img src="assets/pictures/placeholder-module.svg" width="100" alt="Mouse Mic closed box not available yet"></a> | <a href="assets/pictures/placeholder-module.svg" target="_blank"><img src="assets/pictures/placeholder-module.svg" width="100" alt="Heater - Cooler closed box not available yet"></a> | <a href="assets/pictures/placeholder-module.svg" target="_blank"><img src="assets/pictures/placeholder-module.svg" width="100" alt="DC - Controller closed box not available yet"></a> | <a href="assets/pictures/placeholder-module.svg" target="_blank"><img src="assets/pictures/placeholder-module.svg" width="100" alt="BLDC - Controller closed box not available yet"></a> |  |
| <a href="assets/pictures/placeholder-module.svg" target="_blank"><img src="assets/pictures/placeholder-module.svg" width="100" alt="Lung Capacity open box not available yet"></a> | <a href="assets/pictures/placeholder-module.svg" target="_blank"><img src="assets/pictures/placeholder-module.svg" width="100" alt="Mouse Mic open box not available yet"></a> | <a href="assets/pictures/placeholder-module.svg" target="_blank"><img src="assets/pictures/placeholder-module.svg" width="100" alt="Heater - Cooler open box not available yet"></a> | <a href="assets/pictures/placeholder-module.svg" target="_blank"><img src="assets/pictures/placeholder-module.svg" width="100" alt="DC - Controller open box not available yet"></a> | <a href="assets/pictures/placeholder-module.svg" target="_blank"><img src="assets/pictures/placeholder-module.svg" width="100" alt="BLDC - Controller open box not available yet"></a> |  |

The project files are organized into Education Content: &#128214;, Sources used to determine a solution: &#10004;, Solution: &#128194;, Assembly Instructions: &#128736;, Software: &#128200;


- **General Physiology Background**
    - [Cardiac Physiology](cardiac_physiology.md) &#128214;
    - [Common Physiologic Measurements](physiologic_measurements.md) &#128214;
- **Electro Cardiogram Solutions**
    - [ECG Measurement](ecg_measurements.md) &#128214;
    - [ECG Solutions](ecg_solutions.md) &#10004;
    - [ECG & BIOZ MediBrick](https://github.com/MediBrick/ECG_BIOZ_Brick) based on MAX30001G &#128194;
- **Bio Impedance Solutions**
    - [Impedance Measurement](impedance_measurements.md) &#128214;
    - [Impedance Solutions](impedance_solutions.md) &#10004;
    - [ECG & BIOZ MediBrick](https://github.com/MediBrick/ECG_BIOZ_Brick) sane as ECG  MediBrick &#128194;
    - [Impedance MediBrick (not recommended)](https://github.com/MediBrick/BIOZ_Brick) based on AD5933
- **Stethoscope and Sound**
    - [Sound Measurement](sound_measurement.md)&#128214;
    - [Pressure Measurement](pressure_measurements.md) &#128214;
    - [Sound Solutions](sound_solutions.md) Sound Recording Solutions &#10004;
    - [Pressure Solutions](pressure_solutions.md) Pressure Recording Solutions &#10004;
    - [Stethoscope with Blood Pressure MediBrick](https://github.com/MediBrick/Stethoscope_BP_Brick) &#128194;
- **Pulse Oximeter**
    - [SpO<sub>2</sub> Measurement](spo2_measurements.md) &#128214;
    - [SpO<sub>2</sub> Solutions](spo2_solutions.md) &#10004;
    - [SpO<sub>2</sub> MediBrick](SPO2_Board/README.md) &#128194;
- **Temperature and Strain Gauges**
    - [Temperature Measurement](temperature_measurements.md) &#128214;
    - [Temperature Solutions](temperature_solutions.md) &#10004;
    - [Temperature MediBrick](https://github.com/MediBrick/Thermistor_Brick) &#128194;
- **Acceleration, Gyration, Compass and Pressure Solution**
    - [Activity Measurements with Inertial Measurement Unit](imu_measurements.md)&#128214;
    - [Inertial Measurement Unit Solutions](imu_solutions.md) &#10004;
    - [IMU MediBrick](https://github.com/MediBrick/IMU_Brick)&#128194;
    - IMU MediBrick v2, future includes Real Time Kinematic GPS such as [ZED-F9P](https://www.u-blox.com/en/product/zed-f9p-module)
- **Air Quality**
    - [Airquality Measurement](airquality_measurements.md)&#128214;
    - [Airquality Solutions](airquality_solutions.md) &#10004;
    - [Airquality MediBrick](https://github.com/MediBrick/Airquality_Brick) &#128194;
- **Lung Capacity**
    - [Spirometer Measurements](spirometer_measurements.md)&#128214;
    - [Spirometer MediBrick](https://github.com/MediBrick/Airflow_Brick) &#128194;
- **Heater - Cooler**
    - [Power Control Solutions](power_solutions.md) &#10004;
- **DC Power - Controller**
    - [Power Control Solutions](power_solutions.md) &#10004;
    - [DC Controller MediBrick](https://github.com/MediBrick/DC_Power_Brick) &#128194;
- **Mouse - Mic**
    - Not available yet, likely based on [SN-lab](https://github.com/sn-lab/Mouse-Breathing-Sensor)
- **BLDC - Controller**
    - Not available yet

## Microcontroller and Software

- [Software and Programming](microcontroller_programming.md) 
- [Microcontroller Options](microcontroller_solutions.md)

To visualize data use [SerialUI](https://github.com/uutzinger/SerialUI) &#128200;

## Hardware

### Design and Manufacturing 

- [Mechanical Parts Manufacturing](mechanical_design_and_manufacturing.md): Approach to convert the mechanical models to 3D printing instructions.
- [PCB Design](electronic_design.md): Settings for Eagle CAD & KiCad.
- [PCB Manufacturing](pcb_manufacturing.md): Settings for PCBWay.

### Enclosures
| Assembly| Top | Bottom |
| ------- | ------ |  ------ |
| <a href="https://cad.onshape.com/documents/11cbfe9c3c739b6e8ecbf3d7/w/989b564ecd7f6d069e643ac0/e/85542f706be8cc7554218e8d" target="_blank"> <img src="./Housing Models/Assembly.jpg" width="100"></a> | <a href="https://cad.onshape.com/documents/be6b7e5f847d89f3ec5eb9d5/w/761fee9865ca7ef709028476/e/ff897b4f359cec83b782ff14" target="_blank"> <img src="./Housing Models/Brick-Board.jpg" width="100"></a> | <a href="https://cad.onshape.com/documents/92ad78475e8f0b17ff5e260b/w/88a02abbcb12cdbd4d9de3ad/e/fb79ca58ad2b6a0298e9d1b6" target="_blank"> <img src="./Housing Models/Brick-Microcontroller.jpg" width="100"></a> |

Receiver

Charging Station

## Project Status

| Brick | Mechanical CAD | Electrical CAD|  Assembled | Test Software | Production Software
| ------- | ------ |  ------ | ------ | ------ | ------ |
| **Temperature**       | Completed | Completed | Completed | Completed | Working on |
| **SpO<sub>2</sub>**   | Completed | Completed | Completed | Completed| Working on
| **Stethoscope**       | Completed | Testing   | Refining   | Sound Optimizing, Pressure Testing | N.A.
| **Air Quality**       | Completed | Completed| Completed | MICS sensor support missing | N.A.
| **IMU**               | Completed | Completed | Completed | Completed | Working on
| **Bio Potential and BIOZ** | Completed | Untested | Untested | Driver incomplete | Working on
| **Spirometer**        | Completed | Completed | Ongoing | Completed | Working on |
| **Heater - Cooler**   | N.A. | Incomplete | N.A. | N.A. | N.A. |
| **DC - Power**        | N.A. | Completed | Ongoing | N.A. | N.A. |
| **Mouse Monitor**     | N.A. | Concept | N.A. | N.A. | N.A. |
| **BLDC - Controller** | N.A. | N.A. | N.A. | N.A. | N.A. |
| Protoype Sound w third arty ES8388 | Completed | Completed | Completed | Completed | N.A. |  
| Impedance w AD 5933 network analyzer | Completed | Optimization | Testing| Incomplete | N.A.|
| ECG w Sparkfun Breakout | Completed | Completed | Completed | Completed | N.A. |
| Thermistor/Strain Gauge board using LTC2473 | Completed | Completed | Completed | Completed | N.A. |
