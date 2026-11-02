# Calibration log

Single source of truth for measured values. Update after every change and note the date.

| Item | Value | How measured | Date |
|---|---|---|---|
| X / Y steps/mm | 80 | 20T GT2, 16 microsteps | |
| Z steps/mm | 800 | 10 mm Z move test (verify!) | 2026-11-01 |
| E steps/mm | ~1360 | two 100 mm tests: 90 mm moved @1240, 42 mm moved @569.2 | 2026-11-01 |
| Linear Advance K | 0.03 (start) | calibrate with Orca PA tower | |
| Probe offset (M851) | X ? Y ? Z ? | Probe Offset Wizard on hot bed | |
| E current (M906 E) | 500-650 mA | | |
| Input shaping | 40 Hz X/Y placeholder | needs resonance test | |
| Hotend PID | | M303 E0 S200 C8 U1 | |
| Bed PID | | M303 E-1 S60 C8 U1 | |

Rule: save runtime changes with `M500`. A reflash can reset EEPROM, so also put values in `Configuration.h`.
