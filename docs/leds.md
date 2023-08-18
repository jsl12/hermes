# LED Information

## Strips

### Construction

- FCOB - flexible chip-on-board, which refers to the manufacturing method. This method allows the individual LEDs to be really closely spaced.
- SMT - surface mount

### Color Types

- RGB - red, green, blue
  - Each individual LED package has 3 physical diodes in it, one for each color
  - Good for multicolor, but not shades of white (use CCT instead)
- [CCT](https://en.wikipedia.org/wiki/Correlated_color_temperature)
  - [color temperature](https://en.wikipedia.org/wiki/Color_temperature)
  - Each LED package has 2 physical diodes - cool white (CW) and warm white (WW)
- [CRI](https://en.wikipedia.org/wiki/Color_rendering_index)
- 24V is good for longer continuous runs

### Control Schemes

#### Single Color (Analog)

Most LED strips are controlled as a single color with an analog signal. The signal is a PWM between a wire with the positive supply voltage and the wire for each LED. The color spectrum is made up of different combinations of power sent to each LED.

For example an RGB signal would have 4 wires:

- V+
- R (red)
- G (green)
- B (blue)

A CCT signal would just be 3 wires:

- V+ 
- CW (cool white)
- WW (warm white)

#### Addressable (Digital)
