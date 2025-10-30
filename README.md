# Unit Design: Centrifugal Separator for Raw Milk and Fat Separation

This project details the individual unit design for a **Tetra Pak H80 centrifugal separator**, a key component in a larger milk fractionation process to produce whey and casein supplements. The report covers the design methodology, starting with a review of initial calculations and comparison of alternative technologies. It establishes material/energy balances, details the mechanical design of components (bowl, piping, motor), and analyzes performance considering factors like pressure drop, non-Newtonian effects, and fouling. The design is finalized with a comprehensive safety and control analysis, including a P&ID, HAZID, LOPA, and start-up/shutdown procedures.

---

## Contents

* **1. Introduction**
    * **1.1. Executive Summary:** A high-level overview of the entire fractionation process, which involves pasteurization, centrifugation (the project's focus), micro/ultrafiltration, and drying to produce casein and whey powders.
    * **1.2. Tetra Pak H80 Separator:** Discusses the chosen unit's role in separating fat (cream) from milk using centrifugal force and its critical importance for the overall process efficiency and final product quality.
    * **1.3. Group Design Calculations - Review:** Identifies and corrects a critical error from a previous group project where the inlet flowrate (99,092.2 kg/hr) exceeded the unit's maximum capacity. This individual project uses a corrected, optimal flowrate of **61,800 kg/hr**

* **2. Unit Design**
    * **2.1. Alternative Options:** Compares the chosen Tetra Pak H80 hermetic separator against other methods (Open-Type, Microfiltration, Flotation, Gravitational). It concludes the H80 is superior due to its high efficiency, larger capacity, and lower risk of contamination.
    * **2.2. Material and Energy Balance:**
        * **Mass and Component Balance:** Establishes the key process flowrates based on the 61,800 kg/hr inlet: **58,710 kg/hr of skim milk** (outlet) and **3,090 kg/hr of cream** (outlet).
        * **Energy Balance:** Concludes that the inlet and outlet temperatures are the same ($50^{\circ}C$) because the separator itself does not contain a heat exchanger.
        * **Assumptions:** Lists the core assumptions for the calculations, including steady-state operation, a constant separation efficiency of 95%, and homogenous milk composition>
    * **2.3. Unit Component Design:**
        * **Inlet and Outlet Pipes:** Calculates the required pipe radii for the inlet (51 mm), skim milk outlet (50.2 mm), and cream outlet (12.2 mm).
        * **Bowl Design:** Determines the separator's key dimensions, including a total volume of 568.9 L, a height of 2.056 m, and a diameter of 1.028 m.
        * **Motor Design:** Selects a Siemens 1LA5 three-phase induction motor and calculates a required operating power of **26.9 kW**.
        * **Disc Stack Design:** Calculates that approximately 29 discs are required and selects Tetra Pak's Encapt polynode disc technology to improve separation efficiency.
        * **Self-Cleaning (CIP) System:** Designs an automated Clean-In-Place (CIP) system using acid, alkali, and sanitizing agents, with a calculated flow rate of 12.45 L/s.
        * **Heat Exchanger:** Details the design of a 15-plate, plate-and-frame heat exchanger used specifically to heat the CIP system's water from $15^{\circ}C$ to $50^{\circ}C$.
        * **Safety Features:** Specifies key safety components, including a Samson Type 3241 pressure control valve (PCV), a thermal safety switch (TSS) set to activate at $54^{\circ}C$, and a PT100 RTD for precise temperature monitoring>

* **3. Optimization and Performance Evaluation**
    * **3.1. Operation Design Limits:** Defines the unit's operational boundaries, including flowrates (7,000 to 80,000 L/hr) and the legal/operational fat content for skim milk (0.01% to 0.3%) 
    * **3.2. Performance Evaluation:**
        * **Pressure Drop:** Uses a 3D MATLAB plot based on the Darcy-Weisbach equation to visualize the relationship between pipe diameter, length, and pressure drop>
        * **Non-Newtonian Effects:** Refines the pressure drop model by incorporating the power-law model, showing that milk's non-Newtonian fluid properties significantly impact the required pipe dimensions>
        * **Fouling:** Further enhances the model by including the effects of fouling (using the Colebrook-White equation). This analysis reveals that unrealistic pipe lengths or fluid velocities would be needed to achieve the target pressure drop with fouling, highlighting a key design trade-off 

* **4. Mechanical Design**
    * **4.1. Material Selection:** Selects **Grade 304H stainless steel** for the piping and **UNS32750 Super Duplex steel** for the bowl, citing their superior corrosion and thermal resistance>
    * **4.2. Thickness and Weight of Unit:** Calculates the required wall thickness for the bowl (11.54 mm) and the inlet piping (2.26 mm) based on ASME standards. The total weight of the main components is also calculated>
    * **4.3. Design Procedures and Codes:** Confirms the design adheres to key industry standards: **ASME B31.3** (for piping), **ASME BPVC Section VIII** (for the pressure vessel/bowl), and **3-A Sanitary Standards** (for hygiene)>
    * **4.4. Mechanical Drawings:** Provides simplified side, end, and magnified views of the separator with key dimensions>

* **5. P&ID, Control Systems, and Unit Safety**
    * **5.1. P&ID:** Introduces the Piping and Instrumentation Diagram as the core schematic for the unit's operation and control>
    * **5.2. Control Strategy:** Details the four main control loops (Temperature, Pressure, Level, and Flow) designed to maintain optimal and safe operation. A key finding is the need for both pressure and temperature control on the skim milk outlet to prevent protein denaturation and foaming>
    * **5.3. PID Control:** Explains the Proportional-Integral-Derivative (PID) control algorithm. It compares the **Cohen-Coon** and **Ziegler-Nichols** tuning methods, ultimately selecting the Cohen-Coon method because it is more stable, less aggressive, and better suited for maintaining product quality in this process>
    * **5.4. HAZID:** Presents a Hazard Identification (HAZID) study in a table, identifying potential hazards from process fluid release (e.g., acid spills), utility failure (e.g., electrical), human error, and equipment failure (e.g., pipe rupture)>
    * **5.5. LOPA:** Conducts a Layer of Protection Analysis (LOPA) for three critical scenarios: seal failure, overheating, and overpressure. The analysis finds that the total Risk Reduction Factor (RRF) for all scenarios (e.g., **21,200 for seal failure**) is well within the company's tolerable risk limit (<10⁶).
    * **5.6. Start-up and Shutdown Procedures:** Provides a step-by-step list for safely starting (including the CIP cycle) and stopping the separator. It emphasizes a gradual reduction of flow to prevent thermal shock to the equipment>
    * **5.7. Cleaning and Maintenance:** Discusses the primary factors requiring maintenance (Fouling, Corrosion, Wear and Tear) and the mitigation methods, such as chemical cleaning protocols, material selection, and component lubrication>

* **6. Conclusion**
    * **6.1. Specification Sheet:** Summarizes the final design specifications for the Tetra Pak H80 in a comprehensive data sheet. This includes the final flowrates (61,800 kg/hr in), operating conditions ($50^{\circ}C$, 650 kPa), and key dimensions (2.056 m height, 1.028 m width).

* **7. References**
    * Lists all 148 sources cited throughout the report>

* **8. Appendix**
    * Contains supplementary information, including the Moody Diagram, detailed weight calculations, the P&ID legend, and the MATLAB code used for the 3D performance evaluation plots>
