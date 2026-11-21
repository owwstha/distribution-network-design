#distribution-line-design
## 1. Project Overview

* **Scope:** Supply 68 households (100 W each, 6.8 kW total) on the south spur below Bahundanda bazaar. The voltage-drop limit is 5 %. The route comes from a desktop survey only.
* **Design:** A 269 m 11 kV tap (ACSR Squirrel) from the existing NEA feeder feeds a 25 kVA 11/0.4 kV Dyn11 transformer (`T1`). Four radial LV feeders (`A` to `D`) run on 53 poles.
* **Voltage drop (hand calculation and independent sweep):** The worst drop is 2.3 % from `T1-LV` and about 3.7 % from the 11 kV source, meeting the 5 % limit at 100 W per house.
* **ETAP:** Unbalanced load flow (100 % and 150 % load), 3-phase and 1-phase short circuit, and Star protection coordination have been run. The 3-phase fault results agree with the hand values within about 3 %.
* **Data error found:** Far-end ETAP results do not match yet. Both the load-flow cable drops and 1-phase fault currents point to identical cable lengths that belong to other branches (Section 4.4). The lengths must be corrected and the studies rerun before final report inclusion.
* **Protection:** An HV K-link fuse (6K class) and a 16 A MCCB on each LV feeder coordinate in ETAP Star (minor tidy-up remaining).
* **Growth margin:** Small; measured from the 11 kV source, the 5 % voltage-drop limit is reached at about 140 W per house.
* **Cost:** Rs 34,05,433 in total (~Rs 50,080 per house), unchanged from Handover 1.

---

## 2. Design Basis

### Network
* **Source (assumed):** Existing NEA 11 kV feeder, tap pole `HT00` ($28.34271^\circ\text{ N}, 84.40667^\circ\text{ E}$, elevation ~1,279 m), 3-pole ABS.
* **11 kV line (`HT00` to `T1`):** 269 m, 3-phase, ACSR Squirrel.
* **Transformer (`T1`):** 25 kVA, 11/0.4 kV, Dyn11, double-pole structure, DO fuses, 9 kV lightning arresters, LV box with 4 MCCB ways.
* **LV Network:** Four radial feeders, 53 LV poles. ACSR Gopher from `T1` to `D06`, ACSR Squirrel elsewhere. Phase map: $\text{R} = \text{A}$, $\text{Y} = \text{B}$, $\text{Blue} = \text{C}$.

### Impedance Data

| Element | $R$ ($\Omega/\text{km}$) | $X$ ($\Omega/\text{km}$) | Notes |
| :--- | :---: | :---: | :--- |
| **Squirrel, LV** | 1.374 | 0.324 | $X$ from $\text{GMR} = 0.726r$, $0.4\text{ m}$ spacing |
| **Squirrel, 11 kV** | 1.374 | 0.382 | $1.0\text{ m}$ spacing; $Z_0 = 3 \times Z_1$ |
| **Gopher, LV** | 1.093 | 0.317 | `T1` to `D06` only |
| **T1 to A08 ($Z_0$)** | 5.496 | 1.296 | $Z_0 = 4 \times Z_1$: full-size neutral earthed only at `T1` |
| **T1 to D06 ($Z_0$)** | 4.372 | 1.268 | As above |
| **T1** | — | — | $4\%$, $X/R = 1.0$, $Z_0 = Z_1$, solidly earthed star, tap 0 (typical, not nameplate) |
| **Source U1** | — | — | 25 MVA 3-phase and 1-phase, $X/R = 2$, $1.00\text{ pu}$ (assumed) |

### Main Assumptions
* **Desktop survey only:** Pole positions and lengths are not site-checked.
* **Load:** 100 W per house, $\text{pf} = 0.8$, constant-power loads.
* **Utility parameters:** NEA source point, fault level, and conductor practice are assumed pending NEA confirmation.
* **Transformer impedance:** `T1` impedance is a typical value, not a nameplate value.
