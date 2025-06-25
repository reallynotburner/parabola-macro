# Parabola Macro

## Overview
Function that uses current tool position and arguments to make parabolic shapes out of round stock in Computer Numerically Controlled (CNC) lathes.  The code is EIA-ISO, known to machinists as [G Code](https://en.wikipedia.org/wiki/G-code).

## Features
- Usage is similar as the G71 canned cycle, but with parabola specific arguments.
- Position the parabola with the X and Z arguments anywhere in your tool envelope.
- Specify a sub section of the parabola with the A and B arguments for beginning Z and final Z coordinate.  If B > A, the parabola will open in the Z- direction.  A < B the parabola will open in the Z+ direction.
- Scale the parabola in the X direction with the C argument.  Negative value for C will cause the curve to move in the X- direction.

## Usage
    ```
    ; O19760041
    ; PARABOLIC MACRO USAGE
    G28U0W0 ;
    T101 ;
    G00 X0. Z0. ;
    M3 S1000 F10. ;
    ; CALL MACRO
    G65 P19760020 X0. Z0. A0. B6. C1. D.1 U.010 W.005 ;
    M30 ;
    ```
## Contributing
Contributions are welcome! Do a pull request, make a comment.

## License
This project is licensed under the [MIT License](/license.txt).

## Contact
[reallynotburner@github.com](mailto:reallynotburner@github.com).