# Academic Scrub — before / after

Domain examples are illustrative; apply the **function**, not the topic.

## 1. Chinese disclaimer (L1)

**Before:**  
这份作业重点讨论柔性传感器的电容与压阻机理；对此本文分别综述读出电路与 DIW 研究进展。

**After:**  
柔性传感器常用电容与压阻两种换能机理。下文比较其读出电路，并综述近年 DIW 可打印传感单元。

---

## 2. Course provenance vs method (L1)

**Before:**  
The measurement principle used here is the course chain for a resistive gauge. A voltage divider is the front end written in the course examples; it is stated in Section II and is not the source of the tabulated voltages. A named product is given in Section IV.

**After:**  
The measurement principle is based on a resistive gauge: deformation changes the film strain, which changes its resistance and is converted to a voltage by the readout circuit. The voltage-divider configuration is described in Section II, whereas the tabulated voltages are calculated using the constant-current configuration.

---

## 3. Team-project / report framing (L1)

**Before:**  
This report therefore compares the two operating principles … as preparation for prototyping a flexible sensing element in the team project.

**After:**  
The review compares the two operating principles, RC-time-constant and voltage-divider readout, design parameters that govern sensitivity and precision, and recent DIW studies relevant to printable flexible sensing elements.

---

## 4. Negative model definition → positive scope (L3)

**Before:**  
Damage, intrinsic piezoresistivity and time-dependent behaviour are not part of this model.

**After:**  
The formulation describes geometry-driven resistance change within the elastic regime. Intrinsic piezoresistive and time-dependent effects remain beyond the present constitutive formulation.

*(If those mechanisms never enter the argument, prefer deleting the exclusion list entirely after stating what the model describes.)*

---

## 5. “No claim is made” → evidence status (L3)

**Before:**  
No particular camera is claimed to achieve this requirement.

**After:**  
Whether these limits can be achieved with the experimental imaging system remains to be established.

---

## 6. “X cannot establish Y” → what Y requires (L3)

**Before:**  
A motor encoder cannot establish local strain.

**After:**  
Local strain therefore requires deformation information beyond actuator position alone.

---

## 7. Command tone → scientific consequence (L3)

**Before:**  
If the validation chain cannot meet the limits, declare surface strain as the measurand and recompute the calibration.

**After:**  
If these limits cannot be achieved, the experimentally accessible surface strain would provide the more appropriate measurand, with calibration, sensitivity, and uncertainty defined on that basis.

---

## 8. We-stack in methods (L4)

**Before:**  
We use \(t\) for conductor thickness. We change \(t\) while keeping \(E_c\) fixed. We selected 1 GPa.

**After:**  
Conductor thickness is denoted by \(t\). Thickness sensitivity is evaluated by varying \(t\) while holding \(E_c\) and the remaining model parameters constant. \(E_c=1\) GPa is selected as the geometric midpoint of the investigated range.

---

## 9. Abrupt gadget opening → topic sentence (L4)

**Before:**  
A motor encoder establishes actuator motion but…

**After:**  
Deformation feedback is required for closed-loop control. Actuator motion alone does not provide local strain, so a conformable gauge is introduced and evaluated using electrical and mechanical metrics.

---

## 10. Defensive Results → dual-metric framing (L3)

**Before:**  
A high gauge factor alone cannot establish suitability. Importantly, the simulation does not prove experimental accuracy.

**After:**  
Performance is evaluated using both electrical response and mechanical demand. Experimental validation remains necessary for absolute accuracy.

---

## 11. Caption essay → reading aid (L4)

**Before:**  
This work is intentionally not plotted as a GF point because the present model does not include intrinsic piezoresistivity and should not be interpreted as a materials GF claim.

**After (caption):**  
Literature benchmark of reported gauge factor (GF) versus working strain range. Marker fill distinguishes primary and contextual values; marker shape denotes sensor family; the dashed line indicates the reference-strain range considered in this study.

*(Move the modelling rationale to the main text.)*

---

## 12. In-figure defensive / insider labels (L4)

**Before:** `our selected one` · `Not validated` · `current best`  
**After:** `present design` · `Experimental verification pending` · `optimized configuration`

---

## 13. Checklist-style reasoning (L1)

**Before:**  
The calculation therefore keeps the bending-face strain near 1%, keeps one layout from Fig. 1(a), and accepts a design only when the voltage rises and the local peak falls inside the force limit.

**After:**  
The analysis evaluates a fixed conductor geometry at approximately 1% tensile strain and selects designs that increase voltage output while reducing local strain concentration within the force limit.

---

## 14. Roadmap meta (L2)

**Before:**  
This section examines the principal design parameters that govern sensitivity, resolution, linearity, hysteresis, and SNR…

**After:**  
Sensitivity, resolution, linearity, hysteresis, and SNR are governed by material composition, electrode geometry, morphology, and viscoelastic history…

---

## 15. Keep (do not over-scrub)

**Keep:** Their sensitivity numbers use different definitions and loading ranges and should not be ranked directly.  
**Keep:** …analogy, not direct evidence for flexible DIW electrodes.  
**Keep:** R0 rises by more than q falls, so ΔV rises.  
**Keep:** The signal is not a direct measurement of strain; it is derived from the resistance change.  
**Keep (cover only):** AI usage declaration required by the course.  
**Keep:** Occasional `we` where the disciplinary voice expects it and density is low.
