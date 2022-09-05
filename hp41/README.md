# E6-B for HP-41

This contains a set of functions for the HP-41CX or other HP-41 models with the HP 82180A Extended Functions module inserted.

# Implemented Programs

This is still work-in-progress. Programs are implemented on-demand, feel free to request them via an issue.

## DST and PTHMS

DST (Distance, Speed, Time) is a limited re-implementation from scratch of the FM program contained in the HP-41C AVIATION PAC release by HP. It behaves similary but does not currently support the fuel calculation functionality of the FM program.

When started it emits `D=S*T      X`. The idea is to set any two of the three values in the `D=S*T` formula and solve for the third. To set one of the values, enter the desired value on the keypad and press the A, B or C button, the button association follows the same order as the formula printed on screen, i.e. A for D, B for S, C for T. To solve for the third variable, just press the desired button without entering a numerical value first. The X button closes the program and cleans up the state.

It expects no parameters as it is entirely interactive. while running it activates user mode and modifies printing flags. The flags are restored when exiting the program using the X button.

## INMB and MBIN

Converts athmospheric pressure between inch of mercury and millibars.

It expects the source value in the X register, returns the result in the X register. It overwrites the source value and drops the value in the T register.

## KMHKT and KTKMH

Converts speed between kilometers per hour and knots. 

It expects the source value in the X register, returns the result in the X register. It overwrites the source value and drops the value in the T register.

# Installation

For models supporting it, you can generate ready-to-use .raw files that you can copy to your device.
To build the .raw files run `make all`. It requires the `comp41` command from [lifutils](https://github.com/bug400/lifutils) for building. 

Otherwise you can also manually enter the source code of the individual programs into your machine.

# Testing

The code was manually tested on Virtual HP-41 Release 9H and a SwissMicros DM41X.
