# F-16 Altimeter

![Altimeter](pics/altimeter.jpg)

All the files I created my altimeter from...

* The FCStd*-Files are all parts I created in FreeCAD.  
Not all of them are for 3Dprinting, some are just for reference.

* In the folder "3DprintFiles" are the exported parts as .3mf-files to use in your slicer.  
I'm not sure, if all the parts are up2date, since often I do some changes in FreeCAD without exporting the files afterwards.
Best strategy would be to export each part directly from the FreeCAD files.

* The "arduino" folder holds the sourcecode for the Arduino-side of [BMSAIT](https://github.com/mihi4/BMSAIT) by Robin "HummerX" Bruns.  
You can get the Windows program in the link above.
centerController.ini should be used as configuration file in BMSAIT.

The Nano will drive the Centerconsole instruments, except the ADI and HSI.  
Altimeter, the 2 ASI needles, 4 additional servos of VVI and AOA and the MarkerBeacon

- pin A5: input for rotary push to reset motor
- pin A6: switch for pneu/elec
- pin A7: input to zeroize the stepper 
- pins 2, 3: rotary encoder (2 interrupt pins)
- pins 4, 5, 6, 7: Altimeter continous x27 motor
- pins 8, 9, 10: max7210 for 4+3 7-segment displays
- pins 11, 12, 13, A1, A2, A3, A4: servos for PNEU flag, KIAS, MACH, VVI, AOA, VVIFlag, AOAFlag
- pin A0: marker beacon LED

There are no files for the connectionboard of the LEDMatrixBoard to the displays.  
You will have to find the specific pinout with a multimeter and then solder the right pin of the displays to it.

## !!! Use those files at your own risk !!!

All the files are free to use under the GNUGPLv3

If you find those files useful and would like to support me with an icecream, coffee or pizza, you can use paypal.me to do so ;)  
[Paypal.me](https://paypal.me/MichiHirczy)
