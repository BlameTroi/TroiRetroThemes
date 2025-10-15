# 3270/9 Colors and their use

These were CRT displays, initially using green phosphor. The display background was not a true black, and was very faintly green. Unlike modern character or bit addressable displays, the 3270 family displayed characters within fields. The fielding was for transmission efficiency. Fields had attributes: binary switches describing how to display the field and whether or not it was modifiable.

## Basic 3270 displays

The field attributes that relate to color theming are:

- Protected
- Displayable
- Intensified

On monochrome 3270 series terminals, the display was green or bright green on a dark background.

## Adding color

### Four color displays

Four color models mapped colors to attributes thusly:

|             | normal | intensified |
| ----------- | ------ | ----------- |
| protected   | blue   | white       |
| unprotected | green  | red         |

### Seven color displays

More advanced models offered seven colors and additional attributes:

The colors:

- White
- Red
- Blue
- Green (default)
- Pink (magenta)
- Yellow
- Turquoise (cyan)

The additional attributes:

- Blinking
- Reversed
- Underscored
- Outlined

## Theming in Helix

My Helix themes will use monochrome green/amber/white predominately, with some shading. There are enough useful UI features of Helix to warrant using more colors, but they will be limited to the framing UI. Source code/text will use the predominate color, some shading, and italics.

Red and yellow are often used for errors and warnings.

Reverse video is used for the cursor and some selections. There outlining or blinking text.
