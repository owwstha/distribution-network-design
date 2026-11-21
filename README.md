# distribution-network-design
•	Scope: supply 68 households (100 W each, 6.8 kW) on the south spur below Bahundanda bazaar. The voltage-drop limit is 5 %. The route comes from a desktop survey only.
•	Design: a 269 m 11 kV tap (ACSR Squirrel) from the existing NEA feeder feeds a 25 kVA 11/0.4 kV Dyn11 transformer (T1). Four radial LV feeders (A to D) run on 53 poles.
•	Voltage drop (hand calculation and independent sweep): the worst drop is 2.3 % from T1-LV and about 3.7 % from the 11 kV source, so the design meets the 5 % limit at 100 W per house.
•	ETAP: unbalanced load flow (100 % and 150 % load), 3-phase and 1-phase short circuit, and Star protection coordination have been run. The 3-phase fault results agree with the hand values within about 3 %.
•	Data error found: the far-end ETAP results do not match yet. The load-flow cable drops and the 1-phase fault currents both point to the same cable lengths, and those lengths belong to other branches (section 4.4). The lengths must be corrected and the studies rerun before the ETAP numbers go in the final report.
•	Protection: an HV K-link fuse (6K class) and a 16 A MCCB on each LV feeder coordinate in ETAP Star. Some tidy-up is left.
•	Growth margin is small: measured from the 11 kV source, the 5 % limit is reached at about 140 W per house.
•	Cost: Rs 34,05,433 in total, about Rs 50,080 per house (unchanged from handover 1).
2. Design basis
Network
•	Source (assumed): existing NEA 11 kV feeder, tap pole HT00 (28.34271 N, 84.40667 E, about 1,279 m), 3-pole ABS. 
•	11 kV line HT00 to T1: 269 m, 3-phase, ACSR Squirrel. 
•	T1: 25 kVA, 11/0.4 kV, Dyn11, double-pole structure, DO fuses, 9 kV lightning arresters, LV box with 4 MCCB ways.
•	LV: four radial feeders, 53 LV poles. Gopher on T1 to D06, Squirrel elsewhere. Phase map: R = A, Y = B, Blue = C.
mpedance data
Element	R (ohm/km)	X (ohm/km)	Notes
Squirrel, LV	1.374	0.324	X from GMR = 0.726 r, 0.4 m spacing
Squirrel, 11 kV	1.374	0.382	1.0 m spacing; Z0 = 3 x Z1
Gopher, LV	1.093	0.317	T1 to D06 only
T1 to A08 (Z0)	5.496	1.296	Z0 = 4 x Z1: full-size neutral earthed only at T1
T1 to D06 (Z0)	4.372	1.268	as above
T1	-	-	4 %, X/R 1.0, Z0 = Z1, solidly earthed star, tap 0 (typical, not nameplate)
Source U1	-	-	25 MVA 3-phase and 1-phase, X/R 2, 1.00 pu (assumed)
Main assumptions
•	Desktop survey only: pole positions and lengths are not site-checked.
•	100 W per house, pf 0.8, constant-power loads.
•	NEA source point, fault level and conductor practice are assumed until NEA confirms them.
•	T1 impedance is a typical value, not a nameplate value.
