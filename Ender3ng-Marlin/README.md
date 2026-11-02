# Ender 3 NG v1.2 CoreXY (SKR E3 V3 mini)

- Frame: Ender 3 NG v1.2 CoreXY conversion, 235 mm bed, PEI spring steel
- Board: BTT SKR E3 V3 mini (STM32G0B1RE), TMC2209 drivers, stock Ender 3 12864 LCD + SD
- Extruder: direct drive protostruder, HGX-Lite 9:1, NEMA 14
- Probe: BLTouch clone (Twotrees 3D Touch), signal on Z-STOP
- Endstops: X min (left), Y max (back), NC switches
- Firmware: Marlin 2.1.2.9, PlatformIO env `STM32G0B1RE_btt`
- Slicer: Orca (Marlin 2 flavor)

## Layout
- `firmware/` Marlin config files and flashing notes
- `slicer/orca/` machine G-code, limits, process profiles
- `filaments/` one folder per material
- `calibration.md` measured values

## Flashing
Build `firmware.bin`, copy to the SD card **with a new file name each time** (the board ignores a file it already flashed), power-cycle, then `M503` to check settings.
