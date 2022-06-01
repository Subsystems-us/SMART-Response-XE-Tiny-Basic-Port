# SMART-Response-XE-Tiny-Basic-Port
A port of Tiny Basic Plus for the SMART Response XE


**********************************************************************
NOTE: In my Tindie Store I sell this unit with Arduino BASIC installed
**********************************************************************
If differs from Tiny BASIC. To see free memory, use ?. BATT is now a variable so to see battery voltage, use PRINT BATT.
*************************************************************************************************************************


I used Tiny Basic Plus by Gordon Bandly, Mike Field, and Scott Lawrence and the Arduino library for the SMART Response XE by Larry Bank
to port the basic interpreter to the SMART device.

![20210610_205120](https://user-images.githubusercontent.com/78771234/121615018-ef2d6200-ca2d-11eb-914c-564a7f426009.jpg)

The code preserves all of the original commands from Tiny Basic and adds or modifies the following:

LIST: The list command will list the program by page. Click any key to continue paging through. If you want to list to the end, press the space bar.

BYE: Bye will shut down the computer and display, and put the processor to sleep. In this state it consumes very little power. To wake it up, press the power button on the top of the unit.

BATT: The Batt command will return the battery voltage in millivolts.

WAIT: This command waits for a key to be pressed to continue program execution.

MSAVE: This will save the current program into external memory. You must follow the command with the data slot you want to use. There are 10 slots labeled 0 through 9. To save the program to memory slot 5, use the command MSAVE5.

MLOAD: Retrieves the program from memory. If you want to load the program in slot 5, use the command MLOAD5.

Del: The delete key is in the most logical place for the Enter key. In the library, Larry Bank mapped this key to Enter and I think it is the right answer. I tried using the navigation pad right pad for enter and it never felt right. Use the Del key for Enter. Deletion is now mapped to the navigation pad left pad.
**** WARNING ABOUT DELETE ****
Also, I don’t check for invalid keys (like the 10 function keys) so they will just put garbage on the display.

There is no serial or USB port on the device so you have to enter programs manually.

Enjoy!
