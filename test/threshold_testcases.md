# PTPS Threshold Test Cases

## Test Case 1 – Normal Operation
Inputs:
- PTPS_SYSTEM_INPUT = 90
- CONSOLIDATED_LAS = 0
- PSNP_FFRPT_SIGNAL = 0
Expected: "System Operating Normally"

## Test Case 2 – Threshold Breach
Inputs:
- PTPS_SYSTEM_INPUT = 120
- CONSOLIDATED_LAS = 1
- PSNP_FFRPT_SIGNAL = 1
Expected: "MisTrack Detected – Threshold Breached"
