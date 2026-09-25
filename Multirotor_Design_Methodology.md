# Multirotor Design Methodology

Designing a multirotor around specific **payload weight ($W_p$)** and **endurance ($t$)** constraints is an iterative sizing process. You must balance energy density, motor-propeller efficiency, and structural mass.

---

## 1. Initial Mass Estimation

To size components, estimate your **Maximum Takeoff Weight (MTOW)** ($W_{mtow}$). A common rule of thumb for endurance multirotors is that payload accounts for **15% to 25%** of the total aircraft mass ($m_{tot}$).

$$\text{MTOW} \approx \frac{W_p}{0.20}$$

where\
Structural Mass ($m_{frame}$) $\approx 20\\% - 25\\%$ of MTOW\
Battery Mass ($m_{bat}$) $\approx 45\\% - 55\\%$ of MTOW\
Payload Mass ($m_{payload}$) $\approx 20\\%$ of MTOW\
Avionics & Motors ($m_{elec}$) $\approx 10\\% - 15\\%$ of MTOW

---

## 2. Power and Propulsion Sizing

### A. Thrust-to-Weight Ratio
For a stable multirotor, aim for a thrust-to-weight ratio between **1.8:1 and 2.2:1** at maximum throttle.

$$\text{Total Required Thrust} \approx 2.0 \times \text{MTOW}$$

$$\text{Thrust Per Motor} = \frac{\text{Total Required Thrust}}{\text{Number of Motors ($N$)}}$$

### B. Propeller Selection
Endurance scales directly with propeller disc area and pitch-to-diameter ratio:
* **Large Diameter + Low Pitch:** Higher aerodynamic efficiency ($\text{g/W}$) at hover. Select the largest propeller size your frame footprint allows.
* Look for carbon fiber props designed for low-RPM endurance (e.g., T-Motor P-series).

### C. Motor KV Selection
Match the motor KV to the propeller size and battery voltage ($V$):
* **High Payload / High Endurance:** Low KV motors (100–400 KV) paired with high voltage (6S to 12S LiPo/Liion).
* **Hover Efficiency Target:** Target a motor/propeller combination that achieves **$\ge 8 \text{ to } 10 \text{ g/W}$** at hover thrust ($W_{mtow} / N$).

---

## 3. Battery Configuration & Energy Budget

To achieve high endurance ($>30\text{ minutes}$), battery chemistry choice is critical:

* **LiPo (Lithium Polymer):** Higher discharge C-rate, lower energy density ($\sim 180\text{–}220 \text{ Wh/kg}$). Best for heavy payloads or high-wind environments requiring quick throttle response.
* **Li-ion (Lithium-ion):** Higher energy density ($\sim 250\text{–}300 \text{ Wh/kg}$ using 18650/21700 cells), but lower C-rate capability. Ideal for long-endurance, steady hover, or light-payload profiles.

### Estimating Hover Time ($t$)

1. **Calculate Hover Power ($P_{hover}$):**
   $$P_{hover} = \frac{\text{MTOW (g)}}{\eta_{hover} \text{ (g/W)}}$$
   *(where $\eta_{hover}$ is prop/motor efficiency in g/W at hover thrust)*

2. **Calculate Required Battery Capacity ($E_{req}$ in Wh):**
   $$E_{req} = \frac{P_{hover} \times t \text{ (hours)}}{\text{DOD}}$$
   *(where DOD is Depth of Discharge, typically 0.80 for battery longevity)*

3. **Verify Battery Weight:**
   $$m_{bat} = \frac{E_{req}}{\text{Specific Energy (Wh/kg)}}$$

If calculated $m_{bat}$ significantly exceeds your initial target mass fraction ($>55\%$), you must reduce payload, increase prop size/efficiency, or lower your target endurance.

---

## 4. Design & Iteration Workflow

1. **Define Hard Requirements**
   * *Set non-negotiable mission specs:* Establish payload weight ($W_p$), target flight time ($t$), maximum dimensions/frame envelope, and operating environment (wind, altitude).
2. **Select Battery Chemistry**
   * *LiPo vs. Li-ion:* For flights under 30 minutes, choose LiPo. For low-current endurance flights over 30–45+ minutes, configure a custom Li-ion pack (e.g., 6S6P 21700 cells).
3. **Size Propellers and Motors**
   * *Maximize hover efficiency:* Consult manufacturer thrust/power tables (e.g., T-Motor, KDE Direct). Find a motor + prop combination yielding $\ge 9 \text{ g/W}$ at hover thrust for your estimated MTOW.
4. **Select Frame & Layout**
   * *Quad vs. Hexa vs. Octo:*
     * **Quad (X4):** Highest efficiency (lowest frame weight and parasitic drag).
     * **Hexa / Coaxial (X8):** Better wind tolerance and redundancy for expensive payloads.
5. **Refine Mass Budget & Validate**
   * *Iterate until convergence:* Sum actual component masses ($m_{frame} + m_{motors} + m_{esc} + m_{fc} + m_{payload} + m_{bat}$). Re-calculate $P_{hover}$ and $t$. Repeat steps until total mass and required flight time converge.
