## Welcome to my 3d Printer Setup Page

## What you find
You will find informaion about my efforts to handle and calibrate my anycubic mega x 3d printer. 

## How to Calibrate the Printer

# Extruder Steps
To calibrate your extruder, you have to extrude filament with the hotend. 
Therefore you have to measure the filament before the extruder and extrude a specific amount of material. The printer should be heated so you don't damage your printer.
After that you measure again what is left of the filament. The difference can be used to calibrate the esteps of the extruder 

Gcode to set extruder to relative mode
`M83`

Gcode to extract 10 mm filament
`G1 E10 F100`

Gcode to get the information of the esteps
``

Formula for the the new extruder config
``


Gcode to configure the extruder
``

# Z offset

# Fillament thickness
