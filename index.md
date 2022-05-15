## Welcome to my 3d Printer Setup Page

## What you find
You will find informaion about my efforts to handle and calibrate my anycubic mega x 3d printer. 

## How to Calibrate the Printer

### Heat Tower
[my cura file | ]
[Heat Tower on Thingiverse | ]

[Heat Toiwer German | https://www.youtube.com/watch?v=wlRO5C9CUb0&list=PLIr33KPqFkS7zMYsN66CPz1qMfeKCvnlc&index=1&t=1140s]

### Extruder Steps
To calibrate your extruder, you have to extrude filament with the hotend. 
Therefore you have to measure the filament before the extruder and extrude a specific amount of material. The printer should be heated so you don't damage your printer.
After that you measure again what is left of the filament. The difference can be used to calibrate the esteps of the extruder 

Gcode to set extruder to relative mode

`M83`

Gcode to extract 10 mm filament with speed of 100

`G1 E10 F100`

Gcode to get the information of the esteps
`M503`
Search for M92
And take the last value of the esteps

Formula for the the new extruder config
```
new_steps = wanted_extrusion / real_extrusion * current_steps
````


Gcode to configure the extruder
`M92 Enew_steps`

### Z offset

### Fillament thickness

### Extrusion multiplyer / Flowrate
It's quite easy you just print a cube with one layer without top and bottom with a specific width. Take 0,45 mm width for it.
Then measure all five walls and take the mean of it.
```
extrusion_multiplyer = 0.45 / mean_value
```
