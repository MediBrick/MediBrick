# MediBrick

A cost-effective Solution for Biomedical Measurements.

Urs Utzinger, and engineering capstone teams: 24052, 23094, 26048.
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

| ECG and<br>Impedance | Stethoscope<br>and Blood<br>Pressure | Pulse<br>Oximeter | Temperature | Inertial<br>Measurement<br>Unit | Air<br>Quality |
| --- | --- | --- | --- | --- | --- |
| <a href="assets/pictures/ECG_BIOZ_Front_Closed_without_Plugins.jpg" target="_blank"> <img src="assets/pictures/ECG_BIOZ_Front_Closed_without_Plugins.jpg" width="100"> </a> | <a href="assets/pictures/Stethoscope_Front_Closed_with_Plugins.jpg" target="_blank"><img src="assets/pictures/Stethoscope_Front_Closed_with_Plugins.jpg" width="100"></a> | <a href="assets/pictures/PulseOx_Front_Closed_with_Plugins.jpg" target="_blank"><img src="assets/pictures/PulseOx_Front_Closed_with_Plugins.jpg" width="100"></a> | <a href="assets/pictures/Temp_Front_Closed_with_Plugins.jpg" target="_blank"><img src="assets/pictures/Temp_Front_Closed_with_Plugins.jpg" width="100"></a> | <a href="assets/pictures/IMU_Front_Closed_without_Plugins.jpg" target="_blank"><img src="assets/pictures/IMU_Front_Closed_without_Plugins.jpg" width="100"></a> | <a href="assets/pictures/Environment_Front_Closed_without_Plugins.jpg" target="_blank"><img src="assets/pictures/Environment_Front_Closed_without_Plugins.jpg" width="100"></a> |
| <a href="assets/pictures/ECG_BIOZ_Front_Open_without_Plugins.jpg" target="_blank"><img src="assets/pictures/ECG_BIOZ_Front_Open_without_Plugins.jpg" width="100"></a> | <a href="assets/pictures/Stethoscope_Front_Open_without_Plugins.jpg" target="_blank"><img src="assets/pictures/Stethoscope_Front_Open_without_Plugins.jpg" width="100"></a> | <a href="assets/pictures/PulseOx_Front_Open_without_Plugins.jpg" target="_blank"><img src="assets/pictures/PulseOx_Front_Open_without_Plugins.jpg" width="100"></a> | <a href="assets/pictures/Temp_Front_Open_with_Plugins_2.jpg" target="_blank"><img src="assets/pictures/Temp_Front_Open_with_Plugins_2.jpg" width="100"></a> | <a href="assets/pictures/IMU_Front_Open_with_Plugins.jpg" target="_blank"><img src="assets/pictures/IMU_Front_Open_with_Plugins.jpg" width="100"></a> | <a href="assets/pictures/Environment_Front_Open_with_Plugins_2.jpg" target="_blank"><img src="assets/pictures/Environment_Front_Open_with_Plugins_2.jpg" width="100"></a> |
| **Spirometer**<br>2026 | **Mouse<br>Monitor**<br>future | **Heater -<br>Cooler**<br>2026 | **DC -<br>Controller**<br>2026 | **BLDC -<br>Controller**<br>future | Your<br>Suggestion |
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
    - [ECG & BIOZ MediBrick](https://github.com/MediBrick/ECG_BIOZ_Brick) same as ECG  MediBrick &#128194;
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
| Assembly| Top | Bottom | Top with Display |
| ------- | ------ |  ------ | ------ |
| <a href="https://cad.onshape.com/documents/11cbfe9c3c739b6e8ecbf3d7/w/989b564ecd7f6d069e643ac0/e/85542f706be8cc7554218e8d" target="_blank"> <img src="./Housing Models/Assembly.jpg" width="100"></a> | <a href="https://cad.onshape.com/documents/ebcdcbc3e7eb802e05aa7127/w/92c7f2c4a3604ac0392e9e89/e/23d2cedb30284d3e07ce3fd7" target="_blank"> <img src="./Housing Models/Brick-Board.jpg" width="100"></a> | <a href="https://cad.onshape.com/documents/3fee40e68f3fb61ffdb812bb/w/65bb78ada38672d141a5d154/e/0ff82183503e2fd6c450e151" target="_blank"> <img src="./Housing Models/Brick-Microcontroller.jpg" width="100"></a> | <a href="https://cad.onshape.com/documents/c77dd983220b67f240ac3c83/w/46a38f84b86eeefe1a16b563/e/cb5fcb49f9eac92ef2c0d8fc" target="_blank"> <img src="./Housing Models/Brick-Microcontroller-Display.png" width="100"></a>|
| Generic 3D Printer  | [3mf](/Housing%20Models/Brick-Top-v2.2.3mf)      | [3mf](/Housing%20Models/Brick-Bottom-v2.2.3mf)| [3mf](/Housing%20Models/Brick-Top-Display-v2.2.3mf)
| Bambu 3D Printer | [3mf Bamu](/Housing%20Models/Brick-Top-v2.2-Bambu.3mf) | [3mf Bambu](/Housing%20Models/Brick-Bottom-v2.2-Bambu.3mf) | [3mf Bambu](/Housing%20Models/Brick-Top-Display-v2.2-Bambu.3mf) |

### Face Plates

[All Face Plate - 3mf Bambu](/Housing%20Models/Plate-All-Bambu.3mf)

| ECG and<br>Impedance | Stethoscope<br>and Blood<br>Pressure | Pulse<br>Oximeter | Temperature | Inertial<br>Measurement<br>Unit | Air<br>Quality |
| --- | --- | --- | --- | --- | --- |
| <a href="https://cad.onshape.com/documents/4b23bdc1fe41aa5490b46d9c/w/fd4737f6a1ca7fbcd3b1d7f7/e/89122d5ddac798ebf451ad60" target="_blank"> <img src="./Housing Models/Plate-BIOZ.png" width="100" alt="ECG and Impedance"></a> | <a href="https://cad.onshape.com/documents/06546d5c2b6ecb0931149c5d/w/2aa54258cb58c3e795c7fea9/e/823e2851771a01788a8faacf?renderMode=0&uiState=6ae0ddb90c129e27744a4ee3" target="_blank"> <img src="./Housing Models/Plate-Stet.png" width="100" alt="Electronic Stethoscope and Blood Pressure"></a> | <a href="https://cad.onshape.com/documents/bcb286d5b9de6189ba796e00/w/0a567208a5b563fc8cacc531/e/83b1b9bbadf693deafbe5817?renderMode=0&uiState=6ae0dfe921af6fd93ccd3eac" target="_blank"> <img src="./Housing Models/Plate-SpO2.png" width="100" alt="Pulse Oximeter"></a> | <a href="https://cad.onshape.com/documents/dac7e67c5b0270015712d245/w/d60526c34fb0e9aab2c02a4b/e/8ff2bfb0681baf7e99de5ea6?renderMode=0&uiState=6ae0dddc6de4d7ca6fd8081f" target="_blank"> <img src="./Housing Models/Plate-Temp.png" width="100" alt="Temperature"></a> | <a href="https://cad.onshape.com/documents/eb58e78174fdb2053487973b/w/903e17c4126fb90e8782ab92/e/d48348f9b25ba3f16b712f17?renderMode=0&uiState=6ae0ddf926be22b8c4e38dbd" target="_blank"> <img src="./Housing Models/Plate-Activity.png" width="100" alt="Inertial Measurement Unit"></a> | <a href="https://cad.onshape.com/documents/6f9a87cae125641fc3a0651c/w/6e25f32c6ac446efd4e51be7/e/a5b61964693009981eab589c?renderMode=0&uiState=6ae0de19acf0aa66b2cc3514" target="_blank"> <img src="./Housing Models/Plate-Env.png" width="100" alt="Air Quality"></a> |
| [3mf](/Housing%20Models/Plate-BioZ.3mf) | [3mf](/Housing%20Models/Plate-Stet.3mf) | [3mf](/Housing%20Models/Plate-SpO2.3mf) | [3mf](/Housing%20Models/Plate-Temp.3mf) | [3mf](/Housing%20Models/Plate-IMU.3mf) | [3mf](/Housing%20Models/Plate-Env.3mf) |
| [3mf Bambu](/Housing%20Models/Plate-BioZ-Bambu.3mf) | [3mf Bambu](/Housing%20Models/Plate-Stet-Bambu.3mf) | [3mf Bambu](/Housing%20Models/Plate-SpO2-Bambu.3mf) | [3mf Bambu](/Housing%20Models/Plate-Temp-Bambu.3mf) | [3mf Bambu](/Housing%20Models/Plate-IMU-Bambu.3mf) | [3mf Bambu](/Housing%20Models/Plate-Env-Bambu.3mf) |
| **Spirometer** | **Mouse<br>Monitor**<br>future | **Heater -<br>Cooler** | **DC -<br>Controller** | **BLDC -<br>Controller**<br>future | Your<br>Suggestion |
| <a href="https://cad.onshape.com/documents/46a5928b4676a5c421e437e3/w/b54629e17e0805c84654254a/e/496a4d7b998282ef1a835923?renderMode=0&uiState=6ae0e053a244174fd640cdd0" target="_blank"> <img src="./Housing Models/Plate-Spiro.png" width="100" alt="Spirometer** 2026 faceplate"></a> | <a href="./assets/pictures/placeholder-module.svg" target="_blank"> <img src="./assets/pictures/placeholder-module.svg" width="100" alt="Mouse Monitor future faceplate not available yet"></a> | <a href="./assets/pictures/placeholder-module.svg" target="_blank"> <img src="./assets/pictures/placeholder-module.svg" width="100" alt="Heater - Cooler 2026 faceplate not available yet"></a> | <a href="./assets/pictures/placeholder-module.svg" target="_blank"> <img src="./assets/pictures/placeholder-module.svg" width="100" alt="DC - Controller 2026 faceplate not available yet"></a> | <a href="./assets/pictures/placeholder-module.svg" target="_blank"> <img src="./assets/pictures/placeholder-module.svg" width="100" alt="BLDC - Controller future faceplate not available yet"></a> |  |
| [3mf](/Housing%20Models/Plate-Spiro.3mf) |  |  |  |  |  |
| [3mf Bambu](/Housing%20Models/Plate-Spiro-Bambu.3mf) |  |  |  |  |  |


### Receiver
Not availale yet

### Charging Station
Not available yet

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
