Notes for assembling the board
===

1. Be really careful not to accidentally short vias. They are unfortunately very close to the through hole pads in some
places.

2. The resistor and capacitor values in the schematic for the ICG are not trustworthy. Use the latest design from the ICG
team. ECG and PPG should be mostly ok but double check them anyway (PPG gain resistor value isn't in schematic, for 
instance). The level shifter circuit may need some debugging but should theoretically work. I believe it's the only 
part that hasn't been fully prototyped yet.

3. Pin 8 of IC5 needs to be connected to RI25 with a jumper wire. Look at sheet 5 for details (it's the place with the
missing junction. I didn't catch the mistake in time)

4. Resistors and capacitors are named according to which part of the circuit they are part of: RIxx for ICG, RExx for ECG,
RPxx for PPG, RAxx for the level shifter. These components are grouped together on the board. Be careful not to confuse 
"CI6" with "C16", for instance.

5. The switches on the ICG might need series resistors on the clock input.

6. Many optional elements were included for maximum flexibility. Pay attention to whether a particular resistor isn't needed.
For instance, the optional gain resistors on the Sallen-Key filter in the ICG (one should be shorted, one should be open). Don't populate the capacitors in the level
shifter unless you specifically want to add an extra pole.

7. The silkscreen for the capacitors is pretty minimal, so be really careful to make sure to use the correct holes for the
caps.

