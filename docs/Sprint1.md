# Sprint 1 — MVP: Basic Framework and Functionality

**Project:** Smart soil monitoring and watering-support system  
**Controller:** ESP32  
**Sprint focus:** Analogue sensor acquisition, stability testing, local soil calibration, watering-status classification and a local OLED output.

This document records the development, tests, analysis, decisions and evidence for Sprint 1. The system is designed to help non-expert home and school gardeners interpret soil moisture readings as practical watering guidance, without treating a raw analogue value as a direct soil-moisture percentage.

---
## 1. Sprint 1 objectives and plan

The first priority of this sprint was to establish a reliable **sensing and processing framework** before introducing more complex features. I planned to:

1. Confirm that the ESP32 could receive a signal from an analogue sensor.
2. Investigate how the raw ADC output responded to changing physical conditions.
3. Test stability, response over time and repeatability.
4. Trial software filtering to reduce short-term variation.
5. Replace the preliminary resistive sensor with a capacitive soil-moisture sensor.
6. Calibrate soil conditions locally before setting Dry, Suitable and Wet categories.
7. Add a basic local output once the sensing and classification were working.

### Initial sensing approach

The resistive water sensor already available to me was suitable for **preliminary analogue-input experiments**, but not my intended final soil probe. My inquiry found that exposed resistive electrodes could corrode or drift in damp conditions. A capacitive sensor was considered more appropriate for extended contact with soil and was therefore selected for the later prototype.

### Scope decision

The MVP would prioritise trustworthy soil-moisture measurement and a simple recommendation over a wireless dashboard or fully automatic irrigation. A local display would allow users to check the soil condition without a computer, once basic sensing had been verified.
