# WLAN-design-for-SAIT-Senator-Burns
# Senator Burns (Floor 1) – WLAN Design, Implementation &amp; Validation  Team project for CPNT-302-B Wireless Networking. We designed, sized, and validated a Wi-Fi 6 network across six blocks (NH, NJ, NK, NR, NL, NN) using Bluebeam Revu, ExtremeCloud IQ (AP410C), and TamoSoft. Target: RSSI ≥ −65 dBm @ 5 GHz with seamless roaming.
# Senator Burns (Floor 1) – WLAN Design, Implementation & Validation

## Overview
Team project for **CPNT-302-B Wireless Networking** (Dylan Yee, Aira Therens, Amrit Kaur Dhiman, Ridwan Adesina).  
We designed, sized, and validated a production-style WLAN for **SAIT’s Senator Burns Building, Floor 1**, across six blocks:

- **Blocks:** NH (Red), NJ (Green), NK (Purple), NR (Pink), NL (Orange), NN (Blue)  
- **Tools Used:** Bluebeam Revu (survey & calibration), ExtremeCloud IQ (predictive design), AP410C Wi-Fi 6 APs, TamoSoft (validation)  
- **Targets:** RSSI ≥ −65 dBm (5 GHz), seamless roaming in corridors, classroom capacity, optimized channel/power plan  

---

## Phase 1 — WLAN Site Survey
- Imported building floorplan into **Bluebeam Revu** and calibrated scale.  
- Identified wall types & attenuation for RF modeling:  

| Material / Feature             | Loss (dB) |
|--------------------------------|-----------|
| Drywall (classroom ↔ classroom) | 3 dB |
| Brick / tiled corridor walls    | 10 dB |
| Concrete / exterior / shafts    | 12 dB |
| Elevator shaft                  | 30 dB |

- Bandwidth/user = **4–8 Mbps** depending on activity (Zoom, Brightspace, YouTube).  
- Example: **30 students × 4 Mbps = 120 Mbps per classroom**.  
- Corridors: roaming only (~1 Mbps/device).  

---

## Phase 2 — Predictive WLAN Design (ExtremeCloud IQ)
**Access Point Model:** Extreme **AP410C (802.11ax)**, ceiling-mounted (~2.6–2.7 m), internal omni antenna.

| Setting | Classrooms | Corridors |
|---------|------------|-----------|
| Radios | Dual-band (2.4 + 5 GHz) | 5 GHz only |
| Channel Width | 40 MHz (5 GHz) | 20 MHz |
| Tx Power | 16 dBm (5 GHz) / 7 dBm (2.4 GHz) | 8–10 dBm (5 GHz) |
| Target | RSSI ≥ −65 dBm | Roaming continuity |

**AP Count by Block**

| Block | APs Deployed | Notes |
|-------|--------------|-------|
| NH (Red) | 10 | 2 corridor + 8 classrooms |
| NJ (Green) | 12 | 2 corridor + 10 rooms/labs |
| NK (Purple) | 22 | 4 corridor + 18 rooms/labs |
| NR (Pink) | 9 | 2 corridor + 7 classrooms |
| NL (Orange) | 26 | 3 corridor + 23 labs/classrooms/offices |
| NN (Blue) | 22 | 3 corridor + 19 mixed-use (cafeteria, rotunda, offices) |
| **Total** | **101** | across all blocks |

**Capacity Estimates (examples):**
- NH: ~240 users, 1.9–2.0 Gbps aggregate  
- NJ: ~200 users, ~719 Mbps  
- NK: ~248 users, ~892 Mbps  
- NR: ~164 users, ~443 Mbps  
- NL: ~194 users, ~780 Mbps  
- NN: ~209 users, ~593 Mbps  

---

## Phase 3 — Implementation Plan
High-level integrator handoff:

