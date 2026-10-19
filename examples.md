# Academic Scrub — before / after

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

## 4. Defensive file clarification (L3)

**Before:**  
The conductive body is the imported flexible-ink mesh. A second 3MF file, a printed composite trace whose file name contains R12, is stored with it. These two meshes are the geometry inputs. They are not a SolidWorks drawing set, and they are not three CAD projects named P, F, and R16.

**After:**  
The geometry inputs are the imported flexible-ink mesh and a second 3MF composite-trace mesh identified as R12.

---

## 5. Requirement language (L1)

**Before:**  
For the strain-and-bending scene in Fig. 1(b), Table II leaves one paired requirement. The voltage has to follow the surface strain closely enough to be a precise reading, and the same trace has to carry that bending without a local peak that would crack or drift it.

**After:**  
For strain and bending, the design must balance measurement accuracy against local mechanical demand. The voltage should track surface strain closely, while the trace must accommodate bending without excessive local strain that could cause cracking or drift.

---

## 6. Defensive qualification (L3)

**Before:**  
The 99th percentile is a choice: a 90th or 95th percentile would blunt real hotspots, and the 100th percentile is the mesh-sensitive maximum. It is a static design objective, not a measured fatigue life.

**After:**  
The 99th percentile balances sensitivity to local hotspots against the mesh sensitivity of the absolute maximum. C99 is used as a static measure of strain concentration rather than a fatigue-life metric.

---

## 7. Checklist-style reasoning (L1)

**Before:**  
The calculation therefore keeps the bending-face strain near 1%, keeps one layout from Fig. 1(a), and accepts a design only when the voltage rises and the local peak falls inside the force limit.

**After:**  
The analysis evaluates a fixed conductor geometry at approximately 1% tensile strain and selects designs that increase voltage output while reducing local strain concentration within the force limit.

---

## 8. Roadmap meta (L2)

**Before:**  
This section examines the principal design parameters that govern sensitivity, resolution, linearity, hysteresis, and SNR…

**After:**  
Sensitivity, resolution, linearity, hysteresis, and SNR are governed by material composition, electrode geometry, morphology, and viscoelastic history…

---

## 9. Lab-kit brand leakage (L1)

**Before:**  
B. Voltage Divider and Arduino ADC Readout. For a classical Arduino Uno, N = 10…

**After:**  
B. Voltage Divider and Microcontroller ADC Readout. For a 10-bit microcontroller ADC (N = 10)…

---

## 10. Keep (do not over-scrub)

**Keep:** Their sensitivity numbers use different definitions and loading ranges and should not be ranked directly.  
**Keep:** …analogy, not direct evidence for flexible DIW electrodes.  
**Keep:** R0 rises by more than q falls, so ΔV rises.  
**Keep (cover only):** AI usage declaration required by the course.
