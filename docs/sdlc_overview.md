# Software Development Life Cycle (SDLC) Overview

This document outlines the Software Development Life Cycle (SDLC) followed during the development and testing of a generalized **PTPS MisTrack Threshold Selection** module. The original work was carried out as part of an internship at **DRDO – ADE**, and this simulation replicates the logic flow and verification strategy using dummy data for demonstrative purposes only.

---

## 📌 1. Requirements Analysis

The system needed to evaluate **mis-track conditions** during flight based on real-time input signals such as:
- `PTPS_SYSTEM_INPUTS`
- `PTPS_CONSOLIDATED_LAGS`
- `PSNP_IFFRFP_SIGNALS`
- System enable signal: `ENABLE_20HZ`
- Reference thresholds: `PTPS_MISTRACK_THRESHOLDS`

These inputs collectively determine whether the aircraft's tracking behavior falls within acceptable thresholds, or if a mis-track event should be flagged.

---

## 🎨 2. System Design

Below is the architectural diagram showcasing the signal flow and module dependencies:

![PTPS MisTrack Threshold Selection](../diagrams/ptps_threshold_architecture.png)

The system logic was designed to:
- Read input signals at a frequency of 20 Hz
- Compare real-time values against a set of static thresholds
- Process input signals through filtering logic
- Output a status flag indicating whether the system is operating normally or mis-tracking

---

## 💻 3. Implementation

The logic was simulated using **MATLAB** to replicate real-time signal processing.

Key logic features:
- Conditional signal evaluation
- Dynamic input thresholds
- System enable/disable logic
- Modular design for testability

Example file: `src/ThresholdSimulation.m` or `src/ThresholdSimulation.py`

---

## 🧪 4. Testing

Testing was conducted in alignment with **LDRA-style unit and integration testing**, focusing on the following:
- Signal correctness
- Boundary conditions
- MCDC (Modified Condition/Decision Coverage) analysis

Test case document: [`test/threshold_testcases.md`](../test/threshold_testcases.md)

Tested conditions included:
- Normal operation vs. mis-track detection
- Missing signals
- Out-of-threshold values
- Multiple active signals

---

## ✅ 5. Verification & Validation

The logic was validated using:
- MATLAB plots and signal simulators
- Assertion-style conditional testing
- Comparison with expected threshold-based outputs

**MCDC coverage** was used as a metric to ensure that all logical paths were triggered during testing, satisfying basic avionics safety coverage standards.

---

## 🧾 6. Documentation

The entire simulation and structure was documented following standard SDLC practices:
- Design diagram placed in `/diagrams`
- README with project context
- Code in `/src`
- Test cases in `/test`
- This SDLC document in `/docs`

---

## 🔒 Confidentiality Disclaimer

> This repository is a **generalized simulation** of my internship experience at **DRDO – ADE**. It does not contain any real, sensitive, or classified data or code. All information shared is educational and illustrati
