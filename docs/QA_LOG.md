
# Quality Assurance Log
## Project: Smart Lawn Sprinkler System

**Student:** Namrata Santosh Babar  
**PRN:** 202301070101  
**Repository:** smart-lawn-sprinkler  
**Platform:** GitHub  
**Controller:** NodeMCU ESP8266

---

## 1. Introduction

This document records the quality assurance issues identified for the Smart Lawn Sprinkler project. It includes the problem description, severity, possible root cause and proposed solution for each issue.

## 2. QA Issue Summary

| Issue ID | Issue Title | Severity | Status |
|---|---|---|---|
| #1 | Soil Moisture Threshold Calibration | High | Open |
| #2 | Incorrect Rain Sensor Output Detection | High | Open |
| #3 | Relay Active LOW and HIGH Logic Mismatch | High | Open |
| #4 | Pump Operating Outside Scheduled Watering Time | High | Open |
| #5 | Sensor Disconnection and Invalid Reading Handling | Medium | Open |
| #6 | Wi-Fi and Blynk Connection Failure Handling | Medium | Open |

## 3. Detailed QA Analysis

### Issue #1: Soil Moisture Threshold Calibration
**Severity:** High

**Problem:** Incorrect soil moisture threshold may cause the pump to operate at the wrong time.

**Root Cause:** The threshold has not yet been verified using sufficient real sensor readings.

**Proposed Solution:** Collect readings under dry and moist soil conditions and select a suitable threshold.

### Issue #2: Incorrect Rain Sensor Output Detection
**Severity:** High

**Problem:** Incorrect digital signal polarity may cause rainfall to be detected incorrectly.

**Root Cause:** The actual digital output polarity of the rain sensor needs verification.

**Proposed Solution:** Test the sensor under dry and wet conditions and configure the correct detection logic.

### Issue #3: Relay Active LOW and HIGH Logic Mismatch
**Severity:** High

**Problem:** Incorrect relay trigger logic may switch the pump ON or OFF unexpectedly.

**Root Cause:** Relay input polarity may not match the Arduino code.

**Proposed Solution:** Verify the relay trigger level and test the relay with the pump disconnected.

### Issue #4: Pump Operating Outside Scheduled Watering Time
**Severity:** High

**Problem:** The pump may operate outside the planned morning and evening watering periods.

**Root Cause:** Scheduling and time validation are not yet implemented in the starter firmware.

**Proposed Solution:** Implement reliable time-based scheduling and ensure the pump remains OFF outside enabled watering periods.

### Issue #5: Sensor Disconnection and Invalid Reading Handling
**Severity:** Medium

**Problem:** Invalid sensor readings may cause incorrect watering decisions.

**Root Cause:** Complete sensor fault detection is not yet implemented.

**Proposed Solution:** Add sensor validation and keep the pump OFF when a sensor fault is detected.

### Issue #6: Wi-Fi and Blynk Connection Failure Handling
**Severity:** Medium

**Problem:** Network disconnection may prevent the dashboard from displaying updated information.

**Root Cause:** Wi-Fi reconnection and Blynk monitoring are not included in the current starter firmware.

**Proposed Solution:** Implement reconnection handling and maintain safe local pump control during network failure.

## 4. Testing Plan

| Test ID | Test Description | Expected Result |
|---|---|---|
| T01 | Test soil moisture readings | Correct dry/moist identification |
| T02 | Test rain sensor in wet and dry conditions | Correct rain detection |
| T03 | Test relay trigger logic | Correct relay switching |
| T04 | Test watering schedule boundaries | Pump OFF outside schedule |
| T05 | Test sensor disconnection | Safe pump OFF response |
| T06 | Test Wi-Fi disconnection | Safe local operation |

**Note:** These are planned tests. Results must be recorded only after actual hardware testing.

## 5. Severity Classification

- High: Issues that may directly affect pump operation or watering decisions.
- Medium: Issues that affect reliability and system monitoring.
- Low: Minor issues with limited impact.

## 6. Conclusion

The QA analysis identifies six important areas that require attention in the Smart Lawn Sprinkler project. These issues will be addressed through testing, debugging and improvements in the firmware.

The GitHub Issues section is used to track problems, while the GitHub Project board is used to monitor their progress.