| Phase | Task | Duration | Dependencies | Notes |
|-------|------|----------|--------------|-------|
| 1 | Pre-install walkthrough | 1 day | — | Verify cable drops, AP mounting |
| 2 | Cat6 cable runs | 3–5 days | 1 | PoE runs to ceiling APs |
| 3 | Switch install + PoE test | 2 days | 2 | Verify power at drops |
| 4 | WLC config (ExtremeCloud IQ) | 1–2 days | 3 | SSIDs, VLANs, radio tuning |
| 5 | AP installation | 3 days | 4 | Follow AP placement plan |
| 6 | Coverage testing | 2 days | 5 | Ensure −65 dBm in classrooms |
| 7 | Optimization & tuning | 2 days | 6 | Adjust Tx power & channels |
| 8 | Documentation & handover | 1 day | 7 | Provide maps, configs, results |

---

## Bill of Materials (BoM)
**1. Access Points**  
- Extreme AP410C (Wi-Fi 6) — 78 units @ $311 CAD → $23,947  

**2. Switches**  
- ExtremeSwitching X435-24P-4S (PoE+) — 4 units @ $1,500 CAD → $6,000  

**3. Wireless LAN Controller (Cloud)**  
- ExtremeCloud IQ SaaS — 1 license → $1,800  

**4. Cabling & Accessories**  
- Cat6 cabling (~3,000 m) → $1,500  
- Patch panels, RJ-45, mounting kits → $500  

**Total Estimated Cost:** **$33,747 CAD**  

---

## Phase 4 — Post-Deployment Validation
- Validation survey performed with **TamoSoft**:  
  - Actual PHY rates  
  - TCP/UDP upstream/downstream throughput  
  - Packet loss & RTT  
  - Associated APs heatmaps  

- **Findings:**  
  - Classrooms & labs: coverage and performance met design specs.  
  - Corridors: lower but adequate signal for roaming (by design).  
  - Overall: WLAN meets performance requirements for high-density academic use.  

---

## Artifacts
## Artifacts

### 📍 Block Maps (Phase 1 – Site Survey)
- [Area – Block Red (NH)](Area-%20Block%20Red%20-%20NH.png)
- [Area – Block Green (NJ)](Area-%20Block%20Green%20-%20NJ.png)
- [Area – Block Purple (NK)](Area-%20Block%20Purple%20-%20NK.png)
- [Area – Block Pink (NR)](Area-%20Block%20Pink%20-%20NR.png)
- [Area – Block Orange (NL)](Area-%20Block%20Orange%20-%20NL.png)
- [Area – Block Blue (NN)](Area-%20Block%20Blue%20-%20NN.png)

### 📶 Heatmap Coverage (Phase 2 – Predictive Design)
- [Heatmap – Block Red (NH)](heat%20map%20coverage-%20Block%20Red.png)
- [Heatmap – Block Green (NJ)](heat%20map%20coverage-%20Block%20green.png)
- [Heatmap – Block Purple (NK)](heat%20map%20coverage-%20Block%20purple.png)
- [Heatmap – Block Pink (NR)](heat%20map%20coverage-%20Block%20pink.png)
- [Heatmap – Block Orange (NL)](heat%20map%20coverage-%20Block%20orange.png)
- [Heatmap – Block Blue (NN)](heat%20map%20coverage-%20Block%20blue.png)

### ✅ Validation Survey Results (Phase 3 – Post Deployment)
- [Validation – NH](validation%20survey%20area%20NH.png)
- [Validation – NJ](validation%20survey%20area%20NJ.png)
- [Validation – NK](validation%20survey%20area%20NK.png)
- [Validation – NL](validation%20survey%20area%20NL.png)
- [Validation – NN](validation%20survey%20area%20NN.png)
- [Validation – NR](validation%20survey%20area%20NR.png)


---

## Lessons Learned
- **Wall modeling matters**: calibration and attenuation selection drives AP count.  
- **5 GHz-only corridors** = better roaming, less contention.  
- **High-density classrooms** required more APs with 40 MHz channels.  
- **Validation is critical**: predictive ≠ real deployment; post-deployment tuning improved roaming.  

---

## Team
- **Dylan Yee**  
- **Aira Therens**  
- **Amrit Kaur Dhiman**  
- **Ridwan Adesina**

---
