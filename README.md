# M600-Fix

Prusa Slicer 2.5 and the early 2.6 Alphas all have a problem doint manual color changes.  
They leave a spot of the new color whereever the print head was at the end of printing the old color.

FixM600.py is a GCode parser to fix the problem.

This is forked from https://github.com/awabom/3dprint.

From the comment at the beginning of the file it appears that the original author may be @mriscoc.

I have used this on Prusa Slicer 2.5 and 2.6Allpha6 with good results.  Works on my Prusa Mini,
but since it rewrites the gcode it should work on any printer.
