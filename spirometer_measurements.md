**Introduction to Spirometry and Lung Volumes**

Spirometry is a fundamental respiratory test used to assess lung function by measuring the volume and flow of air during inhalation and exhalation. The test provides insights into a patient's breathing patterns and can be used to detect and monitor respiratory diseases. The figure below shows the key lung volume measures, which include:

![Figure 1. Example spirogram showing lung volume as a function of time](assets/spirogram_time_volume.jpg)

[source](https://histology.oit.duke.edu/MBS/Videos/Phys/Phys%205.2%20Resp%20Lung%20Volumes/Phys%205.2%20Resp%20Lung%20Volumes.pdf)


- **Tidal Volume (TV):** The amount of air inhaled or exhaled during normal, resting breathing (typically 400–600 mL).
- **Inspiratory Reserve Volume (IRV):** Additional air that can be forcibly inhaled after a normal inhalation (typically >1700 mL).
- **Expiratory Reserve Volume (ERV):** Additional air that can be forcibly exhaled after a normal exhalation (~800–1200 mL).
- **Residual Volume (RV):** Air remaining in the lungs after maximal exhalation (~1200 mL); not measurable by spirometry.
- **Inspiratory Capacity (IC):** Maximum air that can be inhaled after a normal exhalation; **IC = TV + IRV.**
- **Functional Residual Capacity (FRC):** Volume of air in lungs after a normal exhalation; **FRC = ERV + RV**.
- **Vital Capacity (VC):** Maximum amount of air that can be exhaled after a maximal inhalation; **VC = IRV + TV + ERV**.
- **Total Lung Capacity (TLC):** Total volume the lungs can hold; **TLC = VC + RV.**
- **Forced Vital Capacity (FVC):** The total amount of air exhaled during a forced breath (~3000–5000 mL).
- **FEV₁%:** The percentage of the FVC exhaled in the first second; this value helps assess obstruction (~90%+ in normal lungs).
- **FEF₂₅–₇₅:** The average flow rate during the middle portion of a forced exhalation (4.5 L/s).

![Figure 2. Lung volumes and capacities measured in spirometry](assets/spirometer_lung_volumes_diagram.png)

[source](https://en.wikipedia.org/wiki/Spirometry)

By plotting **flow versus volume**, a spirogram is generated, providing a visual representation of lung performance. This is especially useful for distinguishing between:

- **Normal lungs:** Full volume range, symmetrical loop.
- **Obstructive disorders (e.g., COPD):** Normal volume but reduced flow rate; scooped-out expiratory curves.
- **Restrictive disorders:** Reduced total lung volume with preserved flow patterns.

**Diagnose Normal Lung Function, Obstructive, or Restrictive Lung Disorder**

|     |     |     |     |
| --- | --- | --- | --- |
| Measured Value | Normal | Obstructive (Reduced Flow) | Restrictive (Reduced Capacity) |
| Lung Volumes (TV, IRV and ERV) | Normal: Equal or more than the expected volumes | Normal: About the expected volumes | Low: Significantly less than expected volumes |
| FVC | Normal | Normal | Low: Lungs move less than the normal amount of air |
| FEV₁% | Normal: 90%+ | Low: Less than ~70% of normal airflow | Normal: Airflow is normal |
| FEF₂₅–₇₅ | Normal: Equal or more than the normal value | Low: Significantly less than normal | Normal: Airflow is normal |

Case Analysis

|     |     |     |     |
| --- | --- | --- | --- |
|     | TV (mL) | IRV (mL) | ERV (mL) |
| Case 1 | 400 | 2600 | 1000 |

![Figure 3. Volume versus time curve for Case 1](assets/spirometer_case1_volume_time.png)

|     |     |     |     |
| --- | --- | --- | --- |
|     | TV (mL) | IRV (mL) | ERV (mL) |
| Case 2 | 500 | 2300 | 900 |

![Figure 4. Volume versus time curve for Case 2](assets/spirometer_case2_volume_time.png)

|     |     |     |     |
| --- | --- | --- | --- |
|     | FVC (mL) | **FEV₁%** | **FEF₂₅–₇₅ (L/s)** |
| Case 1 | 4000 | 50  | 0.7 |

![Figure 5. Flow–volume loop for Case 1 indicating obstructive lung disease](assets/spirometer_case1_flow_volume_loop.png)

|     |     |     |     |
| --- | --- | --- | --- |
|     | FVC (mL) | **FEV₁%** | **FEF₂₅–₇₅ (L/s)** |
| Case 2 | 3500 | 95  | 4.0 |

![Figure 6. Flow–volume loop for Case 2 showing normal lung function](assets/spirometer_case2_flow_volume_loop.png)

- **Case 1** has normal FVC (4000 mL) but severely reduced FEV₁% (50%) and FEF₂₅–₇₅ (0.7 L/s), indicating **obstructive lung disease**, likely COPD.
- **Case 2** displays near-normal values (FVC 3500 mL, FEV₁% 95%, FEF₂₅–₇₅ 4.0 L/s), indicating **normal lung function**.

**Preface:**

The spirometer brick is part of the _MediBrick Project_. This spirometer device is designed specifically for educational demonstration and student experiments. The goal is to help learners understand the physics behind respiratory mechanics and thermal mass flow sensing, rather than to provide medical diagnostic results. By visualizing real-time flow data and calculated volume, students can connect theoretical principles with hands-on measurement.

**Composition of spirometer:**

The spirometer is mainly composed of these parts:

- Mouthpiece
- Airflow tube
- Flow sensor

(Other electronics will be added later.)

![Figure 7. Flow sensor setup showing airflow path from breathing mask to sensor](./assets/spirometer_setup.jpg)

**Basic principle**

The flow sensor used in this project is the SFM3300-D. This is a thermal mass flow-rate sensor that directly measures airflow. It has a bidirectional range (±250 slm) and outputs a digital flow value. Because it provides real-time flow data for both inhalation and exhalation, we do not require a separate differential pressure sensor to generate the spirogram (flow vs. volume curve). This simplifies the design and enhances measurement accuracy for educational and demonstration purposes.

The SFM3300-D uses thermal mass flow sensing technology.

Equation 1. Convective heat transfer relation

$$\dot Q = hA(T_h - T_g)$$


This equation is derived from heat-transfer theory and is the physical basis of thermal mass flow detection.

The working mechanism of the SFM3300-D is based on convective heat transfer and temperature-difference detection. As airflow passes through the sensor, it carries heat away from the heating membrane. The sensor calculates mass flow rate by detecting these temperature-difference changes. The heat-loss rate $\dot Q$ is proportional to the mass flow rate $\dot m$:

$$\dot Q \propto \dot m = \rho A \nu$$

where $\rho$ is gas density, $A$ is the cross-sectional area, and $\nu$ is the average velocity.

Although the sensor measures mass flow rather than velocity $\nu$, its digital output is converted to a standardized volume-flow rate $Q_{slm}$

under reference conditions:

$Q_{slm} = \dot m / \rho_{std}$

Lung volumes are obtained by time integration:

$V := \int_{0}^{T} Q(t)\,dt, \qquad v(t) := \frac{Q(t)}{A}$

Thus, the sensor’s flow-rate output effectively represents the average airflow speed inside the device.

In conventional airflow measurement, the gas density $\rho$ is assumed constant. However, in human exhalation, the molar mass $M$ and temperature $T$ both increase compared to ambient air, according to the ideal-gas law:

$\rho = PM / RT$

where $R$ is the universal gas constant and $P$ is pressure. Typical changes in $M$ (due to added CO₂ and H₂O) and in $T$ (warmer exhaled air) cause $\rho$ to vary by about 2-5%. If the system assumes a fixed density when converting flow to volume, this produces a proportional error in the computed lung volume:

$$\Delta V / V \approx \Delta \rho / \rho$$

That means a 5% density change would lead to roughly a 5% volume-calculation error.

The SFM3300-D avoids this problem by directly measuring mass flow rather than velocity or volume flow, because the measured variable already includes $\rho$.

The sensor output inherently compensates for these density variations. Its on-chip digital temperature sensor further corrects for residual thermal effects, maintaining an accuracy of ±3% of reading and only ±0.4% per 10 °C temperature drift. These compensations are based on dry-air calibration. When measuring exhaled breath containing water vapor and CO₂, the gas properties slightly differ from the dry-air model, so an additional BTPS correction needs to be applied in the spirometer software.

**Flow Measurement: Pressure Drop vs Thermal Sensing**

Traditionally, spirometers use a differential pressure sensor to measure the pressure drop across a resistance element and derive flow. However, the SFM3300-D sensor eliminates this need by providing direct mass flow measurement with high precision. Because it senses flow without relying on pressure differentials, there’s no need for multiple pressure ports or compensations.

By measuring mass flow directly, the SFM3300-D also inherently accounts for changes in gas density and temperature. This improves accuracy compared to simple velocity-based methods, especially when measuring exhaled air, which is warmer and contains more water vapor.

**Future Enhancements: Airway Pressure Monitoring**

Although a pressure sensor is not required for spirometry, adding one could expand the functionality of the device. For example, airway pressure monitoring is essential in applications like CPAP therapy, mechanical ventilation, and anesthesia machines. In these systems, pressure data is used to control airflow, protect the airway, and detect patient-triggered breathing efforts.

Sensirion’s evaluation kit for the SFM3300 series includes a clip-on module with a built-in pressure sensor, demonstrating how pressure sensing can be incorporated into a flow-based system. In future iterations, we may add such a sensor to study airway pressure dynamics alongside flow, further enriching the educational experience.

**Directions for use:**

(To be added: full components list, schematics, step-by-step assembly instructions, software/operation instructions, CAD models, and electronics.)