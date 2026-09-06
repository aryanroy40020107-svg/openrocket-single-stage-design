# openrocket-single-stage-design
Single-stage high-altitude model rocket design and flight simulation using OpenRocket. Features 1000m+ apogee, sub-Mach 0.8 velocity, and complete subsystem analysis.


# OpenRocket Single-Stage Model Rocket Design & Flight Simulation

An end-to-end design, analysis, and flight simulation project for a single-stage model rocket built using **OpenRocket**. Developed for the **India Space Lab (ISL) Rocketry Training Program** (Winter Internship Training Program, Feb–Mar 2026).

The primary objective of this project is to engineer an optimized single-stage high-altitude model rocket that strictly adheres to structural, stability, aerodynamic, and recovery constraints.

---

## 🚀 Mission Constraints vs. Achieved Results

| Parameter | Mission Constraint | Simulation Result | Status |
| :--- | :--- | :--- | :--- |
| **Apogee** | $\ge 1000\text{ m}$ | **$1004\text{ m}$** | ✅ Passed |
| **Stability Margin** | $1.0\text{--}2.0\text{ calibers}$ | **$1.66\text{ calibers}$** | ✅ Passed |
| **Max Velocity** | Subsonic ($\text{Mach} < 0.8$) | **$\text{Mach } 0.798$** ($271\text{ m/s}$) | ✅ Passed |
| **Recovery Descent Rate** | $< 10\text{ m/s}$ | **$6.87\text{ m/s}$** | ✅ Passed |
| **Lift-off Mass** | $< 1.5\text{ kg}$ | **$702\text{ g}$** ($0.702\text{ kg}$) | ✅ Passed |
| **Total Length** | $800\text{--}1200\text{ mm}$ | **$939\text{ mm}$** | ✅ Passed |

---

## 🛠 Subsystem Breakdown & Technical Specifications

### 1. Airframe & Nose Cone
* **Nose Cone Profile:** Tangent Ogive (Shape parameter = 1) for minimal wave drag and smooth airflow transitions.
* **Nose Cone Dimensions:** Length $5\text{ cm}$, Base Diameter $5.4\text{ cm}$, Wall Thickness $0.2\text{ cm}$.
* **Material:** Polystyrene (Density: $1.05\text{ g/cm}^3$, Mass: $23.3\text{ g}$).
* **Body Tube:** Outer Diameter $5.4\text{ cm}$, constructed from lightweight fiberglass.

### 2. Aerodynamic Stability (Fin Subsystem)
* **Fin Configuration:** 3 trapezoidal fins with an **airfoil cross-section** to minimize parasitic drag.
* **Fin Dimensions:** Root chord $7\text{ cm}$, Tip chord $4\text{ cm}$, Height $5.5\text{ cm}$, Sweep angle $61^\circ$.
* **Structural Integration:** Through-the-wall (TTW) fin tabs ($5\text{ cm}$ length) anchored into the body tube to eliminate fin flutter under high launch acceleration ($\sim 483\text{ m/s}^2$).
* **Material:** High-stiffness Fiberglass (Density: $1.85\text{ g/cm}^3$, Mass: $42.8\text{ g}$).

### 3. Propulsion System
* **Motor:** Certified **AeroTech H283ST-7** (DMS single-use case, Super Thunder propellant).
* **Total Impulse:** $199\text{ Ns}$ (H-class).
* **Average / Peak Thrust:** $270\text{ N}$ / $337\text{ N}$.
* **Burn Time:** $0.738\text{ s}$.
* **Thrust-to-Weight Ratio:** $\sim 41.1:1$ (exceeds the minimum safety limit of $5:1$, ensuring immediate off-the-rail flight stability).

### 4. Recovery Subsystem
* **Parachute:** $60\text{ cm}$ diameter Ripstop Nylon ($67\text{ g/m}^2$, $C_D = 0.800$).
* **Shroud Lines:** 6 elastic cords ($60\text{ cm}$ length, $1.8\text{ g/m}$).
* **Deployment:** Single-stage deployment triggered at apogee / $200\text{ m}$ ejection charge.
* **Descent Velocity:** Stable touchdown at $\sim 6.8\text{ m/s}$.

### 5. Payload & Avionics
* **Payload Mass:** $111\text{ g}$ (axially centered, offset $-17.7\text{ cm}$ from mid-body).
* **Avionics:** Altimeter integrated into the middle body section for accurate apogee log and recovery triggering.

---

## 📈 Flight Dynamics & Simulation Plots

Simulation outputs generated using **OpenRocket v23.09** confirm stable static and dynamic flight behaviors throughout launch, coast, apogee, and descent:

1. **Altitude, Acceleration & Velocity vs. Time:** Demonstrates smooth boost phase up to peak acceleration ($483\text{ m/s}^2$), coasting phase reaching $1004\text{ m}$ apogee, and constant-velocity parachute descent.
2. **Center of Gravity (CG) vs. Center of Pressure (CP):** Margins remain within $1.66\text{ calibers}$ throughout burn and coast phases, ensuring dynamic resistance to weathercocking.
3. **Drag Coefficient vs. Mach Number:** Drag spikes remain bounded during trans-sonic region ($\text{Mach } 0.798$), verifying subsonic compliance.

---

## 📂 Repository Structure


.
├── rocketry_documentation_by_aryanroy_jgec_isl.pdf   # Complete project documentation & analysis report
├── rocket_design.ork                             # OpenRocket CAD/Simulation design file
├── README.md                                     # Project summary & technical overview
└── LICENSE                                       # Open-source license (MIT)


🔧 How to Run the Simulation
Download OpenRocket: Download and install OpenRocket (Java-based open-source rocketry simulator).
Download Design File: Download rocket_design.ork directly from this repository.
Open Design File: Launch OpenRocket, click File $\rightarrow$ Open, and select rocket_design.ork.Run Flight Simulations: Navigate to the Flight Simulations tab and click Run Simulation to verify apogee, Mach numbers, and stability margins.

👤 Author Aryan Roy
B.Tech Student, Jalpaiguri Government Engineering College (JGEC)Winter Internship Training Program — India Space Lab (ISL)

📜 License
This project is open-source and available under the MIT License.

