# FixM600.py - Improves/fixes PrusaSlicer Color Change Problem

The default behavior of PrusaSlicer 2.5.x and 2.6 (at least through Alpha 6) does the color change at the end of the layer - before traveling to the next print position of the next layer. This can leave a blob in the previous layer when the printer resumes after color change.

This post-processing script moves the M600 command to right before the first extrusion of the next layer. Additionally, you can prime the nozzle after color change, using an extra g-code command.

@awbom tested this using an Ender-3 V2 with "Professional Firmware" (mriscoc).  I've tested on a Prusa Mini running 4.3.1 firmware.
Use

Add the following line in Print Settngs > Output Options > Post-processing scripts:

   path to python3   path to FixM600.py/FixM600.py;


 In addition to moving the M600 command, you can also prime the nozzle with an extra extrusion by adding:

     G1 E6 F2400;

 This script was forked from  https://github.com/awabom/3dprint.


I have used this on Prusa Slicer 2.5 and 2.6 Allpha 6 with good results.  Works on my Prusa Mini,
but since it rewrites the gcode it should work on any printer.
