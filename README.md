# FreeCAD_Macros
### FreeCAD macros for laser cutting
Here are a couple of macros for FreeCAD for designing laser cut boxes for different material thicknesses.
I have found a number of cool box designs online but invariably they were designed for a different thickness
of material than I have on hand and resizing is non-trivial. So I wrote these macros to allow me to create a box
with any material thickness.

The **LaserCutBox** macro creates a basic "tabbed" box with optional slots to allow for an inset lid. Simply 
enter the inside dimension of the box, the material thicknesses, tab width and number of tabs for each side. 
The macro will then generate a sketch for each side selected that can then be exported to a .DXF file for 
lasercutting.

The **LivingHingeBox** macro is a bit more complicated as cutting the hinge itself is complicated.  I originally
planned to somehow calculate the number and size of each segment based on material thickness but, I was
unable to find an algorithm that worked reliably.  Through trial and error I came up with some suggested 
defaults but YMMV so you might have to do your own T&E.  Here's what has worked for me:

3 mm (1/8") material - 6 to 8 3 mm segments</br>
5 mm (3/16") material - 7 or 8 3 mm segments</br>
6.5 mm (1/4") material - 7 to 9 4 mm segments

Feel free to experiment but, I would not recommend a segment size smaller than 3 mm or greater 
than 4 mm.</br></br>
In any case, the number and size of the segments should probably total more than the arc length of the corner
radius, e.g. a 15 mm radius (the only one I've tested) has an arc length of 23.6 mm.
(1/4 of the perimeter)

Also, it is **very important** that you measure the thickness of your material (preferably with calipers) 
to be sure the tabs will fit together. (HINT: round up a bit to be sure there's room.)</br></br>
As for the basic box, the macro will generate sketches that can be exported.  Be very careful 
when assembling the box as the hinges can snap unexpectedly if over stressed. They seem to be fairly robust
once the box is glued together. (HINT: for thicker materials I've heard, but haven't tried, that 
steaming the wood can help.)
### Installation
Just download all the files and copy them to your FreeCAD macro folder. (take the FCMacro and ui files
out of their sub-folders)
### Have Fun!!
Once you have exported the files you can import them into an app like LightBurn or RDWorks and then
apply your own designs to the sides. (don't put anything where hinge segments will be cut) 
Also, consider trying other materials. Acrylic should work well.

I hope you find these macros useful, feel free to modify the code to make it your own and please let 
me know if you find better ways of doing things.
